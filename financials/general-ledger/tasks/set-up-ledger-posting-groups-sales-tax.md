--- 
title: "PVM skirtų DK registravimo grupių nustatymas"
description: "PVM yra skaičiuojamas ir registruojamas į pagrindines sąskaitas, kurios yra nurodytos DK registravimo grupėse."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: e0682afed4664e1491ed46e4e40f467015701711
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a>PVM skirtų DK registravimo grupių nustatymas

[!include[task guide banner](../../includes/task-guide-banner.md)]

PVM yra skaičiuojamas ir registruojamas į pagrindines sąskaitas, kurios yra nurodytos DK registravimo grupėse. DK registravimo grupės pridedamos prie kiekvieno PVM kodo. Galite nustatyti individualias DK registravimo grupes kiekvienam PVM kodui, naudoti vieną DK registravimo grupę visiems PVM kodams arba PVM kodams priskirti kelias DK registravimo grupes. Šiame įraše naudojama demonstracinė įmonė DEMF. 

1. Pasirinkite Mokestis > Sąranka > PVM > DK registravimo grupės.
2. Spustelėkite Naujas.
3. Lauke DK registravimo grupė surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Lauke Mokėtinas PVM pasirinkite siunčiamo PVM, kurį reikia mokėti mokesčių institucijai, pagrindinę sąskaitą.
    * Kai parduodate apmokestintas prekes ir paslaugas, mokesčių institucija renka PVM.  
6. Lauke Gautinas PVM pasirinkite iš mokesčių institucijos gaunamų mokesčių pagrindinę sąskaitą.
    * Kai apmokestintas prekes ir paslaugas perkate, mokesčių institucijos vardu PVM renka tiekėjai. Šis laukas pasiekiamas tik puslapyje DK parametrai pasirinkus parinktį Taikyti PVM apmokestinimo taisykles. Tuomet tiekėjui mokami PVM yra debetuojami į tą pačią sąskaitą kaip ir pirkimas.   
7. Lauke Naudojimo mokesčio išlaidos pasirinkite pagrindinę sąskaitą, į kurią registruoti atskaitomus naudojimo mokesčius, kurių, kaip ES atvirkštinio mokesčio GST/HST, tiekėjai nepareikalavo ir apie kuriuos nepranešė mokesčių institucijai.
    * Prie PVM kodo, esančio PVM grupėje ir naudojamo operacijoje, reikia pasirinkti parinktį Naudojimo mokestis.  Šis laukas pasiekiamas tik puslapyje DK parametrai pasirinkus parinktį Taikyti PVM apmokestinimo taisykles.   
8. Lauke Mokėtinas naudojimo mokestis pasirinkite pagrindinę sąskaitą, į kurią registruoti gaunamus naudojimo mokesčius, kuriuos reikia mokėti mokesčių institucijoms.
    * Norint registruoti naudojimo mokestį, prie PVM kodo, esančio PVM grupėje, reikia pasirinkti parinktį Naudojimo mokestis. Jei DK parametruose pasirinkta parinktis Taikyti PVM apmokestinimo taisykles, korespondentinė sąskaita registruojama operacijos išlaidų sąskaitoje.   
9. Lauke Sudengimo sąskaita pasirinkite pagrindinę sąskaitą, kurioje bus registruojamas DK sąskaitų grynasis balansas, nurodytas laukuose Mokėtinas naudojimo mokestis ir Gautinas PVM.
    * Balansas bus sukurtas, kai bus vykdoma PVM sudengimo ir registravimo užduotis.  Jei sudengimo laikotarpio mokesčių institucija yra susieta su tiekėjo sąskaita, tada balansas registruojamas į tiekėjo sąskaitą.   
10. Lauke Tiekėjo mokėjimo nuolaida pasirinkite pagrindinę sąskaitą, kurioje registruoti PVM kodų, susietų su šia DK registravimo grupe, mokėjimo nuolaidą.
    * Tai nėra privaloma, ir, jei neįvedama jokia sąskaita, bus naudojama pagrindinė mokėjimo nuolaidos sąskaita. Jei PVM grupėms naudojama mokėjimo nuolaidos PVM atšaukimo parinktis, gali būti naudinga kiekvienai DK registravimo grupei naudoti skirtingas sąskaitas.  
11. Lauke Kliento atvejo nuolaida pasirinkite pagrindinę sąskaitą, kurioje registruoti PVM kodų, susietų su šia DK registravimo grupe, mokėjimo nuolaidą.
    * Tai nėra privaloma, ir, jei neįvedama jokia sąskaita, bus naudojama pagrindinė mokėjimo nuolaidos sąskaita. Jei PVM grupėms naudojama mokėjimo nuolaidos PVM atšaukimo parinktis, gali būti naudinga kiekvienai DK registravimo grupei naudoti skirtingas sąskaitas.  
12. Spustelėkite Įrašyti.


