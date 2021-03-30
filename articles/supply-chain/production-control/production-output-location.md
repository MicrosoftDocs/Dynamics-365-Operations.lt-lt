---
title: Gamybos išeigos vieta
description: Šioje temoje aprašoma hierarchija, naudojama gamybos išeigos vietai nustatyti.
author: johanhoffmann
manager: tfehr
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8fa4f7d844c178ee603778fa2f1def6bfc33db97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209448"
---
# <a name="production-output-location"></a><span data-ttu-id="30a80-103">Gamybos išeigos vieta</span><span class="sxs-lookup"><span data-stu-id="30a80-103">Production output location</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30a80-104">Šioje temoje aprašoma hierarchija, naudojama gamybos išeigos vietai nustatyti.</span><span class="sxs-lookup"><span data-stu-id="30a80-104">This topic describes the hierarchy that is used to identify the production output location.</span></span>

<span data-ttu-id="30a80-105">Gamybos išeigos vieta yra vieta, kurioje baigta prekė saugoma ją pagaminus.</span><span class="sxs-lookup"><span data-stu-id="30a80-105">The production output location is the location where a finished good is first stored after it's produced.</span></span> <span data-ttu-id="30a80-106">Paprastai ši vieta yra netoli baigtos prekės gamybos proceso vietos.</span><span class="sxs-lookup"><span data-stu-id="30a80-106">Usually, this location is close to the production process that produces the finished good.</span></span> <span data-ttu-id="30a80-107">Gamybos išeigos vieta naudojama kaip tarpinė medžiagos saugykla prieš ją perkeliant į siuntimo zoną, saugojimo vietą, proceso pabaigos gamybos proceso gamybos įvesties vietą ir t. t.</span><span class="sxs-lookup"><span data-stu-id="30a80-107">The production output location is used as intermediate storage for the material before it's moved on to the shipment area, a storage location, a production input location for a downstream production process, and so on.</span></span> 

<span data-ttu-id="30a80-108">Numatytoji gamybos išeigos vieta nustatoma, kai baigtos prekės užregistruojamos gamybos užsakyme arba paketiniame užsakyme.</span><span class="sxs-lookup"><span data-stu-id="30a80-108">A default production output location is set when finished goods are reported on a production order or batch order.</span></span> <span data-ttu-id="30a80-109">Toliau nurodyta hierarchija naudojama šiai išeigos vietai nustatyti.</span><span class="sxs-lookup"><span data-stu-id="30a80-109">The following hierarchy is used to identify this output location:</span></span>

1. <span data-ttu-id="30a80-110">Naudokite išeigos vietą, nurodytą gamybos užsakymo arba paketo užsakymo antraštėje.</span><span class="sxs-lookup"><span data-stu-id="30a80-110">Use the output location that is defined on the production order or batch order header.</span></span>
2. <span data-ttu-id="30a80-111">Jei ten vieta nenurodyta, naudokite išeigos vietą, nustatytą ištekliuje, kurį naudoja vėliausia gamybos maršrute nurodyta operacija.</span><span class="sxs-lookup"><span data-stu-id="30a80-111">If no location is found there, use the output location that is defined on the resource that is used by the last operation that is defined in the production route.</span></span>
3. <span data-ttu-id="30a80-112">Jei ten vieta nenurodyta, naudokite išeigos vietą, nustatytą išteklių grupėje, kurią naudoja vėliausia gamybos maršrute nurodytos operacijos išteklius.</span><span class="sxs-lookup"><span data-stu-id="30a80-112">If no location is found there, use the output location that is defined on the resource group that is used by the resource for the last operation that is defined in the production route.</span></span>
4. <span data-ttu-id="30a80-113">Jei ten vieta nenurodyta, naudokite išeigos vietą, nurodytą gamybos užsakymo nustatytame sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="30a80-113">If no location is found there, use the output location that is defined on the warehouse that is defined for the production order.</span></span>

<span data-ttu-id="30a80-114">Nurodoma tik produktų, kurie nustatomi naudojant patobulintus sandėlio procesus, numatytoji gamybos išeigos vieta.</span><span class="sxs-lookup"><span data-stu-id="30a80-114">A default production output location is set only for products that are set up by using advanced warehouse processes.</span></span> <span data-ttu-id="30a80-115">Kai šio tipo prekė yra paskelbta baigta, sukuriamas tipo **Baigtos prekės atidėtos** arba **Sudėtinis produktas ir šalutinis produktas atidėti** sandėlio darbas.</span><span class="sxs-lookup"><span data-stu-id="30a80-115">When this type of item is reported as finished, warehouse work of the **Finished goods put away** or **Co-product and by-product put away** type is created.</span></span> <span data-ttu-id="30a80-116">Šio tipo darbe gamybos išeigos vieta naudojama kaip paėmimo vieta.</span><span class="sxs-lookup"><span data-stu-id="30a80-116">This type of work uses the production output location as the pick location.</span></span> <span data-ttu-id="30a80-117">Atidėjimo vieta nustatoma pagal vietos nurodymus.</span><span class="sxs-lookup"><span data-stu-id="30a80-117">The put-away location is determined by the location directives.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]