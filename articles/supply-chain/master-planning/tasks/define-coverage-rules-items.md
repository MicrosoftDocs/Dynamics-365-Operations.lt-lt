---
title: Apibrėžti prekių padengimo taisykles
description: Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11d92185bdbcf7aa1a668b6d2aa311805e42293c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3974985"
---
# <a name="define-coverage-rules-for-items"></a>Apibrėžti prekių padengimo taisykles

[!include [banner](../../includes/banner.md)]

Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Šioje procedūroje nurodoma, kaip kurti padengimo taisykles ir nepaisyti konkrečios prekės padengimo parametrų. Jis taip pat parodo, kaip nurodyti numatytąsias atsargų nuostatas.


## <a name="create-a-coverage-group"></a>Padengimo grupės kūrimas
1. Eikite į **„Naršymo sritis“ > „Moduliai“ > „Bendrasis planavimas“ > „Sąranka“ > „Padengimo grupės“**.
2. Spustelėkite **Naujas**.
3. Lauke **Padengimo grupės** įveskite vertę.
4. Lauke **Pavadinimas** įveskite reikšmę.
5. Lauke **Kalendorius** įveskite reikšmę. Pasirinkite kalendorių, kurį bendrasis planavimas naudos norėdamas sukurti šios grupės prekių papildymo pasiūlymus.  
6. Lauke **Padengimo kodas** pasirinkite parinktį. Pasirinkite Reikalavimai šiai procedūrai.  
7. Lauke **Padengimo laik oribos (dienomis)** įveskite 90. Prekėms šioje grupėje bendrasis planavimas iki 90 dienų ateityje kurs papildymo pasiūlymus.  
8. Lauke **Neigiamos dienos** įveskite „1‟.
9. Lauke **Teigiamos dienos** įveskite „1‟.
10. Išplėskite arba sutraukite sekciją **Kiti**.
11. Sekcijos **Laiko rezervas dienomis** lauke **Gavimo laiko rezervas, pridėtas prie pareikalavimo datos** įveskite 1. Pavyzdžiui, jei nustatytas 1 dienos gavimo laiko rezervas, o pirkimo užsakymo eilutę planuojama gauti gegužės 15 d., bendrajame planavime gavimo data bus pakoreguota į gegužės 16 d.  
12. Lauke **Išdavimo laiko rezervas, atimtas iš pareikalavimo datos** įveskite 1. Pavyzdžiui, jei nustatytas 1 dienos laiko rezervas, o pardavimo užsakymo eilutę planuojama pristatyti gegužės 15 d., bendrajame planavime pristatymo data bus pakoreguota į gegužės 14 d.  
13. Lauke **Keisti maržos, įtrauktos į prekės gamybos laiką, tvarką** įveskite 1.
14. Spustelėkite **Įrašyti**.

## <a name="create-a-new-product"></a>Naujo produkto kūrimas
1. Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Produktai > Patvirtinti produktai**.
2. Spustelėkite **Naujas**.
3. Lauke **Produkto numeris** įveskite reikšmę.
4. Lauke **Produkto gavimo kvitas** įveskite vertę.
5. Lauke **Prekių modelių grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
6. Sąraše raskite ir pasirinkite norimą įrašą.
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.
8. Lauke **Prekių grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
9. Sąraše raskite ir pasirinkite norimą įrašą.
10. Sąraše spustelėkite saitą pasirinktoje eilutėje.
11. Lauke **Saugojimo dimensijų grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
12. Sąraše raskite ir pasirinkite norimą įrašą.
13. Sąraše spustelėkite saitą pasirinktoje eilutėje.
14. Lauke **Sekimo dimensijų grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
15. Sąraše raskite ir pasirinkite norimą įrašą.
16. Sąraše spustelėkite saitą pasirinktoje eilutėje.
17. Spustelėkite **Gerai**.

## <a name="setup-default-order-settings"></a>Nustatyti numatytąsias užsakymo nuostatas
1. Parinktyje **Veiksmų sritis** spustelėkite **Planas**.
2. Dalyje **Užsakymo parametrai** spustelėkite **Numatytieji užsakymo parametrai**.
3. Po **Pirkimo užsakymas** lauku **Numatytoji teritorija** įveskite teritoriją, kuri naudojama kaip numatytoji, kai kuriami pirkimo užsakymai.
4. Lauke **Numatytasis sandėlis** įveskite vietą, kurioje saugoma prekė.
5. Išplėskite arba sutraukite sekciją **Atsargos**.
6. Lauke **Daugkartinis** įveskite „10“.
7. Lauke **„Minimalus užsakymo kiekis** įveskite „10“.
8. Lauke **„Maksimalus užsakymo kiekis** įveskite „100“.
9. Lauke **Standartinis užsakymo kiekis** įveskite „10“.
10. Lauke **Pirkimo vykdymo laikas** įveskite skaičių.
11. Pažymėkite arba išvalykite žymės langelį **Darbo dienos**.
12. Spustelėkite **Įrašyti**.
13. Lauke **Numatytojo užsakymo tipas** pasirinkite „Pirkimo užsakymas“.
14. Spustelėkite **Įrašyti**.
15. Uždarykite puslapį. Uždarykite puslapį Numatytieji užsakymo parametrai.  

## <a name="add-an-item-to-a-coverage-group"></a>Pridėti prekę į padengimo grupę
1. Išplėskite arba sutraukite sekciją **Planas**.
2. Lauke **Padengimo grupės** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
3. Sąraše raskite **Padengimo grupės**, kurią sukūrėte.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.

## <a name="create-item-coverage-rules"></a>Kurti prekių padengimo taisykles
1. Parinktyje **Veiksmų sritis** spustelėkite **Planas**.
2. Dalyje **Padengimas** spustelėkite **Prekės padengimas**.
3. Spustelėkite **Naujas**.
4. Spustelėkite skirtuką **Bendra**.
5. Pažymėkite **Nepaisyti padengimo grupės parametrų** antraštės langelį.
6. Lauke **Padengimo laiko ribos (dienomis)** įveskite 60. Nors prekės padengimo grupėje Poreikis yra planuojamos 90 dienų į priekį, ši prekė bus planuojama 60 dienų į priekį.  
7. Lauke **Neigiamos dienos** įveskite „2‟.
8. Lauke **Teigiamos dienos** įveskite „2‟.
9. Spustelėkite skirtuką **Gamybos laikas**.
10. Pažymėkite **Pirkti** antraštės langelį.
11. Lauke **Pirkimo laikas** įveskite 5.
12. Spustelėkite **Įrašyti**.

