---
title: Kas nauja ar pasikeitė „Dynamics 365 for Talent” (2019 m. liepos 16 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 for Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 07/16/2019
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
ms.search.validFrom: 2019-07-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ac0990a72224395cf109c7eb42cbb48ece2a0b4f
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/30/2019
ms.locfileid: "1795201"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-july-16-2019"></a>Kas nauja ar pasikeitė „Dynamics 365 for Talent” (2019 m. liepos 16 d.)

[!include [banner](includes/banner.md)]

Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 for Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai
Šiame leidime įtraukti smulkūs klaidų ištaisymai, skirti „Dynamics 365 Talent: Attract“

### <a name="coming-soon-in-attract"></a>Jau greitai „Attract“
#### <a name="job-approvals-appear-on-the-home-page"></a>Užduočių patvirtinimai rodomi pagrindiniame puslapyje

Patvirtinimai rodomi ataskaitų srities skyriuje **Patvirtinimai**. Tvirtintojai gali peržiūrėti savo patvirtinimus dalyje **Priskirta jums**, kurioje rodomas užduoties ID, pavadinimas, kiti tvirtintojai ir užduoties priskyrimo data. Vartotojai, pateikę užduotį patvirtinti, gali peržiūrėti savo užduotis dalyje **Jūsų užklausos**, kurioje rodomi pateiktą užduotį dar turintys patvirtinti tvirtintojai.

## <a name="changes-in-onboard"></a>Supažindinimo pakeitimai
Šiame leidime įtraukti smulkūs klaidų ištaisymai, skirti „Dynamics 365 Talent: Onboard“

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai
Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2390 komponavimo versijai.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>„Common Data Service” objektai, kurie dabar palaiko pasirinktinius laukus

- „BusinessProcessCalendar”                     
- „BusinessProcessGroupAssignment”         
- „BusinessProcessStage”                          
- „BusinessProcessTemplateHeader”          
- „BusinessProcessTemplateTask”            
- „HcmBenefitOption”                              
- „HcmBenefitType”                                  
- „HcmCompensationGrid”                            
- „HcmCompensationLevel”                          
- „HcmCompensationPayFrequency”                 
- „HcmCompensationReferencePointSetup”        
- „HcmCompensationReferencePointSetupLine” 
- „HcmCompensationRegion”                     
- „HcmCompFixedPlanTable”                     
- HcmEmployment                                
- „HcmEthnicOrigin”                                
- „HcmFixedCompensationEvent”                 
- „HcmJob”                                           
- „HcmJobFunction”
- „HcmJobType”
- „HcmLanguageCode”
- „HcmPayrollCalculationFrequency”
- „HcmPosition”
- „HcmPositionType”
- „HcmSkillType”
- „HcmVeteranStatus”
- „HcmWorkCalendarHoliday”
- „HcmWorkCalendarHolidayLine”
- „HcmWorker”
- „HcmWorkerPersonalDetail”
- „LeaveType”
- „OMDepartment”
- „OMLegalEntity”
- „PayCycle”
- „PayPeriod”
- „PayrollBenefitCalculationRate”
- „PayrollBenefitCalculationRateDetail”
- „PayrollEarningCode”

### <a name="unable-to-see-goals-and-reviews-in-manager-self-service"></a>Neįmanoma pamatyti tikslų ir apžvalgų vadovo savitarnoje

Šios savaitės pakeitimai dabar leidžia rodyti ir redaguoti tikslus ir apžvalgas aukštesnio lygio vadovams vadovo savitarnoje.

### <a name="goal-form-cannot-be-closed-after-a-user-edits-any-goal-field"></a>Negalima uždaryti tikslo formos po to, kai naudotojas redaguoja bet kurį tikslo lauką

Šis leidimas pataiso problemą, kai tikslo forma neužsidaro pasirinkus **Uždaryti**.

### <a name="creating-new-goals-and-saving-displays-error"></a>Rodoma klaida, kai kuriami ir įrašomi nauji tikslai

Šis leidimas išsprendžia problemą įrašant tikslus darbuotojo ir vadovo savitarnoje.

### <a name="unable-to-add-a-field-to-position-details"></a>Neįmanoma įtraukti lauko į pareigų informaciją 

Po šio leidimo pasirinktiniai laukai palaikomi pareigų informacijoje.
 
### <a name="unable-to-set-up-expiring-date-on-the-earning-code-through-data-management"></a>Neįmanoma nustatyti pajamų kodo galiojimo pabaigos datos naudojant duomenų valdymą

Pakeitimai dabar leidžia nustatyti pajamų kodų galiojimo datas duomenų valdyme.

### <a name="new-custom-fields-dont-sync-quickly-enough"></a>Nauji pasirinktiniai laukai nėra pakankamai greitai sinchronizuojami

Šios savaitės leidime buvo pagerintas pasirinktinių laukų sinchronizavimo „Common Data Service” našumas.

### <a name="entity-export-to-database-jobs-fail-with-error-message-format-of-the-initialization-string-does-not-conform-to-specification-starting-at-index-0"></a>Nepavyksta eksportuoti objekto į duomenų bazės užduotis, ir rodomas klaidos pranešimas: „Inicijavimo eilutės formatas neatitinka specifikacijos, kuri prasideda indeksu 0“.

Šis leidimas išsprendžia problemą, kai nepavyksta atlikti duomenų bazės paketinių užduočių. Norėdami naujinti neautomatiškai, atlikite toliau nurodytus veiksmus.

1. Pasirinkite **Duomenų valdymas**.
2. Pasirinkite **Konfigūruoti objektų eksportavimą į duomenų bazę**.
3. Iš naujo įveskite ryšio eilutę į paskirties duomenų bazę ir pasirinkite **Įrašyti**.

### <a name="smtp-email-configuration-suddenly-fails-with-error-message-the-smtp-server-requires-a-secure-connection-or-the-client-was-not-authenticated"></a>Nepavyksta konfigūruoti SMTP el. pašto, ir rodomas klaidos pranešimas: „SMTP serveriui reikia saugaus ryšio arba klientas nebuvo autentifikuotas”.

Šis leidimas išsprendžia problemą, kai nepavyksta konfigūruoti SMTP el. pašto. Norėdami naujinti neautomatiškai, atlikite toliau nurodytus veiksmus.

1. Pasirinkite **Sistemos administravimas**.
2. Pasirinkite **El. pašto parametrai**.
3. Pasirinkite **SMTP parametrai**. 
4. Iš naujo įveskite vartotojo vardą ir slaptažodį, naudojamą SMTP serveriui, ir pasirinkite **Įrašyti**.

## <a name="in-preview"></a>Peržiūros režimu

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Peržiūros funkcijos įjungtos tik smėlio dėžės egzemplioriuose

Parengdami naują „Talent“ egzempliorių galite nurodyti egzemplioriaus tipą: **Gamyba** arba **Smėlio dėžė**. Naudodami egzempliorių, kurio tipas – **Smėlio dėžė**, galite pirmieji išbandyti naujas funkcijas. Visi esami „Talent“ egzemplioriai bus atnaujinti ir jų tipas bus **Gamyba**. Jei norite vieno iš turimų egzempliorių tipą atnaujinti į **Smėlio dėžė**, kreipkitės į [palaikymo tarnybą](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), kad ši inicijuotų keitimo užklausą.

Daugiau informacijos apie tai, kaip publikuojami pakeitimai, žr. [„Talent“ parengimas](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Atostogų tipų apribojimas prašymuose išleisti iš darbo

Organizacijos darbuotojams gali pasiūlyti įvairių tipų atostogų. Tačiau darbuotojai gali neturėti teisės teikti visų atostogų tipų prašymų išleisti iš darbo. Kai kuriuos atostogų tipus gali valdyti Personalo valdymo skyrius (HR). Naudodami šį leidimą galite sukonfigūruoti, kokių atostogų tipų prašymus išleisti iš darbo gali teikti darbuotojai. 

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Peržiūrėkite informaciją apie vadovų savitarnos tiesioginių ir išplėstinių ataskaitų efektyvumą

Nauja parinktis leis vadovams peržiūrėti savo tiesioginių ataskaitų ir išplėstinių ataskaitų efektyvumą. Dabar tiesioginiai vadovai gali priskirti ir atnaujinti veiklos efektyvumo tikslus bei atlikti naujus vertinimus. Be to, tiesioginiai vadovai ir jų darbuotojai gali prižiūrėti ir atnaujinti našumo žurnalus, kad užtikrintų sklandų veiklos efektyvumo vertinimo procesą. Įdiegus šį pakeitimą vadovai be savo tiesioginių ataskaitų galės peržiūrėti ir tvarkyti su efektyvumu susijusią išplėstinių ataskaitų informaciją.
