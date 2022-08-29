---
title: Užduoties įrašų saugos diagnostika
description: Šiame straipsnyje pateikiama informacija apie tai, kaip analizuoti ir tvarkyti saugos teisių reikalavimus, remiantis užduoties įrašu.
author: Peakerbl
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.search.form: ''
ms.openlocfilehash: e564a0499cb1a5dc00fc027c20a027f9b454600c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272527"
---
# <a name="security-diagnostics-for-task-recordings"></a>Užduoties įrašų saugos diagnostika

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a>Prieš pradedant

Šiame straipsnyje pateikiama informacija apie tai, kaip analizuoti ir tvarkyti saugos teisių reikalavimus, remiantis užduoties įrašu. Prieš pradėdami šiame straipsnyje nurodytus veiksmus, turite turėti verslo proceso, kurį norite analizuoti, užduoties įrašymą. Norėdami įrašyti verslo procesą, žr. [Užduočių įrašymo priemonės ištekliai](../../user-interface/task-recorder.md). 

## <a name="manage-security-for-a-task-recording"></a>Užduoties įrašo saugos valdymas

1. Eikite į **Sistemos administravimas** > **Sauga** > **Užduoties įrašo saugos diagnostika**.
2. Atidarykite užduoties įrašą iš jo buvimo vietos. Pasirinkite **Atidaryti iš šio kompiuterio** arba **Atidaryti iš „Lifecycle Services”** ir pasirinkite **Uždaryti**.
3. Atsidarys puslapis **Saugos meniu elementų informacija**, kuriame pateikiami procesui būtini saugos objektai.

 > [!NOTE]
 > Meniu elementai **Veiksmas** ir **Išvestis** nėra įtraukti į sąrašą.

4. Lauke **Vartotojo ID** pasirinkite vartotoją. Jei vartotojas neturi kai kurių meniu elementų teisių, laukas **Trūkstamos teisės** bus atnaujintas į **Taip**.
  
  ![Saugos meniu elementų informacijos puslapis.](../media/Security-Menu-Item-Details.png)

5. Pasirinkite **Įtraukti nuorodą**, kad peržiūrėtumėte saugos objektų sąrašą, įskaitant vaidmenis, pareigas ir teises, pagal kurias suteikiama trūkstama teisė.
6. Pasirinkite saugos objektą sąraše.

    - Jei pasirinkta **Vaidmuo**, pasirinkite **Įtraukti vaidmenį vartotojui**. Atsidarys puslapis **Priskirti vartotojus vaidmenims**. Norėdami gauti daugiau informacijos, žr. puslapį [Vartotojų priskyrimas saugos vaidmenims](assign-users-security-roles.md).
    - Jei pasirinkta **Pareiga**, pasirinkite **Įtraukti pareigą vaidmeniui**, tada pasirinkite vaidmenis, į kuriuos turi būti įtraukta pareiga, tada – **Gerai**.
    - Jei pasirinkta **Teisė**, pasirinkite **Įtraukti teisę pareigoms**, tada pasirinkite vaidmenis, į kuriuos turi būti įtraukta pareiga, tada – **Gerai**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
