---
title: Darbo eigos elementai
description: "Šiame straipsnyje aprašomi įvairūs elementai, sudarantys darbo eigą."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 05a35e91d3e502309c42c85960b5b1e2025f0e6e
ms.contentlocale: lt-lt
ms.lasthandoff: 04/25/2017


---

# <a name="workflow-elements"></a>Darbo eigos elementai

[!include[banner](../includes/banner.md)]


Šiame straipsnyje aprašomi įvairūs elementai, sudarantys darbo eigą.

Darbo eigą sudaro elementai. Tolesniuose skyriuose aprašomi visi elementų tipai.

## <a name="tasks"></a>Užduotys
*Užduotis* yra darbo vienetas, kurį reikia atlikti. Į darbo eigą galima įtraukti dviejų tipų užduotis: rankines užduotis ir automatizuotas užduotis.

### <a name="manual-task"></a>Rankiniu būdu nustatyta užduotis

*Rankinė užduotis* yra darbo vienetas, kurį turi atlikti vartotojas. Pavyzdžiui, išlaidų ataskaitų darbo eigoje gali būti rankinių užduočių, kurioms reikia priskirtų vartotojų, kad atliktų šiuos veiksmus:

-   Peržiūrėti kvitus, pateiktus kartu su išlaidų ataskaita.
-   Skambinti darbuotojo vadybininkui.

### <a name="automated-task"></a>Automatizuota užduotis

*Automatizuota užduotis* yra darbo vienetas, kurį turi atlikti sistema. Žmogui nereikia atlikti jokių veiksmų. Pavyzdžiui, pardavimo užsakymo darbo eigoje gali būti automatizuotų užduočių, kurioms reikia, kad sistema atliktų šiuos veiksmus:

-   Atlikite kredito tikrinimą.
-   Klientui sukurti kliento įrašą, jei jo dar nėra.

## <a name="approval-processes"></a>Patvirtinimo procesai
*Patvirtinimo procesas* yra procesas, susidedantis iš kelių žingsnių. Atlikdamas kiekvieną patvirtinimo veiksmą, vartotojas gali atlikti šiuos veiksmus:

-   Patvirtinti dokumentą.
-   Atmesti dokumentą.
-   Prašyti pakeisti dokumentą.
-   Priskirti dokumentą kitam vartotojui tvirtinti.

## <a name="lineitem-workflow-elements"></a>Eilutės elemento darbo eigos elementai
Galima sukurti darbo eigą tvarkyti dokumentus arba dokumento eilutės elementus. Pavyzdžiui, sukūrėte tabelių patvirtinimo darbo eigą. (Ši darbo eiga bus vadinama dokumento *darbo eiga*.) Į to dokumento darbo eigą galite įtraukti elementą *eilutės elemento darbo eiga*. Paleidus eilutės elementą, kiekvienas dokumento eilutės elementas pateikiamas apdoroti. Norėdami galite apdoroti visus eilutės elementus vykdydami tos pačios eilutės elemento darbo eigą arba galite kiekvieną eilutės elementą apdoroti atliekant skirtingas eilutės elemento darbo eigas. Įsivaizduokite, kad darbuotojas pateikė tabelį, panašų į tabelį toliau pateikiamame paveikslėlyje. ![Darbo eiga su eilutės elementais](./media/workflow_lineitemworkflow.gif) Tokiu atveju galbūt norėsite sukurti tokias eilutės elemento darbo eigas:

-   **1 eilutės elemento darbo eiga** – ši darbo eiga naudojama apdoroti eilutės elementus, kai projekto ID yra 1111.
-   **2 eilutės elemento darbo eiga** – ši darbo eiga naudojama apdoroti eilutės elementus, kai projekto ID yra 2222.
-   **3 eilutės elemento darbo eiga** – ši darbo eiga naudojama apdoroti eilutės elementus, kai projekto ID yra 3333.

## <a name="flowcontrol-elements"></a>Srauto valdiklių elementai
Šie elementai suteikia galimybę kurti darbo eigas, kurios turi alternatyvias šakas arba šakas, vykdomas tuo pačiu metu.

### <a name="manual-decision"></a>Neautomatinis sprendimas

*Rankinis sprendimas* – tai taškas, kuriame darbo eiga padalijama į dvi šakas. Vartotojas turi nuspręsti, o šis sprendimas nurodo, kuri šaka naudojama apdoroti pateiktą dokumentą.

### <a name="conditional-decision"></a>Sąlyginis sprendimas

*Sąlyginis sprendimas* – taip pat yra taškas, kuriame darbo eiga padalijama į dvi šakas. Tačiau sistema nusprendžia, kurią šaką naudoti apdorojant pateiktą dokumentą. Siekiant nuspręsti sistema įvertina dokumentą, kad nustatytų, ar jis atitinka nurodytas sąlygas.

### <a name="parallel-activity"></a>Lygiagreti veikla

*Lygiagreti veikla* – tai darbo eigos elementas, apimantis dvi ar daugiau vienu metu veikiančių darbo eigos šakų

### <a name="subworkflow"></a>Antrinė darbo eiga

*Antrinė darbo eiga* yra darbo eiga, kuri vyksta kitos darbo eigos kontekste.




