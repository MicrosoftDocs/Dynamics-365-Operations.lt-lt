--- 
title: "Kurti pirkimo grąžinimo užsakymą"
description: "Šioje procedūroje parodoma, kaip kurti pirkimo grąžinimo užsakymą, naudojant veiksmą Kredito pažyma siekiant eilutes iš tiekėjo SF dokumento kopijuoti į naują pirkimo užsakymą."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b9124100f84afb13acc2ac9dda7b9483afb01754
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-return-order"></a>Kurti pirkimo grąžinimo užsakymą

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip kurti pirkimo grąžinimo užsakymą, naudojant veiksmą Kredito pažyma siekiant eilutes iš tiekėjo SF dokumento kopijuoti į naują pirkimo užsakymą. Joje taip pat parodoma, kaip patvirtinti užsakymą ir apdoroti prekių siuntą atgal tiekėjui. Šioje procedūroje pateikiamą pavyzdį galima naudoti demonstracinių duomenų įmonėje USMF. Šią užduotį paprastai atlieka pirkimo agentas.


## <a name="create-a-new-purchase-return-order"></a>Kurti naują pirkimo grąžinimo užsakymą
1. Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Pirkimo užsakymai > Visi pirkimo užsakymai.
    * Pirmuoju veiksmu sukuriamas naujas pirkimo užsakymas, kuris bus naudojamas kaip pirkimo grąžinimo užsakymas.  
2. Spustelėkite Naujas.
3. Lauke Tiekėjo kodas įveskite US-102.
4. Spustelėkite GERAI.
5. Veiksmų srityje spustelėkite Pirkti.
6. Spustelėkite Kredito pažyma.
    * Tai puslapis, kuriame galite informaciją iš esamos tiekėjo SF kopijuoti į savo grąžinimo užsakymą. Tai yra tas pats puslapis, kuris naudojamas kitiems kopijavimo veiksmams atlikti. Tačiau, kadangi mes jį atidarėme naudodami veiksmą Kredito pažyma, puslapis sukonfigūruotas palaikyti tiekėjo SF koresponduojančio grąžinimo užsakymo kūrimą.  
7. Išplėskite skyrių Parametrai.
    * Parinktis Pakeisti ženklą pažymima automatiškai ir jos keisti negalima. Taip užtikrinama, kad bus pakeistas kiekių ženklas įtrauktos užsakymo eilutės koresponduos tiekėjo SF.  
    * Parinktis Kopijuoti išlaidas pažymima automatiškai ir jos keisti negalima. Tai reiškia, kad tiekėjo SF išlaidos įtraukiamos į pirkimo grąžinimo užsakymą, kad būtų galima koresponduoti pradinį mokestį. Užsakymo antraštės ir eilučių keitimus galima modifikuoti vėliau.  
    * Parinktis Kopijuoti tiksliai pažymima automatiškai ir jos keisti negalima. Taip užtikrinama, kad bus sukurta tiksli visų tiekėjo SF antraštės ir eilučių laukų reikšmių kopija. Tai reiškia, kad pirkimo grąžinimo užsakymas sukuriamas naudojant reikšmes, kurios atitinka visas tiekėjo SF dokumento sąlygas.  
    * Parinktis Naikinti pirkimo eilutes panaikina visas pirkimo užsakymo eilutes, jau esančias pirkimo užsakyme, prieš įtraukiant naujas eilutes. Šiame pavyzdyje mes jokių eilučių dar neįtraukėme į pirkimo grąžinimo užsakymą, todėl jokio poveikio nebus. Naudokite šią parinktį atsargiai, nes ji be perspėjimo panaikina visas esamas eilutes.  
    * Parinktis Kopijuoti užsakymo antraštę pažymima automatiškai ir jos keisti negalima. Taip užtikrinama, kad informacija yra kopijuojama iš tiekėjo SF ir taikoma pirkimo grąžinimo užsakymo antraštėje. Tai naudinga, nes galima užtikrinti, kad pirkimo grąžinimo užsakymas koresponduos SF naudodamas panašias sąlygas.  
8. Sutraukite sekciją Parametrai.
9. Išplėskite sekciją SF.
    * Puslapis buvo atidarytas naudojant veiksmą Kredito pažyma, todėl informacijos kopijavimas iš tiekėjo SF yra vienintelė galima parinktis. Šiame skirtuke rodomos visos galimos tiekėjo kodo, nurodyto anksčiau sukurtame pirkimo grąžinimo užsakyme, SF.   SF identifikuojamos pagal SF kvitą arba pirkimo užsakymo ID.  
10. Raskite tiekėjo SF pagal SF numerį AP-0006 ir pažymėkite tą eilutės spustelėdami bet kurį jos lauką.
11. Pažymėkite eilutę spustelėdami eilutės žymės langelį. 
    * Atkreipkite dėmesį, kad tiekėjo SF eilutės automatiškai pažymimos kartu su užsakymu. Šioje konkrečioje tiekėjo SF yra 2 užsakymo eilutės. Šiame pavyzdyje mes grąžinsime dalį antrosios eilutės kiekio.  
12. Pažymėkite antrą eilutę (prekės M0006 eilutę) spustelėdami bet kurį jos lauką.
13. Lauke Kiekis pakeiskite kiekį į 10. Tai kiekis, kuris bus grąžintas tiekėjui. 
14. Pažymėkite pirmą eilutę (prekės M0005 eilutę) spustelėdami bet kurį jos lauką.
15. Panaikinkite eilutės žymės langelio žymėjimą.
    * Tik pasirinktos eilutės bus nukopijuotos į jūsų užsakymą.  
16. Sutraukite sekciją SF.
17. Išplėskite sekciją Pasirinktos eilutės arba antraštės, kurias reikia nukopijuoti.
    * Šiame rodinyje pateikiama visų dokumentų ir eilučių, kuriuos pasirinkote kopijuoti į užsakymą, suvestinė.  
18. Sutraukite sekciją Pasirinktos eilutės arba antraštės, kurias reikia nukopijuoti.
19. Spustelėkite GERAI.
    * Pasirinkta eilutė buvo nukopijuota į pirkimo grąžinimo užsakymą. Lauke Kiekis nurodyta – 10.   
20. Spustelėkite Atsargos.
21. Spustelėkite Žymėti.
    * Sukurta užsakymo eilutė pažymėta pagal tiekėjo SF atsargų operaciją. Taip užtikrinama, kad tiekėjui grąžinamos atsargos yra tokios pat kaip atsargos, kurios iš jų buvo gautos anksčiau. Būna atvejų, kai eilutės nėra žymimos, pvz., jei atsargos jau pažymėtos kaip Suvartotos arba jei pasirinkto tipo produktai nežymimi.  
22. Spustelėkite GERAI.

## <a name="confirm-and-record-the-shipment-of-goods"></a>Tvirtinti ir registruoti prekių siuntą
1. Spustelėkite Patvirtinti.
2. Veiksmų srityje spustelėkite Gauti.
3. Spustelėkite Produkto gavimo kvitas.
    * Šis puslapis naudojamas pirkimo užsakymų produktų gavimo kvitams įrašyti ir prekių grąžinimui tiekėjui apdoroti. Užsakymo eilutės su neigiamu kiekiu nurodo, kad prekes reikia grąžinti tiekėjui, o dokumentą, kurį galima generuoti šiame puslapyje, galima naudoti kaip važtaraštį.   
    * Šiame pavyzdyje lauke Kiekis pasirinkite Užsakytas kiekis.   Taip užtikrinama, kad bus apdorota viso užsakyto kiekio, kurį naudojant buvo sukurtos užsakymo eilutės, siunta.   
4. Lauke Produkto gavimo kvitas surinkite reikšmę.
    * Šiame lauke įvedama nuoroda, kuri naudojama kaip produktų gavimo žurnalo kvitas.  
5. Spustelėkite GERAI.
    * Dabar pirkimo grąžinimo užsakyme prekės užregistruotos kaip išsiųstos ir produktų gavimo kvitų žurnalas sukurtas. Galite naudoti veiksmą Produkto gavimo kvitas, norėdami peržiūrėti žurnalus, sukurtus su pirkimo užsakymu, ir sužinoti, kas ir kada buvo gauta arba grąžinta.  


