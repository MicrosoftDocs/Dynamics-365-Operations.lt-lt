---
title: Įgalinti asmeniniams poreikiams pritaikytų produktų rekomendacijas
description: Šiame straipsnyje aprašoma, kaip padaryti, kad klientams būtų galimos pritaikyti produkto rekomendacijos Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: f626704b41b9d22f6b2ff55dd4ffe1037559a83a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283620"
---
# <a name="enable-personalized-recommendations"></a>Įgalinti asmeniniams poreikiams pritaikytas rekomendacijas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip padaryti, kad klientams būtų galimos pritaikyti produkto rekomendacijos Microsoft Dynamics 365 Commerce.

Naudojant „Microsoft Dynamics 365 Commerce“, mažmenininkai gali pritaikyti produktų rekomendacijas asmeniniams poreikiams (dar žinoma kaip suasmeninimas). Tokiu būdu asmeniniams poreikiams pritaikytos rekomendacijos gali būti įtrauktos į klientų patirtį internete ir elektroniniame kasos aparate (EKA). Įjungus suasmeninimo funkciją, sistema gali susieti vartotojo pirkinio ir produkto informaciją, kad sugeneruotų individualizuotas produkto rekomendacijas.

## <a name="personalization-prerequisites"></a>Suasmeninimo sąlygos

Prieš pateikdami asmeniniams poreikiams pritaikytų produktų rekomendacijas vartotojams, atkreipkite dėmesį, kad produktų rekomendacijos palaikomos tik tiems „Commerce“ vartotojams, kurie perkėlė saugyklą į „Azure Data Lake Store“. Kad klientai galėtų gauti asmeniniams poreikiams pritaikytų produktų rekomendacijas, mažmenininkai turi [Įjungti produktų rekomendacijas](enable-product-recommendations.md).

> [!NOTE]
> Įjungdami produktų rekomendacijas, taip pat įjungiate suasmeninimą. Tačiau jei išjungiate suasmeninimą, negalite išjungti kitų produktų tipų rekomendacijų.

Norėdami gauti daugiau informacijos apie produkto rekomendacijas, žr. [Produktų rekomendacijų apžvalga](product-recommendations.md).

## <a name="turn-on-personalization"></a>Įjungti suasmeninimą

Norėdami įjungti suasmeninimą, atlikite toliau nurodytus veiksmus.

1. "Commerce Headquarters" ieškokite **Funkcijų valdymas**.
1. Norėdami pamatyti galimų funkcijų sąrašą, pasirinkite **Visi**. 
1. Ieškos lauke įveskite **Rekomendacijos**.
1. Pasirinkite **Suasmenintos produktų rekomendacijos** funkciją.
1. Ypatybių srityje **Suasmenintos produktų rekomendacijos** pasirinkite **Įgalinti dabar**.

![Suasmeninimo įjungimas.](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> Įjungus suasmeninimą, pradedamas asmeniniams poreikiams pritaikytų produktų rekomendacijų sąrašų generavimo procesas. Gali prireikti vienos dienos, kol šie sąrašai bus prieinami ir matomi internete ir EKA.

## <a name="personalized-lists"></a>Asmeniniams poreikiams pritaikyti sąrašai

Be to, kad yra galimybė suasmeninti esamus mašinų sugeneruotus sąrašus, rekomendacijų tarnyba suteikia galimybę suasmeninti produkto aptikimą tiek internetu, tiek EKA.

Įjungus suasmeninimą, mažmenininkai gali rodyti pirkėjų asmeniniams poreikiams pritaikytus „Parinkta jums“ sąrašus internete arba „Rekomenduojama klientui“ sąrašus EKA terminaluose. Be to, mažmenininkai gali pritaikyti suasmeninimą esamiems produktų rekomendacijų sąrašams ir leisti autentifikuotiems vartotojams atsisakyti Bendrojo duomenų apsaugos reglamento (BDAR). Jei išjungsite suasmeninimą, taip pat išjungsite ir šias funkcijas.

### <a name="online-picks-for-you-lists"></a>Internetinis sąrašas „Parinkta jums“

Sąrašas „Parinkta jums“ yra dirbtinio intelekto ir mašininio mokymosi (angl. AI-ML) sąrašas, kuriame autentifikuotam vartotojui pateikiamas asmeniniams poreikiams pritaikytas siūlomų produktų sąrašas. Šis sąrašas yra pagrįstas vartotojo kanalų pirkimo istorija. Pagal asmeninius poreikius pritaikytos rekomendacijos yra dinamiškai atnaujinamos, jei vartotojas perka daugiau. Šio tipo sąrašai taip pat palaiko kategorijų filtravimą, kad mažmenininkai galėtų parodyti populiariausias parinktis, remiantis naršymo hierarchijomis.

Kad bet kuriame „e-Commerce“ puslapyje galėtų būti sąrašas „Parinkta jums“, turi būti įvykdyti šie reikalavimai:

- Vartotojas privalo būti prisijungęs. Anoniminis vartotojas nematys asmeniniams poreikiams pritaikytų rekomendacijų.
- Vartotojo paskyroje turi būti bent vienas pirkinys.
- Vartotojas turi pasirinkti gauti asmeniniams poreikiams pritaikytas rekomendacijas.

Toliau parodytame paveikslėlyje pateiktas internetinės parduotuvės puslapyje esančio sąrašo „Parinkta jums“ pavyzdys.

![Internetinis sąrašas „Parinkta jums“.](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a>Sąrašai „Rekomenduojama klientui“, esantys EKA

Norėdami padidinti savo klientų dėmesį, mažmenininkai gali pagal asmeninius poreikius pritaikyti esamus informacijos apie klientus puslapius, pridėdami kontekstinį sąrašą „Rekomenduojama klientui“.

Toliau parodytame paveikslėlyje pateiktas EKA terminale esančio sąrašo „Rekomenduojama klientui“ pavyzdys.

![Sąrašai „Rekomenduojama klientui“, esantys EKA.](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a>Suasmeninimo esamiems rekomendacijų sąrašams pritaikymas

Mažmenininkai gali pritaikyti suasmeninimą esamiems rekomendacijų sąrašams, tokiems kaip „Naujas“, „Populiariausi“, „Geriausiai parduodami“, „Žmonėms taip pat patiko“ ir „Kartu taip pat perkama“. Kai suasmeninimas pritaikomas esamiems sąrašams, prekės, kurias prisijungęs vartotojas nusipirko anksčiau, pašalinamos iš tų sąrašų. Tiek anoniminiams vartotojams, tiek vartotojams, kurie atsisakė gauti asmeniniams poreikiams pritaikytas rekomendacijas, rodomos numatytos esamų sąrašų versijos. Todėl mažmenininkams nereikia rankiniu būdu prižiūrėti atskirų puslapių.

Pavyzdžiui, prisijungęs vartotojas jau nusipirko juodą laikrodį ir rudus darbo batus, kurie pateikiami toliau pateiktoje iliustracijoje, sąraše „Populiariausi – numatytasis“. Todėl vartotojas vietoje tų produktų matys naujus produktus, kaip parodyta sąraše „Populiariausi – asmeniniams poreikiams pritaikyta“.

![Suasmeninimo pritaikymas.](./media/applypersonalization.png)

Jei norite pritaikyti suasmeninimą esamam rekomendacijų sąrašui, esančiam „Commerce“ svetainės daryklėje, atlikite toliau nurodytus veiksmus.

1. Atidarykite esamą svetainių daryklių puslapį, kuriame yra produktų rinkimo modulis.
1. Kairėje naršymo srityje pasirinkite produkto rinkimo modulį.
1. Dešinėje naršymo srityje, skyriuje **Produktai**, pasirinkite sąrašą.
1. Dialogo lange **Pasirinkti produktų sąrašo konfigūraciją**, skyriuje **Tipas**, pasirinkite sąrašo tipą.
1. Pažymėkite žymės langelį **Taikyti suasmeninimą**, tada pasirinkite **Gerai**.

    ![Suasmeninimo pritaikymas populiariausiam sąrašui.](./media/ApplyPersonalizationToTrending.PNG)

1. Išsaugokite puslapį, baikite jį redaguoti ir paskelbkite. Paskelbus puslapį, prisijungę vartotojai matys asmeniniams poreikiams pritaikytus populiariausius sąrašus.

## <a name="additional-resources"></a>Papildomi ištekliai

[Produktų rekomendacijų apžvalga](product-recommendations.md)

[„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje](enable-adls-environment.md)

[Įjungti produktų rekomendacijas](enable-product-recommendations.md)

[Įjungti „apsipirkti panašia mada“ rekomendacijas](shop-similar-looks.md)

[Personalizuotų rekomendacijų atsisakymas](personalization-gdpr.md)

[Produktų rekomendacijų įtraukimas į EKA](product.md)

[Rekomendacijų įtraukimas į operacijų ekraną](add-recommendations-control-pos-screen.md)

[AI-ML rekomendacijų rezultatų koregavimas](modify-product-recommendation-results.md)

[Kuruojamų rekomendacijų kūrimas rankiniu būdu](create-editorial-recommendation-lists.md)

[Rekomendacijų su demonstraciniais duomenimis kūrimas](product-recommendations-demo-data.md)

[DUK apie produktų rekomendacijas](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
