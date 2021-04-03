---
title: Klientų įrašai nerodomi „Commerce“ valdymo srityje
description: Šioje temoje pateikiamos trikčių šalinimo gairės, kurios gali padėti, kai klientų įrašai iš karto nerodomi „Commerce“ valdymo srityje.
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
ms.openlocfilehash: 790468ac244f1647c07024604886c65d22feca24
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585446"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a><span data-ttu-id="34661-103">Klientų įrašai nerodomi „Commerce“ valdymo srityje</span><span class="sxs-lookup"><span data-stu-id="34661-103">Customer records don't appear in Commerce headquarters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34661-104">Šioje temoje pateikiamos trikčių šalinimo gairės, kurios gali padėti, kai klientų įrašai iš karto nerodomi „Commerce“ valdymo srityje.</span><span class="sxs-lookup"><span data-stu-id="34661-104">This topic provides troubleshooting guidance that can help when customer records don't immediately appear in Commerce headquarters.</span></span>

## <a name="description"></a><span data-ttu-id="34661-105">aprašymas</span><span class="sxs-lookup"><span data-stu-id="34661-105">Description</span></span>

<span data-ttu-id="34661-106">Kai sukuriate naują kliento įrašą naudodami registracijos srautą el. komercijos vitrinoje, atitinkamas kliento įrašas iš karto nerodomas „Commerce“ valdymo srityje.</span><span class="sxs-lookup"><span data-stu-id="34661-106">When you create a new customer record by using the sign-up flow in the e-commerce storefront, the corresponding customer record doesn't immediately appear in Commerce headquarters.</span></span>

## <a name="resolution"></a><span data-ttu-id="34661-107">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="34661-107">Resolution</span></span>

### <a name="disable-customer-creation-in-async-mode"></a><span data-ttu-id="34661-108">Išjungti kliento kūrimą „Async“ režimu</span><span class="sxs-lookup"><span data-stu-id="34661-108">Disable customer creation in async mode</span></span>

> [!IMPORTANT]
> <span data-ttu-id="34661-109">Jei išjungsite asinchroninį klientų kūrimą, gali būti paveiktas sistemos našumas, nes sukūrus kiekvieną įrašą „Commerce“ valdymo srityje bus sukuriama užklausa realiuoju laiku.</span><span class="sxs-lookup"><span data-stu-id="34661-109">If you disable asynchronous customer creation, system performance could be affected, because creation of each record will produce a real-time request to Commerce headquarters.</span></span> <span data-ttu-id="34661-110">Be to, jei „Commerce“ valdymo sritis neveikia (pvz., aptarnavimo srautų metu), dėl visų naujų klientų kūrimo srautų bus gaunamos klaidos.</span><span class="sxs-lookup"><span data-stu-id="34661-110">In addition, if Commerce headquarters is down (for example, during servicing flows), any new customer creation flows will produce errors.</span></span>

<span data-ttu-id="34661-111">Kad išjungtumėte kliento kūrimą asinchroniniu režimu „Commerce“ valdymo srityje, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="34661-111">To disable customer creation in async mode in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="34661-112">Eikite į **Mažmeninė prekyba ir komercija \> Kanalo sąranka \> Interneto parduotuvės sąranka \> Funkcijų profiliai**.</span><span class="sxs-lookup"><span data-stu-id="34661-112">Go to **Retail and Commerce \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="34661-113">Jei savo interneto kanalui dar nenaudojate funkcijų profilio, sukurkite jį.</span><span class="sxs-lookup"><span data-stu-id="34661-113">If you aren't already using a functionality profile for your online channel, create one.</span></span>
1. <span data-ttu-id="34661-114">Įsitikinkite, kad parinktis **Kurti klientą asinchroniniu režimu** nustatyta kaip **Ne**.</span><span class="sxs-lookup"><span data-stu-id="34661-114">Make sure that the **Create customer in async mode** option is set to **No**.</span></span>
1. <span data-ttu-id="34661-115">Eikite į **Mažmeninė prekyba ir prekyba \> Kanalai \> Internetinės parduotuvės**.</span><span class="sxs-lookup"><span data-stu-id="34661-115">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="34661-116">Pasirinkite interneto parduotuvę, kad išjungtumėte asinchroninį kliento kūrimą.</span><span class="sxs-lookup"><span data-stu-id="34661-116">Select the online store to disable asynchronous customer creation for.</span></span>
1. <span data-ttu-id="34661-117">Skirtuke **Bendra** patikrinkite, ar laukelis **Funkcijų profilis** nustatytas kaip funkcijų profilis, kurį naudojate savo interneto kanalui.</span><span class="sxs-lookup"><span data-stu-id="34661-117">On the **General** tab, make sure that the **Functionality profile** field is set to the functionality profile that you're using for your online channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34661-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="34661-118">Additional resources</span></span>

[<span data-ttu-id="34661-119">B2C nuomotojo nustatymas „Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="34661-119">Setup a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)