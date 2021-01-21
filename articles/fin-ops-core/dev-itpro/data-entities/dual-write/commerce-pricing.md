---
title: „Dynamics 365 Commerce“ kainodaros mechanizmo naudojimas su „Dynamics 365 Sales“
description: Šioje temoje aprašoma, kaip naudoti „Microsoft Dynamics 365 Commerce” kainodaros mechanizmą, norint kurti pardavimo pasiūlymus programoje „Dynamics 365 Sales”.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: fad5c21d75db62b85efe803f1667dd3f9164a5fc
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594923"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a><span data-ttu-id="52ad5-103">„Dynamics 365 Commerce“ kainodaros mechanizmo naudojimas su „Dynamics 365 Sales“</span><span class="sxs-lookup"><span data-stu-id="52ad5-103">Use the Dynamics 365 Commerce pricing engine with Dynamics 365 Sales</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="52ad5-104">Šioje temoje aprašoma, kaip naudoti „Microsoft Dynamics 365 Commerce” kainodaros mechanizmą, norint kurti pardavimo pasiūlymus programoje „Dynamics 365 Sales”.</span><span class="sxs-lookup"><span data-stu-id="52ad5-104">This topic describes how to use the Microsoft Dynamics 365 Commerce pricing engine to create sales quotations in Dynamics 365 Sales.</span></span>

<span data-ttu-id="52ad5-105">„Dynamics 365 Commerce“ kainodaros mechanizmas palaiko daugumą įmonių ir vartotojų (B2C) kainodaros scenarijų, pvz., parduotuvės lygio kainodarą, kainodarą pagal priskyrimą ir lojalumą, prekių rinkinio nuolaidas, kiekio nuolaidas ir ribines nuolaidas.</span><span class="sxs-lookup"><span data-stu-id="52ad5-105">The Dynamics 365 Commerce pricing engine supports most business-to-consumer (B2C) pricing scenarios, such as store-level pricing, affiliation-based and loyalty-based pricing, mix-and-match discounts, quantity discounts, and threshold discounts.</span></span> <span data-ttu-id="52ad5-106">Kainodaros mechanizmas naudoja sudėtingas taisykles nustatyti geriausią konkretaus pasiūlymo ar užsakymo kainą.</span><span class="sxs-lookup"><span data-stu-id="52ad5-106">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span>

<span data-ttu-id="52ad5-107">Kai naudojate [dvigubą rašymą](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), turite tris parinktis savo kainodaros poreikiams.</span><span class="sxs-lookup"><span data-stu-id="52ad5-107">When you use [dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), you have three options for your pricing needs.</span></span> <span data-ttu-id="52ad5-108">Galite naudoti statinę kainodarą, gaunamą iš „Dynamics 365 Sales“ kainoraščio, „Dynamics 365 Supply Chain Management“ kainodaros mechanizmą arba „Dynamics 365 Commerce“ kainodaros mechanizmą.</span><span class="sxs-lookup"><span data-stu-id="52ad5-108">You can use the static pricing that comes from the price list in Dynamics 365 Sales, the pricing engine in Dynamics 365 Supply Chain Management, or the pricing engine in Dynamics 365 Commerce.</span></span> <span data-ttu-id="52ad5-109">Iš šių parinkčių „Commerce“ kainodaros mechanizmas geriausiai atitinka B2C scenarijus.</span><span class="sxs-lookup"><span data-stu-id="52ad5-109">Among these options, the Commerce pricing engine is best suited to B2C scenarios.</span></span>

## <a name="use-the-commerce-pricing-engine-in-sales"></a><span data-ttu-id="52ad5-110">„Commerce“ kainodaros mechanizmo naudojimas programoje „Sales“</span><span class="sxs-lookup"><span data-stu-id="52ad5-110">Use the Commerce pricing engine in Sales</span></span>

> [!NOTE]
> <span data-ttu-id="52ad5-111">Šiuo metu „Commerce“ kainodaros mechanizmą galima naudoti tik pasiūlymams kurti programoje „Sales“.</span><span class="sxs-lookup"><span data-stu-id="52ad5-111">Currently, the Commerce pricing engine can be used only for quotation creation in the Sales.</span></span> <span data-ttu-id="52ad5-112">„Sales“ užsakymų integravimo su „Commerce“ kainodaros mechanizmu galimybės dar nėra.</span><span class="sxs-lookup"><span data-stu-id="52ad5-112">Sales order integration with the Commerce pricing engine isn't yet available.</span></span>

<span data-ttu-id="52ad5-113">Kai vartotojai pradeda pasiūlymą programoje „Sales“, dvigubo rašymo sistema nukopijuoja pasiūlymo informaciją į „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="52ad5-113">When users initiate a quotation in Sales, the dual-write framework copies the quotation details to Commerce.</span></span> <span data-ttu-id="52ad5-114">Bet kokie esamų pasiūlymo eilučių pakeitimai arba naujai pridėtos „Sales“ pasiūlymo eilutės nukopijuojamos į „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="52ad5-114">Any changes to existing quotation lines or any newly added quotation lines in Sales are copied to Commerce.</span></span> <span data-ttu-id="52ad5-115">Kai vartotojai nori naudoti „Commerce“ kainodaros mechanizmą pasiūlymui įkainoti, jie gali pasirinkti **Įkainoti pasiūlymą** ir atnaujinti pasiūlymo kainas pagal „Commerce“ kainodaros mechanizmą.</span><span class="sxs-lookup"><span data-stu-id="52ad5-115">When users want to use the Commerce pricing engine to price the quotation, they can select **Price quote** to update the prices of the quotation, based on the Commerce pricing engine.</span></span> <span data-ttu-id="52ad5-116">Kainos tada automatiškai atnaujinamos ir programoje „Sales“, ir „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="52ad5-116">Prices are then automatically updated in both Sales and Commerce.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="52ad5-117">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="52ad5-117">Prerequisites</span></span>

- <span data-ttu-id="52ad5-118">Kad galėtumėte naudoti „Commerce“ kainodaros mechanizmą programoje „Sales“, turite atlikti veiksmus, nurodytus dokumente iš [Potencialių klientų pavertimas grynaisiais pinigais naudojant dvigubo rašymo funkciją](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).</span><span class="sxs-lookup"><span data-stu-id="52ad5-118">Before you can use the Commerce pricing engine in Sales, you must follow the steps in [Prospect-to-cash in dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).</span></span>
- <span data-ttu-id="52ad5-119">Turite išjungti prekybos sutarties vertinimą, skirtą neautomatinei įvesčiai, atlikdami tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="52ad5-119">You must turn off trade agreement evaluation for manual entry by following these steps:</span></span>

    1. <span data-ttu-id="52ad5-120">Savo „Commerce“ aplinkoje eikite į **Gautinos sumos \> Nustatymai \> Gautinų sumų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="52ad5-120">In your Commerce environment, go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    1. <span data-ttu-id="52ad5-121">Skirtuko **Kainos**, „FastTab“ **Prekybos sutarties vertinimas** išvalykite žymės langelį **Neautomatinis įvedimas**.</span><span class="sxs-lookup"><span data-stu-id="52ad5-121">On the **Prices** tab, on the **Trade agreement evaluation** FastTab, clear the **Manual entry** check box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="52ad5-122">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="52ad5-122">Additional resources</span></span>

[<span data-ttu-id="52ad5-123">Potencialių klientų pavertimas grynaisiais pinigais dvigubo rašymo funkcijoje</span><span class="sxs-lookup"><span data-stu-id="52ad5-123">Prospect-to-cash in dual-write</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)