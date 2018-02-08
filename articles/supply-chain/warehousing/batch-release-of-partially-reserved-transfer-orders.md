---
title: "Iš dalies rezervuotų perkėlimo užsakymų paketinis išleidimas"
description: "Šioje temoje aprašoma, kaip mobiliuoju įrenginiu nustatyti ir taikyti paketinį iš dalies rezervuotų perkėlimo užsakymų išleidimą."
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ba426692e2e404ab75e5730b8205115fc59e402f
ms.openlocfilehash: 4477749c721cf8c8bd244f551d9eca7ec9449fd1
ms.contentlocale: lt-lt
ms.lasthandoff: 02/08/2018

---

# <a name="batch-release-of-partially-reserved-transfer-orders"></a><span data-ttu-id="55285-103">Iš dalies rezervuotų perkėlimo užsakymų paketinis išleidimas</span><span class="sxs-lookup"><span data-stu-id="55285-103">Batch release of partially reserved transfer orders</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="55285-104">Paketinio iš dalies rezervuotų perkėlimo užsakymų išleidimo funkcija leidžia naudojant paketinę užduotį į sandėlį iš dalies išleisti perkėlimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="55285-104">The functionality for batch release of partially reserved transfer orders lets you partially release transfer orders to a warehouse by using a batch job.</span></span>
<span data-ttu-id="55285-105">Kadangi galite pasirinkti išleisti dalinį kiekį, prieš išleisdami užsakymą neprivalote laukti, kol sandėlyje bus visas užsakymo kiekis.</span><span class="sxs-lookup"><span data-stu-id="55285-105">Because you have the option to release a partial quantity, you don’t have to wait for the whole order quantity to be available in the warehouse before you release an order.</span></span>

<span data-ttu-id="55285-106">Užsakymų išleidimas į sandėlį yra patobulinto sandėlio valdymo procesas.</span><span class="sxs-lookup"><span data-stu-id="55285-106">The release of orders to a warehouse is an advanced warehouse management process.</span></span> <span data-ttu-id="55285-107">Šis procesas apima tokias veiklas kaip paėmimas, pakavimas ir siuntimas, kurias sandėlio darbininkas gali atlikti naudodamas mobilųjį įrenginį.</span><span class="sxs-lookup"><span data-stu-id="55285-107">This process involves activities, such as picking, packing, and shipping, that a warehouse worker can perform by using a mobile device.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="55285-108">Kai taikoma</span><span class="sxs-lookup"><span data-stu-id="55285-108">Where it applies</span></span>

<span data-ttu-id="55285-109">Naudojant šią funkciją užsakymai į sandėlį išleidžiami naudojant paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="55285-109">For this functionality, transfer orders are released to a warehouse by using a batch job.</span></span> <span data-ttu-id="55285-110">Ši funkcija yra naudinga, kai sandėlyje neturite pakankamai atsargų, tačiau vis tiek norite iš vieno sandėlio į kitą perkelti prekių.</span><span class="sxs-lookup"><span data-stu-id="55285-110">This functionality is useful when you don’t have enough inventory in the warehouse, but you still want to transfer items from one warehouse to another.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="55285-111">Kaip tai nustatoma</span><span class="sxs-lookup"><span data-stu-id="55285-111">How it is set up</span></span>

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="55285-112">Perkėlimo užsakymų ir pardavimo užsakymų įvykdymo kriterijų nurodymas</span><span class="sxs-lookup"><span data-stu-id="55285-112">Specify fulfillment criteria for transfer orders and sales orders</span></span>

<span data-ttu-id="55285-113">Kad, naudojant paketinę užduotį, užsakymą būtų galima iš dalies išleisti į sandėlį, turi būti patenkinti įvykdymo kriterijai.</span><span class="sxs-lookup"><span data-stu-id="55285-113">Before an order can be partially released to a warehouse in a batch, the fulfillment criteria must be met.</span></span> <span data-ttu-id="55285-114">Šiuos įvykdymo kriterijus nustato įvykdymo strategija.</span><span class="sxs-lookup"><span data-stu-id="55285-114">These fulfillment criteria are determined by the fulfillment policy.</span></span>

<span data-ttu-id="55285-115">Perkėlimo užsakymų ir pardavimo užsakymų įvykdymo strategijos nurodomos įmonės lygiu.</span><span class="sxs-lookup"><span data-stu-id="55285-115">Fulfillment policies for transfer orders and sales orders are specified at the company level.</span></span> <span data-ttu-id="55285-116">Atsižvelgiant į įvykdymo strategijos sąranką, paketinio užsakymų išleidimo procesas bus patvirtintas arba atmestas.</span><span class="sxs-lookup"><span data-stu-id="55285-116">Depending on the setup of the fulfillment policy, the release of orders in a batch will be accepted or rejected.</span></span> <span data-ttu-id="55285-117">Tada užsakymai bus atitinkamai apdorojami.</span><span class="sxs-lookup"><span data-stu-id="55285-117">The orders will then be processed accordingly.</span></span>

-   <span data-ttu-id="55285-118">Norėdami sukurti perkėlimo užsakymų ir pardavimo užsakymų įvykdymo strategijų, spustelėkite **Sandėlio valdymas** \> **Sąranka** \> **Išleidimas į sandėlį** \> **Įvykdymo strategija** ir sukurkite įvykdymo strategiją įvesdami pavadinimą bei aprašą.</span><span class="sxs-lookup"><span data-stu-id="55285-118">To create fulfillment policies for transfer orders and sales orders, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then create a fulfillment policy by entering a name and a description.</span></span>

-   <span data-ttu-id="55285-119">Norėdami nurodyti įvykdymo koeficientą, reikšmės tipą ir pranešimą, kuris rodomas pažeidus įvykdymo strategiją, spustelėkite **Sandėlio valdymas** \> **Sąranka** \> **Išleidimas į sandėlį** \> **Įvykdymo strategija** ir nustatykite laukus **Įvykdymo koeficientas**, **Reikšmės tipas** bei **Pranešimas apie įvykdymo pažeidimą**.</span><span class="sxs-lookup"><span data-stu-id="55285-119">To specify a fulfillment rate, a value type, and the message that is shown if the fulfillment policy is violated, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then set the **Fulfillment rate**, **Value type**, and **Fulfillment violation message** fields.</span></span>

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="55285-120">Perkėlimo užsakymų ir pardavimo užsakymų įvykdymo strategijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="55285-120">Set the fulfillment policies for transfer orders and sales orders</span></span>

-   <span data-ttu-id="55285-121">Norėdami nustatyti perkėlimo užsakymų įvykdymo strategijas, spustelėkite **Atsargų valdymas** \> **Sąranka** \> **Atsargų ir sandėlio valdymo parametrai** \> **Perkėlimo užsakymai** \> **Sandėlio valdymas** ir pasirinkite perkėlimo užsakymo įvykdymo strategiją.</span><span class="sxs-lookup"><span data-stu-id="55285-121">To set the fulfillment policies for transfer orders, click **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters** \> **Transfer orders** \> **Warehouse management**, and then select a transfer order fulfillment policy.</span></span>

-   <span data-ttu-id="55285-122">Norėdami nustatyti pardavimo užsakymų įvykdymo strategijas, spustelėkite **Gautinos sumos** \> **Sąranka** \> **Gautinų sumų parametrai** \> **Sandėlio valdymas** ir pasirinkite pardavimo užsakymo įvykdymo strategiją.</span><span class="sxs-lookup"><span data-stu-id="55285-122">To set the fulfillment policies for sales orders, click **Accounts receivable** \> **Setup** \> **Accounts receivable parameters** \> **Warehouse management**, and then select a sales order fulfillment policy.</span></span>

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a><span data-ttu-id="55285-123">Paketinio išleidimo proceso leidimas ir kiekio, kurį reikia išleisti kaip paketą, nurodymas</span><span class="sxs-lookup"><span data-stu-id="55285-123">Allow release in a batch and specify the quantity that should be release in a batch</span></span>

<span data-ttu-id="55285-124">Užsakymai į sandėlį kaip paketas išleidžiami naudojant paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="55285-124">A batch job is used to release orders to a warehouse in a batch.</span></span> <span data-ttu-id="55285-125">Parametrai, atskiriantys užsakymus, kurie turi būti vykdomi naudojant paketinę užduotį, yra nustatomi pačioje paketinėje užduotyje.</span><span class="sxs-lookup"><span data-stu-id="55285-125">The parameters that distinguish the orders that should be run in a batch job are set on the batch job itself.</span></span>

<span data-ttu-id="55285-126">Parametras **Kiekis** nurodo, ar kaip paketas turi būti išleistas visas kiekis, ar fiziškai rezervuotas kiekis.</span><span class="sxs-lookup"><span data-stu-id="55285-126">The **Quantity** parameter specifies whether the whole quantity or the physically reserved quantity should be released in the batch.</span></span> <span data-ttu-id="55285-127">Parametras **Leisti išleisti iš dalies išleistus užsakymus** nurodo, ar kaip paketas išleidžiami užsakymai turi būti patvirtinti, ar atmesti, jei jie buvo iš dalies išleisti anksčiau.</span><span class="sxs-lookup"><span data-stu-id="55285-127">The **Allow release of partially released orders** parameter determines whether orders in the batch should be accepted or rejected if they were partially released earlier.</span></span>

-   <span data-ttu-id="55285-128">Norėdami nustatyti perkėlimo užsakymų parametrus **Kiekis** ir **Leisti išleisti iš dalies išleistus užsakymus**, spustelėkite **Sandėlio valdymas** \> **Išleidimas į sandėlį** \> **Automatinis perkėlimo užsakymų išleidimas**.</span><span class="sxs-lookup"><span data-stu-id="55285-128">To set the **Quantity** and **Allow release of partially released orders** parameters for transfer orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of transfer orders**.</span></span>

-   <span data-ttu-id="55285-129">Norėdami nustatyti pardavimo užsakymų parametrus **Kiekis** ir **Leisti išleisti iš dalies išleistus užsakymus**, spustelėkite **Sandėlio valdymas** \> **Išleidimas į sandėlį** \> **Automatinis pardavimo užsakymų išleidimas**.</span><span class="sxs-lookup"><span data-stu-id="55285-129">To set the **Quantity** and **Allow release of partially released orders** parameters for sales orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of sales orders**.</span></span>

