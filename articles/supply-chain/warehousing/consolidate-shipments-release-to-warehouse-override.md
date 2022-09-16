---
title: Siuntų konsolidacija, kai siuntos konsolidavimo strategija yra perrašyta
description: Šiame straipsnyje pateikite scenarijų, kuriame viena ar daugiau pardavimo eilučių turi būti rankiniu būdu išleistos į sandėlį iš puslapio Išleisti į sandėlį, o sistemos nustatytos siuntos konsolidavimo strategijos turi būti nepaisoma prieš išleidžiant.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: e2c4fed880c423790b979f27511d8d5697bd244c
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427961"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden"></a>Siuntų konsolidacija, kai siuntos konsolidavimo strategija yra perrašyta

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikite **scenarijų**, kuriame viena ar daugiau pardavimo eilučių turi būti rankiniu būdu išleistos į sandėlį iš puslapio Išleisti į sandėlį, o sistemos nustatytos siuntos konsolidavimo strategijos turi būti nepaisoma prieš išleidžiant. Gali reikėti perrašyti siuntos konsolidacijos strategiją, jei, pvz., užsakymas, kuris paprastai nėra konsoliduojamas su atviromis siuntomis, turi būti konsoliduojamas su atviromis siuntomis.

Scenarijaus metu sukursite pardavimo užsakymų rinkinį, o tada perrašysite numatytąją siuntos konsolidacijos strategiją prieš užsakymų išleidimą į sandėlį.

## <a name="make-demo-data-available"></a>Demonstracinių duomenų įgalinimas

Scenarijus šiame straipsnyje nurodo vertes ir įrašus, kurie yra įtraukti į standartinius demonstracinius duomenis, kurie pateikiami "Microsoft"Dynamics 365 Supply Chain Management. Jei norite naudoti čia pateiktas reikšmes atlikdami pratimus, įsitikinkite, kad dirbate aplinkoje, kurioje įdiegti demonstraciniai duomenys, ir prieš pradėdami nustatykite juridinį subjektą į **USMF**.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Siuntos konsolidacijos strategijų ir produktų filtrų nustatymas

Čia aprašytame scenarijuje laikoma, kad jūs jau įjungėte funkciją, atlikote pratimus, esančius [Siuntos konsolidacijos strategijų konfigūravimas](configure-shipment-consolidation-policies.md), ir sukūrėte ten aprašytas strategijas ir kitus įrašus. Nepamirškite atlikti šių pratimų prieš tęsdami darbą su šiuo scenarijumi.

## <a name="create-the-sales-orders-for-this-scenario"></a>Šio scenarijaus pardavimo užsakymų kūrimas

1. Eikite į **Gautinos sumos \> Užsakymai \> Visi pardavimo užsakymai** ir sukurkite tris vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-002*

1. Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.

    - **Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)
    - **Kiekis:** *1.00*

1. Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a>Pardavimo užsakymų išleidimas iš puslapio Išleisti į sandėlį

Atlikite tolesnius veiksmus, norėdami perrašyti siuntos konsolidacijos strategiją išleidimo į sandėlį metu.

1. Eikite į **Sandėlio valdymas \> Išleidimas į sandėlį \> Išleidimas į sandėlį**.
1. Viršutinėje srityje pasirinkite pirmąjį šiame scenarijuje sukurtą pardavimo užsakymą.
1. Pasirinkite **Įtraukti**, kad įtrauktumėte eilutę į išleidimą į sandėlį. Atkreipkite dėmesį, kad *numatytoji* siuntos konsolidacijos strategija taikoma apatinėje srityje.
1. Apatinėje srityje pasirinkite **Pasirinkti naują siuntos konsolidacijos strategiją**.
1. Pasirinkite strategiją, leidžiančią konsoliduoti su kitomis tos pačios strategijos atidarytomis siuntomis. Pavyzdžiui, pasirinkite strategiją *CustomerOrderNo*.
1. Pasirinkite **Išleisti į sandėlį**.
1. Pasirinkite antrąjį ir trečiąjį šiame scenarijuje sukurtus pardavimo užsakymus.
1. Pasirinkite **Įtraukti**, kad įtrauktumėte eilutes į išleidimą į sandėlį. Atkreipkite dėmesį, kad *numatytoji* strategija taikoma apatinėje srityje.
1. Pasirinkite antrą eilutę, tada lauke **Pasirinkti naują siuntos konsolidacijos strategiją** pasirinkite strategiją *CustomerOrderNo*.
1. Abiejose eilutėse pasirinkite **Išleisti į sandėlį**.

## <a name="verify-the-shipments"></a>Siuntų tikrinimas

Turėtų būti sukurtos dvi siuntos.

- Pirmoje siuntoje yra dvi eilutės ir ji buvo sukurta naudojant *CustomerOrderNo* siuntos konsolidacijos strategiją.
- Antroje siuntoje yra viena eilutė ir siunta buvo sukurta naudojant *numatytąją* siuntos konsolidacijos strategiją.

Atlikite tolesnius veiksmus, norėdami peržiūrėti sukurtas siuntas.

1. Eikite į **Sandėlio valdymas \> Siuntos \> Visos siuntos**.
1. Raskite ir pasirinkite reikiamą siuntą.
1. Lauke **Siuntos konsolidacijos strategija** peržiūrėkite konsolidacijos strategiją, kuri buvo naudojama kuriant siuntą.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Siuntos konsolidavimo strategijų peržiūra](about-shipment-consolidation-policies.md)
- [Siuntos konsolidacijos strategijų konfigūravimas](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]