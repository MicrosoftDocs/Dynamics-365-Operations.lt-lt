---
title: Įtraukti išraiškos apribojimą į produkto konfigūravimo modelį
description: Ši procedūra nurodo, kaip į produkto konfigūracijos modelį galima įtraukti naują apribojimo išraišką.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920886"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="cc63a-103">Įtraukti išraiškos apribojimą į produkto konfigūravimo modelį</span><span class="sxs-lookup"><span data-stu-id="cc63a-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cc63a-104">Ši procedūra nurodo, kaip į produkto konfigūracijos modelį galima įtraukti naują apribojimo išraišką.</span><span class="sxs-lookup"><span data-stu-id="cc63a-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="cc63a-105">Jame parodoma, kaip galima įgalioti, kad kampo apsauga turi būti taikoma garsiakalbiui, jei vartotojas pasirinko priekines metalo groteles.</span><span class="sxs-lookup"><span data-stu-id="cc63a-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="cc63a-106">Procedūros metu naudojamas aukščiausios klasės garsiakalbio komponentas demonstracinės įmonės USMF.</span><span class="sxs-lookup"><span data-stu-id="cc63a-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>

## <a name="create-an-expression-constraint"></a><span data-ttu-id="cc63a-107">Kaip sukurti išraiškos apribojimą</span><span class="sxs-lookup"><span data-stu-id="cc63a-107">Create an expression constraint</span></span>

1. <span data-ttu-id="cc63a-108">Eikite į **Produkto informacijos valdymas \> Produktai \> Produkto konfigūracijos modeliai**.</span><span class="sxs-lookup"><span data-stu-id="cc63a-108">Go to **Product information management \> Products \> Product configuration models**.</span></span>
3. <span data-ttu-id="cc63a-109">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="cc63a-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cc63a-110">Šiame pavyzdyje naudojamas aukščiausios klasės garsiakalbio modelis.</span><span class="sxs-lookup"><span data-stu-id="cc63a-110">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="cc63a-111">Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="cc63a-111">In the list, select the link in the selected row.</span></span>
5. <span data-ttu-id="cc63a-112">Išplėskite **skyrių** Apribojimai.</span><span class="sxs-lookup"><span data-stu-id="cc63a-112">Expand the **Constraints** section.</span></span>
6. <span data-ttu-id="cc63a-113">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="cc63a-113">Select **Add**.</span></span>
7. <span data-ttu-id="cc63a-114">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="cc63a-114">Select **Create**.</span></span>
8. <span data-ttu-id="cc63a-115">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="cc63a-115">In the **Name** field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="cc63a-116">Įvesti išraišką</span><span class="sxs-lookup"><span data-stu-id="cc63a-116">Enter expression</span></span>

1. <span data-ttu-id="cc63a-117">Pasirinkite **Redaguoti išraišką**.</span><span class="sxs-lookup"><span data-stu-id="cc63a-117">Select **Edit expression**.</span></span>
    * <span data-ttu-id="cc63a-118">Jei atrakinsite vartotojo sąsają užduočių įrašymo metu šiame etape, galite naudoti „IntelliSense“ ir simbolių sąrašą apribojimo išraiškai sukurti.</span><span class="sxs-lookup"><span data-stu-id="cc63a-118">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="cc63a-119">Lauke **„ConstraintBody“** įveskite, 'Implies[FrontGrill=="Metal", CornerProtection] '.</span><span class="sxs-lookup"><span data-stu-id="cc63a-119">In the **ConstraintBody** field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="cc63a-120">Šios išraiškos logika nurodo: jei priekyje grotelės yra metalinės, tada turi būti pasirinkta kampo apsaugos pasirinktis.</span><span class="sxs-lookup"><span data-stu-id="cc63a-120">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="cc63a-121">Pasirinkite **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="cc63a-121">Select **Validate**.</span></span>
    * <span data-ttu-id="cc63a-122">Patikrinimo funkcija patikrina apribojimo išraišką, ar joje nėra sintaksės klaidų.</span><span class="sxs-lookup"><span data-stu-id="cc63a-122">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="cc63a-123">Pasirinkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="cc63a-123">Select **Close**.</span></span>
5. <span data-ttu-id="cc63a-124">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="cc63a-124">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]