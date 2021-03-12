---
title: Failų įkelimas, išskyrus vaizdus ir vaizdo įrašus
description: Šioje temoje aprašoma, kaip įkelti dvejetainius failus, išskyrus vaizdus ir vaizdo įrašus, į „Microsoft Dynamics 365 Commerce“ svetainės generatorių.
author: psimolin
manager: annbe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3392f5f36d04e8cb0a9d6e6b7db31ff62c987649
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995775"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="49b83-103">Failų įkelimas, išskyrus vaizdus ir vaizdo įrašus</span><span class="sxs-lookup"><span data-stu-id="49b83-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="49b83-104">Šioje temoje aprašoma, kaip įkelti failus, išskyrus vaizdus ir vaizdo įrašus, į „Microsoft Dynamics 365 Commerce“ svetainės generatorių.</span><span class="sxs-lookup"><span data-stu-id="49b83-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="49b83-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="49b83-105">Overview</span></span>

<span data-ttu-id="49b83-106">„Commerce“ svetainės generatoriaus medijos biblioteka palaiko dvejetainių išteklių, išskyrus vaizdus ar vaizdo įrašus, įkėlimą.</span><span class="sxs-lookup"><span data-stu-id="49b83-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="49b83-107">Pavyzdžiui, galbūt norėsite įkelti „Microsoft Excel“, „Microsoft Word“, „Microsoft PowerPoint“ arba PDF failus.</span><span class="sxs-lookup"><span data-stu-id="49b83-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="49b83-108">Palaikomi toliau nurodyti dokumentų tipai.</span><span class="sxs-lookup"><span data-stu-id="49b83-108">The following document types are supported:</span></span>
- <span data-ttu-id="49b83-109">7Z</span><span class="sxs-lookup"><span data-stu-id="49b83-109">7Z</span></span>
- <span data-ttu-id="49b83-110">AVI</span><span class="sxs-lookup"><span data-stu-id="49b83-110">AVI</span></span>
- <span data-ttu-id="49b83-111">CS</span><span class="sxs-lookup"><span data-stu-id="49b83-111">CS</span></span>
- <span data-ttu-id="49b83-112">„CSS“</span><span class="sxs-lookup"><span data-stu-id="49b83-112">CSS</span></span>
- <span data-ttu-id="49b83-113">DOC</span><span class="sxs-lookup"><span data-stu-id="49b83-113">DOC</span></span>
- <span data-ttu-id="49b83-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="49b83-114">DOCX</span></span>
- <span data-ttu-id="49b83-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="49b83-115">EPUB</span></span>
- <span data-ttu-id="49b83-116">GIF</span><span class="sxs-lookup"><span data-stu-id="49b83-116">GIF</span></span>
- <span data-ttu-id="49b83-117">INDD</span><span class="sxs-lookup"><span data-stu-id="49b83-117">INDD</span></span>
- <span data-ttu-id="49b83-118">JAR</span><span class="sxs-lookup"><span data-stu-id="49b83-118">JAR</span></span>
- <span data-ttu-id="49b83-119">JPG</span><span class="sxs-lookup"><span data-stu-id="49b83-119">JPG</span></span>
- <span data-ttu-id="49b83-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="49b83-120">JPEG</span></span>
- <span data-ttu-id="49b83-121">JS</span><span class="sxs-lookup"><span data-stu-id="49b83-121">JS</span></span>
- <span data-ttu-id="49b83-122">MP3</span><span class="sxs-lookup"><span data-stu-id="49b83-122">MP3</span></span>
- <span data-ttu-id="49b83-123">MP4</span><span class="sxs-lookup"><span data-stu-id="49b83-123">MP4</span></span>
- <span data-ttu-id="49b83-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="49b83-124">MPEG</span></span>
- <span data-ttu-id="49b83-125">MPG</span><span class="sxs-lookup"><span data-stu-id="49b83-125">MPG</span></span>
- <span data-ttu-id="49b83-126">ODP</span><span class="sxs-lookup"><span data-stu-id="49b83-126">ODP</span></span>
- <span data-ttu-id="49b83-127">ODS</span><span class="sxs-lookup"><span data-stu-id="49b83-127">ODS</span></span>
- <span data-ttu-id="49b83-128">ODT</span><span class="sxs-lookup"><span data-stu-id="49b83-128">ODT</span></span>
- <span data-ttu-id="49b83-129">PDF</span><span class="sxs-lookup"><span data-stu-id="49b83-129">PDF</span></span>
- <span data-ttu-id="49b83-130">PNG</span><span class="sxs-lookup"><span data-stu-id="49b83-130">PNG</span></span>
- <span data-ttu-id="49b83-131">PPT</span><span class="sxs-lookup"><span data-stu-id="49b83-131">PPT</span></span>
- <span data-ttu-id="49b83-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="49b83-132">PPTX</span></span>
- <span data-ttu-id="49b83-133">PS</span><span class="sxs-lookup"><span data-stu-id="49b83-133">PS</span></span>
- <span data-ttu-id="49b83-134">QXP</span><span class="sxs-lookup"><span data-stu-id="49b83-134">QXP</span></span>
- <span data-ttu-id="49b83-135">RAR</span><span class="sxs-lookup"><span data-stu-id="49b83-135">RAR</span></span>
- <span data-ttu-id="49b83-136">RTF</span><span class="sxs-lookup"><span data-stu-id="49b83-136">RTF</span></span>
- <span data-ttu-id="49b83-137">SVG</span><span class="sxs-lookup"><span data-stu-id="49b83-137">SVG</span></span>
- <span data-ttu-id="49b83-138">TAR</span><span class="sxs-lookup"><span data-stu-id="49b83-138">TAR</span></span>
- <span data-ttu-id="49b83-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="49b83-139">TGZ</span></span>
- <span data-ttu-id="49b83-140">TXT</span><span class="sxs-lookup"><span data-stu-id="49b83-140">TXT</span></span>
- <span data-ttu-id="49b83-141">WMV</span><span class="sxs-lookup"><span data-stu-id="49b83-141">WMV</span></span>
- <span data-ttu-id="49b83-142">XLS</span><span class="sxs-lookup"><span data-stu-id="49b83-142">XLS</span></span>
- <span data-ttu-id="49b83-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="49b83-143">XLSX</span></span>
- <span data-ttu-id="49b83-144">XML</span><span class="sxs-lookup"><span data-stu-id="49b83-144">XML</span></span>
- <span data-ttu-id="49b83-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="49b83-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="49b83-146">Nusiųsti failą</span><span class="sxs-lookup"><span data-stu-id="49b83-146">Upload a file</span></span>

<span data-ttu-id="49b83-147">Norėdami įkelti failą į „Commerce“ svetainės generatorių, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="49b83-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="49b83-148">Kairiojoje naršymo srityje pasirinkite **Medijos biblioteka**.</span><span class="sxs-lookup"><span data-stu-id="49b83-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="49b83-149">Komandų juostoje pasirinkite **įkelti \> Įkelti medijos elementus**.</span><span class="sxs-lookup"><span data-stu-id="49b83-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="49b83-150">Failų naršyklėje pasirinkite vieną ar daugiau failų ir pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="49b83-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="49b83-151">Dialogo lange **Įkelti medijos elementą** įveskite pavadinimą, aprašymą ir raktinių žodžių metaduomenis, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="49b83-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="49b83-152">Norėdami iš karto po nusiuntimo publikuoti failus, pažymėkite žymės langelį **Publikuoti medijos elementus po įkėlimo**.</span><span class="sxs-lookup"><span data-stu-id="49b83-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="49b83-153">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="49b83-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="49b83-154">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="49b83-154">Additional resources</span></span>

[<span data-ttu-id="49b83-155">Skaitmeninių išteklių valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="49b83-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="49b83-156">Vaizdų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="49b83-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="49b83-157">Vaizdo įrašų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="49b83-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="49b83-158">Vaizdų apkarpymas</span><span class="sxs-lookup"><span data-stu-id="49b83-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="49b83-159">Vaizdų centro tinkinimas</span><span class="sxs-lookup"><span data-stu-id="49b83-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="49b83-160">Naujinti ir aptarnauti statinius failus</span><span class="sxs-lookup"><span data-stu-id="49b83-160">Upload and serve static files</span></span>](upload-serve-static-files.md)
