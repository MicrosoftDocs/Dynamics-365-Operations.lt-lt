---
title: Apibrėžti prekių padengimo taisykles
description: Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.
author: ShylaThompson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 680d7c9339b089a4da82bef18bae3af41e23af30
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845183"
---
# <a name="define-coverage-rules-for-items"></a>Apibrėžti prekių padengimo taisykles

[!include [task guide banner](../../includes/task-guide-banner.md)]

Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Šioje procedūroje nurodoma, kaip kurti padengimo taisykles ir nepaisyti konkrečios prekės padengimo parametrų. Jis taip pat parodo, kaip nurodyti numatytąsias atsargų nuostatas.


## <a name="create-a-coverage-group"></a>Padengimo grupės kūrimas
1. Eikite į **„Naršymo sritis“ > „Moduliai“ > „Bendrasis planavimas“ > „Sąranka“ > „Padengimo grupės“**.
2. Spustelėkite **Naujas**.
3. Lauke **Coverage group** įveskite vertę.
4. Lauke **Pavadinimas** įveskite reikšmę.
5. Lauke **Kalendorius** įveskite reikšmę. Pasirinkite kalendorių, kurį bendrasis planavimas naudos norėdamas sukurti šios grupės prekių papildymo pasiūlymus.  
6. Lauke **Coverage code** pasirinkite parinktį. Pasirinkite Reikalavimai šiai procedūrai.  
7. Lauke **Coverage time fence (days) field** įveskite „90‟. Prekėms šioje grupėje bendrasis planavimas iki 90 dienų ateityje kurs papildymo pasiūlymus.  
8. Lauke **Negative days** įveskite „1‟.
9. Lauke **Positive days** įveskite „1‟.
10. Išplėskite arba sutraukite sekciją **Other**.
11. Skyriaus **Safety margins in days** lauke **Receipt margin added to requirement date** įveskite „1“. Pavyzdžiui, jei nustatytas 1 dienos gavimo laiko rezervas, o pirkimo užsakymo eilutę planuojama gauti gegužės 15 d., bendrajame planavime gavimo data bus pakoreguota į gegužės 16 d.  
12. Lauke **Issue margin deducted from requirement date** įveskite „1‟. Pavyzdžiui, jei nustatytas 1 dienos laiko rezervas, o pardavimo užsakymo eilutę planuojama pristatyti gegužės 15 d., bendrajame planavime pristatymo data bus pakoreguota į gegužės 14 d.  
13. Lauke **Reorder margin added to item lead time** įveskite „1‟.
14. Spustelėkite **Įrašyti**.

## <a name="create-a-new-product"></a>Naujo produkto kūrimas
1. Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Produktai > Patvirtinti produktai**.
2. Spustelėkite **Naujas**.
3. Lauke **Product number** įveskite reikšmę.
4. Lauke **Produkto gavimo kvitas** įveskite vertę.
5. Lauke **Item model group** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
6. Sąraše raskite ir pasirinkite norimą įrašą.
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.
8. Lauke **Item group** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
9. Sąraše raskite ir pasirinkite norimą įrašą.
10. Sąraše spustelėkite saitą pasirinktoje eilutėje.
11. Lauke **Storage dimension group** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
12. Sąraše raskite ir pasirinkite norimą įrašą.
13. Sąraše spustelėkite saitą pasirinktoje eilutėje.
14. Lauke **Tracking dimension group** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
15. Sąraše raskite ir pasirinkite norimą įrašą.
16. Sąraše spustelėkite saitą pasirinktoje eilutėje.
17. Spustelėkite **Gerai**.

## <a name="setup-default-order-settings"></a>Nustatyti numatytąsias užsakymo nuostatas
1. Parinktyje **Action Pane** spustelėkite **Plan**.
2. Dalyje **Order settings** spustelėkite **Default order settings**.
3. Po **Purchase order** lauku **Default site** įveskite teritoriją, kuri naudojama kaip numatytoji, kai kuriami pirkimo užsakymai.
4. Lauke **Default warehouse** įveskite vietą, kurioje saugoma prekė.
5. Išplėskite arba sutraukite sekciją **Inventory**.
6. Lauke **Multiple** įveskite „10“.
7. Lauke **„Minimalus užsakymo kiekis** įveskite „10“.
8. Lauke **„Maksimalus užsakymo kiekis** įveskite „100“.
9. Lauke **Standard order quantity** įveskite „10“.
10. Lauke **Purchase lead time** įveskite skaičių.
11. Pažymėkite arba išvalykite žymės langelį **Working days**.
12. Spustelėkite **Įrašyti**.
13. Lauke **Default order type** pasirinkite „Pirkimo užsakymas“.
14. Spustelėkite **Įrašyti**.
15. Uždarykite puslapį. Uždarykite puslapį Numatytieji užsakymo parametrai.  

## <a name="add-an-item-to-a-coverage-group"></a>Pridėti prekę į padengimo grupę
1. Išplėskite arba sutraukite sekciją **Plan**.
2. Lauke **Coverage group** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
3. Sąraše raskite **Coverage group**, kurią sukūrėte.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.

## <a name="create-item-coverage-rules"></a>Kurti prekių padengimo taisykles
1. Parinktyje **Action Pane** spustelėkite **Plan**.
2. Dalyje **Coverage** spustelėkite **Item coverage**.
3. Spustelėkite **Naujas**.
4. Spustelėkite skirtuką **Bendra**.
5. Pažymėkite funkcijos **Override coverage group** parametrų antraštės langelį.
6. Lauke **Coverage time fence (days)** įveskite „60‟. Nors prekės padengimo grupėje Poreikis yra planuojamos 90 dienų į priekį, ši prekė bus planuojama 60 dienų į priekį.  
7. Lauke **Negative days** įveskite „2‟.
8. Lauke **Positive days** įveskite „2‟.
9. Spustelėkite skirtuką **Lead time**.
10. Pažymėkite antraštės **Purchase** langelį.
11. Lauke **Purchase time** įveskite „5‟.
12. Spustelėkite **Įrašyti**.

