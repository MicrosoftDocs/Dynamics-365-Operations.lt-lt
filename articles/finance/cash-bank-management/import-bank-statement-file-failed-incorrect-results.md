---
title: Banko išrašo failo importavimo trikčių šalinimas
description: Svarbu, kad banko išrašo failas iš banko atitiktų maketą, kurį palaiko „Microsoft Dynamics 365 Finance“. Dėl griežtų banko išrašų standartų, dauguma integravimų veiks tinkamai. Tačiau kartais išrašo failo nepavyksta importuoti arba rezultatai yra neteisingi. Paprastai šios problemos kyla dėl mažų skirtumų banko išrašo faile. Šiame straipsnyje paaiškinama, kaip pašalinti šiuos skirtumus ir išspręsti problemas.
author: panolte
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0e01881a6b68526479d27014d49a718069cffc9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815889"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="f2354-107">Banko išrašo failo importavimo trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="f2354-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2354-108">Svarbu, kad banko išrašo failas iš banko atitiktų maketą, kurį palaiko „Microsoft Dynamics 365 Finance“.</span><span class="sxs-lookup"><span data-stu-id="f2354-108">It's important that the bank statement file from the bank matches the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="f2354-109">Dėl griežtų banko išrašų standartų, dauguma integravimų veiks tinkamai.</span><span class="sxs-lookup"><span data-stu-id="f2354-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="f2354-110">Tačiau kartais išrašo failo nepavyksta importuoti arba rezultatai yra neteisingi.</span><span class="sxs-lookup"><span data-stu-id="f2354-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="f2354-111">Paprastai šios problemos kyla dėl mažų skirtumų banko išrašo faile.</span><span class="sxs-lookup"><span data-stu-id="f2354-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="f2354-112">Šiame straipsnyje paaiškinama, kaip pašalinti šiuos skirtumus ir išspręsti problemas.</span><span class="sxs-lookup"><span data-stu-id="f2354-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="f2354-113">Kokia klaida?</span><span class="sxs-lookup"><span data-stu-id="f2354-113">What is the error?</span></span>
------------------

<span data-ttu-id="f2354-114">Pabandę importuoti banko išrašo failą, atidarykite užduoties Duomenų valdymas retrospektyvą ir jos vykdymo informaciją, kad rastumėte klaidą.</span><span class="sxs-lookup"><span data-stu-id="f2354-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="f2354-115">Klaida gali suteikti pagalbos, nurodydama išrašą, balansą arba išrašo eilutę.</span><span class="sxs-lookup"><span data-stu-id="f2354-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="f2354-116">Tačiau nėra tikėtina, kad ji suteiks pakankamai informacijos, padėsiančios jums nustatyti lauką arba elementą, dėl kurio kyla problema.</span><span class="sxs-lookup"><span data-stu-id="f2354-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

> [!NOTE]
> <span data-ttu-id="f2354-117">Importuoti banko išrašai gali persidengti tik viename taške.</span><span class="sxs-lookup"><span data-stu-id="f2354-117">Imported bank statements can overlap only for single a point in time.</span></span>  <span data-ttu-id="f2354-118">Pavyzdžiui, jei išrašas baigiasi 2021 m. sausio 1 d. 12:00 val., tada kito išrašo pradžios data gali būti 12:00 AM, jarnuary 1, 2021 12:00:00 AM.</span><span class="sxs-lookup"><span data-stu-id="f2354-118">For example, if a statement ends at 12:00 AM on January 1, 2021, then beginning date for the next statement can be 12:00 AM on Jarnuary 1, 2021 12:00:00 AM.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="f2354-119">Kokie skirtumai?</span><span class="sxs-lookup"><span data-stu-id="f2354-119">What are the differences?</span></span>
<span data-ttu-id="f2354-120">Palyginkite banko failo maketo apibrėžimą su „Finance“ importo apibrėžimu ir pasižymėkite bet kokius laukų ir elementų skirtumus.</span><span class="sxs-lookup"><span data-stu-id="f2354-120">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="f2354-121">Palyginkite banko išrašo failą su susijusiu „Finance“ failo pavyzdžiu.</span><span class="sxs-lookup"><span data-stu-id="f2354-121">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="f2354-122">ISO20022 failuose skirtumus pastebėti turėtų būti lengva.</span><span class="sxs-lookup"><span data-stu-id="f2354-122">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="f2354-123">Importuotų banko išrašų laiko juostų skirtumai</span><span class="sxs-lookup"><span data-stu-id="f2354-123">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="f2354-124">Importavimo failo datos ir laiko reikšmės gali skirtis nuo datos ir laiko reikšmių, rodomų sprendime „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="f2354-124">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="f2354-125">Norėdami išvengti šio neatitikimo, puslapyje **Konfigūruoti duomenų šaltinius** pasirinkite laiko juostos nustatymus.</span><span class="sxs-lookup"><span data-stu-id="f2354-125">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="f2354-126">Daugiau informacijos apie laiko juostos nustatymų nurodymą žr. [Išplėstinio banko derinimo importo nustatymo procesas](set-up-advanced-bank-reconciliation-import-process.md).</span><span class="sxs-lookup"><span data-stu-id="f2354-126">For more information about entering a time zone preference, see [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md).</span></span>

## <a name="transformations"></a><span data-ttu-id="f2354-127">Pakeitimai</span><span class="sxs-lookup"><span data-stu-id="f2354-127">Transformations</span></span>
<span data-ttu-id="f2354-128">Paprastai keitimą reikia atlikti vienoje iš trijų transformacijų.</span><span class="sxs-lookup"><span data-stu-id="f2354-128">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="f2354-129">Kiekviena transformacija parašyta konkrečiam standartui.</span><span class="sxs-lookup"><span data-stu-id="f2354-129">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="f2354-130">Išteklių pavadinimas</span><span class="sxs-lookup"><span data-stu-id="f2354-130">Resource name</span></span>                                         | <span data-ttu-id="f2354-131">Failo vardas</span><span class="sxs-lookup"><span data-stu-id="f2354-131">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="f2354-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="f2354-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="f2354-133">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="f2354-133">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="f2354-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="f2354-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="f2354-135">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="f2354-135">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="f2354-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="f2354-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="f2354-137">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="f2354-137">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="f2354-138">Transformacijų derinimas</span><span class="sxs-lookup"><span data-stu-id="f2354-138">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="f2354-139">BAI2 ir MT940 failų koregavimas</span><span class="sxs-lookup"><span data-stu-id="f2354-139">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="f2354-140">BAI2 ir MT940 failai yra tekstiniai failai ir juos reikia koreguoti, norint įjungti išplėstinės stiliaus aprašų kalbos transformacijų (XSLT) derinimą.</span><span class="sxs-lookup"><span data-stu-id="f2354-140">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="f2354-141">Programa atlieka šį koregavimą, kai failas importuojamas.</span><span class="sxs-lookup"><span data-stu-id="f2354-141">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="f2354-142">Kurkite XML failą ir į jį nukopijuokite tolesnį tekstą.</span><span class="sxs-lookup"><span data-stu-id="f2354-142">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="f2354-143">Nukopijuokite banko išrašo failo turinį ir įklijuokite jį į XML failą, kad jis pakeistų **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="f2354-143">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="f2354-144">XSLT derinimas</span><span class="sxs-lookup"><span data-stu-id="f2354-144">Debug the XSLT</span></span>

<span data-ttu-id="f2354-145">Daugiau informacijos rasite <https://msdn.microsoft.com/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="f2354-145">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="f2354-146">Paleiskite „Visual Studio“.</span><span class="sxs-lookup"><span data-stu-id="f2354-146">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="f2354-147">Kurkite konsolės programą.</span><span class="sxs-lookup"><span data-stu-id="f2354-147">Create a console application.</span></span>
3.  <span data-ttu-id="f2354-148">Atidarykite atitinkamą XSLT.</span><span class="sxs-lookup"><span data-stu-id="f2354-148">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="f2354-149">Spustelėkite XLST ir jos ypatybių puslapį.</span><span class="sxs-lookup"><span data-stu-id="f2354-149">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="f2354-150">Nustatykite įvestį į banko išrašo failo vietą.</span><span class="sxs-lookup"><span data-stu-id="f2354-150">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="f2354-151">Nurodykite išvesties vietą ir failo vardą.</span><span class="sxs-lookup"><span data-stu-id="f2354-151">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="f2354-152">Nustatykite reikiamus ribinius taškus.</span><span class="sxs-lookup"><span data-stu-id="f2354-152">Set the required break points.</span></span>
8.  <span data-ttu-id="f2354-153">Meniu spustelėkite **XML** &gt; **Pradėti derinti XSLT**.</span><span class="sxs-lookup"><span data-stu-id="f2354-153">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="f2354-154">XSTL išvesties formatavimas</span><span class="sxs-lookup"><span data-stu-id="f2354-154">Format the XSLT output</span></span>

<span data-ttu-id="f2354-155">Kai transformacija paleidžiama, ji sukuria išvesties failą, kurį galima peržiūrėti „Visual Studio“.</span><span class="sxs-lookup"><span data-stu-id="f2354-155">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="f2354-156">Naudokite CTRL + A, CTRL + K ir CTRL + D, norėdami greitai formatuoti išvesties failą.</span><span class="sxs-lookup"><span data-stu-id="f2354-156">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="f2354-157">Transformacijos koregavimas</span><span class="sxs-lookup"><span data-stu-id="f2354-157">Adjust the transformation</span></span>

<span data-ttu-id="f2354-158">Koreguokite transformaciją, norėdami banko išrašo faile gauti atitinkamą lauką arba elementą.</span><span class="sxs-lookup"><span data-stu-id="f2354-158">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="f2354-159">Tada susiekite tą lauką arba elementą su atitinkamu „Finance“ elementu.</span><span class="sxs-lookup"><span data-stu-id="f2354-159">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="f2354-160">Debeto / kredito indikatorius</span><span class="sxs-lookup"><span data-stu-id="f2354-160">Debit/credit indicator</span></span>

<span data-ttu-id="f2354-161">Kartais debetai gali būti importuoti kaip kreditai, o kreditai gali importuoti kaip debetai.</span><span class="sxs-lookup"><span data-stu-id="f2354-161">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="f2354-162">Norėdami išspręsti šią problemą, pakeiskite atitinkamą XSLT.</span><span class="sxs-lookup"><span data-stu-id="f2354-162">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="f2354-163">Jeigu banko išrašai pateikiami iš kelių bankų, įsitikinkite, kad jie visi naudoja tą patį debeto / kredito metodą, arba sukurkite atskiras transformacijas.</span><span class="sxs-lookup"><span data-stu-id="f2354-163">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="f2354-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator šablonas</span><span class="sxs-lookup"><span data-stu-id="f2354-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="f2354-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit šablonas</span><span class="sxs-lookup"><span data-stu-id="f2354-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="f2354-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator šablonas</span><span class="sxs-lookup"><span data-stu-id="f2354-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="f2354-167">Banko išrašų formatų ir techninių maketų pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="f2354-167">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="f2354-168">Tolesnėje lentelėje pateikiami išplėstinio banko derinimo importavimo failo techninio maketo aprašų pavyzdžiai ir trys susijusių banko išrašo failų pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="f2354-168">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="f2354-169">Failų pavyzdžius ir techninius maketus galite atsisiųsti čia: [importuoti failo pavyzdžius](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span><span class="sxs-lookup"><span data-stu-id="f2354-169">You can download the example files and technical layouts here: [Import file examples](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span></span>  

| <span data-ttu-id="f2354-170">Techninio maketo aprašas</span><span class="sxs-lookup"><span data-stu-id="f2354-170">Technical layout definition</span></span>                             | <span data-ttu-id="f2354-171">Banko išrašo failo pavyzdys</span><span class="sxs-lookup"><span data-stu-id="f2354-171">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="f2354-172">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="f2354-172">DynamicsAXMT940Layout</span></span>                                   | [<span data-ttu-id="f2354-173">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="f2354-173">MT940StatementExample</span></span>](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| <span data-ttu-id="f2354-174">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="f2354-174">DynamicsAXISO20022Layout</span></span>                                | [<span data-ttu-id="f2354-175">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="f2354-175">ISO20022StatementExample</span></span>](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| <span data-ttu-id="f2354-176">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="f2354-176">DynamicsAXBAI2Layout</span></span>                                    | [<span data-ttu-id="f2354-177">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="f2354-177">BAI2StatementExample</span></span>](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
