---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent Core HR“ (2018 m. spalio 31 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 for Talent Core HR“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
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
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d6942f8e4dc86f18a081b347df0567b1358a87ab
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/19/2019
ms.locfileid: "858795"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-31-2018"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent Core HR“ (2018 m. spalio 31 d.)

[!include [banner](includes/banner.md)]

**8.1.2031 versija**

Šioje temoje aprašomos naujos ir pakeistos „Core HR“ funkcijos.

## <a name="create-links-from-talent-to-finance-and-operations"></a>Kurti duomenų saitus iš „Talent“ į „Finance and Operations“
Naudodamiesi šia nauja naršymo funkcija galite susieti „Talent“ su „Finance and Operations“ ir tiesiogiai pereiti į „Finance and Operations“ puslapius. Konfigūruodami saitus galite nurodyti saito pavadinimą ir grupę, kur saitas bus rodomas „Talent“, bei paskirties puslapį, kuris bus atidaromas „Finance and Operations“.

#### <a name="coming-soon"></a>Jau greitai
Ateityje bus įtrauktas laukų kontekstas, kad galėtumėte tiesiogiai pereiti į atitinkamus „Finance and Operations“ įrašus. Pavyzdžiui, galite naudotiesi **lauko saitu** nurodyti kontekstą, leidžiantį tiesiogiai pereiti į konkretaus darbuotojo arba pareigų duomenis „Finance and Operations“.

### <a name="configure-target-systems"></a>Konfigūruoti paskirties sistemas

Naudodamiesi „Talent“ sistemos administratoriai gali nustatyti saitus, kuriuos bus galima naudoti sistemos administravimo darbo srityje. Konfigūruodami turėsite nustatyti „Finance and Operations“ aplinkas, į kurias naudodamiesi saitu norite pereiti kaip į paskirties vietą. Tai padarysite suteikdami paskirties sistemai pavadinimą ir nurodydami „Finance and Operations“ aplinkos URL. „Finance and Operations“ URL, kurį turėtumėte nurodyti, pavyzdys: https://devax00124aos.cloud.test.dynamics.com/. Sukonfigūravę paskirties sistemas galite nustatyti saitus.

### <a name="configure-links"></a>Konfigūruoti saitus

Kiekviename kuriamame saite bus nurodyta tolesnė informacija.

- Saitas – saito pavadinimas, naudojamas tik identifikavimui.

- Įjungti šį saitą – nustatykite **Taip**, jei norite, kad saitą matytų „Talent“ vartotojai.

- Rodomas pavadinimas – nurodykite pavadinimą, kuris bus rodomas kaip „Finance and Operations“ saitas. Šiuo metu šie duomenys nėra išversti.

- Formoje pridėti saitą – pasirinkite, kurį puslapį norite rodyti naudodami saitą.

- Grupė – grupės nėra būtinos, tačiau jei norite tvarkyti savo saitus naudodami grupes, pasirinkite esamą grupę arba sukurkite naują naudodamiesi lauku **Grupė**.

- Paskiries sistema – pasirinkite paskirties sistemą, sukurtą naudojant parinktį **Konfigūruoti paskirties sistemą**. Tai bus „Finance and Operations“ aplinka, į kurią bus pereinama naudojant saitą.

- Naudoti dabartinę vartotojo įmonę – pasirinkite **Taip**, jei pereinant į „Finance and Operations“ norite naudoti dabartinės vartotojo įmonės kontekstą. Jei pasirinksite **Ne**, galėsite pasirinkti įmonę, kuri bus naudojama.

- Paskirties meniu elementas – įveskite meniu elementą iš „Finance and Operation“, į kurį bus pereinama pasirinkus saitą. Yra meniu elementų, į kuriuos galite pereiti tiesiogiai. Norėdami rasti reikiamą meniu elementą atidarykite „Finance and Operations“ ir naršymo paskirties puslapį. Nukopijuokite meniu elementą iš URL. Pavyzdžiui, jei norite, kad saitas atidarytų darbuotojų sąrašą, esantį „Finance and Operations“, įveskite reikšmę, kuri URL bus po &mi. https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees. Meniu elemento, perkeliančio į darbuotojų sąrašo puslapį, pavyzdys: HcmWorkerListPage_Employees.

- Susieti su duomenų šaltiniu – pasirinkite duomenų šaltinį, kurį nurodo saitas. Galimi dažniausiai naudojami šaltiniai, pvz., **Darbininkas** ir **Pareigos**.

- Lauko saitas – (jau greitai) pasirinkę šią lauko parinktį galėsite tiesiogiai pereiti iš vieno „Talent“ įrašo į vieną „Finance and Operations“ įrašą.

### <a name="access-to-links"></a>Prieiga prie saitų

Sistemos administratoriai nustatytuose puslapiuose matys naujai sukurtus saitus, net jei pasirinkta parinkties **Įjungti šį saitą** reikšmė yra **Ne**. Tai galima naudoti norint patikrinti saitus prieš pateikiant juos naudoti kitiems darbuotojams. Visi kiti vaidmenys matys tik sukonfigūruotus saitus, kai parinktis **Įjungti šį saitą** bus nustatyta kaip **Taip**. Saitus galės pasiekti darbuotojai, turintys prieigą prie puslapių, kuriuose šie saitai yra pridėti.

Vartotojai taip pat gali turėti saugos teisių „Finance and Operations “, nustatanių prieigą prie „Finance and Operations“ puslapių. Jei jie jų neturi, naudojant saitą bus rodomas saugos dialogo langas.


## <a name="other-changesfixes"></a>Kiti pakeitimai / pataisos

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a>Naujam darbuotojui negalima priskirti pareigų, kurių pradžios data yra ateityje.

Atlikti pakeitimai, leidžiantys darbuotojams priskirti būsimas pareigas. Pareigas, kurių pradžios data yra ateityje, galima pasirinkti ir priskirti darbuotojui įrašius arba užbaigus darbo eigą (jei darbo eiga yra įjungta).

### <a name="new-employee-cannot-be-assigned-existing-position"></a>Naujam darbuotojui negalima priskirti esamų pareigų

Atlikti pakeitimai, todėl dabar naujam darbuotojui galima priskirti esamas pareigas.

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a>Kai įdarbinimo pradžios data yra praeityje ir įrašas yra įrašytas, paaukštinimo data / biuro vieta neberodoma

Atlikti matomumo keitimai siekiant pakoreguoti **paaukštinimo datos** ir **biuro vietos** matomumą įrašant buvusių darbuotojų pakeitimus.

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a>Darbininko puslapyje negalima įvesti duomenų apie įdarbinimą, kurio pradžios data yra ateityje

Pagrindiniame darbininko puslapyje išjungti duomenys, susiję su įdarbinimais, kurių pradžios data yra ateityje. Įdarbinimo duomenis galima įvesti **datų tvarkytuvo** puslapiuose. Būsimuose leidimuose bus atlikta daugiau pakeitimų siekiant sudaryti sąlygas įdarbinimo duomenis įvesti tiesiogiai darbo eigos procese.

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a>Į HcmPersonalContactPersonEntity įtraukti ValidFrom ir ValidTo

Atnaujintas „Data Management Framework“ (DMF) objektas HcmPersonalContactPersonEntity įtraukiant datas Galioja nuo ir Galioja iki, kad būtų galima įjungti tam tikrus išmokų integravimo scenarijus. 

## <a name="known-issue"></a>Žinoma problema
- **Problema**: įtraukiant naują priedą į darbininko puslapį mygtukai **Naujas** ir **Redaguoti** yra papilkinti. 
- **Problemos sprendimas:** prieš atidarydami priedų puslapį įsitikinkite, kad „FactBoxes“ laukai puslapyje **Darbininkas** yra uždaryti. Jei „FactBoxes“ laukai yra uždaryti, įkeliant puslapį **Darbininkas** priedų mygtukai bus įjungti. (Ši problema bus pašalinta kitame platformos naujinime.)
