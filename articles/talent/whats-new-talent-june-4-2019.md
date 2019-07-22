---
title: Kas nauja ar pasikeitė „Dynamics 365 for Talent” (2019 m. birželio mėn. 4 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 for Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0a93ad140fb9116ffb0c486b7f3175f90859f125
ms.sourcegitcommit: 7b5ff31c0a82809641beb681510201b942932c74
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/06/2019
ms.locfileid: "1621867"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-june-4-2019"></a>Kas nauja ar pasikeitė „Dynamics 365 for Talent” (2019 m. birželio mėn. 4 d.)

[!include [banner](includes/banner.md)]

Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 for Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai

Šiame leidime įtraukti smulkūs klaidų ištaisymai, skirti „Dynamics 365 for Talent: Attract“.

## <a name="coming-soon-in-attract"></a>Jau greitai „Attract“

### <a name="job-approvals-on-the-home-page"></a>Užduočių patvirtinimai pagrindiniame puslapyje

Patvirtinimai rodomi ataskaitų srities skyriuje **Patvirtinimai**. Tvirtintojai gali peržiūrėti savo patvirtinimus srityje **Priskirta jums**. Šioje dalyje rodomas užduoties ID, pavadinimas, kiti tvirtintojai ir užduoties priskyrimo data. Užduotį pateikę tvirtinti vartotojai gali peržiūrėti savo užduotis srityje **Jūsų užklausos**. Šioje dalyje rodomi tvirtintojai, kurie vis dar turi patvirtinti pateiktą užduotį.

## <a name="changes-in-onboard"></a>Supažindinimo pakeitimai

Šiame leidime įtraukti smulkūs klaidų ištaisymai, skirti „Dynamics 365 for Talent: Onboard“.

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai

Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2330 komponavimo versijai.

### <a name="new-page-to-validate-position-hierarchy-data"></a>Naujas puslapis, skirtas tikrinti pareigų hierarchijos duomenis

Personalo valdymo (HR) darbuotojai ir administratoriai gali tikrinti, ar valdybos hierarchijoje nėra netyčia importuotų ciklinių nuorodų. Šį naują puslapį galite pasiekti srityje **Organizacijos administravimas \> Saitai \> Pareigos \>> Pareigų hierarchijos tikrinimas**.

### <a name="specify-reason-codes-on-leave-types"></a>Nurodykite atostogų tipų priežasties kodus

Organizacijoms gali prireikti papildomos informacijos, susijusios su nedarbo laiko užklausomis. Dabar galite nurodyti nedarbo laiko tipų priežasties kodus ir leisti darbuotojams pasirinkti priežasties kodą savo nedarbo laiko užklausose.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Reikalavimas pateikti priežasties kodus, skirtus tam tikriems nedarbo laiko tipams nedarbo laiko užklausose

Organizacijos gali norėti priežasčių kodus priskirti tam tikriems nedarbo laiko tipams, kai darbuotojai teikia nedarbingumo užklausas. Šis reikalavimas gali būti dėl įmonės strategijos arba reguliavimo reikalavimų. Galite nurodyti, kokių tipų nedarbo laiko priežasties kodus reikia pateikti, ir galite reikalauti darbuotojų pateikti nedarbo laiko tipo priežasties kodą savo nedarbo laiko užklausose.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Nedarbo laiko ir neatvykimo operacijų sąrašo pateikimas personalo skyriui

Galimybė sekti darbuotojų ne darbo laiką ir suprasti, kaip jis skaičiuojamas, ne tik padeda personalo valdymo skyriui atsakyti į darbuotojų klausimus, bet ir padeda užtikrinti, kad jis būtų skiriamas darbuotojams tiksliai. Dabar HR suteikta prieiga prie naujo operacijų (subsidijų, kaupimų, koregavimų ir užklausų) rodinio, kad HR darbuotojai galėtų sužinoti nebuvimo balansų priežastis.

### <a name="deleting-a-record-from-talent-doesnt-remove-the-record-from-common-data-service"></a>Panaikinus įrašą iš „Talent“, jis nepašalinamas iš „Common Data Service։

Iš „Talent Core HR“ pašalinami įrašai dabar taip pat pašalinami ir iš „Common Data Service“.

### <a name="variable-compensation-plan-valid-fromto-dates-arent-being-honored"></a>Neatsižvelgiama į kintamosios atlyginimo dalies plano galiojimo nuo / iki datas

Šiame leidime negalite užregistruoti darbuotojo kintamosios atlyginimo dalies plane, jei pradžios data yra ankstesnė nei plano pradžios data arba pabaigos data yra vėlesnė už plano pabaigos datą. 

### <a name="performance-review-comments-are-removed-when-users-select-cancel"></a>Veiklos efektyvumo vertinimo komentarai pašalinami, kai vartotojai pasirenka Atšaukti

Šiame leidime problema išspęsta pašalinant vertinimo komentarus, jei vartotojas pradeda keisti komentarą, bet vėliau pasirenka **Atšaukti**. 

## <a name="in-preview"></a>Peržiūros režimu

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Peržiūros funkcijos įjungtos tik smėlio dėžės egzemplioriuose

Parengdami naują „Talent“ egzempliorių galite nurodyti egzemplioriaus tipą: **Gamyba** arba **Smėlio dėžė**. Naudodami egzempliorių, kurio tipas – **Smėlio dėžė**, galite pirmieji išbandyti naujas funkcijas. Visi esami „Talent“ egzemplioriai bus atnaujinti ir jų tipas bus **Gamyba**. Jei norite vieno iš turimų egzempliorių tipą atnaujinti į **Smėlio dėžė**, kreipkitės į [palaikymo tarnybą](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), kad ši inicijuotų keitimo užklausą.

Daugiau informacijos apie tai, kaip publikuojami pakeitimai, žr. [„Talent“ parengimas](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Atostogų tipų apribojimas prašymuose išleisti iš darbo

Organizacijos darbuotojams gali pasiūlyti įvairių tipų atostogų. Tačiau darbuotojai gali neturėti teisės teikti visų atostogų tipų prašymų išleisti iš darbo. Kai kuriuos atostogų tipus gali valdyti Personalo valdymo skyrius (HR). Naudodami šį leidimą galite sukonfigūruoti, kokių atostogų tipų prašymus išleisti iš darbo gali teikti darbuotojai. 

## <a name="coming-soon-in-core-hr"></a>Jau greitai „Core HR“ leidime

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Peržiūrėkite išsamią informaciją apie vadovų savitarnos efektyvumą

Nauja parinktis leis vadovams peržiūrėti savo tiesioginių ataskaitų ir išplėstinių ataskaitų efektyvumą. Dabar tiesioginiai vadovai gali priskirti ir atnaujinti veiklos efektyvumo tikslus bei atlikti naujus vertinimus, bendrai valdomus kartu su darbuotojais. Be to, tiesioginiai vadovai ir jų darbuotojai gali prižiūrėti ir atnaujinti našumo žurnalus, kad užtikrintų sklandų veiklos efektyvumo vertinimo procesą. Įdiegus šį pakeitimą vadovai be savo tiesioginių ataskaitų galės peržiūrėti ir tvarkyti su efektyvumu susijusią išplėstinių ataskaitų informaciją. 

### <a name="print-performance-reviews"></a>Veiklos efektyvumo vertinimų spausdinimas

Darbuotojo veiklos efektyvumo vertinimą galės spausdinti darbuotojai, vadovai ir Personalo valdymo skyrius.
