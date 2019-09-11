---
title: Atitikimo kūrimas ir apdorojimas
description: Šioje temoje aiškinama, kaip vykdyti neatitikimo valdymą remiantis esamu kokybės užsakymu.
author: perlynne
manager: AnnBe
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e9cf42f80ef7a4c9c5f68a308386db5835c8f2e
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916650"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="3c530-103">Atitikimo kūrimas ir apdorojimas</span><span class="sxs-lookup"><span data-stu-id="3c530-103">Create and process a conformance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3c530-104">Šioje temoje aiškinama, kaip vykdyti neatitikimo valdymą remiantis esamu kokybės užsakymu.</span><span class="sxs-lookup"><span data-stu-id="3c530-104">This topic explains how to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="3c530-105">Galite paleisti šį įrašą naudodami USMF demonstracinę įmonę ir galite naudoti siūlomas vertes.</span><span class="sxs-lookup"><span data-stu-id="3c530-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="3c530-106">Paprastai šią procedūrą atlieka kokybės klerkas.</span><span class="sxs-lookup"><span data-stu-id="3c530-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="3c530-107">Reikia įvesti būtinus duomenis, todėl užpildykite instrukcijas, esančias [Prekių kokybės tikrinimas](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="3c530-107">As a prerequisite, complete the instructions in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span> <span data-ttu-id="3c530-108">Norint apdoroti neatitikties patvirtinimą, užduoties įrašą paleidusiam vartotojui vartotojo puslapyje turi būti priskirta vertė „Pavadinimas“.</span><span class="sxs-lookup"><span data-stu-id="3c530-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="3c530-109">Norint naudoti dokumento pastabas, vartotojui taip pat turi būti suaktyvinta vartotojo pasirinktis Dokumentų tvarkymas.</span><span class="sxs-lookup"><span data-stu-id="3c530-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="3c530-110">Pasirinkti kokybės užsakymą</span><span class="sxs-lookup"><span data-stu-id="3c530-110">Select a quality order</span></span>
1. <span data-ttu-id="3c530-111">Naršymo srityje eikite į **Moduliai > Atsargų valdymas > Periodinės užduotys > Kokybės valdymas > Kokybės užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="3c530-111">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="3c530-112">Sąraše pasirinkite kokybės užsakymą, kuris buvo sukurtas [Prekių kokybės tikrinimas](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="3c530-112">In the list, select the quality order that was created in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="3c530-113">Neatitikties kūrimas</span><span class="sxs-lookup"><span data-stu-id="3c530-113">Create a nonconformance</span></span>
1. <span data-ttu-id="3c530-114">Veiksmų srityje pažymėkite **Užklausos**.</span><span class="sxs-lookup"><span data-stu-id="3c530-114">In the action pane, select **Inquiries**.</span></span>
2. <span data-ttu-id="3c530-115">Pasirinkite **Neatitikimai**.</span><span class="sxs-lookup"><span data-stu-id="3c530-115">Select **Non conformances**.</span></span>
3. <span data-ttu-id="3c530-116">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="3c530-116">Select **New**.</span></span>
4. <span data-ttu-id="3c530-117">Lauko **Problemos tipas** išskleidžiamajame meniu pažymėkite problemą, kuri buvo aptikta patikrinimo metu.</span><span class="sxs-lookup"><span data-stu-id="3c530-117">In the drop-down menu of the **Problem type** field, select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="3c530-118">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3c530-118">Select **OK**.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="3c530-119">Neatitikties tvirtinimas / atmetimas</span><span class="sxs-lookup"><span data-stu-id="3c530-119">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="3c530-120">Pasirinkite **Funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="3c530-120">Select **Functions**.</span></span>
2. <span data-ttu-id="3c530-121">Pažymėkite **Patvirtinti neatitikimą**.</span><span class="sxs-lookup"><span data-stu-id="3c530-121">Select **Approve non conformance**.</span></span> <span data-ttu-id="3c530-122">Šiuo atveju patvirtinkite neatitiktį.</span><span class="sxs-lookup"><span data-stu-id="3c530-122">For this example, approve the nonconformance.</span></span> <span data-ttu-id="3c530-123">Patvirtintus neatitikimus galima susieti su susijusiomis operacijomis, siekiant įrašyti darbą, kuris atliktas kaip neatitikimo tvarkymo dalis, ir, kaip šioje temoje, taisomojo tvarkymo apdorojimas.</span><span class="sxs-lookup"><span data-stu-id="3c530-123">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this topic, the processing of correction handling.</span></span>  
3. <span data-ttu-id="3c530-124">Pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="3c530-124">Select **Yes**.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="3c530-125">Koregavimo veiksmo kūrimas</span><span class="sxs-lookup"><span data-stu-id="3c530-125">Create a correction action</span></span>
1. <span data-ttu-id="3c530-126">Pažymėkite **Taisymai**.</span><span class="sxs-lookup"><span data-stu-id="3c530-126">Select **Corrections**.</span></span>
2. <span data-ttu-id="3c530-127">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="3c530-127">Select **New**.</span></span>
3. <span data-ttu-id="3c530-128">Naujos eilutės lauke **Darbuotojų skaičius** išplečiamajame meniu pažymėkite pageidaujamą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3c530-128">In the **Personnel number** field of the new row, select the desired record from the drop down menu.</span></span>
4. <span data-ttu-id="3c530-129">Spustelėkite **Pažymėti**.</span><span class="sxs-lookup"><span data-stu-id="3c530-129">Click **Select**.</span></span>
5. <span data-ttu-id="3c530-130">Pažymėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="3c530-130">Select **Attach**.</span></span> <span data-ttu-id="3c530-131">Sukurkite pastabą apie koregavimą.</span><span class="sxs-lookup"><span data-stu-id="3c530-131">Create a note about the correction.</span></span> <span data-ttu-id="3c530-132">Šiuo atveju veiksmas yra susisiekti su tiekėju ir aptarti neatitikties atvejį.</span><span class="sxs-lookup"><span data-stu-id="3c530-132">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
6. <span data-ttu-id="3c530-133">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="3c530-133">Select **New**.</span></span>
7. <span data-ttu-id="3c530-134">Pažymėkite **Pastaba**.</span><span class="sxs-lookup"><span data-stu-id="3c530-134">Select **Note**.</span></span> <span data-ttu-id="3c530-135">Atsižvelgiant į ataskaitos sąranką, galima atspausdinti skirtingus ataskaitų, kurios susijusios su neatitikimų valdymu, dokumentų tipus.</span><span class="sxs-lookup"><span data-stu-id="3c530-135">Depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
8. <span data-ttu-id="3c530-136">Lauke **Aprašo laukas**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3c530-136">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="3c530-137">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3c530-137">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="3c530-138">Koregavimo tvarkymas</span><span class="sxs-lookup"><span data-stu-id="3c530-138">Maintain a correction</span></span>
1. <span data-ttu-id="3c530-139">Pažymėkite **Žymėti kaip užbaigtą**.</span><span class="sxs-lookup"><span data-stu-id="3c530-139">Select **Mark complete**.</span></span>
2. <span data-ttu-id="3c530-140">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3c530-140">Select **OK**.</span></span>
3. <span data-ttu-id="3c530-141">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3c530-141">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="3c530-142">Neatitikties uždarymas</span><span class="sxs-lookup"><span data-stu-id="3c530-142">Close a nonconformance</span></span>
1. <span data-ttu-id="3c530-143">Pažymėkite **Funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="3c530-143">Select **Functions**.</span></span>
2. <span data-ttu-id="3c530-144">Pažymėkite **Uždaryti neatitikimą**.</span><span class="sxs-lookup"><span data-stu-id="3c530-144">Select **Close non conformance**.</span></span>
3. <span data-ttu-id="3c530-145">Pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="3c530-145">Select **Yes**.</span></span>
4. <span data-ttu-id="3c530-146">Uždarykite puslapius.</span><span class="sxs-lookup"><span data-stu-id="3c530-146">Close the pages.</span></span>
