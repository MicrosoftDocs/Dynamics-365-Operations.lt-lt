---
title: Analizės įtraukimas į darbo sritis naudojant „Power BI Embedded“
description: Šioje temoje rodoma, kaip įterpti „Power BI“ ataskaitą darbo srities skirtuke Analizė.
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: de85bf52d8e3415549db64501b2435ebd7377fef
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025859"
---
# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a><span data-ttu-id="205cb-103">Analizės įtraukimas į darbo sritis naudojant „Power BI Embedded“</span><span class="sxs-lookup"><span data-stu-id="205cb-103">Add analytics to workspaces by using Power BI Embedded</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="205cb-104">Šią funkcija palaiko 7.2 arba vėlesnės versijos „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="205cb-104">This feature is supported in Finance and Operations (version 7.2 and later).</span></span>

## <a name="introduction"></a><span data-ttu-id="205cb-105">Įžanga</span><span class="sxs-lookup"><span data-stu-id="205cb-105">Introduction</span></span>
<span data-ttu-id="205cb-106">Šioje temoje rodoma, kaip įterpti „Microsoft Power BI“ ataskaitą darbo srities skirtuke **Analizė**.</span><span class="sxs-lookup"><span data-stu-id="205cb-106">This topic shows how to embed a Microsoft Power BI report on the **Analytics** tab of a workspace.</span></span> <span data-ttu-id="205cb-107">Čia pateiktame pavyzdyje išplėsime Transporto parko valdymo programos darbo sritį **Rezervacijų valdymas**, kad skirtuke **Analizė** galėtume įterpti analizės darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="205cb-107">For the example that is given here, we will extend the **Reservation management** workspace in the Fleet Management application to embed an analytical workspace on an **Analytics** tab.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="205cb-108">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="205cb-108">Prerequisites</span></span>
+ <span data-ttu-id="205cb-109">Prieiga prie projektuotojo terpės, kurioje veikia 8-asis ar naujesnis platformos atnaujinimas.</span><span class="sxs-lookup"><span data-stu-id="205cb-109">Access to a developer environment that runs Platform update 8 or later.</span></span>
+ <span data-ttu-id="205cb-110">Naudojant „Microsoft Power BI Desktop Dekstop“ programą sukurta analizės ataskaita (.pbix failas), kurioje yra iš objekto parduotuvės duomenų bazės gaunamas duomenų modelis.</span><span class="sxs-lookup"><span data-stu-id="205cb-110">An analytical report (.pbix file) that was created by using Microsoft Power BI Desktop, and that has a data model that is sourced from the Entity store database.</span></span>

## <a name="overview"></a><span data-ttu-id="205cb-111">Apžvalga</span><span class="sxs-lookup"><span data-stu-id="205cb-111">Overview</span></span>
<span data-ttu-id="205cb-112">Nesvarbu, ar išplečiate esamą, ar sukuriate naują asmeninę programos darbo sritį, informatyviems ir interaktyviems verslo duomenų rodiniams pristatyti galite naudoti įdėtuosius analizės rodinius.</span><span class="sxs-lookup"><span data-stu-id="205cb-112">Whether you extend an existing application workspace or introduce a new workspace of your own, you can use embedded analytical views to deliver insightful and interactive views of your business data.</span></span> <span data-ttu-id="205cb-113">Analizės darbo srities įtraukimo procesą sudaro keturi veiksmai.</span><span class="sxs-lookup"><span data-stu-id="205cb-113">The process for adding an analytical workspace tab has four steps.</span></span>

1. <span data-ttu-id="205cb-114">Įtraukite .pbix failą kaip „Dynamics 365“ išteklių.</span><span class="sxs-lookup"><span data-stu-id="205cb-114">Add a .pbix file as a Dynamics 365 resource.</span></span>
2. <span data-ttu-id="205cb-115">Apibrėžkite analizės darbo srities skirtuką.</span><span class="sxs-lookup"><span data-stu-id="205cb-115">Define an analytical workspace tab.</span></span>
3. <span data-ttu-id="205cb-116">Įterpkite .pbix išteklių darbo srities skirtuke.</span><span class="sxs-lookup"><span data-stu-id="205cb-116">Embed the .pbix resource on the workspace tab.</span></span>
4. <span data-ttu-id="205cb-117">Pasirinktina: įtraukite plėtinius, kad tinkintumėte rodinį.</span><span class="sxs-lookup"><span data-stu-id="205cb-117">Optional: Add extensions to customize the view.</span></span>

> [!NOTE]
> <span data-ttu-id="205cb-118">Daugiau informacijos apie tai, kaip kurti analizės ataskaitas, ieškokite [Darbo su „Power BI Desktop“ pradžia](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="205cb-118">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span></span> <span data-ttu-id="205cb-119">Šis puslapis – puikus įžvalgų, galinčių padėti kurti patrauklius sprendimus analizės ataskaitoms, šaltinis.</span><span class="sxs-lookup"><span data-stu-id="205cb-119">This page is a great source for insights that can help you create compelling analytical reporting solutions.</span></span>

## <a name="add-a-pbix-file-as-a-resource"></a><span data-ttu-id="205cb-120">Įtraukite .pbix failą kaip išteklių.</span><span class="sxs-lookup"><span data-stu-id="205cb-120">Add a .pbix file as a resource</span></span>
<span data-ttu-id="205cb-121">Prieš pradėdami, turite sukurti arba gauti „Power BI“ ataskaitą, kurią įdėsite į darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="205cb-121">Before you begin, you must create or obtain the Power BI report that you will embed in the workspace.</span></span> <span data-ttu-id="205cb-122">Daugiau informacijos apie tai, kaip kurti analizės ataskaitas, ieškokite [Darbo su „Power BI Desktop“ pradžia](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="205cb-122">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span></span>

<span data-ttu-id="205cb-123">Atlikite šiuos veiksmus, norėdami įtraukti .pbix failą kaip „Visual Studio“ projekto artefaktą.</span><span class="sxs-lookup"><span data-stu-id="205cb-123">Follow these steps to add a .pbix file as a Visual Studio project artifact.</span></span>

1. <span data-ttu-id="205cb-124">Naujo projekto atitinkamame modelyje kūrimas.</span><span class="sxs-lookup"><span data-stu-id="205cb-124">Create a new project in the appropriate model.</span></span>
2. <span data-ttu-id="205cb-125">Sprendimų naršyklėje pasirinkite projektą, spustelėkite dešiniuoju klavišu ir pasirinkite **Įtraukti** \> **Nauja prekė**.</span><span class="sxs-lookup"><span data-stu-id="205cb-125">In Solution Explorer, select the project, right-click, and then select **Add** \> **New Item**.</span></span>
3. <span data-ttu-id="205cb-126">Dialogo lange **Naujo elemento įtraukimas**, esančio parinktyje **Operacijų artefaktai**, pasirinkite šabloną **Išteklius**.</span><span class="sxs-lookup"><span data-stu-id="205cb-126">In the **Add New Item** dialog box, under **Operations Artifacts**, select the **Resource** template.</span></span>
4. <span data-ttu-id="205cb-127">Įveskite pavadinimą, kuris bus naudojamas nurodant ataskaitą X++ metaduomenyse, tada spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="205cb-127">Enter a name that will be used to reference the report in X++ metadata, and then click **Add**.</span></span>

    ![Naujos prekės dialogo lango įtraukimas](media/analytical-workspace-add.png)

5. <span data-ttu-id="205cb-129">Raskite .pbix failą, kuriame yra analizės ataskaitos apibrėžimas, tada spustelėkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="205cb-129">Find the .pbix file that contains the definition of the analytical report, and then click **Open**.</span></span>

    ![Pasirinkite ištekliaus failo dialogo langą](media/analytical-workspace-select-resource.png)

<span data-ttu-id="205cb-131">Įtraukę .pbix failą kaip „Dynamics 365“ išteklių, ataskaitas galite įdėti į darbo sritis ir, naudodami meniu elementus, įtraukti tiesioginių saitų.</span><span class="sxs-lookup"><span data-stu-id="205cb-131">Now that you've added the .pbix file as a Dynamics 365 resource, you can embed the reports in workspaces and add direct links by using menu items.</span></span>

## <a name="add-a-tab-control-to-an-application-workspace"></a><span data-ttu-id="205cb-132">Skirtuko valdiklio įtraukimas į programos darbo sritį</span><span class="sxs-lookup"><span data-stu-id="205cb-132">Add a tab control to an application workspace</span></span>
<span data-ttu-id="205cb-133">Šiame pavyzdyje išplėsime Transporto parko valdymo modelio darbo sritį **Rezervacijų valdymas** į formos **FMClerkWorkspace** apibrėžimą įtraukdami skirtuką **Analizė**.</span><span class="sxs-lookup"><span data-stu-id="205cb-133">In this example, we will extend the **Reservation management** workspace in the Fleet Management model by adding the **Analytics** tab to the definition of the **FMClerkWorkspace** form.</span></span>

<span data-ttu-id="205cb-134">Toliau pavaizduota, kaip forma **FMClerkWorkspace** atrodo „Microsoft Visual Studio“ dizaineryje.</span><span class="sxs-lookup"><span data-stu-id="205cb-134">The following illustration shows what the **FMClerkWorkspace** form looks like in the designer in Microsoft Visual Studio.</span></span>

![Forma FMClerkWorkspace prieš pakeitimus](media/analytical-workspace-definition-before.png)

<span data-ttu-id="205cb-136">Atlikite šiuos veiksmus, norėdami išplėsti darbo srities **Rezervacijų valdymas** formos apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="205cb-136">Follow these steps to extend the form definition for the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="205cb-137">Norėdami išplėsti dizaino apibrėžimą, atidarykite formų dizainerį.</span><span class="sxs-lookup"><span data-stu-id="205cb-137">Open the form designer to extend the design definition.</span></span>
2. <span data-ttu-id="205cb-138">Dizaino apraše pasirinkite viršutinį elementą, pažymėtą **Dizainas | Šablonas: darbo srities veikimas**.</span><span class="sxs-lookup"><span data-stu-id="205cb-138">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
3. <span data-ttu-id="205cb-139">Norėdami įtraukti naują valdiklį pavadinimu **FormTabControl1**, spustelėkite dešiniuoju mygtuku ir pasirinkite **Naujas** \> **Skirtukas**.</span><span class="sxs-lookup"><span data-stu-id="205cb-139">Right-click, and then select **New** \> **Tab** to add a new control that is named **FormTabControl1**.</span></span>
4. <span data-ttu-id="205cb-140">Formų dizaineryje pasirinkite **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="205cb-140">In the form designer, select **FormTabControl1**.</span></span>
5. <span data-ttu-id="205cb-141">Spustelėkite dešiniuoju mygtuku ir pasirinkite **Naujo skirtuko puslapis**, kad įtrauktumėte naujo skirtuko puslapį.</span><span class="sxs-lookup"><span data-stu-id="205cb-141">Right-click, and then select **New Tab Page** to add a new tab page.</span></span>
6. <span data-ttu-id="205cb-142">Pervadinkite skirtuko puslapį suteikdami prasmingesnį pavadinimą, pvz, **Darbo sritis**.</span><span class="sxs-lookup"><span data-stu-id="205cb-142">Rename the tab page to something meaningful, such as **Workspace**.</span></span>
7. <span data-ttu-id="205cb-143">Formų dizaineryje pasirinkite **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="205cb-143">In the form designer, select **FormTabControl1**.</span></span>
8. <span data-ttu-id="205cb-144">Spustelėkite dešiniuoju mygtuku ir pasirinkite **Naujo skirtuko puslapis**.</span><span class="sxs-lookup"><span data-stu-id="205cb-144">Right-click, and then select **New Tab Page**.</span></span>
9. <span data-ttu-id="205cb-145">Pervadinkite skirtuko puslapį suteikdami prasmingesnį pavadinimą, pvz, **Analizė**.</span><span class="sxs-lookup"><span data-stu-id="205cb-145">Rename the tab page to something meaningful, such as **Analytics**.</span></span>
10. <span data-ttu-id="205cb-146">Formų dizaineryje pasirinkite **Analizė (skirtuko puslapis)**.</span><span class="sxs-lookup"><span data-stu-id="205cb-146">In the form designer, select **Analytics (Tab Page)**.</span></span>
11. <span data-ttu-id="205cb-147">Ypatybę **Antraštė** nustatykite į **Analizė**.</span><span class="sxs-lookup"><span data-stu-id="205cb-147">Set the **Caption** property to **Analytics**.</span></span>
12. <span data-ttu-id="205cb-148">Dešiniuoju pelės mygtuku spustelėkite valdiklį, tada pasirinkite **Naujas** \> **Grupė** ir įtraukite naują formos grupės valdiklį.</span><span class="sxs-lookup"><span data-stu-id="205cb-148">Right-click the control, and then select **New** \> **Group** to add a new form group control.</span></span>
13. <span data-ttu-id="205cb-149">Pervadinkite formos grupę suteikdami prasmingesnį pavadinimą, pvz, **powerBIReportGroup**.</span><span class="sxs-lookup"><span data-stu-id="205cb-149">Rename the form group to something meaningful, such as **powerBIReportGroup**.</span></span>
14. <span data-ttu-id="205cb-150">Formų dizaineryje pasirinkite **PanoramaBody (skirtukas)**, tada vilkite valdiklį į skirtuką **Darbo sritis**.</span><span class="sxs-lookup"><span data-stu-id="205cb-150">In the form designer, select **PanoramaBody (Tab)**, and then drag the control onto the **Workspace** tab.</span></span>
15. <span data-ttu-id="205cb-151">Dizaino apraše pasirinkite viršutinį elementą, pažymėtą **Dizainas | Šablonas: darbo srities veikimas**.</span><span class="sxs-lookup"><span data-stu-id="205cb-151">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
16. <span data-ttu-id="205cb-152">Spustelėkite dešiniuoju mygtuku ir pasirinkite **Pašalinti šabloną**.</span><span class="sxs-lookup"><span data-stu-id="205cb-152">Right-click, and then select **Remove pattern**.</span></span>
17. <span data-ttu-id="205cb-153">Dešiniuoju pelės mygtuku spustelėkite dar kartą, tada pasirinkite **Pridėti šabloną** \> **Darbo sritis su skirtukais**.</span><span class="sxs-lookup"><span data-stu-id="205cb-153">Right-click again, and then select **Add pattern** \> **Workspace Tabbed**.</span></span>
18. <span data-ttu-id="205cb-154">Pradėkite kurti, kad patvirtintumėte pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="205cb-154">Perform a build to verify your changes.</span></span>

<span data-ttu-id="205cb-155">Toliau pavaizduota, kaip atrodo dizainas pritaikius šiuos pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="205cb-155">The following illustration shows what the design looks like after these changes are applied.</span></span>

![FMClerkWorkspace po pakeitimų](media/analytical-workspace-definition-after.png)

<span data-ttu-id="205cb-157">Pridėję formų valdiklių, kurie bus naudojami darbo srities ataskaitai įdėti, turite apibrėžti, kokio dydžio turi būti pagrindinis valdiklis, kad tilptų į maketą.</span><span class="sxs-lookup"><span data-stu-id="205cb-157">Now that you've added the form controls that will be used to embed the workspace report, you must define the size of the parent control so that it accommodates the layout.</span></span> <span data-ttu-id="205cb-158">Pagal numatytuosius nustatymus puslapiai **Filtrų sritis** ir **Skirtukas** bus rodomi ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="205cb-158">By default, both the **Filters Pane** page and the **Tab** page will be visible on the report.</span></span> <span data-ttu-id="205cb-159">Tačiau šių valdiklių matomumą galite keisti atitinkamai pagal tikslinį ataskaitos vartotoją.</span><span class="sxs-lookup"><span data-stu-id="205cb-159">However, you can change the visibility of these controls as appropriate for the target consumer of the report.</span></span>

> [!NOTE]
> <span data-ttu-id="205cb-160">Norint išlaikyti nuoseklumą, įdėtoms darbo sritims rekomenduojame naudoti plėtinius, kurie paslėptų puslapius **Filtrų sritis** ir **Skirtukas**.</span><span class="sxs-lookup"><span data-stu-id="205cb-160">For embedded workspaces, we recommend that you use extensions to hide both the **Filters Pane** and **Tab** pages, for consistency.</span></span>

<span data-ttu-id="205cb-161">Užbaigėte prašymo formos apibrėžimo išplėtimo užduotį.</span><span class="sxs-lookup"><span data-stu-id="205cb-161">You've now completed the task of extending the application form definition.</span></span> <span data-ttu-id="205cb-162">Daugiau informacijos apie tai, kaip naudoti plėtinius tinkinimams atlikti, ieškokite [Tinkinimas naudojant plėtinius ir perdengimą](../extensibility/customization-overlayering-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="205cb-162">For more information about how to use extensions to do customizations, see [Customize through extension and overlayering](../extensibility/customization-overlayering-extensions.md).</span></span>

## <a name="add-x-business-logic-to-embed-a-viewer-control"></a><span data-ttu-id="205cb-163">X ++ verslo logikos įtraukimas norint įdėti peržiūros programos valdiklį</span><span class="sxs-lookup"><span data-stu-id="205cb-163">Add X++ business logic to embed a viewer control</span></span>
<span data-ttu-id="205cb-164">Atlikite šiuos veiksmus, norėdami įtraukti verslo logiką, inicijuojančią į darbo sritį **Rezervacijų valdymas** įdėtą peržiūros programos valdiklį.</span><span class="sxs-lookup"><span data-stu-id="205cb-164">Follow these steps to add business logic that initializes the report viewer control that is embedded in the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="205cb-165">Norėdami išplėsti dizaino apibrėžimą, atidarykite **FMClerkWorkspace** formų dizainerį.</span><span class="sxs-lookup"><span data-stu-id="205cb-165">Open the **FMClerkWorkspace** form designer to extend the design definition.</span></span>
2. <span data-ttu-id="205cb-166">Paspauskite F7, kad pasiektumėte kodo aprašo kodą.</span><span class="sxs-lookup"><span data-stu-id="205cb-166">Press F7 to access the code behind the code definition.</span></span>
3. <span data-ttu-id="205cb-167">Įtraukite toliau nurodytą X++ kodą.</span><span class="sxs-lookup"><span data-stu-id="205cb-167">Add the following X++ code.</span></span>

    ```xpp
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                // initialize the PBI report control using shared helper
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
        }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. <span data-ttu-id="205cb-168">Pradėkite kurti, kad patvirtintumėte pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="205cb-168">Perform a build to verify your changes.</span></span>

<span data-ttu-id="205cb-169">Užbaigėte verslo logikos įtraukimo užduotį, skirtą įdėtam ataskaitų peržiūros programos valdikliui inicijuoti.</span><span class="sxs-lookup"><span data-stu-id="205cb-169">You've now completed the task of adding business logic to initialize the embedded report viewer control.</span></span> <span data-ttu-id="205cb-170">Toliau pavaizduota, kaip atrodo darbo sritis pritaikius šiuos pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="205cb-170">The following illustration shows what the workspace looks like after these changes are applied.</span></span>

![Į darbo sritį įdėta ataskaita](media/analytical-workspace-final.png)

> [!NOTE]
> <span data-ttu-id="205cb-172">Esamą operacijų rodinį galite pasiekti naudodami virš puslapio pavadinimo esančius darbo srities skirtukus.</span><span class="sxs-lookup"><span data-stu-id="205cb-172">You can access the existing operational view by using the workspace tabs below the page title.</span></span>

## <a name="reference"></a><span data-ttu-id="205cb-173">Nuoroda</span><span class="sxs-lookup"><span data-stu-id="205cb-173">Reference</span></span>

### <a name="pbireporthelperinitializereportcontrol-method"></a><span data-ttu-id="205cb-174">PBIReportHelper.initializeReportControl metodas</span><span class="sxs-lookup"><span data-stu-id="205cb-174">PBIReportHelper.initializeReportControl method</span></span>
<span data-ttu-id="205cb-175">Šiame skyriuje pateikiama informacija apie pagelbiklio klasę, naudojamą „Power BI“ ataskaitai (.pbix išteklius) į formos grupės valdiklį įdėti.</span><span class="sxs-lookup"><span data-stu-id="205cb-175">This section provides information about the helper class that is used to embed a Power BI report (.pbix resource) in a form group control.</span></span>

#### <a name="syntax"></a><span data-ttu-id="205cb-176">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="205cb-176">Syntax</span></span>
```xpp
public static void initializeReportControl(
    str                 _resourceName,
    FormGroupControl    _formGroupControl,
    str                 _defaultPageName = '',
    boolean             _showFilterPane = false,
    boolean             _showNavPane = false,
    List                _defaultFilters = new List(Types::Class))
```

#### <a name="parameters"></a><span data-ttu-id="205cb-177">Parametrai</span><span class="sxs-lookup"><span data-stu-id="205cb-177">Parameters</span></span>

| <span data-ttu-id="205cb-178">Vardas</span><span class="sxs-lookup"><span data-stu-id="205cb-178">Name</span></span>             | <span data-ttu-id="205cb-179">aprašymas</span><span class="sxs-lookup"><span data-stu-id="205cb-179">Description</span></span>                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="205cb-180">resourceName</span><span class="sxs-lookup"><span data-stu-id="205cb-180">resourceName</span></span>     | <span data-ttu-id="205cb-181">.pbix ištekliaus pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="205cb-181">The name of the .pbix resource.</span></span>                                                                              |
| <span data-ttu-id="205cb-182">formGroupControl</span><span class="sxs-lookup"><span data-stu-id="205cb-182">formGroupControl</span></span> | <span data-ttu-id="205cb-183">Formos grupės valdiklis, kuriam bus taikomas „Power BI“ ataskaitos valdiklis.</span><span class="sxs-lookup"><span data-stu-id="205cb-183">The form group control to apply the Power BI report control to.</span></span>                                              |
| <span data-ttu-id="205cb-184">defaultPageName</span><span class="sxs-lookup"><span data-stu-id="205cb-184">defaultPageName</span></span>  | <span data-ttu-id="205cb-185">Numatytasis puslapio pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="205cb-185">The default page name.</span></span>                                                                                       |
| <span data-ttu-id="205cb-186">showFilterPane</span><span class="sxs-lookup"><span data-stu-id="205cb-186">showFilterPane</span></span>   | <span data-ttu-id="205cb-187">Būlio logikos vertė, kuria nurodoma, ar filtro sritis turi būti rodoma (**true**), ar paslėpta (**klaidinga**).</span><span class="sxs-lookup"><span data-stu-id="205cb-187">A Boolean value that indicates whether the filter pane should be shown (**true**) or hidden (**false**).</span></span>     |
| <span data-ttu-id="205cb-188">showNavPane</span><span class="sxs-lookup"><span data-stu-id="205cb-188">showNavPane</span></span>      | <span data-ttu-id="205cb-189">Būlio logikos vertė, kuria nurodoma, ar naršymo sritis turi būti rodoma (**true**), ar paslėpta (**klaidinga**).</span><span class="sxs-lookup"><span data-stu-id="205cb-189">A Boolean value that indicates whether the navigation pane should be shown (**true**) or hidden (**false**).</span></span> |
| <span data-ttu-id="205cb-190">defaultFilters</span><span class="sxs-lookup"><span data-stu-id="205cb-190">defaultFilters</span></span>   | <span data-ttu-id="205cb-191">Numatytieji „Power BI“ ataskaitos filtrai.</span><span class="sxs-lookup"><span data-stu-id="205cb-191">The default filters for the Power BI report.</span></span>                                                                 |
