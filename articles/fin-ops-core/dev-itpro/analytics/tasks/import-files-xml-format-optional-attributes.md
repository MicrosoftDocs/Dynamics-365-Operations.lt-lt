---
title: (RCS) Failų importavimas XML formatu su pasirinktiniais atributais
description: Šioje temoje pateikiama informacija apie tai, kaip vartotojas gali kurti ER formato konfigūraciją ir XML formatu importuoti failus, kuriuose yra pasirinktinių atributų.
author: NickSelin
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1290598d8dbd5b72d679ccf3e642e75b6dc3215
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182191"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="750b5-103">(RCS) Failų importavimas XML formatu su pasirinktiniais atributais</span><span class="sxs-lookup"><span data-stu-id="750b5-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="750b5-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali kurti ER formato konfigūraciją, naudojamą importuojant XML formato failus, kuriuose yra pasirinktinių atributų.</span><span class="sxs-lookup"><span data-stu-id="750b5-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="750b5-105">Norėdami atlikti šiuos veiksmus, pirmiausia turite juos užbaigti procedūroje „Sukurti konfigūracijos teikėją ir pažymėti jį kaip aktyvų“.</span><span class="sxs-lookup"><span data-stu-id="750b5-105">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="750b5-106">Prieš pradėdami, atsisiųskite ir vietiniame diske išsaugokite failą IncomingDocumentToLearnHowToHandleOptionalAttributes.xml iš [„Microsoft“ atsisiuntimo centro](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="750b5-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.  <span data-ttu-id="750b5-107">Eikite į **Visos darbo sritys** > **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="750b5-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.  <span data-ttu-id="750b5-108">Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip **Aktyvus**.</span><span class="sxs-lookup"><span data-stu-id="750b5-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="750b5-109">Jei nematote šio konfigūracijos teikėjo, atlikite procedūros [Sukurti konfigūracijų teikėją ir jį pažymėti kaip aktyvų](er-configuration-provider-mark-it-active-2016-11.md) veiksmus.</span><span class="sxs-lookup"><span data-stu-id="750b5-109">If you don’t see this configuration provider, complete the steps in the procedure [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.  <span data-ttu-id="750b5-110">Spustelėkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="750b5-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="750b5-111">Sukurti naują duomenų modelio konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="750b5-111">Create a new data model configuration</span></span>
1.  <span data-ttu-id="750b5-112">Spustelėdami **Kurti konfigūraciją**, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="750b5-112">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="750b5-113">Lauke **Pavadinimas** įveskite „xml failo importavimo modelis“.</span><span class="sxs-lookup"><span data-stu-id="750b5-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.  <span data-ttu-id="750b5-114">Spustelėkite **Sukurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="750b5-114">Click **Create configuration**.</span></span>
4.  <span data-ttu-id="750b5-115">Spustelėkite **Konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="750b5-115">Click **Designer**.</span></span>
5.  <span data-ttu-id="750b5-116">Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="750b5-116">Click **New** to open the drop dialog.</span></span>
6.  <span data-ttu-id="750b5-117">Lauke **Pavadinimas** įveskite „Šaknis“.</span><span class="sxs-lookup"><span data-stu-id="750b5-117">In the **Name** field, type 'Root'.</span></span>
7.  <span data-ttu-id="750b5-118">Spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="750b5-118">Click **Add**.</span></span>
8.  <span data-ttu-id="750b5-119">Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="750b5-119">Click **New** to open the drop dialog.</span></span>
9.  <span data-ttu-id="750b5-120">Lauke **Pavadinimas** įveskite „Sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="750b5-120">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="750b5-121">Lauke **Elemento tipas** pasirinkite **Įrašų sąrašas**.</span><span class="sxs-lookup"><span data-stu-id="750b5-121">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="750b5-122">Spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="750b5-122">Click **Add**.</span></span>
12. <span data-ttu-id="750b5-123">Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="750b5-123">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="750b5-124">Lauke **Pavadinimas** įveskite „Kodas“.</span><span class="sxs-lookup"><span data-stu-id="750b5-124">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="750b5-125">Lauke **Elemento tipas** pasirinkite **Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="750b5-125">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="750b5-126">Spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="750b5-126">Click **Add**.</span></span>
16. <span data-ttu-id="750b5-127">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="750b5-127">Click **Save**.</span></span>
17. <span data-ttu-id="750b5-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="750b5-128">Close the page.</span></span>
18. <span data-ttu-id="750b5-129">Spustelėkite **Keisti būseną**.</span><span class="sxs-lookup"><span data-stu-id="750b5-129">Click **Change status**.</span></span>
19. <span data-ttu-id="750b5-130">Spustelėkite **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="750b5-130">Click **Complete**.</span></span>
20. <span data-ttu-id="750b5-131">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="750b5-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="750b5-132">Duomenų importavimo formato kūrimas</span><span class="sxs-lookup"><span data-stu-id="750b5-132">Create a format for data import</span></span>
1.  <span data-ttu-id="750b5-133">Spustelėdami **Kurti konfigūraciją**, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="750b5-133">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="750b5-134">Lauke **Naujas** įveskite „Formatas pagal duomenų modelį xml failo importavimo modelis“.</span><span class="sxs-lookup"><span data-stu-id="750b5-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.  <span data-ttu-id="750b5-135">Lauke **Pavadinimas** įveskite „XML failo importavimo formatas“.</span><span class="sxs-lookup"><span data-stu-id="750b5-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.  <span data-ttu-id="750b5-136">Lauke **Palaikomas duomenų importavimas** pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="750b5-136">Select **Yes** in the **Supports data import** field.</span></span>
5.  <span data-ttu-id="750b5-137">Spustelėkite **Sukurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="750b5-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="750b5-138">Formato, skirto analizuoti gaunamą XML formato failą, kūrimas</span><span class="sxs-lookup"><span data-stu-id="750b5-138">Design a format to parse incoming file in xml format</span></span>
1.  <span data-ttu-id="750b5-139">Spustelėkite **Konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="750b5-139">Click **Designer**.</span></span>
2.  <span data-ttu-id="750b5-140">Spustelėdami **Įtraukti šakninį elementą** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="750b5-140">Click **Add root** to open the drop dialog.</span></span>
3.  <span data-ttu-id="750b5-141">Medyje pasirinkite **XML \ Elementas**.</span><span class="sxs-lookup"><span data-stu-id="750b5-141">In the tree, select **XML\Element**.</span></span>
4.  <span data-ttu-id="750b5-142">Lauke **Pavadinimas** įveskite „šaknis“.</span><span class="sxs-lookup"><span data-stu-id="750b5-142">In the **Name** field, type 'root'.</span></span>
5.  <span data-ttu-id="750b5-143">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="750b5-143">Click **OK**.</span></span>
6.  <span data-ttu-id="750b5-144">Spustelėdami **Įtraukti** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="750b5-144">Click **Add** to open the drop dialog.</span></span>
7.  <span data-ttu-id="750b5-145">Medyje pasirinkite **XML \ Elementas**.</span><span class="sxs-lookup"><span data-stu-id="750b5-145">In the tree, select **XML\Element**.</span></span>
8.  <span data-ttu-id="750b5-146">Lauke **Pavadinimas** įveskite „dokumentas“.</span><span class="sxs-lookup"><span data-stu-id="750b5-146">In the **Name** field, type 'document'.</span></span>
9.  <span data-ttu-id="750b5-147">Lauke **Daugialypumas** pasirinkite **Vienas daug**.</span><span class="sxs-lookup"><span data-stu-id="750b5-147">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="750b5-148">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="750b5-148">Click **OK**.</span></span>
11. <span data-ttu-id="750b5-149">Medyje pasirinkite **root\document**.</span><span class="sxs-lookup"><span data-stu-id="750b5-149">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="750b5-150">Spustelėdami **Įtraukti** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="750b5-150">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="750b5-151">Medyje pasirinkite **XML \ Atributas**.</span><span class="sxs-lookup"><span data-stu-id="750b5-151">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="750b5-152">Lauke **Pavadinimas** įveskite „ID“.</span><span class="sxs-lookup"><span data-stu-id="750b5-152">In the **Name** field, type 'ID'.</span></span>
15. <span data-ttu-id="750b5-153">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="750b5-153">Click **OK**.</span></span>
16. <span data-ttu-id="750b5-154">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="750b5-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="750b5-155">Formato susiejimo, skirto įrašyti išanalizuotą informaciją į duomenų modelį, kūrimas</span><span class="sxs-lookup"><span data-stu-id="750b5-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="750b5-156">Spustelėkite **Susieti formatą su modeliu**.</span><span class="sxs-lookup"><span data-stu-id="750b5-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="750b5-157">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="750b5-157">Click **New**.</span></span>
3. <span data-ttu-id="750b5-158">Lauke **Apibrėžtis** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="750b5-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="750b5-159">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="750b5-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="750b5-160">Lauke **Pavadinimas** įveskite „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="750b5-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="750b5-161">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="750b5-161">Click **Save**.</span></span>
7. <span data-ttu-id="750b5-162">Spustelėkite **Konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="750b5-162">Click **Designer**.</span></span>
8. <span data-ttu-id="750b5-163">Medyje išplėskite **format**.</span><span class="sxs-lookup"><span data-stu-id="750b5-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="750b5-164">Medyje išplėskite **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="750b5-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10. <span data-ttu-id="750b5-165">Medyje pasirinkite \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="750b5-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="750b5-166">(dokumentas)\*\*.</span><span class="sxs-lookup"><span data-stu-id="750b5-166">(document)\*\*.</span></span>
11. <span data-ttu-id="750b5-167">Spustelėkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="750b5-167">Click **Bind**.</span></span>
12. <span data-ttu-id="750b5-168">Medyje išplėskite \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="750b5-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="750b5-169">(dokumentas)\*\*.</span><span class="sxs-lookup"><span data-stu-id="750b5-169">(document)\*\*.</span></span>
13. <span data-ttu-id="750b5-170">Medyje pasirinkite \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="750b5-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="750b5-171">(dokumentas)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="750b5-171">(document)\id\*\*.</span></span>
14. <span data-ttu-id="750b5-172">Medyje išplėskite **List = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="750b5-172">In the tree, expand **List = format.root.document**.</span></span>
15. <span data-ttu-id="750b5-173">Medyje pasirinkite **List = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="750b5-173">In the tree, select **List = format.root.document\Code**.</span></span>
16. <span data-ttu-id="750b5-174">Spustelėkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="750b5-174">Click **Bind**.</span></span>
17. <span data-ttu-id="750b5-175">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="750b5-175">Click **Save**.</span></span>
18. <span data-ttu-id="750b5-176">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="750b5-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="750b5-177">Formato susiejimo vykdymas</span><span class="sxs-lookup"><span data-stu-id="750b5-177">Run format mapping</span></span>
1. <span data-ttu-id="750b5-178">Spustelėkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="750b5-178">Click **Run**.</span></span>
2. <span data-ttu-id="750b5-179">Spustelėkite **Naršyti** ir pasirinkite **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="750b5-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="750b5-180">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="750b5-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="750b5-181">Pasirinktas failas nebuvo importuotas, nes kuriant formatus manoma, kad esama elemento „dokumentas“ atributo „id“, bet importuotame faile tokio atributo nėra.</span><span class="sxs-lookup"><span data-stu-id="750b5-181">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="750b5-182">Formato struktūros, skirtos tvarkyti XML atributą kaip pasirinktinį, modifikavimas</span><span class="sxs-lookup"><span data-stu-id="750b5-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="750b5-183">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="750b5-183">Close the page.</span></span>
2. <span data-ttu-id="750b5-184">Medyje išplėskite **root\document**.</span><span class="sxs-lookup"><span data-stu-id="750b5-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="750b5-185">Medyje pasirinkite **root\document\id**.</span><span class="sxs-lookup"><span data-stu-id="750b5-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="750b5-186">Lauke **Tuščia trūkstamo atributo eilutė** pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="750b5-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="750b5-187">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="750b5-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="750b5-188">Formato susiejimo vykdymas siekiant patikrinti keitimus</span><span class="sxs-lookup"><span data-stu-id="750b5-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="750b5-189">Spustelėkite **Susieti formatą su modeliu**.</span><span class="sxs-lookup"><span data-stu-id="750b5-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="750b5-190">Spustelėkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="750b5-190">Click **Run**.</span></span>
3. <span data-ttu-id="750b5-191">Spustelėkite **Naršyti** ir pasirinkite failą **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="750b5-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="750b5-192">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="750b5-192">Click **OK**.</span></span>
5. <span data-ttu-id="750b5-193">Peržiūrėkite sugeneruotą failą.</span><span class="sxs-lookup"><span data-stu-id="750b5-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="750b5-194">Tas pats failas buvo importuotas kaip formato dizainas. Dabar elemento „dokumentas“ atributą „ID“ laikykite pasirinktinu.</span><span class="sxs-lookup"><span data-stu-id="750b5-194">The same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
