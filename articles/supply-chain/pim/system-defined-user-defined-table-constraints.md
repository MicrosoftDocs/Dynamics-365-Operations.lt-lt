---
title: "Pagal sistemas arba vartotojus nustatyti lentelės apribojimai"
description: "Šiame straipsnyje aprašomi du lentelės apribojimų, skirtų komponentams produktų konfigūravimo modelyje, tipai – apibrėžti vartotojo ir apibrėžti sistemos. Lentelės apribojimai – tai leistinų atributų derinių matricos, kurių kiekvienoje eilutėje apibrėžiamas vienas galimų atributų reikšmių rinkinys."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 4da560ca3cce5a28edd2a00506f825d5d88ef0f3
ms.contentlocale: lt-lt
ms.lasthandoff: 02/07/2018

---

# <a name="system-defined-and-user-defined-table-constraints"></a>Pagal sistemas arba vartotojus nustatyti lentelės apribojimai

[!INCLUDE [banner](../includes/banner.md)]

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

Prieš lentelių apribojimus įsigaliojant produkto konfigūracijos modelio komponentui, lentelių apribojimą reikia įtraukti į vieną iš modelio komponentų. Ši procedūra skirta sukurti naują apribojimą, pasirinkite lentelės apribojimo tipą, tada pasirinkite lentelės apribojimo apibėžimą, kurį naudosite. Galiausiai visus lentelės apribojimo laukus turite susieti su atributais produkto konfigūracijos modelyje.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Pagrindinės produkto konfigūracijos modelių koncepcijos](product-configuration-models.md)




