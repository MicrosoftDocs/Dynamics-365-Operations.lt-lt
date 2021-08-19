---
title: Įgūdžių konfigūravimas
description: Galite sekti savo darbuotojo įgūdžius „Dynamics 365 Human Resources” platformoje. Taip pat galite nurodyti įgūdžius, kurių reikia konkrečiam darbui.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a8025dd4000a3678e7f7eb7faebfa45852f0054570a2948dadbc21913c63f578
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732158"
---
# <a name="configure-skills"></a>Įgūdžių konfigūravimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Galite sekti savo darbuotojo įgūdžius „Dynamics 365 Human Resources” platformoje. Taip pat galite nurodyti įgūdžius, kurių reikia konkrečiam darbui.

Įgūdžių, kuriuos galite sekti, pavyzdžiai:

- Prižiūrėtojo – gebėjimas prižiūrėti kitų darbą.
- Vadovo – gebėjimas vadovauti darbuotojams ir verslo domenams.
- Planuotojo – gebėjimas žvelgti į priekį, formuluoti ir analizuoti planų vizijas.
- HTML – gebėjimas rašyti HTML kodą.

Jei dar nenustatėte įgūdžių tipų ir vertinimo modelių, turėsite juos įtraukti prieš kurdami įgūdžius.

Šie žmonės gali įvesti darbuotojo įgūdžius:

- Darbuotojai gali įvesti savo įgūdžius Darbuotojų savitarnoje. Šiuos įgūdžius privalo patvirtinti vadovas.
- Vadovai gali įvesti savo darbuotojų įgūdžius. Galite sukurti darbo eigą, automatiškai patvirtinančią šiuos įgūdžius.

## <a name="create-a-skill-type"></a>Įgūdžių tipo kūrimas

Įgūdžių tipai yra kategorijos, kurioms priklauso atskiri įgūdžiai, pavyzdžiui, Administravimas arba Pardavimas.

1. Darbo srityje **Darbuotojo plėtra** pasirinkite **Saitai**.

2. Dalyje **Kompetencijos sąranka** pasirinkite **Įgūdžių tipai**.

3. Pasirinkite **Naujas**.

4. Užpildykite toliau nurodytus laukus:

   - **Įgūdžių tipas**: Įveskite įgūdžių tipo pavadinimą.
   - **Aprašas**: Įveskite įgūdžių tipo aprašą.

5. Pasirinkite **Įrašyti**.

## <a name="create-a-rating-model"></a>Vertinimo modelio kūrimas

Vertinimo modelis padeda įvertinti asmens faktinį įgūdžių lygį, turimą pasiekti lygį arba darbui reikalingo įgūdžio lygį. Kiekvienam vertinimo modelio lygiui priskiriamas koeficientas.

1. Darbo srityje **Darbuotojo plėtra** pasirinkite **Saitai**.

2. Dalyje **Kompetencijos sąranka** pasirinkite **Vertinimo modeliai**.

3. Pasirinkite **Naujas**.

4. Užpildykite toliau nurodytus laukus:

   - **Vertinimas**: Įveskite vertinimo modelio pavadinimą, pavyzdžiui, **Įgūdžiai**.
   - **Aprašas**: Įveskite vertinimo modelio aprašą, pavyzdžiui, **Įgūdžių vertinimai**.

5. Dalyje **Lygiai** pasirinkite **Naujas**. Kiekvienam lygiui, kurį norite pridėti, užpildykite šiuos laukus:

   - **Lygis**: Įveskite lygio pavadinimą.
   - **Aprašas**: Įveskite lygio aprašą.
   - **Koeficientas**: Įveskite koeficiento vertę nuo 0 iki 9. Koeficientai padeda normalizuoti skirtingus vertinimo modelius naudojančių įgūdžių rezultatus. Kiekvienas lygis privalo turėti unikalų koeficientą. Didesnių koeficientų lygiai gali daryti didesnę įtaką vertinimo modeliui.

   Tęskite lygių pridėjimą, jei reikia. Kiekvienam vertinimo modeliui galite įvesti iki 10 lygių.

6. Pasirinkite **Įrašyti**.

## <a name="create-a-skill"></a>Įgūdžio kūrimas

Kad galėtumėte priskirti įgūdį, sukurti įgūdžių susiejimo iešką ar įgūdžių profilį, turite įvesti informaciją apie įgūdžius puslapyje **Įgūdžiai**. Kiekvieno įgūdžio atveju pasirinkite įgūdžio tipą ir vertinimo modelį.

1. Darbo srityje **Darbuotojo plėtra** pasirinkite **Saitai**.

2. Dalyje **Kompetencijos sąranka** pasirinkite **Įgūdžiai**.

3. Pasirinkite **Naujas**.

4. Užpildykite toliau nurodytus laukus:

   - **Įgūdis**: Įveskite įgūdžio pavadinimą.
   - **Aprašas**: Įveskite įgūdžio aprašą.
   - **Vertinimas**: Pasirinkite vertinimo modelį, kurį norite naudoti šiam įgūdžiui.
   - **Įgūdžių tipas**: Pasirinkite iš įgūdžių tipų sąrašo.

5. Pasirinkite **Įrašyti**.

## <a name="see-also"></a>Taip pat žiūrėkite

[Įgūdžių įvedimas](hr-develop-enter-skills.md)<br>
[Įgūdžių susiejimas](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]