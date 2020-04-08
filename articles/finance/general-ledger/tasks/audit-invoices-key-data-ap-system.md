---
title: Audituoti SF ir pagrindinius duomenis AP sistemoje
description: Gavę sąskaitą faktūrą iš tiekėjo už prekes ir paslaugas, pateiktas pirkimo užsakyme, atsižvelgiant į verslo procesus, gali reikėti, kad prekės ar paslaugos būtų gautos prieš pateikiant sąskaitą faktūrą apmokėti.
author: saraschi2
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
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e1af0dac107be6009eb3ca576c49ac5abbd9848
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139949"
---
# <a name="audit-invoices-and-key-data-in-ap-system"></a><span data-ttu-id="016b6-103">Audituoti SF ir pagrindinius duomenis AP sistemoje</span><span class="sxs-lookup"><span data-stu-id="016b6-103">Audit invoices and key data in AP system</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="016b6-104">Gavę sąskaitą faktūrą iš tiekėjo už prekes ir paslaugas, pateiktas pirkimo užsakyme, atsižvelgiant į verslo procesus, gali reikėti, kad prekės ar paslaugos būtų gautos prieš pateikiant sąskaitą faktūrą apmokėti.</span><span class="sxs-lookup"><span data-stu-id="016b6-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="016b6-105">Prieš pradėdami įsitikinkite, kad pasirinktas SF gretinimo konfigūracijos raktas.</span><span class="sxs-lookup"><span data-stu-id="016b6-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="016b6-106">Puslapyje Mokėtinų sumų parametrai įsitikinkite, kad pasirinkta parinktis Įgalinti SF gretinimo tikrinimą, laukas Registruoti SF su nesutapimais nustatytas į Reikalauti patvirtinimo, o laukas Eilučių atitikimo strategija nustatytas į Tripusis atitikimas.</span><span class="sxs-lookup"><span data-stu-id="016b6-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="016b6-107">Šioje procedūroje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="016b6-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="016b6-108">Šiuos veiksmus paprastai atlieka mokėtinų sumų vadovo arba apskaitos vadovo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="016b6-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="016b6-109">Pirkimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="016b6-109">Create a purchase order</span></span>
1. <span data-ttu-id="016b6-110">Eikite į **Visi pirkimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="016b6-110">Go to **All purchase orders**.</span></span>
2. <span data-ttu-id="016b6-111">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="016b6-111">Click **New**.</span></span>
3. <span data-ttu-id="016b6-112">Lauke **Tiekėjo sąskaita** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="016b6-112">In the **Vendor account** field, type a value.</span></span>
4. <span data-ttu-id="016b6-113">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="016b6-113">Click **OK**.</span></span>
5. <span data-ttu-id="016b6-114">Spustelėkite **Pridėti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="016b6-114">Click **Add line**.</span></span>
6. <span data-ttu-id="016b6-115">Lauke **Prekės numeris** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="016b6-115">In the **Item number** field, type a value.</span></span>
7. <span data-ttu-id="016b6-116">Veiksmų srityje spustelėkite **Pirkti**.</span><span class="sxs-lookup"><span data-stu-id="016b6-116">On the Action Pane, click **Purchase**.</span></span>
8. <span data-ttu-id="016b6-117">Spustelėkite **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="016b6-117">Click **Confirm**.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="016b6-118">Registruoti produkto gavimo kvitą</span><span class="sxs-lookup"><span data-stu-id="016b6-118">Post a product receipt</span></span>
1. <span data-ttu-id="016b6-119">Veiksmų srityje spustelėkite **Gauti**.</span><span class="sxs-lookup"><span data-stu-id="016b6-119">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="016b6-120">Spustelėkite **Produkto gavimo kvitas**.</span><span class="sxs-lookup"><span data-stu-id="016b6-120">Click **Product receipt**.</span></span>
3. <span data-ttu-id="016b6-121">Lauke **Produkto gavimo kvitas** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="016b6-121">In the **Product receipt** field, type a value.</span></span>
4. <span data-ttu-id="016b6-122">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="016b6-122">Click **OK**.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="016b6-123">Įrašyti bei gretinti tiekėjo SF ir produkto gavimo kvitą</span><span class="sxs-lookup"><span data-stu-id="016b6-123">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="016b6-124">Veiksmų srityje spustelėkite **Sąskaita faktūra > Sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="016b6-124">On the Action Pane, click **Invoice > Invoice**.</span></span>
2. <span data-ttu-id="016b6-125">Lauke **Numeris** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="016b6-125">In the **Number** field, type a value.</span></span>
3. <span data-ttu-id="016b6-126">Spustelėkite **Numatyt. iš: užsakyto kiekio**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="016b6-126">Click **Default from: Ordered quantity** to open the drop dialog.</span></span>
4. <span data-ttu-id="016b6-127">Lauke **Numatytasis eilučių kiekis** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="016b6-127">In the **Default quantity for lines** field, select an option.</span></span>
5. <span data-ttu-id="016b6-128">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="016b6-128">Click **OK**.</span></span>
6. <span data-ttu-id="016b6-129">Spustelėkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="016b6-129">Click **Yes**.</span></span>
7. <span data-ttu-id="016b6-130">Spustelėkite **Sugretinti produktų gavimo kvitus**.</span><span class="sxs-lookup"><span data-stu-id="016b6-130">Click **Match product receipts**.</span></span>
8. <span data-ttu-id="016b6-131">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="016b6-131">Click **OK**.</span></span>
9. <span data-ttu-id="016b6-132">Veiksmų srityje spustelėkite **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="016b6-132">On the Action Pane, click **Review**.</span></span>
10. <span data-ttu-id="016b6-133">Spustelėkite **Gretinimo informacija**.</span><span class="sxs-lookup"><span data-stu-id="016b6-133">Click **Matching details**.</span></span>

