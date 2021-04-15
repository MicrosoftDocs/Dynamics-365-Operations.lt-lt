---
title: Mažmeninė parduotuvė nerodoma atsiėmimo parduotuvių sąraše
description: Šioje temoje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai parduotuvės nėra parduotuvių, kuriose galima atsiimti prekes, sąraše.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 652f5f1a779a412c21c18814071ba0fb7dd2e155
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585454"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a><span data-ttu-id="440d3-103">Mažmeninė parduotuvė nerodoma atsiėmimo parduotuvių sąraše</span><span class="sxs-lookup"><span data-stu-id="440d3-103">Retail store doesn't appear in the list of stores to pick up from</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="440d3-104">Šioje temoje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai parduotuvės nėra parduotuvių, kuriose galima atsiimti prekes, sąraše.</span><span class="sxs-lookup"><span data-stu-id="440d3-104">This topic provides troubleshooting guidance that can help when a retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="description"></a><span data-ttu-id="440d3-105">aprašymas</span><span class="sxs-lookup"><span data-stu-id="440d3-105">Description</span></span>

<span data-ttu-id="440d3-106">Mažmeninės prekybos parduotuvė, kur galima atsiimti prekes, nerodoma sąraše.</span><span class="sxs-lookup"><span data-stu-id="440d3-106">A retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="resolution"></a><span data-ttu-id="440d3-107">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="440d3-107">Resolution</span></span>

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a><span data-ttu-id="440d3-108">Konfigūruokite „Commerce” būstinė parduotuvės adreso ilgumą ir platumos</span><span class="sxs-lookup"><span data-stu-id="440d3-108">Configure the longitude and latitude for the store address in Commerce headquarters</span></span>

<span data-ttu-id="440d3-109">Norėdami konfigūruoti, „Commerce” būstinės parduotuvės adreso ilgumą ir platumos, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="440d3-109">To configure the longitude and latitude for the store address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="440d3-110">Eikite į **Mažmeninė prekyba ir prekyba \> Kanalai \> Parduotuvės \> Visos parduotuvės**.</span><span class="sxs-lookup"><span data-stu-id="440d3-110">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="440d3-111">Raskite parduotuvę, kurią norite matyti el. komercijos svetainės atsiėmimo parinktyse.</span><span class="sxs-lookup"><span data-stu-id="440d3-111">Find the store that you want to appear among the pickup options on the e-commerce site.</span></span> <span data-ttu-id="440d3-112">Užsirašykite savo **Valdymo vieneto numeris** vertę.</span><span class="sxs-lookup"><span data-stu-id="440d3-112">Make a note of its **Operating unit number** value.</span></span>
1. <span data-ttu-id="440d3-113">Eikite į **Organizacijos valdymas \> Organizacijos \> Valdymo vienetai**.</span><span class="sxs-lookup"><span data-stu-id="440d3-113">Go to **Organization administration \> Organizations \> Operating units**.</span></span>
1. <span data-ttu-id="440d3-114">Ieškokite valdymo vieneto numerio, kurį pažymėjote anksčiau, tada ieškos rezultatuose pasirinkti valdymo vienetą.</span><span class="sxs-lookup"><span data-stu-id="440d3-114">Search for the operating unit number that you noted earlier, and then select the operating unit in the search results.</span></span>
1. <span data-ttu-id="440d3-115">„FasTab” skirtuke **Adresai** pasirinkite **Daugiau parinkčių**  ir tada pasirinkite **Išplėstiniai**.</span><span class="sxs-lookup"><span data-stu-id="440d3-115">On the **Addresses** FastTab, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="440d3-116">„FastTab” skirtuke **Bendra**, įsitikinkite, kad laukai **Ilguma** ir **Platuma** yra teisingai nustatyti.</span><span class="sxs-lookup"><span data-stu-id="440d3-116">On the **General** FastTab, make sure that the **Longitude** and **Latitude** fields are correctly set.</span></span> <span data-ttu-id="440d3-117">Atlikdami šį veiksmą, įsitikinkite, kad vertės teisingai nurodytos kaip teigiami arba neigiami skaičiai.</span><span class="sxs-lookup"><span data-stu-id="440d3-117">As part of this step, make sure that the values are correctly specified as positive or negative numbers.</span></span>

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a><span data-ttu-id="440d3-118">Įvykdymo grupių konfigūravimas „Commerce” būstinėje</span><span class="sxs-lookup"><span data-stu-id="440d3-118">Configure fulfillment groups in Commerce headquarters</span></span>

<span data-ttu-id="440d3-119">Norėdami konfigūruoti įvykdymo grupes, „Commerce” būstinėje, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="440d3-119">To configure fulfillment groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="440d3-120">Eikite į **Mažmeninė prekyba ir prekyba \> Kanalai \> Internetinės parduotuvės**.</span><span class="sxs-lookup"><span data-stu-id="440d3-120">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="440d3-121">Pasirinkite internetinę parduotuvę, kurią norite sukonfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="440d3-121">Select the online store to configure.</span></span>
1. <span data-ttu-id="440d3-122">Veiksmų srityje pasirinkite skirtuką **Nustatyti**, tada pasirinkite **Vykdymo grupės priskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="440d3-122">On the Action Pane, select **Set up**, and then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="440d3-123">Puslapyje **Įvykdymo grupės paskyrimas**, pasirinkite interneto parduotuvės įvykdymo grupę.</span><span class="sxs-lookup"><span data-stu-id="440d3-123">On the **Fulfillment group assignment** page, select the fulfillment group for the online store.</span></span>
1. <span data-ttu-id="440d3-124">Dalyje **Sąranka** įsitikinkite, kad įvykdymo grupei skirta mažmeninės prekybos parduotuvė tinkamai sukonfigūruota.</span><span class="sxs-lookup"><span data-stu-id="440d3-124">Under **Setup**, make sure that the retail store is correctly configured for the fulfillment group.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="440d3-125">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="440d3-125">Additional resources</span></span> 

[<span data-ttu-id="440d3-126">Valdymo vieneto kūrimas</span><span class="sxs-lookup"><span data-stu-id="440d3-126">Create an operating unit</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit)

[<span data-ttu-id="440d3-127">Interneto kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="440d3-127">Set up an online channel</span></span>](../channel-setup-online.md)