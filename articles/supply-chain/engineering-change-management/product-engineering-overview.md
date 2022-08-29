---
title: Inžinerijos pakeitimų valdymo peržiūra (yra vaizdo įrašas)
description: Šiame straipsnyje pateikiama inžinerinių pakeitimų valdymo apžvalga, kuri padeda suplanuoti ir valdyti produkto versijų valdymą bei tvarkyti produkto ciklus ir inžinerijos pakeitimus.
author: t-benebo
ms.date: 08/09/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: b494e15488bed148119aed0e9d62ab1740f38add
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334872"
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

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4HE6B]

Ankstesnis vaizdo įrašas ([keiskite valdymo galimybes Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) yra įtrauktas į finansus [ir operacijas,](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) galimas YouTube.

## <a name="turn-on-the-engineering-change-management-features-for-your-system"></a>Įjunkite inžinerijos keitimo valdymą savo sistemos funkcijoms

Prieš pradedami naudoti inžinerinių pakeitimų valdymą, turite įgalinti ir funkciją *Inžinerinių pakeitimų valdymas*, ir jos konfigūracijos raktą. Jei norite sekti operacijų produktų versijos dimensiją (pasirinktinai), turite įgalinti abi funkcijas *Produkto versijos dimensija* ir jos konfigūracijos raktą. Kai tos būtinosios sąlygos nustatytos, galėsite įjungti papildomas inžinerijos pakeitimų valdymo pasirinktines priemones.

### <a name="turn-the-basic-engineering-change-management-features-on-or-off"></a>Įjungti arba išjungti pagrindines inžinerijos pakeitimų valdymo funkcijas

Norėdami įjungti arba išjungti pagrindines inžinerijos keitimo valdymo funkcijas, atlikite šiuos veiksmus. Kaip ir tiekimo grandinės valdymo versija 10.0.25, *inžinerinio* keitimo valdymo funkcija įjungiama pagal numatytuosius nustatymus.

1. Eikite į darbo [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) srityje.
1. Tikrinkite naujinimus.
1. Jei reikia, įjunkite arba *išjunkite priemonę, pavadintą* Inžinerinio keitimo valdymas.
1. Jei norite sekti operacijų produktų versijos dimensiją (pasirinktinai), įjunkite priemonę, pavadintą Produkto *dimensijos versija*.

### <a name="turn-the-required-configuration-keys-on-or-off"></a>Įjungti arba išjungti reikiamus konfigūracijos raktus

Tada įjunkite konfigūracijos raktus atlikdami toliau nurodytus veiksmus. Pagal numatytuosius nustatymus jos nėra įjungiamos.

1. Įdėkite savo sistemą į priežiūros režimą kaip aprašyta [Priežiūros režime](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Eikite į **Sistemos administravimas \> Sąranka \> Licencijos konfigūracija**.
1. Išplėskite mazgą **Prekyba**.
1. Įjungti arba išjungti pagrindinės priemonės konfigūracijos raktą, naudojantis žymės langeliu Inžinerija **keisti** valdymą.
1. Jei reikia, išplėskite **Inžinerinių keitimų mazgą** ir pasirinkite arba išvalykite toliau pateiktus žymės langelius (atsižvelgiant į funkcijas, kurias norite naudoti):

    - **Atributų ieška** – Pasirinkite šį žymės langelį, kad įgalintumėte [atributų ieškos funkciją](engineering-attributes-and-search.md). Rekomenduojame įgalinti šią funkciją, tačiau galite išvalyti šį žymės langelį, jei jos nenaudosite.
    - **Gamybos procesų valdymo keitimas** – Pasirinkite šį žymės langelį, jei norite naudoti Inžinerinių keitimų valdymo funkcijas, kad valdytumėte gamybos procesų formulių pakeitimus. Jei jums nereikia valdyti formulių, galite išvalyti šį žymės langelį. Daugiau informacijos rasite [Formulių ir jų ingredientų pakeitimų valdymas](manage-formula-changes.md).

1. Jei taip pat norite naudoti versijos dimensiją, tada pasirinkite **Produkto dimensija – Versija** žymės langelį. (Šis žymės langelis yra žemyn sąraše, o ne įdėtas po **Inžinerijos pakeitimų valdymo** mazgas.) Jei šios funkcijos jums nereikia, galite išvalyti šį žymės langelį.
1. Išjunkite priežiūros režimą kaip aprašyta [Priežiūros režime](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Duomenų bazė turi būti sinchronizuota siekiant užtikrinti, kad konfigūracijos raktai yra tinkamai atnaujinti, kad atspindėtų jūsų pakeitimus. Atlikite vieną iš šių veiksmų atsižvelgdami į tai, su kokio tipo aplinka dirbate:
    - **Jei naudojate 1 pakopos (programavimo) aplinkas**, atidarykite savo projektą "Microsoft Visual Studio" ir pasirinkite "**Dynamics 365" sinchronizuoti duomenų \> bazės sinchronizavimą \>**.
    - **2 pakopų (ir aukštesnio)** aplinkose: įdus aplinką į priežiūros režimą ir iš jos, duomenų bazė sinchronizuojama automatiškai, kad šį veiksmą būtų galima praleisti.

### <a name="turn-on-additional-engineering-change-management-features"></a>Įjunkite papildomos inžinerijos keitimo valdymą savo sistemos funkcijoms

Įjungus pagrindines inžinerijos keitimo valdymo priemones ir įgalinus jų konfigūracijos raktus, prie priemonių valdymo pridedama keletas papildomų ir pasirinktinių inžinerijos pakeitimų valdymo priemonių. Kiekviena iš šių priemonių pateikta inžinerinio **keitimo valdymo modulyje**. Šioje lentelėje aprašoma kiekviena pasirinktinė priemonė ir pateikiami saitai, kuriuose pateikiama daugiau informacijos.

| Funkcijos pavadinimas funkcijos valdyme | Aprašymas | Funkcijos būsena |
|---|---|---|
| Pakeitimų valdymo įjungimas esamiems produktams | <p>Ši priemonė leidžia konvertuoti esamus produktus į inžinerijos produktus, kad, naudodami inžinerinių pakeitimų valdymą, pradėtumėte juos valdyti.</p><p>- Dėl daugiau informacijos rasite [Pakeitimų valdymo įjungimas esamiems produktams](change-management-existing-products.md).</p> | Pagal numatytąją reikšmę kaip 10.0.25 versija. |
| Inžinerijos pranešimai gamybai | <p>Jei produktas inžinerijos metu pakeičiamas, gali reikėti informuoti gamybą apie šiuos pakeitimus. Tokiu būdu gamybos darbuotojai gali imtis atitinkamų veiksmų, pvz., komponentų pakeitimo, komplektavimo specifikacijos (KS) pakeitimo arba maršruto pakeitimo. Ši priemonė leidžia informuoti gamybą apie produktų, kurie gaminami, pakeitimus.</p><p>Dėl daugiau informacijos, žr. [Valdyti keitimus inžinerijos produktams](engineering-change-management.md).</p> |  Pagal numatytąją reikšmę kaip 10.0.25 versija. |
| Patobulintas atributų paveldimumas inžinerinių pakeitimų valdymui | <p>Ši priemonė supaprastina atributų valdymą baigtoms prekėms ar tarpinėms prekėms. Kai ši funkcija įjungta, lengviau identifikuoti visus atributus, priklausančius prekei, ir galima pasirinkti atributus, kurie turėtų būti platinami iš tos prekės pirminėms prekės. Ši funkcija yra naudinga, kai, pavyzdžiui, vienas baigtos medžiagos komponentas yra dūžtas, pagal ar ištvirtęs, nes galite lengvai identifikuoti dūžtamą, panaudotus ar perduotos atributus ir išplatinti jį į baigtą naudą.</p><p>Inžinerijos atributai dėl daugiau informacijos, žr. [Inžinerijos atributai ir inžinerijos atributų paieška](engineering-attributes-and-search.md).</p> |  Pagal numatytąją reikšmę kaip 10.0.25 versija. |
| Produkto parengties patikros | <p>Funkcija leidžia Jums nustatyti pasirengimo patikrinimų strategijas standartiniams (neinžineriniams) produktams. Naudokite produkto pasirengimo tikrinimus, norėdami užtikrinti, kad kiekvienas produktas yra visiškai apibrėžtas ir kad visos būtinos strategijos yra sukonfigūruotos prieš produkto prieinamumą ir naudojimą operacijose. Jei šią funkciją išjungsite kurį laiką panaudodami, visi esami standartinių produktų pasirengimo tikrinimai bus panaikinti.</p><p>Dėl daugiau informacijos, žr. [Produkto parengimas](product-readiness.md).</p> |  Pagal numatytąją reikšmę kaip 10.0.25 versija. |
| Tvarkyti formulių ir jų sudedamųjų dalių keitimus | <p>Ši funkcija leidžia sekti formulės ingredientų, ingredientų sudėtiuose ir produktuose pakeitimus.</p><p>Daugiau informacijos rasite [Formulių ir jų ingredientų pakeitimų valdymas](manage-formula-changes.md).</p> |  Pagal numatytąją reikšmę kaip 10.0.25 versija. |
| Inžinierinių produktų variantų generavimas | <p>Ši priemonė leidžia generuoti inžinerijos produktų variantus, pagrįstus galima dimensijų vertėmis.</p><p>Daugiau informacijos ieškokite gamybos [produktų variantų gener kuriuos galima generuoti](engineering-variants.md).</p> |  Pagal numatytąją reikšmę kaip 10.0.25 versija. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

