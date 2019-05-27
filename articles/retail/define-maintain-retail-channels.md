---
title: Apibrėžti ir prižiūrėti mažmeninės prekybos kanalus
description: Šioje temoje pateikiama tradicinių parduotuvių, kurios „Microsoft Dynamics 365 for Retail“ nurodomos kaip mažmeninės prekybos parduotuvės, nustatymo proceso apžvalga. Jame pateikiama informacija apie užduotis, kurias turite atlikti prieš ir po mažmeninės prekybos parduotuvės nustatymo.
author: mugunthanm
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 53ba6cdb2378ce9011c6e7e3ce4e67c789adb1e6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560354"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="1006b-104">Apibrėžti ir prižiūrėti mažmeninės prekybos kanalus</span><span class="sxs-lookup"><span data-stu-id="1006b-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1006b-105">Šioje temoje pateikiama tradicinių parduotuvių, kurios „Microsoft Dynamics 365 for Retail“ nurodomos kaip mažmeninės prekybos parduotuvės, nustatymo proceso apžvalga.</span><span class="sxs-lookup"><span data-stu-id="1006b-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="1006b-106">Jame pateikiama informacija apie užduotis, kurias turite atlikti prieš ir po mažmeninės prekybos parduotuvės nustatymo.</span><span class="sxs-lookup"><span data-stu-id="1006b-106">It includes information about the tasks that you must complete both before and after you set up a retail store.</span></span>

<span data-ttu-id="1006b-107">„Dynamics 365 for Retail“ palaiko kelis mažmeninės prekybos kanalus, pvz., internetines parduotuves, skambučių centrus ir tradicines parduotuves.</span><span class="sxs-lookup"><span data-stu-id="1006b-107">Dynamics 365 for Retail supports multiple retail channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="1006b-108">Tradicinė parduotuvė vadinama mažmeninės prekybos parduotuve.</span><span class="sxs-lookup"><span data-stu-id="1006b-108">A brick-and-mortar store is called a retail store.</span></span> <span data-ttu-id="1006b-109">Kiekvienoje mažmeninės prekybos parduotuvėje gali būti naudojami savi mokėjimo būdai, kainų grupės, pardavimo vietos (POS) kasos aparatai, pajamų ir išlaidų sąskaitos bei darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="1006b-109">Each retail store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="1006b-110">Prieš kurdami mažmeninės prekybos parduotuvę, turite nustatyti visus šiuos jos elementus.</span><span class="sxs-lookup"><span data-stu-id="1006b-110">You must set up all these elements for a retail store before you create it.</span></span> <span data-ttu-id="1006b-111">Kai sukuriate mažmeninės prekybos parduotuvę, galite priskirti produktus, kuriuos norite, kad ji platintų.</span><span class="sxs-lookup"><span data-stu-id="1006b-111">After you create the retail store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="1006b-112">Be to, parduotuvei priskiriami darbuotojai, kasos aparatai ir klientai.</span><span class="sxs-lookup"><span data-stu-id="1006b-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="1006b-113">Galiausiai, įtraukite naują parduotuvę į organizacijos hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="1006b-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-retail-stores"></a><span data-ttu-id="1006b-114">Mažmeninės prekybos parduotuvių nustatymas</span><span class="sxs-lookup"><span data-stu-id="1006b-114">Setting up retail stores</span></span>

<span data-ttu-id="1006b-115">Prieš nustatydami mažmeninės prekybos parduotuvę programoje „Dynamics 365 for Retail“, turite atlikti kai kurias būtinąsias užduotis.</span><span class="sxs-lookup"><span data-stu-id="1006b-115">Before you can set up a retail store in Dynamics 365 for Retail, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="1006b-116">Tada galite sukurti mažmeninės prekybos parduotuvę ir pridėti informacijos.</span><span class="sxs-lookup"><span data-stu-id="1006b-116">You can then create the retail store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="1006b-117">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="1006b-117">Prerequisites</span></span>

<span data-ttu-id="1006b-118">Prieš nustatydami mažmeninės prekybos parduotuvę, turite atlikti tolesnes užduotis.</span><span class="sxs-lookup"><span data-stu-id="1006b-118">You must complete the following tasks before you can set up a retail store:</span></span>

1. <span data-ttu-id="1006b-119">Sukonfigūruokite savo organizacijos struktūrą ir nustatykite mažmeninės prekybos asortimento, papildymo ir ataskaitų teikimo organizacijos hierarchijas.</span><span class="sxs-lookup"><span data-stu-id="1006b-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="1006b-120">Nustatykite sandėlį, atitinkantį mažmeninės prekybos parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="1006b-120">Set up a warehouse that represents the retail store.</span></span>
3. <span data-ttu-id="1006b-121">Nustatykite mažmeninės prekybos parduotuvių, parduotuvių išrašų ir išrašų kvitų numeracijas.</span><span class="sxs-lookup"><span data-stu-id="1006b-121">Set up number sequences for retail stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="1006b-122">Sukonfigūruokite „Retail‟ parametrus.</span><span class="sxs-lookup"><span data-stu-id="1006b-122">Configure parameters for Retail.</span></span>
5. <span data-ttu-id="1006b-123">Nustatykite parduotuvėje naudojamus mokėjimo būdus.</span><span class="sxs-lookup"><span data-stu-id="1006b-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="1006b-124">Norėdami kredito kortelių operacijas apdoroti mažmeninės prekybos POS kasos aparatuose, taip pat galite nustatyti mokėjimo paslaugas.</span><span class="sxs-lookup"><span data-stu-id="1006b-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="1006b-125">Nustatykite PVM grupes.</span><span class="sxs-lookup"><span data-stu-id="1006b-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="1006b-126">Nustatykite mažmeninės prekybos produktus.</span><span class="sxs-lookup"><span data-stu-id="1006b-126">Set up retail products.</span></span> <span data-ttu-id="1006b-127">Vykdant šią užduotį, taip pat nustatomos mažmeninės prekybos produktų hierarchijos, produktų variantai ir produktų asortimentai.</span><span class="sxs-lookup"><span data-stu-id="1006b-127">As part of this task, you also set up retail product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="1006b-128">Nustatykite produktų kainų grupes.</span><span class="sxs-lookup"><span data-stu-id="1006b-128">Set up product price groups.</span></span>
10. <span data-ttu-id="1006b-129">Nustatykite mažmeninės prekybos produktų kainodarą.</span><span class="sxs-lookup"><span data-stu-id="1006b-129">Set up retail product pricing.</span></span> <span data-ttu-id="1006b-130">Vykdant šią užduotį, taip pat nustatomi kainos koregavimai, nuolaidos ir nuolaidų laikotarpiai.</span><span class="sxs-lookup"><span data-stu-id="1006b-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="1006b-131">Nustatykite darbuotojus.</span><span class="sxs-lookup"><span data-stu-id="1006b-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1006b-132">Taip pat darbuotojams turite priskirti reikiamas teises, kad jie galėtų prisijungti ir atlikti užduotis naudodami „Dynamics 365 for Retail for Retail POS“ sistemą.</span><span class="sxs-lookup"><span data-stu-id="1006b-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the Dynamics 365 for Retail for Retail POS system.</span></span>

12. <span data-ttu-id="1006b-133">Sukonfigūruokite „Retail POS‟ profilius, priskirtinus parduotuvei.</span><span class="sxs-lookup"><span data-stu-id="1006b-133">Configure the Retail POS profiles to assign to the store.</span></span> <span data-ttu-id="1006b-134">Ši užduotis apima daug kitų užduočių, pvz., kasos aparatų nustatymą, autonominių profilių nustatymą ir kvitų formatų bei profilių nustatymą.</span><span class="sxs-lookup"><span data-stu-id="1006b-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="1006b-135">Peržiūrėkite visas užduotis, įtrauktas į būtinąsias sąlygas, ir atlikite tik jums taikomas užduotis.</span><span class="sxs-lookup"><span data-stu-id="1006b-135">Review all the tasks that are included in the prerequisite, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-retail-store"></a><span data-ttu-id="1006b-136">Parduotuvės nustatymas</span><span class="sxs-lookup"><span data-stu-id="1006b-136">Set up a retail store</span></span>

<span data-ttu-id="1006b-137">Atlikę būtinas užduotis, atlikite tolesnes užduotis, norėdami nustatyti informaciją apie mažmeninės prekybos parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="1006b-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the retail store:</span></span>

1. <span data-ttu-id="1006b-138">Sukurkite mažmeninės prekybos parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="1006b-138">Create a retail store.</span></span>
2. <span data-ttu-id="1006b-139">Priskirkite parduotuvei PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="1006b-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="1006b-140">Parduotuvei priskirkite priimtus mokėjimo būdus.</span><span class="sxs-lookup"><span data-stu-id="1006b-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="1006b-141">Įtraukite informaciją į mažmeninės prekybos parduotuvėse siūlomų produktų aprašus.</span><span class="sxs-lookup"><span data-stu-id="1006b-141">Add details to the product descriptions for products that you offer in your retail stores.</span></span> <span data-ttu-id="1006b-142">Pavyzdžiui, galite įtraukti raiškiojo teksto ir vaizdų.</span><span class="sxs-lookup"><span data-stu-id="1006b-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="1006b-143">Ši produktų informacija rodoma įvairiomis aplinkybėmis, pavyzdžiui, POS kasos aparate ar išspausdintose etiketėse.</span><span class="sxs-lookup"><span data-stu-id="1006b-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="1006b-144">Mažmeninės prekybos parduotuvę pridėkite į numatytąją organizacijos hierarchiją, kuri priskirta **Mažmeninės prekybos asortimento**, **Mažmeninės prekybos papildymo** ar **Mažmeninės prekybos ataskaitų** tikslu.</span><span class="sxs-lookup"><span data-stu-id="1006b-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-retail-store"></a><span data-ttu-id="1006b-145">Nustačius mažmeninės prekybos parduotuvę</span><span class="sxs-lookup"><span data-stu-id="1006b-145">After you set up a retail store</span></span>

<span data-ttu-id="1006b-146">Įvedę mažmeninės prekybos parduotuvės informaciją, atlikite nurodytas užduotis, norėdami nusiųsti naujus mažmeninės prekybos parduotuvės duomenis į „Retail POS‟.</span><span class="sxs-lookup"><span data-stu-id="1006b-146">After you enter the details for the retail store, complete these tasks to send the new retail store data to Retail POS:</span></span>

1. <span data-ttu-id="1006b-147">Sukonfigūruokite parduotuvės POS kasos aparatus.</span><span class="sxs-lookup"><span data-stu-id="1006b-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="1006b-148">Parduotuvei priskirkite produktų asortimentą.</span><span class="sxs-lookup"><span data-stu-id="1006b-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="1006b-149">Apdorokite asortimentus norėdami sukurti produktų, kurie įtraukti į asortimentą, sąrašą ir padaryti produktus pasiekiamus mažmeninės prekybos parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="1006b-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store.</span></span>
4. <span data-ttu-id="1006b-150">Siųskite duomenis, pvz., numeracijas, aparatūros profilius ir POS ekrano maketus į „Retail POS‟ kasos aparatus.</span><span class="sxs-lookup"><span data-stu-id="1006b-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.</span></span>
5. <span data-ttu-id="1006b-151">Publikuokite mažmeninės prekybos parduotuvę norėdami siųsti parduotuvės duomenis į „Retail POS‟.</span><span class="sxs-lookup"><span data-stu-id="1006b-151">Publish the retail store to send store data to Retail POS.</span></span>
6. <span data-ttu-id="1006b-152">Vykdykite užduotis norėdami siųsti parduotuvės duomenis į „Retail POS‟.</span><span class="sxs-lookup"><span data-stu-id="1006b-152">Run the jobs to send the store data to Retail POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="1006b-153">Organizacijų hierarchijos</span><span class="sxs-lookup"><span data-stu-id="1006b-153">Organization hierarchies</span></span>

<span data-ttu-id="1006b-154">„Retail‟ naudoja organizacijos hierarchijas mažmeninės prekybos kanalams struktūrizuoti.</span><span class="sxs-lookup"><span data-stu-id="1006b-154">Retail uses organization hierarchies to structure retail channels.</span></span> <span data-ttu-id="1006b-155">Organizacijos hierarchijos nurodo ryšius tarp organizacijų, kurios sudaro jūsų verslą.</span><span class="sxs-lookup"><span data-stu-id="1006b-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="1006b-156">Kai nustatote parduotuves, galite įtraukti jas į organizacijos hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="1006b-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="1006b-157">Tada parduotuvės bendrina duomenis, kurie naudojami asortimentams, papildymui ir ataskaitoms.</span><span class="sxs-lookup"><span data-stu-id="1006b-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>
