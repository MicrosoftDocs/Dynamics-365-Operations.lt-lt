---
title: Formatų modifikavimas iš naujo pritaikant „Excel‟ šablonus
description: Norėdami užbaigti veiksmus šioje procedūroje, pirmiausia turite užbaigti procedūrą „ER – kurkite konfigūraciją ataskaitoms generuoti OPENXML formatu“.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ca6707095765c25851ee864a99844a82844fae1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564319"
---
# <a name="modify-formats-by-reapplying-excel-templates"></a><span data-ttu-id="c46db-103">Formatų modifikavimas iš naujo pritaikant „Excel‟ šablonus</span><span class="sxs-lookup"><span data-stu-id="c46db-103">Modify formats by reapplying Excel templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c46db-104">Norėdami užbaigti veiksmus šioje procedūroje, pirmiausia turite užbaigti procedūrą „ER – kurkite konfigūraciją ataskaitoms generuoti OPENXML formatu“.</span><span class="sxs-lookup"><span data-stu-id="c46db-104">To complete the steps in this procedure, you must first complete the procedure, ER - Design a configuration for generating reports in OPENXML format.</span></span>

<span data-ttu-id="c46db-105">Šia procedūra paaiškinama, kaip keisti elektroninių ataskaitų teikimo (ER) formato konfigūraciją, iš naujo taikant „Microsoft Excel“ šabloną, kuris buvo pakeistas.</span><span class="sxs-lookup"><span data-stu-id="c46db-105">This procedure explains how to modify an Electronic reporting (ER) format configuration by reapplying a Microsoft Excel template that has been modified.</span></span> <span data-ttu-id="c46db-106">Šios procedūros metu importuosite modifikuotą „Excel“ šabloną į ER formato konfigūracijas, sukurtas pavyzdinei įmonei „Litware, Inc.“, ir tada generuokite elektroninius dokumentus.</span><span class="sxs-lookup"><span data-stu-id="c46db-106">In this procedure, you will import a modified Excel template into ER format configurations that have been created for the sample company, Litware, Inc., and then generate electronic documents.</span></span> <span data-ttu-id="c46db-107">Ši procedūra skirta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="c46db-107">This procedure is intended for users who have the system administrator or electronic reporting developer role.</span></span> <span data-ttu-id="c46db-108">Šiuos veiksmus galima atlikti naudojant GBSI duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="c46db-108">These steps can be completed by using the GBSI dataset.</span></span> <span data-ttu-id="c46db-109">Prieš pradėdami atsisiųskite ir įrašykite failą SampleVendPaymWsReport2.xlsx, kuris nurodytas žinyno temoje „Elektroninių ataskaitų formato modifikavimas iš naujo pritaikant „Excel“ šabloną“ (modify-electronic-reporting-format-reapply-excel-template/).</span><span class="sxs-lookup"><span data-stu-id="c46db-109">Before you begin, download and save the file, SampleVendPaymWsReport2.xlsx, which is listed in the Help topic, Modify Electronic reporting format by reapplying an Excel template (modify-electronic-reporting-format-reapply-excel-template/).</span></span>

1. <span data-ttu-id="c46db-110">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="c46db-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="c46db-111">Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="c46db-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="c46db-112">Jei nematote šio konfigūracijos teikėjo, atlikite procedūros Kurkite konfigūracijos teikėją ir pažymėkite kaip aktyvų veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c46db-112">If you don't see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  

## <a name="select-the-er-format"></a><span data-ttu-id="c46db-113">Pasirinkite ER formatą</span><span class="sxs-lookup"><span data-stu-id="c46db-113">Select the ER format</span></span>
1. <span data-ttu-id="c46db-114">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="c46db-114">Click Reporting configurations.</span></span>
2. <span data-ttu-id="c46db-115">Medyje išplėskite „Mokėjimo modelis‟.</span><span class="sxs-lookup"><span data-stu-id="c46db-115">In the tree, expand 'Payment model'.</span></span>
3. <span data-ttu-id="c46db-116">Medyje pasirinkite Mokėjimo modelis\Darbalapio ataskaitos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="c46db-116">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
4. <span data-ttu-id="c46db-117">Spustelėkite Priedai.</span><span class="sxs-lookup"><span data-stu-id="c46db-117">Click Attachments.</span></span>
    * <span data-ttu-id="c46db-118">Atkreipkite dėmesį, kad SampleVendPaymWsReport.xlsx „Excel“ failas šiuo metu naudojamas kaip šablonas mokėjimo žurnalo apdorojimui.</span><span class="sxs-lookup"><span data-stu-id="c46db-118">Note that the SampleVendPaymWsReport.xlsx Excel file is currently used as a template for payment journal processing.</span></span>   
5. <span data-ttu-id="c46db-119">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="c46db-119">Click Open.</span></span>
    * <span data-ttu-id="c46db-120">Spustelėkite Atidaryti, kad ištirtumėte „Excel“ šablono išdėstymą.</span><span class="sxs-lookup"><span data-stu-id="c46db-120">Click Open to explore the layout of the Excel template.</span></span>  
    * <span data-ttu-id="c46db-121">Peržiūrėkite šabloną.</span><span class="sxs-lookup"><span data-stu-id="c46db-121">Review the template.</span></span> <span data-ttu-id="c46db-122">Žinokite, kad į ją dabar įeina šie kiekvienos mokėjimo eilutės duomenys: tiekėjo sąskaitos numeris, tiekėjo pavadinimas, bankas, kodas, sąskaitos numeris, debetas, kreditas ir valiuta.</span><span class="sxs-lookup"><span data-stu-id="c46db-122">Note that it currently includes the following details for each payment line: vendor account number, vendor name, bank, routing number, account number, debit, credit, and currency.</span></span> <span data-ttu-id="c46db-123">Šiam pavyzdžiui mes norime pratęsti šį sąrašą, pridėdami informacijos apie mokėjimo datą.</span><span class="sxs-lookup"><span data-stu-id="c46db-123">For this example, we want to extend this list by adding details about the payment date.</span></span>   
6. <span data-ttu-id="c46db-124">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c46db-124">Close the page.</span></span>

## <a name="reapply-a-new-excel-template-to-er-format"></a><span data-ttu-id="c46db-125">Iš naujo taikykite naują „Excel“ šabloną į ER formatui</span><span class="sxs-lookup"><span data-stu-id="c46db-125">Reapply a new Excel template to ER format</span></span>
1. <span data-ttu-id="c46db-126">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="c46db-126">Click Designer.</span></span>
    * <span data-ttu-id="c46db-127">Atidarykite pasirinkto ER formato juodraščio versiją redagavimui.</span><span class="sxs-lookup"><span data-stu-id="c46db-127">Open the draft version of the selected ER format for editing.</span></span>  
2. <span data-ttu-id="c46db-128">Veiksmų srityje spustelėkite Importuoti.</span><span class="sxs-lookup"><span data-stu-id="c46db-128">On the Action Pane, click Import.</span></span>
3. <span data-ttu-id="c46db-129">Spustelėkite Naujinti iš „Excel‟.</span><span class="sxs-lookup"><span data-stu-id="c46db-129">Click Update from Excel.</span></span>
    * <span data-ttu-id="c46db-130">Spustelėkite „Naujinti šabloną“ ir pasirinkite failą SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="c46db-130">Click 'Update template', and then select the file, SampleVendPaymWsReport2.xlsx.</span></span>  
    * <span data-ttu-id="c46db-131">Spustelėkite Atnaujinti šabloną ir naršykite, kad gautumėte anksčiau atsisiųstą SampleVendPaymWsReport2.xlsx failą.</span><span class="sxs-lookup"><span data-stu-id="c46db-131">Click Update template and browse to get the downloaded earlier SampleVendPaymWsReport2.xlsx file.</span></span>  
4. <span data-ttu-id="c46db-132">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c46db-132">Click OK.</span></span>
    * <span data-ttu-id="c46db-133">Pritaikytas SampleVendPaymWsReport2.xlsx šablonas.</span><span class="sxs-lookup"><span data-stu-id="c46db-133">The SampleVendPaymWsReport2.xlsx template is applied.</span></span> <span data-ttu-id="c46db-134">ER formato struktūra sinchronizuojama su šablono, kurio elementai pridėti prie ER formato, turiniu.</span><span class="sxs-lookup"><span data-stu-id="c46db-134">The structure of the ER format is synchronized with the content of the template, whose elements are added to the ER format.</span></span> <span data-ttu-id="c46db-135">Bet kokie ER formate esantys elementai, kurie neįtraukti į šabloną, pašalinami iš formato apibrėžties.</span><span class="sxs-lookup"><span data-stu-id="c46db-135">Any existing elements in the ER format that aren't included in the template are removed from the format definition.</span></span>  
5. <span data-ttu-id="c46db-136">Medyje pasirinkite „Excel“.</span><span class="sxs-lookup"><span data-stu-id="c46db-136">In the tree, select 'Excel'.</span></span>
    * <span data-ttu-id="c46db-137">Atkreipkite dėmesį, kad šablono lauke dabar yra nuoroda į naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="c46db-137">Note that the Template field now contains a reference to the new template.</span></span>   
6. <span data-ttu-id="c46db-138">Spustelėkite Priedai.</span><span class="sxs-lookup"><span data-stu-id="c46db-138">Click Attachments.</span></span>
7. <span data-ttu-id="c46db-139">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="c46db-139">Click Open.</span></span>
    * <span data-ttu-id="c46db-140">Spustelėkite Atidaryti, kad ištirtumėte pakeisto „Excel“ šablono išdėstymą.</span><span class="sxs-lookup"><span data-stu-id="c46db-140">Click Open to explore the layout of the modified Excel template.</span></span>  
    * <span data-ttu-id="c46db-141">Peržiūrėkite šabloną.</span><span class="sxs-lookup"><span data-stu-id="c46db-141">Review the template.</span></span> <span data-ttu-id="c46db-142">Atkreipkite dėmesį, kad jame dabar yra eilutė mokėjimo datai.</span><span class="sxs-lookup"><span data-stu-id="c46db-142">Note that it now contains a line for the payment date.</span></span>   
8. <span data-ttu-id="c46db-143">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c46db-143">Close the page.</span></span>
9. <span data-ttu-id="c46db-144">Medyje išplėskite „Excel“.</span><span class="sxs-lookup"><span data-stu-id="c46db-144">In the tree, expand 'Excel'.</span></span>
10. <span data-ttu-id="c46db-145">Medyje išplėskite „Excel \ PaymLines”.</span><span class="sxs-lookup"><span data-stu-id="c46db-145">In the tree, expand 'Excel\PaymLines'.</span></span>
11. <span data-ttu-id="c46db-146">Medyje pasirinkite „Excel\PaymLines\PaymDate“.</span><span class="sxs-lookup"><span data-stu-id="c46db-146">In the tree, select 'Excel\PaymLines\PaymDate'.</span></span>
    * <span data-ttu-id="c46db-147">Atkreipkite dėmesį, kad ER formate dabar yra dar vienas elementas.</span><span class="sxs-lookup"><span data-stu-id="c46db-147">Note that the ER format now contains one more item.</span></span> <span data-ttu-id="c46db-148">Langelis PaymDate pridėtas prie „Excel“ šablono.</span><span class="sxs-lookup"><span data-stu-id="c46db-148">A cell, PaymDate, has been added to the Excel template.</span></span>  
12. <span data-ttu-id="c46db-149">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="c46db-149">Click the Mapping tab.</span></span>
13. <span data-ttu-id="c46db-150">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="c46db-150">In the tree, expand 'model'.</span></span>
14. <span data-ttu-id="c46db-151">Medyje išplėskite „modelis \ Mokėjimai‟.</span><span class="sxs-lookup"><span data-stu-id="c46db-151">In the tree, expand 'model\Payments'.</span></span>
15. <span data-ttu-id="c46db-152">Medyje pasirinkite „modelis \ Mokėjimai \ Operacijos data (TransactionDate)“.</span><span class="sxs-lookup"><span data-stu-id="c46db-152">In the tree, select 'model\Payments\Transaction date(TransactionDate)'.</span></span>
16. <span data-ttu-id="c46db-153">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="c46db-153">Click Bind.</span></span>
    * <span data-ttu-id="c46db-154">Nurodykite, kokie duomenys pridedami prie naujo langelio veikiant.</span><span class="sxs-lookup"><span data-stu-id="c46db-154">Specify what data is added to the new cell at runtime.</span></span>  
17. <span data-ttu-id="c46db-155">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c46db-155">Click Save.</span></span>
18. <span data-ttu-id="c46db-156">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c46db-156">Close the page.</span></span>

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a><span data-ttu-id="c46db-157">Įgalinkite pakeistą ER formato juodraščio versiją naudoti mokėjimų žurnalo apdorojimui</span><span class="sxs-lookup"><span data-stu-id="c46db-157">Enable the modified draft version of the ER format for use in payment journal processing</span></span>
1. <span data-ttu-id="c46db-158">Veiksmų srityje spustelėkite Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="c46db-158">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="c46db-159">Spustelėkite Vartotojo parametrai.</span><span class="sxs-lookup"><span data-stu-id="c46db-159">Click User parameters.</span></span>
3. <span data-ttu-id="c46db-160">Lauke Paleisti parametrus pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="c46db-160">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="c46db-161">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c46db-161">Click OK.</span></span>
5. <span data-ttu-id="c46db-162">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="c46db-162">Click Edit.</span></span>
6. <span data-ttu-id="c46db-163">Lauke Paleisti juodraštį pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="c46db-163">Select Yes in the Run Draft field.</span></span>

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a><span data-ttu-id="c46db-164">Naudokite pakeistą ER formato juodraščio versiją naudoti mokėjimų žurnalo apdorojimui</span><span class="sxs-lookup"><span data-stu-id="c46db-164">Use the modified draft version of the ER format for payment journal processing</span></span>

<span data-ttu-id="c46db-165">Peržiūrėkite sukurtą darbalapį, įskaitant naują mokėjimo eilučių informaciją – mokėjimo data.</span><span class="sxs-lookup"><span data-stu-id="c46db-165">Review the created worksheet, including new detail of payment lines – payment date.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]