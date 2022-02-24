---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. kovo 24 d.)
description: Šiame straipsnyje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2020 m. kovo 24 d.
author: Darinkramer
manager: AnnBe
ms.date: 03/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-03-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 87b7ea660d94c6d564a8f09d4133b098e0ecedf9
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526924"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-24-2020"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. kovo 24 d.)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šiame straipsnyje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources“ funkcijos. Pakeitimai taikomi 8.1.3073 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo „Lifecycle Services“ (LCS) palaikymo numerius kaip nuorodą.

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>„Human Resources“ aplinkų limitai dabar pagrįsti atnaujintu licencijavimu (394595)

Pakeista aplinkų, naudojamų vienam projektui „Lifecycle Services“ (LCS), skaičiaus riba. Ankstesnė riba buvo dvi aplinkos. Gamybos ir smėlio dėžės aplinkų skaičiaus limitas, kurį galite kurti žmogiškiesiems ištekliams LCS, dabar pagrįstas atnaujinti licencijavimu. Dabar galite sukurti tiek aplinkų, kiek reikia vienam LCS projektui, atsižvelgdami į įsigytų licencijų skaičių. Naujas licencijavimas, atnaujintas 2020 m. vasario 1 d., leidžia klientams įsigyti papildomą aplinką. Daugiau informacijos apie papildomų aplinkų licencijavimo reikalavimus žr. [„Dynamics 365“ licencijavimo vadovas](https://dynamics.microsoft.com/pricing/#HumanResources).

## <a name="platform-changes"></a>Platformų pakeitimai

- Viso puslapio programos (peržiūra) – ši peržiūros funkcija, kuriai reikia įjungti įrašytų rodinių funkciją, leidžia įtraukti Power Apps ir trečiųjų šalių programas prietaisų skydelyje kaip viso puslapio patirtį.

- Įrašyti rodiniai (peržiūra) – ši peržiūros funkcija įjungia įrašytus rodinius, kurie labai patobulina personalizavimo posistemį. Ši funkcija suteikia vartotojams galimybę viename puslapyje turėti kelis įvardytuosius individualizavimo rinkinius. Taip pat galite publikuoti saugos vaidmenų rodinius.

- Optimizuota „yra viena iš“ filtravimo patirtis – šia funkcija įjungiama optimizuota „yra viena iš“ filtravimo patirtis, kurią pasitelkus yra lengviau įvesti kelias filtrų vertes, suteikiama paprastesnė priemonė atskiroms arba visoms filtrų vertėms pašalinti ir glaudesnis bei intuityvesnis filtro verčių vizualizavimas.

- Rekomenduojami laukai – vartotojams dažnai reikia pridėti laukus prie tinklelio ar puslapio. Tai gali būti sudėtinga su tiek daug galimų laukų. Vietoje to, kad paieška būtų atliekama dideliame sąraše, ši funkcija leidžia sistemai nustatyti rekomenduojamus laukus, atsižvelgiant į tai, kuriuos kitus vartotojus dažniausiai pridedate panašiose situacijose.

- „Priklijuojamieji“ numatytieji veiksmai tinkleliuose – šia funkcija užtikrinama, kad numatytasis veiksmas tinklelyje būtų susietas su konkrečiu stulpeliu tinklelyje, nepriklausomai nuo to, ar tas stulpelis yra perkeltas ar paslėptas.

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-multiple-leave-type-feature-on-419635"></a>Nepavyksta pakoreguoti plano be kaupimų atostogų balanso, kuris buvo sukurtas naudojant kelių atostogų tipo funkciją (419635)

Atlikus šį pakeitimą, galite koreguoti atostogų planų, sukurtų naudojant (peržiūros) funkciją Kelių atostogų tipas, kuri įjungta funkcijų valdyme, balansus.

## <a name="in-preview"></a>Peržiūros režimu

Šios peržiūros funkcijos tapo pasiekiamos nuo 2020 m. vasario 3 d.:

- **Atostogų ir neatvykimų peržiūros funkcijos** – daugiau informacijos žr. skyrių [Atostogų ir neatvykimų peržiūros funkcijos](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Išmokų valdymo peržiūros funkcija** – norėdami gauti daugiau informacijos, įskaitant žinomas problemas, žr. skyrių [Išmokų valdymo peržiūra](hr-benefits-management-overview.md).

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service sprendimas dabar galimas su šiais pakeitimais:

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
| Naujas subjektas **Pavadinimas** | <ul><li>**Pavadinimas** pridėtas</li></ul>Naujas objektas **Pavadinimas** įtrauktas į Common Data Service, bet šiuo metu nėra nurodomas iš objektų **Pareigos** arba **Darbas**. |

> [!NOTE]
> Abiejų pareigų ir įdarbinimo finansinės dimensijos suteikia vienos krypties integraciją, skirtą atnaujinimams iš „Human Resources“ į Common Data Service. Finansinių dimensijų atnaujinimai dabar nesinchronizuojami iš Common Data Service į „Human Resources“.

Per artimiausias kelias savaites šie objektų pakeitimai bus galimi visose aplinkose. Norėdami rankiniu būdu įdiegti naujausią Common Data Service sprendimą, skirtą „Human Resources“:

1.  Eikite į [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com).

2.  Pasirinkite **Aplinkos**.

3.  Raskite aplinką, kurią norite atnaujinti. Aplinka turėtų atitikti „Human Resources“ formoje **Apie** esančios sekcijos **Common Data Service informacija** reikšmę **Aplinkos pavadinimas**.

4.  Pasirinkite aplinką, kad peržiūrėtumėte detalią aplinkos informaciją.

5.  Veiksmo juostos viršuje pasirinkite **Valdyti sprendimus**. Atsidarys naujas naršyklės langas ir pereisite į **„Dynamics 365“ administravimo centrą** savo aplinkos kontekste.

6.  Sąraše **Sprendimas** pasirinkite **Dynamics 365 Human Resources fiksavimas**.

7.  Pasirinkite **Atnaujinti**, kad pritaikytumėte naujausią sprendimą.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>„SharePoint“ peržiūra neveikia kai kuriose aplinkose

Jei dokumentų peržiūra, skirta dokumentams, saugomiems „SharePoint“, neveikia, bandykite atlikti tolesnę procedūrą.

1. Patikrinkite, ar administratoriaus vartotojo paskyra turi el. pašto adresą, susietą su vartotojo įrašu. Šią informaciją galima peržiūrėti puslapyje **Vartotojas**. Jei el. pašto adresas nenustatytas, turite įtraukti el. pašto adresą ir tiekėją naudodami „OData Excel“ papildinį. Pagal numatytuosius parametrus, „Excel“ dizaine nėra el. pašto adreso. Turėsite redaguoti „Excel“ dizainą, įtraukti visus laukus, taikyti ir atnaujinti. Atlikę šiuos veiksmus, galėsite naujinti administratoriaus paskyrą.

2. Susieję administratoriaus paskyrą su el. pašto paskyra, prisijunkite prie „Human Resources“ naudodami administratoriaus kredencialus.

3. Atidarykite priedą „SharePoint“, kad pradėtumėte dokumento peržiūrą.

4. Prisijunkite su kito vartotojo paskyra, kuri turi prieigą prie priedų, ir patikrinkite, ar peržiūra veikia kaip numatyta.

## <a name="coming-soon"></a>Jau greitai

## <a name="new-production-release-cadence"></a>Nauji gamybos išleidimo intervalai

Nuo balandžio pradžios „Human Resources“ išleidimo intervalai pereis nuo naujinimo kas savaitę prie naujinimo kas dvi savaites. Siekiant užtikrinti derėjimą su saugiomis diegimo praktikomis ir išlaikyti aukštus paslaugos stabilumo ir patikimumo standartus, paslaugų naujinimų diegimo procesas, taikomas visiems regionams, tampa dviejų savaičių išleidimu. Bus atlikti papildomi testavimai ir stebėjimai, kad galėtume užtikrinti sėkmingą diegimą kiekviename proceso etape. Daugiau informacijos apie išleidimo intervalus žr. [Naujinimo procesas](hr-admin-setup-update-process.md).

## <a name="known-issues"></a>Žinomos problemos

## <a name="employment-detail-entity"></a>Objektas Įdarbinimo informacija

Objektas **Įdarbinimo informacija** atnaujintas toliau nurodytais laukais: **Mokėjimo dažnumas**, **Įdarbinimo kategorijos ID**, **Įdarbinimo tipas**, **Įdarbinimo tipo ID** ir **Išmokų įdarbinimo būsena**. Šių laukų nustatymo duomenys priklauso nuo išmokų valdymo įjungimo funkcijų valdyme. Šie laukai neturėtų būti užpildyti ar atnaujinti objekte **Įdarbinimo informacija**, nes importavimo metu įvyks klaidų.

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)