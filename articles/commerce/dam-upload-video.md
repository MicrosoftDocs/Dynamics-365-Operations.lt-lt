---
title: Vaizdo įrašų įkėlimas
description: Šioje temoje aprašoma, kaip įkelti vaizdo įrašus „Microsoft Dynamics 365 Commerce“ svetainės generatoriuje.
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
ms.openlocfilehash: 5ec20f8caee2f5a62230be05923dfd52600c1e35
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799210"
---
# <a name="upload-videos"></a><span data-ttu-id="b0f89-103">Vaizdo įrašų įkėlimas</span><span class="sxs-lookup"><span data-stu-id="b0f89-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b0f89-104">Šioje temoje aprašoma, kaip įkelti vaizdo įrašus „Microsoft Dynamics 365 Commerce“ svetainės generatoriuje.</span><span class="sxs-lookup"><span data-stu-id="b0f89-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="b0f89-105">„Commerce“ svetainės generatoriaus medijos biblioteka leidžia įkelti vaizdo įrašus.</span><span class="sxs-lookup"><span data-stu-id="b0f89-105">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="b0f89-106">Visada turite įkelti vaizdo įrašo, kurio aukščiausia sparta bitais ir skiriamoji geba, versiją, nes vaizdo įrašas bus automatiškai konvertuojamas ir bus tinkamas skirtingoms peržiūros sritims ir jų stabdos taškams.</span><span class="sxs-lookup"><span data-stu-id="b0f89-106">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="b0f89-107">Įkėlimo metu nurodyta vaizdo įrašo informacija</span><span class="sxs-lookup"><span data-stu-id="b0f89-107">Video information specified during upload</span></span>

<span data-ttu-id="b0f89-108">Įkeliant vaizdo įrašą galima nurodyti šią informaciją.</span><span class="sxs-lookup"><span data-stu-id="b0f89-108">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="b0f89-109">**Pavadinimas, aprašas, raktiniai žodžiai**: vaizdo įrašo metaduomenys.</span><span class="sxs-lookup"><span data-stu-id="b0f89-109">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="b0f89-110">**Automatiškai generuoti paslėptuosius titrus**: nurodo, ar turi būti automatiškai sugeneruotos paslėptieji vaizdo įrašo titrai.</span><span class="sxs-lookup"><span data-stu-id="b0f89-110">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="b0f89-111">**Paslėptieji titrai**: nurodo naudotinus paslėptuosius titrus.</span><span class="sxs-lookup"><span data-stu-id="b0f89-111">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="b0f89-112">**Įprastas garsas**: nurodo įprastą garso įrašą, kuris bus naudojamas.</span><span class="sxs-lookup"><span data-stu-id="b0f89-112">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="b0f89-113">**Miniatiūra**: nurodo vaizdo įrašo miniatiūrą.</span><span class="sxs-lookup"><span data-stu-id="b0f89-113">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="b0f89-114">Jei miniatiūra nenustatyta, ji bus sugeneruota automatiškai.</span><span class="sxs-lookup"><span data-stu-id="b0f89-114">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="b0f89-115">**Apibūdinamasis garsas**: nurodo apibūdinamąjį garso įrašą, kuris bus naudojamas.</span><span class="sxs-lookup"><span data-stu-id="b0f89-115">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="b0f89-116">Vaizdo įrašo įkėlimas</span><span class="sxs-lookup"><span data-stu-id="b0f89-116">Upload a video</span></span>

<span data-ttu-id="b0f89-117">Norėdami įkelti vaizdo įrašą svetainės generatoriuje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b0f89-117">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="b0f89-118">Kairiojoje naršymo srityje pasirinkite **Medijos biblioteka**.</span><span class="sxs-lookup"><span data-stu-id="b0f89-118">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="b0f89-119">Komandų juostoje pasirinkite **įkelti \> Įkelti medijos elementus**.</span><span class="sxs-lookup"><span data-stu-id="b0f89-119">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="b0f89-120">Failo naršyklės lange eikite į ir pasirinkite vieną ar daugiau vaizdo įrašo failų, kuriuos norite įkelti, tada pasirinkite **Atverti**.</span><span class="sxs-lookup"><span data-stu-id="b0f89-120">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="b0f89-121">Dialogo lange **Įkelti medijos elementą** įveskite reikiamą pavadinimą ir alternatyvųjį tekstą.</span><span class="sxs-lookup"><span data-stu-id="b0f89-121">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="b0f89-122">Įveskite pasirinktinį aprašą ir raktinius žodžius ir, jei pageidaujama, pasirinkite kategoriją.</span><span class="sxs-lookup"><span data-stu-id="b0f89-122">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="b0f89-123">Norėdami iš karto po nusiuntimo publikuoti vaizdus, pažymėkite žymės langelį **Publikuoti medijos elementus po įkėlimo**</span><span class="sxs-lookup"><span data-stu-id="b0f89-123">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="b0f89-124">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b0f89-124">Select **OK**.</span></span>

<span data-ttu-id="b0f89-125">Jei vienu metu įkeliate kelių tipų išteklius (pvz., vaizdus ir vaizdo įrašus), dialogo lange **Įkelti medijos elementą** galėsite nurodyti tik raktinius žodžius, ar failai bus publikuojami iš karto po įkėlimo, ir ar paslėptieji titrai turėtų būti automatiškai sugeneruoti vaizdo įrašams.</span><span class="sxs-lookup"><span data-stu-id="b0f89-125">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="b0f89-126">Visi ištekliai naudos tuos pačius raktinius žodžius.</span><span class="sxs-lookup"><span data-stu-id="b0f89-126">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b0f89-127">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b0f89-127">Additional resources</span></span>

[<span data-ttu-id="b0f89-128">Skaitmeninių išteklių valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="b0f89-128">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="b0f89-129">Vaizdų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="b0f89-129">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="b0f89-130">Įkelti failus</span><span class="sxs-lookup"><span data-stu-id="b0f89-130">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="b0f89-131">Vaizdų apkarpymas</span><span class="sxs-lookup"><span data-stu-id="b0f89-131">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="b0f89-132">Vaizdų centro tinkinimas</span><span class="sxs-lookup"><span data-stu-id="b0f89-132">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="b0f89-133">Naujinti ir aptarnauti statinius failus</span><span class="sxs-lookup"><span data-stu-id="b0f89-133">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
