---
title: Kas nauja arba pasikeitė „Dynamics 365 Human Resources” (2020 m. balandžio 3 d.)
description: Šiame straipsnyje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2020 m. balandžio 3 d.
author: andreabichsel
ms.date: 04/03/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 08059e38bed2f9daf4c5ff86f9e1cf33e1211785
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892038"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-3-2020"></a>Kas nauja arba pasikeitė „Dynamics 365 Human Resources” (2020 m. balandžio 3 d.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šiame straipsnyje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources“ funkcijos. Pakeitimai taikomi 8.1.3111 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo „Lifecycle Services“ (LCS) palaikymo numerius kaip nuorodą.

## <a name="features-that-are-generally-available-the-week-of-april-6"></a>Funkcijos, kurios visiems prieinamos balandžio 6 d. savaitę

- **Atostogų ir neatvykimų funkcijos** – daugiau informacijos žr. [Atostogų ir neatvykimo apžvalga](hr-leave-and-absence-overview.md).

- **Išmokų valdymo funkcijos** – daugiau informacijos žr. [Išmokų valdymo apžvalga](hr-benefits-management-overview.md).

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>„Human Resources“ aplinkų limitai dabar pagrįsti atnaujintu licencijavimu (394595)

Pakeista aplinkų, naudojamų vienam projektui LCS, skaičiaus riba. Ankstesnė riba buvo dvi aplinkos. Gamybos ir smėlio dėžės aplinkų skaičiaus limitas, kurį galite kurti žmogiškiesiems ištekliams LCS, dabar pagrįstas atnaujinti licencijavimu. Dabar galite sukurti tiek aplinkų, kiek reikia vienam LCS projektui, atsižvelgdami į įsigytų licencijų skaičių. Naujas licencijavimas, atnaujintas 2020 m. vasario 1 d., leidžia klientams įsigyti papildomą aplinką. Daugiau informacijos apie papildomų aplinkų licencijavimo reikalavimus žr. [„Dynamics 365“ licencijavimo vadovas](https://dynamics.microsoft.com/pricing/#HumanResources).
 
## <a name="error-when-trying-to-delete-a-questionnaire-428603"></a>Bandant panaikinti klausimyną įvyko klaida (428603)

Šios savaitės naujinimas išsprendžia problemą, kai bandant panaikinti klausimyną rodoma toliau pateikta klaida.

Aptikta nesubalansuota X++ TTSBEGIN / TTSCOMMIT pora.

## <a name="performance-journal-and-professional-certificates-security-issue-428499"></a>Našumo žurnalo ir profesinių sertifikatų saugos problema (428499)

Šiuo pakeitimu apribojamas našumo žurnalų ir profesinių sertifikatų matomumas remiantis įmonėmis, prie kurių jie turi prieigą. 

## <a name="the-abbreviation-for-quebec-and-manitoba-387510"></a>Kvebeko ir Manitobos santrumpa (387510)

Pradžios data atnaujinta, kad atitiktų teisingą Manitobos ir Kvebeko santrumpą.

## <a name="new-entities-available-in-data-management-framework"></a>Nauji objektai, pasiekiami duomenų valdymo sistemoje

Dabar galimi tolesni objektai. Jei šių objektų nematote objektų sąraše, naudokite parinktį **Atnaujinti objektus** dalyje **Sistemos parametrai > Objekto parametrai > Atnaujinti objektų sąrašą**.

 - Atostogų ir neatvykimo banko operacija V2
 - Atostogų ir neatvykimų registracijos V2
 - Atostogų ir neatvykimų plano pakopos V2
 - Atostogų ir neatvykimų plano V2

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>Dataverse sprendimas dabar galimas su šiais pakeitimais:

| aprašymas | Pakeitimas |
| --- | --- |
| Objekto **Užduotis / pareigos** keitimai | <ul><li>Pridėta **Kompensacijos sritis**</li>|
| Objektas **Pareigų dimensija** pridėtas | <ul><li>Pridėta **Finansinės dimensijos**</li>
| Objekto **Darbininkas** keitimai | <ul><li>Pridėta **Pavadinimų seka**</li><li>Pridėta **Dirba iš namų**</li><li>Pridėta **Kalba**</li><li>Pridėta **Paaukštinimo data**</li><li>Pridėta **Jubiliejaus data**</li><li>Pridėta **Pradinio įdarbinimo data**</li></ul> |
| Objekto **Įdarbinimas** keitimai | <ul><li>Pridėta **Finansinės dimensijos**</li><li>Pridėta **Atleidimo priežastis**</li><li>**Perėjimo data** pervardyta į **Atleidimo data**</li><li>Pridėta **Bandomojo laikotarpio data**</li></ul> |
| Objekto **Darbininko adresas** keitimai | <ul><li>Pridėta **Gatvė**</li><li>**1 adreso eilutė**, **2 adreso eilutė** ir **3 adreso eilutė** pažymėtos kaip nebenaudojamos</li></ul> |
| Nauji kintamosios atlyginimo dalies sąrankos objektai | <ul><li>**Kompensacijų kitimo plano tipas**</li><li>**Kompensacijų kitimo planas**</li><li>**Kintamosios atlyginimo dalies paskirstymo taisyklės**</li><li>**Kompensacijų kitimo plano lygis**</li></ul> |
| Naujas objektas **Darbuotojo įdarbinimo kalendorius** | <ul><li>Pridėta **Darbo kalendoriaus objektas**</li></ul> |
| Naujas objektas **Algalapio pareigų informacija** | <ul><li>Pridėta **Algalapio pareigų informacija**</li></ul> |
| Naujas subjektas **Pavadinimas** | <ul><li>**Pavadinimas** pridėtas</li></ul>Naujas objektas **Pavadinimas** įtrauktas į Dataverse, bet šiuo metu nėra nurodomas iš objektų **Pareigos** arba **Darbas**. |

> [!NOTE]
> Abiejų pareigų ir įdarbinimo finansinės dimensijos suteikia vienos krypties integraciją, skirtą atnaujinimams iš „Human Resources“ į Dataverse. Finansinių dimensijų atnaujinimai dabar nesinchronizuojami iš Dataverse į „Human Resources“.

Per artimiausias kelias savaites šie objektų pakeitimai bus galimi visose aplinkose. Norėdami rankiniu būdu įdiegti naujausią Dataverse sprendimą, skirtą „Human Resources“:

1.  Eikite į [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com).

2.  Pasirinkite **Aplinkos**.

3.  Raskite aplinką, kurią norite atnaujinti. Aplinka turėtų atitikti „Human Resources“ formoje **Apie** esančios sekcijos **Dataverse informacija** reikšmę **Aplinkos pavadinimas**.

4.  Pasirinkite aplinką, kad peržiūrėtumėte detalią aplinkos informaciją.

5.  Veiksmo juostos viršuje pasirinkite **Valdyti sprendimus**. Atsidarys naujas naršyklės langas ir pereisite į **„Dynamics 365“ administravimo centrą** savo aplinkos kontekste.

6.  Sąraše **Sprendimas** pasirinkite **Dynamics 365 Human Resources fiksavimas**.

7.  Pasirinkite **Atnaujinti**, kad pritaikytumėte naujausią sprendimą.

## <a name="in-preview"></a>Peržiūroje

## <a name="leave-suspension"></a>Atostogų sustabdymas

Programoje „Human Resources” galite sustabdyti darbuotojo atostogas ir neatvykimą. Atostogų sustabdymas sustabdo pasirinktų atostogų tipų atostogų kaupimus. Jei sustabdymas įvyksta po to, kai kaupimas buvo apdorotas, atostogų sustabdymas sukurs proporcingai paskirstytą darbuotojo atostogų balanso koregavimą. Daugiau informacijos žr. [Atostogų sulaikymas](hr-leave-and-absence-suspend-leave.md).

## <a name="carry-forward-rules"></a>Perkėlimo taisyklės

Galite nurodyti perkėlimo atostogų tipą, skirtą perkėlimo balansams ir į kurį perkeliami perkeliamų balansų koregavimai. Pavyzdžiui, jei darbuotojas perkelia 10 dienų, toms 10 dienų galite pasirinkti kitą atostogų tipą. Daugiau informacijos žr. [Atostogų ir neatvykimų tipų konfigūravimas](hr-leave-and-absence-types.md).

## <a name="coming-soon"></a>Jau greitai

## <a name="new-production-release-cadence"></a>Nauji gamybos išleidimo intervalai

Nuo balandžio pradžios „Human Resources“ išleidimo intervalai pereis nuo naujinimo kas savaitę prie naujinimo kas dvi savaites. Siekiant užtikrinti derėjimą su saugiomis diegimo praktikomis ir išlaikyti aukštus paslaugos stabilumo ir patikimumo standartus, paslaugų naujinimų diegimo procesas, taikomas visiems regionams, tampa dviejų savaičių išleidimu. Bus atlikti papildomi testavimai ir stebėjimai, kad galėtume užtikrinti sėkmingą diegimą kiekviename proceso etape. Daugiau informacijos apie išleidimo intervalus žr. [Naujinimo procesas](hr-admin-setup-update-process.md).

## <a name="known-issues"></a>Žinomos problemos

## <a name="employment-detail-entity"></a>Objektas Įdarbinimo informacija

Objektas **Įdarbinimo informacija** atnaujintas toliau nurodytais laukais: **Mokėjimo dažnumas**, **Įdarbinimo kategorijos ID**, **Įdarbinimo tipas**, **Įdarbinimo tipo ID** ir **Išmokų įdarbinimo būsena**. Šių laukų nustatymo duomenys priklauso nuo išmokų valdymo įjungimo funkcijų valdyme. Šie laukai neturėtų būti užpildyti ar atnaujinti objekte **Įdarbinimo informacija**, nes importavimo metu įvyks klaidų.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>„SharePoint“ peržiūra neveikia kai kuriose aplinkose

Jei dokumentų peržiūra, skirta dokumentams, saugomiems „SharePoint“, neveikia, bandykite atlikti tolesnę procedūrą.

1. Patikrinkite, ar administratoriaus vartotojo paskyra turi el. pašto adresą, susietą su vartotojo įrašu. Šią informaciją galima peržiūrėti puslapyje **Vartotojas**. Jei el. pašto adresas nenustatytas, turite įtraukti el. pašto adresą ir tiekėją naudodami „OData Excel“ papildinį. Pagal numatytuosius parametrus, „Excel“ dizaine nėra el. pašto adreso. Turėsite redaguoti „Excel“ dizainą, įtraukti visus laukus, taikyti ir atnaujinti. Atlikę šiuos veiksmus, galėsite naujinti administratoriaus paskyrą.

2. Susieję administratoriaus paskyrą su el. pašto paskyra, prisijunkite prie „Human Resources“ naudodami administratoriaus kredencialus.

3. Atidarykite priedą „SharePoint“, kad pradėtumėte dokumento peržiūrą.

4. Prisijunkite su kito vartotojo paskyra, kuri turi prieigą prie priedų, ir patikrinkite, ar peržiūra veikia kaip numatyta.

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]