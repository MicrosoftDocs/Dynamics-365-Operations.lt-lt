---
title: Vykdymo tvarka, skirta pradiniam „Finance and Operations“ ir „Common Data Service“ sinchronizavimui.
description: Šioje temoje nurodomas sinchronizavimas, kurį reikia atlikti norint sukurti pradinius duomenis.
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
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797303"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="df2f1-103">Vykdymo tvarka, skirta pradiniam „Finance and Operations“ ir „Common Data Service“ sinchronizavimui.</span><span class="sxs-lookup"><span data-stu-id="df2f1-103">Execution order for initial sychronization of Finance and Operations and Common Data Service</span></span>

<span data-ttu-id="df2f1-104">Prieš pradėdami naudoti duomenų integravimą, turite sukurti pradinius duomenis, reikalingus pirkėjams, tiekėjams ir kontaktams.</span><span class="sxs-lookup"><span data-stu-id="df2f1-104">Before you use data integration, you must create the initial data required for customers, vendors and contacts.</span></span> <span data-ttu-id="df2f1-105">Pavyzdžiui, jei norite sukurti naują **„Tiekėjo grupė“** prekę ir nustatyti jos **„Mokėjimo sąlygos“** kaip **„Net30“**, prieš bandydami sukurti **„Tiekėjo grupė“** prekę, turite įsitikinti, kad **„Net30“** egzistuoja tiek „Finance and Operations“ ir „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="df2f1-105">For example, if you want to create a new **Vendor group** item and set its **Terms of Payment** as **Net30**, then before you attempt to create the **Vendor group** item you need to make sure that **Net30** exists in both Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="df2f1-106">(Ateityje išleisime dvigubo rašymo platformos funkciją, vadinamą **Initial Sync**. Tai atliks vienkartinį duomenų sinchronizavimą tarp „Finance and Operations“ ir Common Data Service kaip dvigubo rašymo sąrankos dalis.)</span><span class="sxs-lookup"><span data-stu-id="df2f1-106">(In the future, we will release a  dual-write platform functionality called **Initial Sync**. It will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

<span data-ttu-id="df2f1-107">Patarimai: Patarimai: mes išleisime dvigubo rašymo žemėlapį visiems nuorodos duomenis, įskaitant **„Mokėjimo sąlygas“** (mokėjimo sąlygos).</span><span class="sxs-lookup"><span data-stu-id="df2f1-107">Tips: We are releasing a dual-write map for all reference data including **Terms of Payment** (Payment Terms).</span></span> <span data-ttu-id="df2f1-108">Jei jau turite pradinius duomenis vienoje sistemoje, mažas įrašo naujinimas gali sukelti įraše dvigubą rašymą.</span><span class="sxs-lookup"><span data-stu-id="df2f1-108">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span> 

<span data-ttu-id="df2f1-109">Turite vadovautis toliau pateikiama pirmumo tvarka ir užtikrinti, kad pradiniai duomenys būtų pasiekiami ir „Finance and Operations" ir „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="df2f1-109">You must follow the following order of precedence and make sure that the initial data is available on both Finance and Operations and Common Data Service.</span></span>   

## <a name="vendor"></a><span data-ttu-id="df2f1-110">Tiekėjas</span><span class="sxs-lookup"><span data-stu-id="df2f1-110">Vendor</span></span>

<span data-ttu-id="df2f1-111">Tiekėjo vykdymo tvarka:</span><span class="sxs-lookup"><span data-stu-id="df2f1-111">The order of execution for Vendor is:</span></span>

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a><span data-ttu-id="df2f1-112">Kliento organizacija</span><span class="sxs-lookup"><span data-stu-id="df2f1-112">Customer (Organization)</span></span>

<span data-ttu-id="df2f1-113">Kliento vykdymo tvarka:</span><span class="sxs-lookup"><span data-stu-id="df2f1-113">The order of execution for Customer is:</span></span>

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a><span data-ttu-id="df2f1-114">Kontaktinis asmuo</span><span class="sxs-lookup"><span data-stu-id="df2f1-114">Contact (Person)</span></span>

<span data-ttu-id="df2f1-115">Kontakto vykdymo tvarka:</span><span class="sxs-lookup"><span data-stu-id="df2f1-115">The order of execution for Contact is:</span></span>

```
Customer
Vendor               
```
