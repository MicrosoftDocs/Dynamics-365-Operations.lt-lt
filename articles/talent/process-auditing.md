---
title: Įdarbinimo duomenų pakeitimų sekimas
description: Proceso audito funkcija suteikia galimybę stebėti, kada kandidatai, darbo vietos arba darbo paraiškos pasikeičia dėl pranešimų ar atitikties priežasčių.
author: tracykeya
manager: AnnBe
ms.date: 04/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: trkeya
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: 803c935493a4080b8c1d0ef92bbe7db601f3ca03
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518648"
---
# <a name="track-changes-in-recruiting-data"></a>Įdarbinimo duomenų pakeitimų sekimas

Naudodami audito apdorojimą galite stebėti keitimus kandidatams, darbo vietoms ir darbo paraiškoms. Ši funkcija naudinga ataskaitoms ar atitikčiai.

Sekamus duomenis galite peržiūrėti programa „Power BI“, naudodami „OData“ jungtį. Daugiau informacijos rasite [Prisijungimas prie „OData“ informacijos santraukų „Power BI Desktop“](https://docs.microsoft.com/en-us/power-bi/desktop-connect-odata).

## <a name="track-changes"></a>Sekti keitimus
Norėdami nustatyti įdarbinimo duomenų stebėjimą, atlikite šiuos veiksmus:

1. [„Powerapps“](https://web.powerapps.com) pasirinkite tinkamą aplinką.

2. Pasirinkite **Parametrai** (krumpliaračio piktograma), pasirinkite **Išplėstinis tinkinimas**, tada pasirinkite **Ištekliai** dalyje **Kūrėjo ištekliai**. 

3. Puslapyje **Kūrėjo ištekliai** nukopijuokite reikšmę, esančią lauke **Egzemplioriaus žiniatinklio API vertė**. Pavyzdžiui, vertė gali atrodyti taip: https://yourorgname.api.crm.dynamics.com/api/data/v9.1/.

4. Tada galite paprašyti duomenų iš vieno iš šių objektų:
  - Darbo pasiūlymo istorija (msdyn_jobopeninghistories)
  - Darbo paraiškos istorija (msdyn_jobapplicationhistories) 
  - Kandidato istorija (msdyn_candidatehistories)

## <a name="data-reported"></a>Pranešimo duomenys

Su proceso auditu galima naudoti šiuos duomenis.

| Pranešimo duomenys | Aprašas |
| --- | --- |
| Pakeitė (msdyn_ChangedbyId) | Nuoroda į vartotoją |
| Sukūrimo data (createdon) |  Data ir laikas UTC, kai įvyko pokytis |
| Pakeitimo tipas (msdyn_changetype) | Kas pasikeitė |
| Bendros kandidatų vertės, darbo pasiūlymai <br></br>ir darbo paraiškos | Sukurta<br></br>Atnaujinta |
| Darbo paraiškų istorija | Įtrauktas artefaktas <br></br>Pašalintas artefaktas |
| Darbo pasiūlymo istorija | UŽDUOTIS: įtrauktas įrašas <br></br>UŽDUOTIS: pašalintas įrašas <br></br>UŽDUOTIS: įrašas atnaujintas <br></br>UŽDUOTIS: dalyvis įtrauktas <br></br>UŽDUOTIS: dalyvis pašalintas |
| Kandidato istorija | Įtrauktas artefaktas <br></br>Pašalintas artefaktas <br></br>Darbo patirtis įtraukta <br></br>Darbo patirtis pašalinta <br></br>Išsilavinimas įtrauktas <br></br>Išsilavinimas pašalintas <br></br>Įgūdis įtrauktas <br></br>Įgūdis pašalintas <br></br>Žyma įtraukta <br></br>Žyma pašalinta <br></br>Socialinis tinklas įtrauktas <br></br>Socialinis tinklas pašalintas <br></br>Asmeninė informacija įtraukta <br></br>Asmeninė informacija atnaujinta<br></br> |
| Pakeisti laukai (msdyn_changedfields) | Pakeisti JSON objektų sąrašo laukai, gali nepavykti išsaugoti visų laukų verčių.<br></br><br></br>Pakeitimams „Sukurta“ ir „Atnaujinta“ bus išvardyti laukai sukurtame arba pakeistame įraše.<br></br><br></br>Pakeitimų tipams „Įtraukta“ bus išvardyti antrinio įrašo laukai.<br></br><br></br>**Pavyzdys:**<br></br><br></br>„{“<br></br>  "msdyn_applyurl": { "newValue": "" },<br></br>  "msdyn_description": { "valueOmitted": true } <br></br>„}“ |
|Darbo paraiškų istorija | Darbo paraiška (msdyn_JobapplicatonId)<br></br>Būsena (msdyn_status) <br></br>Būsenos priežastis (msdyn_statusreason) <br></br>Atmetimo priežastis (msdyn_rejectionreason) |
| Darbo pasiūlymo istorija | Darbo pasiūlymas (msdyn_JobopeningId) <br></br>Būsena (msdyn_jobopeningstatus) <br></br>Būsenos priežastis (msdyn_jobopeningstatusreason) |
| Kandidato istorija | Kandidatas (msdyn_CandidateId) |
