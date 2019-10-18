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
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185962"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="6df43-103">Išskaitomo mokesčio nustatymas</span><span class="sxs-lookup"><span data-stu-id="6df43-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6df43-104">Šioje temoje paaiškinama, kaip nustatyti dovanų korteles naudojant.</span><span class="sxs-lookup"><span data-stu-id="6df43-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="6df43-105">*Išskaitomas mokestis* yra tiekėjams taikomas mokestis, kurį taikant nesukuriama PVM operacijų.</span><span class="sxs-lookup"><span data-stu-id="6df43-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="6df43-106">Tiekėjas įsipareigoja sumokėti jo mokėjimams priskiriamą išskaitomą mokestį.</span><span class="sxs-lookup"><span data-stu-id="6df43-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="6df43-107">Todėl išskaitomą mokestį galima registruoti tik balanso arba įsipareigojimų sąskaitose.</span><span class="sxs-lookup"><span data-stu-id="6df43-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="6df43-108">Šis užduočių vadovas parodo, kaip nustatyti išskaitomą mokestį.</span><span class="sxs-lookup"><span data-stu-id="6df43-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="6df43-109">Pasirinkite **Mokestis > Netiesioginiai mokesčiai > Išskaitomas mokestis > Išskaitomo mokesčio kodai**.</span><span class="sxs-lookup"><span data-stu-id="6df43-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="6df43-110">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="6df43-110">Select **New**.</span></span>
3. <span data-ttu-id="6df43-111">Lauke **Išskaitomo mokesčio kodas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6df43-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="6df43-112">Lauke **Išskaitomo mokesčio pavadinimas** įveskite išskaitomo mokesčio kodo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="6df43-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="6df43-113">Lauke **Pagrindinė sąskaita** pasirinkite pagrindinę sąskaitą, kurioje registruoti išskaitomo mokesčio įsipareigojimus.</span><span class="sxs-lookup"><span data-stu-id="6df43-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="6df43-114">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="6df43-114">Select **Save**.</span></span>
7. <span data-ttu-id="6df43-115">Produktų **Reikšmės** sąraše raskite ir pasirinkite norimą įrašą</span><span class="sxs-lookup"><span data-stu-id="6df43-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="6df43-116">Lauke **Reikšmė** įveskite procentinę dalį, naudojamą skaičiuoti išskaitomam mokesčiui.</span><span class="sxs-lookup"><span data-stu-id="6df43-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="6df43-117">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="6df43-117">Select **Save**.</span></span>
10. <span data-ttu-id="6df43-118">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="6df43-118">Close the page.</span></span>
11. <span data-ttu-id="6df43-119">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="6df43-119">Select **Save**.</span></span>
12. <span data-ttu-id="6df43-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="6df43-120">Close the page.</span></span>
13. <span data-ttu-id="6df43-121">Pasirinkite **Mokestis > Netiesioginiai mokesčiai > Išskaitomas mokestis > Išskaitomo mokesčio grupės.**</span><span class="sxs-lookup"><span data-stu-id="6df43-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="6df43-122">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="6df43-122">Select **New**.</span></span>
15. <span data-ttu-id="6df43-123">Lauke **Išskaitomo mokesčio grupė** įveskite išskaitomo mokesčio grupės identifikatorių.</span><span class="sxs-lookup"><span data-stu-id="6df43-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="6df43-124">Lauke **Aprašas** įveskite išskaitomo mokesčio grupės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="6df43-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="6df43-125">Lauke **Išskaitomo mokesčio kodas** pasirinkite išskaitomo mokesčio kodą.</span><span class="sxs-lookup"><span data-stu-id="6df43-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="6df43-126">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="6df43-126">Select **Save**.</span></span>
19. <span data-ttu-id="6df43-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="6df43-127">Close the page.</span></span>

