--- 
title: "Gamybos užsakymo išleidimas"
description: "Šioje procedūroje parodoma, kaip išleisti gamybos užsakymą."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2ae2d84bd12d338c9bada5518c43178b22112006
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="release-a-production-order"></a><span data-ttu-id="aa236-103">Gamybos užsakymo išleidimas</span><span class="sxs-lookup"><span data-stu-id="aa236-103">Release a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aa236-104">Šioje procedūroje parodoma, kaip išleisti gamybos užsakymą.</span><span class="sxs-lookup"><span data-stu-id="aa236-104">This procedure shows how to release a production order.</span></span> <span data-ttu-id="aa236-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="aa236-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="aa236-106">Tai yra ketvirtoji procedūra iš septynių, kurioje paaiškinamas gamybos užsakymo ciklas.</span><span class="sxs-lookup"><span data-stu-id="aa236-106">This is the fourth procedure out of seven which explains the production order lifecycle.</span></span>

1. <span data-ttu-id="aa236-107">Pasirinkite Gamybos kontrolė > Gamybos užsakymai > Visi gamybos užsakymai.</span><span class="sxs-lookup"><span data-stu-id="aa236-107">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="aa236-108">Tinklelyje pasirinkite gamybos užsakymą, kurio būsena yra Suplanuota.</span><span class="sxs-lookup"><span data-stu-id="aa236-108">In the grid, select a production order that has the Scheduled status.</span></span>  
2. <span data-ttu-id="aa236-109">Veiksmų srityje spustelėkite Gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="aa236-109">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="aa236-110">Spustelėkite Išleisti.</span><span class="sxs-lookup"><span data-stu-id="aa236-110">Click Release.</span></span>
    * <span data-ttu-id="aa236-111">Šiame puslapyje galite patvirtinti pasirinktų gamybos užsakymų išleidimą.</span><span class="sxs-lookup"><span data-stu-id="aa236-111">On this page, you can confirm the release of the selected range of production orders.</span></span> <span data-ttu-id="aa236-112">Spustelėkite Pasirinkti, jei norite įtraukti užsakymų.</span><span class="sxs-lookup"><span data-stu-id="aa236-112">Click Select if you want to add orders.</span></span>  
    * <span data-ttu-id="aa236-113">Veiksmas Išleisti nurodo, kada gamybos užsakymas išleidžiamas į gamybos cechą, kad cecho operatoriai galėtų pranešti apie gamybos užduočių eigą.</span><span class="sxs-lookup"><span data-stu-id="aa236-113">The Release step indicates when the production order is released to the production shop floor so that the shop floor operators can report progress on the production jobs.</span></span> <span data-ttu-id="aa236-114">Galima išduoti gamybos dokumentus, kuriuose pateikiama aktuali informacija apie užduočių apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="aa236-114">Production papers that contain relevant information about processing the jobs can be issued.</span></span> <span data-ttu-id="aa236-115">Žaliavų paėmimo sandėlyje darbas generuojamas prekėms, kurios nustatytos sandėlio procesui.</span><span class="sxs-lookup"><span data-stu-id="aa236-115">The warehouse work for raw material picking is generated for the items that are set up for the warehouse process.</span></span>  
4. <span data-ttu-id="aa236-116">Spustelėkite skirtuką Bendra.</span><span class="sxs-lookup"><span data-stu-id="aa236-116">Click the General tab.</span></span>
    * <span data-ttu-id="aa236-117">Pasirinkite, kurias gamybos ataskaitas reikėtų spausdinti.</span><span class="sxs-lookup"><span data-stu-id="aa236-117">Select which production reports should be printed.</span></span> <span data-ttu-id="aa236-118">Užduoties kortelės ataskaita spausdina kiekvienos suplanuotos užduoties puslapį ir reikalauja, kad gamybos užsakymas būtų suplanuotas užduoties lygiu.</span><span class="sxs-lookup"><span data-stu-id="aa236-118">The Job card report prints a page for each scheduled job and requires the production order to be scheduled at the job level.</span></span> <span data-ttu-id="aa236-119">Ataskaitoje pateikiama informacija apie suplanuotą pradžios ir pabaigos laiką, norimą gaminti kiekį ir tai, kuris išteklius apdoroja užduotį.</span><span class="sxs-lookup"><span data-stu-id="aa236-119">The report contains information about the scheduled start and end time, the quantity to produce, and which resource processes the job.</span></span> <span data-ttu-id="aa236-120">Maršruto užduoties ataskaita renka tą pačią informaciją tame pačiame puslapyje, tačiau nespausdina kiekvienos užduoties puslapio.</span><span class="sxs-lookup"><span data-stu-id="aa236-120">The Route job report collects the same information on the same page, but does not print a page for each job.</span></span> <span data-ttu-id="aa236-121">Maršruto kortelės ataskaitoje rodomos tik operacijos, bet ne užduotys.</span><span class="sxs-lookup"><span data-stu-id="aa236-121">The Route card report only shows the operations but not the jobs.</span></span> <span data-ttu-id="aa236-122">Todėl šiai ataskaitai nereikia planuoti užduočių, tačiau ją galima naudoti, kai gamybos užsakymai planuojami operacijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="aa236-122">Therefore, this report does not require job scheduling, but can be used when production orders are scheduled at the operation level.</span></span>  
5. <span data-ttu-id="aa236-123">Spustelėkite žymės langelį Spausdinti technologinę kortelę.</span><span class="sxs-lookup"><span data-stu-id="aa236-123">Click the Print route card checkbox.</span></span>
6. <span data-ttu-id="aa236-124">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="aa236-124">Click OK.</span></span>
7. <span data-ttu-id="aa236-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="aa236-125">Close the page.</span></span>


