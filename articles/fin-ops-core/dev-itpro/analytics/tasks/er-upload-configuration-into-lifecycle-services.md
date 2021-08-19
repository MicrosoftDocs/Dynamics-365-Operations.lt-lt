---
title: Konfigūracijos nusiuntimas į „Lifecycle Services‟
description: Šioje temoje paaiškinama, kaip sukurti naują elektroninių ataskaitų (ER) konfigūraciją ir nusiųsti ją į „Microsoft Dynamics Lifecycle Services“ (LCS).
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b480351875c7d300db790a68d61a402218f8ee36d8247188b912762f21d035b3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720765"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a>Konfigūracijos nusiuntimas į „Lifecycle Services”

[!include [banner](../../includes/banner.md)]

Šioje temoje aiškinama, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmenį turintis vartotojas gali sukurti naują [elektroninių ataskaitų (ER) konfigūraciją](../general-electronic-reporting.md#Configuration) ir ją nusiųsti į [projekto lygio turto biblioteką](../../lifecycle-services/asset-library.md) „Microsoft Dynamics Lifecycle Services‟ (LCS).

> [!IMPORTANT]
> LCS naudojimas kaip ER konfigūracijų saugyklos yra [nerekomenduojamas](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Daugiau informacijos rasite [„Regulatory Configuration Service“ (RCS) – „Lifecycle Services“ (LCS) saugykla nerekomenduojama](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).

Šiame pavyzdyje sukursite pavyzdinės įmonės pavadinimu „Litware, Inc“ konfigūraciją ir nusiųsite į LCS. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijas visos įmonės naudoja bendrai. Norint atlikti šiuos veiksmus, pirmiausia reikia atlikti veiksmus, nurodytus [Sukurti konfigūracijų teikėjus ir juos pažymėti kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md). Taip pat reikia prieigos prie LCS.

1. Prisijunkite prie programos naudodami vieną iš tolesnių vaidmenų.

    - Elektroninės ataskaitos kūrėjas
    - Sistemos administratorius

2. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
3. Pasirinkite **„Litware, Inc.‟** ir nustatykite į **Aktyvi**.
4. Pasirinkite **Konfigūracijos**.

<a name="accessconditions"></a>
> [!NOTE]
> Įsitikinkite, kad dabartinis „Dynamics 365 Finance” vartotojas yra LCS projekto, kuriame yra [turto biblioteka](../../lifecycle-services/asset-library.md#asset-library-support), naudojama ER konfigūracijoms importuoti, narys.
>
> Negalima pasiekti LCS projekto iš ER saugyklos, kuri nurodo domeną, kuris skiriasi nuo domeno, naudojamo „Finance”. Jei bandysite, bus rodomas tuščias LCS projektų sąrašas, o jūs negalėsite importuoti ER konfigūracijų iš projekto lygio turto bibliotekos, esančios LCS. Norėdami pasiekti projekto lygio turto bibliotekas iš ER saugyklos, naudojamos importuoti ER konfigūracijas, prisijunkite prie „Finance” naudodami vartotojo, priklausančio nuomotojui (domenui), kuriam sukonfigūruotas dabartinis „Finance” egzempliorius, kredencialus.

## <a name="create-a-new-data-model-configuration"></a>Sukurti naują duomenų modelio konfigūraciją

1. Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.
2. Puslapyje **Konfigūracijos** pasirinkite **Kurti konfigūraciją**, kad atidarytumėte išplečiamąjį dialogo langą.

    Šiame pavyzdyje sukursite konfigūraciją, apimančią elektroninių dokumentų duomenų modelio pavyzdį. Ši duomenų modelio konfigūracija vėliau bus nusiųsta į LCS.

3. Lauke **Pavadinimas** įveskite **Modelio konfigūracijos pavyzdys**.
4. Lauke **Aprašas** įveskite **Modelio konfigūracijos pavyzdys**.
5. Pasirinkite **Kurti konfigūraciją**.
6. Pasirinkite **Modelio dizaino įrankis**.
7. Pasirinkite **Naujas**.
8. Lauke **Pavadinimas** įveskite **Įvesties taškas**.
9. Pasirinkite **Įtraukti**.
10. Pasirinkite **Įrašyti**.
11. Uždarykite puslapį.
12. Pasirinkti **Keisti būseną**.
13. Pasirinkite **Baigti**.
14. Pasirinkite **Gerai**.
15. Uždarykite puslapį.

## <a name="register-a-new-repository"></a>Naujos saugyklos registravimas

1. Eikite į **Organizacijos administravimas \> Darbo sritys \> Elektroninės ataskaitos**.

2. Dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **„Litware, Inc.”**.

3. Plytelėje **„Litware, Inc.”** pasirinkite **Saugyklos**.

    Dabar galite atidaryti „Litware, Inc‟ konfigūracijos teikėjo saugyklų sąrašą.

4. Pažymėkite **Įtraukti**, kad atidarytumėte išplečiamąjį dialogo langą.

    Dabar galite įtraukti naują saugyklą.

5. Lauke **Konfigūracijų saugykla** pasirinkite **LCS**.
6. Pasirinkite **Kurti saugyklą**.
7. Lauke **Projektas** įveskite arba pasirinkite vertę.

    Šiame pavyzdyje pasirinkite norimą LCS projektą. Turite turėti [prieigą](#accessconditions) prie projekto.

8. Pasirinkite **Gerai**.

    Baikite naują saugyklos įrašą.

9. Sąraše pažymėkite pasirinktą eilutę.

    Šiame pavyzdyje pasirinkite **LCS** saugyklos įrašą.

    Atkreipkite dėmesį, kad registruotą saugyklą pažymėjo dabartinis teikėjas. Kitaip tariant, perkelti į šią saugyklą ir vėliau nusiųsti į pasirinktą LCS projektą galima tik tam tiekėjui priklausančias konfigūracijas.

10. Pasirinkite **Atidaryti**.

    Atidarę saugyklą galėsite peržiūrėti ER konfigūracijų sąrašą. Jei pasirinktas projektas dar nenaudotas bendrinant ER konfigūracijas, sąrašas bus tuščias.

11. Uždarykite puslapį.
12. Uždarykite puslapį.

## <a name="upload-a-configuration-into-lcs"></a>Konfigūracijos nusiuntimas į LCS

1. Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.
2. Puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite **Modelio konfigūracijos pavyzdys**.

    Turite pasirinkti sukurtą, jau baigtą konfigūraciją.

3. Sąraše raskite ir pasirinkite norimą įrašą.

    Šiame pavyzdyje pasirinkite pasirinktos konfigūracijos versiją, kurios būsena – **Baigta**.

4. Pasirinkti **Keisti būseną**.
5. Pasirinkite **Bendrinti**.

    Konfigūracijos būsena pasikeičia iš **Baigta** į **Bendrinama**, kai konfigūracija publikuojama LCS.

6. Pasirinkite **Gerai**.
7. Sąraše raskite ir pasirinkite norimą įrašą.

    Šiame pavyzdyje pasirinkite konfigūracijos versiją, kurios būsena – **Bendrinama**.

    Atkreipkite dėmesį, kad pasirinktos versijos būsena pasikeitė iš **Baigta** į **Bendrinama**.

8. Uždarykite puslapį.
9. Pasirinkite **Saugyklos**.

    Dabar galite atidaryti „Litware, Inc‟ konfigūracijos teikėjo saugyklų sąrašą.

10. Pasirinkite **Atidaryti**.

    Šiame pavyzdyje pasirinkite **LCS** saugyklą ir atidarykite.

    Atkreipkite dėmesį, kad pasirinkta konfigūracija rodoma kaip pasirinkto LCS projekto turtas.

11. Atidarykite LCS nuėję į <https://lcs.dynamics.com>.
12. Atidarykite projektą, kuris buvo naudojamas anksčiau saugyklos registracijai.
13. Atidarykite projekto turto biblioteką.
14. Pasirinkite turto tipą **GER konfigūracija**.

    Turi būti nurodyta ER konfigūracija, kurią nusiuntėte.

    Atkreipkite dėmesį, kad, jei tiekėjai turi prieigą prie šio LCS projekto, nusiųstąją LCS konfigūraciją galima importuoti į kitą egzempliorių.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
