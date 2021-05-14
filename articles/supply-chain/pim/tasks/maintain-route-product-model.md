---
title: Tvarkyti produkto modelio maršrutą
description: Norint paleisti šią procedūrą, reikia, kad būtų produkto konfigūracijos modelis.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45c6b1e6e75645bb17ce4defa0bca0e6d2131b6e
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921270"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="a1d4a-103">Tvarkyti produkto modelio maršrutą</span><span class="sxs-lookup"><span data-stu-id="a1d4a-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a1d4a-104">Norint paleisti šią procedūrą, reikia, kad būtų produkto konfigūracijos modelis.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="a1d4a-105">Atliekant šią procedūrą naudojamas aukščiausios kokybės garsiakalbio modelis iš demonstracinės įmonės USMF.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>

## <a name="add-a-route-operation"></a><span data-ttu-id="a1d4a-106">Įtraukti maršruto operaciją</span><span class="sxs-lookup"><span data-stu-id="a1d4a-106">Add a route operation</span></span>

1. <span data-ttu-id="a1d4a-107">Eikite į **Produkto informacijos valdymas \> Produktai \> Produkto konfigūracijos modeliai**.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="a1d4a-108">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a1d4a-109">Šiai užduočiai pasirinkite aukščiausios kokybės garsiakalbio modelį.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-109">Select the High end speaker model for this exercise.</span></span>  
1. <span data-ttu-id="a1d4a-110">Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="a1d4a-111">Išplėskite skyrių **Maršruto operacijos**.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-111">Expand the **Route operations** section.</span></span>
1. <span data-ttu-id="a1d4a-112">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-112">Select **Add**.</span></span>
1. <span data-ttu-id="a1d4a-113">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="a1d4a-114">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="a1d4a-115">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-115">Select **Save**.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="a1d4a-116">Įvesti maršruto operacijos informaciją</span><span class="sxs-lookup"><span data-stu-id="a1d4a-116">Enter route operation details</span></span>

1. <span data-ttu-id="a1d4a-117">Pasirinkite **maršruto operacijos** informaciją.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-117">Select **Route operation details**.</span></span>
1. <span data-ttu-id="a1d4a-118">Lauke **Operacija** įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-118">In the **Operation** field, enter or select a value.</span></span>
1. <span data-ttu-id="a1d4a-119">Lauke **Oper. nr.**</span><span class="sxs-lookup"><span data-stu-id="a1d4a-119">In the **Oper. No.**</span></span> <span data-ttu-id="a1d4a-120">įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-120">field, enter a number.</span></span>
    * <span data-ttu-id="a1d4a-121">Operacijų numeriai nustato maršruto seką.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-121">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="a1d4a-122">Kiekviena maršruto operacijos ypatybė gali gauti statinę vertę arba būti susieta su atributas.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-122">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="a1d4a-123">Susiejus su atributu, vertė bus nustatyta kaip konfigūracijos dalis.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-123">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
1. <span data-ttu-id="a1d4a-124">Lauke **Maršruto grupė** įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-124">In the **Route group** field, enter or select a value.</span></span>
    * <span data-ttu-id="a1d4a-125">Maršruto grupė nustato esminę įkainojimo, suvartojimą ir nustatymo elgseną.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-125">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
1. <span data-ttu-id="a1d4a-126">Pasirinkite skirtuką **Nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-126">Select the **Setup** tab.</span></span>
1. <span data-ttu-id="a1d4a-127">Pasirinkite skirtuką **Laikas**.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-127">Select the **Times** tab.</span></span>
1. <span data-ttu-id="a1d4a-128">Lauke **Apdorojamas kiekis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-128">In the **Process qty.** field, enter a number.</span></span>
    * <span data-ttu-id="a1d4a-129">Nustatykite, kiek bus apdorojama vienos operacijos metu.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-129">Determine how many will be processed during one operation.</span></span>  
1. <span data-ttu-id="a1d4a-130">Lauke **Valandos/laikas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-130">In the **Hours/time** field, enter a number.</span></span>
    * <span data-ttu-id="a1d4a-131">Įveskite laiko koeficientą.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-131">Enter the time ratio.</span></span>  
1. <span data-ttu-id="a1d4a-132">Pažymėkite **Nustatyti** laukelį.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-132">Select the **Set** check box.</span></span>
1. <span data-ttu-id="a1d4a-133">Lauke **Vykdymo laikas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-133">In the **Run time** field, enter a number.</span></span>
    * <span data-ttu-id="a1d4a-134">Nustatykite apdorojimo laiką, reikalingą apdoroti tą kiekį, kurį nurodėte.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-134">Determine the processing time for the quantity that you have specified.</span></span>  
1. <span data-ttu-id="a1d4a-135">Pasirinkite skirtuką **Išteklių reikalavimai**.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-135">Select the **Resource requirements** tab.</span></span>
1. <span data-ttu-id="a1d4a-136">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-136">Select **Add**.</span></span>
1. <span data-ttu-id="a1d4a-137">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-137">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="a1d4a-138">Lauke **Reikalavimų tipas** pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-138">In the **Requirement type** field, select an option.</span></span>
    * <span data-ttu-id="a1d4a-139">Nuspręskite, ar norite nurodyti konkrečius išteklius ar galimybes, kurias jie turi turėti.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-139">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
1. <span data-ttu-id="a1d4a-140">Lauke **Reikalavimai** įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-140">In the **Requirement** field, enter or select a value.</span></span>
1. <span data-ttu-id="a1d4a-141">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a1d4a-141">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]