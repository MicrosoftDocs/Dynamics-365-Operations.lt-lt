--- 
title: "Dimensijomis paremto bendrojo produkto komplektavimo specifikacijos kūrimas"
description: "Norėdami atlikti šią procedūrą, turite būti atlikę ankstesnius 4 šios aštuonių įrašų sekos vadovus."
author: YuyuScheller
manager: AnnBe
ms.date: 06/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: ae42eb317368fe14b043bc375f04cb11aaba8d5a
ms.contentlocale: lt-lt
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Dimensijomis paremto bendrojo produkto komplektavimo specifikacijos kūrimas

[!include[task guide banner](../../includes/task-guide-banner.md)]

Norėdami atlikti šią procedūrą, turite būti atlikę ankstesnius 4 šios aštuonių įrašų sekos vadovus. Pirmaisiais 4 įrašais nustatomi duomenys, kurių reikia norint atlikti šią procedūrą. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Šią užduotį paprastai atlieka produkto kūrėjas.


## <a name="select-the-product"></a>Produkto pasirinkimas
1. Spustelėkite Patvirtinto produkto priežiūra.
2. Spustelėkite Patvirtinti produktai.
3. Sąraše pažymėkite pasirinktą eilutę.
    * Raskite išleistą bendrąjį produktą su konfigūravimo pagal dimensijas technologija, kurį sukūrėte pirmajame šios sekos užduočių vadove.  
4. Veiksmų srityje spustelėkite Inžinierius.
5. Spustelėkite KS versijos.

## <a name="create-new-bom-and-bom-version"></a>Naujos KS ir KS versijos kūrimas
1. Spustelėkite Naujas.
2. Spustelėkite KS ir KS versija.
3. Lauke Pavadinimas surinkite reikšmę.
    * Vietos nustatymas  
    * Atlikdami šią procedūrą konkrečios KS vietos nenustatome.  
4. Spustelėkite GERAI.
5. Spustelėkite Naujas.
    * Atlikdami šią procedūrą, į KS įtrauksime keturias eilutes. Dviejose eilutėse nurodomos laidų parinktys ir dviejose eilutėse nurodomos spintelių parinktys.  
6. Sąraše pažymėkite pasirinktą eilutę.
7. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
    * Pasirinkite prekės numerį A0001, HDMI 6 pėd. laidai.  
8. Lauke Konfigūracijos grupė įveskite arba pasirinkite reikšmę.
    * Pasirinkite laidų konfigūracijos grupę, sukurtą 4-ajame šios sekos vadove.  
9. Spustelėkite Naujas.
    * Pasirinkite prekės numerį A0002, HDMI 12 pėd. laidai.  
10. Sąraše pažymėkite pasirinktą eilutę.
11. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
12. Lauke Konfigūracijos grupė įveskite arba pasirinkite reikšmę.
    * Vėl pasirinkite laidų konfigūracijos grupę.  
13. Spustelėkite Naujas.
14. Sąraše pažymėkite pasirinktą eilutę.
15. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
    * Pasirinkite prekės numerį D0002 Spintelė.  
16. Lauke Konfigūracijos grupė įveskite arba pasirinkite reikšmę.
    * Pasirinkite šios KS eilutės spintelių konfigūracijos grupę.  
17. Spustelėkite Naujas.
18. Sąraše pažymėkite pasirinktą eilutę.
19. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
    * Kaip paskutinę KS eilutę pasirinkite prekės numerį M0007 StandartinėSpintelė.  
20. Lauke Konfigūracijos grupė įveskite arba pasirinkite reikšmę.
    * Pasirinkite paskutinės KS eilutės spintelių konfigūracijos grupę.  

## <a name="approve-and-activate"></a>Patvirtinti ir aktyvinti
1. Uždarykite puslapį.
2. Spustelėkite „Patvirtinti“.
3. Lauke Patvirtino įveskite arba pasirinkite vertę.
4. Lange Ar norite patvirtinti ir KS? pasirinkite Taip. nurodytas operacijos numeris.
5. Spustelėkite GERAI.
6. Spustelėkite Aktyvinti.


