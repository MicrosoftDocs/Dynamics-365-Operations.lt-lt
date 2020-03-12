---
title: „Regression Suite Automation Tool“ mokymo programos naudojimas
description: Šioje temoje parodoma, kaip naudoti „Regression Suite Automation Tool“ (RSAT). Joje aprašomos įvairios funkcijos ir pateikiami pavyzdžiai, kuriuose naudojami išplėstiniai scenarijai.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 6cdaa89fb6d50ebaaaefe7f92d7224a1567d17d1
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070825"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="753d1-104">„Regression Suite Automation Tool“ mokymo programos naudojimas</span><span class="sxs-lookup"><span data-stu-id="753d1-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="753d1-105">Naudodamiesi interneto naršyklės įrankiais atsisiųskite ir įrašykite šį puslapį PDF formatu.</span><span class="sxs-lookup"><span data-stu-id="753d1-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="753d1-106">Šioje mokymo priemonėje paaiškinamos kai kurios išplėstinės „Regression Suite Automation Tool“ (RSAT) funkcijos, pateikiamas demonstracinis priskyrimas ir aprašoma strategija bei pagrindiniai mokymosi aspektai.</span><span class="sxs-lookup"><span data-stu-id="753d1-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="753d1-107">RSAT / užduočių įrašymo priemonės funkcijos</span><span class="sxs-lookup"><span data-stu-id="753d1-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="753d1-108">Patikrinti lauko reikšmę</span><span class="sxs-lookup"><span data-stu-id="753d1-108">Validate a field value</span></span>

<span data-ttu-id="753d1-109">Norėdami gauti informacijos apie šią funkciją, žr. [Naujo užduoties įrašo, turinčio tikrinimo funkciją, kūrimas](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span><span class="sxs-lookup"><span data-stu-id="753d1-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="753d1-110">Įrašytas kintamasis</span><span class="sxs-lookup"><span data-stu-id="753d1-110">Saved variable</span></span>

<span data-ttu-id="753d1-111">Norėdami gauti informacijos apie šią funkciją, žr. [Esamo užduoties įrašo modifikavimas norint sukurti įrašytą kintamąjį](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span><span class="sxs-lookup"><span data-stu-id="753d1-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="753d1-112">Išvesto testo atvejis</span><span class="sxs-lookup"><span data-stu-id="753d1-112">Derived test case</span></span>

1. <span data-ttu-id="753d1-113">Atidarykite „Regression suite automation tool“ (RSAT) ir pasirinkite abu tikrinimo atvejus, kuriuos sukūrėte [„Regression suite automation tool“ mokymo priemonės nustatymas ir diegimas](./hol-set-up-regression-suite-automation-tool.md).</span><span class="sxs-lookup"><span data-stu-id="753d1-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool tutorial](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="753d1-114">Pasirinkite **Naujas \> Kurti išvestinį tikrinimo atvejį**.</span><span class="sxs-lookup"><span data-stu-id="753d1-114">Select **New \> Create derived test case**.</span></span>

    ![Komanda Kurti išvestinį tikrinimo atvejį meniu Naujas](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="753d1-116">Gaunate pranešimą, kuriame teigiama, kad kiekvienam pasirinktam tikrinimui skirtas tikrinimo atvejis bus sukurtas pagal dabartinį tikrinimo komplektą ir kad kiekvienas išvestinis tikrinimo atvejis turės savo „Excel“ parametro failo kopiją.</span><span class="sxs-lookup"><span data-stu-id="753d1-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="753d1-117">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="753d1-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="753d1-118">Paleidus išvestinį tikrinimo atvejį, jis naudoja jo pirminio tikrinimo atvejo ir savo „Excel“ parametro failo kopijos užduoties įrašą.</span><span class="sxs-lookup"><span data-stu-id="753d1-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="753d1-119">Tokiu būdu galite atlikti tą patį tikrinimą su skirtingais parametrais, neprivalėdami tvarkyti daugiau nei vieną užduoties įrašą.</span><span class="sxs-lookup"><span data-stu-id="753d1-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="753d1-120">Išvestinis tikrinimo atvejis nebūtinai turi priklausyti tam pačiam tikrinimų paketui kaip jo pirminis tikrinimo atvejis.</span><span class="sxs-lookup"><span data-stu-id="753d1-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![Pranešimo laukas](./media/use_rsa_tool_02.png)

    <span data-ttu-id="753d1-122">Sukuriami du papildomi išvestiniai tikrinimo atvejai ir pažymimas jų žymės langelis **Išvestinis?**.</span><span class="sxs-lookup"><span data-stu-id="753d1-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![Sukuriami išvestiniai tikrinimo atvejai](./media/use_rsa_tool_03.png)

    <span data-ttu-id="753d1-124">Išvestinis tikrinimo atvejis sukuriamas automatiškai „Azure DevOps“.</span><span class="sxs-lookup"><span data-stu-id="753d1-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="753d1-125">Tai antrinis tikrinimo atvejo **Kurti naują produktą** elementas ir jis pažymėtas specialiu raktažodžiu: **RSAT:DerivedTestSteps**.</span><span class="sxs-lookup"><span data-stu-id="753d1-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="753d1-126">Šie tikrinimo atvejai taip pat automatiškai įtraukiami į tikrinimo planą „Azure DevOps“.</span><span class="sxs-lookup"><span data-stu-id="753d1-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![Raktažodis RSAT:DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="753d1-128">Jei dėl kokių nors priežasčių išvestiniai tikrinimo atvejai nėra pateikiami tinkama tvarka, atidarykite „Azure DevOps“ ir pertvarkykite tikrinimo atvejus tikrinimo komplekte, kad RSAT galėtų paleisti juos tinkama tvarka.</span><span class="sxs-lookup"><span data-stu-id="753d1-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="753d1-129">Pasirinkite išvestinius tikrinimo atvejus ir pasirinkite **Redaguoti**, kad atidarytumėte atitinkamus „Excel“ parametrų failus.</span><span class="sxs-lookup"><span data-stu-id="753d1-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="753d1-130">Redaguokite šiuos „Excel“ parametrų failus tokiu pat būdu, kaip redagavote pirminį failą.</span><span class="sxs-lookup"><span data-stu-id="753d1-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="753d1-131">Kitaip tariant, įsitikinkite, kad produkto ID nustatytas taip, jog jis būtų automatiškai sugeneruotas.</span><span class="sxs-lookup"><span data-stu-id="753d1-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="753d1-132">Taip pat įsitikinkite, kad įrašytas kintamasis nukopijuojamas į atitinkamus laukus.</span><span class="sxs-lookup"><span data-stu-id="753d1-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="753d1-133">Abiejų „Excel“ parametrų failų skirtukuose **Bendra** atnaujinkite lauko **Įmonė** reikšmę į **USSI**, kad išvestiniai tikrinimo atvejai būtų vykdomi kitame juridiniame subjekte nei pirminis tikrinimo atvejis.</span><span class="sxs-lookup"><span data-stu-id="753d1-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="753d1-134">Norėdami vykdyti tikrinimo atvejus pagal konkretų vartotoją (arba vaidmenį, kuris susietas su konkrečiu vartotoju), galite atnaujinti lauko **Tikrinimo vartotojas** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="753d1-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="753d1-135">Pasirinkite **Vykdyti** ir įsitikinkite, kad produktas sukurtas ir juridiniame subjekte USMF ir juridiniame subjekte USSI.</span><span class="sxs-lookup"><span data-stu-id="753d1-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="753d1-136">Tikrinti pranešimus</span><span class="sxs-lookup"><span data-stu-id="753d1-136">Validate notifications</span></span>

<span data-ttu-id="753d1-137">Šią funkciją galima naudoti norint patikrinti, ar įvyko veiksmas.</span><span class="sxs-lookup"><span data-stu-id="753d1-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="753d1-138">Pavyzdžiui, kai sukuriamas, įvertinamas ir pradedamas gamybos užsakymas, programa rodo pranešimą „Gamyba – pradžia“, kad praneštų, jog pradėtas gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="753d1-138">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Pranešimas Gamyba – pradžia](./media/use_rsa_tool_05.png)

<span data-ttu-id="753d1-140">Šį pranešimą galite patikrinti naudodami RSAT – įveskite pranešimo tekstą atitinkamo įrašo „Excel“ parametro failo skirtuke **MessageValidation**.</span><span class="sxs-lookup"><span data-stu-id="753d1-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Skirtukas Pranešimo tikrinimas](./media/use_rsa_tool_06.png)

<span data-ttu-id="753d1-142">Paleidus tikrinimo atvejį, pranešimas „Excel“ parametro faile palyginamas su rodomu pranešimu.</span><span class="sxs-lookup"><span data-stu-id="753d1-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="753d1-143">Jei pranešimai nesutampa, tikrinimo atvejis nepavyks.</span><span class="sxs-lookup"><span data-stu-id="753d1-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="753d1-144">„Excel“ parametro failo skirtuke **MessageValidation** galite įvesti daugiau nei vieną pranešimą.</span><span class="sxs-lookup"><span data-stu-id="753d1-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="753d1-145">Pranešimai taip pat gali būti klaidos arba įspėjantys, o ne informaciniai pranešimai.</span><span class="sxs-lookup"><span data-stu-id="753d1-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="753d1-146">Tikrinti reikšmes naudojant operatorius</span><span class="sxs-lookup"><span data-stu-id="753d1-146">Validate values by using operators</span></span>

<span data-ttu-id="753d1-147">Ankstesnėse RSAT versijose galėjote tikrinti vertes tik jei kontrolinė reikšmė sutapo su numatoma reikšme.</span><span class="sxs-lookup"><span data-stu-id="753d1-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="753d1-148">Nauja funkcija suteikia galimybę patikrinti, ar kintamasis nėra lygus, yra mažesnis arba yra didesnis už nurodytą reikšmę.</span><span class="sxs-lookup"><span data-stu-id="753d1-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="753d1-149">Norėdami naudoti šią funkciją atidarykite failą **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT diegimo aplanke (pvz., **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ir pakeiskite toliau nurodyto elemento reikšmę iš **false** į **true**.</span><span class="sxs-lookup"><span data-stu-id="753d1-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="753d1-150">„Excel“ parametro faile atsiranda naujas laukas **Operatorius**.</span><span class="sxs-lookup"><span data-stu-id="753d1-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="753d1-151">Jei naudojate senesnę RSAT versiją, turite sugeneruoti naujus „Excel“ parametrų failus.</span><span class="sxs-lookup"><span data-stu-id="753d1-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![Laukas Operatorius](./media/use_rsa_tool_07.png)

<span data-ttu-id="753d1-153">Toliau pateiktame pavyzdyje parodyta, kaip galima naudoti šią funkciją norint patikrinti, ar turimos atsargos yra daugiau nei 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="753d1-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="753d1-154">Įmonės **USMF** demonstraciniuose duomenyse sukurkite užduoties įrašą, sudarytą iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="753d1-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="753d1-155">Eikite į **Produkto informacijos valdymas \> Produktai \> Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="753d1-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="753d1-156">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="753d1-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="753d1-157">Pvz., filtruokite lauko **Prekės numeris** reikšme **1000**.</span><span class="sxs-lookup"><span data-stu-id="753d1-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="753d1-158">Pasirinkite **Turimos atsargos**.</span><span class="sxs-lookup"><span data-stu-id="753d1-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="753d1-159">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="753d1-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="753d1-160">Pvz., filtruokite lauko **Vieta** reikšme **1**.</span><span class="sxs-lookup"><span data-stu-id="753d1-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="753d1-161">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="753d1-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="753d1-162">Patikrinkite, ar lauko **Iš viso turima** yra reikšmė yra **411,0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="753d1-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="753d1-163">Įrašykite užduoties įrašą į BPM biblioteką, esančią LCS, ir sinchronizuokite jį į „Azure DevOps“.</span><span class="sxs-lookup"><span data-stu-id="753d1-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="753d1-164">Įtraukite tikrinimo atvejį į tikrinimo planą ir įkelkite tikrinimo atvejį į RSAT.</span><span class="sxs-lookup"><span data-stu-id="753d1-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="753d1-165">Atidarykite „Excel“ parametrų failą.</span><span class="sxs-lookup"><span data-stu-id="753d1-165">Open the Excel parameter file.</span></span> <span data-ttu-id="753d1-166">Skirtuke **InventOnhandItem** matysite skiltį **Tikrinti InventOnhandItem**, kurioje pateiktas laukas **Operatorius**.</span><span class="sxs-lookup"><span data-stu-id="753d1-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Laukas Operatorius](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="753d1-168">Norėdami patikrinti, ar turimos atsargos visada bus didesnės nei 0, pakeiskite lauko **Vertė** reikšmę iš **411** į **0**, o lauko **Operatorius** reikšmę – iš lygybės ženklo (**=**) į ženklą „daugiau nei“ (**\>**).</span><span class="sxs-lookup"><span data-stu-id="753d1-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Pakeistos laukų Vertė ir Operatorius reikšmės](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="753d1-170">Įrašykite ir uždarykite „Excel“ parametro failą.</span><span class="sxs-lookup"><span data-stu-id="753d1-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="753d1-171">Pasirinkite **Įkelti**, kad įrašytumėte keitimus, atliktus „Excel“ parametro faile, į „Azure DevOps“.</span><span class="sxs-lookup"><span data-stu-id="753d1-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="753d1-172">Dabar, jei nurodytos atsargų prekės reikšmė lauke **Iš viso turima** yra didesnė nei 0 (nulis), tikrinimai pavyks, nepriklausomai nuo faktinės turimų atsargų vertės.</span><span class="sxs-lookup"><span data-stu-id="753d1-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="753d1-173">Generatoriaus žurnalai</span><span class="sxs-lookup"><span data-stu-id="753d1-173">Generator logs</span></span>

<span data-ttu-id="753d1-174">Ši funkcija sukuria aplanką, kuriame yra paleistų tikrinimo atvejų žurnalai.</span><span class="sxs-lookup"><span data-stu-id="753d1-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="753d1-175">Norėdami naudoti šią funkciją atidarykite failą **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT diegimo aplanke (pvz., **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ir pakeiskite toliau nurodyto elemento reikšmę iš **false** į **true**.</span><span class="sxs-lookup"><span data-stu-id="753d1-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="753d1-176">Paleidus tikrinimo atvejus, žurnalų failus galima rasti čia: **C:\\Vartotojai\\\<Vartotojo vardas\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span><span class="sxs-lookup"><span data-stu-id="753d1-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![Aplankas GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="753d1-178">Jei prieš pakeičiant vertę, esančią .config faile, buvo tikrinimo atvejų, tų tikrinimo atvejų žurnalai nebus generuojami, kol nesugeneruosite naujų tikrinimo vykdymo failų.</span><span class="sxs-lookup"><span data-stu-id="753d1-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![Komanda Generuoti tik tikrinimo vykdymo failus meniu Naujas](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="753d1-180">Momentinė kopija</span><span class="sxs-lookup"><span data-stu-id="753d1-180">Snapshot</span></span>

<span data-ttu-id="753d1-181">Ši funkcija užfiksuoja veiksmų, kurie buvo atlikti įrašant užduotį, ekrano kopijas.</span><span class="sxs-lookup"><span data-stu-id="753d1-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="753d1-182">Norėdami naudoti šią funkciją atidarykite failą **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT diegimo aplanke (pvz., **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ir pakeiskite toliau nurodyto elemento reikšmę iš **false** į **true**.</span><span class="sxs-lookup"><span data-stu-id="753d1-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="753d1-183">Dalyje **C:\\Vartotojai\\\<Vartotojo vardas\>\\AppData\\Roaming\\regressionTool\\atkūrimas** sukuriamas atskiras aplankas, skirtas kiekvienam paleistam atvejui.</span><span class="sxs-lookup"><span data-stu-id="753d1-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![Tikrinimo atvejo momentinės kopijos aplankas](./media/use_rsa_tool_12.png)

<span data-ttu-id="753d1-185">Kiekviename iš šių aplankų galite rasti veiksmų, kurie buvo atlikti, kai buvo paleisti tikrinimo atvejai, momentines kopijas.</span><span class="sxs-lookup"><span data-stu-id="753d1-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![Momentinės kopijos failai](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="753d1-187">Priskyrimas</span><span class="sxs-lookup"><span data-stu-id="753d1-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="753d1-188">Scenarijus</span><span class="sxs-lookup"><span data-stu-id="753d1-188">Scenario</span></span>

1. <span data-ttu-id="753d1-189">Produkto dizaino įrankis sukuria naują išleistą produktą.</span><span class="sxs-lookup"><span data-stu-id="753d1-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="753d1-190">Gamybos vadovas inicijuoja gamybos užsakymą, kad atsargų lygį pakeltų dviem vienetais.</span><span class="sxs-lookup"><span data-stu-id="753d1-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="753d1-191">Gamyba pradeda ir baigia gamybos užsakymą bei patikrina, ar turimas kiekis yra du vienetai.</span><span class="sxs-lookup"><span data-stu-id="753d1-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="753d1-192">Pardavimo komanda gauna keturių naujo produkto vienetų užsakymą.</span><span class="sxs-lookup"><span data-stu-id="753d1-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="753d1-193">Todėl pardavimo komanda atnaujina grynuosius poreikius naudodami dinaminį planą.</span><span class="sxs-lookup"><span data-stu-id="753d1-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="753d1-194">Kadangi papildomų pajėgumų nėra, numatytoji užsakymo strategija nustatyta kaip „pirkti, o ne gaminti“.</span><span class="sxs-lookup"><span data-stu-id="753d1-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="753d1-195">Todėl sukuriamas suplanuotas pirkimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="753d1-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="753d1-196">Pirkėjas įtraukia tiekėją, sutvirtina suplanuotą pirkimo užsakymą, o tada patvirtina pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="753d1-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="753d1-197">Kai įsigytos prekės pristatomos į parduotuvę, parduotuvės operatorius ieško susijusio pirkimo užsakymo ir gauna prekes.</span><span class="sxs-lookup"><span data-stu-id="753d1-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="753d1-198">Kadangi užsakymas yra baigtas, prekes galima paimti ir supakuoti į pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="753d1-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="753d1-199">„Finance“ registruoja pirkimo SF ir pardavimo SF.</span><span class="sxs-lookup"><span data-stu-id="753d1-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="753d1-200">Tolesnėje iliustracijoje vaizduojamas šio scenarijaus srautas.</span><span class="sxs-lookup"><span data-stu-id="753d1-200">The following illustration shows the flow for this scenario.</span></span>

![Tikrinimo scenarijaus srautas](./media/use_rsa_tool_14.png)

<span data-ttu-id="753d1-202">Tolesnėje iliustracijoje vaizduojami šio scenarijaus veiklos procesai RSAT.</span><span class="sxs-lookup"><span data-stu-id="753d1-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![Tikrinimo scenarijaus veiklos procesai](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="753d1-204">Strategija – pagrindinis mokymasis</span><span class="sxs-lookup"><span data-stu-id="753d1-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="753d1-205">Duomenys</span><span class="sxs-lookup"><span data-stu-id="753d1-205">Data</span></span>

- <span data-ttu-id="753d1-206">Įsitikinkite, kad turite reprezentatyvius duomenis (gamybos / auksinės konfigūracijos duomenų kopiją ir migravo duomenų kopiją).</span><span class="sxs-lookup"><span data-stu-id="753d1-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="753d1-207">Kai generuojate naujus duomenis naudodami užduočių įrašymo priemonę, sukurkite tikrinimo pavadinimus, kurie derės su esamais pavadinimais (pavyzdžiui, naudokite prefiksą **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="753d1-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="753d1-208">Naudokite „Azure“ tam tikro laiko atkūrimą, kad iš naujo paleistumėte tikrinimus ne 1 pakopos aplinkose.</span><span class="sxs-lookup"><span data-stu-id="753d1-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="753d1-209">Nors galite naudoti „Excel“ funkcijas **ATSITIKTINIS** ir **DABAR**, kad sugeneruotumėte unikalų derinį, prireiks gana daug pastangų.</span><span class="sxs-lookup"><span data-stu-id="753d1-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="753d1-210">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="753d1-210">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="753d1-211">Užduoties įrašymo priemonė</span><span class="sxs-lookup"><span data-stu-id="753d1-211">Task recorder</span></span>

- <span data-ttu-id="753d1-212">Apibrėžkite scenarijus prieš pradėdami įrašyti.</span><span class="sxs-lookup"><span data-stu-id="753d1-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="753d1-213">Gerai valdomas projektas turi iš anksto apibrėžtus tikrinimo scenarijus.</span><span class="sxs-lookup"><span data-stu-id="753d1-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="753d1-214">Norėdami sukurti tikrinimo atvejį, pagalvokite, kiek nuspėjamas šių tikrinimo scenarijų rezultatas.</span><span class="sxs-lookup"><span data-stu-id="753d1-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="753d1-215">Išskaidykite įrašus, jei jie atlikti skirtingais vaidmenimis arba jei laukimo laikas ar išorinis įvykis yra prieš kitą veiksmą.</span><span class="sxs-lookup"><span data-stu-id="753d1-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="753d1-216">Venkite pasirinkti reikšmes sąrašuose.</span><span class="sxs-lookup"><span data-stu-id="753d1-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="753d1-217">Vietoje to naudokite teksto formatus, pvz., **FIFO**, **AudioRM** ir **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="753d1-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="753d1-218">Pasirinkus sąraše, įrašoma sąrašo reikšmės padėtis, o ne pati reikšmė.</span><span class="sxs-lookup"><span data-stu-id="753d1-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="753d1-219">Jei prekės yra įtrauktos į tą sąrašą, reikšmės padėtis gali pasikeisti.</span><span class="sxs-lookup"><span data-stu-id="753d1-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="753d1-220">Todėl jūsų įraše bus naudojamas kitoks parametras ir likusi scenarijaus dalis gali būti paveikta.</span><span class="sxs-lookup"><span data-stu-id="753d1-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="753d1-221">Pagalvokite apie kelių vartotojų elgseną.</span><span class="sxs-lookup"><span data-stu-id="753d1-221">Think about multi-user behavior.</span></span> <span data-ttu-id="753d1-222">Pavyzdžiui, nemanykite, kad jūsų naujai sukurtas pardavimo užsakymas visada bus parenkamas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="753d1-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="753d1-223">Vietoje to visada naudokite filtrą, kad rastumėte tinkamą užsakymą.</span><span class="sxs-lookup"><span data-stu-id="753d1-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="753d1-224">Norėdami užduočių įrašymo priemonės funkciją Kopijuoti, kad įrašytumėte naujai sukurto produkto pavadinimą ir jį būtų galima naudoti grandininio tikrinimo atvejais.</span><span class="sxs-lookup"><span data-stu-id="753d1-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="753d1-225">Norėdami nustatyti kontrolės punktus, kurie patikrina, ar veiksmai buvo vykdyti tinkamai, naudokite užduočių įrašymo priemonės funkciją Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="753d1-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="753d1-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="753d1-226">RSAT</span></span>

- <span data-ttu-id="753d1-227">Norėdami vykdyti tikrinimą kitoje įmonėje, galite pakeisti įmonę „Excel“ parametro failo skirtuke **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="753d1-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="753d1-228">Įsitikinkite, kad parametrai ir duomenys yra prieinami naujai pasirinktoje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="753d1-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="753d1-229">Galite pakeisti tikrinimo vartotoją „Excel“ parametro failo skirtuke **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="753d1-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="753d1-230">Nurodykite vartotojo, kuris vykdys tikrinimo atvejį, el. pašto ID.</span><span class="sxs-lookup"><span data-stu-id="753d1-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="753d1-231">Tokiu būdu tikrinimo atvejį galima vykdyti naudojant nurodyto vartotojo saugos teises.</span><span class="sxs-lookup"><span data-stu-id="753d1-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="753d1-232">Norėdami palaukti prieš pradėdami tikrinimą, galite nustatyti pauzę „Excel“ parametro failo skirtuke **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="753d1-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="753d1-233">Ši pauzė gali būti naudojama paketinėje užduotyje (pvz., jei darbo eiga turi būti vykdoma prieš atliekant kitus veiksmus).</span><span class="sxs-lookup"><span data-stu-id="753d1-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="753d1-234">Išplėstinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="753d1-234">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="753d1-235">CLI</span><span class="sxs-lookup"><span data-stu-id="753d1-235">CLI</span></span>

<span data-ttu-id="753d1-236">RSAT galima iškviesti lange **Komandinė eilutė** arba **„PowerShell“**.</span><span class="sxs-lookup"><span data-stu-id="753d1-236">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="753d1-237">Patikrinkite, ar aplinkos kintamasis **TestRoot** nustatytas kaip RSAT diegimo kelias.</span><span class="sxs-lookup"><span data-stu-id="753d1-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="753d1-238">(Programoje „Microsoft Windows“ atidarykite **valdymo skydą**, pasirinkite **Sistema ir sauga \> Sistema \> Išplėstiniai sistemos parametrai** ir pasirinkite **Aplinkos kintamieji**.)</span><span class="sxs-lookup"><span data-stu-id="753d1-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="753d1-239">Atidarykite langą **Komandinė eilutė** arba **„PowerShell“** kaip administratorius.</span><span class="sxs-lookup"><span data-stu-id="753d1-239">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="753d1-240">Nueikite į RSAT įdiegimo katalogą.</span><span class="sxs-lookup"><span data-stu-id="753d1-240">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="753d1-241">Išvardykite visas komandas.</span><span class="sxs-lookup"><span data-stu-id="753d1-241">List all commands.</span></span>

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a><span data-ttu-id="753d1-242">?</span><span class="sxs-lookup"><span data-stu-id="753d1-242">?</span></span> 
<span data-ttu-id="753d1-243">Rodoma pagalba apie visas galimas komandas ir jų parametrus.</span><span class="sxs-lookup"><span data-stu-id="753d1-243">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a><span data-ttu-id="753d1-244">Neprivalomi parametrai</span><span class="sxs-lookup"><span data-stu-id="753d1-244">Optional parameters</span></span>

**``command``**


<span data-ttu-id="753d1-245">Kur ``[command]`` yra viena iš toliau nurodytų komandų.</span><span class="sxs-lookup"><span data-stu-id="753d1-245">Where ``[command]`` is one of the commands specified below.</span></span>


#### <a name="about"></a><span data-ttu-id="753d1-246">about</span><span class="sxs-lookup"><span data-stu-id="753d1-246">about</span></span>
<span data-ttu-id="753d1-247">Rodoma dabartinė versija.</span><span class="sxs-lookup"><span data-stu-id="753d1-247">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="753d1-248">cls</span><span class="sxs-lookup"><span data-stu-id="753d1-248">cls</span></span>
<span data-ttu-id="753d1-249">Išvalomas ekranas.</span><span class="sxs-lookup"><span data-stu-id="753d1-249">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a><span data-ttu-id="753d1-250">atsisiųsti</span><span class="sxs-lookup"><span data-stu-id="753d1-250">download</span></span>
<span data-ttu-id="753d1-251">Į išvesties katalogą atsiunčiami nurodyto testavimo atvejo priedai.</span><span class="sxs-lookup"><span data-stu-id="753d1-251">Downloads attachments for the specified test case to the output directory.</span></span> <span data-ttu-id="753d1-252">Norėdami gauti visus galimus testavimo atvejus, galite naudoti komandą ``list``.</span><span class="sxs-lookup"><span data-stu-id="753d1-252">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="753d1-253">Kaip **test_case_id** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.</span><span class="sxs-lookup"><span data-stu-id="753d1-253">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="753d1-254">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="753d1-254">Required parameters</span></span>
<span data-ttu-id="753d1-255">**``test_case_id``** Nurodo testavimo atvejo ID.</span><span class="sxs-lookup"><span data-stu-id="753d1-255">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="753d1-256">**``output_dir``** Nurodo išvesties katalogą.</span><span class="sxs-lookup"><span data-stu-id="753d1-256">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="753d1-257">Katalogas privalo būti.</span><span class="sxs-lookup"><span data-stu-id="753d1-257">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="753d1-258">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="753d1-258">Examples</span></span>

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a><span data-ttu-id="753d1-259">redaguoti</span><span class="sxs-lookup"><span data-stu-id="753d1-259">edit</span></span>
<span data-ttu-id="753d1-260">Leidžia programoje „Excel“ atverti parametrų failą ir jį redaguoti.</span><span class="sxs-lookup"><span data-stu-id="753d1-260">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="753d1-261">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="753d1-261">Required parameters</span></span>
<span data-ttu-id="753d1-262">**``excel_file``** Turi būti nurodytas visas esamo „Excel“ failo kelias.</span><span class="sxs-lookup"><span data-stu-id="753d1-262">**``excel_file``** Must contain a full path to an existing Excel file.</span></span>

##### <a name="examples"></a><span data-ttu-id="753d1-263">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="753d1-263">Examples</span></span>
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a><span data-ttu-id="753d1-264">generate</span><span class="sxs-lookup"><span data-stu-id="753d1-264">generate</span></span>
<span data-ttu-id="753d1-265">Išvesties kataloge sugeneruojami nurodyto testavimo atvejo testavimo vykdymo ir parametrų failai.</span><span class="sxs-lookup"><span data-stu-id="753d1-265">Generates test execution and parameter files for the specified test case in the output directory.</span></span>
<span data-ttu-id="753d1-266">Norėdami gauti visus galimus testavimo atvejus, galite naudoti komandą ``list``.</span><span class="sxs-lookup"><span data-stu-id="753d1-266">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="753d1-267">Kaip **test_case_id** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.</span><span class="sxs-lookup"><span data-stu-id="753d1-267">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="753d1-268">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="753d1-268">Required parameters</span></span>
<span data-ttu-id="753d1-269">**``test_case_id``** Nurodo testavimo atvejo ID.</span><span class="sxs-lookup"><span data-stu-id="753d1-269">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="753d1-270">**``output_dir``** Nurodo išvesties katalogą.</span><span class="sxs-lookup"><span data-stu-id="753d1-270">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="753d1-271">Katalogas privalo būti.</span><span class="sxs-lookup"><span data-stu-id="753d1-271">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="753d1-272">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="753d1-272">Examples</span></span>
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a><span data-ttu-id="753d1-273">generatederived</span><span class="sxs-lookup"><span data-stu-id="753d1-273">generatederived</span></span>
<span data-ttu-id="753d1-274">Sugeneruojamas naujas testavimo atvejis, išvestas iš pateikto testavimo atvejo.</span><span class="sxs-lookup"><span data-stu-id="753d1-274">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="753d1-275">Norėdami gauti visus galimus testavimo atvejus, galite naudoti komandą ``list``.</span><span class="sxs-lookup"><span data-stu-id="753d1-275">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="753d1-276">Kaip **test_case_id** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.</span><span class="sxs-lookup"><span data-stu-id="753d1-276">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a><span data-ttu-id="753d1-277">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="753d1-277">Required parameters</span></span>
<span data-ttu-id="753d1-278">**``parent_test_case_id``** Nurodo pirminio testavimo atvejo ID.</span><span class="sxs-lookup"><span data-stu-id="753d1-278">**``parent_test_case_id``** Represents the parent test case ID.</span></span>  
<span data-ttu-id="753d1-279">**``test_plan_id``** Nurodo testavimo plano ID.</span><span class="sxs-lookup"><span data-stu-id="753d1-279">**``test_plan_id``** Represents the test plan ID.</span></span>  
<span data-ttu-id="753d1-280">**``test_suite_id``** Nurodo testavimo paketo ID.</span><span class="sxs-lookup"><span data-stu-id="753d1-280">**``test_suite_id``** Represents the test suite ID.</span></span>

##### <a name="examples"></a><span data-ttu-id="753d1-281">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="753d1-281">Examples</span></span>
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a><span data-ttu-id="753d1-282">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="753d1-282">generatetestonly</span></span>
<span data-ttu-id="753d1-283">Išvesties kataloge sugeneruojamas tik nurodyto testavimo atvejo testavimo vykdymo failas.</span><span class="sxs-lookup"><span data-stu-id="753d1-283">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="753d1-284">Norėdami gauti visus galimus testavimo atvejus, galite naudoti komandą ``list``.</span><span class="sxs-lookup"><span data-stu-id="753d1-284">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="753d1-285">Kaip **test_case_id** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.</span><span class="sxs-lookup"><span data-stu-id="753d1-285">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="753d1-286">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="753d1-286">Required parameters</span></span>
<span data-ttu-id="753d1-287">**``test_case_id``** Nurodo testavimo atvejo ID.</span><span class="sxs-lookup"><span data-stu-id="753d1-287">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="753d1-288">**``output_dir``** Nurodo išvesties katalogą.</span><span class="sxs-lookup"><span data-stu-id="753d1-288">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="753d1-289">Katalogas privalo būti.</span><span class="sxs-lookup"><span data-stu-id="753d1-289">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="753d1-290">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="753d1-290">Examples</span></span>
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a><span data-ttu-id="753d1-291">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="753d1-291">generatetestsuite</span></span>
<span data-ttu-id="753d1-292">Išvesties kataloge sugeneruojami visi nurodyto paketo testavimo atvejai.</span><span class="sxs-lookup"><span data-stu-id="753d1-292">Generates all test cases for the specified suite in the output directory.</span></span>
<span data-ttu-id="753d1-293">Norėdami gauti visus galimus testavimo paketus, galite naudoti komandą ``listtestsuitenames``.</span><span class="sxs-lookup"><span data-stu-id="753d1-293">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="753d1-294">Kaip **test_suite_name** parametrą naudokite bet kokią vertę iš stulpelio.</span><span class="sxs-lookup"><span data-stu-id="753d1-294">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="753d1-295">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="753d1-295">Required parameters</span></span>
<span data-ttu-id="753d1-296">**``test_suite_name``** Nurodo testavimo paketo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="753d1-296">**``test_suite_name``** Represents the test suite name.</span></span>  
<span data-ttu-id="753d1-297">**``output_dir``** Nurodo išvesties katalogą.</span><span class="sxs-lookup"><span data-stu-id="753d1-297">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="753d1-298">Katalogas privalo būti.</span><span class="sxs-lookup"><span data-stu-id="753d1-298">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="753d1-299">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="753d1-299">Examples</span></span>
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a><span data-ttu-id="753d1-300">help</span><span class="sxs-lookup"><span data-stu-id="753d1-300">help</span></span>
<span data-ttu-id="753d1-301">Identiška elementui [?](####?)</span><span class="sxs-lookup"><span data-stu-id="753d1-301">Identical to the [?](####?)</span></span> <span data-ttu-id="753d1-302">command</span><span class="sxs-lookup"><span data-stu-id="753d1-302">command</span></span>


#### <a name="list"></a><span data-ttu-id="753d1-303">sąrašas</span><span class="sxs-lookup"><span data-stu-id="753d1-303">list</span></span>
<span data-ttu-id="753d1-304">Išvardijami visi galimi testavimo atvejai.</span><span class="sxs-lookup"><span data-stu-id="753d1-304">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a><span data-ttu-id="753d1-305">listtestplans</span><span class="sxs-lookup"><span data-stu-id="753d1-305">listtestplans</span></span>
<span data-ttu-id="753d1-306">Išvardijami visi galimi testavimo planai.</span><span class="sxs-lookup"><span data-stu-id="753d1-306">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a><span data-ttu-id="753d1-307">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="753d1-307">listtestsuite</span></span>
<span data-ttu-id="753d1-308">Išvardijami nurodyto testavimo paketo testavimo atvejai.</span><span class="sxs-lookup"><span data-stu-id="753d1-308">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="753d1-309">Norėdami gauti visus galimus testavimo paketus, galite naudoti komandą ``listtestsuitenames``.</span><span class="sxs-lookup"><span data-stu-id="753d1-309">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="753d1-310">Kaip **suite_name** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.</span><span class="sxs-lookup"><span data-stu-id="753d1-310">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="753d1-311">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="753d1-311">Required parameters</span></span>
<span data-ttu-id="753d1-312">**``suite_name``** Norimo paketo pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="753d1-312">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="753d1-313">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="753d1-313">Examples</span></span>
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a><span data-ttu-id="753d1-314">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="753d1-314">listtestsuitenames</span></span>
<span data-ttu-id="753d1-315">Išvardijami visi galimi testavimo paketai.</span><span class="sxs-lookup"><span data-stu-id="753d1-315">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a><span data-ttu-id="753d1-316">playback</span><span class="sxs-lookup"><span data-stu-id="753d1-316">playback</span></span>
<span data-ttu-id="753d1-317">Atkuriamas testavimo atvejis naudojant „Excel“ failą.</span><span class="sxs-lookup"><span data-stu-id="753d1-317">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="753d1-318">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="753d1-318">Required parameters</span></span>
<span data-ttu-id="753d1-319">**``excel_file``** Visas kelias iki „Excel“ failo.</span><span class="sxs-lookup"><span data-stu-id="753d1-319">**``excel_file``** A full path to the Excel file.</span></span> <span data-ttu-id="753d1-320">Failas privalo būti.</span><span class="sxs-lookup"><span data-stu-id="753d1-320">File must exist.</span></span> 

##### <a name="examples"></a><span data-ttu-id="753d1-321">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="753d1-321">Examples</span></span>
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a><span data-ttu-id="753d1-322">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="753d1-322">playbackbyid</span></span>
<span data-ttu-id="753d1-323">Vienu metu atkuriami keli testavimo atvejai.</span><span class="sxs-lookup"><span data-stu-id="753d1-323">Plays back multiple test cases at once.</span></span>
<span data-ttu-id="753d1-324">Norėdami gauti visus galimus testavimo atvejus, galite naudoti komandą ``list``.</span><span class="sxs-lookup"><span data-stu-id="753d1-324">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="753d1-325">Kaip **test_case_id** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.</span><span class="sxs-lookup"><span data-stu-id="753d1-325">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a><span data-ttu-id="753d1-326">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="753d1-326">Required parameters</span></span>
<span data-ttu-id="753d1-327">**``test_case_id1``** Esamo testavimo atvejo ID.</span><span class="sxs-lookup"><span data-stu-id="753d1-327">**``test_case_id1``** ID of exisiting test case.</span></span>  
<span data-ttu-id="753d1-328">**``test_case_id2``** Esamo testavimo atvejo ID.</span><span class="sxs-lookup"><span data-stu-id="753d1-328">**``test_case_id2``** ID of exisiting test case.</span></span>  
<span data-ttu-id="753d1-329">**``test_case_idN``** Esamo testavimo atvejo ID.</span><span class="sxs-lookup"><span data-stu-id="753d1-329">**``test_case_idN``** ID of exisiting test case.</span></span>  

##### <a name="examples"></a><span data-ttu-id="753d1-330">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="753d1-330">Examples</span></span>
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a><span data-ttu-id="753d1-331">playbackmany</span><span class="sxs-lookup"><span data-stu-id="753d1-331">playbackmany</span></span>
<span data-ttu-id="753d1-332">Naudojant „Excel“ failus vienu metu atkuriama daug testavimo atvejų.</span><span class="sxs-lookup"><span data-stu-id="753d1-332">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a><span data-ttu-id="753d1-333">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="753d1-333">Required parameters</span></span>
<span data-ttu-id="753d1-334">**``excel_file1``** Visas kelias iki „Excel“ failo.</span><span class="sxs-lookup"><span data-stu-id="753d1-334">**``excel_file1``** Full path to the Excel file.</span></span> <span data-ttu-id="753d1-335">Failas privalo būti.</span><span class="sxs-lookup"><span data-stu-id="753d1-335">File must exist.</span></span>  
<span data-ttu-id="753d1-336">**``excel_file2``** Visas kelias iki „Excel“ failo.</span><span class="sxs-lookup"><span data-stu-id="753d1-336">**``excel_file2``** Full path to the Excel file.</span></span> <span data-ttu-id="753d1-337">Failas privalo būti.</span><span class="sxs-lookup"><span data-stu-id="753d1-337">File must exist.</span></span>  
<span data-ttu-id="753d1-338">**``excel_fileN``** Visas kelias iki „Excel“ failo.</span><span class="sxs-lookup"><span data-stu-id="753d1-338">**``excel_fileN``** Full path to the Excel file.</span></span> <span data-ttu-id="753d1-339">Failas privalo būti.</span><span class="sxs-lookup"><span data-stu-id="753d1-339">File must exist.</span></span>  

##### <a name="examples"></a><span data-ttu-id="753d1-340">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="753d1-340">Examples</span></span>
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a><span data-ttu-id="753d1-341">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="753d1-341">playbacksuite</span></span>
<span data-ttu-id="753d1-342">Atkuriami visi testavimo atvejai iš nurodyto testavimo paketo.</span><span class="sxs-lookup"><span data-stu-id="753d1-342">Plays back all test cases from the specified test suite.</span></span> <span data-ttu-id="753d1-343">Norėdami gauti visus galimus testavimo paketus, galite naudoti komandą ``listtestsuitenames``.</span><span class="sxs-lookup"><span data-stu-id="753d1-343">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="753d1-344">Kaip **suite_name** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.</span><span class="sxs-lookup"><span data-stu-id="753d1-344">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="753d1-345">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="753d1-345">Required parameters</span></span>
<span data-ttu-id="753d1-346">**``suite_name``** Norimo paketo pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="753d1-346">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="753d1-347">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="753d1-347">Examples</span></span>
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a><span data-ttu-id="753d1-348">quit</span><span class="sxs-lookup"><span data-stu-id="753d1-348">quit</span></span>
<span data-ttu-id="753d1-349">Uždaroma programa.</span><span class="sxs-lookup"><span data-stu-id="753d1-349">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a><span data-ttu-id="753d1-350">upload</span><span class="sxs-lookup"><span data-stu-id="753d1-350">upload</span></span>
<span data-ttu-id="753d1-351">Nusiunčiami visi nurodyto testavimo paketo ar testavimo atvejų failai.</span><span class="sxs-lookup"><span data-stu-id="753d1-351">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a><span data-ttu-id="753d1-352">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="753d1-352">Required parameters</span></span>
<span data-ttu-id="753d1-353">**``suite_name``** Bus nusiųsti visi nurodyto testavimo paketo failai.</span><span class="sxs-lookup"><span data-stu-id="753d1-353">**``suite_name``** All files belonging to the specified test suite will be uploaded.</span></span>
<span data-ttu-id="753d1-354">**``testcase_id``** Bus nusiųsti visi nurodyto (-ų) testavimo atvejo (-ų) failai.</span><span class="sxs-lookup"><span data-stu-id="753d1-354">**``testcase_id``** All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="753d1-355">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="753d1-355">Examples</span></span>
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a><span data-ttu-id="753d1-356">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="753d1-356">uploadrecording</span></span>
<span data-ttu-id="753d1-357">Nusiunčiamas tik nurodytų testavimo atvejų įrašo failas.</span><span class="sxs-lookup"><span data-stu-id="753d1-357">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a><span data-ttu-id="753d1-358">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="753d1-358">Required parameters</span></span>
<span data-ttu-id="753d1-359">**``testcase_id``** Bus nusiųstas nurodytų testavimo atvejų įrašo failas.</span><span class="sxs-lookup"><span data-stu-id="753d1-359">**``testcase_id``** Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="753d1-360">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="753d1-360">Examples</span></span>
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a><span data-ttu-id="753d1-361">usage</span><span class="sxs-lookup"><span data-stu-id="753d1-361">usage</span></span>
<span data-ttu-id="753d1-362">Rodomi du būdai, kaip iškviesti šią programą: naudojant numatytąjį parametrų failą arba pateikiant parametrų failą.</span><span class="sxs-lookup"><span data-stu-id="753d1-362">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a><span data-ttu-id="753d1-363">„Windows PowerShell“ pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="753d1-363">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="753d1-364">Tikrinimo atvejo vykdymas cikle</span><span class="sxs-lookup"><span data-stu-id="753d1-364">Run a test case in a loop</span></span>

<span data-ttu-id="753d1-365">Turite tikrinimo scenarijų, kuris sukuria naują klientą.</span><span class="sxs-lookup"><span data-stu-id="753d1-365">You have a test script that creates a new customer.</span></span> <span data-ttu-id="753d1-366">Naudojant scenarijų šis tikrinimo atvejis gali būti vykdomas ciklu, nustatant toliau nurodytų duomenų atsitiktinumą prie kiekvieno pakartojimo vykdymą.</span><span class="sxs-lookup"><span data-stu-id="753d1-366">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="753d1-367">Kliento ID</span><span class="sxs-lookup"><span data-stu-id="753d1-367">Customer ID</span></span>
- <span data-ttu-id="753d1-368">Kliento pavadinimas</span><span class="sxs-lookup"><span data-stu-id="753d1-368">Customer name</span></span>
- <span data-ttu-id="753d1-369">Kliento adresas</span><span class="sxs-lookup"><span data-stu-id="753d1-369">Customer address</span></span>

<span data-ttu-id="753d1-370">Kliento ID bus formato *ATCUS\<skaičius\>*, kai \<skaičius\> yra reikšmė tarp **000000001** ir **999999999**.</span><span class="sxs-lookup"><span data-stu-id="753d1-370">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="753d1-371">Tolesnis pavyzdys naudoja vieną parametrą, **pradžia**, kad apibrėžtų pirmą naudojamą skaičių.</span><span class="sxs-lookup"><span data-stu-id="753d1-371">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="753d1-372">Jis naudoja antrą parametrą, **Nr.**, kad apibrėžtų klientų, kurie turi būti sukurti, skaičių.</span><span class="sxs-lookup"><span data-stu-id="753d1-372">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="753d1-373">Kiekvieno pakartojimo metu „Excel“ parametro failo parametrai pakeičiami naudojant funkciją UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="753d1-373">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="753d1-374">Tada RSAT komandinė eilutė iškviečiama funkcijoje RunTestCase.</span><span class="sxs-lookup"><span data-stu-id="753d1-374">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="753d1-375">Atidarykite „Microsoft Windows PowerShell Integrated Scripting Environment“ (ISE) administratorius režimu ir įklijuokite toliau nurodytą kodą į langą, pavadintą **Untitled1.ps1.**</span><span class="sxs-lookup"><span data-stu-id="753d1-375">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to excel file parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="753d1-376">Vykdykite scenarijų, kuris priklauso nuo duomenų „Microsoft Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="753d1-376">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="753d1-377">Toliau pateiktame pavyzdyje naudojamas „Open Data Protocol“ („OData“) iškvietimas, kad būtų galima rasti pirkimo užsakymo būseną.</span><span class="sxs-lookup"><span data-stu-id="753d1-377">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="753d1-378">Jei būsena nėra **išrašyta SF**, galite, pavyzdžiui, iškviesti RSAT tikrinimo atvejį, kuris užregistruos SF.</span><span class="sxs-lookup"><span data-stu-id="753d1-378">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```xpp
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```
