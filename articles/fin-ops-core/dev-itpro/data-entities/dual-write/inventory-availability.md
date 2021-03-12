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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: a7bfe998d2d787203a507a831c171fc43b03fedc
ms.sourcegitcommit: cc9921295f26804259cc9ec5137788ec9f2a4c6f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/08/2021
ms.locfileid: "4839554"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="3ae11-103">Atsargų pasiekiamumas dvigubam rašymui</span><span class="sxs-lookup"><span data-stu-id="3ae11-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3ae11-104">Naudodami atsargų pasiekiamumą, galite patikrinti savo atsargas prieš pridėdami produktą į **Kainos**, **Užsakymai** arba **Sąskaitos faktūros** puslapį „Microsoft Dynamics 365 Sales”.</span><span class="sxs-lookup"><span data-stu-id="3ae11-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="3ae11-105">Pavyzdžiui, patikrinkite atsargas ir nustatykite įvykdymo datą kaip vieną iš pagrindinių užduočių [potencialaus grynųjų pinigų](dual-write-prospect-to-cash.md) proceso metu.</span><span class="sxs-lookup"><span data-stu-id="3ae11-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="3ae11-106">Jeigu nepakanka atsargų, galite įvertinti pristatymo datą pagal suplanuotų atsargų gavimą ir išdavimą.</span><span class="sxs-lookup"><span data-stu-id="3ae11-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="3ae11-107">Taip pat galite patikrinti produkto prieinamų atsargų (ATP) informaciją, kurioje galima rasti ATP kiekį iš anksto apibrėžtoje laiko riboje.</span><span class="sxs-lookup"><span data-stu-id="3ae11-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="3ae11-108">Turimos atsargos</span><span class="sxs-lookup"><span data-stu-id="3ae11-108">On-hand inventory</span></span>

<span data-ttu-id="3ae11-109">„Dynamics 365 Sales“ naujas **Turimos atsargos** mygtukas pridėtas **Kainos**, **Užsakymai** ir **Sąskaitos faktūros** puslapių antraštėse.</span><span class="sxs-lookup"><span data-stu-id="3ae11-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="3ae11-110">Spustelėjus šį mygtuką, pasirodo dialogo langas, kuriame galite nurodyti įmonę ir produktą, kurio turimas atsargas norite patikrinti.</span><span class="sxs-lookup"><span data-stu-id="3ae11-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="3ae11-111">Šis dialogo langas parodo tokią pačią informaciją kaip [Turimos atsargos](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="3ae11-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="3ae11-112">Dialogo langas grąžina atsargų informaciją iš „Dynamics 365 Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="3ae11-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="3ae11-113">Pateikiama informacija apie šiuos kiekius:</span><span class="sxs-lookup"><span data-stu-id="3ae11-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="3ae11-114">Turimas kiekis</span><span class="sxs-lookup"><span data-stu-id="3ae11-114">On-hand quantity</span></span>
- <span data-ttu-id="3ae11-115">Rezervuotas turimas kiekis</span><span class="sxs-lookup"><span data-stu-id="3ae11-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="3ae11-116">Prieinamas turimas kiekis</span><span class="sxs-lookup"><span data-stu-id="3ae11-116">Available on-hand quantity</span></span>
- <span data-ttu-id="3ae11-117">Užsakytas kiekis.</span><span class="sxs-lookup"><span data-stu-id="3ae11-117">Ordered quantity</span></span>
- <span data-ttu-id="3ae11-118">Užsakymo kiekis</span><span class="sxs-lookup"><span data-stu-id="3ae11-118">On-order quantity</span></span>
- <span data-ttu-id="3ae11-119">Rezervuotas užsakytas kiekis</span><span class="sxs-lookup"><span data-stu-id="3ae11-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="3ae11-120">Bendras prieinamas kiekis</span><span class="sxs-lookup"><span data-stu-id="3ae11-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="3ae11-121">ATP informacija</span><span class="sxs-lookup"><span data-stu-id="3ae11-121">ATP information</span></span>

<span data-ttu-id="3ae11-122">„Sales” naujas **ATP informacija** mygtukas pridėtas prie eilutės elementų **Kainos**, **Užsakymai** ir **Sąskaitos faktūros** puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="3ae11-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="3ae11-123">Spustelėjus šį mygtuką, pasirodo dialogo langas, kuriame galite nurodyti įmonę, produktą, atsargų vietą, atsargų sandėlį ir užsakymo kiekį.</span><span class="sxs-lookup"><span data-stu-id="3ae11-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="3ae11-124">Šis dialogo langas turi tuos pačius parametrus, aprašytus [Užsakymo vykdymo įsipareigojimuose](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="3ae11-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="3ae11-125">Dialogo langas grąžina ATP informaciją iš „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="3ae11-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="3ae11-126">Pateikiama informacija apie šiuos kiekius:</span><span class="sxs-lookup"><span data-stu-id="3ae11-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="3ae11-127">ATP kiekis</span><span class="sxs-lookup"><span data-stu-id="3ae11-127">ATP quantity</span></span>
- <span data-ttu-id="3ae11-128">Gavimo kiekis</span><span class="sxs-lookup"><span data-stu-id="3ae11-128">Receipt quantity</span></span>
- <span data-ttu-id="3ae11-129">Išdavimo kiekis</span><span class="sxs-lookup"><span data-stu-id="3ae11-129">Issue quantity</span></span>
- <span data-ttu-id="3ae11-130">Turimas kiekis</span><span class="sxs-lookup"><span data-stu-id="3ae11-130">On-hand quantity</span></span>

## <a name="how-it-works"></a><span data-ttu-id="3ae11-131">Kaip tai veikia</span><span class="sxs-lookup"><span data-stu-id="3ae11-131">How it works</span></span>

<span data-ttu-id="3ae11-132">Kai pasirenkate mygtuką **Turimos atsargos** puslapiuose **Pasiūlymai**, **Užsakymai**, arba **Sąskaitos faktūros** tiesioginio dvigubo rašymo iškvietimas pateikiamas **Turimų atsargų** API.</span><span class="sxs-lookup"><span data-stu-id="3ae11-132">When you select the **On-hand Inventory** button on the **Quotes**, **Orders**, or **Invoices** page, a live dual-write call is made to the **Onhand inventory** API.</span></span> <span data-ttu-id="3ae11-133">API apskaičiuoja turimos tam tikro produkto atsargas.</span><span class="sxs-lookup"><span data-stu-id="3ae11-133">The API calculates the on-hand inventory for the given product.</span></span> <span data-ttu-id="3ae11-134">Rezultatas saugomas **„InventCDSInventoryOnHandRequestEntity”** ir **„InventCDSInventoryOnHandEntryEntity”** lentelėse, o tada įrašomas į „Dataverse” naudojant dvigubą rašymą.</span><span class="sxs-lookup"><span data-stu-id="3ae11-134">The result is stored in the **InventCDSInventoryOnHandRequestEntity** and **InventCDSInventoryOnHandEntryEntity** tables, and then is written to Dataverse by dual-write.</span></span> <span data-ttu-id="3ae11-135">Norėdami naudoti šią funkciją, turite paleisti šias dvigubo rašymo schemas.</span><span class="sxs-lookup"><span data-stu-id="3ae11-135">To use this functionality, you need to run the following dual-write maps.</span></span> <span data-ttu-id="3ae11-136">Praleiskite pradinį sinchronizavimą, kai paleidžiate schemas.</span><span class="sxs-lookup"><span data-stu-id="3ae11-136">Skip initial synchronization when you run the maps.</span></span>

- <span data-ttu-id="3ae11-137">Turimų CDS atsargų įrašai („msdyn_inventoryonhandentries”)</span><span class="sxs-lookup"><span data-stu-id="3ae11-137">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>
- <span data-ttu-id="3ae11-138">Turimų CDS atsargų užklausos („msdyn_inventoryonhandrequests”)</span><span class="sxs-lookup"><span data-stu-id="3ae11-138">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

## <a name="templates"></a><span data-ttu-id="3ae11-139">Šablonai</span><span class="sxs-lookup"><span data-stu-id="3ae11-139">Templates</span></span>
<span data-ttu-id="3ae11-140">Šie šablonai yra galimi rodyti turimų atsargų duomenims.</span><span class="sxs-lookup"><span data-stu-id="3ae11-140">The following templates are available for the exposing the onhand inventory data.</span></span>

<span data-ttu-id="3ae11-141">„Finance and Operations” programos</span><span class="sxs-lookup"><span data-stu-id="3ae11-141">Finance and Operations apps</span></span> | <span data-ttu-id="3ae11-142">„Customer engagement“ programa</span><span class="sxs-lookup"><span data-stu-id="3ae11-142">Customer engagement app</span></span> | <span data-ttu-id="3ae11-143">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="3ae11-143">Description</span></span> 
---|---|---
[<span data-ttu-id="3ae11-144">CDS turimų atsargų įrašai</span><span class="sxs-lookup"><span data-stu-id="3ae11-144">CDS inventory on-hand entries</span></span>](#145) | <span data-ttu-id="3ae11-145">„msdyn_inventoryonhandentries”</span><span class="sxs-lookup"><span data-stu-id="3ae11-145">msdyn_inventoryonhandentries</span></span> |
[<span data-ttu-id="3ae11-146">CDS turimų atsargų užklausos</span><span class="sxs-lookup"><span data-stu-id="3ae11-146">CDS inventory on-hand requests</span></span>](#147) | <span data-ttu-id="3ae11-147">„msdyn_inventoryonhanrequests”</span><span class="sxs-lookup"><span data-stu-id="3ae11-147">msdyn_inventoryonhandrequests</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a> <span data-ttu-id="3ae11-148">Turimų CDS atsargų įrašai („msdyn_inventoryonhandentries”)</span><span class="sxs-lookup"><span data-stu-id="3ae11-148">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>

<span data-ttu-id="3ae11-149">Naudojant šį šabloną sinchronizuojami duomenys tarp „Finance and Operations“ programų ir „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="3ae11-149">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="3ae11-150">„Finance and Operations“ laukas</span><span class="sxs-lookup"><span data-stu-id="3ae11-150">Finance and Operations field</span></span> | <span data-ttu-id="3ae11-151">Schemos tipas</span><span class="sxs-lookup"><span data-stu-id="3ae11-151">Map type</span></span> | <span data-ttu-id="3ae11-152">„Customer engagement“ laukas</span><span class="sxs-lookup"><span data-stu-id="3ae11-152">Customer engagement field</span></span> | <span data-ttu-id="3ae11-153">Numatytoji reikšmė</span><span class="sxs-lookup"><span data-stu-id="3ae11-153">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a><span data-ttu-id="3ae11-154">Turimų CDS atsargų užklausos (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="3ae11-154">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

<span data-ttu-id="3ae11-155">Naudojant šį šabloną sinchronizuojami duomenys tarp „Finance and Operations“ programų ir „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="3ae11-155">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="3ae11-156">„Finance and Operations“ laukas</span><span class="sxs-lookup"><span data-stu-id="3ae11-156">Finance and Operations field</span></span> | <span data-ttu-id="3ae11-157">Schemos tipas</span><span class="sxs-lookup"><span data-stu-id="3ae11-157">Map type</span></span> | <span data-ttu-id="3ae11-158">„Customer engagement“ laukas</span><span class="sxs-lookup"><span data-stu-id="3ae11-158">Customer engagement field</span></span> | <span data-ttu-id="3ae11-159">Numatytoji reikšmė</span><span class="sxs-lookup"><span data-stu-id="3ae11-159">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |




