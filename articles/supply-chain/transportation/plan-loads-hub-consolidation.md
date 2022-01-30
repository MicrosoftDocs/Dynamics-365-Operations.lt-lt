---
title: Krovinių planavimo naudojant tranzito punktų sujungimą apžvalga
description: Šiame straipsnyje aprašomas siuntų konsolidavimas tranzito punkte, kai tam pačiam klientui pristatomos prekės iš skirtingų sandėlių arba kai prekės į tą patį sandėlį pristatomos iš kelių tiekėjų.
author: Henrikan
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, TMSParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "92273"
- intro-internal
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd47a5745719873cc491d93b9a98a7fde609fe38
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985816"
---
# <a name="plan-loads-using-hub-consolidation-overview"></a>Krovinių planavimo naudojant tranzito punktų sujungimą apžvalga

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomas siuntų konsolidavimas tranzito punkte, kai tam pačiam klientui pristatomos prekės iš skirtingų sandėlių arba kai prekės į tą patį sandėlį pristatomos iš kelių tiekėjų.

Gali būti naudinga konsoliduoti siuntas tranzito punkte, kai tam pačiam klientui pristatote prekes iš skirtingų sandėlių arba kai prekės į tą patį sandėlį pristatomos iš kelių tiekėjų.

## <a name="building-loads"></a>Krovinių kūrimas
Norėdami naudoti tranzito punktų konsolidaciją, puslapyje **transporto valdymo parametrai** turite įjungti parinktį **Transportavimo valdymo parametrai**. Taip pat turite sukurti tranzito punktus, kuriuose bus vykdoma konsolidacija. Pateiktoje diagramoje parodytas tranzito punktų konsolidacijos pavyzdys. Šiuo atveju pardavimo užsakymai iš skirtingų sandėlių vykdomi tam pačiam klientu. Pagrindiniai kroviniai kuriami pagal pardavimo užsakymus įprastu būdu, naudojant puslapį **Krovinio planavimo darbo sritis**. Norėdami tranzito punkte konsoliduoti du krovinius prieš juos pristatydami klientui, puslapio **Krovinio planavimo darbo sritis** lauke **Transportavimas** pasirinkite **Tranzito punktų konsolidacija**. Kiekvienam kroviniui parinkus teisingą tranzito punktą, krovinių tranzito punktas bus nustatytas kaip „pridavimo“ paskirties vieta. Puslapio **Krovinio planavimo darbo sritis** dalyje **Tiekimas ir poreikis** taip pat bus pateiktos dvi transportavimo užklausos eilutės. Tada šias dvi eilutes galite įtraukti į naują krovinį. Šiame naujame krovinyje bus abi pardavimo užsakymo eilutės, jo tranzito punktas bus nustatytas kaip „paėmimo“ adresas, o A klientas – kaip „pridavimo“ paskirties vieta. Tada visų trijų krovinių tarifą ir maršrutą bus galima nustatyti kaip bet kurio kito krovinio tarifą ir maršrutą. Galite pasirinkti bet kokį kiekvieno krovinio vežėją, kurį pasiūlys sistema. [![Telkinio konsolidacija.](./media/hubconsol.jpg)](./media/hubconsol.jpg) Taip pat tą patį metodą galite naudoti norėdami konsoliduoti kelių perkėlimo užsakymų krovinius. Šiuo atveju ankstesnėje diagramoje A klientas yra sandėlis. Arba galite konsoliduoti kelių pirkimo užsakymų krovinius, kurie į tą patį sandėlį pristatomi iš įvairių tiekėjų. Galite nustatyti daugiau nei vieną konsolidavimo tranzito punktą, ir papildomus krovinius, gabenamus iš įvairių sandėlių, galite konsoliduoti keliuose tranzito punktuose. Kai sukuriate pagrindinius krovinius ir naudojate tranzito punktų konsolidavimo parinktį, naujus krovinius kurkite naudodami konsoliduoto transportavimo užklausos eilutes. Tada galite nustatyti krovinių tarifą ir maršrutą.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]