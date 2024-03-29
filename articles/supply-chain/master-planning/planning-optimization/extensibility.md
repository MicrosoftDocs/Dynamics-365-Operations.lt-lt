---
title: Planavimo optimizavimo išplečiamumas
description: Šiame straipsnyje aprašomi extensibility scenarijai, kurie palaikomi planavimo optimizavime.
author: t-benebo
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 7d649110959e6bcfdaeb32dd53c55dbc446ed1be
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857550"
---
# <a name="planning-optimization-extensibility"></a>Planavimo optimizavimo išplečiamumas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašomi extensibility scenarijai, susiję su pagrindiniu planavimu ir palaikomi planavimo optimizavime. Šios debesų kompiuterijos ieškos galimybės prieinamos „Microsoft Dynamics 365 Supply Chain Management“ versijoje 10.0.13.

## <a name="custom-processing-when-master-planning-is-completed"></a>Pasirinktinis apdorojimas, kai bendrasis planavimas baigtas

Dažniausiai „Planning Optimization“ scenarijuje pasirinktinis apdorojimas atliekamas atnaujinus planą. Pavyzdžiui, galite įtraukti stulpelį į suplanuotų užsakymų lentelę arba galite norėti iš sugeneruoto plano gauti (`ReqPO`) tam tikrą statistinę informaciją. Pagrindinis išorinis taškas, įgalinęs šiuos `jobCompletedSuccessfully` scenarijus, yra klasės `MpsMasterPlanningEvents` metodas.

```X++
public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
```

Čia pateikiamas plėtinio, kuris nustato pasirinktinį `CstmOrderPriority` lauką suplanuotoje užsakyme, pavyzdys.

```X++
[ExtensionOf(classStr(MpsMasterPlanningEvents))]
public static final class MpsMasterPlanningEvents_Cstm_Extension
{
    public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
    {
        ttsbegin;

        var affectedPlannedOrdersQuery = _args.parmPostProcessingQueryBuilder().buildAffectedPlannedOrdersQuery();
        var affectedPlannedOrdersQueryRun = new QueryRun(affectedPlannedOrdersQuery);

        while (affectedPlannedOrdersQueryRun.next())
        {
            ReqPO reqPO = affectedPlannedOrdersQueryRun.get(tableNum(ReqPO));
            reqPO.selectForUpdate(true);
            reqPO.CstmOrderPriority = reqPO.ReqDate - systemDateGet() < 7 ? CstmPlannedOrderPriority::Urgent : CstmPlannedOrderPriority::Regular;
            reqPO.doUpdate();
        }

        ttscommit;

        next jobCompletedSuccessfully(_args);
    }

}
```

Įtraukdami pasirinktinę logiką, atsižvelkite į šiuos apribojimus ir geriausią praktiką:

- Metodas `jobCompletedSuccessfully` iškviestas už operacijos apimties ribų. Todėl, kai pradeda veikti pasirinktinė logika, planas jau matomas vartotojui. Jei jūsų tinkinimas nustato papildomus suplanuotų užsakymų laukus, svarbu žinoti, kad tų laukų vertės galiausiai bus nuoseklios (kitaip tariant, baigus planavimo užduotį jos gali būti pasibaigęs iš karto).
- Iškvietus metodą galima pradėti `jobCompletedSuccessfully` kitą bendrojo planavimo užduotį. Nauja užduotis gali paveikti visą planą arba plano dalį. Nauja užduotis gali atnaujinti arba panaikinti tuos pačius suplanuotus užsakymus arba poreikio operacijas, kurios buvo sukurtos arba atnaujintos kaip planavimo užduoties, kuri buvo apdorota, dalis `jobCompletedSuccessfully`. Atnaujinimo nesuderinamumo išimtys turi būti tvarkomos ištęsus šį įvykį.
- Kai išplečiate šį metodą, venkite naudoti vieną operacijos aprėptį. Vienas bendrojo planavimo vykdymas gali sukurti milijonai poreikio operacijų ir šimtų suplanuotų užsakymų. Jei visos šios operacijos ir suplanuoti užsakymai apdorojami vienos operacijos aprėtus, daug SQL užraktų bus ir užblokuos kitus planavimo procesus. Be to, jei operacija vyksta ilgai, SQL duomenų bazėje bus sukurti „sql" įrašai. Kiekvieno proceso sistemoje įrašai turės neigiamos įtakos.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]