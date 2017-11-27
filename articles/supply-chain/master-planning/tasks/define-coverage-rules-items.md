--- 
title: "Apibrėžti prekių padengimo taisykles"
description: "Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF."
author: YuyuScheller
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 76334f7ee4efe33df4a86aaa11a59748387cec89
ms.openlocfilehash: fe92393cc264df68f084db6974f7d4607d37d3ab
ms.contentlocale: lt-lt
ms.lasthandoff: 11/02/2017

---
# <a name="define-coverage-rules-for-items"></a>Apibrėžti prekių padengimo taisykles

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Šioje procedūroje nurodoma, kaip kurti padengimo taisykles ir nepaisyti konkrečios prekės padengimo parametrų. Jis taip pat parodo, kaip nurodyti numatytąsias atsargų nuostatas.


## <a name="create-a-coverage-group"></a>Padengimo grupės kūrimas
1. Eikite į Padengimo grupės.
2. Spustelėkite Naujas.
3. Lauke Padengimo grupė įveskite vertę.
4. Lauke Pavadinimas surinkite reikšmę.
5. Lauke Kalendorius įveskite vertę.
    * Pasirinkite kalendorių, kurį bendrasis planavimas naudos norėdamas sukurti šios grupės prekių papildymo pasiūlymus.  
6. Lauke Padengimo kodas pasirinkite parinktį.
    * Pasirinkite Reikalavimai šiai procedūrai.  
7. Lauke Padengimo laiko ribos (dienomis) įveskite „90‟.
    * Prekėms šioje grupėje bendrasis planavimas iki 90 dienų ateityje kurs papildymo pasiūlymus.  
8. Lauke Neigiamos dienos įveskite „1‟.
9. Lauke Teigiamos dienos įveskite „1‟.
10. Išplėskite arba sutraukite sekciją Kita.
11. Lauke Gavimo laiko rezervas, pridėtas prie pareikalavimo datos įveskite „1‟.
    * Pavyzdžiui, jei nustatytas 1 dienos gavimo laiko rezervas, o pirkimo užsakymo eilutę planuojama gauti gegužės 15 d., bendrajame planavime gavimo data bus pakoreguota į gegužės 16 d.  
12. Lauke Išdavimo laiko rezervas, atimtas iš pareikalavimo datos įveskite „1‟.
    * Pavyzdžiui, jei nustatytas 1 dienos laiko rezervas, o pardavimo užsakymo eilutę planuojama pristatyti gegužės 15 d., bendrajame planavime pristatymo data bus pakoreguota į gegužės 14 d.  
13. Lauke Keisti maržos, įtrauktos į prekės gamybos laiką, tvarką įveskite „1‟.
14. Spustelėkite Įrašyti.

## <a name="create-a-new-product"></a>Kurti naują produktą
1. Eikite į Išleisti produktai.
2. Spustelėkite Naujas.
3. Lauke „Produkto numeris“ įveskite reikšmę.
4. Lauke Produkto pavadinimas įveskite reikšmę.
5. Lauke Prekių modelių grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
6. Sąraše raskite ir pasirinkite norimą įrašą.
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.
8. Lauke Prekių grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
9. Sąraše raskite ir pasirinkite norimą įrašą.
10. Sąraše spustelėkite saitą pasirinktoje eilutėje.
11. Lauke Saugojimo dimensijų grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
12. Sąraše raskite ir pasirinkite norimą įrašą.
13. Sąraše spustelėkite saitą pasirinktoje eilutėje.
14. Lauke Sekimo dimensijų grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
15. Sąraše raskite ir pasirinkite norimą įrašą.
16. Sąraše spustelėkite saitą pasirinktoje eilutėje.
17. Spustelėkite GERAI.

## <a name="setup-default-order-settings"></a>Nustatyti numatytąsias užsakymo nuostatas
1. Veiksmų srityje spustelėkite Planuoti.
2. Spustelėkite Numatytosios užsakymo nuostatos.
3. Lauke Pirkimo teritorija įveskite teritoriją, kuri naudojama kaip numatytoji, kai kuriami pirkimo užsakymai.
4. Lauke Atsargų vieta įveskite vietą, kurioje saugoma prekė.
5. Išplėskite arba sutraukite sekciją Atsargos.
6. Kartotinį nustatykite į „10‟.
7. Min. užsakymų kiekį nustatykite į „10‟.
8. Maks. užsakymų kiekį nustatykite į „100‟.
9. Standartinį užsakymų kiekį nustatykite į „10‟.
10. Lauke Pirkimo vykdymo laikas įveskite skaičių.
11. Pažymėkite arba išvalykite žymės langelį Darbo dienos.
12. Spustelėkite Įrašyti.
13. Lauke Numatytasis užsakymo tipas pasirinkite „Pirkimo užsakymas“.
14. Spustelėkite Įrašyti.
15. Uždarykite puslapį.
    * Uždarykite puslapį Numatytieji užsakymo parametrai.  

## <a name="add-an-item-to-a-coverage-group"></a>Pridėti prekę į padengimo grupę
1. Išplėskite arba sutraukite sekciją Planas.
2. Lauke Padengimo grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
3. Sąraše raskite padengimo grupę, kurią sukūrėte.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.

## <a name="create-item-coverage-rules"></a>Kurti prekių padengimo taisykles
1. Veiksmų srityje spustelėkite Planuoti.
2. Spustelėkite Prekės padengimas.
3. Spustelėkite Naujas.
4. Spustelėkite skirtuką Bendra.
5. Pažymėkite funkcijos Nepaisyti padengimo grupės parametrų antraštės langelį.
6. Lauke Padengimo laiko ribos (dienomis) įveskite „60‟.
    * Nors prekės padengimo grupėje Poreikis yra planuojamos 90 dienų į priekį, ši prekė bus planuojama 60 dienų į priekį.  
7. Lauke Neigiamos dienos įveskite „2‟.
8. Lauke Teigiamos dienos įveskite „2‟.
9. Spustelėkite skirtuką Gamybos laikas.
10. Pažymėkite antraštės Pirkimas langelį.
11. Lauke Pirkimo laikas įveskite „5‟.
12. Spustelėkite Įrašyti.


