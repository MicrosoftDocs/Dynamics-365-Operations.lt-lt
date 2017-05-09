---
title: "Turimų atsargų mobilioji darbo sritis, skirta programai „Microsoft Dynamics 365 for Operations“"
description: "Turimų atsargų mobilioji darbo sritis mobiliojoje aplinkoje suteikia įžvalgų apie rezervuotas ir turimas atsargas bet kur ir bet kada."
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

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Turimų atsargų mobilioji darbo sritis, skirta programai „Microsoft Dynamics 365 for Operations“

Turimų atsargų mobilioji darbo sritis mobiliojoje aplinkoje suteikia įžvalgų apie rezervuotas ir turimas atsargas bet kur ir bet kada. 

<a name="prerequisites"></a>Būtinieji komponentai
-------------

| Būtinoji sąlyga                                                         | aprašymas                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Skaitykite apie „Microsoft Dynamics 365 for Operations“ mobiliąją platformą | [Mobilioji „Dynamics 365 for Operations“ platforma](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Dynamics 365 for Operations                                          | Aplinka, kurioje yra „Microsoft Dynamics 365 for Operations“ 1611 versijos ir „Microsoft Dynamics for Operations“ 3 platformos naujinimas (2016 m. lapkričio mėn.) |
| Karštosios pataisos KB 3215650                                                    | Įdiegę karštąsias pataisas įjunksite „Microsoft Dynamics 365 for Operations“ pateikiamas darbo sritis.                                       |
| Mobilusis įrenginys, kuriame įdiegta programa „Dynamics 365 for Operations“ | Iš mobiliųjų įrenginių programėlių parduotuvės atsisiųskite programą „Dynamics 365 for Operations“.                                                                           |

## <a name="introduction"></a>Įžanga
Paprastai įmonės kas dieną apdoroja daug atsargų siuntų ir gavimų. Dėl šių perkėlimų nuolat kinta turimų atsargų būsena. Turimų atsargų mobilioji darbo sritis suteikia galimybę peržiūrėti turimų atsargų būseną visose įmonėse, todėl galite sužinoti naujausią informaciją apie atsargų duomenis savo pasirinktame mobiliajame įrenginyje. Nepriklausomai nuo to, ar dirbate sandėlyje, pirkimo, pardavimo, gamybos arba vadovybės skyriuje, ar turite kitų vaidmenų, turimų atsargų duomenis galite pasiekti bet kur ir bet kada. Mobilioji darbo sritis suteikia visų objektų turimų atsargų būsenos momentinį rodinį ir galimybę peržiūrėti visų objektų turimas atsargas, esamus medžiagų rezervavimus ir nerezervuotas turimas atsargas. Taip pat galite įvesti prekių numerius ir pateikti turimų atsargų užklausą bei atlikti filtruotą turimų produktų ar jų variantų iešką. Tiksliau sakant, mobilioji darbo sritis suteikia toliau nurodytas funkcijas.

-   Galite ieškoti pagal produkto numerį arba produkto pavadinimą, kad rastumėte produktus, kurių turimų atsargų būseną norite peržiūrėti.
-   Galite peržiūrėti toliau nurodytą informaciją apie pasirinktus produktus.
    -   Turimos atsargos pagal teritoriją
    -   Turimos atsargos pagal sandėlį
    -   Turimos atsargos pagal vietą
    -   Turimos atsargos pagal paketą (skirta paketais valdomiems produktams)
    -   Turimos atsargos pagal atsargų būseną

<!-- -->

-   Produkto turimos atsargos rodomos toliau nurodytais būdais.
    -   Pagal faktines atsargas (Šis rodinys nurodo bendrą sumą.)
    -   Pagal faktines rezervuotas atsargas (Šis rodinys nurodo rezervuotą sumą.)
    -   Pagal turimas faktines atsargas (Šis rodinys nurodo turimą sumą, kuri nėra rezervuota.)

## <a name="get-started"></a>Darbo pradžia
Norėdami pradėti naudoti šią darbo sritį mobiliajame įrenginyje, atlikite tolesnius veiksmus.

1.  Iš mobiliųjų įrenginių programėlių parduotuvės atsisiųskite ir įdiekite programą „Dynamics 365 for operations“.
2.  Paleiskite programą savo mobiliajame įrenginyje.
3.  Įveskite savo „Dynamics 365“ URL.
4.  Įveskite įmonę, prie kurios norite prisijungti. Pavyzdžiui, įveskite **USMF**.
5.  Pirmą kartą prisijungus būsite paraginti įvesti savo „Microsoft Dynamics 365 for Operations“ paskyros vartotojo vardą ir slaptažodį. Įveskite savo kredencialus. Prisijungę matysite galimas savo įmonės darbo sritis.

Norėdami darbo sritis peržiūrėti savo mobiliojoje programoje, pirmiausia turite pageidaujamas sritis publikuoti programoje „Dynamics 365 for Operations“.

1.  Paleiskite „Dynamics 365 for Operations“.
2.  Pasirinkite **Sistemos administravimas** &gt; **Sąranka** &gt; **Sistemos parametrai**.
3.  Pasirinkite **Tvarkyti mobiliąją programą**.
4.  Pasirinkite darbo sritį, kad ją publikuotumėte mobiliojoje platformoje.
5.  Pasirinkite **Publikuoti darbo sritį**.
6.  Atnaujinkite įrenginio rodinį, kad matytumėte publikuojamas darbo sritis.

## <a name="view-the-onhand-inventory-for-a-product"></a>Produkto turimų atsargų peržiūra
1.  Savo mobiliajame įrenginyje pasirinkite darbo sritį **Turimos atsargos**.
2.  Pasirinkite **Patikrinti turimas prekės atsargas**. Matysite produktų, kurie įkelti į jūsų programą ir kuriuos galima tvarkyti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama 50 prekių, tačiau šį skaičių galima keisti. Daugiau informacijos žr. anksčiau perskaitytame vadove.
3.  Jei jūsų prekė nėra įtraukta į sąrašą, pasirinkite **Ieškoti daugiau**, kad galėtumėte atlikti paiešką tinkle programoje „Dynamics 365 for Operations“. Ieškokite pagal produkto numerį arba perjunkite iešką pagal produkto pavadinimą.
4.  Pasirinkite produktą. Jei prekei priskirtas vaizdas, jis bus rodomas.
5.  Pasirinkite vieną iš tolesnių parinkčių, kad peržiūrėtumėte turimų atsargų būseną.
    -   Peržiūrėti turimas atsargas pagal teritoriją
    -   Peržiūrėti turimas atsargas pagal sandėlį
    -   Peržiūrėti turimas atsargas pagal vietą
    -   Peržiūrėti turimas atsargas pagal paketą (skirta paketais valdomiems produktams)
    -   Peržiūrėti turimas atsargas pagal atsargų būseną

    Produkto turimos atsargos rodomos toliau nurodytais būdais.
    -   Pagal faktines atsargas (Šis rodinys nurodo bendrą sumą.)
    -   Pagal faktines rezervuotas atsargas (Šis rodinys nurodo rezervuotą sumą.)
    -   Pagal turimas faktines atsargas (Šis rodinys nurodo turimą sumą, kuri nėra rezervuota.)




