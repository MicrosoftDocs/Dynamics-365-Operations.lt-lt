---
title: Apibrėžti konkretaus kanalo nuolaidas
description: Pardavėjai dažnai nustato skirtingas nuolaidas skirtinguose kanaluose. Šioje temoje apžvelgtos sąvokas, kurias turite žinoti, norėdami sukurti konkretaus kanalo nuolaidą.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 990c0d0b4b89420094dc86552b3e07717e5c7056
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991395"
---
# <a name="define-channel-specific-discounts"></a><span data-ttu-id="f8359-104">Kanalui būdingų nuolaidų nustatymas</span><span class="sxs-lookup"><span data-stu-id="f8359-104">Define channel-specific discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f8359-105">Šioje temoje apžvelgtos sąvokas, kurias turite žinoti, norėdami sukurti konkretaus kanalo nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="f8359-105">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span>

## <a name="channel-specific-discounts"></a><span data-ttu-id="f8359-106">Konkretaus kanalo nuolaidos</span><span class="sxs-lookup"><span data-stu-id="f8359-106">Channel-specific discounts</span></span>

<span data-ttu-id="f8359-107">Pardavėjai dažnai skirtinguose kanaluose siūlo skirtingas nuolaidas.</span><span class="sxs-lookup"><span data-stu-id="f8359-107">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="f8359-108">Taip gali būti daroma reaguojant į vietos rinkos sąlygas arba konkuruojant su kitais pardavėjais.</span><span class="sxs-lookup"><span data-stu-id="f8359-108">This may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="f8359-109">„Commerce“ naudoja kainų grupes konkrečių kanalų nuolaidoms apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="f8359-109">Commerce uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="f8359-110">Kainų grupės gali būti priskirtos vienam ar keliems toliau nurodytiems objektams: kanalams, katalogams, priskyrimams ir lojalumo programoms.</span><span class="sxs-lookup"><span data-stu-id="f8359-110">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="f8359-111">Šiame straipsnyje aptariami kanalai, tačiau tos pačios koncepcijos taikomos katalogų nuolaidoms, priskyrimų nuolaidoms ir lojalumo nuolaidoms.</span><span class="sxs-lookup"><span data-stu-id="f8359-111">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="f8359-112">Kainų grupės</span><span class="sxs-lookup"><span data-stu-id="f8359-112">Price groups</span></span>

<span data-ttu-id="f8359-113">[![Kainų grupės](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="f8359-113">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="f8359-114">Aukščiau pateiktoje diagramoje iliustruojamas ryšys tarp galimų operacijos (kanalo, katalogo, priskyrimo, kliento, lojalumo kortelės) objektų ir įvairių nuolaidų tipų, kuriuos galima sukonfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="f8359-114">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="f8359-115">Visos operacijos vyksta kanale, todėl kanalas operacijoje tikrai bus.</span><span class="sxs-lookup"><span data-stu-id="f8359-115">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="f8359-116">Likę objektai yra neprivalomi.</span><span class="sxs-lookup"><span data-stu-id="f8359-116">The remaining entities are optional.</span></span> <span data-ttu-id="f8359-117">Kiekviename bendrųjų duomenų puslapyje yra saitas į susijusių kainų grupių puslapį, kuriame galite peržiūrėti kainų grupes ir pagal poreikį jų pridėti.</span><span class="sxs-lookup"><span data-stu-id="f8359-117">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="f8359-118">Kainų grupė naudojama keturių skirtingų tipų objektams susieti su nuolaidomis, kainų koregavimais ir prekybos sutartimis.</span><span class="sxs-lookup"><span data-stu-id="f8359-118">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="f8359-119">Rekomenduojame susiplanuoti strategiją, kaip savo kainų grupes įvardysite, kad jos išliktų susistemintos.</span><span class="sxs-lookup"><span data-stu-id="f8359-119">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="f8359-120">Viena galimybė galėtų būti naudoti raidinį arba skaitinį prievardį ar povardį, kad būtų galima atskirti skirtingus tipus.</span><span class="sxs-lookup"><span data-stu-id="f8359-120">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="f8359-121">Pavyzdžiui, 1-xxxxx naudoti kanalų kainų grupėms, o 2-xxxxx – katalogų kainų grupėms.</span><span class="sxs-lookup"><span data-stu-id="f8359-121">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="f8359-122">Yra keturi užklausų puslapiai, kuriuose dėmesys skiriamas kiekvienam prekybos objektui, su kuriuo gali būti susietos nuolaidos.</span><span class="sxs-lookup"><span data-stu-id="f8359-122">There are four inquiry pages that focus on each of the commerce entities that can have discounts associated to them.</span></span>

- <span data-ttu-id="f8359-123">**Kanalo kainų grupės** – šiame puslapyje rodomas kiekvienos kainų grupės kartu susietų kanalų ir nuolaidų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="f8359-123">**Channel channel price groups** – This page shows a list of channels and discounts linked together for each price group.</span></span>
- <span data-ttu-id="f8359-124">**Katalogo kainų grupės** – šiame puslapyje rodomas kiekvienos kainų grupės kartu susietų katalogų ir nuolaidų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="f8359-124">**Catalog price groups** – This page shows a list of catalogs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="f8359-125">**Lojalumo kainų grupės** – šiame puslapyje rodomas kiekvienos kainų grupės kartu susietų lojalumo programų ir nuolaidų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="f8359-125">**Loyalty price groups** – This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="f8359-126">**Priskyrimo kainų grupės** – šiame puslapyje rodomas kiekvienos kainų grupės kartu susietų priskyrimų ir nuolaidų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="f8359-126">**Affiliation price groups** – This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="f8359-127">Kanalo nuolaidos sąrankos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="f8359-127">Example channel discount set up</span></span>

<span data-ttu-id="f8359-128">Toliau pateiktame pavyzdyje iliustruojamos užduotys, atliekamos nustatant kanalo nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="f8359-128">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1. <span data-ttu-id="f8359-129">Šiame pavyzdyje turite kanalą pavadinimu **Hiustonas** ir ketinate sukurti naują nuolaidą pavadinimu **Atgal į mokyklą**.</span><span class="sxs-lookup"><span data-stu-id="f8359-129">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School**.</span></span>
2. <span data-ttu-id="f8359-130">Kadangi kainodaros ir nuolaidų strategija apima kanalo nuolaidų galimybę, kurdami kanalą visada sukuriate konkretaus kanalo kainų grupę.</span><span class="sxs-lookup"><span data-stu-id="f8359-130">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3. <span data-ttu-id="f8359-131">Turite kainų grupę **Hiustono KG**, ir ji priskirta **Hiustono** kanalui.</span><span class="sxs-lookup"><span data-stu-id="f8359-131">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4. <span data-ttu-id="f8359-132">Sukūrę naująją nuolaidą **Atgal į mokyklą**, **Nuolaidos** puslapio viršuje turite spustelėti **Kainų grupės**.</span><span class="sxs-lookup"><span data-stu-id="f8359-132">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="f8359-133">Atsidarys **Nuolaidos kainų grupių** puslapis.</span><span class="sxs-lookup"><span data-stu-id="f8359-133">The **Discount price groups** page will open.</span></span> <span data-ttu-id="f8359-134">Toliau spustelėkite **Naujas** ir pasirinkite kainų grupę **Hiustono KG**.</span><span class="sxs-lookup"><span data-stu-id="f8359-134">Next, click **New** and select the **Houston-PG** price group.</span></span>
5. <span data-ttu-id="f8359-135">Dabar galite įgalinti nuolaidą ir ją perduoti į kanalą.</span><span class="sxs-lookup"><span data-stu-id="f8359-135">Now you can enable the discount and push it to the channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8359-136">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f8359-136">Additional resources</span></span>

[<span data-ttu-id="f8359-137">Kainų koregavimas ir nuolaidos</span><span class="sxs-lookup"><span data-stu-id="f8359-137">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)
