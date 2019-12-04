---
title: Failų importavimas XML formatu su pasirinktiniais atributais
description: Šioje temoje pateikiama informacija apie tai, kaip kuriami ER formatai, kurie nurodo XML atributus, kad būtų analizuojami gaunami elektroniniai dokumentai XML formatu.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5e2989906c5aa3ead9e46b8ed5333e880e5cf1c6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769952"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="1adde-103">Failų importavimas XML formatu su pasirinktiniais atributais</span><span class="sxs-lookup"><span data-stu-id="1adde-103">Import files in XML format with optional attributes</span></span>

<span data-ttu-id="1adde-104">Galite sukurti elektroninių ataskaitų (ER) formatus, skirtus analizuoti gaunamus elektroninius dokumentus XML formatu.</span><span class="sxs-lookup"><span data-stu-id="1adde-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="1adde-105">Sukurtame ER formate tam tikri XML elementų atributai gali būti nurodyti kaip pasirinktiniai.</span><span class="sxs-lookup"><span data-stu-id="1adde-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="1adde-106">Taigi galėsite tinkamai tvarkyti gaunamus failus naudodami tokius XML atributus arba jų nenaudodami.</span><span class="sxs-lookup"><span data-stu-id="1adde-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="1adde-107">Tada galite naudoti šių failų turinį programos duomenims atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="1adde-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="1adde-108">Norėdami daugiau sužinoti apie šią funkciją, atlikite veiksmus, aprašytus temoje [(RCS) XML formato failų su pasirinktiniais atributais importavimas](tasks/import-files-xml-format-optional-attributes.md), kuri yra verslo proceso 7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677) dalis.</span><span class="sxs-lookup"><span data-stu-id="1adde-108">To learn more about this feature, complete the steps in the topic, [(RCS) Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="1adde-109">Šį užduočių vedlį ir susietus failų pavyzdžius galite atsisiųsti iš [„Microsoft“ atsisiuntimo centras](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="1adde-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="1adde-110">Turinio aprašas</span><span class="sxs-lookup"><span data-stu-id="1adde-110">Content description</span></span>       | <span data-ttu-id="1adde-111">Failas</span><span class="sxs-lookup"><span data-stu-id="1adde-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="1adde-112">Failo pavyzdys XML formatu</span><span class="sxs-lookup"><span data-stu-id="1adde-112">Sample file in XML format</span></span> | <span data-ttu-id="1adde-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="1adde-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="1adde-114">Užduočių vedikliai</span><span class="sxs-lookup"><span data-stu-id="1adde-114">Task guide</span></span>                | <span data-ttu-id="1adde-115">RCS XML formato failų su pasirinktiniais atributais importavimas.axtr</span><span class="sxs-lookup"><span data-stu-id="1adde-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="1adde-116">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali kurti ER formato konfigūraciją, naudojamą importuojant XML formato failus, kuriuose yra pasirinktinių atributų.</span><span class="sxs-lookup"><span data-stu-id="1adde-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="1adde-117">Norint atlikti šiuos veiksmus, pirmiausia reikia atlikti veiksmus, nurodytus procedūroje [Sukurti konfigūracijų teikėjus ir juos pažymėti kaip aktyvius](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="1adde-117">To complete these steps, you must first complete the steps in the procedure, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="1adde-118">Prieš pradėdami, atsisiųskite ir vietiniame diske išsaugokite failą IncomingDocumentToLearnHowToHandleOptionalAttributes.xml iš „Microsoft“ atsisiuntimo centro (https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="1adde-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="1adde-119">Eikite į **Organizacijos administravimas** > **Darbo sritys** > **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="1adde-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="1adde-120">Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip **Aktyvus**.</span><span class="sxs-lookup"><span data-stu-id="1adde-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="1adde-121">Jei nematote šio konfigūracijos teikėjo, atlikite veiksmus, nurodytus temoje [Sukurti konfigūracijų teikėjus ir juos pažymėti kaip aktyvius](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="1adde-121">If you don’t see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="1adde-122">Spustelėkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="1adde-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="1adde-123">Sukurti naują duomenų modelio konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="1adde-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="1adde-124">Spustelėdami **Kurti konfigūraciją**, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1adde-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="1adde-125">Lauke **Pavadinimas** įveskite „xml failo importavimo modelis“.</span><span class="sxs-lookup"><span data-stu-id="1adde-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="1adde-126">Spustelėkite **Sukurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="1adde-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="1adde-127">Spustelėkite **Konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="1adde-127">Click **Designer**.</span></span>
5. <span data-ttu-id="1adde-128">Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1adde-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="1adde-129">Lauke **Pavadinimas** įveskite „Šaknis“.</span><span class="sxs-lookup"><span data-stu-id="1adde-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="1adde-130">Spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="1adde-130">Click **Add**.</span></span>
8. <span data-ttu-id="1adde-131">Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1adde-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="1adde-132">Lauke **Pavadinimas** įveskite „Sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="1adde-132">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="1adde-133">Lauke **Elemento tipas** pasirinkite **Įrašų sąrašas**.</span><span class="sxs-lookup"><span data-stu-id="1adde-133">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="1adde-134">Spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="1adde-134">Click **Add**.</span></span>
12. <span data-ttu-id="1adde-135">Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1adde-135">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="1adde-136">Lauke **Pavadinimas** įveskite „Kodas“.</span><span class="sxs-lookup"><span data-stu-id="1adde-136">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="1adde-137">Lauke **Elemento tipas** pasirinkite **Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="1adde-137">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="1adde-138">Spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="1adde-138">Click **Add**.</span></span>
16. <span data-ttu-id="1adde-139">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1adde-139">Click **Save**.</span></span>
17. <span data-ttu-id="1adde-140">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1adde-140">Close the page.</span></span>
18. <span data-ttu-id="1adde-141">Spustelėkite **Keisti būseną**.</span><span class="sxs-lookup"><span data-stu-id="1adde-141">Click **Change status**.</span></span>
19. <span data-ttu-id="1adde-142">Spustelėkite **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="1adde-142">Click **Complete**.</span></span>
20. <span data-ttu-id="1adde-143">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1adde-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="1adde-144">Duomenų importavimo formato kūrimas</span><span class="sxs-lookup"><span data-stu-id="1adde-144">Create a format for data import</span></span>
1. <span data-ttu-id="1adde-145">Spustelėdami **Kurti konfigūraciją**, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1adde-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="1adde-146">Lauke **Naujas** įveskite „Formatas pagal duomenų modelį xml failo importavimo modelis“.</span><span class="sxs-lookup"><span data-stu-id="1adde-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="1adde-147">Lauke **Pavadinimas** įveskite „xml failo importavimo formatas“.</span><span class="sxs-lookup"><span data-stu-id="1adde-147">In the **Nam**e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="1adde-148">Lauke **Palaikomas duomenų importavimas** pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="1adde-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="1adde-149">Spustelėkite **Sukurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="1adde-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="1adde-150">Formato, skirto analizuoti gaunamą XML formato failą, kūrimas</span><span class="sxs-lookup"><span data-stu-id="1adde-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="1adde-151">Spustelėkite **Konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="1adde-151">Click **Designer**.</span></span>
2. <span data-ttu-id="1adde-152">Spustelėdami **Įtraukti šakninį elementą** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1adde-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="1adde-153">Medyje pasirinkite **XML \ Elementas**.</span><span class="sxs-lookup"><span data-stu-id="1adde-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="1adde-154">Lauke **Pavadinimas** įveskite „šaknis“.</span><span class="sxs-lookup"><span data-stu-id="1adde-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="1adde-155">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1adde-155">Click **OK**.</span></span>
6. <span data-ttu-id="1adde-156">Spustelėdami **Įtraukti** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1adde-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="1adde-157">Medyje pasirinkite **XML \ Elementas**.</span><span class="sxs-lookup"><span data-stu-id="1adde-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="1adde-158">Lauke **Pavadinimas** įveskite „dokumentas“.</span><span class="sxs-lookup"><span data-stu-id="1adde-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="1adde-159">Lauke **Daugialypumas** pasirinkite **Vienas daug**.</span><span class="sxs-lookup"><span data-stu-id="1adde-159">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="1adde-160">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1adde-160">Click **OK**.</span></span>
11. <span data-ttu-id="1adde-161">Medyje pasirinkite **root\document**.</span><span class="sxs-lookup"><span data-stu-id="1adde-161">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="1adde-162">Spustelėdami **Įtraukti** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1adde-162">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="1adde-163">Medyje pasirinkite **XML \ Atributas**.</span><span class="sxs-lookup"><span data-stu-id="1adde-163">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="1adde-164">Lauke **Pavadinimas** įveskite „id“.</span><span class="sxs-lookup"><span data-stu-id="1adde-164">In the **Name** field, type 'id'.</span></span>
15. <span data-ttu-id="1adde-165">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1adde-165">Click **OK**.</span></span>
16. <span data-ttu-id="1adde-166">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1adde-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="1adde-167">Formato susiejimo, skirto įrašyti išanalizuotą informaciją į duomenų modelį, kūrimas</span><span class="sxs-lookup"><span data-stu-id="1adde-167">Design a format mapping to save parsed information to data model</span></span>
1.  <span data-ttu-id="1adde-168">Spustelėkite **Susieti formatą su modeliu**.</span><span class="sxs-lookup"><span data-stu-id="1adde-168">Click **Map format to model**.</span></span>
2.  <span data-ttu-id="1adde-169">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1adde-169">Click **New**.</span></span>
3.  <span data-ttu-id="1adde-170">Lauke **Apibrėžtis** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1adde-170">In the **Definition** field, enter or select a value.</span></span>
4.  <span data-ttu-id="1adde-171">Lauke **Pavadinimas** įveskite „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="1adde-171">In the **Name** field, type 'Mapping'.</span></span>
5.  <span data-ttu-id="1adde-172">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1adde-172">Click **Save**.</span></span>
6.  <span data-ttu-id="1adde-173">Spustelėkite **Konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="1adde-173">Click **Designer**.</span></span>
7.  <span data-ttu-id="1adde-174">Medyje išplėskite **format**.</span><span class="sxs-lookup"><span data-stu-id="1adde-174">In the tree, expand **format**.</span></span>
8.  <span data-ttu-id="1adde-175">Medyje išplėskite **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="1adde-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.  <span data-ttu-id="1adde-176">Medyje pasirinkite \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="1adde-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="1adde-177">(dokumentas)\*\*.</span><span class="sxs-lookup"><span data-stu-id="1adde-177">(document)\*\*.</span></span>
10. <span data-ttu-id="1adde-178">Spustelėkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="1adde-178">Click **Bind**.</span></span>
11. <span data-ttu-id="1adde-179">Medyje išplėskite \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="1adde-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="1adde-180">(dokumentas)\*\*.</span><span class="sxs-lookup"><span data-stu-id="1adde-180">(document)\*\*.</span></span>
12. <span data-ttu-id="1adde-181">Medyje pasirinkite \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="1adde-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="1adde-182">(dokumentas)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="1adde-182">(document)\id\*\*.</span></span>
13. <span data-ttu-id="1adde-183">Medyje išplėskite **List = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="1adde-183">In the tree, expand **List = format.root.document**.</span></span>
14. <span data-ttu-id="1adde-184">Medyje pasirinkite **List = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="1adde-184">In the tree, select **List = format.root.document\Code**.</span></span>
15. <span data-ttu-id="1adde-185">Spustelėkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="1adde-185">Click **Bind**.</span></span>
16. <span data-ttu-id="1adde-186">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1adde-186">Click **Save**.</span></span>
17. <span data-ttu-id="1adde-187">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1adde-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="1adde-188">Formato susiejimo vykdymas</span><span class="sxs-lookup"><span data-stu-id="1adde-188">Run format mapping</span></span>
1. <span data-ttu-id="1adde-189">Spustelėkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="1adde-189">Click **Run**.</span></span>
2. <span data-ttu-id="1adde-190">Spustelėkite **Naršyti** ir pasirinkite failą **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="1adde-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="1adde-191">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1adde-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="1adde-192">Pasirinktas failas nebuvo importuotas, nes kuriant formatus manoma, kad esama elemento „dokumentas“ atributo „id“, bet importuotame faile tokio atributo nėra.</span><span class="sxs-lookup"><span data-stu-id="1adde-192">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="1adde-193">Formato struktūros, skirtos tvarkyti XML atributą kaip pasirinktinį, modifikavimas</span><span class="sxs-lookup"><span data-stu-id="1adde-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="1adde-194">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1adde-194">Close the page.</span></span>
2. <span data-ttu-id="1adde-195">Medyje išplėskite **root\document**.</span><span class="sxs-lookup"><span data-stu-id="1adde-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="1adde-196">Medyje pasirinkite **root\document\id**.</span><span class="sxs-lookup"><span data-stu-id="1adde-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="1adde-197">Lauke **Tuščia trūkstamo atributo eilutė** pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="1adde-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="1adde-198">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1adde-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="1adde-199">Formato susiejimo vykdymas siekiant patikrinti keitimus</span><span class="sxs-lookup"><span data-stu-id="1adde-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="1adde-200">Spustelėkite **Susieti formatą su modeliu**.</span><span class="sxs-lookup"><span data-stu-id="1adde-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="1adde-201">Spustelėkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="1adde-201">Click **Run**.</span></span>
3. <span data-ttu-id="1adde-202">Spustelėkite **Naršyti** ir pasirinkite failą **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="1adde-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="1adde-203">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1adde-203">Click **OK**.</span></span>
5. <span data-ttu-id="1adde-204">Peržiūrėkite sugeneruotą failą.</span><span class="sxs-lookup"><span data-stu-id="1adde-204">Review the generated file.</span></span> <span data-ttu-id="1adde-205">Atkreipkite dėmesį, kad tas pats failas buvo importuotas kaip formato dizainas. Dabar elemento „dokumentas“ atributą „ID“ laikykite pasirinktinu.</span><span class="sxs-lookup"><span data-stu-id="1adde-205">Note that same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
