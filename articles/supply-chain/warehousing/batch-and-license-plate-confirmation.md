---
title: Paketo ir numerio lentelės patvirtinimas
description: Šioje temoje aprašoma, kaip nustatyti ir taikyti paketo ir numerio lentelės patvirtinimą iš mobiliojo įrenginio.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efab5b11782fd2344fb5f532272007d187c1465b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "344230"
---
# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="d1f01-103">Paketo ir numerio lentelės patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="d1f01-103">Batch and license plate confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1f01-104">Atlikdami paketo patvirtinimą galite patvirtinti kad iš mobiliojo įrenginio paimamas teisingas paketas.</span><span class="sxs-lookup"><span data-stu-id="d1f01-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="d1f01-105">Taikoma tik pradiniam virš paketo esančių elementų darbo paėmimui, kai parinktimi virš paketo nurodoma, kad ieškos hierarchijoje paketo intervalas yra aukščiau negu vietos intervalas, ir turite patikrinti, ar paimtas paketas atitinka darbo eilutėje nurodytą paketą.</span><span class="sxs-lookup"><span data-stu-id="d1f01-105">On the initial pick of work for batch above-items only, where batch above indicates that batch ranges higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span> 

<span data-ttu-id="d1f01-106">Naudodami numerio lentelės patvirtinimą galite patvirtinti, kad iš mobiliojo įrenginio paimta teisinga numerio lentelė.</span><span class="sxs-lookup"><span data-stu-id="d1f01-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="d1f01-107">Rinkdamiesi darbą iš etapo vietos turite patikrinti, ar pasirinkta numerio lentelė atitinka su darbu susietą numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="d1f01-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="d1f01-108">Jei darbas pradedamas nuskaitant numerio lentelę, šis patvirtinimo veiksmas praleidžiamas.</span><span class="sxs-lookup"><span data-stu-id="d1f01-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="d1f01-109">Kai taikoma</span><span class="sxs-lookup"><span data-stu-id="d1f01-109">Where it applies</span></span>
<span data-ttu-id="d1f01-110">Patvirtinimas taikomas šiais atvejais:</span><span class="sxs-lookup"><span data-stu-id="d1f01-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="d1f01-111">Paketo patvirtinimas taikomas pradiniam virš paketo esančių elementų darbo paėmimui.</span><span class="sxs-lookup"><span data-stu-id="d1f01-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="d1f01-112">Numerio lentelės patvirtinimas taikomas paėmimams iš etapo vietos.</span><span class="sxs-lookup"><span data-stu-id="d1f01-112">License plate confirmation applies to picks from stage locations.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="d1f01-113">Paketo ir numerio lentelės patvirtinimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="d1f01-113">Set up batch and license plate confirmation</span></span>
<span data-ttu-id="d1f01-114">Paketo ir numerio lentelės patvirtinimą galite konfigūruoti pagal mobiliojo įrenginio meniu elementus.</span><span class="sxs-lookup"><span data-stu-id="d1f01-114">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>  
1.  <span data-ttu-id="d1f01-115">Mobiliojo įrenginio meniu elementuose įveskite darbo patvirtinimo sąranką.</span><span class="sxs-lookup"><span data-stu-id="d1f01-115">From the mobile device menu items, enter the work confirmation setup.</span></span>  
2.  <span data-ttu-id="d1f01-116">Pasirinkite paketo arba numerio lentelės patvirtinimo parinktį.</span><span class="sxs-lookup"><span data-stu-id="d1f01-116">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="d1f01-117">Abi parinktys taikomos darbo tipo paėmimams, kuriems neįgalinta automatinio patvirtinimo funkcija.</span><span class="sxs-lookup"><span data-stu-id="d1f01-117">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  
