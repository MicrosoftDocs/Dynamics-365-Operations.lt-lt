---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent“ (2019 m. rugsėjo 10 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 for Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 9/10/2019
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
ms.search.validFrom: 2019-09-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0aadecd5b37759492f7895ccfda1a777793a08b3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461988"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-september-10-2019"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent“ (2019 m. rugsėjo 10 d.)

Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 for Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai

### <a name="candidate-e-mail-login"></a>Kandidato el. pašto prisijungimas

Dabar kandidatai gali naudoti bet kurį el. pašto adresą, kad sukurtų paskyrą ir prisijungtų prie „Talent“ karjeros svetainės, teiktų prašymus dėl darbo ir pasitikrintų prašymų būseną. Ši funkcija papildo funkciją, kurią naudojant anksčiau buvo galima prisijungti prie „Talent“ karjeros svetainės naudojantis socialinėmis paskyromis arba organizacijų kredencialais.

### <a name="job-activation-and-posting"></a>Užduočių aktyvinimas ir registravimas

Įgyvendinome keletą užduočių aktyvinimo ir registravimo keitimų. Jums reikia suaktyvinti užduotis prieš išsiunčiant jas į „Talent“ karjeros svetainę arba į bet kurias išorines darbo sritis, įskaitant „LinkedIn“ arba „Broadbean“.

## <a name="changes-in-onboard"></a>Supažindinimo pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Onboard“.

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai

Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2482 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo palaikymo numerius „Microsoft Dynamics Lifecycle Services“ (LCS).

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>Peržiūros funkcijas galite įjungti smėlio dėžės ir bandomosiose aplinkose

Parengdami naują „Talent“ egzempliorių galite nurodyti egzemplioriaus tipą: Gamyba arba Smėlio dėžė. Naudodami egzempliorių, kurio tipas – Smėlio dėžė, galite pirmieji išbandyti naujas funkcijas. Jei norite vieno iš turimų egzempliorių tipą atnaujinti į Smėlio dėžė, kreipkitės į palaikymo tarnybą, kad ši inicijuotų keitimo užklausą.

Daugiau informacijos apie tai, kaip publikuojami pakeitimai, žr. [„Talent“ parengimas](./provisioning-talent.md).

### <a name="platform-update-29"></a>Platformos „update 29“

Daugiau informacijos apie „Platform Update 29“ žr. [Peržiūros funkcijos „Dynamics 365 for Finance and Operations Platform Update 29“ (2019 m. spalio mėn.)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).

### <a name="new-job-base-entity-available-in-data-management-framework-347202"></a>Naujas užduoties pagrindinis objektas duomenų valdymo sistemoje (347202)

Šiame leidime pateikiamas naujas pagrindinis užduoties objektas, naudojamas importuojant / eksportuojant duomenis. 

### <a name="worker-advanced-security-policy-incorrectly-displays-positions-in-position-hierarchy-354868"></a>Darbininkų išplėstinėje saugos strategijoje netinkamai rodomos pareigų hierarchijos pareigos (354868)

Šiame leidime „tuščias“ darbininkas nebebus rodomas pareigose, kai vartotojų prieiga apribota.

### <a name="job-form-close-box-wont-close-form-in-certain-situations-342467"></a>Užduoties formos uždarymo langeliu tam tikrose situacijose forma neuždaroma (342467)

Į šį leidimą įtrauktas keitimas, kuris leidžia užduoties formą uždaryti visais atvejais.

### <a name="new-case-on-employee-record-is-locked-for-human-resources-manager-role-337111"></a>Naujas atvejis darbuotojo įraše yra skirtas tik personalo valdymo vaidmeniui (337111)

Įgyvendinus šį pakeitimą, atvejų valdymo forma nebėra užrakinta, kai ji pasiekiama naudojant darbuotojo formą.

### <a name="employment-end-date-always-defaults-to-235959-351492"></a>Įdarbinimo pabaigos data visada nustatoma kaip 23:59:59 (351492)

Su šiuo pakeitimu galite pakeisti įdarbinimo datą, kad ji skirtųsi nuo 23:59:59, kai įdarbinimas baigiamas neautomatiniu būdu.

### <a name="unable-to-set-up-expiration-date-on-an-earning-code-through-data-management-336604"></a>Neįmanoma nustatyti pajamų kodo galiojimo pabaigos datos naudojant duomenų valdymą (336604)

Šiame leidime galite nustatyti besibaigiančių pajamų kodus, naudodami objektą **PayrollWorkerPositionEarningCodeEntity**.

### <a name="employee-development-analytic-report-doesnt-display-data-348737"></a>Darbuotojo tobulinimo analitinėje ataskaitoje nerodomi duomenys (348737)

Šios savaitės versijoje darbuotojų įgūdžių analizė buvo atnaujinta, kad būtų teikiami tikslūs pranešimai.

### <a name="terms-of-employment-datetime-dont-default-to-beginning-of-day-349101"></a>Įdarbinimo sąlygų data / laikas pagal numatytuosius nustatymus neatitinka dienos pradžios (349101)

Įgyvendinus šį pakeitimą, pradžios data / laikas dabar pagal numatytuosius nustatymus atitinka dienos pradžią, o pabaigos data / laikas pagal numatytuosius nustatymus atitinka dienos pabaigą.

### <a name="changing-the-employment-end-date-on-worker-action-form-displays-an-error-354092"></a>Pakeitus darbininko veiksmo formos įdarbinimo pabaigos datą, rodoma klaida (354092) 

Šis pakeitimas pataiso problemą, kylančia keičiant įdarbinimo pabaigos datą atliekant su darbininku susijusius veiksmus.

### <a name="applying-onboarding-checklists-across-companies-338433"></a>Visų įmonių supažindinimo kontrolinių sąrašų taikymas (338433)

Šiame leidime dabar suteikiama galimybė taikyti kontrolinius sąrašus darbuotojams, kurie yra įdarbinti kituose juridiniuose subjektuose, o ne prisijungusiame juridiniame subjekte.

## <a name="in-preview"></a>Peržiūros režimu

### <a name="streamlined-employee-entry-and-navigation"></a>Supaprastintas darbuotojo įrašo sukūrimas ir naršymas

Ši funkcija dabar yra smėlio dėžės aplinkose. Norėdami įjungti šią funkciją, pereikite prie **Sistemos administravimas > Saitai > Sąranka > Sistemos parametrai > Peržiūros funkcijos**. Pasirinkite **Patobulintoji darbininko forma ir naršymas**. Tai įgalins šiuos pakeitimus visiems vartotojams. Šią parinktį galite bet kuriuo metu išjungti.

Daugiau informacijos žr. [Supaprastintas darbuotojų įrašas ir naršymas](./streamlined-employee-entry.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]