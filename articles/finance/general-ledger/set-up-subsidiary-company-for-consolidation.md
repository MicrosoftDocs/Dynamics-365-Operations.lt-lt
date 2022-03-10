---
title: Nustatyti papildomą asmenį konsolidavimo procesui
description: Šioje temoje paaiškinama, kaip dirbti su sąskaitų grafikais konsoliduojant bendroves.
author: jinniew
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: fbec5ad8fa5e17b75859c07ee64a66c9568c97d3d18b6a7616a64303d3a33f10
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727964"
---
# <a name="set-up-a-subsidiary-legal-entity-for-consolidation"></a>Nustatyti papildomą asmenį konsolidavimo procesui

[!include [banner](../includes/banner.md)]

Metodas, kurį naudojate siekiant parengti papildomas sąskaitas konsolidavimui priklauso iš dalies nuo plėtinio, prie kurio sąskaitų grafiko struktūra papildomuose juridiniuose asmenyse parodo sąskaitų grafiką konsoliduotame juridiniame asmenyje.

Prieš jums pradedant konsoliduoti kaip laikotarpio pabaigos uždarymo dalį, užbaikite parengimo veiksmus ilgo laiko uždarymui, bet neuždarykite papildomų sąskaitų iki konsolidavimo pabaigos. Dėl daugiau informacijos apie ilgalaikio laikotarpio uždarymą, žr. [Uždaryti bendrą buhalterinę knygą po laikotarpio](close-general-ledger-at-period-end.md) ir [Uždaryti mokestinius metus](tasks/close-fiscal-year.md).

> [!NOTE]
>  Rekomenduojame jums naudoti „Management Reporter“ „Microsoft Dynamics 365 Finance“ siekiant suderinti finansinius rezultatus keliems juridiniams asmenims konsoliduotame formate. „Management Reporter“ leidžia jums kurti konsoliduotas finansines ataskaitas juridiniuose objektuose, naudoti „Exce“ siekiant importuoti konsolidavimo duomenis iš kitų šaltinių ir versti sumas į bet kokių ataskaitų valiutų skaičius be poreikio vykdyti konsolidavimo procesą „Dynamics 365 Finance“.

## <a name="map-subsidiary-main-accounts-to-consolidated-main-accounts"></a>Talpinkite į žemėlapį dukterinės įmonės pagrindines sąskaitas siekiant konsoliduoti pagrindines sąskaitas

Jei sąskaitų grafikas dukteriniame juridiniame asmenyje neseka sąskaitų grafiko konsoliduoto juridinio asmens, galite talpinti žemėlapyje pagrindines sąskaitas dukterinėje įmonėje į pagrindines sąskaitas konsoliduotame juridiname asmenyje.

1. Skyriuje *dukterinis juridinis asmuo*, eiktie į **Pagrindinė buhalterijos knyga \> Nustatymai** \> **Sąskaitų grafikas \> Sąskaitų grafikas**.
2. Rinkitės sąskaitų grafiką. „FastTab“ **Pagrindinės sąskaitos** rinkitės pagrindinę sąskaitą ir tada **Redaguoti**.
3. Rinkitės kiekvieną dukterinę pagrindinę sąskaitą, kuri turi būti talpinama į konsoliduotą pagrindinę sąskaitą. „FastTab“ **Bendri** laukleyje **Konsolidavimo sąskaita** įveskite sąskaitą konsoliduotame juridiniame asmenyje, kurio balansas ar transakcijos turi būti perkeltas į pasirinktos dukterinės pagrindinę sąskaitą. Galite įvesti tą pačią konsoliduotą pagrindinę sąskaitą kelioms dukterinėms sąskaitoms.

    > [!NOTE]
    > Jei pagrindiniai dukterinių sąskaitų tipai yra talpiname žemėlapyje ir skiriasi nuo pagrindinių sąskaitos tipų konsoliduotame juridiniame asmenyje, sąskaitų vertės turinčios pagrindinį sąskaitos tipą **Bendri** yra užrašomos konsolidavimo metu.

4. Parenkite ataskaitas ir finansines ataskaitas konsoliduotam juridiniam asmeniui, kuris yra parengtas pagal finansines dimensijas. Atlikite šiuos žingsnius tam, kad talpintumėte finansines dimensijas, kurios naudojamos dukterinėse sąskaitose finansinėse dimensijose konsoliduotame juridiniame asmenyje:

    1. Skyriuje *Dukterinis juridinis asmuo*, eiktie į **Bendra buhalterijos knyga \> Nustatymai \> Finansinės dimensijos \> Finansinės dimensijos**, rinkitės finansinę dimensiją ir tada rinkitės **Finansinės dimensijos vertės**.
    2. Rinkitės finansinės dimensijos vertę, kad talpintumėte į žemėlapį kitą finansinės dimensijos vertę konsoliduotame juridiniame asmenyje.
    3. „FastTab“ **Bendri** laukelyje **Grupės dimensija** įveskite finansinę dimensiją konsoliduotame juridiniame asmenyje. Konsolidavimo metu, ši finansinė dimensija bus priskirta perlaidoms ir balansams, kurie naudoja pasirinktą finansinę dimensiją dukteriniame juridiniame asmenyje. Finansinės dimensijos, kurias įvedėte čia turi būti naudojamos konsoliduotame juridiniame asmenyje. Galite priskirti finansinę dimensiją, kuri naudojama kaip grupės finansinė dimensija kelioms dukterinėms finansinėms dimensijoms.

5. Jei darote interneto konsolidavimą, atlikite šiuos veiksmus siekiant užtikrinti, kad perlaidos atsitinka kaip norite:

    1. Skyriuje *konsoliduotas juridinis asmuo*, eikite į **Bendra buhalterinė knyga \> Periodinis \> Konsoliduoti \> Konsoliduoti \[Eksportuoti į\]** norėdami atverti **Konsoliduoti \[Internete\]** puslapį.
    2. Skirtuke **Kriterijai** rinkitės **Naudoti konsolidavimo sąskaitą** žymimą laukelį.
    3. Skirtuke **Finansinės dimensijos**, rinkitės tinkamas finansines dimensijas.
    4. Kiekvienai jūsų pasirinktai finansinei dimensijai, įveskite numerį **Segmento užsakymo** laukelyje siekiant nurodyti užsakymą, kuriame dimensijos turėtų pasirodyti.

## <a name="maintain-the-same-chart-of-accounts-in-the-subsidiary-and-consolidated-legal-entities"></a>Išlaikykite sąskaitų grafiką tą patį dukteriniame ir konsoliduotame juridiniame asmenyje

Pagrindinės sąskaitos dukteriniame juridiniame asmenyje gali turėti tuos pačius sąskaitos numerius ir tą pčią struktūrą sąskaitų grafikui, kaip ir pagrindinės sąskaitos konsoliduotame juridiniame asmenyje. Šiuo atveju, jums nereikės rankiniu būdu padaryti pagrindinių sąskaitų žemėlapio dukterinėje įmonėje į pagrindines sąskaitas konsoliduotame juridiniame asmenyje.

Prieš pradėdami konsolidavimą, imkitės tokių veiksmų.

1. Skyriuje *konsoliduotas juridinis asmuo*, eikite į **Bendra buhalterinė knyga \> Periodinis \> Konsoliduoti \> Konsoliduoti \[Eksportuoti į\]** norėdami atverti **Konsoliduoti \[Internete\]** puslapį.
2. Rinkitės **Naudokite konsolidavimo sąskaitą** žymimą laukelį. Konsolidavimo metu, transakcijos ir balansai bus automatiškai perkeliami į tinkamą sąskaitą.

> [!NOTE]
> Jei sąskaitos neatsako, konsolidavimas sustoja ir gausite pranešimą.

## <a name="create-a-chart-of-accounts-for-the-consolidated-legal-entity-based-on-an-existing-chart-of-accounts"></a>Sukurkite sąskaitų grafiką konsoliduotam juridiniam asmeniui pagal esantį sąskaitų grafiką

Galite daryti konsolidavimą bet jei sąskaitų grafikas dar nebuvo sukurtas konsoliduotame juridiniame asmenyje.

- Jei planuojate sąskaitos struktūrą, kurią norite naudoti konsoliduotame juridiniame asmenyje, galite talpinti žemėlapį į dukterines sąskaitas šioje struktūroje.
- Jei netalpinate jokių dukterinių sąskaitų į žemėlapį, sąskaitos konsoliduotame juridiniame asmenyje yra automatiškai sukuriamos kai dukteriniai duomenys yra perkeliami į konsoliduotą juridinį asmenį. Šios sąskaitos yra parengtos pagal pagrindinę sąskaitą. Tolesni duomenys yra kaupiami sąskaitos konsoliduotame juridiniame asmenyje, kuris turi tą patįį numerį kaip dukterinės sąskaitos.

Nepriklausomai nuo to, ar talpinote žemėlapio sąskaitas, pašalinkite **Naudoti konsolidavimo sąskaitą** žymimą laukelį **Konsoliduoti** puslapyje konsoliduotame juridiniame asmenyje prieš vykdydami tokio tipo konsolidavimą.

> [!NOTE]
> Galite naudoti šį metodą siekiant sukurti sąskaitų grafiką konsoliduotame juridiniame asmenyje iš sąskaitų grafiko papildomuose juridiniusoe asmenyse. (Dėl papildomos informacijos, žr. [Konsolidavimo paskyros grupės ir papildomos konsolidavimo sąskaitos](../budgeting/consolidation-account-groups-consolidation-accounts.md).) Tuomet priskirkite atitinkamą konsolidavimo konvertavimo principą kiekvienai konsoliduotai pagrindinei sąskaitai ir vykdykite konsolidavimą visiems dukteriniams juridiniams asmenims.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]