---
title: Kas nauja ar pasikeitė „Dynamics 365 Talent” (2019 m. birželio mėn. 11 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 06/11/2019
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
ms.search.validFrom: 2019-06-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 20dc0768463d9a5d6762cb062deb0bdbe4d53fe3
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528674"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-11-2019"></a>Kas nauja ar pasikeitė „Dynamics 365 Talent” (2019 m. birželio mėn. 11 d.)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai

### <a name="search-engine-optimization-for-job-posts"></a>Darbo skelbimų ieškos modulio optimizavimas

Kai „Dynamics 365 Talent: Attract“ administravimo centre įjungiate parinktį **Ieškos modulio optimizavimas**, programa „Attract“ informuoja „Google“ indeksavimo programos programavimo sąsają (API), kad aptiktų tinklalapį kaskart, kai suaktyvinate ir paskelbiate apie naują užduotį arba atnaujinate esamą. Tokiu būdu darbas bus rodomas „Google“ ir kitų ieškos modulių ieškos rezultatuose.

Taip pat kaskart jums panaikinus darbo skelbimą, „Attract“ informuos indeksavimo API, kad panaikinto darbo skelbimo rodymas ieškos rezultatuose būtų sustabdytas.

> [!NOTE]
> Tinklalapių aptikimo robotams nėra nustatyto tinklalapių nuskaitymo arba ieškos rezultatų atnaujinimo laiko apribojimo.

## <a name="coming-soon-in-attract"></a>Jau greitai „Attract“

### <a name="job-approvals-appear-on-the-home-page"></a>Užduočių patvirtinimai rodomi pagrindiniame puslapyje

Patvirtinimai rodomi ataskaitų srities skyriuje **Patvirtinimai**. Tvirtintojai gali peržiūrėti savo patvirtinimus dalyje **Priskirta jums**, kurioje rodomas užduoties ID, pavadinimas, kiti tvirtintojai ir užduoties priskyrimo data. Vartotojai, pateikę užduotį patvirtinti, gali peržiūrėti savo užduotis dalyje **Jūsų užklausos**, kurioje rodomi pateiktą užduotį dar turintys patvirtinti tvirtintojai.

## <a name="changes-in-onboard"></a>Supažindinimo pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Onboard“.

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai

Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2337 komponavimo versijai.

### <a name="platform-update-27-for-finance-and-operations"></a>„Finance and Operations” platformos 27 naujinimas

Dėl daugiau išsamios informacijos apie „Platform“ naujinimą 27 „Finance and Operations“, žr. [Peržiūrėti funkcijas „Dynamics 365 Finance and Operations“ platformos naujinime 27 (2019 m. birželio mėnesį)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27).

### <a name="feature-management-workspace-in-talent"></a>„Talent“ funkcijų valdymo darbo sritis

Naudodamiesi **sistemos administravimo** darbo sritimi **Funkcijų valdymas** galite peržiūrėti, įjungti, išjungti ir planuoti funkcijas, pristatytas kiekviename leidime. Pagal numatytuosius nustatymus naujos funkcijos yra išjungtos. Darbo sritį **Funkcijų valdymas** galite naudoti norėdami jas įjungti ar peržiūrėti jų instrukcijas.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service objekto palaikymas pasirinktiniams laukams

Išduodančios agentūros objektas dabar palaiko pasirinktinius laukus.

### <a name="new-common-data-service-entities"></a>Nauji „Common Data Service“ objektai

Užduočių grupės objektas įtrauktas.

## <a name="in-preview"></a>Peržiūros režimu

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Peržiūros funkcijos bus įjungtos tik smėlio dėžės aplinkose

Daugiau informacijos apie tai, kaip publikuojami pakeitimai, žr. [„Talent“ parengimas](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

Parengdami naują „Talent“ egzempliorių, galite nurodyti egzemplioriaus tipą: Gamyba arba Smėlio dėžė. Naudodami egzempliorių, kurio tipas – Smėlio dėžė, galite pirmieji išbandyti naujas funkcijas. Visi esami „Talent“ egzemplioriai bus atnaujinti ir jų tipas bus **Gamyba**. Jei norite vieno iš turimų egzempliorių tipą atnaujinti į **Smėlio dėžė**, kreipkitės į [palaikymo tarnybą](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), kad ši inicijuotų keitimo užklausą.

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Atostogų tipų apribojimas prašymuose išleisti iš darbo

Organizacijos darbuotojams gali pasiūlyti daug atostogų tipų. Tačiau darbuotojai gali neturėti teisės teikti visų atostogų tipų prašymų išleisti iš darbo. Kai kuriuos atostogų tipus gali valdyti Personalo valdymo skyrius (HR). Naudodami šį leidimą galite sukonfigūruoti, kokių atostogų tipų prašymus išleisti iš darbo gali teikti darbuotojai. 

## <a name="coming-soon-in-core-hr"></a>Jau greitai „Core HR“ leidime

### <a name="view-extended-information-about-report-performance-in-manager-self-service"></a>Peržiūrėkite išsamią informaciją apie vadovų savitarnos ataskaitų efektyvumą

Nauja parinktis leis vadovams peržiūrėti savo tiesioginių ataskaitų ir išplėstinių ataskaitų efektyvumą. Dabar tiesioginiai vadovai gali priskirti ir atnaujinti veiklos efektyvumo tikslus bei atlikti naujus vertinimus. Be to, tiesioginiai vadovai ir jų darbuotojai gali prižiūrėti ir atnaujinti našumo žurnalus, kad užtikrintų sklandų veiklos efektyvumo vertinimo procesą. Įdiegus šį pakeitimą vadovai be savo tiesioginių ataskaitų galės peržiūrėti ir tvarkyti su efektyvumu susijusią išplėstinių ataskaitų informaciją.

### <a name="print-performance-reviews"></a>Veiklos efektyvumo vertinimų spausdinimas

Darbuotojo veiklos efektyvumo vertinimą galės spausdinti darbuotojai, vadovai ir Personalo valdymo skyrius.


[!INCLUDE[footer-include](../includes/footer-banner.md)]