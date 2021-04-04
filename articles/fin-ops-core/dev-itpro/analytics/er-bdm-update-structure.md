---
title: Verslo dokumento šablono struktūros atnaujinimas
description: Šioje temoje paaiškinama, kaip atnaujinti verslo dokumento šablono struktūrą naudojantis funkcija Verslo dokumentų valdymas.
author: NickSelin
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 09813115544701ea3fffb6be06114bcdd63c0ba0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570453"
---
# <a name="update-the-structure-of-a-business-document-template"></a><span data-ttu-id="1f555-103">Verslo dokumento šablono struktūros atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="1f555-103">Update the structure of a business document template</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1f555-104">Funkcijos [Verslo dokumentų valdymas](er-business-document-management.md) šablonų rengyklės srityje **Šablono struktūra** galite modifikuoti verslo dokumento šabloną, [įtraukdami naujų laukų](er-bdm-add-field-to-excel-template.md) į „Microsoft Excel“ šabloną.</span><span class="sxs-lookup"><span data-stu-id="1f555-104">In the **Template structure** pane of the [Business document management](er-business-document-management.md) template editor, you can modify a business document template by [adding new fields](er-bdm-add-field-to-excel-template.md) to a template in Microsoft Excel.</span></span> <span data-ttu-id="1f555-105">Šablono struktūra tada automatiškai atnaujinama programoje „Dynamics 365 Finance“, kad atspindėtų keitimus, atliktus srityje **Šablono struktūra**.</span><span class="sxs-lookup"><span data-stu-id="1f555-105">The structure of the template is then automatically updated in Dynamics 365 Finance, so that it reflects the changes that you made in the **Template structure** pane.</span></span>

<span data-ttu-id="1f555-106">Taip pat galite modifikuoti šabloną naudodami „Office 365“ internetinę funkciją.</span><span class="sxs-lookup"><span data-stu-id="1f555-106">You can also modify a template by using Office 365 online functionality.</span></span> <span data-ttu-id="1f555-107">Pavyzdžiui, į redaguojamą darbalapį galite įtraukti naują pavadintą elementą, pvz., paveikslėlį ar figūrą.</span><span class="sxs-lookup"><span data-stu-id="1f555-107">For example, you can add a new named item, such as a picture or shape, to the editable worksheet.</span></span> <span data-ttu-id="1f555-108">Šiuo atveju šablono struktūra nėra automatiškai atnaujinama programoje „Finance“, o jūsų įtrauktas elementas nerodomas srityje **Šablono struktūra**.</span><span class="sxs-lookup"><span data-stu-id="1f555-108">In this case, the structure of the template isn't automatically updated in Finance, and the item that you added doesn't appear in the **Template structure** pane.</span></span> <span data-ttu-id="1f555-109">Programoje „Finance“ šablono struktūrą atnaujinkite neautomatiniu būdu, pasirinkdami **Atnaujinti struktūrą** šablonų rengyklės puslapyje.</span><span class="sxs-lookup"><span data-stu-id="1f555-109">Manually update the template structure in Finance by selecting **Update structure** on the template editor page.</span></span>

<span data-ttu-id="1f555-110">Norėdami gauti daugiau informacijos apie šią funkciją, atlikite toliau pateiktą pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="1f555-110">For more information about this feature, complete the following example.</span></span>

## <a name="example-update-the-structure-of-a-business-document-template"></a><span data-ttu-id="1f555-111">Pavyzdys: verslo dokumento šablono struktūros atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="1f555-111">Example: Update the structure of a business document template</span></span>

<span data-ttu-id="1f555-112">Šiame pavyzdyje rodoma, kaip sistemos administratorius gali atnaujinti verslo dokumento šablono struktūrą programoje „Finance“, kai šablonas modifikuojamas programoje „Office Online“.</span><span class="sxs-lookup"><span data-stu-id="1f555-112">This example shows how a system administrator can update the structure of a business document template in Finance after the template is modified in Office Online.</span></span> <span data-ttu-id="1f555-113">Tolesniuose skyriuose aprašomi susiję veiksmai.</span><span class="sxs-lookup"><span data-stu-id="1f555-113">The following sections explain the steps that are involved.</span></span>

### <a name="prepare-a-business-document-template-for-editing"></a><span data-ttu-id="1f555-114">Verslo dokumento šablono paruošimas redaguoti</span><span class="sxs-lookup"><span data-stu-id="1f555-114">Prepare a business document template for editing</span></span>

<span data-ttu-id="1f555-115">Atlikite tolesnes procedūras, nurodytas temoje [Funkcijos Verslo dokumentų valdymas apžvalga](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="1f555-115">Complete the following procedures in [Business document management overview](er-business-document-management.md).</span></span>

1. [<span data-ttu-id="1f555-116">ER parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="1f555-116">Configure ER parameters</span></span>](er-business-document-management.md#configure-er-parameters)
2. [<span data-ttu-id="1f555-117">ER sprendimų importavimas</span><span class="sxs-lookup"><span data-stu-id="1f555-117">Import ER solutions</span></span>](er-business-document-management.md#import-er-solutions)
3. [<span data-ttu-id="1f555-118">Verslo dokumentų valdymo įjungimas</span><span class="sxs-lookup"><span data-stu-id="1f555-118">Enable Business document management</span></span>](er-business-document-management.md#enable-business-document-management)
4. [<span data-ttu-id="1f555-119">Parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="1f555-119">Configure parameters</span></span>](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a><span data-ttu-id="1f555-120">Verslo dokumento šablono redagavimas</span><span class="sxs-lookup"><span data-stu-id="1f555-120">Edit a business document template</span></span>

1. <span data-ttu-id="1f555-121">Darbo srityje **Verslo dokumentų valdymas** pasirinkite **Naujas dokumentas**.</span><span class="sxs-lookup"><span data-stu-id="1f555-121">In the **Business document management** workspace, select **New document**.</span></span>
2. <span data-ttu-id="1f555-122">Puslapyje **Naujo šablono sukūrimas** pasirinkite šabloną **Laisvos formos sąskaita faktūra (ER pavyzdys) („Excel“)**.</span><span class="sxs-lookup"><span data-stu-id="1f555-122">On the **Create a new template** page, select the **Free text invoice (ER sample)(Excel)** template.</span></span>
3. <span data-ttu-id="1f555-123">Pasirinkite **Kurti dokumentą**.</span><span class="sxs-lookup"><span data-stu-id="1f555-123">Select **Create document**.</span></span>
4. <span data-ttu-id="1f555-124">Lauke **Pavadinimas** įveskite **FTI pavyzdys „Litware“**.</span><span class="sxs-lookup"><span data-stu-id="1f555-124">In the **Title** field, enter **FTI sample Litware**.</span></span>
5. <span data-ttu-id="1f555-125">Pasirinkite **Gerai**, kad sukurtumėte naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="1f555-125">Select **OK** to create the new template.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1f555-126">Jei dar neprisijungėte prie „Office Online“, būsite [nukreipti į „Office 365“ prisijungimo puslapį](er-business-document-management.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="1f555-126">If you haven't yet signed in to Office Online, you're [directed to the Office 365 sign-in page](er-business-document-management.md#frequently-asked-questions).</span></span> <span data-ttu-id="1f555-127">Norėdami grįžti į savo „Finance“ aplinką, naršyklėje pasirinkite mygtuką **Atgal**.</span><span class="sxs-lookup"><span data-stu-id="1f555-127">To return to your Finance environment, select the **Back** button in your browser.</span></span>

    <span data-ttu-id="1f555-128">Naujas šablonas atidaromas redaguoti „Excel Online“ įdėtajame valdiklyje, esančiame šablonų rengyklės puslapyje.</span><span class="sxs-lookup"><span data-stu-id="1f555-128">The new template is opened for editing in the Excel Online embedded control on the template editor page.</span></span>

<span data-ttu-id="1f555-129">[![Funkcijos Verslo dokumentų valdymas darbo srities naudojimas norint pradėti redaguoti verslo dokumento šabloną](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span><span class="sxs-lookup"><span data-stu-id="1f555-129">[![Using the Business document management workspace to start to edit a business document template](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span></span>

### <a name="review-the-current-structure-of-the-editable-template"></a><span data-ttu-id="1f555-130">Dabartinės redaguojamojo šablono struktūros peržiūra</span><span class="sxs-lookup"><span data-stu-id="1f555-130">Review the current structure of the editable template</span></span>

1. <span data-ttu-id="1f555-131">„Excel Online“ juostelės skirtuko **Rodinys** grupėje **Rodyti** pasirinkite **Tinklelio eilutės**.</span><span class="sxs-lookup"><span data-stu-id="1f555-131">In Excel Online, on the ribbon, on the **View** tab, in the **Show** group, select **Gridlines**.</span></span>
2. <span data-ttu-id="1f555-132">Redaguojamame šablone pasirinkite stačiakampį, esantį virš šablono pavadinimo.</span><span class="sxs-lookup"><span data-stu-id="1f555-132">In the editable template, select the rectangle above the template title.</span></span> <span data-ttu-id="1f555-133">Šis stačiakampis yra paveikslėlis, pavadintas **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="1f555-133">This rectangle is a picture that is named **rptHeaderCompLogo**.</span></span>
3. <span data-ttu-id="1f555-134">Jei sritis **Šablono struktūra** paslėpta, pasirinkite **Rodyti struktūrą**.</span><span class="sxs-lookup"><span data-stu-id="1f555-134">If the **Template structure** pane is hidden, select **Show structure**.</span></span>
4. <span data-ttu-id="1f555-135">Srityje **Šablono struktūra** išplėskite **Ataskaita \> Sąskaita faktūra \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="1f555-135">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="1f555-136">Atkreipkite dėmesį, kad „Finance“ šablono struktūroje elementas **rptHeaderCompLogo** pateikiamas kaip antrinis **Ataskaita \> Sąskaita faktūra \> rptHeader \> rptHeaderPart1** elementas.</span><span class="sxs-lookup"><span data-stu-id="1f555-136">Notice that, in the template structure in Finance, the **rptHeaderCompLogo** item is presented as a child item of **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>

<span data-ttu-id="1f555-137">[![Funkcijos Verslo dokumentų valdymas darbo srities naudojimas norint peržiūrėti dabartinę redaguojamojo šablono struktūrą](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span><span class="sxs-lookup"><span data-stu-id="1f555-137">[![Using the Business document management workspace to review the current structure of an editable template](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a><span data-ttu-id="1f555-138">Verslo dokumento šablono struktūros atnaujinimas panaikinant paveikslėlį</span><span class="sxs-lookup"><span data-stu-id="1f555-138">Update the structure of a business document template by deleting a picture</span></span>

1. <span data-ttu-id="1f555-139">„Excel Online“ redaguojamame šablone pasirinkite paveikslėlį **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="1f555-139">In Excel Online, in the editable template, select the **rptHeaderCompLogo** picture.</span></span>
2. <span data-ttu-id="1f555-140">Atlikite vieną iš tolesnių veiksmų, kad panaikintumėte pažymėtą paveikslėlį redaguojamame šablone,</span><span class="sxs-lookup"><span data-stu-id="1f555-140">Follow one of these steps to delete the selected picture from the editable template:</span></span>

    - <span data-ttu-id="1f555-141">Pasirinkite klaviatūros klavišą **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="1f555-141">Select the **Delete** key on your keyboard.</span></span>
    - <span data-ttu-id="1f555-142">Pasirinkite ir palaikykite (arba dešiniuoju pelės mygtuku spustelėkite) paveikslėlį ir pasirinkite **Iškirpti**.</span><span class="sxs-lookup"><span data-stu-id="1f555-142">Select and hold (or right-click) the picture, and then select **Cut**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1f555-143">Elementas **rptHeaderCompLogo** šiuo metu vis dar yra „Finance“ šablono struktūroje, net jei paveikslėlis nebėra įtrauktas į „Excel“ šabloną.</span><span class="sxs-lookup"><span data-stu-id="1f555-143">The **rptHeaderCompLogo** item is currently still present in the template structure in Finance, even though the picture is no longer included in the Excel template.</span></span>

3. <span data-ttu-id="1f555-144">Pasirinkite **Atnaujinti struktūrą**, kad sinchronizuotumėte redaguojamojo šablono struktūrą programose „Excel“ ir „Finance“.</span><span class="sxs-lookup"><span data-stu-id="1f555-144">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
4. <span data-ttu-id="1f555-145">Srityje **Šablono struktūra** išplėskite **Ataskaita \> Sąskaita faktūra \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="1f555-145">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="1f555-146">Atkreipkite dėmesį, kad elementas **rptHeaderCompLogo** nebėra įtrauktas į „Finance“ šablono struktūrą.</span><span class="sxs-lookup"><span data-stu-id="1f555-146">Notice that the **rptHeaderCompLogo** item is no longer included in the template structure in Finance.</span></span>

<span data-ttu-id="1f555-147">[![Funkcijos Verslo dokumentų valdymas darbo srities naudojimas norint panaikinti paveikslėlį verslo dokumento šablone](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span><span class="sxs-lookup"><span data-stu-id="1f555-147">[![Using the Business document management workspace to delete a picture from a business document template](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a><span data-ttu-id="1f555-148">Verslo dokumento šablono struktūros atnaujinimas įtraukiant paveikslėlį</span><span class="sxs-lookup"><span data-stu-id="1f555-148">Update the structure of a business document template by adding a picture</span></span>

1. <span data-ttu-id="1f555-149">„Excel Online“ juostelės skirtuko **Įterpti** grupėje **Iliustracijos** pasirinkite **Paveikslėlis**.</span><span class="sxs-lookup"><span data-stu-id="1f555-149">In Excel Online, on the ribbon, on the **Insert** tab, in the **Illustrations** group, select **Picture**.</span></span>
2. <span data-ttu-id="1f555-150">Pasirinkite **Pasirinkti failą**, naršydami pasirinkite vaizdą, kurį norite įtraukti, ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1f555-150">Select **Choose file**, browse to the image that you want to add, select it, and then select **OK**.</span></span>
3. <span data-ttu-id="1f555-151">Pasirinkite **Įterpti**.</span><span class="sxs-lookup"><span data-stu-id="1f555-151">Select **Insert**.</span></span>
4. <span data-ttu-id="1f555-152">Perkelkite naują paveikslėlį į tinkamą vietą.</span><span class="sxs-lookup"><span data-stu-id="1f555-152">Move the new picture until it's in the correct place.</span></span> <span data-ttu-id="1f555-153">Numatyta, kad „Excel“ paveikslėlį pavadina.</span><span class="sxs-lookup"><span data-stu-id="1f555-153">By default, Excel names the picture.</span></span> <span data-ttu-id="1f555-154">Pavyzdžiui, ji gali paveikslėlį pavadinti **2 paveikslėlis**.</span><span class="sxs-lookup"><span data-stu-id="1f555-154">For example, it might name the picture **Picture 2**.</span></span>
5. <span data-ttu-id="1f555-155">Pasirinkite **Atnaujinti struktūrą**, kad sinchronizuotumėte redaguojamojo šablono struktūrą programose „Excel“ ir „Finance“.</span><span class="sxs-lookup"><span data-stu-id="1f555-155">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
6. <span data-ttu-id="1f555-156">Srityje **Šablono struktūra** išplėskite **Ataskaita \> Sąskaita faktūra \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="1f555-156">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
7. <span data-ttu-id="1f555-157">Atkreipkite dėmesį, kad naujas paveikslėlis dabar kaip elementas įtrauktas į „Finance“ šablono struktūrą.</span><span class="sxs-lookup"><span data-stu-id="1f555-157">Notice that the new picture is now included as an item in the template structure in Finance.</span></span>

<span data-ttu-id="1f555-158">[![Funkcijos Verslo dokumentų valdymas darbo srities naudojimas norint įtraukti paveikslėlį į verslo dokumento šabloną](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span><span class="sxs-lookup"><span data-stu-id="1f555-158">[![Using the Business document management workspace to add a picture to a business document template](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span></span>

## <a name="related-links"></a><span data-ttu-id="1f555-159">Susiję saitai</span><span class="sxs-lookup"><span data-stu-id="1f555-159">Related links</span></span>

[<span data-ttu-id="1f555-160">Elektroninių ataskaitų (ER) apžvalga</span><span class="sxs-lookup"><span data-stu-id="1f555-160">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="1f555-161">Verslo dokumentų valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="1f555-161">Business document management overview</span></span>](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]