--- 
title: "Bangos apdorojimo konfigūravimas"
description: "Šiame vadove aprašoma, kaip nustatyti kriterijus, pagal kuriuos nustatoma, koks darbas sugeneruojamas sandėliui apdorojus bangą ir ar bangos apdorojamos rankiniu būdu, ar automatiškai."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSParameters, ProdParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f7a6db585468c235e07c4a0117a83995ec93f4b0
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="configure-wave-processing"></a>Bangos apdorojimo konfigūravimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šiame vadove aprašoma, kaip nustatyti kriterijus, pagal kuriuos nustatoma, koks darbas sugeneruojamas sandėliui apdorojus bangą ir ar bangos apdorojamos rankiniu būdu, ar automatiškai. Kriterijus galite nurodyti nustatydami bangos šablonus ir užklausas, kurios sugretina bangą su išleistais pardavimo užsakymais, gamybos užsakymais arba „kanban“ užsakymais. Bangos apdorojimas naudojamas tuose sandėliuose, kurie šią funkciją naudoja modulyje Sandėlio valdymas, o tuose, kurie šią funkciją naudoja modulyje Atsargų valdymas, jis nenaudojamas. Šią procedūrą galite vykdyti demonstracinių duomenų įmonėje USMF.

1. Pasirinkite Sandėlio valdymas > Nustatymas > Bangos > Bangų šablonai.
2. Spustelėkite Naujas.
3. Lauke Bangos šablono pavadinimas įveskite reikšmę.
    * Kai nustatote bangos šabloną, nurodote seką, kuria šablonai bus gretinami su išleistomis pardavimo užsakymų, gamybos užsakymų ar „kanban‟ eilutėmis. Kai eilutė išleidžiama į sandėlį ar į gamybą, ji naudoja pirmąjį bangos šabloną, kurio kriterijus atitinka. Rekomenduojame padėti šablonus su specifiškiausiais kriterijais sąrašo viršuje. Kuo platesni kriterijai, tuo didesnė tikimybė, kad eilutė atitiks kriterijus, todėl eilutės gali būti priskirtos netinkamai bangai.  
4. Lauke Bangos šablono aprašas įveskite reikšmę.
5. Lauke Teritorija įveskite arba pasirinkite reikšmę.
    * Jei naudojate USMF, galite pasirinkti 2-ąją vietą.  
6. Lauke Sandėlis įveskite arba pasirinkite reikšmę.
    * Jei naudojate USMF, galite pasirinkti 24-ąjį sandėlį.  
7. Lauką Automatiškai kurti bangą nustatykite į Taip.
    * Pasirinkite šią parinktį, kad banga būtų automatiškai kuriama į sandėlį išleidus pardavimo užsakymą, gamybos užsakymą arba „kanban“.  
8. Parinktį Apdoroti bangą išleidžiant ją į sandėlį nustatykite į Taip. 
    * Pasirinkite šią parinktį, kad būtų automatiškai apdorojama banga ir sukuriamas darbas į sandėlį išleidus eilutę.  
9. Parinktį Automatizuoti bangos išleidimą nustatykite į Taip. 
    * Pasirinkus šią parinktį bus automatiškai išleidžiama banga. Paėmimo darbas sukuriamas ir prieinamas mobiliuosiuose įrenginiuose.  
10. Parinktį Priskirti atidaryti bangas nustatykite į Taip. 
    * Eilutės priskiriamos bangoms pagal bangos šablono užklausos filtrą.  
11. Parinktį Apdoroti bangą automatiškai ties ribine reikšme nustatykite į Taip. 
    * Pasirinkite šią parinktį, kad banga būtų automatiškai apdorojama jos vertėms pasiekus svorio, siuntos ir laukų grupėje Bangos slenksčiai nurodytų eilučių slenksčius. Šią parinktį galima naudoti tik lauke Bangos šablono tipas pasirinkus Siunta.  
12. Parinktį Automatiškai leisti papildymo darbą nustatykite į Taip. 
    * Pasirinkus šią parinktį bus automatiškai sukuriamas ir išleidžiamas papildymo darbas pagal poreikį. Turite įtraukti papildymo bangos metodą į bangos šabloną ir sukurti tipo Bangos poreikis papildymo šabloną.  
13. Išplėskite dalį Būdai.
    * Bangos šablonų būdais galima valdyti veiklų, per kurias praeina kiekviena apdorojama banga, seką. Pavyzdžiui, galite turėti bangų papildymo būdą. Kai pridedate metodą, jis automatiškai pateikiamas atitinkamoje vietoje pagal sekos veiksmus. Jei parinktį Automatiškai leisti papildymo darbą nustatėte į Taip, čia turite įtraukti papildymo būdą.  
    * Bangų atributai veikia kaip filtrai – jie riboja, kokios prekės gali naudoti bangą. Pavyzdžiui, galite nurodyti prekių grupę.  
14. Spustelėkite Įrašyti.
15. Uždarykite puslapį.
16. Pasirinkite Sandėlio valdymas > Nustatymas > Sandėlio valdymo parametrai.
17. Išplėskite dalį Bangos apdorojimas.
18. Lauke Bangos apdorojimo paketų grupė įveskite arba pasirinkite reikšmę.
19. Parinktį Apdoroti bangas kaip paketinę užduotį nustatykite į Taip.
20. Lauke Laukti užrakto (ms) įveskite skaičių.
    * Įveskite laiką (milisekundėmis), kurį paskirstymo veiksmas lauks sistemos ištekliaus, kuris užrakintas kito paskirstymo veiksmo. Viršijus laiką, banga neapdorojama ir rodomas klaidos pranešimas.  
21. Spustelėkite Įrašyti.
22. Uždarykite puslapį.
23. Pasirinkite Gamybos kontrolė > Nustatymas > Gamybos kontrolės parametrai.
24. Lauke Išleisti į sandėlį pasirinkite parinktį.
    * Pardavimo užsakymų ir „kanban“ užsakymų atsargos turi būti rezervuotos prie išleidžiant užsakymą į sandėlį. Kitu atveju prekės arba paskirstymo eilutės negalės būti apdorojamos bangoje. Gamybos užsakymuose taip pat galite pasirinkti Leisti dalinį rezervavimą. Pvz., tai naudinga, jei turite medžiagų, kurių reikia, kad galėtumėte pradėti gamybą, ir galite palaukti, kol taps pasiekiamos papildomos medžiagos procesui baigti. Jei pasirinksite šią parinktį, turėsite rankiniu būdu kartoti išleidimo į sandėlį procesą, kai taps pasiekiama papildomų medžiagų.  
25. Uždarykite puslapį.


