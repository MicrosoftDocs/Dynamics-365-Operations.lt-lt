---
title: Konfigūruoti savikainos objekto valdiklio prieigos teises
description: Pasinaudokite šia procedūra, norėdami konfigūruoti prieigos teises savikainos objekto kontrolieriui.
author: kfend
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 17615ff70c15789ac30223464b20ccd61a1bad55
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710648"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a>Konfigūruoti savikainos objekto valdiklio prieigos teises

[!include [banner](../../includes/banner.md)]

Pasinaudokite šia procedūra, norėdami konfigūruoti prieigos teises savikainos objekto kontrolieriui. Šiame įraše naudojama demonstracinių duomenų įmonė USP2.


## <a name="assign-the-cost-object-controller-role"></a>Priskirti išlaidų objekto kontrolieriaus vaidmenį
1. Pasirinkite Sistemos administravimas > Vartotojai > Vartotojai.
2. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pavyzdžiui, filtruokite lauką Vartotojo vardas, naudodami reikšmę „alicia‟.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Spustelėkite „Priskirti vaidmenis“.
5. Sąraše raskite ir pasirinkite norimą įrašą.
6. Spustelėkite GERAI.

## <a name="enable-access-list-security"></a>Įgalinti prieigos sąrašo saugą
1. Eikite į Išlaidų apskaita > Dimensijos > Dimensijų hierarchijos.
2. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkti organizaciją  
3. Spustelėkite Redaguoti.
4. Pasirinkite Taip lauke Prieigos sąrašo hierarchija.
5. Spustelėkite Peržiūrėti hierarchiją.

## <a name="assign-access-rights-to-user"></a>Priskirti prieigos teises vartotojui
1. Spustelėkite Naujas.
2. Sąraše pažymėkite pasirinktą eilutę.
3. Lauke Vartotojo ID įveskite arba pasirinkite vertę.
    * Pasirinkite Admin.  
4. Medyje pasirinkite „Organization\CEO\CFO\FIM“.
5. Spustelėkite Naujas.
6. Sąraše pažymėkite pasirinktą eilutę.
7. Lauke Vartotojo ID įveskite arba pasirinkite vertę.
    * Pasirinkite Alicia.  
8. Spustelėkite Įrašyti.

## <a name="enable-access-rights-in-cost-accounting"></a>Įgalinti išlaidų apskaitos prieigos teises
1. Eikite į Savikainos apskaita > Sąranka > Parametrai.
2. Spustelėkite skirtuką Bendra.
3. Pasirinkite Taip lauke Įgalinti savikainos objekto dimensijos narių peržiūros prieigą.
4. Spustelėkite Įrašyti.
5. Uždarykite puslapį.
6. Eikite į Savikainos apskaita > Sąranka > Savikainos kontrolės darbo srities konfigūracija.
7. Spustelėkite Redaguoti.
8. Lauke Paskelbta pasirinkite Taip.
    * Jei pasirenkate Taip, vartotojas, kuriam priskirtas vienas iš tolesnių keturių vaidmenų, gali matyti ataskaitas savikainos kontrolės darbo srityje: savikainos apskaitos vadovas, savikainos apskaitininkas, savikainos apskaitininko klerkas ir išlaidų objekto kontrolierius. Jei pasirenkate Ne, vartotojas, kuriam priskirtas vienas iš tolesnių vaidmenų, gali matyti ataskaitas: savikainos apskaitos vadovas, savikainos apskaitininkas ir savikainos apskaitininko klerkas.    
9. Spustelėkite Įrašyti.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
