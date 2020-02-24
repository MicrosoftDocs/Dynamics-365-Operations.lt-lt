---
title: Kainų koregavimas ir nuolaidos
description: Šiame straipsnyje pateikiama informacija apie kainų koregavimus ir nuolaidas „Dynamics 365 Commerce“.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: dfaacfa7681258e3b2273083017c0c398d566651
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023465"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="16133-103">Kainų koregavimas ir nuolaidos</span><span class="sxs-lookup"><span data-stu-id="16133-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="16133-104">Šiame straipsnyje pateikiama informacija apie kainų koregavimus ir nuolaidas „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="16133-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="16133-105">„Commerce“ galite koreguoti produktų kainą, taip pat galite nustatyti nuolaidas, taikomas eilutės elementui arba operacijai elektroniniame kasos aparate (EKA), skambučių centro pardavimo užsakyme arba užsakyme internetu.</span><span class="sxs-lookup"><span data-stu-id="16133-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="16133-106">Tiek kainų korekcijas, tiek nuolaidas galima susieti su kainų grupėmis.</span><span class="sxs-lookup"><span data-stu-id="16133-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="16133-107">Kainų koregavimams ir nuolaidoms galite nurodyti vieną pradžios datą ir pabaigos datą arba pasikartojimo laikotarpį, nuolaidos kodą ir keletą papildomų atributų.</span><span class="sxs-lookup"><span data-stu-id="16133-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="16133-108">Kainų koregavimą ir nuolaidos galima taikyti produktams, variantams arba kategorijoms.</span><span class="sxs-lookup"><span data-stu-id="16133-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="16133-109">Jei produktui taikoma daugiau nei viena nuolaida, klientas gali gauti vieną iš nuolaidų arba jungtinę nuolaidą, atsižvelgiant į nuolaidos konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="16133-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="16133-110">„Commerce“ automatiškai taiko nuolaidą ar nuolaidų derinį, kuris klientui pasiūlo geriausią kainą.</span><span class="sxs-lookup"><span data-stu-id="16133-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="16133-111">Nustatydami kainos koregavimą arba nuolaidą įsitikinkite, kad kainų grupės priskiriamos tinkamiems kanalams, katalogams, priskyrimams arba lojalumo programoms, kurioms norite taikyti nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="16133-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="16133-112">Be to, jei norite automatiškai sugeneruoti nuolaidos ID, prieš nustatant naują kainą ar nuolaidą, puslapyje **„Commerce“ parametrai** nustatykite skaičių sekas.</span><span class="sxs-lookup"><span data-stu-id="16133-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="16133-113">Kainos koregavimą arba nuolaidą galima panaikinti.</span><span class="sxs-lookup"><span data-stu-id="16133-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="16133-114">Tačiau bus prarasta statistinė informacija.</span><span class="sxs-lookup"><span data-stu-id="16133-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="16133-115">Nuolaidų tipai</span><span class="sxs-lookup"><span data-stu-id="16133-115">Types of discounts</span></span>

<span data-ttu-id="16133-116">Yra keturių rūšių nuolaidos:</span><span class="sxs-lookup"><span data-stu-id="16133-116">There are four types of discounts:</span></span>

- <span data-ttu-id="16133-117">**Paprasta nuolaida** – vienas procentinis dydis arba suma.</span><span class="sxs-lookup"><span data-stu-id="16133-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="16133-118">**Kiekio nuolaida** – nuolaida, taikoma perkant du ar daugiau produktų.</span><span class="sxs-lookup"><span data-stu-id="16133-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="16133-119">**Nuolaida prekių rinkiniui** – nuolaida, suteikiama perkant tam tikrą produktų derinį.</span><span class="sxs-lookup"><span data-stu-id="16133-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="16133-120">**Ribinė nuolaida** – nuolaida, taikoma, kai operacijos bendroji suma yra didesnė nei nurodyta suma.</span><span class="sxs-lookup"><span data-stu-id="16133-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>

<span data-ttu-id="16133-121">Tiek kainų korekcijas, tiek nuolaidas galima susieti su kainų grupėmis.</span><span class="sxs-lookup"><span data-stu-id="16133-121">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="16133-122">Kainų grupės gali būti susietos su kanalais, katalogais, priskyrimais ir lojalumo programomis.</span><span class="sxs-lookup"><span data-stu-id="16133-122">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>
