---
title: Siuntų, išleistų į sandėlį naudojant automatinį pardavimo užsakymų išleidimą, konsolidacija
description: Šiame straipsnyje pateikiama scenarijų, kai į sandėlį išleidžiami keli užsakymai atliekant tą pačią periodinę išleidimo į sandėlį procedūrą.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 36eb5e788d0473e2fec2214e9aa7e245304347e3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875078"
---
# <a name="consolidate-shipments-released-to-the-warehouse-using-automatic-release-of-sales-orders"></a>Siuntų, išleistų į sandėlį naudojant automatinį pardavimo užsakymų išleidimą, konsolidacija

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama scenarijų, kai į sandėlį išleidžiami keli užsakymai atliekant tą pačią periodinę išleidimo į sandėlį procedūrą. Užsakymai bus automatiškai konsoliduoti į siuntas pagal taisykles, apibrėžiamas kaip siuntos konsolidacijos strategijos.

Scenarijaus metu sukursite pardavimo užsakymų rinkinius ir kiekvieną rinkinį išleisite į sandėlį. Tada galėsite peržiūrėti siuntas, sukurtas arba atnaujintas siuntos konsolidacijos metu pagal sukonfigūruotas strategijas.

## <a name="make-demo-data-available"></a>Demonstracinių duomenų įgalinimas

Scenarijus šiame straipsnyje nurodo vertes ir įrašus, kurie yra įtraukti į standartinius demonstracinius duomenis, kurie pateikiami "Microsoft"Dynamics 365 Supply Chain Management. Jei norite naudoti čia pateiktas reikšmes atlikdami pratimus, įsitikinkite, kad dirbate aplinkoje, kurioje įdiegti demonstraciniai duomenys, ir prieš pradėdami nustatykite juridinį subjektą į **USMF**.

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

#### <a name="sales-order-1-2"></a>1-2 pardavimo užsakymas

1. Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-001*
    - **Pristatymo būdas:** *Airwa-Air*

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*

#### <a name="sales-order-1-3"></a>1-3 pardavimo užsakymas

1. Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-001*
    - **Pristatymo būdas:** *10*

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*

1. Įtraukite antrą pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0002* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*
    - **Pristatymo būdas:** *Airwa-Air*

### <a name="create-order-set-2"></a>2 užsakymų rinkinio kūrimas

#### <a name="sales-orders-2-1-and-2-2"></a>2-1 ir 2-2 pardavimo užsakymai

1. Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-002*

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *M9200* (prekė, kurios filtras **4 kodas** nustatytas į *Degus*)
    - **Kiekis:** *1.00*

1. Įtraukite antrą pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *M9201* (prekė, kurios filtras **4 kodas** nustatytas į *Sprogus*)
    - **Kiekis:** *1.00*
    - **Pristatymo būdas:** *Airwa-Air*

### <a name="create-order-set-3"></a>3 užsakymų rinkinio kūrimas

#### <a name="sales-order-3-1"></a>3-1 pardavimo užsakymas

1. Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-002*

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *M9200* (prekė, kurios filtras **4 kodas** nustatytas į *Degus*)
    - **Kiekis:** *1.00*

1. Įtraukite antrą pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *M9201* (prekė, kurios filtras **4 kodas** nustatytas į *Sprogus*)
    - **Kiekis:** *1.00*
    - **Pristatymo būdas:** *Airwa-Air*

> [!NOTE]
> Šis užsakymas yra toks pat kaip du 2 užsakymų rinkinio užsakymai, kuriuos sukūrėte. Tačiau jis nurodytas kaip jo pačio užsakymų rinkinys, nes vėliau šiame scenarijuje jį išleisite atskirai.

### <a name="create-order-set-4"></a>4 užsakymų rinkinio kūrimas

#### <a name="sales-order-4-1"></a>4-1 pardavimo užsakymas

1. Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-001*
    - **Kliento paraiška:** *1*

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*

### <a name="create-order-set-5"></a>5 užsakymų rinkinio kūrimas

#### <a name="sales-orders-5-1-and-5-2"></a>5-1 ir 5-2 pardavimo užsakymai

1. Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-001*
    - **Kliento paraiška:** *2*

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*

#### <a name="sales-order-5-3"></a>5-3 pardavimo užsakymas

1. Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-001*
    - **Kliento paraiška:** *1*

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*

### <a name="create-order-set-6"></a>6 užsakymų rinkinio kūrimas

#### <a name="sales-orders-6-1-and-6-2"></a>6-1 ir 6-2 pardavimo užsakymai

1. Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-003*
    - **Kliento paraiška:** *2*

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*

#### <a name="sales-orders-6-3-and-6-4"></a>6-3 ir 6-4 pardavimo užsakymai

1. Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-004*
    - **Kliento paraiška:** *1*

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*

#### <a name="sales-orders-6-5-and-6-6"></a>6-5 ir 6-6 pardavimo užsakymai

1. Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-007*
    - **Vieta:** *6*
    - **Sandėlis:** *61*
    - **Telkinys:** *ShipCons*

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*

#### <a name="sales-orders-6-7-and-6-8"></a>6-7 ir 6-8 pardavimo užsakymai

1. Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-007*
    - **Vieta:** *6*
    - **Sandėlis:** *61*
    - **Telkinys:** šį lauką palikite tuščią.

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a>Automatinis pardavimo užsakymų išleidimas į sandėlį

Kiekvienam anksčiau sukurtam pardavimo užsakymų rinkiniui atliksite automatinio išleidimo į sandėlį procedūrą. Kiekvienu atveju dirbsite pagal čia pateiktą [pagrindinę išleidimo į sandėlį procedūrą](#release-procedure).

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a>Pagrindinė išleidimo į sandėlį procedūra

Kiekvienam anksčiau sukurtam pardavimo užsakymų rinkiniui atliksite tris procedūras, aprašytas tolesniuose poskirsniuose.

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a>Bangos šablono, kuris bus naudojamas išleidimo metu, naujinimas

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.
1. Nustatykite lauką **Bangos šablono tipas** į *Siuntimo*.
1. Raskite ir pasirinkite bangos šabloną, susietą su sandėliu, kurį naudojote šio scenarijaus užsakymų rinkiniuose, kuriuos sukūrėte. Pavyzdžiui, jei naudojote *24* sandėlį, pasirinkite bangos šabloną **24 numatytoji siunta**. Jei naudojote *61* sandėlį, pasirinkite bangos šabloną **61 siunta**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Parinktį **Apdoroti bangą išleidžiant ją į sandėlį** nustatykite į *Ne*.

#### <a name="release-to-the-warehouse"></a>Išleidimas į sandėlį

1. Eikite į **Sandėlio valdymas \> Išleidimas į sandėlį \> Automatinis pardavimo užsakymų išleidimas**.
1. Nustatykite lauką **Išleistinas kiekis** į *Visi*.
1. „FastTab” **Įtrauktini įrašai** pasirinkite **Filtruoti**, kad būtų atidarytas užklausos dialogo langas.
1. Skirtuke **Diapazonas** pasirinkite **Įtraukti**, kad įtrauktumėte eilutę, kuriai nustatyti tolesni parametrai, į tinklelį.

    - **Lentelė:** *pardavimo užsakymas*
    - **Išvestinė lentelė:** *pardavimo užsakymas*
    - **Laukas:** *pardavimo užsakymas*
    - **Kriterijai:** įveskite kableliais atskirtų norimo užsakymo rinkinio pardavimo užsakymų numerių sąrašą.

1. Pasirinkite **Gerai**, kad užklausa būtų įrašyta.
1. Pasirinkite **Gerai**, kad pradėtumėte procedūrą *Automatinis išleidimas į sandėlį*.

#### <a name="review-the-shipment-that-is-created-or-updated"></a>Sukurtos arba atnaujintos siuntos peržiūra

1. Eikite į **Sandėlio valdymas \> Siuntos \> Visos siuntos**.
1. Raskite ir pasirinkite reikiamą siuntą.
1. Jei kuriant ar naujinant siuntą buvo naudojama konsolidacijos strategija, turėtumėte ją matyti lauke **Siuntos konsolidacijos strategija**.

### <a name="release-sales-orders-from-order-set-1"></a>1 užsakymų rinkinio pardavimo užsakymų išleidimas

Sekite [pagrindinę išleidimo į sandėlį procedūrą](#release-procedure), kad išleistumėte 1 užsakymų rinkinio pardavimo užsakymus.

Baigę turėtumėte matyti, kad buvo sukurtos dvi siuntos.

- Pirmoje siuntoje yra trys eilutės ir ji buvo sukurta naudojant *CustomerMode* siuntos konsolidacijos strategiją.
- Antroji siunta, nenaudojanti pristatymo transportavimo būdo *Oro keliai*, buvo sukurta naudojant *CustomerOrderNo* siuntos konsolidacijos strategiją.

### <a name="release-sales-orders-from-order-set-2"></a>2 užsakymų rinkinio pardavimo užsakymų išleidimas

Sekite [pagrindinę išleidimo į sandėlį procedūrą](#release-procedure), kad išleistumėte 2 užsakymų rinkinio pardavimo užsakymus.

Baigę turėtumėte matyti, kad buvo sukurtos trys siuntos.

- Pirmojoje siuntoje yra *degių* prekių.
- Kiekvienoje iš kitų dviejų siuntų yra viena eilutė, turinti *sprogią* prekę.

### <a name="release-sales-orders-from-order-set-3"></a>3 užsakymų rinkinio pardavimo užsakymų išleidimas

Sekite [pagrindinę išleidimo į sandėlį procedūrą](#release-procedure), kad išleistumėte 3 užsakymų rinkinio pardavimo užsakymus.

Baigę turėtumėte matyti, kad įvyko tolesni veiksmai.

- Buvo atnaujinta viena esama siunta (siunta, sukurta, kai 2 užsakymų rinkinys buvo išleistas į sandėlį). Buvo įtraukta eilutė, kurioje yra *degi* prekė.
- Buvo sukurta viena nauja siunta, kurioje yra *sprogi* prekė.

### <a name="release-sales-orders-from-order-set-4"></a>4 užsakymų rinkinio pardavimo užsakymų išleidimas

Sekite [pagrindinę išleidimo į sandėlį procedūrą](#release-procedure), kad išleistumėte 4 užsakymų rinkinio pardavimo užsakymus.

Baigę turėtumėte matyti, kad buvo atnaujinta viena esama siunta (kurioje laukas **Kliento paraiška** nustatytas į *1*). Į ją buvo įtraukta viena nauja eilutė.

### <a name="release-sales-orders-from-order-set-5"></a>5 užsakymų rinkinio pardavimo užsakymų išleidimas

Sekite [pagrindinę išleidimo į sandėlį procedūrą](#release-procedure), kad išleistumėte 5 užsakymų rinkinio pardavimo užsakymus.

Baigę turėtumėte matyti, kad įvyko tolesni veiksmai.

- Buvo atnaujinta viena esama siunta (kurioje laukas **Kliento paraiška** nustatytas į *1*). Į ją buvo įtraukta 5-3 pardavimo užsakymo (kuriame laukas **Kliento paraiška** nustatytas į *1*) eilutė.
- Buvo sukurta viena nauja siunta, kurioje 5-1 ir 5-2 pardavimo užsakymų eilutės sugrupuojamos į vieną siuntą.

### <a name="release-sales-orders-from-order-set-6"></a>6 užsakymų rinkinio pardavimo užsakymų išleidimas

Sekite [pagrindinę išleidimo į sandėlį procedūrą](#release-procedure), kad išleistumėte 6 užsakymų rinkinio pardavimo užsakymus.

Baigę turėtumėte matyti, kad buvo sukurtos keturios siuntos.

- Dviejų kliento *US-003* užsakymų eilutės buvo sugrupuotos į vieną siuntą naudojant siuntos konsolidacijos strategiją *Užsakymų telkinys*.
- Dviejų kliento *US-004* užsakymų eilutės buvo sugrupuotos į vieną siuntą naudojant siuntos konsolidacijos strategiją *Užsakymų telkinys*.
- Kliento *US-007* 6-5 ir 6-6 pardavimų užsakymų eilutės buvo sugrupuotos į vieną siuntą naudojant siuntos konsolidacijos strategiją *Užsakymų telkinys*.
- Kliento *US-007* 6-7 ir 6-8 pardavimų užsakymų eilutės buvo sugrupuotos į vieną siuntą naudojant *CrossOrder* siuntos konsolidacijos strategiją.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Siuntos konsolidacijos strategijos](about-shipment-consolidation-policies.md)
- [Siuntos konsolidacijos strategijų konfigūravimas](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]