---
title: Veiklos ryšio kūrimas – vėlesnė veikla
description: „Lean“ gamybos eigos veiklų srautas dokumentuojamas naudojantis veiklų ryšiais.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dfd9d515b9417ce0142b7bf5db3485902968e4de
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149302"
---
# <a name="create-activity-relation---successor"></a>Veiklos ryšio kūrimas – vėlesnė veikla

[!include [banner](../../includes/banner.md)]

„Lean“ gamybos eigos veiklų srautas dokumentuojamas naudojantis veiklų ryšiais. Šiame įraše nurodoma, kaip sukurti veiklos ryšį.

Išankstiniai reikalavimai:

- Gamybos eiga ir versija juodraščio režimu. 

- Dvi gamybos eigoje viena po kitos sekančios veiklos yra sukuriamos, bet nesusiejamos.


## <a name="find-the-production-flow-version"></a>Kaip rasti gamybos eigos versiją 
1. Pasirinkite Gamybos kontrolė > Nustatymai > „Lean“ gamybos eiga > Gamybos eigos.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Sąraše pažymėkite pasirinktą eilutę.
5. Sąraše pasirinkite juodraščio versiją.
    * Veiklos ryšius galima įtraukti į gamybos eigos juodraščio arba aktyvias versijas.  

## <a name="open-the-activity-overview"></a>Kaip atidaryti veiklos apžvalgą
1. Spustelėkite Veiklos.
    * Atkreipkite dėmesį, kad formoje rodomos visos gamybos eigų, su kuriomis dirbate, versijai priskirtos gamybos eigos veiklos.  

## <a name="add-a-successor"></a>Kaip įtraukti vėlesnę veiklą
1. Spustelėkite Įtraukti vėlesnę veiklą.
2. Lauke Veikla spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
3. Sąraše raskite ir pasirinkite norimą įrašą.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Pažymėkite žymės langelį Apribojimas.
6. Lauke Apribojimo vertė įveskite skaičių.
    * Apribojimo laikas yra laikas nuo suplanuotos ankstesnės veiklos pabaigos (termino data ir laikas) iki suplanuotos vėlesnės veiklos pradžios.  
7. Lauke Vienetai įveskite reikšmę.
8. Lauke Ciklo laiko koeficientas įveskite skaičių.
    * Jei tuo pačiu metu vykdomos abi veiklos, ciklo laiko koeficientas turi būti 1. Jei ankstesnė veikla paleidžiama dvigubai greičiau už vėlesnę veiklą, koeficiantas turi būti 2.   Ciklo laiko santykiai naudojami, norint apskaičiuoti gamybos eigos veiklos ciklo laikus  
9. Spustelėkite GERAI.
10. Uždarykite puslapį.
11. Spustelėkite skirtuką GridPanel.
12. Uždarykite puslapį.
13. Atnaujinkite puslapį.

