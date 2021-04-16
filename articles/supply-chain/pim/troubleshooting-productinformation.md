---
title: Produkto informacijos trikties šalinimas
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite dirbdami su produkto informacija.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a05e9957363ef6a659e25ceba84a168507cd641a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841532"
---
# <a name="troubleshoot-product-information"></a><span data-ttu-id="3797e-103">Produkto informacijos trikties šalinimas</span><span class="sxs-lookup"><span data-stu-id="3797e-103">Troubleshoot product information</span></span>

<span data-ttu-id="3797e-104">Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite dirbdami su produkto informacija.</span><span class="sxs-lookup"><span data-stu-id="3797e-104">This topic describes how to fix issues that you might encounter while you work with product information.</span></span>

## <a name="i-cant-delete-a-released-product"></a><span data-ttu-id="3797e-105">Negaliu panaikinti išleisto produkto.</span><span class="sxs-lookup"><span data-stu-id="3797e-105">I can't delete a released product.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3797e-106">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="3797e-106">Issue description</span></span>

<span data-ttu-id="3797e-107">Galite panaikinti išleistą produktą ir visus jo variantus tik, jei išleistas produktas neturi jokių susijusių perlaidų.</span><span class="sxs-lookup"><span data-stu-id="3797e-107">You can delete a released product and all its variants only if the released product doesn't have any related transactions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3797e-108">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="3797e-108">Issue resolution</span></span>

<span data-ttu-id="3797e-109">Atlikite šiuos žingsnius, kad išleistumėte produktą ar pagrindinį produktą.</span><span class="sxs-lookup"><span data-stu-id="3797e-109">Follow these steps to delete a released product or product master.</span></span>

1. <span data-ttu-id="3797e-110">Užverkite visas perlaidas prekei.</span><span class="sxs-lookup"><span data-stu-id="3797e-110">Close all open transactions for the items.</span></span>
1. <span data-ttu-id="3797e-111">Sumažinkite inventorių iki 0 (nulio).</span><span class="sxs-lookup"><span data-stu-id="3797e-111">Reduce the inventory to 0 (zero).</span></span>
1. <span data-ttu-id="3797e-112">Uždarykite inventorių.</span><span class="sxs-lookup"><span data-stu-id="3797e-112">Perform inventory closing.</span></span>
1. <span data-ttu-id="3797e-113">Panaikinkite visus produkto variantus pagrindiniam produktui, kurį norite panaikinti.</span><span class="sxs-lookup"><span data-stu-id="3797e-113">Delete all product variants for the product master that you want to delete.</span></span>

## <a name="can-i-change-the-item-number-of-a-released-product"></a><span data-ttu-id="3797e-114">Ar galiu keisti prekės skaičių išleistam gaminiui?</span><span class="sxs-lookup"><span data-stu-id="3797e-114">Can I change the item number of a released product?</span></span>

<span data-ttu-id="3797e-115">Daugeliu atvejų negalite redaguoti prekės skaičių išleistiems produktams, nes dėl tokio pokyčio duomenys taps užkrėsti.</span><span class="sxs-lookup"><span data-stu-id="3797e-115">In most cases, you can't edit item numbers for released products, because that change will cause data to become corrupted.</span></span> <span data-ttu-id="3797e-116">Galite redaguoti prekės skaičių tik, jei privalote ištaisyti užkrėstus duomenis, kurie kilo dėl anksčiau pervardyto pirminio išleisto produkto rakto, kaip paminėta sąraše [pašalintos ar negaliojančios funkcijos „Finance and Operations“ 10.0.0 su platformos naujinimu 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span><span class="sxs-lookup"><span data-stu-id="3797e-116">You can edit the item number only if you must repair data corruption that was caused by a previous rename of the primary key of that released product, as mentioned in the list of [removed or deprecated features for Finance and Operations 10.0.0 with Platform update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span></span>

<span data-ttu-id="3797e-117">Jei norite galėti redaguoti prekės skaičius išleistiems produktams, [balsuokite už šią idėją idėjų portale](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span><span class="sxs-lookup"><span data-stu-id="3797e-117">If you want to be able to edit item numbers for released products, [vote for this idea in Ideas portal](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span></span>

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a><span data-ttu-id="3797e-118">Nustatytasis nuleidimo principas iš produkto nėra įvedamas į komplektavimo specifikacijos eilutę.</span><span class="sxs-lookup"><span data-stu-id="3797e-118">The default flushing principle from the product isn't being entered on the bill of materials line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3797e-119">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="3797e-119">Issue description</span></span>

<span data-ttu-id="3797e-120">Jums įtraukus prekę į važtaraščio (KS) eilutę, sistema nenaudoti nustatytojo nuleidimo principo informacijos, kuri yra nustatyta prekei.</span><span class="sxs-lookup"><span data-stu-id="3797e-120">When you add an item to a bill of materials (BOM) line, the system doesn't use the default flushing principle information that is set up for the item.</span></span> <span data-ttu-id="3797e-121">Kitaip tariant, nuleidimo principas iš prekės nepasirodo **KS eilutės** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="3797e-121">In other words, the flushing principle from the item doesn't appear on the **BOM line** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3797e-122">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="3797e-122">Issue resolution</span></span>

<span data-ttu-id="3797e-123">Jei nurodote nuleidimo principą KS eilutėje, jis bus taikomas tai KS eilutei.</span><span class="sxs-lookup"><span data-stu-id="3797e-123">If you specify a flushing principle on a BOM line, it will apply to that BOM line.</span></span> <span data-ttu-id="3797e-124">Nepaisant to, jei nuleidimo principas yra tuščias arba jis nėra nustatytas KS eilutėje, nuleidimo principas nustatytas prekėje bus vis tiek taikomas tai KS eilute, net jei jis nerodomas KS eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3797e-124">However, if the flushing principle is blank, or if it isn't set on a BOM line, the flushing principle that is set on the item will still apply to that BOM line, even though it isn't shown on the BOM line.</span></span>

<span data-ttu-id="3797e-125">Nustatytoji logika kitoms funkcijoms „Microsoft Dynamics 365 Supply Chain Management“ dažniausiai neveikia tokiu būdu.</span><span class="sxs-lookup"><span data-stu-id="3797e-125">The defaulting logic for other features in Microsoft Dynamics 365 Supply Chain Management doesn't usually work in this way.</span></span> <span data-ttu-id="3797e-126">Nepaisant to, esamas elgesys negali būti pakeistas.</span><span class="sxs-lookup"><span data-stu-id="3797e-126">However, the current behavior can't be changed.</span></span> <span data-ttu-id="3797e-127">Kitu atveju, kai kurie esantys tinkinimai pagrįsti juo gali sulūžti.</span><span class="sxs-lookup"><span data-stu-id="3797e-127">Otherwise, some existing customizations that rely on it might be broken.</span></span>

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a><span data-ttu-id="3797e-128">Sistema leidžia man įrašyti dublikuotus brūkšninius kodus kitoms prekėms ar tai pačiai prekei su kitokiais matmenimis.</span><span class="sxs-lookup"><span data-stu-id="3797e-128">The system lets me save duplicate bar codes for different items or for the same item that has different dimensions.</span></span>

<span data-ttu-id="3797e-129">Sistema šiuo metu neįpareigoja rengti unikalių brūkšninių kodų ir šio apribojimo priedas sulaužytų keitimą.</span><span class="sxs-lookup"><span data-stu-id="3797e-129">The system doesn't currently enforce unique bar codes, and the addition of this restriction would be a breaking change.</span></span> <span data-ttu-id="3797e-130">Dėl to „Microsoft“ turi įrodymų, kad kai kurie esančių klientų įdiegimai būtų šiuo keitimu pažeisti.</span><span class="sxs-lookup"><span data-stu-id="3797e-130">In fact, Microsoft has evidence that some existing customer installations would be broken by this change.</span></span> <span data-ttu-id="3797e-131">Nepaisant to, atsižvelgsime į platesnį kūrimo pokytį siekiant įjungti šią funkciją ateityje.</span><span class="sxs-lookup"><span data-stu-id="3797e-131">However, we will consider a broader design change to enable this feature in the future.</span></span>

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a><span data-ttu-id="3797e-132">Gaunu tolesnį klaidos pranešimą kai redaguotu prekės įrašo šablonus: „Sandėlio vieta negali būti sukurta dėl to, kad prekė nelaikoma.</span><span class="sxs-lookup"><span data-stu-id="3797e-132">I receive the following error message when I edit item record templates: "The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="3797e-133">Norėdami laikyti prekes, laikomo produkto parinktis susietos prekės modelio grupėje turi būti pasirinkta.“</span><span class="sxs-lookup"><span data-stu-id="3797e-133">To stock items, the Stocked product option on the associated item model group must be selected."</span></span>

### <a name="issue-description"></a><span data-ttu-id="3797e-134">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="3797e-134">Issue description</span></span>

<span data-ttu-id="3797e-135">Jei ši problema atsitinka jums reikia atlikti šiuos žingsnius, kad bandytumėte sukurti šabloną nelaikomai prekei.</span><span class="sxs-lookup"><span data-stu-id="3797e-135">This issue occurs if you follow these steps to try to create a template for an item that isn't stocked.</span></span>

1. <span data-ttu-id="3797e-136">Atverkite išleistą produktą, kuri nėra laikoma.</span><span class="sxs-lookup"><span data-stu-id="3797e-136">Open a released product that isn't stocked.</span></span>
1. <span data-ttu-id="3797e-137">Veiksmų juostoje **Parinktys** skyriuje rinkitės **Įrašo informacija**.</span><span class="sxs-lookup"><span data-stu-id="3797e-137">On the Action Pane, on the **Options** tab, select **Record info**.</span></span>
1. <span data-ttu-id="3797e-138">Teksto laukelyje **Įrašo informacija** rinkitės **Įmonės sąskaitų šablonas**.</span><span class="sxs-lookup"><span data-stu-id="3797e-138">In the **Record information** dialog box, select **Company accounts template**.</span></span>

<span data-ttu-id="3797e-139">Tokiu atveju, gausite tolesnį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="3797e-139">In this case, you receive the following error message:</span></span>

> <span data-ttu-id="3797e-140">Sandėlio vietos sukurti nepavyko dėl to, kad prekė nelaikoma.</span><span class="sxs-lookup"><span data-stu-id="3797e-140">The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="3797e-141">Norėdami laikyti prekes, laikomo produkto parinktis susietos prekės modelio grupėje turi būti pasirinkta.</span><span class="sxs-lookup"><span data-stu-id="3797e-141">To stock items, the Stocked product option on the associated item model group must be selected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3797e-142">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="3797e-142">Issue resolution</span></span>

<span data-ttu-id="3797e-143">Produkto šablonų sukūrimo procesui reikia papildomo produktu būdingos logikos.</span><span class="sxs-lookup"><span data-stu-id="3797e-143">The process of creating product templates requires extra product-specific logic.</span></span> <span data-ttu-id="3797e-144">Dėl to, negalite naudoti bendro **Bendrovės sąskaitų šablono** mygtuko šiuo tikslu.</span><span class="sxs-lookup"><span data-stu-id="3797e-144">Therefore, you can't use the generic **Company accounts template** button for this purpose.</span></span> <span data-ttu-id="3797e-145">Vietoje to, vadovaukitės šiais žingsniais.</span><span class="sxs-lookup"><span data-stu-id="3797e-145">Instead, follow these steps.</span></span>

1. <span data-ttu-id="3797e-146">Atverkite išleistą produktą.</span><span class="sxs-lookup"><span data-stu-id="3797e-146">Open a released product.</span></span>
1. <span data-ttu-id="3797e-147">Veiksmų juostoje skirtuke **Produktas** grupėje **Naujas** pasirinkite **Šablonas \> Kurti bendrintą šabloną**.</span><span class="sxs-lookup"><span data-stu-id="3797e-147">On the Action Pane, on the **Product** tab, in the **New** group, select **Template \> Create shared template**.</span></span>

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a><span data-ttu-id="3797e-148">Numatytasis pagalbos tekstas yra įtraukiamas į produkto atributus ir neįvedamas į išleistą produktą.</span><span class="sxs-lookup"><span data-stu-id="3797e-148">Default Help text that is added in product attributes isn't entered in a released product.</span></span>

<span data-ttu-id="3797e-149">Aprašymas ir pagalbos tekstas yra įtraukiamas į produkto atributus nėra matomi ar įvedami pagal nutylėjimą išleistuose produktuose.</span><span class="sxs-lookup"><span data-stu-id="3797e-149">A description and Help text that are added in the product attributes aren't visible or entered by default in the released products.</span></span> <span data-ttu-id="3797e-150">Toks veikimo būdas yra numatytas.</span><span class="sxs-lookup"><span data-stu-id="3797e-150">This behavior is by design.</span></span>

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a><span data-ttu-id="3797e-151">Numatytasis kiekis, kuris yra įvedamas skiriasi registruojant iš KS ir jo registravimo iš KS versijos metu.</span><span class="sxs-lookup"><span data-stu-id="3797e-151">The default quantity that is entered differs when it's registered from a BOM and when it's registered from a BOM version.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3797e-152">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="3797e-152">Issue description</span></span>

<span data-ttu-id="3797e-153">Pagal nutylėjimą, jums įtraukus elementą į KS, kiekis nustatomas į 1 vietoje kiekio, kuris nustatytas **Min. užsakymo kiekio** laukelyje **Numatytieji užsakymo nustatymai** puslapyje pasirinktiems produktams.</span><span class="sxs-lookup"><span data-stu-id="3797e-153">By default, when you add an item to a BOM, the quantity is set to 1 instead of the quantity that is defined in the **Min. order quantity** field on the **Default order settings** page for a selected product.</span></span> <span data-ttu-id="3797e-154">Nepaisant to, jums įtraukiant prekę iš KS versijos ir pasirinkus prekę ir variantą, kiekis įvestas pagal nutylėjimą atsižvelgia į minimalų kiekį, nustatytą numatytuose užsakymo nustatymuose konkretiems matmenims.</span><span class="sxs-lookup"><span data-stu-id="3797e-154">However, when you add an item from a BOM version, and the item and variant are selected, the quantity that is entered by default takes into account the minimum quantity that is set in the default order settings for the specific dimensions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3797e-155">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="3797e-155">Issue resolution</span></span>

<span data-ttu-id="3797e-156">Tikimasi tokio elgesio.</span><span class="sxs-lookup"><span data-stu-id="3797e-156">This behavior is expected.</span></span> <span data-ttu-id="3797e-157">Nepaisant to, žinoma problema yra ta, kad logika skiriasi KS ir KS versijose.</span><span class="sxs-lookup"><span data-stu-id="3797e-157">However, the fact that the logic differs in the BOM and the BOM version is a known issue.</span></span> <span data-ttu-id="3797e-158">Nepaisant to, šis elgesys nepasikeis, nes keitimas gali veikti daug skirtingų kliento scenarijų.</span><span class="sxs-lookup"><span data-stu-id="3797e-158">Nevertheless, this behavior won't be changed, because a change could affect many different customer scenarios.</span></span>

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a><span data-ttu-id="3797e-159">Išleisto produkto išsamioje informacijoje, negaliu keisti pridėtų paveikslėlių, kurie buvo įkelti iš produkto dokumento priedų duomenų objekto.</span><span class="sxs-lookup"><span data-stu-id="3797e-159">In the released product details, I can't change the attached images that were uploaded from the Product document attachments data entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3797e-160">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="3797e-160">Issue description</span></span>

<span data-ttu-id="3797e-161">Ši problema gali atsitikti, kai pridedate paveikslėlį prie prekės naudodami *Produkto dokumento priedų* duomenų objektą.</span><span class="sxs-lookup"><span data-stu-id="3797e-161">This issue can occur when you attach an image to an item by using the *Product document attachments* data entity.</span></span> <span data-ttu-id="3797e-162">Tokiu atveju, prekės paveikslėlis rodomas prekei.</span><span class="sxs-lookup"><span data-stu-id="3797e-162">In this case, the item image is shown for the item.</span></span> <span data-ttu-id="3797e-163">Nepaisant to, jei pasirenkate **Keisti paveikslėlį**, įkeltų paveikslėlių sąraše nerodoma nieko.</span><span class="sxs-lookup"><span data-stu-id="3797e-163">However, if you select **Change image**, nothing is shown in the list of uploaded images.</span></span> <span data-ttu-id="3797e-164">Taip pat, nerodoma jokių priedų prekei.</span><span class="sxs-lookup"><span data-stu-id="3797e-164">Additionally, no attachments are shown for the item.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3797e-165">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="3797e-165">Issue resolution</span></span>

<span data-ttu-id="3797e-166">Objektas *EcoResProductDocumentAttachmentEntity* importuoja (*Produkto dokumento priedus*) dokumento priedus skirtus *produktams* , o ne *išleistiems produktams*.</span><span class="sxs-lookup"><span data-stu-id="3797e-166">The *EcoResProductDocumentAttachmentEntity* entity (*Product document attachments*) imports document attachments for *products* but not for *released products*.</span></span> <span data-ttu-id="3797e-167">(Išleisti produktai žinomi ir kaip *prekės*.) Norėdami peržiūrėti priedus prekei **Išleisto produkto išsami informacija** puslapyje, privalote naudoti *EcoResReleasedProductDocumentAttachmentEntity* objektą (*Išleisto produkto dokumento priedai*) vietoje to.</span><span class="sxs-lookup"><span data-stu-id="3797e-167">(Released products are also known as *items*.) To view the attachments for an item on the **Released product details** page, you must use the *EcoResReleasedProductDocumentAttachmentEntity* entity (*Released product document attachments*) instead.</span></span>

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a><span data-ttu-id="3797e-168">„Microsoft Flow“ jungtis rodo tolesnį klaidos pranešimą: „Naujinimas neleidžiamas laukeliui 'Produkto numeris'.“</span><span class="sxs-lookup"><span data-stu-id="3797e-168">The Microsoft Flow connector shows the following error message: "Update not allowed for field 'ProductNumber'."</span></span>

### <a name="issue-description"></a><span data-ttu-id="3797e-169">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="3797e-169">Issue description</span></span>

<span data-ttu-id="3797e-170">Ši problema atsitinka kai bandote naujinti **Produkto skaičių** laukelį naudodami *Išleisti produktai* objektą V2 ir „Microsoft Flow“.</span><span class="sxs-lookup"><span data-stu-id="3797e-170">This issue occurs if you try to update the **Product number** field by using the *Released products* entity V2 and Microsoft Flow.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3797e-171">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="3797e-171">Issue resolution</span></span>

<span data-ttu-id="3797e-172">Tikimasi tokio elgesio.</span><span class="sxs-lookup"><span data-stu-id="3797e-172">This behavior is expected.</span></span> <span data-ttu-id="3797e-173">Galimybė redaguoti produkto skaičių išleistam produktui buvo panaikinta „Dynamics 365 Finance and Operations“ 10.0.0 su platformos naujiniu 24 siekiant apsisaugoti nuo duomenų sugadinimo.</span><span class="sxs-lookup"><span data-stu-id="3797e-173">The ability to edit the product number for a released product was removed in Dynamics 365 Finance and Operations 10.0.0 with platform update 24 to help prevent data corruption.</span></span> <span data-ttu-id="3797e-174">Atskirais atvejais, kai turite pataisyti sugadintus duomenis, kurie kilo dėl ankstesnio vardo pakeitimo pagrindinio rakto išleidimo produkto metu, galite prašyti „Microsoft Support“ laikinai panaikinti tokį apribojimą.</span><span class="sxs-lookup"><span data-stu-id="3797e-174">In exceptional cases, where you must repair data corruption that was caused by a previous rename of the primary key of a released product, you can ask Microsoft Support to temporarily remove this restriction.</span></span>

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a><span data-ttu-id="3797e-175">Negaliu išleisti produkto varianto kitu juridiniu subjektu.</span><span class="sxs-lookup"><span data-stu-id="3797e-175">I can't create a released product variant in another legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3797e-176">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="3797e-176">Issue description</span></span>

<span data-ttu-id="3797e-177">Jei bandote išleisti pagrindinį produktą be variantų, tuomet sukurkite variantus kiekviename juridiniame subjekte (įmonėje), kaip būtina, jūs negalėsite išleisti variantų naudodami variantų siūlymus.</span><span class="sxs-lookup"><span data-stu-id="3797e-177">If you try to release a product master without variants, and then create the variants in each legal entity (company) as they are required, you won't be able to release the variants by using variant suggestions.</span></span> <span data-ttu-id="3797e-178">Taip pat negalėsite rankiniu būdu kurti variantų.</span><span class="sxs-lookup"><span data-stu-id="3797e-178">You also won't be able to manually create the variants.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3797e-179">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="3797e-179">Issue resolution</span></span>

<span data-ttu-id="3797e-180">Toks veikimo būdas yra numatytas.</span><span class="sxs-lookup"><span data-stu-id="3797e-180">This behavior is by design.</span></span> <span data-ttu-id="3797e-181">Pagrindinio produkto ryšiai ir matmenys, kuriuos pagrindinis produktas gali paimti laikomi bendrintu lygiu.</span><span class="sxs-lookup"><span data-stu-id="3797e-181">The relations of a product master and the dimensions that the master can take are kept at a shared level.</span></span> <span data-ttu-id="3797e-182">Dėl to, negalite kurti prieinamų matmenų bendrintam produktui konkrečiame juridiniame subjekte, kuriame tie matmenys išleisti ir tuomet kopijuoti proceso visuose juridiniuose subjektuose, kuriuose būtini matmenys.</span><span class="sxs-lookup"><span data-stu-id="3797e-182">Therefore, you can't create the available dimensions for a shared product master in the specific legal entity where those dimensions are released and then replicate the process in each legal entity where the dimensions are required.</span></span> <span data-ttu-id="3797e-183">Vietoj to, turite keisti išleidimo procesą, kad jis prisiderintų prie nustatyto proceso.</span><span class="sxs-lookup"><span data-stu-id="3797e-183">Instead, you must change your release process to adapt to the designed process.</span></span>

<span data-ttu-id="3797e-184">Čia yra produktų išleidimo procesas.</span><span class="sxs-lookup"><span data-stu-id="3797e-184">Here is the process for releasing products.</span></span>

1. <span data-ttu-id="3797e-185">Sukurkite bendrintą pagrindinį produktą ir matmenis, kuriuos galima išleisti į savo juridinius subjektus.</span><span class="sxs-lookup"><span data-stu-id="3797e-185">Create the shared product master and the dimensions that can be released to the legal entities.</span></span>
1. <span data-ttu-id="3797e-186">Išleiskite produktus į juridinius subjektus pagal naudojamo varianto siūlymus arba rankiniu būdu įtraukdami išleidžiamus derinius.</span><span class="sxs-lookup"><span data-stu-id="3797e-186">Release the products to the legal entities either by using variant suggestions or by manually adding the combinations that should be released.</span></span>

<span data-ttu-id="3797e-187">Kitu būdu, galite tiesiogiai kurti išleistą produktą.</span><span class="sxs-lookup"><span data-stu-id="3797e-187">Alternatively, you can directly create the released product.</span></span>

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a><span data-ttu-id="3797e-188">Išleidžiant variantą kitoje bendrovėje, gaunu šį klaidos pranešimą: „Produkto variantas su nurodytais matmenimis jau buvo sukurtas“.</span><span class="sxs-lookup"><span data-stu-id="3797e-188">When I release a variant in another company, I receive the following error message: "Product variant with specified dimensions has already been created."</span></span>

### <a name="issue-description"></a><span data-ttu-id="3797e-189">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="3797e-189">Issue description</span></span>

<span data-ttu-id="3797e-190">Jei produkto variantas jau buvo išleistas bendrovėje A ir bandote jį išleisti į bendrovę B naudodami **Naują** mygtukas puslapyje **Išleisti produkto variantai**, gausite tolesnį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="3797e-190">If a product variant has already been released in a company A, and you try to release it in company B by using the **New** button on the **Released product variants** page, you will receive the following error message:</span></span>

> <span data-ttu-id="3797e-191">Produkto variantas su nurodytomis dimensijomis jau sukurtas.</span><span class="sxs-lookup"><span data-stu-id="3797e-191">Product variant with specified dimensions has already been created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3797e-192">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="3797e-192">Issue resolution</span></span>

<span data-ttu-id="3797e-193">Mygtukas **Naujas** puslapyje **Išleisto produkto variantai** sukuria variantą ir išleidžia jį į bendrovės kontekstą.</span><span class="sxs-lookup"><span data-stu-id="3797e-193">The **New** button on the **Released product variants** page creates the variant and releases it in the company context.</span></span> <span data-ttu-id="3797e-194">Jei variantas jau buvo sukurtas, negalite naudoti **Naujas** mygtuko, kad išleistumėte jį į kitą bendrovę.</span><span class="sxs-lookup"><span data-stu-id="3797e-194">If the variant has already been created, you can't use the **New** button to release it in another company.</span></span>

<span data-ttu-id="3797e-195">Norėdami ištaisyti šią problemą, atverkite **Pagrindinio produkto** puslapį ir rinkitės **Išleisti produktą** norėdami išleisti esantį variantą norimoje bendrovėje.</span><span class="sxs-lookup"><span data-stu-id="3797e-195">To fix the issue, open the **Product master** page, and select **Release product** to release the existing variant in the desired company.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]