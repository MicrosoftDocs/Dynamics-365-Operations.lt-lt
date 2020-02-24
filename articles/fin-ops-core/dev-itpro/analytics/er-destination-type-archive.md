---
title: Archyvo ER paskirties vietos tipas
description: Šioje temoje pateikiama informacija apie tai, kaip sukonfigūruoti elektroninių ataskaitų (ER) formato, kuris sukonfigūruotas siunčiamiems dokumentams generuoti, kiekvieno APLANKO ar FAILO komponento archyvo paskirties vietą.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
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
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 15611a4f0000ca5ccb0ac3f4012251d5bf5689ec
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019908"
---
# <span data-ttu-id="5642d-103"><a name="ArchiveDestinationType">Archyvo paskirties vieta</a></span><span class="sxs-lookup"><span data-stu-id="5642d-103"><a name="ArchiveDestinationType">Archive destination</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5642d-104">Galite sukonfigūruoti elektroninių ataskaitų (ER) formato, kuris sukonfigūruotas siunčiamiems dokumentams generuoti, kiekvieno APLANKO ar FAILO komponento archyvo paskirties vietą.</span><span class="sxs-lookup"><span data-stu-id="5642d-104">You can configure an archive destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="5642d-105">Remiantis paskirties vietos nustatymu, sugeneruotas dokumentas saugomas kaip ER užduočių sąrašo įrašo priedas.</span><span class="sxs-lookup"><span data-stu-id="5642d-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span>

<span data-ttu-id="5642d-106">Šią parinktį galite naudoti, norėdami siųsti sugeneruotą dokumentą į „Microsoft SharePoint“ aplanką arba „Microsoft Azure“ saugyklą.</span><span class="sxs-lookup"><span data-stu-id="5642d-106">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="5642d-107">Nustatykite parinktį **Įgalinta** į **Taip**, norėdami išvestį siųsti į paskirties vietą, kuri nustatoma pagal pasirinkto dokumento tipą.</span><span class="sxs-lookup"><span data-stu-id="5642d-107">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="5642d-108">Pasirinkti galima tik tų tipų dokumentus, kurių grupė nustatyta kaip **Failas**.</span><span class="sxs-lookup"><span data-stu-id="5642d-108">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="5642d-109">Dokumentų [tipus](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) galite nustatyti pasirinkdami **Organizacijos administravimas** \> **Dokumentų valdymas** \> **Dokumentų tipai**.</span><span class="sxs-lookup"><span data-stu-id="5642d-109">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="5642d-110">ER paskirties vietų konfigūracija yra tokia pati, kaip dokumentų valdymo sistemos konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="5642d-110">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="5642d-111">[![Puslapis Dokumentų tipai](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="5642d-111">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="5642d-112">Vieta nurodo, kur failas įrašomas.</span><span class="sxs-lookup"><span data-stu-id="5642d-112">The location determines where the file is saved.</span></span> <span data-ttu-id="5642d-113">Įgalinus paskirties vietą **Archyvas**, rezultatus galima įrašyti užduočių archyve.</span><span class="sxs-lookup"><span data-stu-id="5642d-113">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="5642d-114">Rezultatus galite peržiūrėti pasirinkdami **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Suarchyvuotos elektroninių ataskaitų užduotys**.</span><span class="sxs-lookup"><span data-stu-id="5642d-114">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="5642d-115">Pasirinkite užduočių archyvo dokumento tipą, perėję į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos** \> **Elektroninių ataskaitų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="5642d-115">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="5642d-116">Daugiau informacijos žr. [Elektroninių ataskaitų (ER) sistemos konfigūravimas](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="5642d-116">For more information, [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="5642d-117">„SharePoint“</span><span class="sxs-lookup"><span data-stu-id="5642d-117">SharePoint</span></span>

<span data-ttu-id="5642d-118">Failą galite įrašyti į nustatytą „SharePoint“ aplanką.</span><span class="sxs-lookup"><span data-stu-id="5642d-118">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="5642d-119">Norėdami nustatyti numatytąjį „SharePoint“ serverį, eikite į **Organizacijos administravimas** \> **Dokumentų valdymas** \> **Dokumentų valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="5642d-119">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="5642d-120">Skirtuke **„SharePoint“** sukonfigūruokite „SharePoint“ aplanką.</span><span class="sxs-lookup"><span data-stu-id="5642d-120">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="5642d-121">Tada galite jį pasirinkti kaip aplanką, kuriame bus įrašyta ER išvestis.</span><span class="sxs-lookup"><span data-stu-id="5642d-121">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="5642d-122">**„SharePoint“** vietą reikia pasirinkti šiame dokumento tipe.</span><span class="sxs-lookup"><span data-stu-id="5642d-122">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="5642d-123">[![„SharePoint“ aplanko pasirinkimas](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="5642d-123">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="5642d-124">„Azure“ saugykla</span><span class="sxs-lookup"><span data-stu-id="5642d-124">Azure Storage</span></span>

<span data-ttu-id="5642d-125">Kai nustatyta dokumento tipo vieta yra **„Azure“ saugykla**, galite įrašyti failą į „Azure“ saugyklą.</span><span class="sxs-lookup"><span data-stu-id="5642d-125">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5642d-126">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="5642d-126">Additional resources</span></span>

- [<span data-ttu-id="5642d-127">Elektroninių ataskaitų (ER) apžvalga</span><span class="sxs-lookup"><span data-stu-id="5642d-127">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="5642d-128">Elektroninių ataskaitų (ER) paskirties vietos</span><span class="sxs-lookup"><span data-stu-id="5642d-128">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="5642d-129">Dokumentų valdymo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="5642d-129">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
