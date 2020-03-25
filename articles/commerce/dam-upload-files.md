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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: fc0490e3532dcbb9c1e91101009b2d4605315416
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/03/2020
ms.locfileid: "3097054"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="b87d1-103">Failų įkelimas, išskyrus vaizdus ir vaizdo įrašus</span><span class="sxs-lookup"><span data-stu-id="b87d1-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b87d1-104">Šioje temoje aprašoma, kaip įkelti failus, išskyrus vaizdus ir vaizdo įrašus, į „Microsoft Dynamics 365 Commerce“ svetainės generatorių.</span><span class="sxs-lookup"><span data-stu-id="b87d1-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="b87d1-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="b87d1-105">Overview</span></span>

<span data-ttu-id="b87d1-106">„Commerce“ svetainės generatoriaus medijos biblioteka palaiko dvejetainių išteklių, išskyrus vaizdus ar vaizdo įrašus, įkėlimą.</span><span class="sxs-lookup"><span data-stu-id="b87d1-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="b87d1-107">Pavyzdžiui, galbūt norėsite įkelti „Microsoft Excel“, „Microsoft Word“, „Microsoft PowerPoint“ arba PDF failus.</span><span class="sxs-lookup"><span data-stu-id="b87d1-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="b87d1-108">Palaikomi toliau nurodyti dokumentų tipai.</span><span class="sxs-lookup"><span data-stu-id="b87d1-108">The following document types are supported:</span></span>
- <span data-ttu-id="b87d1-109">7Z</span><span class="sxs-lookup"><span data-stu-id="b87d1-109">7Z</span></span>
- <span data-ttu-id="b87d1-110">AVI</span><span class="sxs-lookup"><span data-stu-id="b87d1-110">AVI</span></span>
- <span data-ttu-id="b87d1-111">CS</span><span class="sxs-lookup"><span data-stu-id="b87d1-111">CS</span></span>
- <span data-ttu-id="b87d1-112">„CSS“</span><span class="sxs-lookup"><span data-stu-id="b87d1-112">CSS</span></span>
- <span data-ttu-id="b87d1-113">DOC</span><span class="sxs-lookup"><span data-stu-id="b87d1-113">DOC</span></span>
- <span data-ttu-id="b87d1-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="b87d1-114">DOCX</span></span>
- <span data-ttu-id="b87d1-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="b87d1-115">EPUB</span></span>
- <span data-ttu-id="b87d1-116">GIF</span><span class="sxs-lookup"><span data-stu-id="b87d1-116">GIF</span></span>
- <span data-ttu-id="b87d1-117">INDD</span><span class="sxs-lookup"><span data-stu-id="b87d1-117">INDD</span></span>
- <span data-ttu-id="b87d1-118">JAR</span><span class="sxs-lookup"><span data-stu-id="b87d1-118">JAR</span></span>
- <span data-ttu-id="b87d1-119">JPG</span><span class="sxs-lookup"><span data-stu-id="b87d1-119">JPG</span></span>
- <span data-ttu-id="b87d1-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="b87d1-120">JPEG</span></span>
- <span data-ttu-id="b87d1-121">JS</span><span class="sxs-lookup"><span data-stu-id="b87d1-121">JS</span></span>
- <span data-ttu-id="b87d1-122">MP3</span><span class="sxs-lookup"><span data-stu-id="b87d1-122">MP3</span></span>
- <span data-ttu-id="b87d1-123">MP4</span><span class="sxs-lookup"><span data-stu-id="b87d1-123">MP4</span></span>
- <span data-ttu-id="b87d1-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="b87d1-124">MPEG</span></span>
- <span data-ttu-id="b87d1-125">MPG</span><span class="sxs-lookup"><span data-stu-id="b87d1-125">MPG</span></span>
- <span data-ttu-id="b87d1-126">ODP</span><span class="sxs-lookup"><span data-stu-id="b87d1-126">ODP</span></span>
- <span data-ttu-id="b87d1-127">ODS</span><span class="sxs-lookup"><span data-stu-id="b87d1-127">ODS</span></span>
- <span data-ttu-id="b87d1-128">ODT</span><span class="sxs-lookup"><span data-stu-id="b87d1-128">ODT</span></span>
- <span data-ttu-id="b87d1-129">PDF</span><span class="sxs-lookup"><span data-stu-id="b87d1-129">PDF</span></span>
- <span data-ttu-id="b87d1-130">PNG</span><span class="sxs-lookup"><span data-stu-id="b87d1-130">PNG</span></span>
- <span data-ttu-id="b87d1-131">PPT</span><span class="sxs-lookup"><span data-stu-id="b87d1-131">PPT</span></span>
- <span data-ttu-id="b87d1-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="b87d1-132">PPTX</span></span>
- <span data-ttu-id="b87d1-133">PS</span><span class="sxs-lookup"><span data-stu-id="b87d1-133">PS</span></span>
- <span data-ttu-id="b87d1-134">QXP</span><span class="sxs-lookup"><span data-stu-id="b87d1-134">QXP</span></span>
- <span data-ttu-id="b87d1-135">RAR</span><span class="sxs-lookup"><span data-stu-id="b87d1-135">RAR</span></span>
- <span data-ttu-id="b87d1-136">RTF</span><span class="sxs-lookup"><span data-stu-id="b87d1-136">RTF</span></span>
- <span data-ttu-id="b87d1-137">SVG</span><span class="sxs-lookup"><span data-stu-id="b87d1-137">SVG</span></span>
- <span data-ttu-id="b87d1-138">TAR</span><span class="sxs-lookup"><span data-stu-id="b87d1-138">TAR</span></span>
- <span data-ttu-id="b87d1-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="b87d1-139">TGZ</span></span>
- <span data-ttu-id="b87d1-140">TXT</span><span class="sxs-lookup"><span data-stu-id="b87d1-140">TXT</span></span>
- <span data-ttu-id="b87d1-141">WMV</span><span class="sxs-lookup"><span data-stu-id="b87d1-141">WMV</span></span>
- <span data-ttu-id="b87d1-142">XLS</span><span class="sxs-lookup"><span data-stu-id="b87d1-142">XLS</span></span>
- <span data-ttu-id="b87d1-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="b87d1-143">XLSX</span></span>
- <span data-ttu-id="b87d1-144">XML</span><span class="sxs-lookup"><span data-stu-id="b87d1-144">XML</span></span>
- <span data-ttu-id="b87d1-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="b87d1-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="b87d1-146">Nusiųsti failą</span><span class="sxs-lookup"><span data-stu-id="b87d1-146">Upload a file</span></span>

<span data-ttu-id="b87d1-147">Norėdami įkelti failą į „Commerce“ svetainės generatorių, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b87d1-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="b87d1-148">Kairiojoje naršymo srityje pasirinkite **Medijos biblioteka**.</span><span class="sxs-lookup"><span data-stu-id="b87d1-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="b87d1-149">Komandų juostoje pasirinkite **įkelti \> Įkelti medijos elementus**.</span><span class="sxs-lookup"><span data-stu-id="b87d1-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="b87d1-150">Failų naršyklėje pasirinkite vieną ar daugiau failų ir pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="b87d1-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="b87d1-151">Dialogo lange **Įkelti medijos elementą** įveskite pavadinimą, aprašymą ir raktinių žodžių metaduomenis, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="b87d1-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="b87d1-152">Norėdami iš karto po nusiuntimo publikuoti failus, pažymėkite žymės langelį **Publikuoti medijos elementus po įkėlimo**.</span><span class="sxs-lookup"><span data-stu-id="b87d1-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="b87d1-153">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b87d1-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b87d1-154">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b87d1-154">Additional resources</span></span>

[<span data-ttu-id="b87d1-155">Skaitmeninių išteklių valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="b87d1-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="b87d1-156">Įkelti paveikslėlius</span><span class="sxs-lookup"><span data-stu-id="b87d1-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="b87d1-157">Įkelti vaizdo įrašą</span><span class="sxs-lookup"><span data-stu-id="b87d1-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="b87d1-158">Apkarpyti vaizdai</span><span class="sxs-lookup"><span data-stu-id="b87d1-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="b87d1-159">Tinkinti centrinius vaizdo taškus</span><span class="sxs-lookup"><span data-stu-id="b87d1-159">Customize image focal points</span></span>](dam-custom-focal-point.md)
