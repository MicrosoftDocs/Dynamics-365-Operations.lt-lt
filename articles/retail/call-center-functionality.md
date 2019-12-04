---
title: Skambučių centro pardavimo funkcijos
description: Šioje temoje pateikiama skambučių centro pardavimo funkcijos programoje „Dynamics 365 Retail“ apžvalga.
author: josaw1
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 2e44770af4a30f539e56d38b21c897cacd2707e7
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812344"
---
# <a name="call-center-sales-functionality"></a><span data-ttu-id="30035-103">Skambučių centro pardavimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="30035-103">Call center sales functionality</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="30035-104">Programoje „Dynamics 365 Retail“ skambučių centras yra mažmeninės prekybos kanalo tipas, kurį galima nustatyti programoje.</span><span class="sxs-lookup"><span data-stu-id="30035-104">In Dynamics 365 Retail, a call center is a type of Retail channel that can be defined in the application.</span></span> <span data-ttu-id="30035-105">Apibrėžus konkretų savo skambučių centro objektų kanalą, sistema leidžia susieti konkrečius duomenis pagal numatytuosius nustatymus ir užsakymo apdorojimo numatytuosius nustatymus su pardavimo užsakymais, sukurtais skambučių centro kanalo vartotojo.</span><span class="sxs-lookup"><span data-stu-id="30035-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="30035-106">Skambučių centro funkcijos apima išplėstinę mažmeninės prekybos kainą ir akcijas, katalogus, dovanų korteles, lojalumo programos ir kuponus.</span><span class="sxs-lookup"><span data-stu-id="30035-106">Call center features include advanced retail price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="30035-107">Skambučių centro užsakymai taip pat pasitelkiami iš elektroninio kasos aparato (EKA) programos, kelių kanalų užsakymo įvykdymo scenarijams palaikyti.</span><span class="sxs-lookup"><span data-stu-id="30035-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="30035-108">Svarbu atkreipti dėmesį, kad jei skambučių centro modulį galima naudoti kitose pramonės šakose už mažmeninės prekybos ribų, dabartinis „Retail“ skambučių centro programos leidimas nėra optimizuotas naudoti verslo įmonių tarpusavio (B2B) užsakymų apdorojimo scenarijams arba tiems scenarijams, kurių užsakymuose yra daug pardavimo eilučių.</span><span class="sxs-lookup"><span data-stu-id="30035-108">It's important to note that while the call center module can be utilized by other industries outside of Retail, the current release of the Retail call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large amount of sales lines.</span></span> <span data-ttu-id="30035-109">Rekomenduojama, kad vartotojai, kurie nori naudoti skambučių centro funkcijos užsakymams apdoroti už įprasto tiesioginio vartotojų operacijų vykdymo ribų, skirtų pakankamai laiko išbandyti ir patikrinti, kad skambučių centro funkcijų įjungimas atitiks funkcinius ir našumo poreikius.</span><span class="sxs-lookup"><span data-stu-id="30035-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="30035-110">Be to, kad palaiko užsakymo kūrimą, skambučių centro modulis vartotojui dar pateikia ir vartotojui patogią aptarnavimo programą, kuri vartotojams leidžia lengviau rasti klientų sąskaitas ir peržiūrėti visus susijusius kliento užsakymų duomenis ir atributus.</span><span class="sxs-lookup"><span data-stu-id="30035-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="30035-111">Klientų aptarnavimo ekranas sukurtas taip, kad leistų vartotojui greitai pasiekti su užsakymu susijusius duomenis, kurie leidžia atsakyti į dažniausius iš klientų gautus su užsakymu susijusius klausimus.</span><span class="sxs-lookup"><span data-stu-id="30035-111">The customer service screen is designed to enable a user to quickly access order related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="30035-112">Šiame puslapyje pateikiami saitai į susijusius dokumentus, susijusius su nustatymas, konfigūracija ir skambučių centro funkcijų naudojimu programoje „Retail“.</span><span class="sxs-lookup"><span data-stu-id="30035-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features in Retail.</span></span>


## <a name="configure-the-call-center"></a><span data-ttu-id="30035-113">Sukonfigūruokite skambučių centrą</span><span class="sxs-lookup"><span data-stu-id="30035-113">Configure the call center</span></span>

[<span data-ttu-id="30035-114">Skambučių centro kanalų nustatymas</span><span class="sxs-lookup"><span data-stu-id="30035-114">Set up call center channels</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="30035-115">Užsakymų apdorojimo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="30035-115">Configure order processing</span></span>

[<span data-ttu-id="30035-116">Įspėjimų dėl apgaulės nustatymas skambučių centre ir jų naudojimas</span><span class="sxs-lookup"><span data-stu-id="30035-116">Set up and work with call center fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="30035-117">Skambučių centro užsakymo sulaikymo funkcijų konfigūravimas ir jų naudojimas</span><span class="sxs-lookup"><span data-stu-id="30035-117">Configure and work with call center order holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="30035-118">Mokėjimo apdorojimo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="30035-118">Configure payment processing</span></span>

[<span data-ttu-id="30035-119">Mokėjimo būdai skambučių centruose</span><span class="sxs-lookup"><span data-stu-id="30035-119">Payment methods in call centers</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="30035-120">Konfigūruoti pristatymo būdus</span><span class="sxs-lookup"><span data-stu-id="30035-120">Configure delivery modes</span></span>

[<span data-ttu-id="30035-121">Konfigūruoti skambučių centro pristatymo būdus ir mokesčius</span><span class="sxs-lookup"><span data-stu-id="30035-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="30035-122">Tiesioginės rinkodaros konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="30035-122">Configure direct marketing</span></span>

[<span data-ttu-id="30035-123">Skambučių centro katalogai</span><span class="sxs-lookup"><span data-stu-id="30035-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="30035-124">„Recency“, dažnumo ir piniginės (RFM) analizės nustatymas</span><span class="sxs-lookup"><span data-stu-id="30035-124">Set up Recency, Frequency, and Monetary (RFM) analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="30035-125">Tęstinumo programų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="30035-125">Configure continuity programs</span></span>

[<span data-ttu-id="30035-126">Skambučių centrų tęstinumo programų nustatymas</span><span class="sxs-lookup"><span data-stu-id="30035-126">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
