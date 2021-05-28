---
title: Atsižvelgiama į vėlai pasirinktą užduotį, kai gamybos užsakymai iš naujo nustatomi naudojant paketinę užduotį
description: Kai naudojate pasikartojančią paketinę užduotį gamybos užsakymo būsenai nustatyti iš naujo, atsižvelgiama į pavėluotus pasirinkimus.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e53198f427f4060421a4f0078277682c43db1320
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026739"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a><span data-ttu-id="75649-103">Atsižvelgiama į vėlai pasirinktą užduotį, kai gamybos užsakymai iš naujo nustatomi naudojant paketinę užduotį</span><span class="sxs-lookup"><span data-stu-id="75649-103">Late selection isn't respected when production orders are reset via a batch job</span></span>

<span data-ttu-id="75649-104">KB numeris: 4614634</span><span class="sxs-lookup"><span data-stu-id="75649-104">KB number: 4614634</span></span>

## <a name="symptoms"></a><span data-ttu-id="75649-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="75649-105">Symptoms</span></span>

<span data-ttu-id="75649-106">Kai naudojate pasikartojančią paketinę užduotį gamybos užsakymo būsenai nustatyti iš naujo, atsižvelgiama į pavėluotus pasirinkimus.</span><span class="sxs-lookup"><span data-stu-id="75649-106">When you use a recurring batch job to reset the status of a production order, late selections aren't respected.</span></span>

## <a name="resolution"></a><span data-ttu-id="75649-107">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="75649-107">Resolution</span></span>

<span data-ttu-id="75649-108">Dabartinis dizainas nepalaiko pavėluotų pasirinkimų naudojimo būsenos *nustatymo iš naujo* procese.</span><span class="sxs-lookup"><span data-stu-id="75649-108">The current design doesn't support the use of late selections for the *Reset status* process.</span></span>
