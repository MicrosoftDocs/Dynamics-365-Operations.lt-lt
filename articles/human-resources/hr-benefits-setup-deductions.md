---
title: Atskaitymų konfigūravimas
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7ee9e8f3bc0e9027e41d3aa91bd097a3f046cbb4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009960"
---
# <a name="configure-deductions"></a><span data-ttu-id="36d74-102">Atskaitymų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="36d74-102">Configure deductions</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="36d74-103">Naudokite atskaitymus programoje „Microsoft Dynamics 365 Human Resources“, siekdami nustatyti, kiek (jei bus atskaitoma) atskaityti iš kiekvienos darbuotojui mokamos išmokos.</span><span class="sxs-lookup"><span data-stu-id="36d74-103">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="36d74-104">Atskaitymai priklauso nuo datos, todėl galite turėti archyvinį atskaitymo informacijos įrašą.</span><span class="sxs-lookup"><span data-stu-id="36d74-104">Deductions are date effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="36d74-105">Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Atskaitymai**.</span><span class="sxs-lookup"><span data-stu-id="36d74-105">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="36d74-106">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="36d74-106">Select **New**.</span></span>

3. <span data-ttu-id="36d74-107">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="36d74-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="36d74-108">Laukas</span><span class="sxs-lookup"><span data-stu-id="36d74-108">Field</span></span> | <span data-ttu-id="36d74-109">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="36d74-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="36d74-110">Atskaitymas</span><span class="sxs-lookup"><span data-stu-id="36d74-110">Deduction</span></span> | <span data-ttu-id="36d74-111">Unikalus ID, naudojamas išmokos atskaitymui nustatyti.</span><span class="sxs-lookup"><span data-stu-id="36d74-111">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="36d74-112">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="36d74-112">Description</span></span> | <span data-ttu-id="36d74-113">Atskaitymo aprašas.</span><span class="sxs-lookup"><span data-stu-id="36d74-113">A description for the deduction.</span></span> |
   | <span data-ttu-id="36d74-114">Galioja</span><span class="sxs-lookup"><span data-stu-id="36d74-114">Effective</span></span> | <span data-ttu-id="36d74-115">Pradžios data.</span><span class="sxs-lookup"><span data-stu-id="36d74-115">The start date.</span></span> <span data-ttu-id="36d74-116">Numatytoji vertė yra dabartinė sistemos data.</span><span class="sxs-lookup"><span data-stu-id="36d74-116">The default value is the current system date.</span></span> |
   | <span data-ttu-id="36d74-117">Galiojimo pabaiga</span><span class="sxs-lookup"><span data-stu-id="36d74-117">Expiration</span></span> | <span data-ttu-id="36d74-118">Pabaigos datą.</span><span class="sxs-lookup"><span data-stu-id="36d74-118">The end date.</span></span> <span data-ttu-id="36d74-119">Numatytoji reikšmė yra 2154-12-31, kuri reiškia, kad niekada.</span><span class="sxs-lookup"><span data-stu-id="36d74-119">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="36d74-120">Antraštė</span><span class="sxs-lookup"><span data-stu-id="36d74-120">Heading</span></span> | <span data-ttu-id="36d74-121">Antraštės kodas iš algalapių sistemos, kurį šis atskaitymas naudos darbuotojo atskaitymo daliai, atliekant į algalapį įtraukiamų išmokų apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="36d74-121">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="36d74-122">Naudojamas, kai naudojate trečiosios šalies algalapio teikėją.</span><span class="sxs-lookup"><span data-stu-id="36d74-122">This is used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="36d74-123">Darbuotojo algalapio atskaitymo rekomendacija</span><span class="sxs-lookup"><span data-stu-id="36d74-123">Employee payroll deduction reference</span></span> | <span data-ttu-id="36d74-124">Atskaitymo kodas iš algalapių sistemos, kurį šis atskaitymas naudos darbuotojo atskaitymo daliai, atliekant į algalapį įtraukiamų išmokų apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="36d74-124">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="36d74-125">Sumos antraštė</span><span class="sxs-lookup"><span data-stu-id="36d74-125">Amount heading</span></span> | <span data-ttu-id="36d74-126">Antraštės kodas iš algalapių sistemos, kurį ši atskaitymo suma naudos darbuotojo atskaitymo daliai, atliekant į algalapį įtraukiamų išmokų apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="36d74-126">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="36d74-127">Paprastai naudojamas, kai naudojate trečiosios šalies algalapio teikėją.</span><span class="sxs-lookup"><span data-stu-id="36d74-127">This is normally used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="36d74-128">Naikinti galima</span><span class="sxs-lookup"><span data-stu-id="36d74-128">Can delete</span></span> | <span data-ttu-id="36d74-129">Nurodo, ar iš „Dynamics 365 for Finance and Operations“ eksportuota vertė gali panaikinti vertę algalapių sistemoje.</span><span class="sxs-lookup"><span data-stu-id="36d74-129">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="36d74-130">Suporuoti stulpeliai</span><span class="sxs-lookup"><span data-stu-id="36d74-130">Paired columns</span></span> | <span data-ttu-id="36d74-131">Nurodo, ar eksportuoti antraštės ir atskaitymo sumą, esančią susietuose gretimuose stulpeliuose, į algalapio sistemą.</span><span class="sxs-lookup"><span data-stu-id="36d74-131">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="36d74-132">Keitimo įsigaliojimo data</span><span class="sxs-lookup"><span data-stu-id="36d74-132">Change effective date</span></span> | <span data-ttu-id="36d74-133">Data, kai įsigalios išmokų atskaitymo pakeitimas.</span><span class="sxs-lookup"><span data-stu-id="36d74-133">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="36d74-134">Šią dieną sistema automatiškai pakeis išmokų atskaitymą ir atnaujins visus su šiuo atskaitymu susijusius išmokų planus, jei vykdysite atskaitymo keitimo naujinimo apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="36d74-134">On this date the system will automatically change the benefit deduction and update all benefit plans associated with this deduction, as long as you run Deduction change update processing.</span></span> |
   | <span data-ttu-id="36d74-135">Atskaitymo pakeitimas atliktas</span><span class="sxs-lookup"><span data-stu-id="36d74-135">Deduction change completed</span></span> | <span data-ttu-id="36d74-136">Žymimasis langelis „Atskaitymo pakeitimas atliktas” bus pasirenkamas automatiškai, kai išmokų atskaitymo pakeitimai bus užbaigti apdorojus atskaitymo pakeitimo atnaujinimą.</span><span class="sxs-lookup"><span data-stu-id="36d74-136">The Deduction change completed check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="36d74-137">Norėdami sekti ir tvarkyti išmokų tarifo sąrankos keitimus, pasirinkite **Veiksmai**, tada pasirinkite **Tvarkyti versijas**.</span><span class="sxs-lookup"><span data-stu-id="36d74-137">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="36d74-138">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="36d74-138">Select **Save**.</span></span> 
