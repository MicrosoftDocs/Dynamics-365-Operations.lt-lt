---
title: Kurti ir tvarkyti atsargų blokavimą
description: Ši tema aprašo, kaip neleisti kitiems siunčiamiems šaltinio dokumentams rezervuoti faktiškai turimų atsargų naudojant atsargų blokavimą.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956163"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="5e737-103">Kurti ir tvarkyti atsargų blokavimą</span><span class="sxs-lookup"><span data-stu-id="5e737-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5e737-104">Ši tema aprašo, kaip neleisti kitiems siunčiamiems šaltinio dokumentams rezervuoti faktiškai turimų atsargų naudojant atsargų blokavimą.</span><span class="sxs-lookup"><span data-stu-id="5e737-104">This topic describes how to use an inventory blocking to prevent physical on-hand inventory from being reserved by other outbound source documents.</span></span> <span data-ttu-id="5e737-105">Prieš pradėdami šioje temoje aprašytas procedūras, turite turėti objektą, kuriam parengsite fizines atsargas.</span><span class="sxs-lookup"><span data-stu-id="5e737-105">Before you start the procedures in this topic, you must have an item that physical on-hand inventory is available for.</span></span>

## <a name="block-inventory"></a><span data-ttu-id="5e737-106">Blokuoti atsargas</span><span class="sxs-lookup"><span data-stu-id="5e737-106">Block inventory</span></span>

<span data-ttu-id="5e737-107">Norėdami sukurti atsargų blokavimo įrašą, kad atsargos būtų užblokuotos, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5e737-107">To create an inventory blocking record so that inventory is blocked, follow these steps.</span></span>

1. <span data-ttu-id="5e737-108">Pasirinkite **Atsargų valdymas \> Periodinės užduotys \> Atsargų blokavimas**.</span><span class="sxs-lookup"><span data-stu-id="5e737-108">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="5e737-109">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="5e737-109">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5e737-110">Naujo blokavimo įrašo antraštėje nustatykite prekės, kurią norite blokuoti, lauką Prekės numeris **įveskite** aprašymą.</span><span class="sxs-lookup"><span data-stu-id="5e737-110">On the header of the new blocking record, set the **Item number** field to the item that you want to block, and enter a description.</span></span>
1. <span data-ttu-id="5e737-111">**Bendra** „FastTab” skirtuke, **Kiekis** lauke, įveskite blokuojamų elementų skaičių.</span><span class="sxs-lookup"><span data-stu-id="5e737-111">On the **General** FastTab, in the **Quantity** field, enter the number of items to block.</span></span>
1. <span data-ttu-id="5e737-112">Atsargų **dimensijų** „FastTab“ nurodykite vieta ir sandėlį, kuriame šiuo metu yra prekės, kurias norite užblokuoti.</span><span class="sxs-lookup"><span data-stu-id="5e737-112">On the **Inventory dimensions** FastTab, specify the site and warehouse where the items that you want to block are currently located.</span></span>
1. <span data-ttu-id="5e737-113">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="5e737-113">On the Action Pane, select **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="5e737-114">Atnaujinti atsargų blokavimo sąlygas</span><span class="sxs-lookup"><span data-stu-id="5e737-114">Update the conditions of the inventory blocking</span></span>

<span data-ttu-id="5e737-115">Norėdami atnaujinti atsargų blokavimo įrašą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5e737-115">To update an inventory blocking record, follow these steps.</span></span>

1. <span data-ttu-id="5e737-116">Pasirinkite **Atsargų valdymas \> Periodinės užduotys \> Atsargų blokavimas**.</span><span class="sxs-lookup"><span data-stu-id="5e737-116">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="5e737-117">Sąrašo srityje pažymėkite atitinkamą blokavimo įrašą.</span><span class="sxs-lookup"><span data-stu-id="5e737-117">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="5e737-118">Redaguokite įrašą pagal reikalą.</span><span class="sxs-lookup"><span data-stu-id="5e737-118">Edit the record as required.</span></span> <span data-ttu-id="5e737-119">Pavyzdžiui, galite keisti tikėtinos datos **Laukelio** vertę, tam, kad galėtumėte nurodyti, kada galima rezervuoti užblokuotas atsargas, priskirdami numatomą datą.</span><span class="sxs-lookup"><span data-stu-id="5e737-119">For example, you might change the value of the **Expected date** field to indicate when the blocked inventory is expected to become available for reservation.</span></span> <span data-ttu-id="5e737-120">Jei **pasirinkta pasirinktis** Numatomi gaviniai, data bus rodoma tikėtinoje operacijoje.</span><span class="sxs-lookup"><span data-stu-id="5e737-120">If the **Expected receipts** option is selected, the date will appear on the expected transaction.</span></span> <span data-ttu-id="5e737-121">(Toliau **Numatyta, kad** numatyta gavimo pasirinktis pasirenkama rankiniu būdu kuriant blokavimo įrašą.)</span><span class="sxs-lookup"><span data-stu-id="5e737-121">(The **Expected receipts** option is selected by default when you manually create a blocking record.)</span></span>
1. <span data-ttu-id="5e737-122">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="5e737-122">On the Action Pane, select **Save**.</span></span>

## <a name="unblock-inventory"></a><span data-ttu-id="5e737-123">Atsargų atblokavimas</span><span class="sxs-lookup"><span data-stu-id="5e737-123">Unblock inventory</span></span>

<span data-ttu-id="5e737-124">Norėdami panaikinti atsargų blokavimo įrašą, kad atsargos būtų atblokuotos, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5e737-124">To remove an inventory blocking record so that inventory is unblocked, follow these steps.</span></span>

1. <span data-ttu-id="5e737-125">Pasirinkite **Atsargų valdymas \> Periodinės užduotys \> Atsargų blokavimas**.</span><span class="sxs-lookup"><span data-stu-id="5e737-125">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="5e737-126">Sąrašo srityje pažymėkite atitinkamą blokavimo įrašą.</span><span class="sxs-lookup"><span data-stu-id="5e737-126">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="5e737-127">Rinkitės **Naikinti** veiksmų juostoje.</span><span class="sxs-lookup"><span data-stu-id="5e737-127">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="5e737-128">Jus paragins patvirtinti operaciją.</span><span class="sxs-lookup"><span data-stu-id="5e737-128">You're prompted to confirm the operation.</span></span> <span data-ttu-id="5e737-129">Pasirinkite **Taip** tam, kad tęstumėte.</span><span class="sxs-lookup"><span data-stu-id="5e737-129">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="5e737-130">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="5e737-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
