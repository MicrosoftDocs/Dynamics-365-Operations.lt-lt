---
title: Prekiaujančių subjektų rūšiavimo tvarkos keitimas
description: Šiame straipsnyje paaiškinamos koncepcijos, susijusios su įvairių su preke susijusių objektų rodymo tvarka Dynamics 365 Commerce.
author: josaw1
ms.date: 08/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 80586597f4f60476b341e4cf1cfd90f3681e15c0
ms.sourcegitcommit: 52e31b1ef2b3ed8675de931d06090cd57e057fc2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9265842"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Prekiaujančių subjektų rūšiavimo tvarkos keitimas


[!Include [banner](includes/banner.md)]

Pardavėjai produktų atradimą laiko pirminiu įrankiu, skirtu bendrauti su klientais visuose kanaluose. Yra keletas priemonių, kurios gali padėti klientams lengvai atrasti produktus. Pavyzdžiui, klientai gali naršyti kategorijas, ieškoti ir filtruoti.

Šiame straipsnyje paaiškinamos koncepcijos, susijusios su įvairių su preke susijusių objektų rodymo tvarka. Čia taip pat aiškinama, kaip pakeisti rūšiavimo tvarką.

## <a name="overview"></a>Apžvalga

Commerce rūšiuojant įvairius su atributais susijusius objektus sulygiuojami su esamais kliento scenarijais ir nebereikia diegimo partnerių plėtinių.

Naudojant "Commerce" 10.0.5 ir ankstesnes versijas, kategorijų rūšiavimo tvarka naršymo hierarchijoje buvo abėcėlės tvarka. Esama pasirinktinio rūšiavimo tvarkos funkcija leidžia prekybos vadovams konfigūruoti įvairių su preke susijusių subjektų rūšiavimo tvarką visuose galutiniame vartotojo klientuose. Šiuos klientus sudaro centrinės būstinės (HQ) ir skambučių centrai.

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a>Produktų hierarchijos kategorijų rodymo tvarkos konfigūravimas

Prieš baigdami šią procedūrą, savo aplinkoje turi įdiegti demonstracinius duomenis.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Prekybos produktų hierarchija**.
2. Spustelėkite **Redaguoti kategorijos hierarchiją**.
3. Spustelėkite **Redaguoti**.
4. Medyje išplėskite **VISI \> Veiksmo sportas**.
5. Medyje išplėskite **VISI \> Komandinis sportas**.
6. Lauke **Rodymo tvarka** įveskite skaičių. (Skaičius gali būti neigiamas)
7. Bet kuriai papildomai kategorijai, kurios tvarką norite pakeisti, pakartokite 4–6 veiksmus.

Kanalo naršymo hierarchijos rodymo tvarka atsispindės prekybos produktų hierarchijos HQ ir pagal kategoriją išleistuose produktuose.

![Produktų hierarchijos pasirinktinis rūšiavimas su neigiamomis reikšmėmis.](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Pagal kategoriją išleistų produktų pasirinktinis rūšiavimas pagal produktų hierarchiją.](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>Kategorijų kanalo naršymo hierarchijoje rodymo tvarkos konfigūravimas

Prieš baigdami šią procedūrą, savo aplinkoje turi įdiegti demonstracinius duomenis.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Kanalo naršymo kategorijos**.
2. Sąraše pažymėkite hierarchiją **Mados naršymas**.
3. Spustelėkite **Redaguoti kategorijos hierarchiją**.
4. Spustelėkite **Redaguoti**.
5. Medyje pasirinkite Madingos **\> moterys moters \> rūbais**.
6. Lauke **Rodymo tvarka** įveskite skaičių.
7. Medyje pažymėkite **Mada \> Drabužiai moterims \> Viršutiniai drabužiai**.

Taip pat galite nustatyti subkategorijų rūšiavimo tvarką.

8. Medyje pažymėkite **Mada \> Drabužiai vyrams \> Laisvalaikio marškinėliai**.
9. Lauke **Rodymo tvarka** įveskite skaičių.
10. Medyje pažymėkite **Mada \> Drabužiai vyrams \> Paltai ir švarkai**.
11. Lauke **Rodymo tvarka** įveskite skaičių.
12. Šiuos veiksmus pakartokite bet kuriai papildomai kategorijai, kurios tvarką norite pakeisti.

Kanalo naršymo hierarchijos rodymo tvarka atsispindi HQ, kataloge ir kanaluose.

![Kanalo naršymo hierarchijos pasirinktinis rūšiavimas.](./media/ChannelNavCustomSorted.png)

![Katalogo naršymo hierarchijos pasirinktis rūšiavimas pagal kanalo naršymo hierarchiją.](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS su pasirinktai surūšiuotomis kategorijomis.](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> Pagal numatytuosius nustatymus **funkcija Įgalinti prekybos objektų** rodymo užsakymą išjungta. Funkcijų [valdymą naudokite](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), norėdami jį įjungti. Sureguliuoę funkciją iš paskirstymo grafiko **paleiskite visuotinę konfigūraciją -1110** CDX užduotį.
> Jei jūsų kategorijų užsakymas EKA nėra atnaujintas, iš naujo suaktyvinkite įrenginį. Kategorijos informacija surenkama, kai vyksta įrenginio aktyvinimas, todėl įrenginiui gali reikėti atsisakyti kategorijos informacijos naudojant atnaujintus rodymo užsakymus. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
