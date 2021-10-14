---
title: Bangos apdorojimo konfigūravimo pavyzdys
description: Šioje temoje pateikiamas pavyzdys, kaip nustatyti kriterijus, pagal kuriuos nusprendžiama, koks darbas sugeneruojamas sandėliui, kai apdorojama banga ir tai, ar bangos apdorojamos rankiniu būdu, ar automatiškai.
author: Mirzaab
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSParameters, ProdParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 39c3fecf9250ee89c22003d5dff4ea662c3042e3
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572990"
---
# <a name="configure-wave-processing-example"></a>Bangos apdorojimo konfigūravimo pavyzdys

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamas pavyzdys, kaip nustatyti kriterijus, pagal kuriuos nusprendžiama, koks darbas sugeneruojamas sandėliui, kai apdorojama banga ir tai, ar bangos apdorojamos rankiniu būdu, ar automatiškai. Kriterijus galite nurodyti nustatydami bangos šablonus ir užklausas, kurios sugretina bangą su išleistais pardavimo užsakymais, gamybos užsakymais arba „kanban“ užsakymais.

## <a name="enable-sample-data"></a>Duomenų pavyzdžių įgalinimas

Norėdami dirbti pagal šį scenarijų, naudojant čia nurodytus įrašų ir reikšmių pavyzdžius, turite naudoti sistemą, kurioje įdiegti standartiniai demonstraciniai duomenys. Prieš pradėdami turite pasirinkti juridinį subjektą **USMF**.

## <a name="example-scenario-configure-wave-processing"></a>Pavyzdinis scenarijus: bangos apdorojimo konfigūravimas

Šio pavyzdžio scenarijus pereina per daugelį įvairių parametrų, darančių įtaką bangų kūrimui, užpildymui, apdorojimui ir išleidimui.

1. Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Konfigūracija > Bangos > Bangos šablonai**.
1. Pasirinkite **Naujas**.
1. Lauke **Bangos šablono pavadinimas** įveskite reikšmę. Kai nustatote bangos šabloną, nurodote seką, kuria šablonai bus gretinami su išleistomis pardavimo užsakymų, gamybos užsakymų ar „kanban‟ eilutėmis. Kai eilutė išleidžiama į sandėlį ar į gamybą, ji naudoja pirmąjį bangos šabloną, kurio kriterijus atitinka. Rekomenduojame padėti šablonus su specifiškiausiais kriterijais sąrašo viršuje. Kuo platesni kriterijai, tuo didesnė tikimybė, kad eilutė atitiks kriterijus, todėl eilutės gali būti priskirtos netinkamai bangai.  
1. Lauke **Bangos šablono aprašas** įveskite reikšmę.
1. Lauke **Teritorija** įveskite arba pasirinkite reikšmę. Jeigu naudojate USMF, galite pasirinkti svetainę „2“.  
1. Lauke **Sandėlis** įveskite arba pasirinkite reikšmę. Jeigu naudojate USMF, galite pasirinkti sandėlį „24“.  
1. Lauką **Automatiškai kurti bangą** nustatykite į **Taip**. Pasirinkite šią parinktį, kad banga būtų automatiškai kuriama į sandėlį išleidus pardavimo užsakymą, gamybos užsakymą arba „kanban“.  
1. Parinktį **Apdoroti bangą išleidžiant ją į sandėlį** nustatykite į **Taip**. Pasirinkite šią parinktį, kad būtų automatiškai apdorojama banga ir sukuriamas darbas į sandėlį išleidus eilutę.  
1. Nustatykite **Parinktis automatizuoti bangos išleidimą** į **Taip**. Pasirinkus šią parinktį bus automatiškai išleidžiama banga. Paėmimo darbas sukuriamas ir prieinamas mobiliuosiuose įrenginiuose.  
1. Nustatykite **Parinktis priskirti atidaryti bangas** į **Taip**. Eilutės priskiriamos bangoms pagal bangos šablono užklausos filtrą.  
1. Nustatykite **Parinktis apdoroti bangą automatiškai ties ribine reikšme** į **Taip**. Pasirinkite šią parinktį, kad banga būtų automatiškai apdorojama jos vertėms pasiekus svorio, siuntos ir laukų grupėje **Bangos slenksčiai** nurodytų eilučių slenksčius. Ši parinktis yra galima tik, jeigu lauke **Bangos šablono tipas** yra pasirinkta **Siunta**.  
1. Nustatykite **Parinktis automatiškai leisti papildymo darbą** į **Taip**. Pasirinkus šią parinktį bus automatiškai sukuriamas ir išleidžiamas papildymo darbas pagal poreikį. Turite įtraukti papildymo bangos metodą į bangos šabloną ir sukurti papildymo šabloną, naudodami **Bangos poreikio** tipą.  
1. Bangos atributų priskyrimui naudokite išsaugotos grupės **Numatytosios reikšmės** parametrus. Bangų atributai veikia kaip filtrai – jie riboja, kokios prekės gali naudoti bangą. Pavyzdžiui, galite nurodyti prekių grupę.  
1. Išplėskite skyrių **Metodai** ir nustatykite bangos šablono atliekamus veiksmus. Bangos šablonų būdais galima valdyti veiklų, per kurias praeina kiekviena apdorojama banga, seką. Pavyzdžiui, galite turėti bangų papildymo būdą. Kai pridedate metodą, jis automatiškai pateikiamas atitinkamoje vietoje pagal sekos veiksmus. Jei parinktį **Automatiškai leisti papildymo darbą** nustatėte į **Taip**, čia turite įtraukti papildymo būdą.  
1. Pasirinkite **Įrašyti**.
1. Uždarykite puslapį.
1. Pasirinkite **Sandėlio valdymas > Sąranka > Sandėlio valdymo parametrai**.
1. Išplėskite dalį **Bangos apdorojimas**.
1. Lauke **Bangos apdorojimo paketų grupė** įveskite arba pasirinkite reikšmę.
1. Nustatykite **Parinktis apdoroti bangas kaip paketinę užduotį** į **Taip**.
1. Lauke **Laukti užrakto (ms)** įveskite skaičių. Įveskite laiką (milisekundėmis), kurį paskirstymo veiksmas lauks sistemos ištekliaus, kuris užrakintas kito paskirstymo veiksmo. Viršijus laiką, banga neapdorojama ir rodomas klaidos pranešimas.  
1. Pasirinkite **Įrašyti**.
1. Uždarykite puslapį.
1. Eikite į **Naršymo sritis > Moduliai > Gamybos kontrolė > Sąranka > Gamybos kontrolės parametrai**.
1. Lauke **Išleisti į sandėlį** pasirinkite parinktį.

    Pardavimo užsakymų ir „kanban“ užsakymų atsargos turi būti rezervuotos prie išleidžiant užsakymą į sandėlį. Kitu atveju prekės arba paskirstymo eilutės negalės būti apdorojamos bangoje. Gamybos užsakymuose taip pat galite pasirinkti **Leisti dalinį rezervavimą**. Pavyzdžiui, tai yra naudinga, jei turite medžiagų, reikalingų pradėti gamybai ir galite palaukti, kol papildomos medžiagos proceso užbaigimui taps pasiekiamos. Jei pasirinksite šią parinktį, turėsite rankiniu būdu kartoti išleidimo į sandėlį procesą, kai taps pasiekiama papildomų medžiagų.
1. Uždarykite puslapį.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Bangos kūrimas ir apdorojimas](../wave-processing.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
