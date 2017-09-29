---
title: "Banko išrašo failo importavimo trikčių šalinimas"
description: "Svarbu, kad banko išrašo failas iš banko atitiktų maketą, kurį palaiko „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“. Dėl griežtų banko išrašų standartų, dauguma integravimų veiks tinkamai. Tačiau kartais išrašo failo nepavyksta importuoti arba rezultatai yra neteisingi. Paprastai šios problemos kyla dėl mažų skirtumų banko išrašo faile. Šiame straipsnyje paaiškinama, kaip pašalinti šiuos skirtumus ir išspręsti problemas."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 51cd32217b2f753f606e3060b4872a8274f16549
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="f4d08-107">Banko išrašo failo importavimo trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="f4d08-107">Bank statement file import troubleshooting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f4d08-108">Svarbu, kad banko išrašo failas iš banko atitiktų maketą, kurį palaiko „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“.</span><span class="sxs-lookup"><span data-stu-id="f4d08-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 for Finance and Operations, Enterprise edition supports.</span></span> <span data-ttu-id="f4d08-109">Dėl griežtų banko išrašų standartų, dauguma integravimų veiks tinkamai.</span><span class="sxs-lookup"><span data-stu-id="f4d08-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="f4d08-110">Tačiau kartais išrašo failo nepavyksta importuoti arba rezultatai yra neteisingi.</span><span class="sxs-lookup"><span data-stu-id="f4d08-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="f4d08-111">Paprastai šios problemos kyla dėl mažų skirtumų banko išrašo faile.</span><span class="sxs-lookup"><span data-stu-id="f4d08-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="f4d08-112">Šiame straipsnyje paaiškinama, kaip pašalinti šiuos skirtumus ir išspręsti problemas.</span><span class="sxs-lookup"><span data-stu-id="f4d08-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="f4d08-113">Kokia klaida?</span><span class="sxs-lookup"><span data-stu-id="f4d08-113">What is the error?</span></span>
------------------

<span data-ttu-id="f4d08-114">Pabandę importuoti banko išrašo failą, atidarykite užduoties Duomenų valdymas retrospektyvą ir jos vykdymo informaciją, kad rastumėte klaidą.</span><span class="sxs-lookup"><span data-stu-id="f4d08-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="f4d08-115">Klaida gali suteikti pagalbos, nurodydama išrašą, balansą arba išrašo eilutę.</span><span class="sxs-lookup"><span data-stu-id="f4d08-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="f4d08-116">Tačiau nėra tikėtina, kad ji suteiks pakankamai informacijos, padėsiančios jums nustatyti lauką arba elementą, dėl kurio kyla problema.</span><span class="sxs-lookup"><span data-stu-id="f4d08-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="f4d08-117">Kokie skirtumai?</span><span class="sxs-lookup"><span data-stu-id="f4d08-117">What are the differences?</span></span>
<span data-ttu-id="f4d08-118">Palyginkite banko failo maketo apibrėžimą su „Finance and Operations“ importo apibrėžimu ir pasižymėkite bet kokius laukų ir elementų skirtumus.</span><span class="sxs-lookup"><span data-stu-id="f4d08-118">Compare the bank file layout definition to the Finance and Operations import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="f4d08-119">Palyginkite banko išrašo failą su susijusiu „Finance and Operations“ failo pavyzdžiu.</span><span class="sxs-lookup"><span data-stu-id="f4d08-119">Compare the bank statement file to the related sample Finance and Operations file.</span></span> <span data-ttu-id="f4d08-120">ISO20022 failuose skirtumus pastebėti turėtų būti lengva.</span><span class="sxs-lookup"><span data-stu-id="f4d08-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="transformations"></a><span data-ttu-id="f4d08-121">Transformacijos</span><span class="sxs-lookup"><span data-stu-id="f4d08-121">Transformations</span></span>
<span data-ttu-id="f4d08-122">Paprastai keitimą reikia atlikti vienoje iš trijų transformacijų.</span><span class="sxs-lookup"><span data-stu-id="f4d08-122">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="f4d08-123">Kiekviena transformacija parašyta konkrečiam standartui.</span><span class="sxs-lookup"><span data-stu-id="f4d08-123">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="f4d08-124">Išteklių pavadinimas</span><span class="sxs-lookup"><span data-stu-id="f4d08-124">Resource name</span></span>                                         | <span data-ttu-id="f4d08-125">Failo vardas</span><span class="sxs-lookup"><span data-stu-id="f4d08-125">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="f4d08-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="f4d08-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="f4d08-127">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="f4d08-127">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="f4d08-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="f4d08-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="f4d08-129">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="f4d08-129">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="f4d08-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="f4d08-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="f4d08-131">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="f4d08-131">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="f4d08-132">Transformacijų derinimas</span><span class="sxs-lookup"><span data-stu-id="f4d08-132">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="f4d08-133">BAI2 ir MT940 failų koregavimas</span><span class="sxs-lookup"><span data-stu-id="f4d08-133">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="f4d08-134">BAI2 ir MT940 failai yra tekstiniai failai ir juos reikia koreguoti, norint įjungti išplėstinės stiliaus aprašų kalbos transformacijų (XSLT) derinimą.</span><span class="sxs-lookup"><span data-stu-id="f4d08-134">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="f4d08-135">Programa atlieka šį koregavimą, kai failas importuojamas.</span><span class="sxs-lookup"><span data-stu-id="f4d08-135">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="f4d08-136">Kurkite XML failą ir į jį nukopijuokite tolesnį tekstą.</span><span class="sxs-lookup"><span data-stu-id="f4d08-136">Create an XML file, and copy the following text into it.</span></span>

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  <span data-ttu-id="f4d08-137">Nukopijuokite banko išrašo failo turinį ir įklijuokite jį į XML failą, kad jis pakeistų **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="f4d08-137">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="f4d08-138">XSLT derinimas</span><span class="sxs-lookup"><span data-stu-id="f4d08-138">Debug the XSLT</span></span>

<span data-ttu-id="f4d08-139">Daugiau informacijos žr. <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="f4d08-139">For more information, see <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="f4d08-140">Paleiskite „Microsoft Visual Studio“.</span><span class="sxs-lookup"><span data-stu-id="f4d08-140">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="f4d08-141">Kurkite konsolės programą.</span><span class="sxs-lookup"><span data-stu-id="f4d08-141">Create a console application.</span></span>
3.  <span data-ttu-id="f4d08-142">Atidarykite atitinkamą XSLT.</span><span class="sxs-lookup"><span data-stu-id="f4d08-142">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="f4d08-143">Spustelėkite XLST ir jos ypatybių puslapį.</span><span class="sxs-lookup"><span data-stu-id="f4d08-143">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="f4d08-144">Nustatykite įvestį į banko išrašo failo vietą.</span><span class="sxs-lookup"><span data-stu-id="f4d08-144">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="f4d08-145">Nurodykite išvesties vietą ir failo vardą.</span><span class="sxs-lookup"><span data-stu-id="f4d08-145">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="f4d08-146">Nustatykite reikiamus ribinius taškus.</span><span class="sxs-lookup"><span data-stu-id="f4d08-146">Set the required break points.</span></span>
8.  <span data-ttu-id="f4d08-147">Meniu spustelėkite **XML** &gt; **Pradėti derinti XSLT**.</span><span class="sxs-lookup"><span data-stu-id="f4d08-147">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="f4d08-148">XSTL išvesties formatavimas</span><span class="sxs-lookup"><span data-stu-id="f4d08-148">Format the XSLT output</span></span>

<span data-ttu-id="f4d08-149">Kai transformacija paleidžiama, ji sukuria išvesties failą, kurį galima peržiūrėti „Visual Studio“.</span><span class="sxs-lookup"><span data-stu-id="f4d08-149">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="f4d08-150">Naudokite CTRL + A, CTRL + K ir CTRL + D, norėdami greitai formatuoti išvesties failą.</span><span class="sxs-lookup"><span data-stu-id="f4d08-150">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="f4d08-151">Transformacijos koregavimas</span><span class="sxs-lookup"><span data-stu-id="f4d08-151">Adjust the transformation</span></span>

<span data-ttu-id="f4d08-152">Koreguokite transformaciją, norėdami banko išrašo faile gauti atitinkamą lauką arba elementą.</span><span class="sxs-lookup"><span data-stu-id="f4d08-152">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="f4d08-153">Tada susiekite tą lauką arba elementą su atitinkamu „Finance and Operations“ elementu.</span><span class="sxs-lookup"><span data-stu-id="f4d08-153">Then map that field or element to the appropriate Finance and Operations element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="f4d08-154">Debeto / kredito indikatorius</span><span class="sxs-lookup"><span data-stu-id="f4d08-154">Debit/credit indicator</span></span>

<span data-ttu-id="f4d08-155">Kartais debetai gali būti importuoti kaip kreditai, o kreditai gali importuoti kaip debetai.</span><span class="sxs-lookup"><span data-stu-id="f4d08-155">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="f4d08-156">Norėdami išspręsti šią problemą, pakeiskite atitinkamą XSLT.</span><span class="sxs-lookup"><span data-stu-id="f4d08-156">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="f4d08-157">Jeigu banko išrašai pateikiami iš kelių bankų, įsitikinkite, kad jie visi naudoja tą patį debeto / kredito metodą, arba sukurkite atskiras transformacijas.</span><span class="sxs-lookup"><span data-stu-id="f4d08-157">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="f4d08-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator šablonas</span><span class="sxs-lookup"><span data-stu-id="f4d08-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="f4d08-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit šablonas</span><span class="sxs-lookup"><span data-stu-id="f4d08-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="f4d08-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator šablonas</span><span class="sxs-lookup"><span data-stu-id="f4d08-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="f4d08-161">Banko išrašų formatų ir techninių maketų pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="f4d08-161">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="f4d08-162">Tolesnėje lentelėje pateikiami išplėstinio banko derinimo importavimo failo techninio maketo aprašų pavyzdžiai ir trys susijusių banko išrašo failų pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="f4d08-162">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="f4d08-163">Failų ir techninių maketų pavyzdžius galite atsisiųsti čia: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="f4d08-163">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="f4d08-164">Techninio maketo aprašas</span><span class="sxs-lookup"><span data-stu-id="f4d08-164">Technical layout definition</span></span>                             | <span data-ttu-id="f4d08-165">Banko išrašo failo pavyzdys</span><span class="sxs-lookup"><span data-stu-id="f4d08-165">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="f4d08-166">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="f4d08-166">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="f4d08-167">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="f4d08-167">MT940StatementExample</span></span>                |
| <span data-ttu-id="f4d08-168">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="f4d08-168">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="f4d08-169">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="f4d08-169">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="f4d08-170">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="f4d08-170">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="f4d08-171">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="f4d08-171">BAI2StatementExample</span></span>                 |





