---
title: „Microsoft Office” stiliaus vartotojo sąsaja Verslo dokumentų valdyme
description: Šioje temoje paaiškinama, kaip naudoti naują vartotojo sąsają Elektroninių ataskaitų (ER) sistemos funkcijoje Verslo dokumentų valdymas.
author: v-anamir
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6c5081f71a18dfac83b7aea950395436b42f50e
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881041"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a><span data-ttu-id="a19f8-103">„Microsoft Office” stiliaus vartotojo sąsaja Verslo dokumentų valdyme</span><span class="sxs-lookup"><span data-stu-id="a19f8-103">Microsoft Office-style user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a19f8-104">Verslo dokumentų valdymas leidžia verslo vartotojams redaguoti verslo dokumentų šablonus naudojant „Microsoft 365 service“ paslaugą arba atitinkamą „Microsoft Office“ darbalaukio programą.</span><span class="sxs-lookup"><span data-stu-id="a19f8-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="a19f8-105">Redagavimas gali būti dizaino keitimai arba nauji diegimai arba vartotojai gali įtraukti vietos rezervavimo ženklų, kad galėtų įtraukti papildomų duomenų, nekeisdami šaltinio kodo.</span><span class="sxs-lookup"><span data-stu-id="a19f8-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="a19f8-106">Norėdami gauti daugiau informacijos apie tai, kaip naudotis funkcija Verslo dokumentų valdymas, žr. [Funkcijos Verslo dokumentų valdymas apžvalga](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="a19f8-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="a19f8-107">Naujo vartotojo sąsaja (UI) yra aiškesnė ir patogesnė naudoti.</span><span class="sxs-lookup"><span data-stu-id="a19f8-107">The new user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="a19f8-108">Srityje **Verslo dokumentas** rodomi tik tie šablonai, kurie yra pasiekiami dabartiniam tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="a19f8-108">The **Business document** area shows only the templates that are available for the current provider.</span></span> <span data-ttu-id="a19f8-109">Ankstesnėje vartotojo sąsajoje, skirtuke **Šablonas** buvo išvardyti visi šablonai, galimi bet kuriam teikėjui.</span><span class="sxs-lookup"><span data-stu-id="a19f8-109">In the previous UI, the **Template** tab listed all the templates that were available for any providers.</span></span> <span data-ttu-id="a19f8-110">Taip pat joje buvo rodomi visi šablonai, kuriuos sukūrė ir redagavo bet kuris vartotojas, turintis tokį patį vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="a19f8-110">It also showed all the templates that were created and edited by any user who had the same role.</span></span>

<span data-ttu-id="a19f8-111">Galite naudoti mygtuką **Naujas dokumentas** kurti ir redaguoti šabloną Elektroninių ataskaitų (ER) formato konfigūracijoje, kurią pateikia kitas teikėjas.</span><span class="sxs-lookup"><span data-stu-id="a19f8-111">You can use the **New document** button to create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="a19f8-112">Šioje temoje pateikiamame pavyzdyje teikėjas yra „Microsoft“.</span><span class="sxs-lookup"><span data-stu-id="a19f8-112">In the example in this topic, the provider is Microsoft.</span></span> <span data-ttu-id="a19f8-113">Taip pat galite sukurti šabloną įkeldami savo šabloną „Excel” formatu.</span><span class="sxs-lookup"><span data-stu-id="a19f8-113">Alternatively, you can create a template by uploading your own template in Excel format.</span></span>


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

<span data-ttu-id="a19f8-114">Video (parodytas aukščiau) apie tai, kaip [Kurti naują verslo dokumentą naudojant Verslo dokumentų valdymą](https://youtu.be/gAIYl-mM_pw) yra įtrauktas į [„Finance and Operations” grojaraštį](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), prieinamą „YouTube”.</span><span class="sxs-lookup"><span data-stu-id="a19f8-114">The [Create a new business document using Business document management](https://youtu.be/gAIYl-mM_pw) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="a19f8-115">Naujo dokumento vartotojo sąsajos įjungimas funkcijoje Verslo dokumentų valdymas</span><span class="sxs-lookup"><span data-stu-id="a19f8-115">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="a19f8-116">Norėdami pradėti naudoti naujo dokumento vartotojo sąsają funkcijoje Verslo dokumentų valdymas, turite įjungti funkciją **Į „Office“ panaši vartotojo sąsaja funkcijoje Verslo dokumentų valdymas** darbo srityje **Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="a19f8-116">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="a19f8-117">Atlikite tolesnius veiksmus, norėdami įjungti šią funkciją visiems juridiniams subjektams.</span><span class="sxs-lookup"><span data-stu-id="a19f8-117">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="a19f8-118">Iš darbo srities **Funkcijų valdymas** skirtuko **Visi** sąrašo pasirinkite funkciją **Į „Office“ panaši vartotojo sąsajos patirtis Verslo dokumentų valdymui**.</span><span class="sxs-lookup"><span data-stu-id="a19f8-118">In the **Feature management** workspace, on the **All** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="a19f8-119">Pasirinkite **Įjungti dabar**, kad įjungtumėte pasirinktą funkciją.</span><span class="sxs-lookup"><span data-stu-id="a19f8-119">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="a19f8-120">Norėdami pasiekti naują funkciją, atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a19f8-120">Refresh the page to access the new feature.</span></span>

## <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="a19f8-121">Šablonų, priklausančių kitiems teikėjams, redagavimas</span><span class="sxs-lookup"><span data-stu-id="a19f8-121">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="a19f8-122">Darbo srityje **Verslo dokumentų valdymas** pasirinkite **Naujas dokumentas**.</span><span class="sxs-lookup"><span data-stu-id="a19f8-122">In the **Business document management** workspace, select **New document**.</span></span>

    ![Darbo sritis Verslo dokumentų valdymas](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="a19f8-124">Skirtuke **Pasirinkti** pasirinkite dokumentą, kurį norite naudoti kaip šabloną, o tada pasirinkite **Kurti dokumentą**.</span><span class="sxs-lookup"><span data-stu-id="a19f8-124">On the **Select** tab, select the document to use as a template, and then select **Create document**.</span></span>

    ![Verslo dokumentų dialogo langas](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="a19f8-126">Naujo dialogo lango lauke **Pavadinimas** pakeiskite pavadinimą į norimą pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="a19f8-126">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="a19f8-127">Pavadinimo tekstas naudojamas automatiškai sukurtai naujai ER formato konfigūracijai pavadinti.</span><span class="sxs-lookup"><span data-stu-id="a19f8-127">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="a19f8-128">Šios konfigūracijos (**Kliento laisvos formos sąskaitos-faktūros ataskaitos (GER) kopija**) juodraščio versijoje bus suredaguotas šablonas ir ji bus naudojama vykdant šį ER formatą, skirtą dabartiniam vartotojui.</span><span class="sxs-lookup"><span data-stu-id="a19f8-128">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="a19f8-129">Originalus šablonas iš pagrindinio ER formato konfigūracijos bus naudojamas visiems kitiems vartotojams skirtam ER formatui vykdyti.</span><span class="sxs-lookup"><span data-stu-id="a19f8-129">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="a19f8-130">Lauke **Pavadinimas** pakeiskite redaguojamo šablono, kuris bus automatiškai sukurtas, pirmo pataisymo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="a19f8-130">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="a19f8-131">Lauke **Komentaras** atnaujinkite redaguojamo šablono, kuris bus automatiškai sukurtas, pataisymo pastabas.</span><span class="sxs-lookup"><span data-stu-id="a19f8-131">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="a19f8-132">Pasirinkite **Gerai**, kad patvirtintumėte redagavimo proceso pradžią.</span><span class="sxs-lookup"><span data-stu-id="a19f8-132">Select **OK** to confirm the start of the editing process.</span></span>

    ![Dokumento kūrimo dialogo langas](./media/BDM_overview_new_template3.png)

<span data-ttu-id="a19f8-134">Paspaudus mygtuką **Naujas dokumentas**, sukuriamas ir redaguojamas šablonas ER formato konfigūracijoje, kurią pateikia kitas teikėjas.</span><span class="sxs-lookup"><span data-stu-id="a19f8-134">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="a19f8-135">Šiame pavyzdyje teikėjas yra „Microsoft“.</span><span class="sxs-lookup"><span data-stu-id="a19f8-135">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="a19f8-136">Pasirinkę **Naujas dokumentas**, peržiūrėsite visus šablonus, priklausančius dabartiniam ir kitiems teikėjams.</span><span class="sxs-lookup"><span data-stu-id="a19f8-136">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="a19f8-137">Pasirinktas šablonas atidaromas ir jį galima redaguoti.</span><span class="sxs-lookup"><span data-stu-id="a19f8-137">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="a19f8-138">Redaguotas šablonas bus išsaugotas naujoje automatiškai sugeneruotoje ER formato konfigūracijoje.</span><span class="sxs-lookup"><span data-stu-id="a19f8-138">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a><span data-ttu-id="a19f8-139">Esamą „Excel” formatą naudojančio šablono įkėlimas</span><span class="sxs-lookup"><span data-stu-id="a19f8-139">Upload a template that uses an existing Excel format</span></span>
<span data-ttu-id="a19f8-140">Norėdami pateikti reikiamą informaciją prieš šablono įkėlimą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a19f8-140">Follow these steps to provide required information before you upload a template.</span></span>

1. <span data-ttu-id="a19f8-141">Darbo srityje **Verslo dokumentų valdymas** pasirinkite **Naujas dokumentas**.</span><span class="sxs-lookup"><span data-stu-id="a19f8-141">In the **Business document management** workspace, select **New document**.</span></span>

    ![Darbo sritis Verslo dokumentų valdymas](./media/BDM_overview_new_template1.png)
    
2. <span data-ttu-id="a19f8-143">Puslapio **Kurti naują šabloną** skirtuko **Įkelti** skirtuke **Šablonas** pasirinkite **Naršyti**, kad surastumėte ir pasirinktumėte „Excel” failą, kurį norite naudoti kaip šabloną.</span><span class="sxs-lookup"><span data-stu-id="a19f8-143">On the **Create a new template** page, on the **Upload** tab, on the **Template** tab, select **Browse** to find and select the Excel file that you want to use as a template.</span></span> <span data-ttu-id="a19f8-144">Skyriaus **Šablono** laukai **Pavadinimas** ir **Aprašas** yra užpildomi automatiškai.</span><span class="sxs-lookup"><span data-stu-id="a19f8-144">In the **Template** section, the **Title** and **Description** fields are automatically filled in.</span></span> <span data-ttu-id="a19f8-145">Jie nurodo naujos, automatiškai kuriamos, ER formato konfigūracijos pavadinimą ir aprašą.</span><span class="sxs-lookup"><span data-stu-id="a19f8-145">They specify the name and description of the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="a19f8-146">Prireikus galite redaguoti šiuos laukus.</span><span class="sxs-lookup"><span data-stu-id="a19f8-146">You can edit these fields as you require.</span></span>
3. <span data-ttu-id="a19f8-147">Skyriaus **Dokumento tipas** lauke **Pavadinimas** nurodykite verslo dokumento tipą.</span><span class="sxs-lookup"><span data-stu-id="a19f8-147">In the **Document Type** section, in the **Name** field, specify the type of business document.</span></span> <span data-ttu-id="a19f8-148">Ši reikšmė bus naudojama ieškoti tinkamam duomenų šaltiniui (tai yra, ER modelio konfigūracijai).</span><span class="sxs-lookup"><span data-stu-id="a19f8-148">This value will be used to search the correct data source (that is, the ER model configuration).</span></span>

    ![Šablono skirtukas](./media/BDM_overview_new_UI_import_21.jpg)

4. <span data-ttu-id="a19f8-150">Skirtuko **Duomenų šaltinis** „FastTab” **Filtras** pasirinkite **Taikyti filtrą**.</span><span class="sxs-lookup"><span data-stu-id="a19f8-150">On the **Data source** tab, on the **Filter** FastTab, select **Apply filter**.</span></span> <span data-ttu-id="a19f8-151">Skyriaus **Duomenų šaltinio** laukas **Pavadinimas** yra užpildomas automatiškai arba galite jo reikšmę pasirinkti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="a19f8-151">In the **Data source** section, the **Name** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="a19f8-152">Galite naudoti filtrą atitinkamam duomenų šaltinio vardui ieškoti pagal vardą, aprašą, šalies/regiono kodą ir verslo dokumento tipą.</span><span class="sxs-lookup"><span data-stu-id="a19f8-152">You can use the filter to search for the appropriate data source name by name, description, country/region code, and business document type.</span></span>

    ![Duomenų šaltinio skirtukas](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > <span data-ttu-id="a19f8-154">„FastTab” **Filtruoti** yra naudojamas ieškoti tinkamam duomenų šaltiniui (tai yra, ER modelio konfigūracijai).</span><span class="sxs-lookup"><span data-stu-id="a19f8-154">The **Filter** FastTab is used to search the correct data source (that is, the ER model configuration).</span></span> <span data-ttu-id="a19f8-155">Galite redaguoti visus filtro laukus, kad rastumėte tinkamiausią duomenų šaltinį įkeliamam dokumentui.</span><span class="sxs-lookup"><span data-stu-id="a19f8-155">You can edit all filter fields to find the most appropriate data source for the document that you're uploading.</span></span>
    > 
    > <span data-ttu-id="a19f8-156">„FastTab” **Filtruoti** esančios sąlygos yra naudojamos kaip **ARBA** sąlygos.</span><span class="sxs-lookup"><span data-stu-id="a19f8-156">The conditions on the **Filter** FastTab are used as **OR** conditions.</span></span>
    
5. <span data-ttu-id="a19f8-157">Skirtuke **Susiejimas** pasirinkite **Automatiškai aptikti**.</span><span class="sxs-lookup"><span data-stu-id="a19f8-157">On the **Mapping** tab, select **Auto detect**.</span></span> <span data-ttu-id="a19f8-158">Laukas **Šakninis aprašas** yra užpildomas automatiškai arba galite jo reikšmę pasirinkti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="a19f8-158">The **Root definition** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="a19f8-159">Šiame skirtuke rodomas galutinis šablono ir modelio elementų susiejimas.</span><span class="sxs-lookup"><span data-stu-id="a19f8-159">This tab shows the end mapping for the elements from the template and the model.</span></span>

    ![Susiejimo skirtukas](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > <span data-ttu-id="a19f8-161">Susiejimas skyriuje **Šablono struktūra** naudoja duomenų šaltinio žymų arba aprašų vartotojo kalba, esančių langelio pavadinime šablone, visišką atitiktį.</span><span class="sxs-lookup"><span data-stu-id="a19f8-161">The mapping in the **Template structure** section uses the full match of the labels or descriptions in the data source in the user's language, and in the cell name in the template.</span></span>

6. <span data-ttu-id="a19f8-162">Pasirinkite **Kurti dokumentą**, kad patvirtintumėte, jog norite sukurti šabloną ir pradėti redagavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="a19f8-162">Select **Create document** to confirm that you want to create a template and start the editing process.</span></span>

<span data-ttu-id="a19f8-163">Daugiau informacijos žr. [Verslo dokumentų valdymo apžvalga](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="a19f8-163">For more information, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="a19f8-164">Jeigu nėra tiekėjo Elektroninėse ataskaitose, jį galite sukurti.</span><span class="sxs-lookup"><span data-stu-id="a19f8-164">If there isn't a provider in Electronic reporting, you can create one.</span></span> <span data-ttu-id="a19f8-165">Jeigu nėra aktyvaus teikėjo, galite pasirinkti jį aktyvavimui.</span><span class="sxs-lookup"><span data-stu-id="a19f8-165">If there's no active provider, you can select to activate one.</span></span>

- <span data-ttu-id="a19f8-166">Norėdami sukurti teikėją, pakeiskite teikėjo pavadinimą lauke **Pavadinimas**, atnaujinkite naujo teikėjo internetinį adresą lauke **Internetinis adresas** ir pasirinkite **Gerai** patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="a19f8-166">To create a provider, change the name of the provider in the **Name** field, update the internet address of the new provider in the **Internet address** field, and select **OK** to confirm.</span></span>

    ![Naujo BDM teikėjo kūrimas](./media/bdm_create_provider.png)
    
- <span data-ttu-id="a19f8-168">Norėdami aktyvuoti esamą teikėją, pasirinkite teikėjo pavadinimą lauke **Konfigūracijos teikėjas** ir pasirinkite **Gerai**, kad nustatytumėte teikėją aktyviu.</span><span class="sxs-lookup"><span data-stu-id="a19f8-168">To activate existing provider, choose the name of the provider in the **Configuration provider** field, and select **OK** to set provider as active.</span></span>

    ![BDM teikėjo aktyvavimas](./media/bdm_choose_provider.png)

> [!NOTE]
> <span data-ttu-id="a19f8-170">Kiekvienas BDM šablonas kreipiasi į teikėją kaip į konfigūracijos autorių.</span><span class="sxs-lookup"><span data-stu-id="a19f8-170">Each BDM template refers to the provider as the author of the configuration.</span></span> <span data-ttu-id="a19f8-171">Štai todėl šablonui reikia aktyvaus teikėjo.</span><span class="sxs-lookup"><span data-stu-id="a19f8-171">This is why an active provider is required for the template.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
