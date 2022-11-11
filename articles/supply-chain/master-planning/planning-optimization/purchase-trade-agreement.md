---
title: Bendrasis planavimas su įsigijimo prekybos sutartimis
description: Šiame straipsnyje aprašoma, kaip pagal geriausią kainą arba gamybos laiką, rastų pirkimo prekybos sutartyse, galima rasti suplanuoto užsakymo tiekėjo ir (arba) gamybos laiką.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c36827738b13d5ca71da910d32e8877c1a408f62
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740991"
---
# <a name="master-planning-with-purchase-trade-agreements"></a>Bendrasis planavimas su įsigijimo prekybos sutartimis

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip pagal geriausią kainą arba gamybos laiką, kuris randamas tarp visų pirkimo prekybos sutarčių, nurodytų nurodytam produktui, galima rasti suplanuoto užsakymo tiekėją ir (arba) gamybos laiką.

## <a name="turn-the-purchase-trade-agreements-for-planning-optimization-feature-on-or-off"></a>Įjungti arba išjungti planavimo optimizavimo funkcijos pirkimo prekybos sutartis

Jei norite naudoti šią funkciją, ją turite įjungti savo sistemoje. Kaip ir tiekimo grandinės valdymo versija 10.0.29, ši funkcija yra privaloma ir jos išjungti negalima. Jei naudojate senesnę nei 10.0.29 versiją, *·*[tada](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) administratoriai gali įjungti arba išjungti šią funkciją ieškodami pirkimo prekybos sutarčių planavimo optimizavimo funkcijos funkcijų valdymo darbo srityje.

## <a name="prepare-your-system-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Paruoškite savo sistemą, kad galėtumėte įvertinti pirkimo prekybos sutartis bendrojo planavimo metu

Norėdami konfigūruoti savo sistemą, kad ji tai jau būtų taikoma pirkimo prekybos sutartims vertinti, atlikite šiuos veiksmus.

1. Eikite į **Bendrasis planavimas \> Sąranka \> Bendrojo planavimo parametrai**. Skirtuko **Suplanuoti užsakymai** dalyje **Tiekėjas** nustatykite šias vertes:

    - **Rasti prekybos sutartį** – nustatykite šią parinktį į **Taip**, kad įterptumėte pirkimo prekybos sutartis į bendrąjį planavimą.
    - **Ieškos kriterijus** – pasirinkite veiksnį, kuriam norite teikti pirmenybę kiekvienai pirkimo prekybos sutarčiai: **Trumpiausias gamybos laikas** arba **Mažiausia vieneto kaina**.

1. Eikite į **Įsigijimas ir šaltinio pasirinkimas \> Sąranka \> Kainos ir nuolaidos \> Aktyvinti kainą / nuolaidą** ir įsitikinkite, kad **Tiekėjo** parinktis nustatyta į **Taip**.
1. Eikite į **Produktų informacijos valdymas \> Sąranka \> Dimensijų ir variantų grupės \> Saugojimo dimensijų grupės** ir pasirinkite saugojimo dimensijų grupę, taikomą produktams, kuriuos bendrojo planavimo metu reikia vertinti pirkimo prekybos sutartims. Įsitikinkite, kad kiekviena reikiama šios grupės saugojimo dimensija pažymėtas varnele stulpelyje **Pirkimo kainos**. Pakartokite šį veiksmą su kiekviena atitinkama saugojimo dimensijų grupe.

## <a name="prepare-a-released-product-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Paruoškite išleistą produktą, kad galėtumėte įvertinti pirkimo prekybos sutartis bendrojo planavimo metu

Kai jūsų sistema bus parengta, kaip aprašyta ankstesniame skyriuje, atlikite šiuos veiksmus, kad įsitikintumėte, jog kiekvienas produktas, kurį norite naudoti su šia funkcija, nustatytas tinkamai.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai** ir atidarykite tikslinį produktą.
1. „FastTab“ skirtuke **Pirkimas** įsitikinkite, kad lauke **Tiekėjas** nepriskirtas joks tiekėjas.
1. Veiksmų srities skirtuko **Planas** grupėje **Padengimas** pasirinkite **Prekės padengimas**, kad pasirinktam produktui būtų atidarytas puslapis **Prekės padengimas**. Patikrinkite šiuos parametrus:

    - Skirtuke **Bendra** nustatyti tiekėjo perrašymus. Jei norite, kad bendrasis planavimas pasirinktų tiekėją pagal pirkimo prekybos sutartis, turėtumėte uždrausti tiekėjų nepaisymus **išvalydami žymės langelį Naudoti konkretų** parametrą.
    - Skirtuke **Gamybos laikas** galite nustatyti gamybos laiko perrašymą. Jei norite, kad bendrojo planavimo metu būtų naudojamas pirkimo prekybos sutarčių vykdymo laikas, turėtumėte uždrausti nepaisyti gamybos laiko. Išvalykite kiekvieno gamybos laiko tipo, kurį norite pasirinkti naudodami pirkimo prekybos sutartis (**Pirkimas**, **Gamyba** ir (arba) **Perkėlimas**), žymės langelį.

1. Norėdami grįžti į pasirinkto produkto informacijos puslapį, uždarykite puslapį **Prekės padengimas**.
1. Veiksmų srities skirtuko **Planas** grupėje **Prognozė**, pasirinkite **Tiekimo prognozė**, kad būtų atidarytas puslapis **Tiekimo prognozė**. Įsitikinkite, kad čia nėra rodomos eilutės, kurios reikšmė stulpelyje yra **Tiekėjo paskyra**.
1. Norėdami grįžti į pasirinkto produkto informacijos puslapį, uždarykite puslapį **Tiekimo prognozė**.
1. Veiksmų srityje, skirtuke **Pirkimas**, grupėje **Prekybos sutartys**, pasirinkite **Rodyti prekybos sutartis**. Įsitikinkite, kad įtrauktos visos atitinkamos pirkimo prekybos sutartys. Taip pat įsitikinkite, **kad pasirinktis** **Nepaisyti** gamybos laiko yra nustatyta kaip Ne kiekvienoje sutartyje, kurioje norite, kad bendrasis planavimas naudos gamybos laiką, kuris nurodytas tai sutartyje.
1. Veiksmų srities skirtuko **Planas** grupėje **Užsakymo parametrai** pasirinkite **Numatytieji užsakymo parametrai**, kad pasirinktam produktui būtų atidarytas puslapis **Numatytieji užsakymo parametrai**. „FastTab“ skirtuke **Pirkimo užsakymas** peržiūrėkite lauko **Pirkimo gamybos laikas** reikšmę. Jei prekės padengimo gamybos laiko nepaisymo nepaisymo atveju, bendrasis planavimas naudos šią vertę, kai pasirinks prekybos sutartis, kuriose nustatyta parinktis **Nepaisyti** gamybos laiko kaip **Taip**. Todėl reikia pakoreguoti šią reikšmę pagal savo poreikius.
1. Šią procedūrą kartokite nustatydami kiekvieną atitinkamą produktą.

> [!NOTE]
> Bendrasis planavimas palaiko kelių valiutų pirkimo prekybos sutartis. Kai ieškote prekybos sutarties naudodami parinktį Žemiausia vieneto kaina, sistema nagrinės galimybę įsigyti prekybos sutarties eilutes su skirtingomis valiutomis, pateiktame valiutos kursą tarp prekybos sutarties eilutės valiutos ir juridinio subjekto apskaitos **valiutos**. Kitu atveju prekybos sutarties eilutės bus nepaisoma, o jūs matysite klaidą bendrojo planavimo metu. Todėl į bendrąjį planavimą bus įtraukta informacija iš visų atitinkamų pirkimo prekybos sutarties eilučių, kuriose kainos gali būti konvertuojamos į apskaitos valiutą. Svarbu pažymėti, kad konvertavimo į apvalinimo taisykles nebus atsižvelgiama prekybos sutarties eilutės kainų konvertavimo metu.

## <a name="examples-of-how-master-planning-finds-vendor-and-lead-times"></a>Pavyzdžiai, kaip bendrasis planavimas suranda tiekėjų ir gamybos laiką

Tolesnėje lentelėje pateikiami pavyzdžiai, kurie rodo, kaip įvairūs išleistų produktų parametrai ir su jais susijusios pirkimo prekybos sutartys lemia sukurto suplanuoto pirkimo užsakymo reikšmes. Dviejų **dešiniųjų** stulpelių paryškintos vertės yra vertės, kurias pasirinkote bendrojo planavimo metu. Kituose stulpeliuose esančios **_paryškintos ir pasviros_** reikšmės yra parametrai, pagal kuriuos buvo sudarytos kiekvienos eilutės reikšmės.

| Išleistas produktas: tiekėjas | Numatytieji užsakymo parametrai: gamybos laikas | Prekės padengimas: nepaisyti tiekėjo | Prekės padengimas: nepaisyti gamybos laiko | Prekybos sutartis: tiekėjas | Prekybos sutartis: gamybos laikas | Prekybos sutartis: nepaisyti gamybos laiko | Gautas tiekėjas | Gautas gamybos laikas |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ***„US001”** _ | _*_„1”_*_ | Ne | Ne | US003 | 3 | Ne | _ *„US001”** | **1** |
| US001 | 1 | ***Taip: US002** _ | _*_Taip: 2_*_ | US003 | 3 | Ne | _ *„US002”** | **2** |
| *(tuščia)* | 1 | Ne | Ne | ***„US003”** _ | _*_„3”_*_ | Ne | _ *„US003”** | **3** |
| *(tuščia)* | ***„1”** _ | Ne | Ne | _*_„US003”_*_ | 3 | Taip | _ *„US003”** | **1** |
| *(tuščia)* | ***„1”** _ | _*_Taip: US002_*_ | Ne | US003 | 3 | Ne | _ *„US002”** | **1** |
| *(tuščia)* | ***„1”** _ | _*_Taip: US002_*_ | Ne | US003 | 3 | Ne | _ *„US002”** | **1** |
| *(tuščia)* | 1 | Ne | Taip: 2 | ***„US003”** _ | _*_„3”_*_ | Ne | _ *„US003”** | **3** |
| *(tuščia)* | 1 | Ne | ***Taip: 2** _ | _*_„US003”_*_ | 3 | Taip | _ *„US003”** | **2** |

## <a name="additional-resources"></a>Papildomi ištekliai

- [Pirkimo sutartys](../../procurement/purchase-agreements.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
