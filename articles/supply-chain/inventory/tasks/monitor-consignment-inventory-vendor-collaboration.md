---
title: "Konsignacinių atsargų stebėjimas naudojant tiekėjo bendradarbiavimą"
description: "Šioje procedūroje parodoma, kaip naudoti tiekėjo bendradarbiavimą, norint pamatyti informaciją apie kliento produktų konsignacijos atsargų lygį."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 567be29bd9989b3471b22d5a970ed0e51e4549ec
ms.contentlocale: lt-lt
ms.lasthandoff: 09/12/2017

---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a><span data-ttu-id="e3d83-103">Konsignacinių atsargų stebėjimas naudojant tiekėjo bendradarbiavimą</span><span class="sxs-lookup"><span data-stu-id="e3d83-103">Monitor consignment inventory using vendor collaboration</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e3d83-104">Šioje procedūroje parodoma, kaip naudoti tiekėjo bendradarbiavimą, norint pamatyti informaciją apie kliento produktų konsignacijos atsargų lygį.</span><span class="sxs-lookup"><span data-stu-id="e3d83-104">This procedure shows how to use vendor collaboration to see information about the stock level of product that you have placed in consignment with a customer.</span></span> <span data-ttu-id="e3d83-105">Taip pat galite stebėti žaliavų sunaudojimą, kai klientas perima atsargų nuosavybę.</span><span class="sxs-lookup"><span data-stu-id="e3d83-105">You can also monitor the consumption of the stock when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="e3d83-106">Šią procedūrą galite naudoti USMF demonstracinių duomenų įmonėje.</span><span class="sxs-lookup"><span data-stu-id="e3d83-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="e3d83-107">Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="e3d83-107">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="view-consumed-inventory"></a><span data-ttu-id="e3d83-108">Sunaudotų atsargų peržiūra</span><span class="sxs-lookup"><span data-stu-id="e3d83-108">View consumed inventory</span></span>
1. <span data-ttu-id="e3d83-109">Eikite į Tiekėjo bendradarbiavimas > Konsignacijos atsargos > Produktai, gauti iš konsignacijos atsargų.</span><span class="sxs-lookup"><span data-stu-id="e3d83-109">Go to Vendor collaboration > Consignment inventory > Products received from consignment inventory.</span></span>
    * <span data-ttu-id="e3d83-110">Sąraše rodomos produkto gavimo kvito eilutės, kurios buvo sugeneruotos, kai konsignacijos atsargų savininkas buvo pakeistas iš tiekėjo į klientą.</span><span class="sxs-lookup"><span data-stu-id="e3d83-110">The list shows the product receipt lines that were generated when ownership of the consignment inventory was changed from the vendor to the customer.</span></span> <span data-ttu-id="e3d83-111">Jums gali tekti slinkti į dešinę, norint pamatyti kiekius ir kitą informaciją.</span><span class="sxs-lookup"><span data-stu-id="e3d83-111">You might have to scroll to the right to see quantities and other information.</span></span> <span data-ttu-id="e3d83-112">Galite naudoti šio sąrašo informaciją, norėdami kurti SF klientui.</span><span class="sxs-lookup"><span data-stu-id="e3d83-112">You can use the information in this list to generate invoices for your customer.</span></span> <span data-ttu-id="e3d83-113">Taip pat galite eksportuoti duomenis į „Microsoft Excel“.</span><span class="sxs-lookup"><span data-stu-id="e3d83-113">You can also export the data to Microsoft Excel.</span></span>   
2. <span data-ttu-id="e3d83-114">Spustelėkite Peržiūrėti pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="e3d83-114">Click View purchase order.</span></span>
3. <span data-ttu-id="e3d83-115">Išplėskite skyrių Eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="e3d83-115">Expand the Line details section.</span></span>
    * <span data-ttu-id="e3d83-116">Eilutė pažymėta kaip Konsignacija, o antraštės skyrius nurodo, kad pirkimo užsakymo būsena yra Gauta.</span><span class="sxs-lookup"><span data-stu-id="e3d83-116">The line is marked as Consignment, and the header section shows that the purchase order has a status of Received.</span></span>  
4. <span data-ttu-id="e3d83-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e3d83-117">Close the page.</span></span>

## <a name="view-on-hand-inventory"></a><span data-ttu-id="e3d83-118">Rodyti turimas atsargas</span><span class="sxs-lookup"><span data-stu-id="e3d83-118">View on-hand inventory</span></span>
1. <span data-ttu-id="e3d83-119">Eikite į Tiekėjo bendradarbiavimas > Konsignacijos atsargos > Turimos konsignacijos atsargos.</span><span class="sxs-lookup"><span data-stu-id="e3d83-119">Go to Vendor collaboration > Consignment inventory > On-hand consignment inventory.</span></span>
    * <span data-ttu-id="e3d83-120">Puslapyje Turimos konsignacijos atsargos rodomos kliento sandėlio atsargos, kuris priklauso jums.</span><span class="sxs-lookup"><span data-stu-id="e3d83-120">The On-hand consignment inventory page shows the stock that you own at the customer’s warehouse.</span></span> <span data-ttu-id="e3d83-121">Galima rodyti papildomas dimensijas, pvz., teritoriją ir sandėlį, spustelėjus skirtuką Rodyti dimensijas.</span><span class="sxs-lookup"><span data-stu-id="e3d83-121">You can show additional dimensions, such as the site and warehouse, by clicking the Display dimensions tab.</span></span>   
