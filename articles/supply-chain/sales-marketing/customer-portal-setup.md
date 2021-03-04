---
title: Kliento portalo įdiegimas, nustatymas ir atnaujinimas
description: Šioje temoje pateikiama licencijavimo informacija ir kliento portalo nustatymo instrukcijos.
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e61fc5f7151a0bb61d496d47f4ad4e727a2a1d65
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529535"
---
# <a name="install-set-up-and-update-the-customer-portal"></a>Kliento portalo įdiegimas, nustatymas ir atnaujinimas

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a>Licencijavimo reikalavimai

Norėdami naudoti kliento portalą, turite turėti toliau išvardytas licencijas.

- **„Power Apps“ portalai** – ši licencija reikalinga kliento portalo prieglobai. Portalai licencijuojami remiantis naudojimu. Norėdami gauti daugiau informacijos, žr. [„Power Apps“ portalų licencijavimo reikalavimus](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).
- **Dvigubas rašymas** – turite turėti būtinas licencijas, kad galėtumėte įjungti dvigubo rašymo funkciją „Supply Chain Management“ objektams. Prireikus daugiau informacijos, žr. [dvigubo rašymo sistemos reikalavimai](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a>Priklausomybė nuo dvigubo rašymo ir „Power Apps“ portalų

Kliento portalas yra priklausomas nuo „Power Apps“ portalų ir dvigubo rašymo, kaip parodyta tolesnėje iliustracijoje.

![Kliento portalo priklausomybės](media/customer-portal-elements.png "Kliento portalo priklausomybes")

Skirtingai nei kitos „Supply Chain Management“ funkcijos, kliento portalo šablonas yra „Power Apps“ portaluose. Todėl klientų portalą riboja „Power Apps“ portalų teikiamos funkcijos bei galimybės ir dvigubą rašymą naudojantys objektai.

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a>Reikalingi nustatymo veiksmai, norint įjungti kliento portalą

Įsitikinę, kad turite reikiamas licencijas, galite nustatyti dvigubo rašymo funkciją, kaip nurodyta [dvigubo rašymo pradinio sinchronizavimo instrukcijose](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).

Būtinai įjunkite toliau išvardytus susiejimus su objektais dvigubo rašymo funkcijoje.

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

- [„Power Apps“ portalų dokumentacija](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [Dvigubo rašymo dokumentacija](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

Norėdami veiksmingai tvarkyti savo portalus, turite suprasti „Power Apps“ portalus ir „Common Data Service“ ciklą. Daugiau informacijos ieškokite šiuose ištekliuose:

- [Apie portalo ciklą](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [Portalo naujovinimas](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [Portalo konfigūracijos perkėlimas](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Sprendimo ciklo valdymas – „Dynamics 365 for Customer Engagement“ programos](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]