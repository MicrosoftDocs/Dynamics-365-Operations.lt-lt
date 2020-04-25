---
title: Gyvenimo įvykių apdorojimas
description: Programoje „Microsoft Dynamics 365 Human Resources“ darbuotojo ciklo metu kiekvienas darbuotojas gali susidurti su įvairiais gyvenimo įvykių pokyčiais.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba8d21482a18c6baa93437fc65c165907bdb515d
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229939"
---
# <a name="process-life-events"></a>Gyvenimo įvykių apdorojimas

Programoje „Microsoft Dynamics 365 Human Resources“ darbuotojo ciklo metu kiekvienas darbuotojas gali susidurti su įvairiais gyvenimo įvykių pokyčiais. Pavyzdžiui, santuoka, užimtumo pokytis arba priklausomojo / gavėjo pokytis. Norėdami naudoti gyvenimo įvykius, turite gyvenimo įvykius įgalinti išmokų parametrų formoje, nustatyti gyvenimo įvykių tipus ir nustatyti planų tipų gyvenimo įvykių parinktis.

Kad galėtumėte apdoroti gyvenimo įvykius, turite bent kartą jau būti paleidę atvirą registraciją per samdos laiko intervalą. Jungtinėse Valstijose atvira registracija paprastai vyksta kartą per metus. Už Jungtinių Valstijų ribų atvira registracija gali būti vykdoma samdos metu. Darbininkui nereikia pasirinkti išmokos plano, kad būtų galima apdoroti gyvenimo įvykius, tačiau jie turi būti įtraukti į atviros registracijos apdorojimą. 

Naudokite gyvenimo įvykių apdorojimą, kai yra darbininkų, kurių gyvenimo įvykiai įvyks ateityje. Šiuo įvykiu apdorojami visi neapdoroti gyvenimo įvykiai (pvz., būsimi gyvenimo įvykiai arba įtraukti gyvenimo įvykiai, kurie nėra būdingi konkretiems darbininkams – vienas pavyzdžių yra nauja išmoka). Realiojo laiko gyvenimo įvykiai yra paslėpti.

Pavyzdžiui, jei šiandien vasario 1 d., o vasario 14 d. planuojama, kad darbininkas Joe Smith pakeis juridinius subjektus, jei vykdote gyvenimo įvykių apdorojimą vasario 15 d., sistema apdoroja visus įvykius iki vasario 15 d. 

1. Darbo srities **Išmokų valdymas** dalyje **Apdorojimas** pasirinkite **Gyvenimo įvykių apdorojimas**.

2. Dialogo lange **Vykdyti gyvenimo įvykių apdorojimą** nurodykite šių laukų vertes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Registracijos laikotarpis** | Gyvenimo įvykių apdorojimo registracijos laikotarpis. |
   | **Juridinis subjektas** | Gyvenimo įvykių apdorojimo juridinis subjektas. |
   | **Gyvenimo įvykio data** | Sistema apdoroja visus įvykius registravimo laikotarpiu, kurie įvyksta iki šios datos. |
   | **Darbininkas** | Gyvenimo įvykių apdorojimo darbininkas. Jei paliksite šį lauką tuščią, visųdarbininkų gyvenimo įvykiai bus apdorojami. |

3. Jei norite vykdyti procesą fone, pasirinkite **Vykdyti fone** ir atlikite šias užduotis:

   1. Įveskite proceso informaciją.

   2. Norėdami nustatyti pasikartojančią užduotį, pasirinkite **Pasikartojimas**, įveskite pasikartojimo informaciją ir pažymėkite **Gerai**.

   3. Norėdami nustatyti užduoties įspėjimą, pasirinkite **Įspėjimai**, pasirinkite gautinus įspėjimus, tada pažymėkite **Gerai**.

   4. Pasirinkite **Gerai**. Procesas bus vykdomas naudojant jūsų nustatytus parametrus.

4. Pasirinkite **Gerai**.
