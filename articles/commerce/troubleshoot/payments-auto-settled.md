---
title: Mokėjimai automatiškai sudengiami prieš išrašant užsakymų SF arba juos išsiunčiant
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai mokėjimas sudengtas „Adyen” portale iš karto po užsakymo pateikimo, net jei nebuvo išrašyta pardavimo užsakymo SF arba jis nebuvo išsiųstas.
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
ms.openlocfilehash: 788854a3119eb9ffaf839beb93a5bc15cdcd6387
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585447"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a><span data-ttu-id="71677-103">Mokėjimai automatiškai sudengiami prieš išrašant užsakymų SF arba juos išsiunčiant</span><span class="sxs-lookup"><span data-stu-id="71677-103">Payments are automatically settled before orders are invoiced or shipped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="71677-104">Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai mokėjimas sudengtas „Adyen” portale iš karto po užsakymo pateikimo, net jei nebuvo išrašyta pardavimo užsakymo SF arba jis nebuvo išsiųstas.</span><span class="sxs-lookup"><span data-stu-id="71677-104">This topic provides troubleshooting guidance that can help when a payment is settled in the Adyen portal immediately after an order is placed, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="description"></a><span data-ttu-id="71677-105">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="71677-105">Description</span></span>

<span data-ttu-id="71677-106">Po užsakymo pateikimo mokėjimas iš karto sudengiamas „Adyen” portale, net jei nebuvo išrašyta pardavimo užsakymo SF arba jis nebuvo išsiųstas.</span><span class="sxs-lookup"><span data-stu-id="71677-106">After an order is placed, the payment is immediately settled in the Adyen portal, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="resolution"></a><span data-ttu-id="71677-107">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="71677-107">Resolution</span></span>

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a><span data-ttu-id="71677-108">Konfigūruoti el. prekybos mokėjimų rankinį fiksavimą „Adyen” portale</span><span class="sxs-lookup"><span data-stu-id="71677-108">Configure manual capture for e-commerce payments in the Adyen portal</span></span>

<span data-ttu-id="71677-109">Norėdami konfigūruoti el. prekybos mokėjimų rankinį fiksavimą „Adyen” portale, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="71677-109">To configure manual capture for e-commerce payments in the Adyen portal, follow these steps.</span></span>

1. <span data-ttu-id="71677-110">Prisijunkite prie „Adyen” portalo.</span><span class="sxs-lookup"><span data-stu-id="71677-110">Sign in to the Adyen portal.</span></span>
1. <span data-ttu-id="71677-111">Viršutiniame dešiniajame kampe pasirinkite savo el. prekybos kanalo prekybininko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="71677-111">In the upper-right corner, select your merchant account for the e-commerce channel.</span></span>
1. <span data-ttu-id="71677-112">Viršutinėje naršymo juostoje pasirinkite **Sąskaita**, tada – **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="71677-112">On the top navigation, select **Account**, and then select **Settings**.</span></span>
1. <span data-ttu-id="71677-113">Lauke **Fiksavimo delsa** pasirinkite **Rankinis**.</span><span class="sxs-lookup"><span data-stu-id="71677-113">In the **Capture Delay** field, select **manual**.</span></span>

    ![Fiksavimo delsos parametras „Adyen” portale](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a><span data-ttu-id="71677-115">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="71677-115">Additional resources</span></span>

[<span data-ttu-id="71677-116">„Adyen“ mokėjimo fiksavimas</span><span class="sxs-lookup"><span data-stu-id="71677-116">Adyen payment capture</span></span>](https://docs.adyen.com/point-of-sale/capturing-payments)

[<span data-ttu-id="71677-117">„Dynamics 365“ mokėjimo jungtis, skirta sprendimui „Adyen“</span><span class="sxs-lookup"><span data-stu-id="71677-117">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="71677-118">„Adyen Payment Connector“, skirtos „Dynamics 365“, nustatymas</span><span class="sxs-lookup"><span data-stu-id="71677-118">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)