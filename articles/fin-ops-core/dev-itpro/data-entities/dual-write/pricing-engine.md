---
title: Sinchronizavimas pagal poreikį naudojant „Dynamics 365 Supply Chain Management” kainodaros mechanizmą
description: Šioje temoje aprašoma, kaip naudoti „Dynamics 365 Sales” kainodaros mechanizmą programoje „Microsoft Dynamics 365 Supply Chain Management”.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: ef4465144155130087b078f9f96911df38b62c41
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173182"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a><span data-ttu-id="336d0-103">Sinchronizavimas pagal poreikį naudojant „Dynamics 365 Supply Chain Management” kainodaros mechanizmą</span><span class="sxs-lookup"><span data-stu-id="336d0-103">Sync with the Dynamics 365 Supply Chain Management pricing engine on demand</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="336d0-104">„Microsoft Dynamics 365 Supply Chain Management” apima kainodaros mechanizmą, kuris tvarko prekybos sutartis, kainoraščius, kliento lojalumo programas, akcijas ir nuolaidas.</span><span class="sxs-lookup"><span data-stu-id="336d0-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="336d0-105">Kainodaros mechanizmas naudoja sudėtingas taisykles nustatyti geriausią konkretaus pasiūlymo ar užsakymo kainą.</span><span class="sxs-lookup"><span data-stu-id="336d0-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="336d0-106">Kai naudojate dvigubą rašymą, naudojate statinę kainodarą arba kainodaros mechanizmą iš „Dynamics 365 Supply Chain Management”, esantį programos „Dynamics 365 Sales” pasiūlymo ir užsakymo puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="336d0-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="336d0-107">Kainodaros mechanizmo iš „Supply Chain Management”, esančio „Sales“ programoje, naudojimas</span><span class="sxs-lookup"><span data-stu-id="336d0-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="336d0-108">Programoje „Sales“ eikite į **Pardavimas \>Užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="336d0-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="336d0-109">Norėdami sukurti užsakymą pasirinkite **Naujas** arba sąraše **Mano užsakymai** pasirinkite esamą užsakymą.</span><span class="sxs-lookup"><span data-stu-id="336d0-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="336d0-110">Įtraukite naują užsakymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="336d0-110">Add a new order line.</span></span>
4. <span data-ttu-id="336d0-111">Jei kuriate naują užsakymą, veiksmų srityje pasirinkite **Kainos užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="336d0-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="336d0-112">Jei atnaujinate esamą užsakymą, veiksmų srityje pasirinkite **Perskaičiuoti**.</span><span class="sxs-lookup"><span data-stu-id="336d0-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="336d0-113">Automatiškai užpildomi šie laukai:</span><span class="sxs-lookup"><span data-stu-id="336d0-113">The following fields are automatically filled in:</span></span>

    + <span data-ttu-id="336d0-114">Išsami suma</span><span class="sxs-lookup"><span data-stu-id="336d0-114">Detail Amount</span></span>
    + <span data-ttu-id="336d0-115">Nuolaida %</span><span class="sxs-lookup"><span data-stu-id="336d0-115">Discount %</span></span>
    + <span data-ttu-id="336d0-116">Nuolaida</span><span class="sxs-lookup"><span data-stu-id="336d0-116">Discount</span></span>
    + <span data-ttu-id="336d0-117">Suma be transportavimo mokesčio</span><span class="sxs-lookup"><span data-stu-id="336d0-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="336d0-118">Suma su transportavimo mokesčiu</span><span class="sxs-lookup"><span data-stu-id="336d0-118">Freight Amount</span></span>
    + <span data-ttu-id="336d0-119">Bendra mokesčių suma</span><span class="sxs-lookup"><span data-stu-id="336d0-119">Total Tax</span></span>
    + <span data-ttu-id="336d0-120">Iš viso</span><span class="sxs-lookup"><span data-stu-id="336d0-120">Total Amount</span></span>

## <a name="how-it-works"></a><span data-ttu-id="336d0-121">Kaip tai veikia</span><span class="sxs-lookup"><span data-stu-id="336d0-121">How it works</span></span>

<span data-ttu-id="336d0-122">Kai pasirenkate „Sales“ programoje **Kainos užsakymas**, tada funkcija **Bendrosios sumos**, esanti „Supply Chain Management” skirtuke **Pardavimo užsakymas \> Peržiūrėti**, iškviečiama susietam pardavimo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="336d0-122">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="336d0-123">„Sales“ programoje užsakymo bendrosios sumos reikšmės yra naudojamos užpildyti atitinkamus „Supply Chain Management” laukus.</span><span class="sxs-lookup"><span data-stu-id="336d0-123">The values in the order total in Sales are used to fill in the corresponding fields in Supply Chain Management.</span></span>

<span data-ttu-id="336d0-124">Kai pardavimo užsakymo bendroji suma apskaičiuojama programoje „Supply Chain Management”, skaičiavimu įvertinamos esamos kliento prekybos sutartys ir pardavimo sutartys bei produktai, kurie išvardyti pardavimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="336d0-124">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="336d0-125">Ši informacija naudojama apskaičiuoti bendrąsias sumas.</span><span class="sxs-lookup"><span data-stu-id="336d0-125">This information is used to calculate the totals.</span></span> <span data-ttu-id="336d0-126">Pasirinkus **Kainos užsakymas**, „Sales“ automatiškai rodo visus parametrus, nustatytus programoje „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="336d0-126">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="336d0-127">Apribojimai</span><span class="sxs-lookup"><span data-stu-id="336d0-127">Limitations</span></span>

<span data-ttu-id="336d0-128">Kai užpildyti „Sales“ laukai, taikomi šie apribojimai:</span><span class="sxs-lookup"><span data-stu-id="336d0-128">When the fields in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="336d0-129">„Supply Chain Management” mokesčių ir išlaidų paskirstymo sąranka nėra dubliuojama programoje „Sales“.</span><span class="sxs-lookup"><span data-stu-id="336d0-129">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="336d0-130">Kainodaroje neatsižvelgiama į specialią mažmeninės prekybos kainodarą, nurodytą lauke **Mažmeninės prekybos kanalas**, esančiame „Supply Chain Management” pardavimo užsakymo eilutės puslapyje.</span><span class="sxs-lookup"><span data-stu-id="336d0-130">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** field on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="336d0-131">Neatsižvelgiama į nuolaidas, nurodytas „Supply Chain Management” skyriuje **Prekybos nuolaidų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="336d0-131">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>
