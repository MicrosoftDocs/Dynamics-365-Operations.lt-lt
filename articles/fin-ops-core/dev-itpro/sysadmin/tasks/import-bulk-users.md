---
title: Vartotojų importavimas iš „Azure Active Directory“
description: Šią procedūrą gali naudoti sistemos administratoriai, norėdami neautomatiškai importuoti pasirinktus vartotojus arba importuoti didelį skaičių vartotojų iš „Azure Active Directory“.
author: peakerbl
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0c2600ad8f441e6b73b143c27afa08ad0a5c2748
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571010"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="65554-103">Vartotojų importavimas iš „Azure Active Directory“</span><span class="sxs-lookup"><span data-stu-id="65554-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="65554-104">Pasirinktų vartotojų importavimas</span><span class="sxs-lookup"><span data-stu-id="65554-104">Import select users</span></span>

<span data-ttu-id="65554-105">Šią procedūrą gali naudoti sistemos administratoriai, norėdami importuoti pasirinktus vartotojus iš „Azure Active Directory“ („Azure AD“).</span><span class="sxs-lookup"><span data-stu-id="65554-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="65554-106">Vartotojas bus importuotas su dabartine seanso įmone kaip numatytoji įmonė.</span><span class="sxs-lookup"><span data-stu-id="65554-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="65554-107">Jei reikia, prieš importuodami vartotojus, keiskite šią įmonę.</span><span class="sxs-lookup"><span data-stu-id="65554-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="65554-108">Pasirinkite **Sistemos administravimas > Vartotojai > Vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="65554-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="65554-109">Spustelėkite **Importuoti vartotojus**.</span><span class="sxs-lookup"><span data-stu-id="65554-109">Click **Import users**.</span></span>
4. <span data-ttu-id="65554-110">Pasirinkite vartotojus, kuriuos reikia importuoti ir pasirinkite **Importuoti vartotojus**.</span><span class="sxs-lookup"><span data-stu-id="65554-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="65554-111">Baigus importavimą bus reikalaujama, kad vartotojai priskirtų vaidmenis.</span><span class="sxs-lookup"><span data-stu-id="65554-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="65554-112">Masinis vartotojų importavimas</span><span class="sxs-lookup"><span data-stu-id="65554-112">Import users in bulk</span></span>

<span data-ttu-id="65554-113">Šią procedūrą gali naudoti sistemos administratoriai, norėdami importuoti didelį skaičių vartotojų iš „Azure Active Directory“.</span><span class="sxs-lookup"><span data-stu-id="65554-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="65554-114">Atkreipkite dėmesį, kad naudojant paketinio importavimo pasirinktį vartotojo pasirinkti negalima.</span><span class="sxs-lookup"><span data-stu-id="65554-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="65554-115">Importavimo kaip paketinės užduoties vykdymas</span><span class="sxs-lookup"><span data-stu-id="65554-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="65554-116">Vartotojas bus importuotas su dabartine seanso įmone kaip numatytoji įmonė.</span><span class="sxs-lookup"><span data-stu-id="65554-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="65554-117">Jei reikia, prieš importuodami vartotojus, keiskite šią įmonę.</span><span class="sxs-lookup"><span data-stu-id="65554-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="65554-118">Pasirinkite **Sistemos administravimas > Vartotojai > Vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="65554-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="65554-119">Spustelėkite **Paketinis importavimas**.</span><span class="sxs-lookup"><span data-stu-id="65554-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="65554-120">Išplėskite skyrių **Vykdyti fone**.</span><span class="sxs-lookup"><span data-stu-id="65554-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="65554-121">Pasirinkite **Taip** lauke **Paketinis vykdymas**.</span><span class="sxs-lookup"><span data-stu-id="65554-121">Select **Yes** in the **Batch processing** field.</span></span>
6. <span data-ttu-id="65554-122">Lauke **Paketinė grupė** įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="65554-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="65554-123">Tai pasirinktinis veiksmas.</span><span class="sxs-lookup"><span data-stu-id="65554-123">This is an optional step.</span></span>  
7. <span data-ttu-id="65554-124">Lauke **Privatus** pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="65554-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="65554-125">Tai pasirinktinis veiksmas.</span><span class="sxs-lookup"><span data-stu-id="65554-125">This is an optional step.</span></span>  
8. <span data-ttu-id="65554-126">Lauke **Kritinė užduotis** pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="65554-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="65554-127">Tai pasirinktinis veiksmas.</span><span class="sxs-lookup"><span data-stu-id="65554-127">This is an optional step.</span></span>  
9. <span data-ttu-id="65554-128">Lauke **Stebėjimo kategorija** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="65554-128">In the **Monitoring category** field, select an option.</span></span>
10. <span data-ttu-id="65554-129">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="65554-129">Click **OK**.</span></span>

<span data-ttu-id="65554-130">Baigus importavimą bus reikalaujama, kad vartotojai priskirtų vaidmenis.</span><span class="sxs-lookup"><span data-stu-id="65554-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="65554-131">Paleiskite smėlio dėžės aplinkoje</span><span class="sxs-lookup"><span data-stu-id="65554-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="65554-132">Pasirinkite **Paketinis importavimas**.</span><span class="sxs-lookup"><span data-stu-id="65554-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="65554-133">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="65554-133">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]