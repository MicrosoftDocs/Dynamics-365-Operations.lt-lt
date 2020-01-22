---
title: Perjungti iš vieno tiekėjo dizaino į kitą
description: Šioje temoje aprašoma, kaip perjungti tiekėjo duomenų integravimą tarp „Finance and Operations“ programų ir „Common Data Service“.
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
ms.openlocfilehash: 204d788e72e79e7acf744d24cbeacb0f9b47da7d
ms.sourcegitcommit: 3306e451f04df01c51d8d332306b135d8ae1e254
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/09/2019
ms.locfileid: "2902730"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="9a55f-103">Perjungti iš vieno tiekėjo dizaino į kitą</span><span class="sxs-lookup"><span data-stu-id="9a55f-103">Switch between vendor designs</span></span>

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="9a55f-104">Tiekėjo duomenų srautas</span><span class="sxs-lookup"><span data-stu-id="9a55f-104">Vendor data flow</span></span> 

<span data-ttu-id="9a55f-105">Jei tiekėjams valdyti naudojate kitas „Dynamics 365” programas ir norite atskirti tiekėjo informaciją nuo klientų, naudokite šį bazinį tiekėjo dizainą.</span><span class="sxs-lookup"><span data-stu-id="9a55f-105">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![Bazinis tiekėjo srautas](media/dual-write-vendor-data-flow.png)
 
<span data-ttu-id="9a55f-107">Jei tiekėjams valdyti naudojate kitas „Dynamics 365” programas ir norite toliau naudoti objektą **Klientas** tiekėjo informacijai saugoti, naudokite šį išplėstąjį tiekėjo dizainą.</span><span class="sxs-lookup"><span data-stu-id="9a55f-107">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="9a55f-108">Taikant šį dizainą išplėstinė tiekėjo informacija, pvz., tiekėjo sulaikymo būsena ir profilis, saugoma „Common Data Service“ **tiekėjų** objekte.</span><span class="sxs-lookup"><span data-stu-id="9a55f-108">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![Išplėstinis tiekėjo srautas](media/dual-write-vendor-detail.jpg)
 
<span data-ttu-id="9a55f-110">Norėdami naudoti išplėstinį tiekėjo dizainą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9a55f-110">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="9a55f-111">**SupplyChainCommon** sprendimo pakete pateikiami darbo eigos procesų šablonai, kaip parodyta tolesniame vaizde.</span><span class="sxs-lookup"><span data-stu-id="9a55f-111">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="9a55f-112">![Darbo eigos procesų šablonai](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="9a55f-112">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="9a55f-113">Naujus darbo eigos procesus galite kurti naudodami darbo eigos procesų šablonus, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="9a55f-113">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="9a55f-114">Naudodami darbo eigos procesą **Kurti tiekėjus kliento objekte**, sukurkite naują objekto **Tiekėjas** darbo eigos procesą ir spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9a55f-114">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="9a55f-115">Šia darbo eiga tvarkomas objekto **Klientas** tiekėjų kūrimo scenarijus.</span><span class="sxs-lookup"><span data-stu-id="9a55f-115">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9a55f-116">![Kurti tiekėjus kliento objekte](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="9a55f-116">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="9a55f-117">Naudodami darbo eigos procesą **Atnaujinti klientų objektą**, sukurkite naują objekto **Tiekėjas** darbo eigos procesą ir spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9a55f-117">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="9a55f-118">Šia darbo eiga tvarkomas objekto **Klientas** tiekėjų naujinimo scenarijus.</span><span class="sxs-lookup"><span data-stu-id="9a55f-118">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9a55f-119">![Atnaujinti klientų objektą](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="9a55f-119">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="9a55f-120">Sukurkite naujų darbo eigos procesų pagal objekte **Klientai** sukurtus šablonus.</span><span class="sxs-lookup"><span data-stu-id="9a55f-120">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9a55f-121">![Kurti tiekėjus tiekėjų objekte](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="9a55f-121">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="9a55f-122">![Atnaujinti tiekėjų objektą](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="9a55f-122">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="9a55f-123">Darbo eigas pagal poreikius galite konfigūruoti kaip realiuoju laiku vykdomas arba fonines darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="9a55f-123">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9a55f-124">![Konvertavimas į foninę darbo eigą](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="9a55f-124">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="9a55f-125">Norėdami pradėti tiekėjų informaciją saugoti naudojant objektą **Klientas**, suaktyvinkite darbo eigas, kurias sukūrėte objektuose **Klientas** ir **Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="9a55f-125">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the **Account** entity for storing vendor information.</span></span> 
 
