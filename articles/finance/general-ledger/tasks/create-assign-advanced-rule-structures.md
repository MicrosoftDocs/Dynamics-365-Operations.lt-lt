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
ms.openlocfilehash: e6a3f7d174c91e357dce8a19ab50a5cd42a85561
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968609"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="42c37-103">Išplėstinių taisyklių struktūrų kūrimas ir priskyrimas</span><span class="sxs-lookup"><span data-stu-id="42c37-103">Create and assign advanced rule structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="42c37-104">Šioje temoje aiškinama, kaip sukurti ir priskirti išplėstinės taisyklės struktūrą prie sąskaitos struktūros.</span><span class="sxs-lookup"><span data-stu-id="42c37-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="42c37-105">Šiame vadove naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="42c37-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="42c37-106">Kurti išplėstinės taisyklės struktūrą</span><span class="sxs-lookup"><span data-stu-id="42c37-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="42c37-107">Eikite į **Naršymo sritis > Moduliai > Didžioji knyga > Sąskaitų planas > Struktūros > Išplėstinės taisyklės struktūros**.</span><span class="sxs-lookup"><span data-stu-id="42c37-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="42c37-108">Pasirinkite **Naujas**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="42c37-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="42c37-109">Lauke **Išplėstinės taisyklės struktūra** įveskite pavadinimą, aprašantį taisyklės struktūrą.</span><span class="sxs-lookup"><span data-stu-id="42c37-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="42c37-110">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="42c37-110">Select **OK**.</span></span>
5. <span data-ttu-id="42c37-111">Pasirinkite **Pridėti segmentą**.</span><span class="sxs-lookup"><span data-stu-id="42c37-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="42c37-112">Segmentų sąraše pasirinkite finansinę dimensiją.</span><span class="sxs-lookup"><span data-stu-id="42c37-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="42c37-113">Pavyzdžiui, **Parduotuvė**.</span><span class="sxs-lookup"><span data-stu-id="42c37-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="42c37-114">Pasirinkite **Pridėti segmentą**.</span><span class="sxs-lookup"><span data-stu-id="42c37-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="42c37-115">Pasirinkite **Aktyvinti**.</span><span class="sxs-lookup"><span data-stu-id="42c37-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="42c37-116">Išplėstinės taisyklės struktūros taikymas sąskaitos struktūrai</span><span class="sxs-lookup"><span data-stu-id="42c37-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="42c37-117">Eikite į **Naršymo sritis > Moduliai > Didžioji knyga > Sąskaitų planas > Struktūros > Sukonfigūruoti sąskaitų struktūras**.</span><span class="sxs-lookup"><span data-stu-id="42c37-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="42c37-118">Sąraše raskite ir pasirinkite sąskaitos struktūrą, kuriai norite taikyti išplėstinę taisyklę.</span><span class="sxs-lookup"><span data-stu-id="42c37-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="42c37-119">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="42c37-119">Select **Edit**.</span></span> <span data-ttu-id="42c37-120">Taip pat galite spustelėti **Išplėstinės taisyklės** ir jūs būsite paraginti pateikti sąskaitos struktūrą **juodraščio režimu**.</span><span class="sxs-lookup"><span data-stu-id="42c37-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="42c37-121">Pasirinkite **Išankstinis**.</span><span class="sxs-lookup"><span data-stu-id="42c37-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="42c37-122">Pasirinkite **Naujas**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="42c37-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="42c37-123">Lauke **Išplėstinė taisyklė** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="42c37-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="42c37-124">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="42c37-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="42c37-125">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="42c37-125">Select **Create**.</span></span>
9. <span data-ttu-id="42c37-126">Spustelėkite **Įtraukti naujų kriterijų**.</span><span class="sxs-lookup"><span data-stu-id="42c37-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="42c37-127">Lauke **Kur** pasirinkite pagrindinę sąskaitą arba finansinę dimensiją.</span><span class="sxs-lookup"><span data-stu-id="42c37-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="42c37-128">Lauke **Operatorius**, pasirinkite parinktį, pvz., **yra tarp** ir **apima**.</span><span class="sxs-lookup"><span data-stu-id="42c37-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="42c37-129">Lauke **Reikšmė** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="42c37-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="42c37-130">Lauke **per** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="42c37-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="42c37-131">Pasirinkite **Įtraukti** ir atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="42c37-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="42c37-132">Sąraše raskite išplėstinės taisyklės struktūrą, kurią norėsite naudoti, kai bus išpildyti įvesti kriterijai.</span><span class="sxs-lookup"><span data-stu-id="42c37-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="42c37-133">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="42c37-133">Select **Add**.</span></span>
17. <span data-ttu-id="42c37-134">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="42c37-134">Close the page.</span></span>
18. <span data-ttu-id="42c37-135">Pasirinkite **Aktyvinti**.</span><span class="sxs-lookup"><span data-stu-id="42c37-135">Select **Activate**.</span></span>

