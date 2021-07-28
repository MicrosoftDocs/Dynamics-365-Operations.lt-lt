---
title: Inžinerijos keitimo valdymo apžvalga
description: Ši tema pateikia inžinerijos keitimo valdymo apžvalgą, kuri padeda jums planuoti ir valdyti produkto versijas ir valdyti produkto gyvenimo ciklus bei inžinerijos pokyčius.
author: t-benebo
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 70567489e5a1b84677ee63c296d15f5bdeb728ca
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/03/2021
ms.locfileid: "6338612"
---
# <a name="engineering-change-management-overview"></a>Inžinerijos keitimo valdymo apžvalga

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Funkcijos santrauka

Šiandien gamintojams reikia stipraus produkto duomenų valdymo, versijos kontrolės ir inžinerijos keitimo valdymo siekiant sėkmės pasaulyje su nuolatos besitraukiančio gyvenimo ciklo produktais, padidinta kokybe ir patikimumo reikalavimais bei padidintu dėmesiu produkto saugai.

Inžinerijos keitimo valdymas suteikia struktūrą ir discipliną produkto duomenų valdymo procesui ir suteikia produktams galimybę būti nustatytiems, išleistiems ir peržiūrėtiems valdymo būdu, kurį palaiko darbo eigos.Per produkto versijas ir inžinerijos keitimo valdymą galite registruoti, įvertinti poveikį ir taikyti inžinerijos keitimus per visą produkto gyvavimo ciklą.

Inžinerijos keitimo valdymo apžvalgą, kuri padeda jums planuoti ir valdyti produkto versijas ir valdyti produkto gyvenimo ciklus bei inžinerijos pokyčius. Pateikiamas pagrindinių savybių sąrašas:

- Produkto versijos
- Pagerintos produkto išleidimo funkcijos, kurios leidžia jums išlaikyti produkto pagrindinius duomenis viename juridiniame asmenyje (inžinerijos bendrovėje) ir publikuoti visiškai sukonfigūruotą išleistą produktą kitiems juridiniams asmenims.
- Patvirtinimo taisyklės, kurioms reikalingas informacija yra įvedama prieš tai, kai įjungiama produkto versija (pasirengimo patikros)
- Pagerintas produkto gyvavimo ciklo valdymas per gerai išdirbtą valdymą, kai išleistas produktas gali būti naudojamas konkrečiuose verslo procesuose
- Inžinerijos pokyčio reikalavimai palaikomi darbo eigų
- Inžinerijos pokyčio užsakymai palaikomi darbo eigų

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

Ankstesnis vaizdo įrašas ([Keitimo valdymo galimybės „Dynamics 365 Supply Chain Management“](https://youtu.be/N313FqvRuBc)) yra įtrauktos į [„Finance and Operations“ grojaraštį](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) prieinamą „YouTube“.

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a>Įjunkite jūsų sistemos inžinerinių pakeitimų valdymą ir versijos dimensijų funkcijas

Prieš pradedami naudoti inžinerinių pakeitimų valdymą, turite įgalinti ir funkciją *Inžinerinių pakeitimų valdymas*, ir jos konfigūracijos raktą. Jei norite sekti operacijų produktų versijos dimensiją (pasirinktinai), turite įgalinti funkciją *Produkto versijos dimensija* ir jos konfigūracijos raktą.

Pirmiausia įjunkite šias funkcijas atlikdami toliau nurodytus veiksmus.

1. Eikite į darbo [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) srityje.
1. Tikrinkite naujinimus.
1. Įjunkite funkciją pavadinimu *Inžinerijos keitimo valdymas*.
1. Jei norite ją naudoti, taip pat įjunkite funkciją, pavadintą *Produkto dimensijos versija*.

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

> [!IMPORTANT]
> Nuo 2022 m. balandžio mėn. „Engineering Change Management“ ir produkto dimensijos licencijos raktai – versija bus įgalinta pagal numatytuosius nustatymus visoms naujiems **diegimams, tačiau prireikus vis tiek galėsite** jas **išjungti**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
