---
title: Kredito kortelės įrašo puslapyje rodoma klaida išregistravimo metu
description: Šioje temoje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai mokėjimo būdo skiltis neįkelta, ir rodomas klaidos pranešimas.
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
ms.openlocfilehash: f0751fc76e6eb4320f766886b4c1efcb1042e996
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585442"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="3f470-103">Kredito kortelės įrašo puslapyje rodoma klaida išregistravimo metu</span><span class="sxs-lookup"><span data-stu-id="3f470-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3f470-104">Šioje temoje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai **mokėjimo būdo** skiltis neįkelta, ir rodomas klaidos pranešimas.</span><span class="sxs-lookup"><span data-stu-id="3f470-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="3f470-105">aprašymas</span><span class="sxs-lookup"><span data-stu-id="3f470-105">Description</span></span>

<span data-ttu-id="3f470-106">Kai atidarote interneto parduotuvės mokėjimo puslapį, skiltis **Mokėjimo būdas** neįkeliama ir rodomas toks klaidos pranešimas: „Kažkas nutiko.</span><span class="sxs-lookup"><span data-stu-id="3f470-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="3f470-107">Bandykite vėliau.“</span><span class="sxs-lookup"><span data-stu-id="3f470-107">Please try again later."</span></span>

![Mokėjimo modulio klaida](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="3f470-109">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="3f470-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="3f470-110">Laukti, kol baigsis „Commerce Scale Unit“ talpyklos galiojimas</span><span class="sxs-lookup"><span data-stu-id="3f470-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="3f470-111">Mokėjimo paslaugos nustatymai interneto parduotuvės mokėjimo puslapyje talpinami „Commerce Scale Unit“ ir gali užtrukti iki 15 minučių, kol jie pasirodys el. komercijos svetainėje.</span><span class="sxs-lookup"><span data-stu-id="3f470-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="3f470-112">Šie mokėjimo tarnybos nustatymai apima prekybininko paskyros ID, debesies API rakto ir įvairių konfigūravimo nustatymų, susijusių su mokėjimo būdu, pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="3f470-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3f470-113">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3f470-113">Additional resources</span></span>

[<span data-ttu-id="3f470-114">Interneto kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="3f470-114">Set up an online channel</span></span>](../channel-setup-online.md)
