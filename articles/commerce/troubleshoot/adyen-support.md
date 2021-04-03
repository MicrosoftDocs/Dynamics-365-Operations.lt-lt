---
title: „Dynamics 365“ mokėjimo jungties, skirtos sprendimui „Adyen“, trikčių šalinimas
description: Šioje temoje pateikiamos trikčių diagnostikos gairės, kurios gali padėti gauti palaikymo, kai kyla problemų su „Microsoft Dynamics 365“ mokėjimo jungtimi, skirta sprendimui „Adyen“.
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
ms.openlocfilehash: f01db3fa670355696c094be544775a3abc557a70
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585440"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="7c287-103">„Dynamics 365“ mokėjimo jungties, skirtos sprendimui „Adyen“, trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="7c287-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7c287-104">Šioje temoje pateikiamos trikčių diagnostikos gairės, kurios gali padėti gauti palaikymo, kai kyla problemų su „Microsoft Dynamics 365“ mokėjimo jungtimi, skirta sprendimui „Adyen“.</span><span class="sxs-lookup"><span data-stu-id="7c287-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="7c287-105">aprašymas</span><span class="sxs-lookup"><span data-stu-id="7c287-105">Description</span></span>

<span data-ttu-id="7c287-106">Šiose srityse jums kyla problemų su „Dynamics 365“ mokėjimo jungtimi, skirta sprendimui „Adyen“ ir jums reikia „Adyen“ komandos palaikymo:</span><span class="sxs-lookup"><span data-stu-id="7c287-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="7c287-107">Elektroninio kasos aparato (EKA), modernaus elektroninio kasos aparato (MEKA), skambučių centro ar „Dynamics 365 Commerce“ konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="7c287-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="7c287-108">„Adyen“ mokėjimo paslaugų teikėjo (MPT) nuorodos numeris (pvz., jei turite klausimų dėl atsisakymų, įskaitant rankiniu būdu įvedamus raktinius \[\] atsisakymus)</span><span class="sxs-lookup"><span data-stu-id="7c287-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="7c287-109">Bet kas, kas neveikia testavimo ar tiesioginio prekybininko aplinkoje</span><span class="sxs-lookup"><span data-stu-id="7c287-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="7c287-110">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="7c287-110">Resolution</span></span>

<span data-ttu-id="7c287-111">Naudokite šį el. laiško šabloną, kad pradėtumėte palaikymo procesą su „Adyen“ komanda.</span><span class="sxs-lookup"><span data-stu-id="7c287-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="7c287-112">Jei paspartinti trikčių šalinimą, įsitikinkite, kad el. laiške yra visa reikiama informacija.</span><span class="sxs-lookup"><span data-stu-id="7c287-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="7c287-113">Laukas</span><span class="sxs-lookup"><span data-stu-id="7c287-113">Field</span></span>        | <span data-ttu-id="7c287-114">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="7c287-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="7c287-115">Į</span><span class="sxs-lookup"><span data-stu-id="7c287-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="7c287-116">Kopija</span><span class="sxs-lookup"><span data-stu-id="7c287-116">Cc</span></span>           | |
| <span data-ttu-id="7c287-117">Temos eilutė</span><span class="sxs-lookup"><span data-stu-id="7c287-117">Subject line</span></span> | <span data-ttu-id="7c287-118">„Microsoft Dynamics“ palaikymo užklausa</span><span class="sxs-lookup"><span data-stu-id="7c287-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="7c287-119">Turinys</span><span class="sxs-lookup"><span data-stu-id="7c287-119">Body</span></span>         | <p><span data-ttu-id="7c287-120">Sveiki, palaikymo skyriaus darbuotojai,</span><span class="sxs-lookup"><span data-stu-id="7c287-120">Hi Support,</span></span></p><p><span data-ttu-id="7c287-121">Prašau suteikti pagalbos sprendžiant šią problemą:</span><span class="sxs-lookup"><span data-stu-id="7c287-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="7c287-122">Prekybininko sąskaita</span><span class="sxs-lookup"><span data-stu-id="7c287-122">Merchant account</span></span></li><li><span data-ttu-id="7c287-123">Aplinka (testavimas / gamyba)</span><span class="sxs-lookup"><span data-stu-id="7c287-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="7c287-124">Kanalas (EKA / skambučių centras / el. komercijos skyrius)</span><span class="sxs-lookup"><span data-stu-id="7c287-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="7c287-125">MPT nuorodos numeris, jei problema yra susijusi su konkrečia operacija (MPT nuorodos numerį galima rasti ant kvito, „Adyen“ klientų aptarnavimo srityje arba EKA terminalo operacijų meniu).</span><span class="sxs-lookup"><span data-stu-id="7c287-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="7c287-126">Klaidos pranešimo ekrano nuotrauka arba nuotrauka, jei taikoma</span><span class="sxs-lookup"><span data-stu-id="7c287-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="7c287-127">Įvykių peržiūros programos žurnalai (.txt formatu)</span><span class="sxs-lookup"><span data-stu-id="7c287-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="7c287-128">Problemos ir trikčių šalinimo veiksmų, kuriuos bandėte atlikti, aprašas</span><span class="sxs-lookup"><span data-stu-id="7c287-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="7c287-129">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="7c287-129">Additional resources</span></span>

[<span data-ttu-id="7c287-130">Priimti mokėjimus naudojant „Adyen“ jungtį, skirtą „Dynamics 365 Commerce“</span><span class="sxs-lookup"><span data-stu-id="7c287-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="7c287-131">„Dynamics 365“ mokėjimo jungtis, skirta sprendimui „Adyen“</span><span class="sxs-lookup"><span data-stu-id="7c287-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="7c287-132">„Adyen Payment Connector“, skirtos „Dynamics 365“, nustatymas</span><span class="sxs-lookup"><span data-stu-id="7c287-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
