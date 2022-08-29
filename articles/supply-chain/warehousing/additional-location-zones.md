---
title: Papildomos vietos zonos
description: Šiame straipsnyje pateikta naujų vietos zonų, kurios buvo pridėtos prie "Microsoft", apžvalga Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 819330e0f6e6cd419da441f919d68ff996b6475c
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336522"
---
# <a name="additional-location-zones"></a>Papildomos vietos zonos

[!include [banner](../includes/banner.md)]

Galimi trys nauji zonų laukai „Microsoft Dynamics 365 Supply Chain Management”. Sandėlio valdytojai gali naudoti juos papildomoms sandėlio organizacijoms arba maketams nustatyti. Naujus zonos laukus galima nustatyti neautomatiniu būdu arba naudojant **Vietos parametras** vedlį. Jie gali būti naudojami bet kurioje užklausoje ar filtruojant, naudojant Vietos lentelę.

Norint naudoti zonos laukus, papildomų nustatymų nereikia.

## <a name="turn-the-additional-location-zone-feature-on-or-off"></a>Įjungti arba išjungti papildomos vietos zonos funkciją

Jei norite naudoti šią funkciją, ją turite įjungti savo sistemoje. Kaip ir tiekimo grandinės valdymo versija 10.0.25, funkcija įjungiama pagal numatytąjį nustatymą. Kaip ir tiekimo grandinės valdymo versija 10.0.29, ši funkcija yra privaloma ir jos išjungti negalima. Jei naudojate senesnę nei 10.0.29 versiją, *·*[tada](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) administratoriai gali įjungti arba išjungti šią funkciją ieškodami papildomos vietos zonos funkcijos funkcijų valdymo darbo srityje.

## <a name="use-location-zones"></a>Vietos zonų naudojimas

1. Eikite į **Sandėlio tvarkymas \> Sąranka \>Sandėlis \> Vietos nustatymo vedlys**.
2. Nustatykite toliau nurodytas reikšmes.

    - Lauke **Sandėlis** pasirinkite _62_.
    - **Zonos ID** lauke pasirinkite _AUKŠTAS_.
    - **Papildoma zona 1** lauke pasirinkite _PASIRINKTIZONĄ1_.
    - **Papildoma zona 2** lauke pasirinkite _INTERNETINĖPARDUOTUVĖ1_.
    - **Vietos profilio ID** lauke pasirinkite _AUKŠTAS_.

3. Pasirinkite **Aukštas** eilutę.
4. **Nuo numeris** įveskite _1_. **Iki numeris** lauke įveskite _3_.
5. Pasirinkite **Perėjimas** eilutę.
6. **Nuo numeris** įveskite _1_. **Iki numeris** lauke įveskite _5_.
7. Pasirinkite **Kurti**.
8. Gaunate pranešimus, kuriuose nurodoma, kad buvo pridėtos naujos vietos. Pasirinkite **Rodyti pranešimus** mygtuką, kada peržiūrėtumėte pranešimus.
9. Eikite į **Sandėlio tvarkymas \> Sąranka \> Sandėlis \> Vietos**. Naujos vietos rodomos sąraše, o visi zonų laukai yra galimi (t. y. esamos zonos laukas ir naujos papildomos zonos laukai).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]