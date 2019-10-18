---
title: Įjungti uždelstą mokesčių skaičiavimą žurnale
description: Šioje temoje paaiškinama, kaip naudoti funkciją **Įjungti uždelstą mokesčių skaičiavimą žurnale** siekiant pagerinti mokesčių skaičiavimo efektyvumą, kai yra daug žurnalo eilučių.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178993"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a><span data-ttu-id="125bf-103">Įjungti uždelstą mokesčių skaičiavimą žurnale</span><span class="sxs-lookup"><span data-stu-id="125bf-103">Enable delayed tax calculation on journal</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="125bf-104">Šioje temoje paaiškinama, kaip naudoti funkciją **Įjungti uždelstą mokesčių skaičiavimą žurnale** siekiant pagerinti mokesčių skaičiavimo efektyvumą, kai yra daug žurnalo eilučių.</span><span class="sxs-lookup"><span data-stu-id="125bf-104">This topic explains how to use the **Enable delayed tax calculation on journal** feature to improve tax calculation performance when the volume of journal lines is huge.</span></span>

<span data-ttu-id="125bf-105">PVM skaičiavimo funkcija žurnale realiuoju laiku suaktyvinama, kai vartotojas atnaujina su mokesčiais susijusius laukus, pvz., PVM grupę / prekės PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="125bf-105">Current sales tax calculation behavior on journal is real-time triggered when user updates tax related fields, e.g. sales tax group/item sales tax group.</span></span> <span data-ttu-id="125bf-106">Atnaujinus bet kurią žurnalo eilutę, iš naujo apskaičiuojama visų žurnalo eilučių mokesčių suma.</span><span class="sxs-lookup"><span data-stu-id="125bf-106">Any update at journal line level will re-calculate tax amount on all journal lines.</span></span> <span data-ttu-id="125bf-107">Tai padeda vartotojui matyti apskaičiuotą mokesčių sumą realiu laiku, bet taip pat gali kelti našumo problemų, jei žurnalo eilučių yra daug.</span><span class="sxs-lookup"><span data-stu-id="125bf-107">It helps user to see real-time calculated tax amount but it could also bring performance issue if  the volume of journal lines is huge.</span></span>

<span data-ttu-id="125bf-108">Ši funkcija suteikia galimybę atidėti mokesčių skaičiavimą siekiant išspręsti našumo problemą.</span><span class="sxs-lookup"><span data-stu-id="125bf-108">This feature provides an option to delay tax calculation to solve performance issue.</span></span> <span data-ttu-id="125bf-109">Jei ši funkcija įjungta, mokesčių suma bus apskaičiuota tik tada, kai vartotojas spustels komandą „PVM“ komandą arba užregistruos žurnalą.</span><span class="sxs-lookup"><span data-stu-id="125bf-109">If this feature is turned on, tax amount will only be calculated when user clicks "Sales Tax" command or posts the journal.</span></span>

<span data-ttu-id="125bf-110">Vartotojas gali įjungti / išjungti parametrą trimis lygiais:</span><span class="sxs-lookup"><span data-stu-id="125bf-110">User can turn on/off the parameter at three levels:</span></span>
- <span data-ttu-id="125bf-111">Pagal juridinį subjektą</span><span class="sxs-lookup"><span data-stu-id="125bf-111">By legal entity</span></span>
- <span data-ttu-id="125bf-112">Pagal žurnalo pavadinimą</span><span class="sxs-lookup"><span data-stu-id="125bf-112">By journal name</span></span>
- <span data-ttu-id="125bf-113">Pagal žurnalo antraštę</span><span class="sxs-lookup"><span data-stu-id="125bf-113">By journal header</span></span>

<span data-ttu-id="125bf-114">Sistema kaip galutinę naudos žurnalo antraštėje esančią parametro reikšmę.</span><span class="sxs-lookup"><span data-stu-id="125bf-114">System will take the parameter value on journal header as final.</span></span> <span data-ttu-id="125bf-115">Parametro reikšmė žurnalo antraštėje bus gauta iš žurnalo pavadinimo.</span><span class="sxs-lookup"><span data-stu-id="125bf-115">Parameter value on journal header will be defaulted from journal name.</span></span> <span data-ttu-id="125bf-116">Parametro reikšmė žurnalo pavadinime bus gauta iš didžiosios knygos parametro sukuriant žurnalo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="125bf-116">Parameter value on journal name will be defaulted from general ledger parameter when the journal name is created.</span></span>

<span data-ttu-id="125bf-117">Jei šis parametras yra įjungtas, žurnalo laukai „Faktinė PVM suma“ ir „Apskaičiuota PVM suma“ bus paslėpti.</span><span class="sxs-lookup"><span data-stu-id="125bf-117">"Actual sales tax amount" and "Calculated sales tax amount" fields on journal will be hided if this parameter is turned on.</span></span> <span data-ttu-id="125bf-118">Taip daroma siekiant nesupainioti vartotojo, nes, prieš vartotojui suaktyvinant mokesčių skaičiavimą, rodoma šių dviejų laukų reikšmė visada bus 0.</span><span class="sxs-lookup"><span data-stu-id="125bf-118">The purpose is not to confuse user because the value of these two fields will always show 0 before user trigger the tax calculation.</span></span>

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a><span data-ttu-id="125bf-119">Įjungti uždelstą mokesčių skaičiavimą pagal juridinį subjektą</span><span class="sxs-lookup"><span data-stu-id="125bf-119">Enable delayed tax calculation by legal entity</span></span>

1. <span data-ttu-id="125bf-120">Eikite į **Didžioji knyga > DK nustatymas > DK parametrai**</span><span class="sxs-lookup"><span data-stu-id="125bf-120">Go to **General ledger > Ledger setup > General ledger parameters**</span></span>
2. <span data-ttu-id="125bf-121">Spustelėkite kortelę **PVM**</span><span class="sxs-lookup"><span data-stu-id="125bf-121">Click **Sales tax** tab</span></span>
3. <span data-ttu-id="125bf-122">Sparčiajame skirtuke **Bendra** suraskite parametrą **Uždelstas mokesčių skaičiavimas** ir jį įjunkite arba išjunkite</span><span class="sxs-lookup"><span data-stu-id="125bf-122">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a><span data-ttu-id="125bf-123">Įjungti uždelstą mokesčių skaičiavimą pagal žurnalo pavadinimą</span><span class="sxs-lookup"><span data-stu-id="125bf-123">Enable delayed tax calculation by journal name</span></span>

1. <span data-ttu-id="125bf-124">Eikite į **Didžioji knyga > Žurnalo nustatymas > Žurnalo pavadinimai**</span><span class="sxs-lookup"><span data-stu-id="125bf-124">Go to **General ledger > Journal setup > Journal names**</span></span>
2. <span data-ttu-id="125bf-125">Sparčiajame skirtuke **Bendra** suraskite parametrą **Uždelstas mokesčių skaičiavimas** ir jį įjunkite arba išjunkite</span><span class="sxs-lookup"><span data-stu-id="125bf-125">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a><span data-ttu-id="125bf-126">Įjungti uždelstą mokesčių skaičiavimą pagal žurnalą</span><span class="sxs-lookup"><span data-stu-id="125bf-126">Enable delayed tax calculation by journal</span></span>

1. <span data-ttu-id="125bf-127">Eikite į **Didžioji knyga > Žurnalo įrašai > Bendrieji žurnalai**</span><span class="sxs-lookup"><span data-stu-id="125bf-127">Go to **General ledger > Journal entries > General journals**</span></span>
2. <span data-ttu-id="125bf-128">Spustelėkite **Naujas**</span><span class="sxs-lookup"><span data-stu-id="125bf-128">Click **New**</span></span>
3. <span data-ttu-id="125bf-129">Pasirinkite žurnalo pavadinimą</span><span class="sxs-lookup"><span data-stu-id="125bf-129">Select a journal name</span></span>
4. <span data-ttu-id="125bf-130">Spustelėkite **Sąranka**</span><span class="sxs-lookup"><span data-stu-id="125bf-130">Click **Setup**</span></span>
5. <span data-ttu-id="125bf-131">Suraskite parametrą **Uždelstas mokesčių skaičiavimas** ir jį įjunkite arba išjunkite</span><span class="sxs-lookup"><span data-stu-id="125bf-131">Find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-header.png)
