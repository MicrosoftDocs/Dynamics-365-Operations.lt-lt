---
title: Pasikartojančio pirkimo užsakymo kūrimas
description: Šiame straipsnyje aprašoma, kaip sukurti pasikartojantį pirkimo užsakymą (PO) kopijuojant eilutes iš ankstesnio pirkimo užsakymo dokumento į naują PU arba esamą PU.
author: GalynaFedorova
ms.date: 09/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, PurchCopying
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 335461d60fa0bc92e9711806c6e42643a3f75d02
ms.sourcegitcommit: 073604c07116e0a87f78ab2c76cb89ae83ebba3c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2022
ms.locfileid: "9608117"
---
# <a name="create-a-repeat-purchase-order"></a>Pasikartojančio pirkimo užsakymo kūrimas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip sukurti pasikartojantį pirkimo užsakymą (PO) kopijuojant eilutes iš ankstesnio pirkimo užsakymo dokumento į naują PU arba esamą PU. Pasikartojančius užsakymus galima kurti dviem būdais. Galite naudoti dokumentų lygio veiksmus veiksmų srityje arba galite naudoti eilutės informacijos veiksmus. Dokumento lygio veiksmai skirti naujam pirkimo užsakymui sukurti, pridedant kito užsakymo eilutes ir antraštės informaciją, o eilutės informacijos veiksmas dažniausiai yra eilučių pridėjimas prie esamo užsakymo. Šiame vedlyje pateikiamą pavyzdį galima naudoti demonstracinių duomenų įmonėje USMF. Šią užduotį paprastai atlieka pirkimo agentas.

## <a name="create-a-new-repeat-purchase-order"></a>Kurti naują pasikartojantį pirkimo užsakymą

1. Naršymo srityje eikite į modulius **\> Įsigijimai ir pirkimo užsakymų \> sąrašas Visi \> pirkimo užsakymai**. Pirmiausia pabandysime informaciją nukopijuoti į naują užsakymą.  
1. Pasirinkite **Naujas**.
1. Lauke **„Tiekėjo paskyra“** įveskite „`US-101`“.
1. Pasirinkite **Gerai**.
1. Veiksmų srityje atidarykite skirtuką **Pirkimo užsakymas** ir kopijavimo grupėje **pasirinkite** Iš **visų**. Atidaromas **kitų dokumentų dialogo** langas Kopija. Iš čia galite kopijuoti iš esamų užsakymų į savo užsakymą. Eilutes galima kopijuoti keliais skirtingais būdais, be to, galima kopijuoti iš įvairių tipų dokumentų. Pirmiausia apžvelkime, kaip galima kopijuoti eilutes.
1. Išplėskite parametrų **"** FastTab".

    - Laukas **Kiekio veiksnys** yra naudingas, jei turite naudoti kiekį, kuris skiriasi nuo kiekio užsakyme, iš kurio kopijuojate. Pavyzdžiui, jei norite užsakyti du kartus didesnį kiekį, nei nurodytas eilutėse, iš kurių kopijuojate, šiame lauke įveskite 2, o tada sistema įtrauks eilutes, pradinį kiekį padaugindama du kartus.  
    - Laukas **Invertuoti ženklą** taip pat palaiko užsakyto kiekio keitimą keičiant užsakymo eilučių, kurios buvo įtrauktos, kiekio ženklą. Tai gali būti naudinga, jei norite atšaukti operaciją, kurdami užsakymo eilutes, kurios paneigia operaciją. Ši parinktis automatiškai pasirenkama, kai puslapis atidaromas iš veiksmo **Kurti kredito pastabą**.  
    - Parinktis **Kopijuoti mokesčius** leidžia kopijuoti mokesčius į naują užsakymą iš dokumento, iš kurio kopijuojate užsakymo eilutes.  
    - Parinktis **Perskaičiuoti kainas** naudoja esamas kainas ir nuolaidas, o ne kopijuoja jas iš dokumento, iš kurio kopijuojate kitą informaciją.  
    - Pasirinktis **Kopijuoti tiksliai** kopijuoja kelių užsakymo antraštės ir eilučių laukų vertes. Jei ši pasirinktis nėra pasirinkta, numatytosios vertės bus naudojamos daugelyje laukų, susijusių su tiekėju ir produktais, kaip ir kuriant naują užsakymą neautomatiniu būdu. Pavyzdžiui, jei **·** *Kopijuojate* tiksliai į Taip ir kopijuojate užsakymą, kuris nepaiso numatytosios tiekėjo SF sąskaitos, tada ta pati SF sąskaita bus kopijuojama į jūsų naują užsakymą. Jei kopijavimą **tiksliai nustatote** kaip *Ne*, numatytasis tiekėjo SF kodas bus naudojamas naujame užsakyme. Šių laukų vertės kopijuojamos, kai **tiksliai nustatytas** kopijavimas kaip *Taip*:
        - Kalba
        - Mokėjimo sąlygos
        - Mokėjimo būdas
        - Mokėjimo specifikacija
        - Numeracijų grupė
        - Mokėjimo nuolaida
        - Nuolaida procentais
        - Valiuta
        - Pristatymo sąlygos
        - Pristatymo būdas
        - Dimensija
        - PVM grupė
        - Perrašyti pardavimo mokestį
        - Kainos su PVM
        - Transportavimas
        - Uostas
        - Statistikos procedūra
        - Šablono ID
        - Adresatas
        - Pašto adresas
        - Nuoroda
        - Nuorodos lentelės ID
    - Parinktis **Naikinti pirkimo eilutes** panaikina visas pirkimo užsakymo eilutes, kurios jau yra pirkimo užsakyme, į kurį kopijuojate, prieš naudojant naujas eilutes. Naudokite šią parinktį atsargiai, nes ji be perspėjimo panaikina visas esamas eilutes.  
    - Jei naudojate parinktį **Kopijuoti užsakymo antraštę**, nereikia rankiniu būdu sukurti naujo užsakymo antraštės informacijos. Pasirinkus šią pasirinktį, laukuose, susijusiuose su tiekėju, bus naudojamos numatytosios vertės. Jei dokumente, iš kurio kopijuojate, įvestos ne numatytosios reikšmės, taip pat naudokite parinktį **Kopijuoti tiksliai**.
    - Galima kopijuoti iš skirtingų dokumentų šaltinių ir kiekvienam jų šiame puslapyje skirta atskira sekcija. Pavyzdžiui, skyriuje **Pirkimo užsakymai** galite kopijuoti iš esamų pirkimo užsakymų.  

1. Skyriuje **Pirkimo užsakymai** pažymėkite eilutes, kurias norite nukopijuoti į mainų sritį. Taip pat galima pasirinkti papildomas pirkimo užsakymų eilutes iš kitų pirkimo užsakymų ir nukopijuoti juos į užsakymą. Taip pat galima įtraukti eilutes iš kitų tipų pirkimo dokumentų. Toliau pateiktuose keliuose veiksmuose apžvelgiamos skirtingos parinktys.  
1. Išplėskite skyrių **Patvirtinimas**. Čia galite pasirinkti pirkimo užsakymų patvirtinimus, iš kurių norite kopijuoti. Pirkimo užsakymų patvirtinimai identifikuojami pagal susijusio pirkimo žurnalo ID arba pirkimo užsakymo ID.  
1. Išplėskite skyrių **Produktų kvitai**. Čia galite pasirinkti produktų gavimo kvitų žurnalus, iš kurių norite kopijuoti. Produktų gavimo kvitų žurnalai identifikuojami pagal produkto gavimo kvitą arba pirkimo užsakymo ID.
1. Išplėskite skyrių **Sąskaitos faktūros**. Čia galite pasirinkti tiekėjo SF, iš kurių norite kopijuoti. SF identifikuojamos pagal SF kvitą arba pirkimo užsakymo ID.
1. Išplėskite skyrių **Kopijuotinos pasirinktos eilutės arba antraštė**. Šiame rodinyje pateikiama visų dokumentų ir eilučių, kuriuos pasirinkote kopijuoti į užsakymą, suvestinė.
1. Pasirinkite **Gerai**. Pasirinktos eilutės buvo nukopijuotos į naują pirkimo užsakymą.

## <a name="copy-lines-to-an-existing-purchase-order"></a>Kopijuoti eilutes į esamą pirkimo užsakymą  

Užuot kopijavus visą užsakymą, dažniau yra kuriamas naujas PU ir įvedama PU antraštės informacija, o tada kopijuojamos atskiros eilutės iš esamų užsakymų.  

1. Pažymėkite eilutę **Pirkimo užsakymas**.
1. Pažymėkite **Iš visų**. Atidaromas puslapis yra toks pat, kaip anksčiau rodytas puslapis, bet atidarant jį iš užsakymo eilučių rodinio pasirenkamos kitos parinktys. Peržiūrėkime parametrus.
1. Išplėskite skyrių **Parametrai**.

    - Pasirinktis **Naikinti** pirkimo eilutes neparinkta. Tai reiškia, kad galite kopijuoti naujas eilutes į užsakymą nešalindami esamų eilučių.
    - Parinktis **Kopijuoti užsakymo antraštę** taip pat nepažymėta, nes mes į užsakymą įtraukiame tik papildomas eilutes.
    - Šiame pavyzdyje kopijuosime eilutes iš esamo pirkimo užsakymo.

1. Pasirinkite eilutę pageidaujamam pirkimo užsakymui. Atkreipkite dėmesį, kad taip pat pažymima viena užsakymo eilutę, esanti šiame PU.  
1. Pasirinkite **Gerai**. Papildoma užsakymo eilutė buvo įtraukta į pirkimo užsakymą.  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]