---
title: Klaida „Mokėjimo tipas turi būti kredito kortelė” pardavimo užsakymo puslapyje
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, galinčios padėti, kai pardavimo užsakymo puslapyje sinchronizavus užsakymą rodomas klaidos pranešimas.
author: Reza-Assadi
manager: AnnBe
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
ms.openlocfilehash: 20f18507dee330fd1affedeee092b3dfa7cc10bc
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585448"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a><span data-ttu-id="60694-103">Klaida „Mokėjimo tipas turi būti kredito kortelė” pardavimo užsakymo puslapyje</span><span class="sxs-lookup"><span data-stu-id="60694-103">"Payment type must be credit card" error on the sales order page</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="60694-104">Šioje temoje pateikiamos trikčių diagnostikos priemonės, galinčios padėti, kai pardavimo užsakymo puslapyje sinchronizavus užsakymą rodomas klaidos pranešimas.</span><span class="sxs-lookup"><span data-stu-id="60694-104">This topic provides troubleshooting guidance that can help when an error message is shown on the sales order page after an order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="60694-105">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="60694-105">Description</span></span>

<span data-ttu-id="60694-106">Kai sinchronizavę užsakymą atidarote pardavimo užsakymo puslapį, gaunate tokį klaidos pranešimą: „Mokėjimo tipas turi būti kredito kortelė, nes nurodytas kredito kortelės numeris.“</span><span class="sxs-lookup"><span data-stu-id="60694-106">When you open the sales order page after you sync an order, you receive the following error message: "The payment type must be credit card, since the credit card number has been specified."</span></span>

![Klaida Mokėjimo tipas turi būti kredito kortelė](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a><span data-ttu-id="60694-108">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="60694-108">Resolution</span></span>

### <a name="set-the-payment-type-in-commerce-headquarters"></a><span data-ttu-id="60694-109">Nustatyti mokėjimo tipą „Commerce Headquarters”</span><span class="sxs-lookup"><span data-stu-id="60694-109">Set the payment type in Commerce headquarters</span></span>

1. <span data-ttu-id="60694-110">Pasirinkite **Gautinos sumos \> Mokėjimų sąranka \> Mokėjimo sąlygos**.</span><span class="sxs-lookup"><span data-stu-id="60694-110">Go to **Accounts receivable \> Payment setup \> Terms of payment**.</span></span>
1. <span data-ttu-id="60694-111">Kairiojoje naršymo srityje pasirinkite mokėjimo sąlygas.</span><span class="sxs-lookup"><span data-stu-id="60694-111">In the left navigation, select your terms of payment.</span></span>
1. <span data-ttu-id="60694-112">Lauke **Mokėjimo tipas** patikrinkite, ar pasirinkta **Kredito kortelė**.</span><span class="sxs-lookup"><span data-stu-id="60694-112">In the **Payment type** field, make sure that **Credit card** is selected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="60694-113">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="60694-113">Additional resources</span></span>

[<span data-ttu-id="60694-114">Pardavimo ir mokėjimų internetu registravimas</span><span class="sxs-lookup"><span data-stu-id="60694-114">Posting of online sales and payments</span></span>](../tasks/posting-online-sales-payments.md)
