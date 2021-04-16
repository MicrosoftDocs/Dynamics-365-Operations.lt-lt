---
title: Neteisingai apskaičiuoti internetinių užsakymų mokesčiai
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, galinčios padėti, kai netinkamai apskaičiuojami internetinių užsakymų mokesčiai arba kai pardavimo eilutės mokesčių grupė nustatyta neteisingai.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7f71add679e1d24f80db8ce3990058b591128ec1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801416"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a><span data-ttu-id="f50e4-103">Neteisingai apskaičiuoti internetinių užsakymų mokesčiai</span><span class="sxs-lookup"><span data-stu-id="f50e4-103">Taxes on online orders are incorrectly calculated</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f50e4-104">Šioje temoje pateikiamos trikčių diagnostikos priemonės, galinčios padėti, kai netinkamai apskaičiuojami internetinių užsakymų mokesčiai arba kai pardavimo eilutės mokesčių grupė nustatyta neteisingai.</span><span class="sxs-lookup"><span data-stu-id="f50e4-104">This topic provides troubleshooting guidance that can help when taxes on online orders are incorrectly calculated, or when the tax group on the sales line isn't correctly set.</span></span>

## <a name="description"></a><span data-ttu-id="f50e4-105">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="f50e4-105">Description</span></span>

<span data-ttu-id="f50e4-106">Kai pateikiamas el. prekybos užsakymas, mokesčiai apskaičiuojami neteisingai arba netinkamai nustatoma pardavimo eilutės mokesčių grupė.</span><span class="sxs-lookup"><span data-stu-id="f50e4-106">When an e-commerce order is placed, the taxes are incorrectly calculated, or the tax group on the sales line is incorrectly set.</span></span>

## <a name="resolution"></a><span data-ttu-id="f50e4-107">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="f50e4-107">Resolution</span></span>

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a><span data-ttu-id="f50e4-108">Konfigūruoti mažmeninės prekybos parduotuvės PVM „Commerce Headquarters“</span><span class="sxs-lookup"><span data-stu-id="f50e4-108">Configure the sales tax for a retail store in Commerce headquarters</span></span>

<span data-ttu-id="f50e4-109">Norėdami konfigūruoti mažmeninės prekybos parduotuvės PVM „Commerce Headquarters“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f50e4-109">To configure the sales tax for a retail store in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f50e4-110">Eikite į **„Retail” ir „Commerce” \> Kanalai \> Visos parduotuvės**.</span><span class="sxs-lookup"><span data-stu-id="f50e4-110">Go to **Retail and Commerce \> Channels \> All stores**.</span></span>
1. <span data-ttu-id="f50e4-111">Pasirinkite parduotuvę, kurios PVM bus konfigūruojamas.</span><span class="sxs-lookup"><span data-stu-id="f50e4-111">Select the store to configure sales tax for.</span></span>
1. <span data-ttu-id="f50e4-112">„FastTab” **Bendra** skyriuje **PVM** sukonfigūruokite parduotuvės PVM informaciją.</span><span class="sxs-lookup"><span data-stu-id="f50e4-112">On the **General** FastTab, in the **Sales tax** section, configure the sales tax information for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="f50e4-113">Jei produktai paimami iš parduotuvės, mokesčių grupė gaunama iš parduotuvės, iš kurios pasirinkta paimti.</span><span class="sxs-lookup"><span data-stu-id="f50e4-113">For product pickup from a store, the tax group comes from the store that is selected for pickup.</span></span> <span data-ttu-id="f50e4-114">Daugiau informacijos žr. [Kitų mokesčių pasirinkčių nustatymas parduotuvėms](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="f50e4-114">For more information, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a><span data-ttu-id="f50e4-115">Kliento adreso PVM konfigūravimas „Commerce Headquarters“</span><span class="sxs-lookup"><span data-stu-id="f50e4-115">Configure the sales tax for a customer's address in Commerce headquarters</span></span>

<span data-ttu-id="f50e4-116">Norėdami konfigūruoti kliento adreso PVM „Commerce Headquarters“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f50e4-116">To configure the sales tax for a customer's address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f50e4-117">Eikite į **Gautinos sumos \> Klientai \> Visi klientai**.</span><span class="sxs-lookup"><span data-stu-id="f50e4-117">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="f50e4-118">Pasirinkite klientą, kurio PVM bus konfigūruojamas.</span><span class="sxs-lookup"><span data-stu-id="f50e4-118">Select the customer to configure sales taxes for.</span></span>
1. <span data-ttu-id="f50e4-119">„FastTab” **Adresai** pasirinkite adresą, kurio PVM norite konfigūruoti, pasirinkite **Daugiau parinkčių**, tada pasirinkite **Išplėstinės**.</span><span class="sxs-lookup"><span data-stu-id="f50e4-119">On the **Addresses** FastTab, select the address to configure sales taxes for, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="f50e4-120">„FastTab“ **Bendra** pasirinkite **Mokesčių grupė**.</span><span class="sxs-lookup"><span data-stu-id="f50e4-120">On the **General** FastTab, select the **Tax group**.</span></span>
1. <span data-ttu-id="f50e4-121">Lauke **PVM** pasirinkite tinkamą vertę.</span><span class="sxs-lookup"><span data-stu-id="f50e4-121">In the **Sales tax** field, select the appropriate value.</span></span>

> [!NOTE]
> <span data-ttu-id="f50e4-122">Siuntimo, kuriam taikomas kliento adreso PVM, eilutės pristatymo adresas nurodo eilutės mokesčių grupę.</span><span class="sxs-lookup"><span data-stu-id="f50e4-122">For shipping that involves sales tax on the customer's address, the delivery address of the line determines the tax group for the line.</span></span> <span data-ttu-id="f50e4-123">Jei klientas siunčia į esamą adresą, kurio mokesčių grupė jau yra sukonfigūruota, bus naudojama esama mokesčių grupė.</span><span class="sxs-lookup"><span data-stu-id="f50e4-123">If the customer is shipping to an existing address that has a tax group that is already configured, the existing tax group will be used.</span></span> <span data-ttu-id="f50e4-124">Pagal numatytuosius nustatymus, kai adresai kuriami, jie neturi mokesčių grupės.</span><span class="sxs-lookup"><span data-stu-id="f50e4-124">By default, addresses don't have a tax group when they are created.</span></span>

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a><span data-ttu-id="f50e4-125">Bendrųjų PVM grupių konfigūravimas „Commerce Headquarters”</span><span class="sxs-lookup"><span data-stu-id="f50e4-125">Configure general sales tax groups in Commerce headquarters</span></span>

<span data-ttu-id="f50e4-126">Norėdami konfigūruoti bendrąsias PVM grupes „Commerce Headquarters“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f50e4-126">To configure general sales tax groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f50e4-127">Eikite į **Mokestis \> Netiesioginiai mokesčiai \> PVM \> PVM grupė**.</span><span class="sxs-lookup"><span data-stu-id="f50e4-127">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax group**.</span></span>
1. <span data-ttu-id="f50e4-128">Kairiojoje naršymo srityje pasirinkite mokesčių grupę, kurią norite konfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="f50e4-128">In the left navigation, select the tax group to configure.</span></span>
1. <span data-ttu-id="f50e4-129">„FastTab” **Mažmeninės prekybos paskirties vietos mokestis** sukonfigūruokite PVM grupės mokesčius.</span><span class="sxs-lookup"><span data-stu-id="f50e4-129">On the **Retail destination based tax** FastTab, configure the taxes for the sales tax group.</span></span>

> [!NOTE]
> <span data-ttu-id="f50e4-130">Siuntimo, kai nėra kliento adreso PVM, mokesčių grupę nustato eilutės pristatymo adresas ir paskirties vietos mokesčiai, sukonfigūruoti mokesčių grupei.</span><span class="sxs-lookup"><span data-stu-id="f50e4-130">For shipping that doesn't involve sales tax on the customer's address, the delivery address of the line and the destination-based taxes that are configured for the tax group determine the tax group.</span></span> <span data-ttu-id="f50e4-131">Dėl išsamesnės informacijos, žr. [Nustatyti mokesčius interneto parduotuvėms pagrįstoms paskirties vietoms](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="f50e4-131">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f50e4-132">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f50e4-132">Additional resources</span></span>

[<span data-ttu-id="f50e4-133">Internetinių užsakymų PVM konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="f50e4-133">Configure sales tax for online orders</span></span>](../sales-tax-config.md)
