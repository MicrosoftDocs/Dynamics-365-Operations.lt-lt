---
title: Projekto įvertinimų šalinimas
description: Šioje temoje pateikiama informacija apie projekto įvertinimų šalinimą po to, kai jis užbaigiamas.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410246"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="7077d-103">Projekto įvertinimų šalinimas</span><span class="sxs-lookup"><span data-stu-id="7077d-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7077d-104">Projekto įvertinimai yra darbo, kuris apskaičiuotas ir suplanuotas projektui, finansinis rodinys.</span><span class="sxs-lookup"><span data-stu-id="7077d-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="7077d-105">Norėdami dirbti su projekto įvertinimais, turite pridėti projektą prie vertinamo projekto.</span><span class="sxs-lookup"><span data-stu-id="7077d-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="7077d-106">Vertinamas projektas visada pagrįstas esamu projektu, tačiau keli projektai gali nurodyti vieną vertinamą projektą.</span><span class="sxs-lookup"><span data-stu-id="7077d-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="7077d-107">Prie vertinamų projektų galima pridėti tik fiksuotos kainos ir investicijų projektus, o šie projektai turi priklausyti tai pačiai projektų grupei kaip vertinamas projektas.</span><span class="sxs-lookup"><span data-stu-id="7077d-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="7077d-108">Norint pašalinti vertinamą projektą, jis turi būti užbaigtas.</span><span class="sxs-lookup"><span data-stu-id="7077d-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="7077d-109">Toliau pateikti veiksmai paaiškina, kaip pašalinti įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="7077d-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="7077d-110">Eikite į **Projektų valdymas ir apskaita** > **Visi projektai** ir atidarykite projektą.</span><span class="sxs-lookup"><span data-stu-id="7077d-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="7077d-111">Skirtuke **Valdymas** pasirinkite **Įvertinimai**, o puslapyje **Įvertinimas** pasirinkite **Pašalinti**.</span><span class="sxs-lookup"><span data-stu-id="7077d-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="7077d-112">Puslapyje **Įvertinimo šalinimas**, skirtuke **Bendra**, nustatykite toliau išvardytas parinktis.</span><span class="sxs-lookup"><span data-stu-id="7077d-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="7077d-113">**Laikotarpio kodas** – pasirinkite laikotarpio kodą, kad galėtumėte pasirinkti atitinkamus vertinamus projektus.</span><span class="sxs-lookup"><span data-stu-id="7077d-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="7077d-114">**Įvertinimo data** – pasirinkite atitinkamą įvertinimo šalinimo datą.</span><span class="sxs-lookup"><span data-stu-id="7077d-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="7077d-115">**Pašalinti su NG įspėjimais** – įjunkite šią pasirinktį, kad būtų rodomas pranešimas, kai pašalinamas su nebaigta gamyba (NG) susijęs įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="7077d-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="7077d-116">Kai ši parinktis neįjungta, šalinimas negali tęstis, jei yra neįvertintų operacijų.</span><span class="sxs-lookup"><span data-stu-id="7077d-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="7077d-117">Ši pasirinktis galima tik tada, kai šalinimas taikomas vertinamam projektui.</span><span class="sxs-lookup"><span data-stu-id="7077d-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="7077d-118">Ji negalima, jei naudojate periodinius registravimus.</span><span class="sxs-lookup"><span data-stu-id="7077d-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="7077d-119">Šis parametras veikia kartu su parametrais, esančiais skirtuke **Įvertinimas**, puslapyje **Projekto parametrai**, laukų grupėje **Leisti pašalinti, kai yra neįvertintų operacijų**.</span><span class="sxs-lookup"><span data-stu-id="7077d-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="7077d-120">**Nustatyti užbaigimo etapą** – įjunkite šią pasirinktį norėdami nustatyti vertinamo projekto etapą į **Baigtas** po to, kai atliekate šalinimą.</span><span class="sxs-lookup"><span data-stu-id="7077d-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="7077d-121">**Spausdinti įvertinimų sąrašą** – pasirinkite informaciją, kuri bus įtraukta spausdinant įvertinimų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="7077d-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="7077d-122">**Rodyti sistemos pranešimą** – įjunkite šią pasirinktį, kad būtų rodomas sistemos pranešimas.</span><span class="sxs-lookup"><span data-stu-id="7077d-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="7077d-123">**Registravimo data** – pasirinkite įvertinimo didžiosios knygos registravimo datą.</span><span class="sxs-lookup"><span data-stu-id="7077d-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="7077d-124">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7077d-124">Select **OK**.</span></span>
5. <span data-ttu-id="7077d-125">Užbaigus šalinimo procesą, pašalintas vertinimas projektas rodomas su neigiama verte.</span><span class="sxs-lookup"><span data-stu-id="7077d-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="7077d-126">Jei neketinote šalinti įvertinimo, galite pasirinkti pašalintą įvertinimą ir spustelėti **Atšaukti šalinimą**.</span><span class="sxs-lookup"><span data-stu-id="7077d-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
