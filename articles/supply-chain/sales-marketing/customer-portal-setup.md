---
title: Kliento portalo įdiegimas, nustatymas ir atnaujinimas
description: Šiame straipsnyje pateikiama licencijavimo informacija ir kliento portalo nustatymo instrukcijos.
author: Henrikan
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 8344212e66cb57ea8c9d4e8c2cdfbf022bc199c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850589"
---
# <a name="install-set-up-and-update-the-customer-portal"></a>Kliento portalo įdiegimas, nustatymas ir atnaujinimas

[!include [banner](../includes/banner.md)]


## <a name="licensing-requirements"></a>Licencijavimo reikalavimai

Norėdami naudoti kliento portalą, turite turėti toliau išvardytas licencijas.

- **„Power Apps“ portalai** – ši licencija reikalinga kliento portalo prieglobai. Portalai licencijuojami remiantis naudojimu. Norėdami gauti daugiau informacijos, žr. [„Power Apps“ portalų licencijavimo reikalavimus](/power-platform/admin/powerapps-flow-licensing-faq#portals).
- **Dvigubas rašymas** – turite turėti būtinas licencijas, kad galėtumėte įjungti dvigubo rašymo funkciją „Supply Chain Management“ lentelėms. Prireikus daugiau informacijos, žr. [dvigubo rašymo sistemos reikalavimai](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a>Priklausomybė nuo dvigubo rašymo ir „Power Apps“ portalų

Kliento portalas yra priklausomas nuo „Power Apps“ portalų ir dvigubo rašymo, kaip parodyta tolesnėje iliustracijoje.

![Kliento portalo priklausomybės.](media/customer-portal-elements.png "Kliento portalo priklausomybes")

Skirtingai nei kitos „Supply Chain Management“ funkcijos, kliento portalo šablonas yra „Power Apps“ portaluose. Todėl klientų portalą riboja „Power Apps“ portalų teikiamos funkcijos bei galimybės ir dvigubą rašymą naudojančios lentelės.

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a>Reikalingi nustatymo veiksmai, norint įjungti kliento portalą

Įsitikinę, kad turite reikiamas licencijas, galite nustatyti dvigubo rašymo funkciją, kaip nurodyta [dvigubo rašymo pradinio sinchronizavimo instrukcijose](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-entity-map.md).

Būtinai įjunkite toliau išvardytus susiejimus su lentelėms dvigubo rašymo funkcijoje.

- Pardavimo užsakymo antraštė
- Pardavimo užsakymo informacija
- Sąskaitos
- Kontaktai
- Produktai

Atlikę šį nustatymą, galite paruošti kliento portalo šabloną.

## <a name="provision-the-customer-portal"></a>Kliento portalo rengimas

Prieš pradėdami įsitikinkite, kad jau atlikote [reikiamus nustatymo veiksmus](#required-setup). Tada atlikite toliau pateiktus veiksmus, kad parengtumėte kliento portalą.

1. Eikite į [make.powerapps.com](https://make.powerapps.com/).
2. Įsitikinkite, kad naudojate aplinką, kurioje įjungėte dvigubo rašymo funkciją.
3. Skirtuke **Kurti** slinkite iki **Pradėti nuo šablono** dalies ir pasirinkite šabloną, pavadintą **Kliento portalas**.
4. Vadovaukitės ekrane pateikiamais nurodymais.

Užbaigus parengimą, kliento portalą galima pasiekti puslapyje **Pagrindinis**, dalyje **Jūsų programos**.

> [!NOTE]
> Jei dvigubo rašymo sprendimas neįdiegtas aplinkoje, su kuria dirbate, jums bus parodytas klaidos pranešimas ir kliento portalas nebus parengtas.

## <a name="update-the-customer-portal"></a>Kliento portalo atnaujinimas

Vėliau į kliento portalą galima įtraukti daugiau funkcijų. Bet kokie pakeitimai, kuriuos „Microsoft“ atlieka pagrindiniams komponentams, bus automatiškai rodomi jūsų aplinkoje. Tačiau svetainėje, kuri parengta jūsų aplinkoje, konfigūravimo duomenų pakeitimai nebus automatiškai rodomi. Jums reikės rankiniu būdu pritaikyti šiuos pakeitimus – gauti kodą iš naujo šablono ir sujungti jį su parengta svetaine.

## <a name="additional-resources"></a>Papildomi ištekliai

Norėdami sužinoti, kaip nustatyti ir tinkinti kliento portalą, pirmiausia peržiūrėkite toliau pateiktą pagrindinių technologijų dokumentaciją.

- [„Power Apps“ portalų dokumentacija](/powerapps/maker/portals/overview)
- [Dvigubo rašymo dokumentacija](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

Norėdami veiksmingai tvarkyti savo portalus, turite suprasti „Power Apps“ portalus ir „Microsoft Dataverse“ ciklą. Daugiau informacijos ieškokite šiuose ištekliuose:

- [Apie portalo ciklą](/powerapps/maker/portals/admin/portal-lifecycle)
- [Portalo naujovinimas](/powerapps/maker/portals/admin/upgrade-portal)
- [Portalo konfigūracijos perkėlimas](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Sprendimo ciklo valdymas – „Dynamics 365 for Customer Engagement“ programos](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]