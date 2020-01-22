---
title: Kurti produkto paketo atributus
description: Ši procedūra nurodo, kaip sukurti paketo atributą, priskirti numatytosios vertės diapazonus ir į grupę įtraukti atributą.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d874b6b6e53164c00d9b4656d27b1060f4e3ba06
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934940"
---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="87a64-103">Kurti produkto paketo atributus</span><span class="sxs-lookup"><span data-stu-id="87a64-103">Create batch attributes for a product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="87a64-104">Ši procedūra nurodo, kaip sukurti paketo atributą, priskirti numatytosios vertės diapazonus ir į grupę įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="87a64-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="87a64-105">Ši procedūra sukurta naudojant demonstracinių duomenų įmonę USP2.</span><span class="sxs-lookup"><span data-stu-id="87a64-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="87a64-106">Pasirinkite Atsargų valdymas > Nustatymas > Paketas > Paketo atributai.</span><span class="sxs-lookup"><span data-stu-id="87a64-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="87a64-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="87a64-107">Click New.</span></span>
3. <span data-ttu-id="87a64-108">Lauke „Atributas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87a64-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="87a64-109">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87a64-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="87a64-110">Lauke „Atributo tipas“ pasirinkite „Trupmena“.</span><span class="sxs-lookup"><span data-stu-id="87a64-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="87a64-111">Ši procedūra naudoja trupmenos tipą, kad būtų galima naudoti dešimtaines reikšmes.</span><span class="sxs-lookup"><span data-stu-id="87a64-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="87a64-112">Galite pasirinkti kitus atributų tipus.</span><span class="sxs-lookup"><span data-stu-id="87a64-112">You can select other attribute types.</span></span> <span data-ttu-id="87a64-113">Jei pasirinksite išvardijimo tipą, turrėsite įvesti reikšmes išvardijimo sąraše ir tik tada galėsite įvesti reikšmę paskirties lauke.</span><span class="sxs-lookup"><span data-stu-id="87a64-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="87a64-114">Lauke „Mažmmiausias“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="87a64-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="87a64-115">Lauke „Didžiausias“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="87a64-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="87a64-116">Lauke „Padidinimas“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="87a64-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="87a64-117">Lauke „Paskirties vieta“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87a64-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="87a64-118">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="87a64-118">Click Save.</span></span>
11. <span data-ttu-id="87a64-119">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="87a64-119">Close the page.</span></span>
12. <span data-ttu-id="87a64-120">Pasirinkite Atsargų valdymas > Nustatymas > Paketas > Paketo atributų grupės.</span><span class="sxs-lookup"><span data-stu-id="87a64-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="87a64-121">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="87a64-121">Click New.</span></span>
14. <span data-ttu-id="87a64-122">Lauke „Atributų grupė“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87a64-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="87a64-123">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87a64-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="87a64-124">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="87a64-124">Click Save.</span></span>
17. <span data-ttu-id="87a64-125">Spustelėkite Grupuoti atributus.</span><span class="sxs-lookup"><span data-stu-id="87a64-125">Click Group attributes.</span></span>
18. <span data-ttu-id="87a64-126">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="87a64-126">Click New.</span></span>
19. <span data-ttu-id="87a64-127">Lauke „Atributas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="87a64-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="87a64-128">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="87a64-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="87a64-129">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="87a64-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="87a64-130">Į bet kurią grupę galima įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="87a64-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="87a64-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="87a64-131">Click Save.</span></span>
23. <span data-ttu-id="87a64-132">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="87a64-132">Close the page.</span></span>

