---
title: Kurti ir priskirti savikainos paskirstymo strategiją savikainos kontrolės įtaisui
description: Naudokite šią procedūrą norėdami sukurti ir priskirti savikainos paskirstymo strategiją ir atitinkamas taisykles savikainos kontrolės įtaisui.
author: twheeloc
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5082f4e80958ddb1e4a79bfe46df4a621f10fc40
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734253"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a>Kurti ir priskirti savikainos paskirstymo strategiją savikainos kontrolės įtaisui

[!include [banner](../../includes/banner.md)]

Naudokite šią procedūrą norėdami sukurti ir priskirti savikainos paskirstymo strategiją ir atitinkamas taisykles savikainos kontrolės įtaisui. Šiame įraše naudojama demonstracinių duomenų įmonė USP2.


## <a name="create-a-policy"></a>Sukurkite strategiją
1. Eikite į **kaštų apskaitos > strategijos > išlaidų paskirstymo strategijas**.
2. Spustelėkite **Naujas**.
3. **Lauke Strategijos pavadinimas** įveskite vertę.
4. Lauke Išlaidų **objekto dimensijų hierarchija** įveskite arba pasirinkite vertę.
    * Pasirinkti organizaciją  
5. Lauke Statistinė **dimensija** įveskite arba pasirinkite vertę.
6. Spustelėkite **Įrašyti**.

## <a name="create-allocation-rules"></a>Sukurkite paskirstymo taisykles
1. Spustelėkite **Naujas**.
2. Sąraše pažymėkite pasirinktą eilutę.
3. Lauke Išlaidų **objekto dimensijų hierarchijos** mazgas įveskite arba pasirinkite vertę.
4. Lauke Išlaidų **veikimo būdas** pasirinkite Bendroji suma.
5. **Lauke Paskirstymo pagrindas** įveskite arba pasirinkite vertę.
6. Spustelėkite **Naujas**.
7. Sąraše pažymėkite pasirinktą eilutę.
8. Lauke Išlaidų **objekto dimensijų hierarchijos** mazgas įveskite arba pasirinkite vertę.
9. Lauke Išlaidų **veikimo būdas** pasirinkite Bendroji suma.
10. **Lauke Paskirstymo pagrindas** įveskite arba pasirinkite vertę.
11. Spustelėkite **Naujas**.
12. Sąraše pažymėkite pasirinktą eilutę.
13. Lauke Išlaidų **objekto dimensijų hierarchijos** mazgas įveskite arba pasirinkite vertę.
14. Lauke Išlaidų **veikimo būdas** pasirinkite Bendroji suma.
15. **Lauke Paskirstymo pagrindas** įveskite arba pasirinkite vertę.
    * Tęskite, kol sukursite visas taisykles.  
16. Spustelėkite **Įrašyti**.

## <a name="assign-the-policy-to-a-cost-control-unit"></a>Priskirkite strategiją savikainos kontrolės įtaisui
1. Spustelėkite **išlaidų kontrolės vieneto strategijos priskyrimus**.
2. Spustelėkite **Naujas**.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Lauke Galioja **nuo apskaitos** datos įveskite datą.
    * Taisyklės taikomos pagal datą. Vartotojas arba sistema gali baigti taisyklių galiojimą, jei sukurta naujesnė versija.  
5. Lauke Išlaidų **valdymo vienetas** įveskite arba pasirinkite vertę.
6. Spustelėkite **Įrašyti**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
