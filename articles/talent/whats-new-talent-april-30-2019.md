---
title: Kas nauja arba pasikeitė „Dynamics 365 Talent” (2019 m. balandžio 30 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 04/30/2019
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
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2539baba84bffeb21d351cc307191eea3e940515
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528200"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-30-2019"></a>Kas nauja arba pasikeitė „Dynamics 365 Talent” (2019 m. balandžio 30 d.)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Attract“.

## <a name="changes-in-onboard"></a>Supažindinimo pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Onboard“.

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai

Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2270 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo palaikymo numerius „Microsoft Dynamics Lifecycle Services“ (LCS).

### <a name="provide-feedback"></a>Pateikite atsiliepimą

Parinktis teikti atsiliepimą yra „Talent“ meniu **Žinynas** (**?**). Šis meniu suteikia prieigą prie šių išteklių:

- Grižt. ryšys
- Žinynas
- Pradžia
- Pagalba
- Idėjos
- Apie

### <a name="improvements-to-the-user-interface-for-duplicate-employee-detection"></a>Darbuotojų dublikatų aptikimo vartotojo sąsajoje patobulinimai

Dėl šio pakeitimo dublikatai dabar aptinkami, kai nustatote pavadinimo laukus, o būsenos indikatorius rodo aptiktų dublikatų skaičių. Pateiktas saitas atidaro puslapį, kuriame galima įvertinti, ar reikia naudoti vieną iš dublikatų. Dublikatų puslapis nėra atidaromos automatiškai, kad nebūtų trukdoma įvesti duomenis. Turite pasirinkti saitą, kad atidarytumėte puslapį.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service objekto palaikymas pasirinktiniams laukams

Šios savaitės leidime, šie objektai dabar palaiko įprastus laukus: Užimtumas, Išmokos tipas ir Apmokėjimo ciklas.

### <a name="an-error-occurs-when-an-off-boarding-checklist-is-assigned-299877"></a>Įvyksta klaida, kai priskiriamas atleidimo kontrolinis sąrašas (299877)

Šis pakeitimas ištaiso klaidos pranešimą, kuris atsiranda paskiriant atleidimo kontrolinį sąrašą darbuotojui, kuris nedalyvauja atleidimo procese.

### <a name="the-exited-workers-link-opens-the-wrong-worker-309939"></a>Atleistų darbuotojų saitas atidaro netinkamą darbuotoją (309939)

Šis pakeitimas pataiso problemą, kuri kyla, kai iš naujo samdote kito juridinio subjekto darbuotoją ir bandote pereiti prie darbuotojo atleistų darbuotojų sąraše.

### <a name="the-employee-self-service-compensation-card-doesnt-show-summary-values-when-advanced-security-is-turned-on-315231"></a>Darbuotojo savarankiškos kompensacijos kortelėje nerodomos suvestinės vertės, kai įjungiama išplėstinė sauga (315231)

Šis pakeitimas pataiso problemą, kuri kyla naudojant išplėstinę kompensacijos saugą. Kai įjungta išplėstinė sauga darbuotojo savitarnoje nuo šiol rodomos darbuotojų ir vadovų kompensacijų sumos. Prieš šį pakeitimą suvestinės vertės buvo rodomos kaip 0 (nulis).

### <a name="if-a-position-without-a-title-is-created-in-common-data-service-no-position-is-created-in-talent-314562"></a>Jeigu pareigos be pavadinimo sukuriamos „Common Data Service“, pareigos nesukuriamos programoje „Talent“ (314562)

Šios savaitės pakeitimai ištaiso problemą, kuri kyla kuriant pareigas „Common Data Service“, bet nenurodant pavadinimo.

### <a name="error-message-in-performance-journal-entries-in-employee-self-service-314134"></a>Klaidos pranešimas našumo žurnalų įrašuose darbuotojo savitarnoje (314134)

Šis pakeitimas ištaiso problemą, kuri atsiranda, kai prie našumo žurnalo įrašų pridedate našumo tikslus darbuotojų savitarnoje.

## <a name="in-preview"></a>Peržiūros režimu

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Leidimas nedarbo laiko tipuose nurodyti priežasčių kodus

Organizacijoms gali prireikti papildomos informacijos, susijusios su nedarbo laiko užklausomis. Dabar galite nurodyti nedarbo laiko tipų priežasties kodus ir leisti darbuotojams pasirinkti priežasties kodą savo nedarbo laiko užklausose.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Reikalavimas pateikti priežasties kodus, skirtus tam tikriems nedarbo laiko tipams nedarbo laiko užklausose

Organizacijos gali norėti priežasčių kodus priskirti tam tikriems nedarbo laiko tipams, kai darbuotojai teikia nedarbingumo užklausas. Šis reikalavimas gali būti dėl įmonės strategijos arba reguliavimo reikalavimų. Dabar galite nurodyti, kokių tipų nedarbo laiko priežasties kodus reikia pateikti, ir galite reikalauti darbuotojų pateikti nedarbo laiko tipo priežasties kodą savo nedarbo laiko užklausose.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Nedarbo laiko ir neatvykimo operacijų sąrašo pateikimas personalo skyriui

Galimybė sekti darbuotojų nedarbo laiką ir suprasti, kaip skaičiuojamas nedarbo laikas, ne tik padeda žmogiškųjų išteklių (HR) skyriui atsakyti į darbuotojų klausimus, bet ir padeda užtikrinti tikslias darbuotojų nedarbo laiko premijas. Dabar HR suteikta prieiga prie naujo operacijų (subsidijų, kaupimų ir užklausų) rodinio, kad HR darbuotojai galėtų sužinoti likučių priežastis.

## <a name="coming-soon"></a>Jau greitai

### <a name="email-support-for-alerts"></a>Įspėjimų el. pašto palaikymas

Platformos 26 naujinime „Finance and Operations“, naudotojai gali sukurti pranešimo taisykles, kurios automatiškai siunčia el. pašto pranešimus į kontaktus, kai įvykis įjungia pranešimus.


[!INCLUDE[footer-include](../includes/footer-banner.md)]