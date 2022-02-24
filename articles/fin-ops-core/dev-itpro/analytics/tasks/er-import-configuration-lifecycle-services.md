---
title: Konfigūracijos importavimas iš „Lifecycle Services‟
description: Šioje temoje aiškinama, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmenį turintis vartotojas gali importuoti naują elektroninių ataskaitų (ER) konfigūracijos versiją iš „Microsoft Dynamics Lifecycle Services‟ (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c43cdce8d073f04a3158c8beb13a5376e669a4c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684456"
---
# <a name="import-a-configuration-from-lifecycle-services"></a>Konfigūracijos importavimas iš „Lifecycle Services‟

[!include [banner](../../includes/banner.md)]

Šioje temoje aiškinama, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmenį turintis vartotojas gali importuoti naują [elektroninių ataskaitų (ER) konfigūracijos](../general-electronic-reporting.md#Configuration) versiją iš [projekto lygio turto bibliotekos](../../lifecycle-services/asset-library.md) „Microsoft Dynamics Lifecycle Services” (LCS).

Šiame pavyzdyje pasirinksite pavyzdinės įmonės pavadinimu „Litware, Inc“ pageidaujamą ER konfigūraciją ir nusiųsite į LCS. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijas visos įmonės naudoja bendrai. Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti [Konfigūracijos įkėlimas į „Lifecycle Services”](er-upload-configuration-into-lifecycle-services.md) veiksmus. Taip pat reikia prieigos prie LCS.

1. Prisijunkite prie programos naudodami vieną iš tolesnių vaidmenų.

    - Elektroninės ataskaitos kūrėjas
    - Sistemos administratorius

2. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
3. Pasirinkite **Konfigūracijos**.

<a name="accessconditions"></a>
> [!NOTE]
> Įsitikinkite, kad dabartinis „Dynamics 365 Finance” vartotojas yra LCS projekto, kuriame yra turto biblioteka, kurią vartotojas nori [pasiekti](../../lifecycle-services/asset-library.md#asset-library-support), naudojama ER konfigūracijoms importuoti, narys.
>
> Negalima pasiekti LCS projekto iš ER saugyklos, kuri nurodo domeną, kuris skiriasi nuo domeno, naudojamo „Finance”. Jei bandysite, bus rodomas tuščias LCS projektų sąrašas, o jūs negalėsite importuoti ER konfigūracijų iš projekto lygio turto bibliotekos, esančios LCS. Norėdami pasiekti projekto lygio turto bibliotekas iš ER saugyklos, naudojamos importuoti ER konfigūracijas, prisijunkite prie „Finance” naudodami vartotojo, priklausančio nuomotojui (domenui), kuriam sukonfigūruotas dabartinis „Finance” egzempliorius, kredencialus.

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a>Duomenų modelio konfigūracijos bendrai naudojamos versijos naikinimas

1. Puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite **Modelio konfigūracijos pavyzdys**.

    Sukūrėte pirmąją modelio konfigūracijos pavyzdžio versiją ir publikavote ją LCS atlikę [Konfigūracijos įkėlimas į „Lifecycle Services“](er-upload-configuration-into-lifecycle-services.md) veiksmus. Atlikdami šią procedūrą, šią ER konfigūracijos versiją panaikinsite. Tada versiją importuosite iš LCS, kaip aprašyta toliau šioje temoje.

2. Sąraše raskite ir pasirinkite norimą įrašą.

    Šiame pavyzdyje pasirinkite konfigūracijos versiją, kurios būsena – **Bendrinama**. Ši būsena nurodo, kad konfigūracija publikuota LCS portale.

3. Pasirinkti **Keisti būseną**.
4. Pasirinkite **Nebenaudoti**.

    Kad galėtumėte versiją panaikinti, jos būseną pakeiskite iš **Bendrinama** į **Nebenaudojama**.

5. Pasirinkite **Gerai**.
6. Sąraše raskite ir pasirinkite norimą įrašą.

    Šiame pavyzdyje pasirinkite konfigūracijos versiją, kurios būsena – **Nebenaudojama**.

7. Pasirinkite **Naikinti**.
8. Pasirinkite **Taip**.

    Atkreipkite dėmesį, kad dabar galima naudoti tik 2 pasirinktos duomenų modelio konfigūracijos juodraščio versiją.

9. Uždarykite puslapį.

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a>Duomenų modelio konfigūracijos bendrai naudojamos versijos importavimas iš LCS

1. Eikite į **Organizacijos administravimas \> Darbo sritys \> Elektroninės ataskaitos**.

2. Dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **„Litware, Inc.”**.

3. Plytelėje **„Litware, Inc.”** pasirinkite **Saugyklos**.

    Dabar galite atidaryti „Litware, Inc‟ konfigūracijos teikėjo saugyklų sąrašą.

4. Pasirinkite **Atidaryti**.

    Šiame pavyzdyje pasirinkite **LCS** saugyklą ir atidarykite. Turite turėti [prieigą](#accessconditions) prie LCS projekto ir turto bibliotekos, kuri pasiekiama naudojant pasirinktą ER saugyklą.

5. Sąraše pažymėkite pasirinktą eilutę.

    Šiame pavyzdyje versijų sąraše pasirinkite pirmąją **Modelio konfigūracijos pavyzdys** versiją.

6. Pasirinkite **Importuoti**.
7. Pasirinkite **Taip**, norėdami patvirtinti pasirinktos versijos importavimą iš LCS.

    Informacinis pranešimas patvirtina, kad pasirinkta versija buvo sėkmingai importuota.

8. Uždarykite puslapį.
9. Uždarykite puslapį.
10. Pasirinkite **Konfigūracijos**.
11. Medyje pasirinkite **Modelio konfigūracijos pavyzdys**.
12. Sąraše raskite ir pasirinkite norimą įrašą.

    Šiame pavyzdyje pasirinkite konfigūracijos versiją, kurios būsena – **Bendrinama**.

    Atkreipkite dėmesį, kad dabar taip pat galima naudoti ir 1 pasirinktos duomenų modelio konfigūracijos bendrai naudojamą versiją.
