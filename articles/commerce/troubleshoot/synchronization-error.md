---
title: Užsakymo sinchronizavimo klaida, susijusi su numatytąja mokėjimo tarnyba
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, galinčios padėti ištaisyti klaidą, kuri gali įvykti sinchronizuojant internetinį užsakymą.
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
ms.openlocfilehash: 45eeae751051b58e1c9e725eb4ed4b5240026e7f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801440"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="b1bcc-103">Užsakymo sinchronizavimo klaida, susijusi su numatytąja mokėjimo tarnyba</span><span class="sxs-lookup"><span data-stu-id="b1bcc-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b1bcc-104">Šioje temoje pateikiamos trikčių diagnostikos priemonės, galinčios padėti ištaisyti klaidą, kuri gali įvykti sinchronizuojant internetinį užsakymą.</span><span class="sxs-lookup"><span data-stu-id="b1bcc-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="b1bcc-105">aprašymas</span><span class="sxs-lookup"><span data-stu-id="b1bcc-105">Description</span></span>

<span data-ttu-id="b1bcc-106">Kai sinchronizuojate internetinį užsakymą, gaunate šį klaidos pranešimą: „Norint apdoroti kredito kortelės operacijas, turi būti nustatyta numatytoji mokėjimo tarnyba.”</span><span class="sxs-lookup"><span data-stu-id="b1bcc-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![Trūkstamos numatytosios mokėjimo tarnybos klaida](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="b1bcc-108">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="b1bcc-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="b1bcc-109">Patvirtinti arba nustatyti numatytąją mokėjimo tarnybą „Commerce Headquarters”</span><span class="sxs-lookup"><span data-stu-id="b1bcc-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="b1bcc-110">Norėdami patvirtinti arba nustatyti numatytąją mokėjimo tarnybą „Commerce Headquarters”, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b1bcc-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="b1bcc-111">Eikite į **Gautinos sumos \> Mokėjimų sąranka \> Mokėjimo tarnybos**.</span><span class="sxs-lookup"><span data-stu-id="b1bcc-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="b1bcc-112">Įsitikinkite, kad vienos mokėjimo tarnybos parinktis **Numatytasis naujų kredito kortelių procesorius** nustatyta į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="b1bcc-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1bcc-113">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b1bcc-113">Additional resources</span></span>

[<span data-ttu-id="b1bcc-114">Kredito kortelių nustatymas, autorizacija ir patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="b1bcc-114">Credit card setup, authorization, and capture</span></span>](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)
