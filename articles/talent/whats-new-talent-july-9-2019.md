---
title: Kas nauja ar pasikeitė „Dynamics 365 Talent” (2019 m. liepos 9 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 07/09/2019
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
ms.search.validFrom: 2019-07-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 99a7e6130d45229011a185087d4872fe34b8224a
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897631"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-9-2019"></a>Kas nauja ar pasikeitė „Dynamics 365 Talent” (2019 m. liepos 9 d.)

Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Attract“.

### <a name="coming-soon-in-attract"></a>Jau greitai „Attract“

#### <a name="job-approvals-appear-on-the-home-page"></a>Užduočių patvirtinimai rodomi pagrindiniame puslapyje

Patvirtinimai rodomi ataskaitų srities skyriuje **Patvirtinimai**. Tvirtintojai gali peržiūrėti savo patvirtinimus dalyje **Priskirta jums**, kurioje rodomas užduoties ID, pavadinimas, kiti tvirtintojai ir užduoties priskyrimo data. Vartotojai, pateikę užduotį patvirtinti, gali peržiūrėti savo užduotis dalyje **Jūsų užklausos**, kurioje rodomi pateiktą užduotį dar turintys patvirtinti tvirtintojai.

## <a name="changes-in-onboard"></a>Supažindinimo pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Onboard“.

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai

Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2374 komponavimo versijai.

### <a name="platform-update-28-for-finance-and-operations"></a>„Finance and Operations“ platformos 28 naujinimas

Daugiau informacijos apie „Finance and Operations“ platformos 28 naujinimą žr. [Peržiūros funkcijos programos „Dynamics 365 Finance and Operations“ platformos 28 naujinime (2019 m. liepos mėn.)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-28).

### <a name="entity-support-for-custom-fields-in-common-data-service"></a>Objekto palaikymas pasirinktiniams laukams „Common Data Service” 

Toliau nurodyti objektai palaiko pasirinktinius laukus. 

- **Kompensavimo planas**
- **Kompensavimo atskaitos taškų nustatymas**
- **Kompensavimo atskaitos taškus nustatanti eilutė**
- **Algalapio pajamų kodas**
- **Mokėjimo laikotarpis**
- **Pastoviosios atlyginimo dalies įvykis**
- **Kompensavimo tinklelis**

Norėdami peržiūrėti visus atnaujintus objektus programoje „Talent”, atlikite toliau nurodytus veiksmus.

1. Pasirinkite **Sistemos administravimas**, tada – **Saitai**, galiausiai pasirinkite **„Common Data Service” konfigūravimas**.
2. Pasirinkite išplečiamąjį meniu **CDS objekto pavadinimas**. Visi išvardyti objektai yra naujausioje versijoje. 

###  <a name="full-name-added-to-worker-entity-in-common-data-service"></a>Viso vardo lauko įtraukimas į darbininko objektą „Common Data Service”

Laukas **Visas vardas** įtrauktas į objektą **Darbininkas**.

### <a name="full-time-equivalent-higher-than-10"></a>Viso etato ekvivalentas yra didesnis nei 1,0

Dabar rodomas įspėjimas, jei didesnė nei 1,0 vertė įvedama visu etatu dirbančio darbuotojo pareigose. 

### <a name="a-warning-no-longer-displays-on-the-worker-page-when-there-is-no-future-dated-employment"></a>Darbininko puslapyje nebebus rodomas įspėjimas, kai nėra įdarbinimo, kurio pradžios data yra ateityje

Nebegausite pranešimo, nurodančio, kad yra būsimas įdarbinimas, kai pereinama į **darbininko** puslapį iš sąrašo **Išeinantys darbuotojai** darbo srityje **Personalo valdymas**. 

### <a name="unable-to-delete-a-business-process-in-talent"></a>Nesėkmingas verslo proceso panaikinimas programoje „Talent”

Verslo procesus galite panaikinti darbo srityje **Verslo procesas**.

### <a name="leave-balance-no-longer-displays-zero-for-plans-with-no-accruals-when-using-balance-as-of-accrual-period"></a>Planuose be kaupimų atostogų balanse nebebus rodomas nulis naudojant likutį kaupimo laikotarpiu

Planai be kaupimų dabar gali rodyti balansą.

## <a name="in-preview"></a>Peržiūros režimu

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Peržiūros funkcijos įjungtos tik smėlio dėžės egzemplioriuose

Parengdami naują „Talent“ egzempliorių galite nurodyti egzemplioriaus tipą: **Gamyba** arba **Smėlio dėžė**. Naudodami egzempliorių, kurio tipas – **Smėlio dėžė**, galite pirmieji išbandyti naujas funkcijas. Visi esami „Talent“ egzemplioriai bus atnaujinti ir jų tipas bus **Gamyba**. Jei norite vieno iš turimų egzempliorių tipą atnaujinti į **Smėlio dėžė**, kreipkitės į [palaikymo tarnybą](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), kad ši inicijuotų keitimo užklausą.

Daugiau informacijos apie tai, kaip publikuojami pakeitimai, žr. [„Talent“ parengimas](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Atostogų tipų apribojimas prašymuose išleisti iš darbo

Organizacijos darbuotojams gali pasiūlyti įvairių tipų atostogų. Tačiau darbuotojai gali neturėti teisės teikti visų atostogų tipų prašymų išleisti iš darbo. Kai kuriuos atostogų tipus gali valdyti Personalo valdymo skyrius (HR). Naudodami šį leidimą galite sukonfigūruoti, kokių atostogų tipų prašymus išleisti iš darbo gali teikti darbuotojai. 

## <a name="coming-soon-in-core-hr"></a>Jau greitai „Core HR“ leidime

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Peržiūrėkite išsamią informaciją apie vadovų savitarnos efektyvumą

Nauja parinktis leis vadovams peržiūrėti savo tiesioginių ataskaitų ir išplėstinių ataskaitų efektyvumą. Dabar tiesioginiai vadovai gali priskirti ir atnaujinti veiklos efektyvumo tikslus bei atlikti naujus vertinimus, bendrai valdomus kartu su darbuotojais. Be to, tiesioginiai vadovai ir jų darbuotojai gali prižiūrėti ir atnaujinti našumo žurnalus, kad užtikrintų sklandų veiklos efektyvumo vertinimo procesą. Įdiegus šį pakeitimą vadovai be savo tiesioginių ataskaitų galės peržiūrėti ir tvarkyti su efektyvumu susijusią išplėstinių ataskaitų informaciją. 

### <a name="entities-supporting-custom-fields"></a>Objektai, palaikantys pasirinktinius laukus

Toliau nurodyti objektai bus įgalinti pasirinktiniams laukams „Common Data Service”. 

- **Atostogų tipas**
- **Darbininko banko kodas**
- **Darbo kalendorius**
