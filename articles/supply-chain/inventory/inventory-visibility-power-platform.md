---
title: Atsargų matomumo programa
description: Šiame straipsnyje aprašoma, kaip naudoti programą Atsargų matomumas.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a360b8beaad2bf6916c22765131e37f90e40282b
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306180"
---
# <a name="use-the-inventory-visibility-app"></a>Naudokite programą „Inventory Visibility“

[!include [banner](../includes/banner.md)]


Šiame straipsnyje aprašoma, kaip naudoti programą Atsargų matomumas.

Atsargų matomumas suteikia modeliu pagrįstą programą vizualizacijai. Programą sudaro trys puslapiai: **Konfigūracija**, **Veiklos matomumas** ir **Atsargų suvestinė**. Jam būdingos šios funkcijos:

- Ji suteikia turimos konfigūracijos ir švelniai rezervavimo konfigūracijos vartotojo sąsają (UI).
- Jis palaiko realiuoju laiku turimų atsargų užklausas įvairiuose dimensijų deriniaie.
- Joje pateikiama vartotojo sąsajos, skirtos UI užklausoms registruoti.
- Ji pateikia pritaikytą turimų produktų atsargų rodinį kartu su visomis dimensijomis.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradėdami, įdiekite ir nustatykite atsargų matomumo priedą, kaip aprašyta [įdiegti ir nustatyti atsargų matomumą](inventory-visibility-setup.md).

## <a name="open-the-inventory-visibility-app"></a>Atverti atsargų matomumo programą

Norėdami atidaryti atsargų matomumo programą, prisijunkite prie savo „Power Apps“ aplinkos ir atidarykite **Atsargų matomumą**.

## <a name="configuration"></a><a name="configuration"></a>Konfigūravimas

Atsargų matomumo programa **Konfigūracijos** puslapis padeda nustatyti turimos konfigūracijos ir soft reservation konfigūraciją. Įdiegus papildinį, numatytoji konfigūracija įtraukia „Microsoft Dynamics 365 Supply Chain Management“ (duomenų `fno` šaltinio vertę). Galite peržiūrėti numatytuosius nustatymus. Tada, atsižvelgdami į savo verslo poreikius ir išorinės sistemos atsargų registravimo reikalavimus, galite modifikuoti konfigūraciją, kad būtų galima standartizuoti būdą, kuriuo atsargų pakeitimai gali būti registruojami, tvarkomi keliose sistemose ir jų bus užklausta.

Išsami informacija apie sprendimo konfigūravimą pateikta [Atsargų matomumo konfigūravimas](inventory-visibility-configuration.md).

## <a name="operational-visibility"></a>Veikimo matomumas

Veiklos **matomumo puslapis** pateikia realiuoju laiku turimų atsargų užklausos rezultatus, paremtus įvairiomis dimensijų kombinacijomis. Kai *OnHandReservation* funkcija įjungta, taip pat galite registruoti rezervavimo užklausas iš **veiklos matomumo** puslapio.

### <a name="on-hand-query"></a>Turimos užklausos

Skirtuke **Turimų atsargų** užklausa rodomi turimų atsargų realiuoju laiku užklausos rezultatai.

Kai pasirenkate skirtuką **Turimų atsargų** užklausa, sistema reikalauja jūsų kredencialų, kad ji galėtų gauti paženklą, kuris būtinas norint pateikti užklausą dėl atsargų matomumo tarnybos. Galite tiesiog įklijuoti ypatybės atpažinimo ženklą į lauką **BearerToken** ir uždaryti dialogo langą. Tada galite registruoti turimos informacijos užklausą.

Jei pateikėjas atpažinimo ženklas netinkamas arba jei jis baigė galioti, lauke **BearerToken** turite įklijuoti naują ženklą. Įveskite teisingą **kliento ID**, **nuomininko ID**, **Kliento rakto** naujinimo reikšmes ir pasirinkite **Atnaujinti**. Sistema automatiškai gaus naują, galiojantį paerio atpažinimo ženklą.

Norėdami užregistruoti turimos informacijos užklausą, įveskite užklausą užklausos tekstą. Naudokite šabloną, kuris aprašytas [Užklausoje, naudodami skelbimo metodą](inventory-visibility-api.md#query-with-post-method).

![Turimos užklausos nustatymai](media/inventory-visibility-query-settings.png "Turimos užklausos nustatymai")

### <a name="reservation-posting"></a>Rezervavimo publikavimas

Norėdami **užregistruoti rezervavimo** užklausą, naudokite skirtuką Rezervavimo registravimas. Kad būtų galima užregistruoti rezervavimo užklausą, reikia įjungti funkciją *OnHandReservation*. Dėl daugiau informacijos apie šią funkciją, žr. [Inventoriaus matomumo rezervavimas](inventory-visibility-reservations.md).

Norėdami registruoti rezervavimo užklausą, turite įvesti vertę užklausos tekstą. Naudokite trafaretą, kuris aprašytas [kurti vieną rezervavimo įvykį](inventory-visibility-api.md#create-one-reservation-event). Tada rinkitės **Publikuoti**. Norėdami peržiūrėti užklausos atsakymo informaciją, pasirinkite **Rodyti išsamią informaciją**. Taip pat galite gauti  `reservationId` vertę iš atsakymo informacijos.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Atsargų suvestinė

Atsargų **suvestinės puslapis** pateikia produktų atsargų suvestinę kartu su visomis dimensijomis. Tai pasirinktinis objekto Atsargų *atsargų suma* rodinys. Atsargų suvestinės duomenys periodiškai sinchronizuojami pagal atsargų matomumą.

### <a name="enable-the-inventory-summary-and-set-the-synchronization-frequency"></a>Įgalinti atsargų suvestinę ir nustatyti sinchronizavimo dažnumą

Norėdami įgalinti atsargų **suvestinės puslapį ir** nustatyti sinchronizavimo dažnumą, atlikite šiuos veiksmus:

1. Atidarykite **Konfigūravimo** puslapį.
1. Atidarykite **skirtuką Priemonių valdymas >** Parametrai.
1. Nustatykite OnHandMostSpecificBackgroundService **funkcijos** perjungimo raktą kaip *Taip*.
1. Įgalinus funkciją, tarnybos **konfigūravimo** **dalis tampa galima, o jos metu konfigūruojama OnHandMostSpecificBackgroundService** funkcija. Šis parametras leidžia pasirinkti dažnumą, kuriuo sinchronizuojami atsargų suvestinės duomenys. Naudokite stulpelio **Vertė** **mygtukus** **Aukštyn ir Žemyn,** norėdami pakeisti laiką tarp sinchronizavimų (kuris gali būti ne mažas kaip 5 minutės). Tada pasirinkite **Įrašyti**.
1. Pasirinkite **Naujinti konfigūraciją,** kad įrašytumėte visus pakeitimus.

![OnHandMostSpecificBackgroundService parametras](media/inventory-visibility-ohms-freq.PNG "OnHandMostSpecificBackgroundService parametras")

> [!NOTE]
> OnHandMostSpecificBackgroundService *funkcija* seka tik turimo produkto keitimus, kurie įvyko po to, kai buvo įjungta funkcija. Produktų, kurie nebuvo pakeisti nuo tada, kai įjungta funkcija, duomenys nebus sinchronizuoti iš atsargų tarnybos talpyklos į aplinką Dataverse. Jei jūsų **atsargų** suvestinės puslapis nerodo visos turimos informacijos, kurios tikitės, **eikite į Atsargų valdymo > Periodinės užduotys > Atsargų matomumo integravimas**, uždrauskite paketinę užduotį ir vėl ją įjunkite. Taip bus inicijuotas stūmiimas ir visi duomenys *bus sinchronizuoti su atsargų sumos objektu* per kitas 15 minučių. Jei norite naudoti šią priemonę, **rekomenduojame ją įjungti prieš kuriant turimų atsargų pakeitimus ir įgalinti atsargų matomumo integravimo paketinę** užduotį.

### <a name="work-with-the-inventory-summary"></a>Darbas su atsargų suvestine

Naudodami **išplėstinį filtrą**, kuris suteikia „Dataverse“, galite sukurti asmeninį rodinį, kuriame būtų rodomos jums svarbios eilutės. Išplėstinės filtro pasirinktys leidžia jums sukurti platų rodinių diapazoną – nuo paprasto iki kompleksinio. Jos taip pat leidžia į filtrus įtraukti sugrupuotas ir įdėtąsias sąlygas. Norėdami sužinoti daugiau apie tai, kaip naudoti **išplėstinį filtrą**, žr. [Redaguoti arba kurti asmeninius rodinius naudojant išplėstinius tinklelių filtrus](/powerapps/user/grid-filters-advanced).

Pritaikyto rodinio viršuje pateikiami trys laukai: **Numatytoji dimensija**, **Pasirinktinė dimensija** ir **Matas**. Šiuos laukus galite naudoti, kad kontroliuojate, kurie stulpeliai yra matomi.

Norėdami filtruoti arba rūšiuoti esamus rezultatus, galite pasirinkti stulpelio antraštę.

Tinkinimo rodinio apačioje rodoma tokia informacija: „50 įrašų (pasirinkta 29)" arba „50 įrašų". Ši informacija nurodo šiuo metu įkeltus įrašus iš **išplėsto filtro** rezultato. Tekstas „29 pasirinktas" nurodo įrašų, kurie buvo pasirinkti naudojant įkeltų įrašų stulpelio antraštės filtrą, skaičių.

Rodinio apačioje yra mygtukas **Įkelti daugiau**, kurį galite naudoti norėdami įkelti daugiau įrašų iš „Dataverse“. Numatytasis įkeltų įrašų skaičius yra 50. Pasirinkus **Įkelti daugiau**, į rodinį įkeliama kita 1000 galimų įrašų. Mygtuko Įkelti **daugiau mygtukas** nurodo šiuo metu įkeltus įrašus ir bendrą išplėstinio filtro **rezultato įrašų** skaičių.

![Atsargų suvestinė](media/inventory-visibility-onhand-list.png "Atsargų suvestinė")
