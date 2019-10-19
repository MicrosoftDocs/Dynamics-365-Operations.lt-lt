---
title: Įrašyti tiekėjo SF ir sugretinti su gautu kiekiu
description: Gavę sąskaitą faktūrą iš tiekėjo už prekes ir paslaugas, pateiktas pirkimo užsakyme, atsižvelgiant į verslo procesus, gali reikėti, kad prekės ar paslaugos būtų gautos prieš pateikiant sąskaitą faktūrą apmokėti.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 66d84f497775ce4f988242dd2b327bf4854faef5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188745"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a><span data-ttu-id="aedcc-103">Įrašyti tiekėjo SF ir sugretinti su gautu kiekiu</span><span class="sxs-lookup"><span data-stu-id="aedcc-103">Record vendor invoice and match against received quantity</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aedcc-104">Gavę sąskaitą faktūrą iš tiekėjo už prekes ir paslaugas, pateiktas pirkimo užsakyme, atsižvelgiant į verslo procesus, gali reikėti, kad prekės ar paslaugos būtų gautos prieš pateikiant sąskaitą faktūrą apmokėti.</span><span class="sxs-lookup"><span data-stu-id="aedcc-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="aedcc-105">Prieš pradėdami įsitikinkite, kad pasirinktas SF gretinimo konfigūracijos raktas.</span><span class="sxs-lookup"><span data-stu-id="aedcc-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="aedcc-106">Puslapyje Mokėtinų sumų parametrai įsitikinkite, kad pasirinkta parinktis Įgalinti SF gretinimo tikrinimą, laukas Registruoti SF su nesutapimais nustatytas į Reikalauti patvirtinimo, o laukas Eilučių atitikimo strategija nustatytas į Tripusis atitikimas.</span><span class="sxs-lookup"><span data-stu-id="aedcc-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="aedcc-107">Šioje procedūroje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="aedcc-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="aedcc-108">Šiuos veiksmus paprastai atlieka mokėtinų sumų vadovo arba apskaitos vadovo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="aedcc-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="aedcc-109">Pirkimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="aedcc-109">Create a purchase order</span></span>
1. <span data-ttu-id="aedcc-110">Eikite į Visi pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="aedcc-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="aedcc-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="aedcc-111">Click New.</span></span>
3. <span data-ttu-id="aedcc-112">Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="aedcc-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="aedcc-113">Lauke Tiekėjo sąskaita surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aedcc-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="aedcc-114">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="aedcc-114">Click OK.</span></span>
6. <span data-ttu-id="aedcc-115">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="aedcc-115">Click Add line.</span></span>
7. <span data-ttu-id="aedcc-116">Lauke Prekės numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aedcc-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="aedcc-117">Veiksmų srityje spustelėkite Pirkti.</span><span class="sxs-lookup"><span data-stu-id="aedcc-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="aedcc-118">Spustelėkite Patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="aedcc-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="aedcc-119">Registruoti produkto gavimo kvitą</span><span class="sxs-lookup"><span data-stu-id="aedcc-119">Post a product receipt</span></span>
1. <span data-ttu-id="aedcc-120">Veiksmų srityje spustelėkite Gauti.</span><span class="sxs-lookup"><span data-stu-id="aedcc-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="aedcc-121">Spustelėkite Produkto gavimo kvitas.</span><span class="sxs-lookup"><span data-stu-id="aedcc-121">Click Product receipt.</span></span>
3. <span data-ttu-id="aedcc-122">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="aedcc-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="aedcc-123">Lauke Produkto gavimo kvitas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aedcc-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="aedcc-124">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="aedcc-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="aedcc-125">Įrašyti bei gretinti tiekėjo SF ir produkto gavimo kvitą</span><span class="sxs-lookup"><span data-stu-id="aedcc-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="aedcc-126">Veiksmų srityje spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="aedcc-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="aedcc-127">Spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="aedcc-127">Click Invoice.</span></span>
3. <span data-ttu-id="aedcc-128">Lauke Numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aedcc-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="aedcc-129">Spustelėkite Numatyt. iš: užsakyto kiekio, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="aedcc-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="aedcc-130">Lauke Numatytasis eilučių kiekis pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="aedcc-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="aedcc-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="aedcc-131">Click OK.</span></span>
7. <span data-ttu-id="aedcc-132">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="aedcc-132">Click Yes.</span></span>
8. <span data-ttu-id="aedcc-133">Spustelėkite Sugretinti gavimo dokumentus.</span><span class="sxs-lookup"><span data-stu-id="aedcc-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="aedcc-134">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="aedcc-134">Click OK.</span></span>
10. <span data-ttu-id="aedcc-135">Veiksmų srityje spustelėkite Peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="aedcc-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="aedcc-136">Spustelėkite Gretinimo informacija.</span><span class="sxs-lookup"><span data-stu-id="aedcc-136">Click Matching details.</span></span>

