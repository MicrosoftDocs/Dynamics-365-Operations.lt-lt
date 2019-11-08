---
title: Proceso šablono kūrimas sprendime „Attract“
description: Šioje temoje pateikiama informacija apie tai, kaip sukurti proceso šabloną sprendime „Attract“.
author: andreabichsel
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.openlocfilehash: 533b9abd3d57c5bf8f3d9da85020c86012436f2f
ms.sourcegitcommit: dd991154231280aff9c9c5799e42799e2bfc02fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622723"
---
# <a name="create-a-process-template-in-attract"></a>Proceso šablono kūrimas sprendime „Attract“

[!include [banner](includes/banner.md)]

*Samdos proceso šablone* pateikiamos visos veiklos, kurios turėtų būti įtrauktos samdymo į darbo vietą proceso metu. Šioje temoje aprašomi proceso šablono, naudojamo „Microsoft“ „Dynamics 365 Talent: Attract“, elementai. Taip pat paaiškinama, kaip sukurti šabloną.

> [!NOTE]
> Šablonų kūrimas yra išsamios įdarbinimo informacijos priedo, skirto „Attract“ dalis.

## <a name="template-management"></a>Šablonų valdymas

Organizacijos gali nuspręsti, ar proceso šablonus sprendime „Attract“ gali kurti komandos nariai, ar tik administratoriai. Norėdami sukonfigūruoti šablonų valdymą, eikite į parinktį **Administravimo centras** \> **Šablonų valdymas**. Norėdami leisti komandos nariams kurti savo šablonus, įjunkite šablonų valdymą. Jei šablonų valdymo neįjungsite, šablonus kurti galės tik administratoriai.

## <a name="default-template"></a>Numatytasis šablonas

Numatytąjį šabloną nustatyti gali tik administratoriai. Numatytasis šablonas naudojamas tada, jei sukūrus darbą nepasirenkamas šablonas. Norėdami nustatyti numatytąjį šabloną, eikite į parinktį **Administravimo centras** \> **Šablonų valdymas**. Šablono, kurį norite nustatyti numatytuoju, kortelėje pasirinkite elipsės mygtuką (**...**), tada pasirinkite **Nustatyti kaip numatytąjį**.

## <a name="create-a-process-template"></a>Proceso šablono kūrimas

Proceso šablonus gali kurti administratoriai, darbdaviai ir samdos vadovai. Proceso šabloną sudaro *etapai* ir *veiklos*. Etapuose sugrupuota viena arba kelios veiklos. Pagal numatytuosius parametrus, kiekviename proceso šablone pateikiamos potencialaus kliento, prašymo ir pasiūlymo veiklos. Etapus, kuriuose yra šios veiklos, galima pervardyti. Daugiau etapų įtraukti galite pasirinkę **+ Naujas etapas**. Veiklas į etapą įtraukti galite nuvilkdami jas į atitinkamą etapą arba du kartus spustelėdami veiklas veiklų sąraše.

> [!NOTE]
> Etapo pavadinimai kandidatams rodomi puslapyje **Prašymo būsena**. Renkant pavadinimus etapams, reikėtų į šį faktą atsižvelgti.

Norėdami sužinoti daugiau apie veiklas, žr. [Samdos proceso veiklos sprendime „Attract“](./activities-attract.md).

Norėdami sukurti samdos proceso šabloną, atlikite toliau nurodytus veiksmus.

1. Eikite į parinktį **Šablonai**.
2. Pasirinkite **Nauja**.
3. Lauke **šablono pavadinimas** įveskite šablono pavadinimą, tada pasirinkite **Kurti**.
4. Sąraše **Pasirinkite patvirtinimo procesą** pasirinkite **Numatytasis**, kad būtų reikalaujama patvirtinti darbą.
5. Pasirinkite norėdami įgalinti arba išjungti potencialius klientus.
6. Pasirenkama: įtraukite etapus arba juos pašalinkite.

    - Norėdami įtraukti etapą, pasirinkite **+ Naujas etapas**.
    - Norėdami pašalinti etapą, laikykite žymeklį virš etapo, tada pasirinkite pasirodantį šiukšliadėžės mygtuką.

        > [!NOTE]
        > Potencialus kliento, prašymo ir pasiūlymo etapų pašalinti negalima, tačiau juos galima pervardyti.

7. Pasirenkama: įtraukite veiklas arba jas pašalinkite.

    - Norėdami įtraukti veiklą, vilkite ją iš dešinėje pateikto veiklų sąrašo į atitinkamo etapą. Taip pat dukart spustelėkite veiklą ir pasirinkite, į kurį etapą norite ją įtraukti.
    - Norėdami veiklą pašalinti, ją išplėskite, tada veiklos antraštėje pasirinkite šiukšliadėžės mygtuką.

8. Pasirinkite **Įrašyti**.
