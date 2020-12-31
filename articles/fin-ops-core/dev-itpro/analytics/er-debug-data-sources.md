---
title: Įvykdyto ER formato duomenų šaltinių derinimas duomenų srautams ir transformacijai analizuoti
description: Šioje temoje paaiškinama, kaip galima derinti įvykdyto ER formato duomenų šaltinius, siekiant geriau suprasti sukonfigūruotą duomenų srautą ir transformaciją.
author: NickSelin
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 3a486800f37dda7829aeeaa56a30285a92a61b9d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680787"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a><span data-ttu-id="4bbc4-103">Įvykdyto ER formato duomenų šaltinių derinimas duomenų srautams ir transformacijai analizuoti</span><span class="sxs-lookup"><span data-stu-id="4bbc4-103">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="4bbc4-104">Kai [konfigūruojate](tasks/er-format-configuration-2016-11.md) elektroninių ataskaitų (ER) sprendimą, kuris generuoja siunčiamus dokumentus, nurodote būdus, kuriais duomenys gaunami iš programos ir įvedami į sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-104">When you [configure](tasks/er-format-configuration-2016-11.md) an Electronic reporting (ER) solution to generate outbound documents, you define the methods that are used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="4bbc4-105">Norint, kad ER sprendimo ciklo palaikymas būtų efektyvesnis, jūsų sprendimas turėtų būti sudarytas iš ER [duomenų modelio](general-electronic-reporting.md#DataModelComponent) ir jo [susiejimo](general-electronic-reporting.md#ModelMappingComponent) komponentų, taip pat ER [formato](general-electronic-reporting.md#FormatComponentOutbound) ir jo susiejimo komponentų, kad modelio susiejimas būtų būdingas konkrečiai programai, o kiti komponentai liktų nesusiję su programa.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-105">To make the life cycle support of the ER solution more efficient, your solution should consist of an ER [data model](general-electronic-reporting.md#DataModelComponent) and its [mapping](general-electronic-reporting.md#ModelMappingComponent) components, and also an ER [format](general-electronic-reporting.md#FormatComponentOutbound) and its mapping components, so that the model mapping is application-specific, whereas other components remain application-agnostic.</span></span> <span data-ttu-id="4bbc4-106">Todėl keli ER komponentai gali [paveikti](general-electronic-reporting.md#FormatComponentOutbound) duomenų įvedimo į sugeneruotą išvestį procesą.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-106">Therefore, several ER components might [affect](general-electronic-reporting.md#FormatComponentOutbound) the process of entering data in the generated output.</span></span>

<span data-ttu-id="4bbc4-107">Kartais sugeneruotos išvesties duomenys atrodo kitokie nei tokie patys duomenys programos duomenų bazėje.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-107">Sometimes, the data of the generated output looks different than the same data in the application database.</span></span> <span data-ttu-id="4bbc4-108">Tokiais atvejais reikia nustatyti, kuris ER komponentas yra atsakingas už duomenų transformaciją.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-108">In these cases, you will want to determine which ER component is responsible for the data transformation.</span></span> <span data-ttu-id="4bbc4-109">ER duomenų šaltinio derintuvo funkcija reikšmingai sumažina šio tyrimo laiką ir išlaidas.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-109">The ER data source debugger feature significantly reduces the time and cost that are involved in this investigation.</span></span> <span data-ttu-id="4bbc4-110">Galite nutraukti ER formato vykdymą ir atidaryti duomenų šaltinio derintuvo sąsają.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-110">You can interrupt the execution of an ER format and open the data source debugger interface.</span></span> <span data-ttu-id="4bbc4-111">Joje galite naršyti esamus duomenų šaltinius ir pasirinkti vykdyti atskirą duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-111">There, you can browse the available data sources and select an individual data source for execution.</span></span> <span data-ttu-id="4bbc4-112">Šis neautomatinis vykdymas imituoja duomenų šaltinio vykdymą atliekant realų ER formato vykdymą.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-112">This manual execution simulates the execution of the data source during the real run of an ER format.</span></span> <span data-ttu-id="4bbc4-113">Rezultatas pateikiamas puslapyje, kur galite analizuoti gaunamus duomenis.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-113">The result is presented on a page where you can analyze the data that is received.</span></span>

<span data-ttu-id="4bbc4-114">Norėdami įjungti duomenų šaltinio derinimo funkciją, ER vartotojo parametruose nustatykite parinkties **Įgalinti duomenų derinimą formato vykdymo metu** reikšmę į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-114">To turn on the data source debugging feature, set the **Enable data debugging at format run** option to **Yes** in the ER user parameters.</span></span> <span data-ttu-id="4bbc4-115">Tada kol vykdote ER formatą siunčiamiems dokumentams generuoti, galite pradėti derinti duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-115">You can then start data source debugging while you run an ER format to generate outbound documents.</span></span> <span data-ttu-id="4bbc4-116">Taip pat galite naudoti parinktį **Pradėti derinimą**, kad inicijuotumėte ER formato, sukonfigūruoto [ER operacijų kūrimo įrankyje](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document), duomenų šaltinio derinimą.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-116">You can also use the **Start debugging** option to initiate data source debugging for an ER format that is configured in the [ER Operation designer](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span></span>

<span data-ttu-id="4bbc4-117">Šioje temoje pateikiamos gairės, kaip inicijuoti vykdomų ER formatų duomenų šaltinio derinimą.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-117">This topic provides guidelines for initiating data source debugging for executed ER formats.</span></span> <span data-ttu-id="4bbc4-118">Joje aiškinama, kaip informacija gali padėti suprasti duomenų srautą ir duomenų transformacijas.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-118">It explains how the information can help you understand the data flow and data transformations.</span></span> <span data-ttu-id="4bbc4-119">Šios temos pavyzdžiuose naudojamas tiekėjo mokėjimų apdorojimo verslo procesas.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-119">The examples in this topic use the business process for vendor payments processing.</span></span>

## <a name="limitations"></a><span data-ttu-id="4bbc4-120">Apribojimai</span><span class="sxs-lookup"><span data-stu-id="4bbc4-120">Limitations</span></span>

<span data-ttu-id="4bbc4-121">Duomenų šaltinio derintuvę galima naudoti norint pasiekti duomenis, esančius duomenų šaltiniuose, kurie yra naudojami ER formatuose, vykdomuose generuojant siunčiamus dokumentus.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-121">The data source debugger can be used to access the data of data sources that are used in ER formats that are run to generate outbound documents.</span></span> <span data-ttu-id="4bbc4-122">Jos negalima naudoti, norint derinti gaunamiems dokumentams analizuoti skirtų ER formatų duomenų šaltinius.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-122">It can't be used to debug data sources of ER formats that are designed to parse inbound documents.</span></span>

<span data-ttu-id="4bbc4-123">Šiuo metu toliau nurodyti ER formatų parametrai duomenų šaltiniui derinti nėra pasiekiami.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-123">The following settings of ER formats aren't currently accessible for data source debugging:</span></span>

- <span data-ttu-id="4bbc4-124">Formatų transformacijos</span><span class="sxs-lookup"><span data-stu-id="4bbc4-124">Format transformations</span></span>
- <span data-ttu-id="4bbc4-125">Formato ir susiejimo tikrinimo taisyklės</span><span class="sxs-lookup"><span data-stu-id="4bbc4-125">Format and mapping validation rules</span></span>
- <span data-ttu-id="4bbc4-126">Išraiškų įgalinimas</span><span class="sxs-lookup"><span data-stu-id="4bbc4-126">Enabling expressions</span></span>
- <span data-ttu-id="4bbc4-127">Išsami informacija apie atminties duomenų rinkimą</span><span class="sxs-lookup"><span data-stu-id="4bbc4-127">Details of in-memory data collection</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4bbc4-128">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="4bbc4-128">Prerequisites</span></span>

- <span data-ttu-id="4bbc4-129">Norėdami atlikti šioje temoje pateiktus pavyzdžius, turite turėti prieigą prie vieno iš toliau nurodytų [vaidmenų](../sysadmin/tasks/assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4bbc4-129">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="4bbc4-130">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="4bbc4-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="4bbc4-131">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="4bbc4-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="4bbc4-132">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="4bbc4-132">System administrator</span></span>

- <span data-ttu-id="4bbc4-133">Įmonė turi būti nustatyta kaip **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-133">The company must be set to **DEMF**.</span></span>

- <span data-ttu-id="4bbc4-134">Norėdami atsisiųsti „Microsoft“ ER sprendimo komponentus, kurių reikia tiekėjo mokėjimams apdoroti, atlikite šios temos [1 priede](#appendix1) nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-134">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the Microsoft ER solution that are required to process vendor payments.</span></span>
- <span data-ttu-id="4bbc4-135">Jei norite tiekėjo mokėjimo apdorojimui mokėtinas sumas parengti naudodami atsisiųstą ER sprendimą, atlikite šios temos [2 priede](#appendix2) nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-135">Follow the steps in [Appendix 2](#appendix2) of this topic to prepare Accounts payable for vendor payment processing by using the ER solution that you will download.</span></span>

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a><span data-ttu-id="4bbc4-136">Tiekėjo mokėjimo apdorojimas mokėjimo failui gauti</span><span class="sxs-lookup"><span data-stu-id="4bbc4-136">Process a vendor payment to get a payment file</span></span>

1. <span data-ttu-id="4bbc4-137">Norėdami apdoroti tiekėjo mokėjimus, atlikite šios temos [3 priede](#appendix3) nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-137">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>

    ![Vykdomas tiekėjo mokėjimo apdorojimas](./media/er-data-debugger-process-payment.png)

2. <span data-ttu-id="4bbc4-139">Atsisiųskite ir įrašykite ZIP failą savo vietiniame kompiuteryje.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-139">Download and save the zip file to your local computer.</span></span>
3. <span data-ttu-id="4bbc4-140">Išskleiskite iš ZIP failo mokėjimo failą **ISO20022 Credit transfer.xml**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-140">Extract the **ISO20022 Credit transfer.xml** payment file from the zip file.</span></span>
4. <span data-ttu-id="4bbc4-141">Atidarykite išskleistą mokėjimo failą naudodami XML failų peržiūros programą.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-141">Open the extracted payment file by using the XML file viewer.</span></span>

    <span data-ttu-id="4bbc4-142">Mokėjimo faile nurodytame tiekėjo banko sąskaitos tarptautiniame banko sąskaitos numeryje (IBAN) nėra tarpų.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-142">In the payment file, the International Bank Account Number (IBAN) code of the vendor bank account contains no spaces.</span></span> <span data-ttu-id="4bbc4-143">Todėl ji skiriasi nuo reikšmės [įvestos](#enteredIBANcode) puslapyje **Bankų kodai**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-143">Therefore, it differs from the value that was [entered](#enteredIBANcode) on the **Bank accounts** page.</span></span>

    ![IBAN kodas be tarpų](./media/er-data-debugger-payment-file.png)

    <span data-ttu-id="4bbc4-145">Norėdami sužinoti, kuris ER sprendimo komponentas naudojamas IBAN kodo tarpams pašalinti, galite naudoti ER duomenų šaltinio derintuvę.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-145">You can use the ER data source debugger to learn which component of the ER solution is used to truncate spaces in the IBAN code.</span></span>

## <a name="turn-on-data-source-debugging"></a><span data-ttu-id="4bbc4-146">Duomenų šaltinio derinimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="4bbc4-146">Turn on data source debugging</span></span>

1. <span data-ttu-id="4bbc4-147">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-147">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="4bbc4-148">Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-148">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="4bbc4-149">Parinkties **Įgalinti duomenų derinimą formato vykdymo metu** reikšmę nustatykite į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-149">Set the **Enable data debugging at format run** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4bbc4-150">Šis parametras yra susijęs su konkrečiu vartotoju ir įmone.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-150">This parameter is user-specific and company-specific.</span></span>

    ![Vartotojo parametrų dialogo langas](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a><span data-ttu-id="4bbc4-152">Tiekėjo mokėjimą apdorojimas derinimui</span><span class="sxs-lookup"><span data-stu-id="4bbc4-152">Process a vendor payment for debugging</span></span>

1. <span data-ttu-id="4bbc4-153">Norėdami apdoroti tiekėjo mokėjimus, atlikite šios temos [3 priede](#appendix3) nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-153">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>
2. <span data-ttu-id="4bbc4-154">Pranešimo lange pasirinkite **Taip**, kad patvirtintumėte, jog norite pertraukti tiekėjo mokėjimo apdorojimą ir vietoj to pradėti duomenų šaltinio derinimą puslapyje **Duomenų šaltinių derinimas**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-154">In the message box, select **Yes** to confirm that you want to interrupt vendor payment processing and instead start data source debugging on the **Debug Datasources** page.</span></span>

    ![Patvirtinimo pranešimo langas](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a><span data-ttu-id="4bbc4-156">Duomenų šaltinius, naudojamų mokėjimui apdoroti, derinimas</span><span class="sxs-lookup"><span data-stu-id="4bbc4-156">Debug data sources that are used in payment processing</span></span>

### <a name="debug-the-model-mapping"></a><span data-ttu-id="4bbc4-157">Modelio susiejimo derinimas</span><span class="sxs-lookup"><span data-stu-id="4bbc4-157">Debug the model mapping</span></span>

1. <span data-ttu-id="4bbc4-158">Puslapyje **Duomenų šaltinių derinimas** esančioje veiksmų srityje pasirinkite **Modelio susiejimas**, kad pradėtumėte derinti iš šio ER komponento.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-158">On the **Debug Datasources** page, on the Action Pane, select **Model mapping** to start to debug from this ER component.</span></span>
2. <span data-ttu-id="4bbc4-159">Kairėje esančioje duomenų šaltinio srityje pasirinkite duomenų šaltinį **\$notSentTransactions**, tada pasirinkite **Skaityti visus įrašus**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-159">In the data source pane on the left, select the **\$notSentTransactions** data source, and then select **Read all records**.</span></span>

    <span data-ttu-id="4bbc4-160">Jei norite, kad iš pasirinkto duomenų šaltinio būtų skaitomas atitinkamas skaičius įrašų, galite pasirinkti **Skaityti 1 įrašą**, **Skaityti 10 įrašų**, **Skaityti 100 įrašų** arba **Skaityti visus įrašus**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-160">You can select **Read 1 record**, **Read 10 records**, **Read 100 records**, or **Read all records** to force the appropriate number of records to be read from the selected data source.</span></span> <span data-ttu-id="4bbc4-161">Tokiu būdu galite imituoti prieigą prie duomenų šaltinio iš vykdomo ER formato.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-161">In this way, you can simulate access to the data source from the running ER format.</span></span>

3. <span data-ttu-id="4bbc4-162">Dešinėje esančioje duomenų srityje pasirinkite **Išplėsti viską**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-162">In the data pane on the right, select **Expand all**.</span></span>

    <span data-ttu-id="4bbc4-163">Galite matyti, kad pasirinktame duomenų šaltinyje, kurio tipas – **Įrašų sąrašas**, yra vienas įrašas.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-163">You can see that the selected data source of the **Record list** type contains a single record.</span></span>

4. <span data-ttu-id="4bbc4-164">Išplėskite duomenų šaltinį **\$notSentTransactions** ir pasirinkite įterptąjį metodą **vendBankAccountInTransactionCompany()**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-164">Expand the **\$notSentTransactions** data source, and select the nested **vendBankAccountInTransactionCompany()** method.</span></span>
5. <span data-ttu-id="4bbc4-165">Išplėskite metodą **vendBankAccountInTransactionCompany()** ir pasirinkite įterptąjį lauką **IBAN**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-165">Expand the **vendBankAccountInTransactionCompany()** method, and select the nested **IBAN** field.</span></span>
6. <span data-ttu-id="4bbc4-166">Pasirinkti **Gauti reikšmę**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-166">Select **Get value**.</span></span>

    <span data-ttu-id="4bbc4-167">Jei norite, kad būtų nuskaitoma pasirinkto duomenų šaltinio pasirinktos lauko reikšmė, galite pasirinkti **Gauti reikšmę**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-167">You can select **Get value** to force the value of a selected field of the selected data source to be read.</span></span> <span data-ttu-id="4bbc4-168">Tokiu būdu galite imituoti prieigą prie šio lauko iš vykdomo ER formato.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-168">In this way, you can simulate access to this field from the running ER format.</span></span>

7. <span data-ttu-id="4bbc4-169">Pažymėkite **Išplėsti viską**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-169">Select **Expand all**.</span></span>

    ![IBAN lauko reikšmė modelio susiejime](./media/er-data-debugger-debugging-model-mapping.png)

    <span data-ttu-id="4bbc4-171">Kaip matote, modelio susiejimas neatsako už pašalintus tarpus, nes tarpai yra IBAN kode, kurį jis grąžina tiekėjo banko sąskaitai.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-171">As you can see, the model mapping isn't responsible for the truncated spaces, because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="4bbc4-172">Todėl turite tęsti duomenų šaltinio derinimą.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-172">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format-mapping"></a><span data-ttu-id="4bbc4-173">Formato susiejimo derinimas</span><span class="sxs-lookup"><span data-stu-id="4bbc4-173">Debug the format mapping</span></span>

1. <span data-ttu-id="4bbc4-174">Puslapyje **Duomenų šaltinių derinimas** esančioje veiksmų srityje pasirinkite **Formato susiejimas**, kad galėtumėte tęsti derinimą iš šio ER komponento.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-174">On the **Debug Datasources** page, on the Action Pane, select **Format mapping** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="4bbc4-175">Pasirinkite duomenų šaltinį **\$PaymentByDebtor**, tada – **Skaityti visus įrašus**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-175">Select the **\$PaymentByDebtor** data source, and then select **Read all records**.</span></span>
3. <span data-ttu-id="4bbc4-176">Išplėskite **\$PaymentByDebtor**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-176">Expand **\$PaymentByDebtor**.</span></span>
4. <span data-ttu-id="4bbc4-177">Išplėskite **\$PaymentByDebtor.Lines**, tada pasirinkite **Skaityti visus įrašus**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-177">Expand **\$PaymentByDebtor.Lines**, and then select **Read all records**.</span></span>
5. <span data-ttu-id="4bbc4-178">Išplėskite **\$PaymentByDebtor.Lines.CreditorAccount**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-178">Expand **\$PaymentByDebtor.Lines.CreditorAccount**.</span></span>
6. <span data-ttu-id="4bbc4-179">Išplėskite **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, tada pasirinkite **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-179">Expand **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, and then select **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span></span>
7. <span data-ttu-id="4bbc4-180">Pasirinkti **Gauti reikšmę**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-180">Select **Get value**.</span></span>
8. <span data-ttu-id="4bbc4-181">Pažymėkite **Išplėsti viską**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-181">Select **Expand all**.</span></span>

    ![IBAN lauko reikšmė formato susiejime](./media/er-data-debugger-debugging-format-mapping.png)

    <span data-ttu-id="4bbc4-183">Kaip matote, formato susiejimo duomenų šaltiniai neatsako už pašalintus tarpus, nes tarpai yra IBAN kode, kurį jie grąžina tiekėjo banko sąskaitai.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-183">As you can see, the data sources of the format mapping aren't responsible for the truncated spaces, because the IBAN code that they return for the vendor bank account includes spaces.</span></span> <span data-ttu-id="4bbc4-184">Todėl turite tęsti duomenų šaltinio derinimą.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-184">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format"></a><span data-ttu-id="4bbc4-185">Formato derinimas</span><span class="sxs-lookup"><span data-stu-id="4bbc4-185">Debug the format</span></span>

1. <span data-ttu-id="4bbc4-186">Puslapyje **Duomenų šaltinių derinimas** esančioje veiksmų srityje pasirinkite **Formatas**, kad galėtumėte tęsti derinimą iš šio ER komponento.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-186">On the **Debug Datasources** page, on the Action Pane, select **Format** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="4bbc4-187">Išplėskite formato elementus, kad pasirinktumėte **ISO20022CTReports** \> **XMLHeader** \> **Dokumentas** \> **CstmrCdtTrfInitn** \> **PmtInf**, tada pasirinkite **Skaityti visus įrašus**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-187">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf**, and then select **Read all records**.</span></span>
3. <span data-ttu-id="4bbc4-188">Išplėskite formato elementus, kad pasirinktumėte **ISO20022CTReports** \> **XMLHeader** \> **Dokumentas** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, tada pasirinkite **Skaityti visus įrašus**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-188">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, and then select **Read all records**.</span></span>
4. <span data-ttu-id="4bbc4-189">Išplėskite formato elementus, kad pasirinktumėte **ISO20022CTReports** \> **XMLHeader** \> **Dokumentas** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, tada pasirinkite **Gauti reikšmę**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-189">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, and then select **Get value**.</span></span>
5. <span data-ttu-id="4bbc4-190">Pažymėkite **Išplėsti viską**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-190">Select **Expand all**.</span></span>

    ![IBAN lauko reikšmė formate](./media/er-data-debugger-debugging-format.png)

   <span data-ttu-id="4bbc4-192">Kaip matote, formato susiejimas neatsako už pašalintus tarpus, nes tarpai yra IBAN kode, kurį jis grąžina tiekėjo banko sąskaitai.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-192">As you can see, the format binding isn't responsible for the truncated spaces because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="4bbc4-193">Todėl **BankIBAN** elementas sukonfigūruotas naudoti formato transformaciją, kuri pašalina tarpus.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-193">Therefore, the **BankIBAN** element is configured to use a format transformation that truncates spaces.</span></span>

6. <span data-ttu-id="4bbc4-194">Uždarykite duomenų šaltinio derintuvę.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-194">Close the data source debugger.</span></span>

### <a name="review-the-format-transformations"></a><span data-ttu-id="4bbc4-195">Formato transformacijų peržiūra</span><span class="sxs-lookup"><span data-stu-id="4bbc4-195">Review the format transformations</span></span>

1. <span data-ttu-id="4bbc4-196">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="4bbc4-197">Puslapyje **Konfigūracijos** pasirinkite **Mokėjimo modelis** \> **ISO20022 kredito pervedimas**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-197">On the **Configurations** page, select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="4bbc4-198">Pasirinkite **Kūrimo įrankis**, tada išplėskite formato elementus, kad pasirinktumėte **Dokumentas** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-198">Select **Designer**, and then expand the elements to select **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span></span>

    ![BankIBAN elementas puslapyje Formato kūrimo įrankis](./media/er-data-debugger-referred-transformation.png)

    <span data-ttu-id="4bbc4-200">Kaip matote, **BankIBAN** elementas sukonfigūruotas naudoti transformaciją **pašalinti ne raidinius-skaitinius simbolius**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-200">As you can see, the **BankIBAN** element is configured to use the **remove not alphanumeric** transformation.</span></span>

4. <span data-ttu-id="4bbc4-201">Pasirinkite skirtuką **Transformacijos**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-201">Select the **Transformations** tab.</span></span>

    ![BankIBAN elemento skirtukas Transformacijos](./media/er-data-debugger-transformation.png)

    <span data-ttu-id="4bbc4-203">Kaip matote, transformacija **pašalinti ne raidinius-skaitinius simbolius** sukonfigūruota naudoti išraišką, kuri pašalina tarpus pateiktoje teksto eilutėje.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-203">As you can see, the **remove not alphanumeric** transformation is configured to use an expression that truncates spaces from the text string that is provided.</span></span>

## <a name="start-to-debug-in-the-operation-designer"></a><span data-ttu-id="4bbc4-204">Derinimo operacijų kūrimo įrankyje pradžia</span><span class="sxs-lookup"><span data-stu-id="4bbc4-204">Start to debug in the Operation designer</span></span>

<span data-ttu-id="4bbc4-205">Kai sukonfigūruojate ER formato juodraštinę versiją, kurią galima tiesiogiai paleisti iš operacijų kūrimo įrankio, duomenų šaltinio derintuvę galite pasiekti veiksmų srityje pasirinkdami **Pradėti derinimą**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-205">When you configure a draft version of the ER format that can be run directly from the Operation designer, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Mygtukas Pradėti derinimą puslapyje Formato kūrimo įrankis](./media/er-data-debugger-run-from-designer.png)

<span data-ttu-id="4bbc4-207">Redaguojamo ER formato susiejimą ir komponentus galima derinti.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-207">The format mapping and format components of the ER format that is being edited are available for debugging.</span></span>

## <a name="start-to-debug-in-the-model-mapping-designer"></a><span data-ttu-id="4bbc4-208">Derinimo modelio susiejimų kūrimo įrankyje pradžia</span><span class="sxs-lookup"><span data-stu-id="4bbc4-208">Start to debug in the Model mapping designer</span></span>

<span data-ttu-id="4bbc4-209">Kai sukonfigūruojate ER modelio susiejimą, kurį galima paleisti iš puslapio **Modelio susiejimas**, duomenų šaltinio derintuvę galite pasiekti veiksmų srityje pasirinkdami **Pradėti derinimą**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-209">When you configure an ER model mapping that can be run from the **Model mapping** page, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Mygtukas Pradėti derinimą puslapyje Modelio susiejimų kūrimo įrankis](./media/er-data-debugger-run-from-designer-mapping.png)

<span data-ttu-id="4bbc4-211">Redaguojamo ER susiejimo modelio susiejimo komponentą galima derinti.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-211">The model mapping component of the ER mapping that is being edited is available for debugging.</span></span>

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a><span data-ttu-id="4bbc4-212">1 priedas. ER sprendimo gavimas</span><span class="sxs-lookup"><span data-stu-id="4bbc4-212">Appendix 1: Get an ER solution</span></span>

### <a name="download-an-er-solution"></a><span data-ttu-id="4bbc4-213">ER sprendimo atsisiuntimas</span><span class="sxs-lookup"><span data-stu-id="4bbc4-213">Download an ER solution</span></span>

<span data-ttu-id="4bbc4-214">Jei apdorojamo tiekėjo elektroninio mokėjimo failui generuoti norite naudoti ER sprendimą, galite [atsisiųsti](download-electronic-reporting-configuration-lcs.md) ER mokėjimo formatą **ISO20022 kredito pervedimas**, kurį galima gauti iš bendrai naudojamo turto bibliotekos, esančios „Microsoft Dynamics Lifecycle Services (LCS)“, arba iš bendrosios saugyklos.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-214">If you want to use an ER solution to generate an electronic payment file for a vendor payment that is processed, you can [download](download-electronic-reporting-configuration-lcs.md) the **ISO20022 Credit transfer** ER payment format that is available from the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) or from the Global repository.</span></span>

![ER mokėjimo formato atsisiuntimas puslapyje Konfigūracijos saugykla](./media/er-data-debugger-import-from-repo.png)

<span data-ttu-id="4bbc4-216">Kartu su pasirinktu ER formatu, kaip ER sprendimo **ISO20022 kredito pervedimas** dalis, į „Microsoft Dynamics 365 Finance“ egzempliorių turi būti automatiškai importuotos toliau nurodytos [konfigūracijos](general-electronic-reporting.md#Configuration).</span><span class="sxs-lookup"><span data-stu-id="4bbc4-216">In addition to the selected ER format, the following [configurations](general-electronic-reporting.md#Configuration) must be automatically imported into your Microsoft Dynamics 365 Finance instance as part of the **ISO20022 Credit transfer** ER solution:</span></span>

- <span data-ttu-id="4bbc4-217">[ER duomenų modelio konfigūracija](general-electronic-reporting.md#DataModelComponent) **Mokėjimo modelis**</span><span class="sxs-lookup"><span data-stu-id="4bbc4-217">**Payment model** [ER data model configuration](general-electronic-reporting.md#DataModelComponent)</span></span>
- <span data-ttu-id="4bbc4-218">[ER formato konfigūracija](general-electronic-reporting.md#FormatComponentOutbound) **ISO20022 kredito pervedimas**</span><span class="sxs-lookup"><span data-stu-id="4bbc4-218">**ISO20022 Credit transfer** [ER format configuration](general-electronic-reporting.md#FormatComponentOutbound)</span></span>
- <span data-ttu-id="4bbc4-219">[ER modelio susiejimo konfigūracija](general-electronic-reporting.md#ModelMappingComponent) **Mokėjimo modelio susiejimas 1611**</span><span class="sxs-lookup"><span data-stu-id="4bbc4-219">**Payment model mapping 1611** [ER model mapping configuration](general-electronic-reporting.md#ModelMappingComponent)</span></span>
- <span data-ttu-id="4bbc4-220">ER modelio susiejimo konfigūracija **Mokėjimo modelio susiejimas su paskirtimi ISO20022**</span><span class="sxs-lookup"><span data-stu-id="4bbc4-220">**Payment model mapping to destination ISO20022** ER model mapping configuration</span></span>

<span data-ttu-id="4bbc4-221">Šias konfigūracijas galite rasti ER sistemos puslapyje **Konfigūracijos** (**Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**).</span><span class="sxs-lookup"><span data-stu-id="4bbc4-221">You can find these configurations on the **Configurations** page of the ER framework (**Organization administration** \> **Electronic reporting** \> **Configurations**).</span></span>

![Puslapyje Konfigūracijos importuotos konfigūracijos](./media/er-data-debugger-configurations.png)

<span data-ttu-id="4bbc4-223">Jeigu konfigūracijos medyje nėra anksčiau išvardytų konfigūracijų, turite jas atsisiųsti rankiniu būdu iš LCS bendrai naudojamo turto bibliotekos taip pat, kaip atsisiuntėte ER mokėjimo formatą **ISO20022 kredito pervedimas**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-223">If any of the previously listed configurations are missing in the configuration tree, you must manually download them from the LCS Shared asset library in the same way that you downloaded the **ISO20022 Credit transfer** ER payment format.</span></span>

### <a name="analyze-the-downloaded-er-solution"></a><span data-ttu-id="4bbc4-224">Atsisiųsto ER sprendimo analizė</span><span class="sxs-lookup"><span data-stu-id="4bbc4-224">Analyze the downloaded ER solution</span></span>

#### <a name="review-the-model-mapping"></a><span data-ttu-id="4bbc4-225">Modelio susiejimo peržiūra</span><span class="sxs-lookup"><span data-stu-id="4bbc4-225">Review the model mapping</span></span>

1. <span data-ttu-id="4bbc4-226">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-226">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="4bbc4-227">Pasirinkite **Mokėjimo modelis** \> **Mokėjimo modelio susiejimas 1611**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-227">Select **Payment model** \> **Payment model mapping 1611**.</span></span>
3. <span data-ttu-id="4bbc4-228">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-228">Select **Designer**.</span></span>
4. <span data-ttu-id="4bbc4-229">Pasirinkite susiejimo įrašą **Mokėjimo modelio susiejimas ISO20022 CT**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-229">Select the **Payment model mapping ISO20022 CT** mapping record.</span></span>
5. <span data-ttu-id="4bbc4-230">Pasirinkite **Kūrimo įrankis**, tada peržiūrėkite atidarytą modelio susiejimą.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-230">Select **Designer**, and then review the model mapping that is opened.</span></span>

    <span data-ttu-id="4bbc4-231">Atkreipkite dėmesį, kad duomenų modelio laukas **Mokėjimai** yra susietas su duomenų šaltiniu **\$notSentTransactions**, kuris grąžina apdorojamų tiekėjo mokėjimo eilučių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-231">Notice that the **Payments** field of the data model is bound to the **\$notSentTransactions** data source that returns the list of vendor payment lines that are being processed.</span></span>

    ![Laukas Mokėjimai puslapyje Modelių susiejimo kūrimo įrankis](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a><span data-ttu-id="4bbc4-233">Formato susiejimo peržiūra</span><span class="sxs-lookup"><span data-stu-id="4bbc4-233">Review the format mapping</span></span>

1. <span data-ttu-id="4bbc4-234">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-234">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="4bbc4-235">Pasirinkite **Mokėjimo modelis** \> **ISO20022 kredito pervedimas**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-235">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="4bbc4-236">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-236">Select **Designer**.</span></span>
4. <span data-ttu-id="4bbc4-237">Skirtuke **Susiejimas** peržiūrėkite atidarytą formato susiejimą.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-237">On the **Mapping** tab, review the format mapping that is opened.</span></span>

    <span data-ttu-id="4bbc4-238">Atkreipkite dėmesį, kad failo **ISO20022CTReports** \> **XMLHeader** elementas **Dokumentas** \> **CstmrCdtTrfInitn** \> **PmtInf** yra susietas su duomenų šaltiniu **\$PaymentByDebtor**, kuris yra sukonfigūruotas grupuoti duomenų modelio lauko **Mokėjimai** įrašus.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-238">Notice that the **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** element of the **ISO20022CTReports** \> **XMLHeader** file is bound to the **\$PaymentByDebtor** data source that is configured to group records of the data model's **Payments** field.</span></span>

    ![PmtInf elementas puslapyje Formato kūrimo įrankis](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a><span data-ttu-id="4bbc4-240">Formato peržiūra</span><span class="sxs-lookup"><span data-stu-id="4bbc4-240">Review the format</span></span>

1. <span data-ttu-id="4bbc4-241">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-241">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="4bbc4-242">Pasirinkite **Mokėjimo modelis** \> **ISO20022 kredito pervedimas**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-242">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="4bbc4-243">Pasirinkite **Kūrimo įrankis**, tada peržiūrėkite atidarytą formatą.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-243">Select **Designer**, and then review the format that is opened.</span></span>

    <span data-ttu-id="4bbc4-244">Atkreipkite dėmesį, kad formato elementas, esantis **Dokumentas** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, yra sukonfigūruotas tiekėjo sąskaitos IBAN kodui įvesti mokėjimo faile.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-244">Notice that the format element under **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** is configured to enter the IBAN code of the vendor account in the payment file.</span></span>

    ![BankIBAN elementas puslapyje Formato kūrimo įrankis](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a><span data-ttu-id="4bbc4-246">2 priedas. Mokėtinų sumų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="4bbc4-246">Appendix 2: Configure Accounts payable</span></span>

### <a name="modify-a-vendor-property"></a><span data-ttu-id="4bbc4-247">Tiekėjo ypatybės modifikavimas</span><span class="sxs-lookup"><span data-stu-id="4bbc4-247">Modify a vendor property</span></span>

1. <span data-ttu-id="4bbc4-248">Eikite į **Mokėtinos sumos** \> **Tiekėjai** \> **Visi tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-248">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="4bbc4-249">Pasirinkite tiekėją **DE-01002**, tada veiksmų srities skirtuko **Tiekėjas** grupėje **Nustatymas** pasirinkite **Bankų sąskaitos**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-249">Select vendor **DE-01002**, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="4bbc4-250">„FastTab“ konteineryje **Identifikacija**, lauke **IBAN**, <a name="enteredIBANcode"></a>įveskite **GB33 BUKB 2020 1555 5555 55**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-250">On the **Identification** FastTab, in the **IBAN** field, <a name="enteredIBANcode"></a>enter **GB33 BUKB 2020 1555 5555 55**.</span></span>
4. <span data-ttu-id="4bbc4-251">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-251">Select **Save**.</span></span>

![Puslapyje Tiekėjo banko sąskaitos nustatytas IBAN laukas](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a><span data-ttu-id="4bbc4-253">Mokėjimo būdo nustatymas</span><span class="sxs-lookup"><span data-stu-id="4bbc4-253">Set up a method of payment</span></span>

1. <span data-ttu-id="4bbc4-254">Eikite į **Mokėtinos sumos** \> **Mokėjimo nustatymas** \> **Mokėjimo būdai**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-254">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="4bbc4-255">Pasirinkite mokėjimo būdą **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-255">Select the **SEPA CT** payment method.</span></span>
3. <span data-ttu-id="4bbc4-256">„FastTab“ konteineryje **Failų formatai**, dalyje **Failų formatai** parinkties **Bendras elektroninis eksportavimo formatas** reikšmę nustatykite kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-256">On the **File formats** FastTab, in the **File formats** section, set the **Generic electronic Export format** option to **Yes**.</span></span>
4. <span data-ttu-id="4bbc4-257">Lauke **Eksportuoti formato konfigūraciją** pasirinkite ER formatą **ISO20022 kredito pervedimas**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-257">In the **Export format configuration** field, select the **ISO20022 Credit transfer** ER format.</span></span>
5. <span data-ttu-id="4bbc4-258">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-258">Select **Save**.</span></span>

![Failo formato parametrai puslapyje Mokėjimo būdai](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a><span data-ttu-id="4bbc4-260">Tiekėjo mokėjimo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="4bbc4-260">Add a vendor payment</span></span>

1. <span data-ttu-id="4bbc4-261">Eikite į **Mokėtinos sumos** \> **Mokėjimai** \> **Tiekėjo mokėjimų žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-261">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="4bbc4-262">Įtraukite naują mokėjimų žurnalą.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-262">Add a new payment journal.</span></span>
3. <span data-ttu-id="4bbc4-263">Pasirinkite **Eilutės** ir įtraukite naują mokėjimo eilutę.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-263">Select **Lines**, and add a new payment line.</span></span>
4. <span data-ttu-id="4bbc4-264">Lauke **Sąskaita** įveskite tiekėją **DE-01002**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-264">In the **Account** field, select vendor **DE-01002**.</span></span>
5. <span data-ttu-id="4bbc4-265">Lauke **Debetas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-265">In the **Debit** field, enter a value.</span></span>
6. <span data-ttu-id="4bbc4-266">Lauke **Mokėjimo būdas** pasirinkite **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-266">In the **Method of payment** field, select **SEPA CT**.</span></span>
7. <span data-ttu-id="4bbc4-267">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-267">Select **Save**.</span></span>

![Tiekėjo mokėjimai įtraukti puslapyje Tiekėjo mokėjimai](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a><span data-ttu-id="4bbc4-269">3 priedas. Tiekėjo mokėjimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="4bbc4-269">Appendix 3: Process a vendor payment</span></span>

1. <span data-ttu-id="4bbc4-270">Eikite į **Mokėtinos sumos** \> **Mokėjimai** \> **Tiekėjo mokėjimų žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-270">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="4bbc4-271">Puslapyje **Tiekėjo mokėjimų žurnalas** pasirinkite anksčiau sukurtą mokėjimų žurnalą, tada pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-271">On the **Vendor payment journal** page, select the payment journal that you previously created, and then select **Lines**.</span></span>
3. <span data-ttu-id="4bbc4-272">Pasirinkite mokėjimo eilutę ir pasirinkite **Mokėjimo būsena** \> **Nėra**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-272">Select the payment line, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="4bbc4-273">Pasirinkite **Generuoti mokėjimus**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-273">Select **Generate payments**.</span></span>
5. <span data-ttu-id="4bbc4-274">Lauke **Mokėjimo būdas** pasirinkite **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-274">In the **Method of payment** field, select **SEPA CT**.</span></span>
6. <span data-ttu-id="4bbc4-275">Lauke **Banko sąskaita** įveskite **DEMF OPER**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-275">In the **Bank account** field, select **DEMF OPER**.</span></span>
7. <span data-ttu-id="4bbc4-276">Dialogo lange **Generuoti mokėjimus** pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-276">In the **Generate payments** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="4bbc4-277">Dialogo lange **Elektroninių ataskaitų parametrai** pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4bbc4-277">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
