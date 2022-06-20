---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. rugsėjo 03 d.)
description: Šiame straipsnyje aprašomos priemonės, kurios yra naujos arba pakeistos programoje Microsoft Dynamics 365 Human Resources 2020 m. spalio 3 d.
author: andreabichsel
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7d558f4b0ddb3e8fe3479567483e2c2349a40774
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891356"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. rugsėjo 3 d.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Šiame straipsnyje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources“ funkcijos. Pakeitimai taikomi 8.1.3504 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo „Lifecycle Services“ (LCS) palaikymo numerius kaip nuorodą.

Daugiau informacijos apie būsimas „Human Resources” funkcijas žr. [„Dynamics 365 Human Resources” 2019 m. leidimo 2 bangos apžvalga](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/). Daugiau informacijos apie „Human Resources” atnaujinimo procesą žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

## <a name="in-this-release"></a>Šiame leidime

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a>Naujas numatytųjų finansinių dimensijų tinklelis ir dialogo lango šablonas visoje „Human Resources” (469495)

Naujas finansinių dimensijų šablonas dabar prieinamas toliau pateiktose srityse.

- Pareigų veiksmai (forma: **HcmPositionActionDetail**)
- Algalapių pajamų kodai (forma: **PayrollEarningCode**)

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a>Įrašai įmonės atostogų kalendoriuje nerodomi, jei neįjungta parinktis Atostogų ir neatvykimų kalendoriaus patobulinimai (484406)

Šiame leidime išspręsta problema, kai atostogų įrašai nerodomi įmonės atostogų kalendoriuje. Ši problema kyla tik tada, kai funkcijų valdymo parinktis **Atostogų ir neatvykimų kalendoriaus patobulinimai** neįjungta.

### <a name="benefitplanemployeeentity-issue-467597"></a>Problema BenefitPlanEmployeeEntity (467597)

Šiame leidime išspręsta objekto **BenefitsPlanEmployee** problema. Importuojant darbininkų registracijų galiojimą, **Padengimo kodas** ir **Plano tipo kodas** dabar nustatomi teisingai. Dėl šios problemos, darbuotojų išmokų planai buvo rodomi neteisingai formose **Darbininkų išmokų planas** ir **Atvira registracija** darbuotojų savitarnoje.

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a>Elektroninio failo 1094-C išvestyje trūksta raidės XML (435190)

Šis pakeitimas pataiso problemą, kai 1094-C išvesties faile trūksta simbolio, kurio reikia pateikiant IRS.

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a>Darbuotojo kintamosios atlyginimo dalies lentelė susieta su pastoviosios atlyginimo dalies forma (476117)

Šis pakeitimas suderina pastoviosios atlyginimo dalies laukus su pastoviosios atlyginimo dalies forma. Kintamosios atlyginimo dalies laukai dabar galimi tik su kintamosios atlyginimo dalies forma.

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a>Atostogų užklausos leidžiamos prieš registraciją, jei to atostogų tipo minimalus balansas yra neigiamas (469917)

Šis pakeitimas draudžia įvesti atostogų užklausas prieš užregistravimą plane, net jei registracijos minimalus balansas yra neigiamas. Galite įvesti arba pateikti užklausas tik tada, kai planas aktyvus.

### <a name="document-templates-dont-download-457279"></a>Nepavyksta atsisiųsti dokumentų šablonų (457279)

Dėl šio pakeitimo galite atsisiųsti visus dokumentų šablonus. 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a>Duomenys rodomi kaip stulpelių antraštės, o ne lauko Užmokesčio tarifas eilutės, atlyginimo dalies plano ataskaitoje (476077)

Analizės ataskaitoje dabar rodoma tinkama **Užmokesčio tarifas** informacija.

## <a name="in-preview"></a>Peržiūros režimu

### <a name="human-resources-application-in-teams"></a>„Human Resources“ programa programoje „Teams“

Darbuotojai gali peržiūrėti ir prašyti atostogų programoje „Microsoft Teams“. Jie gali bendrauti su robotu, kad sukurtų atostogų prašymą. Daugiau informacijos ieškokite:

- [Darbuotojo atostogų ir nebuvimo patirtis „Microsoft Teams“](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) „Dynamics 365“ 2020 leidime bangos 1 plane
- [„Human Resources“ programa „Teams“](./hr-admin-teams-leave-app.md) „Human Resources” dokumentacijoje

### <a name="human-resources-app-in-teams-preview-features"></a>„Human Resources“ programėlė „Teams“ peržiūros funkcijose
 
-  **Pranešimai**: ne darbo laiko užklausų pateikėjai ir tvirtintojai bus informuojami „Teams” esančioje „Human Resources” programėlėje. Tvirtintojai galės patvirtinti arba atmesti prašymus išleisti iš darbo. Pateikėjams bus pranešta, ar užklausa buvo patvirtinta, ar atmesta. Daugiau informacijos ieškokite:
   - [Darbuotojo atostogų ir nebuvimo patirtis „Microsoft Teams“](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) „Dynamics 365“ 2020 leidime bangos 2 plane
   - [„Human Resources“ programos „Teams“ pranešimų įjungimas](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) „Human Resources” dokumentacijoje
   - [„Teams” pranešimų įjungimas arba išjungimas atskiriems vartotojams](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) „Human Resources” dokumentacijoje
   - [„Teams” pranešimai](./hr-teams-leave-app.md#respond-to-teams-notifications) „Human Resources” dokumentacijoje
   - [Jūsų komandos atostogų kalendoriaus peržiūra](./hr-teams-leave-app.md#view-your-teams-leave-calendar) „Human Resources” dokumentacijoje
 
- **Tvarkytuvo ne darbo laiko kalendorius**: vadovai galės peržiūrėti savo tiesioginių ataskaitų kalendoriaus rodinyje patvirtintą ir laukiamą ne darbo laiką. Šis rodinys leidžia lengvai suprasti, kada jų komandos nariai nėra darbe. Daugiau informacijos, žr.:
   - [Darbuotojo atostogų ir nebuvimo patirtis „Microsoft Teams“](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) „Dynamics 365“ 2020 leidime bangos 2 plane
   - [Jūsų komandos atostogų kalendoriaus peržiūra](./hr-teams-leave-app.md#view-your-teams-leave-calendar) „Human Resources” dokumentacijoje

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Konfigūracijos pasirinktis, skirta sąrašui Man priskirti darbo elementai perkelti (477004)

Nauja parinktis dabar galima norint perkelti sąrašą **Man priskirti darbo elementai** į ataskaitų srities dešinėje pusėje esantį stulpelį. Dėl šio pakeitimo visi darbo elementai ir darbo sąrašai rodomi toje pačioje srityje. Įgalinkite šią funkciją, įjungdami **Peržiūra – darbo eigos patobulinimai** funkcijų valdyme. Daugiau informacijos apie peržiūros funkcijas, žr. skyrių [Funkcijų valdymas](hr-admin-manage-features.md).

Ši funkcija taip pat skatina darbo eigos pasirinktis, kurios rodomos personalo veiksmų formose. Darbo eigos parinktys taip pat rodomos virš veiksmų „FastTab“, skirto sparčiajai prieigai. Daugiau informacijos ieškokite: 

- [Organizacijos ir personalo valdymo darbo eigos patobulinimai](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) „Dynamics 365“ 2020 m. leidimo 2 bangos plane

![Man priskirti darbo elementai.](./media/hr-workflow-work-items-assigned-to-me.png)

![Darbo eigos elementų sparčioji prieiga.](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a>Jau greitai

### <a name="checklist-entities-included-in-dataverse"></a>Kontrolinio sąrašo objektai, nurodyti „Dataverse”

Tikrinimo objektai Įtraukimo, Atleidimo, Perleidimo ir Verslo procesams bus greitai prieinami „Dataverse“.

### <a name="benefits-management-reason-codes"></a>Išmokų valdymo priežasčių kodai

Išmokų valdymo priežasčių kodai netrukus bus sujungti su esamais „Human Resources” priežasčių kodais. Jei išmokų valdyme sukūrėte priežasčių kodų, kurie sudaryti iš daugiau nei 15 simbolių, turite pakeisti priežasties kodo pavadinimą išmokų valdymo formoje **Priežasčių kodai**, kad jį sudarytų 15 ar mažiau simbolių. Atnaujinus pavadinimą, priežasties kodas atsiras esamoje priežasties kodo formoje personalo valdyme. Šis pakeitimas bus prieinamas ateityje ir neturės įtakos esamoms funkcijoms.

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
