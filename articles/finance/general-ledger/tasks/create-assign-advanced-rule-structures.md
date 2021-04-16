---
title: Išplėstinių taisyklių struktūrų kūrimas ir priskyrimas
description: Šioje temoje aiškinama, kaip sukurti ir priskirti išplėstinės taisyklės struktūrą prie sąskaitos struktūros.
author: aprilolson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b81e3cc169bf0164af0b9c4de4faeb936df6784
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837062"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="bb764-103">Išplėstinių taisyklių struktūrų kūrimas ir priskyrimas</span><span class="sxs-lookup"><span data-stu-id="bb764-103">Create and assign advanced rule structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bb764-104">Šioje temoje aiškinama, kaip sukurti ir priskirti išplėstinės taisyklės struktūrą prie sąskaitos struktūros.</span><span class="sxs-lookup"><span data-stu-id="bb764-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="bb764-105">Šiame vadove naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="bb764-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="bb764-106">Kurti išplėstinės taisyklės struktūrą</span><span class="sxs-lookup"><span data-stu-id="bb764-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="bb764-107">Eikite į **Naršymo sritis > Moduliai > Didžioji knyga > Sąskaitų planas > Struktūros > Išplėstinės taisyklės struktūros**.</span><span class="sxs-lookup"><span data-stu-id="bb764-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="bb764-108">Pasirinkite **Naujas**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="bb764-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="bb764-109">Lauke **Išplėstinės taisyklės struktūra** įveskite pavadinimą, aprašantį taisyklės struktūrą.</span><span class="sxs-lookup"><span data-stu-id="bb764-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="bb764-110">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="bb764-110">Select **OK**.</span></span>
5. <span data-ttu-id="bb764-111">Pasirinkite **Pridėti segmentą**.</span><span class="sxs-lookup"><span data-stu-id="bb764-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="bb764-112">Segmentų sąraše pasirinkite finansinę dimensiją.</span><span class="sxs-lookup"><span data-stu-id="bb764-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="bb764-113">Pavyzdžiui, **Parduotuvė**.</span><span class="sxs-lookup"><span data-stu-id="bb764-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="bb764-114">Pasirinkite **Pridėti segmentą**.</span><span class="sxs-lookup"><span data-stu-id="bb764-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="bb764-115">Pasirinkite **Aktyvinti**.</span><span class="sxs-lookup"><span data-stu-id="bb764-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="bb764-116">Išplėstinės taisyklės struktūros taikymas sąskaitos struktūrai</span><span class="sxs-lookup"><span data-stu-id="bb764-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="bb764-117">Eikite į **Naršymo sritis > Moduliai > Didžioji knyga > Sąskaitų planas > Struktūros > Sukonfigūruoti sąskaitų struktūras**.</span><span class="sxs-lookup"><span data-stu-id="bb764-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="bb764-118">Sąraše raskite ir pasirinkite sąskaitos struktūrą, kuriai norite taikyti išplėstinę taisyklę.</span><span class="sxs-lookup"><span data-stu-id="bb764-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="bb764-119">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="bb764-119">Select **Edit**.</span></span> <span data-ttu-id="bb764-120">Taip pat galite spustelėti **Išplėstinės taisyklės** ir jūs būsite paraginti pateikti sąskaitos struktūrą **juodraščio režimu**.</span><span class="sxs-lookup"><span data-stu-id="bb764-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="bb764-121">Pasirinkite **Išankstinis**.</span><span class="sxs-lookup"><span data-stu-id="bb764-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="bb764-122">Pasirinkite **Naujas**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="bb764-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="bb764-123">Lauke **Išplėstinė taisyklė** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bb764-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="bb764-124">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bb764-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="bb764-125">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="bb764-125">Select **Create**.</span></span>
9. <span data-ttu-id="bb764-126">Spustelėkite **Įtraukti naujų kriterijų**.</span><span class="sxs-lookup"><span data-stu-id="bb764-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="bb764-127">Lauke **Kur** pasirinkite pagrindinę sąskaitą arba finansinę dimensiją.</span><span class="sxs-lookup"><span data-stu-id="bb764-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="bb764-128">Lauke **Operatorius**, pasirinkite parinktį, pvz., **yra tarp** ir **apima**.</span><span class="sxs-lookup"><span data-stu-id="bb764-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="bb764-129">Lauke **Reikšmė** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bb764-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="bb764-130">Lauke **per** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bb764-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="bb764-131">Pasirinkite **Įtraukti** ir atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="bb764-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="bb764-132">Sąraše raskite išplėstinės taisyklės struktūrą, kurią norėsite naudoti, kai bus išpildyti įvesti kriterijai.</span><span class="sxs-lookup"><span data-stu-id="bb764-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="bb764-133">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="bb764-133">Select **Add**.</span></span>
17. <span data-ttu-id="bb764-134">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bb764-134">Close the page.</span></span>
18. <span data-ttu-id="bb764-135">Pasirinkite **Aktyvinti**.</span><span class="sxs-lookup"><span data-stu-id="bb764-135">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]