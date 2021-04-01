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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ae7b13f743336e01f17248c8d6492b31e8044ef
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222316"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="2c4a5-103">Išskaitomo mokesčio nustatymas</span><span class="sxs-lookup"><span data-stu-id="2c4a5-103">Set up withholding tax</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2c4a5-104">Šioje temoje paaiškinama, kaip nustatyti dovanų korteles naudojant.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="2c4a5-105">*Išskaitomas mokestis* yra tiekėjams taikomas mokestis, kurį taikant nesukuriama PVM operacijų.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="2c4a5-106">Tiekėjas įsipareigoja sumokėti jo mokėjimams priskiriamą išskaitomą mokestį.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="2c4a5-107">Todėl išskaitomą mokestį galima registruoti tik balanso arba įsipareigojimų sąskaitose.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="2c4a5-108">Šis užduočių vadovas parodo, kaip nustatyti išskaitomą mokestį.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="2c4a5-109">Pasirinkite **Mokestis > Netiesioginiai mokesčiai > Išskaitomas mokestis > Išskaitomo mokesčio kodai**.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="2c4a5-110">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-110">Select **New**.</span></span>
3. <span data-ttu-id="2c4a5-111">Lauke **Išskaitomo mokesčio kodas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="2c4a5-112">Lauke **Išskaitomo mokesčio pavadinimas** įveskite išskaitomo mokesčio kodo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="2c4a5-113">Lauke **Pagrindinė sąskaita** pasirinkite pagrindinę sąskaitą, kurioje registruoti išskaitomo mokesčio įsipareigojimus.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="2c4a5-114">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-114">Select **Save**.</span></span>
7. <span data-ttu-id="2c4a5-115">Produktų **Reikšmės** sąraše raskite ir pasirinkite norimą įrašą</span><span class="sxs-lookup"><span data-stu-id="2c4a5-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="2c4a5-116">Lauke **Reikšmė** įveskite procentinę dalį, naudojamą skaičiuoti išskaitomam mokesčiui.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="2c4a5-117">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-117">Select **Save**.</span></span>
10. <span data-ttu-id="2c4a5-118">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-118">Close the page.</span></span>
11. <span data-ttu-id="2c4a5-119">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-119">Select **Save**.</span></span>
12. <span data-ttu-id="2c4a5-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-120">Close the page.</span></span>
13. <span data-ttu-id="2c4a5-121">Pasirinkite **Mokestis > Netiesioginiai mokesčiai > Išskaitomas mokestis > Išskaitomo mokesčio grupės.**</span><span class="sxs-lookup"><span data-stu-id="2c4a5-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="2c4a5-122">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-122">Select **New**.</span></span>
15. <span data-ttu-id="2c4a5-123">Lauke **Išskaitomo mokesčio grupė** įveskite išskaitomo mokesčio grupės identifikatorių.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="2c4a5-124">Lauke **Aprašas** įveskite išskaitomo mokesčio grupės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="2c4a5-125">Lauke **Išskaitomo mokesčio kodas** pasirinkite išskaitomo mokesčio kodą.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="2c4a5-126">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-126">Select **Save**.</span></span>
19. <span data-ttu-id="2c4a5-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-127">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]