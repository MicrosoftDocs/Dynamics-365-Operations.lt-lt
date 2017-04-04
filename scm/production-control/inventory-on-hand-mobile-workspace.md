---
title: "Atsargų turimų mobiliojo darbo Microsoft Dynamics &quot;365&quot; veiklos programa"
description: "Atsargų turimų mobiliojo darbo srities padeda įgyti mobiliojo ryšio įžvalgų saugomos ir turimus atsargų, bet kada ir bet kur."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 85058f55-e566-40e2-9234-42d3e4fe5ff6
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 2ad48765528e1d1c6e7c90417b54a248ec79f546
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Atsargų turimų mobiliojo darbo Microsoft Dynamics "365" veiklos programa

Atsargų turimų mobiliojo darbo srities padeda įgyti mobiliojo ryšio įžvalgų saugomos ir turimus atsargų, bet kada ir bet kur. 

<a name="prerequisites"></a>Būtinieji komponentai
-------------

| Būtinoji sąlyga                                                         | aprašymas                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Skaityti apie Microsoft Dynamics 365 operacijų mobiliųjų platformų | [Dinamika 365 operacijų mobiliųjų platformų](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Dinamika 365 operacijoms                                          | Aplinkoje, kurioje yra Microsoft Dynamics 365 operacijų versija 1611 ir "Microsoft Dynamics" operacijų platformos naujinimas 3 (2016 m lapkričio mėn.) |
| Karštosios pataisos KB 3215650                                                    | Įdiekite karštąją pataisą norite įgalinti darbo srities, kurie yra pateikti jūsų Microsoft Dynamics 365 operacijoms.                                       |
| Mobiliojo įrenginio, turinčio Dynamics 365 dėl operacijų taikomąją programą | Atsisiųskite Dynamics 365 operacijų App iš mobiliųjų programėlių parduotuvėje.                                                                           |

## <a name="introduction"></a>Įžanga
Paprastai, įmonės turi daugkartinius iškrovimus ir kelių kvitų inventorizacijos kiekvieną dieną. Šie judesiai nuolat keisti turimų atsargų būseną. Atsargų turimų mobiliojo ryšio darbo sritį galite matyti įmonės turimų atsargų būseną, taip, kad jūs galite gauti naujausią pažvelgti į atsargų duomenis apie mobiliojo ryšio prietaisas pagal savo pasirinkimą. Nepriklausomai nuo to, ar dirbate sandėlyje, pirkimo, pardavimo, gamybos, ar valdymo, arba turėti kitų vaidmenų, bet kada ir bet kur galite pasiekti turimų atsargų duomenys. Mobiliojo darbo siūlo momentinių atsižvelgiant, turimas statusas patogumai, ir leidžia jums peržiūrėti atsargų patogumai, dabartinės esminės rezervacijos ir be išlygų turimose atsargose. Galite įvesti prekių numerius į užklausą turimas atsargas ir filtruoti ieškos turimų produktų arba variantai. Konkrečiai, mobiliojo ryšio darbo sritį teikia šias funkcijas:

-   Jūs galite ieškoti pagal produkto numerį arba pavadinimą rasti produktų turimų atsargų būseną.
-   Atrinktiems produktams, galite peržiūrėti tokią informaciją:
    -   Turimų atsargų vietai
    -   Turimos atsargos sandėlyje
    -   Turimų atsargų vietai
    -   Turimų atsargų partijoje (už partijos kontroliuojamų prekių)
    -   Turimų atsargų už atsargų būseną

<!-- -->

-   Prekės turimos atsargos yra rodomas vienu iš šių būdų:
    -   Iš faktinių atsargų (šiuo požiūriu yra visa suma).
    -   Iš fizinės rezervuoti (Šis rodinys yra rezervuotos sumos.)
    -   Iš fizinės (Šis vaizdas sudaro sumos, priima be išlygų.)

## <a name="get-started"></a>Darbo pradžia
Pradžia mobiliajame įrenginyje:

1.  Iš mobiliųjų programėlių parduotuvėje, atsisiųskite ir įdiekite "Microsoft Dynamics 365" veiksmų programos.
2.  Paleiskite programėlę į savo įrenginį.
3.  Įveskite savo dinamika 365 URL.
4.  Įveskite prisijungti prie kompanijos. Pavyzdžiui, įveskite **USMF**.
5.  Pirmą kartą, kai prisijungsite, bus rodomas raginimas įvesti vartotojo vardą ir slaptažodį savo Microsoft Dynamics "365" veiklos sąskaita. Įvesti savo kredencialus. Po to, kai prisijungsite, matote laisvų darbo srities jūsų įmonė.

Norėdami peržiūrėti savo mobiliesiems darbo sričių, pirmiausia turi publikuoti norimą darbo srities dinamika 365 operacijų programos.

1.  Paleisti Dynamics 365 operacijoms.
2.  Eikite į **sistemos administravimo**&gt;**nustatymo**&gt;**sistemos parametrai**.
3.  Pasirinkite **tvarkyti mobiliųjų įrenginių programėlę**.
4.  Pasirinkite darbo sritį skelbti apie mobiliųjų platformų.
5.  Pasirinkite **skelbti darbo srities**.
6.  Atnaujinkite įrenginio paskelbtų darbo sritis.

## <a name="view-the-onhand-inventory-for-a-product"></a>Rodyti turimų atsargų aprašą produkto
1.  Mobiliajame įrenginyje, pasirinkite į **turimas atsargas** darbo srities.
2.  Pasirinkite **patikrinti turimos prekės**. Pamatysite sąrašą produktų, kurie yra pakrauta į savo programą naudoti neprisijungus. Pagal numatytuosius nustatymus 50 prekės pakraunamos, tačiau jūs galite pakeisti šį numerį. Daugiau informacijos ieškokite iš anksto skaityti vadovą.
3.  Jei jūsų prekės nėra sąraše, pasirinkite **ieškoti daugiau** daryti interneto paieškos Dynamics 365 operacijoms. Ieškoti pagal produkto numerį, arba pereiti į paieškos pagal prekės pavadinimą.
4.  Pasirinkite produktą. Jei prekė turi vaizdą, vaizdas yra rodomas.
5.  Pasirinkite vieną iš šių parinkčių norėdami peržiūrėti atsargų būseną:
    -   Rodyti turimas vietai
    -   Peržiūrėti turimos sandėlyje
    -   Rodyti turimas vietai
    -   Rodyti turimas partijoje (už partijos kontroliuojamų prekių)
    -   Rodyti turimas už atsargų būseną

    Prekės turimos atsargos yra rodomas vienu iš šių būdų:
    -   Iš faktinių atsargų (šiuo požiūriu yra visa suma).
    -   Iš fizinės rezervuoti (Šis rodinys yra rezervuotos sumos.)
    -   Iš fizinės (šiam požiūriui atstovauja turima suma, kuri priima be išlygų.)




