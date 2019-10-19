---
title: Prekiaujančių subjektų rūšiavimo tvarkos keitimas
description: Šioje temoje paaiškinama koncepcija, kuri yra susijusi su įvairių su prekyba susijusių subjektų rodymo tvarkos valdymu Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c159ff869d6c504fdebbef1fa68115a410c81d85
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/24/2019
ms.locfileid: "2019421"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Prekiaujančių subjektų rūšiavimo tvarkos keitimas


[!include [banner](includes/banner.md)]

Mažmenininkai produkto atradimą laiko pirminiu įrankiu, skirtu bendrauti su klientais visuose mažmeninės prekybos kanaluose. Įvairios funkcijos gali padėti klientams lengviau atrasti produktus. Pavyzdžiui, jie gali naršyti po kategorijas, ieškoti ir filtruoti.

Šioje temoje paaiškinama koncepcija, kuri yra susijusi su įvairių su prekyba susijusių subjektų rodymo tvarkos valdymu. Čia taip pat aiškinama, kaip pakeisti rūšiavimo tvarką.

## <a name="overview"></a>Apžvalga

Patobulinta įvairių su prekybą susijusių subjektų rūšiavimo pagalba. Ši pagalba dabar geriau suderinta su esamais klientų scenarijais, kuriems seniau reikėjo plėtinių iš diegimo partnerių.

Senesnėse nei 10.0.5 „Retail” versijose kategorijų rūšiavimas naršymo hierarchijoje buvo alfabetinis. Naujos pasirinktinės rūšiavimo tvarkos funkcijos leidžia prekybos vadybininkams konfigūruoti įvairių su prekyba susijusių subjektų tvarką visuose galutiniuose klientuose. Šiuos klientus sudaro centrinės būstinės (HQ) ir skambučių centrai.

## <a name="configure-the-display-order-for-categories-in-the-retail-product-hierarchy"></a>Kategorijų mažmeninės prekybos produktų hierarchijoje rodymo tvarkos konfigūravimas

Prieš baigdami šią procedūrą, savo aplinkoje turi įdiegti demonstracinius duomenis.

1. Eikite į **Mažmeninė prekyba \> Produktai ir kategorijos \> Mažmeninės prekybos produktų hierarchija**.
2. Spustelėkite **Redaguoti kategorijos hierarchiją**.
3. Spustelėkite **Redaguoti**.
4. Medyje išplėskite **VISI \> Veiksmo sportas**.
5. Medyje išplėskite **VISI \> Komandinis sportas**.
6. Lauke **Rodymo tvarka** įveskite skaičių. (Skaičius gali būti neigiamas)
7. Bet kuriai papildomai kategorijai, kurios tvarką norite pakeisti, pakartokite 4–6 veiksmus.

Kanalų naršymo hierarchijos rodymo tvarka atsispindės mažmeninės prekybos produktų hierarchijos HQ ir pagal kategoriją išleistuose produktuose.

![Mažmeninės prekybos produktų hierarchijos pasirinktinis rūšiavimas su neigiamomis reikšmėmis](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Pagal kategoriją išleistų produktų pasirinktinis rūšiavimas pagal mažmeninės prekybos produktų hierarchiją](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>Kategorijų kanalo naršymo hierarchijoje rodymo tvarkos konfigūravimas

Prieš baigdami šią procedūrą, savo aplinkoje turi įdiegti demonstracinius duomenis.

1. Eikite į **Mažmeninė prekyba \> Produktai ir kategorijos \> Kanalo naršymo kategorijos**.
2. Sąraše pažymėkite hierarchiją **Mados naršymas**.
3. Spustelėkite **Redaguoti kategorijos hierarchiją**.
4. Spustelėkite **Redaguoti**.
5. Medyje pažymėkite **Mada \> Drabužiai moterims \> Batai moterims**.
6. Lauke **Rodymo tvarka** įveskite skaičių.
7. Medyje pažymėkite **Mada \> Drabužiai moterims \> Viršutiniai drabužiai**.

    Panašiai galite apibrėžti rūšiavimo tvarką antrinėse kategorijose.

8. Medyje pažymėkite **Mada \> Drabužiai vyrams \> Laisvalaikio marškinėliai**.
9. Lauke **Rodymo tvarka** įveskite skaičių.
10. Medyje pažymėkite **Mada \> Drabužiai vyrams \> Paltai ir švarkai**.
11. Lauke **Rodymo tvarka** įveskite skaičių.
12. Šiuos veiksmus pakartokite bet kuriai papildomai kategorijai, kurios tvarką norite pakeisti.

Kanalo naršymo hierarchijos rodymo tvarka atsispindi HQ, kataloge ir mažmeninės prekybos kanaluose.

![Kanalo naršymo hierarchijos pasirinktinis rūšiavimas](./media/ChannelNavCustomSorted.png)

![Katalogo naršymo hierarchijos pasirinktis rūšiavimas pagal kanalo naršymo hierarchiją](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS su pasirinktai surūšiuotomis kategorijomis](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> Pagal numatytuosius parametrus, pasirinktinio rūšiavimo tvarka yra išjungta. Kaip įjungti šią funkciją ir kitas funkcijas, žr. [Funkcijų valdymas](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).
