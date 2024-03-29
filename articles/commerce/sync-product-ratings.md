---
title: „Dynamics 365 Commerce“ produktų įvertinimų sinchronizavimas
description: Šiame straipsnyje aprašoma, kaip sinchronizuoti produkto įvertinimus Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 7946bcaa9c6f318115640c6b20b00554a117dd38
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282029"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a>„Dynamics 365 Commerce“ produktų įvertinimų sinchronizavimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip sinchronizuoti produkto įvertinimus Microsoft Dynamics 365 Commerce.

Norint produktų įvertinimus naudoti daugiakanaliuose, pvz., elektroniniame kasos aparate (EKA) ir skambučių centruose, produktų įvertinimus iš vertinimų ir atsiliepimų paslaugos reikia importuoti į „Commerce“ kanalo duomenų bazę. Kai produktų įvertinimai pateikiami daugiakanaliuose, jie gali netiesiogiai padėti klientams bendraujant su pardavimo darbuotojais.

Šiame straipsnyje aprašomos šios užduotys:

1. Konfigūruokite **Produkto įvertinimų sinchronizavimo užduotį** kaip paketinę užduotį, kad galėtumėte sinchronizuoti produktų įvertinimus iš **Vertinimų ir atsiliepimų paslaugos**.
1. Patikrinkite, ar produkto vertinimų sinchronizavimo paketinė užduotis sėkmingai įvykdyta.
1. Produkto įvertinimus pateikite EKA.

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a>Paketinės užduoties konfigūravimas produkto įvertinimams sinchronizuoti

> [!IMPORTANT]
> Prieš pradėdami įsitikinkite, kad įdiegta „Dynamics 365 Commerce“ 10.0.6 arba naujesnė versija.

### <a name="initialize-the-commerce-scheduler"></a>Prekybos planuoklės inicijavimas

Norėdami inicijuoti prekybos planuoklę, atlikite toliau nurodytus veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Būstinės sąranka \> Prekybos planuoklė \> Inicijuoti prekybos planuoklę**. Taip pat galite ieškoti „Inicijuoti prekybos planuoklę“.
1. Dialogo lange **Inicijuoti prekybos planuoklę** patikrinkite, ar parinktis **Naikinti esamą konfigūraciją** nustatyta kaip **Ne**, tada pasirinkite **Gerai**.

### <a name="verify-the-retailproductrating-subjob"></a>Antrinės užduoties „RetailProductRating“ tikrinimas

Norėdami patikrinti, ar yra antrinė užduotis **RetailProductRating**, atlikite toliau nurodytus veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Būstinės sąranka \> Prekybos planuoklė \> Duomenų apsikeitimo valdymo antrinės užduotys**. Taip pat galite ieškoti „duomenų apsikeitimo valdymo antrinės užduotys“.
1. Antrinių užduočių sąraše raskite antrinę užduotį **RetailProductRating** arba jos ieškokite.

Toliau pateiktoje iliustracijoje rodomas išsamios antrinės užduoties informacijos programoje „Commerce“ pavyzdys.

![Išsami antrinės užduoties „RetailProductRating“ informacija.](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> Jeigu antrinės užduoties **RetailProductRating** nerandate, galbūt užduotį **Produkto įvertinimų sinchronizavimas** ir užduotį **1040 CDX** įvykdėte prieš inicijuodami „Commerce” planuoklę. Tokiu atveju atlikite toliau nurodytus veiksmus, kad vykdytumėte užduotį **Visas duomenų sinchronizavimas**.

> 1. Eikite į **Mažmeninė prekyba ir prekyba \> Būstinės sąranka \> Prekybos planuoklė \> Kanalo duomenų bazė**. Taip pat galite ieškoti „kanalo duomenų bazė“.
> 1. Pasirinkite kanalo duomenų bazę, kurią norite sinchronizuoti.
> 1. Veiksmų srityje pasirinkite **Visas duomenų sinchronizavimas**.
> 1. Išskleidžiamajame dialogo lange **Pasirinkti paskirstymo grafiką** pasirinkite **1040 – produktai**, tada pasirinkite **Gerai**.
> 1. Pakartokite pirmesnės procedūros veiksmus, kad patikrintumėte, ar buvo sukurta antrinė užduotis **RetailProductRating**.

### <a name="import-product-ratings"></a>Produkto įvertinimų importavimas

Norėdami produkto įvertinimus iš įvertinimų ir atsiliepimų tarnybos importuoti į „Commerce”, atlikite toliau nurodytus veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Valdymo sąranka \> Prekybos planuoklė \> Produkto įvertinimų sinchronizavimo užduotis**. Taip pat galite ieškoti „produkto įvertinimų sinchronizavimo užduotis“.
1. Dialogo lango **Gauti produkto įvertinimus** „FastTab“ **Vykdyti fone** pasirinkite **Pasikartojimas**.
1. Dialogo lange **Nustatyti pasikartojimą** nustatykite pasikartojimo modelį. (Siūloma reikšmė yra dvi valandos.) Neplanuokite pasikartojimo, kuris yra mažesnis nei viena valanda.
1. Pasirinkite **Gerai**.
1. Parinktį **Paketinis vykdymas** nustatykite į **Taip**. Šis parametras padeda užtikrinti, kad galėsite tikrinti žurnalus ir paketinių užduočių vykdymo būseną.
1. Norėdami suplanuoti paketinę užduotį pasirinkite **Gerai**.

Toliau pateiktoje iliustracijoje rodomas antrinės užduoties konfigūracijos programoje „Commerce“ pavyzdys.

![Produkto įvertinimų sinchronizavimo paketinės užduoties konfigūracija.](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a>Tikrinimas, ar produkto įvertinimų sinchronizavimo paketinė užduotis buvo sėkmingai įvykdyta

Norėdami patikrinti, ar paketinė užduotis **Produkto įvertinimų sinchronizavimas** buvo sėkmingai įvykdyta, atlikite toliau nurodytus veiksmus.

1. Eikite į dalį **Mažmeninė prekyba ir prekyba \> Sistemos administratorius \> Užklausos \> Paketinės užduotys**, arba, jei naudojate tik prekybos sandėliavimo vienetą (SKU), eikite į dalį **Mažmeninė prekyba ir prekyba \> Užklausos ir ataskaitos \> Paketinės užduotys**. Taip pat galite ieškoti „paketinės užduotys“.
1. Norėdami peržiūrėti išsamią paketinės užduoties informaciją, paketinių užduočių sąrašo stulpelyje **Užduoties aprašymas** ieškokite aprašymo, kuriame yra „Gauti produkto įvertinimus“.
1. Pasirinkite užduoties ID, kad peržiūrėtumėte išsamią paketinės užduoties informaciją, pvz., suplanuotą pradžios datą ir (arba) laiką ir pasikartojimo tekstą.

Toliau pateiktoje iliustracijoje parodytas išsamios paketinės užduoties informacijos programoje „Commerce“ pavyzdys, kai paketinė užduotis suplanuota vykdyti kas dvi valandas.

![Produkto įvertinimų sinchronizavimo paketinės užduoties išsami informacija.](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a>Produkto įvertinimų pateikimas EKA

„Dynamics 365 Commerce“ įvertinimų ir atsiliepimų sprendimas yra daugiakanalis sprendimas. Tačiau pagal numatytuosius nustatymus produktų įvertinimai EKA nerodomi. Norėdami, kad klientai parduotuvėse, kai juos aptarnauja pardavimo darbuotojai, matytų įvertinimus ir atsiliepimus, EKA turite įjungti produkto įvertinimus.

Norėdami EKA įjungti produkto įvertinimus, atlikite toliau nurodytus veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Prekybos sąranka \> Parametrai \> Commerce parametrai**. Taip pat galite ieškoti „Commerce“ parametrai“.
1. Skirtuke **Konfigūracijos parametrai** pasirinkite **Naujas**.
1. Įveskite pavadinimą, pavyzdžiui, **RatingsAndReviews.EnableProductRatingsForRetailStores** ir nustatykite reikšmę **teisinga**.
1. Pasirinkite **Įrašyti**.
1. Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**. Taip pat galite ieškoti „paskirstymo grafikas“.
1. Užduočių sąraše pasirinkite **1110** (**visuotinė konfigūracija**), tada pasirinkite **Vykdyti dabar**.
1. Sėkmingai įvykdžius užduotį patikrinkite, ar dabar produktų įvertinimai rodomi EKA.

Toliau pateiktame paveikslėlyje parodytas „Commerce“ parametrų konfigūracijos norint EKA įjungti produkto įvertinimus pavyzdys.

![„Commerce“ parametrų konfigūracijos norint EKA įjungti produkto įvertinimus pavyzdys.](media/rnr-hq-enable-ratings-in-pos.png)

Tolesnėje iliustracijoje pateikiamas produkto įvertinimų EKA pavyzdys.

![Produkto įvertinimai EKA.](media/rnr-pos-catalog-ratings.png)

Toliau pateiktoje iliustracijoje pateikiamas produkto įvertinimų skambučių centro kanaluose pavyzdys.

![Produkto įvertinimai skambučių centro kanale.](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Įvertinimų ir atsiliepimų apžvalga](ratings-reviews-overview.md)

[Norėdami naudoti įvertinimus ir atsiliepimus, prisijunkite](opt-in-ratings-reviews.md)

[Įvertinimų ir atsiliepimų tvarkymas](manage-reviews.md)

[Įvertinimų ir atsiliepimų konfigūravimas](configure-ratings-reviews.md)

[Produktų įvertinimų sinchronizavimas](sync-product-ratings.md)

[Neautomatinio vadovo įvertinimų ir apžvalgų publikavimo įjungimas](manual-publish-rating-reviews.md)

[Įvertinimų ir atsiliepimų importavimas ir eksportavimas](import-export-reviews.md)

[Ryšių tarp tarnybų autentifikavimo konfigūravimas](service-to-service-auth.md)

[DUK apie įvertinimus ir apžvalgas](ratings-reviews-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
