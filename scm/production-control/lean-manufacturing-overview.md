---
title: "„Lean manufacturing“ apžvalga"
description: "Šiame skyriuje pateikiami „Microsoft Dynamics AX lean manufacturing“ funkcijų apžvalga ir aprašymas."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanBoardTransferJob, KanbanBoardWorkCell, KanbanJobSchedulingListPage, LeanProductionFlow
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19371
ms.assetid: 026c5605-6be7-4fdb-a6f2-8e37a806796c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 3c608f13c93446329702f07ef7e8bb08a29d87b9
ms.lasthandoff: 03/31/2017


---

# <a name="lean-manufacturing-overview"></a>„Lean manufacturing“ apžvalga

[!include[banner](../includes/banner.md)]


Šiame skyriuje pateikiami „Microsoft Dynamics AX lean manufacturing“ funkcijų apžvalga ir aprašymas.

„Lean manufacturing‟ siūlo įrankius, kuriuos galite naudoti „lean‟ operacijoms modeliuoti. Šie įrankiai palaiko ir skatina toliau nurodytas koncepcijas ir verslo veiklas.
-   Gamybos ir logistikos procesus modeliuojant kaip gamybos eigas, kurti „lean manufacturing‟ platformą.
-   Naudojant „kanban‟, diegti „lean‟ traukimo sistemą, siekiant signalizuoti paklausos reikalavimus.
-   Stebėti ir tvarkyti „kanban“ užduotis.

„Lean manufacturing‟ architektūrą programoje „Microsoft Dynamics AX 7‟ sudaro gamybos eigos, veiklos ir „kanban“ taisyklės. Šios struktūros yra visiškai integruotos su „Microsoft Dynamics AX 7‟ procesais. „Lean manufacturing‟ galite naudoti įvairių režimų gamybos aplinkoje, kurioje dera įvairios tiekimo, gamybos ir šaltinio parinkimo strategijos. Šios strategijos apima gamybos užsakymus, paketinius gamybos pramonės šakų užsakymus, pirkimo užsakymus ir perkėlimo užsakymus.
| **Svarbu **                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| „Microsoft Dynamics AX 7‟ galite naudoti, kad būtų palaikomas „lean manufacturing‟ įgyvendinimas su „kanban‟. Tačiau sėkmingas „lean‟ principų įgyvendinimas priklauso nuo naudojamų vidinių verslo procesų ir faktinių gamybos sąlygų bei aplinkos. |

## <a name="modeling-manufacturing-and-logistics-processes-as-production-flows"></a> Gamybos ir logistikos procesų modeliavimas kaip gamybos eigų
Norėdami sukurti „lean manufacturing‟ platformą, gamybos ir logistikos procesus modeliuokite kaip gamybos eigas. Šią veiklą sudaro toliau pateiktos užduotys.
1.  Identifikuokite procesus, kuriems norite įgyvendinti „lean‟ papildymo strategiją, ir šiuos procesus modeliuokite kaip gamybos eigas. Tada galite analizuoti ir racionalizuoti procesus. Vienas iš „lean‟ įgyvendinimo tikslų yra sumažinti atliekų, gerinant medžiagos ir informacijos srautą.
2.  Gamybos eigą apibrėžkite kaip veiklų seką, apibūdinančią medžiagos srautą. Perkėlimo veikla apibrėžia produkto ar produktų judėjimą iš vienos vietos į kitą. Proceso veikla apibrėžia pridėtinės vertės operaciją, kuri taikoma produktui.
3.  Sukurkite gamybos eigos versiją, apibrėžiančią vieneto gamybos laiko reikalavimus. Šie reikalavimai naudojami norint apskaičiuoti kiekvienos gamybos eigos veiklos ciklo laikus. Galite kurti kelias gamybos eigų versijas ir tada šias versijas naudoti procesams tobulinti.

## <a name="using-kanbans-to-signal-demand-requirements"></a> „Kanban‟ naudojamas siekiant signalizuoti paklausos reikalavimus
Traukimo sistema prekes gamina tik kai jų reikia. Ši praktika sumažina pristatymo vykdymo laiką ir atsargų perviršį. Galite naudoti „kanban‟ planuoti, stebėti ir apdoroti reikalavimams, paremtiems gamybos eigomis. Norėdami sukurti „kanban“ sistemą, sukurkite „kanban“ taisykles, apibrėžiančias, kada „kanban“ kuriamos ir kaip vykdomi reikalavimai. Galite kurti dviejų tipų „kanban“ taisykles. Gamybos taisyklės kuria „kanban‟ apdorojimo užduotis, o išėmimo „kanban“ taisyklės kuria „kanban‟ perkėlimo užduotis. Galite nustatyti šias papildymo strategijas:
-   **Fiksuoto kiekio** „kanban“ taisyklės yra susijusios su fiksuotu sandėliavimo vienetų skaičiumi, o tai reiškia, kad aktyvių „kanban‟ skaičius yra pastovus. Kai sunaudojami visi „kanban‟ produktai ir rankiniu būdu ištuštinami sandėliavimo vienetai, sukuriama nauja to paties tipo „kanban“. Kurdami fiksuoto kiekio „kanban‟ taisykles, galite apskaičiuoti optimalius naudojamus „kanban‟ kiekius ir produktų kiekius. Skaičiuojant atsižvelgiama į prognozę, faktinį poreikį iš atidarytų užsakymų, prekių papildymo vykdymo laiką ir praeities poreikius.
-   **Suplanuotos** „kanban“ taisyklės papildo reikalavimus, apskaičiuotus atliekant bendrąjį planavimą. Bendrasis planavimas generuoja suplanuotas „kanban‟, kurios gali būti patvirtintos ir tapti „kanban‟.
-   **Įvykio** „kanban“ taisyklės papildo reikalavimus, kurie kyla iš pardavimo užsakymų eilučių, gamybos KS eilučių, „kanban“ eilučių ar minimalių atsargų nuostatų. Kai sugeneruojamos įvykio „kanban‟, jos susiejamos su šaltinio reikalavimais.

Kuriant „kanban‟, pagal „kanban“ srauto veiklas, kurios yra apibrėžtos „kanban“ taisyklėse, generuojama viena ar kelios „kanban‟ užduotys.

## <a name="monitoring-and-maintaining-kanban-jobs"></a> „Kanban“ užduočių stebėjimas ir tvarkymas
Naudojant „lean manufacturing‟, galima matyti dabartinę gamybos ir logistikos veiklų, kurias valdo „kanban“ taisyklės, būseną. Todėl galite planuoti ir nustatyti prioritetą toliau nurodytoms užduotims.

-   Apžvelgti dabartinį „kanban“ užduočių grafiką.
-   Planuoti ir perplanuoti „kanban“ užduotis.
-   Sekti ir registruoti „kanban“ užduočių būseną.

Toliau pateiktame sąraše aprašomos specializuotos „kanban“ sritys.
-   „Kanban“ užduočių planavimas – apžvelgiamos „kanban“ užduotys. Srityje rodomos vieno ar kelių darbo elementų „kanban“ užduotys ir jų būsena. Užduotys išvardytos pagal planavimo laikotarpius (dienas ar savaites), kurie yra apibrėžti gamybos eigos modelyje. Srityje taip pat rodomos kiekvieno planavimo laikotarpio pajėgumų sąnaudos, kad galėtumėte stebėti suplanuotą apkrovą. Galite keisti „kanban“ užduočių būseną, „kanban“ užduotis perplanuoti skirtingiems planavimo laikotarpiams ir atlikti kitas užduotis.
-   Perkėlimo užduočių „kanban“ sritis – šioje srityje apžvelgiamos dabartinės perkėlimo užduotys. Galite atnaujinti ir registruoti išrinkimo dokumentus, pradėti ir užbaigti perkėlimo užduotis ir atlikti kitas užduotis.
-   Apdorojimo užduočių „kanban“ sritis – ši sritis skirta palaikyti įprastai gamybos eigai ir apžvelgti dabartinei situacijai viename ar keliuose darbo elementuose. Šioje srityje galima nustatyti „kanban‟ prioritetus, jas parinkti ar gaminti. Sritis taip pat skirta palaikyti brūkšninių kodų nuskaitymui teikiant „kanban‟ ataskaitas.

## <a name="kanban-jobs-and-integration-with-microsoft-dynamics-ax-processes"></a> „Kanban“ užduotys ir integracija su „Microsoft Dynamics AX‟ procesais
„Kanban‟ užduotys yra visiškai integruotos su dabartiniais „Microsoft Dynamics AX‟ atsargų operacijų procesais.
-   Galite atlikti parinkimo veiklas, kad papildytumėte medžiagą, naudojamą vykdyti „kanban“ užduočių reikalavimams.
-   Galite spausdinti „kanban“ korteles, cirkuliuojamąsias „kanban“ korteles ir išrinkimo dokumentus, kad būtų palaikomas „kanban“ naudojimas. Šie dokumentai naudojami atstoti, sekti ir registruoti „kanban“ užduotims sandėlyje ir gamybos ceche.
-   Registruoti atsargų išrinkimo ir perkėlimo veiklas galite nuskaitydami brūkšninius kodus.

Be to, „lean manufacturing‟ palaiko paslaugų, į kurias nurodo subrangos veiklos, pirkimo ir SF išrašymo procesus.
-   Subrangos veikloms galite priskirti pirkimo sutarčių eilutes ir paslaugas.
-   Galite kurti periodinius pirkimo užsakymus ir gavimo pažymas, kad būtų palaikomas paslaugų pirkimas ir sąskaitų faktūrų išrašymas.






