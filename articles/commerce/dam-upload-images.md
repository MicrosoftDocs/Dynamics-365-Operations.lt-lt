---
title: Vaizdų nusiuntimas
description: Šioje temoje aprašoma, kaip įkelti vaizdus „Microsoft Dynamics 365 Commerce“ svetainės generatoriuje.
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
ms.openlocfilehash: 2a0a2fdb275cbeb65c06c01128e90ba660f98c9b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799234"
---
# <a name="upload-images"></a><span data-ttu-id="04500-103">Vaizdų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="04500-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="04500-104">Šioje temoje aprašoma, kaip įkelti vaizdus „Microsoft Dynamics 365 Commerce“ svetainės generatoriuje.</span><span class="sxs-lookup"><span data-stu-id="04500-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="04500-105">„Commerce“ svetainės generatoriaus medijų biblioteka leidžia įkelti vaizdus po vieną arba masiškai naudojant aplankus.</span><span class="sxs-lookup"><span data-stu-id="04500-105">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="04500-106">Visada turite įkelti vaizdo, kurio aukščiausia skiriamoji geba ir kokybė, versiją, nes vaizdo dydžio keitimo komponentas automatiškai optimizuos vaizdą skirtingoms peržiūros sritims ir jų stabdos taškams.</span><span class="sxs-lookup"><span data-stu-id="04500-106">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="04500-107">Įkėlimo metu nurodyta vaizdo informacija</span><span class="sxs-lookup"><span data-stu-id="04500-107">Image information specified during upload</span></span>

<span data-ttu-id="04500-108">Įkėliant vaizdą, galima nurodyti šią informaciją.</span><span class="sxs-lookup"><span data-stu-id="04500-108">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="04500-109">**Antraštė, alternatyvusis tekstas, aprašas, raktiniai žodžiai**: vaizdo arba vaizdo įrašo metaduomenys.</span><span class="sxs-lookup"><span data-stu-id="04500-109">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="04500-110">Pavadinimas ir alternatyvusis tekstas yra būtinosios vertės.</span><span class="sxs-lookup"><span data-stu-id="04500-110">Title and alt text are required values.</span></span>
- <span data-ttu-id="04500-111">**Pasirinkti kategoriją**:</span><span class="sxs-lookup"><span data-stu-id="04500-111">**Select category**:</span></span>
    - <span data-ttu-id="04500-112">**Nėra**: naudojama „e-Commerce“ istorijų vaizdui ar vaizdams.</span><span class="sxs-lookup"><span data-stu-id="04500-112">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="04500-113">**Produktas, kategorija, klientas, darbuotojas, katalogas**: naudojamas „Dynamics 365 Commerce“ daugiakanalio vaizdui ar vaizdams.</span><span class="sxs-lookup"><span data-stu-id="04500-113">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="04500-114">**Publikuoti išteklius po įkėlimo**: pažymėjus šį žymės langelį, vaizdas arba vaizdai publikuojami iš karto po įkėlimo.</span><span class="sxs-lookup"><span data-stu-id="04500-114">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="04500-115">Vaizdo ištekliai, kuriems priskirta kategorija, yra taip pat automatiškai žymimi kategorija kaip raktinis žodis, skirtas tam tikros kategorijos ištekliams ieškoti.</span><span class="sxs-lookup"><span data-stu-id="04500-115">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="04500-116">Daugiakanalių vaizdų pavadinimo konvencijos</span><span class="sxs-lookup"><span data-stu-id="04500-116">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="04500-117">Jei konfigūravote medijos biblioteką kaip daugiakanalio vaizdo posistemį, galite naudoti vaizdo kategorijas, kad nuordytumėte, kuriai kategorijai priklauso įkeltas vaizdas.</span><span class="sxs-lookup"><span data-stu-id="04500-117">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="04500-118">Taip pat yra pavadinimų suteikimo konvencijos, kurių reikia laikytis siekiant užtikrinti, kad vaizdai būtų tinkamai nuskaityti kituose kanaluose, pvz., elektroniniame kasos aparate (EKA).</span><span class="sxs-lookup"><span data-stu-id="04500-118">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="04500-119">Numatytoji vardų suteikimo konvencija priklauso nuo kategorijos:</span><span class="sxs-lookup"><span data-stu-id="04500-119">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="04500-120">Katalogo vaizdai turi būti pavadinti „**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**“</span><span class="sxs-lookup"><span data-stu-id="04500-120">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="04500-121">Kategorijos vaizdai turi būti pavadinti „**/Categories/\{CategoryName\}.png**“</span><span class="sxs-lookup"><span data-stu-id="04500-121">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="04500-122">Kliento vaizdai turi būti pavadinti „**/Customers/\{CustomerNumber\}.jpg**“</span><span class="sxs-lookup"><span data-stu-id="04500-122">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="04500-123">Darbuotojų vaizdai turi būti pavadinti „**/Workers/\{WorkerNumber\}.jpg**“</span><span class="sxs-lookup"><span data-stu-id="04500-123">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="04500-124">Produkto vaizdai turi būti pavadinti „**/Products/\{ProductNumber\}_000_001.png**“</span><span class="sxs-lookup"><span data-stu-id="04500-124">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="04500-125">001 yra vaizdo seka, kuri gali būti 001, 002, 003, 004 arba 005</span><span class="sxs-lookup"><span data-stu-id="04500-125">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="04500-126">Produkto varianto vaizdai turi būti pavadinti „**/Produktai/\{Produkto numeris\} \^ \{Stilius\} \^ \{Dydis\} \^ \{Spalva\} \^\_000_001.png**”</span><span class="sxs-lookup"><span data-stu-id="04500-126">Product variant images should be named "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**"</span></span>
    - <span data-ttu-id="04500-127">Pavyzdžiui: 93039 \^\^2 \^ Juoda \^_000_001.png</span><span class="sxs-lookup"><span data-stu-id="04500-127">For example: 93039 \^ \^ 2 \^ Black \^_000_001.png</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="04500-128">Įkelti vaizdą</span><span class="sxs-lookup"><span data-stu-id="04500-128">Upload an image</span></span>

<span data-ttu-id="04500-129">Norėdami įkelti vaizdą svetainės generatoriuje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="04500-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="04500-130">Kairiojoje naršymo srityje pasirinkite **Medijos biblioteka**.</span><span class="sxs-lookup"><span data-stu-id="04500-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="04500-131">Komandų juostoje pasirinkite **įkelti \> Įkelti medijos elementus**.</span><span class="sxs-lookup"><span data-stu-id="04500-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="04500-132">Failo naršyklės lange eikite į ir pasirinkite vieną ar daugiau vaizdų failų, kuriuos norite įkelti, tada pasirinkite **Atverti**.</span><span class="sxs-lookup"><span data-stu-id="04500-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="04500-133">Dialogo lange **Įkelti medijos elementą** įveskite reikiamą pavadinimą ir alternatyvųjį tekstą.</span><span class="sxs-lookup"><span data-stu-id="04500-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="04500-134">Įveskite pasirinktinį aprašą ir raktinius žodžius ir, jei pageidaujama, pasirinkite kategoriją.</span><span class="sxs-lookup"><span data-stu-id="04500-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="04500-135">Norėdami iš karto po nusiuntimo publikuoti vaizdus, pažymėkite žymės langelį **Publikuoti medijos elementus po įkėlimo**.</span><span class="sxs-lookup"><span data-stu-id="04500-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="04500-136">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="04500-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="04500-137">Įkelti vaizdų aplanką</span><span class="sxs-lookup"><span data-stu-id="04500-137">Upload a folder of images</span></span>

<span data-ttu-id="04500-138">Norėdami masiškai įkelti vaizdų aplanką svetainės generatoriuje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="04500-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="04500-139">Kairiojoje naršymo srityje pasirinkite **Medijos biblioteka**.</span><span class="sxs-lookup"><span data-stu-id="04500-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="04500-140">Komandų juostoje pasirinkite **Įkelti \> Įkelti aplanką**.</span><span class="sxs-lookup"><span data-stu-id="04500-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="04500-141">Failo naršyklės lange eikite į ir pasirinkite aplanką, kurį norite įkelti, tada pasirinkite **Atverti**.</span><span class="sxs-lookup"><span data-stu-id="04500-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="04500-142">Dialogo lange **Įkelti medijos elementus** įveskite pasirinktinius raktinius žodžius ir, jei pageidaujama, pasirinkite kategoriją.</span><span class="sxs-lookup"><span data-stu-id="04500-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="04500-143">Norėdami iš karto po nusiuntimo publikuoti aplanke esančius vaizdus, pažymėkite žymės langelį **Publikuoti medijos elementus po įkėlimo**.</span><span class="sxs-lookup"><span data-stu-id="04500-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="04500-144">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="04500-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="04500-145">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="04500-145">Additional resources</span></span>

[<span data-ttu-id="04500-146">Skaitmeninių išteklių valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="04500-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="04500-147">Vaizdo įrašų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="04500-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="04500-148">Įkelti failus</span><span class="sxs-lookup"><span data-stu-id="04500-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="04500-149">Vaizdų apkarpymas</span><span class="sxs-lookup"><span data-stu-id="04500-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="04500-150">Vaizdų centro tinkinimas</span><span class="sxs-lookup"><span data-stu-id="04500-150">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="04500-151">Naujinti ir aptarnauti statinius failus</span><span class="sxs-lookup"><span data-stu-id="04500-151">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
