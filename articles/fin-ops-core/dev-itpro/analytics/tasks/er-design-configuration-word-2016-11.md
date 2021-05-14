---
title: ER konfigūracijų su „Excel” šablonais, skirtų ataskaitų „Word” formatu generavimui, pakartotinis naudojimas
description: Šioje temoje aprašoma, kaip ataskaitai formatai, skirti generuoti ataskaitoms kaip „Excel” darbaknygėms, gali būti konfigūruojami ataskaitų kaip „Word” dokumentų konfigūravimui.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 413be634e80b87781444e1c1445c78691f4b4b0b
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944297"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a><span data-ttu-id="ebd5e-103">ER konfigūracijų su „Excel” šablonais, skirtų ataskaitų „Word” formatu generavimui, pakartotinis naudojimas</span><span class="sxs-lookup"><span data-stu-id="ebd5e-103">Reuse ER configurations with Excel templates to generate reports in Word format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ebd5e-104">Norėdami generuoti ataskaitas kaip „Microsoft Word” dokumentus, galite [konfigūruoti](../er-design-configuration-word.md) naują [Elektroninių ataskaitų (ER)](../general-electronic-reporting.md) [formatą](../general-electronic-reporting.md#FormatComponentOutbound).</span><span class="sxs-lookup"><span data-stu-id="ebd5e-104">To generate reports as Microsoft Word documents, you can [configure](../er-design-configuration-word.md) a new [Electronic reporting (ER)](../general-electronic-reporting.md) [format](../general-electronic-reporting.md#FormatComponentOutbound).</span></span> <span data-ttu-id="ebd5e-105">Arba galite pakartotinai naudoti ER formatą, kuris iš pradžių buvo sukurtas generuoti ataskaitoms kaip „Excel” darbaknygėms.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-105">Alternatively, you can reuse an ER format that was originally designed to generate reports as Excel workbooks.</span></span> <span data-ttu-id="ebd5e-106">Šiuo atveju turite pakeisti „Excel” šabloną į „Word” šabloną.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-106">In this case, you must replace the Excel template with a Word template.</span></span>

<span data-ttu-id="ebd5e-107">Tolesnės procedūros rodo, kaip vartotojas sistemos administratoriaus vaidmenyje arba elektroninės ataskaitos kūrėjo vaidmenyje gali konfigūruoti ER formatą, skirtą generuoti ataskaitoms kaip „Word” failams, pakartotinai naudodamas ER formatą, kuris buvo sukurtas generuoti ataskaitoms kaip „Excel” failams.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-107">The following procedures show how a user in either the System administrator role or the Electronic reporting developer role can configure an ER format to generate reports as Word files by reusing an ER format that was designed to generate reports as Excel files.</span></span>

<span data-ttu-id="ebd5e-108">Šias procedūras galima užbaigti GBSI įmonėje.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-108">These procedures can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ebd5e-109">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="ebd5e-109">Prerequisites</span></span>

<span data-ttu-id="ebd5e-110">Norėdami užbaigti šias procedūras, pirmiausia turite atlikti užduočių vedlyje [Konfigūracijos, skirtos ataskaitoms „OPENXML” formatu generuoti, kūrimas](er-design-reports-openxml-2016-11.md) nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-110">To complete these procedures, you must first follow the steps in the [Design a configuration for generating reports in OPENXML format](er-design-reports-openxml-2016-11.md) task guide.</span></span>

<span data-ttu-id="ebd5e-111">Taip pat turite atsisiųsti ir įrašyti vietoje šiuos šablonus ataskaitos pavyzdžiui:</span><span class="sxs-lookup"><span data-stu-id="ebd5e-111">You must also download and locally save the following templates for the sample report:</span></span>

- [<span data-ttu-id="ebd5e-112">Mokėjimo ataskaitos šablonas (SampleVendPaymDocReport.docx)</span><span class="sxs-lookup"><span data-stu-id="ebd5e-112">Template of Payment Report (SampleVendPaymDocReport.docx)</span></span>](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [<span data-ttu-id="ebd5e-113">Susietas mokėjimo ataskaitos šablonas („SampleVendPaymDocReportBounded.docx”)</span><span class="sxs-lookup"><span data-stu-id="ebd5e-113">Bounded Template of Payment Report (SampleVendPaymDocReportBounded.docx)</span></span>](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

<span data-ttu-id="ebd5e-114">Šios procedūros skirtos funkcijai, kuri buvo įtraukta į 1611 „Dynamics 365 for Operations” versiją (2016 m. lapkričio mėn).</span><span class="sxs-lookup"><span data-stu-id="ebd5e-114">These procedures are for a feature that was added in Dynamics 365 for Operations version 1611 (November 2016).</span></span>

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="ebd5e-115">Pasirinkite esamą ER ataskaitos konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="ebd5e-115">Select the existing ER report configuration</span></span>

1. <span data-ttu-id="ebd5e-116">„Dynamics 365 Finance” eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-116">In Dynamics 365 Finance, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ebd5e-117">Įsitikinkite, kad konfigūracijos teikėjas **„Litware, Inc.“** yra pasirinktas kaip **Aktyvus**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-117">Make sure that the **Litware, Inc.** configuration provider is selected as **Active**.</span></span> <span data-ttu-id="ebd5e-118">Jeigu nėra, atlikite veiksmus, nurodytus [Kurkite konfigūracijos teikėjus ir pažymėkite juos kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md) užduočių vedlyje.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-118">If it isn't, follow the steps in the [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) task guide.</span></span>
3. <span data-ttu-id="ebd5e-119">Pasirinkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-119">Select **Reporting configurations**.</span></span> <span data-ttu-id="ebd5e-120">Pakartotinai naudosite esamą ER konfigūraciją, kuri iš buvo sukurta ataskaitos išvesčiai „OPENXML” formatu generuoti.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-120">You will reuse the existing ER configuration that was designed to generate the report output in OPENXML format.</span></span>
4. <span data-ttu-id="ebd5e-121">Puslapio **Konfigūracijos** konfigūracijų medžio kairėje srityje išskleiskite **Mokėjimo modelis**, o tada pasirinkite **Pavyzdinė darbalapio ataskaita**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-121">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and select **Sample worksheet report**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ebd5e-122">Pasirinktos ER formato konfigūracijos šablono versiją galima redaguoti **Versijos** „FastTab” skirtuke.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-122">The draft version of the selected ER format can be edited on the **Versions** FastTab.</span></span>

5. <span data-ttu-id="ebd5e-123">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-123">Select **Designer**.</span></span>
6. <span data-ttu-id="ebd5e-124">Puslapyje **Formato dizaino įrankis** atkreipkite dėmesį, kad šakninio formato elemento pavadinimas nurodo, kad šiuo metu naudojamas „Excel” šablonas.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-124">On the **Format designer** page, notice that the title of the root format element indicates that an Excel template is currently used.</span></span>

![Esamos konfigūracijos pasirinkimas](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a><span data-ttu-id="ebd5e-126">Peržiūrėkite atsisiųstą „Word” šabloną</span><span class="sxs-lookup"><span data-stu-id="ebd5e-126">Review the downloaded Word template</span></span>

1. <span data-ttu-id="ebd5e-127">„Word” darbalaukio programoje atidarykite **„SampleVendPaymDocReport.docx”** šablono failą, kurį atsisiuntėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-127">In the Word desktop application, open the **SampleVendPaymDocReport.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="ebd5e-128">Patvirtinkite, kad šiame šablone yra tik dokumento maketas, kurį norite sugeneruoti kaip ER išvestį.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-128">Verify that the template contains only the layout of the document that you want to generate as ER output.</span></span>

![„Word” šablono maketas darbalaukio programoje](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a><span data-ttu-id="ebd5e-130">Pakeiskite „Excel” šabloną į „Word” šabloną ir įtraukite pasirinktinę XML dalį</span><span class="sxs-lookup"><span data-stu-id="ebd5e-130">Replace the Excel template with the Word template and add a custom XML part</span></span>

<span data-ttu-id="ebd5e-131">Šiuo metu „Excel” dokumentas naudojamas kaip šablonas OPENXML formato išvesčiai generuoti.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-131">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="ebd5e-132">Šį šabloną pakeisite į „Word” šablono failą „SampleVendPaymDocReport.docx”, kurį atsisiuntėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-132">You will replace this template with the SampleVendPaymDocReport.docx Word template file that you downloaded earlier.</span></span> <span data-ttu-id="ebd5e-133">Taip pat išplėsite „Word“ šabloną įtraukdami pasirinktinę XML dalį.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-133">You will also extend the Word template by adding a custom XML part.</span></span>

1. <span data-ttu-id="ebd5e-134">„Finance” puslapio **Formato dizaino įrankis** skirtuke **Formatas** pasirinkite **Priedai**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-134">In Finance, on the **Format designer** page, on the **Format** tab, select **Attachments**.</span></span>
2. <span data-ttu-id="ebd5e-135">Puslapyje **Priedai** pasirinkite **Naikinti** esamo „Excel” šablono pašalinimui.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-135">On the **Attachments** page, select **Delete** to remove the existing Excel template.</span></span> <span data-ttu-id="ebd5e-136">Pasirinkite **Taip** pakeitimo patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-136">Select **Yes** to confirm the change.</span></span>
3. <span data-ttu-id="ebd5e-137">Pasirinkite **Naujas** \> **Failas**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-137">Select **New** \> **File**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ebd5e-138">Turite pasirinkti dokumento tipą, kuris buvo [sukonfigūruotas](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) naudojant ER parametrus, kad išsaugotumėte ER formato šablonus.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-138">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

4. <span data-ttu-id="ebd5e-139">Pasirinkite **Naršyti**, o tada pereikite ir pasirinkite **„SampleVendPaymDocReport.docx”** failą, kurį atsisiuntėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-139">Select **Browse**, and then browse to and select the **SampleVendPaymDocReport.docx** file that you downloaded earlier.</span></span>
5. <span data-ttu-id="ebd5e-140">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-140">Select **OK**.</span></span>
6. <span data-ttu-id="ebd5e-141">Uždarykite puslapį **Priedai**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-141">Close the **Attachments** page.</span></span>
7. <span data-ttu-id="ebd5e-142">Puslapio **Formato dizaino įrankis** lauke **Šablonas** įveskite arba pasirinkite **„SampleVendPaymDocReport.docx”** failą naudoti „Word” šablonui, vietoj anksčiau naudoto „Excel” šablono.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-142">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReport.docx** file to use that Word template instead of the Excel template that was previously used.</span></span>
8. <span data-ttu-id="ebd5e-143">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-143">Select **Save**.</span></span>

    <span data-ttu-id="ebd5e-144">Be to, kad išsaugomi konfigūracijos pakeitimai, veiksmas **Įrašyti** atnaujinamą pridėtą „Word” šabloną.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-144">In addition to storing configuration changes, the **Save** action updates the attached Word template.</span></span> <span data-ttu-id="ebd5e-145">Sukurto formato hierarchinė struktūra įtraukiama į pridėtą „Word” dokumentą kaip nauja pasirinktinė XML dalis, pavadinta **Ataskaita**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-145">The hierarchical structure of the designed format is added to the attached Word document as a new custom XML part that is named **Report**.</span></span> <span data-ttu-id="ebd5e-146">Pridėtame „Word” šablone yra dokumento maketas, kuris bus sugeneruotas kaip ER išvestis, ir duomenų struktūra, kurią apdorojimo metu ER įves į šį šabloną.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-146">The attached Word template contains the layout of the document that will be generated as ER output and the structure of data that ER will enter in that template at runtime.</span></span>

9. <span data-ttu-id="ebd5e-147">Atkreipkite dėmesį, kad šakninio formato elemento pavadinimas nurodo, kad šiuo metu naudojamas „Word” šablonas.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-147">Notice that the title of the root format element indicates that a Word template is currently used.</span></span>

    ![„Excel” šablono pakeitimas „Word” šablonu ir pasirinktinės XML dalies įtraukimas](../media/er-design-configuration-word-2016-11-image03.gif)

10. <span data-ttu-id="ebd5e-149">Skirtuke **Formatas** pasirinkite **Priedai.**</span><span class="sxs-lookup"><span data-stu-id="ebd5e-149">On the **Format** tab, select **Attachments**.</span></span>

<span data-ttu-id="ebd5e-150">Dabar galite susieti pasirinktinės XML dalies **Ataskaita** elementus su „Word“ dokumento turinio valdikliais.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-150">You can now map the elements of the **Report** custom XML part to the content controls of the Word document.</span></span>

<span data-ttu-id="ebd5e-151">Jei esate susipažinę su „Word“ dokumentų kaip formų, turinčių [turinio valdiklius](/office/client-developer/word/content-controls-in-word), susietus su [pasirinktinių XML dalių](/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) elementais, kūrimo procesu, atlikite visus tolesnės procedūros veiksmus, kad sukurtumėte tokį dokumentą.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-151">If you're familiar with the process of designing Word documents as forms that contain [content controls](/office/client-developer/word/content-controls-in-word) that are mapped to elements of [custom XML parts](/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), complete all steps in the next procedure to create the document.</span></span> <span data-ttu-id="ebd5e-152">Daugiau informacijos žiūrėkite [Formų, kurias vartotojai užbaigia ar spausdina programoje „Word“, kūrimas](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span><span class="sxs-lookup"><span data-stu-id="ebd5e-152">For more information, see [Create forms that users complete or print in Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span></span> <span data-ttu-id="ebd5e-153">Kitu atveju praleiskite tolesnę procedūrą.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-153">Otherwise, skip the next procedure.</span></span>

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a><span data-ttu-id="ebd5e-154">Gaukite „Word” dokumentą su pasirinktine XML dalimi ir atlikite duomenų susiejimą</span><span class="sxs-lookup"><span data-stu-id="ebd5e-154">Get a Word document that has a custom XML part and do data mapping</span></span>

1. <span data-ttu-id="ebd5e-155">„Finance” puslapyje **Priedai** pasirinkite **Atidaryti** šablono atsisiuntimui iš „Finance” ir jo saugojimui vietoje kaip „Word” dokumento.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-155">In Finance, on the **Attachments** page, select **Open** to download the selected template from Finance and store it locally as a Word document.</span></span>
3. <span data-ttu-id="ebd5e-156">„Word” darbalaukio programoje atidarykite ką tik atsisiųstą dokumentą.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-156">In the Word desktop application, open the document that you just downloaded.</span></span>
4. <span data-ttu-id="ebd5e-157">Skirtuke **Kūrėjas** pasirinkite **XML susiejimo sritis**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-157">On the **Developer** tab, select **XML Mapping Pane**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ebd5e-158">Jei juostelėje nerodomas **Programuotojo** skirtukas, tinkinkite juostelę jam įtraukti.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-158">If the **Developer** tab doesn't appear on the ribbon, customize the ribbon to add it.</span></span>

5. <span data-ttu-id="ebd5e-159">Srities **XML susiejimas** lauke **Pasirinktinė XML dalis** pasirinkite **Ataskaitos** pasirinktinę XML dalį.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-159">In the **XML Mapping** pane, in the **Custom XML Part** field, select the **Report** custom XML part.</span></span>
6. <span data-ttu-id="ebd5e-160">Susiekite pasirinktos **Ataskaitos** pasirinktinės XML dalies elementus ir „Word“ dokumento turinio valdiklius.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-160">Map the elements of the selected **Report** custom XML part and the content controls of the Word document.</span></span>
7. <span data-ttu-id="ebd5e-161">Įrašykite vietoje atnaujintą „Word” dokumentą kaip **„SampleVendPaymDocReportBounded.docx”**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-161">Save the updated Word document locally as **SampleVendPaymDocReportBounded.docx**.</span></span>

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="ebd5e-162">Peržiūrėti „Word“ šabloną, kuriame pasirinktinė XML dalis yra susieta su turinio valdikliais</span><span class="sxs-lookup"><span data-stu-id="ebd5e-162">Review the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="ebd5e-163">„Word” darbalaukio programoje atidarykite **„SampleVendPaymDocReportBounded.docx”** šablono failą.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-163">In the Word desktop application, open the **SampleVendPaymDocReportBounded.docx** template file.</span></span>
2. <span data-ttu-id="ebd5e-164">Patvirtinkite, kad šiame šablone yra dokumento maketas, kurį norite sugeneruoti kaip ER išvestį.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-164">Verify that the template contains the layout of the document that you want to generate as ER output.</span></span> <span data-ttu-id="ebd5e-165">Turinio valdikliai, kurie yra naudojami kaip vietos rezervavimo ženklai duomenims, ER įvedamiems į šį šabloną vykdymo metu, yra paremti susiejimais, sukonfigūruotais tarp **Ataskaitos** pasirinktinės XML dalies elementų ir „Word” dokumento turinio valdiklių.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-165">The content controls that are used as placeholders for data that ER will enter in this template at runtime are based on the mappings that are configured between elements of the **Report** custom XML part and the content controls of the Word document.</span></span>

![„Word” šablono peržiūra darbalaukio programoje](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="ebd5e-167">Įkelkite „Word“ šabloną, kuriame pasirinktinė XML dalis yra susieta su turinio valdikliais</span><span class="sxs-lookup"><span data-stu-id="ebd5e-167">Upload the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="ebd5e-168">„Finance” puslapyje **Priedai** pasirinkite **Naikinti** „Word” šabloną, kuriame nėra susiejimų tarp **Ataskaitos** pasirinktinės XML dalies ir turinio valdiklių.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-168">In Finance, on the **Attachments** page, select **Delete** to remove the Word template that has no mappings between elements of the **Report** custom XML part and content controls.</span></span> <span data-ttu-id="ebd5e-169">Pasirinkite **Taip** pakeitimo patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-169">Select **Yes** to confirm the change.</span></span>
2. <span data-ttu-id="ebd5e-170">Pasirinkite **Nauja** \> **Failas** pridėti naujam šablonui, kuriame yra susiejimai tarp **Ataskaitos** pasirinktinės XML dalies elementų ir turinio valdiklių.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-170">Select **New** \> **File** to add a new template file that contains mappings between elements of the **Report** custom XML part and content controls.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ebd5e-171">Turite pasirinkti dokumento tipą, kuris buvo [sukonfigūruotas](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) naudojant ER parametrus, kad išsaugotumėte ER formato šablonus.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-171">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

3. <span data-ttu-id="ebd5e-172">Pasirinkite **Naršyti**, o tada naršykite ir pasirinkite **„SampleVendPaymDocReportBounded.docx”** failą, kurį atsisiuntėte ar paruošėte atlikdami procedūrą, aprašytą [Gaukite „Word” su pasirinktine XML dalimi duomenų susiejimui](#get-word-doc) skyriuje.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-172">Select **Browse**, and then browse to and select the **SampleVendPaymDocReportBounded.docx** file that you downloaded or prepared by completing the procedure in the [Get a Word that has a custom XML part to do data mapping](#get-word-doc) section.</span></span>
4. <span data-ttu-id="ebd5e-173">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-173">Select **OK**.</span></span>
5. <span data-ttu-id="ebd5e-174">Uždarykite puslapį **Priedai**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-174">Close the **Attachments** page.</span></span>
6. <span data-ttu-id="ebd5e-175">Puslapio **Formato dizaino įrankis** lauke **Šablonas** pasirinkite ką tik atsisiųstą dokumentą.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-175">On the **Format designer** page, in the **Template** field, select the document that you just downloaded.</span></span>
7. <span data-ttu-id="ebd5e-176">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-176">Select **Save**.</span></span>
8. <span data-ttu-id="ebd5e-177">Uždarykite puslapį **Formato dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-177">Close the **Format designer** page.</span></span>

## <a name="mark-the-configured-format-as-runnable"></a><span data-ttu-id="ebd5e-178">Pažymėkite sukonfigūruotą formatą kaip vykdytiną</span><span class="sxs-lookup"><span data-stu-id="ebd5e-178">Mark the configured format as runnable</span></span>

<span data-ttu-id="ebd5e-179">Norėdami paleisti redaguojamo formato juodraščio versiją, turite ją padaryti [vykdytina](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span><span class="sxs-lookup"><span data-stu-id="ebd5e-179">To run the draft version of the editable format, you must make it [runnable](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span></span>

1. <span data-ttu-id="ebd5e-180">„Finance” puslapio **Konfigūracijos** veiksmų srities skirtuko **Konfigūracijos** grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-180">In Finance, on the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
2. <span data-ttu-id="ebd5e-181">**Vartotojo parametrai** dialogo lange nustatykite **Leisti parametrus** parinktį į **Taip** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-181">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
3. <span data-ttu-id="ebd5e-182">Pasirinkite **Redaguoti**, kad pagal poreikį galėtumėte redaguoti esamą puslapį.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-182">Select **Edit** to make the current page editable, as required.</span></span>
4. <span data-ttu-id="ebd5e-183">Šiuo metu pasirinktai **Pavyzdinio darbalapio ataskaitos** konfigūracijai nustatykite parinktį **Vykdyti juodraštį** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-183">For the currently selected **Sample worksheet report** configuration, set the **Run Draft** option to **Yes**.</span></span>
5. <span data-ttu-id="ebd5e-184">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-184">Select **Save**.</span></span>

## <a name="run-the-format-to-create-output-in-word-format"></a><span data-ttu-id="ebd5e-185">Vykdykite formatą išvesties „Word” formatu sukūrimui</span><span class="sxs-lookup"><span data-stu-id="ebd5e-185">Run the format to create output in Word format</span></span>

1. <span data-ttu-id="ebd5e-186">„Finance” eikite į **Mokėtinos sumos** \> **Mokėjimai** \> **Mokėjimų žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-186">In Finance, go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="ebd5e-187">Anksčiau įvestame mokėjimo žurnale pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-187">In a payment journal that you entered earlier, select **Lines**.</span></span>
3. <span data-ttu-id="ebd5e-188">Puslapyje **Tiekėjo mokėjimai** pasirinkite visas tinklelio eilutes.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-188">On the **Vendor payments** page, select all rows in the grid.</span></span>
4. <span data-ttu-id="ebd5e-189">Pasirinkite **Mokėjimo būsena** \> **Nėra**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-189">Select **Payment status** \> **None**.</span></span>

    ![Apdorotini mokėjimai puslapyje Tiekėjo mokėjimai](../media/er-design-configuration-word-2016-11-image05.png)

5. <span data-ttu-id="ebd5e-191">Veiksmų srityje pasirinkite **Generuoti mokėjimus**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-191">On the Action Pane, select **Generate payments**.</span></span>
6. <span data-ttu-id="ebd5e-192">Atsiradusiame dialogo lange atlikite toliau nurodytus veiksmus:</span><span class="sxs-lookup"><span data-stu-id="ebd5e-192">In the dialog box that appears, follow these steps:</span></span>

    1. <span data-ttu-id="ebd5e-193">Lauke **Mokėjimo būdas** pasirinkite **Elektroninis**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-193">In the **Method of payment** field, select **Electronic**.</span></span>
    2. <span data-ttu-id="ebd5e-194">Lauke **Banko sąskaita** įveskite **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-194">In the **Bank account** field, select **GBSI OPER**.</span></span>
    3. <span data-ttu-id="ebd5e-195">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-195">Select **OK**.</span></span>

7. <span data-ttu-id="ebd5e-196">Dialogo lange **Elektroninių ataskaitų parametrai** pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-196">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="ebd5e-197">Sugeneruota išvestis pateikiama „Word” formatu kartu su informacija apie apdorotus mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-197">The generated output is presented in Word format and contains the details of the processed payments.</span></span> <span data-ttu-id="ebd5e-198">Analizuokite sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="ebd5e-198">Analyze the generated output.</span></span>

    ![Sugeneruota išvestis „Word” formatu](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a><span data-ttu-id="ebd5e-200">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ebd5e-200">Additional resources</span></span>

- [<span data-ttu-id="ebd5e-201">Naujos ER konfigūracijos, skirtos ataskaitų generavimui „Word“ formatu, kūrimas</span><span class="sxs-lookup"><span data-stu-id="ebd5e-201">Design a new ER configuration to generate reports in Word format</span></span>](../er-design-configuration-word.md)
- [<span data-ttu-id="ebd5e-202">Vaizdų ir figūrų įterpimas generuojamuose dokumentuose naudojant ER</span><span class="sxs-lookup"><span data-stu-id="ebd5e-202">Embed images and shapes in documents that you generate by using ER</span></span>](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
