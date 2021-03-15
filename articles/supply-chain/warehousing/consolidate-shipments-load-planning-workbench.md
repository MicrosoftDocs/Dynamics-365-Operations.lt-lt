---
title: Siuntų konsolidacija naudojant išleidimo į sandėlį funkciją krovinio planavimo darbo srityje
description: Šioje temoje pateikiamas scenarijus, kai į sandėlį išleidžiami keli to paties krovinio užsakymai, o tada jie automatiškai konsoliduojami į siuntas.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: c0af6764742532cbe181c8a20e7bf783b0e6d7cf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983097"
---
# <a name="consolidate-shipments-by-using-release-to-warehouse-from-the-load-planning-workbench"></a>Siuntų konsolidacija naudojant išleidimo į sandėlį funkciją krovinio planavimo darbo srityje

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiamas scenarijus, kai į sandėlį išleidžiami keli to paties krovinio užsakymai, o tada jie automatiškai konsoliduojami į siuntas.

## <a name="make-demo-data-available"></a>Leidimas naudoti demonstracinius duomenis

Šioje temoje esantis scenarijus nurodo reikšmes ir įrašus, įtrauktus į standartinius „Microsoft Dynamics 365 Supply Chain Management” demonstracinius duomenis. Jei norite naudoti čia pateiktas reikšmes atlikdami pratimus, įsitikinkite, kad dirbate aplinkoje, kurioje įdiegti demonstraciniai duomenys, ir prieš pradėdami nustatykite juridinį subjektą į **USMF**.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Siuntos konsolidacijos strategijų ir produktų filtrų nustatymas

Čia aprašytame scenarijuje laikoma, kad jūs jau įjungėte funkciją, atlikote pratimus, esančius [Siuntos konsolidacijos strategijų konfigūravimas](configure-shipment-consolidation-policies.md), ir sukūrėte ten aprašytas strategijas ir kitus įrašus. Nepamirškite atlikti šių pratimų prieš tęsdami darbą su šiuo scenarijumi.

## <a name="create-the-sales-orders-for-this-scenario"></a>Šio scenarijaus pardavimo užsakymų kūrimas

Pirmiausia sukurkite pardavimo užsakymų, su kuriais galite dirbti, rinkinį. Turite dirbti su sandėliu, kuris parengtas naudoti išplėstiniuose sandėlio (WMS) procesuose. Jeigu nėra aiškiai nurodyto kito sandėlio, kiekviename iš tolesnių užsakymų rinkinių reikia naudoti tą patį sandėlį.

Eikite į **Gautinos sumos \> Užsakymai \> Visi pardavimo užsakymai** ir sukurkite pardavimo užsakymų, kuriuose nustatyti tolesniuose poskirsniuose aprašyti parametrai, rinkinį.

### <a name="create-order-set-1"></a>1 užsakymų rinkinio kūrimas

#### <a name="sales-order-1-1"></a>1-1 pardavimo užsakymas

1. Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-001*
    - **Pristatymo būdas:** *Airwa-Air*

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*

1. Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.

#### <a name="sales-order-1-2"></a>1-2 pardavimo užsakymas

1. Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-001*
    - **Pristatymo būdas:** *Airwa-Air*

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*

1. Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.

#### <a name="sales-order-1-3"></a>1-3 pardavimo užsakymas

1. Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-001*
    - **Pristatymo būdas:** *10*

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*

1. Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.
1. Įtraukite antrą pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0002* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*
    - **Pristatymo būdas:** *Airwa-Air*

1. Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad būtų rezervuota antroji užsakymo eilutė.

### <a name="create-order-set-2"></a>2 užsakymų rinkinio kūrimas

#### <a name="sales-orders-2-1-and-2-2"></a>2-1 ir 2-2 pardavimo užsakymai

1. Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-002*

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *M9200* (prekė, kurios filtras **4 kodas** nustatytas į *Degus*)
    - **Kiekis:** *1.00*

1. Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.
1. Įtraukite antrą pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *M9201* (prekė, kurios filtras **4 kodas** nustatytas į *Sprogus*)
    - **Kiekis:** *1.00*
    - **Pristatymo būdas:** *Airwa-Air*

1. Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad būtų rezervuota antroji užsakymo eilutė.

### <a name="create-order-set-3"></a>3 užsakymų rinkinio kūrimas

#### <a name="sales-orders-3-1-and-3-2"></a>3-1 ir 3-2 pardavimo užsakymai

1. Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-001*
    - **Kliento paraiška:** *1*

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*

1. Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.

#### <a name="sales-orders-3-3-and-3-4"></a>3-3 ir 3-4 pardavimo užsakymai

1. Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-001*
    - **Kliento paraiška:** *2*

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*

1. Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.

### <a name="create-order-set-4"></a>4 užsakymų rinkinio kūrimas

#### <a name="sales-orders-4-1-and-4-2"></a>4-1 ir 4-2 pardavimo užsakymai

1. Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-003*

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*

1. Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.

#### <a name="sales-orders-4-3-and-4-4"></a>4-3 ir 4-4 pardavimo užsakymai

1. Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-004*

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*

1. Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.

#### <a name="sales-orders-4-5-and-4-6"></a>4-5 ir 4-6 pardavimo užsakymai

1. Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-007*
    - **Vieta:** *6*
    - **Sandėlis:** *61*
    - **Telkinys:** *ShipCons*

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*

1. Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.

#### <a name="sales-orders-4-7-and-4-8"></a>4-7 ir 4-8 pardavimo užsakymai

1. Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-007*
    - **Vieta:** *6*
    - **Sandėlis:** *61*
    - **Telkinys:** šį lauką palikite tuščią.

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*

1. Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a>Krovinio planavimo darbo srities naudojimas kroviniams kurti ir paleisti į sandėlį

Atlikite tolesnius veiksmus, kad sukurtumėte krovinį kiekvienam šiame scenarijuje sukurtam užsakymų rinkiniui ir išleistumėte į sandėlį.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Krovinio planavimo darbo sritis**.
1. Skirtuke **Pardavimo eilutės** raskite ir pasirinkite visas vieno iš sukurtų užsakymų rinkinių, sukurtų šiame scenarijuje, pardavimo užsakymo eilutes.
1. Veiksmų srities skirtuke **Pasiūla ir paklausa** pasirinkite **Įtraukti \> Į naują krovinį**, kad įtrauktumėte pasirinktas užsakymo eilutes į naują krovinį.
1. Dialogo lango **Krovinio šablono priskyrimas** lauke **Krovinio šablono ID** pasirinkite krovinio šabloną, pvz., *Stnd krovinio šablonas*.
1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą. 
1. Dalyje **Kroviniai** raskite ir pasirinkite ką tik sukurtą krovinį.
1. Pasirinkite **Išleidimas \> Išleidimas į sandėlį**, kad išleistumėte pasirinktą krovinį į sandėlį.
1. Kartokite šią procedūrą trims kitiems šiame scenarijuje sukurtiems užsakymų rinkiniams.

## <a name="verify-the-shipments"></a>Siuntų tikrinimas

Tolesnė procedūra leidžia tikrinti siuntas, sukurtas arba atnaujintas dėl siuntos konsolidacijos. Naudokite ją, norėdami peržiūrėti kiekvieną užsakymą, kurį sukūrėte šiam scenarijui, ir tada peržiūrėkite tolesnius poskyrius, kad įsitikintumėte, jog gavote numatytus rezultatus.

1. Eikite į **Sandėlio valdymas \> Siuntos \> Visos siuntos**.
1. Raskite ir pasirinkite reikiamą siuntą.
1. Jei kuriant ar naujinant siuntą buvo naudojama konsolidacijos strategija, turėtumėte ją matyti lauke **Siuntos konsolidacijos strategija**.

### <a name="release-order-set-1-in-one-load"></a>1 užsakymų rinkinio išleidimas viename krovinyje

Turėtų būti sukurtos dvi siuntos.

- Pirmoje siuntoje yra trys eilutės ir ji buvo sukurta naudojant *CustomerMode* siuntos konsolidacijos strategiją.
- Antroji siunta, nenaudojanti pristatymo transportavimo būdo *Oro keliai*, buvo sukurta naudojant *CustomerOrderNo* siuntos konsolidacijos strategiją.

### <a name="release-order-set-2-in-one-load"></a>2 užsakymų rinkinio išleidimas viename krovinyje

Turėtų būti sukurtos trys siuntos.

- Pirmojoje siuntoje yra *degių* prekių.
- Kiekvienoje iš kitų dviejų siuntų yra viena eilutė, turinti *sprogią* prekę.

### <a name="release-order-set-3-in-one-load"></a>3 užsakymų rinkinio išleidimas viename krovinyje

Turėtų būti sukurtos dvi siuntos.

- Pirmoje siuntoje yra pardavimo užsakymo eilučių, kuriose laukas **Kliento paraiška** nustatytas į *1*.
- Antroje siuntoje yra pardavimo užsakymo eilučių, kuriose laukas **Kliento paraiška** nustatytas į *2*.

### <a name="release-order-set-4-in-one-load"></a>4 užsakymų rinkinio išleidimas viename krovinyje

Turėtų būti sukurtos keturios siuntos.

- Dviejų kliento sąskaitos *US-003* užsakymų eilutės buvo sugrupuotos į vieną siuntą naudojant siuntos konsolidacijos strategiją *Užsakymų telkinys*.
- Dviejų kliento sąskaitos *US-004* užsakymų eilutės buvo sugrupuotos į vieną siuntą naudojant siuntos konsolidacijos strategiją *Užsakymų telkinys*.
- Kliento sąskaitos *US-007* 4-5 ir 4-6 pardavimų užsakymų eilutės buvo sugrupuotos į vieną siuntą naudojant siuntos konsolidacijos strategiją *Užsakymų telkinys*.
- Kliento sąskaitos *US-007* 4-7 ir 4-8 pardavimų užsakymų eilutės buvo sugrupuotos į vieną siuntą naudojant *CrossOrder* siuntos konsolidacijos strategiją.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Siuntos konsolidacijos strategijos](about-shipment-consolidation-policies.md)
- [Siuntos konsolidacijos strategijų konfigūravimas](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]