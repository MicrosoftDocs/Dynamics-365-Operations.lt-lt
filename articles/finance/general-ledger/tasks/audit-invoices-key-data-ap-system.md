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
ms.openlocfilehash: c6e8967fe4db67ff98fc7093792bdb82b73a33d9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178977"
---
# <a name="audit-invoices-and-key-data-in-ap-system"></a><span data-ttu-id="34513-103">Audituoti SF ir pagrindinius duomenis AP sistemoje</span><span class="sxs-lookup"><span data-stu-id="34513-103">Audit invoices and key data in AP system</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="34513-104">Gavę sąskaitą faktūrą iš tiekėjo už prekes ir paslaugas, pateiktas pirkimo užsakyme, atsižvelgiant į verslo procesus, gali reikėti, kad prekės ar paslaugos būtų gautos prieš pateikiant sąskaitą faktūrą apmokėti.</span><span class="sxs-lookup"><span data-stu-id="34513-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="34513-105">Prieš pradėdami įsitikinkite, kad pasirinktas SF gretinimo konfigūracijos raktas.</span><span class="sxs-lookup"><span data-stu-id="34513-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="34513-106">Puslapyje Mokėtinų sumų parametrai įsitikinkite, kad pasirinkta parinktis Įgalinti SF gretinimo tikrinimą, laukas Registruoti SF su nesutapimais nustatytas į Reikalauti patvirtinimo, o laukas Eilučių atitikimo strategija nustatytas į Tripusis atitikimas.</span><span class="sxs-lookup"><span data-stu-id="34513-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="34513-107">Šioje procedūroje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="34513-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="34513-108">Šiuos veiksmus paprastai atlieka mokėtinų sumų vadovo arba apskaitos vadovo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="34513-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="34513-109">Pirkimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="34513-109">Create a purchase order</span></span>
1. <span data-ttu-id="34513-110">Eikite į **Visi pirkimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="34513-110">Go to **All purchase orders**.</span></span>
2. <span data-ttu-id="34513-111">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="34513-111">Click **New**.</span></span>
3. <span data-ttu-id="34513-112">Lauke **Tiekėjo sąskaita** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="34513-112">In the **Vendor account** field, type a value.</span></span>
4. <span data-ttu-id="34513-113">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="34513-113">Click **OK**.</span></span>
5. <span data-ttu-id="34513-114">Spustelėkite **Pridėti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="34513-114">Click **Add line**.</span></span>
6. <span data-ttu-id="34513-115">Lauke **Prekės numeris** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="34513-115">In the **Item number** field, type a value.</span></span>
7. <span data-ttu-id="34513-116">Veiksmų srityje spustelėkite **Pirkti**.</span><span class="sxs-lookup"><span data-stu-id="34513-116">On the Action Pane, click **Purchase**.</span></span>
8. <span data-ttu-id="34513-117">Spustelėkite **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="34513-117">Click **Confirm**.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="34513-118">Registruoti produkto gavimo kvitą</span><span class="sxs-lookup"><span data-stu-id="34513-118">Post a product receipt</span></span>
1. <span data-ttu-id="34513-119">Veiksmų srityje spustelėkite **Gauti**.</span><span class="sxs-lookup"><span data-stu-id="34513-119">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="34513-120">Spustelėkite **Produkto gavimo kvitas**.</span><span class="sxs-lookup"><span data-stu-id="34513-120">Click **Product receipt**.</span></span>
3. <span data-ttu-id="34513-121">Lauke **Produkto gavimo kvitas** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="34513-121">In the **Product receipt** field, type a value.</span></span>
4. <span data-ttu-id="34513-122">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="34513-122">Click **OK**.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="34513-123">Įrašyti bei gretinti tiekėjo SF ir produkto gavimo kvitą</span><span class="sxs-lookup"><span data-stu-id="34513-123">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="34513-124">Veiksmų srityje spustelėkite **Sąskaita faktūra > Sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="34513-124">On the Action Pane, click **Invoice > Invoice**.</span></span>
2. <span data-ttu-id="34513-125">Lauke **Numeris** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="34513-125">In the **Number** field, type a value.</span></span>
3. <span data-ttu-id="34513-126">Spustelėkite **Numatyt. iš: užsakyto kiekio**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="34513-126">Click **Default from: Ordered quantity** to open the drop dialog.</span></span>
4. <span data-ttu-id="34513-127">Lauke **Numatytasis eilučių kiekis** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="34513-127">In the **Default quantity for lines** field, select an option.</span></span>
5. <span data-ttu-id="34513-128">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="34513-128">Click **OK**.</span></span>
6. <span data-ttu-id="34513-129">Spustelėkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="34513-129">Click **Yes**.</span></span>
7. <span data-ttu-id="34513-130">Spustelėkite **Sugretinti produktų gavimo kvitus**.</span><span class="sxs-lookup"><span data-stu-id="34513-130">Click **Match product receipts**.</span></span>
8. <span data-ttu-id="34513-131">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="34513-131">Click **OK**.</span></span>
9. <span data-ttu-id="34513-132">Veiksmų srityje spustelėkite **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="34513-132">On the Action Pane, click **Review**.</span></span>
10. <span data-ttu-id="34513-133">Spustelėkite **Gretinimo informacija**.</span><span class="sxs-lookup"><span data-stu-id="34513-133">Click **Matching details**.</span></span>

