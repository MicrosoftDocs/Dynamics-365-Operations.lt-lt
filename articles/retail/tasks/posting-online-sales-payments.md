--- 
title: "Pardavimo ir mokėjimų internetu registravimas"
description: "Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančią paketinę užduotį, norint kurti internetinės parduotuvės operacijų pardavimo užsakymus ir mokėjimus."
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 13839bbe6ca03f3cfc7036fce87477bf7d5af2a7
ms.contentlocale: lt-lt
ms.lasthandoff: 10/16/2018

---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="e5fb6-103">Pardavimo ir mokėjimų internetu registravimas</span><span class="sxs-lookup"><span data-stu-id="e5fb6-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e5fb6-104">Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančią paketinę užduotį, norint kurti internetinės parduotuvės operacijų pardavimo užsakymus ir mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="e5fb6-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="e5fb6-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="e5fb6-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="e5fb6-106">Eikite į Visos darbo sritys > Mažmeninės prekybos parduotuvės finansai.</span><span class="sxs-lookup"><span data-stu-id="e5fb6-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="e5fb6-107">Spustelėkite Sinchronizuoti užsakymus.</span><span class="sxs-lookup"><span data-stu-id="e5fb6-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="e5fb6-108">Lauke Organizacijos hierarchija pasirinkite „Mažmeninės prekybos parduotuvės pagal regioną“.</span><span class="sxs-lookup"><span data-stu-id="e5fb6-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="e5fb6-109">Pasirinkite konkrečią interneto parduotuvę arba pasirinkite mazgą, jei norite kurti parduotuvių grupės paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="e5fb6-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="e5fb6-110">Spustelėkite rodyklę ir įtraukite savo pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="e5fb6-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="e5fb6-111">Spustelėkite skirtuką Vykdyti fone.</span><span class="sxs-lookup"><span data-stu-id="e5fb6-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="e5fb6-112">Pažymėkite arba atžymėkite žymės langelį Paketinis vykdymas.</span><span class="sxs-lookup"><span data-stu-id="e5fb6-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="e5fb6-113">Spustelėkite Pasikartojimas.</span><span class="sxs-lookup"><span data-stu-id="e5fb6-113">Click Recurrence.</span></span>
7. <span data-ttu-id="e5fb6-114">Pasirinkite parinktį Nėra pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="e5fb6-114">Select the No end date option.</span></span>
8. <span data-ttu-id="e5fb6-115">Lauke Skaičius įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="e5fb6-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="e5fb6-116">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e5fb6-116">Click OK.</span></span>
10. <span data-ttu-id="e5fb6-117">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e5fb6-117">Click OK.</span></span>


