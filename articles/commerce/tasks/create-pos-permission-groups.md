---
title: EKA teisių grupių kūrimas
description: Šioje temoje aiškinama, kaip sukurti POS teisių grupę.
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ffc64fd39a390af3ca7110178ef0999527106dc
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141389"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="dc787-103">EKA teisių grupių kūrimas</span><span class="sxs-lookup"><span data-stu-id="dc787-103">Create POS permission groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc787-104">Šioje temoje aiškinama, kaip sukurti POS teisių grupę.</span><span class="sxs-lookup"><span data-stu-id="dc787-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="dc787-105">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USRT.</span><span class="sxs-lookup"><span data-stu-id="dc787-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="dc787-106">Ši užduotis skirta prekybos operacijų vadovo vaidmeniui.</span><span class="sxs-lookup"><span data-stu-id="dc787-106">This task is intended for the Commerce operations manager role.</span></span>

1. <span data-ttu-id="dc787-107">Naršymo srityje eikite į **Moduliai > Mažmeninė prekyba ir prekyba > Darbuotojai > Teisių grupės**.</span><span class="sxs-lookup"><span data-stu-id="dc787-107">In the navigation pane, go to **Modules > Retail and Commerce > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="dc787-108">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="dc787-108">Select **New**.</span></span>
3. <span data-ttu-id="dc787-109">Lauke **POS teisių grupės ID** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="dc787-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="dc787-110">Lauke **Aprašo laukas**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="dc787-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="dc787-111">Pažymėkite **Taip** lauke **Peržiūrėti laiko laikrodžio įrašus**.</span><span class="sxs-lookup"><span data-stu-id="dc787-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="dc787-112">Dabar galite įjungti arba uždrausti įvairias savo EKA teisių grupės teises.</span><span class="sxs-lookup"><span data-stu-id="dc787-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="dc787-113">Galite nustatyti kai kurių teisių reikšmę, kuri bus naudojama siekiant įvertinti, ar EKA vartotojas gali atlikti veiksmą.</span><span class="sxs-lookup"><span data-stu-id="dc787-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="dc787-114">Šiame užduočių vadove įjungiamos kelios teisės, kurias galima suteikti kasininkui.</span><span class="sxs-lookup"><span data-stu-id="dc787-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="dc787-115">Pažymėkite **Taip** lauke **Leisti kurti užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="dc787-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="dc787-116">Pažymėkite **Taip** lauke **Leisti redaguoti užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="dc787-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="dc787-117">Pažymėkite **Taip** lauke **Leisti nuskaityti užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="dc787-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="dc787-118">Pažymėkite **Taip** lauke **Leisti keisti slaptažodį**.</span><span class="sxs-lookup"><span data-stu-id="dc787-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="dc787-119">Pažymėkite **Taip** lauke **Leisti anoniminį uždarymą**.</span><span class="sxs-lookup"><span data-stu-id="dc787-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="dc787-120">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="dc787-120">Select **Save**.</span></span> <span data-ttu-id="dc787-121">Įrašius keitimus, reikia paleisti darbuotojų paskirstymo grafiką, kad keitimai būtų taikomi prekybos kanalams.</span><span class="sxs-lookup"><span data-stu-id="dc787-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to commerce channels.</span></span> 
12. <span data-ttu-id="dc787-122">Naršymo srityje eikite į **Moduliai > Žmogiškieji ištekliai > Darbai > Darbai**.</span><span class="sxs-lookup"><span data-stu-id="dc787-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="dc787-123">Dabar mes priskirsime EKA teisių grupę užduočiai.</span><span class="sxs-lookup"><span data-stu-id="dc787-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="dc787-124">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="dc787-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="dc787-125">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="dc787-125">Select **Edit**.</span></span>
15. <span data-ttu-id="dc787-126">Išplėskite skyrių **Darbų klasifikacija**.</span><span class="sxs-lookup"><span data-stu-id="dc787-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="dc787-127">Lauke EKA teisių grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="dc787-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="dc787-128">Visi darbuotojai su šios užduoties pareigomis naudos šios EKA teisių grupės parametrus, nebent darbuotojų EKA teisių nepaisoma pareigų lygyje.</span><span class="sxs-lookup"><span data-stu-id="dc787-128">All Workers in Positions for this Job will use this POS permission group's settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="dc787-129">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="dc787-129">Select **Save**.</span></span> <span data-ttu-id="dc787-130">Įrašius keitimus, reikia paleisti darbuotojų paskirstymo grafiką, kad keitimai būtų taikomi kanalams.</span><span class="sxs-lookup"><span data-stu-id="dc787-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to channels.</span></span>  

