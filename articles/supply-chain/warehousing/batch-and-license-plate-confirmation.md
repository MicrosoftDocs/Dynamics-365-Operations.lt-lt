---
title: Paketo ir numerio lentelės patvirtinimas
description: Šioje temoje aprašoma, kaip nustatyti ir taikyti paketo ir numerio lentelės patvirtinimą iš mobiliojo įrenginio.
author: Mirzaab
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c588e6ed11d275b75133e2824f3d385048050426
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837542"
---
# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="5db3b-103">Paketo ir numerio lentelės patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="5db3b-103">Batch and license plate confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5db3b-104">Atlikdami paketo patvirtinimą galite patvirtinti kad iš mobiliojo įrenginio paimamas teisingas paketas.</span><span class="sxs-lookup"><span data-stu-id="5db3b-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="5db3b-105">Pradiniame tik *Virš paketo\[vieta\]* elementų darbo paėmime, kai „virš paketo” reiškia, kad paketas yra aukščiau nei vieta ieškos hierarchijoje, turite patikrinti, ar paimtas paketas atitinka darbo eilutėje nurodytą paketą.</span><span class="sxs-lookup"><span data-stu-id="5db3b-105">On the initial pick of work for *Batch-above\[location\]* items only, where batch-above indicates that batch is placed higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span>

<span data-ttu-id="5db3b-106">Naudodami numerio lentelės patvirtinimą galite patvirtinti, kad iš mobiliojo įrenginio paimta teisinga numerio lentelė.</span><span class="sxs-lookup"><span data-stu-id="5db3b-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="5db3b-107">Rinkdamiesi darbą iš etapo vietos turite patikrinti, ar pasirinkta numerio lentelė atitinka su darbu susietą numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="5db3b-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="5db3b-108">Jei darbas pradedamas nuskaitant numerio lentelę, šis patvirtinimo veiksmas praleidžiamas.</span><span class="sxs-lookup"><span data-stu-id="5db3b-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="5db3b-109">Kai taikoma</span><span class="sxs-lookup"><span data-stu-id="5db3b-109">Where it applies</span></span>

<span data-ttu-id="5db3b-110">Patvirtinimas taikomas šiais atvejais:</span><span class="sxs-lookup"><span data-stu-id="5db3b-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="5db3b-111">Paketo patvirtinimas taikomas pradiniam virš paketo esančių elementų darbo paėmimui.</span><span class="sxs-lookup"><span data-stu-id="5db3b-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="5db3b-112">Numerio lentelės patvirtinimas taikomas paėmimams iš etapo vietos.</span><span class="sxs-lookup"><span data-stu-id="5db3b-112">License plate confirmation applies to picks from stage locations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5db3b-113">Papildymas nėra palaikomoas licencijos lentelės patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="5db3b-113">Replenishment is not supported for license plate confirmation.</span></span> <span data-ttu-id="5db3b-114">Atliekand papildymo darbą nėra sukuriamas joks lentelės patvirtinimo žingsnis.</span><span class="sxs-lookup"><span data-stu-id="5db3b-114">When executing replenishment work, no license plate confirmation step is created.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="5db3b-115">Paketo ir numerio lentelės patvirtinimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="5db3b-115">Set up batch and license plate confirmation</span></span>

<span data-ttu-id="5db3b-116">Paketo ir numerio lentelės patvirtinimą galite konfigūruoti pagal mobiliojo įrenginio meniu elementus.</span><span class="sxs-lookup"><span data-stu-id="5db3b-116">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>

1. <span data-ttu-id="5db3b-117">Mobiliojo įrenginio meniu elementuose įveskite darbo patvirtinimo sąranką.</span><span class="sxs-lookup"><span data-stu-id="5db3b-117">From the mobile device menu items, enter the work confirmation setup.</span></span>  
1. <span data-ttu-id="5db3b-118">Pasirinkite paketo arba numerio lentelės patvirtinimo parinktį.</span><span class="sxs-lookup"><span data-stu-id="5db3b-118">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="5db3b-119">Abi parinktys taikomos darbo tipo paėmimams, kuriems neįgalinta automatinio patvirtinimo funkcija.</span><span class="sxs-lookup"><span data-stu-id="5db3b-119">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
