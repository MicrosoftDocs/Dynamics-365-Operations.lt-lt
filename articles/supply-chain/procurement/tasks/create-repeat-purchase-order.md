---
title: Pasikartojančio pirkimo užsakymo kūrimas
description: Šioje temoje rodoma, kaip sukurti pakartotinį pirkimo užsakymą (PO) kopijuojant eilutes iš ankstesnio pirkimo užsakymo dokumento į naują PO arba esamą PO.
author: FrankDahl
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchCopying
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0abbce32e2fabe860077502875b92f93ea0ea95c
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867082"
---
# <a name="create-a-repeat-purchase-order"></a>Pasikartojančio pirkimo užsakymo kūrimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje temoje rodoma, kaip sukurti pakartotinį pirkimo užsakymą (PO) kopijuojant eilutes iš ankstesnio pirkimo užsakymo dokumento į naują PO arba esamą PO. Pasikartojančius užsakymus galima kurti dviem būdais. Galite naudoti dokumentų lygio veiksmus veiksmų srityje arba galite naudoti eilutės informacijos veiksmus. Dokumentų lygio veiksmai daugiausia naudojamas naujiems pirkimo užsakymams kurti, įtraukiant eilučių ir antraštės informaciją iš kito užsakymo, o eilutės informacijos veiksmas daugiausia naudojamas eilutėms į esamą užsakymą įtraukti. Šiame vedlyje pateikiamą pavyzdį galima naudoti demonstracinių duomenų įmonėje USMF. Šią užduotį paprastai atlieka pirkimo agentas.


## <a name="create-a-new-repeat-purchase-order"></a>Kurti naują pasikartojantį pirkimo užsakymą
1. Naršymo srityje eikite į **„Moduliai“ > „Įsigijimas ir šaltiniai“ > „Pirkimo užsakymai“ > „Visi pirkimo užsakymai“**. Pirmiausia pabandysime informaciją nukopijuoti į naują užsakymą.  
2. Pasirinkite **Naujas**.
3. Lauke **„Tiekėjo paskyra“** įveskite „`US-101`“.
4. Pasirinkite **Gerai**.
5. Veiksmų srityje pažymėkite **Pirkimo užsakymas**.
6. Pažymėkite **Iš visų**. Tai puslapis, kuriame galite informaciją iš esamų užsakymų kopijuoti į savo užsakymą. Eilutes galima kopijuoti keliais skirtingais būdais, be to, galima kopijuoti iš įvairių tipų dokumentų. Pirmiausia apžvelkime, kaip galima kopijuoti eilutes. 
7. Išplėskite skyrių **Parametrai**.

    - Laukas **Kiekio veiksnys** yra naudingas, jei turite naudoti kiekį, kuris skiriasi nuo kiekio užsakyme, iš kurio kopijuojate. Pavyzdžiui, jei norite užsakyti du kartus didesnį kiekį, nei nurodytas eilutėse, iš kurių kopijuojate, šiame lauke įveskite 2, o tada sistema įtrauks eilutes, pradinį kiekį padaugindama du kartus.  
    - Laukas **Invertuoti ženklą** taip pat palaiko užsakyto kiekio keitimą keičiant užsakymo eilučių, kurios buvo įtrauktos, kiekio ženklą. Tai gali būti naudinga, jei norite atšaukti operaciją, kurdami užsakymo eilutes, kurios paneigia operaciją. Ši parinktis automatiškai pasirenkama, kai puslapis atidaromas iš veiksmo **Kurti kredito pastabą**.  
    - Parinktis **Kopijuoti mokesčius** leidžia kopijuoti mokesčius į naują užsakymą iš dokumento, iš kurio kopijuojate užsakymo eilutes.  
    - Parinktis **Perskaičiuoti kainas** naudoja esamas kainas ir nuolaidas, o ne kopijuoja jas iš dokumento, iš kurio kopijuojate kitą informaciją.  
    - Parinktis **Kopijuoti tiksliai** sukuria tikslią verčių visuose užsakymo dokumento antraštės ir eilučių laukuose kopijas. Jei ši parinktis nepasirinkta, daugelyje su tiekėju ir produktais susijusių laukų naudojamos numatytosios reikšmės – lyg kurtumėte naują užsakymą neautomatiniu būdu. Pvz., jei užsakymas, iš kurio kopijuojate, perrašė numatytąją tiekėjo SF sąskaitą, ta pati SF sąskaita bus kopijuojama į jūsų užsakymą. Jei nepažymėsite parinkties **Kopijuoti tiksliai**, jūsų užsakymui bus naudojama numatytoji tiekėjui skirta sąskaitos faktūros sąskaita.  
    - Parinktis **Naikinti pirkimo eilutes** panaikina visas pirkimo užsakymo eilutes, kurios jau yra pirkimo užsakyme, į kurį kopijuojate, prieš naudojant naujas eilutes. Naudokite šią parinktį atsargiai, nes ji be perspėjimo panaikina visas esamas eilutes.  
    - Jei naudojate parinktį **Kopijuoti užsakymo antraštę**, nereikia rankiniu būdu sukurti naujo užsakymo antraštės informacijos. Atkreipkite dėmesį, kad naudojant šią parinktį su tiekėju susijusiuose laukuose bus naudojamos numatytosios reikšmės. Jei dokumente, iš kurio kopijuojate, įvestos ne numatytosios reikšmės, taip pat naudokite parinktį **Kopijuoti tiksliai**.   
    - Galima kopijuoti iš skirtingų dokumentų šaltinių ir kiekvienam jų šiame puslapyje skirta atskira sekcija. Pavyzdžiui, skyriuje **Pirkimo užsakymai** galite kopijuoti iš esamų pirkimo užsakymų.  

8. Skyriuje **Pirkimo užsakymai** pažymėkite eilutes, kurias norite nukopijuoti į mainų sritį. Taip pat galima pasirinkti papildomas pirkimo užsakymų eilutes iš kitų pirkimo užsakymų ir nukopijuoti juos į užsakymą. Taip pat galima įtraukti eilutes iš kitų tipų pirkimo dokumentų. Toliau pateiktuose keliuose veiksmuose apžvelgiamos skirtingos parinktys.  
9. Išplėskite skyrių **Patvirtinimas**. Čia galite pasirinkti pirkimo užsakymų patvirtinimus, iš kurių norite kopijuoti. Pirkimo užsakymų patvirtinimai identifikuojami pagal susijusio pirkimo žurnalo ID arba pirkimo užsakymo ID.  
10. Išplėskite skyrių **Produktų kvitai**. Čia galite pasirinkti produktų gavimo kvitų žurnalus, iš kurių norite kopijuoti. Produktų gavimo kvitų žurnalai identifikuojami pagal produkto gavimo kvitą arba pirkimo užsakymo ID.   
11. Išplėskite skyrių **Sąskaitos faktūros**. Čia galite pasirinkti tiekėjo SF, iš kurių norite kopijuoti. SF identifikuojamos pagal SF kvitą arba pirkimo užsakymo ID.   
12. Išplėskite skyrių **Kopijuotinos pasirinktos eilutės arba antraštė**. Šiame rodinyje pateikiama visų dokumentų ir eilučių, kuriuos pasirinkote kopijuoti į užsakymą, suvestinė.   
13. Pasirinkite **Gerai**. Pasirinktos eilutės buvo nukopijuotos į naują pirkimo užsakymą.   

## <a name="copy-lines-to-an-existing-purchase-order"></a>Kopijuoti eilutes į esamą pirkimo užsakymą  

Užuot kopijavus visą užsakymą, dažniau yra kuriamas naujas PU ir įvedama PU antraštės informacija, o tada kopijuojamos atskiros eilutės iš esamų užsakymų.  

1. Pažymėkite eilutę **Pirkimo užsakymas**.
2. Pažymėkite **Iš visų**. Atidaromas puslapis yra toks pat, kaip anksčiau rodytas puslapis, bet atidarant jį iš užsakymo eilučių rodinio pasirenkamos kitos parinktys. Peržiūrėkime parametrus.   
3. Išplėskite skyrių **Parametrai**.

    - Parinktis **Naikinti pirkimo eilutes** nepažymėta. Tai reiškia, kad galite kopijuoti naujas eilutes į užsakymą nešalindami esamų eilučių.   
    - Parinktis **Kopijuoti užsakymo antraštę** taip pat nepažymėta, nes mes į užsakymą įtraukiame tik papildomas eilutes.   
    - Šiame pavyzdyje kopijuosime eilutes iš esamo pirkimo užsakymo.   

4. Pasirinkite eilutę pageidaujamam pirkimo užsakymui. Atkreipkite dėmesį, kad taip pat pažymima viena užsakymo eilutę, esanti šiame PU.  
5. Pasirinkite **Gerai**. Papildoma užsakymo eilutė buvo įtraukta į pirkimo užsakymą.  

