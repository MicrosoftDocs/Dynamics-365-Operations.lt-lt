---
title: "Apibrėžti konkretaus kanalo nuolaidas"
description: "Pardavėjai dažnai nustato skirtingas nuolaidas skirtinguose kanaluose. Šioje temoje apžvelgtos sąvokas, kurias turite žinoti, norėdami sukurti konkretaus kanalo nuolaidą."
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 34039b298e8994e50a7c06ef034698e8c1264389
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="define-channel-specific-discounts"></a><span data-ttu-id="481f9-104">Apibrėžti konkretaus kanalo nuolaidas</span><span class="sxs-lookup"><span data-stu-id="481f9-104">Define channel-specific discounts</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="481f9-105">Pardavėjai dažnai nustato skirtingas nuolaidas skirtinguose kanaluose.</span><span class="sxs-lookup"><span data-stu-id="481f9-105">Retailers often set different discounts in different channels.</span></span> <span data-ttu-id="481f9-106">Šioje temoje apžvelgtos sąvokas, kurias turite žinoti, norėdami sukurti konkretaus kanalo nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="481f9-106">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span> 

<a name="channel-specific-discounts"></a><span data-ttu-id="481f9-107">Konkretaus kanalo nuolaidos</span><span class="sxs-lookup"><span data-stu-id="481f9-107">Channel-specific discounts</span></span>
--------------------------

<span data-ttu-id="481f9-108">Pardavėjai dažnai skirtinguose kanaluose siūlo skirtingas nuolaidas.</span><span class="sxs-lookup"><span data-stu-id="481f9-108">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="481f9-109">Taip gali būti daroma reaguojant į vietos rinkos sąlygas arba konkuruojant su kitais pardavėjais.</span><span class="sxs-lookup"><span data-stu-id="481f9-109">This is may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="481f9-110">Apibrėžti konkrečių kanalų nuolaidoms „Microsoft Dynamics 365 for Retail‟ naudojamos kainų grupės.</span><span class="sxs-lookup"><span data-stu-id="481f9-110">Microsoft Dynamics 365 for Retail uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="481f9-111">Kainų grupės gali būti priskirtos vienam ar keliems toliau nurodytiems objektams: kanalams, katalogams, priskyrimams ir lojalumo programoms.</span><span class="sxs-lookup"><span data-stu-id="481f9-111">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="481f9-112">Šiame straipsnyje aptariami kanalai, tačiau tos pačios koncepcijos taikomos katalogų nuolaidoms, priskyrimų nuolaidoms ir lojalumo nuolaidoms.</span><span class="sxs-lookup"><span data-stu-id="481f9-112">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="481f9-113">Kainų grupės</span><span class="sxs-lookup"><span data-stu-id="481f9-113">Price groups</span></span>

<span data-ttu-id="481f9-114">[![Kainų grupės](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="481f9-114">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="481f9-115">Aukščiau pateiktoje diagramoje iliustruojamas ryšys tarp galimų operacijos (kanalo, katalogo, priskyrimo, kliento, lojalumo kortelės) objektų ir įvairių nuolaidų tipų, kuriuos galima sukonfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="481f9-115">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="481f9-116">Visos operacijos vyksta kanale, todėl kanalas operacijoje tikrai bus.</span><span class="sxs-lookup"><span data-stu-id="481f9-116">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="481f9-117">Likę objektai yra neprivalomi.</span><span class="sxs-lookup"><span data-stu-id="481f9-117">The remaining entities are optional.</span></span> <span data-ttu-id="481f9-118">Kiekviename bendrųjų duomenų puslapyje yra saitas į susijusių kainų grupių puslapį, kuriame galite peržiūrėti kainų grupes ir pagal poreikį jų pridėti.</span><span class="sxs-lookup"><span data-stu-id="481f9-118">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="481f9-119">Kainų grupė naudojama keturių skirtingų tipų objektams susieti su nuolaidomis, kainų koregavimais ir prekybos sutartimis.</span><span class="sxs-lookup"><span data-stu-id="481f9-119">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="481f9-120">Rekomenduojame susiplanuoti strategiją, kaip savo kainų grupes įvardysite, kad jos išliktų susistemintos.</span><span class="sxs-lookup"><span data-stu-id="481f9-120">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="481f9-121">Viena galimybė galėtų būti naudoti raidinį arba skaitinį prievardį ar povardį, kad būtų galima atskirti skirtingus tipus.</span><span class="sxs-lookup"><span data-stu-id="481f9-121">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="481f9-122">Pavyzdžiui, 1-xxxxx naudoti kanalų kainų grupėms, o 2-xxxxx – katalogų kainų grupėms.</span><span class="sxs-lookup"><span data-stu-id="481f9-122">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="481f9-123">Yra keturi užklausų puslapiai, kuriuose dėmesys skiriamas kiekvienam mažmeninės prekybos objektui, su kuriuo gali būti susietos nuolaidos.</span><span class="sxs-lookup"><span data-stu-id="481f9-123">There are four inquiry pages that focus on each of the retail entities that can have discounts associated to them.</span></span>

-   <span data-ttu-id="481f9-124">**Mažmeninės prekybos kanalo kainų grupės** – šiame puslapyje rodomas kiekvienos kainų grupės kartu susietų kanalų ir nuolaidų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="481f9-124">**Retail channel price groups** - This page shows a list of channels and discounts linked together for each price group.</span></span>
-   <span data-ttu-id="481f9-125">**Katalogo kainų grupės** – šiame puslapyje rodomas kiekvienos kainų grupės kartu susietų katalogų ir nuolaidų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="481f9-125">**Catalog price groups** - This page shows a list of catalogs and discounts linked together for each price group.</span></span>
-   <span data-ttu-id="481f9-126">**Lojalumo kainų grupės** – šiame puslapyje rodomas kiekvienos kainų grupės kartu susietų lojalumo programų ir nuolaidų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="481f9-126">**Loyalty price groups** - This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
-   <span data-ttu-id="481f9-127">**Priskyrimo kainų grupės** – šiame puslapyje rodomas kiekvienos kainų grupės kartu susietų priskyrimų ir nuolaidų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="481f9-127">**Affiliation price groups** - This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="481f9-128">Kanalo nuolaidos sąrankos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="481f9-128">Example channel discount set up</span></span>
<span data-ttu-id="481f9-129">Toliau pateiktame pavyzdyje iliustruojamos užduotys, atliekamos nustatant kanalo nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="481f9-129">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1.  <span data-ttu-id="481f9-130">Šiame pavyzdyje turite kanalą pavadinimu **Hiustonas** ir ketinate sukurti naują nuolaidą pavadinimu **Atgal į mokyklą.**</span><span class="sxs-lookup"><span data-stu-id="481f9-130">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School.**</span></span>
2.  <span data-ttu-id="481f9-131">Kadangi kainodaros ir nuolaidų strategija apima kanalo nuolaidų galimybę, kurdami kanalą visada sukuriate konkretaus kanalo kainų grupę.</span><span class="sxs-lookup"><span data-stu-id="481f9-131">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3.  <span data-ttu-id="481f9-132">Turite kainų grupę **Hiustono KG**, ir ji priskirta **Hiustono** kanalui.</span><span class="sxs-lookup"><span data-stu-id="481f9-132">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4.  <span data-ttu-id="481f9-133">Sukūrę naująją nuolaidą **Atgal į mokyklą**, **Nuolaidos** puslapio viršuje turite spustelėti **Kainų grupės**.</span><span class="sxs-lookup"><span data-stu-id="481f9-133">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="481f9-134">Atsidarys **Nuolaidos kainų grupių** puslapis.</span><span class="sxs-lookup"><span data-stu-id="481f9-134">The **Discount price groups** page will open.</span></span> <span data-ttu-id="481f9-135">Toliau spustelėkite **Naujas** ir pasirinkite kainų grupę **Hiustono KG**.</span><span class="sxs-lookup"><span data-stu-id="481f9-135">Next, click **New** and select the **Houston-PG** price group.</span></span>
5.  <span data-ttu-id="481f9-136">Dabar galite įgalinti nuolaidą ir ją perduoti į kanalą.</span><span class="sxs-lookup"><span data-stu-id="481f9-136">Now you can enable the discount and push it to the channel.</span></span>



<a name="see-also"></a><span data-ttu-id="481f9-137">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="481f9-137">See also</span></span>
--------

[<span data-ttu-id="481f9-138">Kainų koregavimas ir nuolaidos</span><span class="sxs-lookup"><span data-stu-id="481f9-138">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)




