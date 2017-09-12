--- 
title: "Įtraukti išraiškos apribojimą į produkto konfigūravimo modelį"
description: "Ši procedūra nurodo, kaip į produkto konfigūracijos modelį galima įtraukti naują apribojimo išraišką."
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8db46c5b8361c96745b440c0d0684e18c06a6c6f
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="f63c9-103">Įtraukti išraiškos apribojimą į produkto konfigūravimo modelį</span><span class="sxs-lookup"><span data-stu-id="f63c9-103">Add an expression constraint to a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f63c9-104">Ši procedūra nurodo, kaip į produkto konfigūracijos modelį galima įtraukti naują apribojimo išraišką.</span><span class="sxs-lookup"><span data-stu-id="f63c9-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="f63c9-105">Jame parodoma, kaip galima įgalioti, kad kampo apsauga turi būti taikoma garsiakalbiui, jei vartotojas pasirinko priekines metalo groteles.</span><span class="sxs-lookup"><span data-stu-id="f63c9-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="f63c9-106">Procedūros metu naudojamas aukščiausios klasės garsiakalbio komponentas demonstracinės įmonės USMF.</span><span class="sxs-lookup"><span data-stu-id="f63c9-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="f63c9-107">Kaip sukurti išraiškos apribojimą</span><span class="sxs-lookup"><span data-stu-id="f63c9-107">Create an expression constraint</span></span>
1. <span data-ttu-id="f63c9-108">Spustelėkite Produkto varianto modelio aprašą.</span><span class="sxs-lookup"><span data-stu-id="f63c9-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="f63c9-109">Spustelėkite Produkto konfigūracijos modeliai.</span><span class="sxs-lookup"><span data-stu-id="f63c9-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="f63c9-110">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f63c9-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f63c9-111">Šiame pavyzdyje naudojamas aukščiausios klasės garsiakalbio modelis.</span><span class="sxs-lookup"><span data-stu-id="f63c9-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="f63c9-112">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f63c9-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f63c9-113">Išplėskite skyrių Apribojimai.</span><span class="sxs-lookup"><span data-stu-id="f63c9-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="f63c9-114">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="f63c9-114">Click Add.</span></span>
7. <span data-ttu-id="f63c9-115">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="f63c9-115">Click Create.</span></span>
8. <span data-ttu-id="f63c9-116">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f63c9-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="f63c9-117">Įvesti išraišką</span><span class="sxs-lookup"><span data-stu-id="f63c9-117">Enter expression</span></span>
1. <span data-ttu-id="f63c9-118">Spustelėkite Redaguoti išraišką.</span><span class="sxs-lookup"><span data-stu-id="f63c9-118">Click Edit expression.</span></span>
    * <span data-ttu-id="f63c9-119">Jei atrakinsite vartotojo sąsają užduočių įrašymo metu šiame etape, galite naudoti „IntelliSense“ ir simbolių sąrašą apribojimo išraiškai sukurti.</span><span class="sxs-lookup"><span data-stu-id="f63c9-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="f63c9-120">Lauke „ConstraintBody“ įveskite 'Implies[FrontGrill=="Metal", CornerProtection]'.</span><span class="sxs-lookup"><span data-stu-id="f63c9-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="f63c9-121">Šios išraiškos logika nurodo: jei priekyje grotelės yra metalinės, tada turi būti pasirinkta kampo apsaugos pasirinktis.</span><span class="sxs-lookup"><span data-stu-id="f63c9-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="f63c9-122">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="f63c9-122">Click Validate.</span></span>
    * <span data-ttu-id="f63c9-123">Patikrinimo funkcija patikrina apribojimo išraišką, ar joje nėra sintaksės klaidų.</span><span class="sxs-lookup"><span data-stu-id="f63c9-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="f63c9-124">Spustelėkite Uždaryti.</span><span class="sxs-lookup"><span data-stu-id="f63c9-124">Click Close.</span></span>
5. <span data-ttu-id="f63c9-125">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f63c9-125">Click OK.</span></span>


