---
title: Kurti pasikartojantį pirkimo užsakymą
description: Šioje procedūroje parodoma, kaip kurti pasikartojantį pirkimo užsakymą (PU) kopijuojant eilutes iš ankstesnio pirkimo užsakymo dokumento į naują PU arba į esamą PO.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchCopying
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 74dcee8a614363cf1f1ebc71e3e39a14c59bb774
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "345886"
---
# <a name="create-a-repeat-purchase-order"></a>Kurti pasikartojantį pirkimo užsakymą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip kurti pasikartojantį pirkimo užsakymą (PU) kopijuojant eilutes iš ankstesnio pirkimo užsakymo dokumento į naują PU arba į esamą PO. Pasikartojančius užsakymus galima kurti dviem būdais. Galite naudoti dokumentų lygio veiksmus veiksmų srityje arba galite naudoti eilutės informacijos veiksmus. Dokumentų lygio veiksmai daugiausia naudojamas naujiems pirkimo užsakymams kurti, įtraukiant eilučių ir antraštės informaciją iš kito užsakymo, o eilutės informacijos veiksmas daugiausia naudojamas eilutėms į esamą užsakymą įtraukti. Šiame vedlyje pateikiamą pavyzdį galima naudoti demonstracinių duomenų įmonėje USMF. Šią užduotį paprastai atlieka pirkimo agentas.


## <a name="create-a-new-repeat-purchase-order"></a>Kurti naują pasikartojantį pirkimo užsakymą
1. Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Pirkimo užsakymai > Visi pirkimo užsakymai.
    * Pirmiausia pabandysime informaciją nukopijuoti į naują užsakymą.  
2. Spustelėkite Naujas.
3. Lauke Tiekėjo kodas įveskite US-101.
4. Spustelėkite GERAI.
5. Veiksmų srityje spustelėkite Pardavimo užsakymas.
6. Spustelėkite Iš visų.
    * Tai puslapis, kuriame galite informaciją iš esamų užsakymų kopijuoti į savo užsakymą. Eilutes galima kopijuoti keliais skirtingais būdais, be to, galima kopijuoti iš įvairių tipų dokumentų. Pirmiausia apžvelkime, kaip galima kopijuoti eilutes.   
7. Išplėskite skyrių Parametrai.
    * Laukas Kiekio koeficientas yra naudingas, jei norite naudoti kiekį, kitokį nei užsakymo, iš kurio kopijuojate, kiekis. Pavyzdžiui, jei norite užsakyti du kartus didesnį kiekį, nei nurodytas eilutėse, iš kurių kopijuojate, šiame lauke įveskite 2, o tada sistema įtrauks eilutes, pradinį kiekį padaugindama du kartus.  
    * Laukas Pakeisti ženklą taip pat palaiko galimybę pakeisti užsakytą kiekį pakeičiant įtraukiamų užsakymo eilučių kiekio ženklą. Tai gali būti naudinga, jei norite atšaukti operaciją, kurdami užsakymo eilutes, kurios paneigia operaciją. Atidarius puslapį naudojant veiksmą Kurti kredito pažymą, ši parinktis bus pasirinkta automatiškai.  
    * Parinktis Kopijuoti išlaidas suteikia galimybę kopijuoti išlaidas į naują užsakymą iš dokumento, iš kurio kopijuojate užsakymo eilutes.  
    * Parinktyje Perskaičiuoti kainas naudojamos dabartinės kainos ir nuolaidos, o ne nukopijuotos iš dokumento, iš kurio kopijuojate kitą informaciją.  
    * Parinktis Kopijuoti tiksliai sukuria tikslią reikšmių kopiją visuose užsakymo dokumento antraštės ir eilučių laukuose. Jei ši parinktis nepasirinkta, daugelyje su tiekėju ir produktais susijusių laukų naudojamos numatytosios reikšmės – lyg kurtumėte naują užsakymą neautomatiniu būdu. Pvz., jei užsakymas, iš kurio kopijuojate, perrašė numatytąją tiekėjo SF sąskaitą, ta pati SF sąskaita bus kopijuojama į jūsų užsakymą. Jei nepasirinkote parinkties Kopijuoti tiksliai, jūsų užsakyme būtų naudojama numatytoji tiekėjo SF sąskaita.  
    * Parinktis Naikinti pirkimo eilutes panaikina visas pirkimo užsakymo eilutes, jau esančias pirkimo užsakyme, iš kurio kopijuojate, prieš taikant naujas eilutes. Naudokite šią parinktį atsargiai, nes ji be perspėjimo panaikina visas esamas eilutes.  
    * Jei naudojate parinktį Kopijuoti užsakymo antraštę, naujame užsakyme nereikia neautomatiniu būdu kurti antraštės informacijos. Atkreipkite dėmesį, kad naudojant šią parinktį su tiekėju susijusiuose laukuose bus naudojamos numatytosios reikšmės. Jei dokumente, iš kurio kopijuojate, įvestos ne numatytosios reikšmės, kurias norite nukopijuoti, taip pat naudokite parinktį Kopijuoti tiksliai.  
8. Sutraukite sekciją Parametrai.
    * Galima kopijuoti iš skirtingų dokumentų šaltinių ir kiekvienam jų šiame puslapyje skirta atskira sekcija. Pvz., sekcijoje Pirkimo užsakymai galima kopijuoti iš esamų pirkimo užsakymų.  
9. Spustelėkite pirkimo užsakymo, kurio ID yra 00015, eilutę. 
10. Pažymėkite eilutę spustelėdami žymės langelį.
11. Išvalykite eilutės žymės langelį, kad ji nebūtų kopijuojama į užsakymą.
    * Dabar pasirinktos 4 eilutės, kurios bus nukopijuotos į pirkimo užsakymą. Taip pat galima pasirinkti papildomas pirkimo užsakymų eilutes iš kitų pirkimo užsakymų ir nukopijuoti juos į užsakymą. Taip pat galima įtraukti eilutes iš kitų tipų pirkimo dokumentų. Toliau pateiktuose keliuose veiksmuose apžvelgiamos skirtingos parinktys.  
12. Sutraukite sekciją Pirkimo užsakymai.
13. Išplėskite sekciją Patvirtinimas.
    * Čia galite pasirinkti pirkimo užsakymų patvirtinimus, iš kurių norite kopijuoti. Pirkimo užsakymų patvirtinimai identifikuojami pagal susijusio pirkimo žurnalo ID arba pirkimo užsakymo ID.  
14. Sutraukite sekciją Patvirtinimas.
15. Išplėskite sekciją Produktų gavimo kvitai.
    * Čia galite pasirinkti produktų gavimo kvitų žurnalus, iš kurių norite kopijuoti. Produktų gavimo kvitų žurnalai identifikuojami pagal produkto gavimo kvitą arba pirkimo užsakymo ID.   
16. Sutraukite sekciją Produktų gavimo kvitai.
17. Išplėskite sekciją SF.
    * Čia galite pasirinkti tiekėjo SF, iš kurių norite kopijuoti. SF identifikuojamos pagal SF kvitą arba pirkimo užsakymo ID.   
18. Sutraukite sekciją SF.
19. Išplėskite sekciją Pasirinktos eilutės arba antraštės, kurias reikia nukopijuoti.
    * Šiame rodinyje pateikiama visų dokumentų ir eilučių, kuriuos pasirinkote kopijuoti į užsakymą, suvestinė.   
20. Sutraukite sekciją Pasirinktos eilutės arba antraštės, kurias reikia nukopijuoti.
21. Spustelėkite GERAI.
    * Pasirinktos 4 eilutės buvo nukopijuotos į naują pirkimo užsakymą.   

## <a name="copy-lines-to-an-existing-purchase-order"></a>Kopijuoti eilutes į esamą pirkimo užsakymą
    * Užuot kopijavus visą užsakymą, dažniau yra kuriamas naujas PU ir įvedama PU antraštės informacija, o tada kopijuojamos atskiros eilutės iš esamų užsakymų.  
1. Spustelėkite Pirkimo užsakymo eilutė.
2. Spustelėkite Iš visų.
    * Atidaromas puslapis yra toks pat, kaip anksčiau rodytas puslapis, bet atidarant jį iš užsakymo eilučių rodinio pasirenkamos kitos parinktys. Peržiūrėkime parametrus.   
3. Išplėskite skyrių Parametrai.
    * Parinktis Naikinti pirkimo eilutes nepasirinkta. Tai reiškia, kad galite kopijuoti naujas eilutes į užsakymą nešalindami esamų eilučių.   
    * Parinktis Kopijuoti užsakymo antraštę taip pat nepažymėta, nes į užsakymą įtraukiame tik papildomas eilutes.   
4. Sutraukite sekciją Parametrai.
    * Šiame pavyzdyje kopijuosime eilutes iš esamo pirkimo užsakymo.   
5. Spustelėkite pirkimo užsakymo, kurio ID yra 00034, eilutę. 
6. Pažymėkite eilutę spustelėdami žymės langelį.
    * Atkreipkite dėmesį, kad taip pat pažymima viena užsakymo eilutę, esanti šiame PU.  
7. Spustelėkite GERAI.
    * Papildoma užsakymo eilutė buvo įtraukta į pirkimo užsakymą.  

