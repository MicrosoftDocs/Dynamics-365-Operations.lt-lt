---
title: 'ER: konfigūracijos importavimas iš „Lifecycle Services‟'
description: Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo rolę turintis vartotojas gali importuoti naują elektroninių ataskaitų (ER) versiją iš „Microsoft Lifecycle Services‟ (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 036d7e7e3f79e0945d6fef866a30edd41e688c07
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551327"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a>ER: konfigūracijos importavimas iš „Lifecycle Services‟

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo rolę turintis vartotojas gali importuoti naują elektroninių ataskaitų (ER) versiją iš „Microsoft Lifecycle Services‟ (LCS).

Šiame pavyzdyje pasirinksite pavyzdinės įmonės „Litware, Inc“ pageidaujamą ER konfigūraciją ir nusiųsite į LCS. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijas visos įmonės naudoja bendrai. Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti procedūros „ER konfigūracijos nusiuntimas į „Lifecycle Services‟“ veiksmus. Norint atlikti šiuos veiksmus, taip pat reikia prieigos prie LCS.

1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
2. Spustelėkite „Konfigūracijos“.

## <a name="delete-a-shared-version-of-data-model-configuration"></a>Duomenų modelio konfigūracijos bendrai naudojamos versijos naikinimas
1. Medyje pasirinkite „Modelio konfigūracijos pavyzdys‟.
    * Pirmoji modelio konfigūracijos pavyzdžio versija sukurta ir publikuota LCS portale atliekant procedūrą „ER konfigūracijos nusiuntimas į „Lifecycle Services‟‟. Atlikdami šią procedūrą, šią ER konfigūracijos versiją panaikinsite. Ši pavyzdžio duomenų modelio konfigūracijos versija bus importuota vėliau iš LCS.  
2. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkite šios konfigūracijos versiją, kurios būsena – „Bendrai naudojama‟. Ši būsena nurodo, kad konfigūracija publikuota LCS portale.  
3. Spustelėkite keisti būseną.
4. Spustelėkite Nebenaudoti.
    * Kad galėtumėte pasirinktą versiją panaikinti, jos būseną pakeiskite iš „Bendrai naudojama" į „Nebenaudojama‟.  
5. Spustelėkite GERAI.
6. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkite šios konfigūracijos versiją, kurios būsena – „Nebenaudojama‟.  
7. Spustelėkite Naikinti.
8. Spustelėkite Taip.
    * Atkreipkite dėmesį, kad galima naudoti tik 2 pasirinktos duomenų modelio konfigūracijos juodraščio versiją.  
9. Uždarykite puslapį.

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a>Duomenų modelio konfigūracijos bendrai naudojamos versijos importavimas iš LCS
1. Sąraše pažymėkite pasirinktą eilutę.
    * Atidarykite „Litware, Inc.‟ konfigūracijų teikėjo saugyklų sąrašą.  
2. Spustelėkite Saugyklos.
3. Spustelėkite Atidaryti.
    * Pasirinkite LCS saugyklą ir ją atidarykite.  
4. Sąraše pažymėkite pasirinktą eilutę.
    * Versijų sąraše pasirinkite pirmąją modelio konfigūracijos pavyzdžio versiją.  
5. Spustelėkite Importuoti.
6. Spustelėkite Taip.
    * Patvirtinkite pasirinktos versijos importavimą iš LCS.  
    * Atkreipkite dėmesį, kad informaciniu pranešimu (virš formos) patvirtinamas sėkmingas pasirinktos versijos importavimas.  
7. Uždarykite puslapį.
8. Uždarykite puslapį.
9. Spustelėkite „Konfigūracijos“.
10. Medyje pasirinkite „Modelio konfigūracijos pavyzdys‟.
11. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkite šios konfigūracijos versiją, kurios būsena – „Bendrai naudojama‟.  
    * Atkreipkite dėmesį, kad dabar taip pat galima naudoti ir 1 pasirinktos duomenų modelio konfigūracijos bendrai naudojamą versiją.  

