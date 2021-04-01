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
ms.openlocfilehash: c065aa961cf5c2d6770ae47c63a75953e6d38e00
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222542"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="cd4ba-103">Kitų nei vaizdo ir vaizdo įrašų failų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="cd4ba-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cd4ba-104">Šioje temoje aprašoma, kaip įkelti failus, išskyrus vaizdus ir vaizdo įrašus, į „Microsoft Dynamics 365 Commerce“ svetainės generatorių.</span><span class="sxs-lookup"><span data-stu-id="cd4ba-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="cd4ba-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="cd4ba-105">Overview</span></span>

<span data-ttu-id="cd4ba-106">„Commerce“ svetainės generatoriaus medijos biblioteka palaiko dvejetainių išteklių, išskyrus vaizdus ar vaizdo įrašus, įkėlimą.</span><span class="sxs-lookup"><span data-stu-id="cd4ba-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="cd4ba-107">Pavyzdžiui, galbūt norėsite įkelti „Microsoft Excel“, „Microsoft Word“, „Microsoft PowerPoint“ arba PDF failus.</span><span class="sxs-lookup"><span data-stu-id="cd4ba-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="cd4ba-108">Palaikomi toliau nurodyti dokumentų tipai.</span><span class="sxs-lookup"><span data-stu-id="cd4ba-108">The following document types are supported:</span></span>
- <span data-ttu-id="cd4ba-109">7Z</span><span class="sxs-lookup"><span data-stu-id="cd4ba-109">7Z</span></span>
- <span data-ttu-id="cd4ba-110">AVI</span><span class="sxs-lookup"><span data-stu-id="cd4ba-110">AVI</span></span>
- <span data-ttu-id="cd4ba-111">CS</span><span class="sxs-lookup"><span data-stu-id="cd4ba-111">CS</span></span>
- <span data-ttu-id="cd4ba-112">„CSS“</span><span class="sxs-lookup"><span data-stu-id="cd4ba-112">CSS</span></span>
- <span data-ttu-id="cd4ba-113">DOC</span><span class="sxs-lookup"><span data-stu-id="cd4ba-113">DOC</span></span>
- <span data-ttu-id="cd4ba-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="cd4ba-114">DOCX</span></span>
- <span data-ttu-id="cd4ba-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="cd4ba-115">EPUB</span></span>
- <span data-ttu-id="cd4ba-116">GIF</span><span class="sxs-lookup"><span data-stu-id="cd4ba-116">GIF</span></span>
- <span data-ttu-id="cd4ba-117">INDD</span><span class="sxs-lookup"><span data-stu-id="cd4ba-117">INDD</span></span>
- <span data-ttu-id="cd4ba-118">JAR</span><span class="sxs-lookup"><span data-stu-id="cd4ba-118">JAR</span></span>
- <span data-ttu-id="cd4ba-119">JPG</span><span class="sxs-lookup"><span data-stu-id="cd4ba-119">JPG</span></span>
- <span data-ttu-id="cd4ba-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="cd4ba-120">JPEG</span></span>
- <span data-ttu-id="cd4ba-121">JS</span><span class="sxs-lookup"><span data-stu-id="cd4ba-121">JS</span></span>
- <span data-ttu-id="cd4ba-122">MP3</span><span class="sxs-lookup"><span data-stu-id="cd4ba-122">MP3</span></span>
- <span data-ttu-id="cd4ba-123">MP4</span><span class="sxs-lookup"><span data-stu-id="cd4ba-123">MP4</span></span>
- <span data-ttu-id="cd4ba-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="cd4ba-124">MPEG</span></span>
- <span data-ttu-id="cd4ba-125">MPG</span><span class="sxs-lookup"><span data-stu-id="cd4ba-125">MPG</span></span>
- <span data-ttu-id="cd4ba-126">ODP</span><span class="sxs-lookup"><span data-stu-id="cd4ba-126">ODP</span></span>
- <span data-ttu-id="cd4ba-127">ODS</span><span class="sxs-lookup"><span data-stu-id="cd4ba-127">ODS</span></span>
- <span data-ttu-id="cd4ba-128">ODT</span><span class="sxs-lookup"><span data-stu-id="cd4ba-128">ODT</span></span>
- <span data-ttu-id="cd4ba-129">PDF</span><span class="sxs-lookup"><span data-stu-id="cd4ba-129">PDF</span></span>
- <span data-ttu-id="cd4ba-130">PNG</span><span class="sxs-lookup"><span data-stu-id="cd4ba-130">PNG</span></span>
- <span data-ttu-id="cd4ba-131">PPT</span><span class="sxs-lookup"><span data-stu-id="cd4ba-131">PPT</span></span>
- <span data-ttu-id="cd4ba-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="cd4ba-132">PPTX</span></span>
- <span data-ttu-id="cd4ba-133">PS</span><span class="sxs-lookup"><span data-stu-id="cd4ba-133">PS</span></span>
- <span data-ttu-id="cd4ba-134">QXP</span><span class="sxs-lookup"><span data-stu-id="cd4ba-134">QXP</span></span>
- <span data-ttu-id="cd4ba-135">RAR</span><span class="sxs-lookup"><span data-stu-id="cd4ba-135">RAR</span></span>
- <span data-ttu-id="cd4ba-136">RTF</span><span class="sxs-lookup"><span data-stu-id="cd4ba-136">RTF</span></span>
- <span data-ttu-id="cd4ba-137">SVG</span><span class="sxs-lookup"><span data-stu-id="cd4ba-137">SVG</span></span>
- <span data-ttu-id="cd4ba-138">TAR</span><span class="sxs-lookup"><span data-stu-id="cd4ba-138">TAR</span></span>
- <span data-ttu-id="cd4ba-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="cd4ba-139">TGZ</span></span>
- <span data-ttu-id="cd4ba-140">TXT</span><span class="sxs-lookup"><span data-stu-id="cd4ba-140">TXT</span></span>
- <span data-ttu-id="cd4ba-141">WMV</span><span class="sxs-lookup"><span data-stu-id="cd4ba-141">WMV</span></span>
- <span data-ttu-id="cd4ba-142">XLS</span><span class="sxs-lookup"><span data-stu-id="cd4ba-142">XLS</span></span>
- <span data-ttu-id="cd4ba-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="cd4ba-143">XLSX</span></span>
- <span data-ttu-id="cd4ba-144">XML</span><span class="sxs-lookup"><span data-stu-id="cd4ba-144">XML</span></span>
- <span data-ttu-id="cd4ba-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="cd4ba-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="cd4ba-146">Nusiųsti failą</span><span class="sxs-lookup"><span data-stu-id="cd4ba-146">Upload a file</span></span>

<span data-ttu-id="cd4ba-147">Norėdami įkelti failą į „Commerce“ svetainės generatorių, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cd4ba-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="cd4ba-148">Kairiojoje naršymo srityje pasirinkite **Medijos biblioteka**.</span><span class="sxs-lookup"><span data-stu-id="cd4ba-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="cd4ba-149">Komandų juostoje pasirinkite **įkelti \> Įkelti medijos elementus**.</span><span class="sxs-lookup"><span data-stu-id="cd4ba-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="cd4ba-150">Failų naršyklėje pasirinkite vieną ar daugiau failų ir pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="cd4ba-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="cd4ba-151">Dialogo lange **Įkelti medijos elementą** įveskite pavadinimą, aprašymą ir raktinių žodžių metaduomenis, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="cd4ba-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="cd4ba-152">Norėdami iš karto po nusiuntimo publikuoti failus, pažymėkite žymės langelį **Publikuoti medijos elementus po įkėlimo**.</span><span class="sxs-lookup"><span data-stu-id="cd4ba-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="cd4ba-153">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="cd4ba-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cd4ba-154">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="cd4ba-154">Additional resources</span></span>

[<span data-ttu-id="cd4ba-155">Skaitmeninių išteklių valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="cd4ba-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="cd4ba-156">Vaizdų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="cd4ba-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="cd4ba-157">Vaizdo įrašų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="cd4ba-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="cd4ba-158">Vaizdų apkarpymas</span><span class="sxs-lookup"><span data-stu-id="cd4ba-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="cd4ba-159">Vaizdų centro tinkinimas</span><span class="sxs-lookup"><span data-stu-id="cd4ba-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="cd4ba-160">Naujinti ir aptarnauti statinius failus</span><span class="sxs-lookup"><span data-stu-id="cd4ba-160">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]