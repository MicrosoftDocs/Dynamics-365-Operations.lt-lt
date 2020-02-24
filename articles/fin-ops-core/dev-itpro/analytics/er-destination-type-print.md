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
# <a name="PrinterDestinationType"></a><span data-ttu-id="1dbd9-103">Spausdintuvo paskirties vieta</span><span class="sxs-lookup"><span data-stu-id="1dbd9-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1dbd9-104">Galite siųsti sugeneruotą dokumentą tiesiogiai į tinklo spausdintuvą, kad jis būtų atspausdintas tiesiogiai.</span><span class="sxs-lookup"><span data-stu-id="1dbd9-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1dbd9-105">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="1dbd9-105">Prerequisites</span></span>

<span data-ttu-id="1dbd9-106">Prieš pradėdami, turite įdiegti ir sukonfigūruoti Dokumento maršruto planavimo agentą, o paskui užregistruoti tinklo spausdintuvus.</span><span class="sxs-lookup"><span data-stu-id="1dbd9-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="1dbd9-107">Daugiau informacijos žr. [Dokumento maršruto planavimo agento diegimas siekiant įjungti tinklo spausdinimą](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span><span class="sxs-lookup"><span data-stu-id="1dbd9-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="1dbd9-108">Spausdintuvo paskirties vietos įgalinimas</span><span class="sxs-lookup"><span data-stu-id="1dbd9-108">Make the Printer destination available</span></span>

<span data-ttu-id="1dbd9-109">Norėdami, kad paskirties vieta **Spausdintuvas** būtų prieinama dabartiniame „Microsoft Dynamics 365 Finance“ egzemplioriuje, eikite į darbo sritį **Funkcijų valdymas** ir įjunkite toliau pateikiamas funkcijas nurodyta tvarka.</span><span class="sxs-lookup"><span data-stu-id="1dbd9-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="1dbd9-110">Konvertuoti siunčiamus elektroninių ataskaitų dokumentus iš „Microsoft Office“ formatų („Excel“ / „Word“) į PDF</span><span class="sxs-lookup"><span data-stu-id="1dbd9-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="1dbd9-111">Dokumento maršruto planavimo agentas kaip siunčiamų dokumentų elektroninių ataskaitų teikimo vieta</span><span class="sxs-lookup"><span data-stu-id="1dbd9-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="1dbd9-112">[![Spausdintuvo paskirties vietos funkcijos įjungimas srityje Funkcijų valdymas](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="1dbd9-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="1dbd9-113">Taikymas</span><span class="sxs-lookup"><span data-stu-id="1dbd9-113">Applicability</span></span>

<span data-ttu-id="1dbd9-114">Paskirties vietą **Spausdintuvas** galima sukonfigūruoti tik failų komponentams, kurie naudojami generuojant išvestį spausdintinu PDF formatu (PDF suliejimo arba PDF failo formato elementai) arba „Microsoft Office Excel“ ar „Word“ formatu („Excel“ failas).</span><span class="sxs-lookup"><span data-stu-id="1dbd9-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="1dbd9-115">Generuojant išvestį PDF formatu, ji siunčiama į spausdintuvą.</span><span class="sxs-lookup"><span data-stu-id="1dbd9-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="1dbd9-116">Generuojant išvestį „Microsoft Office“ formatu, ji automatiškai konvertuojama į PDF formatą, o tada siunčiama į spausdintuvą.</span><span class="sxs-lookup"><span data-stu-id="1dbd9-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="1dbd9-117">Apribojimai</span><span class="sxs-lookup"><span data-stu-id="1dbd9-117">Limitations</span></span>

<span data-ttu-id="1dbd9-118">Ši funkcija yra peržiūros funkcija ir jai taikomos naudojimo sąlygos, aprašytos skyriuje [Papildomos „Microsoft Dynamics 365” peržiūrų naudojimo sąlygos](https://go.microsoft.com/fwlink/?linkid=2105274).</span><span class="sxs-lookup"><span data-stu-id="1dbd9-118">This feature is a preview feature and is subject to the terms of use that are described in [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>

<span data-ttu-id="1dbd9-119">Paskirties vieta **Spausdintuvas** galima tik naudojant įdiegtis debesyje.</span><span class="sxs-lookup"><span data-stu-id="1dbd9-119">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="1dbd9-120">Paskirties vietos Spausdintuvas naudojimas</span><span class="sxs-lookup"><span data-stu-id="1dbd9-120">Use the Printer destination</span></span>

1. <span data-ttu-id="1dbd9-121">Parinktyje **Įjungta** nustatykite **Taip**, kad sugeneruotas dokumentas būtų nusiųstas į spausdintuvą.</span><span class="sxs-lookup"><span data-stu-id="1dbd9-121">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="1dbd9-122">Lauke **Spausdintuvo pavadinimas** pasirinkite reikiamą tinklo spausdintuvą.</span><span class="sxs-lookup"><span data-stu-id="1dbd9-122">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="1dbd9-123">Parinktyje **Įrašyti spausdinimo archyve?** nustatykite **Taip**, norėdami sugeneruotą išvestį saugoti spausdinimo archyve, kad ją būtų galima spausdinti vėliau.</span><span class="sxs-lookup"><span data-stu-id="1dbd9-123">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="1dbd9-124">Norėdami vėliau peržiūrėti suarchyvuotą išvestį, eikite į **Organizacijos administravimas** \> **Užklausos ir ataskaitos** \> **Ataskaitų archyvas**.</span><span class="sxs-lookup"><span data-stu-id="1dbd9-124">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="1dbd9-125">[![Paskirties vietos Spausdintuvas naudojimas](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="1dbd9-125">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="1dbd9-126">Nebūtina įjungti parinktį **Konvertuoti į PDF**, kai konfigūruojate paskirties vietą **Spausdintuvas**.</span><span class="sxs-lookup"><span data-stu-id="1dbd9-126">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="1dbd9-127">Spausdinant bus konvertuojama į PDF, net jei parinktis yra išjungta.</span><span class="sxs-lookup"><span data-stu-id="1dbd9-127">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1dbd9-128">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1dbd9-128">Additional resources</span></span>

- [<span data-ttu-id="1dbd9-129">Elektroninių ataskaitų (ER) apžvalga</span><span class="sxs-lookup"><span data-stu-id="1dbd9-129">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="1dbd9-130">Elektroninių ataskaitų (ER) paskirties vietos</span><span class="sxs-lookup"><span data-stu-id="1dbd9-130">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
