---
title: Kurti naują produktą
description: Šia užduotimi rodoma, kaip sukurti naują bendrai naudojamą produktą.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a603d89749242a4c6039ab83da286ec6ab727d8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548421"
---
# <a name="create-a-new-product"></a><span data-ttu-id="8b91a-103">Kurti naują produktą</span><span class="sxs-lookup"><span data-stu-id="8b91a-103">Create a new product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8b91a-104">Šia užduotimi rodoma, kaip sukurti naują bendrai naudojamą produktą.</span><span class="sxs-lookup"><span data-stu-id="8b91a-104">This task shows how to create a new shared product.</span></span> <span data-ttu-id="8b91a-105">Ją paprastai atlieka produkto kūrėjas.</span><span class="sxs-lookup"><span data-stu-id="8b91a-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="8b91a-106">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="8b91a-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="8b91a-107">Pasirinkite Produkto informacijos valdymas > Produktai > Produktai.</span><span class="sxs-lookup"><span data-stu-id="8b91a-107">Go to Product information management > Products > Products.</span></span>

## <a name="create-a-product"></a><span data-ttu-id="8b91a-108">Sukurti produktą</span><span class="sxs-lookup"><span data-stu-id="8b91a-108">Create a product</span></span>
1. <span data-ttu-id="8b91a-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="8b91a-109">Click New.</span></span>
2. <span data-ttu-id="8b91a-110">Lauke „Produkto numeris“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8b91a-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="8b91a-111">Jei nenustatyta produkto numerio numeracija, ją reikia įvesti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="8b91a-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
3. <span data-ttu-id="8b91a-112">Lauke Produkto pavadinimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8b91a-112">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="8b91a-113">Produkto pavadinimas naudojamas kaip numatytasis paieškos pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="8b91a-113">The product name defaults to the search name.</span></span> <span data-ttu-id="8b91a-114">Prireikus tai galima keisti.</span><span class="sxs-lookup"><span data-stu-id="8b91a-114">You can change this if needed.</span></span>  
4. <span data-ttu-id="8b91a-115">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="8b91a-115">Click OK.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="8b91a-116">Dimensijų grupių nustatymas</span><span class="sxs-lookup"><span data-stu-id="8b91a-116">Set up dimension groups</span></span>
1. <span data-ttu-id="8b91a-117">Spustelėdami „Dimensijų grupės“ atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="8b91a-117">Click Dimension groups to open the drop dialog.</span></span>
2. <span data-ttu-id="8b91a-118">Lauke Saugojimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8b91a-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="8b91a-119">Saugojimo dimensijų grupe nustatoma, kurias produkto saugojimo dimensijas turite įvesti atlikdami kiekvieną operaciją ir kaip jis bus sekamas atsargose.</span><span class="sxs-lookup"><span data-stu-id="8b91a-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="8b91a-120">Lauke Sekimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8b91a-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="8b91a-121">Sekimo dimensijų grupe nustatoma, kurias kiekvienos produkto operacijos sekimo dimensijas turite įvesti ir kaip jis bus tvarkomas atsargose.</span><span class="sxs-lookup"><span data-stu-id="8b91a-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="8b91a-122">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="8b91a-122">Click OK.</span></span>

