---
title: Nepasirodo parinktis Įrašyti kitam mokėjimui
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai el. prekybos svetainės pirkimo užbaigimo puslapio lauke Mokėjimo būdas neatsiranda žymės lankelis Įrašyti kitam mokėjimui.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: af19a3abd78d543d82f7a8d017e2dc413115a6d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018439"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a><span data-ttu-id="1a943-103">Nepasirodo parinktis „Įrašyti kitam mokėjimui”</span><span class="sxs-lookup"><span data-stu-id="1a943-103">"Save for my next payment" option doesn't appear</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1a943-104">Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai el. prekybos svetainės pirkimo užbaigimo puslapio lauke **Mokėjimo būdas** neatsiranda žymės lankelis **Įrašyti kitam mokėjimui**.</span><span class="sxs-lookup"><span data-stu-id="1a943-104">This topic provides troubleshooting guidance that can help when the **Save for my next payment** check box doesn't appear under **Payment method** on an e-commerce site's checkout page.</span></span>

## <a name="description"></a><span data-ttu-id="1a943-105">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="1a943-105">Description</span></span>

<span data-ttu-id="1a943-106">Žymės langelis **Įrašyti kitam mokėjimui** nerodomas el. prekybos svetainės pirkimo užbaigimo puslapio sekcijoje **Mokėjimo būdas**.</span><span class="sxs-lookup"><span data-stu-id="1a943-106">The **Save for my next payment** check box doesn't appear in the **Payment method** section on an e-commerce site's checkout page.</span></span>

<span data-ttu-id="1a943-107">Šioje iliustracijoje pateikiamas pirkimo užbaigimo puslapio, kuriame yra žymės langelis **Įrašyti kitam mokėjimui**, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="1a943-107">The following illustration shows an example of a checkout page that includes the **Save for my next payment** check box.</span></span>

![Žymės langelis „Įrašyti kitam mokėjimui” mokėjimo modulyje](media/payment-module-save-payment.jpg)

## <a name="resolution"></a><span data-ttu-id="1a943-109">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="1a943-109">Resolution</span></span>

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a><span data-ttu-id="1a943-110">Patikrinkite, ar „Dynamics 365 Payment Connector“, skirta „Adyen“, tinkamai sukonfigūruota „Commerce Headquarters”</span><span class="sxs-lookup"><span data-stu-id="1a943-110">Verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters</span></span>

<span data-ttu-id="1a943-111">Norėdami patikrinti, ar „Dynamics 365 Payment Connector“, skirta „Adyen“, tinkamai sukonfigūruota „Commerce Headquarters”, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1a943-111">To verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="1a943-112">Eikite į **„Retail” ir „Commerce” \> Kanalai \> Interneto parduotuvės**.</span><span class="sxs-lookup"><span data-stu-id="1a943-112">Go to **Retail and Commerce \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="1a943-113">Pasirinkite internetinę parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="1a943-113">Select the online store.</span></span>
1. <span data-ttu-id="1a943-114">Įsitikinkite, kad „FastTab” **Mokėjimo sąskaitos** laukas **Leisti įrašyti el. prekybos mokėjimo informaciją** nustatytas į **Teisinga**.</span><span class="sxs-lookup"><span data-stu-id="1a943-114">On the **Payment accounts** FastTab, make sure that the **Allow saving payment information in e-commerce** field is set to **True**.</span></span>

![Leisti įrašyti mokėjimo informaciją „Commerce Headquarters” el. prekybos lauke](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a><span data-ttu-id="1a943-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1a943-116">Additional resources</span></span>

[<span data-ttu-id="1a943-117">Mokėjimo modulis</span><span class="sxs-lookup"><span data-stu-id="1a943-117">Payment module</span></span>](../payment-module.md)

[<span data-ttu-id="1a943-118">Internetinių mokėjimo priemonių įrašymas naudojant „Adyen“ jungtį</span><span class="sxs-lookup"><span data-stu-id="1a943-118">Saving online payment instruments with the Adyen connector</span></span>](../dev-itpro/adyen-connector-listPI.md)
