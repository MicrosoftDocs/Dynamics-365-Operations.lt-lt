---
title: Grąžinimo užsakymo pinigų grąžinimas atmestas
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, galinčios padėti, kai atmetamas grąžinimo užsakymo pinigų grąžinimas, nes SF išrašyti naudojama kredito kortelė skiriasi nuo kortelės, kuri buvo naudojama atliekant pradinį mokėjimo autorizavimą.
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
ms.openlocfilehash: e202c6b4b9e025d5af1cd5eb6235884aab6444e6
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585453"
---
# <a name="refund-on-a-return-order-is-declined"></a><span data-ttu-id="166dd-103">Grąžinimo užsakymo pinigų grąžinimas atmestas</span><span class="sxs-lookup"><span data-stu-id="166dd-103">Refund on a return order is declined</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="166dd-104">Šioje temoje pateikiamos trikčių diagnostikos priemonės, galinčios padėti, kai atmetamas grąžinimo užsakymo pinigų grąžinimas, nes SF išrašyti naudojama kredito kortelė skiriasi nuo kortelės, kuri buvo naudojama atliekant pradinį mokėjimo autorizavimą.</span><span class="sxs-lookup"><span data-stu-id="166dd-104">This topic provides troubleshooting guidance that can help when a refund on a return order is declined because the credit card that is used for invoicing differs from the card that was used during the original payment authorization.</span></span>

## <a name="description"></a><span data-ttu-id="166dd-105">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="166dd-105">Description</span></span>

<span data-ttu-id="166dd-106">Pinigų grąžinimas atmetamas, kai grąžinimo užsakymo SF išrašyti naudojama kredito kortelė skiriasi nuo kortelės, naudotos atliekant pradinį mokėjimo autorizavimą.</span><span class="sxs-lookup"><span data-stu-id="166dd-106">A refund is declined when the credit card that is used to invoice a return order differs from the card that was used during the original payment authorization.</span></span> <span data-ttu-id="166dd-107">Gaunate toliau nurodytą klaidos pranešimą: „Kai kurių mokėjimų būsena nėra tinkama registruoti.</span><span class="sxs-lookup"><span data-stu-id="166dd-107">You receive the following error message: "Some payments are not in the correct status for posting.</span></span> <span data-ttu-id="166dd-108">Prieš išrašydami SF, iš naujo patikrinkite visų mokėjimų būsenas.”</span><span class="sxs-lookup"><span data-stu-id="166dd-108">Please re-validate the status of all payments prior to invoicing."</span></span>

<span data-ttu-id="166dd-109">Mokėjimo autorizavimo informacijoje rasite toliau nurodytą klaidos pranešimą: „Adyen“ šliuzas SendRequest() nepavyko, būsena „InternalServerError“.22144; Iš „Adyen” grąžintas tuščias atsakymas.(22001);”</span><span class="sxs-lookup"><span data-stu-id="166dd-109">The payment authorization details will include the following error message: "Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"</span></span>

![Klaida Grąžinimo užsakymo pinigų grąžinimas atmestas](media/refund-order-decline.jpg)

## <a name="resolution"></a><span data-ttu-id="166dd-111">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="166dd-111">Resolution</span></span>

### <a name="enable-blind-returns-in-adyen"></a><span data-ttu-id="166dd-112">Įgalinti anoniminius „Adyen” grąžinimus</span><span class="sxs-lookup"><span data-stu-id="166dd-112">Enable blind returns in Adyen</span></span>

<span data-ttu-id="166dd-113">Norėdami įgalinti anoniminius grąžinimus, atlikite veiksmus, pateiktus [„Dynamics 365 Payment Connector“, skirtos „Adyen“, trikčių šalinimas](adyen-support.md), norėdami susisiekti su „Adyen“ palaikymo komanda ir pateikti užklausą, kad jūsų „Adyen“ prekybininko sąskaitoje būtų įjungti anoniminiai grąžinimai.</span><span class="sxs-lookup"><span data-stu-id="166dd-113">To enable blind returns, follow the steps in [Troubleshoot Dynamics 365 Payment Connector for Adyen issues](adyen-support.md) to contact the Adyen support team and request that blind returns be enabled on your Adyen merchant account.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="166dd-114">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="166dd-114">Additional resources</span></span>

[<span data-ttu-id="166dd-115">„Dynamics 365“ mokėjimo jungtis, skirta sprendimui „Adyen“</span><span class="sxs-lookup"><span data-stu-id="166dd-115">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="166dd-116">„Adyen Payment Connector“, skirtos „Dynamics 365“, nustatymas</span><span class="sxs-lookup"><span data-stu-id="166dd-116">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
