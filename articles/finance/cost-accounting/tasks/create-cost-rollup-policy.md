---
title: Kurti savikainos sumavimo strategija
description: Ši procedūra parodo, kaip sukurti savikainos sumavimo strategiją ir sukurti taisykles strategijai.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0a648984a8b4aaa314707e72a615f516116a193
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990747"
---
# <a name="create-a-cost-rollup-policy"></a>Kurti savikainos sumavimo strategija

[!include [banner](../../includes/banner.md)]

Ši procedūra parodo, kaip sukurti savikainos sumavimo strategiją ir sukurti taisykles strategijai. Kuriant šią procedūrą buvo naudojami USP2 demonstraciniai duomenys.


## <a name="create-a-policy"></a>Sukurkite strategiją
1. Eikite į Išlaidų apskaita > Strategijos > Savikainos sumavimo strategijos.
2. Spustelėkite Naujas.
3. Lauke Strategijos pavadinimas įrašykite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Lauke Savikainos objekto dimensijų hierarchija įveskite arba pasirinkite reikšmę.
    * Pasirinkite Savikainos sumavimo CC.  
6. Lauke Savikainos elementų dimensijų hierarchija įveskite arba pasirinkite reikšmę.
    * Pasirinkite Savikainos sumavimo CC.  
7. Spustelėkite Įrašyti.

## <a name="create-rules-for-the-cost-rollup-policy"></a>Sukurkite savikainos sumavimo strategijos taisykles
1. Spustelėkite Naujas.
2. Sąraše pažymėkite pasirinktą eilutę.
3. Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.
    * Pasirinkite 007.  
4. Lauke Savikainos elementų dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.
    * Pasirinkite Savikainos sumavimo CE.  
5. Lauke Antrinis savikainos elementas įveskite arba pasirinkite reikšmę.
    * Šiam pavyzdžiui priskirkite antrinį savikainos elementą CC-007 išlaidų centrui.  
6. Spustelėkite Naujas.
7. Sąraše pažymėkite pasirinktą eilutę.
8. Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.
    * Pasirinkite 008.  
9. Lauke Savikainos elementų dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.
    * Pasirinkite Savikainos sumavimo CE.  
10. Lauke Antrinis savikainos elementas įveskite arba pasirinkite reikšmę.
    * Šiam pavyzdžiui priskirkite antrinį savikainos elementą CC-008 išlaidų centrui.  
11. Spustelėkite Naujas.
12. Sąraše pažymėkite pasirinktą eilutę.
13. Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.
    * Pasirinkite 009.  
14. Lauke Savikainos elementų dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.
    * Pasirinkite Savikainos sumavimo CE.  
15. Lauke Antrinis savikainos elementas įveskite arba pasirinkite reikšmę.
    * Šiam pavyzdžiui priskirkite antrinį savikainos elementą CC-009 išlaidų centrui.  
    * Tęskite, kol visi išlaidų centrai bus susieti su jų atitinkamais antrinės savikainos elementais.  
16. Spustelėkite Įrašyti.

