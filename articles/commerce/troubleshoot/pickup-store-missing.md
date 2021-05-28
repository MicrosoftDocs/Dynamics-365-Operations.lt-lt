---
title: Mažmeninė parduotuvė nerodoma atsiėmimo parduotuvių sąraše
description: Šioje temoje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai parduotuvės nėra parduotuvių, kuriose galima atsiimti prekes, sąraše.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: ad7ddf8a17640471a2344c45eef76f682d29ef2b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020832"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a><span data-ttu-id="8c63e-103">Mažmeninė parduotuvė nerodoma atsiėmimo parduotuvių sąraše</span><span class="sxs-lookup"><span data-stu-id="8c63e-103">Retail store doesn't appear in the list of stores to pick up from</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8c63e-104">Šioje temoje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai parduotuvės nėra parduotuvių, kuriose galima atsiimti prekes, sąraše.</span><span class="sxs-lookup"><span data-stu-id="8c63e-104">This topic provides troubleshooting guidance that can help when a retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="description"></a><span data-ttu-id="8c63e-105">aprašymas</span><span class="sxs-lookup"><span data-stu-id="8c63e-105">Description</span></span>

<span data-ttu-id="8c63e-106">Mažmeninės prekybos parduotuvė, kur galima atsiimti prekes, nerodoma sąraše.</span><span class="sxs-lookup"><span data-stu-id="8c63e-106">A retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="resolution"></a><span data-ttu-id="8c63e-107">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="8c63e-107">Resolution</span></span>

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a><span data-ttu-id="8c63e-108">Konfigūruokite „Commerce” būstinė parduotuvės adreso ilgumą ir platumos</span><span class="sxs-lookup"><span data-stu-id="8c63e-108">Configure the longitude and latitude for the store address in Commerce headquarters</span></span>

<span data-ttu-id="8c63e-109">Norėdami konfigūruoti, „Commerce” būstinės parduotuvės adreso ilgumą ir platumos, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="8c63e-109">To configure the longitude and latitude for the store address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="8c63e-110">Eikite į **Mažmeninė prekyba ir prekyba \> Kanalai \> Parduotuvės \> Visos parduotuvės**.</span><span class="sxs-lookup"><span data-stu-id="8c63e-110">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="8c63e-111">Raskite parduotuvę, kurią norite matyti el. komercijos svetainės atsiėmimo parinktyse.</span><span class="sxs-lookup"><span data-stu-id="8c63e-111">Find the store that you want to appear among the pickup options on the e-commerce site.</span></span> <span data-ttu-id="8c63e-112">Užsirašykite savo **Valdymo vieneto numeris** vertę.</span><span class="sxs-lookup"><span data-stu-id="8c63e-112">Make a note of its **Operating unit number** value.</span></span>
1. <span data-ttu-id="8c63e-113">Eikite į **Organizacijos valdymas \> Organizacijos \> Valdymo vienetai**.</span><span class="sxs-lookup"><span data-stu-id="8c63e-113">Go to **Organization administration \> Organizations \> Operating units**.</span></span>
1. <span data-ttu-id="8c63e-114">Ieškokite valdymo vieneto numerio, kurį pažymėjote anksčiau, tada ieškos rezultatuose pasirinkti valdymo vienetą.</span><span class="sxs-lookup"><span data-stu-id="8c63e-114">Search for the operating unit number that you noted earlier, and then select the operating unit in the search results.</span></span>
1. <span data-ttu-id="8c63e-115">„FasTab” skirtuke **Adresai** pasirinkite **Daugiau parinkčių**  ir tada pasirinkite **Išplėstiniai**.</span><span class="sxs-lookup"><span data-stu-id="8c63e-115">On the **Addresses** FastTab, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="8c63e-116">„FastTab” skirtuke **Bendra**, įsitikinkite, kad laukai **Ilguma** ir **Platuma** yra teisingai nustatyti.</span><span class="sxs-lookup"><span data-stu-id="8c63e-116">On the **General** FastTab, make sure that the **Longitude** and **Latitude** fields are correctly set.</span></span> <span data-ttu-id="8c63e-117">Atlikdami šį veiksmą, įsitikinkite, kad vertės teisingai nurodytos kaip teigiami arba neigiami skaičiai.</span><span class="sxs-lookup"><span data-stu-id="8c63e-117">As part of this step, make sure that the values are correctly specified as positive or negative numbers.</span></span>

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a><span data-ttu-id="8c63e-118">Įvykdymo grupių konfigūravimas „Commerce” būstinėje</span><span class="sxs-lookup"><span data-stu-id="8c63e-118">Configure fulfillment groups in Commerce headquarters</span></span>

<span data-ttu-id="8c63e-119">Norėdami konfigūruoti įvykdymo grupes, „Commerce” būstinėje, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="8c63e-119">To configure fulfillment groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="8c63e-120">Eikite į **Mažmeninė prekyba ir prekyba \> Kanalai \> Internetinės parduotuvės**.</span><span class="sxs-lookup"><span data-stu-id="8c63e-120">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="8c63e-121">Pasirinkite internetinę parduotuvę, kurią norite sukonfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="8c63e-121">Select the online store to configure.</span></span>
1. <span data-ttu-id="8c63e-122">Veiksmų srityje pasirinkite skirtuką **Nustatyti**, tada pasirinkite **Vykdymo grupės priskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="8c63e-122">On the Action Pane, select **Set up**, and then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="8c63e-123">Puslapyje **Įvykdymo grupės paskyrimas**, pasirinkite interneto parduotuvės įvykdymo grupę.</span><span class="sxs-lookup"><span data-stu-id="8c63e-123">On the **Fulfillment group assignment** page, select the fulfillment group for the online store.</span></span>
1. <span data-ttu-id="8c63e-124">Dalyje **Sąranka** įsitikinkite, kad įvykdymo grupei skirta mažmeninės prekybos parduotuvė tinkamai sukonfigūruota.</span><span class="sxs-lookup"><span data-stu-id="8c63e-124">Under **Setup**, make sure that the retail store is correctly configured for the fulfillment group.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8c63e-125">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="8c63e-125">Additional resources</span></span> 

[<span data-ttu-id="8c63e-126">Valdymo vieneto kūrimas</span><span class="sxs-lookup"><span data-stu-id="8c63e-126">Create an operating unit</span></span>](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md)

[<span data-ttu-id="8c63e-127">Interneto kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="8c63e-127">Set up an online channel</span></span>](../channel-setup-online.md)