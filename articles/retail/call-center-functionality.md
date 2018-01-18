---
title: "Skambučių centro funkcijos"
description: "Šioje temoje pateikiama skambučių centro pardavimo funkcijos programoje „Microsoft Dynamics 365 for Retail“ apžvalga."
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 55bad891f9295eca6b0bf39847ede890b7294370
ms.contentlocale: lt-lt
ms.lasthandoff: 01/17/2018

---

# <a name="call-center-functionality"></a><span data-ttu-id="b8675-103">Skambučių centro funkcijos</span><span class="sxs-lookup"><span data-stu-id="b8675-103">Call center functionality</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="b8675-104">Šiame straipsnyje pateikta skambučių centro pardavimo funkcijos programoje „Microsoft Dynamics 365 for Retail“ apžvalga.</span><span class="sxs-lookup"><span data-stu-id="b8675-104">This article provides an overview of the call center sales functionality in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="b8675-105">„Dynamics 365 for Retail“ palaiko skambučių centrus kaip mažmeninės prekybos kanalo tipą.</span><span class="sxs-lookup"><span data-stu-id="b8675-105">Dynamics 365 for Retail supports call centers as a type of retail channel.</span></span> <span data-ttu-id="b8675-106">Skambučių centre darbuotojai telefonu priima klientų užsakymus ir kuria pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="b8675-106">In a call center, workers take orders from customers over the phone and create sales orders.</span></span> <span data-ttu-id="b8675-107">Skambučių centro funkcija apima savybes, kurios padeda lengviau priimti užsakymus telefonu ir vykdyti klientų aptarnavimą visu užsakymo vykdymo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="b8675-107">Call center functionality includes features that are designed to make it easier to take phone orders and handle customer service throughout the order fulfillment process.</span></span> <span data-ttu-id="b8675-108">Pavyzdžiui, skambučių centro darbuotojai gali įvesti mokėjimo informaciją tiesiai į pardavimo užsakymą ir peržiūrėti išsamią mokesčių ir mokėjimų suvestinę prieš pateikdami užsakymą.</span><span class="sxs-lookup"><span data-stu-id="b8675-108">For example, call center workers can enter payment information directly into the sales order, and can view a detailed summary of charges and payments before they submit the order.</span></span> <span data-ttu-id="b8675-109">Darbuotojai taip pat turi galimybę kontroliuoti kainodarą ir gali pasiekti įvairius duomenis apie klientus, produktus ir kainas iš puslapio **Pardavimo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="b8675-109">Workers also have options for controlling pricing, and can access various data about customers, products, and prices from the **Sales order** page.</span></span> <span data-ttu-id="b8675-110">Be to, skambučių centruose yra išplėstinė funkcija, suteikianti galimybę stebėti klientų retrospektyvą ir užsakymo būseną.</span><span class="sxs-lookup"><span data-stu-id="b8675-110">Additionally, call centers have enhanced functionality for tracking customer history and order status.</span></span> <span data-ttu-id="b8675-111">Kiekvienas skambučių centras gali turėti atskirus vartotojus, mokėjimo būdus, kainų grupes, finansines dimensijas ir pristatymo būdus.</span><span class="sxs-lookup"><span data-stu-id="b8675-111">Each call center can have its own users, payment methods, price groups, financial dimensions, and modes of delivery.</span></span> <span data-ttu-id="b8675-112">Šias parinktis galite konfigūruoti kurdami skambučių centrą.</span><span class="sxs-lookup"><span data-stu-id="b8675-112">You can configure these options when you create the call center.</span></span> <span data-ttu-id="b8675-113">Papildomai galite naudoti puslapį **Skambučių centras** norėdami įjungti arba išjungti šias unikalių skambučių centrų funkcijų grupes.</span><span class="sxs-lookup"><span data-stu-id="b8675-113">Additionally, you can use the **Call center** page to enable or disable the following groups of features that are unique to call centers:</span></span>

-   <span data-ttu-id="b8675-114">**Užsakymo baigimas** – ši grupė apima funkcijas, susijusias su mokėjimais ir užsakymo baigimu puslapyje **Pardavimo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="b8675-114">**Order completion** – This group includes features that are related to payments and order completion on the **Sales order** page.</span></span>
-   <span data-ttu-id="b8675-115">**Tiesioginis pardavimas** – ši grupė apima funkcijas, susijusias su šaltinio kodais, scenarijais ir katalogų užklausomis.</span><span class="sxs-lookup"><span data-stu-id="b8675-115">**Directed selling** – This group includes features that are related to source codes, scripts, and catalog requests.</span></span>

<span data-ttu-id="b8675-116">Įjungus šias funkcijas skambučių centro parametruose, puslapyje **Pardavimo užsakymas** jas gali pasiekti su skambučių centru susieti vartotojai.</span><span class="sxs-lookup"><span data-stu-id="b8675-116">After you enable these features in the call center settings, they are available on the **Sales order** page to users who are associated with the call center.</span></span> <span data-ttu-id="b8675-117">Norint naudoti daugumą šių funkcijų, reikia atlikti papildomą nustatymą.</span><span class="sxs-lookup"><span data-stu-id="b8675-117">Most of these features require additional setup before they can be used.</span></span> <span data-ttu-id="b8675-118">Kad vartotojai galėtų kurti skambučių centro užsakymus, turite pridėti tuos vartotojus kaip skambučių centro vartotojus.</span><span class="sxs-lookup"><span data-stu-id="b8675-118">Before users can create call center orders, you must add those users to the call center as call center users.</span></span> <span data-ttu-id="b8675-119">Šis veiksmas užtikrina skambučių centro kanalui būdingą konfigūraciją ir funkcijas.</span><span class="sxs-lookup"><span data-stu-id="b8675-119">This step enables the call center channel-specific configuration and functionality.</span></span> <span data-ttu-id="b8675-120">Štai keletas funkcijų, kurios tampa pasiekiamos, pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="b8675-120">Here are some examples of the functionality that becomes available:</span></span>

-   <span data-ttu-id="b8675-121">Interaktyviojo pardavimo funkcija teikia pardavimo telefonu scenarijų ir produkto vaizdų, kurie padeda pardavimo klerkams ir teikia jiems gaires priimant užsakymus, konfigūracijos galimybes.</span><span class="sxs-lookup"><span data-stu-id="b8675-121">Guided selling provides configuration options for tele-sales scripts and product images to help and guide sales clerks while they take orders.</span></span>
-   <span data-ttu-id="b8675-122">Užsakymų negalima baigti, kol pardavimo klerkai neužfiksavo bent vieno mokėjimo metodo.</span><span class="sxs-lookup"><span data-stu-id="b8675-122">Orders can't be completed until sales clerks have captured at least one payment method.</span></span>
-   <span data-ttu-id="b8675-123">Papildomo pardavimo ir kryžminio pardavimo taisykles galima konfigūruoti, kad pardavimo klerkai būtų raginami reklamuoti klientui konkrečius produktus.</span><span class="sxs-lookup"><span data-stu-id="b8675-123">Upsell and cross-sell rules can be configured to prompt sales clerks to promote specific products to the customer.</span></span>
-   <span data-ttu-id="b8675-124">Pardavimo tarnautojai gali užfiksuoti katalogo, iš kurio klientas užsako, šaltinio kodą.</span><span class="sxs-lookup"><span data-stu-id="b8675-124">Sales clerks can capture the source code for the catalog that a customer is ordering from.</span></span>
-   <span data-ttu-id="b8675-125">Pardavimo klerkai gali prie užsakymo pridėti mažmenininko kuponų.</span><span class="sxs-lookup"><span data-stu-id="b8675-125">Sales clerks can add a retailer's coupons to the order.</span></span>
-   <span data-ttu-id="b8675-126">Pardavimo klerkai gali parduoti tęstinumo programas.</span><span class="sxs-lookup"><span data-stu-id="b8675-126">Sales clerks can sell continuity programs.</span></span>
-   <span data-ttu-id="b8675-127">Užsakymus galima sulaikyti rankiniu būdu arba automatiškai norint nurodyti, kad užsakymą bus galima apdoroti tik atlikus papildomą tyrimą.</span><span class="sxs-lookup"><span data-stu-id="b8675-127">Orders can be put on hold manually or automatically, to indicate that additional investigation is required before the order can be processed.</span></span>





