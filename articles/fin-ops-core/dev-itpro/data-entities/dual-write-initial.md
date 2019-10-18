---
title: Pradinio „Finance and Operations“ programų ir „Common Data Service“ sinchronizavimo vykdymo tvarka
description: Šioje temoje nurodoma sinchronizavimo tvarka, kurią turite sekti, kad sukurtumėte pradinius duomenis.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 3110cb809558d168e9d97f640701b249caf73f6c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184513"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="6d3ae-103">Pradinio „Finance and Operations“ programų ir „Common Data Service“ sinchronizavimo vykdymo tvarka</span><span class="sxs-lookup"><span data-stu-id="6d3ae-103">Execution order for initial synchronization of Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="6d3ae-104">Prieš pradėdami naudoti duomenų integraciją, turite sukurti pradinius duomenis, reikalingus klientams, tiekėjams ir kontaktams.</span><span class="sxs-lookup"><span data-stu-id="6d3ae-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="6d3ae-105">Pavyzdžiui, norite sukurti naują elementą **Tiekėjų grupė** ir nustatyti jo **Mokėjimo sąlygos** reikšmę į **„Net30“**.</span><span class="sxs-lookup"><span data-stu-id="6d3ae-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="6d3ae-106">Tokiu atveju, prieš bandydami sukurti elementą **Tiekėjų grupė**, turite įsitikinti, kad **„Net30“** yra ir programoje, ir „Common Data Service”</span><span class="sxs-lookup"><span data-stu-id="6d3ae-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both the application and Common Data Service.</span></span> <span data-ttu-id="6d3ae-107">(Ateityje „Microsoft“ išleis dvigubo rašymo platformos funkciją, vadinamą pradiniu sinchronizavimu. Ši funkcija atliks vienkartinį duomenų sinchronizavimą tarp programos ir „Common Data Service“ kaip dvigubo rašymo sąrankos dalis.)</span><span class="sxs-lookup"><span data-stu-id="6d3ae-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between the application and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="6d3ae-108">„Microsoft“ išleidžia dvigubo rašymo schemą visiems nuorodos duomenims, įskaitant **Mokėjimo sąlygos** (mokėjimo sąlygas).</span><span class="sxs-lookup"><span data-stu-id="6d3ae-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="6d3ae-109">Jei jau turite pradinius duomenis vienoje sistemoje, mažas įrašo naujinimas gali sukelti įraše dvigubą rašymą.</span><span class="sxs-lookup"><span data-stu-id="6d3ae-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="6d3ae-110">Turite sekti šią pirmumo tvarką ir įsitikinti, kad pradiniai duomenys prieinami programoje ir „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="6d3ae-110">You must follow the following order of precedence and make sure that the initial data is available in the application and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="6d3ae-111">Tiekėjas</span><span class="sxs-lookup"><span data-stu-id="6d3ae-111">Vendor</span></span>

<span data-ttu-id="6d3ae-112">Objekto **Tiekėjas** vykdymo tvarka:</span><span class="sxs-lookup"><span data-stu-id="6d3ae-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="6d3ae-113">Tiekėjų grupė</span><span class="sxs-lookup"><span data-stu-id="6d3ae-113">Vendor group</span></span>

    1. <span data-ttu-id="6d3ae-114">Mokėjimo sąlygos</span><span class="sxs-lookup"><span data-stu-id="6d3ae-114">Terms of payment</span></span>

        1. <span data-ttu-id="6d3ae-115">Mokėjimo diena ir eilutės</span><span class="sxs-lookup"><span data-stu-id="6d3ae-115">Payment day and lines</span></span>
        2. <span data-ttu-id="6d3ae-116">Mokėjimo grafikas</span><span class="sxs-lookup"><span data-stu-id="6d3ae-116">Payment schedule</span></span>

2. <span data-ttu-id="6d3ae-117">Tiekėjo mokėjimo būdas</span><span class="sxs-lookup"><span data-stu-id="6d3ae-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="6d3ae-118">Kliento organizacija</span><span class="sxs-lookup"><span data-stu-id="6d3ae-118">Customer (Organization)</span></span>

<span data-ttu-id="6d3ae-119">Objekto **Klientas** vykdymo tvarka:</span><span class="sxs-lookup"><span data-stu-id="6d3ae-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="6d3ae-120">Klientų grupė</span><span class="sxs-lookup"><span data-stu-id="6d3ae-120">Customer group</span></span>

    1. <span data-ttu-id="6d3ae-121">Mokėjimo sąlygos</span><span class="sxs-lookup"><span data-stu-id="6d3ae-121">Terms of payment</span></span>

        1. <span data-ttu-id="6d3ae-122">Mokėjimo diena ir eilutės</span><span class="sxs-lookup"><span data-stu-id="6d3ae-122">Payment day and lines</span></span>
        2. <span data-ttu-id="6d3ae-123">Mokėjimas</span><span class="sxs-lookup"><span data-stu-id="6d3ae-123">Payment</span></span> 

2. <span data-ttu-id="6d3ae-124">Kliento mokėjimo būdas</span><span class="sxs-lookup"><span data-stu-id="6d3ae-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="6d3ae-125">Kontaktinis asmuo</span><span class="sxs-lookup"><span data-stu-id="6d3ae-125">Contact (Person)</span></span>

<span data-ttu-id="6d3ae-126">Objekto **Kontaktas** vykdymo tvarka:</span><span class="sxs-lookup"><span data-stu-id="6d3ae-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="6d3ae-127">Klientas</span><span class="sxs-lookup"><span data-stu-id="6d3ae-127">Customer</span></span>
2. <span data-ttu-id="6d3ae-128">Tiekėjas</span><span class="sxs-lookup"><span data-stu-id="6d3ae-128">Vendor</span></span>
