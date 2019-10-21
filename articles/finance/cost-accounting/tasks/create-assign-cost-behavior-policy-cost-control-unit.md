---
title: Kurti ir priskirti savikainos veikimo būdo strategiją savikainos kontrolės įtaisui
description: Išlaidų taisyklė yra išlaidų klasifikavimas kaip fiksuotų arba kintamų.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16d9dceb4c2a22eab9a5ecb8501393444f20498b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187825"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a>Kurti ir priskirti savikainos veikimo būdo strategiją savikainos kontrolės įtaisui

[!include [task guide banner](../../includes/task-guide-banner.md)]

Išlaidų taisyklė yra išlaidų klasifikavimas kaip fiksuotų arba kintamų. Kainos kontrolės įtaisui turi būti priskirta strategija ir atitinkamos taisyklės, kad strategija pasidarytų veiksminga. Naudokite šią procedūrą norėdami sukurti strategiją, ir tada priskirkite strategiją išlaidų kontrolės įtaisui.


## <a name="create-a-cost-behavior-hierarchy"></a>Sukurkite išlaidų taisyklių hierarchiją
1. Eikite į Išlaidų apskaita > Dimensijos > Dimensijų hierarchijos.
2. Spustelėkite Naujas.
3. Spustelėkite Kurti.
4. Dimensijų hierarchijos pavadinimo lauke įveskite „Išlaidų taisyklės hierarchija“.
5. Lauke Dimensija įveskite arba pasirinkite reikšmę.
    * Pasirinkite Savikainos elementai.  
6. Spustelėkite Įrašyti.
7. Spustelėkite Peržiūrėti hierarchiją.
8. Spustelėkite Naujas.
9. Lauke Mazgo pavadinimas įrašykite reikšmę.
    * Įveskite Fiksuotą savikainą.  
10. Medyje pasirinkite „Išlaidų taisyklės hierarchija“.
11. Spustelėkite Naujas.
12. Lauke Mazgo pavadinimas įrašykite reikšmę.
    * Įveskite Kintamą savikainą.  
13. Spustelėkite Įrašyti.
14. Medyje pasirinkite „Cost behavior hierarchy\Fixed cost“.
15. Spustelėkite Naujas.
16. Sąraše pažymėkite pasirinktą eilutę.
17. Lauke Iš dimensijų nario įveskite arba pasirinkite reikšmę.
    * Dimensijos narių diapazone gali būti tarpų, tačiau nariai negali persidengti.  
18. Lauke Dimensijų nariui įveskite arba pasirinkite reikšmę.
    * Dimensijos narių diapazone gali būti tarpų, tačiau nariai negali persidengti.  
19. Medyje pasirinkite „Cost behavior hierarchy\Variable cost“.
20. Spustelėkite Naujas.
21. Sąraše pažymėkite pasirinktą eilutę.
22. Lauke Iš dimensijų nario įveskite arba pasirinkite reikšmę.
    * Dimensijos narių diapazone gali būti tarpų, tačiau nariai negali persidengti.  
23. Lauke Dimensijų nariui įveskite arba pasirinkite reikšmę.
    * Dimensijos narių diapazone gali būti tarpų, tačiau nariai negali persidengti.  
24. Spustelėkite Įrašyti.

## <a name="create-the-policy-and-rules"></a>Sukurkite strategiją ir taisykles
1. Eikite į Išlaidų apskaita > Strategijos > Išlaidų taisyklės strategijos.
2. Spustelėkite Naujas.
3. Lauke Strategijos pavadinimas įrašykite reikšmę.
4. Lauke Savikainos elementų dimensijų hierarchija įveskite arba pasirinkite reikšmę.
    * Pasirinkite savo ką tik sukurtą strategijos hierarchiją.  
5. Lauke Savikainos objekto dimensijų hierarchija įveskite arba pasirinkite reikšmę.
    * Pasirinkti organizaciją  
6. Spustelėkite Įrašyti.
7. Spustelėkite Naujas.
8. Sąraše pažymėkite pasirinktą eilutę.
9. Lauke Savikainos elementų dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.
    * Išplėskite hierarchiją, kad pasirinktumėte Kintamą savikainą.  
10. Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.
    * Numatytai kintamas procentas yra 100 procentų.  
11. Spustelėkite Savikainos kontrolės įtaiso strategijos priskyrimai.
12. Spustelėkite Naujas.
13. Sąraše pažymėkite pasirinktą eilutę.
14. Lauke Galioja nuo apskaitos datos įveskite datą.
    * Taisyklės taikomos pagal datą, ir vartotojas arba sistema gali baigti taisyklės galiojimą, jei sukurta naujesnė versija.  
15. Lauke Savikainos kontrolės įtaisas įveskite arba pasirinkite reikšmę.
16. Spustelėkite Įrašyti.
