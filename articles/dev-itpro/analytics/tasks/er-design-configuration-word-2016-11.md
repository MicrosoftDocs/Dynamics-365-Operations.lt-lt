---
title: ER konfigūracijų kūrimas siekiant generuoti ataskaitas „Word“ formatu
description: Toliau nurodytuose veiksmuose paaiškinta, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmens vartotojas gali konfigūruoti elektroninių ataskaitų formatus, norėdamas ataskaitas generuoti kaip „Microsoft Word“ failus.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc47d44285af4c720d2f450d11fb1004ef461d0f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "362354"
---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a><span data-ttu-id="c2eec-103">ER konfigūracijų kūrimas siekiant generuoti ataskaitas „Word“ formatu</span><span class="sxs-lookup"><span data-stu-id="c2eec-103">Design ER configurations to generate reports in Word format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c2eec-104">Toliau nurodytuose veiksmuose paaiškinta, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmens vartotojas gali konfigūruoti elektroninių ataskaitų (ER) formatus, norėdamas ataskaitas generuoti kaip „Microsoft Word“ failus.</span><span class="sxs-lookup"><span data-stu-id="c2eec-104">The following steps explain how a user in either the System administrator or Electronic reporting developer role can configure an Electronic reporting (ER) formats to generate reports as Microsoft Word files.</span></span> <span data-ttu-id="c2eec-105">Šiuos veiksmus galima atlikti GBSI įmonėje.</span><span class="sxs-lookup"><span data-stu-id="c2eec-105">These steps can be performed in the GBSI company.</span></span>

<span data-ttu-id="c2eec-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite užbaigti užduočių vadovo „ER konfigūracijos, skirtos generuoti ataskaitoms OPENXML formatu, kūrimas“ veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c2eec-106">To complete these steps, you must first complete the steps in the “Create an ER configuration for generating reports in OPENXML format” task guide.</span></span> <span data-ttu-id="c2eec-107">Iš anksto taip pat turite atsisiųsti ir įrašyti šiuos šablonus vietoje ataskaitos pavyzdžiui:</span><span class="sxs-lookup"><span data-stu-id="c2eec-107">In advance, you must also download and save the following templates locally for the sample report:</span></span>

- [<span data-ttu-id="c2eec-108">Mokėjimo ataskaitos šablonas</span><span class="sxs-lookup"><span data-stu-id="c2eec-108">Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="c2eec-109">Susietas mokėjimo ataskaitos šablonas</span><span class="sxs-lookup"><span data-stu-id="c2eec-109">Bounded Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)


<span data-ttu-id="c2eec-110">Ši procedūra yra skirta į 1611 „Microsoft Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="c2eec-110">This procedure is for a feature that was added in Microsoft Dynamics 365 for Operations version 1611.</span></span>


## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="c2eec-111">Pasirinkite esamą ER ataskaitos konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="c2eec-111">Select the existing ER report configuration</span></span>
1. <span data-ttu-id="c2eec-112">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="c2eec-112">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="c2eec-113">Įsitikinkite, kad konfigūracijos teikėjas „Litware, Inc.“.</span><span class="sxs-lookup"><span data-stu-id="c2eec-113">Make sure that the configuration provider ‘Litware, Inc.’</span></span> <span data-ttu-id="c2eec-114">pasirinktas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="c2eec-114">is selected as active.</span></span>  
2. <span data-ttu-id="c2eec-115">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="c2eec-115">Click Reporting configurations.</span></span>
    * <span data-ttu-id="c2eec-116">Pakartotinai naudosime esamą ER konfigūraciją, kuri iš pradžių buvo skirta ataskaitos išvesčiai OPENXML formatu generuoti.</span><span class="sxs-lookup"><span data-stu-id="c2eec-116">We will re-use the existing ER configuration that has been originally designed to generate the report output in OPENXML format.</span></span>  
3. <span data-ttu-id="c2eec-117">Medyje išplėskite „Mokėjimo modelis‟.</span><span class="sxs-lookup"><span data-stu-id="c2eec-117">In the tree, expand 'Payment model'.</span></span>
4. <span data-ttu-id="c2eec-118">Medyje pasirinkite Mokėjimo modelis\Darbalapio ataskaitos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="c2eec-118">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
5. <span data-ttu-id="c2eec-119">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="c2eec-119">Click Designer.</span></span>

## <a name="replace-the-excel-template-with-the-word-template"></a><span data-ttu-id="c2eec-120">„Excel” šabloną pakeiskite „Word“ šablonu</span><span class="sxs-lookup"><span data-stu-id="c2eec-120">Replace the Excel template with the Word template</span></span>
    * <span data-ttu-id="c2eec-121">Šiuo metu „Excel” dokumentas naudojamas kaip šablonas OPENXML formato išvesčiai generuoti.</span><span class="sxs-lookup"><span data-stu-id="c2eec-121">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="c2eec-122">Importuosime ataskaitos šabloną „Word“ formatu.</span><span class="sxs-lookup"><span data-stu-id="c2eec-122">We will import the report’s template in Word format.</span></span>  
1. <span data-ttu-id="c2eec-123">Spustelėkite Priedai.</span><span class="sxs-lookup"><span data-stu-id="c2eec-123">Click Attachments.</span></span>
    * <span data-ttu-id="c2eec-124">Esamą „Excel” šabloną pakeiskite „Word“ šablonu SampleVendPaymDocReport.docx, kurį atsisiuntėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="c2eec-124">Replace the existing Excel template with the Word template that you downloaded earlier, SampleVendPaymDocReport.docx.</span></span> <span data-ttu-id="c2eec-125">Atkreipkite dėmesį, kad šiame šablone yra tik dokumento maketas, kurį norime sugeneruoti kaip ER išvestį.</span><span class="sxs-lookup"><span data-stu-id="c2eec-125">Note, this template only contains the layout of the document we want to generate as ER output.</span></span>  
2. <span data-ttu-id="c2eec-126">Spustelėkite Naikinti.</span><span class="sxs-lookup"><span data-stu-id="c2eec-126">Click Delete.</span></span>
3. <span data-ttu-id="c2eec-127">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="c2eec-127">Click Yes.</span></span>
4. <span data-ttu-id="c2eec-128">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c2eec-128">Click New.</span></span>
5. <span data-ttu-id="c2eec-129">Spustelėkite Failas.</span><span class="sxs-lookup"><span data-stu-id="c2eec-129">Click File.</span></span>
6. <span data-ttu-id="c2eec-130">Spustelėkite Naršyti.</span><span class="sxs-lookup"><span data-stu-id="c2eec-130">Click Browse.</span></span> <span data-ttu-id="c2eec-131">Suraskite ir pasirinkite anksčiau atsisiųstą failą SampleVendPaymDocReport.docx.</span><span class="sxs-lookup"><span data-stu-id="c2eec-131">Navigate to and select SampleVendPaymDocReport.docx that you previously downloaded.</span></span> <span data-ttu-id="c2eec-132">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c2eec-132">Click OK.</span></span>
    * <span data-ttu-id="c2eec-133">Pasirinkite šabloną, kurį atsisiuntėte vykdydami ankstesnį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="c2eec-133">Select the template that you downloaded in the previous step.</span></span>  
7. <span data-ttu-id="c2eec-134">Lauke Šablonas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c2eec-134">In the Template field, enter or select a value.</span></span>

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a><span data-ttu-id="c2eec-135">Išplėskite „Word“ šabloną įtraukdami pasirinktinę XML dalį</span><span class="sxs-lookup"><span data-stu-id="c2eec-135">Extend the Word template by adding a custom XML part</span></span>
1. <span data-ttu-id="c2eec-136">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c2eec-136">Click Save.</span></span>
    * <span data-ttu-id="c2eec-137">Be to, norėdami išsaugoti konfigūracijos pakeitimus, atlikite veiksmą Įrašyti, kuriuo taip pat atnaujinamas pridėtas „Word” šablonas.</span><span class="sxs-lookup"><span data-stu-id="c2eec-137">In addition to storing configuration changes, the Save action also updates the attached Word template.</span></span> <span data-ttu-id="c2eec-138">Sukurto formato struktūra perkeliama į pridėtą „Word” dokumentą kaip nauja pasirinktinė XML dalis, kurios pavadinimas „Ataskaita“.</span><span class="sxs-lookup"><span data-stu-id="c2eec-138">The structure of the designed format is ported to the attached Word document as a new custom XML part with the name ‘Report’.</span></span> <span data-ttu-id="c2eec-139">Atminkite, kad pridėtame „Word” šablone yra ne tik dokumento maketas, kurį norime sugeneruoti kaip ER išvestį, bet ir duomenų struktūra, kuri apdorojimo metu ER perkels į šį šabloną.</span><span class="sxs-lookup"><span data-stu-id="c2eec-139">Note that the attached Word template contains not only the layout of the document we want to generate as ER output, it also contains the structure of data that ER will populate into this template at runtime.</span></span>  
2. <span data-ttu-id="c2eec-140">Spustelėkite Priedai.</span><span class="sxs-lookup"><span data-stu-id="c2eec-140">Click Attachments.</span></span>
    * <span data-ttu-id="c2eec-141">Dabar turite susieti pasirinktinės XML dalies „Ataskaita“ elementus su „Word” dokumento dalimis.</span><span class="sxs-lookup"><span data-stu-id="c2eec-141">Now you need to bind the elements of the custom XML part ‘Report’ to the Word document parts.</span></span>  
    * <span data-ttu-id="c2eec-142">Jei esate susipažinę su „Word“ dokumentais, kurie gali būti sukurti kaip formos, turinčios su pasirinktinių XML dalių elementais susietų turinio valdiklių, paleiskite visus kitos papildomos užduoties veiksmus, kad sukurtumėte tokį dokumentą.</span><span class="sxs-lookup"><span data-stu-id="c2eec-142">If you're familiar with Word documents that can be designed as forms containing content controls that are bounded with elements of custom XML parts – play all steps of the next sub-task to create such a document.</span></span> <span data-ttu-id="c2eec-143">Norėdami gauti daugiau informacijos, žr. šią nuorodą https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span><span class="sxs-lookup"><span data-stu-id="c2eec-143">For more details, see this link https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span></span> <span data-ttu-id="c2eec-144">Priešingu atveju praleiskite visus kitos papildomos užduoties veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c2eec-144">Otherwise, skip all the steps in the next sub-task.</span></span>  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a><span data-ttu-id="c2eec-145">Norėdami gauti „Word“ dokumentą su pasirinktine XML dalimi, susiekite duomenis</span><span class="sxs-lookup"><span data-stu-id="c2eec-145">Get Word with custom XML part to do data bindings</span></span>
    * <span data-ttu-id="c2eec-146">Atidarykite šį dokumentą programa „Word“ ir atlikite tokius veiksmus: - atidarykite skirtuką „Word“ kūrėjas (pritaikykite juostelę, jei dar neįjungta);</span><span class="sxs-lookup"><span data-stu-id="c2eec-146">Open this document in Word and do the following:  - Open the Word Developer tab (customize the ribbon if it is not enabled yet).</span></span>  <span data-ttu-id="c2eec-147">- pasirinkite XML susiejimo sritį;</span><span class="sxs-lookup"><span data-stu-id="c2eec-147">- Select XML mapping pane.</span></span>  <span data-ttu-id="c2eec-148">- peržvalgos sąraše pasirinkite pasirinktinę XML dalį „Ataskaita“;</span><span class="sxs-lookup"><span data-stu-id="c2eec-148">- Select the ‘Report’ custom XML part in the lookup.</span></span>  <span data-ttu-id="c2eec-149">- pasirinktos pasirinktinės XML dalies elementus susiekite su „Word“ dokumento turinio valdikliais;</span><span class="sxs-lookup"><span data-stu-id="c2eec-149">- Do mapping of the elements of the selected custom XML part and content controls of the Word document.</span></span>  <span data-ttu-id="c2eec-150">- atnaujintą „Word” dokumentą įrašykite į vietinį diską.</span><span class="sxs-lookup"><span data-stu-id="c2eec-150">- Save the updated Word document on a local drive.</span></span>  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a><span data-ttu-id="c2eec-151">Įkelkite „Word“ šabloną su turinio valdikliais susieta pasirinktine XML dalimi</span><span class="sxs-lookup"><span data-stu-id="c2eec-151">Upload the Word template with custom XML part bounded to content controls</span></span>
1. <span data-ttu-id="c2eec-152">Spustelėkite Naikinti.</span><span class="sxs-lookup"><span data-stu-id="c2eec-152">Click Delete.</span></span>
2. <span data-ttu-id="c2eec-153">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="c2eec-153">Click Yes.</span></span>
    * <span data-ttu-id="c2eec-154">Įtraukite naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="c2eec-154">Add a new template.</span></span> <span data-ttu-id="c2eec-155">Jei atlikote ankstesnės papildomos užduoties veiksmus, pasirinkite paruoštą ir įrašytą vietoje „Word“ dokumentą.</span><span class="sxs-lookup"><span data-stu-id="c2eec-155">If you competed the steps in the previous subtask, select the Word document that you prepared and saved locally.</span></span> <span data-ttu-id="c2eec-156">Priešingu atveju pasirinkite „MS Word” šabloną SampleVendPaymDocReportBounded.docx, kurį atsisiuntėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="c2eec-156">Otherwise, select the SampleVendPaymDocReportBounded.docx MS Word template that you downloaded earlier.</span></span>  
3. <span data-ttu-id="c2eec-157">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c2eec-157">Click New.</span></span>
4. <span data-ttu-id="c2eec-158">Spustelėkite Failas.</span><span class="sxs-lookup"><span data-stu-id="c2eec-158">Click File.</span></span>
5. <span data-ttu-id="c2eec-159">Spustelėkite Naršyti.</span><span class="sxs-lookup"><span data-stu-id="c2eec-159">Click Browse.</span></span> <span data-ttu-id="c2eec-160">Suraskite ir pasirinkite anksčiau atsisiųstą failą SampleVendPaymDocReportBounded.docx.</span><span class="sxs-lookup"><span data-stu-id="c2eec-160">Navigate to and select SampleVendPaymDocReportBounded.docx that you previously downloaded.</span></span> <span data-ttu-id="c2eec-161">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="c2eec-161">Click OK.</span></span>
6. <span data-ttu-id="c2eec-162">Lauke Šablonas pasirinkite dokumentą, kurį atsisiuntėte vykdydami ankstesnį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="c2eec-162">In the Template field, select the document that you downloaded in the previous step.</span></span>
7. <span data-ttu-id="c2eec-163">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c2eec-163">Click Save.</span></span>
8. <span data-ttu-id="c2eec-164">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c2eec-164">Close the page.</span></span>

## <a name="execute-the-format-to-create-word-output"></a><span data-ttu-id="c2eec-165">Formato paleidimas norint kurti „Word“ išvestį</span><span class="sxs-lookup"><span data-stu-id="c2eec-165">Execute the format to create Word output</span></span>
1. <span data-ttu-id="c2eec-166">Veiksmų srityje spustelėkite Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="c2eec-166">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="c2eec-167">Spustelėkite Vartotojo parametrai.</span><span class="sxs-lookup"><span data-stu-id="c2eec-167">Click User parameters.</span></span>
3. <span data-ttu-id="c2eec-168">Lauke Paleisti parametrus pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="c2eec-168">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="c2eec-169">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c2eec-169">Click OK.</span></span>
5. <span data-ttu-id="c2eec-170">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="c2eec-170">Click Edit.</span></span>
6. <span data-ttu-id="c2eec-171">Lauke Paleisti juodraštį pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="c2eec-171">Select Yes in the Run Draft field.</span></span>
7. <span data-ttu-id="c2eec-172">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c2eec-172">Click Save.</span></span>
8. <span data-ttu-id="c2eec-173">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c2eec-173">Close the page.</span></span>
9. <span data-ttu-id="c2eec-174">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c2eec-174">Close the page.</span></span>
10. <span data-ttu-id="c2eec-175">Pasirinkite Mokėtinos sumos > Mokėjimai > Mokėjimų žurnalas.</span><span class="sxs-lookup"><span data-stu-id="c2eec-175">Go to Accounts payable > Payments > Payment journal.</span></span>
11. <span data-ttu-id="c2eec-176">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="c2eec-176">Click Lines.</span></span>
12. <span data-ttu-id="c2eec-177">Pažymėkite arba atžymėkite visas sąrašo eilutes.</span><span class="sxs-lookup"><span data-stu-id="c2eec-177">In the list, mark or unmark all rows.</span></span>
13. <span data-ttu-id="c2eec-178">Spustelėkite mokėjimo būsena.</span><span class="sxs-lookup"><span data-stu-id="c2eec-178">Click Payment status.</span></span>
14. <span data-ttu-id="c2eec-179">Spustelėkite Nėra.</span><span class="sxs-lookup"><span data-stu-id="c2eec-179">Click None.</span></span>
15. <span data-ttu-id="c2eec-180">Spustelėkite Generuoti mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="c2eec-180">Click Generate payments.</span></span>
16. <span data-ttu-id="c2eec-181">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c2eec-181">Click OK.</span></span>
17. <span data-ttu-id="c2eec-182">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c2eec-182">Click OK.</span></span>
    * <span data-ttu-id="c2eec-183">Analizuokite sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="c2eec-183">Analyze the generated output.</span></span> <span data-ttu-id="c2eec-184">Įsidėmėkite, kad sukurta išvestis pateikiama „Word” formatu kartu su informacija apie apdorotus mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="c2eec-184">Note that the created output is presented in Word format and contains the details of the processed payments.</span></span>  

