---
title: Garantijos sutartys
description: Šioje temoje paaiškintos garantijos sutartys modulyje Turto valdymas.
author: josaw1
manager: tfehr
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e9cbb9068101f3004179f338da18af0369190807
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215383"
---
# <a name="warranty-agreements"></a><span data-ttu-id="296d3-103">Garantijos sutartys</span><span class="sxs-lookup"><span data-stu-id="296d3-103">Warranty agreements</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="296d3-104">Modulyje Turto valdymas galite nustatyti garantijos sąlygas, kurias galima susieti su turtu ar jo tipu.</span><span class="sxs-lookup"><span data-stu-id="296d3-104">In Asset Management, you can set up warranty terms that can be connected to an asset or an asset type.</span></span> <span data-ttu-id="296d3-105">Garantijos sąlygos kuriamos konkrečiam laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="296d3-105">Warranty terms are created for a specific period.</span></span> <span data-ttu-id="296d3-106">Galima nustatyti visos arba dalinės apimties garantiją ir galite nustatyti sąlygas, susijusias su valandomis, išlaidomis bei prekėmis.</span><span class="sxs-lookup"><span data-stu-id="296d3-106">Warranty can be set up to provide full coverage or partial coverage, and you can set up terms that are related to hours, expenses, and items.</span></span>

<span data-ttu-id="296d3-107">Pirmasis veiksmas – sukurti turimas tiekėjų įrangai taikomas garantijos sutartis.</span><span class="sxs-lookup"><span data-stu-id="296d3-107">The first step is to create any vendor warranty agreements that you have for your equipment.</span></span> <span data-ttu-id="296d3-108">Tada garantijos sutartys pridedamos prie turto ar jo tipų.</span><span class="sxs-lookup"><span data-stu-id="296d3-108">You then attach warranty agreements to assets or asset types.</span></span> <span data-ttu-id="296d3-109">Tiekėjų garantijos sutartys naudojamos tik informaciniais tikslais.</span><span class="sxs-lookup"><span data-stu-id="296d3-109">Vendor warranty agreements are used only for informational purposes.</span></span> <span data-ttu-id="296d3-110">Jei prie turto nustatyta tiekėjo garantija, galite matyti turto garantijos apimties laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="296d3-110">If vendor warranty is set up on an asset, you can see the warranty coverage period on the asset.</span></span>

## <a name="create-a-warranty-agreement"></a><span data-ttu-id="296d3-111">Garantijos sutarties sukūrimas</span><span class="sxs-lookup"><span data-stu-id="296d3-111">Create a warranty agreement</span></span>

<span data-ttu-id="296d3-112">Garantijos sutartyje gali būti kelios eilutės, apimančios darbo valandų, išlaidų ir prekių garantiją.</span><span class="sxs-lookup"><span data-stu-id="296d3-112">A warranty agreement can include several agreement lines to cover the warranty for work hours, expenses, and items.</span></span>

1. <span data-ttu-id="296d3-113">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Turtas** \> **Garantija**.</span><span class="sxs-lookup"><span data-stu-id="296d3-113">Select **Asset management** \> **Setup** \> **Assets** \> **Warranty**.</span></span>
2. <span data-ttu-id="296d3-114">Pasirinkite **Naujas**, kad sukurtumėte produktą.</span><span class="sxs-lookup"><span data-stu-id="296d3-114">Select **New** to create a product.</span></span>
3. <span data-ttu-id="296d3-115">Lauke **Garantija** įveskite garantijos ID.</span><span class="sxs-lookup"><span data-stu-id="296d3-115">In the **Warranty** field, enter a warranty ID.</span></span>
4. <span data-ttu-id="296d3-116">Lauke **Pavadinimas** įveskite aprašomąjį pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="296d3-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="296d3-117">„FastTab“ **Išsami informacija** esančiame lauke **Turtas** rodomas aktyvių turto objektų, su kuriais naudojama garantijos sutartis, skaičius.</span><span class="sxs-lookup"><span data-stu-id="296d3-117">On the **Details** FastTab, the **Assets** field shows the number of active assets that use the warranty agreement.</span></span>

5. <span data-ttu-id="296d3-118">„FastTab“ konteineriuose **Valandų garantija** ir **Prekių garantija** atlikdami toliau nurodytus veiksmus, įtraukite eilutes, kurios turi būti garantijos sutartyje, susijusioje su valandomis ir prekėmis.</span><span class="sxs-lookup"><span data-stu-id="296d3-118">On the **Hour warranty** and **Item warranty** FastTabs, follow these steps to add lines that should be included in a warranty agreement that pertains to hours or items:</span></span>

    1. <span data-ttu-id="296d3-119">Pasirinkite **Įtraukti eilutę**, kad į garantiją įtrauktumėte naują sąlygą.</span><span class="sxs-lookup"><span data-stu-id="296d3-119">Select **Add line** to add a new condition to the warranty.</span></span> <span data-ttu-id="296d3-120">Lauke **Eilutė** automatiškai pagal eilės tvarką įvedamas eilutės numeris.</span><span class="sxs-lookup"><span data-stu-id="296d3-120">A sequential line number is automatically entered in the **Line** field.</span></span>
    2. <span data-ttu-id="296d3-121">Lauke **Laikotarpis** pasirinkite garantijos laikotarpio tipą.</span><span class="sxs-lookup"><span data-stu-id="296d3-121">In the **Period** field, select the type of warranty period.</span></span>
    3. <span data-ttu-id="296d3-122">Lauke **Intervalas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="296d3-122">In the **Interval** field, enter a number.</span></span> <span data-ttu-id="296d3-123">Šiame lauke nustatomas laikotarpių, kuriuos garantija turi galioti, skaičius.</span><span class="sxs-lookup"><span data-stu-id="296d3-123">This field defines the number of periods that the warranty should be valid for.</span></span>
    4. <span data-ttu-id="296d3-124">Lauke **Procentas** įveskite garantijos eilutės apimties procentinę dalį.</span><span class="sxs-lookup"><span data-stu-id="296d3-124">In the **Percent** field, enter the coverage percentage for the warranty line.</span></span> <span data-ttu-id="296d3-125">Ši procentinė dalis nurodo, kokia yra jūsų įmonės garantijos apimtis.</span><span class="sxs-lookup"><span data-stu-id="296d3-125">The percentage indicates how much is covered by your company.</span></span>

![Garantijos puslapis](media/01-warranty.png)
