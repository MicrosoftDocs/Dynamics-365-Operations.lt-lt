---
title: Prekių padengimo taisyklių apibrėžimas
description: Šioje procedūroje nurodoma, kaip kurti padengimo taisykles ir nepaisyti konkrečios prekės padengimo parametrų. Jis taip pat parodo, kaip nurodyti numatytąsias atsargų nuostatas.
author: ChristianRytt
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3947c8a51facfb02012cc8e9a3ffd5887073bd9
ms.sourcegitcommit: 8c17717b800c2649af573851ab640368af299981
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/23/2021
ms.locfileid: "7860618"
---
# <a name="define-coverage-rules-for-items"></a>Prekių padengimo taisyklių apibrėžimas

[!include [banner](../../includes/banner.md)]

Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Šioje procedūroje nurodoma, kaip kurti padengimo taisykles ir nepaisyti konkrečios prekės padengimo parametrų. Jis taip pat parodo, kaip nurodyti numatytąsias atsargų nuostatas.

## <a name="create-a-coverage-group"></a>Padengimo grupės kūrimas

Sukurkite padengimo grupę, atlikdami šiuos veiksmus:

1. Eikite į **„Naršymo sritis“ > „Moduliai“ > „Bendrasis planavimas“ > „Sąranka“ > „Padengimo grupės“**.
1. Pasirinkite **Naujas**.
1. Lauke **Padengimo grupės** įveskite vertę.
1. Lauke **Pavadinimas** įveskite reikšmę.
1. Lauke **Kalendorius** įveskite reikšmę. Pasirinkite kalendorių, kurį bendrasis planavimas naudos norėdamas sukurti šios grupės prekių papildymo pasiūlymus.  
1. Lauke **Padengimo kodas** pasirinkite parinktį. Pasirinkite Reikalavimai šiai procedūrai.  
1. Lauke **Padengimo laiko ribos (dienomis)** įveskite 90. Prekėms šioje grupėje bendrasis planavimas iki 90 dienų ateityje kurs papildymo pasiūlymus.  
1. Lauke **Neigiamos dienos** įveskite „1‟.
1. Lauke **Teigiamos dienos** įveskite „1‟.
1. Išplėskite arba sutraukite sekciją **Kiti**.
1. Sekcijos **Laiko rezervas dienomis** lauke **Gavimo laiko rezervas, pridėtas prie pareikalavimo datos** įveskite 1. Pavyzdžiui, jei nustatytas 1 dienos gavimo laiko rezervas, o pirkimo užsakymo eilutę planuojama gauti gegužės 15 d., bendrajame planavime gavimo data bus pakoreguota į gegužės 16 d.
1. Lauke **Išdavimo laiko rezervas, atimtas iš pareikalavimo datos** įveskite 1. Pavyzdžiui, jei nustatytas 1 dienos laiko rezervas, o pardavimo užsakymo eilutę planuojama pristatyti gegužės 15 d., bendrajame planavime pristatymo data bus pakoreguota į gegužės 14 d.  
1. Lauke **Keisti maržos, įtrauktos į prekės gamybos laiką, tvarką** įveskite 1.
1. Pasirinkite **Įrašyti**.

## <a name="create-a-new-product"></a>Kurti naują produktą

Sukurkite naują produktą, atlikdami šiuos veiksmus:

1. Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Produktai > Patvirtinti produktai**.
1. Pasirinkite **Naujas**.
1. Lauke **Produkto numeris** įveskite reikšmę.
1. Lauke **Produkto pavadinimas** įveskite vertę.
1. Lauke **Prekių modelių grupė** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
1. Sąraše raskite ir pasirinkite norimą įrašą.
1. Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.
1. Lauke **Prekių grupė** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
1. Sąraše raskite ir pasirinkite norimą įrašą.
1. Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.
1. Lauke **Saugojimo dimensijų grupė** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
1. Sąraše raskite ir pasirinkite norimą įrašą.
1. Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.
1. Lauke **Sekimo dimensijų grupė** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
1. Sąraše raskite ir pasirinkite norimą įrašą.
1. Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.
1. Pasirinkite **Gerai**.

## <a name="set-up-default-order-settings"></a>Nustatyti numatytąsias užsakymo nuostatas

Nustatykite numatytuosius užsakymo parametrus, atlikdami šiuos veiksmus:

1. **Veiksmų srityje**, pasirinkite **Planas**.
1. Dalyje **Užsakymo parametrai** rinkitės **Numatytieji užsakymo parametrai**.
1. Po **Pirkimo užsakymas** lauku **Numatytoji teritorija** įveskite teritoriją, kuri naudojama kaip numatytoji, kai kuriami pirkimo užsakymai.
1. Lauke **Numatytasis sandėlis** įveskite vietą, kurioje saugoma prekė.
1. Išplėskite arba sutraukite sekciją **Atsargos**.
1. Lauke **Daugkartinis** įveskite „10“.
1. Lauke **„Minimalus užsakymo kiekis** įveskite „10“.
1. Lauke **„Maksimalus užsakymo kiekis** įveskite „100“.
1. Lauke **Standartinis užsakymo kiekis** įveskite „10“.
1. Lauke **Pirkimo vykdymo laikas** įveskite skaičių.
1. Pažymėkite arba išvalykite žymės langelį **Darbo dienos**.
1. Pasirinkite **Įrašyti**.
1. Lauke **Numatytojo užsakymo tipas** pasirinkite „Pirkimo užsakymas“.
1. Pasirinkite **Įrašyti**.
1. Uždarykite puslapį. Uždarykite puslapį Numatytieji užsakymo parametrai.  

## <a name="add-an-item-to-a-coverage-group"></a>Pridėti prekę į padengimo grupę

Įtraukite prekę į padengimo grupę, atlikdami šiuos veiksmus:

1. Išplėskite arba sutraukite sekciją **Planas**.
1. Lauke **Padengimo grupės** rinkitės išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
1. Sąraše raskite **Padengimo grupės**, kurią sukūrėte.
1. Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.

## <a name="create-item-coverage-rules"></a>Kurti prekių padengimo taisykles

Sukurkite prekės padengimo taisykles, atlikdami šiuos veiksmus:

1. **Veiksmų srityje**, pasirinkite **Planas**.
1. Dalyje **Padengimas** rinkitės **Prekės padengimas**.
1. Pasirinkite **Naujas**.
1. Pasirinkite skirtuką **Bendra**.
1. Pažymėkite **Nepaisyti padengimo grupės parametrų** antraštės langelį.
1. Lauke **Padengimo laiko ribos (dienomis)** įveskite 60. Nors prekės padengimo grupėje Poreikis yra planuojamos 90 dienų į priekį, ši prekė bus planuojama 60 dienų į priekį.  
1. Lauke **Neigiamos dienos** įveskite „2‟.
1. Lauke **Teigiamos dienos** įveskite „2‟.
1. Rinkitės skirtuką **Gamybos laikas**.
1. Pažymėkite **Pirkti** antraštės langelį.
1. Lauke **Pirkimo laikas** įveskite 5.
1. Pasirinkite **Įrašyti**.

> [!NOTE]
> Pagamintų prekių gamybos **laikas** naudojamas, jei nėra prekės maršruto. Jei su preke susietas aktyvus maršrutas, bendrasis planavimas suplanuos užsakymą ir apskaičiuos jo datas pagal maršruto laiką ir išteklių pajėgumą (jei taikoma).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
