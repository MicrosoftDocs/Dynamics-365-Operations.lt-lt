---
title: Ataskaita KS baigtomis
description: "Šiame straipsnyje pateikiama informacija apie skelbiant KS baigtomis."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMReportFinish, BOMReportFinishMax
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53251
ms.assetid: 510d05a3-0073-438d-b0c4-b6a6df1882ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 318c88f88277a8300b1fcda5056a9a92c9a81eae
ms.lasthandoff: 03/31/2017


---

# <a name="report-boms-as-finished"></a>Ataskaita KS baigtomis

Šiame straipsnyje pateikiama informacija apie skelbiant KS baigtomis.

Puslapiai **Skelbti baigtu** ir **Maks. skelbti baigtu** naudojami skelbti komplektavimo specifikacijoms (KS) kaip baigtoms. Teoriškai KS skelbimo baigta procesas yra toks pats kaip gamybos užsakymo skelbimo baigtu procesas. Šis procesas gali būti naudojamas, pvz., paprastuose surinkimo ir komplektacijos procesuose, kuriuose išplėstinių gamybos užsakymų pajėgumų nereikia. Puslapyje **Skelbti baigta** kelias KS baigtomis galima skelbti paketu. Į **Max. ataskaita baigta** puslapis leidžia jums pranešti tik vieną KS baigtomis vienu metu. Į **paskelbti baigtu** puslapyje yra prieinama iš meniu elementą – atsargų valdymas, ir abu puslapiai yra, nes meniu elementai ant to **išleisti produktai** puslapis.

## <a name="report-as-finished-page"></a>Puslapis Skelbti baigtu
Jei puslapį **Skelbti baigtu** atidarote iš išleisto produkto, puslapyje jums siūloma standartinių atsargų numatytąjį kiekį skelbti baigtu. Pagal numatytąsias nuostatas rodoma aktyvi KS versija, tačiau, jei yra kitų patvirtintų versijų, KS versiją galite keisti. Šiame puslapyje taip pat galima naikinti įrašus ir kurti naujus išleistų produktų, kuriuos reikėtų skelbti baigtais, įrašus. Norėdami naudojant užklausą pasirinkti produktus, spustelėkite meniu elementą **Pasirinkti**. Galite rankiniu būdu patvirtinti pasirinktų produktų skelbimą baigtais spustelėdami **Gerai**. Arba, galite nustatyti, kad procesas būtų vykdomas paketu. Kai skelbimo baigtu procesas patvirtintas, sistema sugeneruoja KS žurnalą, kuriame apdorojamas registravimas atsargose. Šį žurnalą sudaro viena galutinio produkto eilutės prekė ir kiekvienos KS eilutės prekė. Galite kontroliuoti, ar žurnalas automatiškai registruojamas, ar paliekamas atidarytas, kad būtų galima papildomai koreguoti.

## <a name="max-report-as-finished-page"></a>Maks. Ataskaitos puslapio
Puslapyje **Maks. skelbti baigtu** kiekviena KS eilutė nurodo produkto vienetų, kuriuos galima skelbti baigtais, skaičių. Šis skaičiavimas yra paremtas faktinėmis turimomis kiekvienos medžiagos eilutės atsargomis. Šiame pavyzdyje vienas prekės numerio FG vienetas sunaudoja du žaliavos RM10 vinetus ir vieną žaliavos RM20 vienetą. Kadangi turima tik 10 RM10 vienetų, maksimalus FG, kurį galima skelbti baigtu, kiekis yra penki vienetai. Ši reikšmė rodoma lauke **Maks. skelbti baigtu**.

| Lygis | Prekės numeris | Kiekis | Turima | Maks. Skelbti baigtu |
|-------|-------------|----------|---------|-------------------------|
| 0     | FG          |  1       | 0       | 5                       |
| 1     | RM10        | -2       | 10      | 5                       |
| 1     | RM20        | -1       |  8      | 8                       |

## <a name="boms-that-have-multiple-levels"></a>KS, turinčios kelis lygius
Kai KS turi keletą lygių, kontroliuoti, kaip medžiagos yra apskaitomos visais lygiais, galite naudodami **Išskleidimo** lauką. Šį lauką galima rasti tiek puslapyje **Skelbti baigtu**, tiek puslapyje **Maks. skelbti baigtu**. Galimos toliau nurodytos pasirinktys:

-   **Niekada** – jei trūksta medžiagų, žemesnio lygio KS niekada neišskleidžiamos.
-   **Visada** – visos žemesnio lygio KS visiškai išskleidžiamos. Todėl nenaudojamos jokios laisvos turimos pusiau baigtų sudedamųjų prekių atsargos.
-   **Trūkumas** – žemesnio lygio KS išskleidžiamos tik tada, jei negalima gauti viso norimo medžiagos kiekio.

### <a name="example"></a>Pavyzdys

Šiame pavyzdyje skelbti baigtais galima tris galutinio produkto (prekės numeris FG) vienetus. KS yra dviejų lygių, kaip parodyta čia.

| Lygis | Prekės numeris | KS eilutės kiekis | Turima |
|-------|-------------|-------------------|---------|
| 0     | FG          |                   |         |
| 1     | COMP        | 1                 | 2       |
| 1     | RM          | 1                 |         |

Toliau pateiktose lentelėse rodoma, kaip **Išskleidimo** lauko nuostata veikia KS žurnalo eilučių generavimą. **Išskleidimas: niekada**

| Lygis | Prekės numeris | Kiekis |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | COMP        | -3       |

Kadangi ankstesnė lentelė rodo, tik prekės numeris COMP laikoma atimama leidinyje. Prekės numeris RM, kuris yra dalis iš COMP, ne sprogo žurnalo eilutei, ir dviejų turimų vienetų iš COMP nelaikomi. **Išskleidimas: visada**

| Lygis | Prekės numeris | Kiekis |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | RM          | -3       |

Šiuo atveju prekės numeris COMP išskleidžiamas į žaliavą, prekės numerį RM. Vertinant sunaudotiną RM kiekį, du turimi COMP vienetai neliečiami. **Išskleidimas: trūkumas**

| Lygis | Prekės numeris | Kiekis |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | COMP        | -2       |
| 1     | RM          | -1       |

Šiuo atveju į šiuos du turimus prekės numerio COMP vienetus atsižvelgiama. Tačiau kadangi reikia trijų prekės numerio FG vienetų, norint pagaminti papildomą vieną COMP vienetą, taip pat reikia vieno prekės numerio RM vieneto.


