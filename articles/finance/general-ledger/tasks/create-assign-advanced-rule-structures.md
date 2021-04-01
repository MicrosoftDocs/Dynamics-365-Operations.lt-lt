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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a7b9d0c20a49996b4c8d45b030d9e587818de3d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216550"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="d9919-103">Išplėstinių taisyklių struktūrų kūrimas ir priskyrimas</span><span class="sxs-lookup"><span data-stu-id="d9919-103">Create and assign advanced rule structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d9919-104">Šioje temoje aiškinama, kaip sukurti ir priskirti išplėstinės taisyklės struktūrą prie sąskaitos struktūros.</span><span class="sxs-lookup"><span data-stu-id="d9919-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="d9919-105">Šiame vadove naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="d9919-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="d9919-106">Kurti išplėstinės taisyklės struktūrą</span><span class="sxs-lookup"><span data-stu-id="d9919-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="d9919-107">Eikite į **Naršymo sritis > Moduliai > Didžioji knyga > Sąskaitų planas > Struktūros > Išplėstinės taisyklės struktūros**.</span><span class="sxs-lookup"><span data-stu-id="d9919-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="d9919-108">Pasirinkite **Naujas**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="d9919-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="d9919-109">Lauke **Išplėstinės taisyklės struktūra** įveskite pavadinimą, aprašantį taisyklės struktūrą.</span><span class="sxs-lookup"><span data-stu-id="d9919-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="d9919-110">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d9919-110">Select **OK**.</span></span>
5. <span data-ttu-id="d9919-111">Pasirinkite **Pridėti segmentą**.</span><span class="sxs-lookup"><span data-stu-id="d9919-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="d9919-112">Segmentų sąraše pasirinkite finansinę dimensiją.</span><span class="sxs-lookup"><span data-stu-id="d9919-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="d9919-113">Pavyzdžiui, **Parduotuvė**.</span><span class="sxs-lookup"><span data-stu-id="d9919-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="d9919-114">Pasirinkite **Pridėti segmentą**.</span><span class="sxs-lookup"><span data-stu-id="d9919-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="d9919-115">Pasirinkite **Aktyvinti**.</span><span class="sxs-lookup"><span data-stu-id="d9919-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="d9919-116">Išplėstinės taisyklės struktūros taikymas sąskaitos struktūrai</span><span class="sxs-lookup"><span data-stu-id="d9919-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="d9919-117">Eikite į **Naršymo sritis > Moduliai > Didžioji knyga > Sąskaitų planas > Struktūros > Sukonfigūruoti sąskaitų struktūras**.</span><span class="sxs-lookup"><span data-stu-id="d9919-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="d9919-118">Sąraše raskite ir pasirinkite sąskaitos struktūrą, kuriai norite taikyti išplėstinę taisyklę.</span><span class="sxs-lookup"><span data-stu-id="d9919-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="d9919-119">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="d9919-119">Select **Edit**.</span></span> <span data-ttu-id="d9919-120">Taip pat galite spustelėti **Išplėstinės taisyklės** ir jūs būsite paraginti pateikti sąskaitos struktūrą **juodraščio režimu**.</span><span class="sxs-lookup"><span data-stu-id="d9919-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="d9919-121">Pasirinkite **Išankstinis**.</span><span class="sxs-lookup"><span data-stu-id="d9919-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="d9919-122">Pasirinkite **Naujas**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="d9919-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="d9919-123">Lauke **Išplėstinė taisyklė** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d9919-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="d9919-124">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d9919-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="d9919-125">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="d9919-125">Select **Create**.</span></span>
9. <span data-ttu-id="d9919-126">Spustelėkite **Įtraukti naujų kriterijų**.</span><span class="sxs-lookup"><span data-stu-id="d9919-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="d9919-127">Lauke **Kur** pasirinkite pagrindinę sąskaitą arba finansinę dimensiją.</span><span class="sxs-lookup"><span data-stu-id="d9919-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="d9919-128">Lauke **Operatorius**, pasirinkite parinktį, pvz., **yra tarp** ir **apima**.</span><span class="sxs-lookup"><span data-stu-id="d9919-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="d9919-129">Lauke **Reikšmė** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d9919-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="d9919-130">Lauke **per** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d9919-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="d9919-131">Pasirinkite **Įtraukti** ir atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="d9919-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="d9919-132">Sąraše raskite išplėstinės taisyklės struktūrą, kurią norėsite naudoti, kai bus išpildyti įvesti kriterijai.</span><span class="sxs-lookup"><span data-stu-id="d9919-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="d9919-133">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="d9919-133">Select **Add**.</span></span>
17. <span data-ttu-id="d9919-134">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d9919-134">Close the page.</span></span>
18. <span data-ttu-id="d9919-135">Pasirinkite **Aktyvinti**.</span><span class="sxs-lookup"><span data-stu-id="d9919-135">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]