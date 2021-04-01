---
title: Vaizdo įrašų įkėlimas
description: Šioje temoje aprašoma, kaip įkelti vaizdo įrašus „Microsoft Dynamics 365 Commerce“ svetainės generatoriuje.
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
ms.openlocfilehash: d74e7116d68074bfc917784a8f51f85d5682c5d6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213847"
---
# <a name="upload-videos"></a><span data-ttu-id="3074a-103">Vaizdo įrašų įkėlimas</span><span class="sxs-lookup"><span data-stu-id="3074a-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3074a-104">Šioje temoje aprašoma, kaip įkelti vaizdo įrašus „Microsoft Dynamics 365 Commerce“ svetainės generatoriuje.</span><span class="sxs-lookup"><span data-stu-id="3074a-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="3074a-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="3074a-105">Overview</span></span>

<span data-ttu-id="3074a-106">„Commerce“ svetainės generatoriaus medijos biblioteka leidžia įkelti vaizdo įrašus.</span><span class="sxs-lookup"><span data-stu-id="3074a-106">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="3074a-107">Visada turite įkelti vaizdo įrašo, kurio aukščiausia sparta bitais ir skiriamoji geba, versiją, nes vaizdo įrašas bus automatiškai konvertuojamas ir bus tinkamas skirtingosm peržiūros sritims ir jų stabdos taškams.</span><span class="sxs-lookup"><span data-stu-id="3074a-107">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="3074a-108">Įkėlimo metu nurodyta vaizdo įrašo informacija</span><span class="sxs-lookup"><span data-stu-id="3074a-108">Video information specified during upload</span></span>

<span data-ttu-id="3074a-109">Įkėliant vaizdo įrašą, galima nurodyti šią informaciją.</span><span class="sxs-lookup"><span data-stu-id="3074a-109">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="3074a-110">**Pavadinimas, aprašas, raktiniai žodžiai**: vaizdo įrašo metaduomenys.</span><span class="sxs-lookup"><span data-stu-id="3074a-110">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="3074a-111">**Automatiškai generuoti paslėptuosius titrus**: nurodo, ar turi būti automatiškai sugeneruotos paslėptieji vaizdo įrašo titrai.</span><span class="sxs-lookup"><span data-stu-id="3074a-111">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="3074a-112">**Paslėptieji titrai**: nurodo naudotinus paslėptuosius titrus.</span><span class="sxs-lookup"><span data-stu-id="3074a-112">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="3074a-113">**Įprastas garsas**: nurodo įprastą garso įrašą, kuris bus naudojamas.</span><span class="sxs-lookup"><span data-stu-id="3074a-113">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="3074a-114">**Miniatiūra**: nurodo vaizdo įrašo miniatiūrą.</span><span class="sxs-lookup"><span data-stu-id="3074a-114">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="3074a-115">Jei miniatiūra nenustatyta, ji bus sugeneruota automatiškai.</span><span class="sxs-lookup"><span data-stu-id="3074a-115">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="3074a-116">**Apibūdinamasis garsas**: nurodo apibūdinamąjį garso įrašą, kuris bus naudojamas.</span><span class="sxs-lookup"><span data-stu-id="3074a-116">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="3074a-117">Vaizdo įrašo įkėlimas</span><span class="sxs-lookup"><span data-stu-id="3074a-117">Upload a video</span></span>

<span data-ttu-id="3074a-118">Norėdami įkelti vaizdo įrašą svetainės generatoriuje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3074a-118">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="3074a-119">Kairiojoje naršymo srityje pasirinkite **Medijos biblioteka**.</span><span class="sxs-lookup"><span data-stu-id="3074a-119">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="3074a-120">Komandų juostoje pasirinkite **įkelti \> Įkelti medijos elementus**.</span><span class="sxs-lookup"><span data-stu-id="3074a-120">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="3074a-121">Failo naršyklės lange eikite į ir pasirinkite vieną ar daugiau vaizdo įrašo failų, kuriuos norite įkelti, tada pasirinkite **Atverti**.</span><span class="sxs-lookup"><span data-stu-id="3074a-121">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="3074a-122">Dialogo lange **Įkelti medijos elementą** įveskite reikiamą pavadinimą ir alternatyvųjį tekstą.</span><span class="sxs-lookup"><span data-stu-id="3074a-122">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="3074a-123">Įveskite pasirinktinį aprašą ir raktinius žodžius ir, jei pageidaujama, pasirinkite kategoriją.</span><span class="sxs-lookup"><span data-stu-id="3074a-123">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="3074a-124">Norėdami iš karto po nusiuntimo publikuoti vaizdus, pažymėkite žymės langelį **Publikuoti medijos elementus po įkėlimo**</span><span class="sxs-lookup"><span data-stu-id="3074a-124">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="3074a-125">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3074a-125">Select **OK**.</span></span>

<span data-ttu-id="3074a-126">Jei vienu metu įkeliate kelių tipų išteklius (pvz., vaizdus ir vaizdo įrašus), dialogo lange **Įkelti medijos elementą** galėsite nurodyti tik raktinius žodžius, ar failai bus publikuojami iš karto po įkėlimo, ir ar paslėptieji titrai turėtų būti automatiškai sugeneruoti vaizdo įrašams.</span><span class="sxs-lookup"><span data-stu-id="3074a-126">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="3074a-127">Visi ištekliai naudos tuos pačius raktinius žodžius.</span><span class="sxs-lookup"><span data-stu-id="3074a-127">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3074a-128">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3074a-128">Additional resources</span></span>

[<span data-ttu-id="3074a-129">Skaitmeninių išteklių valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="3074a-129">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="3074a-130">Vaizdų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="3074a-130">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="3074a-131">Įkelti failus</span><span class="sxs-lookup"><span data-stu-id="3074a-131">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="3074a-132">Vaizdų apkarpymas</span><span class="sxs-lookup"><span data-stu-id="3074a-132">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="3074a-133">Vaizdų centro tinkinimas</span><span class="sxs-lookup"><span data-stu-id="3074a-133">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="3074a-134">Naujinti ir aptarnauti statinius failus</span><span class="sxs-lookup"><span data-stu-id="3074a-134">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]