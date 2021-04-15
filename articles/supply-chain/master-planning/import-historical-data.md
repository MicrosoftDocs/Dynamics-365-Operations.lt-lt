---
title: Retrospektyvinių duomenų importavimas į poreikio prognozėms generuoti
description: Norint generuoti tikslias poreikio prognozes, reikia retrospektyvinių poreikio duomenų pagal prekę arba prekių paskirstymo raktą. Šioje temoje paaiškinama, kaip naudoti duomenų objektus norint importuoti retrospektyvinius poreikio duomenis iš bet kurios sistemos, kad turėtumėte ilgesnę poreikio prognozės duomenų retrospektyvą.
author: roxanadiaconu
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9bb3c178a698bdcd46e7c596247360ba9233b398
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816489"
---
# <a name="import-historical-data-for-demand-forecasts"></a>Retrospektyvinių duomenų importavimas į poreikio prognozėms generuoti

[!include [banner](../includes/banner.md)]

Norint užtikrinti poreikio prognozių tikslumą, jums reikia kiek įmanoma daugiau retrospektyvinių poreikio duomenų pagal prekę arba prekių paskirstymo raktą. Jei retrospektyviniai poreikio duomenys dar neimportuoti, importuokite juos naudodami „Dynamics 365 Supply Chain Management“ duomenų objektą **Retrospektyvinis išorinis poreikis** (ReqDemPlanHistoricalExternalDemandEntity).

Darbo srityje **Duomenų valdymas** galite peržiūrėti visų objekto laukų apžvalgą.

1. Atidarykite darbo sritį **Duomenų valdymas**.
2. Pasirinkite **Duomenų objektai** plytelę.
3. Objektų sąraše ieškokite objekto **Retrospektyvinis išorinis poreikis**.
4. Pasirinkite **Paskirties laukai**. Šie objekto laukai yra privalomi: teritorija (**DeliveringSiteId**), data (**DemandDate**), kiekis (**DemandQuantity**) ir prekės numeris (**ItemNumber**) arba prekių paskirstymo raktas (**ProductAllocationKeyId**).

Norint naudoti duomenų objektą, reikalingas „Microsoft Excel“ failas arba kableliais atskirtų verčių (CSV) failas, kuriame yra retrospektyviniai poreikio duomenys. Toliau pateikiamame pavyzdyje parodyta, kaip importuoti duomenis iš CSV failo.

Norėdami gauti daugiau informacijos apie duomenų importavimą, įskaitant duomenų valymą po importavimo, žiūrėkite [Duomenų importavimo ir eksportavimo užduočių apžvalga](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) ir susijusias temas.

## <a name="example"></a>Pavyzdys

Kaip pavyzdį galite naudoti toliau nurodytą failą. Atsisiųskite [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/). Šiame faile yra prekės D0001 retrospektyviniai poreikio duomenys. Jame yra tik šie privalomi laukai: teritorija, kiekis ir poreikio data.

1. Pasirinkite įmonę, į kurią norite importuoti į retrospektyvinius poreikio duomenis.
2. Atidarykite darbo sritį **Duomenų valdymas**.
3. Pasirinkite **Importuoti** plytelę.
4. Įveskite importavimo projekto pavadinimą, pavyzdžiui, **Prekės D0001 retrospektyvinio poreikio importavimas**.
5. Lauke **Šaltinio duomenų formatas** pasirinkite importuojamo failo formatą. Šiame pavyzdyje norėdami importuoti failą HistoricalDemandData, pvz., pasirinkite **CSV**.
6. Lauke **Objekto pavadinimas** pasirinkite **Retrospektyvinis išorinis poreikis**.
7. Įrašykite failą kompiuteryje ir tada jį įkelkite.
8. Pasirinkite **Importuoti**.
9. Automatiškai atidaromas puslapis **Vykdymo suvestinė**. Patikrinkite importuotus duomenis puslapyje.

Importavus retrospektyvinius poreikio duomenis, galima generuoti pagrindinę poreikio prognozę.

## <a name="additional-resources"></a>Papildomi ištekliai

[Pagrindinės statistinės prognozės generavimas](generate-statistical-baseline-forecast.md)  
[Duomenų importavimo ir eksportavimo užduočių apžvalga](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]