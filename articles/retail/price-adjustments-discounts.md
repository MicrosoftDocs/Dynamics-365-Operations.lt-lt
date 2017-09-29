---
title: "Kainų koregavimas ir nuolaidos"
description: "Šiame straipsnyje pateikiama informacija apie kainų koregavimus ir nuolaidas „Microsoft Dynamics 365 for Retail‟."
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c96f7afdb095fd45b5dd88c7760a24226518f61c
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="49164-103">Kainų koregavimas ir nuolaidos</span><span class="sxs-lookup"><span data-stu-id="49164-103">Price adjustments and discounts</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="49164-104">Šiame straipsnyje pateikiama informacija apie kainų koregavimus ir nuolaidas „Microsoft Dynamics 365 for Retail‟.</span><span class="sxs-lookup"><span data-stu-id="49164-104">This article provides information about price adjustments and discounts in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="49164-105">Naudodami „Dynamics 365 for Retail“ galite koreguoti produktų kainas ir nustatyti nuolaidas, taikomas eilutės elementui arba elektroninio kasos aparato (EKA) operacijai, vykdydami skambučių centro pardavimo užsakymą arba internetinį užsakymą.</span><span class="sxs-lookup"><span data-stu-id="49164-105">In Dynamics 365 for Retail, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="49164-106">Tiek kainų korekcijas, tiek nuolaidas galima susieti su kainų grupėmis.</span><span class="sxs-lookup"><span data-stu-id="49164-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="49164-107">Kainų koregavimams ir nuolaidoms galite nurodyti vieną pradžios datą ir pabaigos datą arba pasikartojimo laikotarpį, nuolaidos kodą ir keletą papildomų atributų.</span><span class="sxs-lookup"><span data-stu-id="49164-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> <span data-ttu-id="49164-108">Kainų koregavimą ir nuolaidos galima taikyti produktams, variantams arba kategorijoms.</span><span class="sxs-lookup"><span data-stu-id="49164-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="49164-109">Jei produktui taikoma daugiau nei viena nuolaida, klientas gali gauti vieną iš nuolaidų arba jungtinę nuolaidą, atsižvelgiant į nuolaidos konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="49164-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="49164-110">„Dynamics 365 for Retail“ automatiškai taikoma nuolaida ar jungtinė nuolaida ir taip klientui suteikiama geriausia kaina.</span><span class="sxs-lookup"><span data-stu-id="49164-110">Dynamics 365 for Retail automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="49164-111">Nustatydami kainos koregavimą arba nuolaidą įsitikinkite, kad kainų grupės priskiriamos tinkamiems kanalams, katalogams, priskyrimams arba lojalumo programoms, kurioms norite taikyti nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="49164-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="49164-112">Be to, jei norite automatiškai generuoti nuolaidos ID, prieš koreguodami kainą arba nuolaidą, puslapyje **Mažmeninės prekybos parametrai** nustatykite numerių sekas.</span><span class="sxs-lookup"><span data-stu-id="49164-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Retail parameters** page before you define a new price adjustment or discount.</span></span> <span data-ttu-id="49164-113">**Pastaba.** Kainos koregavimą arba nuolaidą galima panaikinti.</span><span class="sxs-lookup"><span data-stu-id="49164-113">**Note:** You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="49164-114">Tačiau bus prarasta statistinė informacija.</span><span class="sxs-lookup"><span data-stu-id="49164-114">However, statistical information will be lost.</span></span>

### <a name="types-of-discounts"></a><span data-ttu-id="49164-115">Nuolaidų tipai</span><span class="sxs-lookup"><span data-stu-id="49164-115">Types of discounts</span></span>

<span data-ttu-id="49164-116">Mažmeninės prekybos nuolaidos būna keturių tipų.</span><span class="sxs-lookup"><span data-stu-id="49164-116">There are four types of retail discounts:</span></span>

-   <span data-ttu-id="49164-117">**Paprasta nuolaida** – vienas procentinis dydis arba suma.</span><span class="sxs-lookup"><span data-stu-id="49164-117">**Simple discount** – A single percentage or amount.</span></span>
-   <span data-ttu-id="49164-118">**Kiekio nuolaida** – nuolaida, taikoma perkant du ar daugiau produktų.</span><span class="sxs-lookup"><span data-stu-id="49164-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
-   <span data-ttu-id="49164-119">**Nuolaida prekių rinkiniui** – nuolaida, suteikiama perkant tam tikrą produktų derinį.</span><span class="sxs-lookup"><span data-stu-id="49164-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
-   <span data-ttu-id="49164-120">**Ribinė nuolaida** – nuolaida, taikoma, kai operacijos bendroji suma yra didesnė nei nurodyta suma.</span><span class="sxs-lookup"><span data-stu-id="49164-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>

<span data-ttu-id="49164-121">Tiek kainų korekcijas, tiek nuolaidas galima susieti su kainų grupėmis.</span><span class="sxs-lookup"><span data-stu-id="49164-121">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="49164-122">Kainų grupės gali būti susietos su kanalais, katalogais, priskyrimais ir lojalumo programomis.</span><span class="sxs-lookup"><span data-stu-id="49164-122">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>



