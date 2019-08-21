---
title: Naujo produkto kūrimas
description: Šioje temoje aprašoma, kaip sukurti naują konfigūraciją.
author: ShylaThompson
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 722414eee1e738e1438bbb40dbd9b8ca606f9245
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844806"
---
# <a name="create-a-new-product"></a><span data-ttu-id="83f4f-103">Naujo produkto kūrimas</span><span class="sxs-lookup"><span data-stu-id="83f4f-103">Create a new product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="83f4f-104">Šioje temoje aprašoma, kaip sukurti naują konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="83f4f-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="83f4f-105">Ją paprastai atlieka produkto kūrėjas.</span><span class="sxs-lookup"><span data-stu-id="83f4f-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="83f4f-106">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="83f4f-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="83f4f-107">Sukurti produktą</span><span class="sxs-lookup"><span data-stu-id="83f4f-107">Create a product</span></span>
1. <span data-ttu-id="83f4f-108">Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Produktai > Produktai**.</span><span class="sxs-lookup"><span data-stu-id="83f4f-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="83f4f-109">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="83f4f-109">Select **New**.</span></span>
3. <span data-ttu-id="83f4f-110">Lauke **Produkto numeris** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="83f4f-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="83f4f-111">Jei nenustatyta produkto numerio numeracija, ją reikia įvesti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="83f4f-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="83f4f-112">Lauke **Produkto gavimo kvitas** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="83f4f-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="83f4f-113">Produkto pavadinimas naudojamas kaip numatytasis paieškos pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="83f4f-113">The product name defaults to the search name.</span></span> <span data-ttu-id="83f4f-114">Prireikus tai galima keisti.</span><span class="sxs-lookup"><span data-stu-id="83f4f-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="83f4f-115">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="83f4f-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="83f4f-116">Dimensijų grupių nustatymas</span><span class="sxs-lookup"><span data-stu-id="83f4f-116">Set up dimension groups</span></span>
1. <span data-ttu-id="83f4f-117">Pasirinkę **Dimensijų grupės** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="83f4f-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="83f4f-118">Lauke **Saugojimo dimensijų grupė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="83f4f-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="83f4f-119">Saugojimo dimensijų grupe nustatoma, kurias produkto saugojimo dimensijas turite įvesti atlikdami kiekvieną operaciją ir kaip jis bus sekamas atsargose.</span><span class="sxs-lookup"><span data-stu-id="83f4f-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="83f4f-120">Lauke **Sekimo dimensijų grupė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="83f4f-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="83f4f-121">Sekimo dimensijų grupe nustatoma, kurias kiekvienos produkto operacijos sekimo dimensijas turite įvesti ir kaip jis bus tvarkomas atsargose.</span><span class="sxs-lookup"><span data-stu-id="83f4f-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="83f4f-122">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="83f4f-122">Select **OK**.</span></span>

