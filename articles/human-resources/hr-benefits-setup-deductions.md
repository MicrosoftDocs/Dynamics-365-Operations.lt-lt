---
title: Atskaitymų konfigūravimas
description: Naudokite atskaitymus programoje „Microsoft Dynamics 365 Human Resources“, siekdami nustatyti, kiek (jei bus atskaitoma) atskaityti iš kiekvienos darbuotojui mokamos išmokos.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4fac1624ce3a88b9fb4adcf303860e82f9d9165b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055561"
---
# <a name="configure-deductions"></a><span data-ttu-id="7ad3e-103">Atskaitymų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="7ad3e-103">Configure deductions</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7ad3e-104">Naudokite atskaitymus programoje „Microsoft Dynamics 365 Human Resources“, siekdami nustatyti, kiek (jei bus atskaitoma) atskaityti iš kiekvienos darbuotojui mokamos išmokos.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="7ad3e-105">Atskaitymai priklauso nuo datos, todėl galite turėti archyvinį atskaitymo informacijos įrašą.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-105">Deductions are date-effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="7ad3e-106">Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Atskaitymai**.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="7ad3e-107">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-107">Select **New**.</span></span>

3. <span data-ttu-id="7ad3e-108">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="7ad3e-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="7ad3e-109">Laukas</span><span class="sxs-lookup"><span data-stu-id="7ad3e-109">Field</span></span> | <span data-ttu-id="7ad3e-110">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="7ad3e-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="7ad3e-111">**Atskaitymas**</span><span class="sxs-lookup"><span data-stu-id="7ad3e-111">**Deduction**</span></span> | <span data-ttu-id="7ad3e-112">Unikalus ID, naudojamas išmokos atskaitymui nustatyti.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="7ad3e-113">**Aprašymas**</span><span class="sxs-lookup"><span data-stu-id="7ad3e-113">**Description**</span></span> | <span data-ttu-id="7ad3e-114">Atskaitymo aprašas.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="7ad3e-115">**Galioja**</span><span class="sxs-lookup"><span data-stu-id="7ad3e-115">**Effective**</span></span> | <span data-ttu-id="7ad3e-116">Pradžios data.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-116">The start date.</span></span> <span data-ttu-id="7ad3e-117">Numatytoji vertė yra dabartinė sistemos data.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="7ad3e-118">**Galiojimo pabaiga**</span><span class="sxs-lookup"><span data-stu-id="7ad3e-118">**Expiration**</span></span> | <span data-ttu-id="7ad3e-119">Pabaigos datą.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-119">The end date.</span></span> <span data-ttu-id="7ad3e-120">Numatytoji reikšmė yra 2154-12-31, kuri reiškia, kad niekada.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="7ad3e-121">**Antraštė**</span><span class="sxs-lookup"><span data-stu-id="7ad3e-121">**Heading**</span></span> | <span data-ttu-id="7ad3e-122">Antraštės kodas iš algalapių sistemos, kurį šis atskaitymas naudos darbuotojo atskaitymo daliai, atliekant į algalapį įtraukiamų išmokų apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="7ad3e-123">Naudojamas, kai naudojate trečiosios šalies algalapio teikėją.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-123">This is used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="7ad3e-124">**Darbuotojo algalapio atskaitymo rekomendacija**</span><span class="sxs-lookup"><span data-stu-id="7ad3e-124">**Employee payroll deduction reference**</span></span> | <span data-ttu-id="7ad3e-125">Atskaitymo kodas iš algalapių sistemos, kurį šis atskaitymas naudos darbuotojo atskaitymo daliai, atliekant į algalapį įtraukiamų išmokų apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="7ad3e-126">**Sumos antraštė**</span><span class="sxs-lookup"><span data-stu-id="7ad3e-126">**Amount heading**</span></span> | <span data-ttu-id="7ad3e-127">Antraštės kodas iš algalapių sistemos, kurį ši atskaitymo suma naudos darbuotojo atskaitymo daliai, atliekant į algalapį įtraukiamų išmokų apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="7ad3e-128">Paprastai naudojamas, kai naudojate trečiosios šalies algalapio teikėją.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-128">This is normally used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="7ad3e-129">**Naikinti galima**</span><span class="sxs-lookup"><span data-stu-id="7ad3e-129">**Can delete**</span></span> | <span data-ttu-id="7ad3e-130">Nurodo, ar iš „Dynamics 365 for Finance and Operations“ eksportuota vertė gali panaikinti vertę algalapių sistemoje.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="7ad3e-131">**Suporuoti stulpeliai**</span><span class="sxs-lookup"><span data-stu-id="7ad3e-131">**Paired columns**</span></span> | <span data-ttu-id="7ad3e-132">Nurodo, ar eksportuoti antraštės ir atskaitymo sumą, esančią susietuose gretimuose stulpeliuose, į algalapio sistemą.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="7ad3e-133">**Keitimo įsigaliojimo data**</span><span class="sxs-lookup"><span data-stu-id="7ad3e-133">**Change effective date**</span></span> | <span data-ttu-id="7ad3e-134">Data, kai įsigalios išmokų atskaitymo pakeitimas.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="7ad3e-135">Šią dieną sistema automatiškai pakeičia išmokų atskaitymą ir atnaujina visus su šiuo atskaitymu susijusius išmokų planus, jei vykdysite **atskaitymo keitimo naujinimo** apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-135">On this date, the system automatically changes the benefit deduction and updates all benefit plans associated with this deduction, as long as you run **Deduction change update** processing.</span></span> |
   | <span data-ttu-id="7ad3e-136">**Atskaitymo pakeitimas atliktas**</span><span class="sxs-lookup"><span data-stu-id="7ad3e-136">**Deduction change completed**</span></span> | <span data-ttu-id="7ad3e-137">Žymimasis langelis **Atskaitymo pakeitimas atliktas** bus pasirenkamas automatiškai, kai išmokų atskaitymo pakeitimai bus užbaigti apdorojus atskaitymo pakeitimo atnaujinimą.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-137">The **Deduction change completed** check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="7ad3e-138">Norėdami sekti ir tvarkyti išmokų tarifo sąrankos keitimus, pasirinkite **Veiksmai**, tada pasirinkite **Tvarkyti versijas**.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="7ad3e-139">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7ad3e-139">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]