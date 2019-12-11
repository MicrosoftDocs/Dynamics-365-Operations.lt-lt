---
title: „Dynamics 365 Retail“ produktų įvertinimų sinchronizavimas
description: Šioje temoje aprašoma, kaip sinchronizuoti produktų įvertinimus naudojant „Microsoft Dynamics 365 Retail“.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: db5a4e1f78797d20ded2274cc99bef422fd50acc
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698170"
---
# <a name="sync-product-ratings-in-dynamics-365-retail"></a>„Dynamics 365 Retail“ produktų įvertinimų sinchronizavimas

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip sinchronizuoti produktų įvertinimus naudojant „Microsoft Dynamics 365 Retail“.

## <a name="overview"></a>Peržiūrėti

Norint produktų įvertinimus naudoti daugiakanaliuose, pvz., elektroniniame kasos aparate (EKA) ir skambučių centruose, produktų įvertinimus iš vertinimų ir atsiliepimų paslaugos reikia importuoti į „Retail“ kanalo duomenų bazę. Kai produktų įvertinimai pateikiami daugiakanaliuose, jie gali netiesiogiai padėti klientams bendraujant su pardavimo darbuotojais.

Šioje temoje aprašomos toliau nurodytos užduotys.

1. „Retail“ paketinės užduoties konfigūravimas produkto įvertinimams importuoti.
1. Patikrinkite, ar produkto vertinimų sinchronizavimo paketinė užduotis sėkmingai įvykdyta.
1. Produkto įvertinimus pateikite EKA.

## <a name="configure-a-retail-batch-job-to-import-product-ratings"></a>„Retail“ paketinės užduoties konfigūravimas produkto įvertinimams importuoti

> [!IMPORTANT]
> Prieš pradėdami įsitikinkite, kad įdiegta „Retail“ 10.0.6 arba naujesnė versija.

### <a name="initialize-the-retail-scheduler"></a>Duomenų apsikeitimo valdymo inicijavimas

Norėdami inicijuoti duomenų apsikeitimo valdymą, atlikite toliau nurodytus veiksmus.

1. Eikite į **Mažmeninė prekyba \> Valdymo sąranka \> Duomenų apsikeitimo valdymas \> Inicijuoti duomenų apsikeitimo valdymą**. Taip pat galite ieškoti „Inicijuoti duomenų apsikeitimo valdymą“.
1. Dialogo lange **Inicijuoti duomenų apsikeitimo valdymą** patikrinkite, ar parinktis **Naikinti esamą konfigūraciją** nustatyta kaip **Ne**, tada pasirinkite **Gerai**.

### <a name="verify-the-retailproductrating-subjob"></a>Antrinės užduoties „RetailProductRating“ tikrinimas

Norėdami patikrinti, ar yra antrinė užduotis **RetailProductRating**, atlikite toliau nurodytus veiksmus.

1. Eikite į **Mažmeninė prekyba \> Valdymo sąranka \> Duomenų apsikeitimo valdymas \> Duomenų apsikeitimo valdymo antrinės užduotys**. Taip pat galite ieškoti „duomenų apsikeitimo valdymo antrinės užduotys“.
1. Antrinių užduočių sąraše raskite antrinę užduotį **RetailProductRating** arba jos ieškokite.

Toliau pateiktoje iliustracijoje rodomas išsamios antrinės užduoties informacijos programoje „Retail“ pavyzdys.

![Išsami antrinės užduoties „RetailProductRating“ informacija](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> Jeigu antrinės užduoties **RetailProductRating** nerandate, galbūt užduotį **Produkto įvertinimų sinchronizavimas** ir užduotį **1040 CDX** įvykdėte prieš inicijuodami duomenų apsikeitimo valdymą. Tokiu atveju atlikite toliau nurodytus veiksmus, kad vykdytumėte užduotį **Visas duomenų sinchronizavimas**.
>
> 1. Eikite į **Mažmeninė prekyba \> Valdymo sąranka \> Duomenų apsikeitimo valdymas \> Kanalo duomenų bazė**. Taip pat galite ieškoti „kanalo duomenų bazė“.
> 1. Pasirinkite kanalo duomenų bazę, kurią norite sinchronizuoti.
> 1. Veiksmų srityje pasirinkite **Visas duomenų sinchronizavimas**.
> 1. Išskleidžiamajame dialogo lange **Pasirinkti paskirstymo grafiką** pasirinkite **1040 – produktai**, tada pasirinkite **Gerai**.
> 1. Pakartokite pirmesnės procedūros veiksmus, kad patikrintumėte, ar buvo sukurta antrinė užduotis **RetailProductRating**.

### <a name="import-product-ratings"></a>Produkto įvertinimų importavimas

Norėdami produkto įvertinimus iš įvertinimų ir atsiliepimų tarnybos importuoti į „Retail“, atlikite toliau nurodytus veiksmus.

1. Eikite į **Mažmeninė prekyba \> Valdymo sąranka \> Duomenų apsikeitimo valdymas \> Produkto įvertinimų sinchronizavimo užduotis**. Taip pat galite ieškoti „produkto įvertinimų sinchronizavimo užduotis“.
1. Dialogo lango **Gauti produkto įvertinimus** „FastTab“ **Vykdyti fone** pasirinkite **Pasikartojimas**.
1. Dialogo lange **Nustatyti pasikartojimą** nustatykite pasikartojimo modelį. (Siūloma reikšmė yra dvi valandos.) Neplanuokite pasikartojimo, kuris yra mažesnis nei viena valanda.
1. Pasirinkite **Gerai**.
1. Parinktį **Paketinis vykdymas** nustatykite į **Taip**. Šis parametras padeda užtikrinti, kad galėsite tikrinti žurnalus ir paketinių užduočių vykdymo būseną.
1. Norėdami suplanuoti paketinę užduotį pasirinkite **Gerai**.

Toliau pateiktoje iliustracijoje rodomas antrinės užduoties konfigūracijos programoje „Retail“ pavyzdys.

![Produkto įvertinimų sinchronizavimo paketinės užduoties konfigūracija](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a>Tikrinimas, ar produkto įvertinimų sinchronizavimo paketinė užduotis buvo sėkmingai įvykdyta

Norėdami patikrinti, ar paketinė užduotis **Produkto įvertinimų sinchronizavimas** buvo sėkmingai įvykdyta, atlikite toliau nurodytus veiksmus.

1. Eikite į dalį **Mažmeninė prekyba \> Sistemos administratorius \> Užklausos \> Paketinės užduotys**, arba, jei naudojate tik mažmeninės prekybos sandėliavimo vienetą (SKU), eikite į dalį **Mažmeninė prekyba \> Užklausos ir ataskaitos \> Paketinės užduotys**. Taip pat galite ieškoti „paketinės užduotys“.
1. Norėdami peržiūrėti išsamią paketinės užduoties informaciją, paketinių užduočių sąrašo stulpelyje **Užduoties aprašymas** ieškokite aprašymo, kuriame yra „Gauti produkto įvertinimus“.
1. Pasirinkite užduoties ID, kad peržiūrėtumėte išsamią paketinės užduoties informaciją, pvz., suplanuotą pradžios datą ir (arba) laiką ir pasikartojimo tekstą.

Toliau pateiktoje iliustracijoje parodytas išsamios paketinės užduoties informacijos programoje „Retail“ pavyzdys, kai paketinė užduotis suplanuota vykdyti kas dvi valandas.

![Produkto įvertinimų sinchronizavimo paketinės užduoties išsami informacija](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a>Produkto įvertinimų pateikimas EKA

„Dynamics 365 Commerce“ įvertinimų ir atsiliepimų sprendimas yra daugiakanalis sprendimas. Tačiau pagal numatytuosius nustatymus produktų įvertinimai EKA nerodomi. Norėdami, kad klientai parduotuvėse, kai juos aptarnauja pardavimo darbuotojai, matytų įvertinimus ir atsiliepimus, EKA turite įjungti produkto įvertinimus.

Norėdami EKA įjungti produkto įvertinimus, atlikite toliau nurodytus veiksmus.

1. Eikite į **Mažmeninė prekyba \> Mažmeninės prekybos sąranka \> Parametrai \> Mažmeninės prekybos parametrai**. Taip pat galite ieškoti „mažmeninės prekybos parametrai“.
1. Skirtuke **Konfigūracijos parametrai** pasirinkite **Naujas**.
1. Įveskite pavadinimą, pavyzdžiui, **RatingsAndReviews.EnableProductRatingsForRetailStores** ir nustatykite reikšmę **teisinga**.
1. Pasirinkite **Įrašyti**.
1. Eikite į **Mažmeninė prekyba \> Mažmeninės prekybos IT \> Paskirstymo grafikas**. Taip pat galite ieškoti „paskirstymo grafikas“.
1. Užduočių sąraše pasirinkite **1110** (**visuotinė konfigūracija**), tada pasirinkite **Vykdyti dabar**.
1. Sėkmingai įvykdžius užduotį patikrinkite, ar dabar produktų įvertinimai rodomi EKA.

Toliau pateiktame paveikslėlyje parodytas „Retail“ parametrų konfigūracijos norint EKA įjungti produkto įvertinimus pavyzdys.

![„Retail“ parametrų konfigūracijos norint EKA įjungti produkto įvertinimus pavyzdys](media/rnr-hq-enable-ratings-in-pos.png)

Tolesnėje iliustracijoje pateikiamas produkto įvertinimų EKA pavyzdys.

![Produkto įvertinimai EKA](media/rnr-pos-catalog-ratings.png)

Toliau pateiktoje iliustracijoje pateikiamas produkto įvertinimų skambučių centro kanaluose pavyzdys.

![Produkto įvertinimai skambučių centro kanale](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Įvertinimų ir atsiliepimų apžvalga](ratings-reviews-overview.md)

[Prisijunkite, norėdami naudoti įvertinimus ir atsiliepimus](opt-in-ratings-reviews.md)

[Įvertinimų ir atsiliepimų tvarkymas](manage-reviews.md)

[Įvertinimų ir atsiliepimų konfigūravimas](configure-ratings-reviews.md)
