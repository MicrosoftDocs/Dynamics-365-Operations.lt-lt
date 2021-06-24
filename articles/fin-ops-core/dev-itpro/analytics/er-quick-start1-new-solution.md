---
title: Suprojektuokite naują ER sprendimą tinkintos ataskaitos spausdinimui
description: Šioje temoje paaiškinama, kaip suprojektuoti elektroninį ataskaitos sprendimą tinkintos ataskaitos spausdinimui.
author: NickSelin
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0f5a3ac7cae58d17409ea081ec30f61cecf29ce9
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224039"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a><span data-ttu-id="7dab4-103">Suprojektuokite naują ER sprendimą tinkintos ataskaitos spausdinimui</span><span class="sxs-lookup"><span data-stu-id="7dab4-103">Design a new ER solution to print a custom report</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7dab4-104">Toliau atlikti žingsniai paaiškina, kaip vartotojas sistemos administratoriaus, elektroninės ataskaitos kūrėjo ar elektroninės ataskaitos funkcijų konsultanto vaidmenyje gali konfigūruoti ES darbo grafiko sprendimus, projektuoti reikiamas naujo ER konfigūracijas prieigai prie konkrečių verslo domeno duomenų ir kurti tinkintą ataskaitą „Microsoft Office“ formate.</span><span class="sxs-lookup"><span data-stu-id="7dab4-104">The following steps explain how a user in the System Administrator, Electronic Reporting Developer, or Electronic Reporting Functional Consultant role can configure parameters of the ER framework, design the required ER configurations of a new ER solution to access the data of a particular business domain, and generate a custom report in Microsoft Office format.</span></span> <span data-ttu-id="7dab4-105">Šie žingsniai gali būti užbaigti **USMF** bendrovėje.</span><span class="sxs-lookup"><span data-stu-id="7dab4-105">These steps can be completed in the **USMF** company.</span></span>

- [<span data-ttu-id="7dab4-106">ER sistemos konfigūracija</span><span class="sxs-lookup"><span data-stu-id="7dab4-106">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="7dab4-107">ER parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-107">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="7dab4-108">Aktyvuokite ER konfigūracijos tiekėją</span><span class="sxs-lookup"><span data-stu-id="7dab4-108">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="7dab4-109">Peržiūrėkite ER konfigūracijos teikėjų sąrašą</span><span class="sxs-lookup"><span data-stu-id="7dab4-109">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="7dab4-110">Pridėkite naują ER konfigūracijos tiekėją</span><span class="sxs-lookup"><span data-stu-id="7dab4-110">Add a new ER configuration provider</span></span>](#AddProvider)
        - [<span data-ttu-id="7dab4-111">Aktyvuokite ER konfigūracijos tiekėją</span><span class="sxs-lookup"><span data-stu-id="7dab4-111">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="7dab4-112">Suprojektuokite specialų domeno duomenų modelį</span><span class="sxs-lookup"><span data-stu-id="7dab4-112">Design a domain-specific data model</span></span>](#DesignModel)

    - [<span data-ttu-id="7dab4-113">Importuokite naują duomenų modelio konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="7dab4-113">Import a new data model configuration</span></span>](#ImportDataModel)
    - [<span data-ttu-id="7dab4-114">Sukurti naują duomenų modelio konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="7dab4-114">Create a new data model configuration</span></span>](#DesignDataModel)

        - [<span data-ttu-id="7dab4-115">Pavadinkite duomenų modelį</span><span class="sxs-lookup"><span data-stu-id="7dab4-115">Name the data model</span></span>](#NameDataModel)
        - [<span data-ttu-id="7dab4-116">Įtraukite duomenų modelio laukelius</span><span class="sxs-lookup"><span data-stu-id="7dab4-116">Add data model fields</span></span>](#FieldsEntry)
        - [<span data-ttu-id="7dab4-117">Užbaikite duomenų modelio projektavimą</span><span class="sxs-lookup"><span data-stu-id="7dab4-117">Complete the design of the data model</span></span>](#CompleteDataModel)

- [<span data-ttu-id="7dab4-118">Suprojektuokite konfigūruoto duomenų modelio žemėlapį</span><span class="sxs-lookup"><span data-stu-id="7dab4-118">Design a model mapping for the configured data model</span></span>](#DesignMapping)

    - [<span data-ttu-id="7dab4-119">Importuokite naują modelio žemėlapio konfigūravimą</span><span class="sxs-lookup"><span data-stu-id="7dab4-119">Import a new model mapping configuration</span></span>](#ImportModelMapping)
    - [<span data-ttu-id="7dab4-120">Sukurkite naują modelio žemėlapio konfigūravimą</span><span class="sxs-lookup"><span data-stu-id="7dab4-120">Create a new model mapping configuration</span></span>](#CreateModelMapping)

        - [<span data-ttu-id="7dab4-121">Projektuokite naują modelio žemėlapio komponentą</span><span class="sxs-lookup"><span data-stu-id="7dab4-121">Design a new model mapping component</span></span>](#DesignMappingComponent)
        - [<span data-ttu-id="7dab4-122">Įtraukite duomenų šaltinius į prieigos programos lenteles</span><span class="sxs-lookup"><span data-stu-id="7dab4-122">Add data sources to access application tables</span></span>](#AddMmDataSource1)
        - [<span data-ttu-id="7dab4-123">Įtraukite duomenų šaltinius tam, kad prieitumėte prie programos numeracijų</span><span class="sxs-lookup"><span data-stu-id="7dab4-123">Add data sources to access application enumerations</span></span>](#AddMmDataSource2)
        - [<span data-ttu-id="7dab4-124">Įtraukite ER žymes tam, kad sukurtumėte ataskaitą konkrečia kalba</span><span class="sxs-lookup"><span data-stu-id="7dab4-124">Add ER labels to generate a report in a specified language</span></span>](#AddMmLabels)
        - [<span data-ttu-id="7dab4-125">Įtraukite duomenų šaltinį tam, kad paverstumėte numeracijos verčių lyginimo rezultatus į teksto vertes</span><span class="sxs-lookup"><span data-stu-id="7dab4-125">Add a data source to transform the results of comparing enumeration values to a text value</span></span>](#AddMmDataSource3)
        - [<span data-ttu-id="7dab4-126">Susiekite duomenų šaltinius su duomenų modelio laukeliais</span><span class="sxs-lookup"><span data-stu-id="7dab4-126">Bind data sources to data model fields</span></span>](#AddMmBindings1)
        - [<span data-ttu-id="7dab4-127">Užbaikite modelio žemėlapio projektavimą</span><span class="sxs-lookup"><span data-stu-id="7dab4-127">Complete the design of the model mapping</span></span>](#CompleteModelMapping)

- [<span data-ttu-id="7dab4-128">Suprojektuokite tinkintos ataskaitos šabloną</span><span class="sxs-lookup"><span data-stu-id="7dab4-128">Design a template for a custom report</span></span>](#DesignReportTemplate)
- [<span data-ttu-id="7dab4-129">Formato kūrimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-129">Design a format</span></span>](#DesignFormat)

    - [<span data-ttu-id="7dab4-130">Importuokite suprojektuotą formato konfigūravimą</span><span class="sxs-lookup"><span data-stu-id="7dab4-130">Import a designed format configuration</span></span>](#FormatImport)
    - [<span data-ttu-id="7dab4-131">Kurti naują formato konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="7dab4-131">Create a new format configuration</span></span>](#FormatCreate)

        - [<span data-ttu-id="7dab4-132">Importuokite ataskaitos šabloną</span><span class="sxs-lookup"><span data-stu-id="7dab4-132">Import a report template</span></span>](#ImportReportTemplate)
        - [<span data-ttu-id="7dab4-133">Konfigūruokite formatą</span><span class="sxs-lookup"><span data-stu-id="7dab4-133">Configure a format</span></span>](#ConfigureFormat)
        - [<span data-ttu-id="7dab4-134">Nustatykite duomenų susiejimą ataskaitos pavadinimui</span><span class="sxs-lookup"><span data-stu-id="7dab4-134">Define the data binding for a report title</span></span>](#DefineFormatBindings)
        - [<span data-ttu-id="7dab4-135">Peržiūrėkite modelio duomenų šaltinį</span><span class="sxs-lookup"><span data-stu-id="7dab4-135">Review the model data source</span></span>](#ReviewModelDataSource)
        - [<span data-ttu-id="7dab4-136">Susiekite formato elementus su duomenų šaltinio laukeliais</span><span class="sxs-lookup"><span data-stu-id="7dab4-136">Bind format elements to data source fields</span></span>](#BindFormatElements)

    - [<span data-ttu-id="7dab4-137">Vykdykite suprojektuotą formatą iš ER</span><span class="sxs-lookup"><span data-stu-id="7dab4-137">Run a designed format from ER</span></span>](#RunFormatFromER)

- [<span data-ttu-id="7dab4-138">Suderinkite projektavimo formatą</span><span class="sxs-lookup"><span data-stu-id="7dab4-138">Tune a designed format</span></span>](#TuneFormat)

    - [<span data-ttu-id="7dab4-139">Keiskite formatą tam, kad pakeistumėte sukurto dokumento pavadinimą</span><span class="sxs-lookup"><span data-stu-id="7dab4-139">Modify a format to change the name of a generated document</span></span>](#ModifyToChangeName)
    - [<span data-ttu-id="7dab4-140">Keiskite formatą tam, kad pakeistumėte klausimų seką</span><span class="sxs-lookup"><span data-stu-id="7dab4-140">Modify a format to change the order of questions</span></span>](#ModifyToOrder)
    - [<span data-ttu-id="7dab4-141">Vykdykite pakeistą formatą iš ER</span><span class="sxs-lookup"><span data-stu-id="7dab4-141">Run a modified format from ER</span></span>](#RunFormatFromER2)
    - [<span data-ttu-id="7dab4-142">Užbaikite formato projektą</span><span class="sxs-lookup"><span data-stu-id="7dab4-142">Complete the format design</span></span>](#CompleteFormat)

- [<span data-ttu-id="7dab4-143">Vystykite programos artefaktus tam, kad iškviestumėte suprojektuotą ataskaitą</span><span class="sxs-lookup"><span data-stu-id="7dab4-143">Develop application artefacts to call the designed report</span></span>](#DevelopCustomCode)

    - [<span data-ttu-id="7dab4-144">Šaltinio kodo modifikavimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-144">Modify source code</span></span>](#ModifySourceCode)

        - [<span data-ttu-id="7dab4-145">Įtraukite duomenų sutarties klasę</span><span class="sxs-lookup"><span data-stu-id="7dab4-145">Add a data contract class</span></span>](#DataContractClass)
        - [<span data-ttu-id="7dab4-146">Įtraukite UI kūrėjo klasę</span><span class="sxs-lookup"><span data-stu-id="7dab4-146">Add a UI builder class</span></span>](#UIBuilderClass)
        - [<span data-ttu-id="7dab4-147">Įtraukite duomenų tiekėjo klasę</span><span class="sxs-lookup"><span data-stu-id="7dab4-147">Add a data provider class</span></span>](#DataProviderClass)
        - [<span data-ttu-id="7dab4-148">Įtraukite žymių failą</span><span class="sxs-lookup"><span data-stu-id="7dab4-148">Add a labels file</span></span>](#LabelsFile)
        - [<span data-ttu-id="7dab4-149">Įtraukite ataskaitos paslaugos klasę</span><span class="sxs-lookup"><span data-stu-id="7dab4-149">Add a report service class</span></span>](#ServiceClass)
        - [<span data-ttu-id="7dab4-150">Įtraukite ataskaitos valdiklio klasę</span><span class="sxs-lookup"><span data-stu-id="7dab4-150">Add a report controller class</span></span>](#ControllerClass)
        - [<span data-ttu-id="7dab4-151">Įtraukite meniu elementą</span><span class="sxs-lookup"><span data-stu-id="7dab4-151">Add a menu item</span></span>](#MenuItem)
        - [<span data-ttu-id="7dab4-152">Įtraukite meniu elementą į meniu</span><span class="sxs-lookup"><span data-stu-id="7dab4-152">Add a menu item to a menu</span></span>](#Menu)
        - [<span data-ttu-id="7dab4-153">Sukurkite „Visual Studio“ projektą</span><span class="sxs-lookup"><span data-stu-id="7dab4-153">Build a Visual Studio project</span></span>](#BuildVSProject)

    - [<span data-ttu-id="7dab4-154">Vykdykite formatą iš programos</span><span class="sxs-lookup"><span data-stu-id="7dab4-154">Run a format from the application</span></span>](#RunFormatFromApp)

- [<span data-ttu-id="7dab4-155">Suderinkite suprojektuotą ER sprendimą</span><span class="sxs-lookup"><span data-stu-id="7dab4-155">Tune a designed ER solution</span></span>](#TuneSolution)

    - [<span data-ttu-id="7dab4-156">Keiskite modelio žemėlapį</span><span class="sxs-lookup"><span data-stu-id="7dab4-156">Modify a model mapping</span></span>](#ModifyModelMapping)

        - [<span data-ttu-id="7dab4-157">Įtraukite duomenų šaltinį prieigai prie duomenų sutarties objekto</span><span class="sxs-lookup"><span data-stu-id="7dab4-157">Add data sources to access a data contract object</span></span>](#AddDataSource1)
        - [<span data-ttu-id="7dab4-158">Įtraukite duomenų šaltinį prieigai prie ER formato žemėlapio įrašų</span><span class="sxs-lookup"><span data-stu-id="7dab4-158">Add a data source to access ER format mapping records</span></span>](#AddDataSource2)
        - [<span data-ttu-id="7dab4-159">Įtraukti duomenų šaltinį prieigai prie formato žemėlapio ER formato įrašo vykdymo</span><span class="sxs-lookup"><span data-stu-id="7dab4-159">Add a data source to access a format mapping record of a running ER format</span></span>](#AddDataSource3)
        - [<span data-ttu-id="7dab4-160">Įveskite vykdomo ER formato pavadinimą duomenų modelyje</span><span class="sxs-lookup"><span data-stu-id="7dab4-160">Enter the name of the running ER format in the data model</span></span>](#AddBinding)
        - [<span data-ttu-id="7dab4-161">Užbaikite modelio žemėlapio dizainą</span><span class="sxs-lookup"><span data-stu-id="7dab4-161">Complete the design of the model mapping</span></span>](#CompleteModelMapping2)

    - [<span data-ttu-id="7dab4-162">Keiskite formatą</span><span class="sxs-lookup"><span data-stu-id="7dab4-162">Modify a format</span></span>](#ModifyFormat)

        - [<span data-ttu-id="7dab4-163">Įkelkite naują formato elementą</span><span class="sxs-lookup"><span data-stu-id="7dab4-163">Add a new format element</span></span>](#AddFormatElement)
        - [<span data-ttu-id="7dab4-164">Susiekite įkeltą formato elementą</span><span class="sxs-lookup"><span data-stu-id="7dab4-164">Bind the added format element</span></span>](#BindAddedFormatElement)
        - [<span data-ttu-id="7dab4-165">Užbaikite formato projektavimą</span><span class="sxs-lookup"><span data-stu-id="7dab4-165">Complete the format design</span></span>](#CompleteFormat2)

    - [<span data-ttu-id="7dab4-166">Vykdykite formatą iš programos</span><span class="sxs-lookup"><span data-stu-id="7dab4-166">Run a format from the application</span></span>](#RunFormatFromApp2)
    - [<span data-ttu-id="7dab4-167">Vykdykite formatą iš ER</span><span class="sxs-lookup"><span data-stu-id="7dab4-167">Run a format from ER</span></span>](#RunFormatFromER3)
    - [<span data-ttu-id="7dab4-168">Konfigūruokite formato paskirtį ekrane rodomoje peržiūroje</span><span class="sxs-lookup"><span data-stu-id="7dab4-168">Configure a format destination for on-screen preview</span></span>](#ConfigureDestination)
    - [<span data-ttu-id="7dab4-169">Vykdykite formatą iš programos tam, kad peržiūrėtumėte jį kaip PDF dokumentą</span><span class="sxs-lookup"><span data-stu-id="7dab4-169">Run a format from the application to preview it as a PDF document</span></span>](#RunFormatFromApp3)

- [<span data-ttu-id="7dab4-170">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="7dab4-170">Additional resources</span></span>](#References)

<span data-ttu-id="7dab4-171">Šiame pavyzdyje, sukursite naują ER sprendimą [Klausimynas](../../../human-resources/hr-learning-questionnaires.md) moduliui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-171">In this example, you will create a new ER solution for the [Questionnaire](../../../human-resources/hr-learning-questionnaires.md) module.</span></span> <span data-ttu-id="7dab4-172">Šis naujas ER sprendimas leidžia jums projektuoti ataskaitą naudojant „Microsoft Excel“ darbalapį kaip šabloną.</span><span class="sxs-lookup"><span data-stu-id="7dab4-172">This new ER solution lets you design a report by using a Microsoft Excel worksheet as a template.</span></span> <span data-ttu-id="7dab4-173">Tuomet galite sukurti **Klausimyno** ataskaitą „Excel“ arba PDF formatu, taip pat sukurti esančią SQL serverio ataskaitos paslaugų ataskaitą SSRS.</span><span class="sxs-lookup"><span data-stu-id="7dab4-173">You can then generate the **Questionnaire** report in Excel or PDF format, in addition to generating the existing SQL Server Reporting Services (SSRS) report.</span></span> <span data-ttu-id="7dab4-174">Taip pat galite keisti naują ataskaitą vėliau pagal užklausą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-174">You can also modify the new report later, upon request.</span></span> <span data-ttu-id="7dab4-175">Kodavimas nebūtinas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-175">No coding is required.</span></span>

1. <span data-ttu-id="7dab4-176">Tam, kad vykdytumėte esančią ataskaitą, eikite į **Klausimynas** \> **Projektavimas** \> **Klausimyno ataskaita**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-176">To run the existing report, go to **Questionnaire** \> **Design** \> **Questionnaires report**.</span></span>

    ![Pasirinkite klausimyno ataskaitos meniu elementą klausimyno modulyje tam, kad vykdytumėte esančią SSRS ataskaitą](./media/er-quick-start1-application-menu-origin.png)

2. <span data-ttu-id="7dab4-178">**Klausimyno ataskaitos** teksto laukelyje nurodykite atrankos kriterijus.</span><span class="sxs-lookup"><span data-stu-id="7dab4-178">In the **Questionnaires report** dialog box, specify selection criteria.</span></span> <span data-ttu-id="7dab4-179">Taikykite filtrą taip, kad ataskaita apimtų tik **SBCCrsExam** klausimyną.</span><span class="sxs-lookup"><span data-stu-id="7dab4-179">Apply a filter so that the report includes only the **SBCCrsExam** questionnaire.</span></span>

    ![Atrankos kriterijų klausimyno ataskaitos teksto laukelyje nurodymas](./media/er-quick-start1-ssrs-report-dialog.png)

<span data-ttu-id="7dab4-181">Toliau pateiktame paveikslėlyje rodoma bendra SSRS ataskaitos sukurta versija **SBCCrsExam** klausimynui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-181">The following illustration shows the generated version of the SSRS report for the **SBCCrsExam** questionnaire.</span></span>

![Sukurta SSRS ataskaita](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a><span data-ttu-id="7dab4-183">ER sistemos konfigūracija</span><span class="sxs-lookup"><span data-stu-id="7dab4-183">Configure the ER framework</span></span>

<span data-ttu-id="7dab4-184">Kaip elektroninės ataskaitos kūrėjo vaidmenyje esantis vartotojas, turite sukonfigūruoti mažiausią ER parametrų rinkinį prieš jums pradedant naudoti ER darbotvarkę jūsų naujo ER sprendimo projektavimui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-184">As a user in the Electronic Reporting Developer role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design your new ER solution.</span></span>

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a><span data-ttu-id="7dab4-185">ER parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-185">Configure ER parameters</span></span>

1. <span data-ttu-id="7dab4-186">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-186">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7dab4-187">Darbo srityje **Elektroninės ataskaitos** pasirinkite **Elektroninių ataskaitų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-187">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="7dab4-188">**Elektroninių ataskaitų parametrai** puslapyje **Bendra** skirtuke nustatykite **Įjungti dizaino režimą** parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-188">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="7dab4-189">**Priedai** skirtuke nustatykite tolesnius parametrus:</span><span class="sxs-lookup"><span data-stu-id="7dab4-189">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="7dab4-190">Nustatykite **Konfigūravimai** laukelį į **Failas** **USMF** bendrovei.</span><span class="sxs-lookup"><span data-stu-id="7dab4-190">Set the **Configurations** field to **File** for the **USMF** company.</span></span>
    - <span data-ttu-id="7dab4-191">Nustatykite **Darbo archyvas**, **Laikinas**, **Pagrindinis** ir **Kiti** laukeliai į **Failas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-191">Set **Job archive**, **Temporary**, **Baseline**, and **Others** fields to **File**.</span></span>

<span data-ttu-id="7dab4-192">Norėdami sužinoti daugiau apie ER parametrus, žr. [ER sistemos konfigūracija](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7dab4-192">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a><span data-ttu-id="7dab4-193">ER konfigūracijos tiekėjo aktyvavimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-193">Activate an ER configuration provider</span></span>

<span data-ttu-id="7dab4-194">Visi ER konfigūravimai yra pažymėti kaip turimi ER konfigūravimo tiekėjo.</span><span class="sxs-lookup"><span data-stu-id="7dab4-194">Every ER configuration is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="7dab4-195">Dėl to, turite įjungti ER konfigūravimo tiekėją **Elektroninės ataskaitos** darbo srityje prieš tai, kai pradėsite įtraukti ar redaguoti visas ER konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-195">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit any ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="7dab4-196">Tik ER konfigūracijos savininkas gali redaguoti.</span><span class="sxs-lookup"><span data-stu-id="7dab4-196">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="7dab4-197">Todėl prieš redaguojant ER konfigūraciją atitinkamas ER konfigūracijos tiekėjas turi būti aktyvuotas **Elektroninė ataskaita** darbo srityje.</span><span class="sxs-lookup"><span data-stu-id="7dab4-197">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a><span data-ttu-id="7dab4-198">ER konfigūracijos teikėjų sąrašo peržiūra</span><span class="sxs-lookup"><span data-stu-id="7dab4-198">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="7dab4-199">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-199">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7dab4-200">**Elektroninės ataskaitos** darbo srityje, **Susijusios nuorodos** skyriuje, pasirinkite **Konfigūravimo tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-200">In the **Electronic reporting** workspace, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="7dab4-201">**Konfigūravimo tiekėjai** puslapyje, visi konfigūravimo tiekėjo įrašai turi unikalų pavadinimą ir URL.</span><span class="sxs-lookup"><span data-stu-id="7dab4-201">On the **Configuration providers** page, each configuration provider record has a unique name and URL.</span></span> <span data-ttu-id="7dab4-202">Peržiūrėkite šio puslapio turinį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-202">Review the contents of this page.</span></span> <span data-ttu-id="7dab4-203">Jei įrašas, skirtas **Litware, Inc.** ( `https://www.litware.com`) jau yra, praleiskite sekančią procedūrą, [Pridėkite naują ER konfigūracijos teikėją](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="7dab4-203">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a><span data-ttu-id="7dab4-204">Pridėkite naują ER konfigūracijos tiekėją</span><span class="sxs-lookup"><span data-stu-id="7dab4-204">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="7dab4-205">**Konfigūracijos tiekėjai** puslapyje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-205">On the **Configuration providers** page, select **New**.</span></span>
2. <span data-ttu-id="7dab4-206">Lauke **Pavadinimas** įveskite **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="7dab4-206">In the **Name** field, enter **Litware, Inc.**</span></span>
3. <span data-ttu-id="7dab4-207">**Internetinis adresas** lauke įveskite `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="7dab4-207">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
4. <span data-ttu-id="7dab4-208">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-208">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a><span data-ttu-id="7dab4-209">ER konfigūracijos tiekėjo aktyvavimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-209">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="7dab4-210">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-210">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7dab4-211">**Elektroninės ataskaitos** darbo srityje, pasirinkite **Litware, Inc.** konfigūravimo tiekėją.</span><span class="sxs-lookup"><span data-stu-id="7dab4-211">In the **Electronic reporting** workspace, select the **Litware, Inc.** configuration provider.</span></span>
3. <span data-ttu-id="7dab4-212">Pasirinkite **Nustatyti kaip aktyvų**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-212">Select **Set active**.</span></span>

<span data-ttu-id="7dab4-213">Daugiau informacijos apie ER konfigūracijos tiekėjus žr. [Konfigūracijos teikėjų kūrimas pažymint juos kaip aktyvius](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="7dab4-213">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a><span data-ttu-id="7dab4-214">Suprojektuoti domeno konkretų duomenų modelį</span><span class="sxs-lookup"><span data-stu-id="7dab4-214">Design a domain-specific data model</span></span>

<span data-ttu-id="7dab4-215">Privalote sukurti naują ER konfigūraciją, kurioje yra verslo domeno **Klausimynas** komponentą [duomenų modelis](general-electronic-reporting.md#data-model-and-model-mapping-components).</span><span class="sxs-lookup"><span data-stu-id="7dab4-215">You must create a new ER configuration that contains a [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** business domain.</span></span> <span data-ttu-id="7dab4-216">Šis duomenų modelis vėliau bus naudojamas kaip duomenų šaltinis, kai projektuosite ER formatą **Klausimyno** ataskaitos sukūrimui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-216">This data model will later be used as a data source when you design an ER format to generate the **Questionnaire** report.</span></span>

<span data-ttu-id="7dab4-217">Atlikę žingsnius [Importuoti naują duomenų modelio konfigūravimą](#ImportDataModel) skyriuje, galite importuoti reikiamą duomenų modelį iš pateikto XML failo.</span><span class="sxs-lookup"><span data-stu-id="7dab4-217">By completing the steps in the [Import a new data model configuration](#ImportDataModel) section, you can import the required data model from the provided XML file.</span></span> <span data-ttu-id="7dab4-218">Kitu atveju, galite atlikti žingsnius [Sukurti naują duomenų modelio konfigūravimą](#DesignDataModel) skyriuje tam, kad suprojektuotumėte šį duomenų modelį iš pradžių.</span><span class="sxs-lookup"><span data-stu-id="7dab4-218">Alternatively, you can complete the steps in the [Create a new data model configuration](#DesignDataModel) section to design this data model from scratch.</span></span>

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a><span data-ttu-id="7dab4-219">Importuokite naują duomenų modelio konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="7dab4-219">Import a new data model configuration</span></span>

1. <span data-ttu-id="7dab4-220">Atsisiųskite [Klausimynų model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) failą ir įrašykite jį į savo vietinį kompiuterį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-220">Download the [Questionnaires model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="7dab4-221">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-221">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="7dab4-222">**Elektroninės ataskaitos** darbo srityje pasirinkite **Ataskaitos konfigūravimai**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-222">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="7dab4-223">Veiksmų srityje pasirinkite **Pakeisti** \> **Įkelti iš XML failo**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-223">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="7dab4-224">Pasirinkite **Naršyti** ir tuomet suraskite ir pasirinkite **Klausimynų model.version.1.xml** failą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-224">Select **Browse**, and then find and select the **Questionnaires model.version.1.xml** file.</span></span>
6. <span data-ttu-id="7dab4-225">Pasirinkite **OK** tam, kad importuotumėte konfigūravimą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-225">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="7dab4-226">Tam, kad tęstumėte, praleiskite kitą procedūrą, [Sukurti naują duomenų modelio konfigūravimą](#DesignDataModel).</span><span class="sxs-lookup"><span data-stu-id="7dab4-226">To continue, skip the next procedure, [Create a new data model configuration](#DesignDataModel).</span></span>

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a><span data-ttu-id="7dab4-227">Sukurti naują duomenų modelio konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="7dab4-227">Create a new data model configuration</span></span>

1. <span data-ttu-id="7dab4-228">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-228">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7dab4-229">**Elektroninės ataskaitos** darbo srityje pasirinkite **Ataskaitos konfigūravimai**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-229">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="7dab4-230">Pasirinkite **Kurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-230">Select **Create configuration**.</span></span>
4. <span data-ttu-id="7dab4-231">Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **Klausimyno modelis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-231">In the drop-down dialog box, in the **Name** field, enter **Questionnaire model**.</span></span>
5. <span data-ttu-id="7dab4-232">Pasirinkite **Sukurti konfigūravimą** tam, kad sukurtumėte konfigūravimą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-232">Select **Create configuration** to create the configuration.</span></span>

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a><span data-ttu-id="7dab4-233">Pavadinkite duomenų modelį</span><span class="sxs-lookup"><span data-stu-id="7dab4-233">Name the data model</span></span>

1. <span data-ttu-id="7dab4-234">**Konfigūravimai** puslapyje, konfigūravimo medyje, pasirinkite **Klausimyno modelis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-234">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
2. <span data-ttu-id="7dab4-235">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-235">Select **Designer**.</span></span>
3. <span data-ttu-id="7dab4-236">**Duomenų modelio kūrėjo** puslapyje, **Bendri** „FastTab“, **Pavadinimas** laukelyje įveskite <a name="DataModeName"></a>**Klausimynai**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-236">On the **Data model designer** page, on the **General** FastTab, in the **Name** field, enter <a name="DataModeName"></a>**Questionnaires**.</span></span>

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a><span data-ttu-id="7dab4-237">Įtraukite naujus duomenų modelio laukelius</span><span class="sxs-lookup"><span data-stu-id="7dab4-237">Add new data model fields</span></span>

1. <span data-ttu-id="7dab4-238">**Duomenų modelio kūrėjo** puslapyje, pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-238">On the **Data model designer** page, select **New**.</span></span>
2. <span data-ttu-id="7dab4-239">Iškrentančiame teksto laukelyje duomenų modelio mazgo įtraukimui, atlikite šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="7dab4-239">In the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="7dab4-240">Pasirinkite **Modelio šaknis** kaip naujo modelio tipą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-240">Select **Model root** as the type of the new node.</span></span>
    2. <span data-ttu-id="7dab4-241">**Pavadinimas** laukelyje, įveskite <a name="RootDefinitionName"></a>**Šaknį**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-241">In the **Name** field, enter <a name="RootDefinitionName"></a>**Root**.</span></span>
    3. <span data-ttu-id="7dab4-242">Pasirinkite **Įtraukti** tam, kad įtrauktumėte naują mazgą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-242">Select **Add** to add the new node.</span></span>

    <span data-ttu-id="7dab4-243">Šis šaknies deskriptorius bus naudojamas duomenų pateikimui **Klausimyno** ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="7dab4-243">This root descriptor will be used to provide data for the **Questionnaire** report.</span></span> <span data-ttu-id="7dab4-244">Vienas duomenų modelis gali turėti keletą deskriptorių.</span><span class="sxs-lookup"><span data-stu-id="7dab4-244">A single data model can have multiple descriptors.</span></span> <span data-ttu-id="7dab4-245">Visi deskriptoriai gali būti nurodyti vienam ER formatui tam, kad būtų atpažinti ataskaitos sukūrimui būtini duomenys.</span><span class="sxs-lookup"><span data-stu-id="7dab4-245">Each descriptor can be specified for a single ER format, to identify data that is required to generate the report.</span></span>

3. <span data-ttu-id="7dab4-246">Pasirinkite **Naujas** dar kartą ir tuomet iškrentančiame teksto laukelyje duomenų modelio mazgo įtraukimui, atlikite šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="7dab4-246">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="7dab4-247">Pasirinkite **Įjungto mazgo vaikas** kaip naujo modelio tipą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-247">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="7dab4-248">**Pavadinimas** laukelyje, įveskite **Bendrovėspavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-248">In the **Name** field, enter **CompanyName**.</span></span>
    3. <span data-ttu-id="7dab4-249">Lauke **Elemento tipas** pasirinkite **Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-249">In the **Item type** field, select **String**.</span></span>
    4. <span data-ttu-id="7dab4-250">Pasirinkite **Įtraukti** tam, kad įtrauktumėte naują laukelį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-250">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="7dab4-251">Šis laukelis yra būtinas esančios bendrovės pavadinimo perdavimui į ER ataskaitą, kuris naudoja šį duomenų modelį kaip duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-251">This field is required to pass the name of the current company to an ER report that consumes this data model as a data source.</span></span>

4. <span data-ttu-id="7dab4-252">Pasirinkite **Naujas** dar kartą ir tuomet iškrentančiame teksto laukelyje duomenų modelio mazgo įtraukimui, atlikite šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="7dab4-252">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="7dab4-253">Pasirinkite **Įjungto mazgo vaikas** kaip naujo modelio tipą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-253">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="7dab4-254">**Pavadinimas** laukelyje, įveskite **Klausimynas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-254">In the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="7dab4-255">Lauke **Elemento tipas** pasirinkite **Įrašų sąrašas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-255">In the **Item type** field, select **Record list**.</span></span>
    4. <span data-ttu-id="7dab4-256">Pasirinkite **Įtraukti** tam, kad įtrauktumėte naują laukelį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-256">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="7dab4-257">Šis laukelis bus naudojamas klausimyno sąrašo perdavimui į ER ataskaitą, kuri naudoja šį duomenų modelį kaip duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-257">This field will be used to pass the list of questionnaires to an ER report that consumes this data model as a data source.</span></span>

5. <span data-ttu-id="7dab4-258">Pasirinkite **Klausimynas** mazgą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-258">Select the **Questionnaire** node.</span></span>
6. <span data-ttu-id="7dab4-259">Tęskite redaguojamo duomenų modelio būtinų laukelių įtraukimą tokiu pačiu būdu, kol užbaigsite toliau pateiktų duomenų modelio struktūrą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-259">Continue to add the required fields of the editable data model in the same manner until you complete the following data model structure.</span></span>

    | <span data-ttu-id="7dab4-260">Lauko kelias</span><span class="sxs-lookup"><span data-stu-id="7dab4-260">Field path</span></span>                                                    | <span data-ttu-id="7dab4-261">Duomenų tipas</span><span class="sxs-lookup"><span data-stu-id="7dab4-261">Data type</span></span>   | <span data-ttu-id="7dab4-262">Laukelio projektavimas/grįžtamoji vertė</span><span class="sxs-lookup"><span data-stu-id="7dab4-262">Field designation/returned value</span></span> |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | <span data-ttu-id="7dab4-263">Šaknis</span><span class="sxs-lookup"><span data-stu-id="7dab4-263">Root</span></span>                                                          |             | <span data-ttu-id="7dab4-264">Ataskaitos taškas klausimyno duomenų užklausai.</span><span class="sxs-lookup"><span data-stu-id="7dab4-264">The reference point to request questionnaire data.</span></span> |
    | <span data-ttu-id="7dab4-265">Šaknis\\Bendrovėspavadinimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-265">Root\\CompanyName</span></span>                                             | <span data-ttu-id="7dab4-266">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-266">String</span></span>      | <span data-ttu-id="7dab4-267">Esančios bendrovės pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-267">The name of the current company.</span></span> |
    | <span data-ttu-id="7dab4-268">Šaknis\\Vykdymoturinys</span><span class="sxs-lookup"><span data-stu-id="7dab4-268">Root\\ExecutionContext</span></span>                                        | <span data-ttu-id="7dab4-269">Įrašyti</span><span class="sxs-lookup"><span data-stu-id="7dab4-269">Record</span></span>      | <span data-ttu-id="7dab4-270">Vykdymo formato išsami informacija.</span><span class="sxs-lookup"><span data-stu-id="7dab4-270">Format execution details.</span></span> |
    | <span data-ttu-id="7dab4-271">Šaknis\\Vykdymoturinys\\Formatopavadinimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-271">Root\\ExecutionContext\\FormatName</span></span>                            | <span data-ttu-id="7dab4-272">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-272">String</span></span>      | <span data-ttu-id="7dab4-273">Vykdomo ER formato pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-273">The name of the ER format that is being run.</span></span> |
    | <span data-ttu-id="7dab4-274">Šaknis\\Klausimynas</span><span class="sxs-lookup"><span data-stu-id="7dab4-274">Root\\Questionnaire</span></span>                                           | <span data-ttu-id="7dab4-275">Įrašų sąrašas</span><span class="sxs-lookup"><span data-stu-id="7dab4-275">Record list</span></span> | <span data-ttu-id="7dab4-276">Klausimynų sąrašas</span><span class="sxs-lookup"><span data-stu-id="7dab4-276">The list of questionnaires</span></span> |
    | <span data-ttu-id="7dab4-277">Šaknis\\Klausimynas\\Įjungtas</span><span class="sxs-lookup"><span data-stu-id="7dab4-277">Root\\Questionnaire\\Active</span></span>                                   | <span data-ttu-id="7dab4-278">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-278">String</span></span>      | <span data-ttu-id="7dab4-279">Esamo klausimyno statusas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-279">The status of the current questionnaire.</span></span> |
    | <span data-ttu-id="7dab4-280">Šaknis\\Klausimynas\\Kodas</span><span class="sxs-lookup"><span data-stu-id="7dab4-280">Root\\Questionnaire\\Code</span></span>                                     | <span data-ttu-id="7dab4-281">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-281">String</span></span>      | <span data-ttu-id="7dab4-282">Esamo klausimyno kodas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-282">The code of the current questionnaire.</span></span> |
    | <span data-ttu-id="7dab4-283">Šaknis\\Klausimynas\\Aprašas</span><span class="sxs-lookup"><span data-stu-id="7dab4-283">Root\\Questionnaire\\Description</span></span>                              | <span data-ttu-id="7dab4-284">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-284">String</span></span>      | <span data-ttu-id="7dab4-285">Esamo klausimyno aprašas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-285">The description of the current questionnaire.</span></span> |
    | <span data-ttu-id="7dab4-286">Šaknis\\Klausimynas\\Klausimynotipas</span><span class="sxs-lookup"><span data-stu-id="7dab4-286">Root\\Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="7dab4-287">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-287">String</span></span>      | <span data-ttu-id="7dab4-288">Esamo klausimyno tipas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-288">The type of the current questionnaire.</span></span> |
    | <span data-ttu-id="7dab4-289">Šaknis\\Klausimynas\\Klausimynotvarka</span><span class="sxs-lookup"><span data-stu-id="7dab4-289">Root\\Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="7dab4-290">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-290">String</span></span>      | <span data-ttu-id="7dab4-291">Esamo klausimyno eilės tvarka.</span><span class="sxs-lookup"><span data-stu-id="7dab4-291">The numerical order of the current questionnaire.</span></span> |
    | <span data-ttu-id="7dab4-292">Šaknis\\Klausimynas\\Rezultatogrupė</span><span class="sxs-lookup"><span data-stu-id="7dab4-292">Root\\Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="7dab4-293">Įrašyti</span><span class="sxs-lookup"><span data-stu-id="7dab4-293">Record</span></span>      | <span data-ttu-id="7dab4-294">Esamo klausimyno eilės parametrų rezultatas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-294">The result parameters of the current questionnaire.</span></span> |
    | <span data-ttu-id="7dab4-295">Šaknis\\Klausimynas\\Rezultatųgrupė\\Kodas</span><span class="sxs-lookup"><span data-stu-id="7dab4-295">Root\\Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="7dab4-296">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-296">String</span></span>      | <span data-ttu-id="7dab4-297">Esamos rezultatų grupės identifikavimo kodas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-297">The identification code of the current result group.</span></span> |
    | <span data-ttu-id="7dab4-298">Šaknis\\Klausimynas\\Rezultatųgrupė\\Aprašas</span><span class="sxs-lookup"><span data-stu-id="7dab4-298">Root\\Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="7dab4-299">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-299">String</span></span>      | <span data-ttu-id="7dab4-300">Esamo klausimyno rezultatų grupė.</span><span class="sxs-lookup"><span data-stu-id="7dab4-300">The description of the current result group.</span></span> |
    | <span data-ttu-id="7dab4-301">Šaknis\\Klausimynas\\Rezultatųgrupė\\Maks.taškųskaičius</span><span class="sxs-lookup"><span data-stu-id="7dab4-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="7dab4-302">Tikrasis</span><span class="sxs-lookup"><span data-stu-id="7dab4-302">Real</span></span>        | <span data-ttu-id="7dab4-303">Maksimalus taškų skaičius, kurį galima gauti.</span><span class="sxs-lookup"><span data-stu-id="7dab4-303">The maximum number of points that could be earned.</span></span> |
    | <span data-ttu-id="7dab4-304">Šaknis\\Klausimynas\\Klausimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-304">Root\\Questionnaire\\Question</span></span>                                 | <span data-ttu-id="7dab4-305">Įrašų sąrašas</span><span class="sxs-lookup"><span data-stu-id="7dab4-305">Record list</span></span> | <span data-ttu-id="7dab4-306">Esamo klausimyno klausimų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-306">The list of questions for the current questionnaire.</span></span> |
    | <span data-ttu-id="7dab4-307">Šaknis\\Klausimynas\\Klausimas\\Surinkimoeilėsnumeris</span><span class="sxs-lookup"><span data-stu-id="7dab4-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="7dab4-308">Sveikasis skaičius</span><span class="sxs-lookup"><span data-stu-id="7dab4-308">Integer</span></span>     | <span data-ttu-id="7dab4-309">Esamo atsakymo surinkimo eilės numeris.</span><span class="sxs-lookup"><span data-stu-id="7dab4-309">The sequence number of the current answer collection.</span></span> |
    | <span data-ttu-id="7dab4-310">Šaknis\\Klausimynas\\Klausimas\\Id</span><span class="sxs-lookup"><span data-stu-id="7dab4-310">Root\\Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="7dab4-311">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-311">String</span></span>      | <span data-ttu-id="7dab4-312">Esamos rezultatų grupės identifikavimo klausimas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-312">The identification code of the current question.</span></span> |
    | <span data-ttu-id="7dab4-313">Šaknis\\Klausimynas\\Klausimas\\Turibūtiužbaigtas</span><span class="sxs-lookup"><span data-stu-id="7dab4-313">Root\\Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="7dab4-314">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-314">String</span></span>      | <span data-ttu-id="7dab4-315">Vėliava rodanti, ar esamas klausimas turi būti atsakytas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-315">A flag that indicates whether the current question must be answered.</span></span> |
    | <span data-ttu-id="7dab4-316">Šaknis\\Klausimynas\\Klausimas\\Pirmasisklausimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="7dab4-317">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-317">String</span></span>      | <span data-ttu-id="7dab4-318">Vėliava rodanti, ar esamas klausimas yra pirmasis.</span><span class="sxs-lookup"><span data-stu-id="7dab4-318">A flag that indicates whether the current question is primary.</span></span> |
    | <span data-ttu-id="7dab4-319">Šaknis\\Klausimynas\\Klausimas\\Eilėsnumeris</span><span class="sxs-lookup"><span data-stu-id="7dab4-319">Root\\Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="7dab4-320">Sveikasis skaičius</span><span class="sxs-lookup"><span data-stu-id="7dab4-320">Integer</span></span>     | <span data-ttu-id="7dab4-321">Esamo klausimo eilės numeris.</span><span class="sxs-lookup"><span data-stu-id="7dab4-321">The sequence number of the current question.</span></span> |
    | <span data-ttu-id="7dab4-322">Šaknis\\Klausimynas\\Klausimas\\Tekstas</span><span class="sxs-lookup"><span data-stu-id="7dab4-322">Root\\Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="7dab4-323">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-323">String</span></span>      | <span data-ttu-id="7dab4-324">Esamo klausimo tekstas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-324">The text of the current question.</span></span> |
    | <span data-ttu-id="7dab4-325">Šaknis\\Klausimynas\\Klausimas\\Atsakymas</span><span class="sxs-lookup"><span data-stu-id="7dab4-325">Root\\Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="7dab4-326">Įrašų sąrašas</span><span class="sxs-lookup"><span data-stu-id="7dab4-326">Record list</span></span> | <span data-ttu-id="7dab4-327">Esamo klausimo atsakymų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-327">The list of answers for the current question.</span></span> |
    | <span data-ttu-id="7dab4-328">Šaknis\\Klausimynas\\Klausimas\\Atsakymas\\Teisingasatsakymas</span><span class="sxs-lookup"><span data-stu-id="7dab4-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="7dab4-329">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-329">String</span></span>      | <span data-ttu-id="7dab4-330">Vėliava rodanti, ar esamas atsakymas yra teisingas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-330">A flag that indicates whether the current answer is correct.</span></span> |
    | <span data-ttu-id="7dab4-331">Šaknis\\Klausimynas\\Klausimas\\Atsakymas\\Taškai</span><span class="sxs-lookup"><span data-stu-id="7dab4-331">Root\\Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="7dab4-332">Tikrasis</span><span class="sxs-lookup"><span data-stu-id="7dab4-332">Real</span></span>        | <span data-ttu-id="7dab4-333">Taškai, kurie yra uždirbami, kai esamas atsakymas yra pasirenkamas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-333">The points that are earned when the current answer is selected.</span></span> |
    | <span data-ttu-id="7dab4-334">Šaknis\\Klausimynas\\Klausimas\\Atsakymas\\Eilėsnumeris</span><span class="sxs-lookup"><span data-stu-id="7dab4-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="7dab4-335">Sveikasis skaičius</span><span class="sxs-lookup"><span data-stu-id="7dab4-335">Integer</span></span>     | <span data-ttu-id="7dab4-336">Esamo atsakymo eilės numeris.</span><span class="sxs-lookup"><span data-stu-id="7dab4-336">The sequence number of the current answer.</span></span> |
    | <span data-ttu-id="7dab4-337">Šaknis\\Klausimynas\\Klausimas\\Atsakymas\\Tekstas</span><span class="sxs-lookup"><span data-stu-id="7dab4-337">Root\\Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="7dab4-338">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-338">String</span></span>      | <span data-ttu-id="7dab4-339">Esamo atsakymo tekstas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-339">The text of the current answer.</span></span> |

    <span data-ttu-id="7dab4-340">Tolesnis paveikslėlis rodo užbaigtą redaguojamus duomenų modelį **Duomenų modelio kūrimo** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="7dab4-340">The following illustration shows the completed editable data model on the **Data model designer** page.</span></span>

    ![Konfigūruotas duomenų modelis ER duomenų modelio kūrimo įrankyje](./media/er-quick-start1-model2.png)

7. <span data-ttu-id="7dab4-342">Įrašykite pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="7dab4-342">Save your changes.</span></span>
8. <span data-ttu-id="7dab4-343">Uždarykite **Duomenų modelio kūrimo** puslapį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-343">Close the **Data model designer** page.</span></span>

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a><span data-ttu-id="7dab4-344">Užbaikite duomenų modelio projektavimą</span><span class="sxs-lookup"><span data-stu-id="7dab4-344">Complete the design of the data model</span></span>

1. <span data-ttu-id="7dab4-345">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-345">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7dab4-346">**Konfigūravimai** puslapyje, konfigūravimo medyje, pasirinkite **Klausimyno modelis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-346">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="7dab4-347">**Versijos** „FastTab“, pasirinkite konfigūravimo versiją, kuri turi statusą **Juodraštis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-347">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="7dab4-348">Pasirinkite **Keisti statusą** \> **Užbaigtas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-348">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="7dab4-349">Šios konfigūracijos versijos 1 statusas yra keičiamas iš **Juodraštis** į **Užbaigtas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-349">The status of version 1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="7dab4-350">Versija 1 nebegali būti keičiama.</span><span class="sxs-lookup"><span data-stu-id="7dab4-350">Version 1 can no longer be changed.</span></span> <span data-ttu-id="7dab4-351">Šioje versijoje yra konfigūruotų duomenų modelis ir gali būti naudojamas pagal kitas ER konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-351">This version contains the configured data model and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="7dab4-352">Šios konfigūracijos versija 2 yra sukurta ir turi **Juodraštis** statusą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-352">Version 2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="7dab4-353">Galite redaguoti šią versiją tam, kad keistumėte **Klausimyno** duomenų modelį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-353">You can edit this version to adjust the **Questionnaire** data model.</span></span>

![Redaguojamos ER konfigūracijos versijos konfigūravimo puslapyje](./media/er-quick-start1-model-configuration.png)

<span data-ttu-id="7dab4-355">Dėl platesnės informacijos apie ER konfigūracijų versijas, žr. [Elektroninės ataskaitos (ER) peržiūra](general-electronic-reporting.md#component-versioning).</span><span class="sxs-lookup"><span data-stu-id="7dab4-355">For more information about versioning for ER configurations, see [Electronic reporting (ER) overview](general-electronic-reporting.md#component-versioning).</span></span>

> [!NOTE]
> <span data-ttu-id="7dab4-356">Konfigūruotas duomenų modelis yra **Klausimyno** verslo domeno bendra reprezentacija ir neturi jokio ryšio su artefaktais nurodytais „Microsoft Dynamics 365 Finance“.</span><span class="sxs-lookup"><span data-stu-id="7dab4-356">The configured data model is your abstract representation of the **Questionnaire** business domain and contains no relations to artefacts that are specific to Microsoft Dynamics 365 Finance.</span></span>

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a><span data-ttu-id="7dab4-357">Suprojektuokite konfigūruoto duomenų modelio žemėlapį</span><span class="sxs-lookup"><span data-stu-id="7dab4-357">Design a model mapping for the configured data model</span></span>

<span data-ttu-id="7dab4-358">Kaip vartotojas elektroninės ataskaitos kūrėjo vaidmenyje, turite sukurti naują ER konfigūravimą, kuris turi [modelio žemėlapį](general-electronic-reporting.md#data-model-and-model-mapping-components) komponentą **Klausimyno** duomenų modeliui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-358">As a user in the Electronic Reporting Developer role, you must create a new ER configuration that contains a [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** data model.</span></span> <span data-ttu-id="7dab4-359">Kadangi šis komponentas įgyvendina konfigūruotų duomenų modelį finansams, jis yra skirtas būtent finansams.</span><span class="sxs-lookup"><span data-stu-id="7dab4-359">Because this component implements the configured data model for Finance, it's Finance-specific.</span></span> <span data-ttu-id="7dab4-360">Privalote konfigūruoti modelio žemėlapio komponentą tam, kad nurodytumėte programos objektus, kurie turi būti naudojami konfigūruoto duomenų modelio užpildymui su programos duomenimis vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="7dab4-360">You must configure the model mapping component to specify the application objects that must be used to fill in the configured data model with application data at runtime.</span></span> <span data-ttu-id="7dab4-361">Šios užduoties atlikimui, turite žinoti duomenų struktūros implementavimo išsamius duomenis **Klausimyno** verslo domene finansuose.</span><span class="sxs-lookup"><span data-stu-id="7dab4-361">To complete this task, you must be aware of the implementation details of the data structure of the **Questionnaire** business domain in Finance.</span></span>

<span data-ttu-id="7dab4-362">Atlikę žingsnius [Naujo modelio žemėlapio konfigūravimo importavimo](#ImportModelMapping) toliau pateiktame skyriuje, galite importuoti būtiną modelį žemėlapio konfigūravimui iš pateikto XML failo.</span><span class="sxs-lookup"><span data-stu-id="7dab4-362">By completing the steps in the [Import a new model mapping configuration](#ImportModelMapping) section that follows, you can import the required model mapping configuration from the provided XML file.</span></span> <span data-ttu-id="7dab4-363">Kitu atveju, galite atlikti žingsnius [Naujo modelio žemėlapio konfigūravimo sukūrimas](#CreateModelMapping) skyriuje tam, kad suprojektuotumėte modelio žemėlapį iš pradžių.</span><span class="sxs-lookup"><span data-stu-id="7dab4-363">Alternatively, you can complete the steps in the [Create a new model mapping configuration](#CreateModelMapping) section to design this model mapping from scratch.</span></span>

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a><span data-ttu-id="7dab4-364">Importuokite naują modelio žemėlapio konfigūravimą</span><span class="sxs-lookup"><span data-stu-id="7dab4-364">Import a new model mapping configuration</span></span>

1. <span data-ttu-id="7dab4-365">Atsisiųskite [Klausimynų mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) failą ir įrašykite jį į savo vietinį kompiuterį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-365">Download the [Questionnaires mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="7dab4-366">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-366">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="7dab4-367">**Elektroninės ataskaitos** darbo srityje pasirinkite **Ataskaitos konfigūravimai**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-367">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="7dab4-368">Veiksmų srityje pasirinkite **Pakeisti** \> **Įkelti iš XML failo**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-368">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="7dab4-369">Pasirinkite **Naršyti** ir tuomet suraskite ir pasirinkite **Klausimynų mapping.version.1.1.xml** failą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-369">Select **Browse**, and then find and select the **Questionnaires mapping.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="7dab4-370">Pasirinkite **OK** tam, kad importuotumėte konfigūravimą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-370">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="7dab4-371">Tam, kad tęstumėte, praleiskite kitą procedūrą [Sukurti naują modelio žemėlapio konfigūravimą](#CreateModelMapping).</span><span class="sxs-lookup"><span data-stu-id="7dab4-371">To continue, skip the next procedure, [Create a new model mapping configuration](#CreateModelMapping).</span></span>

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a><span data-ttu-id="7dab4-372">Sukurkite naują modelio žemėlapio konfigūravimą</span><span class="sxs-lookup"><span data-stu-id="7dab4-372">Create a new model mapping configuration</span></span>

1. <span data-ttu-id="7dab4-373">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-373">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7dab4-374">**Konfigūravimai** puslapyje, konfigūravimo medyje, pasirinkite **Klausimyno modelis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-374">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="7dab4-375">Pasirinkite **Kurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-375">Select **Create configuration**.</span></span>
4. <span data-ttu-id="7dab4-376">Išplečiamajame dialogo lange atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7dab4-376">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="7dab4-377">Laukelyje **Naujas** pasirinkite **Modelio žemėlapio kūrimas pagal duomenų modelio klausimynus**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-377">In the **New** field, select **Model Mapping based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="7dab4-378">**Pavadinimas** laukelyje, įveskite **Klausimyno žemėlapio kūrimas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-378">In the **Name** field, enter **Questionnaire mapping**.</span></span>
    3. <span data-ttu-id="7dab4-379">**Duomenų modelio sąvoka** laukelyje, pasirinkite **Šaknies** sąvoka.</span><span class="sxs-lookup"><span data-stu-id="7dab4-379">In the **Data model definition** field, select the **Root** definition.</span></span>
    4. <span data-ttu-id="7dab4-380">Pasirinkite **Sukurti konfigūravimą** tam, kad sukurtumėte konfigūravimą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-380">Select **Create configuration** to create the configuration.</span></span>

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a><span data-ttu-id="7dab4-381">Projektuokite naują modelio žemėlapio komponentą</span><span class="sxs-lookup"><span data-stu-id="7dab4-381">Design a new model mapping component</span></span>

1. <span data-ttu-id="7dab4-382">**Konfigūravimai** puslapyje, konfigūravimo medyje, pasirinkite **Klausimyno žemėlapio kūrimas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-382">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
2. <span data-ttu-id="7dab4-383">Norėdami atidaryti susiejimų sąrašą, pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-383">Select **Designer** to open the list of mappings.</span></span>
3. <span data-ttu-id="7dab4-384">Pasirinkite **Klausimyno žemėlapio kūrimas** žemėlapio kūrimą, kuris buvo automatiškai įtrauktas **Šaknies** sąvokai</span><span class="sxs-lookup"><span data-stu-id="7dab4-384">Select the **Questionnaires mapping** mapping that was automatically added for the **Root** definition</span></span>
4. <span data-ttu-id="7dab4-385">Pasirinkite **Kūrimo įrankį** tam, kad pradėtumėte konfigūruoti pasirinktą žemėlapį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-385">Select **Designer** to start to configure the selected mapping.</span></span>

<span data-ttu-id="7dab4-386">Naujas žemėlapio kūrimas yra automatiškai įtrauktas **Šaknies** sąvokai.</span><span class="sxs-lookup"><span data-stu-id="7dab4-386">A new mapping is automatically added for the **Root** definition.</span></span> <span data-ttu-id="7dab4-387">Šis žemėlapio kūrimas turi **Į modelį** paskirties vietą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-387">This mapping has the **To model** direction.</span></span> <span data-ttu-id="7dab4-388">Dėl to, šis žemėlapio kūrimas gali būti naudojamas duomenų modelio užpildymui būtinais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="7dab4-388">Therefore, this mapping can be used to fill in a data model with required data.</span></span>

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a><span data-ttu-id="7dab4-389">Įtraukite duomenų šaltinius į prieigos programos lenteles</span><span class="sxs-lookup"><span data-stu-id="7dab4-389">Add data sources to access application tables</span></span>

<span data-ttu-id="7dab4-390">Privalote konfigūruoti duomenų šaltinius tam, kad prieitumėte prie programos lentelių, turinčių klausimyno išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="7dab4-390">You must configure data sources to access the application tables that contain questionnaire details.</span></span>

1. <span data-ttu-id="7dab4-391">**Modelio žemėlapio kūrimo įrankis** puslapyje, **Duomenų šaltinio tipai** juostoje, pasirinkite **Dynamics 365 for Operations\\Lentelės įrašai**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-391">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="7dab4-392">Įtraukite naują duomenų šaltinį, kuris bus naudojamas prieigai prie KMCollection lentelės, kurioje visi įrašai rodo vieną klausimyną:</span><span class="sxs-lookup"><span data-stu-id="7dab4-392">Add a new data source that will be used to access the KMCollection table, where every record represents a single questionnaire:</span></span>

    1. <span data-ttu-id="7dab4-393">**Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-393">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="7dab4-394">Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **Klausimynas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-394">In dialog box, in the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="7dab4-395">**Lentelė** laukelyje, įveskite **KMCollection**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-395">In the **Table** field, enter **KMCollection**.</span></span>
    4. <span data-ttu-id="7dab4-396">Nustatykite **Prašyti užklausos** parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-396">Set the **Ask for query** option to **Yes**.</span></span> <span data-ttu-id="7dab4-397">Galėsite tuomet nurodyti [filtravimo](../../fin-ops/get-started/advanced-filtering-query-options.md) parinktis šiai lentelei sistemos užklausos teksto laukelyje vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="7dab4-397">You will then be able to specify [filtering](../../fin-ops/get-started/advanced-filtering-query-options.md) options for this table in the system query dialog box at runtime.</span></span>
    5. <span data-ttu-id="7dab4-398">Pasirinkite **Gerai** tam, kad įtrauktumėte naują duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-398">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="7dab4-399">**Duomenų šaltinio tipai** juostoje pasirinkite **Dynamics 365 for Operations\\Lentelės įrašai**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-399">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
4. <span data-ttu-id="7dab4-400">Įtraukite naują duomenų šaltinį, kuris bus naudojamas prieigai prie KMQuestion lentelės, kurioje visi įrašai rodo vieną klausimą klausimyne:</span><span class="sxs-lookup"><span data-stu-id="7dab4-400">Add a new data source that will be used to access the KMQuestion table, where every record represents a single question in a questionnaire:</span></span>

    1. <span data-ttu-id="7dab4-401">**Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-401">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="7dab4-402">Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **Klausimas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-402">In the dialog box, in the **Name** field, enter **Question**.</span></span>
    3. <span data-ttu-id="7dab4-403">**Lentelė** laukelyje, įveskite **KMQuestion**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-403">In the **Table** field, enter **KMQuestion**.</span></span>
    4. <span data-ttu-id="7dab4-404">Pasirinkite **Gerai** tam, kad įtrauktumėte naują duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-404">Select **OK** to add the new data source.</span></span>

5. <span data-ttu-id="7dab4-405">**Duomenų šaltinio tipai** juostoje pasirinkite **Dynamics 365 for Operations\\Lentelės įrašai**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-405">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
6. <span data-ttu-id="7dab4-406">Įtraukite naują duomenų šaltinio bandymą, kuris bus naudojamas prieigai prie KMAnswer lentelės, kurioje visi įrašai rodo vieną atsakymą į klausimą klausimyne:</span><span class="sxs-lookup"><span data-stu-id="7dab4-406">Add a new data source try that will be used to access the KMAnswer table, where every record represents a single answer to a question in a questionnaire:</span></span>

    1. <span data-ttu-id="7dab4-407">**Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-407">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="7dab4-408">**Pavadinimas** laukelyje, įveskite **Atsakymas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-408">In the **Name** field, enter **Answer**.</span></span>
    3. <span data-ttu-id="7dab4-409">**Lentelė** laukelyje, įveskite **KMAnswer**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-409">In the **Table** field, enter **KMAnswer**.</span></span>
    4. <span data-ttu-id="7dab4-410">Pasirinkite **Gerai** tam, kad įtrauktumėte naują duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-410">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="7dab4-411">**Duomenų šaltinio tipai** juostoje, pasirinkite **Funkcijos\\Apskaičiuotas laukelis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-411">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="7dab4-412">Įtraukite naują apskaičiuotą laukelį, kuris bus naudojamas prieigai prie KMQuestionResultGroup lentelės įrašo iš kiekvienos susijusios KMCollection lentelės įrašo:</span><span class="sxs-lookup"><span data-stu-id="7dab4-412">Add a new calculated field that will be used to access a record of the KMQuestionResultGroup table from every record of the parent KMCollection table:</span></span>

    1. <span data-ttu-id="7dab4-413">**Duomenų šaltiniai** juostoje pasirinkite **Klausimynas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-413">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="7dab4-414">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-414">Select **Add**.</span></span>
    3. <span data-ttu-id="7dab4-415">Teksto laukelyje **Pavadinimas** laukelyje, įveskite **\$Rezultatogrupė**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-415">In the dialog box, in the **Name** field, enter **\$ResultGroup**.</span></span>
    4. <span data-ttu-id="7dab4-416">Pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-416">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="7dab4-417">[ER formulės redaktoriuje](general-electronic-reporting-formula-designer.md), **Formulės** laukelyje įveskite **FIRSTORNULL(\@.'\<Sąsajos'.KMQuestionResultGroup)** tam, kad naudotumėte [kelią](er-formula-language.md#paths) vieno su daugeliu ryšyje tarp KMCollection ir KMQuestionResultGroup lentelių.</span><span class="sxs-lookup"><span data-stu-id="7dab4-417">In the [ER formula editor](general-electronic-reporting-formula-designer.md), in the **Formula** field, enter **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** to use the [path](er-formula-language.md#paths) of the one-to-many relation between the KMCollection and KMQuestionResultGroup tables.</span></span>
    6. <span data-ttu-id="7dab4-418">Pasirinkite **Įrašyti** ir uždarykite formulės redaktorių.</span><span class="sxs-lookup"><span data-stu-id="7dab4-418">Select **Save**, and close the formula editor.</span></span>
    7. <span data-ttu-id="7dab4-419">Pasirinkite **Gerai** tam, kad įtrauktumėte naują apskaičiuotą laukelį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-419">Select **OK** to add the new calculated field.</span></span>

9. <span data-ttu-id="7dab4-420">**Duomenų šaltinio tipai** juostoje, pasirinkite **Funkcijos\\Apskaičiuotas laukelis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-420">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
10. <span data-ttu-id="7dab4-421">Įtraukite naują apskaičiuotą laukelį, kuris bus naudojamas prieigai prie KMQuestionResultGroup klausimo įrašų iš kiekvienos susijusios KMCollectionQuestion lentelės įrašo:</span><span class="sxs-lookup"><span data-stu-id="7dab4-421">Add a new calculated field that will be used to access question records of the KMQuestion table from every record of the parent KMCollectionQuestion table:</span></span>

    1. <span data-ttu-id="7dab4-422">**Duomenų šaltiniai** juostoje pasirinkite **Klausimynas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-422">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="7dab4-423">Išplėskite **\<Ryšiai** mazgą, kuris turi vieną su keliais ryšius KMCollection lentelę.</span><span class="sxs-lookup"><span data-stu-id="7dab4-423">Expand the **\<Relations** node that contains one-to-many relations of the KMCollection table.</span></span>
    3. <span data-ttu-id="7dab4-424">Pasirinkite susijusią **KMCollectionQuestion** lentelę ir tuomet pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-424">Select the related **KMCollectionQuestion** table, and then select **Add**.</span></span>
    4. <span data-ttu-id="7dab4-425">Teksto laukelyje, **Pavadinimas** laukelyje įveskite **\$Klausimas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-425">In the dialog box, in the **Name** field, enter **\$Question**.</span></span>
    5. <span data-ttu-id="7dab4-426">Pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-426">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="7dab4-427">Formulės redaktoriuje **Formulės** laukelyje įveskite **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** tam, kad grąžintumėte atitinkamus klausimo įrašus iš KMQuestion lentelės.</span><span class="sxs-lookup"><span data-stu-id="7dab4-427">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** to return the appropriate question records from the KMQuestion table.</span></span>
    7. <span data-ttu-id="7dab4-428">Pasirinkite **Įrašyti** ir uždarykite formulės redaktorių.</span><span class="sxs-lookup"><span data-stu-id="7dab4-428">Select **Save**, and close the formula editor.</span></span>
    8. <span data-ttu-id="7dab4-429">Pasirinkite **Gerai** tam, kad įtrauktumėte naują apskaičiuotą laukelį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-429">Select **OK** to add the new calculated field.</span></span>

11. <span data-ttu-id="7dab4-430">**Duomenų šaltinio tipai** juostoje, pasirinkite **Funkcijos\\Apskaičiuotas laukelis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-430">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
12. <span data-ttu-id="7dab4-431">Įtraukite naują apskaičiuotą laukelį, kuris bus naudojamas prieigai prie KMAnswer atsakymo įrašų iš kiekvienos susijusios KMQuestion lentelės įrašo:</span><span class="sxs-lookup"><span data-stu-id="7dab4-431">Add a new calculated field that will be used to access answer records of the KMAnswer table from every record of the parent KMQuestion table:</span></span>

    1. <span data-ttu-id="7dab4-432">**Duomenų šaltinio** juostoje pasirinkite **Klausimynas.\<Sąsajos.KMCollectionQuestion.\$Klausimas** ir tuomet pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-432">In the **Data sources** pane, select **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**, and then select **Add**.</span></span>
    2. <span data-ttu-id="7dab4-433">Teksto laukelyje, **Pavadinimas** laukelyje įveskite **\$Atsakymas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-433">In the dialog box, in the **Name** field, enter **\$Answer**.</span></span>
    3. <span data-ttu-id="7dab4-434">Pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-434">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="7dab4-435">Formulės redaktoriaus laukelyje **Formulė** įveskite **FILTRAS (Atsakymas, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** tam, kad grįžtumėte prie atitinkamo atsakymo įrašų iš KMAnswer lentelės.</span><span class="sxs-lookup"><span data-stu-id="7dab4-435">In the formula editor, in the **Formula** field, enter **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** to return the appropriate answer records from the KMAnswer table.</span></span>
    5. <span data-ttu-id="7dab4-436">Pasirinkite **Įrašyti** ir uždarykite formulės redaktorių.</span><span class="sxs-lookup"><span data-stu-id="7dab4-436">Select **Save**, and close the formula editor.</span></span>
    6. <span data-ttu-id="7dab4-437">Pasirinkite **Gerai** tam, kad įtrauktumėte naują apskaičiuotą laukelį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-437">Select **OK** to add the new calculated field.</span></span>

13. <span data-ttu-id="7dab4-438">**Duomenų šaltinio tipai** juostoje pasirinkite **Dynamics 365 for Operations\\Lentelė**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-438">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table**.</span></span>
14. <span data-ttu-id="7dab4-439">Įtraukite naują duomenų šaltinį, kuris bus naudojamas prieigos metodams CompanyInfo lentelėje.</span><span class="sxs-lookup"><span data-stu-id="7dab4-439">Add a new data source that will be used to access methods of the CompanyInfo table.</span></span> <span data-ttu-id="7dab4-440">Atkreipkite dėmesį, kad **find()** metodas šioje lentelėje grįžta į įrašą rodantį esamos finansų instancijos bendrovę, kuriuo vadinamas šis žemėlapis.</span><span class="sxs-lookup"><span data-stu-id="7dab4-440">Note that the **find()** method of this table returns a record that represents a company of the current Finance instance that this mapping is called in the context of.</span></span>

    1. <span data-ttu-id="7dab4-441">**Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-441">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="7dab4-442">Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-442">In the dialog box, in the **Name** field, enter **CompanyInfo**.</span></span>
    3. <span data-ttu-id="7dab4-443">**Lentelė** laukelyje, įveskite **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-443">In the **Table** field, enter **CompanyInfo**.</span></span>
    4. <span data-ttu-id="7dab4-444">Pasirinkite **Gerai** tam, kad įtrauktumėte naują duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-444">Select **OK** to add the new data source.</span></span>

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a><span data-ttu-id="7dab4-445">Įtraukite duomenų šaltinius tam, kad prieitumėte prie programos numeracijų</span><span class="sxs-lookup"><span data-stu-id="7dab4-445">Add data sources to access application enumerations</span></span>

<span data-ttu-id="7dab4-446">Privalote konfigūruoti duomenų šaltinius prieigai prie programų numeracijų ir palyginti jų vertes su laukelių vertėmis **Numeracijos** tipo programos lentelėse.</span><span class="sxs-lookup"><span data-stu-id="7dab4-446">You must configure data sources to access application enumerations and compare their values with values of fields of the **Enumeration** type in the application tables.</span></span> <span data-ttu-id="7dab4-447">Privalote naudoti palyginimo rezultatą tam, kad užpildytumėte atitinkamus duomenų modelio laukelius.</span><span class="sxs-lookup"><span data-stu-id="7dab4-447">You must use the result of the comparison to fill in appropriate fields of the data model.</span></span>

1. <span data-ttu-id="7dab4-448">**Modelio žemėlapio kūrimo įrankis** puslapyje, **Duomenų šaltinio tipai** juostoje, pasirinkite **Dynamics 365 for Operations\\Numeracija**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-448">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
2. <span data-ttu-id="7dab4-449">Įtraukite naują duomenų šaltinį, kuris bus naudojamas prieigos **EnumAppNoYes** numeracijai:</span><span class="sxs-lookup"><span data-stu-id="7dab4-449">Add a new data source that will be used to access values of the **EnumAppNoYes** enumeration:</span></span>

    1. <span data-ttu-id="7dab4-450">**Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-450">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="7dab4-451">Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **EnumAppNoYes**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-451">In the dialog box, in the **Name** field, enter **EnumAppNoYes**.</span></span>
    3. <span data-ttu-id="7dab4-452">**Numeracija** laukelyje, įveskite **NeTaip**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-452">In the **Enumeration** field, enter **NoYes**.</span></span>
    4. <span data-ttu-id="7dab4-453">Pasirinkite **Gerai** tam, kad įtrauktumėte naują duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-453">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="7dab4-454">**Duomenų šaltinio tipai** juostoje pasirinkite **Dynamics 365 for Operations\\Numeracija**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-454">In the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
4. <span data-ttu-id="7dab4-455">Įtraukite naują duomenų šaltinį, kuris bus naudojamas prieigos **KMCollectionQuestionMode** numeracijai:</span><span class="sxs-lookup"><span data-stu-id="7dab4-455">Add a new data source that will be used to access the values of the **KMCollectionQuestionMode** enumeration:</span></span>

    1. <span data-ttu-id="7dab4-456">**Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-456">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="7dab4-457">Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **EnumAppQuestionOrder**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-457">In the dialog box, in the **Name** field, enter **EnumAppQuestionOrder**.</span></span>
    3. <span data-ttu-id="7dab4-458">**Numeracija** laukelyje, įveskite **KMCollectionQuestionMode**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-458">In the **Enumeration** field, enter **KMCollectionQuestionMode**.</span></span>
    4. <span data-ttu-id="7dab4-459">Pasirinkite **Gerai** tam, kad įtrauktumėte naują duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-459">Select **OK** to add the new data source.</span></span>

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a><span data-ttu-id="7dab4-460">Įtraukite ER žymes tam, kad sukurtumėte ataskaitą konkrečia kalba</span><span class="sxs-lookup"><span data-stu-id="7dab4-460">Add ER labels to generate a report in a specified language</span></span>

<span data-ttu-id="7dab4-461">Galite įtraukti ER žymes tam, kad konfigūruotumėte kai kuriuos savo duomenų šaltinius ir grąžintumėte vertes priklausančias nuo kalbos, nustatytos modelio žemėlapio iškvietimo turinyje.</span><span class="sxs-lookup"><span data-stu-id="7dab4-461">You can add ER labels to configure some of your data sources to return values that depend on the language that is defined in the context of the model mapping's call.</span></span>

1. <span data-ttu-id="7dab4-462">**Modelio žemėlapio kūrimo įrankis** puslapyje **Duomenų šaltiniai** juostoje pasirinkite **Atsakymas** ir tuomet pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-462">On the **Model mapping designer** page, in the **Data sources** pane, select **Answer**, and then select **Edit**.</span></span>
2. <span data-ttu-id="7dab4-463">Įjunkite **Žymės** laukelį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-463">Activate the **Label** field.</span></span>
3. <span data-ttu-id="7dab4-464">Pasirinkite **Versti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-464">Select **Translate**.</span></span>
4. <span data-ttu-id="7dab4-465">**Teksto vertimo** teksto laukelyje, pasirinkite šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="7dab4-465">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="7dab4-466">**Žymos Id** laukelyje įveskite **Teigiamasatsakymas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-466">In the **Label Id** field, enter **PositiveAnswer**.</span></span>
    2. <span data-ttu-id="7dab4-467">**Tekstas nustatytąja kalba** laukelyje įveskite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-467">In the **Text in default language** field, enter **Yes**.</span></span>
    3. <span data-ttu-id="7dab4-468">Pasirinkite **Versti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-468">Select **Translate**.</span></span>
    4. <span data-ttu-id="7dab4-469">**Žymos Id** laukelyje įveskite **Neigiamasatsakymas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-469">In the **Label Id** field, enter **NegativeAnswer**.</span></span>
    5. <span data-ttu-id="7dab4-470">**Tekstas nustatytąja kalba** laukelyje įveskite **Ne**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-470">In the **Text in default language** field, enter **No**.</span></span>
    6. <span data-ttu-id="7dab4-471">Pasirinkite **Versti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-471">Select **Translate**.</span></span>

5. <span data-ttu-id="7dab4-472">Uždarykite **Teksto vertimo** teksto laukelį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-472">Close the **Text translation** dialog box.</span></span>
6. <span data-ttu-id="7dab4-473">Pasirinkite **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-473">Select **Cancel**.</span></span>

![ER žymių įtraukimas redaguojamam modelio žemėlapio kūrimui](./media/er-quick-start1-adding-labels.png)

<span data-ttu-id="7dab4-475">Įvedėte ER žymes tik nustatytajai kalbai.</span><span class="sxs-lookup"><span data-stu-id="7dab4-475">You've entered ER labels only for the default language.</span></span> <span data-ttu-id="7dab4-476">Dėl informacijos apie tai, kaip ER žymės gali būti išverstos į kitas kalbas, žr. [Kelių kalbų ataskaitų projektavimas](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="7dab4-476">For information about how ER labels can be translated into other languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a><span data-ttu-id="7dab4-477">Įtraukite duomenų šaltinį tam, kad paverstumėte numeracijos verčių lyginimo rezultatus į teksto vertes</span><span class="sxs-lookup"><span data-stu-id="7dab4-477">Add a data source to transform the results of comparing enumeration values to a text value</span></span>

<span data-ttu-id="7dab4-478">Kadangi turite paversti palyginimo rezultatus tarp numeracijos verčių ir teksto verčių keletą kartų skirtingiems šaltiniams, būtų gerai konfigūruoti šią logiką kaip vieną duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-478">Because you must transform the results of the comparison between enumeration values and text values several times for difference sources, it's a good idea to configure this logic as a single data source.</span></span> <span data-ttu-id="7dab4-479">Nepaisant to, tam, kad šis duomenų šaltinis galėtų būti dar kartą panaudojamas, tuomet turite sukonfigūruoti jį kaip parametrų duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-479">However, to make this data source reusable, you must then configure it as the parametrized data source.</span></span> <span data-ttu-id="7dab4-480">Dėl išsamesnės informacijos, žr. [Palaikyti parametrų ER duomenų šaltinių skambučius apskaičiuotam laukelio tipui](er-calculated-field-type.md).</span><span class="sxs-lookup"><span data-stu-id="7dab4-480">For more information, see [Support parameterized calls of ER data sources of the Calculated field type](er-calculated-field-type.md).</span></span>

1. <span data-ttu-id="7dab4-481">**Modelio žemėlapio kūrimo įrankio** puslapyje, **Duomenų šaltinio tipai** juostoje pasirinkite **Bendri\\Tuščia talpykla**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-481">On the **Model mapping designer** page, in the **Data source types** pane, select **General\\Empty container**.</span></span>
2. <span data-ttu-id="7dab4-482">Įtraukite naują talpyklos duomenų šaltinį:</span><span class="sxs-lookup"><span data-stu-id="7dab4-482">Add a new container data source:</span></span>

    1. <span data-ttu-id="7dab4-483">**Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-483">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="7dab4-484">Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **Pagalbininkas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-484">In the dialog box, in the **Name** field, enter **Helper**.</span></span>
    3. <span data-ttu-id="7dab4-485">Pasirinkite **Gerai** tam, kad įtrauktumėte naują duomenų šaltinio talpyklą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-485">Select **OK** to add the new container data source.</span></span>

3. <span data-ttu-id="7dab4-486">**Duomenų šaltinio tipai** juostoje, pasirinkite **Funkcijos\\Apskaičiuotas laukelis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-486">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="7dab4-487">Įtraukite naują duomenų šaltinį:</span><span class="sxs-lookup"><span data-stu-id="7dab4-487">Add a new data source:</span></span>

    1. <span data-ttu-id="7dab4-488">**Duomenų šaltiniai** juostoje pasirinkite **Pagalbininkas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-488">In the **Data sources** pane, select **Helper**.</span></span>
    2. <span data-ttu-id="7dab4-489">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-489">Select **Add**.</span></span>
    3. <span data-ttu-id="7dab4-490">Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **Klausimyno modelis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-490">In the dialog box, in the **Name** field, enter **NoYesEnumToString**.</span></span>
    4. <span data-ttu-id="7dab4-491">Pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-491">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="7dab4-492">Formulės redaktoriuje pasirinkite **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-492">In the formula editor, select **Parameters**.</span></span>
    6. <span data-ttu-id="7dab4-493">Atlikite šiuos žingsnius tam, kad nurodytumėte parametrus konfigūruotai išraiškai:</span><span class="sxs-lookup"><span data-stu-id="7dab4-493">Follow these steps to specify parameters for the configured expression:</span></span>

        1. <span data-ttu-id="7dab4-494">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-494">Select **New**.</span></span>
        2. <span data-ttu-id="7dab4-495">Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **Argumentas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-495">In the dialog box, in the **Name** field, enter **Argument**.</span></span>
        3. <span data-ttu-id="7dab4-496">**Tipo** laukelyje pasirinkite **Boolean** duomenų tipą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-496">In the **Type** field, select the **Boolean** data type.</span></span>
        4. <span data-ttu-id="7dab4-497">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-497">Select **OK**.</span></span>

    7. <span data-ttu-id="7dab4-498">**Formulės** laukelyje įveskite **IF (Argumentas = teisinga, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** tam, kad grąžintumėte tinkamos ER žymos tekstą priklausomai nuo vykdymo kalbos konteksto ir nurodyto parametro vertės.</span><span class="sxs-lookup"><span data-stu-id="7dab4-498">In the **Formula** field, enter **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** to return the text of the appropriate ER label, depending on the language of the execution context and value of the specified parameter.</span></span>
    8. <span data-ttu-id="7dab4-499">Pasirinkite **Įrašyti** ir uždarykite formulės redaktorių.</span><span class="sxs-lookup"><span data-stu-id="7dab4-499">Select **Save**, and close the formula editor.</span></span>
    9. <span data-ttu-id="7dab4-500">Pasirinkite **Gerai** tam, kad įtrauktumėte naują duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-500">Select **OK** to add the new data source.</span></span>

![Konfigūruotas žemėlapio modelis ER duomenų žemėlapio modelio kūrimo įrankyje](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a><span data-ttu-id="7dab4-502">Susiekite duomenų šaltinius su duomenų modelio laukeliais</span><span class="sxs-lookup"><span data-stu-id="7dab4-502">Bind data sources to data model fields</span></span>

<span data-ttu-id="7dab4-503">Privalote susieti konfigūruotus duomenų šaltinius į duomenų modelio laukelius tam, kad nurodytumėte, kaip duomenų modelis bus užpildytas programos duomenų vykdymo laike.</span><span class="sxs-lookup"><span data-stu-id="7dab4-503">You must bind the configured data sources to the fields of the data model to specify how the data model will by filled in with application data at runtime.</span></span>

1. <span data-ttu-id="7dab4-504">**Modelio žemėlapio kūrimo įrankis** puslapyje, **Duomenų modelio** juostoje pasirinkite **BendrovėsPavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-504">On the **Model mapping designer** page, in the **Data model** pane, select **CompanyName**.</span></span>
2. <span data-ttu-id="7dab4-505">**Duomenų šaltiniai** juostoje išplėskite **Bendrovėsinformacija** ir tuomet atlikite šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="7dab4-505">In the **Data sources** pane, expand **CompanyInfo**, and then follow these steps:</span></span>

    1. <span data-ttu-id="7dab4-506">Išplėskite **CompanyInfo.find()** mazgą, kuris atspindi **find()** metodą bendrovėsinformacijos lentelėje.</span><span class="sxs-lookup"><span data-stu-id="7dab4-506">Expand the **CompanyInfo.find()** node that represents the **find()** method of the CompanyInfo table.</span></span>
    2. <span data-ttu-id="7dab4-507">Pasirinkite **CompanyInfo.find().Pavadinimą**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-507">Select **CompanyInfo.find().Name**.</span></span>
    3. <span data-ttu-id="7dab4-508">Pasirinkite **Susieti** tam, kad užpildytumėte bendrovės pavadinimą, kuris yra sukonfigūruotas modelio žemėlapio kūrimas, kuris iškviečiamas vykdymo laiko kontekste.</span><span class="sxs-lookup"><span data-stu-id="7dab4-508">Select **Bind** to fill in the name of the company that the configured model mapping is called in the context of at runtime.</span></span>

3. <span data-ttu-id="7dab4-509">**Duomenų modelis** juostoje pasirinkite **Klausimynas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-509">In the **Data model** pane, select **Questionnaire**.</span></span>
4. <span data-ttu-id="7dab4-510">**Duomenų šaltiniai** juostoje pasirinkite **Klausimynas** ir tuomet pasirinkite **Susieti** tam, kad užpildytumėte klausimyno įrašus.</span><span class="sxs-lookup"><span data-stu-id="7dab4-510">In the **Data sources** pane, select **Questionnaire**, and then select **Bind** to fill in questionnaire records.</span></span>
5. <span data-ttu-id="7dab4-511">**Duomenų modelis** juostoje išplėskite **Klausimynas** ir tuomet atlikite šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="7dab4-511">In the **Data model** pane, expand **Questionnaire**, and then follow these steps:</span></span>

    1. <span data-ttu-id="7dab4-512">**Duomenų modelis** juostoje pasirinkite **Įjungtas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-512">In the **Data model** pane, select **Active**.</span></span>
    2. <span data-ttu-id="7dab4-513">**Duomenų modelis** juostoje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-513">In the **Data model** pane, select **Edit**.</span></span>
    3. <span data-ttu-id="7dab4-514">**Formulės** laukelyje įveskite **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** tam, kad užpildytumėte nuo teksto ir kalbos priklausomą palyginimo rezultatą tarp numeracijos verčių.</span><span class="sxs-lookup"><span data-stu-id="7dab4-514">In the **Formula** field, enter **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** to fill the text-dependent and language-dependent result of the comparison between enumeration values.</span></span>

6. <span data-ttu-id="7dab4-515">Toliau tęskite duomenų šaltinių susiejimą su duomenų modelio laukeliais tokiu pačiu būdu, kol pasieksite tolesnį rezultatą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-515">Continue to bind data sources to data model fields in the same manner until you achieve the following result.</span></span>

    | <span data-ttu-id="7dab4-516">Lauko kelias</span><span class="sxs-lookup"><span data-stu-id="7dab4-516">Field path</span></span>                                              | <span data-ttu-id="7dab4-517">Duomenų tipas</span><span class="sxs-lookup"><span data-stu-id="7dab4-517">Data type</span></span>   | <span data-ttu-id="7dab4-518">Veiksmas</span><span class="sxs-lookup"><span data-stu-id="7dab4-518">Action</span></span> | <span data-ttu-id="7dab4-519">Susiejimo išraiška</span><span class="sxs-lookup"><span data-stu-id="7dab4-519">Binding expression</span></span> |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | <span data-ttu-id="7dab4-520">Bendrovėspavadinimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-520">CompanyName</span></span>                                             | <span data-ttu-id="7dab4-521">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-521">String</span></span>      | <span data-ttu-id="7dab4-522">Susieti</span><span class="sxs-lookup"><span data-stu-id="7dab4-522">Bind</span></span>   | <span data-ttu-id="7dab4-523">CompanyInfo.'find()'.Pavadinimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-523">CompanyInfo.'find()'.Name</span></span> |
    | <span data-ttu-id="7dab4-524">Klausimynas</span><span class="sxs-lookup"><span data-stu-id="7dab4-524">Questionnaire</span></span>                                           | <span data-ttu-id="7dab4-525">Įrašų sąrašas</span><span class="sxs-lookup"><span data-stu-id="7dab4-525">Record list</span></span> | <span data-ttu-id="7dab4-526">Susieti</span><span class="sxs-lookup"><span data-stu-id="7dab4-526">Bind</span></span>   | <span data-ttu-id="7dab4-527">Klausimynas</span><span class="sxs-lookup"><span data-stu-id="7dab4-527">Questionnaire</span></span> |
    | <span data-ttu-id="7dab4-528">Klausimynas\\Įjungtas</span><span class="sxs-lookup"><span data-stu-id="7dab4-528">Questionnaire\\Active</span></span>                                   | <span data-ttu-id="7dab4-529">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-529">String</span></span>      | <span data-ttu-id="7dab4-530">Redagavimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-530">Edit</span></span>   | <span data-ttu-id="7dab4-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="7dab4-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="7dab4-532">Klausimyno\\Kodas</span><span class="sxs-lookup"><span data-stu-id="7dab4-532">Questionnaire\\Code</span></span>                                     | <span data-ttu-id="7dab4-533">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-533">String</span></span>      | <span data-ttu-id="7dab4-534">Susieti</span><span class="sxs-lookup"><span data-stu-id="7dab4-534">Bind</span></span>   | <span data-ttu-id="7dab4-535">\@.kmCollectionId</span><span class="sxs-lookup"><span data-stu-id="7dab4-535">\@.kmCollectionId</span></span> |
    | <span data-ttu-id="7dab4-536">Klausimynas\\Aprašas</span><span class="sxs-lookup"><span data-stu-id="7dab4-536">Questionnaire\\Description</span></span>                              | <span data-ttu-id="7dab4-537">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-537">String</span></span>      | <span data-ttu-id="7dab4-538">Susieti</span><span class="sxs-lookup"><span data-stu-id="7dab4-538">Bind</span></span>   | <span data-ttu-id="7dab4-539">\@.Aprašas</span><span class="sxs-lookup"><span data-stu-id="7dab4-539">\@.Description</span></span> |
    | <span data-ttu-id="7dab4-540">Klausimynas\\Klausimynotipas</span><span class="sxs-lookup"><span data-stu-id="7dab4-540">Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="7dab4-541">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-541">String</span></span>      | <span data-ttu-id="7dab4-542">Susieti</span><span class="sxs-lookup"><span data-stu-id="7dab4-542">Bind</span></span>   | <span data-ttu-id="7dab4-543">\@.'&gt;Relations'.kmCollectionTypeId.Aprašas</span><span class="sxs-lookup"><span data-stu-id="7dab4-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span></span> |
    | <span data-ttu-id="7dab4-544">Klausimynas\\KlausimynoTvarka</span><span class="sxs-lookup"><span data-stu-id="7dab4-544">Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="7dab4-545">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-545">String</span></span>      | <span data-ttu-id="7dab4-546">Redagavimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-546">Edit</span></span>   | <span data-ttu-id="7dab4-547">CASE (\@.questionMode,</span><span class="sxs-lookup"><span data-stu-id="7dab4-547">CASE (\@.questionMode,</span></span><br><span data-ttu-id="7dab4-548">EnumAppQuestionOrder.Conditional, "Conditional",</span><span class="sxs-lookup"><span data-stu-id="7dab4-548">EnumAppQuestionOrder.Conditional, "Conditional",</span></span><br><span data-ttu-id="7dab4-549">EnumAppQuestionOrder.Random, "Atsitiktinis (procentai klausimyne)",</span><span class="sxs-lookup"><span data-stu-id="7dab4-549">EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",</span></span><br><span data-ttu-id="7dab4-550">EnumAppQuestionOrder.RandomGroup, "Atsitiktinis (procentai rezultato grupėse)",</span><span class="sxs-lookup"><span data-stu-id="7dab4-550">EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",</span></span><br><span data-ttu-id="7dab4-551">EnumAppQuestionOrder.Sequence, "Nuoseklus",</span><span class="sxs-lookup"><span data-stu-id="7dab4-551">EnumAppQuestionOrder.Sequence, "Sequential",</span></span><br><span data-ttu-id="7dab4-552">"")</span><span class="sxs-lookup"><span data-stu-id="7dab4-552">"")</span></span> |
    | <span data-ttu-id="7dab4-553">Klausimynas\\Rezultatųgrupė</span><span class="sxs-lookup"><span data-stu-id="7dab4-553">Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="7dab4-554">Įrašyti</span><span class="sxs-lookup"><span data-stu-id="7dab4-554">Record</span></span>      |        | |
    | <span data-ttu-id="7dab4-555">Klausimynas\\Rezultatųgrupė\\Kodas</span><span class="sxs-lookup"><span data-stu-id="7dab4-555">Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="7dab4-556">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-556">String</span></span>      | <span data-ttu-id="7dab4-557">Susieti</span><span class="sxs-lookup"><span data-stu-id="7dab4-557">Bind</span></span>   | <span data-ttu-id="7dab4-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span><span class="sxs-lookup"><span data-stu-id="7dab4-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span></span> |
    | <span data-ttu-id="7dab4-559">Klausimynas\\RezultatųGrupė\\Aprašas</span><span class="sxs-lookup"><span data-stu-id="7dab4-559">Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="7dab4-560">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-560">String</span></span>      | <span data-ttu-id="7dab4-561">Susieti</span><span class="sxs-lookup"><span data-stu-id="7dab4-561">Bind</span></span>   | <span data-ttu-id="7dab4-562">\@.'\$ResultGroup'.aprašas</span><span class="sxs-lookup"><span data-stu-id="7dab4-562">\@.'\$ResultGroup'.description</span></span> |
    | <span data-ttu-id="7dab4-563">Klausimynas\\RezultatųGrupė\\Maks.Taškųskaičius</span><span class="sxs-lookup"><span data-stu-id="7dab4-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="7dab4-564">Tikrasis</span><span class="sxs-lookup"><span data-stu-id="7dab4-564">Real</span></span>        | <span data-ttu-id="7dab4-565">Susieti</span><span class="sxs-lookup"><span data-stu-id="7dab4-565">Bind</span></span>   | <span data-ttu-id="7dab4-566">\@.'\$ResultGroup'.Maks.Taškai</span><span class="sxs-lookup"><span data-stu-id="7dab4-566">\@.'\$ResultGroup'.maxPoint</span></span> |
    | <span data-ttu-id="7dab4-567">Klausimynas\\Klausimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-567">Questionnaire\\Question</span></span>                                 | <span data-ttu-id="7dab4-568">Įrašų sąrašas</span><span class="sxs-lookup"><span data-stu-id="7dab4-568">Record list</span></span> | <span data-ttu-id="7dab4-569">Susieti</span><span class="sxs-lookup"><span data-stu-id="7dab4-569">Bind</span></span>   | <span data-ttu-id="7dab4-570">\@.'&lt;Ryšiai'.KMRinkimoKlausimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-570">\@.'&lt;Relations'.KMCollectionQuestion</span></span> |
    | <span data-ttu-id="7dab4-571">Klausimynas\\Klausimas\\RinkimoSekosNumeris</span><span class="sxs-lookup"><span data-stu-id="7dab4-571">Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="7dab4-572">Sveikasis skaičius</span><span class="sxs-lookup"><span data-stu-id="7dab4-572">Integer</span></span>     | <span data-ttu-id="7dab4-573">Susieti</span><span class="sxs-lookup"><span data-stu-id="7dab4-573">Bind</span></span>   | <span data-ttu-id="7dab4-574">\@.answerRinkimoSekosNumeris</span><span class="sxs-lookup"><span data-stu-id="7dab4-574">\@.answerCollectionSequenceNumber</span></span> |
    | <span data-ttu-id="7dab4-575">Klausimynas\\Klausimas\\Id</span><span class="sxs-lookup"><span data-stu-id="7dab4-575">Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="7dab4-576">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-576">String</span></span>      | <span data-ttu-id="7dab4-577">Susieti</span><span class="sxs-lookup"><span data-stu-id="7dab4-577">Bind</span></span>   | <span data-ttu-id="7dab4-578">\@.kmQuestionId</span><span class="sxs-lookup"><span data-stu-id="7dab4-578">\@.kmQuestionId</span></span> |
    | <span data-ttu-id="7dab4-579">Klausimynas\\Klausimas\\TuriBūtiUžbaigtas</span><span class="sxs-lookup"><span data-stu-id="7dab4-579">Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="7dab4-580">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-580">String</span></span>      | <span data-ttu-id="7dab4-581">Redagavimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-581">Edit</span></span>   | <span data-ttu-id="7dab4-582">Helper.NoYesEnumToString(\@.privalomas = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="7dab4-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="7dab4-583">Klausimynas\\Klausimas\\PirminisKlausimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-583">Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="7dab4-584">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-584">String</span></span>      | <span data-ttu-id="7dab4-585">Susieti</span><span class="sxs-lookup"><span data-stu-id="7dab4-585">Bind</span></span>   | <span data-ttu-id="7dab4-586">\@.parentQuestionId</span><span class="sxs-lookup"><span data-stu-id="7dab4-586">\@.parentQuestionId</span></span> |
    | <span data-ttu-id="7dab4-587">Klausimynas\\Klausimas\\EilėsNumeris</span><span class="sxs-lookup"><span data-stu-id="7dab4-587">Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="7dab4-588">Sveikasis skaičius</span><span class="sxs-lookup"><span data-stu-id="7dab4-588">Integer</span></span>     | <span data-ttu-id="7dab4-589">Susieti</span><span class="sxs-lookup"><span data-stu-id="7dab4-589">Bind</span></span>   | <span data-ttu-id="7dab4-590">\@.EilėsNumeris</span><span class="sxs-lookup"><span data-stu-id="7dab4-590">\@.SequenceNumber</span></span> |
    | <span data-ttu-id="7dab4-591">Klausimynas\\Klausimas\\Tekstas</span><span class="sxs-lookup"><span data-stu-id="7dab4-591">Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="7dab4-592">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-592">String</span></span>      | <span data-ttu-id="7dab4-593">Susieti</span><span class="sxs-lookup"><span data-stu-id="7dab4-593">Bind</span></span>   | <span data-ttu-id="7dab4-594">\@.'\$Klausimo'.tekstas</span><span class="sxs-lookup"><span data-stu-id="7dab4-594">\@.'\$Question'.text</span></span> |
    | <span data-ttu-id="7dab4-595">Klausimynas\\Klausimas\\Atsakymas</span><span class="sxs-lookup"><span data-stu-id="7dab4-595">Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="7dab4-596">Įrašų sąrašas</span><span class="sxs-lookup"><span data-stu-id="7dab4-596">Record list</span></span> | <span data-ttu-id="7dab4-597">Susieti</span><span class="sxs-lookup"><span data-stu-id="7dab4-597">Bind</span></span>   | <span data-ttu-id="7dab4-598">\@.'\$Klausimas'.'\$Atsakymas'</span><span class="sxs-lookup"><span data-stu-id="7dab4-598">\@.'\$Question'.'\$Answer'</span></span> |
    | <span data-ttu-id="7dab4-599">Klausimynas\\Klausimas\\Atsakymas\\TeisingasAtsakymas</span><span class="sxs-lookup"><span data-stu-id="7dab4-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="7dab4-600">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-600">String</span></span>      | <span data-ttu-id="7dab4-601">Redagavimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-601">Edit</span></span>   | <span data-ttu-id="7dab4-602">Helper.NoYesEnumToString(\@.teisingasAtsakymas = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="7dab4-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="7dab4-603">Klausimynas\\Klausimas\\Atsakymas\\Taškai</span><span class="sxs-lookup"><span data-stu-id="7dab4-603">Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="7dab4-604">Tikrasis</span><span class="sxs-lookup"><span data-stu-id="7dab4-604">Real</span></span>        | <span data-ttu-id="7dab4-605">Susieti</span><span class="sxs-lookup"><span data-stu-id="7dab4-605">Bind</span></span>   | <span data-ttu-id="7dab4-606">\@.taškas</span><span class="sxs-lookup"><span data-stu-id="7dab4-606">\@.point</span></span> |
    | <span data-ttu-id="7dab4-607">Klausimynas\\Klausimas\\Atsakymas\\EilėsTvarka</span><span class="sxs-lookup"><span data-stu-id="7dab4-607">Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="7dab4-608">Sveikasis skaičius</span><span class="sxs-lookup"><span data-stu-id="7dab4-608">Integer</span></span>     | <span data-ttu-id="7dab4-609">Susieti</span><span class="sxs-lookup"><span data-stu-id="7dab4-609">Bind</span></span>   | <span data-ttu-id="7dab4-610">\@.eilėsNumeris</span><span class="sxs-lookup"><span data-stu-id="7dab4-610">\@.sequenceNumber</span></span> |
    | <span data-ttu-id="7dab4-611">Klausimynas\\Klausimas\\Atsakymas\\Tekstas</span><span class="sxs-lookup"><span data-stu-id="7dab4-611">Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="7dab4-612">Eilutė</span><span class="sxs-lookup"><span data-stu-id="7dab4-612">String</span></span>      | <span data-ttu-id="7dab4-613">Susieti</span><span class="sxs-lookup"><span data-stu-id="7dab4-613">Bind</span></span>   | <span data-ttu-id="7dab4-614">\@.tekstas</span><span class="sxs-lookup"><span data-stu-id="7dab4-614">\@.text</span></span> |

    <span data-ttu-id="7dab4-615">Tolesnis paveikslėlis rodo galutinį konfigūruoto modelio žemėlapio statusą **Modelio žemėlapio kūrimo įrankio** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="7dab4-615">The following illustration shows the final state of the configured model mapping on the **Model mapping designer** page.</span></span>

    ![Visiškai konfigūruotas žemėlapio modelis ER duomenų žemėlapio modelio kūrimo įrankyje](./media/er-quick-start1-mapping2.png)

7. <span data-ttu-id="7dab4-617">Įrašykite pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="7dab4-617">Save your changes.</span></span>
8. <span data-ttu-id="7dab4-618">Uždarykite puslapį **Modelio susiejimo dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-618">Close the **Model mapping designer** page.</span></span>

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a><span data-ttu-id="7dab4-619">Užbaikite modelio žemėlapio dizainą</span><span class="sxs-lookup"><span data-stu-id="7dab4-619">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="7dab4-620">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-620">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7dab4-621">**Konfigūravimai** puslapyje, konfigūravimo medyje, pasirinkite **Klausimyno žemėlapio kūrimas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-621">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="7dab4-622">**Versijos** „FastTab“, pasirinkite konfigūravimo versiją, kuri turi statusą **Juodraštis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-622">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="7dab4-623">Pasirinkite **Keisti statusą** \> **Užbaigtas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-623">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="7dab4-624">Šios konfigūracijos versijos 1.1 statusas yra keičiamas iš **Juodraštis** į **Užbaigtas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-624">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="7dab4-625">Versija 1.1 nebegali būti keičiama.</span><span class="sxs-lookup"><span data-stu-id="7dab4-625">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="7dab4-626">Šioje versijoje yra konfigūruotų žemėlapio modelis ir gali būti naudojamas pagal kitas ER konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-626">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="7dab4-627">Šios konfigūracijos versija 1.2 yra sukurta ir turi **Juodraštis** statusą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-627">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="7dab4-628">Galite redaguoti šią versiją tam, kad keistumėte **Klausimyno žemėlapio** konfigūravimą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-628">You can edit this version to adjust the **Questionnaire mapping** configuration.</span></span>

![Redaguojamos ER konfigūracijos versijos konfigūravimo puslapyje](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> <span data-ttu-id="7dab4-630">Konfigūruotas modelio žemėlapis yra jūsų finansų konkretus abstrakčių duomenų modelio implementavimas, kuris rodo **Klausimyno** verslo domeną.</span><span class="sxs-lookup"><span data-stu-id="7dab4-630">The configured model mapping is your Finance-specific implementation of the abstract data model that represents the **Questionnaire** business domain.</span></span>

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a><span data-ttu-id="7dab4-631">Suprojektuokite tinkintos ataskaitos šabloną</span><span class="sxs-lookup"><span data-stu-id="7dab4-631">Design a template for a custom report</span></span>

<span data-ttu-id="7dab4-632">ER darbotvarkė naudoja iš anksto nustatytus šablonus tam, kad sukurtų ataskaitas „Microsoft Office“ formatuose („Excel“ darbo knygose ar „Word“ dokumentuose).</span><span class="sxs-lookup"><span data-stu-id="7dab4-632">The ER framework uses predefined templates to generate reports in Microsoft Office formats (Excel workbooks or Word documents).</span></span> <span data-ttu-id="7dab4-633">Kol būtina ataskaita yra kuriama, šablonas yra užpildomas su būtinais duomenimis pagal konfigūruotą darbo srautą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-633">While the required report is being generated, a template is filled in with required data according to the configured dataflow.</span></span> <span data-ttu-id="7dab4-634">Dėl to, pirmiausia turite projektuoti šabloną jūsų tinkintai ataskaitai.</span><span class="sxs-lookup"><span data-stu-id="7dab4-634">Therefore, you must first design a template for your custom report.</span></span> <span data-ttu-id="7dab4-635">Ši ataskaita turi būti sukurta kaip „Excel“ darbo knyga, struktūra rodo tinkintos ataskaitos maketą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-635">This template must be designed as an Excel workbook, the structure of which represents the layout of a custom report.</span></span> <span data-ttu-id="7dab4-636">Privalote užvadinti visus „Excel“ elementus, kuriuos planuojate užpildyti būtinais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="7dab4-636">You must name every Excel item that you plan to fill in with required data.</span></span>

1. <span data-ttu-id="7dab4-637">Atsisiųskite [Klausimynų ataskaitos template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) failą ir įrašykite jį į savo vietinį kompiuterį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-637">Download the [Questionnaires report template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="7dab4-638">Atverkite failą „Excel“ ir peržiūrėkite darbo knygos struktūrą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-638">Open the file in Excel, and review the structure of the workbook.</span></span>

<span data-ttu-id="7dab4-639">Kaip rodo tolesnis paveikslėlis, atsiųstas šablonas buvo suprojektuotas konkrečių klausimynų spausdinimui, kurie rodo klausimyno klausimus kartu su atitinkamais atsakymais.</span><span class="sxs-lookup"><span data-stu-id="7dab4-639">As the following illustration shows, the downloaded template has been designed to print specified questionnaires that present a questionnaire's questions together with appropriate answers.</span></span>

![„Excel“ šablonas konkrečių klausimų spausdinimui](./media/er-quick-start1-template-layout.png)

<span data-ttu-id="7dab4-641">„Excel“ pavadinimai buvo įtraukti į šį šabloną tam, kad būtų užpildyta išsami klausimyno informacija.</span><span class="sxs-lookup"><span data-stu-id="7dab4-641">Excel names have been added to this template to fill in the questionnaire details.</span></span> <span data-ttu-id="7dab4-642">Galite naudoti vadovo pavadinimą „Excel“ pavadinimo peržiūrai.</span><span class="sxs-lookup"><span data-stu-id="7dab4-642">You can use Name Manager to review the Excel names.</span></span>

![Pavadinimo vadovo naudojimas „Excel“ pavadinimų peržiūrai „Excel“ šablone](./media/er-quick-start1-template-names.png)

<span data-ttu-id="7dab4-644">Ataskaitos žymės buvo įkeltos kaip fiksuotas tekstas anglų kalba.</span><span class="sxs-lookup"><span data-stu-id="7dab4-644">Report labels have been added as fixed text in the English language.</span></span> <span data-ttu-id="7dab4-645">Galite pakeisti ataskaitos žymes naujais „Excel“ pavadinimais, kurie užpildo žymes nuo kalbos priklausomu tekstu naudojant ER formatą [žymes](#AddMmLabels), taip kaip padarėte nuo kalbos priklausomomis sąvokomis konfigūruotame modelio žemėlapyje.</span><span class="sxs-lookup"><span data-stu-id="7dab4-645">You can replace the report labels with new Excel names that fill in the labels with language-dependent text by using the ER format [labels](#AddMmLabels), as you did for language-dependent expressions in the configured model mapping.</span></span> <span data-ttu-id="7dab4-646">Šiuo atveju, ER žymės turi būti įtrauktos į redaguojamą ER formatą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-646">In this case, ER labels must be added in the editable ER format.</span></span>

<span data-ttu-id="7dab4-647">Kaip rodo tolesnis paveikslėlis, tinkinta ataskaitos antraštė buvo nurodyta siekiant įjungti „Excel“ puslapių numeravimui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-647">As the following illustration shows, the custom report header has been specified to enable Excel to do paging.</span></span>

![Tinkinta ataskaitos antraštė pateiktame „Excel“ šablone](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a><span data-ttu-id="7dab4-649">Formato kūrimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-649">Design a format</span></span>

<span data-ttu-id="7dab4-650">Kaip vartotojas elektroninės ataskaitos funkcijų konsultanto vaidmenyje, turite sukurti naują ER konfigūraciją, kurioje būtų [formato](general-electronic-reporting.md#FormatComponentOutbound) komponentas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-650">As a user in the Electronic Reporting Functional Consultant role, you must create a new ER configuration that contains a [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="7dab4-651">Turite sukonfigūruoti formato komponentą tam, kad nurodytumėte, kaip ataskaitos šablonas bus užpildytas su būtinais duomenimis vykdymo laiku.</span><span class="sxs-lookup"><span data-stu-id="7dab4-651">You must configure the format component to specify how a report template will be filled in with required data at runtime.</span></span>

<span data-ttu-id="7dab4-652">Atlikę žingsnius [Importuoti suprojektuoto formato konfigūravimą](#FormatImport) skyriuje, galite importuoti reikiamą formatą pateiktame XML faile.</span><span class="sxs-lookup"><span data-stu-id="7dab4-652">By completing the steps in the [Import a designed format configuration](#FormatImport) section, you can import the required format from the provided XML file.</span></span> <span data-ttu-id="7dab4-653">Kitu atveju, galite atlikti žingsnius [Sukurti naują formato konfigūravimą](#FormatCreate) skyriuje, kad suprojektuotumėte šį formatą iš pradžių.</span><span class="sxs-lookup"><span data-stu-id="7dab4-653">Alternatively, you can complete the steps in the [Create a new format configuration](#FormatCreate) section to design this format from scratch.</span></span>

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a><span data-ttu-id="7dab4-654">Importuokite suprojektuotą formato konfigūravimą</span><span class="sxs-lookup"><span data-stu-id="7dab4-654">Import a designed format configuration</span></span>

1. <span data-ttu-id="7dab4-655">Atsisiųskite [Klausimynų format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) failą ir įrašykite jį į savo vietinį kompiuterį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-655">Download the [Questionnaires format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="7dab4-656">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-656">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="7dab4-657">**Elektroninės ataskaitos** darbo srityje pasirinkite **Ataskaitos konfigūravimai**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-657">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="7dab4-658">Veiksmų juostoje pasirinkite **Keisti** \> **Įkelti iš XML failo**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-658">On the Action pane, Select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="7dab4-659">Pasirinkite **Naršyti** ir tuomet suraskite ir pasirinkite **Klausimynų format.version.1.1.xml** failą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-659">Select **Browse**, and then find and select the **Questionnaires format.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="7dab4-660">Pasirinkite **OK** tam, kad importuotumėte konfigūravimą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-660">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="7dab4-661">Tam, kad tęstumėte, praleiskite kitą procedūrą, [Sukurti naujo formato konfigūravimą](#FormatCreate).</span><span class="sxs-lookup"><span data-stu-id="7dab4-661">To continue, skip the next procedure, [Create a new format configuration](#FormatCreate).</span></span>

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a><span data-ttu-id="7dab4-662">Kurti naują formato konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="7dab4-662">Create a new format configuration</span></span>
 
1. <span data-ttu-id="7dab4-663">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-663">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7dab4-664">**Konfigūravimai** puslapyje, konfigūravimo medyje, pasirinkite **Klausimyno modelis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-664">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="7dab4-665">Pasirinkite **Kurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-665">Select **Create configuration**.</span></span>
4. <span data-ttu-id="7dab4-666">Išplečiamajame dialogo lange atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7dab4-666">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="7dab4-667">**Naujas** laukelyje, pasirinkite **Formatas pagal duomenų modelio klausimynus**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-667">In the **New** field, select **Format based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="7dab4-668">**Pavadinimas** laukelyje, įveskite **Klausimyno ataskaita**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-668">In the **Name** field, enter **Questionnaire report**.</span></span>
    3. <span data-ttu-id="7dab4-669">**Duomenų modelio versijos** laukelyje pasirinkite **1**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-669">In the **Data model version** field, select **1**.</span></span>

        > [!NOTE]
        > - <span data-ttu-id="7dab4-670">Jei pasirenkate konkrečia bazinio duomenų modelio versiją, atitinkamos duomenų modelio versijos struktūra bus rodoma jums kaip **Modelio** duomenų šaltinio struktūra sukurtame formate.</span><span class="sxs-lookup"><span data-stu-id="7dab4-670">If you select a specific version of the base data model, the structure of the corresponding version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span>
        > - <span data-ttu-id="7dab4-671">Galite palikti šį laukelį tuščią.</span><span class="sxs-lookup"><span data-stu-id="7dab4-671">You can leave this field blank.</span></span> <span data-ttu-id="7dab4-672">Tokiu atveju, **Juodraščio** duomenų modelio versijos struktūra bus rodoma jums kaip **Modelio** duomenų šaltinio struktūra sukurtu formatu.</span><span class="sxs-lookup"><span data-stu-id="7dab4-672">In that case, the structure of the **Draft** version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span> <span data-ttu-id="7dab4-673">Tuomet galite keisti savo modelį ir nedelsiant matyti pakeitimus savo formate.</span><span class="sxs-lookup"><span data-stu-id="7dab4-673">You can then adjust your model and immediately see those adjustments in your format.</span></span> <span data-ttu-id="7dab4-674">Tokia prieiga gali pagerinti ER sprendimo projekto efektyvumą jums konfigūruojant savo duomenų modelį, modelio žemėlapio kūrimas ir formatą vienu metu.</span><span class="sxs-lookup"><span data-stu-id="7dab4-674">This approach might improve the efficiency of ER solution design when you configure your data model, model mapping, and format simultaneously.</span></span>
        > - <span data-ttu-id="7dab4-675">Jei pasirenkate konkrečią bazinio duomenų modelio versiją, galite perjungti į naudojimą **Juodraščio** versijos vėliau, kai pradėsite redaguoti formatą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-675">If you select a specific version of the base data model, you can switch to using the **Draft** version later, when you start to edit a format.</span></span>

    4. <span data-ttu-id="7dab4-676">**Duomenų modelio sąvoka** laukelyje, pasirinkite **Šaknies** sąvoka.</span><span class="sxs-lookup"><span data-stu-id="7dab4-676">In the **Data model definition** field, select the **Root** definition.</span></span>

5. <span data-ttu-id="7dab4-677">Pasirinkite **Sukurti konfigūravimą** tam, kad sukurtumėte konfigūravimą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-677">Select **Create configuration** to create the configuration.</span></span>

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a><span data-ttu-id="7dab4-678">Importuokite ataskaitos šabloną</span><span class="sxs-lookup"><span data-stu-id="7dab4-678">Import a report template</span></span>

1. <span data-ttu-id="7dab4-679">**Konfigūravimai** puslapyje, konfigūravimo medyje, pasirinkite **Klausimyno ataskaita**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-679">On the **Configurations** page, in the configuration tree, select **Questionnaire report**.</span></span>
2. <span data-ttu-id="7dab4-680">Pasirinkite **Kūrimo įrankį** tam, kad konfigūruotumėte tinkintą formatą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-680">Select **Designer** to start to configure a custom format.</span></span>
3. <span data-ttu-id="7dab4-681">**Formato kūrimo įrankio** puslapyje, veiksmų juostoje pasirinkite  **Importuoti** \> **Importuoti iš „Excel“**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-681">On the **Format designer** page, on the Action Pane, select **Import** \> **Import from Excel**.</span></span>
4. <span data-ttu-id="7dab4-682">Teksto laukelyje, pasirinkite šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="7dab4-682">In the dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="7dab4-683">Pasirinkite **Įtraukti šabloną**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-683">Select **Add template**.</span></span>
    2. <span data-ttu-id="7dab4-684">Suraskite ir pasirinkite vietiniu lygmeniu įrašytus **Klausimynų ataskaitos template.xslx** failą ir tuomet pasirinkite **Atverti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-684">Find and select the locally saved **Questionnaires report template.xslx** file, and then select **Open**.</span></span>
    3. <span data-ttu-id="7dab4-685">Pasirinkite **Gerai** tam, kad importuotumėte šabloną.</span><span class="sxs-lookup"><span data-stu-id="7dab4-685">Select **OK** to import the template.</span></span>

    ![Ataskaitos šablono importavimas](./media/er-quick-start1-template-import.png)

<span data-ttu-id="7dab4-687">**„Excel“\\faile** formato elementas yra automatiškai įtrauktas į redaguojamą formatą kaip šaknies elementas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-687">The **Excel\\File** format element is automatically added to the editable format as a root element.</span></span> <span data-ttu-id="7dab4-688">Taip pat, arba **„Excel“\\Intervalo** formato elementas arba **„Excel“\\Laukelis** formato elementas yra automatiškai įtraukiamas visiems „Excel“ atpažįstamiems importuoto šablono pavadinimams.</span><span class="sxs-lookup"><span data-stu-id="7dab4-688">Additionally, either the **Excel\\Range** format element or the **Excel\\Cell** format element is automatically added for every recognized Excel name of the imported template.</span></span> <span data-ttu-id="7dab4-689">**„Excel“\\Antraštės** formatas buvo patalpintas į lizdą **Eilutės** elemente yra automatiškai įtraukiamas taip, kad rodytų antraštės nustatymus importuotame šablone.</span><span class="sxs-lookup"><span data-stu-id="7dab4-689">The **Excel\\Header** format that has the nested **String** element is automatically added to reflect the header settings of the imported template.</span></span>

![Formato struktūra apima automatiškai įtrauktus elementus ER veikimo kūrimo įrankyje](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a><span data-ttu-id="7dab4-691">Konfigūruokite formatą</span><span class="sxs-lookup"><span data-stu-id="7dab4-691">Configure a format</span></span>

1. <span data-ttu-id="7dab4-692">**Formato kūrimo įrankio** puslapyje, formato medyje pasirinkite **„Excel“** šaknies elementą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-692">On the **Format designer** page, in the format tree, select the **Excel** root element.</span></span>
2. <span data-ttu-id="7dab4-693">**Formato** skirtuke dešinėje puslapio pusėje, **Pavadinimo** laukelyje įveskite <a name="AddFormatRootElement"></a>**Atskaitą**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-693">On the **Format** tab on the right side of the page, in the **Name** field, enter <a name="AddFormatRootElement"></a>**Report**.</span></span>
3. <span data-ttu-id="7dab4-694">**Kalbos pirmenybės** laukelyje pasirinkite **Vartotojo pirmenybės** tam, kad vykdytumėte ataskaitą vartotojo pirmenybine kalba.</span><span class="sxs-lookup"><span data-stu-id="7dab4-694">In the **Language preference** field, select **User preference** to run the report in the user's preferred language.</span></span>
4. <span data-ttu-id="7dab4-695">**Kultūros pirmenybės** laukelyje pasirinkite **Vartotojo pirmenybės** tam, kad vykdytumėte ataskaitą vartotojo pirmenybine kultūra.</span><span class="sxs-lookup"><span data-stu-id="7dab4-695">In the **Culture preference** field, select **User preference** to run the report in the user's preferred culture.</span></span>

    <span data-ttu-id="7dab4-696">Dėl informacijos apie tai, kaip nurodyti kalbos ir kultūros kontekstus ER procesui, žr. [Kelių kalbų ataskaitų projektavimas](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="7dab4-696">For information about how to specify the language and culture contexts for an ER process, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

    ![Kalbos ir kultūros nustatymų konfigūravimas pasirinktai ataskaitai ER veiksmų kūrimo įrankyje](./media/er-quick-start1-template-format-structure1.png)

5. <span data-ttu-id="7dab4-698">Formato medyje išplėskite šaknies lizdą ir tuomet pasirinkite **RezultatųGrupė**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-698">In the format tree, expand the root node, and then select **ResultsGroup**.</span></span>
6. <span data-ttu-id="7dab4-699">**Formato** skirtuke, **Atkartojimo kryptis** laukelyje pasirinkite **Jokio atkartojimo**, nes nesitikite turėti daugiau nei vienos rezultatų grupės vienam klausimynui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-699">On the **Format** tab, in the **Replication direction** field, select **No replication**, because you don't expect to have multiple result groups for a single questionnaire.</span></span>

    ![Atkartojimo krypties nustatymas intervalo formato elementams ER veikimo kūrimo įrankyje](./media/er-quick-start1-template-format-structure2.png)

7. <span data-ttu-id="7dab4-701">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-701">Select **Save**.</span></span>

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a><span data-ttu-id="7dab4-702">Nustatykite duomenų susiejimą ataskaitos pavadinimui</span><span class="sxs-lookup"><span data-stu-id="7dab4-702">Define the data binding for a report title</span></span>

<span data-ttu-id="7dab4-703">Privalote nurodyti duomenų susiejimą formato elementui, kuris yra naudojamas užpildyti sukurtos ataskaitos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-703">You must specify a data binding for a format element that is used to fill in the title of a generated report.</span></span>

1. <span data-ttu-id="7dab4-704">**Formato kūrimo įrankio** puslapyje, **Žemėlapio kūrimo** skirtuke dešinėje pasirinkite **Ataskaita\\Ataskaitos pavadinimas** elementą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-704">On the **Format designer** page, on the **Mapping** tab on the right, select the **Report\\ReportTitle** element.</span></span>
2. <span data-ttu-id="7dab4-705">Pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-705">Select **Edit formula**.</span></span>
3. <span data-ttu-id="7dab4-706">Formulės redaktoriuje pasirinkite **Versti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-706">In the formula editor, select **Translate**.</span></span>
4. <span data-ttu-id="7dab4-707">**Teksto vertimo** teksto laukelyje, pasirinkite šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="7dab4-707">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="7dab4-708">**Žymos ID** laukelyje įveskite **Ataskaitopavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-708">In the **Label ID** field, enter **ReportTitle**.</span></span>
    2. <span data-ttu-id="7dab4-709">**Tekstas nustatytąja kalba** laukelyje įveskite **Klausimyno ataskaita**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-709">In the **Text in default language** field, enter **Questionnaires report**.</span></span>
    3. <span data-ttu-id="7dab4-710">Pasirinkite **Versti**, tuomet pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-710">Select **Translate**, and then select **Save**.</span></span>
    4. <span data-ttu-id="7dab4-711">Pasirinkite **Versti** tam, kad užvertumėte **Teksto vertimo** teksto laukelį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-711">Select **Translate** to close the **Text translation** dialog box.</span></span>

5. <span data-ttu-id="7dab4-712">Uždarykite formulės redaktorių.</span><span class="sxs-lookup"><span data-stu-id="7dab4-712">Close the formula editor.</span></span>

    ![Konfigūruokite susiejimą sukurtos ataskaitos pavadinimo užpildymui](./media/er-quick-start1-add-report-title-label.png)

<span data-ttu-id="7dab4-714">Galite naudoti šią techniką tam, kad paverstumėte visas kitas esamo šablono žymes priklausomas nuo kalbos.</span><span class="sxs-lookup"><span data-stu-id="7dab4-714">You can use this technique to make all other labels of the current template language-dependent.</span></span> <span data-ttu-id="7dab4-715">Dėl informacijos apie tai, kaip vieno ER konfigūravimo žymės gali būti išverstos į visas palaikomas kalbas, žr. [Kelių kalbų ataskaitų projektavimas](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="7dab4-715">For information about how the added labels of a single ER configuration can be translated into all supported languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a><span data-ttu-id="7dab4-716">Peržiūrėkite modelio duomenų šaltinį</span><span class="sxs-lookup"><span data-stu-id="7dab4-716">Review model data source</span></span>

1. <span data-ttu-id="7dab4-717">**Formato kūrimo** puslapyje, **Žemėlapio** skirtuke pasirinkite <a name="ModelDSName"></a>**modelio** duomenų šaltinį, kuris rodo pagrindinį šio ER formato duomenų modelį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-717">On the **Format designer** page, on the **Mapping** tab, select the <a name="ModelDSName"></a>**model** data source that represents the base data model of this ER format.</span></span>
2. <span data-ttu-id="7dab4-718">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-718">Select **Edit**.</span></span>
3. <span data-ttu-id="7dab4-719">Peržiūrėkite informaciją esančią **Duomenų šaltinio ypatybės** teksto laukelyje.</span><span class="sxs-lookup"><span data-stu-id="7dab4-719">Review the information in the **Data source properties** dialog box.</span></span> <span data-ttu-id="7dab4-720">Šis duomenų šaltinis rodo **Klausimynų** duomenų modelio komponento versiją 1, kuri yra **Klausimynų modelio** ER konfigūravime.</span><span class="sxs-lookup"><span data-stu-id="7dab4-720">This data source represents version 1 of the **Questionnaires** data model component that resides in the **Questionnaires model** ER configuration.</span></span>

![Modelio duomenų šaltinio ypatybės ER veikimo kūrimo įrankyje](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a><span data-ttu-id="7dab4-722">Susiekite formato elementus su duomenų šaltinio laukeliais</span><span class="sxs-lookup"><span data-stu-id="7dab4-722">Bind format elements to data source fields</span></span>

<span data-ttu-id="7dab4-723">Tam, kad nurodytumėte, kaip šablonas yra užpildomas vykdymo laiku, privalote susieti visus formato elementus, susijusius su atitinkamu „Excel“ pavadinimu į vieną šio formato duomenų šaltinio laukelį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-723">To specify how a template is filled in at runtime, you must bind every format element that is associated with an appropriate Excel name to a single field of this format's data source.</span></span>

1. <span data-ttu-id="7dab4-724">**FFormato kūrimo įrankio** puslapyje, formato medyje, pasirinkite **Ataskaita\\BendrovėsPavadinimo** formato elementą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-724">On the **Format designer** page, in the format tree, select the **Report\\CompanyName** format element.</span></span>
2. <span data-ttu-id="7dab4-725">**Žemėlapio kūrimas** skirtuke, pasirinkite **model.BendrovėPavadinimo** duomenų šaltinio laukelius **Eilutė** tipe.</span><span class="sxs-lookup"><span data-stu-id="7dab4-725">On the **Mapping** tab, select the **model.CompanyName** data source field of the **String** type.</span></span>
3. <span data-ttu-id="7dab4-726">Pasirinkite **Susieti** tam, kad įvestumėte bendrovės pavadinimą šablone.</span><span class="sxs-lookup"><span data-stu-id="7dab4-726">Select **Bind** to enter a company name in a template.</span></span>
4. <span data-ttu-id="7dab4-727">Formato medyje pasirinkite **Ataskaita\\Klausimynas** elementą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-727">In the format tree, select the **Report\\Questionnaire** element.</span></span>
5. <span data-ttu-id="7dab4-728">**Žemėlapio kūrimas** skirtuke, pasirinkite **model.Klausimynas** duomenų šaltinio laukelius **Įrašo sąrašas** tipe.</span><span class="sxs-lookup"><span data-stu-id="7dab4-728">On the **Mapping** tab, select the **model.Questionnaire** data source field of the **Record list** type.</span></span>
6. <span data-ttu-id="7dab4-729">Pasirinkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-729">Select **Bind**.</span></span>
7. <span data-ttu-id="7dab4-730">Pasirinkite **Rodyti išsamią informaciją** tam, kad matytumėte daugiau išsamios informacijos formato elementams.</span><span class="sxs-lookup"><span data-stu-id="7dab4-730">Select **Show details** to see more details for format elements.</span></span>

    <span data-ttu-id="7dab4-731">**Klausimynas** intervalo formato elementas yra sukonfigūruotas vertikaliam atkartojimui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-731">The **Questionnaire** range format element is configured as vertically replicated.</span></span> <span data-ttu-id="7dab4-732">Kai jis susietas su duomenų šaltinius **Įrašo sąrašo** tipe, atitinkamas **Klausimyno** intervalas „Excel“ šablone yra kartojamas kiekvienam susieto duomenų šaltinio įrašui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-732">When it's bound to a data source of the **Record list** type, the appropriate **Questionnaire** range of the Excel template is repeated for every record of the bound data source.</span></span>
 
    ![Klausimyno intervalo formato elemento susiejimas su atitinkamais įrašo sąrašo duomenų šaltiniais ER veikimo kūrimo įrankyje](./media/er-quick-start1-bindings1.png)

    <span data-ttu-id="7dab4-734">Kadangi **Klausimyno** intervalas „Excel“ šablone yra nurodytas tarp 5 per 14, šios eilutės yra atkartojamos visiems ataskaitos klausimynams.</span><span class="sxs-lookup"><span data-stu-id="7dab4-734">Because the **Questionnaire** range of the Excel template is defined between rows 5 through 14, these rows are repeated for every reported questionnaire.</span></span>

    ![Eilutės „Excel“ šablone, kurios bus atkartotos sukurtoje ataskaitoje kiekvienam įrašui įrašo sąrašo duomenų šaltiniuose](./media/er-quick-start1-template-questionnaire-range.png)

8. <span data-ttu-id="7dab4-736">Konfigūruoti panašius susiejimus likusiems formato elementams, kaip aprašyta tolesnėje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="7dab4-736">Configure similar bindings for the remaining format elements, as described in the following table.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7dab4-737">Šioje lentelėje, „Duomenų šaltinio kelio“ informacijos stulpelis daro prielaidą, kad [atitinkamas kelias](relative-path-data-bindings-er-models-format.md) ER funkcija yra įjungta.</span><span class="sxs-lookup"><span data-stu-id="7dab4-737">In this table, the information in the "Data source path" column assumes that the [relative path](relative-path-data-bindings-er-models-format.md) ER feature is turned on.</span></span>

    | <span data-ttu-id="7dab4-738">Formato elemento kelias</span><span class="sxs-lookup"><span data-stu-id="7dab4-738">Format element path</span></span>                                      | <span data-ttu-id="7dab4-739">Duomenų šaltinio kelias</span><span class="sxs-lookup"><span data-stu-id="7dab4-739">Data source path</span></span> |
    |----------------------------------------------------------|------------------|
    | <span data-ttu-id="7dab4-740">„Excel“\\AtaskaitosPavadinimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-740">Excel\\ReportTitle</span></span>                                       | <span data-ttu-id="7dab4-741">**\@"GER\_LABEL:ReportTitle"**</span><span class="sxs-lookup"><span data-stu-id="7dab4-741">**\@"GER\_LABEL:ReportTitle"**</span></span> |
    | <span data-ttu-id="7dab4-742">„Excel“\\BendrovėsPavadinimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-742">Excel\\CompanyName</span></span>                                       | <span data-ttu-id="7dab4-743">**model.CompanyName**</span><span class="sxs-lookup"><span data-stu-id="7dab4-743">**model.CompanyName**</span></span> |
    | <span data-ttu-id="7dab4-744">„Excel“\\Klausimynas</span><span class="sxs-lookup"><span data-stu-id="7dab4-744">Excel\\Questionnaire</span></span>                                     | <span data-ttu-id="7dab4-745">**model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="7dab4-745">**model.Questionnaire**</span></span> |
    | <span data-ttu-id="7dab4-746">„Excel“\\Klausimynas\\Įjungtas</span><span class="sxs-lookup"><span data-stu-id="7dab4-746">Excel\\Questionnaire\\Active</span></span>                             | <span data-ttu-id="7dab4-747">**\@.Įjungtas**, kai **\@** yra **modelio.Klausimynas**</span><span class="sxs-lookup"><span data-stu-id="7dab4-747">**\@.Active**, where **\@** is **model.Questionnaire**</span></span> |
    | <span data-ttu-id="7dab4-748">„Excel“\\Klausimynas\\Kodas</span><span class="sxs-lookup"><span data-stu-id="7dab4-748">Excel\\Questionnaire\\Code</span></span>                               | <span data-ttu-id="7dab4-749">**\@.Kodas**</span><span class="sxs-lookup"><span data-stu-id="7dab4-749">**\@.Code**</span></span> |
    | <span data-ttu-id="7dab4-750">„Excel“\\Klausimynas\\Aprašas</span><span class="sxs-lookup"><span data-stu-id="7dab4-750">Excel\\Questionnaire\\Description</span></span>                        | <span data-ttu-id="7dab4-751">**\@.Aprašas**</span><span class="sxs-lookup"><span data-stu-id="7dab4-751">**\@.Description**</span></span> |
    | <span data-ttu-id="7dab4-752">„Excel“\\Klausimynas\\Klausimynotipas</span><span class="sxs-lookup"><span data-stu-id="7dab4-752">Excel\\Questionnaire\\QuestionnaireType</span></span>                  | <span data-ttu-id="7dab4-753">**\@.KlausimynoTipas**</span><span class="sxs-lookup"><span data-stu-id="7dab4-753">**\@.QuestionnaireType**</span></span> |
    | <span data-ttu-id="7dab4-754">„Excel“\\Klausimynas\\Klausimynotvarka</span><span class="sxs-lookup"><span data-stu-id="7dab4-754">Excel\\Questionnaire\\QuestionOrder</span></span>                      | <span data-ttu-id="7dab4-755">**\@.KlausimynoTvarka**</span><span class="sxs-lookup"><span data-stu-id="7dab4-755">**\@.QuestionOrder**</span></span> |
    | <span data-ttu-id="7dab4-756">„Excel“\\Klausimynas\\RezultatųGrupė\\Kodas\_</span><span class="sxs-lookup"><span data-stu-id="7dab4-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span></span>               | <span data-ttu-id="7dab4-757">**\@.RezultatųGrupės.Kodas**</span><span class="sxs-lookup"><span data-stu-id="7dab4-757">**\@.ResultsGroup.Code**</span></span> |
    | <span data-ttu-id="7dab4-758">„Excel“\\Klausimynas\\RezultatųGrupė\\Aprašas\_</span><span class="sxs-lookup"><span data-stu-id="7dab4-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span></span>        | <span data-ttu-id="7dab4-759">**\@.RezultatųGrupės.Aprašas**</span><span class="sxs-lookup"><span data-stu-id="7dab4-759">**\@.ResultsGroup.Description**</span></span> |
    | <span data-ttu-id="7dab4-760">„Excel“\\Klausimynas\\Rezultatųgrupė\\Maks.taškųskaičius</span><span class="sxs-lookup"><span data-stu-id="7dab4-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>    | <span data-ttu-id="7dab4-761">**\@.RezultatųGrupė.Maks.taškųskaičius**</span><span class="sxs-lookup"><span data-stu-id="7dab4-761">**\@.ResultsGroup.MaxNumberOfPoint**</span></span> |
    | <span data-ttu-id="7dab4-762">„Excel“\\Klausimynas\\Klausimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-762">Excel\\Questionnaire\\Question</span></span>                           | <span data-ttu-id="7dab4-763">**\@.Klausimas**</span><span class="sxs-lookup"><span data-stu-id="7dab4-763">**\@.Question**</span></span> |
    | <span data-ttu-id="7dab4-764">„Excel“\\Klausimynas\\Klausimas\\Surinkimoeilėsnumeris</span><span class="sxs-lookup"><span data-stu-id="7dab4-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span></span> | <span data-ttu-id="7dab4-765">**\@.CollectionSequenceNumber**, kai **\@** yra **modelio.Klausimynas.Klausimas**</span><span class="sxs-lookup"><span data-stu-id="7dab4-765">**\@.CollectionSequenceNumber**, where **\@** is **model.Questionnaire.Question**</span></span> |
    | <span data-ttu-id="7dab4-766">„Excel“\\Klausimynas\\Klausimas\\Id</span><span class="sxs-lookup"><span data-stu-id="7dab4-766">Excel\\Questionnaire\\Question\\Id</span></span>                       | <span data-ttu-id="7dab4-767">**\@.Id**</span><span class="sxs-lookup"><span data-stu-id="7dab4-767">**\@.Id**</span></span> |
    | <span data-ttu-id="7dab4-768">„Excel“\\Klausimynas\\Klausimas\\Turibūtiužbaigtas</span><span class="sxs-lookup"><span data-stu-id="7dab4-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span></span>          | <span data-ttu-id="7dab4-769">**\@.Turibūtiužbaigtas**</span><span class="sxs-lookup"><span data-stu-id="7dab4-769">**\@.MustBeCompleted**</span></span> |
    | <span data-ttu-id="7dab4-770">„Excel“\\Klausimynas\\Klausimas\\Pirmasisklausimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span></span>          | <span data-ttu-id="7dab4-771">**\@.PirmasisKlausimas**</span><span class="sxs-lookup"><span data-stu-id="7dab4-771">**\@.PrimaryQuestion**</span></span> |
    | <span data-ttu-id="7dab4-772">„Excel“\\Klausimynas\\Klausimas\\Eilėsnumeris</span><span class="sxs-lookup"><span data-stu-id="7dab4-772">Excel\\Questionnaire\\Question\\SequenceNumber</span></span>           | <span data-ttu-id="7dab4-773">**\@.EilėsNumeris**</span><span class="sxs-lookup"><span data-stu-id="7dab4-773">**\@.SequenceNumber**</span></span> |
    | <span data-ttu-id="7dab4-774">„Excel“\\Klausimynas\\Klausimas\\Tekstas</span><span class="sxs-lookup"><span data-stu-id="7dab4-774">Excel\\Questionnaire\\Question\\Text</span></span>                     | <span data-ttu-id="7dab4-775">**\@.Tekstas**</span><span class="sxs-lookup"><span data-stu-id="7dab4-775">**\@.Text**</span></span> |
    | <span data-ttu-id="7dab4-776">„Excel“\\Klausimynas\\Klausimas\\Atsakymas</span><span class="sxs-lookup"><span data-stu-id="7dab4-776">Excel\\Questionnaire\\Question\\Answer</span></span>                   | <span data-ttu-id="7dab4-777">**\@.Atsakymas**</span><span class="sxs-lookup"><span data-stu-id="7dab4-777">**\@.Answer**</span></span> |
    | <span data-ttu-id="7dab4-778">„Excel“\\Klausimynas\\Klausimas\\Atsakymas\\Teisingasatsakymas</span><span class="sxs-lookup"><span data-stu-id="7dab4-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>    | <span data-ttu-id="7dab4-779">**\@.TeisingasAtsakymas**, kai **\@** yra **modelio.Klausimynas.Atsakymas**</span><span class="sxs-lookup"><span data-stu-id="7dab4-779">**\@.CorrectAnswer**, where **\@** is **model.Questionnaire.Answer**</span></span> |
    | <span data-ttu-id="7dab4-780">„Excel“\\Klausimynas\\Klausimas\\Atsakymas\\Taškai</span><span class="sxs-lookup"><span data-stu-id="7dab4-780">Excel\\Questionnaire\\Question\\Answer\\Points</span></span>           | <span data-ttu-id="7dab4-781">**\@.Taškai**</span><span class="sxs-lookup"><span data-stu-id="7dab4-781">**\@.Points**</span></span> |
    | <span data-ttu-id="7dab4-782">„Excel“\\Klausimynas\\Klausimas\\Atsakymas\\Tekstas</span><span class="sxs-lookup"><span data-stu-id="7dab4-782">Excel\\Questionnaire\\Question\\Answer\\Text</span></span>             | <span data-ttu-id="7dab4-783">**\@.Tekstas**</span><span class="sxs-lookup"><span data-stu-id="7dab4-783">**\@.Text**</span></span> |

9. <span data-ttu-id="7dab4-784">Jums pabaigus, pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-784">When you've finished, select **Save**.</span></span>

<span data-ttu-id="7dab4-785">Toliau pateiktas paveikslėlis rodo galutinį sukonfigūruotų susietus duomenis **Formato žemėlapio kūrimo įrankio** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="7dab4-785">The following illustration shows the final state of the configured data bindings on the **Format designer** page.</span></span>

![Konfigūruotas duomenų susiejimas ER veikimo kūrimo įrankyje](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> <span data-ttu-id="7dab4-787">Visa konkrečių duomenų šaltinių ir susiejimų kolekcija rodo formato žemėlapio komponentą konfigūruotam formatui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-787">The whole collection of specified data sources and bindings represents a format mapping component of the configured format.</span></span> <span data-ttu-id="7dab4-788">Šio formato žemėlapio kūrimas yra iškviečiamas jums vykdant konfigūruotą formatą ataskaitos kūrimui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-788">This format mapping is called when you run the configured format for report generation.</span></span>

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a><span data-ttu-id="7dab4-789">Vykdykite suprojektuotą formatą iš ER</span><span class="sxs-lookup"><span data-stu-id="7dab4-789">Run a designed format from ER</span></span>

<span data-ttu-id="7dab4-790">Dabar galite vykdyti suprojektuotą formatą bandymo tikslais iš **Konfigūravimo** puslapio.</span><span class="sxs-lookup"><span data-stu-id="7dab4-790">You can now run a designed format for testing purposes from the **Configurations** page.</span></span>

1. <span data-ttu-id="7dab4-791">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-791">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7dab4-792">**Konfigūravimo** puslapyje, konfigūravimo medyje, išplėskite **Klausimyno modelį** ir tuomet pasirinkite **Klausimyno ataskaitą**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-792">On the **Configuration** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="7dab4-793">Pasirinkite **Kūrimo įrankį** formato versijai,, kuri turi statusą **Juodraštis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-793">Select **Designer** for the format version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="7dab4-794">Puslapyje **Formato dizaino įrankis** pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-794">On the **Format designer** page, select **Run**.</span></span>
5. <span data-ttu-id="7dab4-795">**ER parametrai** teksto laukelyje, **Apimami įrašai** „FastTab“, konfigūruokite filtravimo parinktis taip, kad tik **SBCCrsExam** klausimynas būtų įtrauktas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-795">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
6. <span data-ttu-id="7dab4-796">Pasirinkite **Gerai** filtravimo parinkties patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-796">Select **OK** to confirm the filtering option.</span></span>
7. <span data-ttu-id="7dab4-797">Pasirinkite **Gerai** ataskaitos vykdymui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-797">Select **OK** to run the report.</span></span>
8. <span data-ttu-id="7dab4-798">Peržiūrėkite sukurtą ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-798">Review the generated report.</span></span>

<span data-ttu-id="7dab4-799">Pagal [nutylėjimą](electronic-reporting-destinations.md#default-behavior), sukurta ataskaita yra pristatoma „Excel“ faile, kurį galite atsisiųsti.</span><span class="sxs-lookup"><span data-stu-id="7dab4-799">By [default](electronic-reporting-destinations.md#default-behavior), a generated report is delivered as an Excel file that you can download.</span></span> <span data-ttu-id="7dab4-800">Tolesni paveikslėliai rodo du „Excel“ formatų sukurtos ataskaitos puslapius.</span><span class="sxs-lookup"><span data-stu-id="7dab4-800">The following illustrations show two pages of the generated report in Excel format.</span></span>

![„Excel“ formatų sukurtos ataskaitos pavyzdys, puslapis 1](./media/er-quick-start1-report1a.png)

![„Excel“ formatų sukurtos ataskaitos pavyzdys, puslapis 2](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a><span data-ttu-id="7dab4-803">Suderinkite projektavimo formatą</span><span class="sxs-lookup"><span data-stu-id="7dab4-803">Tune a designed format</span></span>

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a><span data-ttu-id="7dab4-804">Keiskite formatą tam, kad pakeistumėte sukurto dokumento pavadinimą</span><span class="sxs-lookup"><span data-stu-id="7dab4-804">Modify a format to change the name of a generated document</span></span>

<span data-ttu-id="7dab4-805">Pagal nutylėjimą, sukurtas dokumentas yra pavadintas naudojant esamo vartotojo slapyvardį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-805">By default, a generated document is named by using the alias of the current user.</span></span> <span data-ttu-id="7dab4-806">Keisdami formatą galite pakeisti šią elgseną taip, kad sukurtas dokumentas būtų pavadintas pagal jūsų tinkintą logiką.</span><span class="sxs-lookup"><span data-stu-id="7dab4-806">By modifying the format, you can change this behavior so that a generated document is named based on your custom logic.</span></span> <span data-ttu-id="7dab4-807">Pavyzdžiui, sugeneruoto dokumento pavadinimas gali būti paremtas esamos datos ir laiko sesija ir ataskaitos pavadinimu.</span><span class="sxs-lookup"><span data-stu-id="7dab4-807">For example, the name of a generated document can be based on the current session date and time, and on the report's title.</span></span>

1. <span data-ttu-id="7dab4-808">**Formato kūrimo įrankio** puslapyje, formato medyje pasirinkite **„Ataskaita“** šaknies elementą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-808">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="7dab4-809">**Žemėlapis** skirtuke pasirinkite **Redaguoti failo pavadinimą**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-809">On the **Mapping** tab, select **Edit file name**.</span></span>
3. <span data-ttu-id="7dab4-810">**Formulės** laukelyje įveskite **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-810">In the **Formula** field, enter **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span></span>
4. <span data-ttu-id="7dab4-811">Pasirinkite **Įrašyti** ir uždarykite formulės redaktorių.</span><span class="sxs-lookup"><span data-stu-id="7dab4-811">Select **Save**, and close the formula editor.</span></span>
5. <span data-ttu-id="7dab4-812">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-812">Select **Save**.</span></span>

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a><span data-ttu-id="7dab4-813">Keiskite formatą tam, kad pakeistumėte klausimų seką</span><span class="sxs-lookup"><span data-stu-id="7dab4-813">Modify a format to change the order of questions</span></span>

<span data-ttu-id="7dab4-814">Klausimai yra teisingai išrikiuoti sukurtoje ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="7dab4-814">The questions aren't correctly ordered in a generated report.</span></span> <span data-ttu-id="7dab4-815">Galite keisti tvarką keisdami formatą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-815">You can change the order by modifying the format.</span></span>

1. <span data-ttu-id="7dab4-816">**Formato kūrimo įrankio** puslapyje, formato medyje pasirinkite **„Ataskaita“** šaknies elementą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-816">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="7dab4-817">**Žemėlapio** skirtuke, formato medyje, išplėskite **Ataskaita\\Klausimynas\\Klausimas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-817">On the **Mapping** tab, in the format tree, expand **Report\\Questionnaire\\Question**.</span></span>

    ![Klausimo formato intervalo tipo elementas ER veikimo kūrimo įrankyje](./media/er-quick-start1-bindings3.png)

3. <span data-ttu-id="7dab4-819">**Žemėlapis** skirtuke pasirinkite **modelio.Klausimynas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-819">On the **Mapping** tab, select **model.Questionnaire**.</span></span>
4. <span data-ttu-id="7dab4-820">Pasirinkite **Įtraukti** \> **Funkcijos\\Apskaičiuotas laukelis** ir tuomet **Pavadinimo** laukelyje įveskite **IšrikiuotiKlausimai**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-820">Select **Add** \> **Functions\\Calculated field**, and then, in the **Name** field, enter **OrderedQuestions**.</span></span>
5. <span data-ttu-id="7dab4-821">Pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-821">Select **Edit formula**.</span></span>
6. <span data-ttu-id="7dab4-822">Formulės redaktoriuje, **Formulės** laukelyje įveskite **RIKIUOTIPAGAL (modelis.Klausimynas.Klausimas, modelis.Klausimynas.Klausimas.EilėsTvarka)** tam, kad išrikiuotumėte klausimų sąrašą pagal esamą klausimyną eilės tvarkos skaičiais.</span><span class="sxs-lookup"><span data-stu-id="7dab4-822">In the formula editor, in the **Formula** field, enter **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** to order the list of questions of the current questionnaire by the sequence order number.</span></span>
7. <span data-ttu-id="7dab4-823">Pasirinkite **Įrašyti** ir uždarykite formulės redaktorių.</span><span class="sxs-lookup"><span data-stu-id="7dab4-823">Select **Save**, and close the formula editor.</span></span>
8. <span data-ttu-id="7dab4-824">Pasirinkite **Gerai** tam, kad užbaigtumėte naujo apskaičiuoto laukelio įvedimą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-824">Select **OK** to complete the entry of a new calculated field.</span></span>
9. <span data-ttu-id="7dab4-825">**Žemėlapis** skirtuke pasirinkite **modelio.Klausimynas.IšrikiuotiKlausimai**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-825">On the **Mapping** tab, select **model.Questionnaire.OrderedQuestions**.</span></span>
10. <span data-ttu-id="7dab4-826">Formato medyje pasirinkite **„Excel“\\Klausimynas\\Klausimas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-826">In the format tree, select **Excel\\Questionnaire\\Question**.</span></span>
11. <span data-ttu-id="7dab4-827">Pasirinkite **Susieti** ir tuomet patvirtinkite, kad esamas **modelis.Klausimynas.Klausimai** kelias yra pakeistas nauju **modeliu.Klausimynu.IšrikiuotiKlausimai** keliu visų lizduose esančių elementų susiejime.</span><span class="sxs-lookup"><span data-stu-id="7dab4-827">Select **Bind**, and then confirm that the current **model.Questionnaire.Questions** path is replaced by the new **model.Questionnaire.OrderedQuestions** path in all bindings of nested elements.</span></span>
12. <span data-ttu-id="7dab4-828">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-828">Select **Save**.</span></span>

![Susiekite klausimų formato elementą su konfigūruotu išriškiuotųklausimų duomenų šaltiniu ER veikimo kūrimo įrankyje](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a><span data-ttu-id="7dab4-830">Vykdykite pakeistą formatą iš ER</span><span class="sxs-lookup"><span data-stu-id="7dab4-830">Run a modified format from ER</span></span>

<span data-ttu-id="7dab4-831">Dabar galite vykdyti pakeistą formatą bandymo tikslais iš ER darbotvarkės.</span><span class="sxs-lookup"><span data-stu-id="7dab4-831">You can now run a modified format for testing purposes from the ER framework.</span></span>

1. <span data-ttu-id="7dab4-832">Puslapyje **Formato dizaino įrankis** pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-832">On the **Format designer** page, select **Run**.</span></span>
2. <span data-ttu-id="7dab4-833">**ER parametrai** teksto laukelyje, **Apimami įrašai** „FastTab“, konfigūruokite filtravimo parinktis taip, kad tik **SBCCrsExam** klausimynas būtų įtrauktas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-833">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
3. <span data-ttu-id="7dab4-834">Pasirinkite **Gerai** filtravimo parinkties patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-834">Select **OK** to confirm the filtering option.</span></span>
4. <span data-ttu-id="7dab4-835">Pasirinkite **Gerai** ataskaitos vykdymui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-835">Select **OK** to run the report.</span></span>
5. <span data-ttu-id="7dab4-836">Peržiūrėkite sukurtą ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-836">Review the generated report.</span></span>

<span data-ttu-id="7dab4-837">Tolesnis paveikslėlis rodo „Excel“ formatu sukurtą ataskaitą, kurioje klausimai yra teisingai išrikiuoti.</span><span class="sxs-lookup"><span data-stu-id="7dab4-837">The following illustration shows a generated report in Excel format where the questions are correctly ordered.</span></span>

![Sukurta ataskaita „Excel“ formatu turi tinkamai išrikiuotus klausimus](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a><span data-ttu-id="7dab4-839">Užbaikite formato projektavimą</span><span class="sxs-lookup"><span data-stu-id="7dab4-839">Complete the format design</span></span>

1. <span data-ttu-id="7dab4-840">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-840">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7dab4-841">**Konfigūravimai** puslapyje, konfigūravimo medyje, išplėskite **Klausimyno modelį** ir tuomet pasirinkite **Klausimyno ataskaitą**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-841">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="7dab4-842">**Versijos** „FastTab“, pasirinkite konfigūravimo versiją, kuri turi statusą **Juodraštis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-842">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="7dab4-843">Pasirinkite **Keisti statusą** \> **Užbaigtas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-843">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="7dab4-844">Šios konfigūracijos versijos 1.1 statusas yra keičiamas iš **Juodraštis** į **Užbaigtas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-844">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="7dab4-845">Versija 1.1 nebegali būti keičiama.</span><span class="sxs-lookup"><span data-stu-id="7dab4-845">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="7dab4-846">Šioje versijoje yra konfigūruotas formatas ir gali būti naudojamas jūsų tinkintos ataskaitos spausdinimui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-846">This version contains the configured format and can be used to print your custom report.</span></span> <span data-ttu-id="7dab4-847">Šios konfigūracijos versija 1.2 yra sukurta ir turi **Juodraštis** statusą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-847">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="7dab4-848">Galite redaguoti šią versiją tam, kad keistumėte jūsų ataskaitos **Klausimyno** formatą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-848">You can edit this version to adjust the format of your **Questionnaire** report.</span></span>

![Redaguojamos ER konfigūracijos versijos redagavimas puslapyje](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> <span data-ttu-id="7dab4-850">Konfigūruotas formatas yra jūsų suprojektuota  **Klausimyno** ataskaita ir neturi jokių sąsajų su finansų artefaktais.</span><span class="sxs-lookup"><span data-stu-id="7dab4-850">The configured format is your design of the **Questionnaire** report and contains no relations to the Finance-specific artefacts.</span></span>

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a><span data-ttu-id="7dab4-851">Vystykite programos artefaktus tam, kad iškviestumėte suprojektuotą ataskaitą</span><span class="sxs-lookup"><span data-stu-id="7dab4-851">Develop application artefacts to call the designed report</span></span>

<span data-ttu-id="7dab4-852">Kaip vartotojas sistemos administratoriaus vaidmenyje, privalote vystyti naują logiką taip, kad konfigūruotas ER formatas galėtų būti iškviestas programos vartotojo sąsajos (UI) siekiant sukurti jūsų tinkintą ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-852">As a user in the System Administrator role, you must develop new logic so that the configured ER format can be called from the application user interface (UI) to generate your custom report.</span></span> <span data-ttu-id="7dab4-853">Šiuo metu, ER nesiūlo jokių galimybių konfigūruoti tokio tipo logikos.</span><span class="sxs-lookup"><span data-stu-id="7dab4-853">Currently, ER doesn't offer any capability for configuring this type of logic.</span></span> <span data-ttu-id="7dab4-854">Dėl to, reikalingas nedidelis inžinerinis darbas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-854">Therefore, some engineering work is required.</span></span> 

<span data-ttu-id="7dab4-855">Naujos logikos sukūrimui, privalote talpinti topologiją, galinčią palaikyti nuolatinį kūrimą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-855">To develop the new logic, you must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="7dab4-856">Daugiau informacijos žr. [Visuotinis topologijų, palaikančių nuolatinio komponavimo versijų ir testavimo automatizavimo funkciją, diegimas](../perf-test/continuous-build-test-automation.md).</span><span class="sxs-lookup"><span data-stu-id="7dab4-856">For more information, see [Deploy topologies that support continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span> <span data-ttu-id="7dab4-857">Taip pat jums reikia prieigos prie šios topologijos kūrimo aplinkos.</span><span class="sxs-lookup"><span data-stu-id="7dab4-857">You must also have access to the development environment for this topology.</span></span> <span data-ttu-id="7dab4-858">Dėl platesnės informacijos apie prieinamus ER API, žr. [ER darbotvarkės API](er-apis-app73.md).</span><span class="sxs-lookup"><span data-stu-id="7dab4-858">For more information about the available ER API, see [ER framework API](er-apis-app73.md).</span></span>

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a><span data-ttu-id="7dab4-859">Šaltinio kodo modifikavimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-859">Modify source code</span></span>

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a><span data-ttu-id="7dab4-860">Įtraukite duomenų sutarties klasę</span><span class="sxs-lookup"><span data-stu-id="7dab4-860">Add a data contract class</span></span>

<span data-ttu-id="7dab4-861">Įtraukite naują **KlausimynoERataskaitossutarties** klasę į savo „Microsoft Visual Studio“ projektą ir parašykite kodą, kuris nurodo duomenų sutartį, naudotiną konfigūruoto ER formato vykdymui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-861">Add the new **QuestionnairesErReportContract** class to your Microsoft Visual Studio project, and write code that specifies the data contract that should be used to run the configured ER format.</span></span>

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a><span data-ttu-id="7dab4-862">Įtraukite UI kūrėjo klasę</span><span class="sxs-lookup"><span data-stu-id="7dab4-862">Add a UI builder class</span></span>

<span data-ttu-id="7dab4-863">Įtraukite naują **KlausimynoERAtaskaitosUIkūrėjo** klasę į savo „Microsoft Visual Studio“ projektą ir parašykite kodą, kuriuo bus sukuriamas vykdymo laiko teksto laukelis naudojamas būtino vykdyti ER formato ieškojimo žemėlapio ID.</span><span class="sxs-lookup"><span data-stu-id="7dab4-863">Add the new **QuestionnairesErReportUIBuilder** class to your Visual Studio project, and write code to generate a runtime dialog box that will be used to look up the format mapping ID of the ER format that must be run.</span></span> <span data-ttu-id="7dab4-864">Pateiktas kodas ieško tik ER formatų, kurie gali turėti duomenų šaltinį **Duomenų modelio** tipo, kuris nurodo į **[Klausimynus](#DataModeName)** duomenų modelį naudojant **[Šaknies](#RootDefinitionName)** sąvoką.</span><span class="sxs-lookup"><span data-stu-id="7dab4-864">The provided code looks up only ER formats that contain a data source of the **Data model** type that refers to the **[Questionnaires](#DataModeName)** data model by using the **[Root](#RootDefinitionName)** definition.</span></span>

> [!NOTE]
> <span data-ttu-id="7dab4-865">Kitu atveju, galite naudoti ER integravimo taškus siekiant filtruoti ER formatus.</span><span class="sxs-lookup"><span data-stu-id="7dab4-865">Alternatively, you can use ER integration points to filter ER formats.</span></span> <span data-ttu-id="7dab4-866">Dėl išsamesnės informacijos, žr. [API formato žemėlapio paieškos rodymui](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span><span class="sxs-lookup"><span data-stu-id="7dab4-866">For more information, see [API to show a format mapping lookup](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span></span>

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a><span data-ttu-id="7dab4-867">Įtraukite duomenų tiekėjo klasę</span><span class="sxs-lookup"><span data-stu-id="7dab4-867">Add a data provider class</span></span>

<span data-ttu-id="7dab4-868">Įtraukite naują **KlausimynoErAtaskaitosDP** klasę į savo „Microsoft Visual Studio“ projektą ir parašykite kodą, kuris pateikia duomenų tiekėją, naudotiną konfigūruoto ER formato vykdymui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-868">Add the new **QuestionnairesErReportDP** class to your Visual Studio project, and write code that introduces the data provider that should used to run the configured ER format.</span></span> <span data-ttu-id="7dab4-869">Pateiktas kodas apima tik šio duomenų tiekėjo sutarties duomenis.</span><span class="sxs-lookup"><span data-stu-id="7dab4-869">The provided code includes only the data contract for this data provider.</span></span>

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a><span data-ttu-id="7dab4-870">Įtraukite žymių failą</span><span class="sxs-lookup"><span data-stu-id="7dab4-870">Add a labels file</span></span>

<span data-ttu-id="7dab4-871">Įtraukite naujas **QuestionnairesErReportLabels\_en-US** žymių failą savo „Visual Studio“ projektui ir nurodykite tolesnes žymes naujiems UI šaltiniams:</span><span class="sxs-lookup"><span data-stu-id="7dab4-871">Add the new **QuestionnairesErReportLabels\_en-US** labels file to your Visual Studio project, and specify the following labels for new UI resources:</span></span>

- <span data-ttu-id="7dab4-872">**\@KlausimynoAtaskaita** žymė naujam meniu elementui, turinčiam tolesnį tekstą JAV anglų k. (en-US): **Klausimyno ataskaita (įjungta ER)**</span><span class="sxs-lookup"><span data-stu-id="7dab4-872">The **\@QuestionnairesReport** label for a new menu item that contains the following text in US English (en-US): **Questionnaires report (powered by ER)**</span></span>
- <span data-ttu-id="7dab4-873">**\@QuestionnairesReportBatchJobDescription** žymė paketo darbo pavadinimui, jei pasirinktas ER formatas yra nustatytas paketo darbo vykdymui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-873">The **\@QuestionnairesReportBatchJobDescription** label for a batch job title if a selected ER format is scheduled for execution as a batch job</span></span>

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a><span data-ttu-id="7dab4-874">Įtraukite ataskaitos paslaugos klasę</span><span class="sxs-lookup"><span data-stu-id="7dab4-874">Add a report service class</span></span>

<span data-ttu-id="7dab4-875">Įtraukite naują **KlausimynoERAtaskaitosPaslaugų** klasę į savo „Microsoft Visual Studio“ projektą ir parašykite kodą, kuris iškviečia ER formatą, atpažįsta jį formatuodamas žemėlapio ID ir pateikia duomenų sutartį kaip parametrą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-875">Add the new **QuestionnairesErReportService** class to your Visual Studio project, and write code that calls an ER format, identifies it by a format mapping ID, and provides a data contract as a parameter.</span></span>

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

<span data-ttu-id="7dab4-876">Kai turite naudoti ER formatą vykdantį programos duomenis, privalote konfigūruoti duomenų šaltinį **Duomenų modelio** tipe formato žemėlapyje.</span><span class="sxs-lookup"><span data-stu-id="7dab4-876">When you must use an ER format that runs application data, you must configure a data source of the **Data model** type in the format mapping.</span></span> <span data-ttu-id="7dab4-877">Šis duomenų šaltinis rodo į konkrečią konkrečių duomenų modelio dalį naudodamas vienos šaknies sąvoką.</span><span class="sxs-lookup"><span data-stu-id="7dab4-877">This data source refers to a specific part of the specified data model by using a single root definition.</span></span> <span data-ttu-id="7dab4-878">Kai ER formatas yra vykdomas, jis iškviečia duomenų šaltinį prieigai prie tinkamo ER modelio žemėlapio, kuris yra konfigūruotas pagal esamą modelį ir šaknies sąvoką.</span><span class="sxs-lookup"><span data-stu-id="7dab4-878">When the ER format is run, it calls this data source to access the appropriate ER model mapping that is configured for a given model and root definition.</span></span>

<span data-ttu-id="7dab4-879">Visa informacija, kurią jums gali reikėti parengti šaltinio kode yra laikyti kaip duomenų sutarties dalį, gali būti pakeista vykdant ER formatą ir naudojant šio tipo ER modelio žemėlapį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-879">All the information that you might prepare in the source code and store as part of the data contract can be passed to the running ER format by using an ER model mapping of this type.</span></span> <span data-ttu-id="7dab4-880">ER modelio žemėlapio kūrime, turite konfigūruoti **Objekto** tipo duomenų šaltinį, kuris rodo į **[KlausimynoErAtaskaitosSutarties](#DataContractClass)** klasę.</span><span class="sxs-lookup"><span data-stu-id="7dab4-880">In the ER model mapping, you must configure a data source of the **Object** type that refers to the **[QuestionnairesErReportContract](#DataContractClass)** class.</span></span> <span data-ttu-id="7dab4-881">Siekiant atpažinti modelio žemėlapį, turite nurodyti duomenų šaltinį, kuris iškviečia modelio žemėlapį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-881">To identify a model mapping, you must specify a data source that calls this model mapping.</span></span> <span data-ttu-id="7dab4-882">Pateiktame kode, šis duomenų šaltinis nurodytas **ERmodelioduomenųšaltiniopavadinimas** konstantoje turi **[modelio](#ModelDSName)** vertę.</span><span class="sxs-lookup"><span data-stu-id="7dab4-882">In the provided code, this data source specified by the **ERModelDataSourceName** constant that has the **[model](#ModelDSName)** value.</span></span> <span data-ttu-id="7dab4-883">Siekiant atpažinti, kuris duomenų šaltinis yra naudojamas duomenų sutarties rodymui modelio žemėlapyje, turite nurodyti duomenų šaltinio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-883">To identify which data source is used to expose the data contract in the model mapping, you must specify a data source name.</span></span> <span data-ttu-id="7dab4-884">Pateiktame kode, šis pavadinimas yra nurodytas **ParametrųDuomenųŠaltinioPavadinimas** konstantoje, kuri turi <a name="DataContractDSName"></a>**VykdomoLaikoParametrų** vertę.</span><span class="sxs-lookup"><span data-stu-id="7dab4-884">In the provided code, this name is specified by the **ParametersDataSourceName** constant that has <a name="DataContractDSName"></a>**RunTimeParameters** value.</span></span>

> [!NOTE]
> <span data-ttu-id="7dab4-885">Naujoje aplinkoje, jums gali reikėti atnaujinti ER metaduomenis taip, kad šis klasės tipas būtų prieinamas ER modelio žemėlapio kūrimo įrankyje.</span><span class="sxs-lookup"><span data-stu-id="7dab4-885">In a new environment, you might have to refresh the ER metadata so that this type of class is available in the ER model mapping designer.</span></span> <span data-ttu-id="7dab4-886">Dėl platesnės informacijos, žr. [Konfigūruoti ER darbotvarkę](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="7dab4-886">For more information, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span></span>

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a><span data-ttu-id="7dab4-887">Įtraukite ataskaitos valdiklio klasę</span><span class="sxs-lookup"><span data-stu-id="7dab4-887">Add a report controller class</span></span>

<span data-ttu-id="7dab4-888">Įtraukite naują **QuestionnairesErReportController** klasę savo „Visual Studio“ projektui ir parašykite kodą, kuris vykdo ER formatą sinchroniniu būdu ar paketo būdu, kaip jums patogu, teksto laukelyje, kuris yra sukurtas pagal logiką pateiktą **QuestionnairesErReportUIBuilder** klasėje.</span><span class="sxs-lookup"><span data-stu-id="7dab4-888">Add the new **QuestionnairesErReportController** class to your Visual Studio project, and write code that runs an ER format in either synchronous mode or batch mode, as you prefer, in the dialog box that is built based on the logic of the provided **QuestionnairesErReportUIBuilder** class.</span></span>

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a><span data-ttu-id="7dab4-889">Įtraukite meniu elementą</span><span class="sxs-lookup"><span data-stu-id="7dab4-889">Add a menu item</span></span>

<span data-ttu-id="7dab4-890">Įtraukite naują **QuestionnairesErReport** meniu elementą į savo „Visual Studio“ projektą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-890">Add the new **QuestionnairesErReport** menu item to your Visual Studio project.</span></span> <span data-ttu-id="7dab4-891">**Objekto** ypatybėse, šis meniu rodo į **QuestionnairesErReportController** klasę ir yra naudojamas nurodyti vartotojo teises pasirinkti ir vykdyti ER formatą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-891">In the **Object** property, this menu item refers to the **QuestionnairesErReportController** class, and it's used to specify a user permission to select and run an ER format.</span></span> <span data-ttu-id="7dab4-892">**Žymės** ypatybėse, šis meniu elementas rodo **\@QuestionnairesReport** žymę, kurią sukūrėte anksčiau, todėl teisingas tekstas yra rodomas UI programoje.</span><span class="sxs-lookup"><span data-stu-id="7dab4-892">In the **Label** property, this menu item refers to the **\@QuestionnairesReport** label that you created earlier, so that correct text is presented in the application UI.</span></span>

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a><span data-ttu-id="7dab4-893">Įtraukite meniu elementą į meniu</span><span class="sxs-lookup"><span data-stu-id="7dab4-893">Add a menu item to a menu</span></span>

<span data-ttu-id="7dab4-894">Įtraukite esantį **KM** meniu elementą į savo „Visual Studio“ projektą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-894">Add the existing **KM** menu to your Visual Studio project.</span></span> <span data-ttu-id="7dab4-895">Įtraukite naują **QuestionnairesErReport** elementą **Išorės** tipe šiame meniu.</span><span class="sxs-lookup"><span data-stu-id="7dab4-895">You must add a new **QuestionnairesErReport** item of the **Output** type to this menu.</span></span> <span data-ttu-id="7dab4-896">Šis elementas turi rodyti **QuestionnairesErReport** meniu elementą, kuris yra aprašytas ankstesniame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="7dab4-896">This item must refer to the **QuestionnairesErReport** menu item that is described in the previous section.</span></span>

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a><span data-ttu-id="7dab4-897">Sukurkite „Visual Studio“ projektą</span><span class="sxs-lookup"><span data-stu-id="7dab4-897">Build a Visual Studio project</span></span>

<span data-ttu-id="7dab4-898">Sukurkite savo projektą tam, kad padarytumėte naują meniu elementą prieinamą vartotojams.</span><span class="sxs-lookup"><span data-stu-id="7dab4-898">Build your project to make a new menu item available to users.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a><span data-ttu-id="7dab4-899">Vykdykite formatą iš programos</span><span class="sxs-lookup"><span data-stu-id="7dab4-899">Run a format from the application</span></span>

1. <span data-ttu-id="7dab4-900">Eikite į **Klausimynas** \> **Projektavimas** \> **Klausimynų ataskaita (vykdoma ER)**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-900">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>

    ![Pasirinkite klausimyno ataskaitą (vykdoma ER) meniu elementą klausimyno modulyje tam, kad vykdytumėte konfigūruotą ER formatą](./media/er-quick-start1-application-menu-modified.png)

2. <span data-ttu-id="7dab4-902">Iškrentančiame teksto laukelyje, **Formato žemėlapis** laukelyje, pasirinkite **Klausimynų ataskaita**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-902">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="7dab4-903">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-903">Select **OK**.</span></span>
4. <span data-ttu-id="7dab4-904">**Elektroninės ataskaitos parametrai** teksto laukelyje, **Apimami įrašai** „FastTab“, konfigūruokite filtravimo parinktis taip, kad tik **SBCCrsExam** klausimynas būtų įtrauktas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-904">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="7dab4-905">Pasirinkite **Gerai** filtravimo parinkties patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-905">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="7dab4-906">Pasirinkite **Gerai** ataskaitos vykdymui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-906">Select **OK** to run the report.</span></span>

    ![Atrankos kriterijų nurodymas elektroninės ataskaitos teksto laukelyje](./media/er-quick-start1-report-run-dialog-page.png)

7. <span data-ttu-id="7dab4-908">Peržiūrėkite sukurtą ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-908">Review the generated report.</span></span>

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a><span data-ttu-id="7dab4-909">Suderinkite suprojektuotą ER sprendimą</span><span class="sxs-lookup"><span data-stu-id="7dab4-909">Tune a designed ER solution</span></span>

<span data-ttu-id="7dab4-910">Galite keisti konfigūruotą ER sprendimą taip, kad jis naudotų duomenis pateiktus klasėje, kuriuos sukūrėte prieigai prie ER formato vykdymo išsamios informacijos ir taip, kad jis įvestų šio ER formato pavadinimą sukurtoje ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="7dab4-910">You can modify the configured ER solution so that it uses the data provider class that you developed to access details of the running ER format, and so that it enters the name of this ER format in a generated report.</span></span>

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a><span data-ttu-id="7dab4-911">Keiskite modelio žemėlapį</span><span class="sxs-lookup"><span data-stu-id="7dab4-911">Modify a model mapping</span></span>

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a><span data-ttu-id="7dab4-912">Įtraukite duomenų šaltinį prieigai prie duomenų sutarties objekto</span><span class="sxs-lookup"><span data-stu-id="7dab4-912">Add data sources to access a data contract object</span></span>

1. <span data-ttu-id="7dab4-913">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-913">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7dab4-914">**Konfigūravimai** puslapyje, konfigūravimo medyje, išplėskite **Klausimyno modelį** ir tuomet pasirinkite **Klausimyno žemėlapis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-914">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="7dab4-915">Pasirinkit **Kūrimo įrankį** tam, kad atvertumėte **Modelis į duomenų šaltinio žemėlapio** puslapį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-915">Select **Designer** to open the **Model to datasource mapping** page.</span></span>
4. <span data-ttu-id="7dab4-916">Pasirinkite **Kūrimo įrankį** tam, kad atvertumėte žemėlapį modelio žemėlapio kūrimo įrankyje.</span><span class="sxs-lookup"><span data-stu-id="7dab4-916">Select **Designer** to open the selected mapping in the model mapping designer.</span></span>
5. <span data-ttu-id="7dab4-917">**Modelio žemėlapio kūrimo įrankis** puslapyje, **Duomenų šaltinio tipai** juostoje, pasirinkite **Dynamics 365 for Operations\\Objektas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-917">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Object**.</span></span>
6. <span data-ttu-id="7dab4-918">**Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-918">In the **Data sources** pane, select **Add root**.</span></span>
7. <span data-ttu-id="7dab4-919">Teksto laukelyje, **Pavadinimas** laukelyje įveskite **[RunTimeParameters](#DataContractDSName)**, kaip nurodytą šaltinio **QuestionnairesErReportService** klasės kodą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-919">In the dialog box, in the **Name** field, enter **[RunTimeParameters](#DataContractDSName)**, as defined in the source code of the **QuestionnairesErReportService** class.</span></span>
8. <span data-ttu-id="7dab4-920">**Klasės** laukelyje įveskite **[QuestionnairesErReportContract](#DataContractClass)**, kuris buvo užkoduotas anksčiau.</span><span class="sxs-lookup"><span data-stu-id="7dab4-920">In the **Class** field, enter **[QuestionnairesErReportContract](#DataContractClass)**, which was coded earlier.</span></span>
9. <span data-ttu-id="7dab4-921">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-921">Select **OK**.</span></span>
10. <span data-ttu-id="7dab4-922">Išplėskite **VykdymoLaikoParametrus**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-922">Expand **RunTimeParameters**.</span></span>

<span data-ttu-id="7dab4-923">Įtrauktas duomenų šaltinis pateikia informaciją apie vykdomo ER formato žemėlapio įrašo ID.</span><span class="sxs-lookup"><span data-stu-id="7dab4-923">The added data source provides information about the record ID of the running ER format mapping.</span></span>

![Įtrauktas duomenų šaltinis ER modelio žemėlapio kūrimo įrankyje](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a><span data-ttu-id="7dab4-925">Įtraukite duomenų šaltinį prieigai prie ER formato žemėlapio įrašų</span><span class="sxs-lookup"><span data-stu-id="7dab4-925">Add a data source to access ER format mapping records</span></span>

<span data-ttu-id="7dab4-926">Tęskite pasirinkto modelio žemėlapio redagavimą įtraukdami duomenų šaltinį prieigai prie ER formato žemėlapio įrašų.</span><span class="sxs-lookup"><span data-stu-id="7dab4-926">Continue to edit the selected model mapping by adding a data source to access ER format mapping records.</span></span>

1. <span data-ttu-id="7dab4-927">**Modelio žemėlapio kūrimo įrankis** puslapyje, **Duomenų šaltinio tipai** juostoje, pasirinkite **Dynamics 365 for Operations\\Lentelės įrašai**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-927">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="7dab4-928">**Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-928">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="7dab4-929">Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **ER1**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-929">In the dialog box, in the **Name** field, enter **ER1**.</span></span>
4. <span data-ttu-id="7dab4-930">**Lentelė** laukelyje, įveskite **ERFormatMappingTable**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-930">In the **Table** field, enter **ERFormatMappingTable**.</span></span>
5. <span data-ttu-id="7dab4-931">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-931">Select **OK**.</span></span>

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a><span data-ttu-id="7dab4-932">Įtraukti duomenų šaltinį prieigai prie formato žemėlapio ER formato įrašo vykdymo</span><span class="sxs-lookup"><span data-stu-id="7dab4-932">Add a data source to access a format mapping record of a running ER format</span></span>

<span data-ttu-id="7dab4-933">Tęskite pasirinkto modelio žemėlapio redagavimą įtraukdami duomenų šaltinį prieigai prie formato žemėlapio ER formato vykdymo įrašo.</span><span class="sxs-lookup"><span data-stu-id="7dab4-933">Continue to edit the selected model mapping by adding a data source to access the format mapping record of the running ER format.</span></span>

1. <span data-ttu-id="7dab4-934">**Modelio žemėlapio kūrimo įrankio** puslapyje, **Duomenų šaltinio tipai** juostoje pasirinkite **Funkcijos\\Apskaičiuotas laukelis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-934">On the **Model mapping designer** page, in the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
2. <span data-ttu-id="7dab4-935">**Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-935">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="7dab4-936">Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **ER2**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-936">In the dialog box, in the **Name** field, enter **ER2**.</span></span>
4. <span data-ttu-id="7dab4-937">Pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-937">Select **Edit formula**.</span></span>
5. <span data-ttu-id="7dab4-938">Formulės redaktoriuje **Formulės** laukelyje įveskite **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-938">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span></span>
6. <span data-ttu-id="7dab4-939">Pasirinkite **Įrašyti** ir uždarykite formulės redaktorių.</span><span class="sxs-lookup"><span data-stu-id="7dab4-939">Select **Save**, and close the formula editor.</span></span>
7. <span data-ttu-id="7dab4-940">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-940">Select **OK**.</span></span>

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a><span data-ttu-id="7dab4-941">Įveskite vykdomo ER formato pavadinimą duomenų modelyje</span><span class="sxs-lookup"><span data-stu-id="7dab4-941">Enter the name of the running ER format in the data model</span></span>

<span data-ttu-id="7dab4-942">Tęskite pasirinkto modelio žemėlapio redagavimą taip, kad ER formato vykdymo pavadinimas būtų įvestas į duomenų modelį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-942">Continue to edit the selected model mapping so that the name of the running ER format is entered in the data model.</span></span>

1. <span data-ttu-id="7dab4-943">**Modelio žemėlapio kūrimo įrankis** puslapyje, **Duomenų modelis** juostoje išplėskite **ExecutionContext** ir tuomet pasirinkite **ExecutionContext\\FormatName**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-943">On the **Model mapping designer** page, in the **Data model** pane, expand **ExecutionContext**, and then select **ExecutionContext\\FormatName**.</span></span>
2. <span data-ttu-id="7dab4-944">**Duomenų modelis** juostoje pasirinkite **Redaguoti** tam, kad konfigūruotumėte duomenų susiejimą pasirinkto duomenų modelio laukeliui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-944">In the **Data model** pane, select **Edit** to configure a data binding for the selected data model's field.</span></span>
3. <span data-ttu-id="7dab4-945">Formulės redaktoriuje **Formulės** laukelyje įveskite **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-945">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span></span>
4. <span data-ttu-id="7dab4-946">Pasirinkite **Įrašyti** ir uždarykite formulės redaktorių.</span><span class="sxs-lookup"><span data-stu-id="7dab4-946">Select **Save**, and close the formula editor.</span></span>

<span data-ttu-id="7dab4-947">Kadangi naudojote **FormatName** laukelį, konfigūruotas modelio žemėlapis dabar rodo ER formato pavadinimą, kuri iškviečia modelio žemėlapį vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="7dab4-947">Because you used the **FormatName** field, the configured model mapping now exposes the name of an ER format that calls this model mapping during execution.</span></span>

![Duomenų modelio laukelio susiejimas su įtrauktu duomenų šaltinio metodu ER modelio žemėlapio kūrimo įrankyje](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a><span data-ttu-id="7dab4-949">Užbaikite modelio žemėlapio dizainą</span><span class="sxs-lookup"><span data-stu-id="7dab4-949">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="7dab4-950">**Modelio žemėlapio kūrimo įrankis** puslapyje, pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-950">On the **Model mapping designer** page, select **Save**.</span></span>
2. <span data-ttu-id="7dab4-951">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-951">Close the page.</span></span>
3. <span data-ttu-id="7dab4-952">Uždarykite modelio žemėlapio puslapį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-952">Close the model mappings page.</span></span>
4. <span data-ttu-id="7dab4-953">**Konfigūravimai** puslapyje, konfigūravimo medyje, įsitikinkite, kad **Klausimyno žemėlapio** konfigūravimas vis dar pasirinktas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-953">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire mapping** configuration is still selected.</span></span> <span data-ttu-id="7dab4-954">Tuomet, **Versijos** „FastTab“, pasirinkite konfigūravimo versiją, kuri turi statusą **Juodraštis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-954">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
5. <span data-ttu-id="7dab4-955">Pasirinkite **Keisti statusą** \> **Užbaigtas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-955">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="7dab4-956">Šios konfigūracijos versijos 1.2 statusas yra keičiamas iš **Juodraštis** į **Užbaigtas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-956">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="7dab4-957">Versija 1.2 nebegali būti keičiama.</span><span class="sxs-lookup"><span data-stu-id="7dab4-957">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="7dab4-958">Šioje versijoje yra konfigūruotų žemėlapio modelis ir gali būti naudojamas pagal kitas ER konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-958">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="7dab4-959">Šios konfigūracijos versija 1.3 yra sukurta ir turi **Juodraštis** statusą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-959">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="7dab4-960">Galite redaguoti šią versiją tam, kad keistumėte **Klausimyno** žemėlapio modelį.</span><span class="sxs-lookup"><span data-stu-id="7dab4-960">You can edit this version to adjust the **Questionnaire** model mapping.</span></span>

### <a name="modify-a-format"></a><a name="ModifyFormat"></a><span data-ttu-id="7dab4-961">Keisti formatą</span><span class="sxs-lookup"><span data-stu-id="7dab4-961">Modify a format</span></span>

<span data-ttu-id="7dab4-962">Galite keisti konfigūruotą ER formatą taip, kad jo pavadinimas būtų rodomas ataskaitos poraštėje, kuri yra sukurta vykdant ER formatą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-962">You can modify the configured ER format so that its name is shown in the footer of a report that is generated when the ER format is run.</span></span>

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a><span data-ttu-id="7dab4-963">Įkelkite naują formato elementą</span><span class="sxs-lookup"><span data-stu-id="7dab4-963">Add a new format element</span></span>

1. <span data-ttu-id="7dab4-964">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-964">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7dab4-965">**Konfigūravimai** puslapyje, konfigūravimo medyje, išplėskite **Klausimyno modelį** ir tuomet pasirinkite **Klausimyno ataskaitą**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-965">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="7dab4-966">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-966">Select **Designer**.</span></span>
4. <span data-ttu-id="7dab4-967">**Formato kūrimo įrankio** puslapyje, formato medyje pasirinkite **„Ataskaita“** šaknies elementą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-967">On the **Format designer** page, select the **Report** root item.</span></span>
5. <span data-ttu-id="7dab4-968">Pasirinkite **Įtraukti** tam, kad įtrauktumėte lizdo formato elementą pasirinktam **Ataskaitos** šaknies elementui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-968">Select **Add** to add a new nested format element for the selected **Report** root item.</span></span>
6. <span data-ttu-id="7dab4-969">Pasirinkite **Excel\\Poraštė**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-969">Select **Excel\\Footer**.</span></span>
7. <span data-ttu-id="7dab4-970">**Pavadinimas** laukelyje, įveskite **Poraštė**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-970">In the **Name** field, enter **Footer**.</span></span>
8. <span data-ttu-id="7dab4-971">Pasirinkite **Šaknis\Poraštė** ir tuomet pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-971">Select **Report\Footer**, and then select **Add**.</span></span>
9. <span data-ttu-id="7dab4-972">Pasirinkite **Tekstas\\Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-972">Select **Text\\String**.</span></span>

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a><span data-ttu-id="7dab4-973">Susiekite įkeltą formato elementą</span><span class="sxs-lookup"><span data-stu-id="7dab4-973">Bind the added format element</span></span>

1. <span data-ttu-id="7dab4-974">**Formato kūrimo** puslapyje,**Žemėlapio** skirtuke, formato medyje, įjungtame **Poraštės\\Eilutės** elemente, pasirinkite **Redaguoti formulę**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-974">On the **Format designer** page, on the **Mapping** tab, in the format tree, for the active **Footer\\String** element, select **Edit formula**.</span></span>
2. <span data-ttu-id="7dab4-975">Formulės redaktoriaus laukelyje **Formulė** įveskite **CONCATENATE ("\&C\&10", FORMAT("Sukurta'\%1' ER sprendimas", model.ExecutionContext.FormatName))**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-975">In the formula editor, in the **Formula** field, enter **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span></span>
3. <span data-ttu-id="7dab4-976">Pasirinkite **Įrašyti** ir uždarykite formulės redaktorių.</span><span class="sxs-lookup"><span data-stu-id="7dab4-976">Select **Save**, and close the formula editor.</span></span>
4. <span data-ttu-id="7dab4-977">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-977">Select **Save**.</span></span>

<span data-ttu-id="7dab4-978">Konfigūruotas formatas dabar buvo pakeistas taip, kad jo pavadinimas bus įvestas sukurtos ataskaitos poraštėje naudojant **Poraštės\\Eilutės** elementą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-978">The configured format has now been modified so that its name will be entered in the footer of a generated report by using the **Footer\\String** element.</span></span>

![Poraštės formato elemento įtraukimas į konfigūruotą formatą ER veiksmo kūrimo įrankyje](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a><span data-ttu-id="7dab4-980">Užbaikite formato projektavimą</span><span class="sxs-lookup"><span data-stu-id="7dab4-980">Complete the format design</span></span>

1. <span data-ttu-id="7dab4-981">Uždarykite puslapį **Formato dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-981">Close the **Format designer** page.</span></span>
2. <span data-ttu-id="7dab4-982">**Konfigūravimai** puslapyje, konfigūravimo medyje, įsitikinkite, kad **Klausimyno ataskaita** konfigūravimas vis dar pasirinktas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-982">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire report** configuration is still selected.</span></span> <span data-ttu-id="7dab4-983">Tuomet, **Versijos** „FastTab“, pasirinkite konfigūravimo versiją, kuri turi statusą **Juodraštis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-983">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
3. <span data-ttu-id="7dab4-984">Pasirinkite **Keisti statusą** \> **Užbaigtas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-984">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="7dab4-985">Šios konfigūracijos versijos 1.2 statusas yra keičiamas iš **Juodraštis** į **Užbaigtas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-985">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="7dab4-986">Versija 1.2 nebegali būti keičiama.</span><span class="sxs-lookup"><span data-stu-id="7dab4-986">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="7dab4-987">Šioje versijoje yra konfigūruotų formatas ir gali būti naudojamas pagal kitas ER konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-987">This version contains the configured format and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="7dab4-988">Šios konfigūracijos versija 1.3 yra sukurta ir turi **Juodraštis** statusą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-988">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="7dab4-989">Galite redaguoti šią versiją tam, kad keistumėte **Klausimyno** ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-989">You can edit this version to adjust the **Questionnaire** report.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a><span data-ttu-id="7dab4-990">Vykdykite formatą iš programos</span><span class="sxs-lookup"><span data-stu-id="7dab4-990">Run a format from the application</span></span>

1. <span data-ttu-id="7dab4-991">Eikite į **Klausimynas** \> **Projektavimas** \> **Klausimynų ataskaita (vykdoma ER)**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-991">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="7dab4-992">Iškrentančiame teksto laukelyje, **Formato žemėlapis** laukelyje, pasirinkite **Klausimynų ataskaita**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-992">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="7dab4-993">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-993">Select **OK**.</span></span>
4. <span data-ttu-id="7dab4-994">**ER parametrai** teksto laukelyje, **Apimami įrašai** „FastTab“, konfigūruokite filtravimo parinktis taip, kad tik **SBCCrsExam** klausimynas būtų įtrauktas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-994">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="7dab4-995">Pasirinkite **Gerai** filtravimo parinkties patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-995">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="7dab4-996">Pasirinkite **Gerai** ataskaitos vykdymui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-996">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="7dab4-997">Peržiūrėkite sukurtą ataskaitą „Excel“ formatu.</span><span class="sxs-lookup"><span data-stu-id="7dab4-997">Review the generated report in Excel format.</span></span>

<span data-ttu-id="7dab4-998">Atkreipkite dėmesį, kad sukurtos ataskaitos poraštė turi ER formato pavadinimą, kuris yra naudojamas jos sukūrimui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-998">Notice that the footer of the generated report contains the name of the ER format that was used to generate it.</span></span>

![Sukurta ataskaita „Excel“ formatu](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a><span data-ttu-id="7dab4-1000">Vykdykite formatą iš ER</span><span class="sxs-lookup"><span data-stu-id="7dab4-1000">Run a format from ER</span></span>

1. <span data-ttu-id="7dab4-1001">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-1001">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7dab4-1002">**Konfigūravimai** puslapyje, konfigūravimo medyje, išplėskite **Klausimyno modelį** ir tuomet pasirinkite **Klausimyno ataskaitą**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-1002">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="7dab4-1003">Veiksmų srityje pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-1003">On the Action Pane, select **Run**.</span></span>
4. <span data-ttu-id="7dab4-1004">**Elektroninės ataskaitos parametrai** teksto laukelyje, **Apimami įrašai** „FastTab“, konfigūruokite filtravimo parinktis taip, kad tik **SBCCrsExam** klausimynas būtų įtrauktas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-1004">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="7dab4-1005">Pasirinkite **Gerai** filtravimo parinkties patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-1005">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="7dab4-1006">Pasirinkite **Gerai** ataskaitos vykdymui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-1006">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="7dab4-1007">Peržiūrėkite sukurtą ataskaitą „Excel“ formatu.</span><span class="sxs-lookup"><span data-stu-id="7dab4-1007">Review the generated report in Excel format.</span></span>

<span data-ttu-id="7dab4-1008">Atkreipkite dėmesį, kad sukurtos ataskaitos poraštė neturi ER formato pavadinimo, kuris buvo naudotas sukūrimui, nes duomenų sutarties objektas nebuvo perduotas vykdymo modelio žemėlapiui, kai jis buvo iškviestas ER formato vykdomo iš ER.</span><span class="sxs-lookup"><span data-stu-id="7dab4-1008">Notice that the footer of the generated report doesn't contain the name of ER format that was used to generate it, because the data contract object wasn't passed to the running model mapping when it was called by the ER format that was run from ER.</span></span>

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a><span data-ttu-id="7dab4-1009">Konfigūruokite formato paskirtį ekrane rodomoje peržiūroje</span><span class="sxs-lookup"><span data-stu-id="7dab4-1009">Configure a format destination for on-screen preview</span></span>

1. <span data-ttu-id="7dab4-1010">Eikite **Organizacijos administravimas** \> **Elektroninė ataskaita** \> **Elektroninės ataskaitos paskirtis**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-1010">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting destination**.</span></span>
2. <span data-ttu-id="7dab4-1011">**Elektroninės ataskaitos paskirties** puslapyje įtraukite įrašo paskirtį konfigūruotą **Klausimyno ataskaitos** ER formatą.</span><span class="sxs-lookup"><span data-stu-id="7dab4-1011">On the **Electronic reporting destination** page, add a destination record for the configured **Questionnaire report** ER format.</span></span>
3. <span data-ttu-id="7dab4-1012">**Failo paskirties** „FastTab“, nustatykite **Ekrano** [paskirtį](er-destination-type-screen.md) **Ataskaitos** formato komponentui, kuris buvo [įtrauktas](#AddFormatRootElement) kaip šaknies elementas konfigūruoto **Klausimyno ataskaitos** ER formato.</span><span class="sxs-lookup"><span data-stu-id="7dab4-1012">On the **File destination** FastTab, set up the **Screen** [destination](er-destination-type-screen.md) for the **Report** format component that has been [added](#AddFormatRootElement) as the root element of the configured **Questionnaire report** ER format.</span></span>
4. <span data-ttu-id="7dab4-1013">**PDF pakeitimo nustatymų** „FastTab“, konfigūruokite paskirties vietą pavertimui į ataskaitą [PDF formatu](electronic-reporting-destinations.md#OutputConversionToPDF), kuris naudoja **Kraštovaizdžio** puslapio orientaciją.</span><span class="sxs-lookup"><span data-stu-id="7dab4-1013">On the **PDF conversion settings** FastTab, configure the destination to convert a report to [PDF format](electronic-reporting-destinations.md#OutputConversionToPDF) that uses the **Landscape** page orientation.</span></span>

![Tinkinto ekrano paskirties vietos konfigūravimas ER formatui elektroninės ataskaitos paskirties puslapyje](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a><span data-ttu-id="7dab4-1015">Vykdykite formatą iš programos tam, kad peržiūrėtumėte jį kaip PDF dokumentą</span><span class="sxs-lookup"><span data-stu-id="7dab4-1015">Run a format from the application to preview it as a PDF document</span></span>

1. <span data-ttu-id="7dab4-1016">Eikite į **Klausimynas** \> **Projektavimas** \> **Klausimynų ataskaita (vykdoma ER)**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-1016">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="7dab4-1017">Iškrentančiame teksto laukelyje, **Formato žemėlapis** laukelyje, pasirinkite **Klausimynų ataskaita**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-1017">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="7dab4-1018">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-1018">Select **OK**.</span></span>
4. <span data-ttu-id="7dab4-1019">**Elektroninės ataskaitos parametrai** teksto laukelyje, **Apimami įrašai** „FastTab“, konfigūruokite filtravimo parinktis taip, kad tik **SBCCrsExam** klausimynas būtų įtrauktas.</span><span class="sxs-lookup"><span data-stu-id="7dab4-1019">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="7dab4-1020">Pasirinkite **Gerai** filtravimo parinkties patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-1020">Select **OK** to confirm the filtering option.</span></span>

    <span data-ttu-id="7dab4-1021">**Paskirties vietos** „FastTab“, atkreipkite dėmesį, kad **Išorės** laukelis yra nustatytas į **Ekranas**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-1021">On the **Destinations** FastTab, notice that the **Output** field is set to **Screen**.</span></span> <span data-ttu-id="7dab4-1022">Jei norite keisti konfigūruotą paskirties vietą, pasirinkite **Keisti**.</span><span class="sxs-lookup"><span data-stu-id="7dab4-1022">If you want to change the configured destination, select **Change**.</span></span>

    ![ER ataskaitos vykdymo laiko teksto laukelis, kuriame galite keisti konfigūruotą paskirties vietą](./media/er-quick-start1-run-settings.png)

6. <span data-ttu-id="7dab4-1024">Pasirinkite **Gerai** ataskaitos vykdymui.</span><span class="sxs-lookup"><span data-stu-id="7dab4-1024">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="7dab4-1025">Peržiūrėkite sukurtą ataskaitą PDF formatu.</span><span class="sxs-lookup"><span data-stu-id="7dab4-1025">Review the generated report in PDF format.</span></span>

    ![Ekrane rodoma sukurtos ataskaitos PDF formatu peržiūra](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a><span data-ttu-id="7dab4-1027">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="7dab4-1027">Additional resources</span></span>

- [<span data-ttu-id="7dab4-1028">Elektroninių ataskaitų apžvalga</span><span class="sxs-lookup"><span data-stu-id="7dab4-1028">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="7dab4-1029">Elektroninių ataskaitų formulių kalba</span><span class="sxs-lookup"><span data-stu-id="7dab4-1029">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="7dab4-1030">Ataskaitų keliomis kalbomis kūrimas</span><span class="sxs-lookup"><span data-stu-id="7dab4-1030">Design multilingual reports</span></span>](er-design-multilingual-reports.md)
- [<span data-ttu-id="7dab4-1031">ER sistemos API</span><span class="sxs-lookup"><span data-stu-id="7dab4-1031">ER framework API</span></span>](er-apis-app73.md)
- [<span data-ttu-id="7dab4-1032">CASE funkcija</span><span class="sxs-lookup"><span data-stu-id="7dab4-1032">CASE function</span></span>](er-functions-logical-case.md)
- [<span data-ttu-id="7dab4-1033">CONCATENATE funkcija</span><span class="sxs-lookup"><span data-stu-id="7dab4-1033">CONCATENATE function</span></span>](er-functions-text-concatenate.md)
- [<span data-ttu-id="7dab4-1034">DATETIMEFORMAT funkcija</span><span class="sxs-lookup"><span data-stu-id="7dab4-1034">DATETIMEFORMAT function</span></span>](er-functions-datetime-datetimeformat.md)
- [<span data-ttu-id="7dab4-1035">FILTER funkcija</span><span class="sxs-lookup"><span data-stu-id="7dab4-1035">FILTER function</span></span>](er-functions-list-filter.md)
- [<span data-ttu-id="7dab4-1036">FIRSTORNULL funkcija</span><span class="sxs-lookup"><span data-stu-id="7dab4-1036">FIRSTORNULL function</span></span>](er-functions-list-firstornull.md)
- [<span data-ttu-id="7dab4-1037">FORMAT funkcija</span><span class="sxs-lookup"><span data-stu-id="7dab4-1037">FORMAT function</span></span>](er-functions-text-format.md)
- [<span data-ttu-id="7dab4-1038">IF funkcija</span><span class="sxs-lookup"><span data-stu-id="7dab4-1038">IF function</span></span>](er-functions-logical-if.md)
- [<span data-ttu-id="7dab4-1039">ORDERBY funkcija</span><span class="sxs-lookup"><span data-stu-id="7dab4-1039">ORDERBY function</span></span>](er-functions-list-orderby.md)
- [<span data-ttu-id="7dab4-1040">SESSIONNOW funkcija</span><span class="sxs-lookup"><span data-stu-id="7dab4-1040">SESSIONNOW function</span></span>](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
