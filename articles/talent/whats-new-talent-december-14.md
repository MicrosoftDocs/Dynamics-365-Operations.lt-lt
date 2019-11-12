---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent – Core HR“ (2018 m. gruodžio 14 d.)
description: Šioje temoje aprašomos „Microsoft“ sistemos „Dynamics 365 Talent – Core HR“ naujos ir pakeistos funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
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
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c972c04638f436f2fd56055e83bbcf06b29a9f20
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551869"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-december-14-2018"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent – Core HR“ (2018 m. gruodžio 14 d.)

[!include [banner](includes/banner.md)]

**8.1.2085 versija**

Šioje temoje aprašomos naujos ir pakeistos „Core HR“ funkcijos.

## <a name="changes"></a>Pakeitimai

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a>JAV – ACA (įstatymas dėl prieinamos sveikatos priežiūros) palaiko 2018 mokestinių metų 1095-B ir 1095-C formas

Kiekvienais metais „Applicable Large Employers“ (ALE) turi pateikti kiekvieno visą darbo dieną dirbančio darbuotojo 1095-C formą. Be to, jei darbdavys teikia savarankišką draudimą, jis turi pateikti 1095-C (jei jis yra ALE) ir 1095-B (jei jis yra smulkus darbdavys) formą bet kuriam visą darbo dieną arba ne visą darbo dieną dirbančiam darbuotojui, kuriam taikomas vienas iš jo siūlomų sveikatos planų. Ši funkcija numato spausdintines tiek 1095-C, tiek 1095-B formas.

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a>Importuojant nepaisoma lauko SubmittedByPersonId, esančio HcmPerfJournalEntity

Importuojant / eksportuojant našumo žurnalo įrašus, nepaisoma lauko **Pateikė**. Atlikus šį pakeitimą, vertė **importuota / eksportuota** parodys vertę lentelėje eksportuojant, kai importuojama sistema atnaujinama pagal importavimo faile pateiktą vertę.

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a>Darbo srities „Atostogos ir neatvykimai“ analizės skirtuke rodoma ne sistemos administratoriaus vaidmenų klaida „OpenConnectionError“

Įdiegus šį naujinimą, atidarant darbo srities **Atostogos ir neatvykimai** skirtuką **Analizė** nekils jokių klaidų.

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Darbuotojų savitarnos, pareigų hierarchijos išklotinės detalizavimui nepavyksta gauti pirminio mazgo

Atliktas pakeitimas siekiant ištaisyti klaidą „Nepavyko gauti pirminio mazgo“, personalizavus pareigų hierarchiją, kuri turi būti rodoma esamoje darbo srityje, ir pasirinkus pareigas hierarchijoje.  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a>Reikia būti sistemos administratoriumi, norint peržiūrėti puslapyje Pareigos esantį skirtuką Algalapis

Atliktas pakeitimas siekiant įtraukti tinkamus saugos elementus į esamą teisę: „Tvarkyti algalapio darbuotojo ir pareigų informaciją“. Atlikus šį pakeitimą, pagal numatytuosius parametrus algalapio administratorius turės prieigą prie pareigų puslapyje esančių algalapio laukų.

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a>Klaida, kai vadovui pateikiama našumo rezultatų apžvalga ir pateikimo instrukcijose naudojamas vietos rezervavimo ženklas %Reviews.PerfPeriod%

Atliktas pakeitimas, kuris ištaiso klaidą „Nulinė nuoroda“, kai pateikimo instrukcijose naudojamas vietos rezervavimo ženklas %Reviews.PerfPeriod%.

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a>Darbo jėgos „Power BI“ ataskaitoje rodoma klaida, kai darbuotojo paaukštinimo data yra keliamoji diena

Atlikus šį pakeitimą, keliamosios dienos dabar palaikomos „Power BI“.

### <a name="integration-between-core-hr-and-attract"></a>Integravimas tarp „Core HR“ ir „Attract“

Atliktas pakeitimas siekiant atnaujinti su samdytinais kandidatais susijusį integravimą tarp „Core HR“ ir „Attract“. Kad samdytini kandidatai būtų matomi darbo srityje **Personalo valdymas**, naudojami šie „Common Data Service“ objektai.

Prašymas įdarbinti
- Būsenos tipas turi būti nustatytas kaip Pasiūlymas priimtas
-   Pateikiamas kandidatas ir laisva darbo vieta

Pretendentas
-   Pateikiama kandidato informacija

Laisva darbo vieta
-   Pateikiamas laisvos darbo vietos skelbimo ID ir laisvos darbo vietos dalyviai

Laisvos darbo vietos dalyviai
-   Pateikiamas samdos vadovas

Kandidatą įtraukus į personalo valdymą, jo dabar taip pat galima atsisakyti naudojant naują kandidato kortelėje esančią parinktį.

## <a name="coming-soon"></a>Jau greitai

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a>Atostogos ir neatvykimai: būsimų atostogų ir prognozuojamų atostogų balansai

Atlikus pakeitimus tam, kad darbuotojai galėtų prognozuoti ne darbo laiką ir teikti būsimo ne darbo laiko prašymus, taip pat keičiasi būdas, kaip bus rodomi ne darbo laiko balansai, nepaveikiant jų dabartinio ne darbo laiko balansų. 

Šiuo metu rodomas turimas balansas yra prašymams teikti galima ne darbo laiko suma, įskaitant šios dienos kaupimus ir visus patvirtintus atostogų prašymus iki laiko pabaigos. 

Pateikus galimybę prognozuoti, rodomas balansas bus toks, koks bus dabartinis ne darbo laiko balansas, įskaitant šios dienos kaupimus ir šios dienos prašymus. Darbuotojai ir vadovai šiuos atnaujintus balansus matys darbuotojo ir vadovo savitarnos kortelėje **Ne darbo laikas** ir lange **Ne darbo laiko balansai**. Personalo vadovai šiuos atnaujintus balansus matys darbo srityje **Žmonės** ir darbuotojo lange **Priskirti atostogų planai**.

## <a name="known-issue"></a>Žinoma problema

### <a name="mapping-errors-in-the-integration-with-finance"></a>Susiejimo klaidos integruojant su „Finance“

Dabartiniame „Talent“ integravimo su „Dynamics 365 Finance“ šablone buvo nustatytos toliau nurodytos problemos. Netrukus bus paskelbtas naujas šablonas, kurį bus galima taikyti visiems naujai sukurtiems integravimo projektams. Esamiems integravimo projektams užduočių susiejimai gali būti atnaujinti. Atnaujintų susiejimų žr. toliau pateiktoje lentelėje. 

>[!NOTE]
> Neintegruojami pareigų, skirtų pareigų pirminės užduoties priskyrimui, užduoties duomenys. Ši problema šiuo metu sprendžiama. Nėra dabartinio susiejimo problemos sprendimo būdo. 

Padalinių, skirtų valdymo vienetui, užduočiai reikia atnaujinti šiuos susiejimus.

| Esamas šaltinio laukas          | Naujas šaltinio laukas |
| -------------------------------|------------------|
| cdm_description (aprašas)  | cdm_name (pavadinimas)  |

Taip pat reikia įtraukti papildomą susiejimą. Norėdami įtraukti šį susiejimą, pasirinkite paskutinį lauką **Nėra**.

| Šaltinio laukas                   | Paskirties laukas    |
| -------------------------------|----------------------|
| cdm_description (aprašas)  | NAMEALIAS (PAVADINIMO PSEUDONIMAS)|

Atnaujinti susiejimai turėtų atrodyti taip, kaip toliau parodytame paveikslėlyje.

![Padalinių, skirtų valdymo vienetams, užduotis](./media/DepartmentMapping.png)


Pareigų, skirtų pareigų informacijai, užduočiai reikia atnaujinti šiuos susiejimus.

| Esamas šaltinio laukas          | Naujas šaltinio laukas                   |
| -------------------------------|------------------------------------|
| cdm_name (pavadinimas)                | cdm_description (aprašas)      |
| cdm_name (aprašas)         | cdm_jobdescription (užduoties aprašas)|


Atnaujinti susiejimai turėtų atrodyti taip, kaip žemiau parodytame paveikslėlyje.

![Pareigų, skirtų pareigų informacijai, užduotis](./media/JobMapping.png)

Darbuotojų, skirtų darbui, užduočiai reikia atnaujinti šiuos susiejimus.

| Esamas šaltinio laukas                 | Naujas šaltinio laukas                               |
| --------------------------------------|------------------------------------------------|
| cdm_emailaddress1 (1 el. pašto adresas)   | cdm_primaryemailaddress (pagrindinis el. pašto adresas) |
| cdm_telephone1 (1 telefonas)          | cdm_primarytelephone (pagrindinis telefonas)       |

Taip pat reikia atnaujinti lyties lauko transformaciją. Pasirinkite lyties susiejimo tipą **fn** (funkcija) ir atnaujinkite šiuos vertės susiejimus.

| „Common Data Service“ vertė                   | „Finance and Operations“ vertė                     |
| ----------------------------|--------------------------------------------------|
| 75440000                    | Vyras                                             |
| 75440001                    | Moteris                                           |
| 75440002                    | Joks                                             | 
| 75440003                    | Neapibrėžta                                      |

Atnaujinti susiejimai turėtų atrodyti taip, kaip toliau parodytuose paveikslėliuose.

![Darbuotojų, skirtų darbuotojui, užduotis](./media/WorkerMapping.png)

![Lyties lauko transformacija](./media/WorkerTransform.png)
