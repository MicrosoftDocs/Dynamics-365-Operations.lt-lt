---
title: Nustatyti PVM skirtas DK registravimo grupes
description: PVM yra skaičiuojamas ir registruojamas į pagrindines sąskaitas, kurios yra nurodytos DK registravimo grupėse.
author: twheeloc
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6cc96cbdb11f24d727bddfa5fd4aaa579537802a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968459"
---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a>Nustatyti PVM skirtas DK registravimo grupes

[!include [banner](../../includes/banner.md)]

PVM yra skaičiuojamas ir registruojamas į pagrindines sąskaitas, kurios yra nurodytos DK registravimo grupėse. DK registravimo grupės pridedamos prie kiekvieno PVM kodo. Galite nustatyti individualias DK registravimo grupes kiekvienam PVM kodui, naudoti vieną DK registravimo grupę visiems PVM kodams arba PVM kodams priskirti kelias DK registravimo grupes. Šiame įraše naudojama demonstracinė įmonė DEMF. 

1. Eikite į **Naršymo sritis > Moduliai > Mokestis > Sąranka > PVM > DK registravimo grupės**.
2. Spustelėkite **Naujas**.
3. Lauke **DK registravimo grupė** įveskite reikšmę.
4. Lauke **Aprašo laukas** surinkite reikšmę.
5. Lauke **Mokėtinas PVM** pasirinkite pagrindinę mokesčių institucijai mokamo PVM sąskaitą. Kai parduodate apmokestintas prekes ir paslaugas, mokesčių institucija renka PVM.  
6. Lauke **Gaunamas PVM** pasirinkite pagrindinę iš mokesčių institucijos gaunamų mokesčių sąskaitą. Kai apmokestintas prekes ir paslaugas perkate, mokesčių institucijos vardu PVM renka tiekėjai. Šis laukas nepasiekiamas, jei puslapyje **Didžiosios knygos parametrai** pažymėta parinktis Taikyti PVM apmokestinimo taisykles. Tuomet tiekėjui mokami PVM yra debetuojami į tą pačią sąskaitą kaip ir pirkimas.   
7. Lauke **Naudojimo mokesčio išlaidos** pasirinkite pagrindinę sąskaitą, skirtą atskaitomiems naudojimo mokesčiams, kurie nesusigrąžinami ar apie kuriuos tiekėjai neteikia ataskaitų mokesčių institucijai pagal ES atvirkštinio apmokestinimo GST / HST. **PVM grupėje**, kuri naudojama operacijai, turi būti pažymėta **PVM kodas** parinktis **Naudojimo mokestis**. Šis laukas nepasiekiamas, jei puslapyje **Didžiosios knygos parametrai** pažymėta parinktis **Taikyti PVM apmokestinimo taisykles**.   
8. Lauke **Mokėtinas naudojimo mokestis** pasirinkite pagrindinę sąskaitą, kurioje bus registruojami gaunami naudojimo mokesčiai, mokėtini mokesčių institucijoms. Norint registruoti **naudojimo mokestį** **PVM grupėje** turi būti pažymėta **PVM kodas** parinktis **Naudojimo mokestis**. Jei puslapyje **Didžiosios knygos parametrai** pasirinkta parinktis **Taikyti PVM apmokestinimo taisykles**, korespondentinė sąskaita skelbiama operacijos išlaidų paskyroje.   
9. Lauke **Sudengimo sąskaita** pasirinkite pagrindinę sąskaitą, kurioje bus registruojamas laukuose **Mokėtinas naudojimo mokestis** ir **Gaunamas PVM** nurodytų DK sąskaitų grynasis balansas. Balansas bus sudarytas įvykdžius PVM sudengimo ir registravimo užduotį.  Jei sudengimo laikotarpio mokesčių institucija yra susieta su tiekėjo sąskaita, balansas bus registruojamas tiekėjo sąskaitoje.
10. Lauke **Tiekėjo mokėjimo nuolaida** pasirinkite pagrindinę sąskaitą, kurioje bus registruojama mokėjimo nuolaida pagal PVM kodus, susietus su šia DK registravimo grupe. Tai neprivaloma – jei neįvedama jokia sąskaita, bus naudojama srityje **Mokėjimo nuolaidų kodai** nurodyta pagrindinė sąskaita. Gali būti naudinga kiekvienai **DK registravimo grupei** naudoti skirtingas sąskaitas, jei PVM grupėse naudojama PVM atšaukimo mokėjimo nuolaidai parinktis.  
11. Lauke **Kliento atvejo nuolaida** pasirinkite pagrindinę sąskaitą, kurioje bus registruojama mokėjimo nuolaida pagal **PVM kodus**, susietus su šia **DK registravimo grupe**. Tai neprivaloma – jei neįvedama jokia sąskaita, bus naudojama srityje **Mokėjimo nuolaidų kodai** nurodyta pagrindinė sąskaita. Gali būti naudinga kiekvienai **DK registravimo grupei** naudoti skirtingas sąskaitas, jei **PVM grupėse** naudojama PVM atšaukimo mokėjimo nuolaidai parinktis.  
12. Spustelėkite **Įrašyti**.

