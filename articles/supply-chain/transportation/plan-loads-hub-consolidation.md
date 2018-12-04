---
title: "Krovinių planavimas naudojant tranzito punktų konsolidaciją"
description: "Šiame straipsnyje aprašomas siuntų konsolidavimas tranzito punkte, kai tam pačiam klientui pristatomos prekės iš skirtingų sandėlių arba kai prekės į tą patį sandėlį pristatomos iš kelių tiekėjų."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 475fa9b73deeddd0f9118b0062e834a053fcb919
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="plan-loads-using-hub-consolidation"></a>Krovinių planavimas naudojant tranzito punktų konsolidaciją

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomas siuntų konsolidavimas tranzito punkte, kai tam pačiam klientui pristatomos prekės iš skirtingų sandėlių arba kai prekės į tą patį sandėlį pristatomos iš kelių tiekėjų.

Gali būti naudinga konsoliduoti siuntas tranzito punkte, kai tam pačiam klientui pristatote prekes iš skirtingų sandėlių arba kai prekės į tą patį sandėlį pristatomos iš kelių tiekėjų.

## <a name="building-loads"></a>Krovinių kūrimas
Norėdami naudoti tranzito punktų konsolidaciją, puslapyje **transporto valdymo parametrai** turite įjungti parinktį **Transportavimo valdymo parametrai**. Taip pat turite sukurti tranzito punktus, kuriuose bus vykdoma konsolidacija. Pateiktoje diagramoje parodytas tranzito punktų konsolidacijos pavyzdys. Šiuo atveju pardavimo užsakymai iš skirtingų sandėlių vykdomi tam pačiam klientu. Pagrindiniai kroviniai kuriami pagal pardavimo užsakymus įprastu būdu, naudojant puslapį **Krovinio planavimo darbo sritis**. Norėdami tranzito punkte konsoliduoti du krovinius prieš juos pristatydami klientui, puslapio **Krovinio planavimo darbo sritis** lauke **Transportavimas** pasirinkite **Tranzito punktų konsolidacija**. Kiekvienam kroviniui parinkus teisingą tranzito punktą, krovinių tranzito punktas bus nustatytas kaip „pridavimo“ paskirties vieta. Puslapio **Krovinio planavimo darbo sritis** dalyje **Tiekimas ir poreikis** taip pat bus pateiktos dvi transportavimo užklausos eilutės. Tada šias dvi eilutes galite įtraukti į naują krovinį. Šiame naujame krovinyje bus abi pardavimo užsakymo eilutės, jo tranzito punktas bus nustatytas kaip „paėmimo“ adresas, o A klientas – kaip „pridavimo“ paskirties vieta. Tada visų trijų krovinių tarifą ir maršrutą bus galima nustatyti kaip bet kurio kito krovinio tarifą ir maršrutą. Galite pasirinkti bet kokį kiekvieno krovinio vežėją, kurį pasiūlys sistema. [![Tranzito punktų konsolidacija](./media/hubconsol.jpg)](./media/hubconsol.jpg) Taip pat tą patį metodą galite naudoti norėdami konsoliduoti kelių perkėlimo užsakymų krovinius. Šiuo atveju ankstesnėje diagramoje A klientas yra sandėlis. Arba galite konsoliduoti kelių pirkimo užsakymų krovinius, kurie į tą patį sandėlį pristatomi iš įvairių tiekėjų. Galite nustatyti daugiau nei vieną konsolidavimo tranzito punktą, ir papildomus krovinius, gabenamus iš įvairių sandėlių, galite konsoliduoti keliuose tranzito punktuose. Kai sukuriate pagrindinius krovinius ir naudojate tranzito punktų konsolidavimo parinktį, naujus krovinius kurkite naudodami konsoliduoto transportavimo užklausos eilutes. Tada galite nustatyti krovinių tarifą ir maršrutą.




