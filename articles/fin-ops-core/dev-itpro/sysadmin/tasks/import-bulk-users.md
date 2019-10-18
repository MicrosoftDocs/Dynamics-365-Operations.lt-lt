---
title: Masinis vartotojų importavimas
description: Šią procedūrą gali naudoti sistemos administratoriai, norėdami importuoti didelį skaičių vartotojų iš „Azure Active Directory“.
author: maertenm
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb2c316465f8c6964a562e92ce0a2233b37d38fe
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180903"
---
# <a name="import-users-in-bulk"></a><span data-ttu-id="748a1-103">Masinis vartotojų importavimas</span><span class="sxs-lookup"><span data-stu-id="748a1-103">Import users in bulk</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="748a1-104">Šią procedūrą gali naudoti sistemos administratoriai, norėdami importuoti didelį skaičių vartotojų iš „Azure Active Directory“.</span><span class="sxs-lookup"><span data-stu-id="748a1-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="748a1-105">Vykdyti kaip paketinę užduotį</span><span class="sxs-lookup"><span data-stu-id="748a1-105">Run as a batch job</span></span>
1. <span data-ttu-id="748a1-106">Pasirinkite Sistemos administravimas > Vartotojai > Vartotojai.</span><span class="sxs-lookup"><span data-stu-id="748a1-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="748a1-107">Spustelėkite Paketo importavimas.</span><span class="sxs-lookup"><span data-stu-id="748a1-107">Click Batch import.</span></span>
3. <span data-ttu-id="748a1-108">Išplėskite dalį Vykdyti fone.</span><span class="sxs-lookup"><span data-stu-id="748a1-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="748a1-109">Lauke Paketinis vykdymas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="748a1-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="748a1-110">Lauke Užduoties aprašas įrašykite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="748a1-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="748a1-111">Lauke Paketo grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="748a1-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="748a1-112">Tai pasirinktinis veiksmas.</span><span class="sxs-lookup"><span data-stu-id="748a1-112">This is an optional step.</span></span>  
7. <span data-ttu-id="748a1-113">Lauke Privatus pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="748a1-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="748a1-114">Tai pasirinktinis veiksmas.</span><span class="sxs-lookup"><span data-stu-id="748a1-114">This is an optional step.</span></span>  
8. <span data-ttu-id="748a1-115">Lauke Kritinis darbas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="748a1-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="748a1-116">Tai pasirinktinis veiksmas.</span><span class="sxs-lookup"><span data-stu-id="748a1-116">This is an optional step.</span></span>  
9. <span data-ttu-id="748a1-117">Lauke Stebėjimo kategorija pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="748a1-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="748a1-118">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="748a1-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="748a1-119">Paleiskite smėlio dėžės aplinkoje</span><span class="sxs-lookup"><span data-stu-id="748a1-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="748a1-120">Spustelėkite Paketo importavimas.</span><span class="sxs-lookup"><span data-stu-id="748a1-120">Click Batch import.</span></span>
2. <span data-ttu-id="748a1-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="748a1-121">Click OK.</span></span>

