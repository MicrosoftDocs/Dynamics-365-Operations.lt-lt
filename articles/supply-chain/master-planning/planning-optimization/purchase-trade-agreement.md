---
title: Bendrasis planavimas su įsigijimo prekybos sutartimis
description: Šioje temoje aprašoma, kaip planavimo optimizavimo funkcija gali rasti suplanuoto užsakymo tiekėją ir (arba) gamybos laiką pagal geriausią pirkimo prekybos sutartyse nurodytą kainą arba gamybos laiką.
author: ChristianRytt
ms.date: 06/29/2020
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
ms.author: crytt
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 570b0995821dcaa2e180b48c25facee01e98f8e3
ms.sourcegitcommit: 51cad1ce3ed44ebf7eb9bdf553ee2df4c1f03135
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015906"
---
# <a name="master-planning-with-purchase-trade-agreements"></a>Bendrasis planavimas su įsigijimo prekybos sutartimis

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašoma, kaip planavimo optimizavimo funkcija gali rasti suplanuoto užsakymo tiekėją ir (arba) gamybos laiką pagal geriausią visose pirkimo prekybos sutartyse, kurios buvo nurodytos konkrečiam produktui, nurodytą kainą arba gamybos laiką.

## <a name="turn-on-the-purchase-trade-agreements-for-planning-optimization-feature"></a>Įjungti pirkimo prekybos sutartis, skirtas planavimo optimizavimo funkcijai

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [Funkcijos valdymas](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia. Ten ši funkcija pateikiama taip:

- **Modulis:** *Bendrasis planavimas*
- **Funkcijos pavadinimas:** *pirkimo prekybos sutartis, skirta planavimo optimizavimui*

## <a name="prepare-your-system-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Paruoškite savo sistemą, kad galėtumėte įvertinti pirkimo prekybos sutartis bendrojo planavimo metu

Atlikite šiuos veiksmus, kad sukonfigūruotumėte savo sistemą taikyti planavimo optimizavimą, kuris įvertina pirkimo prekybos sutartis.

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

    - Skirtuke **Bendra** nustatyti tiekėjo perrašymus. Jei norite, kad planavimo optimizavimo funkcija naudotų pirkimo prekybos sutartis tiekėjui pasirinkti, turite uždrausti tiekėjo perrašymus, panaikindami žymės langelio **Naudoti konkretų parametrą** žymėjimą.
    - Skirtuke **Gamybos laikas** galite nustatyti gamybos laiko perrašymą. Jei norite, kad planavimo optimizavimo funkcija naudotų pirkimo prekybos sutartis gamybos laikui pasirinkti, turite gamybos laiko perrašymus. Išvalykite kiekvieno gamybos laiko tipo, kurį norite pasirinkti naudodami pirkimo prekybos sutartis (**Pirkimas**, **Gamyba** ir (arba) **Perkėlimas**), žymės langelį.

1. Norėdami grįžti į pasirinkto produkto informacijos puslapį, uždarykite puslapį **Prekės padengimas**.
1. Veiksmų srities skirtuko **Planas** grupėje **Prognozė**, pasirinkite **Tiekimo prognozė**, kad būtų atidarytas puslapis **Tiekimo prognozė**. Įsitikinkite, kad čia nėra rodomos eilutės, kurios reikšmė stulpelyje yra **Tiekėjo paskyra**.
1. Norėdami grįžti į pasirinkto produkto informacijos puslapį, uždarykite puslapį **Tiekimo prognozė**.
1. Veiksmų srityje, skirtuke **Pirkimas**, grupėje **Prekybos sutartys**, pasirinkite **Rodyti prekybos sutartis**. Įsitikinkite, kad įtrauktos visos atitinkamos pirkimo prekybos sutartys. Taip pat įsitikinkite, kad parinktis **Neatsižvelgti į gamybos laiką** nustatyta į **Ne** kiekvienai sutarčiai, kurioje norite planavimo optimizavimo, kad galėtumėte naudoti šiai sutarčiai nurodytą gamybos laiką.
1. Veiksmų srities skirtuko **Planas** grupėje **Užsakymo parametrai** pasirinkite **Numatytieji užsakymo parametrai**, kad pasirinktam produktui būtų atidarytas puslapis **Numatytieji užsakymo parametrai**. „FastTab“ skirtuke **Pirkimo užsakymas** peržiūrėkite lauko **Pirkimo gamybos laikas** reikšmę. Jei nenurodytas prekės padengimo gamybos laiko perrašymas, planavimo optimizavimo funkcija naudos šią reikšmę, pasirinkdama prekybos sutartis, kuriose parinktis **Nepaisyti gamybos laiko** yra nustatyta į **Taip**. Todėl reikia pakoreguoti šią reikšmę pagal savo poreikius.
1. Šią procedūrą kartokite nustatydami kiekvieną atitinkamą produktą.

> [!NOTE]
> „Planning Optimization“ palaiko kelių valiutų įsigijimo prekybos sutartis. Kai ieškote prekybos sutarties naudodami parinktį Žemiausia vieneto kaina, sistema nagrinės galimybę įsigyti prekybos sutarties eilutes su skirtingomis valiutomis, pateiktame valiutos kursą tarp prekybos sutarties eilutės valiutos ir juridinio subjekto apskaitos **valiutos**. Kitu atveju prekybos sutarties eilutės bus nepaisoma, o jūs matysite klaidą bendrojo planavimo metu. Todėl į bendrąjį planavimą bus įtraukta informacija iš visų atitinkamų pirkimo prekybos sutarties eilučių, kuriose kainos gali būti konvertuojamos į apskaitos valiutą. Svarbu pažymėti, kad konvertavimo į apvalinimo taisykles nebus atsižvelgiama prekybos sutarties eilutės kainų konvertavimo metu.

## <a name="examples-of-how-planning-optimization-finds-vendor-and-lead-times"></a>Planavimo optimizavimo, kuris nustato tiekėjo ir gamybos laiką, pavyzdžiai

Tolesnėje lentelėje pateikiami pavyzdžiai, kurie rodo, kaip įvairūs išleistų produktų parametrai ir su jais susijusios pirkimo prekybos sutartys lemia sukurto suplanuoto pirkimo užsakymo reikšmes. **Paryškintos** reikšmės dviejuose dešiniausiuose stulpeliuose yra planavimo optimizavimo pasirinktos reikšmės. Kituose stulpeliuose esančios **_paryškintos ir pasviros_** reikšmės yra parametrai, pagal kuriuos buvo sudarytos kiekvienos eilutės reikšmės.

| Išleistas produktas: tiekėjas | Numatytieji užsakymo parametrai: gamybos laikas | Prekės padengimas: nepaisyti tiekėjo | Prekės padengimas: nepaisyti gamybos laiko | Prekybos sutartis: tiekėjas | Prekybos sutartis: gamybos laikas | Prekybos sutartis: nepaisyti gamybos laiko | Gautas tiekėjas | Gautas gamybos laikas |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ***„US001”** _ | _*_„1”_*_ | nr. | nr. | US003 | 3 | nr. | _ *„US001”** | **1** |
| US001 | 1 | ***Taip: US002** _ | _*_Taip: 2_*_ | US003 | 3 | nr. | _ *„US002”** | **2** |
| *(tuščia)* | 1 | nr. | nr. | ***„US003”** _ | _*_„3”_*_ | nr. | _ *„US003”** | **3** |
| *(tuščia)* | ***„1”** _ | nr. | nr. | _*_„US003”_*_ | 3 | Taip | _ *„US003”** | **1** |
| *(tuščia)* | ***„1”** _ | _*_Taip: US002_*_ | nr. | US003 | 3 | nr. | _ *„US002”** | **1** |
| *(tuščia)* | ***„1”** _ | _*_Taip: US002_*_ | nr. | US003 | 3 | nr. | _ *„US002”** | **1** |
| *(tuščia)* | 1 | nr. | Taip: 2 | ***„US003”** _ | _*_„3”_*_ | nr. | _ *„US003”** | **3** |
| *(tuščia)* | 1 | nr. | ***Taip: 2** _ | _*_„US003”_*_ | 3 | Taip | _ *„US003”** | **2** |

## <a name="additional-resources"></a>Papildomi ištekliai

[Pirkimo sutartys](../../procurement/purchase-agreements.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
