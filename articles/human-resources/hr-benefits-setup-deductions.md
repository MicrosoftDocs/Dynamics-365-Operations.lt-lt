---
title: Atskaitymų konfigūravimas
description: Naudokite atskaitymus programoje „Microsoft Dynamics 365 Human Resources“, siekdami nustatyti, kiek (jei bus atskaitoma) atskaityti iš kiekvienos darbuotojui mokamos išmokos.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7c59fa09e83ca91e0ad866e5875ff06370b7491d
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430698"
---
# <a name="configure-deductions"></a><span data-ttu-id="c0e8b-103">Atskaitymų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="c0e8b-103">Configure deductions</span></span>

<span data-ttu-id="c0e8b-104">Naudokite atskaitymus programoje „Microsoft Dynamics 365 Human Resources“, siekdami nustatyti, kiek (jei bus atskaitoma) atskaityti iš kiekvienos darbuotojui mokamos išmokos.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="c0e8b-105">Atskaitymai priklauso nuo datos, todėl galite turėti archyvinį atskaitymo informacijos įrašą.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-105">Deductions are date-effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="c0e8b-106">Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Atskaitymai**.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="c0e8b-107">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-107">Select **New**.</span></span>

3. <span data-ttu-id="c0e8b-108">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="c0e8b-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="c0e8b-109">Laukas</span><span class="sxs-lookup"><span data-stu-id="c0e8b-109">Field</span></span> | <span data-ttu-id="c0e8b-110">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="c0e8b-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c0e8b-111">**Atskaitymas**</span><span class="sxs-lookup"><span data-stu-id="c0e8b-111">**Deduction**</span></span> | <span data-ttu-id="c0e8b-112">Unikalus ID, naudojamas išmokos atskaitymui nustatyti.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="c0e8b-113">**Aprašymas**</span><span class="sxs-lookup"><span data-stu-id="c0e8b-113">**Description**</span></span> | <span data-ttu-id="c0e8b-114">Atskaitymo aprašas.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="c0e8b-115">**Galioja**</span><span class="sxs-lookup"><span data-stu-id="c0e8b-115">**Effective**</span></span> | <span data-ttu-id="c0e8b-116">Pradžios data.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-116">The start date.</span></span> <span data-ttu-id="c0e8b-117">Numatytoji vertė yra dabartinė sistemos data.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="c0e8b-118">**Galiojimo pabaiga**</span><span class="sxs-lookup"><span data-stu-id="c0e8b-118">**Expiration**</span></span> | <span data-ttu-id="c0e8b-119">Pabaigos datą.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-119">The end date.</span></span> <span data-ttu-id="c0e8b-120">Numatytoji reikšmė yra 2154-12-31, kuri reiškia, kad niekada.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="c0e8b-121">**Antraštė**</span><span class="sxs-lookup"><span data-stu-id="c0e8b-121">**Heading**</span></span> | <span data-ttu-id="c0e8b-122">Antraštės kodas iš algalapių sistemos, kurį šis atskaitymas naudos darbuotojo atskaitymo daliai, atliekant į algalapį įtraukiamų išmokų apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="c0e8b-123">Naudojamas, kai naudojate trečiosios šalies algalapio teikėją.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-123">This is used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="c0e8b-124">**Darbuotojo algalapio atskaitymo rekomendacija**</span><span class="sxs-lookup"><span data-stu-id="c0e8b-124">**Employee payroll deduction reference**</span></span> | <span data-ttu-id="c0e8b-125">Atskaitymo kodas iš algalapių sistemos, kurį šis atskaitymas naudos darbuotojo atskaitymo daliai, atliekant į algalapį įtraukiamų išmokų apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="c0e8b-126">**Sumos antraštė**</span><span class="sxs-lookup"><span data-stu-id="c0e8b-126">**Amount heading**</span></span> | <span data-ttu-id="c0e8b-127">Antraštės kodas iš algalapių sistemos, kurį ši atskaitymo suma naudos darbuotojo atskaitymo daliai, atliekant į algalapį įtraukiamų išmokų apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="c0e8b-128">Paprastai naudojamas, kai naudojate trečiosios šalies algalapio teikėją.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-128">This is normally used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="c0e8b-129">**Naikinti galima**</span><span class="sxs-lookup"><span data-stu-id="c0e8b-129">**Can delete**</span></span> | <span data-ttu-id="c0e8b-130">Nurodo, ar iš „Dynamics 365 for Finance and Operations“ eksportuota vertė gali panaikinti vertę algalapių sistemoje.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="c0e8b-131">**Suporuoti stulpeliai**</span><span class="sxs-lookup"><span data-stu-id="c0e8b-131">**Paired columns**</span></span> | <span data-ttu-id="c0e8b-132">Nurodo, ar eksportuoti antraštės ir atskaitymo sumą, esančią susietuose gretimuose stulpeliuose, į algalapio sistemą.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="c0e8b-133">**Keitimo įsigaliojimo data**</span><span class="sxs-lookup"><span data-stu-id="c0e8b-133">**Change effective date**</span></span> | <span data-ttu-id="c0e8b-134">Data, kai įsigalios išmokų atskaitymo pakeitimas.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="c0e8b-135">Šią dieną sistema automatiškai pakeičia išmokų atskaitymą ir atnaujina visus su šiuo atskaitymu susijusius išmokų planus, jei vykdysite **atskaitymo keitimo naujinimo** apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-135">On this date, the system automatically changes the benefit deduction and updates all benefit plans associated with this deduction, as long as you run **Deduction change update** processing.</span></span> |
   | <span data-ttu-id="c0e8b-136">**Atskaitymo pakeitimas atliktas**</span><span class="sxs-lookup"><span data-stu-id="c0e8b-136">**Deduction change completed**</span></span> | <span data-ttu-id="c0e8b-137">Žymimasis langelis **Atskaitymo pakeitimas atliktas** bus pasirenkamas automatiškai, kai išmokų atskaitymo pakeitimai bus užbaigti apdorojus atskaitymo pakeitimo atnaujinimą.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-137">The **Deduction change completed** check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="c0e8b-138">Norėdami sekti ir tvarkyti išmokų tarifo sąrankos keitimus, pasirinkite **Veiksmai**, tada pasirinkite **Tvarkyti versijas**.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="c0e8b-139">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="c0e8b-139">Select **Save**.</span></span> 
