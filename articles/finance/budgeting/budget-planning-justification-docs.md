---
title: Biudžeto planavimo pagrindimo dokumentai
description: Pagrindimo dokumentai prašantiems biudžeto asmenims suteikia informacijos, padedančios paaiškinti, kodėl konkretus biudžetas yra reikalingas.
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 321da6643b421070ddd9f32bddd3e8d72f0adb86
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188561"
---
# <a name="budget-planning-justification-documents"></a><span data-ttu-id="203c0-103">Biudžeto planavimo pagrindimo dokumentai</span><span class="sxs-lookup"><span data-stu-id="203c0-103">Budget planning justification documents</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="203c0-104">Pagrindimo dokumentai prašantiems biudžeto asmenims suteikia informacijos, padedančios paaiškinti, kodėl konkretus biudžetas yra reikalingas.</span><span class="sxs-lookup"><span data-stu-id="203c0-104">Justification documents provide a narrative for those requesting a budget to explain why a specific budget is necessary.</span></span> 

<span data-ttu-id="203c0-105">Biudžeto plano šabloną sukuria biudžeto vadovas programoje „Microsoft Word“ ir priskiria dabartiniam biudžeto planavimo procesui.</span><span class="sxs-lookup"><span data-stu-id="203c0-105">A budget plan template is created by the budget manager in Microsoft Word and assigned to the current budget planning process.</span></span> <span data-ttu-id="203c0-106">Tada biudžeto savininkai gali atidaryti šabloną ir automatiškai įvesti duomenis į „Word“ dokumentą pagal savo biudžeto užklausą.</span><span class="sxs-lookup"><span data-stu-id="203c0-106">Budget owners can then open the template and have data automatically populated in Word based on their budget request.</span></span> <span data-ttu-id="203c0-107">Tada jie gali įtraukti papildomo teksto arba duomenų, prieš įrašydami ir pridėdami savo pritaikytą pagrindimo dokumentą prie savo biudžeto plano.</span><span class="sxs-lookup"><span data-stu-id="203c0-107">They can then add additional text or data prior to saving and attaching their personalized justification document to their budget plan.</span></span>

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a><span data-ttu-id="203c0-108">„Microsoft Microsoft Dynamics“ papildinio, skirto „Microsoft Word“, nustatymas</span><span class="sxs-lookup"><span data-stu-id="203c0-108">Set up Microsoft Dynamics Office Add-in for Microsoft Word</span></span>

1.  <span data-ttu-id="203c0-109">Atidarykite naują „Microsoft Word“ dokumentą.</span><span class="sxs-lookup"><span data-stu-id="203c0-109">Open a new Microsoft Word document.</span></span>
2.  <span data-ttu-id="203c0-110">Juostelėje spustelėkite **Įterpti** ir spustelėkite **Parduotuvė**.</span><span class="sxs-lookup"><span data-stu-id="203c0-110">Click **Insert** on the ribbon, and click **Store**.</span></span>
3.  <span data-ttu-id="203c0-111">Raskite „Microsoft Dynamics Office“ papildinį ir spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="203c0-111">Search for Microsoft Dynamics Office Add-in and click **Add**.</span></span>
4.  <span data-ttu-id="203c0-112">Programos „Word“ kairiojoje srityje spustelėkite **Įtraukti serverio informaciją**.</span><span class="sxs-lookup"><span data-stu-id="203c0-112">In Word, in the right pane, click **Add server information**.</span></span>
5.  <span data-ttu-id="203c0-113">Įveskite arba įklijuokite serverio URL ir spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="203c0-113">Type or paste the server URL and click **OK**.</span></span>

##### <a name="define-the-justification-template-in-microsoft-word"></a><span data-ttu-id="203c0-114">Pagrindimo šablono nurodymas programoje „Microsoft Word“</span><span class="sxs-lookup"><span data-stu-id="203c0-114">Define the Justification template in Microsoft Word</span></span>

1.  <span data-ttu-id="203c0-115">Kai prisijungsite, „Microsoft Dynamics Office“ papildinyje spustelėkite **Dizainas**.</span><span class="sxs-lookup"><span data-stu-id="203c0-115">Click **Design** in the Microsoft Dynamics Office Add-in after you’ve logged in.</span></span>
2.  <span data-ttu-id="203c0-116">Norėdami tvarkyti antraštės informaciją, naudokite mygtuką **Įtraukti laukų**.</span><span class="sxs-lookup"><span data-stu-id="203c0-116">For header information, use the **Add fields** button.</span></span>
3.  <span data-ttu-id="203c0-117">Pasirinkite BudgetPlanJustification objekto duomenų šaltinį ir spustelėkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="203c0-117">Select the entity data source of BudgetPlanJustification, and click **Next**.</span></span> <span data-ttu-id="203c0-118">**Pastaba:** šis objektas reikalingas visiems pagrindimo dokumentams.</span><span class="sxs-lookup"><span data-stu-id="203c0-118">**Note:** This entity is required for any justification document.</span></span> <span data-ttu-id="203c0-119">Galima naudoti kitus objektus, bet jei šis objektas nėra įtrauktas, nusiuntimas į „Microsoft Dynamics 365 Finance“ nepavyks.</span><span class="sxs-lookup"><span data-stu-id="203c0-119">Other entities can be used but the upload back to Microsoft Dynamics 365 Finance will fail if this entity isn’t included.</span></span>
4.  <span data-ttu-id="203c0-120">Į „Word“ dokumentą įtraukite BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter ir DocumentNumber žymas ir reikšmes.</span><span class="sxs-lookup"><span data-stu-id="203c0-120">Add the BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter, and DocumentNumber labels and values in the Word document.</span></span> <span data-ttu-id="203c0-121">**Pastaba:** jei reikia, galite naudoti savo pasirinktines žymas, o ne standartines žymas.</span><span class="sxs-lookup"><span data-stu-id="203c0-121">**Note:** You can use your own custom labels, rather than the standard labels, if needed.</span></span>
5.  <span data-ttu-id="203c0-122">Norėdami baigti tvarkyti antraštės dalį, spustelėkite **Atlikta**.</span><span class="sxs-lookup"><span data-stu-id="203c0-122">Click **Done** to complete the header section.</span></span>
6.  <span data-ttu-id="203c0-123">Norėdami tvarkyti biudžeto plano eilutės lygio informaciją, spustelėkite **Įtraukti lentelę**.</span><span class="sxs-lookup"><span data-stu-id="203c0-123">For line level detail of budget plan amounts, click **Add table**.</span></span>
7.  <span data-ttu-id="203c0-124">Vėl pasirinkite BudgetPlanJustification objekto duomenų šaltinį ir spustelėkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="203c0-124">Again, select the entity data source of BudgetPlanJustification, and click **Next**.</span></span>
8.  <span data-ttu-id="203c0-125">Įtraukite laukus EffectiveDate, ScenarioName, AccountDisplayValue ir AccountingCurrencyExpenseAmount.</span><span class="sxs-lookup"><span data-stu-id="203c0-125">Add fields for EffectiveDate, ScenarioName, AccountDisplayValue, and AccountingCurrencyExpenseAmount.</span></span> <span data-ttu-id="203c0-126">**Pastaba:** jei komentarus galima įtraukti į atskiras biudžeto plano eilutes, juos galima įtraukti į lentelę čia.</span><span class="sxs-lookup"><span data-stu-id="203c0-126">**Note:** If comments are available to add within individual budget plan lines, those can be added to the table here.</span></span>
9.  <span data-ttu-id="203c0-127">Įtraukite bet kokias papildomas instrukcijas galutiniam vartotojui ir atlikite visus reikalingus dokumento formatavimo arba stiliaus keitimo veiksmus.</span><span class="sxs-lookup"><span data-stu-id="203c0-127">Add any additional instructions to provide to the end user, and perform any necessary formatting or styling to the document.</span></span>
10. <span data-ttu-id="203c0-128">Prieš tęsdami įrašykite dokumentą į vietinį kompiuterį ir uždarykite failą.</span><span class="sxs-lookup"><span data-stu-id="203c0-128">Save the document to your local computer and close the file before continuing.</span></span>

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a><span data-ttu-id="203c0-129">Biudžeto planavimo proceso nustatymas naudoti pagrindimo šabloną</span><span class="sxs-lookup"><span data-stu-id="203c0-129">Set up the Budget planning process to use the Justification template</span></span>

1.  <span data-ttu-id="203c0-130">Atidarykite **Biudžeto sudarymas** &gt; **Sąranka** &gt; **Biudžeto planavimas** &gt; **Pagrindimo dokumento šablonai**.</span><span class="sxs-lookup"><span data-stu-id="203c0-130">Go to **Budgeting** &gt; **Setup** &gt; **Budget planning** &gt; **Justification document templates**.</span></span>
2.  <span data-ttu-id="203c0-131">Spustelėkite **Naujas** ir naršydami atidarykite naujai sukurtą „Microsoft Word“ dokumentą.</span><span class="sxs-lookup"><span data-stu-id="203c0-131">Click **New** and browse to your newly created Microsoft Word document.</span></span>
3.  <span data-ttu-id="203c0-132">Įveskite šablono rodomą pavadinimą ir aprašą.</span><span class="sxs-lookup"><span data-stu-id="203c0-132">Enter a template display name and description.</span></span> <span data-ttu-id="203c0-133">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="203c0-133">Click **OK**.</span></span>
4.  <span data-ttu-id="203c0-134">Atidarykite **Biudžeto sudarymas** &gt; **Sąranka** &gt; **Biudžeto** **planavimas** &gt; **Biudžeto planavimo procesas**.</span><span class="sxs-lookup"><span data-stu-id="203c0-134">Go to **Budgeting** &gt; **Setup** &gt; **Budget** **planning** &gt; **Budget planning process**.</span></span>
5.  <span data-ttu-id="203c0-135">Pasirinkite procesą, kuriame bus naudojamas pagrindimo šablonas, ir spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="203c0-135">Select the process where the justification template should be used, and click **Edit**.</span></span>
6.  <span data-ttu-id="203c0-136">Lauke **Pagrindimo dokumento šablonas** pasirinkite reikiamą šabloną ir įrašykite.</span><span class="sxs-lookup"><span data-stu-id="203c0-136">In the **Justification document template** field, select the appropriate template and save.</span></span>

##### <a name="edit-and-save-personalized-justification-documents"></a><span data-ttu-id="203c0-137">Pritaikytų pagrindimo dokumentų redagavimas ir įrašymas</span><span class="sxs-lookup"><span data-stu-id="203c0-137">Edit and save personalized justification documents</span></span>

1.  <span data-ttu-id="203c0-138">Sukurkite naują biudžeto planą arba atidarykite esamą biudžeto planą.</span><span class="sxs-lookup"><span data-stu-id="203c0-138">Create a new budget plan or open an existing budget plan.</span></span>
2.  <span data-ttu-id="203c0-139">Išplečiamajame meniu **Pagrindimas** pasirinkite **Kurti naują pagrindimą**.</span><span class="sxs-lookup"><span data-stu-id="203c0-139">In the **Justification** drop-down menu, select **Create new justification**.</span></span>
3.  <span data-ttu-id="203c0-140">Įvedę informaciją pasirinkite įkelti pritaikytą dokumentą iš išplečiamojo meniu **Pagrindimas**.</span><span class="sxs-lookup"><span data-stu-id="203c0-140">After filling in the details, select to upload the personalized document from the **Justification** drop-down menu.</span></span>




