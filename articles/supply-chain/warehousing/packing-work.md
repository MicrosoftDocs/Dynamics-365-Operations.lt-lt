---
title: Siunčiamų konteinerių pakavimo ir siuntų apdorojimo darbas
description: Šiame straipsnyje aprašomas darbo užsakymo tipas Pakavimas, kuris valdo konteinerių pakavimo darbą ir palaiko dalinius supakuotų konteinerių, susijusių su kroviniais, kur lieka išpakuotos atsargų prekės, siuntas.
author: perlynne
ms.date: 7/13/2022
ms.topic: article
ms.search.form: WHSPackingWorkLocationSetup, WHSPack, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 34a7087df7e7768d0012ea4f534aa109654af8fa
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220759"
---
# <a name="packing-work-for-packing-outbound-containers-and-processing-shipments"></a>Siunčiamų konteinerių pakavimo ir siuntų apdorojimo darbas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašomas *darbo* užsakymo pakavimo užsakymo tipas, kuris valdo konteinerių pakavimo darbą ir palaiko dalinius supakuotų konteinerių, susijusių su kroviniais, kur lieka išpakuotos atsargų prekės, siuntas. Pakavimo darbas leidžia naudoti patvirtinimo [ir perkėlimo funkciją](confirm-and-transfer.md) siunčiamoms siuntoms, susijusioms su konteineriais, patvirtinti.

Pakavimo darbas sukuriamas automatiškai, kai atsargos, susijusios su šaltinio dokumento darbu, įvedamos į pakavimo *vietos tipo* vietas. Darbą sudaro dvi eilutės: *·* *paėmimo* ir kitos – padėti, ir jis automatiškai tvarkomas kaip konteinerio uždarymo / pakartotinio atidarymo proceso dalis.

Daugiau informacijos apie tai, kaip nustatyti ir naudoti konteinerio pakavimo procesą, ieškokite siuntimo konteinerių [paketais](packing-containers.md).

## <a name="turn-on-the-feature"></a>Funkcijos įjungimas

Jei jūsų sistema dar neturi funkcijų, aprašytų šiame straipsnyje, [eikite į Funkcijų](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) valdymą ir toliau pateikiama tvarka įjunkite šias funkcijas. Abi priemonės yra sandėlio **valdymo modulio** dalis.

1. *Tvirtinimas ir perkėlimas*
1. *Pakavimo vietų pakavimo darbas*

## <a name="set-up-a-location-for-packing-work"></a>Nustatyti pakavimo darbo vietą

Norėdami nustatyti pakavimo vietas, naudokite nurodytą procedūrą. Galima pasirinkti, ar kiekvienai vietai sistema automatiškai sukurs pakavimo darbą.

1. Eiti į sandėlio **valdymo nustatymą \>\> Pakavimo \> pakavimo stoties nustatymas**.
1. Veiksmų srityje pasirinkite Naujas, kad įtraukumėte **pakavimo** stoties nustatymo įrašą.
1. Naujame įraše nustatykite šiuos laukus:

    - **Sandėlis** – pasirinkite arba įveskite sandėlį, kuriame yra pakavimo vieta.
    - **Vieta** – pasirinkite arba įveskite pakavimo vietą. Ši vieta turi būti priskirta vietos **šablonui, kuris naudoja vietos tipą, kuris sandėlio valdymo parametrų puslapyje sukonfigūruotas kaip jūsų įmonės pakavimo vietos** tipas. Daugiau informacijos rasite siuntimo konteinerių [paketais](packing-containers.md).
    - **Kurti pakavimo** darbą – pažymėkite šį žymės langelį, jei norite kurti pakavimo darbą kiekvieną kartą, kai prekės pristatomos į pakavimo vietą. Darbas apims saitus į susijusias krovinio eilutes, kad būtų galima supakuoti ir išsiųsti dalinius krovinius.

## <a name="example-scenario"></a>Pavyzdinis scenarijus

Šis pavyzdinis scenarijus rodo, kaip apdoroti siunčiamų pardavimo užsakymų srautą pakuojant konteinerį ir išsiųsti dalinį krovinį.

### <a name="make-sample-data-available"></a>Įgalinkite duomenų pavyzdį

Norėdami dirbti pagal šį scenarijų, naudojant nurodytus įrašų ir reikšmių pavyzdžius, standartiniai [demonstraciniai duomenys](../../fin-ops-core/fin-ops/get-started/demo-data.md) turi būti įdiegti Jūsų sistemoje. Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.

Kaip gamybos sistemos priemonę galite naudoti šį scenarijų kaip nurodymus. Nepaisant to, tokiu atveju, turėsite pakeisti savo vertes kiekvienam šiame dokumente aprašytam nustatymui.

### <a name="configure-packing-work-for-warehouse-packing-location"></a>Konfigūruoti sandėlio pakavimo vietos pakavimo darbą

Norėdami pradėti, turite sukonfigūruoti konkretaus *sandėlio* ir vietos pakavimo darbo procesą.

1. Eiti į sandėlio **valdymo nustatymą \>\> Pakavimo \> pakavimo stoties nustatymas**.
1. Veiksmų srityje pasirinkite Naujas, kad **įtraukumėte** nustatymo įrašą.
1. Naujame įraše nustatykite šias vertes:

    - **Sandėlis:** *62*
    - **Vieta:** *Pakavimas*
    - **Kurti pakavimo darbą:** *Taip*

1. Uždarykite **pakavimo stoties nustatymo** puslapį.

### <a name="create-a-load-template-that-allows-partial-shipping"></a>Kurti krovinio šabloną, leidžiaį dalinį siuntimą

Norėdami įgalinti krovinį pristatyti per kelias siuntas, turite susieti jį su krovinio šablonu, leidžiaiu atlikti dalinį siuntimą. Norėdami sukurti reikiamą šabloną, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Krovinys \> Krovinio šablonai**.
1. Veiksmų srityje pasirinkite Naujas, kad **įtraukumėte** nustatymo įrašą.
1. Naujame įraše nustatykite šias vertes:

    - **Krovinio šablono ID: dalinis** *·*
    - **Leisti skaidyti krovinį patvirtinant siuntą:** *Taip*

1. Uždarykite krovinio **šablonų** puslapį.

Daugiau informacijos ieškokite Confirm [ir transfer](Confirm-and-transfer.md).

### <a name="process-a-sales-order"></a>Pardavimo užsakymo procesas

Norėdami apdoroti pardavimo užsakymą ir iš dalies jį išsiųsti, atlikite šiuos veiksmus.

1. Atlikite [pavyzdį scenarijų](packing-containers.md#scenario), kuris pateikiamas siuntimo [konteinerių paketais](packing-containers.md). Tokiu atveju, jūs sukursite dviejų prekės dalių pardavimo užsakymą. Tada į konteinerį pakuojami tik vienas iš vienetų ir uždarysite konteinerį. Turite pažymėti savo sukurtą siuntos ID, kaip nurodyta scenarijuje.
1. Pasirinkite **Sandėlio valdymas \> Darbas \> Visi darbai**.
1. Filtro srityje pažymėkite žymės langelį Rodyti **uždarytą** darbą. Tada į lauką Filtras įveskite siuntos **ID** ir pasirinkite filtruoti pagal siuntos **ID** vertę. Dabar turėtumėte matyti tris darbo antraštes. Jis skirtas pardavimo užsakymo paėmimo darbui, jo būsena yra *Uždaryta*. Dvi prekės yra pakavimo procesui: *viena* susijusi su uždarytu konteineriu, jos būsena yra Uždaryta, o kita – su išpakuota likusia preke ir jos būsena yra *Atidaryta*.
1. Norėdami atidaryti **krovinio informacijos puslapį, pasirinkite bet kurios darbo** antraštės **krovinio ID** vertę.
1. Perjunkite **Antraštės** rodinį.
1. Bendrajame **"** FastTab" pasirinkite mygtuką **Redaguoti**, kuris bus skirtas laukui **Krovinio šablono ID**. Tada pasirinkite dalinio siuntimo krovinio šabloną, kurį sukūrėte šiam scenarijui (Dalinis *·*).
1. Veiksmų srities skirtuko Siuntimas **ir gauti grupėje** Patvirtinti **pasirinkite** Siunčiama **siunta**.
1. Dialogo lange **Siuntimo patvirtinimas** pasirinkite parinktį Skaidyti **kiekį į naują krovinį**.
1. Pasirinkite **Gerai**.

Dabar siuntėte vieną konteinerį, susijusį su pradiniu kroviniu, o sistema sukūrė naują likusių prekių, kurias vis dar reikia supakuoti konteineryje, krovinį.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
