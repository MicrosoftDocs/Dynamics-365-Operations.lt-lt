---
title: Atitikimo kūrimas ir apdorojimas
description: Šioje temoje aiškinama, kaip vykdyti neatitikimo valdymą remiantis esamu kokybės užsakymu.
author: perlynne
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c4f7e61adf37e74bdb082270b689cf0375ccc7f7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833958"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="e436f-103">Atitikimo kūrimas ir apdorojimas</span><span class="sxs-lookup"><span data-stu-id="e436f-103">Create and process a conformance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e436f-104">Šioje temoje aiškinama, kaip vykdyti neatitikimo valdymą remiantis esamu kokybės užsakymu.</span><span class="sxs-lookup"><span data-stu-id="e436f-104">This topic explains how to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="e436f-105">Galite paleisti šį įrašą naudodami USMF demonstracinę įmonę ir galite naudoti siūlomas vertes.</span><span class="sxs-lookup"><span data-stu-id="e436f-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="e436f-106">Paprastai šią procedūrą atlieka kokybės klerkas.</span><span class="sxs-lookup"><span data-stu-id="e436f-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="e436f-107">Reikia įvesti būtinus duomenis, todėl užpildykite instrukcijas, esančias [Prekių kokybės tikrinimas](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="e436f-107">As a prerequisite, complete the instructions in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span> <span data-ttu-id="e436f-108">Norint apdoroti neatitikties patvirtinimą, užduoties įrašą paleidusiam vartotojui vartotojo puslapyje turi būti priskirta vertė „Pavadinimas“.</span><span class="sxs-lookup"><span data-stu-id="e436f-108">To process the approval of a nonconformance, the user who runs the task recording must have a "Name" value assigned on the Users page.</span></span> <span data-ttu-id="e436f-109">Norint naudoti dokumento pastabas, vartotojui taip pat turi būti suaktyvinta vartotojo pasirinktis Dokumentų tvarkymas.</span><span class="sxs-lookup"><span data-stu-id="e436f-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="e436f-110">Pasirinkti kokybės užsakymą</span><span class="sxs-lookup"><span data-stu-id="e436f-110">Select a quality order</span></span>
1. <span data-ttu-id="e436f-111">Naršymo srityje eikite į **Moduliai > Atsargų valdymas > Periodinės užduotys > Kokybės valdymas > Kokybės užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="e436f-111">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="e436f-112">Sąraše pasirinkite kokybės užsakymą, kuris buvo sukurtas [Prekių kokybės tikrinimas](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="e436f-112">In the list, select the quality order that was created in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="e436f-113">Neatitikties kūrimas</span><span class="sxs-lookup"><span data-stu-id="e436f-113">Create a nonconformance</span></span>
1. <span data-ttu-id="e436f-114">Veiksmų srityje pažymėkite **Užklausos**.</span><span class="sxs-lookup"><span data-stu-id="e436f-114">On the Action Pane, select **Inquiries**.</span></span>
2. <span data-ttu-id="e436f-115">Pasirinkite **Neatitikimai**.</span><span class="sxs-lookup"><span data-stu-id="e436f-115">Select **Non conformances**.</span></span>
3. <span data-ttu-id="e436f-116">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="e436f-116">Select **New**.</span></span>
4. <span data-ttu-id="e436f-117">Lauko **Problemos tipas** išskleidžiamajame meniu pažymėkite problemą, kuri buvo aptikta patikrinimo metu.</span><span class="sxs-lookup"><span data-stu-id="e436f-117">In the drop-down menu of the **Problem type** field, select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="e436f-118">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="e436f-118">Select **OK**.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="e436f-119">Neatitikties tvirtinimas / atmetimas</span><span class="sxs-lookup"><span data-stu-id="e436f-119">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="e436f-120">Pasirinkite **Funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="e436f-120">Select **Functions**.</span></span>
2. <span data-ttu-id="e436f-121">Pažymėkite **Patvirtinti neatitikimą**.</span><span class="sxs-lookup"><span data-stu-id="e436f-121">Select **Approve non conformance**.</span></span> <span data-ttu-id="e436f-122">Šiuo atveju patvirtinkite neatitiktį.</span><span class="sxs-lookup"><span data-stu-id="e436f-122">For this example, approve the nonconformance.</span></span> <span data-ttu-id="e436f-123">Patvirtintus neatitikimus galima susieti su susijusiomis operacijomis, siekiant įrašyti darbą, kuris atliktas kaip neatitikimo tvarkymo dalis, ir, kaip šioje temoje, taisomojo tvarkymo apdorojimas.</span><span class="sxs-lookup"><span data-stu-id="e436f-123">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this topic, the processing of correction handling.</span></span>  
3. <span data-ttu-id="e436f-124">Pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="e436f-124">Select **Yes**.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="e436f-125">Koregavimo veiksmo kūrimas</span><span class="sxs-lookup"><span data-stu-id="e436f-125">Create a correction action</span></span>
1. <span data-ttu-id="e436f-126">Pažymėkite **Taisymai**.</span><span class="sxs-lookup"><span data-stu-id="e436f-126">Select **Corrections**.</span></span>
2. <span data-ttu-id="e436f-127">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="e436f-127">Select **New**.</span></span>
3. <span data-ttu-id="e436f-128">Naujos eilutės lauke **Darbuotojų skaičius** išplečiamajame meniu pažymėkite pageidaujamą įrašą.</span><span class="sxs-lookup"><span data-stu-id="e436f-128">In the **Personnel number** field of the new row, select the desired record from the drop down menu.</span></span>
4. <span data-ttu-id="e436f-129">Spustelėkite **Pažymėti**.</span><span class="sxs-lookup"><span data-stu-id="e436f-129">Click **Select**.</span></span>
5. <span data-ttu-id="e436f-130">Pažymėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="e436f-130">Select **Attach**.</span></span> <span data-ttu-id="e436f-131">Sukurkite pastabą apie koregavimą.</span><span class="sxs-lookup"><span data-stu-id="e436f-131">Create a note about the correction.</span></span> <span data-ttu-id="e436f-132">Šiuo atveju veiksmas yra susisiekti su tiekėju ir aptarti neatitikties atvejį.</span><span class="sxs-lookup"><span data-stu-id="e436f-132">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
6. <span data-ttu-id="e436f-133">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="e436f-133">Select **New**.</span></span>
7. <span data-ttu-id="e436f-134">Pažymėkite **Pastaba**.</span><span class="sxs-lookup"><span data-stu-id="e436f-134">Select **Note**.</span></span> <span data-ttu-id="e436f-135">Atsižvelgiant į ataskaitos sąranką, galima atspausdinti skirtingus ataskaitų, kurios susijusios su neatitikimų valdymu, dokumentų tipus.</span><span class="sxs-lookup"><span data-stu-id="e436f-135">Depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
8. <span data-ttu-id="e436f-136">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e436f-136">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="e436f-137">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e436f-137">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="e436f-138">Koregavimo tvarkymas</span><span class="sxs-lookup"><span data-stu-id="e436f-138">Maintain a correction</span></span>
1. <span data-ttu-id="e436f-139">Pažymėkite **Žymėti kaip užbaigtą**.</span><span class="sxs-lookup"><span data-stu-id="e436f-139">Select **Mark complete**.</span></span>
2. <span data-ttu-id="e436f-140">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="e436f-140">Select **OK**.</span></span>
3. <span data-ttu-id="e436f-141">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e436f-141">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="e436f-142">Neatitikties uždarymas</span><span class="sxs-lookup"><span data-stu-id="e436f-142">Close a nonconformance</span></span>
1. <span data-ttu-id="e436f-143">Pažymėkite **Funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="e436f-143">Select **Functions**.</span></span>
2. <span data-ttu-id="e436f-144">Pažymėkite **Uždaryti neatitikimą**.</span><span class="sxs-lookup"><span data-stu-id="e436f-144">Select **Close non conformance**.</span></span>
3. <span data-ttu-id="e436f-145">Pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="e436f-145">Select **Yes**.</span></span>
4. <span data-ttu-id="e436f-146">Uždarykite puslapius.</span><span class="sxs-lookup"><span data-stu-id="e436f-146">Close the pages.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]