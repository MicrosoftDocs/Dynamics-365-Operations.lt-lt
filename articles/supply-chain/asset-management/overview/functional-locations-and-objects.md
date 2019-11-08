---
title: Funkcinės vietos ir turtas
description: Šioje temoje aprašomos funkcinės vietos ir turtas modulyje Turto valdymas. Turto valdymas yra išplėstinis modulis, skirtas turtui ir priežiūros užduotims valdyti programoje „Dynamics 365 Supply Chain Management“.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3a42d36fd137aa780886276a4235f1b8f3a3680
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653352"
---
# <a name="functional-locations-and-assets"></a><span data-ttu-id="6e737-104">Funkcinės vietos ir turtas</span><span class="sxs-lookup"><span data-stu-id="6e737-104">Functional locations and assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6e737-105">Šioje temoje aprašomos funkcinės vietos ir turtas modulyje Turto valdymas.</span><span class="sxs-lookup"><span data-stu-id="6e737-105">This topic describes functional locations and assets in Asset Management.</span></span> <span data-ttu-id="6e737-106">Turto valdymas yra išplėstinis modulis, skirtas turtui ir priežiūros užduotims valdyti programoje „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="6e737-106">Asset Management is an advanced module for managing assets and maintenance jobs in Dynamics 365 Supply Chain Management.</span></span>

## <a name="overview"></a><span data-ttu-id="6e737-107">Apžvalga</span><span class="sxs-lookup"><span data-stu-id="6e737-107">Overview</span></span>

<span data-ttu-id="6e737-108">Turto valdymas sklandžiai integruojamas su keletu kitų „Finance and Operations“ programų modulių.</span><span class="sxs-lookup"><span data-stu-id="6e737-108">Asset Management is integrated seamlessly with several modules with other Finance and Operations apps.</span></span> <span data-ttu-id="6e737-109">Toliau pateikiamoje iliustracijoje pavaizduotos sąsajos su kitais moduliais.</span><span class="sxs-lookup"><span data-stu-id="6e737-109">The following illustration shows the interfaces with other modules.</span></span>

![Diagrama, rodanti, kaip turto valdymas siejasi su kitais moduliais](media/01-overview-image.png)

<span data-ttu-id="6e737-111">Turto valdymas leidžia efektyviai valdyti ir atlikti visas užduotis, susijusias su daugelio tipų įrangos valdymu ir aptarnavimu jūsų įmonėje.</span><span class="sxs-lookup"><span data-stu-id="6e737-111">Asset Management lets you efficiently manage and perform all tasks that are related to managing and servicing many types of equipment in your company.</span></span> <span data-ttu-id="6e737-112">Ši įranga apima mašinas, gamybos įrangą ir transporto priemones.</span><span class="sxs-lookup"><span data-stu-id="6e737-112">This equipment includes machines, production equipment, and vehicles.</span></span> <span data-ttu-id="6e737-113">Modulyje Turto valdymas taip pat palaikomi sprendimai daugelyje pramonės šakų.</span><span class="sxs-lookup"><span data-stu-id="6e737-113">Asset Management also supports solutions across numerous industries.</span></span>

<span data-ttu-id="6e737-114">Toliau esančioje iliustracijoje pateikiama modulio Turto valdymas pagrindinių funkcijų apžvalga.</span><span class="sxs-lookup"><span data-stu-id="6e737-114">The following illustration shows an overview of the main functionality that is covered by Asset Management.</span></span>

![Diagrama, rodanti pagrindines turto valdymo funkcijas](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a><span data-ttu-id="6e737-116">Funkcinės vietos ir turtas</span><span class="sxs-lookup"><span data-stu-id="6e737-116">Functional locations and assets</span></span>

<span data-ttu-id="6e737-117">Funkcinės vietos naudojamos vietose esančiam turtui valdyti.</span><span class="sxs-lookup"><span data-stu-id="6e737-117">Functional locations are used to manage assets on locations.</span></span> <span data-ttu-id="6e737-118">Šis valdymas apima turto išlaidų sekimą funkcinėse vietose.</span><span class="sxs-lookup"><span data-stu-id="6e737-118">This management includes tracking of asset costs on functional locations.</span></span> <span data-ttu-id="6e737-119">Funkcinių vietų struktūra yra hierarchinė, o vietose gali būti antrinių vietų.</span><span class="sxs-lookup"><span data-stu-id="6e737-119">Functional locations are structured hierarchically, and locations can have sub-locations.</span></span> <span data-ttu-id="6e737-120">Funkcinių vietų struktūra yra statinė.</span><span class="sxs-lookup"><span data-stu-id="6e737-120">The structure of functional locations is static.</span></span> <span data-ttu-id="6e737-121">Kitaip tariant, negalima keisti vietų buvimo vietų.</span><span class="sxs-lookup"><span data-stu-id="6e737-121">In other words, locations can't change place.</span></span> <span data-ttu-id="6e737-122">Turtas gali būti įdiegtas funkcinėse vietose ir, jei reikia, vėliau gali būti įdiegtas kitose funkcinėse vietose.</span><span class="sxs-lookup"><span data-stu-id="6e737-122">Assets can be installed on functional locations and, as required, can be installed on other functional locations later.</span></span>

<span data-ttu-id="6e737-123">Turto išlaidos visada priklauso nuo turto vietos.</span><span class="sxs-lookup"><span data-stu-id="6e737-123">Asset costs always follow the location of the asset.</span></span> <span data-ttu-id="6e737-124">Kitaip tariant, jei įdiegiate turtą naujoje funkcinėje vietoje, turtas automatiškai naudoja finansines dimensijas, susijusias su nauja funkcine vieta.</span><span class="sxs-lookup"><span data-stu-id="6e737-124">In other words, if you install an asset on a new functional location, the asset automatically uses the financial dimensions that are related to the new functional location.</span></span> <span data-ttu-id="6e737-125">Todėl turto išlaidos visada yra susijusios su funkcine vieta, kurioje turtas šiuo metu yra įdiegtas.</span><span class="sxs-lookup"><span data-stu-id="6e737-125">Therefore, asset costs are always related to the functional location that the asset is  currently installed on.</span></span> <span data-ttu-id="6e737-126">Toks automatinis finansinių dimensijų tvarkymas padeda užtikrinti visišką išlaidų sekimą, kai jūsų įmonė kontroliuoja projektus ir teikia ataskaitas apie funkcines vietas.</span><span class="sxs-lookup"><span data-stu-id="6e737-126">This automatic handling of financial dimensions helps guarantee complete tracking of costs when your company does project controlling and reporting on functional locations.</span></span>

<span data-ttu-id="6e737-127">Funkcinių vietų hierarchijos kūrimo būdas priklauso nuo jūsų įmonės reikalavimų dėl vidinės įrangos priežiūros arba klientų įrangos aptarnavimo.</span><span class="sxs-lookup"><span data-stu-id="6e737-127">The way that you build your hierarchy of functional locations depends on your company's requirements for maintaining internal equipment or servicing customer equipment.</span></span> <span data-ttu-id="6e737-128">Toliau pateikiamame paveikslėlyje pavaizduotas geografinėmis vietovėmis pagrįstų funkcinių vietų pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="6e737-128">The following figure shows an example of functional locations that are based on geographical locations.</span></span>

![Diagrama, rodanti geografinėmis vietovėmis pagrįstas funkcines vietas](media/03-overview-image.png)

<span data-ttu-id="6e737-130">Toliau pateikiamame paveikslėlyje pavaizduotas klientais pagrįstų funkcinių vietų pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="6e737-130">The following figure shows an example of functional locations that are based on customers.</span></span>

![Diagrama, rodanti klientais pagrįstas funkcines vietas](media/04-overview-image.png)
