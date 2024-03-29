---
title: Kas nauja ar pasikeitė „Dynamics 365 Human Resources” (2020 m. rugpjūčio 20 d.)
description: Šiame straipsnyje aprašomos priemonės, kurios yra naujos arba pakeistos Microsoft Dynamics 365 Human Resources 2020 m. rugpjūčio 20 d.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3c71a742022afba36c417092d5a9b75c78600357
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902175"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a>Kas nauja ar pasikeitė „Dynamics 365 Human Resources” (2020 m. rugpjūčio 20 d.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Šiame straipsnyje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources“ funkcijos. Pakeitimai taikomi 8.1.3478 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo „Lifecycle Services“ (LCS) palaikymo numerius kaip nuorodą.

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a>Būsimų ir laukiamų atostogų laiko informacijos rodymas kortelėms, esančioms darbo srityje Žmonės

Laukiamų ir būsimų atostogų užklausos pasirinktys dabar pasiekiamos atostogų ir neatvykimų kortelėse, esančiose darbo srityje **Žmonės**.

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a>Asmeninis laukas nėra „Taip” pagal numatytuosius parametrus darbuotojo vaidmeniui darbuotojų savitarnoje (477106)

**Asmeninis** laukas dabar nustatomas kaip **Taip**, kai darbuotojai įtraukia naujus adresų įrašus darbuotojų savitarnos **Asmeninės informacijos** puslapyje. 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a>Kandidatai samdyti „FastTab” personalo valdyme, parodo neteisingą kandidatų skaičių (470110)

**Personalo valdymo** puslapyje dabar tiksliai rodomas samdomų kandidatų skaičius. 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a>Negalima įvesti ligos, skirtos atleistam darbuotojui, kai kaupimas nustatytas kaip nulis (446195)

Dabar atostogų operacijos leidžiamos darbuotojams, kurie bus atleisti ateityje, o kaupimas nustatytas kaip nulis. Atostogų operacijos gali būti įvestos iki darbuotojo atleidimo datos. 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a>Pasirinktinių laukų įtraukimas į naują darbininko formą išjungia atostogų tvarkymo laukus veiksmų srityje (473314)

Veiksmų srities parinktys naujoje **Darbininko** formoje, **Tvarkyti atostogas** parinktyje, nebus išjungtos, jei pasirinktiniai laukai buvo įtraukti į naują **Darbininko** formą.

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a>Darant atostogų komentarų lauką privalomą, leidžiama pateikti atostogų užklausą, kai neįvesta jokių komentarų (473543)

Komentarų laukai dabar gali būti privalomi, o atostogų užklausos atsižvelgia į šį parametrą. Privalomi laukai yra peržiūros funkcija.

### <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF objektas pasiekiamas kaupimo sustabdymams

DMF objektas dabar pasiekiamas kaupimo sustabdymams.

## <a name="in-preview"></a>Peržiūros režimu

### <a name="mandatory-fields"></a>Privalomi laukai

Galite nustatyti laukelius privalomais naudodami Žmogiškųjų išteklių personalizavimo galimybes. Šiai funkcijai reikia **Įrašyti rodiniai**. Dėl platesnės informacijos apie įrašytas peržiūras, žr.:

- [Įrašytos peržiūras - bendras prieinamumas](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) „Dynamics 365 2020“ leidime bangos 2 planas
- [Formų, kurios visiškai išnaudoja įrašytus rodinius, kūrimas](../fin-ops-core/dev-itpro/user-interface/understanding-saved-views.md)

### <a name="human-resources-application-in-teams"></a>„Human Resources“ programa programoje „Teams“

Darbuotojai gali peržiūrėti ir prašyti atostogų programoje „Microsoft Teams“. Jie gali bendrauti su robotu, kad sukurtų atostogų prašymą. Daugiau informacijos ieškokite:

- [Darbuotojo atostogų ir nebuvimo patirtis „Microsoft Teams“](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) „Dynamics 365“ 2020 leidime bangos 1 plane
- [„Human Resources“ programa „Teams“](./hr-admin-teams-leave-app.md)

## <a name="coming-soon"></a>Jau greitai

### <a name="human-resources-app-in-teams-preview-features"></a>„Human Resources“ programėlė „Teams“ peržiūros funkcijose
 
-  **Pranešimai**: ne darbo laiko užklausų pateikėjai ir tvirtintojai bus informuojami „Teams” esančioje „Human Resources” programėlėje. Tvirtintojai galės patvirtinti arba atmesti ne darbo laiko užklausas, o pateikėjai bus informuojami, jei užklausa buvo patvirtinta arba atmesta.
 
- **Tvarkytuvo ne darbo laiko kalendorius**: vadovai galės peržiūrėti savo tiesioginių ataskaitų kalendoriaus rodinyje patvirtintą ir laukiamą ne darbo laiką. Šis rodinys leidžia lengvai suprasti, kada jų komandos nariai nėra darbe.

### <a name="checklist-entities-included-in-dataverse"></a>Kontrolinio sąrašo objektai, nurodyti „Dataverse”

Tikrinimo objektai Įtraukimo, Atleidimo, Perleidimo ir Verslo procesams bus greitai prieinami „Dataverse“.

## <a name="known-issues"></a>Žinomos problemos

**Ateities valdymas** darbo sritis gali rodyti funkcijas, kurios yra išjungtos kaip peržiūros funkcijos joms bendrai esant įjungtoms. Toliau pateiktas bendras esamų funkcijų sąrašas, rodantis neteisingą statusą. 

- Išmokų valdymas
- Atvejų valdymas
- Duomenų įrašymas (auditavimas)
- Atostogų skaičiavimas vienai bendrai ar vienam planui
- Atostogų ir nebuvimo skaičiavimo sustabdymas
- Balanso keitimo priežasties kodas ir komentaras
- Atostogų pirkimas ir pardavimas
- Atostogų ir nebuvimo kalendorius
- Atostogų turėjimo perdavimo taisyklės
- Atostogų skaičiavimo auditas
- Atostogų skaičiavimo pašalinimas
- Atostogų skaičiavimo apvalinimas
- Konfigūruoti keletą atostogų tipų viename atostogų plane
- Atnaujinti nedirbamo laiko papildymus
- Naudoti darbuotojo FTE apskaičiavimams
- Kryžminės bendrovės kompensavimo peržiūra
- Veiklos efektyvumo vertinimų spausdinimas
- Atostogų kaupimo šventinių dienų taisymai

### <a name="benefit-plan-employee-entity"></a>Darbuotojų Išmokų plano objektas 

Neseniai aptikome dvi problemas, susijusias su **DarbuotojųIšmokųPlano** objektu. Importuojant darbininkų registracijų galiojimą, **Padengimo kodas** ir **Plano tipo kodas** nustatomi neteisingai. Dėl šios problemos, darbuotojų išmokų planai rodomi neteisingai **Darbininkų išmokų plano** formoje ir **Atviros registracijos** formoje darbuotojų savitarnoje. Ši problema taip pat gali paveikti darbuotojo gebėjimą pasirinkti planus darbuotojų savitarnoje. Šiuo metu nėra problemos sprendimo būdo. Mes laikome tai kaip aukšto prioriteto pataisą ir pristatysime šią pataisą kitame leidime.

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]