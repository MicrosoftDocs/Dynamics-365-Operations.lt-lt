---
title: Spausdintuvo ER paskirties vietos tipas
description: Šioje temoje paaiškinama, kaip sukonfigūruoti elektroninių ataskaitų (ER) formato, kuris sukonfigūruotas siunčiamiems dokumentams generuoti PDF arba „Microsoft Office“ formatais („Excel“\„Word“), kiekvieno APLANKO ar FAILO komponento spausdintuvo paskirties vietą.
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: b7a279dcb30e7681ae654ab17d898a5364391d57
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679611"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a><span data-ttu-id="0ebe7-103">Spausdintuvo paskirties vieta</span><span class="sxs-lookup"><span data-stu-id="0ebe7-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ebe7-104">Galite siųsti sugeneruotą dokumentą tiesiogiai į tinklo spausdintuvą, kad jis būtų atspausdintas tiesiogiai.</span><span class="sxs-lookup"><span data-stu-id="0ebe7-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0ebe7-105">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="0ebe7-105">Prerequisites</span></span>

<span data-ttu-id="0ebe7-106">Prieš pradėdami, turite įdiegti ir sukonfigūruoti Dokumento maršruto planavimo agentą, o paskui užregistruoti tinklo spausdintuvus.</span><span class="sxs-lookup"><span data-stu-id="0ebe7-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="0ebe7-107">Daugiau informacijos žr. [Dokumento maršruto planavimo agento diegimas siekiant įjungti tinklo spausdinimą](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span><span class="sxs-lookup"><span data-stu-id="0ebe7-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="0ebe7-108">Spausdintuvo paskirties vietos įgalinimas</span><span class="sxs-lookup"><span data-stu-id="0ebe7-108">Make the Printer destination available</span></span>

<span data-ttu-id="0ebe7-109">Norėdami, kad paskirties vieta **Spausdintuvas** būtų prieinama dabartiniame „Microsoft Dynamics 365 Finance“ egzemplioriuje, eikite į darbo sritį **Funkcijų valdymas** ir įjunkite toliau pateikiamas funkcijas nurodyta tvarka.</span><span class="sxs-lookup"><span data-stu-id="0ebe7-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="0ebe7-110">Konvertuoti siunčiamus elektroninių ataskaitų dokumentus iš „Microsoft Office“ formatų („Excel“ / „Word“) į PDF</span><span class="sxs-lookup"><span data-stu-id="0ebe7-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="0ebe7-111">Dokumento maršruto planavimo agentas kaip siunčiamų dokumentų elektroninių ataskaitų teikimo vieta</span><span class="sxs-lookup"><span data-stu-id="0ebe7-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="0ebe7-112">[![Spausdintuvo paskirties vietos funkcijos įjungimas srityje Funkcijų valdymas](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="0ebe7-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="0ebe7-113">Taikymas</span><span class="sxs-lookup"><span data-stu-id="0ebe7-113">Applicability</span></span>

<span data-ttu-id="0ebe7-114">Paskirties vietą **Spausdintuvas** galima sukonfigūruoti tik failų komponentams, kurie naudojami generuojant išvestį spausdintinu PDF formatu (PDF suliejimo arba PDF failo formato elementai) arba „Microsoft Office Excel“ ar „Word“ formatu („Excel“ failas).</span><span class="sxs-lookup"><span data-stu-id="0ebe7-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="0ebe7-115">Generuojant išvestį PDF formatu, ji siunčiama į spausdintuvą.</span><span class="sxs-lookup"><span data-stu-id="0ebe7-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="0ebe7-116">Generuojant išvestį „Microsoft Office“ formatu, ji automatiškai konvertuojama į PDF formatą, o tada siunčiama į spausdintuvą.</span><span class="sxs-lookup"><span data-stu-id="0ebe7-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="0ebe7-117">Apribojimai</span><span class="sxs-lookup"><span data-stu-id="0ebe7-117">Limitations</span></span>

<span data-ttu-id="0ebe7-118">Ši funkcija yra peržiūros funkcija ir jai taikomos naudojimo sąlygos, aprašytos skyriuje [Papildomos „Microsoft Dynamics 365” peržiūrų naudojimo sąlygos](https://go.microsoft.com/fwlink/?linkid=2105274).</span><span class="sxs-lookup"><span data-stu-id="0ebe7-118">This feature is a preview feature and is subject to the terms of use that are described in [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>

<span data-ttu-id="0ebe7-119">Paskirties vieta **Spausdintuvas** galima tik naudojant įdiegtis debesyje.</span><span class="sxs-lookup"><span data-stu-id="0ebe7-119">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="0ebe7-120">Paskirties vietos Spausdintuvas naudojimas</span><span class="sxs-lookup"><span data-stu-id="0ebe7-120">Use the Printer destination</span></span>

1. <span data-ttu-id="0ebe7-121">Parinktyje **Įjungta** nustatykite **Taip**, kad sugeneruotas dokumentas būtų nusiųstas į spausdintuvą.</span><span class="sxs-lookup"><span data-stu-id="0ebe7-121">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="0ebe7-122">Lauke **Spausdintuvo pavadinimas** pasirinkite reikiamą tinklo spausdintuvą.</span><span class="sxs-lookup"><span data-stu-id="0ebe7-122">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="0ebe7-123">Parinktyje **Įrašyti spausdinimo archyve?** nustatykite **Taip**, norėdami sugeneruotą išvestį saugoti spausdinimo archyve, kad ją būtų galima spausdinti vėliau.</span><span class="sxs-lookup"><span data-stu-id="0ebe7-123">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="0ebe7-124">Norėdami vėliau peržiūrėti suarchyvuotą išvestį, eikite į **Organizacijos administravimas** \> **Užklausos ir ataskaitos** \> **Ataskaitų archyvas**.</span><span class="sxs-lookup"><span data-stu-id="0ebe7-124">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="0ebe7-125">[![Paskirties vietos Spausdintuvas naudojimas](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="0ebe7-125">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="0ebe7-126">Nebūtina įjungti parinktį **Konvertuoti į PDF**, kai konfigūruojate paskirties vietą **Spausdintuvas**.</span><span class="sxs-lookup"><span data-stu-id="0ebe7-126">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="0ebe7-127">Spausdinant bus konvertuojama į PDF, net jei parinktis yra išjungta.</span><span class="sxs-lookup"><span data-stu-id="0ebe7-127">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

<span data-ttu-id="0ebe7-128">Norėdami naudoti konkrečią [puslapio padėtį](electronic-reporting-destinations.md#SelectPdfPageOrientation), kai spausdinate siuntimo dokumentą „Excel” formatu, turite įjungti parinktį **Konvertuoti į PDF**.</span><span class="sxs-lookup"><span data-stu-id="0ebe7-128">To use a specific [page orientation](electronic-reporting-destinations.md#SelectPdfPageOrientation) when you print an outbound document in Excel format, you must turn on the **Convert to PDF** option.</span></span> <span data-ttu-id="0ebe7-129">Kai nustatote parinktį **Konvertuoti į PDF** kaip **Taip**, laukas **Puslapio padėtis** tampa pasiekiamas.</span><span class="sxs-lookup"><span data-stu-id="0ebe7-129">When you set the **Convert to PDF** option to **Yes**, the **Page orientation** field becomes available.</span></span> <span data-ttu-id="0ebe7-130">Lauke **Puslapio padėtis** galite pasirinkti puslapio padėtį.</span><span class="sxs-lookup"><span data-stu-id="0ebe7-130">In the **Page orientation** field, you can select a page orientation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0ebe7-131">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="0ebe7-131">Additional resources</span></span>

- [<span data-ttu-id="0ebe7-132">Elektroninių ataskaitų (ER) apžvalga</span><span class="sxs-lookup"><span data-stu-id="0ebe7-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="0ebe7-133">Elektroninių ataskaitų (ER) paskirties vietos</span><span class="sxs-lookup"><span data-stu-id="0ebe7-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
