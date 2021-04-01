---
title: Konfigūruoti pardavimo mokesčius interneto užsakymams
description: Šioje temoje pateikta pardavimo mokesčių grupės parinkimo skirtingiems interneto užsakymų tipams apžvalga „Dynamics 365 Commerce“.
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 36dd3e8a3d47f02eed5b9c8bb79d773d98069376
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254846"
---
# <a name="configure-sales-tax-for-online-orders"></a><span data-ttu-id="f172e-103">Konfigūruoti pardavimo mokesčius interneto užsakymams</span><span class="sxs-lookup"><span data-stu-id="f172e-103">Configure sales tax for online orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f172e-104">Šioje temoje pateikta pardavimo mokesčių grupės parinkimo skirtingiems interneto užsakymų tipams apžvalga.</span><span class="sxs-lookup"><span data-stu-id="f172e-104">This topic provides an overview of sales tax group selection for different online order types.</span></span> 

<span data-ttu-id="f172e-105">Jūsų e-komercijos kanalas gali palaikyti parinktis tokias kaip interneto užsakymų pristatymas ar paėmimas.</span><span class="sxs-lookup"><span data-stu-id="f172e-105">Your e-commerce channel may want to support options like delivery or pickup for online orders.</span></span> <span data-ttu-id="f172e-106">Pardavimo mokesčių taikymas yra paremtas parinktimi, kurią pasirinko jūsų interneto vartotojai.</span><span class="sxs-lookup"><span data-stu-id="f172e-106">The sales tax applicability is based on the option selected by your online users.</span></span> <span data-ttu-id="f172e-107">Kai saito klientas pasirenka įsigyti prekę internetu ir gauna ją atsiųstą pasirinktu adresu, pardavimo mokesčiai yra nustatomi pagal siuntėjo siuntimo adreso mokesčių grupės nustatymus.</span><span class="sxs-lookup"><span data-stu-id="f172e-107">When a site customer chooses to buy an item online and gets it shipped to an address, the sales tax is determined based on the customer's shipping address tax group setting.</span></span> <span data-ttu-id="f172e-108">Kai klientas pasirenka atsiimti įsigytą prekę iš parduotuvės, pardavimo mokesčiai yra nustatomi pagal paėmimo parduotuvės mokesčių grupės nustatymą.</span><span class="sxs-lookup"><span data-stu-id="f172e-108">When a customer opts to pick up a purchased item at a store, the sales tax is determined based on the pickup store's tax group setting.</span></span> 

## <a name="orders-shipped-to-a-customer-address"></a><span data-ttu-id="f172e-109">Užsakymai siųsti kliento adresu</span><span class="sxs-lookup"><span data-stu-id="f172e-109">Orders shipped to a customer address</span></span> 

<span data-ttu-id="f172e-110">Bendrai, mokesčiai interneto užsakymams, kurie siunčiami kliento adresu yra nustatyti pagal paskirties vietą.</span><span class="sxs-lookup"><span data-stu-id="f172e-110">In general, taxes for online orders that ship to customer addresses are defined by the destination.</span></span> <span data-ttu-id="f172e-111">Visos pardavimo mokesčių grupės turi mažmenos paskirties mokesčių tikslais konfigūravimą, kuriame jūsų verslas gali nustatyti paskirties vietos išsamią informaciją, tokią kaip šalis/regionas, valstija, valstybė ir miestas hierarchine tvarka.</span><span class="sxs-lookup"><span data-stu-id="f172e-111">Every sales tax group has a retail destination-based tax configuration in which your business can define destination details such as county/region, state, county, and city in a hierarchical form.</span></span> <span data-ttu-id="f172e-112">Padarius interneto užsakymą, „Commerce“ mokesčių variklis naudoja kiekvienos eilutės prekės užsakyme pristatymo adresą ir suranda pardavimo mokesčių grupes su atitinkančiais paskirties vietos pagrįstais mokesčių kriterijais.</span><span class="sxs-lookup"><span data-stu-id="f172e-112">When an online order is placed, the Commerce tax engine uses the delivery address of every line item in the order, and finds sales tax groups with matching destination-based tax criteria.</span></span> <span data-ttu-id="f172e-113">Pavyzdžiui, interneto užsakymui su eilutės prekės pristatymo adresu į San Franciską, Kaliforniją, mokesčių variklis suras pardavimo mokesčių grupę ir kodą Kalifornijai ir tada apskaičiuos mokesčiu kiekvienai eilutės prekei atitinkamai.</span><span class="sxs-lookup"><span data-stu-id="f172e-113">For example, for an online order with a line item delivery address to San Francisco, California, the tax engine will find the sales tax group and sales tax code for California and then calculate tax for each line item accordingly.</span></span>  

## <a name="customer-based-tax-groups"></a><span data-ttu-id="f172e-114">Klientu pagrįsta mokesčių grupė</span><span class="sxs-lookup"><span data-stu-id="f172e-114">Customer-based tax groups</span></span>

<span data-ttu-id="f172e-115">„Commerce“ štabe, esama dviejų vietų, kuriose kliento mokesčio grupės yra sukonfigūruotos:</span><span class="sxs-lookup"><span data-stu-id="f172e-115">In Commerce headquarters, there are two places where customer tax groups are configured:</span></span>

- <span data-ttu-id="f172e-116">**Kliento profilis**</span><span class="sxs-lookup"><span data-stu-id="f172e-116">**Customer's profile**</span></span>
- <span data-ttu-id="f172e-117">**Kliento siuntimo adresas**</span><span class="sxs-lookup"><span data-stu-id="f172e-117">**Customer's shipping address**</span></span>

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a><span data-ttu-id="f172e-118">Jei kliento profilis turi sukonfigūruotą mokesčių grupę</span><span class="sxs-lookup"><span data-stu-id="f172e-118">If a customer's profile has a tax group configured</span></span>

<span data-ttu-id="f172e-119">Kliento profilio įrašas štabe gali turėti sukonfigūruotą pardavimo mokesčių grupę, nepaisant to interneto užsakymams pardavimo mokesčių grupė sukonfigūruota kliento profilyje nebus naudojama mokesčių variklio.</span><span class="sxs-lookup"><span data-stu-id="f172e-119">A customer's profile record in headquarters may have a sales tax group configured, however for online orders the sales tax group configured in a customer's profile will not be used by the tax engine.</span></span> 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a><span data-ttu-id="f172e-120">Jei kliento siuntimo adresas turi sukonfigūruotą mokesčių grupę</span><span class="sxs-lookup"><span data-stu-id="f172e-120">If a customer's shipping address has a tax group configured</span></span>

<span data-ttu-id="f172e-121">Jei kliento siuntimo adreso įrašas turi kitą sukonfigūruotą mokesčių grupę ir interneto užsakymą (ar eilutės prekę) siunčiamą kliento siuntimo adresu, sukonfigūruota mokesčių grupė kliento adreso įraše bus naudojama mokesčių variklio mokesčių apskaičiavimui.</span><span class="sxs-lookup"><span data-stu-id="f172e-121">If a customer's shipping address record has a tax group configured and an online order (or line item) is shipped to the customer's shipping address, the tax group configured in the customer's address record will be used by the tax engine for tax calculations.</span></span>

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a><span data-ttu-id="f172e-122">Konfigūruoti mokesčių grupę kliento siuntimo adreso įrašui</span><span class="sxs-lookup"><span data-stu-id="f172e-122">Configure a tax group for a customer's shipping address record</span></span>

<span data-ttu-id="f172e-123">Norėdami Konfigūruoti mokesčių grupę kliento siuntimo adreso įrašui „Commerce“ štabe, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="f172e-123">To configure a tax group for a customer's shipping address record in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f172e-124">Eikite į **Visi klientai** ir tada rinkitės norimą klientą.</span><span class="sxs-lookup"><span data-stu-id="f172e-124">Go to **All customers**, and then select the desired customer.</span></span> 
1. <span data-ttu-id="f172e-125">„FastTab“ **Adresa** pasirinkite norimą adresą ir tada rinkitės **Daugiau parinkčių \> Papildomos**.</span><span class="sxs-lookup"><span data-stu-id="f172e-125">On the **Addresses** FastTab, select the desired address, and then select **More options \> Advanced**.</span></span> 
1. <span data-ttu-id="f172e-126">Skirtuke **Bendri** puslapyje **Valdyti adresus**, nustatykite pardavimo mokesčių vertę, kaip būtina.</span><span class="sxs-lookup"><span data-stu-id="f172e-126">Under the **General** tab on the **Manage addresses** page, set the sales tax value as needed.</span></span>

> [!NOTE]
> <span data-ttu-id="f172e-127">Mokesčių grupė yra nustatoma naudojant užsakymo eilutės pristatymo adresą ir paskirties vieta pagrįstus mokesčius, kurie sukonfigūruojami pačioje mokesčių grupėje.</span><span class="sxs-lookup"><span data-stu-id="f172e-127">The tax group is defined using the delivery address of the order line and the destination-based taxes are configured at the tax group itself.</span></span> <span data-ttu-id="f172e-128">Dėl išsamesnės informacijos, žr. [Nustatyti mokesčius interneto parduotuvėms pagrįstoms paskirties vietoms](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="f172e-128">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="order-pickup-in-store"></a><span data-ttu-id="f172e-129">Užsakymo atsiėmimas parduotuvėje</span><span class="sxs-lookup"><span data-stu-id="f172e-129">Order pickup in store</span></span>

<span data-ttu-id="f172e-130">Užsakymo eilutėms su atsiėmimu parduotuvėje ar per langelį, bus taikoma mokesčių grupė iš pasirinktos atsiėmimo parduotuvės.</span><span class="sxs-lookup"><span data-stu-id="f172e-130">For order lines with pickup in store or curbside pickup specified, the tax group from the selected pickup store will be applied.</span></span> <span data-ttu-id="f172e-131">Dėl informacijos apie tai, kaip konfigūruoti mokesčių grupę parinktai parduotuvei, žr. [Nustatyti kitas mokesčių parinktis parduotuvėms](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="f172e-131">For details about how to configure the tax group for a given store, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

> [!NOTE]
> <span data-ttu-id="f172e-132">Kai užsakymo eilutė yra atsiimama parduotuvėje, kliento adreso mokesčių nustatymai (jei nustatyti) bus ignoruojami mokesčių variklio ir bus taikomi atsiėmimo parduotuvėje mokesčiai.</span><span class="sxs-lookup"><span data-stu-id="f172e-132">When an order line is picked up at a store, a customer's address tax settings (if set up) will be ignored by the tax engine and the pickup store's tax configuration will be applied.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="f172e-133">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f172e-133">Additional resources</span></span>

[<span data-ttu-id="f172e-134">PVM apžvalga</span><span class="sxs-lookup"><span data-stu-id="f172e-134">Sales tax overview</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="f172e-135">PVM skaičiavimo metodai lauke Kilmė</span><span class="sxs-lookup"><span data-stu-id="f172e-135">Sales tax calculation methods in the Origin field</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="f172e-136"> PVM priskyrimas ir perrašymai​</span><span class="sxs-lookup"><span data-stu-id="f172e-136">Sales tax assignment and overrides</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="f172e-137">PVM kodų skaičiavimo parinktys Visa suma ir Intervalas</span><span class="sxs-lookup"><span data-stu-id="f172e-137">Whole amount and Interval calculation options for sales tax codes</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="f172e-138">Atleidimo nuo mokesčių skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="f172e-138">Calculation of tax exemption</span></span>](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]