---
title: Apibrėžti ir prižiūrėti mažmeninės prekybos kanalus
description: Šioje temoje pateikiama tradicinių parduotuvių, kurios „Dynamics 365 Commerce“ nurodomos kaip parduotuvės, nustatymo proceso apžvalga. Jame pateikiama informacija apie užduotis, kurias turite atlikti prieš ir po parduotuvės nustatymo.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a2ac4a4a42447e4ee57d24548a79f43b88b03927
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213703"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="78e8e-104">Mažmeninės prekybos kanalų nustatymas ir tvarkymas</span><span class="sxs-lookup"><span data-stu-id="78e8e-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="78e8e-105">Šioje temoje pateikiama tradicinių parduotuvių, kurios „Dynamics 365 Commerce“ nurodomos kaip parduotuvės, nustatymo proceso apžvalga.</span><span class="sxs-lookup"><span data-stu-id="78e8e-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as stores in Dynamics 365 Commerce.</span></span> <span data-ttu-id="78e8e-106">Jame pateikiama informacija apie užduotis, kurias turite atlikti prieš ir po parduotuvės nustatymo.</span><span class="sxs-lookup"><span data-stu-id="78e8e-106">It includes information about the tasks that you must complete both before and after you set up a store.</span></span>

<span data-ttu-id="78e8e-107">„Commerce“ palaiko kelis kanalus, pvz., internetines parduotuves, skambučių centrus ir tradicines parduotuves.</span><span class="sxs-lookup"><span data-stu-id="78e8e-107">Commerce supports multiple channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="78e8e-108">Tradicinė parduotuvė vadinama parduotuve.</span><span class="sxs-lookup"><span data-stu-id="78e8e-108">A brick-and-mortar store is called a store.</span></span> <span data-ttu-id="78e8e-109">Kiekvienoje parduotuvėje gali būti naudojami savi mokėjimo būdai, kainų grupės, elektroninių kasos aparatų (EKA) registrai, pajamų ir išlaidų sąskaitos bei darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="78e8e-109">Each store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="78e8e-110">Prieš kurdami parduotuvę, turite nustatyti visus šiuos jos elementus.</span><span class="sxs-lookup"><span data-stu-id="78e8e-110">You must set up all these elements for a store before you create it.</span></span> <span data-ttu-id="78e8e-111">Kai sukuriate parduotuvę, galite priskirti produktus, kuriuos norite, kad ji platintų.</span><span class="sxs-lookup"><span data-stu-id="78e8e-111">After you create the store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="78e8e-112">Be to, parduotuvei priskiriami darbuotojai, kasos aparatai ir klientai.</span><span class="sxs-lookup"><span data-stu-id="78e8e-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="78e8e-113">Galiausiai, įtraukite naują parduotuvę į organizacijos hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="78e8e-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-stores"></a><span data-ttu-id="78e8e-114">Parduotuvių nustatymas</span><span class="sxs-lookup"><span data-stu-id="78e8e-114">Setting up stores</span></span>

<span data-ttu-id="78e8e-115">Prieš nustatydami parduotuvę programoje „Commerce“, turite atlikti kai kurias būtinąsias užduotis.</span><span class="sxs-lookup"><span data-stu-id="78e8e-115">Before you can set up a store in Commerce, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="78e8e-116">Tada galite sukurti parduotuvę ir pridėti informacijos.</span><span class="sxs-lookup"><span data-stu-id="78e8e-116">You can then create the store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="78e8e-117">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="78e8e-117">Prerequisites</span></span>

<span data-ttu-id="78e8e-118">Prieš nustatydami parduotuvę, turite atlikti tolesnes užduotis.</span><span class="sxs-lookup"><span data-stu-id="78e8e-118">You must complete the following tasks before you can set up a store:</span></span>

1. <span data-ttu-id="78e8e-119">Sukonfigūruokite savo organizacijos struktūrą ir nustatykite mažmeninės prekybos asortimento, papildymo ir ataskaitų teikimo organizacijos hierarchijas.</span><span class="sxs-lookup"><span data-stu-id="78e8e-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="78e8e-120">Nustatykite sandėlį, atitinkantį parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="78e8e-120">Set up a warehouse that represents the store.</span></span>
3. <span data-ttu-id="78e8e-121">Nustatykite parduotuvių, parduotuvių išrašų ir išrašų kvitų numeracijas.</span><span class="sxs-lookup"><span data-stu-id="78e8e-121">Set up number sequences for stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="78e8e-122">Konfigūruokite „Commerce“ parametrus.</span><span class="sxs-lookup"><span data-stu-id="78e8e-122">Configure parameters for Commerce.</span></span>
5. <span data-ttu-id="78e8e-123">Nustatykite parduotuvėje naudojamus mokėjimo būdus.</span><span class="sxs-lookup"><span data-stu-id="78e8e-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="78e8e-124">Norėdami kredito kortelių operacijas apdoroti POS kasos aparatuose, taip pat galite nustatyti mokėjimo paslaugas.</span><span class="sxs-lookup"><span data-stu-id="78e8e-124">To process credit card transactions at POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="78e8e-125">Nustatykite PVM grupes.</span><span class="sxs-lookup"><span data-stu-id="78e8e-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="78e8e-126">Nustatykite produktus.</span><span class="sxs-lookup"><span data-stu-id="78e8e-126">Set up products.</span></span> <span data-ttu-id="78e8e-127">Vykdant šią užduotį, taip pat nustatomos produktų hierarchijos, produktų variantai ir produktų asortimentai.</span><span class="sxs-lookup"><span data-stu-id="78e8e-127">As part of this task, you also set up product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="78e8e-128">Nustatykite produktų kainų grupes.</span><span class="sxs-lookup"><span data-stu-id="78e8e-128">Set up product price groups.</span></span>
10. <span data-ttu-id="78e8e-129">Nustatykite produktų kainodarą.</span><span class="sxs-lookup"><span data-stu-id="78e8e-129">Set up product pricing.</span></span> <span data-ttu-id="78e8e-130">Vykdant šią užduotį, taip pat nustatomi kainos koregavimai, nuolaidos ir nuolaidų laikotarpiai.</span><span class="sxs-lookup"><span data-stu-id="78e8e-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="78e8e-131">Nustatykite darbuotojus.</span><span class="sxs-lookup"><span data-stu-id="78e8e-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="78e8e-132">Taip pat darbuotojams turite priskirti reikiamas teises, kad jie galėtų prisijungti ir atlikti užduotis naudodami EKA sistemą.</span><span class="sxs-lookup"><span data-stu-id="78e8e-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the POS system.</span></span>

12. <span data-ttu-id="78e8e-133">Sukonfigūruokite EKA šablonus norėdami priskirti parduotuvei.</span><span class="sxs-lookup"><span data-stu-id="78e8e-133">Configure the POS profiles to assign to the store.</span></span> <span data-ttu-id="78e8e-134">Ši užduotis apima daug kitų užduočių, pvz., kasos aparatų nustatymą, autonominių profilių nustatymą ir kvitų formatų bei profilių nustatymą.</span><span class="sxs-lookup"><span data-stu-id="78e8e-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="78e8e-135">Peržiūrėkite visas užduotis, įtrauktas į būtinąsias sąlygas, ir atlikite tik jums taikomas užduotis.</span><span class="sxs-lookup"><span data-stu-id="78e8e-135">Review all the tasks that are included in the prerequisites, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-store"></a><span data-ttu-id="78e8e-136">Parduotuvės nustatymas</span><span class="sxs-lookup"><span data-stu-id="78e8e-136">Set up a store</span></span>

<span data-ttu-id="78e8e-137">Atlikę būtinas užduotis, atlikite toliau pateikiamas užduotis, norėdami nustatyti informaciją apie parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="78e8e-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the store:</span></span>

1. <span data-ttu-id="78e8e-138">Sukurkite parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="78e8e-138">Create a store.</span></span>
2. <span data-ttu-id="78e8e-139">Priskirkite parduotuvei PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="78e8e-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="78e8e-140">Parduotuvei priskirkite priimtus mokėjimo būdus.</span><span class="sxs-lookup"><span data-stu-id="78e8e-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="78e8e-141">Įtraukite informaciją į parduotuvėse siūlomų produktų aprašus.</span><span class="sxs-lookup"><span data-stu-id="78e8e-141">Add details to the product descriptions for products that you offer in your stores.</span></span> <span data-ttu-id="78e8e-142">Pavyzdžiui, galite įtraukti raiškiojo teksto ir vaizdų.</span><span class="sxs-lookup"><span data-stu-id="78e8e-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="78e8e-143">Ši produktų informacija rodoma įvairiomis aplinkybėmis, pavyzdžiui, POS kasos aparate ar išspausdintose etiketėse.</span><span class="sxs-lookup"><span data-stu-id="78e8e-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="78e8e-144">Mažmeninės prekybos parduotuvę pridėkite į numatytąją organizacijos hierarchiją, kuri priskirta **Mažmeninės prekybos asortimento**, **Mažmeninės prekybos papildymo** ar **Mažmeninės prekybos ataskaitų** tikslu.</span><span class="sxs-lookup"><span data-stu-id="78e8e-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-store"></a><span data-ttu-id="78e8e-145">Nustačius parduotuvę</span><span class="sxs-lookup"><span data-stu-id="78e8e-145">After you set up a store</span></span>

<span data-ttu-id="78e8e-146">Įvedę parduotuvės informaciją, atlikite nurodytas užduotis norėdami nusiųsti naujus parduotuvės duomenis į EKA.</span><span class="sxs-lookup"><span data-stu-id="78e8e-146">After you enter the details for the store, complete these tasks to send the new store data to POS:</span></span>

1. <span data-ttu-id="78e8e-147">Sukonfigūruokite parduotuvės POS kasos aparatus.</span><span class="sxs-lookup"><span data-stu-id="78e8e-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="78e8e-148">Parduotuvei priskirkite produktų asortimentą.</span><span class="sxs-lookup"><span data-stu-id="78e8e-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="78e8e-149">Apdorokite asortimentus norėdami sukurti produktų, kurie įtraukti į asortimentą, sąrašą ir padaryti produktus pasiekiamus parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="78e8e-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the store.</span></span>
4. <span data-ttu-id="78e8e-150">Siųskite duomenis, pvz., numeracijas, aparatūros profilius ir POS ekrano maketus į EKA registrus.</span><span class="sxs-lookup"><span data-stu-id="78e8e-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the POS registers.</span></span>
5. <span data-ttu-id="78e8e-151">Publikuokite parduotuvę norėdami siųsti parduotuvės duomenis į EKA.</span><span class="sxs-lookup"><span data-stu-id="78e8e-151">Publish the store to send store data to POS.</span></span>
6. <span data-ttu-id="78e8e-152">Vykdykite užduotis norėdami siųsti parduotuvės duomenis į EKA.</span><span class="sxs-lookup"><span data-stu-id="78e8e-152">Run the jobs to send the store data to POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="78e8e-153">Organizacijų hierarchijos</span><span class="sxs-lookup"><span data-stu-id="78e8e-153">Organization hierarchies</span></span>

<span data-ttu-id="78e8e-154">„Commerce“ naudoja organizacijos hierarchijas kanalams struktūrizuoti.</span><span class="sxs-lookup"><span data-stu-id="78e8e-154">Commerce uses organization hierarchies to structure channels.</span></span> <span data-ttu-id="78e8e-155">Organizacijos hierarchijos nurodo ryšius tarp organizacijų, kurios sudaro jūsų verslą.</span><span class="sxs-lookup"><span data-stu-id="78e8e-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="78e8e-156">Kai nustatote parduotuves, galite įtraukti jas į organizacijos hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="78e8e-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="78e8e-157">Tada parduotuvės bendrina duomenis, kurie naudojami asortimentams, papildymui ir ataskaitoms.</span><span class="sxs-lookup"><span data-stu-id="78e8e-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

> [!NOTE]
> <span data-ttu-id="78e8e-158">Norint naudoti „Commerce“ pardavimo funkcijas, turi būti įgalintas konfigūracijos raktas **Kelios siuntimo vietos**.</span><span class="sxs-lookup"><span data-stu-id="78e8e-158">To use Commerce sales functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="78e8e-159">Šį konfigūracijos raktą galima rasti prie **prekybos konfigūracijos** raktų (**Sistemos administravimas** \> **Sąranka** \> **Licencijos konfigūracija**).</span><span class="sxs-lookup"><span data-stu-id="78e8e-159">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="78e8e-160">Tai būtina dėl įvairių tikrinimų pagal pristatymo adresą, sukonfigūruotų pardavimo užsakymo eilutės lygiu.</span><span class="sxs-lookup"><span data-stu-id="78e8e-160">This is required due to various validations based on the delivery address configured at the sales order line level.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]