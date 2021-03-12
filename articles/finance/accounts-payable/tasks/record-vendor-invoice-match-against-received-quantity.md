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
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be1e818e8a97684248c9c0b9d43c39e631f855f5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979268"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a><span data-ttu-id="22bd0-103">Įrašyti tiekėjo SF ir sugretinti su gautu kiekiu</span><span class="sxs-lookup"><span data-stu-id="22bd0-103">Record vendor invoice and match against received quantity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="22bd0-104">Gavę sąskaitą faktūrą iš tiekėjo už prekes ir paslaugas, pateiktas pirkimo užsakyme, atsižvelgiant į verslo procesus, gali reikėti, kad prekės ar paslaugos būtų gautos prieš pateikiant sąskaitą faktūrą apmokėti.</span><span class="sxs-lookup"><span data-stu-id="22bd0-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="22bd0-105">Prieš pradėdami įsitikinkite, kad pasirinktas SF gretinimo konfigūracijos raktas.</span><span class="sxs-lookup"><span data-stu-id="22bd0-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="22bd0-106">Puslapyje Mokėtinų sumų parametrai įsitikinkite, kad pasirinkta parinktis Įgalinti SF gretinimo tikrinimą, laukas Registruoti SF su nesutapimais nustatytas į Reikalauti patvirtinimo, o laukas Eilučių atitikimo strategija nustatytas į Tripusis atitikimas.</span><span class="sxs-lookup"><span data-stu-id="22bd0-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="22bd0-107">Šioje procedūroje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="22bd0-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="22bd0-108">Šiuos veiksmus paprastai atlieka mokėtinų sumų vadovo arba apskaitos vadovo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="22bd0-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="22bd0-109">Pirkimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="22bd0-109">Create a purchase order</span></span>
1. <span data-ttu-id="22bd0-110">Eikite į Visi pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="22bd0-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="22bd0-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="22bd0-111">Click New.</span></span>
3. <span data-ttu-id="22bd0-112">Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="22bd0-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="22bd0-113">Lauke Tiekėjo sąskaita surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="22bd0-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="22bd0-114">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="22bd0-114">Click OK.</span></span>
6. <span data-ttu-id="22bd0-115">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="22bd0-115">Click Add line.</span></span>
7. <span data-ttu-id="22bd0-116">Lauke Prekės numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="22bd0-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="22bd0-117">Veiksmų srityje spustelėkite Pirkti.</span><span class="sxs-lookup"><span data-stu-id="22bd0-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="22bd0-118">Spustelėkite Patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="22bd0-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="22bd0-119">Registruoti produkto gavimo kvitą</span><span class="sxs-lookup"><span data-stu-id="22bd0-119">Post a product receipt</span></span>
1. <span data-ttu-id="22bd0-120">Veiksmų srityje spustelėkite Gauti.</span><span class="sxs-lookup"><span data-stu-id="22bd0-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="22bd0-121">Spustelėkite Produkto gavimo kvitas.</span><span class="sxs-lookup"><span data-stu-id="22bd0-121">Click Product receipt.</span></span>
3. <span data-ttu-id="22bd0-122">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="22bd0-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="22bd0-123">Lauke Produkto gavimo kvitas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="22bd0-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="22bd0-124">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="22bd0-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="22bd0-125">Įrašyti bei gretinti tiekėjo SF ir produkto gavimo kvitą</span><span class="sxs-lookup"><span data-stu-id="22bd0-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="22bd0-126">Veiksmų srityje spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="22bd0-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="22bd0-127">Spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="22bd0-127">Click Invoice.</span></span>
3. <span data-ttu-id="22bd0-128">Lauke Numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="22bd0-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="22bd0-129">Spustelėkite Numatyt. iš: užsakyto kiekio, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="22bd0-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="22bd0-130">Lauke Numatytasis eilučių kiekis pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="22bd0-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="22bd0-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="22bd0-131">Click OK.</span></span>
7. <span data-ttu-id="22bd0-132">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="22bd0-132">Click Yes.</span></span>
8. <span data-ttu-id="22bd0-133">Spustelėkite Sugretinti gavimo dokumentus.</span><span class="sxs-lookup"><span data-stu-id="22bd0-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="22bd0-134">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="22bd0-134">Click OK.</span></span>
10. <span data-ttu-id="22bd0-135">Veiksmų srityje spustelėkite Peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="22bd0-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="22bd0-136">Spustelėkite Gretinimo informacija.</span><span class="sxs-lookup"><span data-stu-id="22bd0-136">Click Matching details.</span></span>

