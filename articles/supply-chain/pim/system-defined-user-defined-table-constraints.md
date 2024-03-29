---
title: Pagal sistemas arba vartotojus nustatyti lentelės apribojimai
description: Šiame straipsnyje aprašomi du lentelės apribojimų, skirtų komponentams produktų konfigūravimo modelyje, tipai – apibrėžti vartotojo ir apibrėžti sistemos. Lentelės apribojimai – tai leistinų atributų derinių matricos, kurių kiekvienoje eilutėje apibrėžiamas vienas galimų atributų reikšmių rinkinys.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c4b484c99bc8f1cc830d4177460ec15a26714a56
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577389"
---
# <a name="system-defined-and-user-defined-table-constraints"></a>Pagal sistemas arba vartotojus nustatyti lentelės apribojimai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomi du lentelės apribojimų, skirtų komponentams produktų konfigūravimo modelyje, tipai – apibrėžti vartotojo ir apibrėžti sistemos. Lentelės apribojimai – tai leistinų atributų derinių matricos, kurių kiekvienoje eilutėje apibrėžiamas vienas galimų atributų reikšmių rinkinys.

Lentelės apribojimai nurodo produkto konfigūracijos modelyje leidžiamų komponentų atributų derinių matricas. Kiekviena eilutė lentelėje nurodo vieną galimų atributų reikšmių rinkinį. Produkto konfigūracijos modelyje galite nurodyti dviejų toliau nurodytų tipų apribojimus.

-   **Išraiškos apribojimas** – kurkite išraišką, kuri apibrėžia atributų ryšius, siekdami užtikrinti, kad prekės konfigūravimo metu būtų galima pasirinkti tik suderinamas reikšmes.
-   **Lentelės apribojimas** – kurkite lentelę, kuri nurodo visus leidžiamus konkretaus atributų rinkinio derinius. Galima naudoti dviejų tipų lentelės apribojimus: vartotojo nustatytus lentelės apribojimus ir sistemos nustatytus lentelės apribojimus.

Šiame straipsnyje aprašomi vartotojo ir sistemos nustatyti lentelės apribojimai, skirti komponentams produktų konfigūravimo modelyje.

## <a name="user-defined-table-constraints"></a>Vartotojo nustatyti lentelės apribojimai
Vartotojo nustatytas lentelės apribojimas yra matricos tipas, naudojamas atributų reikšmių, kurias apibrėžia atributo tipas, deriniams apibūdinti. Pavyzdžiui, jei gaminate garsiakalbius, į vartotojo nustatytą lentelės apribojimą galite įtraukti spintelės apdailos ir priekinių grotelių stulpelius. Spintelės apdailos atributo tipas gali turėti keturias reikšmes, o priekinių grotelių atributo tipas gali turėti tris reikšmes. Todėl, jei apribojimai nėra taikomi, galimų derinių skaičius yra 4 × 3 = 12. Tačiau pagal šį pavyzdį galima naudoti tik šešis derinius, kaip parodyta toliau pateiktoje lentelėje. Ši informacija rodoma puslapio **Redaguoti lentelės apribojimą** skirtuke **Leistini deriniai**.

| Spintelės apdaila | Priekinės grotelės |
|----------------|-------------|
| Juoda          | Juoda       |
| Juoda          | Metalo       |
| Ąžuolo            | Juoda       |
| Raudonmedžio       | Balta       |
| Balta          | Juoda       |
| Balta          | Balta       |

Vartotojo nustatytus lentelės apribojimus apibrėžia statinė lentelės įvestis, kuri veikia taip pat, kaip išraiškos apribojimas. Privalumas naudojant vartotojo nustatytą lentelės apribojimą yra tai, kad dažnai lengviau kurti, suprasti ir prižiūrėti lenteles, o ne ilgis išraiškos apribojimus.

## <a name="system-defined-table-constraints"></a>Sistemos nustatyti lentelės apribojimai
Sistemos nustatytas lentelės apribojimas sukuria dinaminį susiejimą tarp atributo tipo ir lauko lentelėje. Kai sistemos nustatytas lentelės apribojimas įtraukiamas į produkto konfigūracijos modelį, susiejimas garantuoja, bus rodomi lentelės duomenys, o ne atributo tipo reikšmės. Rezultatas yra dinaminis apribojimas, nes lentelės turinį galima modifikuoti (pvz., naudojant kitus modulius).  

Kurdami sistemos nustatytą lentelės apribojimą, turite pasirinkti lentelę, pasirinktinai nustatyti naudotiną užklausą, o tada atributų tipus susieti su pasirinktos lentelės laukais. Laukų tipai turi atitikti atributų tipus .  

Prieš lentelių apribojimus įsigaliojant produkto konfigūracijos modelio komponentui, lentelių apribojimą reikia įtraukti į vieną iš modelio komponentų. Ši procedūra skirta sukurti naują apribojimą, pasirinkite lentelės apribojimo tipą, tada pasirinkite lentelės apribojimo apibrėžimą, kurį naudosite. Galiausiai visus lentelės apribojimo laukus turite susieti su atributais produkto konfigūracijos modelyje.

## <a name="additional-resources"></a>Papildomi ištekliai

[Produkto konfigūracijos modelių apžvalga](product-configuration-models.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]