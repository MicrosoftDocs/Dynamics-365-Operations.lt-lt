---
title: Atsargų pasiekiamumas dvigubam rašymui
description: Šioje temoje pateikiama informacija apie atsargų pasiekiamumo tikrinimą dvigubo rašymo funkcijoje.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 227a2062a7985a787f8278c196f7df2fb6f31691
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443877"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="ac924-103">Atsargų pasiekiamumas dvigubam rašymui</span><span class="sxs-lookup"><span data-stu-id="ac924-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ac924-104">Naudodami atsargų pasiekiamumą, galite patikrinti savo atsargas prieš pridėdami produktą į **Kainos**, **Užsakymai** arba **Sąskaitos faktūros** puslapį „Microsoft Dynamics 365 Sales”.</span><span class="sxs-lookup"><span data-stu-id="ac924-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="ac924-105">Pavyzdžiui, patikrinkite atsargas ir nustatykite įvykdymo datą kaip vieną iš pagrindinių užduočių [potencialaus grynųjų pinigų](dual-write-prospect-to-cash.md) proceso metu.</span><span class="sxs-lookup"><span data-stu-id="ac924-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="ac924-106">Jeigu nepakanka atsargų, galite įvertinti pristatymo datą pagal suplanuotų atsargų gavimą ir išdavimą.</span><span class="sxs-lookup"><span data-stu-id="ac924-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="ac924-107">Taip pat galite patikrinti produkto prieinamų atsargų (ATP) informaciją, kurioje galima rasti ATP kiekį iš anksto apibrėžtoje laiko riboje.</span><span class="sxs-lookup"><span data-stu-id="ac924-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="ac924-108">Turimos atsargos</span><span class="sxs-lookup"><span data-stu-id="ac924-108">On-hand inventory</span></span>

<span data-ttu-id="ac924-109">„Dynamics 365 Sales“ naujas **Turimos atsargos** mygtukas pridėtas **Kainos**, **Užsakymai** ir **Sąskaitos faktūros** puslapių antraštėse.</span><span class="sxs-lookup"><span data-stu-id="ac924-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="ac924-110">Spustelėjus šį mygtuką, pasirodo dialogo langas, kuriame galite nurodyti įmonę ir produktą, kurio turimas atsargas norite patikrinti.</span><span class="sxs-lookup"><span data-stu-id="ac924-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="ac924-111">Šis dialogo langas parodo tokią pačią informaciją kaip [Turimos atsargos](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="ac924-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="ac924-112">Dialogo langas grąžina atsargų informaciją iš „Dynamics 365 Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="ac924-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="ac924-113">Pateikiama informacija apie šiuos kiekius:</span><span class="sxs-lookup"><span data-stu-id="ac924-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="ac924-114">Turimas kiekis</span><span class="sxs-lookup"><span data-stu-id="ac924-114">On-hand quantity</span></span>
- <span data-ttu-id="ac924-115">Rezervuotas turimas kiekis</span><span class="sxs-lookup"><span data-stu-id="ac924-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="ac924-116">Prieinamas turimas kiekis</span><span class="sxs-lookup"><span data-stu-id="ac924-116">Available on-hand quantity</span></span>
- <span data-ttu-id="ac924-117">Užsakytas kiekis.</span><span class="sxs-lookup"><span data-stu-id="ac924-117">Ordered quantity</span></span>
- <span data-ttu-id="ac924-118">Užsakymo kiekis</span><span class="sxs-lookup"><span data-stu-id="ac924-118">On-order quantity</span></span>
- <span data-ttu-id="ac924-119">Rezervuotas užsakytas kiekis</span><span class="sxs-lookup"><span data-stu-id="ac924-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="ac924-120">Bendras prieinamas kiekis</span><span class="sxs-lookup"><span data-stu-id="ac924-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="ac924-121">ATP informacija</span><span class="sxs-lookup"><span data-stu-id="ac924-121">ATP information</span></span>

<span data-ttu-id="ac924-122">„Sales” naujas **ATP informacija** mygtukas pridėtas prie eilutės elementų **Kainos**, **Užsakymai** ir **Sąskaitos faktūros** puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="ac924-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="ac924-123">Spustelėjus šį mygtuką, pasirodo dialogo langas, kuriame galite nurodyti įmonę, produktą, atsargų vietą, atsargų sandėlį ir užsakymo kiekį.</span><span class="sxs-lookup"><span data-stu-id="ac924-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="ac924-124">Šis dialogo langas turi tuos pačius parametrus, aprašytus [Užsakymo vykdymo įsipareigojimuose](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="ac924-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="ac924-125">Dialogo langas grąžina ATP informaciją iš „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="ac924-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="ac924-126">Pateikiama informacija apie šiuos kiekius:</span><span class="sxs-lookup"><span data-stu-id="ac924-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="ac924-127">ATP kiekis</span><span class="sxs-lookup"><span data-stu-id="ac924-127">ATP quantity</span></span>
- <span data-ttu-id="ac924-128">Gavimo kiekis</span><span class="sxs-lookup"><span data-stu-id="ac924-128">Receipt quantity</span></span>
- <span data-ttu-id="ac924-129">Išdavimo kiekis</span><span class="sxs-lookup"><span data-stu-id="ac924-129">Issue quantity</span></span>
- <span data-ttu-id="ac924-130">Turimas kiekis</span><span class="sxs-lookup"><span data-stu-id="ac924-130">On-hand quantity</span></span>
