---
title: Kurti ir priskirti savikainos paskirstymo strategiją savikainos kontrolės įtaisui
description: Naudokite šią procedūrą norėdami sukurti ir priskirti savikainos paskirstymo strategiją ir atitinkamas taisykles savikainos kontrolės įtaisui.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b22dba0106721c095e6ce2e9b76cb9f5267e1c28
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208732"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a>Kurti ir priskirti savikainos paskirstymo strategiją savikainos kontrolės įtaisui

[!include [banner](../../includes/banner.md)]

Naudokite šią procedūrą norėdami sukurti ir priskirti savikainos paskirstymo strategiją ir atitinkamas taisykles savikainos kontrolės įtaisui. Šiame įraše naudojama demonstracinių duomenų įmonė USP2.


## <a name="create-a-policy"></a>Sukurkite strategiją
1. Eikite į Išlaidų apskaita > Strategijos > Savikainos paskirstymo strategijos.
2. Spustelėkite Naujas.
3. Lauke Strategijos pavadinimas įrašykite reikšmę.
4. Lauke Savikainos objekto dimensijų hierarchija įveskite arba pasirinkite reikšmę.
    * Pasirinkti organizaciją  
5. Lauke Statistikos dimensija įveskite arba pasirinkite reikšmę.
6. Spustelėkite Įrašyti.

## <a name="create-allocation-rules"></a>Sukurkite paskirstymo taisykles
1. Spustelėkite Naujas.
2. Sąraše pažymėkite pasirinktą eilutę.
3. Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.
4. Lauke Savikainos taisyklės pasirinkite „Iš viso“.
5. Lauke Paskirstymo pagrindas įveskite arba pasirinkite reikšmę.
6. Spustelėkite Naujas.
7. Sąraše pažymėkite pasirinktą eilutę.
8. Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.
9. Lauke Savikainos taisyklės pasirinkite „Iš viso“.
10. Lauke Paskirstymo pagrindas įveskite arba pasirinkite reikšmę.
11. Spustelėkite Naujas.
12. Sąraše pažymėkite pasirinktą eilutę.
13. Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.
14. Lauke Savikainos taisyklės pasirinkite „Iš viso“.
15. Lauke Paskirstymo pagrindas įveskite arba pasirinkite reikšmę.
    * Tęskite, kol sukursite visas taisykles.  
16. Spustelėkite Įrašyti.

## <a name="assign-the-policy-to-a-cost-control-unit"></a>Priskirkite strategiją savikainos kontrolės įtaisui
1. Spustelėkite Savikainos kontrolės įtaiso strategijos priskyrimai.
2. Spustelėkite Naujas.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Lauke Galioja nuo apskaitos datos įveskite datą.
    * Taisyklės taikomos pagal datą. Vartotojas arba sistema gali baigti taisyklių galiojimą, jei sukurta naujesnė versija.  
5. Lauke Savikainos kontrolės įtaisas įveskite arba pasirinkite reikšmę.
6. Spustelėkite Įrašyti.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]