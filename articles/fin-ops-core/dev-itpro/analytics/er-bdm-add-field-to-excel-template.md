---
title: Naujų laukų įtraukimas į verslo dokumento šabloną programoje „Microsoft Excel“
description: Šioje temoje pateikiama informacijos apie tai, kaip programoje „Microsoft Excel“ naudojant funkciją Verslo dokumentų valdymas į verslo dokumento šabloną įtraukti naujų laukų.
author: NickSelin
manager: AnnBe
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 8c3a905c90f5dd4ad3487f004a958c0dcd52115d
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893252"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a><span data-ttu-id="5ca61-103">Naujų laukų įtraukimas į verslo dokumento šabloną programoje „Microsoft Excel“</span><span class="sxs-lookup"><span data-stu-id="5ca61-103">Add new fields to a business document template in Microsoft Excel</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5ca61-104">Galite įtraukti naujų laukų į šabloną, kurį naudojant generuojami verslo dokumentai „Microsoft Excel“ formatu.</span><span class="sxs-lookup"><span data-stu-id="5ca61-104">You can add new fields to a template that is used to generate business documents in Microsoft Excel format.</span></span> <span data-ttu-id="5ca61-105">Šiuos laukus galima įtraukti kaip vietos rezervavimo ženklus, kuriuos naudojant sugeneruoti dokumentai užpildomi reikiama informacija iš programos.</span><span class="sxs-lookup"><span data-stu-id="5ca61-105">These fields can be added as placeholders that are used to fill generated documents with required information from the application.</span></span> <span data-ttu-id="5ca61-106">Prie kiekvieno įtraukto lauko taip pat galite nurodyti susiejimą su duomenų šaltiniais, kad nurodytumėte, kokie programos duomenys bus įvedami į lauką, kai, naudojant šabloną, bus generuojami verslo dokumentai.</span><span class="sxs-lookup"><span data-stu-id="5ca61-106">For every field that you add, you can also specify a binding to the data sources, to specify what application data will be entered in the field when the template is used to generate business documents.</span></span>

<span data-ttu-id="5ca61-107">Norėdami sužinoti daugiau apie šią funkciją, atlikite šioje temoje esantį pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="5ca61-107">To learn more about this feature, complete the example in this topic.</span></span> <span data-ttu-id="5ca61-108">Šiame pavyzdyje parodyta, kaip atnaujinti šabloną ir užpildyti sugeneruotos laisvos formos sąskaitos faktūros laukus.</span><span class="sxs-lookup"><span data-stu-id="5ca61-108">This example shows how to update a template to fill in the fields in free text invoice forms that are generated.</span></span>

## <a name="configure-business-document-management-to-edit-templates"></a><span data-ttu-id="5ca61-109">Funkcijos Verslo dokumentų valdymas konfigūravimas šablonams redaguoti</span><span class="sxs-lookup"><span data-stu-id="5ca61-109">Configure Business document management to edit templates</span></span>

<span data-ttu-id="5ca61-110">Kadangi funkcija Verslo dokumentų valdymas (BDM) yra sukurta sistemos [Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md) pagrindu, pradėti dirbti su BDM galėsite tik sukonfigūravę reikiamus ER ir BDM parametrus.</span><span class="sxs-lookup"><span data-stu-id="5ca61-110">Because Business document management (BDM) is built on top of the [Electronic reporting (ER) overview](general-electronic-reporting.md) framework, you must configure the required ER and BDM parameters before you can start to work with BDM.</span></span>

1.  <span data-ttu-id="5ca61-111">Kaip sistemos administratorius prisijunkite prie „Microsoft Dynamics 365 Finance“ egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="5ca61-111">Sign in to the instance of Microsoft Dynamics 365 Finance as the system administrator.</span></span>
2.  <span data-ttu-id="5ca61-112">Atlikite tolesnius temoje [Funkcijos Verslo dokumentų valdymas apžvalga](er-business-document-management.md) pateikto pavyzdžio veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5ca61-112">Complete the following steps of the example in the [Business document management overview](er-business-document-management.md) topic:</span></span>

    1.  <span data-ttu-id="5ca61-113">Sukonfigūruokite ER parametrus.</span><span class="sxs-lookup"><span data-stu-id="5ca61-113">Configure ER parameters.</span></span>
    2.  <span data-ttu-id="5ca61-114">Įjunkite BDM.</span><span class="sxs-lookup"><span data-stu-id="5ca61-114">Turn on BDM.</span></span>

<span data-ttu-id="5ca61-115">Dabar galite pradėti naudoti BDM ir redaguoti verslo dokumentų šablonus.</span><span class="sxs-lookup"><span data-stu-id="5ca61-115">You can now start to use BDM to edit business document templates.</span></span>

## <a name="import-er-solutions-that-contain-a-template"></a><span data-ttu-id="5ca61-116">ER sprendimų, kuriuose yra šablonas, importavimas</span><span class="sxs-lookup"><span data-stu-id="5ca61-116">Import ER solutions that contain a template</span></span>

<span data-ttu-id="5ca61-117">Šios procedūros pavyzdyje naudojamas oficialiai publikuotas ER sprendimas.</span><span class="sxs-lookup"><span data-stu-id="5ca61-117">The example in this procedure uses the officially published ER solution.</span></span> <span data-ttu-id="5ca61-118">Šio sprendimo ER konfigūracijas turite importuoti į savo dabartinį „Finance“ egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="5ca61-118">You must import the ER configurations of this solution into your current instance of Finance.</span></span>

<span data-ttu-id="5ca61-119">Šio sprendimo ER formato konfigūracijoje **Laisvos formos sąskaita faktūra („Excel“)** yra verslo dokumento šablonas „Excel“ formatu, kurį galima redaguoti naudojant BDM.</span><span class="sxs-lookup"><span data-stu-id="5ca61-119">The **Free text invoice (Excel)** ER format configuration of this solution contains the business document template in Excel format that can be edited by using BDM.</span></span> <span data-ttu-id="5ca61-120">Importuokite naujausią šios ER formato konfigūracijos versiją iš „Microsoft Dynamics“ Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="5ca61-120">Import the latest version of this ER format configuration from Microsoft Dynamics Lifecycle Service (LCS).</span></span> <span data-ttu-id="5ca61-121">Atitinkamas ER duomenų modelis ir ER modelio susiejimo konfigūracijos bus importuoti automatiškai.</span><span class="sxs-lookup"><span data-stu-id="5ca61-121">The corresponding ER data model and ER model mapping configurations will be imported automatically.</span></span>

<span data-ttu-id="5ca61-122">Norėdami gauti daugiau informacijos apie tai, kaip importuoti ER konfigūracijas, žr. [ER konfigūracijų ciklo valdymas](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="5ca61-122">For more information about how to import ER configurations, see [Manage the ER configuration lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![LCS puslapis Bendrai naudojamo turto biblioteka](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a><span data-ttu-id="5ca61-124">ER sprendimo šablono redagavimas</span><span class="sxs-lookup"><span data-stu-id="5ca61-124">Edit the ER solution template</span></span>

1.  <span data-ttu-id="5ca61-125">Prisijunkite kaip vartotojas, kuriam suteikta prieiga prie darbo srities **Verslo dokumentų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-125">Sign in as a user who has access to the **Business document management** workspace.</span></span>
2.  <span data-ttu-id="5ca61-126">Darbo sritį **Verslo dokumentų valdymas** atidarykite.</span><span class="sxs-lookup"><span data-stu-id="5ca61-126">Open the **Business document management** workspace.</span></span>

    ![Darbo sritis Verslo dokumentų valdymas](./media/BDM-AddFldExcel-Workspace.png)

3.  <span data-ttu-id="5ca61-128">Tinklelyje pasirinkite šabloną **Laisvos formos sąskaita faktūra („Excel“)**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-128">In the grid, select the **Free text invoice (Excel)** template.</span></span>
4.  <span data-ttu-id="5ca61-129">Dešiniojoje srityje pasirinkite **Naujas šablonas**, kad sukurtumėte naują šabloną pasirinkto šablono pagrindu.</span><span class="sxs-lookup"><span data-stu-id="5ca61-129">In the right pane, select **New template** to create a new template that is based on the selected template.</span></span>
5.  <span data-ttu-id="5ca61-130">Lauke **Pavadinimas** kaip naujo šablono pavadinimą įveskite **Laisvos formos sąskaita faktūra („Excel“) „Contoso“**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-130">In the **Title** field, enter **Free text invoice (Excel) Contoso** as the title of the new template.</span></span>
6.  <span data-ttu-id="5ca61-131">Pasirinkite **Gerai**, kad patvirtintumėte redagavimo proceso pradžią.</span><span class="sxs-lookup"><span data-stu-id="5ca61-131">Select **OK** to confirm the start of the editing process.</span></span>

<span data-ttu-id="5ca61-132">Atidaromas BDM šablonų rengyklės puslapis.</span><span class="sxs-lookup"><span data-stu-id="5ca61-132">The BDM template editor page appears.</span></span> <span data-ttu-id="5ca61-133">Naudodami „Microsoft 365“, pasirinktą šabloną galite redaguoti internetu, įdėtajame valdiklyje.</span><span class="sxs-lookup"><span data-stu-id="5ca61-133">You can use Microsoft 365 to edit the selected template online in the embedded control.</span></span>

![BDM šablonų rengyklės puslapis](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a><span data-ttu-id="5ca61-135">Naujo lauko žymos įtraukimas į šabloną</span><span class="sxs-lookup"><span data-stu-id="5ca61-135">Add the label for a new field to the template</span></span>

1.  <span data-ttu-id="5ca61-136">BDM šablonų rengyklės puslapio „Excel“ juostelės skirtuke **Rodinys** pažymėkite redaguojamojo „Excel“ šablono žymės langelius **Antraštės ir Tinklelio eilutės**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-136">On the BDM template editor page, on the Excel ribbon, on the **View** tab, select the **Headings and Gridlines** check boxes for the editable Excel template.</span></span>

    ![Pažymėti žymės langeliai Antraštės ir Tinklelio eilutės](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  <span data-ttu-id="5ca61-138">Pažymėkite langelius **E8:F8**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-138">Select cells **E8:F8**.</span></span>
3.  <span data-ttu-id="5ca61-139">„Excel“ juostelės skirtuke **Pradžia** pasirinkdami **Sulieti ir centruoti**, pažymėtus langelius suliekite į naują sulietą langelį **E8:F8**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-139">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **E8:F8** cell.</span></span>
4.  <span data-ttu-id="5ca61-140">Sulietame langelyje **E8:F8** įveskite **URL**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-140">In the merged cell **E8:F8**, enter **URL**.</span></span>
5.  <span data-ttu-id="5ca61-141">Pasirinkite sulietą langelį **E7:F7** , tada – **Formato kopijavimo priemonė** ir sulietą langelį **E8:F8**, kad jį suformatuotumėte taip, kaip sulietas langelis **E7:F7**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-141">Select merged cell **E7:F7**, select **Format painter**, and then select merged cell **E8:F8** to format it in the same way as merged cell **E7:F7**.</span></span>

    ![Naujo lauko žyma įtraukta į šabloną](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a><span data-ttu-id="5ca61-143">Šablono formatavimas norint rezervuoti vietą naujam laukui</span><span class="sxs-lookup"><span data-stu-id="5ca61-143">Format the template to reserve space for a new field</span></span>

1.  <span data-ttu-id="5ca61-144">BDM šablonų rengyklės puslapyje pasirinkite sulietą langelį **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-144">On the BDM template editor page, select merged cell **G8:H8**.</span></span>
2.  <span data-ttu-id="5ca61-145">„Excel“ juostelės skirtuke **Pradžia** pasirinkdami **Sulieti ir centruoti**, pažymėtus langelius suliekite į naują sulietą langelį **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-145">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **G8:H8** cell.</span></span>
3.  <span data-ttu-id="5ca61-146">Pasirinkite sulietą langelį **G7:H7** , tada – **Formato kopijavimo priemonė** ir sulietą langelį **G8:H8**, kad jį suformatuotumėte taip, kaip sulietas langelis **G7:H7**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-146">Select merged cell **G7:H7**, select **Format painter**, and then select merged cell **G8:H8** to format it in the same way as merged cell **G7:H7**.</span></span>

    ![Vieta rezervuota naujam laukui](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  <span data-ttu-id="5ca61-148">Langelio lauke **Pavadinimas** pasirinkite **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-148">In the **Name** box field, select **CompanyInfo**.</span></span>

    <span data-ttu-id="5ca61-149">Dabartinio „Excel“ šablono intervale **CompanyInfo** yra visi laukai, kuriuos naudojant sugeneruotos ataskaitos antraštė užpildoma dabartinės įmonės kaip pardavėjo šalies informacija.</span><span class="sxs-lookup"><span data-stu-id="5ca61-149">The **CompanyInfo** range of the current Excel template holds all the fields that are used to fill the header of a generated report with the details of the current company as a seller party.</span></span>

    ![Parinktas intervalas CompanyInfo.](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a><span data-ttu-id="5ca61-151">Naujo lauko įtraukimas į šabloną</span><span class="sxs-lookup"><span data-stu-id="5ca61-151">Add a new field to the template</span></span>

1.  <span data-ttu-id="5ca61-152">Puslapio **BDM šablonų rengyklė** veiksmų srityje pasirinkite **Rodyti formatą**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-152">On the **BDM template editor** page, on the Action Pane, select **Show format**.</span></span>
2.  <span data-ttu-id="5ca61-153">Srityje **Šablono struktūra** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-153">In the **Template structure** pane, select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5ca61-154">Turite koreguoti šablono skyrių, kurį norite naudoti kaip naują lauką.</span><span class="sxs-lookup"><span data-stu-id="5ca61-154">You must adjust the section of the template that you want to use as a new field.</span></span> <span data-ttu-id="5ca61-155">Jį jau pakoregavote formatuodami sulietą langelį **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-155">You already made this adjustment by formatting merged cell **G8:H8**.</span></span>

    ![Naujo lauko įtraukimas į šabloną](./media/BDM-AddFldExcel-AddCell.png)

3.  <span data-ttu-id="5ca61-157">Pasirinkite **„Excel“\langelis**, kad į šabloną kaip langelį įtrauktumėte naują lauką.</span><span class="sxs-lookup"><span data-stu-id="5ca61-157">Select **Excel\Cell** to add a new field as a cell in the template.</span></span>

    <span data-ttu-id="5ca61-158">Jei į šabloną norite įtraukti naują intervalą, galite pasirinkti **„Excel“\intervalas**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-158">You can select **Excel\Range** if you want to add a new range to the template.</span></span> <span data-ttu-id="5ca61-159">Įvestame intervale gali būti keli langeliai.</span><span class="sxs-lookup"><span data-stu-id="5ca61-159">The range that is entered can contain multiple cells.</span></span> <span data-ttu-id="5ca61-160">Šiuos langelius galite įtraukti vėliau.</span><span class="sxs-lookup"><span data-stu-id="5ca61-160">You can add these cells later.</span></span>
    
    <span data-ttu-id="5ca61-161">Atkreipkite dėmesį, kad srityje **Šablono struktūra** šablono komponentas **CompanyInfo** pasirinktas automatiškai, nes jis dabartinėje šablono struktūroje yra tinkamiausias pirminis komponentas įtraukiamam laukui.</span><span class="sxs-lookup"><span data-stu-id="5ca61-161">Notice that the **CompanyInfo** template component, is automatically selected in the **Template structure** pane, because it's the most suitable parent component in the current template structure for the field that you're adding.</span></span>
    
4.  <span data-ttu-id="5ca61-162">Lauke **„Excel“ intervalas** įveskite **CompanyURL_Value**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-162">In the **Excel range** field, enter **CompanyURL_Value**.</span></span>
5.  <span data-ttu-id="5ca61-163">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-163">Select **OK**.</span></span>

    ![Laukas CompanyURL_Value įtrauktas į šablono struktūrą](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  <span data-ttu-id="5ca61-165">Srityje **Šablono struktūra** pasirinkite daugtaškio mygtuką (...), tada – **Rodyti susiejimus**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-165">In the **Template structure** pane, select the ellipsis button (...), and then select **Show bindings**.</span></span>

    ![Pasirinkta Rodyti susiejimus](./media/BDM-AddFldExcel-ShowBindings.png)

    <span data-ttu-id="5ca61-167">Srityje **Šablono struktūra** dabar rodomi duomenų šaltiniai, pasiekiami esamame ER formate.</span><span class="sxs-lookup"><span data-stu-id="5ca61-167">The **Template structure** pane now shows the data sources that are available in the underlying ER format.</span></span>

7.  <span data-ttu-id="5ca61-168">Kaip lauką, kurį planuojate susieti su esamo ER formato duomenų šaltiniu, pasirinkite **CompanyInfo_Value**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-168">Select **CompanyInfo_Value** as the field that you plan to bind to a data source of the underlying ER format.</span></span>
8.  <span data-ttu-id="5ca61-169">Srities **Šablono struktūra** skyriuje **Duomenų šaltiniai** išplėskite **Modelis \>InvoiceBase \>CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-169">In the **Data sources** section of the **Template structure** pane, expand **Model \> InvoiceBase \> CompanyInfo**.</span></span>
9.  <span data-ttu-id="5ca61-170">Dalyje **CompanyInfo** pasirinkite elementą **WebsiteURI**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-170">Under **CompanyInfo**, select the **WebsiteURI** item.</span></span>

    ![Pasirinktas elementas WebsiteURI](./media/BDM-AddFldExcel-BindURL.png)

10. <span data-ttu-id="5ca61-172">Pasirinkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-172">Select **Bind**.</span></span>
11. <span data-ttu-id="5ca61-173">Srityje **Šablono struktūra** pasirinkite **Įrašyti** ir uždarykite BDM šablonų rengyklės puslapį.</span><span class="sxs-lookup"><span data-stu-id="5ca61-173">In the **Template structure** pane, select **Save**, and then close the BDM template editor page.</span></span>

<span data-ttu-id="5ca61-174">Atnaujintas šablonas rodomas darbo srities **Verslo dokumentų valdymas** skirtuko **Šablonas** dešiniojoje srityje.</span><span class="sxs-lookup"><span data-stu-id="5ca61-174">In the **Business document management** workspace, the **Template** tab in the right pane shows the updated template.</span></span> <span data-ttu-id="5ca61-175">Atkreipkite dėmesį, kad tinklelyje redaguoto šablono laukas **Būsena** pakeistas į **Juodraštis**, o laukas **Tikslinimas** nebėra tuščias.</span><span class="sxs-lookup"><span data-stu-id="5ca61-175">In the grid, notice that the **Status** field for the edited template has been changed to **Draft**, and the **Revision** field is no longer blank.</span></span> <span data-ttu-id="5ca61-176">Šie pokyčiai nurodo, kad pradėtas šio šablono redagavimo procesas.</span><span class="sxs-lookup"><span data-stu-id="5ca61-176">These changes indicate that the process of editing this template has been started.</span></span>

![Redaguotas šablonas darbo srityje Verslo dokumentų valdymas](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a><span data-ttu-id="5ca61-178">Įmonės parametrų peržiūra</span><span class="sxs-lookup"><span data-stu-id="5ca61-178">Review company settings</span></span>

1.  <span data-ttu-id="5ca61-179">Nueikite į **Organizacijos administravimas \> Organizacijos \> Juridiniai subjektai**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-179">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>
2.  <span data-ttu-id="5ca61-180">Patikrinkite, ar „FastTab“ elemente **Kontaktinė informacija** įvestas įmonės URL.</span><span class="sxs-lookup"><span data-stu-id="5ca61-180">On the **Contact information** FastTab, verify that the company URL is entered.</span></span>

![Puslapyje Juridiniai subjektai įvestas įmonės URL](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a><span data-ttu-id="5ca61-182">Verslo dokumentų generavimas atnaujintam šablonui patikrinti</span><span class="sxs-lookup"><span data-stu-id="5ca61-182">Generate business documents to test the updated template</span></span>

1.  <span data-ttu-id="5ca61-183">Programoje įmonę pakeiskite į **USMF** ir nueikite į **Gautinos sumos \> Sąskaitos faktūros \> Visos laisvos formos sąskaitos faktūros**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-183">In the application, change the company to **USMF**, and go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2.  <span data-ttu-id="5ca61-184">Pasirinkite sąskaitą-faktūrą **FTI-00000002**, tada – **Spausdinimo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-184">Select invoice **FTI-00000002**, and then select **Print management**.</span></span>
3.  <span data-ttu-id="5ca61-185">Kairiojoje srityje išplėskite **Modulis – gautinos sumos \> Dokumentai \> Laisvos formos sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-185">In the left pane, expand **Module - accounts receivable \> Documents \> Free text invoice**.</span></span>
4.  <span data-ttu-id="5ca61-186">Dalyje **Laisvos formos sąskaita faktūra** pasirinkite lygmenį **Originalus dokumentas**, kad nurodytumėte apdoroti skirtų sąskaitų faktūrų aprėptį.</span><span class="sxs-lookup"><span data-stu-id="5ca61-186">Under **Free text invoice**, select the **Original document** level to specify the scope of invoices for processing.</span></span>
5.  <span data-ttu-id="5ca61-187">Dešiniosios srities lauke **Ataskaitos formatas** pasirinkite nurodyto dokumento lygio šabloną **Laisvos formos sąskaita faktūra („Excel“) „Contoso“**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-187">In the right pane, in the **Report format** field, select the **Free text invoice (Excel) Contoso** template for the specified document level.</span></span>

    ![Pasirinktas šablonas Laisvos formos sąskaita faktūra („Excel“) „Contoso“](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  <span data-ttu-id="5ca61-189">Paspauskite **„Esc“**, kad uždarytumėte dabartinį puslapį.</span><span class="sxs-lookup"><span data-stu-id="5ca61-189">Press **Esc** to close the current page.</span></span>
7.  <span data-ttu-id="5ca61-190">Pasirinkite **Spausdinti \> Pasirinkta**.</span><span class="sxs-lookup"><span data-stu-id="5ca61-190">Select **Print \> Selected**.</span></span>
8.  <span data-ttu-id="5ca61-191">Atsisiųskite sugeneruotą dokumentą ir jį atidarykite programoje „Excel“.</span><span class="sxs-lookup"><span data-stu-id="5ca61-191">Download the generated document, and open it in Excel.</span></span>

    ![Laisvos formos sąskaita faktūra programoje „Excel“](./media/BDM-AddFldExcel-PreviewReport.png)

<span data-ttu-id="5ca61-193">Modifikuotas šablonas naudojamas pažymėtos prekės laisvos formos sąskaitos-faktūros ataskaitai generuoti.</span><span class="sxs-lookup"><span data-stu-id="5ca61-193">The modified template is used to generate the free text invoice report for the selected item.</span></span> <span data-ttu-id="5ca61-194">Norėdami išanalizuoti, kaip šią ataskaitą paveikė jūsų atlikti šablono pakeitimai, vykdykite šią ataskaitą viename programos seanse iš karto po to, kai paleičiate šabloną kitame programos seanse.</span><span class="sxs-lookup"><span data-stu-id="5ca61-194">To analyze how this report is affected by changes that you make to the template, run the report in one application session immediately after you change the template in another application session.</span></span>

## <a name="related-links"></a><span data-ttu-id="5ca61-195">Susiję saitai</span><span class="sxs-lookup"><span data-stu-id="5ca61-195">Related links</span></span>

[<span data-ttu-id="5ca61-196">Elektroninių ataskaitų (ER) apžvalga</span><span class="sxs-lookup"><span data-stu-id="5ca61-196">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="5ca61-197">Verslo dokumentų valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="5ca61-197">Business document management overview</span></span>](er-business-document-management.md)

[<span data-ttu-id="5ca61-198">Konfigūracijos, skirtos ataskaitoms OPENXML formatu generuoti, kūrimas</span><span class="sxs-lookup"><span data-stu-id="5ca61-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks/er-design-reports-openxml-2016-11.md)
