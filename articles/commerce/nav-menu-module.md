---
title: Naršymo meniu modulis
description: Šioje temoje aprašomi naršymo meniu moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 91239bd1db3f5819b7ad8d45ccfd8ab0d88b1b41
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817879"
---
# <a name="navigation-menu-module"></a>Naršymo meniu modulis

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šioje temoje aprašomi naršymo meniu moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūra

Pagrindinė naršymo meniu modulių paskirtis yra leisti svetainių vartotojams naršyti produktus ir svetainių puslapius pagal kanalo naršymo hierarchiją, nustatytą „Dynamics 365 Commerce Headquarters”. Naršymo meniu modulyje sukonfigūruotos prekės rodomos kaip svetainės antraštės naršymo elementai. Naršymo meniu moduliai taip pat palaiko statinius meniu elementus, kurie susieti su kitais „e-Commerce” svetainės puslapiais.

Naršymo meniu modulį galima įtraukti į puslapio antraštės modulį. „Fabrikam” temos naršymo meniu pagal numatytuosius nustatymus pateikiami du lygiai. Darbo pradžios temos naršymo meniu pagal numatytuosius nustatymus pateikiami trys lygiai. Norint pakeisti lygių skaičių, temoje reikalingas peržiūros plėtinys.

Toliau pateiktoje iliustracijoje parodytas „Fabrikam” svetainės naršymo meniu pavyzdys, kuriame yra du kategorijų hierarchijos lygiai ir keli statiniai meniu elementai.
![Naršymo meniu modulio pavyzdys](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>Naršymo meniu modulio ypatybės

| Ypatybės pavadinimas             | Reikšmė                 | Aprašas |
|---------------------------|-----------------------|-------------|
| Šaltinis                  | **„Retail”** , **Kūrimas neautomatiniu būdu** , **„Retail” ir kūrimas neautomatiniu būdu** | Reikšmė **„Retail”** leidžia naršymo meniu rodyti „Commerce Headquarters” kanalų naršymo hierarchiją. Reikšmė **Kūrimas neautomatiniu būdu** leidžia kuruoti statinius meniu elementus. Reikšmė **„Retail” ir kūrimas neautomatiniu būdu** leidžia abiejų reikšmių derinį. |
| Rodyti kategorijos vaizdus | **Teisinga** arba **Klaidinga**    | Įjungus Ši ypatybė naršymo meniu rodo kategorijos atvaizdus, kaip nurodyta kiekvienos kategorijos "Commerce Headquarters". Įtraukta į „Commerce” 10.0.14 leidimą. |
| Statinis meniu elementas| Reikšmių masyvas| Statiniai meniu elementai, susiejantys meniu elemento pavadinimą su statinio svetainės puslapio saitu. Galite kurti meniu elementus po kitais meniu elementais. Pagal numatytuosius nustatymus statiniai meniu rodomi šakniniame lygyje ir yra pridedami prie kanalų naršymo hierarchijos, jei tokia yra. |

Toliau pateiktame paveikslėlyje parodytas kategorijos vaizdo, rodomo „Fabrikam“ svetainės naršymo meniu, pavyzdys.
![Naršymo meniu modulio su kategorijos vaizdais pavyzdys](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>Naršymo meniu modulio įtraukimas į antraštės modulį

Daugiau informacijos apie tai, kaip įtraukti naršymo meniu modulį į antraštės modulį, žr. [Antraštės modulis](author-header-module.md) .

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos apžvalga](starter-kit-overview.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Slapukų atitiktis](cookie-compliance.md)

[Antraštės modulis](author-header-module.md)
