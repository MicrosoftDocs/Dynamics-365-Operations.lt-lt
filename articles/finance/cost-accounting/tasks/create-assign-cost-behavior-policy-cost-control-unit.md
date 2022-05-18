---
title: Kurti ir priskirti savikainos veikimo būdo strategiją savikainos kontrolės įtaisui
description: Išlaidų taisyklė yra išlaidų klasifikavimas kaip fiksuotų arba kintamų.
author: twheeloc
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 653bfb69c4ca118c700755cb95a6b349d2c6bbad
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735148"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a>Kurti ir priskirti savikainos veikimo būdo strategiją savikainos kontrolės įtaisui

[!include [banner](../../includes/banner.md)]

Išlaidų taisyklė yra išlaidų klasifikavimas kaip fiksuotų arba kintamų. Kainos kontrolės įtaisui turi būti priskirta strategija ir atitinkamos taisyklės, kad strategija pasidarytų veiksminga. Naudokite šią procedūrą norėdami sukurti strategiją, ir tada priskirkite strategiją išlaidų kontrolės įtaisui.


## <a name="create-a-cost-behavior-hierarchy"></a>Sukurkite išlaidų taisyklių hierarchiją
1. Eikite **į kaštų > dimensijų > hierarchijas**.
2. Spustelėkite **Naujas**.
3. Spustelėkite **Kurti**.
4. Lauke Dimensijų **hierarchijos pavadinimas** įveskite Išlaidų veikimo būdas hierarchija.
5. **Lauke Dimensija** įveskite arba pasirinkite vertę.
    * Pasirinkite Savikainos elementai.  
6. Spustelėkite **Įrašyti**.
7. Spustelėkite Peržiūrėti **hierarchiją**.
8. Spustelėkite **Naujas**.
9. Mazgo **pavadinimo** lauke įveskite vertę.
    * Įveskite Fiksuotą savikainą.  
10. Medyje pasirinkite „Išlaidų taisyklės hierarchija“.
11. Spustelėkite **Naujas**.
12. Mazgo **pavadinimo** lauke įveskite vertę.
    * Įveskite Kintamą savikainą.  
13. Spustelėkite **Įrašyti**.
14. Medyje pasirinkite „Cost behavior hierarchy\Fixed cost“.
15. Spustelėkite **Naujas**.
16. Sąraše pažymėkite pasirinktą eilutę.
17. Dimensijos nario **lauke** Iš įveskite arba pasirinkite vertę.
    * Dimensijų narių diapazone gali būti tarpų, tačiau nariai negali persidengti.  
18. Lauke Į **dimensijos** narį įveskite arba pasirinkite vertę.
    * Dimensijų narių diapazone gali būti tarpų, tačiau nariai negali persidengti.  
19. Medyje pasirinkite „Cost behavior hierarchy\Variable cost“.
20. Spustelėkite **Naujas**.
21. Sąraše pažymėkite pasirinktą eilutę.
22. Dimensijos nario **lauke** Iš įveskite arba pasirinkite vertę.
    * Dimensijų narių diapazone gali būti tarpų, tačiau nariai negali persidengti.  
23. Lauke Į **dimensijos** narį įveskite arba pasirinkite vertę.
    * Dimensijų narių diapazone gali būti tarpų, tačiau nariai negali persidengti.  
24. Spustelėkite **Įrašyti**.

## <a name="create-the-policy-and-rules"></a>Sukurkite strategiją ir taisykles
1. Eikite į **kaštų apskaitos > strategijos > išlaidų elgsenos strategijas**.
2. Spustelėkite **Naujas**.
3. **Lauke Strategijos pavadinimas** įveskite vertę.
4. Lauke Išlaidų **elemento dimensijų hierarchija** įveskite arba pasirinkite vertę.
    * Pasirinkite savo ką tik sukurtą strategijos hierarchiją.  
5. Lauke Išlaidų **objekto dimensijų hierarchija** įveskite arba pasirinkite vertę.
    * Pasirinkti organizaciją  
6. Spustelėkite **Įrašyti**.
7. Spustelėkite **Naujas**.
8. Sąraše pažymėkite pasirinktą eilutę.
9. Lauke Išlaidų **elemento dimensijų hierarchijos** mazgas įveskite arba pasirinkite vertę.
    * Išplėskite hierarchiją, kad pasirinktumėte Kintamą savikainą.  
10. Lauke Išlaidų **objekto dimensijų hierarchijos** mazgas įveskite arba pasirinkite vertę.
    * Numatytai kintamas procentas yra 100 procentų.  
11. Spustelėkite **išlaidų kontrolės vieneto strategijos priskyrimus**.
12. Spustelėkite **Naujas**.
13. Sąraše pažymėkite pasirinktą eilutę.
14. Lauke Galioja **nuo apskaitos** datos įveskite datą.
    * Taisyklės taikomos pagal datą, ir vartotojas arba sistema gali baigti taisyklės galiojimą, jei sukurta naujesnė versija.  
15. Lauke Išlaidų **valdymo vienetas** įveskite arba pasirinkite vertę.
16. Spustelėkite **Įrašyti**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
