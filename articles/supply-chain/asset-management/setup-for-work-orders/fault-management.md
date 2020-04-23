---
title: Gedimų valdymas
description: Šioje temoje aiškinamas gedimų valdymas modulyje Turto valdymas.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6665e80342af1baa7176aee92693b77e83b368f0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205925"
---
# <a name="fault-management"></a>Gedimų valdymas

[!include [banner](../../includes/banner.md)]

 

Modulyje Turto valdymas gedimų dizaino įrankiu galite nustatyti turto tipų gedimų požymius, gedimų sritis ir gedimų tipus. Taip galite valdyti rastus turto gedimus. Be to, gedimų priežastis ir pasiūlymus dėl gedimų pašalinimo galima užregistruoti darbo užsakyme.

Gedimų registravimo ir valdymo procesą sudaro toliau pateikiami veiksmai.

1. Sukurkite turto tipų galimus gedimų požymius, gedimų sritis ir gedimų tipus.
2. Gedimų dizaino įrankiu nustatykite turto tipų gedimų požymius, gedimų sritis ir gedimų tipus.

Toliau pateikiama pavyzdžių, padėsiančių suprasti skirtumą tarp gedimų požymių, gedimų sričių ir gedimų tipų.

**Gedimų požymiai.**

- Įtampų disbalansas
- Trumpasis jungimas
- Triukšmas
- Nuotėkis
- Vibracija

**Gedimų sritys.**

- Elektra
- Mechanika
- Hidraulika
- Pneumatika

**Gedimų tipai.**

- Sugedusi pagrindinė statoriaus apvija
- Sugedęs diodas
- Nešvarios apvijos
- Sugedęs generatorius
- Sugedęs jutiklis

## <a name="create-fault-symptoms"></a>Gedimų požymių kūrimas

Atlikite toliau pateikiamus veiksmus, norėdami sukurti požymių sąrašą, kurį galima naudoti gedimų dizaino įrankyje.

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Gedimas** \> **Gedimų požymiai**.
2. Pasirinkite **Naujas** pranešimui sukurti.
3. Lauke **Gedimo požymis** įveskite gedimo požymio pavadinimą.
4. Lauke **Aprašas** įveskite aprašą.
5. Pasirinkite **Įrašyti**.

## <a name="create-fault-areas"></a>Gedimų sričių kūrimas

Atlikite toliau pateikiamus veiksmus, norėdami sukurti sričių arba vietų sąrašą, kurį galima naudoti gedimų dizaino įrankyje.

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Gedimas** \> **Gedimų sritys**.
2. Pasirinkite **Naujas** pranešimui sukurti.
3. Lauke **Gedimo sritis** įveskite gedimo srities pavadinimą.
4. Lauke **Aprašas** įveskite aprašą.
5. Pasirinkite **Įrašyti**.

## <a name="create-fault-types"></a>Gedimų tipų kūrimas

Atlikite toliau pateikiamus veiksmus, norėdami sukurti gedimų tipų sąrašą, kurį galima naudoti gedimų dizaino įrankyje.

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Gedimas** \> **Gedimų tipai**.
2. Pasirinkite **Naujas** pranešimui sukurti.
3. Lauke **Gedimo tipas** įveskite gedimo tipo pavadinimą.
4. Lauke **Aprašas** įveskite aprašą.
5. Pasirinkite **Įrašyti**.

## <a name="set-up-the-fault-designer"></a>Gedimų dizaino įrankio nustatymas

Gedimų dizaino įrankiu nustatomi turto tipų gedimų duomenys.

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Gedimas** \> **Gedimų dizaino įrankis**.
2. Kairiojoje srityje pasirinkite turto tipą, kuriam norite sukurti gedimų įrašą.
3. FastTab **Gedimo požymis** pasirinkite **Įtraukti eilutę**, paskui lauke **Gedimo požymis** pasirinkite gedimo požymį.
4. FastTab **Gedimo sritis** pasirinkite **Įtraukti eilutę**, paskui lauke **Gedimo sritis** pasirinkite gedimo sritį.
5. FastTab **Gedimo tipas** pasirinkite **Įtraukti eilutę**, paskui lauke **Gedimo tipas** pasirinkite gedimo tipą.
6. Greitai sukurkite pasirinkto turto tipo visų esamų gedimų požymių, sričių ir tipų derinius, pasirinkę **Kurti gedimų derinius**. Ši funkcija naudinga, jei įtraukėte daug gedimų požymių, sričių ir tipų. Paprasčiau panaikinti turto tipui neaktualias derinių eilutes, nei rankiniu būdu sukurti naujų eilučių.

    > [!NOTE]
    > Nukopijuokite gedimų požymių, sričių ir tipų sąranką iš vieno turto tipo į pasirinktą turto tipą, pasirinkę **Kopijuoti iš turto tipo**.

7. Pasirinkite **Įrašyti**, kad įrašytumėte pakeitimus.

![Gedimų dizaino įrankio puslapis](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a>Gedimų priežasčių kūrimas

Atlikite toliau pateikiamus veiksmus, norėdami sukurti žinomų gedimų priežasčių sąrašą, kurį galima įtraukti į darbo užsakymą arba priežiūros užklausą.

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Gedimas** \> **Gedimų priežastys**.
2. Pasirinkite **Naujas** pranešimui sukurti.
3. Lauke **Gedimo priežastis** įveskite gedimo priežasties pavadinimą.
4. Lauke **Aprašas** įveskite aprašą.
5. Pasirinkite **Įrašyti**.

## <a name="create-fault-remedies"></a>Gedimų šalinimo priemonių kūrimas

Atlikite toliau pateikiamus veiksmus, norėdami sukurti pasiūlymų dėl gedimų šalinimo ir remonto sąrašą, kurį galima įtraukti į darbo užsakymą arba priežiūros užklausą.

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Gedimas** \> **Gedimų šalinimo priemonės**.
2. Pasirinkite **Naujas** pranešimui sukurti.
3. Lauke **Gedimo šalinimo priemonė** įveskite gedimo šalinimo priemonės pavadinimą.
4. Lauke **Aprašas** įveskite aprašą.
5. Pasirinkite **Įrašyti**.

> [!NOTE]
> Jei reikia, galite pakeisti gedimų požymių, sričių, tipų, priežasčių ir šalinimo priemonių pavadinimus. Pavadinimo pakeitimai automatiškai fiksuojami atitinkamo gedimo registracijos įrašuose.
