---
title: Spausdintuvo ER paskirties vietos tipas
description: Šioje temoje paaiškinama, kaip galite konfigūruoti spausdintuvo paskirties vietą kiekvienam APLANKO ar FAILO komponentui elektroninių ataskaitų (ER) formatu.
author: NickSelin
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 7749a458020de664d00e81ccf0e480ae459da617
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894009"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Spausdintuvo paskirties vieta

[!include [banner](../includes/banner.md)]

Galite siųsti sugeneruotą dokumentą tiesiogiai į tinklo spausdintuvą, kad jis būtų atspausdintas tiesiogiai.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradėdami, turite įdiegti ir sukonfigūruoti Dokumento maršruto planavimo agentą, o paskui užregistruoti tinklo spausdintuvus. Daugiau informacijos žr. [Dokumento maršruto planavimo agento diegimas siekiant įjungti tinklo spausdinimą](./install-document-routing-agent.md).

## <a name="make-the-printer-destination-available"></a>Spausdintuvo paskirties vietos įgalinimas

Norėdami, kad paskirties vieta **Spausdintuvas** būtų prieinama dabartiniame „Microsoft Dynamics 365 Finance“ egzemplioriuje, eikite į darbo sritį **Funkcijų valdymas** ir įjunkite toliau pateikiamas funkcijas nurodyta tvarka.

1. Konvertuoti siunčiamus elektroninių ataskaitų dokumentus iš „Microsoft Office“ formatų („Excel“ / „Word“) į PDF
2. Dokumento maršruto planavimo agentas kaip siunčiamų dokumentų elektroninių ataskaitų teikimo vieta

[![Spausdintuvo paskirties vietos funkcijos įjungimas srityje Funkcijų valdymas](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Taikymas

Paskirties vietą **Spausdintuvas** galima sukonfigūruoti tik failų komponentams, kurie naudojami generuojant išvestį spausdintinu PDF formatu (PDF suliejimo arba PDF failo formato elementai) arba „Microsoft Office Excel“ ar „Word“ formatu („Excel“ failas). Generuojant išvestį PDF formatu, ji siunčiama į spausdintuvą. Generuojant išvestį „Microsoft Office“ formatu, ji automatiškai konvertuojama į PDF formatą, o tada siunčiama į spausdintuvą.

### <a name="limitations"></a>Apribojimai

Paskirties vieta **Spausdintuvas** galima tik naudojant įdiegtis debesyje.

### <a name="use-the-printer-destination"></a>Paskirties vietos Spausdintuvas naudojimas

1. Parinktyje **Įjungta** nustatykite **Taip**, kad sugeneruotas dokumentas būtų nusiųstas į spausdintuvą.
2. Lauke **Spausdintuvo pavadinimas** pasirinkite reikiamą tinklo spausdintuvą.
3. Parinktyje **Įrašyti spausdinimo archyve?** nustatykite **Taip**, norėdami sugeneruotą išvestį saugoti spausdinimo archyve, kad ją būtų galima spausdinti vėliau. Norėdami vėliau peržiūrėti suarchyvuotą išvestį, eikite į **Organizacijos administravimas** \> **Užklausos ir ataskaitos** \> **Ataskaitų archyvas**.

[![Paskirties vietos Spausdintuvas naudojimas](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> Nebūtina įjungti parinktį **Konvertuoti į PDF**, kai konfigūruojate paskirties vietą **Spausdintuvas**. Spausdinant bus konvertuojama į PDF, net jei parinktis yra išjungta.

Norėdami naudoti konkrečią [puslapio padėtį](electronic-reporting-destinations.md#SelectPdfPageOrientation), kai spausdinate siuntimo dokumentą „Excel” formatu, turite įjungti parinktį **Konvertuoti į PDF**. Kai nustatote parinktį **Konvertuoti į PDF** kaip **Taip**, laukas **Puslapio padėtis** tampa pasiekiamas. Lauke **Puslapio padėtis** galite pasirinkti puslapio padėtį.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)
- [Elektroninių ataskaitų (ER) paskirties vietos](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]