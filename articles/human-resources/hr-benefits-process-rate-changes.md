---
title: Tarifo pakeitimų apdorojimas
description: Išmokų tarifo pakeitimų apdorojimas programoje „Microsoft Dynamics 365 Human Resources“, kai pasikeičia naujo ar esamo išmokų plano tinkamumo taisyklių parametrai.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c841f5d5d409c7e73cdc38988f8233747a11f837
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803830"
---
# <a name="process-rate-changes"></a><span data-ttu-id="91d0d-103">Tarifo pakeitimų apdorojimas</span><span class="sxs-lookup"><span data-stu-id="91d0d-103">Process rate changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="91d0d-104">Išmokų tarifo pakeitimų apdorojimas programoje „Microsoft Dynamics 365 Human Resources“, kai pasikeičia naujo ar esamo išmokų plano tinkamumo taisyklių parametrai.</span><span class="sxs-lookup"><span data-stu-id="91d0d-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="91d0d-105">Jei sukuriama nauja tinkamumo taisyklė ir priskiriama planui, sistema iš naujo patikrina darbuotojo tinkamumą ir nustato, ar pagal naujas tinkamumo parinktis jis turi teisę gauti šį planą.</span><span class="sxs-lookup"><span data-stu-id="91d0d-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to rerun worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="91d0d-106">Darbo srities **Išmokų valdymas** dalyje **Apdorojimas** pasirinkite **Tarifo pakeitimo naujinimo apdorojimas**.</span><span class="sxs-lookup"><span data-stu-id="91d0d-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="91d0d-107">Dialogo lange **Vykdyti išmokų tarifo naujinimo procesą** nurodykite šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="91d0d-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="91d0d-108">Laukas</span><span class="sxs-lookup"><span data-stu-id="91d0d-108">Field</span></span> | <span data-ttu-id="91d0d-109">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="91d0d-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="91d0d-110">**Registracijos laikotarpis**</span><span class="sxs-lookup"><span data-stu-id="91d0d-110">**Enrollment period**</span></span> | <span data-ttu-id="91d0d-111">Išmokų pakeitimų apdorojimo registracijos laikotarpis.</span><span class="sxs-lookup"><span data-stu-id="91d0d-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="91d0d-112">Jei norite vykdyti procesą fone, pasirinkite **Vykdyti fone** ir atlikite šias užduotis:</span><span class="sxs-lookup"><span data-stu-id="91d0d-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="91d0d-113">Įveskite proceso informaciją.</span><span class="sxs-lookup"><span data-stu-id="91d0d-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="91d0d-114">Norėdami nustatyti pasikartojančią užduotį, pasirinkite **Pasikartojimas**, įveskite pasikartojimo informaciją ir pažymėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="91d0d-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="91d0d-115">Norėdami nustatyti užduoties įspėjimą, pasirinkite **Įspėjimai**, pasirinkite gautinus įspėjimus, tada pažymėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="91d0d-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="91d0d-116">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="91d0d-116">Select **OK**.</span></span> <span data-ttu-id="91d0d-117">Procesas bus vykdomas naudojant jūsų nustatytus parametrus.</span><span class="sxs-lookup"><span data-stu-id="91d0d-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="91d0d-118">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="91d0d-118">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]