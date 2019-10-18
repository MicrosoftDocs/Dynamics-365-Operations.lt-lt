---
title: Išplėstinių taisyklių struktūrų kūrimas ir priskyrimas
description: Šioje temoje aiškinama, kaip sukurti ir priskirti išplėstinės taisyklės struktūrą prie sąskaitos struktūros.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cff07c13553ea140f537160da7f93820d5e3f77a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175551"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="43be0-103">Išplėstinių taisyklių struktūrų kūrimas ir priskyrimas</span><span class="sxs-lookup"><span data-stu-id="43be0-103">Create and assign advanced rule structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="43be0-104">Šioje temoje aiškinama, kaip sukurti ir priskirti išplėstinės taisyklės struktūrą prie sąskaitos struktūros.</span><span class="sxs-lookup"><span data-stu-id="43be0-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="43be0-105">Šiame vadove naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="43be0-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="43be0-106">Kurti išplėstinės taisyklės struktūrą</span><span class="sxs-lookup"><span data-stu-id="43be0-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="43be0-107">Eikite į **Naršymo sritis > Moduliai > Didžioji knyga > Sąskaitų planas > Struktūros > Išplėstinės taisyklės struktūros**.</span><span class="sxs-lookup"><span data-stu-id="43be0-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="43be0-108">Pasirinkite **Naujas**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="43be0-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="43be0-109">Lauke **Išplėstinės taisyklės struktūra** įveskite pavadinimą, aprašantį taisyklės struktūrą.</span><span class="sxs-lookup"><span data-stu-id="43be0-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="43be0-110">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="43be0-110">Select **OK**.</span></span>
5. <span data-ttu-id="43be0-111">Pasirinkite **Pridėti segmentą**.</span><span class="sxs-lookup"><span data-stu-id="43be0-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="43be0-112">Segmentų sąraše pasirinkite finansinę dimensiją.</span><span class="sxs-lookup"><span data-stu-id="43be0-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="43be0-113">Pavyzdžiui, **Parduotuvė**.</span><span class="sxs-lookup"><span data-stu-id="43be0-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="43be0-114">Pasirinkite **Pridėti segmentą**.</span><span class="sxs-lookup"><span data-stu-id="43be0-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="43be0-115">Pasirinkite **Aktyvinti**.</span><span class="sxs-lookup"><span data-stu-id="43be0-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="43be0-116">Išplėstinės taisyklės struktūros taikymas sąskaitos struktūrai</span><span class="sxs-lookup"><span data-stu-id="43be0-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="43be0-117">Eikite į **Naršymo sritis > Moduliai > Didžioji knyga > Sąskaitų planas > Struktūros > Sukonfigūruoti sąskaitų struktūras**.</span><span class="sxs-lookup"><span data-stu-id="43be0-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="43be0-118">Sąraše raskite ir pasirinkite sąskaitos struktūrą, kuriai norite taikyti išplėstinę taisyklę.</span><span class="sxs-lookup"><span data-stu-id="43be0-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="43be0-119">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="43be0-119">Select **Edit**.</span></span> <span data-ttu-id="43be0-120">Taip pat galite spustelėti **Išplėstinės taisyklės** ir jūs būsite paraginti pateikti sąskaitos struktūrą **juodraščio režimu**.</span><span class="sxs-lookup"><span data-stu-id="43be0-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="43be0-121">Pasirinkite **Išankstinis**.</span><span class="sxs-lookup"><span data-stu-id="43be0-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="43be0-122">Pasirinkite **Naujas**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="43be0-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="43be0-123">Lauke **Išplėstinė taisyklė** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="43be0-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="43be0-124">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="43be0-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="43be0-125">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="43be0-125">Select **Create**.</span></span>
9. <span data-ttu-id="43be0-126">Spustelėkite **Įtraukti naujų kriterijų**.</span><span class="sxs-lookup"><span data-stu-id="43be0-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="43be0-127">Lauke **Kur** pasirinkite pagrindinę sąskaitą arba finansinę dimensiją.</span><span class="sxs-lookup"><span data-stu-id="43be0-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="43be0-128">Lauke **Operatorius**, pasirinkite parinktį, pvz., **yra tarp** ir **apima**.</span><span class="sxs-lookup"><span data-stu-id="43be0-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="43be0-129">Lauke **Reikšmė** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="43be0-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="43be0-130">Lauke **per** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="43be0-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="43be0-131">Pasirinkite **Įtraukti** ir atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="43be0-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="43be0-132">Sąraše raskite išplėstinės taisyklės struktūrą, kurią norėsite naudoti, kai bus išpildyti įvesti kriterijai.</span><span class="sxs-lookup"><span data-stu-id="43be0-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="43be0-133">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="43be0-133">Select **Add**.</span></span>
17. <span data-ttu-id="43be0-134">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="43be0-134">Close the page.</span></span>
18. <span data-ttu-id="43be0-135">Pasirinkite **Aktyvinti**.</span><span class="sxs-lookup"><span data-stu-id="43be0-135">Select **Activate**.</span></span>

