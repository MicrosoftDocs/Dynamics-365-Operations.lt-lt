---
title: Išskaitomo mokesčio nustatymas
description: Šioje temoje paaiškinama, kaip nustatyti dovanų korteles naudojant.
author: twheeloc
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10e7018c79e54841d0729636b08ad475a94d20d5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834739"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="b091d-103">Išskaitomo mokesčio nustatymas</span><span class="sxs-lookup"><span data-stu-id="b091d-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b091d-104">Šioje temoje paaiškinama, kaip nustatyti dovanų korteles naudojant.</span><span class="sxs-lookup"><span data-stu-id="b091d-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="b091d-105">*Withholding tax* yra tiekėjams taikomas mokestis, kurį taikant nesukuriama PVM operacijų.</span><span class="sxs-lookup"><span data-stu-id="b091d-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="b091d-106">Tiekėjas įsipareigoja sumokėti jo mokėjimams priskiriamą išskaitomą mokestį.</span><span class="sxs-lookup"><span data-stu-id="b091d-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="b091d-107">Todėl išskaitomą mokestį galima registruoti tik balanso arba įsipareigojimų sąskaitose.</span><span class="sxs-lookup"><span data-stu-id="b091d-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="b091d-108">Šis užduočių vadovas parodo, kaip nustatyti išskaitomą mokestį.</span><span class="sxs-lookup"><span data-stu-id="b091d-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="b091d-109">Pasirinkite **Mokestis > Netiesioginiai mokesčiai > Išskaitomas mokestis > Išskaitomo mokesčio kodai.**</span><span class="sxs-lookup"><span data-stu-id="b091d-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="b091d-110">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b091d-110">Select **New**.</span></span>
3. <span data-ttu-id="b091d-111">Lauke **Withholding tax code**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b091d-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="b091d-112">Lauke **Withholding tax name** įveskite išskaitomo mokesčio kodo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="b091d-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="b091d-113">Lauke **Main account** pasirinkite pagrindinę sąskaitą, kurioje registruoti išskaitomo mokesčio įsipareigojimus.</span><span class="sxs-lookup"><span data-stu-id="b091d-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="b091d-114">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b091d-114">Select **Save**.</span></span>
7. <span data-ttu-id="b091d-115">Produktų **Values** sąraše raskite ir pasirinkite norimą įrašą</span><span class="sxs-lookup"><span data-stu-id="b091d-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="b091d-116">Lauke **Value** įveskite procentinę dalį, naudojamą skaičiuoti išskaitomam mokesčiui.</span><span class="sxs-lookup"><span data-stu-id="b091d-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="b091d-117">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b091d-117">Select **Save**.</span></span>
10. <span data-ttu-id="b091d-118">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b091d-118">Close the page.</span></span>
11. <span data-ttu-id="b091d-119">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b091d-119">Select **Save**.</span></span>
12. <span data-ttu-id="b091d-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b091d-120">Close the page.</span></span>
13. <span data-ttu-id="b091d-121">Pasirinkite **Mokestis > Netiesioginiai mokesčiai > Išskaitomas mokestis > Išskaitomo mokesčio grupės.**</span><span class="sxs-lookup"><span data-stu-id="b091d-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="b091d-122">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b091d-122">Select **New**.</span></span>
15. <span data-ttu-id="b091d-123">Lauke **Withholding tax group** įveskite išskaitomo mokesčio grupės identifikatorių.</span><span class="sxs-lookup"><span data-stu-id="b091d-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="b091d-124">Lauke **Description** įveskite išskaitomo mokesčio grupės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="b091d-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="b091d-125">Lauke **Withholding tax code** pasirinkite išskaitomo mokesčio kodą.</span><span class="sxs-lookup"><span data-stu-id="b091d-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="b091d-126">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b091d-126">Select **Save**.</span></span>
19. <span data-ttu-id="b091d-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b091d-127">Close the page.</span></span>

