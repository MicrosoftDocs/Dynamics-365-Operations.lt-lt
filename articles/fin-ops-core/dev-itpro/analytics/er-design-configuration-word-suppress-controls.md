---
title: Nerodomo „Word” turinio valdikliai sugeneruotose ataskaitose
description: Šioje temoje paaiškinama, kaip konfigūruoti elektroninės ataskaitos (ER) formatą ataskaitoms generuoti, pavyzdžiui, failams „Microsoft Word”, kuriuose turinio valdikliai nerodomi.
author: NickSelin
manager: AnnBe
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 81ad25514154dd8982aa4f849f0b2bfeb85270f7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562123"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a><span data-ttu-id="c0175-103">Nerodomo „Word” turinio valdikliai sugeneruotose ataskaitose</span><span class="sxs-lookup"><span data-stu-id="c0175-103">Suppress Word content controls in generated reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0175-104">Norėdami generuoti ataskaitas „Microsoft Word” kaip dokumentus, turite sukurti ataskaitų šabloną kaip „Word” dokumentą.</span><span class="sxs-lookup"><span data-stu-id="c0175-104">To generate reports as Microsoft Word documents, you must design a template for the reports as a Word document.</span></span> <span data-ttu-id="c0175-105">Šiame šablone turi būti „Word” duomenų valdikliai, kaip vietos rezervavimo ženklai duomenims, kurie turi būti užpildyti apdorojimo metu.</span><span class="sxs-lookup"><span data-stu-id="c0175-105">This template must contain Word content controls as placeholders for data that will be filled in at runtime.</span></span> <span data-ttu-id="c0175-106">Norėdami naudoti „Word” dokumentą, sukurtą kaip šabloną jūsų ataskaitoms, galite [sukonfigūruoti](er-design-configuration-word.md) naują [elektroninės ataskaitos (ER)](general-electronic-reporting.md) [sprendimą](er-quick-start1-new-solution.md).</span><span class="sxs-lookup"><span data-stu-id="c0175-106">To use the Word document that is created as a template for your reports, you can [configure](er-design-configuration-word.md) a new [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md).</span></span> <span data-ttu-id="c0175-107">Šis sprendimas turi apimti ER [konfigūraciją,](general-electronic-reporting.md#Configuration) kurioje yra ER [formato](general-electronic-reporting.md#FormatComponentOutbound) komponentas.</span><span class="sxs-lookup"><span data-stu-id="c0175-107">The solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="c0175-108">Šis ER formatas turi būti sukonfigūruotas naudoti skirtą šabloną ataskaitai kurti.</span><span class="sxs-lookup"><span data-stu-id="c0175-108">This ER format must be configured to use the designed template for report generation.</span></span>

<span data-ttu-id="c0175-109">Versijoje 10.0.6 ir vėlesnėse „Dynamics 365 Finance” versijose galite konfigūruoti formules savo ER formatu, kad sugeneruotuose dokumentuose nerodomi kai kuriuos „Word” turinio valdiklius.</span><span class="sxs-lookup"><span data-stu-id="c0175-109">In version 10.0.6 and later of Dynamics 365 Finance, you can configure formulas in your ER format to suppress some Word content controls in generated documents.</span></span>

<span data-ttu-id="c0175-110">Toliau paaiškinama, kaip vartotojas, kuris priskirtas sistemos administratoriui arba elektroninio ataskaitų funkcinio konsultanto vaidmeniui, gali konfigūruoti ER formatą, kuris generuoja ataskaitas kaip „Word” failus ir nerodo kai kuriuos sugeneruotų ataskaitų, kurios sukonfigūruotos naudojant „Word” šabloną, turinio valdiklius.</span><span class="sxs-lookup"><span data-stu-id="c0175-110">The following steps explain how a user who is assigned to the System administrator or Electronic reporting functional consultant role can configure an ER format that generates reports as Word files and suppresses some of the content controls in the generated reports that have been configured by using a Word template.</span></span>

<span data-ttu-id="c0175-111">Šie žingsniai gali būti užbaigti GBSI bendrovėje.</span><span class="sxs-lookup"><span data-stu-id="c0175-111">These steps can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c0175-112">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="c0175-112">Prerequisites</span></span>

<span data-ttu-id="c0175-113">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti šių užduočių vadovuose nurodytus veiksmus:</span><span class="sxs-lookup"><span data-stu-id="c0175-113">To complete these steps, you must first complete the steps in the following task guides:</span></span>

- [<span data-ttu-id="c0175-114">Konfigūracijos, skirtos ataskaitoms OPENXML formatu generuoti, kūrimas</span><span class="sxs-lookup"><span data-stu-id="c0175-114">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="c0175-115">Pakartotinai naudokite ER konfigūracijas su „Excel“ šablonais, kad sugeneruotumėte ataskaitas „Word“ formatu</span><span class="sxs-lookup"><span data-stu-id="c0175-115">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)

<span data-ttu-id="c0175-116">Kai atliksite šių užduočių vedlių veiksmus, šie elementai bus paruošti:</span><span class="sxs-lookup"><span data-stu-id="c0175-116">When you complete the steps of these task guides, the following items are prepared:</span></span>

- <span data-ttu-id="c0175-117">**Darbalapio ataskaitos pavyzdys** ER formatas, sukonfigūruotas generuoti dokumentą „Word” formatu</span><span class="sxs-lookup"><span data-stu-id="c0175-117">A **Sample worksheet report** ER format that is configured to generate a document in Word format</span></span>
- <span data-ttu-id="c0175-118">[Juodraštis](general-electronic-reporting.md#component-versioning) ataskaitos **Darbalapio ataskaitos pavyzdys** versijos, pažymėtas kaip **Vykdytinas**</span><span class="sxs-lookup"><span data-stu-id="c0175-118">A [draft](general-electronic-reporting.md#component-versioning) version of the **Sample worksheet report** ER format that is marked as **Runnable**</span></span>
- <span data-ttu-id="c0175-119">**Elektroninis** mokėjimo būdas, sukonfigūruotas naudoti **Darbalapio ataskaitos pavyzdys** ER formatu tiekėjo mokėjimui apdoroti</span><span class="sxs-lookup"><span data-stu-id="c0175-119">An **Electronic** method of payments that is configured to use the **Sample worksheet report** ER format for vendor payment processing</span></span>

<span data-ttu-id="c0175-120">Taip pat turite atsisiųsti ir įrašyti šį ataskaitos pavyzdžio šabloną:</span><span class="sxs-lookup"><span data-stu-id="c0175-120">You must also download and save the following template for the sample report:</span></span>

- [<span data-ttu-id="c0175-121">Susietas mokėjimo ataskaitos šablonas Nr. 2 (SampleVendPaymDocReportBounded2.docx)</span><span class="sxs-lookup"><span data-stu-id="c0175-121">Bounded Template 2 of Payment Report (SampleVendPaymDocReportBounded2.docx)</span></span>](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a><span data-ttu-id="c0175-122">Peržiūrėkite atsisiųstą „Word” šabloną</span><span class="sxs-lookup"><span data-stu-id="c0175-122">Review the downloaded Word template</span></span>

1. <span data-ttu-id="c0175-123">„Word” darbalaukio programoje atidarykite **SampleVendPaymDocReportBounded2.docx** šablono failą, kurį atsisiuntėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="c0175-123">In the Word desktop application, open the **SampleVendPaymDocReportBounded2.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="c0175-124">Patikrinkite, ar šablono faile yra suvestinės skyrius, kuriame rodomos kiekvieno valiutos kodo, kurį atitiko apdoroti mokėjimai, bendros mokėjimo sumos.</span><span class="sxs-lookup"><span data-stu-id="c0175-124">Verify that the template file contains a summary section that shows the total payment amounts for every currency code that has been met in the processed payments.</span></span>

    - <span data-ttu-id="c0175-125">Suvestinės dalis yra atskiroje „Word” dokumento lentelėje.</span><span class="sxs-lookup"><span data-stu-id="c0175-125">The summary section resides in a separate table of the Word document.</span></span>
    - <span data-ttu-id="c0175-126">Pirmoje šios lentelės eilutėje lentelės stulpelių antraštės yra sekcijos antraštė.</span><span class="sxs-lookup"><span data-stu-id="c0175-126">The first row of this table holds the table columns headings as the section header.</span></span>
    - <span data-ttu-id="c0175-127">Antroje šios lentelės eilutėje kaip išsami informacija apie sekciją yra pasikartojantis turinio valdiklis.</span><span class="sxs-lookup"><span data-stu-id="c0175-127">The second row of this table holds the repeating content control as the section details.</span></span>
    - <span data-ttu-id="c0175-128">Šis turinio valdiklis yra susietas su **SuvestinėsEilutės** lauko **Ataskaita** tinkintos XML dalies.</span><span class="sxs-lookup"><span data-stu-id="c0175-128">This content control is mapped to the **SummaryLines** field of the **Report** custom XML part.</span></span>
    - <span data-ttu-id="c0175-129">Pagal šį susiejimą turinio valdiklis yra susietas su **SuvestinėsEilutės** redaguotino ER formato elementu.</span><span class="sxs-lookup"><span data-stu-id="c0175-129">Based on this mapping, the content control is associated with the **SummaryLines** element of the editable ER format.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c0175-130">Pasikartojantis turinio valdiklis žymimas **SuvestinėsEilutės** raktu, atitinkančiu pasirinktinės susietos XML dalies lauką.</span><span class="sxs-lookup"><span data-stu-id="c0175-130">The repeating content control is tagged by the **SummaryLines** key that matches the field of the custom XML part that it has been mapped to.</span></span>

    ![„Word” šablono maketas](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="c0175-132">Pasirinkite esamą ER ataskaitos konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="c0175-132">Select the existing ER report configuration</span></span>

<span data-ttu-id="c0175-133">Toliau nurodytus veiksmus atlikite iš naujo naudodami esamą ER konfigūraciją, kurią konfigūravote, kai įbaigsite anksčiau paminėtuose užduočių vadovuose nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c0175-133">For the following steps, you will reuse the existing ER configuration that you configured when you completed the steps in the previously mentioned task guides.</span></span>

1. <span data-ttu-id="c0175-134">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="c0175-134">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="c0175-135">Pasirinkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="c0175-135">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="c0175-136">Puslapyje **Konfigūracijos** konfigūracijų medžio kairinėje srityje išskleiskite **Mokėjimo modelis**, o tada pasirinkite **Darbalapio ataskaitos pavyzdys**.</span><span class="sxs-lookup"><span data-stu-id="c0175-136">On the **Configurations** page, in the configuration tree, expand **Payment model**, and select **Sample worksheet report**.</span></span>
4. <span data-ttu-id="c0175-137">Pasirinkite **Kūrimo įrankis**, kad galėtumėte redaguoti pasirinkto ER formato juodraščio versiją.</span><span class="sxs-lookup"><span data-stu-id="c0175-137">Select **Designer** to edit the draft version of the selected ER format.</span></span>

## <a name="replace-the-current-template-with-the-new-template"></a><span data-ttu-id="c0175-138">Pakeiskite esamą šabloną nauju šablonu</span><span class="sxs-lookup"><span data-stu-id="c0175-138">Replace the current template with the new template</span></span>

<span data-ttu-id="c0175-139">Šiuo metu SampleVendPaymDocReportBounded.docx failas naudojamas kaip šablonas „Word” formato išvesčiai generuoti.</span><span class="sxs-lookup"><span data-stu-id="c0175-139">Currently, the SampleVendPaymDocReportBounded.docx file is used as a template to generate the output in Word format.</span></span> <span data-ttu-id="c0175-140">Atlikdami kitus veiksmus, pakeisite šį „Word” šabloną nauju „Word” šablonu, SampleVendPaymDocReportBounded2.docx, kurį atsisiuntėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="c0175-140">In the following steps, you will replace this Word template with the new Word template, SampleVendPaymDocReportBounded2.docx, that you downloaded earlier.</span></span>

1. <span data-ttu-id="c0175-141">Puslapyje **Formato kūrimo įrankis** pasirinkite **Priedai**.</span><span class="sxs-lookup"><span data-stu-id="c0175-141">On the **Format designer** page, select **Attachments**.</span></span>
2. <span data-ttu-id="c0175-142">Puslapyje **Priedai** pasirinkite **Naikinti**, kad pašalintumėte esamą „Excel” šabloną.</span><span class="sxs-lookup"><span data-stu-id="c0175-142">On the **Attachments** page, select **Delete** to remove the existing template.</span></span>
3. <span data-ttu-id="c0175-143">Norėdami patvirtinti sunaikinimo operaciją, pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="c0175-143">Select **Yes** to confirm the deletion.</span></span>
4. <span data-ttu-id="c0175-144">Pasirinkite **Naujas** \> **Failas**.</span><span class="sxs-lookup"><span data-stu-id="c0175-144">Select **New** \> **File**.</span></span>
5. <span data-ttu-id="c0175-145">Pasirinkite **Naršyti**, o tada pereikite ir pasirinkite **SampleVendPaymDocReportBounded2.docx** failą, kurį atsisiuntėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="c0175-145">Select **Browse**, and browse to and select the **SampleVendPaymDocReportBounded2.docx** file that you downloaded earlier.</span></span>
6. <span data-ttu-id="c0175-146">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c0175-146">Select **OK**.</span></span>
7. <span data-ttu-id="c0175-147">Uždarykite puslapį **Priedai**.</span><span class="sxs-lookup"><span data-stu-id="c0175-147">Close the **Attachments** page.</span></span>
8. <span data-ttu-id="c0175-148">**Formato kūrimo įrankis** puslapyje, **Šablonas** lauke įveskite arba pasirinkite **SampleVendPaymDocReportBounded2.docx** failą.</span><span class="sxs-lookup"><span data-stu-id="c0175-148">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReportBounded2.docx** file.</span></span>

## <a name="run-the-format-to-create-word-output"></a><span data-ttu-id="c0175-149">Paleiskite formatą, kad sukurtumėte „Word“ išvestį</span><span class="sxs-lookup"><span data-stu-id="c0175-149">Run the format to create Word output</span></span>

1. <span data-ttu-id="c0175-150">Eikite į **Mokėtinos sąskaitos** \> **Mokėjimai** \> **Mokėjimų žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="c0175-150">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="c0175-151">Puslapyje **Tiekėjų mokėjimai**, **Sąrašas** skirtuke pasirinkite visus mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="c0175-151">On the **Vendor payments** page, on the **List** tab, select all the payments.</span></span>
3. <span data-ttu-id="c0175-152">Pasirinkite **Mokėjimo būsena** \> **Nėra**.</span><span class="sxs-lookup"><span data-stu-id="c0175-152">Select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="c0175-153">Pasirinkite **Generuoti mokėjimus**.</span><span class="sxs-lookup"><span data-stu-id="c0175-153">Select **Generate payments**.</span></span>
5. <span data-ttu-id="c0175-154">Lauke **Mokėjimo būdas** pasirinkite **Elektroninis**.</span><span class="sxs-lookup"><span data-stu-id="c0175-154">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="c0175-155">Lauke **Banko sąskaita** įveskite **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="c0175-155">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="c0175-156">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c0175-156">Select **OK**.</span></span>
8. <span data-ttu-id="c0175-157">**Elektroninės ataskaitos parametrai** dialogo lange pasirinkite **Gerai** ir išanalizuokite sugeneruotą išeigą.</span><span class="sxs-lookup"><span data-stu-id="c0175-157">In the **Electronic report parameters** dialog box, select **OK**, and analyze the generated output.</span></span>

    ![Apdorotini mokėjimai puslapyje Tiekėjo mokėjimai](./media/er-design-configuration-word-suppress-controls-image2.gif)

    <span data-ttu-id="c0175-159">Išvestis pateikiama „Word” formatu ir joje yra suvestinės dalis.</span><span class="sxs-lookup"><span data-stu-id="c0175-159">The output is presented in Word format and contains the summary section.</span></span>

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a><span data-ttu-id="c0175-160">Konfigūruokite redaguojamą formatą, kad suvestinės skyrius būtų nerodomas</span><span class="sxs-lookup"><span data-stu-id="c0175-160">Configure the editable format to suppress the summary section</span></span>

<span data-ttu-id="c0175-161">Jei norite nerodyti suvestinės skyriaus sugeneruotame dokumente, remiantis vartotojo, kuris paleidžia šį ER formatą, užklausa, turite modifikuoti redaguojamą ER formatą.</span><span class="sxs-lookup"><span data-stu-id="c0175-161">If you want to suppress the summary section in a generated document, based on the request of a user who runs this ER format, you must modify the editable ER format.</span></span>

1. <span data-ttu-id="c0175-162">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos** ir atidarykite ER formato juodraščio versiją, kad jį suredaguotumėte.</span><span class="sxs-lookup"><span data-stu-id="c0175-162">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**, and open the draft version of the ER format for editing.</span></span>
2. <span data-ttu-id="c0175-163">Pasirinkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="c0175-163">Select **Reporting configurations**.</span></span> 
3. <span data-ttu-id="c0175-164">**Konfigūracijos** puslapyje, konfigūracijų medyje, išplėskite **Mokėjimo modelis** \> **Darbalapio ataskaitos pavyzdys**.</span><span class="sxs-lookup"><span data-stu-id="c0175-164">On the **Configurations** page, in the configuration tree, expand **Payment model** \> **Sample worksheet report**.</span></span>
4. <span data-ttu-id="c0175-165">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="c0175-165">Select **Designer**.</span></span>
5. <span data-ttu-id="c0175-166">**Formato kūrimo įrankis** puslapyje išplėskite **„Word”** ir pasirinkite **SuvestinėsEilutės**.</span><span class="sxs-lookup"><span data-stu-id="c0175-166">On the **Format designer** page, expand **Word**, and select **SummaryLines**.</span></span>
6. <span data-ttu-id="c0175-167">**Susiejimas** skirtuke, pridėkite duomenų šaltinį, kad paklaustumėte vartotojo, ar apdorojimo metu nerodyti suvestinės sekcijos:</span><span class="sxs-lookup"><span data-stu-id="c0175-167">On the **Mapping** tab, add a new data source to ask the user, at runtime, whether the summary section should be suppressed:</span></span>

    1. <span data-ttu-id="c0175-168">Pasirinkite **Įtraukti šaknį**.</span><span class="sxs-lookup"><span data-stu-id="c0175-168">Select **Add root**.</span></span>
    2. <span data-ttu-id="c0175-169">**Pridėti duomenų šaltinį** dialogo lange pasirinkite **Bendras / Vartotojo įvesties parametras**, kad atidarytumėte **Vartotojo įvesties parametro duomenų šaltinio ypatybės** dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c0175-169">In the **Add data source** dialog box, select **General\User input parameter** to open the **'User input parameter' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="c0175-170">Lauke **Pavadinimas** įveskite **uipNerodyti**.</span><span class="sxs-lookup"><span data-stu-id="c0175-170">In the **Name** field, enter **uipSuppress**.</span></span>
    4. <span data-ttu-id="c0175-171">Lauke **Žyma** įveskite **Nerodyti suvestinės sekcijos**.</span><span class="sxs-lookup"><span data-stu-id="c0175-171">In the **Label** field, enter **Suppress summary section**.</span></span>
    5. <span data-ttu-id="c0175-172">Lauke **Operacijų duomenų tipo pavadinimas** lauke pasirinkite arba įveskite **NeTaip**.</span><span class="sxs-lookup"><span data-stu-id="c0175-172">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="c0175-173">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c0175-173">Select **OK**.</span></span>

7. <span data-ttu-id="c0175-174">Pridėkite naują duomenų šaltinį **NeTaip** programos išvardijimo tipo:</span><span class="sxs-lookup"><span data-stu-id="c0175-174">Add a new data source of the **NoYes** application enumeration type:</span></span>

    1. <span data-ttu-id="c0175-175">Pasirinkite **Įtraukti šaknį**.</span><span class="sxs-lookup"><span data-stu-id="c0175-175">Select **Add root**.</span></span>
    2. <span data-ttu-id="c0175-176">**Pridėti duomenų šaltinį** dialogo lange pasirinkite **Dynamics 365 for Operations\Išvardijimas**, kad atidarytumėte **„Išvardijimo” duomenų šaltinio ypatybės** dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c0175-176">In the **Add data source** dialog box, select **Dynamics 365 for Operations\Enumeration** to open the **'Enumeration' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="c0175-177">Lauke **Pavadinimas** įveskite **enumNeTaip**.</span><span class="sxs-lookup"><span data-stu-id="c0175-177">In the **Name** field, enter **enumNoYes**.</span></span>
    4. <span data-ttu-id="c0175-178">Lauke **Žyma** įveskite **Nerodyti parinkčių**.</span><span class="sxs-lookup"><span data-stu-id="c0175-178">In the **Label** field, enter **Suppress options**.</span></span>
    5. <span data-ttu-id="c0175-179">Lauke **Operacijų duomenų tipo pavadinimas** lauke pasirinkite arba įveskite **NeTaip**.</span><span class="sxs-lookup"><span data-stu-id="c0175-179">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="c0175-180">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c0175-180">Select **OK**.</span></span>

8. <span data-ttu-id="c0175-181">Pasirinktam **SuvestinėsEilutės** formato elementui, sukonfigūruokite formulę, nurodančią, kada „Word” turinio valdiklis, susietas su pasirinktu formato elementu, turi būti nerodomas:</span><span class="sxs-lookup"><span data-stu-id="c0175-181">For the selected **SummaryLines** format element, configure the formula to specify when the Word content control that is associated with the selected format element should be suppressed:</span></span>

    1. <span data-ttu-id="c0175-182">**Susiejimas** skirtuke, **Pašalinta** dalyje, pasirinkite **Redaguoti**, kad atidarytumėte **[Formulės kūrimo įrankio](general-electronic-reporting-formula-designer.md)** puslapį.</span><span class="sxs-lookup"><span data-stu-id="c0175-182">On the **Mapping** tab, in the **Removed** section, select **Edit** to open the **[Formula designer](general-electronic-reporting-formula-designer.md)** page.</span></span>
    2. <span data-ttu-id="c0175-183">**Formulė** lauke įveskite formulę `uipSuppress = enumNoYes.Yes`.</span><span class="sxs-lookup"><span data-stu-id="c0175-183">In the **Formula** field, enter the formula `uipSuppress = enumNoYes.Yes`.</span></span>
    3. <span data-ttu-id="c0175-184">Pasirinkite **Įrašyti** ir uždarykite puslapį **Formulių dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="c0175-184">Select **Save**, and close the **Formula designer** page.</span></span>

        > [!NOTE]
        > <span data-ttu-id="c0175-185">Ši formulė bus taikoma sugeneruotame dokumente, **kai bus paleisti visi kiti formato elementai**.</span><span class="sxs-lookup"><span data-stu-id="c0175-185">This formula will be applied to a generated document **after all other format elements are run**.</span></span> <span data-ttu-id="c0175-186">Norėdami taikyti šią formulę, sugeneruotame dokumente randamas „Word” turinio valdiklis, žymimas kaip formato elementas, kurį sukonfigūravo formulė (šiuo atveju **SuvestinėsEilutės**).</span><span class="sxs-lookup"><span data-stu-id="c0175-186">To apply this formula, a Word content control that is tagged as a format element that the formula is configured for (**SummaryLines** in this case) is found in a generated document.</span></span> <span data-ttu-id="c0175-187">Tada šis turinio valdiklis yra visiškai pašalintas kartu su „Word” lentelės eilute, kurioje jis yra.</span><span class="sxs-lookup"><span data-stu-id="c0175-187">That content control is then completely removed, together with the row in the Word table that holds it.</span></span> <span data-ttu-id="c0175-188">Suvestinės skyriaus informacijos eilutė pašalinama iš sugeneruoto dokumento.</span><span class="sxs-lookup"><span data-stu-id="c0175-188">The details row of the summary section is removed from the generated document.</span></span>
        >
        > <span data-ttu-id="c0175-189">Kūrimo metu galite konfigūruoti formato elementą **Pašalinta**, tačiau nei vienas jūsų naudojamas turinio valdiklis „Word” šablone neturi žymos, atitinkančios formato elemento pavadinimą, pagal kurį **Pašalinta** ypatybė yra sukonfigūruota.</span><span class="sxs-lookup"><span data-stu-id="c0175-189">At design time, you might configure the **Removed** formula for a format element, even though no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span> <span data-ttu-id="c0175-190">Kai tikrinate formatą kūrimo metu, gaunate [perspėjimą](er-components-inspections.md#i14) apie šį nesutapimą.</span><span class="sxs-lookup"><span data-stu-id="c0175-190">When you validate the format at design time, you receive a [warning](er-components-inspections.md#i14) about this inconsistency.</span></span>
        >
        > <span data-ttu-id="c0175-191">Apdorojimo metu pateikiama išimtis, jei nėra „Word” šablono, kurį naudojate, turinio valdiklio žymės, kuri atitinka formato elemento, kurio sukonfigūruota ypatybė **Pašalinta** pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c0175-191">At runtime, an exception is thrown if no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span>

    4. <span data-ttu-id="c0175-192">Skirtuko **Susiejimas**, **Pašalinta** dalyje, nustatykite **Su tėviniu** parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="c0175-192">On the **Mapping** tab, in the **Removed** section, set the **With parent** option to **Yes**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="c0175-193">Turite nustatyti parinktį į **Taip**, kad pašalintumėte visą „Word” lentelę kaip eilutės pirminį objektą, kuriame yra suvestinės skyriaus informacija.</span><span class="sxs-lookup"><span data-stu-id="c0175-193">You must set this option to **Yes** to remove the whole Word table as the parent object of the row that holds the summary section details.</span></span> <span data-ttu-id="c0175-194">Jei nustatote šią parinktį į **Ne**, skyriaus antraštės eilutė lieka sugeneruotame dokumente.</span><span class="sxs-lookup"><span data-stu-id="c0175-194">If you set this option to **No**, the section header row remains in the generated document.</span></span>

9. <span data-ttu-id="c0175-195">Pasirinkite **Įrašyti** tam, kad išsaugotumėte pakeitimus redaguotiname formate.</span><span class="sxs-lookup"><span data-stu-id="c0175-195">Select **Save** to save your changes to the editable format.</span></span>

    ![Sugeneruota išvestis „Word” formatu](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a><span data-ttu-id="c0175-197">Paleiskite pakeistą formatą, kad sukurtumėte „Word“ išvestį</span><span class="sxs-lookup"><span data-stu-id="c0175-197">Run the modified format to create Word output</span></span>

1. <span data-ttu-id="c0175-198">Eikite į **Mokėtinos sąskaitos** \> **Mokėjimai** \> **Mokėjimų žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="c0175-198">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="c0175-199">Pasirinkite jūsų sukurtą mokėjimo žurnalą, tada pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="c0175-199">Select the payment journal that you created, and then select **Lines**.</span></span>
3. <span data-ttu-id="c0175-200">Puslapyje **Tiekėjo mokėjimai** pasirinkite visas eilutes, tada pasirinkite **Mokėjimo būsena**\> **Nėra**.</span><span class="sxs-lookup"><span data-stu-id="c0175-200">On the **Vendor payments** page, select all the rows, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="c0175-201">Pasirinkite **Generuoti mokėjimus**.</span><span class="sxs-lookup"><span data-stu-id="c0175-201">Select **Generate payments**.</span></span>
5. <span data-ttu-id="c0175-202">Lauke **Mokėjimo būdas** pasirinkite **Elektroninis**.</span><span class="sxs-lookup"><span data-stu-id="c0175-202">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="c0175-203">Lauke **Banko sąskaita** įveskite **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="c0175-203">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="c0175-204">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c0175-204">Select **OK**.</span></span>
8. <span data-ttu-id="c0175-205">**Elektroninės ataskaitos parametrai** dialogo lange, lauke **Nerodyti suvestinės skyriaus** lauke, pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="c0175-205">In the **Electronic report parameters** dialog box, in the **Suppress summary section** field, select **Yes**.</span></span>
9. <span data-ttu-id="c0175-206">Pasirinkite **Gerai** ir analizuokite sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="c0175-206">Select **OK**, and analyze the generated output.</span></span>

    ![Sugeneruota išvestis „Word” formatu](./media/er-design-configuration-word-suppress-controls-image4.gif)

    <span data-ttu-id="c0175-208">Atkreipkite dėmesį, kad išvestyje nėra suvestinės skyriaus, nes jis nerodomas.</span><span class="sxs-lookup"><span data-stu-id="c0175-208">Notice that the output doesn't contain the summary section, because it has been suppressed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c0175-209">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c0175-209">Additional resources</span></span>

- [<span data-ttu-id="c0175-210">Konfigūracijos, skirtos ataskaitoms OPENXML formatu generuoti, kūrimas</span><span class="sxs-lookup"><span data-stu-id="c0175-210">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="c0175-211">Ataskaitų generavimo „Word“ formatu naujos ER konfigūracijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="c0175-211">Design a new ER configuration to generate reports in Word format</span></span>](er-design-configuration-word.md)
- [<span data-ttu-id="c0175-212">Pakartotinai naudokite ER konfigūracijas su „Excel“ šablonais, kad sugeneruotumėte ataskaitas „Word“ formatu</span><span class="sxs-lookup"><span data-stu-id="c0175-212">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)
- [<span data-ttu-id="c0175-213">Sukonfigūruoto ER komponento patikrinimas, kad nekiltų vykdymo problemų</span><span class="sxs-lookup"><span data-stu-id="c0175-213">Inspect the configured ER component to prevent runtime issues</span></span>](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]