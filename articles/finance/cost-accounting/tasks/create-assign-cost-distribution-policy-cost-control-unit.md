---
title: Kurti ir priskirti savikainos paskirstymo strategiją savikainos kontrolės įtaisui
description: Savikainos paskirstymo taisyklės naudojamos norint paskirstyti savikainą, kuri buvo finansiškai apskaičiuota kolektyviniame išlaidų centre.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostDistributionRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66921d5eddb31ffba0946c41f634719a684e4ad1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445924"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a>Kurti ir priskirti savikainos paskirstymo strategiją savikainos kontrolės įtaisui

[!include [banner](../../includes/banner.md)]

Savikainos paskirstymo taisyklės naudojamos norint paskirstyti savikainą, kuri buvo finansiškai apskaičiuota kolektyviniame išlaidų centre. Savikainos apskaitininkas užtikrina, kad savikaina būtų paskirstyta išlaidų centrams remiantis paskirstymo pagrindu. Strategija ir atitinkamos taisyklės priskiriamos savikainos kontrolės įtaisui. Šiame užduočių vedlyje naudojamas pavyzdys, norint parodyti, kaip sukurti savikainos paskirstymo strategiją ir atitinkamas taisykles.


## <a name="create-a-policy"></a>Sukurkite strategiją
1. Eikite į Išlaidų apskaita > Strategijos > Savikainos paskirstymo strategijos.
2. Spustelėkite Naujas.
3. Lauke Strategijos pavadinimas įrašykite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Lauke Savikainos objekto dimensijų hierarchija įveskite arba pasirinkite reikšmę.
    * Pasirinkti organizaciją  
6. Lauke Savikainos elementų dimensijų hierarchija įveskite arba pasirinkite reikšmę.
    * Pasirinkite CDS P/L.  
7. Lauke Statistikos dimensija įveskite arba pasirinkite reikšmę.
    * Pasirinkite statistinius elementus.  
8. Spustelėkite Įrašyti.

## <a name="create-rules-for-the-policy"></a>Sukurkite taisykles strategijai
1. Spustelėkite Naujas.
2. Sąraše pažymėkite pasirinktą eilutę.
3. Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.
    * Išplėskite hierarchiją, kad pasirinktumėte 094.  
4. Lauke Savikainos elementų dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.
    * Pasirinkite Kitos veiklos išlaidos ir tada pasirinkite 605110 valymas.  
5. Lauke Savikainos taisyklė pasirinkite parinktį.
    * Pasirinkite Fiksuota savikaina.  
6. Lauke Paskirstymo pagrindas įveskite arba pasirinkite reikšmę.
7. Spustelėkite Naujas.
8. Sąraše pažymėkite pasirinktą eilutę.
9. Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.
    * Išplėskite hierarchiją, kad pasirinktumėte 094.  
10. Lauke Savikainos elementų dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.
    * Pasirinkite Kitos veiklos išlaidos ir tada pasirinkite 605150 nuoma.  
11. Lauke Savikainos taisyklė pasirinkite parinktį.
    * Pasirinkite Fiksuota savikaina.  
12. Lauke Paskirstymo pagrindas įveskite arba pasirinkite reikšmę.
13. Spustelėkite Įrašyti.

## <a name="assign-rules-to-a-cost-control-unit"></a>Priskirkite taisykles išlaidų kontrolės įtaisui
1. Spustelėkite Savikainos kontrolės įtaiso strategijos priskyrimai.
2. Spustelėkite Naujas.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Lauke Galioja nuo apskaitos datos įveskite datą.
    * Pasirinkite tinkamų finansinių metų rugsėjo 1.  
5. Lauke Savikainos kontrolės įtaisas įveskite arba pasirinkite reikšmę.
6. Spustelėkite Įrašyti.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]