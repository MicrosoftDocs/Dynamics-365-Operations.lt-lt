---
title: "Biudžeto planavimo „Excel“ šablonai"
description: "Šioje temoje aprašoma, kaip kurti „Microsoft Excel“ šablonus, kuriuos galima naudoti biudžeto planuose."
author: ryansandness
manager: AnnBe
ms.date: 07/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 96df6bbfe5c9e158b616230c2b061762a5edda08
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="budget-planning-templates-for-excel"></a><span data-ttu-id="1f71d-103">Biudžeto planavimo „Excel“ šablonai</span><span class="sxs-lookup"><span data-stu-id="1f71d-103">Budget planning templates for Excel</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1f71d-104">Šioje temoje aprašoma, kaip kurti „Microsoft Excel“ šablonus, kuriuos galima naudoti biudžeto planuose.</span><span class="sxs-lookup"><span data-stu-id="1f71d-104">This topic describes how to create Microsoft Excel templates that can be used with budget plans.</span></span>

<span data-ttu-id="1f71d-105">Šioje temoje parodoma, kaip kurti biudžeto planuose naudojamus „Excel“ šablonus, naudojant standartinį demonstracinių duomenų rinkinį ir administratoriaus vartotojo prisijungimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="1f71d-105">This topic shows how to create Excel templates that will be used with budget plans using the standard demo data set and the Admin user login.</span></span> <span data-ttu-id="1f71d-106">Daugiau informacijos apie biudžeto planavimą žr. [Biudžeto planavimo apžvalga.](budget-planning-overview-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="1f71d-106">For more information about budget planning, see [Budget planning overview.](budget-planning-overview-configuration.md)</span></span> <span data-ttu-id="1f71d-107">Taip galite vadovautis mokymo programa [Biudžeto planavimo 101](budget-plan.md), kad sužinotumėte pagrindinius modulio konfigūracijos ir naudojimo principus.</span><span class="sxs-lookup"><span data-stu-id="1f71d-107">You can also follow the [Budget planning 101](budget-plan.md) tutorial to learn basic module configuration and usage principles.</span></span>

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a><span data-ttu-id="1f71d-108">Darbalalapio generavimas naudojant biudžeto plano dokumento maketą</span><span class="sxs-lookup"><span data-stu-id="1f71d-108">Generate a worksheet using budget plan document layout</span></span>

<span data-ttu-id="1f71d-109">Biudžeto plano dokumentus galime peržiūrėti ir redaguoti naudojant vieną arba daugiau maketų.</span><span class="sxs-lookup"><span data-stu-id="1f71d-109">Budget plan documents can be viewed and edited using one or more layouts.</span></span> <span data-ttu-id="1f71d-110">Kiekvienam maketui galima priskirti biudžeto plano dokumento šabloną, kad būtų galima peržiūrėti ir redaguoti biudžeto plano duomenis „Excel“ darbalapyje.</span><span class="sxs-lookup"><span data-stu-id="1f71d-110">Each layout can have an associated budget plan document template to view and edit the budget plan data in an Excel worksheet.</span></span> <span data-ttu-id="1f71d-111">Šioje temoje biudžeto plano dokumento šablonas bus sugeneruotas naudojant esamo maketo konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="1f71d-111">In this topic, a budget plan document template will be generated using an existing layout configuration.</span></span> 

1. <span data-ttu-id="1f71d-112">Atidarykite **Biudžeto planų sąrašas** (**Biudžeto sudarymas** &gt; **Biudžeto planai**).</span><span class="sxs-lookup"><span data-stu-id="1f71d-112">Open the **Budget plans list** (**Budgeting** &gt; **Budget plans**).</span></span> 
2. <span data-ttu-id="1f71d-113">Spustelėkite **Naujas**, kad sukurtumėte naują biudžeto plano dokumentą.</span><span class="sxs-lookup"><span data-stu-id="1f71d-113">Click **New** to create a new budget plan document.</span></span> 

  <span data-ttu-id="1f71d-114">[![Biudžeto planų sąrašas](./media/bpt11-1024x552.png)](./media/bpt11.png)</span><span class="sxs-lookup"><span data-stu-id="1f71d-114">[![Budget plans list](./media/bpt11-1024x552.png)](./media/bpt11.png)</span></span> 

3. <span data-ttu-id="1f71d-115">Naudokite eilutės parinktį **Įtraukti**, kad įtrauktumėte eilučių.</span><span class="sxs-lookup"><span data-stu-id="1f71d-115">Use the **Add** line option to add lines.</span></span> <span data-ttu-id="1f71d-116">Spustelėkite **Maketai**, kad peržiūrėtumėte biudžeto plano dokumento maketo konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="1f71d-116">Click **Layouts** to view the budget plan document layout configuration.</span></span> 

  <span data-ttu-id="1f71d-117">[![Biudžeto planų įtraukimas](./media/bpt2-1024x274.png)](./media/bpt2.png)</span><span class="sxs-lookup"><span data-stu-id="1f71d-117">[![Budget plans add](./media/bpt2-1024x274.png)](./media/bpt2.png)</span></span> 

<span data-ttu-id="1f71d-118">Maketo konfigūraciją galite peržiūrėti ir pagal poreikį koreguoti.</span><span class="sxs-lookup"><span data-stu-id="1f71d-118">You can review the layout configuration and adjust it as needed.</span></span> 
1. <span data-ttu-id="1f71d-119">Atidarykite **Šablonas** &gt; **Generuoti**, kad sukurtumėte šio maketo „Excel“ failą.</span><span class="sxs-lookup"><span data-stu-id="1f71d-119">Go to **Template** &gt; **Generate** to create an Excel file for this layout.</span></span> 
2. <span data-ttu-id="1f71d-120">Sugeneravę šabloną pasirinkite **Šablonas** &gt; **Peržiūrėti**, kad atidarytumėte ir peržiūrėtumėte biudžeto plano dokumento šabloną.</span><span class="sxs-lookup"><span data-stu-id="1f71d-120">After the template is generated, go to **Template** &gt; **View** to open and review the budget plan document template.</span></span> <span data-ttu-id="1f71d-121">„Excel“ failą galite įrašyti į vietinį diską.</span><span class="sxs-lookup"><span data-stu-id="1f71d-121">You can save the Excel file to your local drive.</span></span> 

<span data-ttu-id="1f71d-122">[![Įrašyti kaip](./media/bpt3-1024x545.png)](./media/bpt3.png)</span><span class="sxs-lookup"><span data-stu-id="1f71d-122">[![Save as](./media/bpt3-1024x545.png)](./media/bpt3.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="1f71d-123">Biudžeto plano dokumento maketo redaguoti negalima, kai jis susietas su „Excel“ šablonu.</span><span class="sxs-lookup"><span data-stu-id="1f71d-123">The Budget plan document layout cannot be edited after an Excel template is associated with it.</span></span> <span data-ttu-id="1f71d-124">Norėdami redaguoti maketą, panaikinkite susietą „Excel“ šablono failą ir sugeneruokite jį iš naujo.</span><span class="sxs-lookup"><span data-stu-id="1f71d-124">To modify the layout, delete the associated Excel template file and regenerate it.</span></span> <span data-ttu-id="1f71d-125">Tai būtina, kad maketo ir darbalapio laukai būtų sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="1f71d-125">This is required to keep the fields in the layout and the worksheet synchronized.</span></span> 

<span data-ttu-id="1f71d-126">„Excel“ šablone bus pateikti visi biudžeto plano dokumento maketo elementai, kurių stulpelis **Pasiekiama darbalapyje** nustatytas į True.</span><span class="sxs-lookup"><span data-stu-id="1f71d-126">The Excel template will contain all of the elements from the budget plan document layout, where the **Available in Worksheet** column is set to True.</span></span> <span data-ttu-id="1f71d-127">Persidengiančių elementų „Excel“ šablone pateikti negalima.</span><span class="sxs-lookup"><span data-stu-id="1f71d-127">Overlapping elements are not allowed in the Excel template.</span></span> <span data-ttu-id="1f71d-128">Pvz., jei makete yra stulpeliai Užklausa per 1 ketvirtį, Užklausa per 2 ketvirtį, Užklausa per 3 ketvirtį ir Užklausa per 4 ketvirtį bei visų užklausų stulpelis, kuris nurodo visų 4 ketvirčių stulpelių sumą, „Excel“ šablone galima naudoti tik ketvirčių stulpelius arba visų užklausų stulpelį.</span><span class="sxs-lookup"><span data-stu-id="1f71d-128">For example, if the layout contains Request Q1, Request Q2, Request Q3, and Request Q4 columns, and a total request column that represents a sum of all 4 quarterly columns, only the quarterly columns or total column is available to be used in the Excel template.</span></span> <span data-ttu-id="1f71d-129">Naujinimo metu „Excel“ failas negali atnaujinti persidengiančių stulpelių, nes lentelės duomenys gali tapti pasenę ir netikslūs.</span><span class="sxs-lookup"><span data-stu-id="1f71d-129">The Excel file cannot update overlapping columns during the update because data in the table could become out of date and inaccurate.</span></span>

<span data-ttu-id="1f71d-130">[![Pavyzdys:](./media/bpt4-1024x615.png)](./media/bpt4.png)</span><span class="sxs-lookup"><span data-stu-id="1f71d-130">[![Example](./media/bpt4-1024x615.png)](./media/bpt4.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="1f71d-131">Siekiant išvengti galimų problemų, susijusių su biudžeto plano duomenų peržiūra ir redagavimu programoje „Excel“, tas pats vartotojas turėtų prisijungti prie „Dynamics 365 for Operations“ (leidimas „Enterprise“) ir prie „Microsoft Dynamics Office“ papildinio duomenų jungties.</span><span class="sxs-lookup"><span data-stu-id="1f71d-131">To avoid potential issues with viewing and editing budget plan data using Excel, the same user should be logged into both Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and the Microsoft Dynamics Office Add-in Data Connector.</span></span>

## <a name="add-a-header-to-budget-plan-document-template"></a><span data-ttu-id="1f71d-132">Antraštės įtraukimas į biudžeto plano dokumento šabloną</span><span class="sxs-lookup"><span data-stu-id="1f71d-132">Add a header to budget plan document template</span></span>
<span data-ttu-id="1f71d-133">Norėdami įtraukti antraštės informaciją, pasirinkite viršutinę „Excel“ failo eilutę ir įterpkite tuščių eilučių.</span><span class="sxs-lookup"><span data-stu-id="1f71d-133">To add header information, select the top row in the Excel file and insert empty rows.</span></span> <span data-ttu-id="1f71d-134">Dalyje **Duomenų jungtis** spustelėkite **Dizainas**, kad į „Excel“ failą įtrauktumėte antraštės laukų.</span><span class="sxs-lookup"><span data-stu-id="1f71d-134">Click **Design** in the **Data Connector** to add header fields to the Excel file.</span></span>

<span data-ttu-id="1f71d-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span><span class="sxs-lookup"><span data-stu-id="1f71d-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span></span> 

<span data-ttu-id="1f71d-136">Skirtuke **Dizainas** spustelėkite **Įtraukti** ir tada **BudgetPlanHeader** pasirinkite kaip objekto duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="1f71d-136">In the **Design** tab, click **Add** fields, and then select **BudgetPlanHeader** as the entity data source.</span></span>

<span data-ttu-id="1f71d-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span><span class="sxs-lookup"><span data-stu-id="1f71d-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span></span>

<span data-ttu-id="1f71d-138">Nuveskite žymeklį į norimą vietą „Excel“ faile.</span><span class="sxs-lookup"><span data-stu-id="1f71d-138">Point the cursor to the desired location in the Excel file.</span></span> <span data-ttu-id="1f71d-139">Spustelėkite **Įtraukti žymą**, kad į pasirinktą vietą įtrauktumėte lauko žymą.</span><span class="sxs-lookup"><span data-stu-id="1f71d-139">Click **Add label** to add the field label to the selected location.</span></span> <span data-ttu-id="1f71d-140">Pasirinkite **Įtraukti vertę**, kad į pasirinktą vietą įtrauktumėte vertės lauką.</span><span class="sxs-lookup"><span data-stu-id="1f71d-140">Select **Add Value** to add the value field to the selected place.</span></span> <span data-ttu-id="1f71d-141">Spustelėkite **Atlikta**, kad uždarytumėte dizaino įrankį.</span><span class="sxs-lookup"><span data-stu-id="1f71d-141">Click **Done** to close the designer.</span></span>

## <a name="bpt7mediabpt7pngmediabpt7png"></a><span data-ttu-id="1f71d-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span><span class="sxs-lookup"><span data-stu-id="1f71d-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span></span>

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a><span data-ttu-id="1f71d-143">Apskaičiuoto stulpelio įtraukimas į biudžeto plano dokumento šablono lentelę</span><span class="sxs-lookup"><span data-stu-id="1f71d-143">Add a calculated column to budget plan document template table</span></span>
--------------------------------------------------------------

<span data-ttu-id="1f71d-144">Tada apskaičiuoti stulpeliai įtraukiami į sugeneruotą biudžeto plano dokumento šabloną.</span><span class="sxs-lookup"><span data-stu-id="1f71d-144">Next, calculated columns will be added to generated budget plan document template.</span></span> <span data-ttu-id="1f71d-145">Stulpelis **Bendra užklausų suma**, kuriame pateikiama paraiškų už 1–4 ketvirčių stulpelių suma, ir stulpelis **Koregavimas**, kuriame stulpelio **Bendra užklausų suma** vertė perskaičiuojama naudojant iš anksto nustatytą koeficientą.</span><span class="sxs-lookup"><span data-stu-id="1f71d-145">A **Total request** column, which summarizes Request Q1: Request Q4 columns, and an **Adjustment** column, which recalculates the **Total Request** column by a predefined factor.</span></span>

<span data-ttu-id="1f71d-146">Dalyje **Duomenų jungtis** spustelėkite **Dizainas**, kad į lentelę įtrauktumėte stulpelių.</span><span class="sxs-lookup"><span data-stu-id="1f71d-146">Click **Design** in the **Data connector** to add columns to the table.</span></span> <span data-ttu-id="1f71d-147">Šalia duomenų šaltinio **BudgetPlanWorksheet** spustelėkite **Redaguoti**, kad pradėtumėte įkelti stulpelius.</span><span class="sxs-lookup"><span data-stu-id="1f71d-147">Click **Edit** next to **BudgetPlanWorksheet** data source to start adding columns.</span></span>

<span data-ttu-id="1f71d-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span><span class="sxs-lookup"><span data-stu-id="1f71d-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span></span> 

<span data-ttu-id="1f71d-149">Pasirinktoje laukų grupėje rodomi stulpeliai, pateikiami šablone.</span><span class="sxs-lookup"><span data-stu-id="1f71d-149">The selected field group displays the columns that are available in the template.</span></span> <span data-ttu-id="1f71d-150">Spustelėkite **Formulė**, kad įtrauktumėte naują stulpelį.</span><span class="sxs-lookup"><span data-stu-id="1f71d-150">Click **Formula** to add a new column.</span></span> <span data-ttu-id="1f71d-151">Pavadinkite naują stulpelį ir tada įklijuokite formulę lauke **Formulė**.</span><span class="sxs-lookup"><span data-stu-id="1f71d-151">Name the new column and then paste the formula into the **Formula** field.</span></span> <span data-ttu-id="1f71d-152">Spustelėkite **Naujinti**, kad įterptumėte stulpelį.</span><span class="sxs-lookup"><span data-stu-id="1f71d-152">Click **Update** to insert the column.</span></span>

<span data-ttu-id="1f71d-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span><span class="sxs-lookup"><span data-stu-id="1f71d-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="1f71d-154">Norėdami apibrėžti formulę, sukurkite formulę skaičiuoklėje ir tada nukopijuokite ją į langą **Dizainas**.</span><span class="sxs-lookup"><span data-stu-id="1f71d-154">To define the formula, create the formula in the spreadsheet, and then copy it to the **Design** window.</span></span> <span data-ttu-id="1f71d-155">„Finance and Operations“ susieta lentelė paprastai būna pavadinta „AXTable1“.</span><span class="sxs-lookup"><span data-stu-id="1f71d-155">A Finance and Operations bound table will typically be named "AXTable1".</span></span> <span data-ttu-id="1f71d-156">Pvz., norėdami susumuoti paraiškų už 1–4 ketvirčių stulpelius skaičiuoklėje, sukurkite tokią formulę: AxTable1\[Paraiška už 1 ketvirtį\] + AxTable1\[Paraiška už 2 ketvirtį\] + AxTable1\[Paraiška už 3 ketvirtį\] + AxTable1\[Paraiška už 4 ketvirtį\].</span><span class="sxs-lookup"><span data-stu-id="1f71d-156">For example, to summarize Request Q1 : Request Q4 columns in the spreadsheet, the formula = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].</span></span>

<span data-ttu-id="1f71d-157">Pakartokite šiuos veiksmus ir įterpkite stulpelį **Koregavimas**.</span><span class="sxs-lookup"><span data-stu-id="1f71d-157">Repeat these steps to insert the **Adjustment** column.</span></span> <span data-ttu-id="1f71d-158">Šiam stulpeliui priskirkite formulę: AxTable1\[Bendra užklausų suma\]\*$I$1</span><span class="sxs-lookup"><span data-stu-id="1f71d-158">Use formula = AxTable1\[Total request\]\*$I$1 for this column.</span></span> <span data-ttu-id="1f71d-159">Tokiu būdu langelio I1 vertė bus padauginta iš stulpelio **Bendra užklausų suma** verčių, kad būtų apskaičiuotos koregavimo sumos.</span><span class="sxs-lookup"><span data-stu-id="1f71d-159">This will take the value in cell I1 and multiply the values in the **Total request** column to calculate adjustment amounts.</span></span>

<span data-ttu-id="1f71d-160">Įrašykite ir uždarykite „Excel“ failą.</span><span class="sxs-lookup"><span data-stu-id="1f71d-160">Save and close the Excel file.</span></span> <span data-ttu-id="1f71d-161">Vėl atidarykite „Finance and Operations“ ir dalyje **Maketai** spustelėkite **Šablonas &gt; Naujinti**, kad įkeltumėte įrašytą „Excel“ šabloną naudoti biudžeto plane.</span><span class="sxs-lookup"><span data-stu-id="1f71d-161">Return to Finance and Operations, and in **Layouts**, click **Template &gt; Upload** to upload the saved Excel template to be used for the budget plan.</span></span> 

<span data-ttu-id="1f71d-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span><span class="sxs-lookup"><span data-stu-id="1f71d-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span></span> 

<span data-ttu-id="1f71d-163">Uždarykite slankiklį **Maketai**.</span><span class="sxs-lookup"><span data-stu-id="1f71d-163">Close the **Layouts** slider.</span></span> <span data-ttu-id="1f71d-164">Dokumente **Biudžeto planas** spustelėkite **Darbalapis**, kad dokumentą peržiūrėtumėte ir redaguotumėte programoje „Excel“.</span><span class="sxs-lookup"><span data-stu-id="1f71d-164">In **Budget plan** document, click **Worksheet** to view and edit the document in Excel.</span></span> <span data-ttu-id="1f71d-165">Atkreipkite dėmesį, kad pakoreguotas „Excel“ šablonas buvo naudojamas šiam biudžeto plano darbalapiui sukurti, o apskaičiuoti stulpeliai atnaujinti naudojant formules, kurios buvo apibrėžtos ankstesniuose veiksmuose.</span><span class="sxs-lookup"><span data-stu-id="1f71d-165">Note that the adjusted Excel template was used to create this budget plan worksheet and calculated columns are updated using the formulas that were defined in the previous steps.</span></span> 

<span data-ttu-id="1f71d-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span><span class="sxs-lookup"><span data-stu-id="1f71d-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span></span>

## <a name="tips--tricks-for-creating-budget-plan-templates"></a><span data-ttu-id="1f71d-167">Biudžeto plano šablonų kūrimo patarimai</span><span class="sxs-lookup"><span data-stu-id="1f71d-167">Tips & tricks for creating budget plan templates</span></span>
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a><span data-ttu-id="1f71d-168">Ar galiu į biudžeto plano šabloną įtraukti ir naudoti papildomus duomenų šaltinius?</span><span class="sxs-lookup"><span data-stu-id="1f71d-168">Can I add and use additional data sources to a budget plan template?</span></span>

<span data-ttu-id="1f71d-169">Taip, galite naudoti meniu **Dizainas**, kad į tą patį ar kitus „Excel“ šablono lapus įtrauktumėte papildomų objektų.</span><span class="sxs-lookup"><span data-stu-id="1f71d-169">Yes, you can use the **Design** menu to add additional entities to the same or other sheets in the Excel template.</span></span> <span data-ttu-id="1f71d-170">Pvz., galite įtraukti duomenų šaltinį **BudgetPlanProposedProject**, kad sukurtumėte ir tvarkytumėte siūlomų projektų sąrašą tuo pačiu metu, kai dirbate su biudžeto plano duomenimis programoje „Excel“.</span><span class="sxs-lookup"><span data-stu-id="1f71d-170">For example, you can add the **BudgetPlanProposedProject** data source to create and maintain a list of proposed projects at the same time when working with budget plan data in Excel.</span></span> <span data-ttu-id="1f71d-171">Atkreipkite dėmesį, kad įtraukiant didelės apimties duomenų šaltinius gali būti paveiktas „Excel“ darbaknygės veikimas.</span><span class="sxs-lookup"><span data-stu-id="1f71d-171">Note that including high-volume data sources might impact performance of the Excel workbook.</span></span> 

<span data-ttu-id="1f71d-172">Galite naudoti dalyje **Duomenų jungtis** pateiktą parinktį **Filtras**, kad į papildomus duomenų šaltinius įtrauktumėte norimų filtrų.</span><span class="sxs-lookup"><span data-stu-id="1f71d-172">You can use the **Filter** option in the **Data Connector** to add desired filters to additional data sources.</span></span>

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a><span data-ttu-id="1f71d-173">Ar galiu nuo kitų vartotojų paslėpti duomenų jungties parinktį Dizainas?</span><span class="sxs-lookup"><span data-stu-id="1f71d-173">Can I hide the Design option in the Data connector for other users?</span></span>

<span data-ttu-id="1f71d-174">Taip, atidarykite dalies **Duomenų jungiklis** parinktis, kad paslėptumėte parinktį **Dizainas** nuo kitų vartotojų.</span><span class="sxs-lookup"><span data-stu-id="1f71d-174">Yes, open the **Data Connector** options to hide the **Design** option from other users.</span></span>

<span data-ttu-id="1f71d-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span><span class="sxs-lookup"><span data-stu-id="1f71d-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span></span>

<span data-ttu-id="1f71d-176">Išplėskite dalies **Duomenų jungtis** parinktis ir atžymėkite žymės langelį **Įjungti dizainą**.</span><span class="sxs-lookup"><span data-stu-id="1f71d-176">Expand **Data connector options** and clear the **Enable design** check box.</span></span> <span data-ttu-id="1f71d-177">Tokiu būdu paslėpsite dalies **Duomenų jungtis** parinktį **Dizainas**.</span><span class="sxs-lookup"><span data-stu-id="1f71d-177">This will hide the **Design** option from the **Data connector**.</span></span>

<span data-ttu-id="1f71d-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span><span class="sxs-lookup"><span data-stu-id="1f71d-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span></span>

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a><span data-ttu-id="1f71d-179">Ar galiu užtikrinti, kad vartotojai, dirbdami su duomenimis, atsitiktinai neuždarytų duomenų jungties?</span><span class="sxs-lookup"><span data-stu-id="1f71d-179">Can I prevent users from accidently closing the Data connector while working with data?</span></span>

<span data-ttu-id="1f71d-180">Rekomenduojame užrakinti šabloną, kad vartotojai jos atsitiktinai neišjungtų.</span><span class="sxs-lookup"><span data-stu-id="1f71d-180">We recommend locking the template to prevent users from closing it.</span></span> <span data-ttu-id="1f71d-181">Norėdami įjungti užraktą, spustelėkite **Duomenų jungtis**, viršutiniame kairiajame kampe pasirodo rodyklė.</span><span class="sxs-lookup"><span data-stu-id="1f71d-181">To turn on the lock, click the **Data connector**, in the top right corner an arrow appears.</span></span> 

<span data-ttu-id="1f71d-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span><span class="sxs-lookup"><span data-stu-id="1f71d-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span></span> 

<span data-ttu-id="1f71d-183">Spustelėkite rodyklę, kad būtų parodytas papildomas meniu.</span><span class="sxs-lookup"><span data-stu-id="1f71d-183">Click the arrow for an additional menu.</span></span> <span data-ttu-id="1f71d-184">Pasirinkite **Užrakinti**.</span><span class="sxs-lookup"><span data-stu-id="1f71d-184">Select **Lock**.</span></span>

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a><span data-ttu-id="1f71d-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span><span class="sxs-lookup"><span data-stu-id="1f71d-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span></span>

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a><span data-ttu-id="1f71d-186">Ar galiu biudžeto plano šablonuose naudoti kitas „Excel“ funkcijas, pvz., langelių formatavimą, spalvas, sąlyginį formatavimą ir diagramas?</span><span class="sxs-lookup"><span data-stu-id="1f71d-186">Can I use other Excel features, like cell formatting, colors, conditional formatting, and charts with my budget plan templates?</span></span>

<span data-ttu-id="1f71d-187">Taip, biudžeto plano šablonuose veiks dauguma standartinių „Excel“ funkcijų.</span><span class="sxs-lookup"><span data-stu-id="1f71d-187">Yes, most of the standard Excel capabilities will work in budget plan templates.</span></span> <span data-ttu-id="1f71d-188">Rekomenduojame naudoti kodavimo spalvomis funkciją, kad vartotojai galėtų lengviau atskirti tik skaitomus ir redaguojamus stulpelius.</span><span class="sxs-lookup"><span data-stu-id="1f71d-188">We recommend using color-coding for users to distinguish between read-only and editable columns.</span></span> <span data-ttu-id="1f71d-189">Sąlyginio formatavimo funkciją galima naudoti norint paryškinti problematiškas biudžeto sritis.</span><span class="sxs-lookup"><span data-stu-id="1f71d-189">Conditional formatting can be used to highlight problematic areas of the budget.</span></span> <span data-ttu-id="1f71d-190">Bendras stulpelių sumas galima lengvai pateikti naudojant „Excel“ formules virš lentelės.</span><span class="sxs-lookup"><span data-stu-id="1f71d-190">Column totals can easily be presented by using standard Excel formulas above the table.</span></span>

<span data-ttu-id="1f71d-191">Taip pat galite kurti ir naudoti suvestinės lenteles bei diagramas, norėdami atlikti papildomų biudžeto duomenų grupavimo ir vizualizavimo veiksmų.</span><span class="sxs-lookup"><span data-stu-id="1f71d-191">You can also create and use pivot tables and charts for additional groupings and visualizations of budget data.</span></span> <span data-ttu-id="1f71d-192">Skirtuko **Duomenys** grupėje **Ryšiai** spustelėkite **Atnaujinti viską**, o tada spustelėkite **Ryšių ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="1f71d-192">On the **Data** tab, in the **Connections** group, click **Refresh All**, and then click **Connection Properties**.</span></span> <span data-ttu-id="1f71d-193">Spustelėkite skirtuką **Naudojimas**. Dalyje **Naujinti** pažymėkite žymės langelį **Naujinti duomenis atidarant failą**.</span><span class="sxs-lookup"><span data-stu-id="1f71d-193">Click the **Usage** tab. Under **Refresh**, select the **Refresh data when opening the file** check box.</span></span> 

<span data-ttu-id="1f71d-194">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span><span class="sxs-lookup"><span data-stu-id="1f71d-194">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span></span>




