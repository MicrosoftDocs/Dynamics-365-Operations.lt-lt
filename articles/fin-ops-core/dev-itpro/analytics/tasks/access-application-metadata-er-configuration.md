---
title: Prieiga prie programos metaduomenų naudojant ER konfigūraciją
description: Šioje temoje paaiškinama, kaip „Regulatory configuration service“ vartotojas gali kurti naują elektroninės ataskaitos modelio susiejimą naudodamas metaduomenis.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58697148ecf83f4962bd64a221945b6d911e11a6
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093310"
---
# <a name="access-application-metadata-by-using-er-configuration"></a><span data-ttu-id="df82f-103">Prieiga prie programos metaduomenų naudojant ER konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="df82f-103">Access application metadata by using ER configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="df82f-104">Toliau nurodyti veiksmai paaiškina, kaip „Regulatory configuration service“ (RCS) vartotojas, turintis sistemos administratoriaus arba elektroninės ataskaitos kūrėjo vaidmenį, gali kurti naują elektroninės ataskaitos (ER) modelio susiejimą naudodamas programos metaduomenis.</span><span class="sxs-lookup"><span data-stu-id="df82f-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using the application metadata.</span></span> <span data-ttu-id="df82f-105">Programos metaduomenys bus pasiekiami naudojant ER metaduomenų konfigūraciją, kurioje yra metaduomenų pavyzdžių rinkinys, skirtas užsienio prekybos operacijoms pasiekti.</span><span class="sxs-lookup"><span data-stu-id="df82f-105">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span> <span data-ttu-id="df82f-106">Norint atlikti šiuos veiksmus, pirmiausia RCS reikia atlikti temos [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md) procedūros veiksmus.</span><span class="sxs-lookup"><span data-stu-id="df82f-106">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> <span data-ttu-id="df82f-107">Tada reikia atlikti temoje [Programos metaduomenų, kurie bus naudojami RCS, paruošimas](prepare-application-metadata-rcs.md) nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="df82f-107">Then complete the steps in the topic, [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="df82f-108">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="df82f-108">Prerequisites</span></span>
1. <span data-ttu-id="df82f-109">Eikite į **Visos darbo sritys** > **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="df82f-109">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="df82f-110">Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip **Aktyvus**.</span><span class="sxs-lookup"><span data-stu-id="df82f-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="df82f-111">Jei nematote šio konfigūracijos teikėjo, atlikite procedūros [Sukurti konfigūracijų teikėjus ir juos pažymėti kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md) veiksmus.</span><span class="sxs-lookup"><span data-stu-id="df82f-111">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="import-metadata-configuration"></a><span data-ttu-id="df82f-112">Metaduomenų konfigūracijos importavimas</span><span class="sxs-lookup"><span data-stu-id="df82f-112">Import metadata configuration</span></span> 
1. <span data-ttu-id="df82f-113">Spustelėkite **Metaduomenų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="df82f-113">Click **Metadata configurations**.</span></span> 
2. <span data-ttu-id="df82f-114">Importuokite ER metaduomenų konfigūraciją, kurioje yra metaduomenys, kurie sukonfigūruoti generuoti elektroninius dokumentus, skirtus užsienio prekybos įmonėms.</span><span class="sxs-lookup"><span data-stu-id="df82f-114">Import the ER metadata configuration that contains metadata that has been configured to generate electronic documents for foreign trade business.</span></span> <span data-ttu-id="df82f-115">Ši ER metaduomenų konfigūracija eksportuota kaip XML failas ir atlikti [Programos metaduomenų, kurie bus naudojami RCS, paruošimas](prepare-application-metadata-rcs.md) procedūros veiksmai.</span><span class="sxs-lookup"><span data-stu-id="df82f-115">This ER metadata configuration has been exported as XML file while the steps in the [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md) procedure have been completed.</span></span> 
3. <span data-ttu-id="df82f-116">Spustelėkite **Keitimas**.</span><span class="sxs-lookup"><span data-stu-id="df82f-116">Click **Exchange**.</span></span> 
4. <span data-ttu-id="df82f-117">Spustelėkite **Įkelti iš XML failo**.</span><span class="sxs-lookup"><span data-stu-id="df82f-117">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="df82f-118">Spustelėkite **Naršyti** ir pasirinkite failą Užsienio prekybos metaduomenys.xml.</span><span class="sxs-lookup"><span data-stu-id="df82f-118">Click **Browse** and select the 'Foreign trade metadata.xml' file.</span></span> 
6. <span data-ttu-id="df82f-119">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="df82f-119">Click **OK**.</span></span> 
7. <span data-ttu-id="df82f-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="df82f-120">Close the page.</span></span> 

## <a name="create-data-model-configuration"></a><span data-ttu-id="df82f-121">Duomenų modelio konfigūracijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="df82f-121">Create data model configuration</span></span>
1. <span data-ttu-id="df82f-122">Spustelėkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="df82f-122">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="df82f-123">Spustelėdami **Kurti konfigūraciją**, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="df82f-123">Click **Create configuration** to open the drop dialog.</span></span> 
3. <span data-ttu-id="df82f-124">Lauke **Pavadinimas** įveskite Užsienio prekybos modelis.</span><span class="sxs-lookup"><span data-stu-id="df82f-124">In the **Name** field, type 'Foreign trade model'.</span></span> 
4. <span data-ttu-id="df82f-125">Spustelėkite **Sukurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="df82f-125">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="df82f-126">Spustelėkite **Konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="df82f-126">Click **Designer**.</span></span> 
6. <span data-ttu-id="df82f-127">Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="df82f-127">Click **New** to open the drop dialog.</span></span> 
7. <span data-ttu-id="df82f-128">Lauke **Pavadinimas** įveskite „Šaknis“.</span><span class="sxs-lookup"><span data-stu-id="df82f-128">In the **Name** field, type 'Root'.</span></span> 
8. <span data-ttu-id="df82f-129">Spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="df82f-129">Click **Add**.</span></span> 
9. <span data-ttu-id="df82f-130">Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="df82f-130">Click **New** to open the drop dialog.</span></span> 
10.    <span data-ttu-id="df82f-131">Lauke **Pavadinimas** įveskite Operacija.</span><span class="sxs-lookup"><span data-stu-id="df82f-131">In the **Name** field, type 'Transaction'.</span></span> 
11.    <span data-ttu-id="df82f-132">Lauke **Elemento tipas** pasirinkite **Įrašų sąrašas**.</span><span class="sxs-lookup"><span data-stu-id="df82f-132">In the **Item type** field, select **Record list**.</span></span> 
12.    <span data-ttu-id="df82f-133">Spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="df82f-133">Click **Add**.</span></span> 
13.    <span data-ttu-id="df82f-134">Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="df82f-134">Click **New** to open the drop dialog.</span></span> 
14.    <span data-ttu-id="df82f-135">Lauke **Pavadinimas** įveskite Prekės kodas.</span><span class="sxs-lookup"><span data-stu-id="df82f-135">In the **Name** field, type 'Commodity code'.</span></span> 
15.    <span data-ttu-id="df82f-136">Lauke **Elemento tipas** pasirinkite **Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="df82f-136">In the **Item type** field, select **String**.</span></span> 
16.    <span data-ttu-id="df82f-137">Spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="df82f-137">Click **Add**.</span></span> 
17.    <span data-ttu-id="df82f-138">Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="df82f-138">Click **New** to open the drop dialog.</span></span> 
18.    <span data-ttu-id="df82f-139">Lauke **Pavadinimas** įveskite Sąskaitos faktūros suma.</span><span class="sxs-lookup"><span data-stu-id="df82f-139">In the **Name** field, type 'Invoiced amount'.</span></span> 
19.    <span data-ttu-id="df82f-140">Lauke **Elemento tipas** pasirinkite **Realusis skaičius**.</span><span class="sxs-lookup"><span data-stu-id="df82f-140">In the **Item type** field, select **Real**.</span></span> 
20.    <span data-ttu-id="df82f-141">Spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="df82f-141">Click **Add**.</span></span> 
21.    <span data-ttu-id="df82f-142">Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="df82f-142">Click **New** to open the drop dialog.</span></span> 
22.    <span data-ttu-id="df82f-143">Lauke **Pavadinimas** įveskite Data.</span><span class="sxs-lookup"><span data-stu-id="df82f-143">In the **Name** field, type 'Date'.</span></span> 
23.    <span data-ttu-id="df82f-144">Lauke **Elemento tipas** pasirinkite **Data**.</span><span class="sxs-lookup"><span data-stu-id="df82f-144">In the **Item type** field, select **Date**.</span></span> 
24.    <span data-ttu-id="df82f-145">Spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="df82f-145">Click **Add**.</span></span> 
25.    <span data-ttu-id="df82f-146">Spustelėkite **Šakninė nuoroda**.</span><span class="sxs-lookup"><span data-stu-id="df82f-146">Click **Root reference**.</span></span> 
26.    <span data-ttu-id="df82f-147">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="df82f-147">Click **OK**.</span></span> 
27.    <span data-ttu-id="df82f-148">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="df82f-148">Click **Save**.</span></span> 
28.    <span data-ttu-id="df82f-149">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="df82f-149">Close the page.</span></span> 
29.    <span data-ttu-id="df82f-150">Spustelėkite **Keisti būseną**.</span><span class="sxs-lookup"><span data-stu-id="df82f-150">Click **Change status**.</span></span> 
30.    <span data-ttu-id="df82f-151">Spustelėkite **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="df82f-151">Click **Complete**.</span></span> 
31.    <span data-ttu-id="df82f-152">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="df82f-152">Click **OK**.</span></span> 

## <a name="create-model-mapping-configuration"></a><span data-ttu-id="df82f-153">Modelio susiejimo konfigūracijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="df82f-153">Create model mapping configuration</span></span> 
1. <span data-ttu-id="df82f-154">Spustelėdami **Kurti konfigūraciją**, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="df82f-154">Click **Create configuration** to open the drop dialog.</span></span> 
2. <span data-ttu-id="df82f-155">Lauke **Naujas** įveskite Modelio susiejimas remiantis duomenų modeliu Užsienio prekybos modelis.</span><span class="sxs-lookup"><span data-stu-id="df82f-155">In the **New** field, enter 'Model Mapping based on data model Foreign trade model'.</span></span> 
3. <span data-ttu-id="df82f-156">Lauke **Pavadinimas** įveskite Užsienio prekybos susiejimas.</span><span class="sxs-lookup"><span data-stu-id="df82f-156">In the **Name** field, type 'Foreign trade mapping'.</span></span> 
4. <span data-ttu-id="df82f-157">Spustelėkite **Sukurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="df82f-157">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="df82f-158">Išplėskite sekciją **Būtinieji komponentai**.</span><span class="sxs-lookup"><span data-stu-id="df82f-158">Expand the **Prerequisites** section.</span></span> 
6. <span data-ttu-id="df82f-159">Spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="df82f-159">Click **Edit**.</span></span> 
7. <span data-ttu-id="df82f-160">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="df82f-160">Click **New**.</span></span> 
8. <span data-ttu-id="df82f-161">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="df82f-161">In the list, mark the selected row.</span></span> 
9. <span data-ttu-id="df82f-162">Lauke **Būtinojo komponento tipas** pasirinkite **Konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="df82f-162">In the **Prerequisite component type** field, select **Configuration**.</span></span> 
10.    <span data-ttu-id="df82f-163">Pasirinkite konfigūraciją **Užsienio prekybos metaduomenys**.</span><span class="sxs-lookup"><span data-stu-id="df82f-163">Select **Foreign trade metadata** configuration.</span></span> 
11.    <span data-ttu-id="df82f-164">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="df82f-164">Click **Save**.</span></span> 
12.    <span data-ttu-id="df82f-165">Įtraukėme nuorodą į konfigūracijos „Užsienio prekybos metaduomenys“ 1 versiją.</span><span class="sxs-lookup"><span data-stu-id="df82f-165">We added the reference to the version 1 of the 'Foreign trade metadata' configuration.</span></span> <span data-ttu-id="df82f-166">Kuriant šį modelio susiejimą bus siūlomi šios konfigūracijos programos metaduomenys.</span><span class="sxs-lookup"><span data-stu-id="df82f-166">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 
13.    <span data-ttu-id="df82f-167">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="df82f-167">Close the page.</span></span> 
14.    <span data-ttu-id="df82f-168">Spustelėkite **Konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="df82f-168">Click **Designer**.</span></span> 
15.    <span data-ttu-id="df82f-169">Spustelėkite **Konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="df82f-169">Click **Designer**.</span></span> 
16.    <span data-ttu-id="df82f-170">Medyje pasirinkite **Dynamics 365 for Operations\Lentelės įrašai**.</span><span class="sxs-lookup"><span data-stu-id="df82f-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
17.    <span data-ttu-id="df82f-171">Spustelėkite **Įtraukti šakninį elementą**.</span><span class="sxs-lookup"><span data-stu-id="df82f-171">Click **Add root**.</span></span> 
18.    <span data-ttu-id="df82f-172">Lauke **Pavadinimas** įveskite Intrastat.</span><span class="sxs-lookup"><span data-stu-id="df82f-172">In the **Name** field, type 'Intrastat'.</span></span> 
19.    <span data-ttu-id="df82f-173">Pasirinkite **Intrastat** lentelės įrašus.</span><span class="sxs-lookup"><span data-stu-id="df82f-173">Select **Intrastat** table records.</span></span> 
20.    <span data-ttu-id="df82f-174">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="df82f-174">Click **OK**.</span></span> 

> [!NOTE]
> <span data-ttu-id="df82f-175">Siūlytos tik 2 lentelės, nes tik 2 lentelės buvo įtrauktos į šiuo metų naudojamų metaduomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="df82f-175">The only 2 tables were offered as the only 2 tables were added into the set of metadata which is currently in use.</span></span> 

21.    <span data-ttu-id="df82f-176">Spustelėkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="df82f-176">Click **Bind**.</span></span> 
22.    <span data-ttu-id="df82f-177">Medyje išplėskite **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="df82f-177">In the tree, expand **Intrastat**.</span></span> 
23.    <span data-ttu-id="df82f-178">Medyje pasirinkite **Intrastat\AmountMST**.</span><span class="sxs-lookup"><span data-stu-id="df82f-178">In the tree, select **Intrastat\AmountMST**.</span></span> 
24.    <span data-ttu-id="df82f-179">Medyje išplėskite **Operacija = Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="df82f-179">In the tree, expand **Transaction = Intrastat**.</span></span> 
25.    <span data-ttu-id="df82f-180">Medyje pasirinkite **Operacija = Intrastat\Sąskaitos faktūros suma**.</span><span class="sxs-lookup"><span data-stu-id="df82f-180">In the tree, select **Transaction = Intrastat\Invoiced amount**.</span></span> 
26.    <span data-ttu-id="df82f-181">Spustelėkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="df82f-181">Click **Bind**.</span></span> 
27.    <span data-ttu-id="df82f-182">Medyje pasirinkite **Intrastat\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="df82f-182">In the tree, select **Intrastat\TransDate**.</span></span> 
28.    <span data-ttu-id="df82f-183">Medyje pasirinkite **Operacija = Intrastat\Data**.</span><span class="sxs-lookup"><span data-stu-id="df82f-183">In the tree, select **Transaction = Intrastat\Date**.</span></span> 
29.    <span data-ttu-id="df82f-184">Spustelėkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="df82f-184">Click **Bind**.</span></span> 
30.    <span data-ttu-id="df82f-185">Medyje išplėskite **Intrastat\>Ryšiai**.</span><span class="sxs-lookup"><span data-stu-id="df82f-185">In the tree, expand **Intrastat\>Relations**.</span></span> 
31.    <span data-ttu-id="df82f-186">Medyje išplėskite **Intrastat\>Ryšiai\IntrastatCommodity**.</span><span class="sxs-lookup"><span data-stu-id="df82f-186">In the tree, expand **Intrastat\>Relations\IntrastatCommodity**.</span></span> 
32.    <span data-ttu-id="df82f-187">Medyje pasirinkite **Intrastat\>Ryšiai\IntrastatCommodity\Kodas**.</span><span class="sxs-lookup"><span data-stu-id="df82f-187">In the tree, select **Intrastat\>Relations\IntrastatCommodity\Code**.</span></span> 
33.    <span data-ttu-id="df82f-188">Medyje pasirinkite **Operacija = Intrastat\Prekės kodas**.</span><span class="sxs-lookup"><span data-stu-id="df82f-188">In the tree, select **Transaction = Intrastat\Commodity code**.</span></span> 
34.    <span data-ttu-id="df82f-189">Spustelėkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="df82f-189">Click **Bind**.</span></span> 
35.    <span data-ttu-id="df82f-190">Spustelėkite **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="df82f-190">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="df82f-191">Sėkmingai susiejome duomenų modelio elementus su duomenų šaltinių elementais, kurie aprašomi naudojant programos metaduomenų informaciją iš nurodytos ER metaduomenų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="df82f-191">We have successfully bound elements of data model with items of data sources that are described by using details of application metadata from the referred ER metadata configuration.</span></span> 
36.    <span data-ttu-id="df82f-192">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="df82f-192">Click **Save**.</span></span> 
37.    <span data-ttu-id="df82f-193">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="df82f-193">Close the page.</span></span> 
38.    <span data-ttu-id="df82f-194">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="df82f-194">Close the page.</span></span> 
39.    <span data-ttu-id="df82f-195">Kai reikia, galite išplėsti esamą metaduomenų rinkinį ir eksportuoti naują baigtos versijos ER metaduomenų konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="df82f-195">When needed, you can extend the existing set of metadata and then export the new completed version of ER metadata configuration.</span></span> <span data-ttu-id="df82f-196">Tada galite importuoti ją į RCS ir atnaujinti sukonfigūruoto modelio susiejimo konfigūracijos būtinuosius komponentus, nurodančius naują importuotų metaduomenų konfigūracijos versiją.</span><span class="sxs-lookup"><span data-stu-id="df82f-196">You can then import it to RCS, and update the prerequisites of the configured model mapping configuration referring to a new version of imported metadata configuration.</span></span> 

> [!NOTE]
> <span data-ttu-id="df82f-197">Tai yra vienintelis būdas gauti informaciją apie programos metaduomenis, prieinamas naudojant vietinėje sistemoje įdiegtas programas (kai naudojamas vietos verslo duomenų (LBD) arba vietinio diegimo modelis).</span><span class="sxs-lookup"><span data-stu-id="df82f-197">This way of getting information about application metadata is the only one available for locally deployed applications (when local business data (LBD), or on-premises, deployment model is used).</span></span>
        
