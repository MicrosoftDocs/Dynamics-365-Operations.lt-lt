---
title: Priežiūros biudžeto atnaujinimas
description: Šioje temoje aiškinama, kaip atnaujinti priežiūros biudžetą modulyje Turto valdymas.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 21aba6224bba98eb9bbb423847e123616003b5d9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253475"
---
# <a name="update-maintenance-budgets"></a><span data-ttu-id="024b0-103">Priežiūros biudžeto atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="024b0-103">Update maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="024b0-104">Puslapyje **Priežiūros biudžeto eilutės** rodomos visos biudžeto eilutės, kurios buvo sukurtos puslapyje **Priežiūros biudžetas** pasirinktame biudžete.</span><span class="sxs-lookup"><span data-stu-id="024b0-104">The **Maintenance budget lines** page shows all the budget lines that have been created for the budget that is selected on the **Maintenance budgets** page.</span></span> <span data-ttu-id="024b0-105">(Norėdami gauti daugiau informacijos žr. [Priežiūros biudžetų kūrimas](create-maintenance-budget.md).) Priežiūros biudžeto eilutes galite perskaičiuoti ir koreguoti tol, kol priežiūros biudžetas bus patvirtintas.</span><span class="sxs-lookup"><span data-stu-id="024b0-105">(For more information, see [Create maintenance budgets](create-maintenance-budget.md).) You can recalculate and adjust maintenance budget lines until the maintenance budget is approved.</span></span> <span data-ttu-id="024b0-106">Praėjus biudžeto laikotarpiui ir paskelbus išlaidas modulyje Turto valdymas biudžeto eilutes taip pat galite atnaujinti pagal faktines išlaidas.</span><span class="sxs-lookup"><span data-stu-id="024b0-106">After the budget period has passed, and costs have been posted in Asset Management, you can also update the budget lines with actual costs.</span></span>

## <a name="recalculate-a-maintenance-budget"></a><span data-ttu-id="024b0-107">Priežiūros biudžeto perskaičiavimas</span><span class="sxs-lookup"><span data-stu-id="024b0-107">Recalculate a maintenance budget</span></span>

<span data-ttu-id="024b0-108">Priežiūros biudžetą galite perskaičiuoti puslapyje **Priežiūros biudžeto eilutės**.</span><span class="sxs-lookup"><span data-stu-id="024b0-108">You can recalculate a maintenance budget on the **Maintenance budget lines** page.</span></span> <span data-ttu-id="024b0-109">Perskaičiuojant priežiūros biudžetą esamos biudžeto eilutės ištrinamos ir atliekami nauji skaičiavimai.</span><span class="sxs-lookup"><span data-stu-id="024b0-109">When you recalculate a maintenance budget, the existing budget lines are deleted, and a new calculation is done.</span></span>

1. <span data-ttu-id="024b0-110">Puslapyje **Priežiūros biudžeto eilutės** pasirinkite **Perskaičiuoti**.</span><span class="sxs-lookup"><span data-stu-id="024b0-110">On the **Maintenance budget lines** page, select **Recalculate**.</span></span>
2. <span data-ttu-id="024b0-111">Dialogo lange **Perskaičiuoti biudžetą** atlikite reikiamus pakeitimus naujam skaičiavimui, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="024b0-111">In the **Recalculate budget** dialog box, make the required changes for the new calculation, and then select **OK**.</span></span>

<span data-ttu-id="024b0-112">Atsižvelgiant į nustatytas reikšmes sukuriamos naujos biudžeto eilutės.</span><span class="sxs-lookup"><span data-stu-id="024b0-112">New budget lines are created according to the values that you set.</span></span>

## <a name="adjust-budget-lines"></a><span data-ttu-id="024b0-113">Biudžeto eilučių koregavimas</span><span class="sxs-lookup"><span data-stu-id="024b0-113">Adjust budget lines</span></span>

<span data-ttu-id="024b0-114">Vietoj viso priežiūros biudžeto perskaičiavimo galite koreguoti pasirinktas eilutes, susijusias su biudžeto išlaidomis.</span><span class="sxs-lookup"><span data-stu-id="024b0-114">Instead of recalculating the whole maintenance budget, you can adjust selected lines that are related to budget costs.</span></span>

1. <span data-ttu-id="024b0-115">Puslapyje **Priežiūros biudžeto eilutės** pasirinkite eilutes, dėl kurių norite atnaujinti biudžeto išlaidas.</span><span class="sxs-lookup"><span data-stu-id="024b0-115">On the **Maintenance budget lines** page, select the lines to update the budget cost for.</span></span>
2. <span data-ttu-id="024b0-116">Pasirinkite **Koreguoti**.</span><span class="sxs-lookup"><span data-stu-id="024b0-116">Select **Adjust**.</span></span>
3. <span data-ttu-id="024b0-117">Norėdami į pasirinktas eilutes įtraukti sumą, pažymėkite žymės langelį **Įtraukti išlaidas**, o tada lauke **Įtraukti reikšmę** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="024b0-117">To add an amount to the selected lines, select the **Add cost** check box, and then enter the value in the **Add value** field.</span></span>
4. <span data-ttu-id="024b0-118">Norėdami biudžeto išlaidas pasirinktose biudžeto eilutėse padauginti iš koeficiento, pažymėkite žymės langelį **Dauginti išlaidas**, o lauke **Dauginimo reikšmė** įveskite koeficientą.</span><span class="sxs-lookup"><span data-stu-id="024b0-118">To multiply the budget cost on the selected budget lines by a factor, select the **Multiply cost** check box, and enter the factor in the **Multiply value** field.</span></span>

    <span data-ttu-id="024b0-119">Pavyzdžiui, jei lauke **Dauginimo reikšmė** įvesite **1,2**, biudžeto išlaidos pasirinktose eilutėse padidės 20 procentų.</span><span class="sxs-lookup"><span data-stu-id="024b0-119">For example, if you enter **1.2** in the **Multiply value** field, you increase the budget cost on the selected lines by 20 percent.</span></span> <span data-ttu-id="024b0-120">Jei įvesite **0,7**, biudžeto išlaidos pasirinktose eilutėse sumažės 30 procentų.</span><span class="sxs-lookup"><span data-stu-id="024b0-120">If you enter **0.7**, you reduce the budget cost on the selected lines by 30 percent.</span></span>

5. <span data-ttu-id="024b0-121">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="024b0-121">Select **OK**.</span></span>

<span data-ttu-id="024b0-122">Pasirinktos biudžeto eilutės atnaujinamos pagal reikšmes, kurias nustatėte atlikdami 3 arba 4 veiksmą.</span><span class="sxs-lookup"><span data-stu-id="024b0-122">The selected budget lines are updated according to the values that you set in step 3 or 4.</span></span>

## <a name="update-actual-costs"></a><span data-ttu-id="024b0-123">Faktinių išlaidų atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="024b0-123">Update actual costs</span></span>

<span data-ttu-id="024b0-124">Praėjus biudžeto eilučių datoms ir paskelbus faktines išlaidas modulyje Turto valdymas galite atnaujinti priežiūros biudžeto faktines išlaidas.</span><span class="sxs-lookup"><span data-stu-id="024b0-124">After the dates on the budget lines have passed, and actual costs have been posted in Asset Management, you can update the actual costs on the maintenance budget.</span></span>

1. <span data-ttu-id="024b0-125">Puslapyje **Priežiūros biudžeto eilutės** pasirinkite **Atnaujinti išlaidas**.</span><span class="sxs-lookup"><span data-stu-id="024b0-125">On the **Maintenance budget lines** page, select **Update cost**.</span></span>
2. <span data-ttu-id="024b0-126">Dialogo lange **Apskaičiuoti faktines išlaidas** pažymėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="024b0-126">In the **Calculate actual cost** dialog box, select **OK**.</span></span>

<span data-ttu-id="024b0-127">Biudžeto eilučių laukai **Faktinės išlaidos** atnaujinami, jei buvo paskelbtos faktinės išlaidos.</span><span class="sxs-lookup"><span data-stu-id="024b0-127">The **Actual cost** fields on the budget lines are updated if actual costs have been posted.</span></span> <span data-ttu-id="024b0-128">Jei nuo tada, kai sukūrėte biudžetą, buvo sukurta naujų turto tipų, ir jei šie turto tipai buvo naudojami turtui, kuriam buvo sukurta darbo užsakymų ir paskelbtos susijusios išlaidos, gali būti sugeneruota naujų biudžeto eilučių.</span><span class="sxs-lookup"><span data-stu-id="024b0-128">New budget lines might be generated if new asset types have been created since you created the budget, and if those asset types have been used on assets that work orders have been created for and related costs have been posted for.</span></span> <span data-ttu-id="024b0-129">Naujose biudžeto eilutėse rodomos tik faktinės išlaidos, nes šiose eilutėse nebuvo apskaičiuotos biudžeto išlaidos.</span><span class="sxs-lookup"><span data-stu-id="024b0-129">New budget lines show only actual costs, because no budget costs were calculated for them.</span></span>

> [!NOTE]
> <span data-ttu-id="024b0-130">Norėdami peržiūrėti faktinių išlaidų, padalytų į prevencines, korekcines ir investavimo išlaidas, apžvalgą, puslapyje **Turto išlaidų valdymas** galite atlikti skaičiavimą pagal tą patį laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="024b0-130">To see an overview of actual costs divided into preventive, corrective, and investment costs, you can do a calculation for the same period on the **Asset cost control** page.</span></span> 

## <a name="manually-add-budget-lines"></a><span data-ttu-id="024b0-131">Biudžeto eilučių įtraukimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="024b0-131">Manually add budget lines</span></span>

<span data-ttu-id="024b0-132">Puslapyje **Priežiūros biudžeto eilutės** galite rankiniu būdu įtraukti naują priežiūros eilutę pasirinkdami **Nauja**, o tada pasirinkdami atitinkamas parinktis eilutėje.</span><span class="sxs-lookup"><span data-stu-id="024b0-132">On the **Maintenance budget lines** page, you can manually add a new budget line by selecting **New** and then making selections on the line.</span></span> <span data-ttu-id="024b0-133">Toliau pateikiame kelis situacijų, kuriose toks metodas gali būti naudingas, pavyzdžius.</span><span class="sxs-lookup"><span data-stu-id="024b0-133">Here are some examples of situations where this approach might be useful:</span></span>

- <span data-ttu-id="024b0-134">Žinote, kad planuojamas kai kurio turto atnaujinimas, tačiau modulyje Turto valdymas dar nėra sukurta susijusių užduočių.</span><span class="sxs-lookup"><span data-stu-id="024b0-134">You know that refurbishment of some assets is currently in the planning phase, but related jobs haven't yet been created in Asset Management.</span></span> <span data-ttu-id="024b0-135">Tačiau norite, kad šių užduočių biudžeto išlaidos būtų įtrauktos į priežiūros biudžetą.</span><span class="sxs-lookup"><span data-stu-id="024b0-135">However, you want budget costs for those jobs to be included in the maintenance budget.</span></span>
- <span data-ttu-id="024b0-136">Nuo tada, kai sudarėte priežiūros biudžetą, buvo sukurta naujo turto ar turto tipų, tačiau dar nėra nustatyta šio turto ar turto tipų priežiūros planų.</span><span class="sxs-lookup"><span data-stu-id="024b0-136">New assets or asset types have been created since you made the maintenance budget, but maintenance plans haven't yet been set up on those assets or asset types.</span></span> <span data-ttu-id="024b0-137">Tačiau norite, kad šių turto tipų išlaidos būtų įtrauktos į priežiūros biudžetą.</span><span class="sxs-lookup"><span data-stu-id="024b0-137">However, you want budget costs for those asset types to be included in the maintenance budget.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]