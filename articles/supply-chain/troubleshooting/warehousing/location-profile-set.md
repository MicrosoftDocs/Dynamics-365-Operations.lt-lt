---
title: Vietos šablone neleidžiamos neigiamos atsargos, bet leidžiamos neigiamos turimos atsargos
description: Vietos šablone nustatyta parinktis Leisti neigiamas atsargas yra nustatyta kaip Ne, bet sistema vis dar leidžia neigiamas turimų atsargų atsargas.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026743"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a><span data-ttu-id="61849-103">Vietos šablone neleidžiamos neigiamos atsargos, bet leidžiamos neigiamos turimos atsargos</span><span class="sxs-lookup"><span data-stu-id="61849-103">Location profile disallows negative inventory, but negative on-hand inventory is permitted</span></span>

<span data-ttu-id="61849-104">KB numeris: 4613622</span><span class="sxs-lookup"><span data-stu-id="61849-104">KB number: 4613622</span></span>

## <a name="symptoms"></a><span data-ttu-id="61849-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="61849-105">Symptoms</span></span>

<span data-ttu-id="61849-106">Vietos šablone nustatyta parinktis **Leisti neigiamas atsargas** yra nustatyta kaip *Ne*, bet sistema vis dar leidžia neigiamas turimų atsargų atsargas.</span><span class="sxs-lookup"><span data-stu-id="61849-106">The **Allow negative inventory** option for the location profile is set to *No*, but the system still allows negative on-hand inventory.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="61849-107">Pavyzdinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="61849-107">Example scenario</span></span>

<span data-ttu-id="61849-108">Vyriausybės reguliuojamų operacijų sistema turi turėti galimybę įrašyti neigiamas atsargas į rezervuoti nuostolius.</span><span class="sxs-lookup"><span data-stu-id="61849-108">For government-regulated transactions, the system must be able to record negative inventory to book losses.</span></span> <span data-ttu-id="61849-109">Norite, kad prekė galėtų rodyti neigiamas atsargas, bet tik tam skirtose vietose, pvz., talpyklose.</span><span class="sxs-lookup"><span data-stu-id="61849-109">You want an item to be able to show negative inventory, but only in designated locations, such as tanks.</span></span> <span data-ttu-id="61849-110">Tačiau, jei prekių modelių grupė leidžia neigiamas atsargas, reikia išsiaiškinti, ar nustatyta vieta leidžia neigiamas atsargas.</span><span class="sxs-lookup"><span data-stu-id="61849-110">However, if the item model group allows negative inventory, you find that it doesn't matter whether the location is set to allow negative inventory.</span></span> <span data-ttu-id="61849-111">Jei prekė nustatyta taip, kad neigiamos atsargos neleidžiamos, nesvarbu, kaip nustatytas vietos šablonas.</span><span class="sxs-lookup"><span data-stu-id="61849-111">If the item is set up so that negative inventory isn't allowed, it doesn't matter how the location profile is set up.</span></span>

## <a name="resolution"></a><span data-ttu-id="61849-112">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="61849-112">Resolution</span></span>

<span data-ttu-id="61849-113">Neigiamas **atsargų parametras Leisti** iš vietos šablono taikomas tik sandėlio procesams, pvz., paėmimui.</span><span class="sxs-lookup"><span data-stu-id="61849-113">The **Allow negative inventory** setting from the location profile applies only to warehouse processes, such as picking.</span></span> <span data-ttu-id="61849-114">Tačiau prekių modelių grupės, kurios nustatytos leisti neigiamas atsargas, paveikia visus atsargų valdymo ir sandėlio valdymo modulių procesus, o vietos šablonas nepaiso parametro.</span><span class="sxs-lookup"><span data-stu-id="61849-114">However, item model groups that are set to allow negative inventory affect all processes from the Inventory management and Warehouse management modules, and the location profile won't override the setting.</span></span>

<span data-ttu-id="61849-115">Galite kontroliuoti, ar sandėlyje gali būti neigiamos atsargos.</span><span class="sxs-lookup"><span data-stu-id="61849-115">You can control whether a warehouse is allowed to carry negative inventory.</span></span> <span data-ttu-id="61849-116">Nustatykite savo prekių modelių grupes taip, kad jų neigiamos faktinės atsargos būtų neleidžiamos, ir nustatykite, kad neigiamos atsargos būtų leidžiamos tik susijusiuose sandėliuose.</span><span class="sxs-lookup"><span data-stu-id="61849-116">Set your item model groups to disallow negative physical inventory, and set only the relevant warehouse to allow negative inventory.</span></span>
