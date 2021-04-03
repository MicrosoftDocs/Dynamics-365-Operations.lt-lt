---
title: Inžinerijos keitimo valdymo apžvalga
description: Ši tema pateikia inžinerijos keitimo valdymo apžvalgą, kuri padeda jums planuoti ir valdyti produkto versijas ir valdyti produkto gyvenimo ciklus bei inžinerijos pokyčius.
author: t-benebo
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 3fde9194ece4774c4d39785e337caf2413052159
ms.sourcegitcommit: ee7a890e3e4ed6436898e5ab6eff309082a073f8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/18/2021
ms.locfileid: "5476680"
---
# <a name="engineering-change-management-overview"></a>Inžinerijos keitimo valdymo apžvalga

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Funkcijos santrauka

Šiandien gamintojams reikia stipraus produkto duomenų valdymo, versijos kontrolės ir inžinerijos keitimo valdymo siekiant sėkmės pasaulyje su nuolatos besitraukiančio gyvenimo ciklo produktais, padidinta kokybe ir patikimumo reikalavimais bei padidintu dėmesiu produkto saugai.

Inžinerijos keitimo valdymas suteikia struktūrą ir discipliną produkto duomenų valdymo procesui ir suteikia produktams galimybę būti nustatytiems, išleistiems ir peržiūrėtiems valdymo būdu, kurį palaiko darbo eigos. Per produkto versijas ir inžinerijos keitimo valdymą galite registruoti, įvertinti poveikį ir taikyti inžinerijos keitimus per visą produkto gyvavimo ciklą.

Inžinerijos keitimo valdymo apžvalgą, kuri padeda jums planuoti ir valdyti produkto versijas ir valdyti produkto gyvenimo ciklus bei inžinerijos pokyčius. Pateikiamas pagrindinių savybių sąrašas:

- Produkto versijos
- Pagerintos produkto išleidimo funkcijos, kuriso leidžia jums išlaikyti produkto pagrindinius duomenis viename juridiniame asmenyje (inžinerijso bendrovėje) ir publikuoti visiškai sukonfigūruotą išleistą produktą kitiems juridiniams asmenims.
- Patvirtinimo taisyklės, kurioms reikalingas informacija yra įvedama prieš tai, kai įjungiama produkto versija (pasirengimo patikros)
- Pagerintas produkto gyvavimo ciklo valdymas per gerai išdirbtą valdymą, kai išleistas produktas gali būti naudojamas konkrečiuose verslo procesuose
- Inžinerijos pokyčio reikalavimai palaikomi darbo eigų
- Inžinerijos pokyčio užsakymai palaikomi darbo eigų

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

Ankstesnis vaizdo įrašas ([Keitimo valdymo galimybės „Dynamics 365 Supply Chain Management“](https://youtu.be/N313FqvRuBc)) yra įtrauktos į [„Finance and Operations“ grojaraštį](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) prieinamą „YouTube“.

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a>Įjunkite jūsų sistemos inžinerinių pakeitimų valdymą ir versijos dimensijų funkcijas

Prieš pradedami naudoti inžinerinių pakeitimų valdymą, turite įgalinti ir funkciją *Inžinerinių pakeitimų valdymas*, ir jos konfigūracijos raktą. Jei norite sekti operacijų produktų versijos dimensiją (pasirinktinai), turite įgalinti funkciją *Produkto versijos dimensija* ir jos konfigūracijos raktą.

Pirmiausia įjunkite šias funkcijas atlikdami toliau nurodytus veiksmus.

1. Eikite į [Funkcijos valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Tikrinkite naujinimus.
1. Įjunkite funkciją pavadinimu **Inžinerijos keitimo valdymas**.
1. Jei norite ją naudoti, įjunkite ir funkciją, kuri pavadinta **Produkto dimensijos versija**.

Tada įjunkite konfigūracijos raktus atlikdami toliau nurodytus veiksmus.

1. Įdėkite savo sistemą į priežiūros režimą kaip aprašyta [Priežiūros režime](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Eikite į **Sistemos administravimas \> Sąranka \> Licencijos konfigūracija**.
1. Išplėskite mazgą **Prekyba**
1. Pažymėkite žymės langelį **Inžinerinių pakeitimų valdymas**.
1. Jei norite jį naudoti, tada taip pat pažymėkite žymės langelį **Produkto dimensija – versija**.
1. Išjunkite priežiūros režimą kaip aprašyta [Priežiūros režime](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
