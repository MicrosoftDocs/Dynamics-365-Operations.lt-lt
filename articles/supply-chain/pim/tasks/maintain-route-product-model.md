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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cc41f99085e5f30ae29edce296a5e3752cbabd33
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433450"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="9d080-103">Tvarkyti produkto modelio maršrutą</span><span class="sxs-lookup"><span data-stu-id="9d080-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9d080-104">Norint paleisti šią procedūrą, reikia, kad būtų produkto konfigūracijos modelis.</span><span class="sxs-lookup"><span data-stu-id="9d080-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="9d080-105">Atliekant šią procedūrą naudojamas aukščiausios kokybės garsiakalbio modelis iš demonstracinės įmonės USMF.</span><span class="sxs-lookup"><span data-stu-id="9d080-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="9d080-106">Įtraukti maršruto operaciją</span><span class="sxs-lookup"><span data-stu-id="9d080-106">Add a route operation</span></span>
1. <span data-ttu-id="9d080-107">Spustelėkite Produkto varianto modelio aprašą.</span><span class="sxs-lookup"><span data-stu-id="9d080-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="9d080-108">Spustelėkite Produkto konfigūracijos modeliai.</span><span class="sxs-lookup"><span data-stu-id="9d080-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="9d080-109">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="9d080-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9d080-110">Šiai užduočiai pasirinkite aukščiausios kokybės garsiakalbio modelį.</span><span class="sxs-lookup"><span data-stu-id="9d080-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="9d080-111">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="9d080-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9d080-112">Išplėskite skyrių Maršruto operacijos.</span><span class="sxs-lookup"><span data-stu-id="9d080-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="9d080-113">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="9d080-113">Click Add.</span></span>
7. <span data-ttu-id="9d080-114">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9d080-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="9d080-115">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9d080-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="9d080-116">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="9d080-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="9d080-117">Įvesti maršruto operacijos informaciją</span><span class="sxs-lookup"><span data-stu-id="9d080-117">Enter route operation details</span></span>
1. <span data-ttu-id="9d080-118">Spustelėkite Maršruto operacijos informacija.</span><span class="sxs-lookup"><span data-stu-id="9d080-118">Click Route operation details.</span></span>
2. <span data-ttu-id="9d080-119">Lauke Operacija įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="9d080-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="9d080-120">Lauke Oper.</span><span class="sxs-lookup"><span data-stu-id="9d080-120">In the Oper.</span></span> <span data-ttu-id="9d080-121">Nr.</span><span class="sxs-lookup"><span data-stu-id="9d080-121">No.</span></span> <span data-ttu-id="9d080-122">įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="9d080-122">field, enter a number.</span></span>
    * <span data-ttu-id="9d080-123">Operacijų numeriai nustato maršruto seką.</span><span class="sxs-lookup"><span data-stu-id="9d080-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="9d080-124">Kiekviena maršruto operacijos ypatybė gali gauti statinę vertę arba būti susieta su atributas.</span><span class="sxs-lookup"><span data-stu-id="9d080-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="9d080-125">Susiejus su atributu, vertė bus nustatyta kaip konfigūracijos dalis.</span><span class="sxs-lookup"><span data-stu-id="9d080-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="9d080-126">Lauke Maršruto grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="9d080-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="9d080-127">Maršruto grupė nustato esminę įkainojimo, suvartojimą ir nustatymo elgseną.</span><span class="sxs-lookup"><span data-stu-id="9d080-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="9d080-128">Spustelėkite skirtuką Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="9d080-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="9d080-129">Spustelėkite skirtuką Laikas.</span><span class="sxs-lookup"><span data-stu-id="9d080-129">Click the Times tab.</span></span>
7. <span data-ttu-id="9d080-130">Lauke Apdorojamas kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="9d080-130">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="9d080-131">Nustatykite, kiek bus apdorojama vienos operacijos metu.</span><span class="sxs-lookup"><span data-stu-id="9d080-131">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="9d080-132">Lauke Valandos / laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="9d080-132">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="9d080-133">Įveskite laiko koeficientą.</span><span class="sxs-lookup"><span data-stu-id="9d080-133">Enter the time ratio.</span></span>  
9. <span data-ttu-id="9d080-134">Pažymėkite žymės langelį Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="9d080-134">Select the Set check box.</span></span>
10. <span data-ttu-id="9d080-135">Lauke Vykdymo laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="9d080-135">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="9d080-136">Nustatykite apdorojimo laiką, reikalingą apdoroti tą kiekį, kurį nurodėte.</span><span class="sxs-lookup"><span data-stu-id="9d080-136">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="9d080-137">Spustelėkite skirtuką Išteklių reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="9d080-137">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="9d080-138">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="9d080-138">Click Add.</span></span>
13. <span data-ttu-id="9d080-139">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="9d080-139">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="9d080-140">Lauke Reikalavimų tipas pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="9d080-140">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="9d080-141">Nuspręskite, ar norite nurodyti konkrečius išteklius ar galimybes, kurias jie turi turėti.</span><span class="sxs-lookup"><span data-stu-id="9d080-141">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="9d080-142">Lauke Reikalavimai įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="9d080-142">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="9d080-143">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9d080-143">Click OK.</span></span>

