---
title: Nustatyti išskaitomą mokestį
description: Išskaitomas mokestis yra tiekėjams taikomas mokestis, kurį taikant nesukuriama PVM operacijų.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 382b6332665af2491563960a75d498a4f007aba8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562793"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="4aad3-103">Nustatyti išskaitomą mokestį</span><span class="sxs-lookup"><span data-stu-id="4aad3-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4aad3-104">Išskaitomas mokestis yra tiekėjams taikomas mokestis, kurį taikant nesukuriama PVM operacijų.</span><span class="sxs-lookup"><span data-stu-id="4aad3-104">Withholding tax is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="4aad3-105">Tiekėjas įsipareigoja sumokėti jo mokėjimams priskiriamą išskaitomą mokestį.</span><span class="sxs-lookup"><span data-stu-id="4aad3-105">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="4aad3-106">Todėl išskaitomą mokestį galima registruoti tik balanso arba įsipareigojimų sąskaitose.</span><span class="sxs-lookup"><span data-stu-id="4aad3-106">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="4aad3-107">Šis užduočių vadovas parodo, kaip nustatyti išskaitomą mokestį.</span><span class="sxs-lookup"><span data-stu-id="4aad3-107">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="4aad3-108">Pasirinkite Mokestis > Netiesioginiai mokesčiai > Išskaitomas mokestis > Išskaitomo mokesčio kodai.</span><span class="sxs-lookup"><span data-stu-id="4aad3-108">Go to Tax > Indirect taxes > Withholding tax > Withholding tax codes.</span></span>
2. <span data-ttu-id="4aad3-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="4aad3-109">Click New.</span></span>
3. <span data-ttu-id="4aad3-110">Lauke Išskaitomo mokesčio kodas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4aad3-110">In the Withholding tax code field, type a value.</span></span>
4. <span data-ttu-id="4aad3-111">Lauke Išskaitomo mokesčio pavadinimas įveskite išskaitomo mokesčio kodo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="4aad3-111">In the Withholding tax name field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="4aad3-112">Lauke Pagrindinė sąskaita pasirinkite pagrindinę sąskaitą, kurioje registruoti išskaitomo mokesčio įsipareigojimus.</span><span class="sxs-lookup"><span data-stu-id="4aad3-112">In the Main account field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="4aad3-113">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4aad3-113">Click Save.</span></span>
7. <span data-ttu-id="4aad3-114">Spustelėkite Reikšmės.</span><span class="sxs-lookup"><span data-stu-id="4aad3-114">Click Values.</span></span>
8. <span data-ttu-id="4aad3-115">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="4aad3-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="4aad3-116">Lauke Reikšmė įveskite procentinę dalį, naudojamą skaičiuoti išskaitomam mokesčiui.</span><span class="sxs-lookup"><span data-stu-id="4aad3-116">In the Value field, enter a percentage used for the calculation of the withholding tax.</span></span>
10. <span data-ttu-id="4aad3-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4aad3-117">Click Save.</span></span>
11. <span data-ttu-id="4aad3-118">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4aad3-118">Close the page.</span></span>
12. <span data-ttu-id="4aad3-119">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4aad3-119">Click Save.</span></span>
13. <span data-ttu-id="4aad3-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4aad3-120">Close the page.</span></span>
14. <span data-ttu-id="4aad3-121">Pasirinkite Mokestis > Netiesioginiai mokesčiai > Išskaitomas mokestis > Išskaitomo mokesčio grupės.</span><span class="sxs-lookup"><span data-stu-id="4aad3-121">Go to Tax > Indirect taxes > Withholding tax > Withholding tax groups.</span></span>
15. <span data-ttu-id="4aad3-122">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="4aad3-122">Click New.</span></span>
16. <span data-ttu-id="4aad3-123">Lauke Išskaitomo mokesčio grupė įveskite išskaitomo mokesčio grupės identifikatorių.</span><span class="sxs-lookup"><span data-stu-id="4aad3-123">In the Withholding tax group field, enter the identifier of the withholding tax group.</span></span>
17. <span data-ttu-id="4aad3-124">Lauke Aprašas įveskite išskaitomo mokesčio grupės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="4aad3-124">In the Description field, enter the name of the withholding tax group.</span></span>
18. <span data-ttu-id="4aad3-125">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="4aad3-125">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="4aad3-126">Lauke Išskaitomo mokesčio kodas pasirinkite išskaitomo mokesčio kodą.</span><span class="sxs-lookup"><span data-stu-id="4aad3-126">In the Withholding tax code field, select the withholding tax code.</span></span>
20. <span data-ttu-id="4aad3-127">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="4aad3-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="4aad3-128">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4aad3-128">Click Save.</span></span>

