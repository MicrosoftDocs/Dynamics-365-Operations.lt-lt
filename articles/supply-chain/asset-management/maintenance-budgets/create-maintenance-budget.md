---
title: Priežiūros biudžetų kūrimas
description: Šioje temoje aiškinama, kaip biudžetą priežiūros biudžetą turto valdyme.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 593a03e3317de5759427dfc61093530c4b7ef7e9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253499"
---
# <a name="create-maintenance-budgets"></a><span data-ttu-id="287fe-103">Priežiūros biudžetų kūrimas</span><span class="sxs-lookup"><span data-stu-id="287fe-103">Create maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 



<span data-ttu-id="287fe-104">Priežiūros biudžetai naudojami norint apžvelgti prevencinės priežiūros numatytus kaštus.</span><span class="sxs-lookup"><span data-stu-id="287fe-104">Maintenance budgets are used to provide an overview of expected costs for preventive maintenance.</span></span> <span data-ttu-id="287fe-105">Biudžeto eilutės apskaičiuojamos pagal priežiūros grafiko eilutes, kuriose nurodyta numatyta pradžios data biudžeto laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="287fe-105">Budget lines are calculated based on maintenance schedule lines that have an expected start date during the budget period.</span></span>

<span data-ttu-id="287fe-106">Priežiūros biudžetai pagrįsti kaštų tipais, kurie naudojami turto valdyme: **Prevencinis**, **Taisomasis** ir **Investicija**.</span><span class="sxs-lookup"><span data-stu-id="287fe-106">Maintenance budgets are based on the cost types that are used in Asset Management: **Preventive**, **Corrective**, and **Investment**.</span></span> <span data-ttu-id="287fe-107">Į aktyvų turtą, kuriam numatyta pakeitimo data biudžeto laikotarpiu ir susijusi pakeitimo vertė, įtraukti investicijų priežiūros biudžeto kaštai.</span><span class="sxs-lookup"><span data-stu-id="287fe-107">Budget costs for investment maintenance are included for active assets that have a replacement date during the budget period and a related replacement value.</span></span> <span data-ttu-id="287fe-108">Taisomosios priežiūros biudžeto kaštai yra įtraukti, jei buvusi taisymo data yra įtraukta į biudžeto skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="287fe-108">Budget costs for corrective maintenance are included if a past corrective date is included in the budget calculation.</span></span> <span data-ttu-id="287fe-109">Tokiu atveju taisomieji kaštai iš ankstesnio laikotarpio yra skaičiuojami tokiam pačiam laikotarpiui, kuriam skaičiuojate priežiūros biudžetą, ateityje.</span><span class="sxs-lookup"><span data-stu-id="287fe-109">In that case, corrective costs from an earlier period are calculated for the same future period that you calculate the maintenance budget for.</span></span>

## <a name="create-a-maintenance-budget"></a><span data-ttu-id="287fe-110">Priežiūros biudžeto kūrimas</span><span class="sxs-lookup"><span data-stu-id="287fe-110">Create a maintenance budget</span></span>

1. <span data-ttu-id="287fe-111">Pažymėkite **Turto valdymas** \> **Užklausos** \> **Priežiūros biudžetas** \> **Biudžetas**.</span><span class="sxs-lookup"><span data-stu-id="287fe-111">Select **Asset management** \> **Inquiries** \> **Maintenance budget** \> **Budget**.</span></span>
2. <span data-ttu-id="287fe-112">Pažymėkite **Kurti biudžetą**.</span><span class="sxs-lookup"><span data-stu-id="287fe-112">Select **Create budget**.</span></span>
3. <span data-ttu-id="287fe-113">Lauke **Priežiūros biudžetas** įveskite biudžeto ID.</span><span class="sxs-lookup"><span data-stu-id="287fe-113">In the **Maintenance budget** field, enter a budget ID.</span></span>
4. <span data-ttu-id="287fe-114">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="287fe-114">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="287fe-115">„FastTab“ **Laikotarpis** laukuose **Nuo datos** ir **Iki datos** įveskite biudžeto laikotarpio pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="287fe-115">On the **Period** FastTab, in the **From date** and **To date** fields, enter the start and end dates of the budget period.</span></span>
5. <span data-ttu-id="287fe-116">Norėdami įtraukti taisomojo biudžeto kaštus, kurie apskaičiuoti remiantis praėjusio laikotarpio faktiniais kaštais, lauke **Taisomasis nuo datos** įveskite laikotarpio, iš kurio turi būti įtrauktos šios išlaidos, pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="287fe-116">To include corrective budget costs that are calculated on the basis of actual costs from a previous period, in the **Corrective from date** field, enter the start date of the period that those costs should be included from.</span></span>
6. <span data-ttu-id="287fe-117">Atsižvelgiant į biudžetui taikomą išsamumo lygį, nustatykite tinkamas penkias parinktis „FastTabs“ **Grupuoti pagal**.</span><span class="sxs-lookup"><span data-stu-id="287fe-117">Depending on the level of detail that is required in the budget, set the relevant options on the five **Group by** FastTabs.</span></span>
7. <span data-ttu-id="287fe-118">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="287fe-118">Select **OK**.</span></span>
8. <span data-ttu-id="287fe-119">Pažymėkite **Biudžeto eilutės**, kad atidarytumėte puslapį **Priežiūros biudžeto eilutės**, kuriame galite peržiūrėti visas biudžeto eilutes, kurios buvo sukurtos laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="287fe-119">Select **Budget lines** to open **Maintenance budget lines** page, where you can view all the budget lines that have been created for the period.</span></span>
9. <span data-ttu-id="287fe-120">Norėdami patvirtinti biudžetą, pažymėkite jį puslapyje **Priežiūros biudžetai**, tada pažymėkite **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="287fe-120">To approve the budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="287fe-121">Tada dialogo lange **Patvirtinti biudžetą** pažymėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="287fe-121">Then, in the **Approve budget** dialog box, select **OK**.</span></span> <span data-ttu-id="287fe-122">Jūsų vardas yra įvedamas lauke **Patvirtini** puslapyje **Priežiūros biudžetai**.</span><span class="sxs-lookup"><span data-stu-id="287fe-122">Your name is entered in the **Approved by** field on the **Maintenance budgets** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="287fe-123">Patvirtinę priežiūros biudžetą, puslapyje **Priežiūros biudžeto eilutės** negalite perskaičiuoti arba koreguoti susijusių eilučių, nebent pirmiau pašalintumėte patvirtinimą.</span><span class="sxs-lookup"><span data-stu-id="287fe-123">After you've approved a maintenance budget, you can't recalculate or adjust the related lines on the **Maintenance budget lines** page unless you first remove the approval.</span></span> <span data-ttu-id="287fe-124">Norėdami pašalinti priežiūros biudžeto patvirtinimą, pažymėkite jį puslapyje **Priežiūros biudžetai**, tada pažymėkite **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="287fe-124">To remove the approval of a maintenance budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="287fe-125">Tada dialogo lange **Patvirtinti biudžetą** pažymėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="287fe-125">Then, in the **Approve budget** dialog box, select **OK**.</span></span>

![Priežiūros biudžetai](media/01-maintenance-budgets.png)

<span data-ttu-id="287fe-127">Taip pat galite kurti naują priežiūros biudžetą nukopijuodami esamą biudžetą.</span><span class="sxs-lookup"><span data-stu-id="287fe-127">You can also create a new maintenance budget by copying an existing budget.</span></span> <span data-ttu-id="287fe-128">Puslapyje **Priežiūros biudžetai** pažymėkite kopijuotiną biudžetą, tada pažymėkite **Kopijuoti**.</span><span class="sxs-lookup"><span data-stu-id="287fe-128">On the **Maintenance budgets** page, select the budget to copy, and then select **Copy**.</span></span> <span data-ttu-id="287fe-129">Šis metodas yra naudingas, jei, pavyzdžiui, sukūrėte vieno mėnesio biudžetą ir norite jį kopijuoti į kitus mėnesius.</span><span class="sxs-lookup"><span data-stu-id="287fe-129">This approach is useful if, for example, you've created a budget for one month and want to copy it to other months.</span></span>

> [!NOTE]
> <span data-ttu-id="287fe-130">Priežiūros biudžetas skaičiuoja tik tuos biudžeto kaštus, kurie pagrįsti priežiūros grafiko eilutėmis.</span><span class="sxs-lookup"><span data-stu-id="287fe-130">The maintenance budget calculates only budget costs based on maintenance schedule lines.</span></span> <span data-ttu-id="287fe-131">Norėdami apskaičiuoti faktiniu faktinius to paties laikotarpio kaštus, šį skaičiavimą galite atlikti puslapyje **Turto kaštų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="287fe-131">To calculate actual costs for the same period, you can do that calculation on the **Asset cost control** page.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]