---
title: Naršymo meniu modulis
description: Šioje temoje aprašomi naršymo meniu moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b112bb453e0840120c63038bf8d6897fbf5ff288
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798758"
---
# <a name="navigation-menu-module"></a>Naršymo meniu modulis

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi naršymo meniu moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

Pagrindinė naršymo meniu modulių paskirtis yra leisti svetainių vartotojams naršyti produktus ir svetainių puslapius pagal kanalo naršymo hierarchiją, nustatytą „Dynamics 365 Commerce Headquarters”. Naršymo meniu modulyje sukonfigūruotos prekės rodomos kaip svetainės antraštės naršymo elementai. Naršymo meniu moduliai taip pat palaiko statinius meniu elementus, kurie susieti su kitais „e-Commerce” svetainės puslapiais.

Naršymo meniu modulį galima įtraukti į puslapio antraštės modulį. „Fabrikam” temos naršymo meniu pagal numatytuosius nustatymus pateikiami du lygiai. Darbo pradžios temos naršymo meniu pagal numatytuosius nustatymus pateikiami trys lygiai. Norint pakeisti lygių skaičių, temoje reikalingas peržiūros plėtinys.

Toliau pateiktoje iliustracijoje parodytas „Fabrikam” svetainės naršymo meniu pavyzdys, kuriame yra du kategorijų hierarchijos lygiai ir keli statiniai meniu elementai.
![Naršymo meniu modulio pavyzdys](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>Naršymo meniu modulio ypatybės

| Ypatybės pavadinimas             | Reikšmė                 | Aprašas |
|---------------------------|-----------------------|-------------|
| Šaltinis                  | **„Retail”** , **Kūrimas neautomatiniu būdu** , **„Retail” ir kūrimas neautomatiniu būdu** | Reikšmė **„Retail”** leidžia naršymo meniu rodyti „Commerce Headquarters” kanalų naršymo hierarchiją. Reikšmė **Kūrimas neautomatiniu būdu** leidžia kuruoti statinius meniu elementus. Reikšmė **„Retail” ir kūrimas neautomatiniu būdu** leidžia abiejų reikšmių derinį. |
| Rodyti kategorijos vaizdus | **Teisinga** arba **Klaidinga**    | Įjungus Ši ypatybė naršymo meniu rodo kategorijos atvaizdus, kaip nurodyta kiekvienos kategorijos "Commerce Headquarters". Įtraukta į „Commerce” 10.0.14 leidimą. |
| Rodyti akcijas | **Teisinga** arba **Klaidinga** | Kai ypatybė yra įjungta, akcijos gali būti konfigūruojamos naudojant paveikslėlius, nuorodas ir tekstą. Ši ypatybė buvo įtraukta į „Commerce“ versijos 10.0.17 leidimą. |
| Įtraukti akcijas | Tekstas, paveikslėlis ar nuoroda | Kai **Rodyti akcijas** ypatybė yra įjungta, galite įtraukti tekstą, paveikslėlį ar nuorodą kaip akcijos turinį naršymo meniu. |
| Įjungti kelių lygių naršymo meniu | **Teisinga** arba **Klaidinga** | Kai ši ypatybė įjungta, naršymo meniu gali rodyti kelis naršymo hierarchijos lygius. Ši funkcija yra prieinama „Commerce“ versijos 10.0.15 leidime. |
| Lygių skaičius | sveikasis skaičius | Ši ypatybė nurodo lygių, kurie turėtų būti rodomi, jei ypatybė **Įjungti kelių lygių naršymo meniu** nustatyta į **Teisinga**, skaičių. |
| Statinis meniu elementas| Reikšmių masyvas| Statiniai meniu elementai, susiejantys meniu elemento pavadinimą su statinio svetainės puslapio saitu. Galite kurti meniu elementus po kitais meniu elementais. Pagal numatytuosius nustatymus statiniai meniu rodomi šakniniame lygyje ir yra pridedami prie kanalų naršymo hierarchijos, jei tokia yra. |
| Rodyti šakninį meniu | **Teisinga** arba **Klaidinga** | Kai ši ypatybė įjungta, naršymo meniu gali būti nustatytas pagal pasirinktinę šaknį (pvz., **Pirkti dabar**). Ši funkcija pasiekiama „Dynamics 365 Commerce“ 10.0.15 leidime. |
| Šakninis meniu | eilutė | Ši ypatybė gali būti naudojama norint nustatyti pasirinktinės šaknies tekstą, jei ypatybė **Rodyti šakninį meniu** nustatyta į **Teisinga**. |

Toliau pateiktame paveikslėlyje parodytas kategorijos vaizdo, rodomo „Fabrikam“ svetainės naršymo meniu, pavyzdys.
![Naršymo meniu modulio su kategorijos vaizdais pavyzdys](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>Naršymo meniu modulio įtraukimas į antraštės modulį

Daugiau informacijos apie tai, kaip įtraukti naršymo meniu modulį į antraštės modulį, žr. [Antraštės modulis](author-header-module.md) .

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[Naršymo kelio modulis](add-breadcrumb.md)

[Svetainės išrinkiklio modulis](site-selector.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Slapukų atitiktis](cookie-compliance.md)

[Antraštės modulis](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
