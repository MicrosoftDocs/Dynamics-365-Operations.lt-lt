---
title: Mokėtinų sumų SF ir pagrindinių duomenų auditas
description: Šioje temoje aprašyta, kaip tikrinti mokėtinų sumų SF ir pagrindinius duomenis.
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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e173d2efe0d5acb1be60c9ba315c21563c2bf105
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994770"
---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a><span data-ttu-id="a8ec9-103">Mokėtinų sumų SF ir pagrindinių duomenų auditas</span><span class="sxs-lookup"><span data-stu-id="a8ec9-103">Audit invoices and key data in accounts payable</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a8ec9-104">Gavę sąskaitą faktūrą iš tiekėjo už prekes ir paslaugas, pateiktas pirkimo užsakyme, atsižvelgiant į verslo procesus, gali reikėti, kad prekės ar paslaugos būtų gautos prieš pateikiant sąskaitą faktūrą apmokėti.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="a8ec9-105">Prieš pradėdami įsitikinkite, kad pasirinktas SF gretinimo konfigūracijos raktas.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="a8ec9-106">Puslapyje **Mokėtinų sumų parametrai** įsitikinkite, kad pasirinkta parinktis Įgalinti SF gretinimo tikrinimą, laukas **Registruoti SF su nesutapimais** nustatytas į **Reikalauti patvirtinimo**, o laukas **Eilučių atitikimo strategija** nustatytas į **Tripusis atitikimas**.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-106">In the **Accounts payable parameters** page, ensure that the Enable invoice matching validation option is selected, the **Post invoice with discrepancies** field is set to **Require approval**, and the **Line matching policy** field is set to **Three-way matching**.</span></span>

<span data-ttu-id="a8ec9-107">Šioje procedūroje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="a8ec9-108">Šiuos veiksmus paprastai atlieka mokėtinų sumų vadovo arba apskaitos vadovo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="a8ec9-109">Pirkimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="a8ec9-109">Create a purchase order</span></span>
1. <span data-ttu-id="a8ec9-110">Eikite į **Visi pirkimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-110">Go to **All purchase orders**.</span></span>
2. <span data-ttu-id="a8ec9-111">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-111">Click **New**.</span></span>
3. <span data-ttu-id="a8ec9-112">Lauke **Tiekėjo sąskaita** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-112">In the **Vendor account** field, type a value.</span></span>
4. <span data-ttu-id="a8ec9-113">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-113">Click **OK**.</span></span>
5. <span data-ttu-id="a8ec9-114">Spustelėkite **Pridėti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-114">Click **Add line**.</span></span>
6. <span data-ttu-id="a8ec9-115">Lauke **Prekės numeris** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-115">In the **Item number** field, type a value.</span></span>
7. <span data-ttu-id="a8ec9-116">Veiksmų srityje spustelėkite **Pirkti**.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-116">On the Action Pane, click **Purchase**.</span></span>
8. <span data-ttu-id="a8ec9-117">Spustelėkite **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-117">Click **Confirm**.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="a8ec9-118">Registruoti produkto gavimo kvitą</span><span class="sxs-lookup"><span data-stu-id="a8ec9-118">Post a product receipt</span></span>
1. <span data-ttu-id="a8ec9-119">Veiksmų srityje spustelėkite **Gauti**.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-119">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="a8ec9-120">Spustelėkite **Produkto gavimo kvitas**.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-120">Click **Product receipt**.</span></span>
3. <span data-ttu-id="a8ec9-121">Lauke **Produkto gavimo kvitas** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-121">In the **Product receipt** field, type a value.</span></span>
4. <span data-ttu-id="a8ec9-122">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-122">Click **OK**.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="a8ec9-123">Įrašyti bei gretinti tiekėjo SF ir produkto gavimo kvitą</span><span class="sxs-lookup"><span data-stu-id="a8ec9-123">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="a8ec9-124">Veiksmų srityje spustelėkite **Sąskaita faktūra > Sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-124">On the Action Pane, click **Invoice > Invoice**.</span></span>
2. <span data-ttu-id="a8ec9-125">Lauke **Numeris** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-125">In the **Number** field, type a value.</span></span>
3. <span data-ttu-id="a8ec9-126">Spustelėkite **Numatyt. iš: užsakyto kiekio**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-126">Click **Default from: Ordered quantity** to open the drop dialog.</span></span>
4. <span data-ttu-id="a8ec9-127">Lauke **Numatytasis eilučių kiekis** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-127">In the **Default quantity for lines** field, select an option.</span></span>
5. <span data-ttu-id="a8ec9-128">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-128">Click **OK**.</span></span>
6. <span data-ttu-id="a8ec9-129">Spustelėkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-129">Click **Yes**.</span></span>
7. <span data-ttu-id="a8ec9-130">Spustelėkite **Sugretinti produktų gavimo kvitus**.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-130">Click **Match product receipts**.</span></span>
8. <span data-ttu-id="a8ec9-131">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-131">Click **OK**.</span></span>
9. <span data-ttu-id="a8ec9-132">Veiksmų srityje spustelėkite **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-132">On the Action Pane, click **Review**.</span></span>
10. <span data-ttu-id="a8ec9-133">Spustelėkite **Gretinimo informacija**.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-133">Click **Matching details**.</span></span>

