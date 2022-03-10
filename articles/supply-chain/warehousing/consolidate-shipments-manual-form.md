---
title: Siuntų konsolidacija rankiniu būdu naudojant siuntų konsolidavimo puslapį
description: Šioje temoje pateikiamas scenarijus, kai į sandėlį išleidžiami keli užsakymai, o vėliau jie konsoliduojami naudojant puslapį Konsoliduoti siuntas.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 0da98b24b9e0ab1ae19fd353ec226b2e0ab008fe
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574214"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a>Siuntų konsolidacija rankiniu būdu naudojant siuntų konsolidavimo puslapį

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiamas scenarijus, kai į sandėlį išleidžiami keli užsakymai, o vėliau jie konsoliduojami naudojant puslapį **Konsoliduoti siuntas**.

## <a name="make-demo-data-available"></a>Leidimas naudoti demonstracinius duomenis

Šioje temoje esantis scenarijus nurodo reikšmes ir įrašus, įtrauktus į standartinius „Microsoft Dynamics 365 Supply Chain Management” demonstracinius duomenis. Jei norite naudoti čia pateiktas reikšmes atlikdami pratimus, įsitikinkite, kad dirbate aplinkoje, kurioje įdiegti demonstraciniai duomenys, ir prieš pradėdami nustatykite juridinį subjektą į **USMF**.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Siuntos konsolidacijos strategijų ir produktų filtrų nustatymas

Čia aprašytame scenarijuje laikoma, kad jūs jau įjungėte funkciją, atlikote pratimus, esančius [Siuntos konsolidacijos strategijų konfigūravimas](configure-shipment-consolidation-policies.md), ir sukūrėte ten aprašytas strategijas ir kitus įrašus. Nepamirškite atlikti šių pratimų prieš tęsdami darbą su šiuo scenarijumi.

## <a name="create-the-sales-orders-for-this-scenario"></a>Šio scenarijaus pardavimo užsakymų kūrimas

Pirmiausia sukurkite pardavimo užsakymų, su kuriais galite dirbti, rinkinį. Turite dirbti su sandėliu, kuris parengtas naudoti išplėstiniuose sandėlio (WMS) procesuose. Jeigu nėra aiškiai nurodyto kito sandėlio, kiekviename iš tolesnių užsakymų rinkinių reikia naudoti tą patį sandėlį.

Eikite į **Gautinos sumos \> Užsakymai \> Visi pardavimo užsakymai** ir sukurkite pardavimo užsakymų, kuriuose nustatyti tolesniuose poskirsniuose aprašyti parametrai, rinkinį.

### <a name="create-sales-orders-1-and-2"></a>1 ir 2 pardavimo užsakymų kūrimas

1. Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-007*
    - **Telkinys:** *ShipCons*

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*

1. Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.

### <a name="create-sales-orders-3-and-4"></a>3 ir 4 pardavimo užsakymų kūrimas

1. Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-007*
    - **Telkinys:** šį lauką palikite tuščią.

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*

1. Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.

## <a name="release-the-orders-to-the-warehouse"></a>Užsakymų išleidimas į sandėlį

Atlikite tolesnius veiksmus, kad išleistumėte kiekvieną šiame scenarijuje sukurtą pardavimo užsakymą į sandėlį.

1. Eikite į **Gautinos sumos \> Užsakymai \> Visi pardavimo užsakymai**.
1. Raskite ir pasirinkite pardavimo užsakymą, kurį norite išleisti.
1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Veiksmai \> Išleisti į sandėlį**, kad būtų išleistas pasirinktas pardavimo užsakymas.
1. Kartokite šią procedūrą kiekvienam kitam šiame scenarijuje sukurtam pardavimo užsakymui.

## <a name="consolidate-shipments"></a>Konsoliduoti siuntas

1. Eikite į **Sandėlio valdymas \> Siuntos \> Visos siuntos**.
1. Raskite ir pasirinkite siuntą, sukurtą, kai į sandėlį buvo išleistas 1 pardavimo užsakymas. (Jos laukas **Siuntos konsolidacijos strategija** turėtų būti nustatytas į *Užsakymų telkinys*.)
1. Veiksmų srities skirtuke **Siuntos** pasirinkite **Siuntos \> Konsoliduoti siuntas**.
1. Patikrinkite siuntas, kurias siūloma konsoliduoti. Konsolidavimui turi būti siūloma tik viena siunta, turinti tą pačią strategiją.
1. Puslapį **Siuntos konsolidacija** uždarykite.
1. Raskite ir pasirinkite siuntą, sukurtą, kai į sandėlį buvo išleistas 3 pardavimo užsakymas. (Jos laukas **Siuntos konsolidacijos strategija** turėtų būti nustatytas į *Numatytoji*.)
1. Veiksmų srities skirtuke **Siuntos** pasirinkite **Siuntos \> Konsoliduoti siuntas**.
1. Patikrinkite, ar nėra siūlomų konsoliduoti siuntų.
1. Pasirinkite **Rodyti filtrus**.
1. Srityje **Filtrai** pašalinkite filtrą **Užsakymo numeris** ir pasirinkite **Taikyti**.
1. Patikrinkite siuntas, kurias siūloma konsoliduoti. Konsolidavimui turi būti siūloma tik viena siunta, turinti tą pačią strategiją.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Siuntos konsolidacijos strategijos](about-shipment-consolidation-policies.md)
- [Siuntos konsolidacijos strategijų konfigūravimas](configure-shipment-consolidation-policies.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]