---
title: Tvarkyti produkto modelio maršrutą
description: Norint paleisti šią procedūrą, reikia, kad būtų produkto konfigūracijos modelis.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90ea3f65284cc97906002015c715d9f071202bdb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966835"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="95bbc-103">Tvarkyti produkto modelio maršrutą</span><span class="sxs-lookup"><span data-stu-id="95bbc-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="95bbc-104">Norint paleisti šią procedūrą, reikia, kad būtų produkto konfigūracijos modelis.</span><span class="sxs-lookup"><span data-stu-id="95bbc-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="95bbc-105">Atliekant šią procedūrą naudojamas aukščiausios kokybės garsiakalbio modelis iš demonstracinės įmonės USMF.</span><span class="sxs-lookup"><span data-stu-id="95bbc-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="95bbc-106">Įtraukti maršruto operaciją</span><span class="sxs-lookup"><span data-stu-id="95bbc-106">Add a route operation</span></span>
1. <span data-ttu-id="95bbc-107">Spustelėkite Produkto varianto modelio aprašą.</span><span class="sxs-lookup"><span data-stu-id="95bbc-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="95bbc-108">Spustelėkite Produkto konfigūracijos modeliai.</span><span class="sxs-lookup"><span data-stu-id="95bbc-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="95bbc-109">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="95bbc-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="95bbc-110">Šiai užduočiai pasirinkite aukščiausios kokybės garsiakalbio modelį.</span><span class="sxs-lookup"><span data-stu-id="95bbc-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="95bbc-111">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="95bbc-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="95bbc-112">Išplėskite skyrių Maršruto operacijos.</span><span class="sxs-lookup"><span data-stu-id="95bbc-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="95bbc-113">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="95bbc-113">Click Add.</span></span>
7. <span data-ttu-id="95bbc-114">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="95bbc-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="95bbc-115">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="95bbc-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="95bbc-116">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="95bbc-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="95bbc-117">Įvesti maršruto operacijos informaciją</span><span class="sxs-lookup"><span data-stu-id="95bbc-117">Enter route operation details</span></span>
1. <span data-ttu-id="95bbc-118">Spustelėkite Maršruto operacijos informacija.</span><span class="sxs-lookup"><span data-stu-id="95bbc-118">Click Route operation details.</span></span>
2. <span data-ttu-id="95bbc-119">Lauke Operacija įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="95bbc-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="95bbc-120">Lauke Oper.</span><span class="sxs-lookup"><span data-stu-id="95bbc-120">In the Oper.</span></span> <span data-ttu-id="95bbc-121">Nr.</span><span class="sxs-lookup"><span data-stu-id="95bbc-121">No.</span></span> <span data-ttu-id="95bbc-122">įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="95bbc-122">field, enter a number.</span></span>
    * <span data-ttu-id="95bbc-123">Operacijų numeriai nustato maršruto seką.</span><span class="sxs-lookup"><span data-stu-id="95bbc-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="95bbc-124">Kiekviena maršruto operacijos ypatybė gali gauti statinę vertę arba būti susieta su atributas.</span><span class="sxs-lookup"><span data-stu-id="95bbc-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="95bbc-125">Susiejus su atributu, vertė bus nustatyta kaip konfigūracijos dalis.</span><span class="sxs-lookup"><span data-stu-id="95bbc-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="95bbc-126">Lauke Maršruto grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="95bbc-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="95bbc-127">Maršruto grupė nustato esminę įkainojimo, suvartojimą ir nustatymo elgseną.</span><span class="sxs-lookup"><span data-stu-id="95bbc-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="95bbc-128">Spustelėkite skirtuką Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="95bbc-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="95bbc-129">Spustelėkite skirtuką Laikas.</span><span class="sxs-lookup"><span data-stu-id="95bbc-129">Click the Times tab.</span></span>
7. <span data-ttu-id="95bbc-130">Lauke Apdorojamas kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="95bbc-130">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="95bbc-131">Nustatykite, kiek bus apdorojama vienos operacijos metu.</span><span class="sxs-lookup"><span data-stu-id="95bbc-131">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="95bbc-132">Lauke Valandos / laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="95bbc-132">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="95bbc-133">Įveskite laiko koeficientą.</span><span class="sxs-lookup"><span data-stu-id="95bbc-133">Enter the time ratio.</span></span>  
9. <span data-ttu-id="95bbc-134">Pažymėkite žymės langelį Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="95bbc-134">Select the Set check box.</span></span>
10. <span data-ttu-id="95bbc-135">Lauke Vykdymo laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="95bbc-135">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="95bbc-136">Nustatykite apdorojimo laiką, reikalingą apdoroti tą kiekį, kurį nurodėte.</span><span class="sxs-lookup"><span data-stu-id="95bbc-136">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="95bbc-137">Spustelėkite skirtuką Išteklių reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="95bbc-137">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="95bbc-138">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="95bbc-138">Click Add.</span></span>
13. <span data-ttu-id="95bbc-139">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="95bbc-139">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="95bbc-140">Lauke Reikalavimų tipas pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="95bbc-140">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="95bbc-141">Nuspręskite, ar norite nurodyti konkrečius išteklius ar galimybes, kurias jie turi turėti.</span><span class="sxs-lookup"><span data-stu-id="95bbc-141">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="95bbc-142">Lauke Reikalavimai įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="95bbc-142">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="95bbc-143">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="95bbc-143">Click OK.</span></span>

