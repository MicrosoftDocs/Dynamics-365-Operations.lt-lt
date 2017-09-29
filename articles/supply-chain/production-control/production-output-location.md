---
title: "Gamybos išeigos vieta"
description: "Šioje temoje aprašoma hierarchija, naudojama gamybos išeigos vietai nustatyti."
author: johanhoffmann
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: e53c8e96579dba3b47bef0c00e55b8fa786fc55c
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---

# <a name="production-output-location"></a><span data-ttu-id="e72cb-103">Gamybos išeigos vieta</span><span class="sxs-lookup"><span data-stu-id="e72cb-103">Production output location</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e72cb-104">Šioje temoje aprašoma hierarchija, naudojama gamybos išeigos vietai nustatyti.</span><span class="sxs-lookup"><span data-stu-id="e72cb-104">This topic describes the hierarchy that is used to identify the production output location.</span></span>

<span data-ttu-id="e72cb-105">Gamybos išeigos vieta yra vieta, kurioje baigta prekė saugoma ją pagaminus.</span><span class="sxs-lookup"><span data-stu-id="e72cb-105">The production output location is the location where a finished good is first stored after it's produced.</span></span> <span data-ttu-id="e72cb-106">Paprastai ši vieta yra netoli baigtos prekės gamybos proceso vietos.</span><span class="sxs-lookup"><span data-stu-id="e72cb-106">Usually, this location is close to the production process that produces the finished good.</span></span> <span data-ttu-id="e72cb-107">Gamybos išeigos vieta naudojama kaip tarpinė medžiagos saugykla prieš ją perkeliant į siuntimo zoną, saugojimo vietą, proceso pabaigos gamybos proceso gamybos įvesties vietą ir t. t.</span><span class="sxs-lookup"><span data-stu-id="e72cb-107">The production output location is used as intermediate storage for the material before it's moved on to the shipment area, a storage location, a production input location for a downstream production process, and so on.</span></span> 

<span data-ttu-id="e72cb-108">Numatytoji gamybos išeigos vieta nustatoma, kai baigtos prekės užregistruojamos gamybos užsakyme arba paketiniame užsakyme.</span><span class="sxs-lookup"><span data-stu-id="e72cb-108">A default production output location is set when finished goods are reported on a production order or batch order.</span></span> <span data-ttu-id="e72cb-109">Toliau nurodyta hierarchija naudojama šiai išeigos vietai nustatyti.</span><span class="sxs-lookup"><span data-stu-id="e72cb-109">The following hierarchy is used to identify this output location:</span></span>

1. <span data-ttu-id="e72cb-110">Naudokite išeigos vietą, nurodytą gamybos užsakymo arba paketo užsakymo antraštėje.</span><span class="sxs-lookup"><span data-stu-id="e72cb-110">Use the output location that is defined on the production order or batch order header.</span></span>
2. <span data-ttu-id="e72cb-111">Jei ten vieta nenurodyta, naudokite išeigos vietą, nustatytą ištekliuje, kurį naudoja vėliausia gamybos maršrute nurodyta operacija.</span><span class="sxs-lookup"><span data-stu-id="e72cb-111">If no location is found there, use the output location that is defined on the resource that is used by the last operation that is defined in the production route.</span></span>
3. <span data-ttu-id="e72cb-112">Jei ten vieta nenurodyta, naudokite išeigos vietą, nustatytą išteklių grupėje, kurią naudoja vėliausia gamybos maršrute nurodytos operacijos išteklius.</span><span class="sxs-lookup"><span data-stu-id="e72cb-112">If no location is found there, use the output location that is defined on the resource group that is used by the resource for the last operation that is defined in the production route.</span></span>
4. <span data-ttu-id="e72cb-113">Jei ten vieta nenurodyta, naudokite išeigos vietą, nurodytą gamybos užsakymo nustatytame sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="e72cb-113">If no location is found there, use the output location that is defined on the warehouse that is defined for the production order.</span></span>

<span data-ttu-id="e72cb-114">Nurodoma tik produktų, kurie nustatomi naudojant patobulintus sandėlio procesus, numatytoji gamybos išeigos vieta.</span><span class="sxs-lookup"><span data-stu-id="e72cb-114">A default production output location is set only for products that are set up by using advanced warehouse processes.</span></span> <span data-ttu-id="e72cb-115">Kai šio tipo prekė yra paskelbta baigta, sukuriamas tipo **Baigtos prekės atidėtos** arba **Sudėtinis produktas ir šalutinis produktas atidėti** sandėlio darbas.</span><span class="sxs-lookup"><span data-stu-id="e72cb-115">When this type of item is reported as finished, warehouse work of the **Finished goods put away** or **Co-product and by-product put away** type is created.</span></span> <span data-ttu-id="e72cb-116">Šio tipo darbe gamybos išeigos vieta naudojama kaip paėmimo vieta.</span><span class="sxs-lookup"><span data-stu-id="e72cb-116">This type of work uses the production output location as the pick location.</span></span> <span data-ttu-id="e72cb-117">Atidėjimo vieta nustatoma pagal vietos nurodymus.</span><span class="sxs-lookup"><span data-stu-id="e72cb-117">The put-away location is determined by the location directives.</span></span>
