---
title: Dimensijomis paremto bendrojo produkto komplektavimo specifikacijos kūrimas
description: Norėdami atlikti šią procedūrą, turite būti atlikę ankstesnius 4 šios aštuonių įrašų sekos vadovus.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 677aacb72d1c3f33bed8bb6c9cd32e5dbca677cc
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844926"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Dimensijomis paremto bendrojo produkto komplektavimo specifikacijos kūrimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

