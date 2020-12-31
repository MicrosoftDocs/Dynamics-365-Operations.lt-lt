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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 740ae20704abd9c59f64c2c7622fa96d65dccb1d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4455451"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a><span data-ttu-id="5c204-103">Sinchronizavimas pagal poreikį naudojant „Dynamics 365 Supply Chain Management” kainodaros mechanizmą</span><span class="sxs-lookup"><span data-stu-id="5c204-103">Sync with the Dynamics 365 Supply Chain Management pricing engine on demand</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="5c204-104">„Microsoft Dynamics 365 Supply Chain Management” apima kainodaros mechanizmą, kuris tvarko prekybos sutartis, kainoraščius, kliento lojalumo programas, akcijas ir nuolaidas.</span><span class="sxs-lookup"><span data-stu-id="5c204-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="5c204-105">Kainodaros mechanizmas naudoja sudėtingas taisykles nustatyti geriausią konkretaus pasiūlymo ar užsakymo kainą.</span><span class="sxs-lookup"><span data-stu-id="5c204-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="5c204-106">Kai naudojate dvigubą rašymą, naudojate statinę kainodarą arba kainodaros mechanizmą iš „Dynamics 365 Supply Chain Management”, esantį programos „Dynamics 365 Sales” pasiūlymo ir užsakymo puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="5c204-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="5c204-107">Kainodaros mechanizmo iš „Supply Chain Management”, esančio „Sales“ programoje, naudojimas</span><span class="sxs-lookup"><span data-stu-id="5c204-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="5c204-108">Programoje „Sales“ eikite į **Pardavimas \>Užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="5c204-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="5c204-109">Norėdami sukurti užsakymą pasirinkite **Naujas** arba sąraše **Mano užsakymai** pasirinkite esamą užsakymą.</span><span class="sxs-lookup"><span data-stu-id="5c204-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="5c204-110">Įtraukite naują užsakymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="5c204-110">Add a new order line.</span></span>
4. <span data-ttu-id="5c204-111">Jei kuriate naują užsakymą, veiksmų srityje pasirinkite **Kainos užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="5c204-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="5c204-112">Jei atnaujinate esamą užsakymą, veiksmų srityje pasirinkite **Perskaičiuoti**.</span><span class="sxs-lookup"><span data-stu-id="5c204-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="5c204-113">Automatiškai užpildomi šie laukai:</span><span class="sxs-lookup"><span data-stu-id="5c204-113">The following fields are automatically filled in:</span></span>

    + <span data-ttu-id="5c204-114">Išsami suma</span><span class="sxs-lookup"><span data-stu-id="5c204-114">Detail Amount</span></span>
    + <span data-ttu-id="5c204-115">Nuolaida %</span><span class="sxs-lookup"><span data-stu-id="5c204-115">Discount %</span></span>
    + <span data-ttu-id="5c204-116">Nuolaida</span><span class="sxs-lookup"><span data-stu-id="5c204-116">Discount</span></span>
    + <span data-ttu-id="5c204-117">Suma be transportavimo mokesčio</span><span class="sxs-lookup"><span data-stu-id="5c204-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="5c204-118">Suma su transportavimo mokesčiu</span><span class="sxs-lookup"><span data-stu-id="5c204-118">Freight Amount</span></span>
    + <span data-ttu-id="5c204-119">Bendra mokesčių suma</span><span class="sxs-lookup"><span data-stu-id="5c204-119">Total Tax</span></span>
    + <span data-ttu-id="5c204-120">Iš viso</span><span class="sxs-lookup"><span data-stu-id="5c204-120">Total Amount</span></span>
    
5. <span data-ttu-id="5c204-121">Norėdami užtikrinti, kad sistema skaičiuodama kainą atsižvelgtų į prekybos ir pardavimo sutartis, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5c204-121">To ensure that the system considers trade and sales agreements to calculate the price:</span></span>
    1. <span data-ttu-id="5c204-122">Pereikite į „Supply Chain Management” aplinką.</span><span class="sxs-lookup"><span data-stu-id="5c204-122">Navigate to your Supply Chain Management environment.</span></span>
    2. <span data-ttu-id="5c204-123">Eikite į **Gautinos sumos \> Nustatymai \> Gautinų sumų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="5c204-123">Navigate to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    3. <span data-ttu-id="5c204-124">Pasirinkite šoninės naršymo juostos skirtuką **Kainos**.</span><span class="sxs-lookup"><span data-stu-id="5c204-124">Select the **Prices** tab in the side navigation bar.</span></span>
    4. <span data-ttu-id="5c204-125">„FastTab“ **Prekybos sutarties vertinimas** atžymėkite parinktį **Įvedimas rankiniu būdu**.</span><span class="sxs-lookup"><span data-stu-id="5c204-125">Under the **Trade agreement evaluation** fastab, uncheck the **Manual entry** option.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="5c204-126">Kaip tai veikia</span><span class="sxs-lookup"><span data-stu-id="5c204-126">How it works</span></span>

<span data-ttu-id="5c204-127">Kai pasirenkate „Sales“ programoje **Kainos užsakymas**, tada funkcija **Bendrosios sumos**, esanti „Supply Chain Management” skirtuke **Pardavimo užsakymas \> Peržiūrėti**, iškviečiama susietam pardavimo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="5c204-127">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="5c204-128">„Sales“ programoje užsakymo bendrosios sumos reikšmės yra naudojamos užpildyti atitinkamus „Supply Chain Management” laukus.</span><span class="sxs-lookup"><span data-stu-id="5c204-128">The values in the order total in Sales are used to fill in the corresponding fields in Supply Chain Management.</span></span>

<span data-ttu-id="5c204-129">Kai pardavimo užsakymo bendroji suma apskaičiuojama programoje „Supply Chain Management”, skaičiavimu įvertinamos esamos kliento prekybos sutartys ir pardavimo sutartys bei produktai, kurie išvardyti pardavimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="5c204-129">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="5c204-130">Ši informacija naudojama apskaičiuoti bendrąsias sumas.</span><span class="sxs-lookup"><span data-stu-id="5c204-130">This information is used to calculate the totals.</span></span> <span data-ttu-id="5c204-131">Pasirinkus **Kainos užsakymas**, „Sales“ automatiškai rodo visus parametrus, nustatytus programoje „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="5c204-131">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="5c204-132">Apribojimai</span><span class="sxs-lookup"><span data-stu-id="5c204-132">Limitations</span></span>

<span data-ttu-id="5c204-133">Kai užpildyti „Sales“ laukai, taikomi šie apribojimai:</span><span class="sxs-lookup"><span data-stu-id="5c204-133">When the fields in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="5c204-134">„Supply Chain Management” mokesčių ir išlaidų paskirstymo sąranka nėra dubliuojama programoje „Sales“.</span><span class="sxs-lookup"><span data-stu-id="5c204-134">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="5c204-135">Kainodaroje neatsižvelgiama į specialią mažmeninės prekybos kainodarą, nurodytą lauke **Mažmeninės prekybos kanalas**, esančiame „Supply Chain Management” pardavimo užsakymo eilutės puslapyje.</span><span class="sxs-lookup"><span data-stu-id="5c204-135">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** field on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="5c204-136">Neatsižvelgiama į nuolaidas, nurodytas „Supply Chain Management” skyriuje **Prekybos nuolaidų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="5c204-136">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>
