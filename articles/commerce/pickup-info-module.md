---
title: Paėmimo informacijos modulis
description: Ši tema apima paėmimo informacijos modulį ir aprašo, kaip įtraukti jį į išregistravimo puslapius „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 222e8ad79b30e5197f7140958309d442b284f286
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263185"
---
# <a name="pickup-information-module"></a><span data-ttu-id="69d55-103">Paėmimo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="69d55-103">Pickup information module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="69d55-104">Ši tema apima paėmimo informacijos modulį ir aprašo, kaip įtraukti jį į išregistravimo puslapius „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="69d55-104">This topic covers the pickup information module and describes how to add it to checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="69d55-105">Paėmimo informacijos modelis gali būti naudojamas išsiregistravimo modeliui, kad jis rodytų užsakymo paėmimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="69d55-105">The pickup information module can be used in a checkout module to show order pickup information.</span></span> <span data-ttu-id="69d55-106">Klientai gali peržiūrėti esamas paėmimo datas ir laiko vietas ir tada rinktis tinkamą laiką jų užsakymo paėmimui.</span><span class="sxs-lookup"><span data-stu-id="69d55-106">Customers can view available pickup dates and time slots, and then select a suitable time to pick up their order.</span></span> <span data-ttu-id="69d55-107">Pavyzdžiui, klientas gali rinktis paėmimą 15 valandą kovo 21 dieną iš San Francisko parduotuvės.</span><span class="sxs-lookup"><span data-stu-id="69d55-107">For example, a customer can choose to pick up an order at 3 PM on March 21 from the San Francisco store.</span></span>

<span data-ttu-id="69d55-108">Paėmimo laikai atitinkamoms parduotuvėms turi būti sukonfigūruoti komercijos štabe.</span><span class="sxs-lookup"><span data-stu-id="69d55-108">Pickup time slots for the appropriate stores must be configured in Commerce headquarters.</span></span> <span data-ttu-id="69d55-109">Dėl išsamesnės informacijos, žr. [Sukurti ir naujinti laiko vietas kliento paėmimui](dev-itpro/pickup-timeslots.md).</span><span class="sxs-lookup"><span data-stu-id="69d55-109">For more information, see [Create and update time slots for customer pickup](dev-itpro/pickup-timeslots.md).</span></span>

<span data-ttu-id="69d55-110">Jei paėmimo informacijos modulis sukuriamas išsiregistravimo puslapyje, bet nėra jokių laiko vietų nustatytų parduotuvei, kuri pasirinkta, modulis rodys informaciją, bet vartotojas negalės pasirinkti laiko vietos.</span><span class="sxs-lookup"><span data-stu-id="69d55-110">If a pickup information module is created on a checkout page, but no time slots are defined for the store that is selected for pickup, the module will show information, but the user won't be able to select any time slots.</span></span> <span data-ttu-id="69d55-111">Laiko vietos yra pasirenkamos ir nebūtinos užsakymo padarymui.</span><span class="sxs-lookup"><span data-stu-id="69d55-111">Time slots are optional and aren't required to place an order.</span></span>

<span data-ttu-id="69d55-112">Jei kelios prekės pasirenkamos paėmimui keletoje parduotuvių, paėmimo informacijos modulis leidžia vartotojui pasirinkti laiko vietą kiekvienai parduotuvei su sąlyga, kad laiko vietos yra joms prieinamos.</span><span class="sxs-lookup"><span data-stu-id="69d55-112">If multiple items are selected for pickup across multiple stores, the pickup information module will let the user select a time slot for each store, provided that time slots are available for it.</span></span>

> [!NOTE]
> <span data-ttu-id="69d55-113">Palaikymas laiko vietoms ir išsiregistravimo paėmimo informacijos modulis prieinamas „Dynamics 365 Commerce“ versijoje 10.0.15 ir vėlesnėse.</span><span class="sxs-lookup"><span data-stu-id="69d55-113">Support for time slots and the checkout pickup information module is available in Dynamics 365 Commerce version 10.0.15 and later.</span></span>

<span data-ttu-id="69d55-114">Tolesnis paveikslėlis rodo pavyzdį laiko vietos pasirinkimo per paėmimo informacijos modulį išsiregistravimo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="69d55-114">The following illustration shows an example of time slot selection through the pickup information module on a checkout page.</span></span>

![Paėmimo informacijos modulio pavyzdys išsiregsitravimo puslapyje](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a><span data-ttu-id="69d55-116">Modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="69d55-116">Module properties</span></span>

- <span data-ttu-id="69d55-117">**Antraštė** – Įveskite antraštę moduliui.</span><span class="sxs-lookup"><span data-stu-id="69d55-117">**Heading** – Enter a heading for the module.</span></span>

## <a name="show-time-slot-information-after-an-order-is-placed"></a><span data-ttu-id="69d55-118">Rodyti vietos informaciją po užsakymo padarymo</span><span class="sxs-lookup"><span data-stu-id="69d55-118">Show time slot information after an order is placed</span></span>

<span data-ttu-id="69d55-119">Kai užsakymas yra padarytas, informacija apie pasirinktą laiko vietą gali būti peržiūrėta [užsakymo patvirtinimo modulis](order-confirmation-module.md) ir [užsakymo informacijos modulis](account-management.md#order-details-page).</span><span class="sxs-lookup"><span data-stu-id="69d55-119">After an order is placed, information about the selected time slot can be viewed in the [order confirmation module](order-confirmation-module.md) and the [order details module](account-management.md#order-details-page).</span></span> <span data-ttu-id="69d55-120">Abu šie moduliai turi **Rodyti laiko vietos informacijos** ypatybę.</span><span class="sxs-lookup"><span data-stu-id="69d55-120">Both these modules have a **Show timeslot information** property.</span></span> <span data-ttu-id="69d55-121">Prieš tai, kai galima rodyti pasirinktą laiko vietą užsakymo proceso metu, ši ypatybė turi būti nustatyta į **Teisinga**.</span><span class="sxs-lookup"><span data-stu-id="69d55-121">Before they can show the selected time slot during the order process, this property must be set to **True**.</span></span>

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a><span data-ttu-id="69d55-122">Įtraukite išsiregistravimo paėmimo informacijos modulį į puslapį</span><span class="sxs-lookup"><span data-stu-id="69d55-122">Add a checkout pickup information module to a page</span></span>

<span data-ttu-id="69d55-123">Dėl instrukcijų, kaip įtraukti paėmimo informacijos modulį į išsiregistravimo puslapį ir nustatyti būtinas ypatybes, žr. [Išsiregistravimo modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="69d55-123">For instructions about how to add a pickup information module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="69d55-124">Tolesnis paveikslėlis rodo e-komercijos išsiregistravimo puslapio pavyzdį, kuris apima laiko vietas paėmimo eilučių prekėms.</span><span class="sxs-lookup"><span data-stu-id="69d55-124">The following illustration shows an example of an e-Commerce checkout page that includes time slots for pickup line items.</span></span>

![E-komercijos išsiregistravimo puslapio pavyzdys, kuris apima laiko vietas paėmimo eilučių prekėms.](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a><span data-ttu-id="69d55-126">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="69d55-126">Additional resources</span></span>

[<span data-ttu-id="69d55-127">Sukurti ir naujinti laiko vietas kliento paėmimu</span><span class="sxs-lookup"><span data-stu-id="69d55-127">Create and update time slots for customer pickup</span></span>](dev-itpro/pickup-timeslots.md)

[<span data-ttu-id="69d55-128">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="69d55-128">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="69d55-129">Užsakymo patvirtinimo modulis</span><span class="sxs-lookup"><span data-stu-id="69d55-129">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="69d55-130">Išsamios užsakymo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="69d55-130">Order details module</span></span>](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]