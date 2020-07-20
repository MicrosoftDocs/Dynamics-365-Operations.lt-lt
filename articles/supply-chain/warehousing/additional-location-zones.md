---
title: Papildomos vietos zonos
description: Šioje temoje apžvelgiamos naujos vietos zonos, kurios pridėtos į „Microsoft Dynamics 365 Supply Chain Management”.
author: Mirzaab
manager: AnnBe
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 9727187ad555f9e3d09beed3f3447a22c29ed22a
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530172"
---
# <a name="additional-location-zones"></a>Papildomos vietos zonos

[!include [banner](../includes/banner.md)]

Galimi trys nauji zonų laukai „Microsoft Dynamics 365 Supply Chain Management”. Sandėlio valdytojai gali naudoti juos papildomoms sandėlio organizacijoms arba maketams nustatyti. Naujus zonos laukus galima nustatyti neautomatiniu būdu arba naudojant **Vietos parametras** vedlį. Jie gali būti naudojami bet kurioje užklausoje ar filtruojant, naudojant Vietos lentelę.

Norint naudoti zonos laukus, papildomų nustatymų nereikia.

## <a name="turn-on-the-additional-location-zone-feature"></a>Papildomos vietos zonos įjungimo funkcija

Norint naudoti *Papildomos vietos zona* funkciją, įjunkite ją savo sistemoje. Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, kad patikrintų funkcijos būseną ir įjungtų ją, kai reikia. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *sandėlio valdymas*
- **Funkcijos pavadinimas:** *Papildomos vietos zona*

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
