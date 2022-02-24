---
title: Kas nauja ar pasikeitė „Dynamics 365 Talent” (2019 m. birželio mėn. 25 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-25
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 98ac7df9fa33635814b390427fd3292bdc1175ed
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528650"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-25-2019"></a>Kas nauja ar pasikeitė „Dynamics 365 Talent” (2019 m. birželio mėn. 25 d.)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Attract“.

## <a name="coming-soon-in-attract"></a>Jau greitai „Attract“

### <a name="job-approvals-appear-on-the-home-page"></a>Užduočių patvirtinimai rodomi pagrindiniame puslapyje

Patvirtinimai rodomi ataskaitų srities skyriuje **Patvirtinimai**. Tvirtintojai gali peržiūrėti savo patvirtinimus dalyje **Priskirta jums**, kurioje rodomas užduoties ID, pavadinimas, kiti tvirtintojai ir užduoties priskyrimo data. Vartotojai, pateikę užduotį patvirtinti, gali peržiūrėti savo užduotis dalyje **Jūsų užklausos**, kurioje rodomi pateiktą užduotį dar turintys patvirtinti tvirtintojai.

## <a name="changes-in-onboard"></a>Supažindinimo pakeitimai
Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Onboard“.

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai

Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2357 komponavimo versijai.

### <a name="incorrect-value-displayed-for-primary-position-314266"></a>Neteisinga rodoma pagrindinių pareigų reikšmė (314266)

Įdiegus šiuos pakeitimus parametras **Pagrindinės pareigos** bus nuosekliai rodomas visuose puslapiuose.

### <a name="cant-edit-after-recalling-the-workflow-in-review-318180"></a>Atšaukus darbo eigą vertinime, negalima redaguoti (318180)

Dabar vertinimus, atšauktus naudojant darbo eigą, galima redaguoti.

### <a name="final-comments-field-in-reviews-isnt-translated-325921"></a>Neverčiamas vertinimų laukas Baigiamieji komentarai (325921)

Naudojant „Talent“ žyma **Baigiamieji komentarai** bus išversta.

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Peržiūros funkcijos bus įjungtos tik smėlio dėžės aplinkose

Parengdami naują „Talent“ egzempliorių, galite nurodyti egzemplioriaus tipą: **Gamyba** arba **Smėlio dėžė**. Naudodami egzempliorių, kurio tipas – **Smėlio dėžė**, galite pirmieji išbandyti naujas funkcijas. Visi esami „Talent“ egzemplioriai bus atnaujinti ir jų tipas bus **Gamyba**. Jei norite vieno iš turimų egzempliorių tipą atnaujinti į **Smėlio dėžė**, kreipkitės į [palaikymo tarnybą](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), kad ši inicijuotų keitimo užklausą.

Daugiau informacijos apie tai, kaip publikuojami pakeitimai, žr. [„Talent“ parengimas](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

## <a name="in-preview"></a>Peržiūros režimu

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Atostogų tipų apribojimas prašymuose išleisti iš darbo

Organizacijos darbuotojams gali pasiūlyti daug atostogų tipų. Tačiau darbuotojai gali neturėti teisės teikti visų atostogų tipų prašymų išleisti iš darbo. Kai kuriuos atostogų tipus gali valdyti Personalo valdymo skyrius (HR). Naudodami šį leidimą galite sukonfigūruoti, kokių atostogų tipų prašymus išleisti iš darbo gali teikti darbuotojai. 

## <a name="coming-soon-in-core-hr"></a>Jau greitai „Core HR“ leidime

### <a name="feature-management-area-in-talent"></a>„Talent“ funkcijų valdymo sritis

Sritis **Funkcijų valdymas** bus pašalinta iš srities **Sistemos administravimas** dėl su šia funkcija susijusių problemų. Būsimame leidime įdiegsime sritį **Funkcijų valdymas** iš naujo. 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service objekto palaikymas pasirinktiniams laukams

Pasirinktinius laukus palaikys šie objektai: **Algalapio pajamų kodai**, **Pastoviosios atlyginimo dalies įvykis**, **Kompensavimo tinklelis**, **Mokėjimo laikotarpis** ir **Kompensavimo atskaitos taškas**. 

### <a name="new-common-data-service-entities"></a>Nauji „Common Data Service“ objektai

Į „Common Data Service“ bus įtrauktas objektas **Priežasčių kodai**.

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Peržiūrėkite informaciją apie vadovų savitarnos tiesioginių ir išplėstinių ataskaitų efektyvumą

Nauja parinktis leis vadovams peržiūrėti savo tiesioginių ataskaitų ir išplėstinių ataskaitų efektyvumą. Dabar tiesioginiai vadovai gali priskirti ir atnaujinti veiklos efektyvumo tikslus bei atlikti naujus vertinimus. Be to, tiesioginiai vadovai ir jų darbuotojai gali prižiūrėti ir atnaujinti našumo žurnalus, kad užtikrintų sklandų veiklos efektyvumo vertinimo procesą. Įdiegus šį pakeitimą vadovai be savo tiesioginių ataskaitų galės peržiūrėti ir tvarkyti su efektyvumu susijusią išplėstinių ataskaitų informaciją.

### <a name="print-performance-reviews"></a>Veiklos efektyvumo vertinimų spausdinimas

Darbuotojo veiklos efektyvumo vertinimą galės spausdinti darbuotojai, vadovai ir Personalo valdymo skyrius.
