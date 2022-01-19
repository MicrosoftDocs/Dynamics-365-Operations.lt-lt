---
title: Inžinerijos pakeitimų valdymo peržiūra (yra vaizdo įrašas)
description: Ši tema pateikia inžinerijos keitimo valdymo apžvalgą, kuri padeda jums planuoti ir valdyti produkto versijas ir valdyti produkto gyvenimo ciklus bei inžinerijos pokyčius.
author: t-benebo
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: d667aef827addcf7c34075b08afffffe3fd71935
ms.sourcegitcommit: f5fd2122a889b04e14f18184aabd37f4bfb42974
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/10/2022
ms.locfileid: "7952603"
---
# <a name="engineering-change-management-overview"></a>Inžinerijos keitimo valdymo apžvalga

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Funkcijos santrauka

Šiandienos gamintojai reikalauja griežto produkto duomenų valdymo, versijų kontrolės ir inžinerinių pakeitimų valdymo, kad viso pasaulio produkto ciklo sutraukimas, padidintas kokybės ir patikimumo poreikis ir padidintas dėmesys produkto saugai.

Inžinerijos pakeitimų valdymas sukuria struktūrą ir discipliną produkto duomenų valdymo procesui ir įgalina produktus apibrėžti, paleisti ir peržiūrėti kontroliuojamu būdu, kurį palaiko darbo eigos. Naudodami produkto versijas ir inžinerijos pakeitimų valdymą, galite dokumentuoti, įvertinti poveikį ir taikyti inžinerijos pakeitimus viso produkto ciklo metu.

Inžinerijos keitimo valdymo apžvalgą, kuri padeda jums planuoti ir valdyti produkto versijas ir valdyti produkto gyvenimo ciklus bei inžinerijos pokyčius. Pateikiamas pagrindinių savybių sąrašas:

- Produkto versijos
- Pagerintos produkto išleidimo funkcijos, kurios leidžia jums išlaikyti produkto pagrindinius duomenis viename juridiniame asmenyje (inžinerijos bendrovėje) ir publikuoti visiškai sukonfigūruotą išleistą produktą kitiems juridiniams asmenims.
- Patvirtinimo taisyklės, kurioms reikalingas informacija yra įvedama prieš tai, kai įjungiama produkto versija (pasirengimo patikros)
- Pagerintas produkto gyvavimo ciklo valdymas per gerai išdirbtą valdymą, kai išleistas produktas gali būti naudojamas konkrečiuose verslo procesuose
- Inžinerijos pokyčio reikalavimai palaikomi darbo eigų
- Inžinerijos pokyčio užsakymai palaikomi darbo eigų

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

Ankstesnis vaizdo įrašas ([Keitimo valdymo galimybės „Dynamics 365 Supply Chain Management“](https://youtu.be/N313FqvRuBc)) yra įtrauktos į [„Finance and Operations“ grojaraštį](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) prieinamą „YouTube“.

## <a name="turn-on-the-engineering-change-management-features-for-your-system"></a>Įjunkite inžinerijos keitimo valdymą savo sistemos funkcijoms

Prieš pradedami naudoti inžinerinių pakeitimų valdymą, turite įgalinti ir funkciją *Inžinerinių pakeitimų valdymas*, ir jos konfigūracijos raktą. Jei norite sekti operacijų produktų versijos dimensiją (pasirinktinai), turite įgalinti abi funkcijas *Produkto versijos dimensija* ir jos konfigūracijos raktą. Kai tos būtinosios sąlygos nustatytos, galėsite įjungti papildomas inžinerijos pakeitimų valdymo pasirinktines priemones.

### <a name="turn-on-the-basic-engineering-change-management-features"></a>Įjunkite pagrindinės inžinerijos keitimo valdymą savo sistemos funkcijoms

Pirmiausia įjunkite šias funkcijas atlikdami toliau nurodytus veiksmus.

1. Eikite į darbo [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) srityje.
1. Tikrinkite naujinimus.
1. Įjunkite funkciją pavadinimu *Inžinerijos keitimo valdymas*.
1. Jei norite ją naudoti, taip pat įjunkite funkciją, pavadintą *Produkto dimensijos versija*.

### <a name="turn-on-the-required-configuration-keys"></a>Įjungti būtinus konfigūracijos raktus

Tada įjunkite konfigūracijos raktus atlikdami toliau nurodytus veiksmus.

1. Įdėkite savo sistemą į priežiūros režimą kaip aprašyta [Priežiūros režime](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Eikite į **Sistemos administravimas \> Sąranka \> Licencijos konfigūracija**.
1. Išplėskite mazgą **Prekyba**.
1. Įgalinkite pagrindinės funkcijos konfigūracijos raktą pasirinkdami **Inžinerinių keitimų valdymo** žymės langelį.
1. Jei reikia, išplėskite **Inžinerinių keitimų mazgą** ir pasirinkite arba išvalykite toliau pateiktus žymės langelius (atsižvelgiant į funkcijas, kurias norite naudoti):

    - **Atributų ieška** – Pasirinkite šį žymės langelį, kad įgalintumėte [atributų ieškos funkciją](engineering-attributes-and-search.md). Rekomenduojame įgalinti šią funkciją, tačiau galite išvalyti šį žymės langelį, jei jos nenaudosite.
    - **Gamybos procesų valdymo keitimas** – Pasirinkite šį žymės langelį, jei norite naudoti Inžinerinių keitimų valdymo funkcijas, kad valdytumėte gamybos procesų formulių pakeitimus. Jei jums nereikia valdyti formulių, galite išvalyti šį žymės langelį. Daugiau informacijos rasite [Formulių ir jų ingredientų pakeitimų valdymas](manage-formula-changes.md).

1. Jei taip pat norite naudoti versijos dimensiją, tada pasirinkite **Produkto dimensija – Versija** žymės langelį. (Šis žymės langelis yra žemiau sąraše, o ne įdėtas po **Inžinerinių keitimų valdymo** mazgu.)
1. Išjunkite priežiūros režimą kaip aprašyta [Priežiūros režime](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Vykdykite duomenų bazės sinchronizavimą, kad konfigūracijos raktai būtų tinkamai įgalinti.

> [!IMPORTANT]
> Nuo 2022 m. balandžio mėn. „Engineering Change Management“ ir produkto dimensijos licencijos raktai – versija bus įgalinta pagal numatytuosius nustatymus visoms naujiems **diegimams, tačiau prireikus vis tiek galėsite** jas **išjungti**.

### <a name="turn-on-additional-engineering-change-management-features"></a>Įjunkite papildomos inžinerijos keitimo valdymą savo sistemos funkcijoms

Įjungus pagrindines inžinerijos keitimo valdymo priemones ir įgalinus jų konfigūracijos raktus, prie priemonių valdymo pridedama keletas papildomų ir pasirinktinių inžinerijos pakeitimų valdymo priemonių. Kiekviena iš šių priemonių pateikta inžinerinio **keitimo valdymo modulyje**. Šioje lentelėje aprašoma kiekviena pasirinktinė priemonė ir pateikiami saitai, kuriuose pateikiama daugiau informacijos.

| Funkcijos pavadinimas funkcijos valdyme | Aprašas |
|---|---|
| Pakeitimų valdymo įjungimas esamiems produktams | <p>Ši priemonė leidžia konvertuoti esamus produktus į inžinerijos produktus, kad, naudodami inžinerinių pakeitimų valdymą, pradėtumėte juos valdyti.</p><p>- Dėl daugiau informacijos rasite [Pakeitimų valdymo įjungimas esamiems produktams](change-management-existing-products.md).</p> |
| Inžinerijos pranešimai gamybai | <p>Jei produktas inžinerijos metu pakeičiamas, gali reikėti informuoti gamybą apie šiuos pakeitimus. Tokiu būdu gamybos darbuotojai gali imtis atitinkamų veiksmų, pvz., komponentų pakeitimo, komplektavimo specifikacijos (KS) pakeitimo arba maršruto pakeitimo. Ši priemonė leidžia informuoti gamybą apie produktų, kurie gaminami, pakeitimus.</p><p>Dėl daugiau informacijos, žr. [Valdyti keitimus inžinerijos produktams](engineering-change-management.md).</p> |
| Patobulintas atributų paveldimumas inžinerinių pakeitimų valdymui | <p>Ši priemonė supaprastina atributų valdymą baigtoms prekėms ar tarpinėms prekėms. Kai ši funkcija įjungta, lengviau identifikuoti visus atributus, priklausančius prekei, ir galima pasirinkti atributus, kurie turėtų būti platinami iš tos prekės pirminėms prekės. Ši funkcija yra naudinga, kai, pavyzdžiui, vienas baigtos medžiagos komponentas yra dūžtas, pagal ar ištvirtęs, nes galite lengvai identifikuoti dūžtamą, panaudotus ar perduotos atributus ir išplatinti jį į baigtą naudą.</p><p>Inžinerijos atributai dėl daugiau informacijos, žr. [Inžinerijos atributai ir inžinerijos atributų paieška](engineering-attributes-and-search.md).</p> |
| Produkto parengties patikros | <p>Funkcija leidžia Jums nustatyti pasirengimo patikrinimų strategijas standartiniams (neinžineriniams) produktams. Naudokite produkto pasirengimo tikrinimus, norėdami užtikrinti, kad kiekvienas produktas yra visiškai apibrėžtas ir kad visos būtinos strategijos yra sukonfigūruotos prieš produkto prieinamumą ir naudojimą operacijose. Jei šią funkciją išjungsite kurį laiką panaudodami, visi esami standartinių produktų pasirengimo tikrinimai bus panaikinti.</p><p>Dėl daugiau informacijos, žr. [Produkto parengimas](product-readiness.md).</p> |
| Tvarkyti formulių ir jų sudedamųjų dalių keitimus | <p>Ši funkcija leidžia sekti formulės ingredientų, ingredientų sudėtiuose ir produktuose pakeitimus.</p><p>Daugiau informacijos rasite [Formulių ir jų ingredientų pakeitimų valdymas](manage-formula-changes.md).</p> |
| Inžinierinių produktų variantų generavimas | <p>Ši priemonė leidžia generuoti inžinerijos produktų variantus, pagrįstus galima dimensijų vertėmis.</p><p>Daugiau informacijos ieškokite gamybos [produktų variantų gener kuriuos galima generuoti](engineering-variants.md).</p> |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
