---
title: Kas nauja arba pasikeitė „Dynamics 365 Human Resources” (2020 m. balandžio 13 d.)
description: Šiame straipsnyje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2020 m. balandžio 13 d.
author: andreabichsel
manager: tfehr
ms.date: 04/13/2020
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
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3afc112f8a30bb187fbe37c9062afe7943e986ec
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127902"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a>Kas nauja arba pasikeitė „Dynamics 365 Human Resources” (2020 m. balandžio 13 d.)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šiame straipsnyje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources“ funkcijos. Pakeitimai taikomi 8.1.3136 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo LCS palaikymo numerius informaciniais tikslais.

## <a name="new-production-release-cadence"></a>Nauji gamybos išleidimo intervalai

Šios savaitės leidime „Human Resources“ išleidimo intervalai keičiasi iš naujinimo kas savaitę į naujinimą kas dvi savaites. Siekiant užtikrinti derėjimą su saugiomis diegimo praktikomis ir išlaikyti aukštus paslaugos stabilumo ir patikimumo standartus, paslaugų naujinimų diegimo procesas, taikomas visiems regionams, dabar tampa dviejų savaičių išleidimu. Atlikti papildomi testavimai ir stebėjimai, kad galėtume užtikrinti sėkmingą diegimą kiekviename proceso etape. Daugiau informacijos apie išleidimo intervalus žr. [Naujinimo procesas](hr-admin-setup-update-process.md).

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a>Lauko Apvalinimo tikslumas negalima redaguoti nurodžius apvalinimo tipą (435616)

Atlikus šį pakeitimą, laukas **Apvalinimo tikslumas** galimas po lauko **Apvalinimo tipas** atnaujinimo.

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a>Negalima redaguoti atostogų registracijos pabaigos datos, kai atostogų plane nėra kaupimo laikotarpių (413628)

Dabar galite redaguoti registracijos pabaigos datą ir negauti klaidos „Būtina užpildyti lauką Kaupimo datos pagrindas”.

## <a name="employment-entity-doesnt-sync-to-dataverse-430834"></a>Įdarbinimo objektas nesinchronizuojamas su „Dataverse” (430834)

Šis pakeitimas pataiso problemą dėl įdarbinimo duomenų nesinchronizavimo su „Dataverse” pridėjus finansinių dimensijų. 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a>Darbo kalendoriaus laiko intervalo objekto kelių pirminių elementų pašalinimas (431775)

Šis pakeitimas pašalina **darbo kalendoriaus laiko intervalo** objekto kelis pirminius elementus.

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a>Filtras, kuriame yra CAST funkcija, neveikia „OData” iškvietimo darbininko pareigų priskyrimo objekte (431699)

Šiame naujinime yra keitimas, leidžiantis filtrui, kuriame yra CAST funkcija, veikti „OData” **darbininko pareigų priskyrimo** objekte.

## <a name="in-preview"></a>Peržiūroje

## <a name="leave-suspension"></a>Atostogų sustabdymas

Programoje „Human Resources” galite sustabdyti darbuotojo atostogas ir neatvykimą. Atostogų sustabdymas sustabdo pasirinktų atostogų tipų atostogų kaupimus. Jei sustabdymas įvyksta po to, kai kaupimas buvo apdorotas, atostogų sustabdymas sukuria proporcingai paskirstytą darbuotojo atostogų balanso koregavimą. Daugiau informacijos žr. [Atostogų sulaikymas](hr-leave-and-absence-suspend-leave.md).

## <a name="carry-forward-rules"></a>Perkėlimo taisyklės

Galite nurodyti perkėlimo atostogų tipą, skirtą perkėlimo balansams ir į kurį perkeliami perkeliamų balansų koregavimai. Pavyzdžiui, jei darbuotojas perkelia 10 dienų, toms 10 dienų galite pasirinkti kitą atostogų tipą. Daugiau informacijos žr. [Atostogų ir neatvykimų tipų konfigūravimas](hr-leave-and-absence-types.md).

## <a name="known-issues"></a>Žinomos problemos

## <a name="employment-details-entity"></a>Objektas Įdarbinimo informacija

Objektas **Įdarbinimo informacija** atnaujintas toliau nurodytais laukais.

- **Mokėjimo dažnumas**
- **Įdarbinimo kategorijos ID**
- **Įdarbinimo tipas**
- **Įdarbinimo tipo ID**
- **Išmokų įdarbinimo būsena**

Šių laukų nustatymo duomenys priklauso nuo išmokų valdymo įjungimo darbo srityje **Funkcijų valdymas**. Neužpildykite ir nenaujinkite šių laukų objekte **Įdarbinimo informacija**, nes importavimo metu įvyks klaidų.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>„SharePoint“ peržiūra neveikia kai kuriose aplinkose

Jei dokumentų peržiūra, skirta dokumentams, saugomiems „SharePoint“, neveikia, bandykite atlikti tolesnę procedūrą.

1. Patikrinkite, ar administratoriaus vartotojo paskyra turi el. pašto adresą, susietą su vartotojo įrašu. Šią informaciją galima peržiūrėti puslapyje **Vartotojas**. Jei el. pašto adresas nenustatytas, turite įtraukti el. pašto adresą ir tiekėją naudodami „OData Excel“ papildinį. Pagal numatytuosius parametrus, „Excel“ dizaine nėra el. pašto adreso. Turėsite redaguoti „Excel“ dizainą, įtraukti visus laukus, taikyti ir atnaujinti. Atlikę šiuos veiksmus, galėsite naujinti administratoriaus paskyrą.

2. Susieję administratoriaus paskyrą su el. pašto paskyra, prisijunkite prie „Human Resources“ naudodami administratoriaus kredencialus.

3. Atidarykite priedą „SharePoint“, kad pradėtumėte dokumento peržiūrą.

4. Prisijunkite su kito vartotojo paskyra, kuri turi prieigą prie priedų, ir patikrinkite, ar peržiūra veikia kaip numatyta.

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)