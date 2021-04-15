---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. rugsėjo 16 d.)
description: Šioje temoje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2020 m. rugsėjo 16 d.
author: jcart1106
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bf0e2d90b07cb488429311d04dfbc4d1d3520842
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800098"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. rugsėjo 16 d.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources” funkcijos. Pakeitimai taikomi 8.1.3557 komponavimo versijai. Prie kai kurių funkcijų esantys skaičiai skliausteliuose nurodo „Lifecycle Services“ (LCS) palaikymo numerius kaip nuorodą.

## <a name="included-in-this-release"></a>Kas yra įtraukta į šį leidimą?

-  [Įrašyti rodiniai – bendras pasiekiamumas](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br>- Norėdami gauti išsamesnės informacijos, žr.: [Įrašytos peržiūros](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/saved-views). 

- Formoje **Pareigų veiksmai** yra atnaujintas dimensijų tinklelis ir naujas dialogas (469495).

- Jeigu nustatote **Riboti prieigą prie darbuotojo informacijos** į taip **Išplėstinė prieiga** srityje **Personalo bendri parametrai**, dabar išmokos formose rodomi tik atitinkami darbuotojai (393384).

- Naujo kalendoriaus sukūrimo parinktys **Darbo kalendoriaus** objekte (477055):<br>- Numatytasis pabaigos laikas<br>- Numatytasis pradžios laikas<br>- Ar penktadienis yra darbo diena?<br>- Ar pirmadienis yra darbo diena?<br>- Ar šeštadienis yra darbo diena?<br>- Ar sekmadienis yra darbo diena?<br>- Ar ketvirtadienis yra darbo diena?<br>- Ar antradienis yra darbo diena?<br>- Ar trečiadienis yra darbo diena?<br>- Darbo kalendoriaus atostogų ID

- Objekte **LeaveBankTransactionV1** dabar yra priežasties kodas (477823).

- Dabar galite įrašyti užduočių įrašus (492923).

- Dabar duomenys sėkmingai publikuojami iš **HCMWorkerContactEntity** (427620).

- „FastTab” skirtuke **Kompensacija** dabar rodomi rangovo darbuotojų tipui formoje **Darbuotojo veiksmai** (482494).

- Laukai **Lygis** ir **Planas** dabar yra privalomi, jei nustatysite **Pastoviąją atlyginimo dalį**. Parodomas klaidos pranešimas, jei paliekate šiuos laukus tuščius (482497).

- Laukas **Plano tipas**, esantis skyriuje **Išmokos** dabar yra išplečiamasis sąrašas (488768).

- Sistemos administratoriai dabar gauna pranešimą, jei pasirinktas laukas yra panaikintas iš žmogiškųjų išteklių (481408).

- Nutraukus darbuotojų procesą, personalas elgiasi taip, kaip tikėtasi, o po to, kai ji rodoma užrakinti (479877), nepasikeičia pasirinktoje įmonėje. 

- Vadovai nebegali pridėti numerio stulpelio per personalizavimą (485317).

- Vadovai nebegali pašalinti duomenų diapazono filtro iš identifikacijos numerių, kurių galiojimo laikas baigiasi (485321).

- Kai laukas **Ataskaitos į** yra tuščias, pareigų išsami informacija vis dar rodoma, kai pelės žymeklis užvedamas ant pareigų (433328).

- Darbuotojai dabar gali peržiūrėti išmokų plano informaciją darbuotojų savitarnos tarnyboje (481676).

- Dabar darbuotojai gali matyti visus užregistruotus kursus (429048).

- Dabar galite apriboti peržiūros parinktis **Profesionalių sertifikatų** puslapyje. Galite apriboti peržiūros parinktis dabartiniame juridiniame subjekte pagal darbuotojo būseną ir pagal darbuotojo tipą (451501). 


## <a name="in-preview"></a>Peržiūroje

### <a name="human-resources-app-in-teams"></a>„Human Resources“ programa „Teams“

Darbuotojai gali peržiūrėti ir prašyti atostogų programoje „Microsoft Teams“. Jie gali bendrauti su robotu, kad sukurtų atostogų prašymą. Daugiau informacijos ieškokite:

- [Darbuotojo atostogų ir nebuvomo patirtis „Microsoft Teams“](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) „Dynamics 365“ 2020 leidime bangos 1 plane
- [„Human Resources“ programa „Teams“](https://go.microsoft.com/fwlink/?linkid=2127841) „Human Resources” dokumentacijoje

### <a name="human-resources-app-in-teams-preview-features"></a>„Human Resources“ programėlė „Teams“ peržiūros funkcijose
 
-  **Pranešimai**: ne darbo laiko užklausų pateikėjai ir tvirtintojai bus informuojami „Teams” esančioje „Human Resources” programėlėje. Tvirtintojai gali patvirtinti arba atmesti prašymus išleisti iš darbo. Pateikėjams bus pranešta, ar užklausa buvo patvirtinta, ar atmesta. Daugiau informacijos ieškokite:
   - [Darbuotojo atostogų ir nebuvomo patirtis „Microsoft Teams“](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) „Dynamics 365“ 2020 leidime bangos 2 plane
   - [„Human Resources“ programos „Teams“ pranešimų įjungimas](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) „Human Resources” dokumentacijoje
   - [„Teams” pranešimų įjungimas arba išjungimas atskiriems vartotojams](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) „Human Resources” dokumentacijoje
   - [„Teams” pranešimai](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) „Human Resources” dokumentacijoje
   - [Jūsų komandos atostogų kalendoriaus peržiūra](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) „Human Resources” dokumentacijoje
 
- **Vadovo ne darbo laiko kalendorius**: Vadovai gali peržiūrėti savo tiesioginių ataskaitų kalendoriaus rodinyje patvirtintą ir laukiamą ne darbo laiką. Šis rodinys leidžia lengvai suprasti, kada jų komandos nariai nėra darbe. Daugiau informacijos, žr.:
   - [Darbuotojo atostogų ir nebuvomo patirtis „Microsoft Teams“](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) „Dynamics 365“ 2020 leidime bangos 2 plane
   - [Jūsų komandos atostogų kalendoriaus peržiūra](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) „Human Resources” dokumentacijoje

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Konfigūracijos pasirinktis, skirta sąrašui Man priskirti darbo elementai perkelti (477004)

Nauja parinktis dabar galima norint perkelti sąrašą **Man priskirti darbo elementai** į ataskaitų srities dešinėje pusėje esantį stulpelį. Dėl šio pakeitimo visi darbo elementai ir darbo sąrašai rodomi toje pačioje srityje. Įgalinkite šią funkciją, įjungdami **Peržiūra – darbo eigos patobulinimai** funkcijų valdyme. Daugiau informacijos apie peržiūros funkcijas, žr. skyrių [Funkcijų valdymas](hr-admin-manage-features.md).

Ši funkcija taip pat skatina darbo eigos pasirinktis, kurios rodomos personalo veiksmų formose. Darbo eigos parinktys taip pat rodomos virš veiksmų „FastTab“, skirto sparčiajai prieigai. Daugiau informacijos ieškokite: 

- [Organizacijos ir personalo valdymo darbo eigos patobulinimai](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) „Dynamics 365“ 2020 m. leidimo 2 bangos plane

![Man priskirti darbo elementai](./media/hr-workflow-work-items-assigned-to-me.png)

![Darbo eigos elementų sparčioji prieiga](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a>Atostogų ir neatvykimų kalendorius

Šis leidimas apima papildomas kalendoriaus pasirinktis, skirtas atostogų ir neatvykimų kalendoriams. Daugiau informacijos žr. [Komandos ir įmonės kalendorių peržiūra](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-calendar).

## <a name="coming-soon"></a>Jau greitai

### <a name="checklist-entities-included-in-dataverse"></a>Kontrolinio sąrašo objektai, nurodyti „Dataverse”

Tikrinimo objektai Įtraukimo, Atleidimo, Perleidimo ir Verslo procesams bus greitai prieinami „Dataverse“.

### <a name="benefits-management-reason-codes"></a>Išmokų valdymo priežasčių kodai

Išmokų valdymo priežasčių kodai netrukus bus sujungti su esamais „Human Resources” priežasčių kodais. Jei išmokų valdyme sukūrėte priežasčių kodų, kurie sudaryti iš daugiau nei 15 simbolių, turite pakeisti priežasties kodo pavadinimą išmokų valdymo formoje **Priežasčių kodai**, kad jį sudarytų 15 ar mažiau simbolių. Atnaujinus pavadinimą, priežasties kodas atsiras esamoje priežasties kodo formoje personalo valdyme. Šis pakeitimas bus prieinamas ateityje ir neturės įtakos jau esamoms funkcijoms.

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]