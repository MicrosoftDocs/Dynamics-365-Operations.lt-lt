---
title: Failų įkėlimas, išskyrus vaizdus ir vaizdo įrašus
description: Šioje temoje aprašoma, kaip įkelti dvejetainius failus, išskyrus vaizdus ir vaizdo įrašus, į „Microsoft Dynamics 365 Commerce“ svetainės generatorių.
author: psimolin
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 380bcccd1053cbcc276e964ce97f16d1d39ea75a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799258"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="66917-103">Kitų nei vaizdo ir vaizdo įrašų failų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="66917-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="66917-104">Šioje temoje aprašoma, kaip įkelti failus, išskyrus vaizdus ir vaizdo įrašus, į „Microsoft Dynamics 365 Commerce“ svetainės generatorių.</span><span class="sxs-lookup"><span data-stu-id="66917-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="66917-105">„Commerce“ svetainės generatoriaus medijos biblioteka palaiko dvejetainių išteklių, išskyrus vaizdus ar vaizdo įrašus, įkėlimą.</span><span class="sxs-lookup"><span data-stu-id="66917-105">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="66917-106">Pavyzdžiui, galbūt norėsite įkelti „Microsoft Excel“, „Microsoft Word“, „Microsoft PowerPoint“ arba PDF failus.</span><span class="sxs-lookup"><span data-stu-id="66917-106">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="66917-107">Palaikomi toliau nurodyti dokumentų tipai.</span><span class="sxs-lookup"><span data-stu-id="66917-107">The following document types are supported:</span></span>
- <span data-ttu-id="66917-108">7Z</span><span class="sxs-lookup"><span data-stu-id="66917-108">7Z</span></span>
- <span data-ttu-id="66917-109">AVI</span><span class="sxs-lookup"><span data-stu-id="66917-109">AVI</span></span>
- <span data-ttu-id="66917-110">CS</span><span class="sxs-lookup"><span data-stu-id="66917-110">CS</span></span>
- <span data-ttu-id="66917-111">„CSS“</span><span class="sxs-lookup"><span data-stu-id="66917-111">CSS</span></span>
- <span data-ttu-id="66917-112">DOC</span><span class="sxs-lookup"><span data-stu-id="66917-112">DOC</span></span>
- <span data-ttu-id="66917-113">DOCX</span><span class="sxs-lookup"><span data-stu-id="66917-113">DOCX</span></span>
- <span data-ttu-id="66917-114">EPUB</span><span class="sxs-lookup"><span data-stu-id="66917-114">EPUB</span></span>
- <span data-ttu-id="66917-115">GIF</span><span class="sxs-lookup"><span data-stu-id="66917-115">GIF</span></span>
- <span data-ttu-id="66917-116">INDD</span><span class="sxs-lookup"><span data-stu-id="66917-116">INDD</span></span>
- <span data-ttu-id="66917-117">JAR</span><span class="sxs-lookup"><span data-stu-id="66917-117">JAR</span></span>
- <span data-ttu-id="66917-118">JPG</span><span class="sxs-lookup"><span data-stu-id="66917-118">JPG</span></span>
- <span data-ttu-id="66917-119">JPEG</span><span class="sxs-lookup"><span data-stu-id="66917-119">JPEG</span></span>
- <span data-ttu-id="66917-120">JS</span><span class="sxs-lookup"><span data-stu-id="66917-120">JS</span></span>
- <span data-ttu-id="66917-121">MP3</span><span class="sxs-lookup"><span data-stu-id="66917-121">MP3</span></span>
- <span data-ttu-id="66917-122">MP4</span><span class="sxs-lookup"><span data-stu-id="66917-122">MP4</span></span>
- <span data-ttu-id="66917-123">MPEG</span><span class="sxs-lookup"><span data-stu-id="66917-123">MPEG</span></span>
- <span data-ttu-id="66917-124">MPG</span><span class="sxs-lookup"><span data-stu-id="66917-124">MPG</span></span>
- <span data-ttu-id="66917-125">ODP</span><span class="sxs-lookup"><span data-stu-id="66917-125">ODP</span></span>
- <span data-ttu-id="66917-126">ODS</span><span class="sxs-lookup"><span data-stu-id="66917-126">ODS</span></span>
- <span data-ttu-id="66917-127">ODT</span><span class="sxs-lookup"><span data-stu-id="66917-127">ODT</span></span>
- <span data-ttu-id="66917-128">PDF</span><span class="sxs-lookup"><span data-stu-id="66917-128">PDF</span></span>
- <span data-ttu-id="66917-129">PNG</span><span class="sxs-lookup"><span data-stu-id="66917-129">PNG</span></span>
- <span data-ttu-id="66917-130">PPT</span><span class="sxs-lookup"><span data-stu-id="66917-130">PPT</span></span>
- <span data-ttu-id="66917-131">PPTX</span><span class="sxs-lookup"><span data-stu-id="66917-131">PPTX</span></span>
- <span data-ttu-id="66917-132">PS</span><span class="sxs-lookup"><span data-stu-id="66917-132">PS</span></span>
- <span data-ttu-id="66917-133">QXP</span><span class="sxs-lookup"><span data-stu-id="66917-133">QXP</span></span>
- <span data-ttu-id="66917-134">RAR</span><span class="sxs-lookup"><span data-stu-id="66917-134">RAR</span></span>
- <span data-ttu-id="66917-135">RTF</span><span class="sxs-lookup"><span data-stu-id="66917-135">RTF</span></span>
- <span data-ttu-id="66917-136">SVG</span><span class="sxs-lookup"><span data-stu-id="66917-136">SVG</span></span>
- <span data-ttu-id="66917-137">TAR</span><span class="sxs-lookup"><span data-stu-id="66917-137">TAR</span></span>
- <span data-ttu-id="66917-138">TGZ</span><span class="sxs-lookup"><span data-stu-id="66917-138">TGZ</span></span>
- <span data-ttu-id="66917-139">TXT</span><span class="sxs-lookup"><span data-stu-id="66917-139">TXT</span></span>
- <span data-ttu-id="66917-140">WMV</span><span class="sxs-lookup"><span data-stu-id="66917-140">WMV</span></span>
- <span data-ttu-id="66917-141">XLS</span><span class="sxs-lookup"><span data-stu-id="66917-141">XLS</span></span>
- <span data-ttu-id="66917-142">XLSX</span><span class="sxs-lookup"><span data-stu-id="66917-142">XLSX</span></span>
- <span data-ttu-id="66917-143">XML</span><span class="sxs-lookup"><span data-stu-id="66917-143">XML</span></span>
- <span data-ttu-id="66917-144">ZIP</span><span class="sxs-lookup"><span data-stu-id="66917-144">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="66917-145">Nusiųsti failą</span><span class="sxs-lookup"><span data-stu-id="66917-145">Upload a file</span></span>

<span data-ttu-id="66917-146">Norėdami įkelti failą į „Commerce“ svetainės generatorių, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="66917-146">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="66917-147">Kairiojoje naršymo srityje pasirinkite **Medijos biblioteka**.</span><span class="sxs-lookup"><span data-stu-id="66917-147">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="66917-148">Komandų juostoje pasirinkite **įkelti \> Įkelti medijos elementus**.</span><span class="sxs-lookup"><span data-stu-id="66917-148">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="66917-149">Failų naršyklėje pasirinkite vieną ar daugiau failų ir pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="66917-149">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="66917-150">Dialogo lange **Įkelti medijos elementą** įveskite pavadinimą, aprašymą ir raktinių žodžių metaduomenis, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="66917-150">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="66917-151">Norėdami iš karto po nusiuntimo publikuoti failus, pažymėkite žymės langelį **Publikuoti medijos elementus po įkėlimo**.</span><span class="sxs-lookup"><span data-stu-id="66917-151">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="66917-152">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="66917-152">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="66917-153">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="66917-153">Additional resources</span></span>

[<span data-ttu-id="66917-154">Skaitmeninių išteklių valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="66917-154">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="66917-155">Vaizdų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="66917-155">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="66917-156">Vaizdo įrašų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="66917-156">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="66917-157">Vaizdų apkarpymas</span><span class="sxs-lookup"><span data-stu-id="66917-157">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="66917-158">Vaizdų centro tinkinimas</span><span class="sxs-lookup"><span data-stu-id="66917-158">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="66917-159">Naujinti ir aptarnauti statinius failus</span><span class="sxs-lookup"><span data-stu-id="66917-159">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
