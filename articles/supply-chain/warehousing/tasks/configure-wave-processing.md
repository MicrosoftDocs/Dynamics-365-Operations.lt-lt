---
title: Bangos apdorojimo konfigūravimas
description: Šiame vadove aprašoma, kaip nustatyti kriterijus, pagal kuriuos nustatoma, koks darbas sugeneruojamas sandėliui apdorojus bangą ir ar bangos apdorojamos rankiniu būdu, ar automatiškai.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSParameters, ProdParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e22816b33739141fbcd188d631a07313db415959
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977293"
---
# <a name="configure-wave-processing"></a>Bangos apdorojimo konfigūravimas

[!include [banner](../../includes/banner.md)]

Šiame vadove aprašoma, kaip nustatyti kriterijus, pagal kuriuos nustatoma, koks darbas sugeneruojamas sandėliui apdorojus bangą ir ar bangos apdorojamos rankiniu būdu, ar automatiškai. Kriterijus galite nurodyti nustatydami bangos šablonus ir užklausas, kurios sugretina bangą su išleistais pardavimo užsakymais, gamybos užsakymais arba „kanban“ užsakymais. Bangos apdorojimas naudojamas tuose sandėliuose, kurie šią funkciją naudoja modulyje Sandėlio valdymas, o tuose, kurie šią funkciją naudoja modulyje Atsargų valdymas, jis nenaudojamas. Šią procedūrą galite vykdyti demonstracinių duomenų įmonėje USMF.

1. Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Konfigūracija > Bangos > Bangos šablonai**.
2. Spustelėkite **Naujas**.
3. Lauke **Bangos šablono pavadinimas** įveskite reikšmę. Kai nustatote bangos šabloną, nurodote seką, kuria šablonai bus gretinami su išleistomis pardavimo užsakymų, gamybos užsakymų ar „kanban‟ eilutėmis. Kai eilutė išleidžiama į sandėlį ar į gamybą, ji naudoja pirmąjį bangos šabloną, kurio kriterijus atitinka. Rekomenduojame padėti šablonus su specifiškiausiais kriterijais sąrašo viršuje. Kuo platesni kriterijai, tuo didesnė tikimybė, kad eilutė atitiks kriterijus, todėl eilutės gali būti priskirtos netinkamai bangai.  
4. Lauke **Bangos šablono aprašas** įveskite reikšmę.
5. Lauke **Teritorija** įveskite arba pasirinkite reikšmę. Jeigu naudojate USMF, galite pasirinkti svetainę „2“.  
6. Lauke **Sandėlis** įveskite arba pasirinkite reikšmę. Jeigu naudojate USMF, galite pasirinkti sandėlį „24“.  
7. Lauką **Automatiškai kurti bangą** nustatykite į **Taip**. Pasirinkite šią parinktį, kad banga būtų automatiškai kuriama į sandėlį išleidus pardavimo užsakymą, gamybos užsakymą arba „kanban“.  
8. Parinktį **Apdoroti bangą išleidžiant ją į sandėlį** nustatykite į **Taip**. Pasirinkite šią parinktį, kad būtų automatiškai apdorojama banga ir sukuriamas darbas į sandėlį išleidus eilutę.  
9. Nustatykite **Parinktis automatizuoti bangos išleidimą** į **Taip**. Pasirinkus šią parinktį bus automatiškai išleidžiama banga. Paėmimo darbas sukuriamas ir prieinamas mobiliuosiuose įrenginiuose.  
10. Nustatykite **Parinktis priskirti atidaryti bangas** į **Taip**. Eilutės priskiriamos bangoms pagal bangos šablono užklausos filtrą.  
11. Nustatykite **Parinktis apdoroti bangą automatiškai ties ribine reikšme** į **Taip**. Pasirinkite šią parinktį, kad banga būtų automatiškai apdorojama jos vertėms pasiekus svorio, siuntos ir laukų grupėje Bangos slenksčiai nurodytų eilučių slenksčius. Šią parinktį galima naudoti tik lauke Bangos šablono tipas pasirinkus Siunta.  
12. Nustatykite **Parinktis automatiškai leisti papildymo darbą** į **Taip**. Pasirinkus šią parinktį bus automatiškai sukuriamas ir išleidžiamas papildymo darbas pagal poreikį. Turite įtraukti papildymo bangos metodą į bangos šabloną ir sukurti tipo Bangos poreikis papildymo šabloną.  
13. Išplėskite dalį **Metodai**.

    - Bangos šablonų būdais galima valdyti veiklų, per kurias praeina kiekviena apdorojama banga, seką. Pavyzdžiui, galite turėti bangų papildymo būdą. Kai pridedate metodą, jis automatiškai pateikiamas atitinkamoje vietoje pagal sekos veiksmus. Jei parinktį Automatiškai leisti papildymo darbą nustatėte į Taip, čia turite įtraukti papildymo būdą.  
    - Bangų atributai veikia kaip filtrai – jie riboja, kokios prekės gali naudoti bangą. Pavyzdžiui, galite nurodyti prekių grupę.  
14. Spustelėkite **Įrašyti**.
15. Uždarykite puslapį.
16. Pasirinkite **Sandėlio valdymas > Sąranka > Sandėlio valdymo parametrai**.
17. Išplėskite dalį **Bangos apdorojimas**.
18. Lauke **Bangos apdorojimo paketų grupė** įveskite arba pasirinkite reikšmę.
19. Nustatykite **Parinktis apdoroti bangas kaip paketinę užduotį** į **Taip**.
20. Lauke **Laukti užrakto (ms)** įveskite skaičių. Įveskite laiką (milisekundėmis), kurį paskirstymo veiksmas lauks sistemos ištekliaus, kuris užrakintas kito paskirstymo veiksmo. Viršijus laiką, banga neapdorojama ir rodomas klaidos pranešimas.  
21. Spustelėkite **Įrašyti**.
22. Uždarykite puslapį.
23. Eikite į **Naršymo sritis > Moduliai > Gamybos kontrolė > Sąranka > Gamybos kontrolės parametrai**.
24. Lauke **Išleisti į sandėlį** pasirinkite parinktį.

Pardavimo užsakymų ir „kanban“ užsakymų atsargos turi būti rezervuotos prie išleidžiant užsakymą į sandėlį. Kitu atveju prekės arba paskirstymo eilutės negalės būti apdorojamos bangoje. Gamybos užsakymuose taip pat galite pasirinkti Leisti dalinį rezervavimą. Pvz., tai naudinga, jei turite medžiagų, kurių reikia, kad galėtumėte pradėti gamybą, ir galite palaukti, kol taps pasiekiamos papildomos medžiagos procesui baigti. Jei pasirinksite šią parinktį, turėsite rankiniu būdu kartoti išleidimo į sandėlį procesą, kai taps pasiekiama papildomų medžiagų.  
25. Uždarykite puslapį.

