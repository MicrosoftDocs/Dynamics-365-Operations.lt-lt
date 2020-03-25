---
title: Įkelti vaizdus
description: Šioje temoje aprašoma, kaip įkelti vaizdus „Microsoft Dynamics 365 Commerce“ svetainės generatoriuje.
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
ms.openlocfilehash: 8571c52b98a87751400dab9482168ee370834bcc
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/03/2020
ms.locfileid: "3097055"
---
# <a name="upload-images"></a><span data-ttu-id="714b6-103">Įkelti vaizdus</span><span class="sxs-lookup"><span data-stu-id="714b6-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="714b6-104">Šioje temoje aprašoma, kaip įkelti vaizdus „Microsoft Dynamics 365 Commerce“ svetainės generatoriuje.</span><span class="sxs-lookup"><span data-stu-id="714b6-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="714b6-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="714b6-105">Overview</span></span>

<span data-ttu-id="714b6-106">„Commerce“ svetainės generatoriaus medijų biblioteka leidžia įkelti vaizdus po vieną arba masiškai naudojant aplankus.</span><span class="sxs-lookup"><span data-stu-id="714b6-106">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="714b6-107">Visada turite įkelti vaizdo, kurio aukščiausia skiriamoji geba ir kokybė, versiją, nes vaizdo dydžio keitimo komponentas automatiškai optimizuos vaizdą skirtingoms peržiūros sritims ir jų stabdos taškams.</span><span class="sxs-lookup"><span data-stu-id="714b6-107">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="714b6-108">Įkėlimo metu nurodyta vaizdo informacija</span><span class="sxs-lookup"><span data-stu-id="714b6-108">Image information specified during upload</span></span>

<span data-ttu-id="714b6-109">Įkėliant vaizdą, galima nurodyti šią informaciją.</span><span class="sxs-lookup"><span data-stu-id="714b6-109">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="714b6-110">**Antraštė, alternatyvusis tekstas, aprašas, raktiniai žodžiai**: vaizdo arba vaizdo įrašo metaduomenys.</span><span class="sxs-lookup"><span data-stu-id="714b6-110">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="714b6-111">Pavadinimas ir alternatyvusis tekstas yra būtinosios vertės.</span><span class="sxs-lookup"><span data-stu-id="714b6-111">Title and alt text are required values.</span></span>
- <span data-ttu-id="714b6-112">**Pasirinkti kategoriją**:</span><span class="sxs-lookup"><span data-stu-id="714b6-112">**Select category**:</span></span>
    - <span data-ttu-id="714b6-113">**Nėra**: naudojama „e-Commerce“ istorijų vaizdui ar vaizdams.</span><span class="sxs-lookup"><span data-stu-id="714b6-113">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="714b6-114">**Produktas, kategorija, klientas, darbuotojas, katalogas**: naudojamas „Dynamics 365 Commerce“ daugiakanalio vaizdui ar vaizdams.</span><span class="sxs-lookup"><span data-stu-id="714b6-114">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="714b6-115">**Publikuoti išteklius po įkėlimo**: pažymėjus šį žymės langelį, vaizdas arba vaizdai publikuojami iš karto po įkėlimo.</span><span class="sxs-lookup"><span data-stu-id="714b6-115">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="714b6-116">Vaizdo ištekliai, kuriems priskirta kategorija, yra taip pat automatiškai žymimi kategorija kaip raktinis žodis, skirtas tam tikros kategorijos ištekliams ieškoti.</span><span class="sxs-lookup"><span data-stu-id="714b6-116">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="714b6-117">Daugiakanalių vaizdų pavadinimo konvencijos</span><span class="sxs-lookup"><span data-stu-id="714b6-117">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="714b6-118">Jei konfigūravote medijos biblioteką kaip daugiakanalio vaizdo posistemį, galite naudoti vaizdo kategorijas, kad nuordytumėte, kuriai kategorijai priklauso įkeltas vaizdas.</span><span class="sxs-lookup"><span data-stu-id="714b6-118">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="714b6-119">Taip pat yra pavadinimų suteikimo konvencijos, kurių reikia laikytis siekiant užtikrinti, kad vaizdai būtų tinkamai nuskaityti kituose kanaluose, pvz., elektroniniame kasos aparate (EKA).</span><span class="sxs-lookup"><span data-stu-id="714b6-119">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="714b6-120">Numatytoji vardų suteikimo konvencija priklauso nuo kategorijos:</span><span class="sxs-lookup"><span data-stu-id="714b6-120">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="714b6-121">Katalogo vaizdai turi būti pavadinti „**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**“</span><span class="sxs-lookup"><span data-stu-id="714b6-121">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="714b6-122">Kategorijos vaizdai turi būti pavadinti „**/Categories/\{CategoryName\}.png**“</span><span class="sxs-lookup"><span data-stu-id="714b6-122">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="714b6-123">Kliento vaizdai turi būti pavadinti „**/Customers/\{CustomerNumber\}.jpg**“</span><span class="sxs-lookup"><span data-stu-id="714b6-123">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="714b6-124">Darbuotojų vaizdai turi būti pavadinti „**/Workers/\{WorkerNumber\}.jpg**“</span><span class="sxs-lookup"><span data-stu-id="714b6-124">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="714b6-125">Produkto vaizdai turi būti pavadinti „**/Products/\{ProductNumber\}_000_001.png**“</span><span class="sxs-lookup"><span data-stu-id="714b6-125">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="714b6-126">001 yra vaizdo seka, kuri gali būti 001, 002, 003, 004 arba 005</span><span class="sxs-lookup"><span data-stu-id="714b6-126">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="714b6-127">Produkto variantų vaizdai turi būti pavadinti „**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**“</span><span class="sxs-lookup"><span data-stu-id="714b6-127">Product variant images should be named "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="714b6-128">Įkelti vaizdą</span><span class="sxs-lookup"><span data-stu-id="714b6-128">Upload an image</span></span>

<span data-ttu-id="714b6-129">Norėdami įkelti vaizdą svetainės generatoriuje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="714b6-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="714b6-130">Kairiojoje naršymo srityje pasirinkite **Medijos biblioteka**.</span><span class="sxs-lookup"><span data-stu-id="714b6-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="714b6-131">Komandų juostoje pasirinkite **įkelti \> Įkelti medijos elementus**.</span><span class="sxs-lookup"><span data-stu-id="714b6-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="714b6-132">Failo naršyklės lange eikite į ir pasirinkite vieną ar daugiau vaizdų failų, kuriuos norite įkelti, tada pasirinkite **Atverti**.</span><span class="sxs-lookup"><span data-stu-id="714b6-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="714b6-133">Dialogo lange **Įkelti medijos elementą** įveskite reikiamą pavadinimą ir alternatyvųjį tekstą.</span><span class="sxs-lookup"><span data-stu-id="714b6-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="714b6-134">Įveskite pasirinktinį aprašą ir raktinius žodžius ir, jei pageidaujama, pasirinkite kategoriją.</span><span class="sxs-lookup"><span data-stu-id="714b6-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="714b6-135">Norėdami iš karto po nusiuntimo publikuoti vaizdus, pažymėkite žymės langelį **Publikuoti medijos elementus po įkėlimo**.</span><span class="sxs-lookup"><span data-stu-id="714b6-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="714b6-136">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="714b6-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="714b6-137">Įkelti vaizdų aplanką</span><span class="sxs-lookup"><span data-stu-id="714b6-137">Upload a folder of images</span></span>

<span data-ttu-id="714b6-138">Norėdami masiškai įkelti vaizdų aplanką svetainės generatoriuje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="714b6-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="714b6-139">Kairiojoje naršymo srityje pasirinkite **Medijos biblioteka**.</span><span class="sxs-lookup"><span data-stu-id="714b6-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="714b6-140">Komandų juostoje pasirinkite **Įkelti \> Įkelti aplanką**.</span><span class="sxs-lookup"><span data-stu-id="714b6-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="714b6-141">Failo naršyklės lange eikite į ir pasirinkite aplanką, kurį norite įkelti, tada pasirinkite **Atverti**.</span><span class="sxs-lookup"><span data-stu-id="714b6-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="714b6-142">Dialogo lange **Įkelti medijos elementus** įveskite pasirinktinius raktinius žodžius ir, jei pageidaujama, pasirinkite kategoriją.</span><span class="sxs-lookup"><span data-stu-id="714b6-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="714b6-143">Norėdami iš karto po nusiuntimo publikuoti aplanke esančius vaizdus, pažymėkite žymės langelį **Publikuoti medijos elementus po įkėlimo**.</span><span class="sxs-lookup"><span data-stu-id="714b6-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="714b6-144">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="714b6-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="714b6-145">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="714b6-145">Additional resources</span></span>

[<span data-ttu-id="714b6-146">Skaitmeninių išteklių valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="714b6-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="714b6-147">Įkelti vaizdo įrašą</span><span class="sxs-lookup"><span data-stu-id="714b6-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="714b6-148">Įkelti failus</span><span class="sxs-lookup"><span data-stu-id="714b6-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="714b6-149">Apkarpyti vaizdai</span><span class="sxs-lookup"><span data-stu-id="714b6-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="714b6-150">Tinkinti centrinius vaizdo taškus</span><span class="sxs-lookup"><span data-stu-id="714b6-150">Customize image focal points</span></span>](dam-custom-focal-point.md)
