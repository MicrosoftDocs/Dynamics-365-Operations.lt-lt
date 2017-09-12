---
title: "Biudžeto sukūrimas iš operacijų sąskaitų ir bendrųjų sąskaitų sumų"
description: "Šiame straipsnyje pateikta biudžetų kūrimo pagal bendrąsias sąskaitas proceso apžvalga. Jame taip pat paaiškinta, kaip įjungti bendrųjų sąskaitų biudžeto kontrolę, jei biudžeto kontrolė reikalinga."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: fd6dc5173fd37f0257c98c1a41f3e6ce40b5b680
ms.contentlocale: lt-lt
ms.lasthandoff: 06/29/2017


---

# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a><span data-ttu-id="41cae-104">Biudžeto sukūrimas iš operacijų sąskaitų ir bendrųjų sąskaitų sumų</span><span class="sxs-lookup"><span data-stu-id="41cae-104">Create a budget from transaction accounts and total accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="41cae-105">Šiame straipsnyje pateikta biudžetų kūrimo pagal bendrąsias sąskaitas proceso apžvalga.</span><span class="sxs-lookup"><span data-stu-id="41cae-105">This article provides an overview of the process for creating budgets based on total accounts.</span></span> <span data-ttu-id="41cae-106">Jame taip pat paaiškinta, kaip įjungti bendrųjų sąskaitų biudžeto kontrolę, jei biudžeto kontrolė reikalinga.</span><span class="sxs-lookup"><span data-stu-id="41cae-106">It also explains how to turn on budget control for total accounts, if budget control is required.</span></span>

<span data-ttu-id="41cae-107">Biudžeto plano ir biudžeto registro įrašų dokumentai leidžia sudaryti biudžetus pagrindinėse sąskaitose, kurių pagrindinės sąskaitos tipas yra **Bendra suma**.</span><span class="sxs-lookup"><span data-stu-id="41cae-107">Both budget plan and budget register entry documents allow for budgeting on main accounts that have a main account type of **Total**.</span></span> <span data-ttu-id="41cae-108">Faktines sumas galima registruoti tik pagrindinėse operacinėse sąskaitose.</span><span class="sxs-lookup"><span data-stu-id="41cae-108">Actuals can be posted only to transactional main accounts.</span></span> 

<span data-ttu-id="41cae-109">Periodiniam procesui **Generuoti biudžeto planą iš didžiosios knygos** skirtuke **Šaltinis** galite kaip kriterijų nurodyti pagrindinės sąskaitos tipą **Iš viso**.</span><span class="sxs-lookup"><span data-stu-id="41cae-109">For the **Generate budget plan from General ledger** periodic process, on the **Source** tab, you can specify the **Total** main account type as a criterion.</span></span> <span data-ttu-id="41cae-110">Tokiu atveju kiekviena bendros sumos pagrindinė sąskaita bus įtrauktas į tikslinį biudžeto planą ir suma bus lygi bendrai pasirinktų pagrindinių sąskaitų diapazono sumai.</span><span class="sxs-lookup"><span data-stu-id="41cae-110">In this case, each total main account will be included in the target budget plan, and the amount will equal the total amount of the range of selected main accounts.</span></span> 

<span data-ttu-id="41cae-111">Galite suaktyvinti **Bendra suma** tipo pagrindinių sąskaitų biudžeto kontrolę.</span><span class="sxs-lookup"><span data-stu-id="41cae-111">You can activate budget control for main accounts of the **Total** type.</span></span> <span data-ttu-id="41cae-112">Ši funkcija palaikoma naudojant biudžeto grupes.</span><span class="sxs-lookup"><span data-stu-id="41cae-112">This functionality is supported through the use of budget groups.</span></span> <span data-ttu-id="41cae-113">Kiekvienai bendros sumos pagrindinei sąskaitai biudžetas, kurį turi kontroliuoti biudžeto grupė, turi būti kuriamas puslapyje **Biudžeto kontrolės konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="41cae-113">For each total main account, the budget that should be controlled for a budget group must be created on the **Budget control configuration **page.</span></span> <span data-ttu-id="41cae-114">Jūsų nurodomi kriterijai turi apimti bendros sumos pagrindinę sąskaitą ir sąskaitų diapazoną.</span><span class="sxs-lookup"><span data-stu-id="41cae-114">The criteria that you specify must include the total main account and the range of accounts.</span></span> <span data-ttu-id="41cae-115">Norėdami paspartinti biudžeto grupių kūrimo procesą, galite pasinaudoti biudžeto kontrolės grupių duomenų objektu.</span><span class="sxs-lookup"><span data-stu-id="41cae-115">To speed up the process of creating budget groups, you can take advantage of the Budget control groups data entity.</span></span> 

<span data-ttu-id="41cae-116">Kai biudžetas naudojamas teikiant ataskaitas, pvz., finansines ataskaitas, bendrosios sąskaitos biudžeto sumą sudaro tokios sumos:</span><span class="sxs-lookup"><span data-stu-id="41cae-116">When a budget is used in reporting, such as on a financial statement, the budget sum for the total account consists of the following amounts:</span></span>

-   <span data-ttu-id="41cae-117">Biudžetai, kurie sukurti iš kiekvienos operacijos DK sąskaitos, patenkantys į bendrosios sąskaitos intervalą.</span><span class="sxs-lookup"><span data-stu-id="41cae-117">The budgets that are created from each transaction ledger account in the interval of the total account.</span></span>
-   <span data-ttu-id="41cae-118">Biudžeto suma, kuri įvedama tiesiai į bendrąją sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="41cae-118">The budget amount that is entered directly on the total account.</span></span>

<span data-ttu-id="41cae-119">Todėl galite kurti atskirus svarbiausių operacijų sąskaitų, patenkančių į bendrosios sąskaitos intervalą, biudžetus ir pridėti turimą biudžeto sumą prie bendrosios sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="41cae-119">Therefore, you can create separate budgets for the most significant transaction accounts in the interval of the total account, and then add the available budget amount to the total account.</span></span>




