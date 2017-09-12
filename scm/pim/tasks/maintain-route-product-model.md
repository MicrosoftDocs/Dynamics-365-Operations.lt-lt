--- 
title: "Prižiūrėti produkto modelio maršrutą"
description: "Norint paleisti šią procedūrą, reikia, kad būtų produkto konfigūracijos modelis."
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 3f6bacc54664c32a7d42f2befc51c420e29ada56
ms.contentlocale: lt-lt
ms.lasthandoff: 07/28/2017

---
# <a name="maintain-a-route-for-a-product-model"></a><span data-ttu-id="1756c-103">Prižiūrėti produkto modelio maršrutą</span><span class="sxs-lookup"><span data-stu-id="1756c-103">Maintain a route for a product model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1756c-104">Norint paleisti šią procedūrą, reikia, kad būtų produkto konfigūracijos modelis.</span><span class="sxs-lookup"><span data-stu-id="1756c-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="1756c-105">Atliekant šią procedūrą naudojamas aukščiausios kokybės garsiakalbio modelis iš demonstracinės įmonės USMF.</span><span class="sxs-lookup"><span data-stu-id="1756c-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="1756c-106">Įtraukti maršruto operaciją</span><span class="sxs-lookup"><span data-stu-id="1756c-106">Add a route operation</span></span>
1. <span data-ttu-id="1756c-107">Spustelėkite Produkto varianto modelio aprašą.</span><span class="sxs-lookup"><span data-stu-id="1756c-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="1756c-108">Spustelėkite Produkto konfigūracijos modeliai.</span><span class="sxs-lookup"><span data-stu-id="1756c-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="1756c-109">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="1756c-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1756c-110">Šiai užduočiai pasirinkite aukščiausios kokybės garsiakalbio modelį.</span><span class="sxs-lookup"><span data-stu-id="1756c-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="1756c-111">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1756c-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="1756c-112">Išplėskite skyrių Maršruto operacijos.</span><span class="sxs-lookup"><span data-stu-id="1756c-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="1756c-113">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1756c-113">Click Add.</span></span>
7. <span data-ttu-id="1756c-114">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1756c-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="1756c-115">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1756c-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="1756c-116">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1756c-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="1756c-117">Įvesti maršruto operacijos informaciją</span><span class="sxs-lookup"><span data-stu-id="1756c-117">Enter route operation details</span></span>
1. <span data-ttu-id="1756c-118">Spustelėkite Maršruto operacijos informacija.</span><span class="sxs-lookup"><span data-stu-id="1756c-118">Click Route operation details.</span></span>
2. <span data-ttu-id="1756c-119">Lauke Operacija įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="1756c-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="1756c-120">Lauke Oper.</span><span class="sxs-lookup"><span data-stu-id="1756c-120">In the Oper.</span></span> <span data-ttu-id="1756c-121">Nr.</span><span class="sxs-lookup"><span data-stu-id="1756c-121">No.</span></span> <span data-ttu-id="1756c-122">įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="1756c-122">field, enter a number.</span></span>
    * <span data-ttu-id="1756c-123">Operacijų numeriai nustato maršruto seką.</span><span class="sxs-lookup"><span data-stu-id="1756c-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="1756c-124">Kiekviena maršruto operacijos ypatybė gali gauti statinę vertę arba būti susieta su atributas.</span><span class="sxs-lookup"><span data-stu-id="1756c-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="1756c-125">Susiejus su atributu, vertė bus nustatyta kaip konfigūracijos dalis.</span><span class="sxs-lookup"><span data-stu-id="1756c-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="1756c-126">Lauke Maršruto grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="1756c-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="1756c-127">Maršruto grupė nustato esminę įkainojimo, suvartojimą ir nustatymo elgseną.</span><span class="sxs-lookup"><span data-stu-id="1756c-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="1756c-128">Spustelėkite skirtuką Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="1756c-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="1756c-129">Spustelėkite skirtuką Laikas.</span><span class="sxs-lookup"><span data-stu-id="1756c-129">Click the Times tab.</span></span>
7. <span data-ttu-id="1756c-130">Proceso kiekis.</span><span class="sxs-lookup"><span data-stu-id="1756c-130">In the Process qty.</span></span> <span data-ttu-id="1756c-131">įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="1756c-131">field, enter a number.</span></span>
    * <span data-ttu-id="1756c-132">Nustatykite, kiek bus apdorojama vienos operacijos metu.</span><span class="sxs-lookup"><span data-stu-id="1756c-132">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="1756c-133">Lauke Valandos / laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="1756c-133">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="1756c-134">Įveskite laiko koeficientą.</span><span class="sxs-lookup"><span data-stu-id="1756c-134">Enter the time ratio.</span></span>  
9. <span data-ttu-id="1756c-135">Pažymėkite žymės langelį Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="1756c-135">Select the Set check box.</span></span>
10. <span data-ttu-id="1756c-136">Lauke Vykdymo laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="1756c-136">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="1756c-137">Nustatykite apdorojimo laiką, reikalingą apdoroti tą kiekį, kurį nurodėte.</span><span class="sxs-lookup"><span data-stu-id="1756c-137">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="1756c-138">Spustelėkite skirtuką Išteklių reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="1756c-138">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="1756c-139">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1756c-139">Click Add.</span></span>
13. <span data-ttu-id="1756c-140">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="1756c-140">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="1756c-141">Lauke Reikalavimų tipas pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="1756c-141">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="1756c-142">Nuspręskite, ar norite nurodyti konkrečius išteklius ar galimybes, kurias jie turi turėti.</span><span class="sxs-lookup"><span data-stu-id="1756c-142">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="1756c-143">Lauke Reikalavimai įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="1756c-143">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="1756c-144">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="1756c-144">Click OK.</span></span>


