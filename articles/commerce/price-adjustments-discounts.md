---
title: Kainų koregavimas ir nuolaidos
description: Šiame straipsnyje pateikiama informacija apie kainų koregavimus ir nuolaidas „Dynamics 365 Commerce“.
author: scott-tucker
ms.date: 06/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 44c03ae0a04d648e788a72d8f6dcc3671c5736c7
ms.sourcegitcommit: 7c9d6be464db058511df9cb6ba162d21dc0554e8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/11/2021
ms.locfileid: "6240947"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="59a69-103">Kainų koregavimas ir nuolaidos</span><span class="sxs-lookup"><span data-stu-id="59a69-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="59a69-104">Šiame straipsnyje pateikiama informacija apie kainų koregavimus ir nuolaidas „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="59a69-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="59a69-105">„Commerce“ galite koreguoti produktų kainą, taip pat galite nustatyti nuolaidas, taikomas eilutės elementui arba operacijai elektroniniame kasos aparate (EKA), skambučių centro pardavimo užsakyme arba užsakyme internetu.</span><span class="sxs-lookup"><span data-stu-id="59a69-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="59a69-106">Tiek kainų korekcijas, tiek nuolaidas galima susieti su kainų grupėmis.</span><span class="sxs-lookup"><span data-stu-id="59a69-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="59a69-107">Kainų koregavimams ir nuolaidoms galite nurodyti vieną pradžios datą ir pabaigos datą arba pasikartojimo laikotarpį, nuolaidos kodą ir keletą papildomų atributų.</span><span class="sxs-lookup"><span data-stu-id="59a69-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="59a69-108">Kainų koregavimą ir nuolaidos galima taikyti produktams, variantams arba kategorijoms.</span><span class="sxs-lookup"><span data-stu-id="59a69-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="59a69-109">Jei produktui taikoma daugiau nei viena nuolaida, klientas gali gauti vieną iš nuolaidų arba jungtinę nuolaidą, atsižvelgiant į nuolaidos konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="59a69-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="59a69-110">„Commerce“ automatiškai taiko nuolaidą ar nuolaidų derinį, kuris klientui pasiūlo geriausią kainą.</span><span class="sxs-lookup"><span data-stu-id="59a69-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="59a69-111">Nustatydami kainos koregavimą arba nuolaidą įsitikinkite, kad kainų grupės priskiriamos tinkamiems kanalams, katalogams, priskyrimams arba lojalumo programoms, kurioms norite taikyti nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="59a69-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="59a69-112">Be to, jei norite automatiškai sugeneruoti nuolaidos ID, prieš nustatant naują kainą ar nuolaidą, puslapyje **„Commerce“ parametrai** nustatykite skaičių sekas.</span><span class="sxs-lookup"><span data-stu-id="59a69-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="59a69-113">Kainos koregavimą arba nuolaidą galima panaikinti.</span><span class="sxs-lookup"><span data-stu-id="59a69-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="59a69-114">Tačiau bus prarasta statistinė informacija.</span><span class="sxs-lookup"><span data-stu-id="59a69-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="59a69-115">Nuolaidų tipai</span><span class="sxs-lookup"><span data-stu-id="59a69-115">Types of discounts</span></span>

<span data-ttu-id="59a69-116">Yra daug tipų nuolaidų:</span><span class="sxs-lookup"><span data-stu-id="59a69-116">There are many types of discounts:</span></span>

- <span data-ttu-id="59a69-117">**Paprasta nuolaida** – vienas procentinis dydis arba suma.</span><span class="sxs-lookup"><span data-stu-id="59a69-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="59a69-118">**Kiekio nuolaida** – nuolaida, taikoma perkant du ar daugiau produktų.</span><span class="sxs-lookup"><span data-stu-id="59a69-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="59a69-119">**Nuolaida prekių rinkiniui** – nuolaida, suteikiama perkant tam tikrą produktų derinį.</span><span class="sxs-lookup"><span data-stu-id="59a69-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="59a69-120">**Ribinė nuolaida** – nuolaida, taikoma, kai operacijos bendroji suma yra didesnė nei nurodyta suma.</span><span class="sxs-lookup"><span data-stu-id="59a69-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="59a69-121">**Nuomotoju pagrįsta nuolaida** – Nuolaida, kuri yra taikoma, kai perlaidos bendra suma yra didesnė nei nurodyta suma ir konkretus apmokėjimo tipas (pavyzdžiui, grynieji, kredito ar debeto kortelė) naudojama apmokėjimui.</span><span class="sxs-lookup"><span data-stu-id="59a69-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="59a69-122">**Siuntimo nuolaida** – Nuolaida, kuri yra taikoma, kai perlaidos bendra suma yra didesnė nei nurodyta suma ir konkretus pristatymo būdas (pavyzdžiui, dviejų dienų siuntimas ar siuntimas per naktį) naudojamas užsakyme.</span><span class="sxs-lookup"><span data-stu-id="59a69-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="59a69-123">Tiek kainų korekcijas, tiek nuolaidas galima susieti su kainų grupėmis.</span><span class="sxs-lookup"><span data-stu-id="59a69-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="59a69-124">Kainų grupės gali būti susietos su kanalais, katalogais, priskyrimais ir lojalumo programomis.</span><span class="sxs-lookup"><span data-stu-id="59a69-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>

> [!NOTE]
> <span data-ttu-id="59a69-125">Nuolaidos prekių nuolaidai ir ribinei vertei taikomos ypatybės, kurių pavadinimai Skaičiuoti produktus, kuriems nuolaida nėra taikoma" ir „Skaičiuoti produktus, kuriems nuolaida nėra taikoma, kaip ribinė reikšmė".</span><span class="sxs-lookup"><span data-stu-id="59a69-125">The mix and match discount and the threshold discount have properties named "Count non-discountable products" and "Count non-discountable products towards threshold", respectively.</span></span> <span data-ttu-id="59a69-126">Jei šios ypatybės įgalintos, prekė, kuri neturi teisės į jokias nuolaidas, vis tiek gali padėti nustatyti nuolaidos operaciją, bet netinkama prekė negaus nuolaidos.</span><span class="sxs-lookup"><span data-stu-id="59a69-126">If these properties are enabled, an item that is not eligible for any discount can still help qualify a transaction for the discount, but the ineligible item will not get the discount.</span></span> 
> 
> <span data-ttu-id="59a69-127">Pavyzdžiui, jei sukuriate nuolaidą prekių maišai su dviem eilutėmis A ir B, kur klientui 10% nuolaida turi būti atjungta, o A prekės konfigūracija pažymėta Kaip Neleisti visų nuolaidų, tai paprastai reiškia, kad A prekė neįtraukiama į nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="59a69-127">For example, if you create a mix and match discount with two lines, A and B, where a customer should get 10% off on both items, but item A has the configuration "Prevent all discounts" checked, then this would typically stop item A from being included in the discount.</span></span> <span data-ttu-id="59a69-128">Tačiau, jei įgalinta ypatybė Skaičiuoti produktus, kuriems netaikoma nuolaida, prekę A galima naudoti norint pritaikyti nuolaidą prekių prekių nuolaidai, tačiau 10% nuolaida bus taikoma tik prekei B. Panaši logika taikoma ribinei nuolaidai.</span><span class="sxs-lookup"><span data-stu-id="59a69-128">However, if the "Count non-discountable products" property is enabled, then item A can be used to qualify for the mix and match discount, but the 10% discount will only be applied to item B. Similar logic applies to the threshold discount.</span></span> 
>
> <span data-ttu-id="59a69-129">Tačiau ypatybė „Skaičiuoti produktus, kuriems taikoma nuolaida siekiant slenkstį“, turi papildomą galimybę, kai ji lyginama su nuolaidų prekių nuolaidai taikoma ypatybė Skaičiuoti produktus, kuriems nuolaida nėra taikoma.</span><span class="sxs-lookup"><span data-stu-id="59a69-129">However, the property "Count non-discountable products towards threshold" has an additional capability when compared to the "Count non-discountable products" property of the mix and match discounts.</span></span> <span data-ttu-id="59a69-130">Jei įgalinta ribinė nuolaida ir jei yra prekė, kuriai taikoma esama nuolaida, kuri apsaugotų nuo bet kokių kitų nuolaidų, už šią prekę sumokėta kaina atitiktų ribinę vertę, tačiau ši prekė negaus papildomos nuolaidos.</span><span class="sxs-lookup"><span data-stu-id="59a69-130">If the threshold discount is enabled, and if there is an item that has an existing discount which would prevent the item from any other discounts, then  the price paid for this item would qualify towards meeting the threshold, but this item will not get the additional discount.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
