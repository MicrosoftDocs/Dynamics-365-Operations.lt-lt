---
title: Veiklos ryšio kūrimas – vėlesnė veikla
description: „Lean“ gamybos eigos veiklų srautas dokumentuojamas naudojantis veiklų ryšiais.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e46dda12d4ad2b23ee86d240e6cdd8a1d46f1838
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829239"
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
    * Jei tuo pačiu metu vykdomos abi veiklos, ciklo laiko koeficientas turi būti 1. Jei ankstesnė veikla paleidžiama dvigubai greičiau už vėlesnę veiklą, koeficientas turi būti 2.   Ciklo laiko santykiai naudojami apskaičiuoti gamybos eigos veiklos ciklo laikus.  
9. Spustelėkite GERAI.
10. Uždarykite puslapį.
11. Spustelėkite skirtuką GridPanel.
12. Uždarykite puslapį.
13. Atnaujinkite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]