---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent“ (2019 m. gegužės 13 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 for Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 05/13/2019
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
ms.search.validFrom: 2019-05-13
ms.dyn365.ops.version: Talent
ms.openlocfilehash: dac453ee83492655b6681b9784af4712bf39fc2a
ms.sourcegitcommit: 2bbc0eeca6826c529fb729b82d16f287c1ce05bb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/16/2019
ms.locfileid: "1591507"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-may-13-2019"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent“ (2019 m. gegužės 13 d.)

[!include [banner](includes/banner.md)]

Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 for Talent“ funkcijos.

## <a name="coming-soon-in-attract"></a>Jau greitai „Attract“

### <a name="job-approvals-on-home-page"></a>Užduočių patvirtinimai pagrindiniame puslapyje

Patvirtinimai rodomi ataskaitų srities skyriuje **Patvirtinimai**. Tvirtintojai gali peržiūrėti jiems priskirtą patvirtinimą dalyje **Priskirta jums**, kurioje nurodomas užduoties ID, pavadinimas, kiti tvirtintojai ir priskirta data. Vartotojai, pateikę užduotį patvirtinimui, gali peržiūrėti savo užduotis dalyje **Jūsų užklausos**, kurioje nurodomi pateiktos užduoties dar nepatvirtinę tvirtintojai.

## <a name="changes-in-onboard"></a>Supažindinimo pakeitimai

Šiame leidime įtraukti smulkūs klaidų ištaisymai, skirti „Dynamics 365 Talent: Onboard“

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai

Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2297 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo palaikymo numerius „Microsoft Dynamics Lifecycle Services“ (LCS).

### <a name="indicate-instance-type-when-provisioning-talent"></a>Nurodykite egzemplioriaus tipą rengdami „Talent“

Kuriant naują „Talent“ egzempliorių galima nurodyti, ar egzemplioriaus tipas yra **Gamyba** ar **Smėlio dėžė**, kad būtų galima iš anksto patikrinti naujas funkcijas. Visi esami „Talent“ egzemplioriai bus atnaujinti ir jų tipas bus **Gamyba**. Jei norite, kad vieno iš esamų egzempliorių tipas būtų atnaujintas į **Smėlio dėžė**, kreipkitės į [Palaikymo tarnybą](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/talent-support), kad ši inicijuotų keitimo užklausą.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service objekto palaikymas pasirinktiniams laukams

Šios savaitės leidime nuo šiol palaikomi šių „Common Data Service“ objektų pasirinktiniai laukai: Įdarbinimas, Išmokos apskaičiavimo dažnis, Išmokos apskaičiavimo koeficientas, Darbo kalendorius atostogos ir Identifikacijos tipas.

### <a name="common-data-service-integration-page"></a>„Common Data Service“ integravimo puslapis

Šiame leidime pateikiama nauja parinktis **Sistemos administravimas > Saitai > Integravimai > „Common Data Service“ konfigūracija**. Parinktis **„Common Data Service“ konfigūracija** suteikia administratoriui arba duomenų valdymo administratoriui tam tikro lankstumo ir įžvalgų naudojantis „Common Data Service“. Naudodamiesi šia parinktimi galite įjungti arba išjungti „Common Data Service“ integravimą su „Talent“ egzemplioriumi ir peržiūrėti informaciją apie „Talent“ egzemplioriaus sinchronizavimą su „Common Data Service“.

### <a name="import-performance-data-with-final-employee-rating-316710"></a>Našumo duomenų su galutiniu darbuotojo įvertinimu importavimas (316710)

Šiame leidime galite importuoti retrospektyvinius darbuotojo vertinimo duomenis. Lauke **FinalEmployeeRatingId** dabar suteikiama rašymo teisė.

### <a name="cant-create-worker-address-in-common-data-service-and-sync-it-with-talent-317555"></a>Nepavykta sukurti darbininko adreso naudojantis „Common Data Service“ ir susinchronizuoti su „Talent“ (317555)

Atlikus šį pakeitimą, naudojantis „Common Data Service“ sukurtus adresų duomenis galima sinchronizuoti su „Talent“.

## <a name="in-preview"></a>Peržiūros režimu

### <a name="new-page-to-validate-position-hierarchy-data"></a>Naujas puslapis, skirtas tikrinti pareigų hierarchijos duomenis

Personalo (HR) skyrius ir administratoriai gali tikrinti visą valdybos hierarchiją, ar joje nėra netyčia importuotų ciklinių nuorodų. Galite pasiekti naują puslapį dalyje **Organizacijos administravimas > Saitai > Pareigos > Pareigų hierarchijos tikrinimas**.

### <a name="specify-reason-codes-on-leave-types"></a>Nurodykite atostogų tipų priežasties kodus

Organizacijoms gali prireikti papildomos informacijos, susijusios su nedarbo laiko užklausomis. Dabar galite nurodyti nedarbo laiko tipų priežasties kodus ir leisti darbuotojams pasirinkti priežasties kodą savo nedarbo laiko užklausose.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Reikalavimas pateikti priežasties kodus, skirtus tam tikriems nedarbo laiko tipams nedarbo laiko užklausose

Organizacijos gali norėti priežasčių kodus priskirti tam tikriems nedarbo laiko tipams, kai darbuotojai teikia nedarbingumo užklausas. Šis reikalavimas gali būti dėl įmonės strategijos arba reguliavimo reikalavimų. Galite nurodyti, kokių tipų nedarbo laiko priežasties kodus reikia pateikti, ir galite reikalauti darbuotojų pateikti nedarbo laiko tipo priežasties kodą savo nedarbo laiko užklausose.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Nedarbo laiko ir neatvykimo operacijų sąrašo pateikimas personalo skyriui

Galimybė sekti darbuotojų nedarbo laiką ir suprasti, kaip skaičiuojamas nedarbo laikas, ne tik padeda personalo skyriui atsakyti į darbuotojų klausimus, bet ir padeda užtikrinti tikslias darbuotojų nedarbo laiko premijas. Dabar HR suteikta prieiga prie naujo operacijų (subsidijų, kaupimų, koregavimų ir užklausų) rodinio, kad HR darbuotojai galėtų sužinoti nebuvimo balansų priežastis.
