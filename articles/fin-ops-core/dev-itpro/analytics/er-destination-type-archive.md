---
title: Archyvo ER paskirties vietos tipas
description: Šioje temoje pateikiama informacija apie tai, kaip konfigūruoti archyvo paskirties vietą kiekvienam APLANKO ar FAILO komponentui elektroninių ataskaitų (ER) formatu.
author: NickSelin
ms.date: 11/30/2020
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
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 18c662fee0cedaa55f63ffeb25b0d61ee7baffda
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753533"
---
# <a name="archive-er-destination-type"></a><span data-ttu-id="b8ba7-103">Archyvo ER paskirties vietos tipas</span><span class="sxs-lookup"><span data-stu-id="b8ba7-103">Archive ER destination type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8ba7-104">Galite sukonfigūruoti elektroninių ataskaitų (ER) formato, kuris sukonfigūruotas siunčiamiems dokumentams generuoti, kiekvieno **aplanko** arba **failo** komponento archyvo paskirties vietą.</span><span class="sxs-lookup"><span data-stu-id="b8ba7-104">You can configure an archive destination for each **Folder** or **File** component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="b8ba7-105">Remiantis paskirties vietos nustatymu, sugeneruotas dokumentas saugomas kaip ER užduočių sąrašo įrašo priedas.</span><span class="sxs-lookup"><span data-stu-id="b8ba7-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span> <span data-ttu-id="b8ba7-106">Rezultatus galite peržiūrėti pasirinkdami **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Elektroninių ataskaitų užduotys**.</span><span class="sxs-lookup"><span data-stu-id="b8ba7-106">To view the results, go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>

<span data-ttu-id="b8ba7-107">Šią parinktį galite naudoti, norėdami siųsti sugeneruotą dokumentą į „Microsoft SharePoint“ aplanką arba „Microsoft Azure“ saugyklą.</span><span class="sxs-lookup"><span data-stu-id="b8ba7-107">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="b8ba7-108">Nustatykite parinktį **Įgalinta** į **Taip**, norėdami išvestį siųsti į paskirties vietą, kuri nustatoma pagal pasirinkto dokumento tipą.</span><span class="sxs-lookup"><span data-stu-id="b8ba7-108">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="b8ba7-109">Pasirinkti galima tik tų tipų dokumentus, kurių grupė nustatyta kaip **Failas**.</span><span class="sxs-lookup"><span data-stu-id="b8ba7-109">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="b8ba7-110">Dokumentų [tipus](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) galite nustatyti pasirinkdami **Organizacijos administravimas** \> **Dokumentų valdymas** \> **Dokumentų tipai**.</span><span class="sxs-lookup"><span data-stu-id="b8ba7-110">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="b8ba7-111">ER paskirties vietų konfigūracija yra tokia pati, kaip dokumentų valdymo sistemos konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="b8ba7-111">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="b8ba7-112">[![Puslapis Dokumentų tipai](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="b8ba7-112">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="b8ba7-113">Vieta nurodo, kur failas įrašomas.</span><span class="sxs-lookup"><span data-stu-id="b8ba7-113">The location determines where the file is saved.</span></span> <span data-ttu-id="b8ba7-114">Įgalinus paskirties vietą **Archyvas**, rezultatus galima įrašyti užduočių archyve.</span><span class="sxs-lookup"><span data-stu-id="b8ba7-114">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="b8ba7-115">Rezultatus galite peržiūrėti pasirinkdami **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Suarchyvuotos elektroninių ataskaitų užduotys**.</span><span class="sxs-lookup"><span data-stu-id="b8ba7-115">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="b8ba7-116">Pasirinkite užduočių archyvo dokumento tipą, perėję į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos** \> **Elektroninių ataskaitų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="b8ba7-116">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="b8ba7-117">Daugiau informacijos žr. [Elektroninių ataskaitų (ER) sistemos konfigūravimas](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="b8ba7-117">For more information, see [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="b8ba7-118">„SharePoint“</span><span class="sxs-lookup"><span data-stu-id="b8ba7-118">SharePoint</span></span>

<span data-ttu-id="b8ba7-119">Failą galite įrašyti į nustatytą „SharePoint“ aplanką.</span><span class="sxs-lookup"><span data-stu-id="b8ba7-119">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="b8ba7-120">Norėdami nustatyti numatytąjį „SharePoint“ serverį, eikite į **Organizacijos administravimas** \> **Dokumentų valdymas** \> **Dokumentų valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="b8ba7-120">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="b8ba7-121">Skirtuke **„SharePoint“** sukonfigūruokite „SharePoint“ aplanką.</span><span class="sxs-lookup"><span data-stu-id="b8ba7-121">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="b8ba7-122">Tada galite jį pasirinkti kaip aplanką, kuriame bus įrašyta ER išvestis.</span><span class="sxs-lookup"><span data-stu-id="b8ba7-122">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="b8ba7-123">**„SharePoint“** vietą reikia pasirinkti šiame dokumento tipe.</span><span class="sxs-lookup"><span data-stu-id="b8ba7-123">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="b8ba7-124">[![„SharePoint“ aplanko pasirinkimas](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="b8ba7-124">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="b8ba7-125">„Azure“ saugykla</span><span class="sxs-lookup"><span data-stu-id="b8ba7-125">Azure Storage</span></span>

<span data-ttu-id="b8ba7-126">Kai nustatyta dokumento tipo vieta yra **„Azure“ saugykla**, galite įrašyti failą į „Azure“ saugyklą.</span><span class="sxs-lookup"><span data-stu-id="b8ba7-126">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

> [!NOTE] 
> <span data-ttu-id="b8ba7-127">ER sistema failus nuolat saugo „Azure“ didelių dvejetainių objektų saugykloje – skirtingai nuo duomenų valdymo sistemos, kuri taiko septynių dienų saugojimo strategiją dokumentams, kuriuos reikia apdoroti.</span><span class="sxs-lookup"><span data-stu-id="b8ba7-127">The ER framework permanently stores files in Azure Blob storage unlike the Data management framework that applies the seven-day retention policy for documents that must be processed.</span></span> <span data-ttu-id="b8ba7-128">Norėdami gauti daugiau informacijos, žr. [Pranešimų būsenos gavimo API](../data-entities/recurring-integrations.md#api-for-getting-message-status)ir [būsenos tikrinimo API ](../data-entities/data-management-api.md#status-check-api).</span><span class="sxs-lookup"><span data-stu-id="b8ba7-128">For more information, see [API for getting message status](../data-entities/recurring-integrations.md#api-for-getting-message-status) and [Status check API](../data-entities/data-management-api.md#status-check-api).</span></span> <span data-ttu-id="b8ba7-129">Su ER susiję failai bus saugomi „Azure“ didelių dvejetainių objektų saugykloje kaip programos lentelės įrašų priedai, kiek reikės.</span><span class="sxs-lookup"><span data-stu-id="b8ba7-129">The ER-related files will be stored in Azure Blob storage as attachments of application table records as long as necessary.</span></span> <span data-ttu-id="b8ba7-130">Vienas failas bus panaikintas iš „Azure“ didelių dvejetainių objektų saugyklos kartu su programos lentelės įrašu, prie kurio pridėtas šis failas.</span><span class="sxs-lookup"><span data-stu-id="b8ba7-130">A single file will be deleted from Azure Blob storage along with the application table record that this file was attached to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b8ba7-131">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b8ba7-131">Additional resources</span></span>

- [<span data-ttu-id="b8ba7-132">Elektroninių ataskaitų (ER) apžvalga</span><span class="sxs-lookup"><span data-stu-id="b8ba7-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="b8ba7-133">Elektroninių ataskaitų (ER) paskirties vietos</span><span class="sxs-lookup"><span data-stu-id="b8ba7-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="b8ba7-134">Dokumentų valdymo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="b8ba7-134">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]