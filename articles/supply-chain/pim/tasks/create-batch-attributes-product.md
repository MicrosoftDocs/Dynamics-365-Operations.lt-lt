---
title: Kurti produkto paketo atributus
description: Ši procedūra nurodo, kaip sukurti paketo atributą, priskirti numatytosios vertės diapazonus ir į grupę įtraukti atributą.
author: ShylaThompson
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PdsBatchAttrib
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5deb35028ee499633fb6b0bb5155df2fd91e643a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820111"
---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="17d3d-103">Kurti produkto paketo atributus</span><span class="sxs-lookup"><span data-stu-id="17d3d-103">Create batch attributes for a product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="17d3d-104">Ši procedūra nurodo, kaip sukurti paketo atributą, priskirti numatytosios vertės diapazonus ir į grupę įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="17d3d-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="17d3d-105">Ši procedūra sukurta naudojant demonstracinių duomenų įmonę USP2.</span><span class="sxs-lookup"><span data-stu-id="17d3d-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="17d3d-106">Pasirinkite Atsargų valdymas > Nustatymas > Paketas > Paketo atributai.</span><span class="sxs-lookup"><span data-stu-id="17d3d-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="17d3d-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="17d3d-107">Click New.</span></span>
3. <span data-ttu-id="17d3d-108">Lauke „Atributas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="17d3d-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="17d3d-109">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="17d3d-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="17d3d-110">Lauke „Atributo tipas“ pasirinkite „Trupmena“.</span><span class="sxs-lookup"><span data-stu-id="17d3d-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="17d3d-111">Ši procedūra naudoja trupmenos tipą, kad būtų galima naudoti dešimtaines reikšmes.</span><span class="sxs-lookup"><span data-stu-id="17d3d-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="17d3d-112">Galite pasirinkti kitus atributų tipus.</span><span class="sxs-lookup"><span data-stu-id="17d3d-112">You can select other attribute types.</span></span> <span data-ttu-id="17d3d-113">Jei pasirinksite išvardijimo tipą, turėsite įvesti reikšmes išvardijimo sąraše ir tik tada galėsite įvesti reikšmę paskirties lauke.</span><span class="sxs-lookup"><span data-stu-id="17d3d-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="17d3d-114">Lauke „Mažiausias“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="17d3d-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="17d3d-115">Lauke „Didžiausias“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="17d3d-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="17d3d-116">Lauke „Padidinimas“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="17d3d-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="17d3d-117">Lauke „Paskirties vieta“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="17d3d-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="17d3d-118">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="17d3d-118">Click Save.</span></span>
11. <span data-ttu-id="17d3d-119">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="17d3d-119">Close the page.</span></span>
12. <span data-ttu-id="17d3d-120">Pasirinkite Atsargų valdymas > Nustatymas > Paketas > Paketo atributų grupės.</span><span class="sxs-lookup"><span data-stu-id="17d3d-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="17d3d-121">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="17d3d-121">Click New.</span></span>
14. <span data-ttu-id="17d3d-122">Lauke „Atributų grupė“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="17d3d-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="17d3d-123">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="17d3d-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="17d3d-124">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="17d3d-124">Click Save.</span></span>
17. <span data-ttu-id="17d3d-125">Spustelėkite Grupuoti atributus.</span><span class="sxs-lookup"><span data-stu-id="17d3d-125">Click Group attributes.</span></span>
18. <span data-ttu-id="17d3d-126">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="17d3d-126">Click New.</span></span>
19. <span data-ttu-id="17d3d-127">Lauke „Atributas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="17d3d-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="17d3d-128">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="17d3d-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="17d3d-129">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="17d3d-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="17d3d-130">Į bet kurią grupę galima įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="17d3d-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="17d3d-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="17d3d-131">Click Save.</span></span>
23. <span data-ttu-id="17d3d-132">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="17d3d-132">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]