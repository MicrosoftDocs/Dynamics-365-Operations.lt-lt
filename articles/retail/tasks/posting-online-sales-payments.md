--- 
title: " Pardavimo ir mokėjimų internetu registravimas"
description: "Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančią paketinę užduotį, norint kurti internetinės parduotuvės operacijų pardavimo užsakymus ir mokėjimus."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 2feaf580c7ae1fc53f9257f117576c99764c6ea0
ms.contentlocale: lt-lt
ms.lasthandoff: 02/07/2018

---
# <a name="post-online-sales-and-payments"></a><span data-ttu-id="ba049-103"> Pardavimo ir mokėjimų internetu registravimas</span><span class="sxs-lookup"><span data-stu-id="ba049-103">Post online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ba049-104">Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančią paketinę užduotį, norint kurti internetinės parduotuvės operacijų pardavimo užsakymus ir mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="ba049-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="ba049-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="ba049-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="ba049-106">Eikite į Visos darbo sritys > Mažmeninės prekybos parduotuvės finansai.</span><span class="sxs-lookup"><span data-stu-id="ba049-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="ba049-107">Spustelėkite Sinchronizuoti užsakymus.</span><span class="sxs-lookup"><span data-stu-id="ba049-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="ba049-108">Lauke Organizacijos hierarchija pasirinkite „Mažmeninės prekybos parduotuvės pagal regioną“.</span><span class="sxs-lookup"><span data-stu-id="ba049-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="ba049-109">Pasirinkite konkrečią interneto parduotuvę arba pasirinkite mazgą, jei norite kurti parduotuvių grupės paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="ba049-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="ba049-110">Spustelėkite rodyklę ir įtraukite savo pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="ba049-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="ba049-111">Spustelėkite skirtuką Vykdyti fone.</span><span class="sxs-lookup"><span data-stu-id="ba049-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="ba049-112">Pažymėkite arba atžymėkite žymės langelį Paketinis vykdymas.</span><span class="sxs-lookup"><span data-stu-id="ba049-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="ba049-113">Spustelėkite Pasikartojimas.</span><span class="sxs-lookup"><span data-stu-id="ba049-113">Click Recurrence.</span></span>
7. <span data-ttu-id="ba049-114">Pasirinkite parinktį Nėra pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="ba049-114">Select the No end date option.</span></span>
8. <span data-ttu-id="ba049-115">Lauke Skaičius įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="ba049-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="ba049-116">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ba049-116">Click OK.</span></span>
10. <span data-ttu-id="ba049-117">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ba049-117">Click OK.</span></span>


