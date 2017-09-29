---
title: Paketo atributai
description: "Šiame straipsnyje pateikiama informacija apie paketo atributus. Paketo atributai yra žaliavų ir pagamintų produktų, kurie sudaro atsargų paketus, savybės. Šiame straipsnyje taip pat paaiškinama, kaip paketo atributus priskirti ir kaip galite jų ieškoti rezervuodami paketus."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 0c3f5115377178941984e53749c18cc1c9179812
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="batch-attributes"></a><span data-ttu-id="182e5-105">Paketo atributai</span><span class="sxs-lookup"><span data-stu-id="182e5-105">Batch attributes</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="182e5-106">Šiame straipsnyje pateikiama informacija apie paketo atributus.</span><span class="sxs-lookup"><span data-stu-id="182e5-106">This article provides information about batch attributes.</span></span> <span data-ttu-id="182e5-107">Paketo atributai yra žaliavų ir pagamintų produktų, kurie sudaro atsargų paketus, savybės.</span><span class="sxs-lookup"><span data-stu-id="182e5-107">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="182e5-108">Šiame straipsnyje taip pat paaiškinama, kaip paketo atributus priskirti ir kaip galite jų ieškoti rezervuodami paketus.</span><span class="sxs-lookup"><span data-stu-id="182e5-108">The article also explains how to assign batch attributes, and how you can search on them when you reserve batches.</span></span>

<span data-ttu-id="182e5-109">Paketo atributai yra žaliavų ir pagamintų produktų, kurie sudaro atsargų paketus, savybės.</span><span class="sxs-lookup"><span data-stu-id="182e5-109">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="182e5-110">Paketo atributai gali skirtis, atsižvelgiant į tokius veiksnius, kaip aplinkos sąlygos, žaliavų, naudojamų gaminant paketą, kokybė arba baigto produkto rezultatas.</span><span class="sxs-lookup"><span data-stu-id="182e5-110">Batch attributes can vary, depending on factors such as environmental conditions, the quality of the raw materials that are used to produce the batch, or the outcome of the finished product.</span></span> <span data-ttu-id="182e5-111">Naudojamų paketo atributų skaičius ir tipas skirtingose pramonės šakose gali būti labai įvairus.</span><span class="sxs-lookup"><span data-stu-id="182e5-111">The number and types of batch attributes that are used can vary widely from one industry to another.</span></span> <span data-ttu-id="182e5-112">Štai du pavyzdžiai, kaip naudoti paketo atributus:</span><span class="sxs-lookup"><span data-stu-id="182e5-112">Here are two examples that show how to use batch attributes:</span></span>

-   <span data-ttu-id="182e5-113">Sūrio pramonėje pieno, kuris yra viena iš žaliavų, naudojamų sūriui gaminti, atributai gali būti, pvz., riebalų kiekis ir procentinis svoris.</span><span class="sxs-lookup"><span data-stu-id="182e5-113">In the cheese industry, milk, which is one of the raw materials that are used to produce the cheese, can have attributes such as fat content and percentage weight.</span></span> <span data-ttu-id="182e5-114">Sūrio, gaminamo iš pieno, atributai gali būti kiti, pvz., drėgmė ir amžius.</span><span class="sxs-lookup"><span data-stu-id="182e5-114">The cheese that is produced from the milk can have other attributes, such as moisture and age.</span></span>
-   <span data-ttu-id="182e5-115">Plieno pramonėje pagamintos geležies atributai gali būti, pvz., magnio, sidabro ir cinko kiekis procentais.</span><span class="sxs-lookup"><span data-stu-id="182e5-115">In the steel industry, the iron that is produced might have attributes such as the percentages of magnesium content, silver content, and zinc content.</span></span>

<span data-ttu-id="182e5-116">Norėdami geriau valdyti atributų skaičių ir tipus, galite naudoti paketo atributų grupes.</span><span class="sxs-lookup"><span data-stu-id="182e5-116">To better manage the number and types of attributes, you can use batch attribute groups.</span></span> <span data-ttu-id="182e5-117">Tokiu būdu jums nereikės įtraukti kiekvieno atributo atskirai.</span><span class="sxs-lookup"><span data-stu-id="182e5-117">In this way, you don't have to add each attribute individually.</span></span>

## <a name="assign-batch-attributes"></a><span data-ttu-id="182e5-118">Paketo atributų priskyrimas</span><span class="sxs-lookup"><span data-stu-id="182e5-118">Assign batch attributes</span></span>
<span data-ttu-id="182e5-119">Galite priskirti paketo atributus atskiriems produktams, esantiems atsargų paketuose, arba galite juos priskirti produktams, susietiems su konkrečiais klientais.</span><span class="sxs-lookup"><span data-stu-id="182e5-119">You can assign batch attributes to individual products that are held in inventory batches, or you can assign them to products that are associated with specific customers.</span></span> <span data-ttu-id="182e5-120">Kad galėtumėte priskirti paketo atributą kliento lygiu, turite priskirti jį produkto lygiu.</span><span class="sxs-lookup"><span data-stu-id="182e5-120">Before you can assign a batch attribute at the customer level, you must assign it at the product level.</span></span> <span data-ttu-id="182e5-121">Produkto paketo dimensija sekimo dimensijų grupėje turi būti nustatyta kaip **Aktyvi**.</span><span class="sxs-lookup"><span data-stu-id="182e5-121">The product must have the batch dimension set to **Active** in the tracking dimension group.</span></span> <span data-ttu-id="182e5-122">Norėdami priskirti paketo atributą atskiram produktui, naudokite konkretaus produkto puslapį.</span><span class="sxs-lookup"><span data-stu-id="182e5-122">To assign a batch attribute to an individual product, use the product-specific page.</span></span> <span data-ttu-id="182e5-123">Jei atributas būdingas klientui skirtam produktui, naudokite konkretaus kliento puslapį.</span><span class="sxs-lookup"><span data-stu-id="182e5-123">If the attribute is specific to a product for a customer, use the customer-specific page.</span></span> <span data-ttu-id="182e5-124">Kai įtraukiate atributą į produktą, taip pat apibrėžiate kitus parametrus.</span><span class="sxs-lookup"><span data-stu-id="182e5-124">When you add an attribute to a product, you also define other parameters.</span></span> <span data-ttu-id="182e5-125">Štai keletas pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="182e5-125">Here are some examples:</span></span>

-   <span data-ttu-id="182e5-126">Mažiausias ir didžiausias atributo, kurio tipas **Sveikasis skaičius** arba **Trupmena** diapazonas.</span><span class="sxs-lookup"><span data-stu-id="182e5-126">The minimum and maximum ranges for an attribute of the **Integer** or **Fraction** type.</span></span>
-   <span data-ttu-id="182e5-127">Atributo, kurio tipas **Sveikasis skaičius** arba **Trupmena**, nuokrypio veiksmai.</span><span class="sxs-lookup"><span data-stu-id="182e5-127">The tolerance actions for an attribute of the **Integer** or **Fraction** type.</span></span> <span data-ttu-id="182e5-128">Jei atributo vertė nepatenka į mažiausią ir didžiausią diapazoną, veiksmas gali būti įspėjimas arba klaidos pranešimas.</span><span class="sxs-lookup"><span data-stu-id="182e5-128">If the value of the attribute falls outside the minimum and maximum range, the action can be either a warning message or an error message.</span></span>
-   <span data-ttu-id="182e5-129">Atributo tikslinė vertė.</span><span class="sxs-lookup"><span data-stu-id="182e5-129">The target value for the attribute.</span></span> <span data-ttu-id="182e5-130">Ši vertė yra optimali atributo vertė, ir ji taikoma visiems atributų tipams.</span><span class="sxs-lookup"><span data-stu-id="182e5-130">This value is the optimal value of the attribute, and it applies to all attribute types.</span></span>

<span data-ttu-id="182e5-131">Galite pasiekti produktų, kuriuos pasirinkote dalies Produkto informacijos valdymas puslapyje **Patvirtinti produktai**, puslapius.</span><span class="sxs-lookup"><span data-stu-id="182e5-131">You can access the pages for products that you select on the **Released products** page in Product information management.</span></span> <span data-ttu-id="182e5-132">Produktui priskyrę paketo atributus, puslapyje **Atsargų paketo atributai** galite į atributus įtraukti tam tikras vertes.</span><span class="sxs-lookup"><span data-stu-id="182e5-132">After you assign batch attributes to a product, you can add specific values to the attributes on the **Inventory batch attributes** page.</span></span>

## <a name="reserve-batches"></a><span data-ttu-id="182e5-133">Paketų rezervavimas</span><span class="sxs-lookup"><span data-stu-id="182e5-133">Reserve batches</span></span>
<span data-ttu-id="182e5-134">Galite ieškoti paketo atributuose, kai atliekate pardavimo užsakymo paketo rezervavimus, kad įvykdytumėte kliento užsakymą, arba kai išrenkate ir rezervuojate paketus gamybos užsakymui.</span><span class="sxs-lookup"><span data-stu-id="182e5-134">You can search on batch attributes when you do batch reservations for a sales order to fullfill a customer's order, or when you pick and reserve batches for a production order.</span></span> <span data-ttu-id="182e5-135">Ieška padės rasti atsargų paketą, kuriame yra produktas su paketo atributu, kurio norite.</span><span class="sxs-lookup"><span data-stu-id="182e5-135">The search helps locate an inventory batch that contains the product that has the batch attribute that you want.</span></span> <span data-ttu-id="182e5-136">Radę paketą ar paketus galite rezervuoti produktą į atsiradusią atsargų operacijos eilutę.</span><span class="sxs-lookup"><span data-stu-id="182e5-136">After you locate the batch or batches, you can reserve the product to the originating inventory transaction line.</span></span>




