---
title: Personalo valdymo darbo sritis
description: Šioje temoje aprašomi abstraktūs Personalo valdymo darbo srities elementai.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: twheeloc
ms.reviewer: twheeloc
ms.search.scope: Human Resources
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7a83dea308e3e2eec1edebd5d619f9455e1a2268
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066580"
---
# <a name="personnel-management-workspace"></a>Personalo valdymo darbo sritis


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Personalo valdymo** darbo srityje yra didelis turinio kiekis. Jame yra personalo judėjimas, sekami darbuotojų pasikeitimai, atviros pareigos, adresų pasikeitimai, pasibaigiantys įrašai ir analizė, pateikiamos nuorodos į konkrečią informaciją. Šioje temoje pateikiama išsami informacija apie kiekvieną darbo srities dalį.

## <a name="activity-tab"></a>Skirtukas Veikla

Skirtuke **Veikla** yra skyrių, grupuojančių darbuotojus pagal jų įdarbinimo proceso etapus:

- **Samdytini kandidatai**
- **Greitai prasideda**
- **Neseniai pasamdyta**
- **Išeinama**
- **Išėjęs**

Kai darbuotojas yra viename iš šių etapų, tam tikrus veiksmus galima naudoti kaip mygtuką kortelėje arba meniu, kuris atsiranda viršutiniame dešiniajame kampe pasirinkus daugtaškį ( **„...”**). Toliau pateikti poskyriai aprašo **Veiklos** skirtuko skyrius ir pateikia galimų veiksmų sąrašą.

### <a name="candidates-to-hire"></a>Samdytini kandidatai

Darbo srities skyrius **Samdytini kandidatai** yra užpildomas iš kelių šaltinių:

- Atviro duomenų protokolo („OData”) objektas
- „LinkedIn‟ integravimas
- Duomenys, rankiniu būdu įvesti į produktą

Kai kandidatai pasirodo **Samdytinų kandidatų** skyriuje, galite atlikti šiuos veiksmus pasirinkdami daugtaškį kandidato kortelėje:

- **Atmesti kandidatą**
- **Nesamdyti**
- **Samdyti**

> [!NOTE]
> Jei kandidatų sąrašas užpildomas iš „Microsoft Dataverse”, tie patys kandidatai bus rodomi visuose juridiniuose subjektuose, nes juridinis subjektas nebuvo susietas su kandidatu.

### <a name="starting-soon"></a>Greitai pradeda

Skyriuje **Greitai pradeda** išvardyti darbuotojai, kurių pradžios data yra ateityje. Sąrašo duomenys rūšiuojami pagal pradžios datą. Pirma pateikta pradžios data, kuri yra arčiausiai šios dienos duomenų.

Jei vadovo nėra kortelėje, darbuotojui nebus priskirtos pareigos.

> [!NOTE] 
> Prieš taikant kontrolinį sąrašą rekomenduojame darbuotojui priskirti pareigas. Kartais įdarbinimo užduotys paskiriamos naujai pasamdyto darbuotojo vadovui. Tačiau jei nepriskirtos jokios pareigos, negalima nustatyti naujo darbuotojo vadovo. Tokiu atveju vadovui numatytos supažindinimo užduotys vietoj to bus priskirtos kontrolinio sąrašo savininkui.

Kai darbuotojai atsiranda **Greitai pradės** dalyje, jiems galima atlikti šiuos veiksmus:

- Priskirti pareigas
- Tikrinti įdarbinimą
- Priskirti pastoviąją atlyginimo dalį
- Priskirti kintamąją atlyginimo dalį
- Žiūrėti Hierarchijoje
- Taikyti kontrolinį sąrašą\*\*

\*\* Šis veiksmas yra numatytasis. Jis rodomas kaip kortelės mygtukas.

### <a name="recent-hires"></a>Naujausi samdiniai

**Naujausių samdinių** skyriuje išvardyti darbuotojai, kurių pradžios data yra netolimoje praeityje. Sąrašo duomenys rūšiuojami pagal pradžios datą. Pirma pateikta pradžios data, kuri yra arčiausiai šios dienos datos.

Pagal numatytuosius nustatymus, sąraše rodomi darbuotojai, pasamdyti per paskutines septynias dienas. Norėdami pakeisti šį parametrą, **Žmogiškųjų išteklių parametrų** puslapio skirtuke **Bendra** nustatykite skirtąjį laiką **Naujausi samdiniai**. Skyriaus **Naujausi samdiniai** duomenys gali būti rodomi tam tikrą dienų, mėnesių ar metų skaičių. Pavyzdžiui, norėdami peržiūrėti darbuotojų, kurie buvo pasamdyti per paskutines 14 dienų, sąrašą, nustatykite **Laikotarpio** lauką į **14**, o **Vieneto** lauką – į **Dienos**.

> [!NOTE]
> Nustatymai **Žmogiškųjų išteklių parametrai** puslapyje yra konkrečios įmonės. Todėl skirtasis laikas, per kurį peržiūrite naujausius samdinius gali skirtis pagal įmonę. Pavyzdžiui, „USMF” įmonėje galbūt norėsite peržiūrėti visus naujus samdinius per paskutines septynias dienas. Tačiau USSI įmonėje galbūt norėsite peržiūrėti visus naujus pasamdžius per pastarąsias 14 dienų. Tokiu atveju atidarykite **Žmogiškųjų išteklių parametrai** puslapį kiekvienoje įmonėje ir pagal poreikį nustatykite parametrus.

Jei vadovo nėra kortelėje, darbuotojui nebus priskirtos pareigos.

Kai darbuotojai atsiranda **nauji samdiniai** dalyje, jiems galima atlikti šiuos veiksmus:

- Priskirti pareigas
- Tikrinti įdarbinimą
- Pastovioji atlyginimo dalis
- Priskirti kintamąją atlyginimo dalį
- Žiūrėti hierarchijoje
- Taikyti kontrolinį sąrašą\*\*

\*\* Šis veiksmas yra numatytasis. Jis rodomas kaip kortelės mygtukas.

### <a name="exiting"></a>Išeinama

Skyriuje **Išeinama** išvardyti darbuotojai, kurių sutarties nutraukimo data yra ateityje. Sąrašo duomenys rūšiuojami pagal pabaigos datą. Pirma pateikta pabaigos data, kuri yra arčiausiai šios dienos datos. 

Pagal numatytuosius nustatymus, sąraše rodomi darbuotojai, kurių sutarties nutraukimo data yra per artimiausias septynias dienas. Norėdami pakeisti šį parametrą, **Žmogiškųjų išteklių parametrų** puslapio skirtuke **Bendra** nustatykite skirtąjį laiką **Žiūrėti išeinančius darbuotojus**. Skyriaus **Išeinantys** duomenys gali būti rodomi tam tikrą dienų, mėnesių ar metų skaičių. Pavyzdžiui, norėdami peržiūrėti darbuotojų, kurie nutrauks sutartį per artimiausias 14 dienų, sąrašą, nustatykite **Laikotarpio** lauką į **14**, o **Vieneto** lauką – į **Dienos**.

Kai darbuotojai atsiranda **Išeinantys** dalyje, jiems galima atlikti šiuos veiksmus:

- Taikyti kontrolinį sąrašą\*\*
- Tikrinti įdarbinimą
- Žiūrėti Hierarchijoje

\*\* Šis veiksmas yra numatytasis. Jis rodomas kaip kortelės mygtukas.

### <a name="exited"></a>Išėjęs

**Išėjusiųjų** skyriuje išvardyti darbuotojai, kurių sutarties nutraukimo data yra netolimoje praeityje. Sąrašo duomenys rūšiuojami pagal pabaigos datą. Pirma pateikta pabaigos data, kuri yra arčiausiai šios dienos datos.

Pagal numatytuosius nustatymus, sąraše rodomi darbuotojai, kurių sutarties nutraukimo data yra paskutinės septynios dienos. Norėdami pakeisti šį parametrą, **Žmogiškųjų išteklių parametrų** puslapio skirtuke **Bendra** nustatykite skirtąjį laiką **Žiūrėti išėjusius darbuotojus**. Skyriaus **Išėję** duomenys gali būti rodomi tam tikrą dienų, mėnesių ar metų skaičių. Pavyzdžiui, norėdami peržiūrėti darbuotojų, kurie nutraukė sutartį per paskutines 14 dienų, sąrašą, nustatykite **Laikotarpio** lauką į **14**, o **Vieneto** lauką – į **Dienos**.

Kai darbuotojas atsiranda **Išėję** dalyje, jiems galima atlikti šiuos veiksmus:

- Taikyti kontrolinį sąrašą\*\*
- Tikrinti įdarbinimą
- Žiūrėti hierarchijoje

\*\* Šis veiksmas yra numatytasis. Jis rodomas kaip kortelės mygtukas.

## <a name="employee-changes-tab"></a>Skirtukas Darbuotojo pakeitimai

Skirtuke **Darbuotojo pakeitimai** pateikiamas visų darbuotojo personalo veiksmų sąrašas. Šis sąrašas nėra prieinamas pagal numatytuosius nustatymus. Norėdami įjungti funkcijas, **Bendrinamų Žmogiškųjų išteklių parametrų** puslapio skirtuke **Personalo veiksmai** nustatykite parinktį **Įgalinti darbuotojo veiksmus** į **Taip**.

## <a name="position-changes-tab"></a>Skirtukas Pareigų pakeitimai

Skirtuke **Pareigų pakeitimai** pateikiamas visų pareigų personalo veiksmų sąrašas. Šis sąrašas nėra prieinamas pagal numatytuosius nustatymus. Norėdami įjungti funkcijas, **Bendrinamų Žmogiškųjų išteklių parametrų** puslapio skirtuke **Personalo veiksmai** nustatykite parinktį **Įgalinti pareigų veiksmus** į **Taip**.

## <a name="open-positions-tab"></a>Skirtukas Laisvos pareigos

Skirtuke **Laisvos pareigos** išvardytos visos laisvos pareigos. Tam, kad jos būtų rodomos sąraše, pareigų aktyvinimo data turi būti šiandienos arba ankstesnė, o joms negali būti priskirtas dabartinis darbuotojas.

> [!NOTE]
> Sąraše laikoma, kad darbuotojas priskirtas nuo šiandien. Bet kurios pareigos, turinčios būsimą darbuotojo priskyrimą, ir toliau bus rodomos sąraše. Tačiau po darbuotojo priskyrimo įsigaliojimo datos, pareigos bus pašalintos iš sąrašo.

## <a name="expiring-records-tab"></a>Baigiančių galioti įrašų skirtukas

**Baigiančių galioti įrašų** skirtuke išvardijamos visos prekės, kurių galiojimas baigėsi arba kurios baigs galioti įmonės, kurioje vartotojas yra prisiregistravęs, darbuotojams. Sąraše rodomi šie elementai:

- **Sertifikatai**
- **Identifikavimas**
- **Bandomieji laikotarpiai**
- **Atrankos**
- **Testai**

Norėdami nurodyti, ar sąraše rodomi nebegaliojantys įrašai ar baigiantys galioti įrašai, **Žmogiškųjų išteklių parametrų** skirtuke **Bendra** apibrėžkite skirtąjį laiką **Baigiantiems galioti įrašams** arba **Nebegaliojantiems įrašams**. Duomenys **Baigiantys galioti įrašai** gali būti rodomi tam tikrą dienų skaičių. Pavyzdžiui, norėdami peržiūrėti įrašų, kurių galiojimas baigsis per artimiausias 14 dienų, sąrašą, nustatykite lauką **Dienų skaičius** į **14**.

> [!NOTE] 
> Jei nustatote skirtąjį laiką **Nebegaliojantiems įrašams** ar **Baigiantiems galioti įrašams** į **0** puslapyje **Žmogiškųjų išteklių parametrai**, sąrašas nerodys jokių tų įrašų.

## <a name="employees-tile"></a>Darbuotojų plytelė

**Darbuotojų** plytelė pateikia visų darbuotojų, dirbančių įmonėje, prie kurios vartotojas šiuo metu yra prisijungęs, skaičių. Kai pasirenkate **Darbuotojų** plytelę, naujas puslapis rodo išsamią darbuotojų informaciją.

## <a name="contractors-tile"></a>Rangovų plytelė

**Rangovų** plytelė pateikia visų rangovų, dirbančių įmonėje, prie kurios vartotojas šiuo metu yra prisijungęs, skaičių. Kai pasirenkate **Rangovų** plytelę, naujas puslapis rodo išsamią rangovų informaciją.

## <a name="open-positions-tile"></a>Laisvų pareigų plytelė

**Laisvų pareigų** plytelė pateikia visų laisvų pareigų skaičių. Kai pasirenkate **Laisvų pareigų** plytelę, naujas puslapis rodo išsamią laisvų pareigų informaciją. Tam, kad jos būtų įtrauktos į skaičiavimą, pareigų aktyvinimo data turi būti šiandienos arba ankstesnė, o joms negali būti priskirtas dabartinis darbuotojas.

> [!NOTE]
> Plytelėje laikoma, kad darbuotojas priskirtas nuo šiandien. Bet kurios pareigos, turinčios būsimą darbuotojo priskyrimą, ir toliau bus įtrauktos į skaičiavimą. Tačiau po darbuotojo priskyrimo įsigaliojimo datos, pareigos nebus įtrauktos į skaičiavimą.

## <a name="approvals-tile"></a>Patvirtinimų plytelė

**Patvirtinimų** plytelė pateikia visų darbo eigos elementų, laukiančių dabartinio vartotojo patvirtinimo, skaičių. Kai pasirenkate **Patvirtinimų** plytelę, naujas puslapis rodo išsamią darbo eigos elementų, kuriems reikia jūsų patvirtinimo, informaciją.

## <a name="address-changes-tile"></a>Adreso pakeitimų plytelė

**Adreso pakeitimų** plytelė pateikia visų adreso pakeitimų, atliktų per dienų skaičių, nurodytą **Žmogiškųjų išteklių parametrų** puslapyje, skaičių. Kai pasirenkate **Adreso pakeitimai** plytelę, naujas puslapis parodo visų adresų keitimų išsamią informaciją. Viršutiniame dešiniajame puslapio kampe galite pasirinkti **Įtraukti būsimus adreso pakeitimus**, kad peržiūrėtumėte adreso keitimus su ateities data.

Daugiau informacijos apie tai, kaip peržiūrėti ir tvarkyti adreso pakeitimus, rasite [Peržiūrėti ir tvarkyti adreso pakeitimus](hr-personnel-view-address-changes.md).
