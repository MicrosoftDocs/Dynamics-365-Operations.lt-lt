---
title: "Pateikti gamybos užsakymus"
description: "Išleistas gamybos užsakymas yra užsakymas, kurį leista gaminti. Terminas Išleistas naudojamas apibūdinti gamybos užsakymo ciklo būsenai, kai gamybos užsakymą galima vykdyti gamybos ceche ir atliekant sandėlio procesus."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: aa38c50a58bed5702332182b9e0827b863f536f7
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="release-production-orders"></a><span data-ttu-id="f96cc-104">Pateikti gamybos užsakymus</span><span class="sxs-lookup"><span data-stu-id="f96cc-104">Release production orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f96cc-105">Išleistas gamybos užsakymas yra užsakymas, kurį leista gaminti.</span><span class="sxs-lookup"><span data-stu-id="f96cc-105">A released production order is an order that has been authorized for production.</span></span> <span data-ttu-id="f96cc-106">Terminas Išleistas naudojamas apibūdinti gamybos užsakymo ciklo būsenai, kai gamybos užsakymą galima vykdyti gamybos ceche ir atliekant sandėlio procesus.</span><span class="sxs-lookup"><span data-stu-id="f96cc-106">The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.</span></span> 

<a name="characteristics-of-the-released-state"></a><span data-ttu-id="f96cc-107">Būsenos Patvirtinta charakteristikos</span><span class="sxs-lookup"><span data-stu-id="f96cc-107">Characteristics of the Released state</span></span>
-------------------------------------

<span data-ttu-id="f96cc-108">Būsena **Patvirtinta** yra viena gamybos užsakymo ciklo būsenų.</span><span class="sxs-lookup"><span data-stu-id="f96cc-108">The **Released** state is one state in the production order life cycle.</span></span> <span data-ttu-id="f96cc-109">Gamybos užsakymus, kurie yra būsenos **Patvirtinta**, galima vykdyti gamybos ceche ir atliekant sandėlio procesus.</span><span class="sxs-lookup"><span data-stu-id="f96cc-109">Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes.</span></span> <span data-ttu-id="f96cc-110">Būsenos **Patvirtinta** charakteristikos yra tokios:</span><span class="sxs-lookup"><span data-stu-id="f96cc-110">The **Released** state has the following characteristics:</span></span>

-   <span data-ttu-id="f96cc-111">Gamybos užsakymo būseną galima pakeisti į **Patvirtinta** gamybos užsakyme arba vykdant paketinį vykdymą.</span><span class="sxs-lookup"><span data-stu-id="f96cc-111">A production order can be changed to the **Released** state either from the production order or by using a batch process.</span></span> <span data-ttu-id="f96cc-112">Gamybos užsakymą taip pat galima atnaujinti automatiškai suplanuotuose gamybos užsakymuose, patvirtintuose puslapio **Bendrasis planas** lauke **Tvirtinimo laiko ribos**.</span><span class="sxs-lookup"><span data-stu-id="f96cc-112">The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.</span></span>
-   <span data-ttu-id="f96cc-113">Būsena **patvirtintų** yra cecho operatoriams (operatoriams) skirtas signalas pradėti vykdyti gamybos užduotis ceche.</span><span class="sxs-lookup"><span data-stu-id="f96cc-113">The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.</span></span>
-   <span data-ttu-id="f96cc-114">Gamybos dokumentai, pvz., maršruto kortelės, maršruto užduotys ir užduočių kortelės, suteikia informacijos apie gamybos užduotis ir gali būti išduodami.</span><span class="sxs-lookup"><span data-stu-id="f96cc-114">Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.</span></span>
-   <span data-ttu-id="f96cc-115">Esant faktiškai rezervuotų medžiagų, generuojamas sandėlio darbas, kad būtų galima pasirinkti gamybos užsakymo medžiagas.</span><span class="sxs-lookup"><span data-stu-id="f96cc-115">For materials that are physically reserved, warehouse work is generated to pick materials for the production order.</span></span>

## <a name="releasing-jobs-to-the-shop-floor"></a><span data-ttu-id="f96cc-116">Užduočių perdavimas į cechą</span><span class="sxs-lookup"><span data-stu-id="f96cc-116">Releasing jobs to the shop floor</span></span>
<span data-ttu-id="f96cc-117">Išleidus gamybos užsakymą, su užsakymu susijusios gamybos užduotys yra matomos ir paruoštos registruoti.</span><span class="sxs-lookup"><span data-stu-id="f96cc-117">After a production order is released, production jobs that are related to the order are visible and ready for registration.</span></span> <span data-ttu-id="f96cc-118">Operatoriai gali atlikti užduočių registravimus, pvz., pradžios, pabaigos ir užbaigimo, arba puslapyje **Užduoties kortelės terminalas** arba **Užduoties kortelės įrenginys**.</span><span class="sxs-lookup"><span data-stu-id="f96cc-118">The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page.</span></span> <span data-ttu-id="f96cc-119">Registruotas laikas ir kiekis automatiškai perkeliami iš registracijos puslapių į gamybos žurnalus, kad būtų galima sekti sunaudotą laiką ir kiekį.</span><span class="sxs-lookup"><span data-stu-id="f96cc-119">The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.</span></span>

## <a name="route-cards"></a><span data-ttu-id="f96cc-120">Technologinės kortelės</span><span class="sxs-lookup"><span data-stu-id="f96cc-120">Route cards</span></span>
<span data-ttu-id="f96cc-121">Technologinė kortelė pateikia informacijos, gaunamos iš maršruto ir operacijų nustatymų bei iš operacijų ir užduočių planavimo metodų, apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="f96cc-121">A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.</span></span>

## <a name="route-jobs"></a><span data-ttu-id="f96cc-122">Maršruto užduotys</span><span class="sxs-lookup"><span data-stu-id="f96cc-122">Route jobs</span></span>
<span data-ttu-id="f96cc-123">Maršruto užduotyje pateikiama kiekviena smulki operacijos užduotis ir įtraukiamas nustatymo, proceso, laukimo eilėje ir transportavimo laikas.</span><span class="sxs-lookup"><span data-stu-id="f96cc-123">A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times.</span></span> <span data-ttu-id="f96cc-124">Pavyzdžiui, tokiai operacijai, kaip dažymas, gali prireikti atskirų užduočių, tokių kaip nustatymo laikas, dažymo proceso laikas ir laukimo eilėje laikas džiūvimui.</span><span class="sxs-lookup"><span data-stu-id="f96cc-124">For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.</span></span>

## <a name="job-cards"></a><span data-ttu-id="f96cc-125">Užduočių kortelės</span><span class="sxs-lookup"><span data-stu-id="f96cc-125">Job cards</span></span>
<span data-ttu-id="f96cc-126">Užduoties kortelė pateikia atskirų užduočių numerius tam tikrai operacijai.</span><span class="sxs-lookup"><span data-stu-id="f96cc-126">A job card lists the individual job numbers of a particular operation.</span></span> <span data-ttu-id="f96cc-127">Kiekviename puslapyje pateikiama viena užduotis.</span><span class="sxs-lookup"><span data-stu-id="f96cc-127">One job appears on each page.</span></span> <span data-ttu-id="f96cc-128">Užduoties kortelėje įtraukiamos užduotys ir jų numatomi laikai gaunami iš maršruto ir operacijos nustatymo informacijos.</span><span class="sxs-lookup"><span data-stu-id="f96cc-128">The jobs that are included on a job card, and their estimated times, come from the route and operation setup information.</span></span> <span data-ttu-id="f96cc-129">Užduoties kortelėje galite atidaryti puslapį **Gamybos žurnalo eilutės**, **užduoties kortelė**.</span><span class="sxs-lookup"><span data-stu-id="f96cc-129">From a job card, you can open the **Production journal lines**, **job card** page.</span></span> <span data-ttu-id="f96cc-130">Žmonės, prižiūrintys operacijų išteklius, gali pateikti atsiliepimus apie gamybos procesą.</span><span class="sxs-lookup"><span data-stu-id="f96cc-130">People who run operations resources can provide feedback about the production process.</span></span> <span data-ttu-id="f96cc-131">Yra laukų kur galite įvesti suvartojimo statistiką ir informaciją, tokią kaip klaidų kiekis.</span><span class="sxs-lookup"><span data-stu-id="f96cc-131">There are fields where you can enter consumption statistics and information such as the error quantity.</span></span>

## <a name="warehouse-work-for-raw-material-picking"></a><span data-ttu-id="f96cc-132">Sandėlio darbas žaliavoms paimti</span><span class="sxs-lookup"><span data-stu-id="f96cc-132">Warehouse work for raw material picking</span></span>
<span data-ttu-id="f96cc-133">Žaliavų paėmimo darbas generuojamas paleidimo metu.</span><span class="sxs-lookup"><span data-stu-id="f96cc-133">Work for raw material picking is generated during release.</span></span> <span data-ttu-id="f96cc-134">Darbas generuojamas tik tam medžiagų kiekiui, kuris buvo faktiškai rezervuotas gamybos užsakymui prieš pateikiant užsakymą.</span><span class="sxs-lookup"><span data-stu-id="f96cc-134">Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released.</span></span> <span data-ttu-id="f96cc-135">Norint generuoti žaliavų paėmimo sandėlyje darbą reikalinga toliau nurodyta sąranka.</span><span class="sxs-lookup"><span data-stu-id="f96cc-135">The following setup is required to generate warehouse work for raw material picking:</span></span>

-   <span data-ttu-id="f96cc-136">Žaliavų paėmimo vietos nurodymas nustato, iš kurios sandėlio vietos paimti medžiagas</span><span class="sxs-lookup"><span data-stu-id="f96cc-136">A location directive for raw materials picking that determines which warehouse location to pick the materials in</span></span>
-   <span data-ttu-id="f96cc-137">Žaliavų bangos šablonas, kuriame sukonfigūruotos sandėlio darbo vykdymo strategijos</span><span class="sxs-lookup"><span data-stu-id="f96cc-137">A wave template for raw materials, where policies for the execution of warehouse work are configured</span></span>
-   <span data-ttu-id="f96cc-138">Gamybos įvesties vieta, nurodanti, kur dedamos medžiagos</span><span class="sxs-lookup"><span data-stu-id="f96cc-138">A production input location that determines where materials are put</span></span>





