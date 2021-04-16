---
title: Naujo produkto kūrimas
description: Šioje temoje aprašoma, kaip sukurti naują konfigūraciją.
author: ShylaThompson
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6d33a13920e1881cdc69ad7c100180d3b3b441d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820039"
---
# <a name="create-a-new-product"></a><span data-ttu-id="01eff-103">Naujo produkto kūrimas</span><span class="sxs-lookup"><span data-stu-id="01eff-103">Create a new product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="01eff-104">Šioje temoje aprašoma, kaip sukurti naują konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="01eff-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="01eff-105">Ją paprastai atlieka produkto kūrėjas.</span><span class="sxs-lookup"><span data-stu-id="01eff-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="01eff-106">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="01eff-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="01eff-107">Sukurti produktą</span><span class="sxs-lookup"><span data-stu-id="01eff-107">Create a product</span></span>
1. <span data-ttu-id="01eff-108">Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Produktai > Produktai**.</span><span class="sxs-lookup"><span data-stu-id="01eff-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="01eff-109">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="01eff-109">Select **New**.</span></span>
3. <span data-ttu-id="01eff-110">Lauke **Produkto numeris** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="01eff-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="01eff-111">Jei nenustatyta produkto numerio numeracija, ją reikia įvesti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="01eff-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="01eff-112">Lauke **Produkto gavimo kvitas** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="01eff-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="01eff-113">Produkto pavadinimas naudojamas kaip numatytasis paieškos pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="01eff-113">The product name defaults to the search name.</span></span> <span data-ttu-id="01eff-114">Prireikus tai galima keisti.</span><span class="sxs-lookup"><span data-stu-id="01eff-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="01eff-115">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="01eff-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="01eff-116">Dimensijų grupių nustatymas</span><span class="sxs-lookup"><span data-stu-id="01eff-116">Set up dimension groups</span></span>
1. <span data-ttu-id="01eff-117">Pasirinkę **Dimensijų grupės** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="01eff-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="01eff-118">Lauke **Saugojimo dimensijų grupė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="01eff-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="01eff-119">Saugojimo dimensijų grupe nustatoma, kurias produkto saugojimo dimensijas turite įvesti atlikdami kiekvieną operaciją ir kaip jis bus sekamas atsargose.</span><span class="sxs-lookup"><span data-stu-id="01eff-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="01eff-120">Lauke **Sekimo dimensijų grupė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="01eff-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="01eff-121">Sekimo dimensijų grupe nustatoma, kurias kiekvienos produkto operacijos sekimo dimensijas turite įvesti ir kaip jis bus tvarkomas atsargose.</span><span class="sxs-lookup"><span data-stu-id="01eff-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="01eff-122">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="01eff-122">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]