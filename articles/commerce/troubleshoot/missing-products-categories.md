---
title: Nukopijavus aplinką trūksta produktų ir kategorijų
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai po svetainės kopijavimo iš vienos aplinkos į kitą arba toje pačioje aplinkoje trūksta produktų ir kategorijų.
author: Reza-Assadi
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
ms.openlocfilehash: 527fd0fa62775f65f61b538474b1d45d1a0155ed
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801728"
---
# <a name="products-and-categories-missing-after-environment-copy"></a><span data-ttu-id="1cf3c-103">Nukopijavus aplinką trūksta produktų ir kategorijų</span><span class="sxs-lookup"><span data-stu-id="1cf3c-103">Products and categories missing after environment copy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1cf3c-104">Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai po svetainės kopijavimo iš vienos aplinkos į kitą arba toje pačioje aplinkoje trūksta produktų ir kategorijų.</span><span class="sxs-lookup"><span data-stu-id="1cf3c-104">This topic provides troubleshooting guidance that can help when products and categories are missing after a site is copied between environments or within the same environment.</span></span>

## <a name="description"></a><span data-ttu-id="1cf3c-105">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="1cf3c-105">Description</span></span>

<span data-ttu-id="1cf3c-106">Kai svetainė nukopijuojama iš vienos aplinkos į kitą arba toje pačioje aplinkoje, svetainėje trūksta produktų ir kategorijų.</span><span class="sxs-lookup"><span data-stu-id="1cf3c-106">After a site is copied from one environment to another, or within the same environment, the products and categories are missing from the site.</span></span> <span data-ttu-id="1cf3c-107">Produktų ir kategorijų trūks el. prekybos parduotuvėje bei „Commerce“ svetainių daryklės skirtuke **Produktai**.</span><span class="sxs-lookup"><span data-stu-id="1cf3c-107">The products and categories will be missing from the e-commerce storefront and from the **Products** tab in Commerce site builder.</span></span>

## <a name="resolution"></a><span data-ttu-id="1cf3c-108">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="1cf3c-108">Resolution</span></span>

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a><span data-ttu-id="1cf3c-109">Susieti kanalo valdymo vieneto numerį su naujai nukopijuota svetaine „Commerce” svetainių daryklėje</span><span class="sxs-lookup"><span data-stu-id="1cf3c-109">Map the channel operating unit number to a newly copied site in Commerce site builder</span></span>

<span data-ttu-id="1cf3c-110">Norėdami susieti kanalo valdymo vieneto numerį (OUN) su naujai nukopijuota svetaine „Commerce” svetainių daryklėje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1cf3c-110">To map the channel operating unit number (OUN) to a newly copied site in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="1cf3c-111">Pasirinkite naujai nukopijuotą svetainę.</span><span class="sxs-lookup"><span data-stu-id="1cf3c-111">Select the newly copied site.</span></span>
1. <span data-ttu-id="1cf3c-112">Dalyje **Svetainės parametrai** pasirinkite **Kanalai**.</span><span class="sxs-lookup"><span data-stu-id="1cf3c-112">Under **Site settings**, select **Channels**.</span></span>
1. <span data-ttu-id="1cf3c-113">Šalia kanalo pavadinimo pasirinkite daugtaškį (**...**), tada pasirinkite **Keisti internetinės parduotuvės kanalą**.</span><span class="sxs-lookup"><span data-stu-id="1cf3c-113">Next to the channel name, select the ellipsis (**...**), and then select **Change online store channel**.</span></span>
1. <span data-ttu-id="1cf3c-114">Dialogo lange **Keisti internetinės parduotuvės kanalą** pasirinkite kanalą, kurį norite susieti su naujai nukopijuota svetaine, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1cf3c-114">In the **Change online store channel** dialog box, select the channel to map to the newly copied site, and then select **OK**.</span></span>
1. <span data-ttu-id="1cf3c-115">Pasirinkite **įrašyti ir publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="1cf3c-115">Select **Save and publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1cf3c-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1cf3c-116">Additional resources</span></span>

[<span data-ttu-id="1cf3c-117">Susiekite „Dynamics 365 Commerce“ saitą su interneto kanalu</span><span class="sxs-lookup"><span data-stu-id="1cf3c-117">Associate a Dynamics 365 Commerce site with an online channel</span></span>](../associate-site-online-store.md)
