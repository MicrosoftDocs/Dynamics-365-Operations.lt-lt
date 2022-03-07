---
title: Pardavimo ir perkėlimo užsakymų surinkimo viršijimas
description: Šioje temoje paaiškinama, kaip įgalinti pardavimo ir perkėlimo užsakymų surinkimo perviršį.
author: GalynaFedorova
ms.date: 07/06/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-06
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3c6f9d386f79754edce38e4e2cf4c9bfefbce69bdb252e8754f39d909827fa02
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722156"
---
# <a name="over-picking-for-sales-orders-and-transfer-orders"></a>Pardavimo ir perkėlimo užsakymų surinkimo viršijimas

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiamas scenarijus, kuris rodo, kaip įgalinti konkretų darbuotoją arba visus darbuotojus surinkimo viršijimui. Surinkimo viršijimo procesas leidžia rinkimo metu valdyti surinkimo perviršį.

Sandėlio surinkimo viršijimas yra paprastos koncepcijos. Sistema leidžia darbuotojams surinkti daugiau prekių, nei nurodyta užsakyme. Tačiau, vis dar yra atsižvelgiama į pristatymo pertekumo ribą, kuri nustatyta perkėlimo užsakymo arba pardavimo užsakymo eilutės lygyje. Jei ši riba viršijama, „Warehouse Management“ programa darbuotojams praneša, kad jie viršija pristatymo perviršio ribą.

Surinkimo viršijimo funkcija padeda sumažinti priežiūrą ir taip pat padeda jūsų nustatymui išlikti kintamu. Galite nurodyti vieną ar daugiau mobiliojo įrenginio meniu elementų ir įgalinti surinkimo perviršį tik kai kuriuose iš jų. Be to, kad nereikėtų keisti meniu elementų, galite neleisti pasirinktiems darbuotojams pasirinkti pardavimo ir (arba) perkėlimo užsakymų surinkimo viršijimo. Užuot tai darę, galite išjungti vieną arba abi šias galimybes atitinkamų darbuotojų nustatymuose.

Surinkimo viršijimo funkcija gali padėti darbuotojams sutaupyti laiko ir pastangų surenkant ir išsiunčiant prekes. Pavyzdžiui, funkcija leidžia darbuotojams atlikti šias užduotis:

- Kompensuoti sumažėjimą paėmimo arba siuntimo metu.
- Išvengti kai kurių pakavimo medžiagų išpakavimo išrinkimo proceso metu.
- Kompensuoti už prekės sugadinimą transportavimo metu.
- Išsiųsti netikslų vienetų kiekį arba nevienodų matavimų.
- Iki minimumo sumažinti licenzijuotų lentelių kiekį.
- Išvengti brangių medžiagų švaistymo ir trūkumo.
- Išmatuoti paimtą kiekį po surinkimo (pvz. pasveriant sunkvežimį).

> [!IMPORTANT]
> Surinkimo viršijimo funkcija taikoma tik pardavimo užsakymui ir perkėlimo užsakymo paėmimui bei apdorojimui. Papildymas nepalaiko surinkimo perviršio funkcijos. Kai atliekamas papildymo darbas, sistema neleidžia vartotojams surinkti per daug.

Šioje temoje parodytas scenarijus, kaip nustatyti ir naudoti perrinkimo funkciją.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Būtina scenarijaus sąlyga: padaryti pasiekiamas demonstracinius duomenis

Šioje temoje esantis scenarijus nurodo reikšmes ir įrašus, įtrauktus į standartinius „Microsoft Dynamics 365 Supply Chain Management” demonstracinius duomenis. Jei norite naudoti čia pateiktas reikšmes atlikdami pratimus, įsitikinkite, kad dirbate aplinkoje, kurioje įdiegti demonstraciniai duomenys, ir prieš pradėdami nustatykite juridinį subjektą į *USMF*.

## <a name="scenario-setup"></a>Scenarijaus nustatymas

Prieš naudodami pavyzdinį scenarijų turite įgalinti surinkimo perviršį tiek atitinkam darbuotojui, tiek ir atitinkamo meniu elementui.

### <a name="set-up-a-worker-to-allow-for-over-picking"></a>Nustatykite darbuotoją, kad būtų leidžiamas surinkimo perviršis

Čia pateikiama bendra darbuotojo konfigūravimo procedūra, norint atskirai įgalinti pardavimo užsakymų ir perkėlimo užsakymų surinkimo viršijimą. Ši konfigūracija valdo, kuris rinkimo darbuotojas gali atlikti surinkimo viršijimą ir, ar tas darbuotojas gali atlikti perrinkimą tiek perkėlimo užsakymams, tiek ir pardavimo užsakymams.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Darbuotojai**.
1. Sąrašo srityje pasirinkite **„Julia Funderburk”**.
1. „FastTab” **Vartotojai** pasirinkite eilutę, kuri turi toliau pateiktas vertes. Jei nei viena eilutė neturi šių verčių, sukurkite ją.

    - **Vartotojo ID:** *„24”*
    - **Vartotojo vardas:** *„WH 24”*
    - **Nustatytasis sandėlis:** *24*
    - **Meniu pavadinimas:** *Pagrindinis*

1. „FastTab” **Darbas** nustatykite šias reikšmes *„24”* vartotojui, jei jos dar nėra nustatytos:

    - **Leisti pardavimų surinkimo perviršį:** *Taip*
    - **Leisti perkėlimo užsakymo surinkimo perviršį:** *Taip*

### <a name="set-up-a-mobile-device-menu-item-to-allow-for-over-picking"></a>Mobiliojo įrenginio meniu elemento nustatymas surinkimo perviršio įgalinimui

Čia yra bendroji mobiliojo įrenginio meniu elemento konfigūravimo, siekiant įgalinti surinkimo perviršio funkciją, procedūra. Priklausomai nuo jūsų verslo reikalavimų, keliamų darbuotojui, kuris naudos mobiliojo įrenginio meniu, lygio, kai kurie parametrai gali būti įjungti arba išjungti.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Sąrašo srityje pasirinkite įrašą, pavadintą *Pardavimų surinkimas*. Jei joks esamas įrašas neturi šio pavadinimo, sukurkite jį. Patvirtinkite arba nustatykite šias įrašo vertes:

    - **Meniu elemento pavadinimas:** *Pardavimų surinkimas*
    - **Pavadinimas:** *Pardavimų surinkimas*
    - **Režimas:** *Darbas*
    - **Naudoti esamą darbą:** *Taip*
    - **Vadovas:** *Vartotojui nurodyta*
    - **Nepaisyti paskirties numerio lentelės:** *Taip*
    - **Nepaisyti numerio lentelės padavimo metu:** *Taip*
    - **Palikti vartotojo užrakintą darbą:** *Taip*
    - **Leisti surinkimo perviršį:** *Taip*

> [!IMPORTANT]
> Įgalinus atitinkamus darbuotojo ir mobiliojo įrenginio meniu elemento parametrus, surinkimo perviršį galima apdoroti tik naudojant mobilųjį įrenginį.

## <a name="example-scenario"></a>Pavyzdinis scenarijus

Kai būtinosios sąlygos, darbuotojų nustatymas ir meniu elemento nustatymas yra pritaikyti, esate pasiruošę dirbti su šia funkcija.

### <a name="create-a-sales-order-that-allows-for-overdelivery"></a>Sukurkite pardavimo užsakymą, kuriam leidžiamas pristatymo viršijimas

1. Eikite į **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Norėdami kurti naują pardavimo užsakymą, pasirinkite **Naujas**.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - **Kliento sąskaita:** *US-001*
    - **Sandėlis:** *24*

1. Pasirinkite **Gerai**.
1. Naujas pardavimo užsakymas yra atidarytas. **Prekybos užsakymai** „FastTab“, įtraukite eilutę, kuri turi šiuos nustatymus:

    - **Prekės numeris:** *A0001*
    - **Kiekis:** *10*

1. „FastTab“ konteinerio **Eilutės informacija** skirtuke **Pristatymas** nustatykite lauko **Pristatymo perteklius** reikšmę kaip *10*.
1. **Prekybos užsakymo eilučių** „FastTab“, pasirinkite **Atsargos \> Rezervavimas**.
1. **Rezervavimo** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** inventoriaus rezervavimui.
1. Uždarykite **Rezervavimas** puslapį.
1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.

Kai išleidimas bus atliktas, gausite informacinį pranešimą, kuriame bus rodomi sukurti bangos ir krovinio ID.

### <a name="get-the-work-id-and-license-plate-number-for-the-new-order"></a>Gauti naujo užsakymo darbo ID ir numerio lentelę

Paleidus pardavimo užsakymą į sandėlį, sistema turi sukurti naują darbo ID, kuriame yra viena surinkimo eilutė. Norėdami rasti darbo ID ir numerio lentelių priskyrimus, atlikite toliau pateiktus veiksmus.

1. Pasirinkite **Sandėlio valdymas \> Darbas \> Darbo išsami informacija**.
1. Tinklelyje **Apžvalga** ieškokite pardavimo užsakymo, kurį ką tik sukūrėte, stulpelio **Užsakymo numeris**. Tam pardavimo užsakymui pažymėkite atitinkamą darbo ID.
1. Naujam pardavimo užsakymui pasirinkite eilutę, kad tinklelyje **Eilutės** būtų rodoma susijusi informacija. Pasižymėkite tos prekės vietą, kur ji bus paimta.
1. Eikite į **Atsargų valdymas \> Užklausos ir ataskaitos \> Turimas sąrašas**.
1. Veiksmų juostoje, pasirinkite **Dimensijos**.
1. Dialogo langelyje **Išmatavimų rodymas** užtikrinkite, kad yra pasirinkti **Numerio lentelė**, **Sandėlys**, ir **Prekės numeris** žymės langeliai ir tada pasirinkite **OK**.
1. Srityje **Filtras**, nustatykite toliau nurodytus filtrus.

    - **Prekės numeris** – **yra vienas iš** – *A0001*
    - **Sandėlis** – **prasideda** – *24*

1. Pasirinkite **Taikyti**.
1. Pasižymėkite rodomas **numerio lentelės** reikšmes.

### <a name="over-pick-the-order-by-using-the-warehouse-management-mobile-app"></a>Naudojantis „Warehouse Management“ mobiliąją programa atlikite užsakymo surinkimo viršijimą

1. Prisijunkite prie „Warehouse Management“ mobiliųjų įrenginių programėlės kaip vartotojas sandėlyje *24*.
1. Eikite į **Išorė \> Prekybos paėmimas**.
1. **Nuskaityti darbo ID arba numerio lentelę** laukelyje įveskite darbo ID, kuris buvo sukurtas pardavimo užsakymui.
1. Pasirinkite **Gerai** (varnelės simbolis).
1. Pasirinkite **Surinkimo perviršis**.
1. Nustatykite **Surinkimo kiek.** laukelį į *14*.
1. Pasirinkite **Gerai** (varnelės simbolis).

    **Perrinkimo** puslapyje gausite tokią žinutę: "Eilutės pristatymo perviršis yra 40.00 procentų, tačiau leistinas pristatymo perviršis yra tik 10.00 procentų." Šis pranešimas nurodo, kad jūsų įvestas paėmimo kiekis viršija pristatymo perviršio ribą. Pardavimo užsakymo eilutės pristatymo perviršio riba yra 10 procentų. Todėl, jei nurodytas kiekis yra 10, surinkimą viršyti galite tik 1, kad bendras surinktas kiekis būtų – 11.

1. Nustatykite **Surinkimo kiek.** laukelį į *11*.
1. Pasirinkite **Gerai** (varnelės simbolis).
1. **Numerio lentelės** laukelyje įveskite numerio lentelę, kurią pasižymėjote kaip nurodyta ankstesniame skyriuje.
1. **Tikslinės numerio lentelės** laukelyje įveskite tikslinės numerio lentelės ID. Atkreipkite dėmesį, kad yra rodoma paėmimo vieta (*FLOOR-001*), elementas (*A0001*) ir kiekis (*11 vnt.*).
1. Pasirinkite **Gerai** (varnelės simbolis).
1. Peržiūrėkite informaciją **Prekybos užsakymai - Paėmimas** puslapyje. **Loc** laukelis turi rodyti, kad paimti elementai bus *BAYDOOR* vietoje.
1. Pasirinkite **Gerai** (varnelės simbolis).

**Darbo / licencijos numerio identifikavimo kodo nuskaitymo** puslapyje jums bus parodytas pranešimas „Darbas baigtas“. Šis pranešimas nurodo, kad pardavimo užsakymo darbo ID baigtas, o surinkimo viršijimo kiekis neviršija 10 procentų pristatymo perviršio ribos.
