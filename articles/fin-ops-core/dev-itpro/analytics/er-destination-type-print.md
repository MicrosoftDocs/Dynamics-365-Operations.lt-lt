---
title: Spausdintuvo ER paskirties vietos tipas
description: Šioje temoje paaiškinama, kaip sukonfigūruoti elektroninių ataskaitų (ER) formato, kuris sukonfigūruotas siunčiamiems dokumentams generuoti PDF arba „Microsoft Office“ formatais („Excel“\„Word“), kiekvieno APLANKO ar FAILO komponento spausdintuvo paskirties vietą.
author: NickSelin
manager: AnnBe
ms.date: 01/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 58e067baa130458e3a8e788d978604f208140a03
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019907"
---
# <a name="PrinterDestinationType"></a>Spausdintuvo paskirties vieta

[!include [banner](../includes/banner.md)]

Galite siųsti sugeneruotą dokumentą tiesiogiai į tinklo spausdintuvą, kad jis būtų atspausdintas tiesiogiai.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradėdami, turite įdiegti ir sukonfigūruoti Dokumento maršruto planavimo agentą, o paskui užregistruoti tinklo spausdintuvus. Daugiau informacijos žr. [Dokumento maršruto planavimo agento diegimas siekiant įjungti tinklo spausdinimą](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).

## <a name="make-the-printer-destination-available"></a>Spausdintuvo paskirties vietos įgalinimas

Norėdami, kad paskirties vieta **Spausdintuvas** būtų prieinama dabartiniame „Microsoft Dynamics 365 Finance“ egzemplioriuje, eikite į darbo sritį **Funkcijų valdymas** ir įjunkite toliau pateikiamas funkcijas nurodyta tvarka.

1. Konvertuoti siunčiamus elektroninių ataskaitų dokumentus iš „Microsoft Office“ formatų („Excel“ / „Word“) į PDF
2. Dokumento maršruto planavimo agentas kaip siunčiamų dokumentų elektroninių ataskaitų teikimo vieta

[![Spausdintuvo paskirties vietos funkcijos įjungimas srityje Funkcijų valdymas](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Taikymas

Paskirties vietą **Spausdintuvas** galima sukonfigūruoti tik failų komponentams, kurie naudojami generuojant išvestį spausdintinu PDF formatu (PDF suliejimo arba PDF failo formato elementai) arba „Microsoft Office Excel“ ar „Word“ formatu („Excel“ failas). Generuojant išvestį PDF formatu, ji siunčiama į spausdintuvą. Generuojant išvestį „Microsoft Office“ formatu, ji automatiškai konvertuojama į PDF formatą, o tada siunčiama į spausdintuvą.

### <a name="limitations"></a>Apribojimai

Ši funkcija yra peržiūros funkcija ir jai taikomos naudojimo sąlygos, aprašytos skyriuje [Papildomos „Microsoft Dynamics 365” peržiūrų naudojimo sąlygos](https://go.microsoft.com/fwlink/?linkid=2105274).

Paskirties vieta **Spausdintuvas** galima tik naudojant įdiegtis debesyje.

### <a name="use-the-printer-destination"></a>Paskirties vietos Spausdintuvas naudojimas

1. Parinktyje **Įjungta** nustatykite **Taip**, kad sugeneruotas dokumentas būtų nusiųstas į spausdintuvą.
2. Lauke **Spausdintuvo pavadinimas** pasirinkite reikiamą tinklo spausdintuvą.
3. Parinktyje **Įrašyti spausdinimo archyve?** nustatykite **Taip**, norėdami sugeneruotą išvestį saugoti spausdinimo archyve, kad ją būtų galima spausdinti vėliau. Norėdami vėliau peržiūrėti suarchyvuotą išvestį, eikite į **Organizacijos administravimas** \> **Užklausos ir ataskaitos** \> **Ataskaitų archyvas**.

[![Paskirties vietos Spausdintuvas naudojimas](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> Nebūtina įjungti parinktį **Konvertuoti į PDF**, kai konfigūruojate paskirties vietą **Spausdintuvas**. Spausdinant bus konvertuojama į PDF, net jei parinktis yra išjungta.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)
- [Elektroninių ataskaitų (ER) paskirties vietos](electronic-reporting-destinations.md)
