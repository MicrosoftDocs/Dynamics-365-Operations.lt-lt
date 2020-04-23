---
title: Konsignacinių atsargų stebėjimas naudojant tiekėjo bendradarbiavimą
description: Šioje procedūroje parodoma, kaip naudoti tiekėjo bendradarbiavimą, norint pamatyti informaciją apie kliento produktų konsignacijos atsargų lygį.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c74f09ee2056ce88442bf8f8ccba3985638525a6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213954"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a><span data-ttu-id="50326-103">Konsignacinių atsargų stebėjimas naudojant tiekėjo bendradarbiavimą</span><span class="sxs-lookup"><span data-stu-id="50326-103">Monitor consignment inventory using vendor collaboration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="50326-104">Šioje procedūroje parodoma, kaip naudoti tiekėjo bendradarbiavimą, norint pamatyti informaciją apie kliento produktų konsignacijos atsargų lygį.</span><span class="sxs-lookup"><span data-stu-id="50326-104">This procedure shows how to use vendor collaboration to see information about the stock level of product that you have placed in consignment with a customer.</span></span> <span data-ttu-id="50326-105">Taip pat galite stebėti žaliavų sunaudojimą, kai klientas perima atsargų nuosavybę.</span><span class="sxs-lookup"><span data-stu-id="50326-105">You can also monitor the consumption of the stock when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="50326-106">Šią procedūrą galite naudoti USMF demonstracinių duomenų įmonėje.</span><span class="sxs-lookup"><span data-stu-id="50326-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="50326-107">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="50326-107">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="view-consumed-inventory"></a><span data-ttu-id="50326-108">Sunaudotų atsargų peržiūra</span><span class="sxs-lookup"><span data-stu-id="50326-108">View consumed inventory</span></span>
1. <span data-ttu-id="50326-109">Eikite į Tiekėjo bendradarbiavimas > Konsignacijos atsargos > Produktai, gauti iš konsignacijos atsargų.</span><span class="sxs-lookup"><span data-stu-id="50326-109">Go to Vendor collaboration > Consignment inventory > Products received from consignment inventory.</span></span>
    * <span data-ttu-id="50326-110">Sąraše rodomos produkto gavimo kvito eilutės, kurios buvo sugeneruotos, kai konsignacijos atsargų savininkas buvo pakeistas iš tiekėjo į klientą.</span><span class="sxs-lookup"><span data-stu-id="50326-110">The list shows the product receipt lines that were generated when ownership of the consignment inventory was changed from the vendor to the customer.</span></span> <span data-ttu-id="50326-111">Jums gali tekti slinkti į dešinę, norint pamatyti kiekius ir kitą informaciją.</span><span class="sxs-lookup"><span data-stu-id="50326-111">You might have to scroll to the right to see quantities and other information.</span></span> <span data-ttu-id="50326-112">Galite naudoti šio sąrašo informaciją, norėdami kurti SF klientui.</span><span class="sxs-lookup"><span data-stu-id="50326-112">You can use the information in this list to generate invoices for your customer.</span></span> <span data-ttu-id="50326-113">Taip pat galite eksportuoti duomenis į „Microsoft Excel“.</span><span class="sxs-lookup"><span data-stu-id="50326-113">You can also export the data to Microsoft Excel.</span></span>   
2. <span data-ttu-id="50326-114">Spustelėkite Peržiūrėti pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="50326-114">Click View purchase order.</span></span>
3. <span data-ttu-id="50326-115">Išplėskite skyrių Eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="50326-115">Expand the Line details section.</span></span>
    * <span data-ttu-id="50326-116">Eilutė pažymėta kaip Konsignacija, o antraštės skyrius nurodo, kad pirkimo užsakymo būsena yra Gauta.</span><span class="sxs-lookup"><span data-stu-id="50326-116">The line is marked as Consignment, and the header section shows that the purchase order has a status of Received.</span></span>  
4. <span data-ttu-id="50326-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="50326-117">Close the page.</span></span>

## <a name="view-on-hand-inventory"></a><span data-ttu-id="50326-118">Rodyti turimas atsargas</span><span class="sxs-lookup"><span data-stu-id="50326-118">View on-hand inventory</span></span>
1. <span data-ttu-id="50326-119">Eikite į Tiekėjo bendradarbiavimas > Konsignacijos atsargos > Turimos konsignacijos atsargos.</span><span class="sxs-lookup"><span data-stu-id="50326-119">Go to Vendor collaboration > Consignment inventory > On-hand consignment inventory.</span></span>
    * <span data-ttu-id="50326-120">Puslapyje Turimos konsignacijos atsargos rodomos jūsų kliento sandėlyje turimos atsargos.</span><span class="sxs-lookup"><span data-stu-id="50326-120">The On-hand consignment inventory page shows the stock that you own at the customer's warehouse.</span></span> <span data-ttu-id="50326-121">Galima rodyti papildomas dimensijas, pvz., teritoriją ir sandėlį, spustelėjus skirtuką Rodyti dimensijas.</span><span class="sxs-lookup"><span data-stu-id="50326-121">You can show additional dimensions, such as the site and warehouse, by clicking the Display dimensions tab.</span></span>   

