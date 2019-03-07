---
title: Kurti ir apdoroti atitiktis
description: Naudokite šią procedūrą norėdami atlikti neatitikties valdymą pagal esamą kokybės užsakymą.
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
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
ms.openlocfilehash: 16ed11bce92920fe8240fc85f706a2ac6ab0a04b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "336295"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="257fd-103">Kurti ir apdoroti atitiktis</span><span class="sxs-lookup"><span data-stu-id="257fd-103">Create and process a conformance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="257fd-104">Naudokite šią procedūrą norėdami atlikti neatitikties valdymą pagal esamą kokybės užsakymą.</span><span class="sxs-lookup"><span data-stu-id="257fd-104">Use this procedure to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="257fd-105">Galite paleisti šį įrašą naudodami USMF demonstracinę įmonę ir galite naudoti siūlomas vertes.</span><span class="sxs-lookup"><span data-stu-id="257fd-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="257fd-106">Paprastai šią procedūrą atlieka kokybės klerkas.</span><span class="sxs-lookup"><span data-stu-id="257fd-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="257fd-107">Kaip būtinąjį komponentą paleiskite užduoties įrašą „Tikrinti prekių kokybę“.</span><span class="sxs-lookup"><span data-stu-id="257fd-107">As a prerequisite, run the “Inspect the quality of goods” task recording.</span></span> <span data-ttu-id="257fd-108">Norint apdoroti neatitikties patvirtinimą, užduoties įrašą paleidusiam vartotojui vartotojo puslapyje turi būti priskirta vertė „Pavadinimas“.</span><span class="sxs-lookup"><span data-stu-id="257fd-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="257fd-109">Norint naudoti dokumento pastabas, vartotojui taip pat turi būti suaktyvinta vartotojo pasirinktis Dokumentų tvarkymas.</span><span class="sxs-lookup"><span data-stu-id="257fd-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="257fd-110">Pasirinkti kokybės užsakymą</span><span class="sxs-lookup"><span data-stu-id="257fd-110">Select a quality order</span></span>
1. <span data-ttu-id="257fd-111">Eikite į Kokybės užsakymai.</span><span class="sxs-lookup"><span data-stu-id="257fd-111">Go to Quality orders.</span></span>
2. <span data-ttu-id="257fd-112">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="257fd-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="257fd-113">Pasirinkite kokybės užsakymą, sukurtą iš užduoties įrašo „Tikrinti prekių kokybę“.</span><span class="sxs-lookup"><span data-stu-id="257fd-113">Select the quality order that was created from the "Inspect the quality of goods" task recording.</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="257fd-114">Neatitikties kūrimas</span><span class="sxs-lookup"><span data-stu-id="257fd-114">Create a nonconformance</span></span>
1. <span data-ttu-id="257fd-115">Spustelėkite Užklausos.</span><span class="sxs-lookup"><span data-stu-id="257fd-115">Click Inquiries.</span></span>
2. <span data-ttu-id="257fd-116">Spustelėkite Neatitiktys.</span><span class="sxs-lookup"><span data-stu-id="257fd-116">Click Non conformances.</span></span>
3. <span data-ttu-id="257fd-117">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="257fd-117">Click New.</span></span>
4. <span data-ttu-id="257fd-118">Lauke Problemos tipas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="257fd-118">In the Problem type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="257fd-119">Pasirinkite problemą, kuri buvo nustatyta atliekant tikrinimo procesą.</span><span class="sxs-lookup"><span data-stu-id="257fd-119">Select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="257fd-120">Lauke Problemos tipas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="257fd-120">In the Problem type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="257fd-121">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="257fd-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="257fd-122">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="257fd-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="257fd-123">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="257fd-123">Click OK.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="257fd-124">Neatitikties tvirtinimas / atmetimas</span><span class="sxs-lookup"><span data-stu-id="257fd-124">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="257fd-125">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="257fd-125">Click Functions.</span></span>
2. <span data-ttu-id="257fd-126">Spustelėkite Patvirtinti neatitiktį.</span><span class="sxs-lookup"><span data-stu-id="257fd-126">Click Approve non conformance.</span></span>
    * <span data-ttu-id="257fd-127">Šiuo atveju patvirtinkite neatitiktį.</span><span class="sxs-lookup"><span data-stu-id="257fd-127">For this example, approve the nonconformance.</span></span> <span data-ttu-id="257fd-128">Patvirtintas neatitiktis galima susieti su susijusiomis operacijomis, kad būtų įrašomas darbas, atliekamas tvarkant neatitiktį, ir įrašant užduotį kaip koregavimo apdorojimas.</span><span class="sxs-lookup"><span data-stu-id="257fd-128">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this task recording, the processing of correction handling.</span></span>  
3. <span data-ttu-id="257fd-129">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="257fd-129">Click Yes.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="257fd-130">Koregavimo veiksmo kūrimas</span><span class="sxs-lookup"><span data-stu-id="257fd-130">Create a correction action</span></span>
1. <span data-ttu-id="257fd-131">Spustelėkite Taisymai.</span><span class="sxs-lookup"><span data-stu-id="257fd-131">Click Corrections.</span></span>
2. <span data-ttu-id="257fd-132">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="257fd-132">Click New.</span></span>
3. <span data-ttu-id="257fd-133">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="257fd-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="257fd-134">Lauke Darbuotojo numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="257fd-134">In the Personnel number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="257fd-135">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="257fd-135">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="257fd-136">Spustelėkite Pažymėti.</span><span class="sxs-lookup"><span data-stu-id="257fd-136">Click Select.</span></span>
7. <span data-ttu-id="257fd-137">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="257fd-137">Click Attach.</span></span>
    * <span data-ttu-id="257fd-138">Sukurkite pastabą apie koregavimą.</span><span class="sxs-lookup"><span data-stu-id="257fd-138">Create a note about the correction.</span></span> <span data-ttu-id="257fd-139">Šiuo atveju veiksmas yra susisiekti su tiekėju ir aptarti neatitikties atvejį.</span><span class="sxs-lookup"><span data-stu-id="257fd-139">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
8. <span data-ttu-id="257fd-140">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="257fd-140">Click New.</span></span>
9. <span data-ttu-id="257fd-141">Spustelėkite Pastaba.</span><span class="sxs-lookup"><span data-stu-id="257fd-141">Click Note.</span></span>
    * <span data-ttu-id="257fd-142">Atkreipkite dėmesį, kad, priklausomai nuo ataskaitos nustatymų, skirtingus dokumentų tipus galima spausdinti ataskaitose, susijusiose su neatitikties valdymu.</span><span class="sxs-lookup"><span data-stu-id="257fd-142">Note that, depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
10. <span data-ttu-id="257fd-143">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="257fd-143">In the Description field, type a value.</span></span>
11. <span data-ttu-id="257fd-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="257fd-144">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="257fd-145">Koregavimo tvarkymas</span><span class="sxs-lookup"><span data-stu-id="257fd-145">Maintain a correction</span></span>
1. <span data-ttu-id="257fd-146">Spustelėkite Žymėjimas baigtas.</span><span class="sxs-lookup"><span data-stu-id="257fd-146">Click Mark complete.</span></span>
2. <span data-ttu-id="257fd-147">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="257fd-147">Click OK.</span></span>
3. <span data-ttu-id="257fd-148">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="257fd-148">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="257fd-149">Neatitikties uždarymas</span><span class="sxs-lookup"><span data-stu-id="257fd-149">Close a nonconformance</span></span>
1. <span data-ttu-id="257fd-150">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="257fd-150">Click Functions.</span></span>
2. <span data-ttu-id="257fd-151">Spustelėkite Uždaryti neatitiktį.</span><span class="sxs-lookup"><span data-stu-id="257fd-151">Click Close non conformance.</span></span>
3. <span data-ttu-id="257fd-152">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="257fd-152">Click Yes.</span></span>
4. <span data-ttu-id="257fd-153">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="257fd-153">Close the page.</span></span>
5. <span data-ttu-id="257fd-154">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="257fd-154">Close the page.</span></span>
