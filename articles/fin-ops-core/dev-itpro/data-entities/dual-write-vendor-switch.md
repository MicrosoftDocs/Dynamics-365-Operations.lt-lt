---
title: Vieno tiekėjo dizaino perjungimas į kitą
description: ''
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
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
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772369"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="9ce8a-102">Vieno tiekėjo dizaino perjungimas į kitą</span><span class="sxs-lookup"><span data-stu-id="9ce8a-102">Switch between vendor designs</span></span>

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="9ce8a-103">Tiekėjo duomenų srautas</span><span class="sxs-lookup"><span data-stu-id="9ce8a-103">Vendor data flow</span></span> 

<span data-ttu-id="9ce8a-104">Jei tiekėjams valdyti naudojate kitas „Dynamics 365” programas ir norite atskirti tiekėjo informaciją nuo klientų, naudokite šį bazinį tiekėjo dizainą.</span><span class="sxs-lookup"><span data-stu-id="9ce8a-104">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![Bazinis tiekėjo srautas](media/dual-write-switch-1.png)
 
<span data-ttu-id="9ce8a-106">Jei tiekėjams valdyti naudojate kitas „Dynamics 365” programas ir norite toliau naudoti objektą **Klientas** tiekėjo informacijai saugoti, naudokite šį išplėstąjį tiekėjo dizainą.</span><span class="sxs-lookup"><span data-stu-id="9ce8a-106">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="9ce8a-107">Taikant šį dizainą išplėstinė tiekėjo informacija, pvz., tiekėjo sulaikymo būsena ir profilis, saugoma „Common Data Service“ **tiekėjų** objekte.</span><span class="sxs-lookup"><span data-stu-id="9ce8a-107">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![Išplėstinis tiekėjo srautas](media/dual-write-switch-2.png)
 
<span data-ttu-id="9ce8a-109">Norėdami naudoti išplėstinį tiekėjo dizainą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9ce8a-109">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="9ce8a-110">**SupplyChainCommon** sprendimo pakete pateikiami darbo eigos procesų šablonai, kaip parodyta tolesniame vaizde.</span><span class="sxs-lookup"><span data-stu-id="9ce8a-110">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="9ce8a-111">![Darbo eigos procesų šablonai](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="9ce8a-111">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="9ce8a-112">Naujus darbo eigos procesus galite kurti naudodami darbo eigos procesų šablonus, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="9ce8a-112">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="9ce8a-113">Naudodami darbo eigos procesą **Kurti tiekėjus kliento objekte**, sukurkite naują objekto **Tiekėjas** darbo eigos procesą ir spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9ce8a-113">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="9ce8a-114">Šia darbo eiga tvarkomas objekto **Klientas** tiekėjų kūrimo scenarijus.</span><span class="sxs-lookup"><span data-stu-id="9ce8a-114">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9ce8a-115">![Kurti tiekėjus kliento objekte](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="9ce8a-115">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="9ce8a-116">Naudodami darbo eigos procesą **Atnaujinti klientų objektą**, sukurkite naują objekto **Tiekėjas** darbo eigos procesą ir spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9ce8a-116">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="9ce8a-117">Šia darbo eiga tvarkomas objekto **Klientas** tiekėjų naujinimo scenarijus.</span><span class="sxs-lookup"><span data-stu-id="9ce8a-117">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9ce8a-118">![Atnaujinti klientų objektą](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="9ce8a-118">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="9ce8a-119">Sukurkite naujų darbo eigos procesų pagal objekte **Klientai** sukurtus šablonus.</span><span class="sxs-lookup"><span data-stu-id="9ce8a-119">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9ce8a-120">![Kurti tiekėjus tiekėjų objekte](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="9ce8a-120">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="9ce8a-121">![Atnaujinti tiekėjų objektą](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="9ce8a-121">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="9ce8a-122">Darbo eigas pagal poreikius galite konfigūruoti kaip realiuoju laiku vykdomas arba fonines darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="9ce8a-122">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9ce8a-123">![Konvertavimas į foninę darbo eigą](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="9ce8a-123">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="9ce8a-124">Norėdami pradėti tiekėjų informaciją saugoti naudojant „Customer Engagement“ objektą **Klientas**, suaktyvinkite darbo eigas, kurias sukūrėte objektuose **Klientas** ir **Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="9ce8a-124">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the Customer Engagement **Account** entity for storing vendor information.</span></span> 
 
