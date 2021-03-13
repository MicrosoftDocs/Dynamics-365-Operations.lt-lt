---
title: Produkto informacijos trikties šalinimas
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite dirbdami su produkto informacija.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4c505ccfd1998acd40dbae715c7fa572e315af2e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007521"
---
# <a name="troubleshoot-product-information"></a><span data-ttu-id="46de3-103">Produkto informacijos trikties šalinimas</span><span class="sxs-lookup"><span data-stu-id="46de3-103">Troubleshoot product information</span></span>

<span data-ttu-id="46de3-104">Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite dirbdami su produkto informacija.</span><span class="sxs-lookup"><span data-stu-id="46de3-104">This topic describes how to fix issues that you might encounter while you work with product information.</span></span>

## <a name="i-cant-delete-a-released-product"></a><span data-ttu-id="46de3-105">Negaliu panaikinti išleisto produkto.</span><span class="sxs-lookup"><span data-stu-id="46de3-105">I can't delete a released product.</span></span>

### <a name="issue-description"></a><span data-ttu-id="46de3-106">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="46de3-106">Issue description</span></span>

<span data-ttu-id="46de3-107">Galite panaikinti išleistą produktą ir visus jo variantus tik, jei išleistas produktas neturi jokių susijusių perlaidų.</span><span class="sxs-lookup"><span data-stu-id="46de3-107">You can delete a released product and all its variants only if the released product doesn't have any related transactions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="46de3-108">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="46de3-108">Issue resolution</span></span>

<span data-ttu-id="46de3-109">Atlikite šiuos žingsnius, kad išleistumėte produktą ar pagrindinį produktą.</span><span class="sxs-lookup"><span data-stu-id="46de3-109">Follow these steps to delete a released product or product master.</span></span>

1. <span data-ttu-id="46de3-110">Užverkite visas perlaidas prekei.</span><span class="sxs-lookup"><span data-stu-id="46de3-110">Close all open transactions for the items.</span></span>
1. <span data-ttu-id="46de3-111">Sumažinkite inventorių iki 0 (nulio).</span><span class="sxs-lookup"><span data-stu-id="46de3-111">Reduce the inventory to 0 (zero).</span></span>
1. <span data-ttu-id="46de3-112">Uždarykite inventorių.</span><span class="sxs-lookup"><span data-stu-id="46de3-112">Perform inventory closing.</span></span>
1. <span data-ttu-id="46de3-113">Panaikinkite visus produkto variantus pagrindiniam produktui, kurį norite panaikinti.</span><span class="sxs-lookup"><span data-stu-id="46de3-113">Delete all product variants for the product master that you want to delete.</span></span>

## <a name="can-i-change-the-item-number-of-a-released-product"></a><span data-ttu-id="46de3-114">Ar galiu keisti prekės skaičių išleistam gaminiui?</span><span class="sxs-lookup"><span data-stu-id="46de3-114">Can I change the item number of a released product?</span></span>

<span data-ttu-id="46de3-115">Daugeliu atvejų negalite redaguoti prekės skaičių išleistiems produktams, nes dėl tokio pokyčio duomenys taps užkrėsti.</span><span class="sxs-lookup"><span data-stu-id="46de3-115">In most cases, you can't edit item numbers for released products, because that change will cause data to become corrupted.</span></span> <span data-ttu-id="46de3-116">Galite redaguoti prekės skaičių tik, jei privalote ištaisyti užkrėstus duomenis, kurie kilo dėl anksčiau pervardyto pirminio išleisto produkto rakto, kaip paminėta sąraše [pašalintos ar negaliojančios funkcijos „Finance and Operations“ 10.0.0 su platformos naujinimu 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span><span class="sxs-lookup"><span data-stu-id="46de3-116">You can edit the item number only if you must repair data corruption that was caused by a previous rename of the primary key of that released product, as mentioned in the list of [removed or deprecated features for Finance and Operations 10.0.0 with Platform update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span></span>

<span data-ttu-id="46de3-117">Jei norite galėti redaguoti prekės skaičius išleistiems produktams, [balsuokite už šią idėją idėjų portale](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span><span class="sxs-lookup"><span data-stu-id="46de3-117">If you want to be able to edit item numbers for released products, [vote for this idea in Ideas portal](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span></span>

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a><span data-ttu-id="46de3-118">Nustatytasis nuleidimo principas iš produkto nėra įvedamas į medžiagų važštaraščio eilutę.</span><span class="sxs-lookup"><span data-stu-id="46de3-118">The default flushing principle from the product isn't being entered on the bill of materials line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="46de3-119">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="46de3-119">Issue description</span></span>

<span data-ttu-id="46de3-120">Jums įtraukus prekę į važtaraščio (BOM) eilutę, sistema nenaudoti nustatytojo nuleidimo principo informacijos, kuri yra nustatyta prekei.</span><span class="sxs-lookup"><span data-stu-id="46de3-120">When you add an item to a bill of materials (BOM) line, the system doesn't use the default flushing principle information that is set up for the item.</span></span> <span data-ttu-id="46de3-121">Kitaip tariant, nuleidimo principas iš prekės nepasirodo **BOM eilutės** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="46de3-121">In other words, the flushing principle from the item doesn't appear on the **BOM line** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="46de3-122">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="46de3-122">Issue resolution</span></span>

<span data-ttu-id="46de3-123">Jei nurodote nuleidimo principą BOM eilutėje, jis bus taikomas tai BOM eilutei.</span><span class="sxs-lookup"><span data-stu-id="46de3-123">If you specify a flushing principle on a BOM line, it will apply to that BOM line.</span></span> <span data-ttu-id="46de3-124">Nepaisant to, jei nuleidimo principas yra tuščias arba jis nėra nustatytas BOM eilutėje, nuleidimo principas nustatytas prekėje bus vis tiek tiakomas tai BOM eilute, net jei jis nerodomas BOM eilutėje.</span><span class="sxs-lookup"><span data-stu-id="46de3-124">However, if the flushing principle is blank, or if it isn't set on a BOM line, the flushing principle that is set on the item will still apply to that BOM line, even though it isn't shown on the BOM line.</span></span>

<span data-ttu-id="46de3-125">Nustatytoji logika kitoms funkcijoms „Microsoft Dynamics 365 Supply Chain Management“ dažniausiai neveikia tokiu būdu.</span><span class="sxs-lookup"><span data-stu-id="46de3-125">The defaulting logic for other features in Microsoft Dynamics 365 Supply Chain Management doesn't usually work in this way.</span></span> <span data-ttu-id="46de3-126">Nepaisant to, esamas elgesys negali būti pakeistas.</span><span class="sxs-lookup"><span data-stu-id="46de3-126">However, the current behavior can't be changed.</span></span> <span data-ttu-id="46de3-127">Kitu atveju, kai kurie esantys tinkinimai pagrįsti juo gali sulūžti.</span><span class="sxs-lookup"><span data-stu-id="46de3-127">Otherwise, some existing customizations that rely on it might be broken.</span></span>

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a><span data-ttu-id="46de3-128">Sistema leidžia man įrašyti dublikuotus brūkšninius kodus kitoms prekėms ar tai pačiai prekei su kitokiais matmenimis.</span><span class="sxs-lookup"><span data-stu-id="46de3-128">The system lets me save duplicate bar codes for different items or for the same item that has different dimensions.</span></span>

<span data-ttu-id="46de3-129">Sistema šiuo metu neįpareigoja rengti unikalių brūkštinių kodų ir šio apribojimo priedas sulaužytų keitimą.</span><span class="sxs-lookup"><span data-stu-id="46de3-129">The system doesn't currently enforce unique bar codes, and the addition of this restriction would be a breaking change.</span></span> <span data-ttu-id="46de3-130">Dėl to „Microsoft“ turi įrodymų, kad kai kurie esančių klientų įdiegimai būtų šiuo keitimu pažeisti.</span><span class="sxs-lookup"><span data-stu-id="46de3-130">In fact, Microsoft has evidence that some existing customer installations would be broken by this change.</span></span> <span data-ttu-id="46de3-131">Nepaisant to, atsižvelgsime į platesnį kūrimo pokytį siekiant įjungti šią funkciją ateityje.</span><span class="sxs-lookup"><span data-stu-id="46de3-131">However, we will consider a broader design change to enable this feature in the future.</span></span>

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a><span data-ttu-id="46de3-132">Gaunu tolesnį klaidos pranešimą kai redaguotu prekės įrašo šablonus: „Sandėlio vieta negali būti sukurta dėl to, kad prekė nelaikoma.</span><span class="sxs-lookup"><span data-stu-id="46de3-132">I receive the following error message when I edit item record templates: "The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="46de3-133">Norėdami laikyti prekes, laikomo produkto parinktis susietos prekės modelio grupėje turi būti pasirinkta.“</span><span class="sxs-lookup"><span data-stu-id="46de3-133">To stock items, the Stocked product option on the associated item model group must be selected."</span></span>

### <a name="issue-description"></a><span data-ttu-id="46de3-134">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="46de3-134">Issue description</span></span>

<span data-ttu-id="46de3-135">Jei ši problema atsitinka jums reikia atlikti šiuos žingsnius, kad bandytumėte sukurti šabloną nelaikomai prekei.</span><span class="sxs-lookup"><span data-stu-id="46de3-135">This issue occurs if you follow these steps to try to create a template for an item that isn't stocked.</span></span>

1. <span data-ttu-id="46de3-136">Atverkite išleistą produktą, kuri nėra laikoma.</span><span class="sxs-lookup"><span data-stu-id="46de3-136">Open a released product that isn't stocked.</span></span>
1. <span data-ttu-id="46de3-137">Veiksmų juostoje **Parinktys** skyriuje rinkitės **Įrašo informacija**.</span><span class="sxs-lookup"><span data-stu-id="46de3-137">On the Action Pane, on the **Options** tab, select **Record info**.</span></span>
1. <span data-ttu-id="46de3-138">Teksto laukelyje **Įrašo informacija** rinkitės **Įmonės sąskaitų šablonas**.</span><span class="sxs-lookup"><span data-stu-id="46de3-138">In the **Record information** dialog box, select **Company accounts template**.</span></span>

<span data-ttu-id="46de3-139">Tokiu atveju, gausite tolesnį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="46de3-139">In this case, you receive the following error message:</span></span>

> <span data-ttu-id="46de3-140">Sandėlio vietos sukurti nepavyko dėl to, kad prekė nelaikoma.</span><span class="sxs-lookup"><span data-stu-id="46de3-140">The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="46de3-141">Norėdami laikyti prekes, laikomo produkto parinktis susietos prekės modelio grupėje turi būti pasirinkta.</span><span class="sxs-lookup"><span data-stu-id="46de3-141">To stock items, the Stocked product option on the associated item model group must be selected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="46de3-142">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="46de3-142">Issue resolution</span></span>

<span data-ttu-id="46de3-143">Produkto šablonų sukūrimo procesui reikia papildomo produktu būdingos logikos.</span><span class="sxs-lookup"><span data-stu-id="46de3-143">The process of creating product templates requires extra product-specific logic.</span></span> <span data-ttu-id="46de3-144">Dėl to, negalite naudoti bendro **Bendrovės sąskaitų šablono** mygtuko šiuo tikslu.</span><span class="sxs-lookup"><span data-stu-id="46de3-144">Therefore, you can't use the generic **Company accounts template** button for this purpose.</span></span> <span data-ttu-id="46de3-145">Vietoje to, vadovaukitės šiais žingsniais.</span><span class="sxs-lookup"><span data-stu-id="46de3-145">Instead, follow these steps.</span></span>

1. <span data-ttu-id="46de3-146">Atverkite išleistą produktą.</span><span class="sxs-lookup"><span data-stu-id="46de3-146">Open a released product.</span></span>
1. <span data-ttu-id="46de3-147">Veiksmų juostoje skirtuke **Produktas** grupėje **Naujas** pasirinkite **Šablonas \> Kurti bendrintą šabloną**.</span><span class="sxs-lookup"><span data-stu-id="46de3-147">On the Action Pane, on the **Product** tab, in the **New** group, select **Template \> Create shared template**.</span></span>

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a><span data-ttu-id="46de3-148">Numatytasis pagalbos tekstas yra įtraukiamas į produkto atributus ir neįvedamas į išleistą produktą.</span><span class="sxs-lookup"><span data-stu-id="46de3-148">Default Help text that is added in product attributes isn't entered in a released product.</span></span>

<span data-ttu-id="46de3-149">Aprašymas ir pagalbos tekstas yra įtraukiamas į produkto atributus nėra matomi ar įvedami pagal nutylėjimą išleistuose produktuose.</span><span class="sxs-lookup"><span data-stu-id="46de3-149">A description and Help text that are added in the product attributes aren't visible or entered by default in the released products.</span></span> <span data-ttu-id="46de3-150">Toks veikimo būdas yra numatytas.</span><span class="sxs-lookup"><span data-stu-id="46de3-150">This behavior is by design.</span></span>

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a><span data-ttu-id="46de3-151">Numatytasis kiekis, kuris yra įvedamas skiriasi registruojant iš BOM ir jo registravimo iš BOM versijos metu.</span><span class="sxs-lookup"><span data-stu-id="46de3-151">The default quantity that is entered differs when it's registered from a BOM and when it's registered from a BOM version.</span></span>

### <a name="issue-description"></a><span data-ttu-id="46de3-152">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="46de3-152">Issue description</span></span>

<span data-ttu-id="46de3-153">Pagal nutylėjimą, jums įtraukus elementą į BOM, kiekis nustatomas į 1 vietoje kiekio, kuris nustatytas **Min. užsakymo kiekio** laukelyje **Numatytieji užsakymo nustatymai** puslapyje pasirinktiems produktams.</span><span class="sxs-lookup"><span data-stu-id="46de3-153">By default, when you add an item to a BOM, the quantity is set to 1 instead of the quantity that is defined in the **Min. order quantity** field on the **Default order settings** page for a selected product.</span></span> <span data-ttu-id="46de3-154">Nepaisant to, jums įtraukiant prkę iš BOM versijos ir pasirinkus prekę ir variantą, kiekis įvestas pagal nutylėjimą atsižvelgia į minimalų kiekį, nustatytą numatytuose užsakymo nustatmyusoe konkretiems matmenims.</span><span class="sxs-lookup"><span data-stu-id="46de3-154">However, when you add an item from a BOM version, and the item and variant are selected, the quantity that is entered by default takes into account the minimum quantity that is set in the default order settings for the specific dimensions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="46de3-155">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="46de3-155">Issue resolution</span></span>

<span data-ttu-id="46de3-156">Tikimasi tokio elgesio.</span><span class="sxs-lookup"><span data-stu-id="46de3-156">This behavior is expected.</span></span> <span data-ttu-id="46de3-157">Nepaisant to, žinoma problema yra ta, kad logika skiriasi BOM ir BOM versijose.</span><span class="sxs-lookup"><span data-stu-id="46de3-157">However, the fact that the logic differs in the BOM and the BOM version is a known issue.</span></span> <span data-ttu-id="46de3-158">Nepaisant to, šis elgesys nepasikeis, nes keitimas gali veikti daug skirtingų kliento scenarijų.</span><span class="sxs-lookup"><span data-stu-id="46de3-158">Nevertheless, this behavior won't be changed, because a change could affect many different customer scenarios.</span></span>

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a><span data-ttu-id="46de3-159">Išleisto produkto išsamioje informacijoje, negaliu keisti pridėtų paveikslėlių, kurie buvo įkelti iš produkto dokumento priedų duomenų objekto.</span><span class="sxs-lookup"><span data-stu-id="46de3-159">In the released product details, I can't change the attached images that were uploaded from the Product document attachments data entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="46de3-160">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="46de3-160">Issue description</span></span>

<span data-ttu-id="46de3-161">Ši problema gali atsitikti, kai pridedate paveikslėlį prie prekės naudodami *Produkto dokumento priedų* duomenų objektą.</span><span class="sxs-lookup"><span data-stu-id="46de3-161">This issue can occur when you attach an image to an item by using the *Product document attachments* data entity.</span></span> <span data-ttu-id="46de3-162">Tokiu atveju, prekės paveikslėlis rodomas prekei.</span><span class="sxs-lookup"><span data-stu-id="46de3-162">In this case, the item image is shown for the item.</span></span> <span data-ttu-id="46de3-163">Nepaisant to, jei pasirenkate **Keisti paveikslėlį**, įkeltų paveikslėlių sąraše nerodoma nieko.</span><span class="sxs-lookup"><span data-stu-id="46de3-163">However, if you select **Change image**, nothing is shown in the list of uploaded images.</span></span> <span data-ttu-id="46de3-164">Taip pat, nerodoma jokių priedų prekei.</span><span class="sxs-lookup"><span data-stu-id="46de3-164">Additionally, no attachments are shown for the item.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="46de3-165">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="46de3-165">Issue resolution</span></span>

<span data-ttu-id="46de3-166">Objektas *EcoResProductDocumentAttachmentEntity* importuoja (*Produkto dokumento priedus*) dokumento priedus skirtus *produktams* , o ne *išleistiems produktams*.</span><span class="sxs-lookup"><span data-stu-id="46de3-166">The *EcoResProductDocumentAttachmentEntity* entity (*Product document attachments*) imports document attachments for *products* but not for *released products*.</span></span> <span data-ttu-id="46de3-167">(Išleisti produktai žinomi ir kaip *prekės*.) Norėdami peržiūrėti priedus prekei **Išleisto produkto išsami informacija** puslapyje, privalote naudoti *EcoResReleasedProductDocumentAttachmentEntity* objektą (*Išleisto produkto dokumento priedai*) vietoje to.</span><span class="sxs-lookup"><span data-stu-id="46de3-167">(Released products are also known as *items*.) To view the attachments for an item on the **Released product details** page, you must use the *EcoResReleasedProductDocumentAttachmentEntity* entity (*Released product document attachments*) instead.</span></span>

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a><span data-ttu-id="46de3-168">„Microsoft Flow“ jungtis rodo tolesnį klaidos pranešimą: „Naujinimas neleidžiamas laukeliui 'Produktoskaičius'.“</span><span class="sxs-lookup"><span data-stu-id="46de3-168">The Microsoft Flow connector shows the following error message: "Update not allowed for field 'ProductNumber'."</span></span>

### <a name="issue-description"></a><span data-ttu-id="46de3-169">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="46de3-169">Issue description</span></span>

<span data-ttu-id="46de3-170">Ši problema atsitinka kai bandote naujinti **Produkto skaičių** laukelį naudodami *Išleisti produktai* objektą V2 ir „Microsoft Flow“.</span><span class="sxs-lookup"><span data-stu-id="46de3-170">This issue occurs if you try to update the **Product number** field by using the *Released products* entity V2 and Microsoft Flow.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="46de3-171">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="46de3-171">Issue resolution</span></span>

<span data-ttu-id="46de3-172">Tikimasi tokio elgesio.</span><span class="sxs-lookup"><span data-stu-id="46de3-172">This behavior is expected.</span></span> <span data-ttu-id="46de3-173">Galimybė redaguoti produkto skaičių išleistam produktui buvo panaikinta „Dynamics 365 Finance and Operations“ 10.0.0 su platformos naujiniu 24 siekiant apsisaugoti nuo duomenų sugadinimo.</span><span class="sxs-lookup"><span data-stu-id="46de3-173">The ability to edit the product number for a released product was removed in Dynamics 365 Finance and Operations 10.0.0 with platform update 24 to help prevent data corruption.</span></span> <span data-ttu-id="46de3-174">Atskirais atvejais, kai turite pataisyti sugadintus duomenis, kurie kilo dėl ankstesnio pervardymo pagridninio rakto išleidimo produkto metu, galite prašyti „Microsoft Support“ laikinai panaikinti tokį apribojimą.</span><span class="sxs-lookup"><span data-stu-id="46de3-174">In exceptional cases, where you must repair data corruption that was caused by a previous rename of the primary key of a released product, you can ask Microsoft Support to temporarily remove this restriction.</span></span>

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a><span data-ttu-id="46de3-175">Negaliu išleisti produkto varianto kitu juridniu asmeniu.</span><span class="sxs-lookup"><span data-stu-id="46de3-175">I can't create a released product variant in another legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="46de3-176">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="46de3-176">Issue description</span></span>

<span data-ttu-id="46de3-177">Jei bandote išleisti pagrindinį produktą be variantų, tuomet sukurkite variantus kiekviename juridniame asmenyje (bendrovėje), kaip būtina, jūs negalėsite išleisti variantų naudodami variantų siūlymus.</span><span class="sxs-lookup"><span data-stu-id="46de3-177">If you try to release a product master without variants, and then create the variants in each legal entity (company) as they are required, you won't be able to release the variants by using variant suggestions.</span></span> <span data-ttu-id="46de3-178">Taip pat negalėsite rankiniu būdu kurti variantų.</span><span class="sxs-lookup"><span data-stu-id="46de3-178">You also won't be able to manually create the variants.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="46de3-179">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="46de3-179">Issue resolution</span></span>

<span data-ttu-id="46de3-180">Toks veikimo būdas yra numatytas.</span><span class="sxs-lookup"><span data-stu-id="46de3-180">This behavior is by design.</span></span> <span data-ttu-id="46de3-181">Pagrindinio produkto ryšiai ir matmenys, kuriuos pagrindinis produktas gali paimti laikomi bendrintu lygiu.</span><span class="sxs-lookup"><span data-stu-id="46de3-181">The relations of a product master and the dimensions that the master can take are kept at a shared level.</span></span> <span data-ttu-id="46de3-182">Dėl to, negalite kurti prieinamų matmenų bendrintam produktui konkrečiame juridiniame asmenyje, kuriame tie matmenys išleisti ir tuomet kopijuoti proceso visuose juridiniuose asmenyse, kuriuose būtini matmenys.</span><span class="sxs-lookup"><span data-stu-id="46de3-182">Therefore, you can't create the available dimensions for a shared product master in the specific legal entity where those dimensions are released and then replicate the process in each legal entity where the dimensions are required.</span></span> <span data-ttu-id="46de3-183">Vietoje to, turite keisti išeidimo procesą, kad jis prisiderintų prie nustatyto proceso.</span><span class="sxs-lookup"><span data-stu-id="46de3-183">Instead, you must change your release process to adapt to the designed process.</span></span>

<span data-ttu-id="46de3-184">Čia yra produktų išleidimo procesas.</span><span class="sxs-lookup"><span data-stu-id="46de3-184">Here is the process for releasing products.</span></span>

1. <span data-ttu-id="46de3-185">Sukurkite bendrintą pagrindinį produktą ir matmenis, kuriuos galima išleisti į savo juridinius asmenis.</span><span class="sxs-lookup"><span data-stu-id="46de3-185">Create the shared product master and the dimensions that can be released to the legal entities.</span></span>
1. <span data-ttu-id="46de3-186">Išleiskite produktus į juridinius asmenis pagal naudojamo varianto siūlymus arba rankiniu būdu įtraukdami išleidžiamus derinius.</span><span class="sxs-lookup"><span data-stu-id="46de3-186">Release the products to the legal entities either by using variant suggestions or by manually adding the combinations that should be released.</span></span>

<span data-ttu-id="46de3-187">Kitu būdu, galite tiesiogiai kurti išleistą produktą.</span><span class="sxs-lookup"><span data-stu-id="46de3-187">Alternatively, you can directly create the released product.</span></span>

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a><span data-ttu-id="46de3-188">Išleidžiant variantą kitoje bendrovėje, gaunu šį klaidos pranešimą: „Produkto variantas su nurodytais matmenimis jau buvo sukurtas“.</span><span class="sxs-lookup"><span data-stu-id="46de3-188">When I release a variant in another company, I receive the following error message: "Product variant with specified dimensions has already been created."</span></span>

### <a name="issue-description"></a><span data-ttu-id="46de3-189">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="46de3-189">Issue description</span></span>

<span data-ttu-id="46de3-190">Jei produkto variantas jau buvo išleistas bendrovėje A ir bandote jį išleisti į bendrovę B naudodami **Naują** mygtukas puslapyje **Išleisti produkto variantai**, gausite tolesnį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="46de3-190">If a product variant has already been released in a company A, and you try to release it in company B by using the **New** button on the **Released product variants** page, you will receive the following error message:</span></span>

> <span data-ttu-id="46de3-191">Produkto variantas su nurodytomis dimensijomis jau sukurtas.</span><span class="sxs-lookup"><span data-stu-id="46de3-191">Product variant with specified dimensions has already been created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="46de3-192">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="46de3-192">Issue resolution</span></span>

<span data-ttu-id="46de3-193">Mygtukas **Naujas** puslapyje **Išleisto produkto variantai** sukuria variantą ir išleidžia jį į bendrovės kontekstą.</span><span class="sxs-lookup"><span data-stu-id="46de3-193">The **New** button on the **Released product variants** page creates the variant and releases it in the company context.</span></span> <span data-ttu-id="46de3-194">Jei variantas jau buvo sukurtas, negalite naudoti **Naujas** mygtiko, kad išleistumėte jį į kitą bendrovę.</span><span class="sxs-lookup"><span data-stu-id="46de3-194">If the variant has already been created, you can't use the **New** button to release it in another company.</span></span>

<span data-ttu-id="46de3-195">Norėdami ištaisyti šią problemą, atverkite **Pagrindinio produkto** puslapį ir rinkitės **Išleisti produktą** norėdami išleisti esantį variantą norimoje bendrovėje.</span><span class="sxs-lookup"><span data-stu-id="46de3-195">To fix the issue, open the **Product master** page, and select **Release product** to release the existing variant in the desired company.</span></span>
