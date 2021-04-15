---
title: Užduoties įrašų saugos diagnostika
description: Šioje temoje pateikiama informacija apie tai, kaip analizuoti ir valdyti saugos teisių reikalavimus, paremtus užduoties įrašu.
author: Peakerbl
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: cb4d544d8d74ad10432901381253f84ec9331ae7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745770"
---
# <a name="security-diagnostics-for-task-recordings"></a>Užduoties įrašų saugos diagnostika

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a>Prieš pradedant

Šioje temoje pateikiama informacija apie tai, kaip analizuoti ir valdyti saugos teisių reikalavimus, paremtus užduoties įrašu. Prieš atlikdami šioje temoje aprašytus veiksmus, turite turėti verslo proceso, kurį norite analizuoti, užduoties įrašą. Norėdami įrašyti verslo procesą, žr. [Užduočių įrašymo priemonės ištekliai](../../user-interface/task-recorder.md). 

## <a name="manage-security-for-a-task-recording"></a>Užduoties įrašo saugos valdymas

1. Eikite į **Sistemos administravimas** > **Sauga** > **Užduoties įrašo saugos diagnostika**.
2. Atidarykite užduoties įrašą iš jo buvimo vietos. Pasirinkite **Atidaryti iš šio kompiuterio** arba **Atidaryti iš „Lifecycle Services”** ir pasirinkite **Uždaryti**.
3. Atsidarys puslapis **Saugos meniu elementų informacija**, kuriame pateikiami procesui būtini saugos objektai.

 > [!NOTE]
 > Meniu elementai **Veiksmas** ir **Išvestis** nėra įtraukti į sąrašą.

4. Lauke **Vartotojo ID** pasirinkite vartotoją. Jei vartotojas neturi kai kurių meniu elementų teisių, laukas **Trūkstamos teisės** bus atnaujintas į **Taip**.
  
  ![Saugos meniu elementų informacijos puslapis](../media/Security-Menu-Item-Details.png)

5. Pasirinkite **Įtraukti nuorodą**, kad peržiūrėtumėte saugos objektų sąrašą, įskaitant vaidmenis, pareigas ir teises, pagal kurias suteikiama trūkstama teisė.
6. Pasirinkite saugos objektą sąraše.

    - Jei pasirinkta **Vaidmuo**, pasirinkite **Įtraukti vaidmenį vartotojui**. Atsidarys puslapis **Priskirti vartotojus vaidmenims**. Norėdami gauti daugiau informacijos, žr. puslapį [Vartotojų priskyrimas saugos vaidmenims](assign-users-security-roles.md).
    - Jei pasirinkta **Pareiga**, pasirinkite **Įtraukti pareigą vaidmeniui**, tada pasirinkite vaidmenis, į kuriuos turi būti įtraukta pareiga, tada – **Gerai**.
    - Jei pasirinkta **Teisė**, pasirinkite **Įtraukti teisę pareigoms**, tada pasirinkite vaidmenis, į kuriuos turi būti įtraukta pareiga, tada – **Gerai**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]