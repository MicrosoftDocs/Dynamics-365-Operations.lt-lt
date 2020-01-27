---
title: Kas nauja ar pasikeitė „Dynamics 365 for Talent” (2019 m. rugpjūčio 27 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 for Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 8/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: andreabichsel
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-08-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1d7e5be0d9ba5e372e57f06fec77326561196626
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899248"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-august-27-2019"></a>Kas nauja ar pasikeitė „Dynamics 365 for Talent” (2019 m. rugpjūčio 27 d.)

Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 for Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Attract“.

## <a name="changes-in-onboard"></a>Supažindinimo pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Onboard“.

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai

Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2447 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo palaikymo numerius „Microsoft Dynamics Lifecycle Services“ (LCS).

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Peržiūros funkcijos įjungtos tik smėlio dėžės egzemplioriuose

Parengdami naują „Talent“ egzempliorių galite nurodyti egzemplioriaus tipą: Gamyba arba Smėlio dėžė. Naudodami egzempliorių, kurio tipas – Smėlio dėžė, galite pirmieji išbandyti naujas funkcijas. Visi esami „Talent“ egzemplioriai bus atnaujinti ir jų tipas bus Gamyba. Jei norite vieno iš turimų egzempliorių tipą atnaujinti į Smėlio dėžė, kreipkitės į palaikymo tarnybą, kad ši inicijuotų keitimo užklausą.

Daugiau informacijos apie tai, kaip publikuojami pakeitimai, žr. [„Talent“ parengimas](./provisioning-talent.md).

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Peržiūrėkite išsamią informaciją apie vadovų savitarnos efektyvumą

Nauja parinktis leis vadovams peržiūrėti savo tiesioginių ataskaitų ir išplėstinių ataskaitų efektyvumą. Dabar tiesioginiai vadovai gali priskirti ir atnaujinti veiklos efektyvumo tikslus bei atlikti naujus vertinimus. Be to, tiesioginiai vadovai ir jų darbuotojai gali prižiūrėti ir atnaujinti našumo žurnalus, kad užtikrintų sklandų veiklos efektyvumo vertinimo procesą. Įdiegus šį pakeitimą vadovai be savo tiesioginių ataskaitų galės peržiūrėti ir tvarkyti su efektyvumu susijusią išplėstinių ataskaitų informaciją.

### <a name="deleting-legal-entities-isnt-allowed-if-employees-exist-within-the-company-339849"></a>Jei įmonėje yra darbuotojų, juridinių subjektų panaikinti negalima (339849)

Atlikus šį pakeitimą negalima pašalinti arba panaikinti įmonių, jei yra juridinio subjekto darbuotojų ir kitų susijusių duomenų.

### <a name="compensation-management-business-intelligence-analytics-dont-match-on-the-compensation-workspace-322493"></a>Kompensavimo valdymo verslo įžvalgų analizės nesutampa kompensacijos darbo srityje (322493)

Šiame išleidime kompensacijų analizės buvo pakoreguotos, kad tiksliai atspindėtų darbuotojams priskirtus planus.

### <a name="workflow-placeholder-company-displays-dat-when-hiring-employees-through-workflow-343905"></a>Darbo eigos vietos rezervavimo ženklas %įmonė% rodo DAT, kai darbuotojai samdomi naudojant darbo eigą (343905)

Šiame išleidime įmonės vietos rezervavimo ženklas rodo juridinį subjektą, susietą su naujo darbuotojo įdarbinimu.

### <a name="the-cdsjobposition-entity-displays-an-error-when-valid-to-date-is-set-349387"></a>„CDSJobPosition” objektas rodo klaidą, kai nustatyta galiojimo pabaigos data (349387)

Šiame leidime **pareigų informacijos** ir **pareigų trukmės** duomenų šaltiniai objekte **CDSJobPosition** leidžia redagavimus iš „Common Data Service” į **įsigaliojimo datos** laukus. 

### <a name="for-employee-termination-the-last-day-worked-is-populated-on-assignment-end-date-332496"></a>Atleidus darbuotoją, paskutinė dirbta diena yra užpildoma kaip paskyrimo pabaigos data (332496)

Po šio pakeitimo, pareigų **priskyrimo pabaigos data** automatiškai keičiama į **įdarbinimo pabaigos datą**. Įvesdami duomenis galite pakeisti šiuos numatytuosius parametrus.

### <a name="legal-entities-arent-limited-with-hire-338871"></a>Darbuotojams nėra ribojami juridiniai subjektai (338871)
 
Šis pakeitimas apriboja samdos procesą rodyti tik tuos juridinius subjektus, prie kurių vartotojas turi prieigą.  

## <a name="in-preview"></a>Peržiūros režimu

### <a name="streamlined-employee-entry-and-navigation"></a>Supaprastintas darbuotojo įrašo sukūrimas ir naršymas

Ši funkcija dabar yra smėlio dėžės ir bandomosios versijos aplinkose. Norėdami įjungti šią funkciją, pereikite prie **Sistemos administravimas > Saitai > Sąranka > Sistemos parametrai > Peržiūros funkcijos**. Pasirinkite **Patobulintoji darbuotojo forma ir naršymas**. Tai įgalina šiuos pakeitimus visiems vartotojams. Šią parinktį galite bet kuriuo metu išjungti.

Daugiau informacijos žr. [Supaprastintas darbuotojų įrašas ir naršymas](./streamlined-employee-entry.md).

## <a name="coming-soon"></a>Jau greitai

### <a name="platform-update-29"></a>Platformos „update 29“

Daugiau informacijos apie „Platform Update 29“ žr. [Peržiūros funkcijos „Dynamics 365 for Finance and Operations Platform Update 29“ (2019 m. spalio mėn.)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).
