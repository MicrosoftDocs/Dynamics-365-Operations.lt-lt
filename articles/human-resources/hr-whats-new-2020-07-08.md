---
title: Kas nauja ar pasikeitė „Dynamics 365 Human Resources” (2020 m. liepos 8 d.)
description: Šioje temoje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2020 m. liepos 8 d.
author: andreabichsel
manager: tfehr
ms.date: 07/08/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9715f332088b7b5340f4252af5f789d226d90ff2
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463603"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a>Kas nauja ar pasikeitė „Dynamics 365 Human Resources” (2020 m. liepos 8 d.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources” funkcijos. Pakeitimai taikomi 8.1.3382 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo LCS palaikymo numerius informaciniais tikslais.

## <a name="database-logging"></a>Duomenų bazės registravimas

Duomenų bazės registravimo funkcija leidžia nustatyti, kurios lentelės ir laukai turi būti stebimi. Taip pat galite nustatyti įvykius, kurie turi aktyvinti keitimų sekimą. Naudojate duomenų bazės registravimo galimybes, kad laikui bėgant pamatytumėte šiuos pakeitimus. Daugiau informacijos ieškokite [Duomenų bazės registravimo konfigūravimas ir tvarkymas](hr-admin-database-logging.md).

## <a name="configure-the-name-of-employee-self-service"></a>Konfigūruokite Darbuotojo savitarnos paslaugų pavadinimą

**Žmogiškųjų išteklių parametruose**, dabar galite pakeisti **Darbuotojo savitarnos paslaugų** darbo srities pavadinimą į **Savitarnos paslaugos**. Dėl išsamesnės informacijos, žr. [Darbuotojo savitarnos paslaugų darbo srities pavadinimo keitimas](hr-employee-self-service-workspace-name.md)

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a>Naudos valdymo atidarymo įtraukimo prieiga ne laikotarpyje

Šis išleidimas pataiso klaidą, kai darbuotojas gali prisijungti prie naudos atidarydamas įtraukimą ne per įtraukimo laikotarpį ar be gyvavimo ciklo įvykio. Dėl to, jei turite demonstracijoje atidaryte įtraukimą Darbuotojo savitarnos paslaugose, jums reikia pataisyti atidarymo įtraukimo datas į šiandien (ar anksčiau) tam, kad jį padarytumėte prieinamą. Galite pakeisti šį nustatymą **Naudų valdymas > Laikotarpių taisyklės ir parinktys**.

## <a name="email-employee-enrollment-confirmation"></a>Darbuotojo įtraukimo patvirtinimo siuntimas elektroniniu paštu

Dabar galite nusiųsti elektroninį laišką darbuotojams po to, kai jie pabaigs jų naudos pasirinkimą. Galite nusiųsti nustatytąją žinutę ar naudoti organizacijos elektronini pašto šabloną. Šie nustatymai yra **Žmogiškųjų išteklių parametrai > Naudjos valdymas**.

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a>Atšauktas leidimas vis dar rodomas ateities laiku Žmonių darbo srityje (441358)

Atšauktas leidimas nebėra rodomas kaip ateinantis laikas leidimo kortelėse **Žmonių** darbo srityje.

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a>Negalima naudoti skyriaus objekto savybių PositionV2 objekte (456486)

Dabar galite įtraukti skyrių nekurdami dublikuoto ryšio.

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a>PayrollWorkerEnrolledBenefitDetailEntity turi naudoti tik apskaičiuotą laukelį išėjimo į pensiją planams (459779)

Eksportuojant **PayrollWorkerEnrolledBenefitDetailEntity** objektą, eksportavimas nustato, ar jis turi naudoti apskaičiuotą laukelį pagal santykio lentelę, ar naudoti **ContributionAmountCur** laukelį atsarginėje lentelėje. Duomenų objekto naudojama logika naudoja santykio lentelę tais atvejais, kai paraiška įprastai neegzistuoja. Ši logika lemia objekto eksportavimo grįžimą į nulio vertę šiame stulpelyje, nes nėra apskaičiavimo santykio lenteės ir produktas neleidžia klientui jo nurodyti.
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a>Painūs vertimai čekų kalba Personalo valdyme ir Darbuotojo savitarnos paslaugose (400276)

Šis leidimas pataiso **Bendrovės aplanko**, **Kito registruoto kurso**, **Darbo** ir **Padėties** vertimus.
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a>WorkCalendarEmployment lentelė neturi sukurtų ir pakeistų įjungtų sistemos laukelių (460171)

Sukurti ir pakeisti sistemos laukeliai dabar yra įjungti **WorkCalendarEmployment** lentelėje Žmogiškuosiuose ryšiuose.
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a>Nulinė ataskaitos išimtis Samdymui ir informacijos įtraukimas ateities darbuotojams (455475)

Šis leidimas pataiso klaidą (jokios nuorodos) rodomame darbuotojų įraše, kai jūs priimate į darbą darbuotoją naudodami parinktį **Samdyti ir įtraukti informaciją**.

## <a name="changes-made-in-the-dataverse-worker-entity-dont-reflect-in-human-resources-455652"></a>Pakeitimai atlikti „Dataverse Worker“ objekte nepasirodo Žmogiškuosiuose ištekliuose (455652)

Toliau pateiktų laukelių pakeitimai **Darbutoojas** objekte „Dataverse“ nepasirodys Žmogiškuosiuose ištekliuose:

- **Darbas iš namų**
- **Paaukštinimo data**
- **Jubiliejaus data**
- **Pradinio įdarbinimo data**

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a>Tinkamas užmokesčio lygis nėra nustatytasis pagal pareigoms priskirtą darbą (394136)

Šiuo pakeitimu tinkamas užmokesčio lygis yra nustatytasis pagal **Įsigaliojimo datą** ir įrašomas **Pareigų informacij** ir **Pradžios data** esančius **Užmokesčio planavimo priskyrime**.

## <a name="in-preview"></a>Peržiūros režimu

## <a name="mandatory-fields"></a>Privalomi laukai 

Dabar galite padaryti laukus privalomais naudodami Žmogiškųjų išteklių personalizavimo galimybes. Šiai funkcijai reikia **Įrašyti rodiniai**.

## <a name="human-resources-application-in-teams"></a>„Human Resources“ programa programoje „Teams“

Darbuotojai gali peržiūrėti ir prašyti atostogų programoje „Microsoft Teams“. Jie gali bendrauti su robotu, kad sukurtų atostogų prašymą. Daugiau informacijos žr. [„Human Resources“ programa programoje „Teams“](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Duomenų valdymo sistemos (DMF) objektai, skirti išmokų valdymui
 
Išmokų valdymo objektai ir išleidimas. DMF objektai leidžia paprastai importuoti ir eksportuoti duomenis, kad lengviau konfigūruotumėte išmokų valdymą. Išmokų valdymo šablonas taps prieinamu duomenų perkėlimui. Šablonas nuosekliai eksportuoja ir importuoja duomenis išsaugodamas duomenų priklausomumą.

## <a name="buy-and-sell-leave"></a>Atostogų pirkimas ir pardavimas 

Kai kurios organizacijos suteikia išmoką, kuri leidžia darbuotojams pirkti ar parduoti savo atostogas. Šis procesas dažnai valdomas neautomatiniu būdu. Ši funkcija automatizuoja žmogiškųjų išteklių departamento valdymo strategijas ir užklausas. Ji supaprastina atostogų valdymo procesą ir padeda pašalinti klaidas. Daugiau informacijos ieškokite:

- [Atostogų pirkimo ir pardavimo strategijų valdymas](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Atostogų pirkimas ir pardavimas](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Atostogų kaupimas vienai įmonei arba vienam planui

Klientai gali apdoroti vienoje įmonėje sukauptas atostogas, vienkartines atostogas ir neatvykimų planą. Tokia galimybė suteikia kaupimo proceso aiškumą klientams su skirtingais išėjimo į pensiją metais ir išėjimo į pensiją kaupimo politika. Norėdami sužinoti daugiau, skaitykite [Sukauptos atostogos įmonėje ar atostogų planas](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Įtraukite priedus į laiko prašymus

Galimybė pridėti priedus prie patvirtintų atostogų prašymų yra itin svarbi dabartinėje COVID-19 situacijoje. Dabar darbuotojai gali pridėti šiuos priedus. Jie taip pat turi daugiau įžvalgų apie atostogų prašymų naujinimų kūrimą. Norėdami sužinoti daugiau, skaitykite [Priedo prie esamo prašymo pridėjimas](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Priežasties kodo pridėjimas į kaupimo sustabdymus 

Į kaupimo sustabdymus įtraukti priežasties kodai.

## <a name="carry-forward-rules"></a>Perkėlimo taisyklės 

Galite nurodyti perkėlimo atostogų tipą, skirtą perkėlimo balansams ir į kurį perkeliami perkeliamų balansų koregavimai. Pavyzdžiui, jei darbuotojas perkelia 10 dienų, toms 10 dienų galite pasirinkti kitą atostogų tipą. Daugiau informacijos žr. [Atostogų ir neatvykimų tipų konfigūravimas](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Atostogų kaupimo sustabdymas konkretiems atostogų tipams

Galite sukurti taisyklę sustabdyti darbuotojų, įvedusių neapmokamų atostogų prašymus, atostogų kaupimą. Neapmokamos atostogos gali būti tipas, tačiau tai neprivaloma. Galite sustabdyti bet kokias atostogas, pagrįstas kitu atostogų tipu.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF objektas pasiekiamas kaupimo sustabdymams 

DMF objektas dabar pasiekiamas kaupimo sustabdymams.

## <a name="coming-soon"></a>Jau greitai

## <a name="checklist-entities-included-in-dataverse"></a>Kontrolinio sąrašo objektai, nurodyti „Dataverse”

Tikrinimo objektai Įtraukimo, Atleidimo, Perleidimo ir Verslo procesams bus greitai prieinami „Dataverse“.

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]