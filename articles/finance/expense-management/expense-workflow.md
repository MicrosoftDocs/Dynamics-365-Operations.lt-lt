---
title: Išlaidų valdymo darbo eiga
description: Šioje temoje paaiškinama, kaip, naudojant „Microsoft Dynamics 365 Finance“ darbo eigų sistemą, modulyje Išlaidų valdymas galima nustatyti išlaidų ataskaitų peržiūros procesą.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/21/2020
ms.locfileid: "3153978"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="9fb3e-103">Išlaidų valdymo darbo eiga</span><span class="sxs-lookup"><span data-stu-id="9fb3e-103">Expense management workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9fb3e-104">Naudodami darbo eigų sistemą, modulyje Išlaidų valdymas galite nustatyti išlaidų ataskaitų peržiūros procesą.</span><span class="sxs-lookup"><span data-stu-id="9fb3e-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="9fb3e-105">Nustatę darbo eigą, naudojančią tolesnius kriterijus, galite nustatyti, kas tvirtina išlaidų ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="9fb3e-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="9fb3e-106">Darbuotojų ataskaitų hierarchija ir iš anksto nustatyti tvirtinimo limitai</span><span class="sxs-lookup"><span data-stu-id="9fb3e-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="9fb3e-107">Kelių lygių tvirtinimo funkcija, palaikanti laikinus tvirtintojus ir galutinį tvirtintoją</span><span class="sxs-lookup"><span data-stu-id="9fb3e-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="9fb3e-108">Finansinės dimensijos ir projekto atsakomybė</span><span class="sxs-lookup"><span data-stu-id="9fb3e-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="9fb3e-109">Priskyrimas konkretiems vartotojams ar vartotojų grupėms</span><span class="sxs-lookup"><span data-stu-id="9fb3e-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="9fb3e-110">Galima kurti išlaidų ataskaitų, kelionių paraiškų, avansų grynaisiais pinigais ir pridėtinės vertės mokesčio (PVM) susigrąžinimo darbo eigų tvirtinimus.</span><span class="sxs-lookup"><span data-stu-id="9fb3e-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="9fb3e-111">**Pavyzdys:**</span><span class="sxs-lookup"><span data-stu-id="9fb3e-111">**Example**</span></span>

<span data-ttu-id="9fb3e-112">Toliau pateiktas procesas yra išlaidų ataskaitos išlaidų valdymo darbo eigos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="9fb3e-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="9fb3e-113">Darbuotojas sukuria ir įrašo išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="9fb3e-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="9fb3e-114">Darbuotojas išlaidų ataskaitą pateikia tvirtinti.</span><span class="sxs-lookup"><span data-stu-id="9fb3e-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="9fb3e-115">Tvirtintojas identifikuojamas pagal taisykles, apibrėžtas nustatant darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="9fb3e-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="9fb3e-116">Tvirtintojas gauna pranešimą, kad išlaidų ataskaita paruošta tvirtinti.</span><span class="sxs-lookup"><span data-stu-id="9fb3e-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="9fb3e-117">Tvirtintojas peržiūri išlaidų ataskaitą ir patikrina, ar tenkinamos tolesnės sąlygos.</span><span class="sxs-lookup"><span data-stu-id="9fb3e-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="9fb3e-118">Išlaidos nepažeidžia jokių išlaidų strategijų.</span><span class="sxs-lookup"><span data-stu-id="9fb3e-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="9fb3e-119">Jei išlaidos pažeidžia strategiją, tvirtintojas patikrina, ar į išlaidų ataskaitą įtrauktas tinkamas verslo pagrindimas.</span><span class="sxs-lookup"><span data-stu-id="9fb3e-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="9fb3e-120">Prie išlaidų ataskaitos pridėti elektroniniai kvitai.</span><span class="sxs-lookup"><span data-stu-id="9fb3e-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="9fb3e-121">Tvirtintojas patvirtina išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="9fb3e-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="9fb3e-122">Išlaidų ataskaita priskiriama modulio Mokėtinos sumos koordinatoriui užregistruoti.</span><span class="sxs-lookup"><span data-stu-id="9fb3e-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="9fb3e-123">Atsižvelgiant į tai, ar sukonfigūruota automatinio registravimo funkcija, vykdomas vienas iš tolesnių veiksmų.</span><span class="sxs-lookup"><span data-stu-id="9fb3e-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="9fb3e-124">Jei automatinio registravimo funkcija sukonfigūruota, išlaidų ataskaita apdorojama mokėjimui atlikti, o išlaidų ataskaitos būsena atnaujinama.</span><span class="sxs-lookup"><span data-stu-id="9fb3e-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="9fb3e-125">Jei automatinio registravimo funkcija nesukonfigūruota, modulio Mokėtinos sumos koordinatorius patikrina, ar pateikti visi pradiniai kvitai ir ar jie sutampa su išlaidų ataskaitoje nurodytomis išlaidomis.</span><span class="sxs-lookup"><span data-stu-id="9fb3e-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="9fb3e-126">Taip pat reikia patikrinti, ar teisingi visi išlaidų ataskaitoje įvesti mokesčių kodai.</span><span class="sxs-lookup"><span data-stu-id="9fb3e-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="9fb3e-127">Patikrinus visus šiuos reikalavimus, išlaidų ataskaita registruojama.</span><span class="sxs-lookup"><span data-stu-id="9fb3e-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="9fb3e-128">Užregistravus išlaidų ataskaitą, autorizuojamas mokėjimas už išlaidų ataskaitos išlaidas ir darbuotojui išmokama kompensacija.</span><span class="sxs-lookup"><span data-stu-id="9fb3e-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>
