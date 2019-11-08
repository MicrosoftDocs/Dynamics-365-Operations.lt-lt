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
ms.openlocfilehash: 9afa98156c58d10c19454430769a3d60343661dc
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550962"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="5b2ee-104">„Regression Suite Automation Tool“ mokymo programos naudojimas</span><span class="sxs-lookup"><span data-stu-id="5b2ee-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="5b2ee-105">Naudodamiesi interneto naršyklės įrankiais atsisiųskite ir įrašykite šį puslapį PDF formatu.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="5b2ee-106">Šioje mokymo priemonėje paaiškinamos kai kurios išplėstinės „Regression Suite Automation Tool“ (RSAT) funkcijos, pateikiamas demonstracinis priskyrimas ir aprašoma strategija bei pagrindiniai mokymosi aspektai.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="5b2ee-107">RSAT / užduočių įrašymo priemonės funkcijos</span><span class="sxs-lookup"><span data-stu-id="5b2ee-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="5b2ee-108">Patikrinti lauko reikšmę</span><span class="sxs-lookup"><span data-stu-id="5b2ee-108">Validate a field value</span></span>

<span data-ttu-id="5b2ee-109">Norėdami gauti informacijos apie šią funkciją, žr. [Naujo užduoties įrašo, turinčio tikrinimo funkciją, kūrimas](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span><span class="sxs-lookup"><span data-stu-id="5b2ee-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="5b2ee-110">Įrašytas kintamasis</span><span class="sxs-lookup"><span data-stu-id="5b2ee-110">Saved variable</span></span>

<span data-ttu-id="5b2ee-111">Norėdami gauti informacijos apie šią funkciją, žr. [Esamo užduoties įrašo modifikavimas norint sukurti įrašytą kintamąjį](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span><span class="sxs-lookup"><span data-stu-id="5b2ee-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="5b2ee-112">Išvesto testo atvejis</span><span class="sxs-lookup"><span data-stu-id="5b2ee-112">Derived test case</span></span>

1. <span data-ttu-id="5b2ee-113">Atidarykite „Regression Suite Automation Tool“ (RSAT) ir pasirinkite abu bandomuosius atvejus, kuriuos sukūrėte atlikdami veiksmą [„Regression Suite Automation Tool“ nustatymas ir diegimas](./hol-set-up-regression-suite-automation-tool.md).</span><span class="sxs-lookup"><span data-stu-id="5b2ee-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="5b2ee-114">Pasirinkite **Naujas \> Kurti išvestinį tikrinimo atvejį**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-114">Select **New \> Create derived test case**.</span></span>

    ![Komanda Kurti išvestinį tikrinimo atvejį meniu Naujas](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="5b2ee-116">Gaunate pranešimą, kuriame teigiama, kad kiekvienam pasirinktam tikrinimui skirtas tikrinimo atvejis bus sukurtas pagal dabartinį tikrinimo komplektą ir kad kiekvienas išvestinis tikrinimo atvejis turės savo „Excel“ parametro failo kopiją.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="5b2ee-117">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5b2ee-118">Paleidus išvestinį tikrinimo atvejį, jis naudoja jo pirminio tikrinimo atvejo ir savo „Excel“ parametro failo kopijos užduoties įrašą.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="5b2ee-119">Tokiu būdu galite atlikti tą patį tikrinimą su skirtingais parametrais, neprivalėdami tvarkyti daugiau nei vieną užduoties įrašą.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="5b2ee-120">Išvestinis tikrinimo atvejis nebūtinai turi priklausyti tam pačiam tikrinimų paketui kaip jo pirminis tikrinimo atvejis.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![Pranešimo laukas](./media/use_rsa_tool_02.png)

    <span data-ttu-id="5b2ee-122">Sukuriami du papildomi išvestiniai tikrinimo atvejai ir pažymimas jų žymės langelis **Išvestinis?**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![Sukuriami išvestiniai tikrinimo atvejai](./media/use_rsa_tool_03.png)

    <span data-ttu-id="5b2ee-124">Išvestinis tikrinimo atvejis sukuriamas automatiškai „Azure DevOps“.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="5b2ee-125">Tai antrinis tikrinimo atvejo **Kurti naują produktą** elementas ir jis pažymėtas specialiu raktažodžiu: **RSAT:DerivedTestSteps**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="5b2ee-126">Šie tikrinimo atvejai taip pat automatiškai įtraukiami į tikrinimo planą „Azure DevOps“.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![Raktažodis RSAT:DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="5b2ee-128">Jei dėl kokių nors priežasčių išvestiniai tikrinimo atvejai nėra pateikiami tinkama tvarka, atidarykite „Azure DevOps“ ir pertvarkykite tikrinimo atvejus tikrinimo komplekte, kad RSAT galėtų paleisti juos tinkama tvarka.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="5b2ee-129">Pasirinkite išvestinius tikrinimo atvejus ir pasirinkite **Redaguoti**, kad atidarytumėte atitinkamus „Excel“ parametrų failus.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="5b2ee-130">Redaguokite šiuos „Excel“ parametrų failus tokiu pat būdu, kaip redagavote pirminį failą.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="5b2ee-131">Kitaip tariant, įsitikinkite, kad produkto ID nustatytas taip, jog jis būtų automatiškai sugeneruotas.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="5b2ee-132">Taip pat įsitikinkite, kad įrašytas kintamasis nukopijuojamas į atitinkamus laukus.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="5b2ee-133">Abiejų „Excel“ parametrų failų skirtukuose **Bendra** atnaujinkite lauko **Įmonė** reikšmę į **USSI**, kad išvestiniai tikrinimo atvejai būtų vykdomi kitame juridiniame subjekte nei pirminis tikrinimo atvejis.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="5b2ee-134">Norėdami vykdyti tikrinimo atvejus pagal konkretų vartotoją (arba vaidmenį, kuris susietas su konkrečiu vartotoju), galite atnaujinti lauko **Tikrinimo vartotojas** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="5b2ee-135">Pasirinkite **Vykdyti** ir įsitikinkite, kad produktas sukurtas ir juridiniame subjekte USMF ir juridiniame subjekte USSI.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="5b2ee-136">Tikrinti pranešimus</span><span class="sxs-lookup"><span data-stu-id="5b2ee-136">Validate notifications</span></span>

<span data-ttu-id="5b2ee-137">Šią funkciją galima naudoti norint patikrinti, ar įvyko veiksmas.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="5b2ee-138">Pavyzdžiui, kai sukuriamas, įvertinamas ir pradedamas gamybos užsakymas, programa rodo pranešimą „Gamyba – pradžia“, kad praneštų, jog pradėtas gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-138">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Pranešimas Gamyba – pradžia](./media/use_rsa_tool_05.png)

<span data-ttu-id="5b2ee-140">Šį pranešimą galite patikrinti naudodami RSAT – įveskite pranešimo tekstą atitinkamo įrašo „Excel“ parametro failo skirtuke **MessageValidation**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Skirtukas Pranešimo tikrinimas](./media/use_rsa_tool_06.png)

<span data-ttu-id="5b2ee-142">Paleidus tikrinimo atvejį, pranešimas „Excel“ parametro faile palyginamas su rodomu pranešimu.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="5b2ee-143">Jei pranešimai nesutampa, tikrinimo atvejis nepavyks.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="5b2ee-144">„Excel“ parametro failo skirtuke **MessageValidation** galite įvesti daugiau nei vieną pranešimą.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="5b2ee-145">Pranešimai taip pat gali būti klaidos arba įspėjantys, o ne informaciniai pranešimai.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="5b2ee-146">Tikrinti reikšmes naudojant operatorius</span><span class="sxs-lookup"><span data-stu-id="5b2ee-146">Validate values by using operators</span></span>

<span data-ttu-id="5b2ee-147">Ankstesnėse RSAT versijose galėjote tikrinti vertes tik jei kontrolinė reikšmė sutapo su numatoma reikšme.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="5b2ee-148">Nauja funkcija suteikia galimybę patikrinti, ar kintamasis nėra lygus, yra mažesnis arba yra didesnis už nurodytą reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="5b2ee-149">Norėdami naudoti šią funkciją atidarykite failą **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT diegimo aplanke (pvz., **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ir pakeiskite toliau nurodyto elemento reikšmę iš **false** į **true**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="5b2ee-150">„Excel“ parametro faile atsiranda naujas laukas **Operatorius**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5b2ee-151">Jei naudojate senesnę RSAT versiją, turite sugeneruoti naujus „Excel“ parametrų failus.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![Laukas Operatorius](./media/use_rsa_tool_07.png)

<span data-ttu-id="5b2ee-153">Toliau pateiktame pavyzdyje parodyta, kaip galima naudoti šią funkciją norint patikrinti, ar turimos atsargos yra daugiau nei 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="5b2ee-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="5b2ee-154">Įmonės **USMF** demonstraciniuose duomenyse sukurkite užduoties įrašą, sudarytą iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="5b2ee-155">Eikite į **Produkto informacijos valdymas \> Produktai \> Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="5b2ee-156">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5b2ee-157">Pvz., filtruokite lauko **Prekės numeris** reikšme **1000**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="5b2ee-158">Pasirinkite **Turimos atsargos**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="5b2ee-159">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5b2ee-160">Pvz., filtruokite lauko **Vieta** reikšme **1**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="5b2ee-161">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="5b2ee-162">Patikrinkite, ar lauko **Iš viso turima** yra reikšmė yra **411,0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="5b2ee-163">Įrašykite užduoties įrašą į BPM biblioteką, esančią LCS, ir sinchronizuokite jį į „Azure DevOps“.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="5b2ee-164">Įtraukite tikrinimo atvejį į tikrinimo planą ir įkelkite tikrinimo atvejį į RSAT.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="5b2ee-165">Atidarykite „Excel“ parametrų failą.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-165">Open the Excel parameter file.</span></span> <span data-ttu-id="5b2ee-166">Skirtuke **InventOnhandItem** matysite skiltį **Tikrinti InventOnhandItem**, kurioje pateiktas laukas **Operatorius**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Laukas Operatorius](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="5b2ee-168">Norėdami patikrinti, ar turimos atsargos visada bus didesnės nei 0, pakeiskite lauko **Vertė** reikšmę iš **411** į **0**, o lauko **Operatorius** reikšmę – iš lygybės ženklo (**=**) į ženklą „daugiau nei“ (**\>**).</span><span class="sxs-lookup"><span data-stu-id="5b2ee-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Pakeistos laukų Vertė ir Operatorius reikšmės](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="5b2ee-170">Įrašykite ir uždarykite „Excel“ parametro failą.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="5b2ee-171">Pasirinkite **Įkelti**, kad įrašytumėte keitimus, atliktus „Excel“ parametro faile, į „Azure DevOps“.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="5b2ee-172">Dabar, jei nurodytos atsargų prekės reikšmė lauke **Iš viso turima** yra didesnė nei 0 (nulis), tikrinimai pavyks, nepriklausomai nuo faktinės turimų atsargų vertės.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="5b2ee-173">Generatoriaus žurnalai</span><span class="sxs-lookup"><span data-stu-id="5b2ee-173">Generator logs</span></span>

<span data-ttu-id="5b2ee-174">Ši funkcija sukuria aplanką, kuriame yra paleistų tikrinimo atvejų žurnalai.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="5b2ee-175">Norėdami naudoti šią funkciją atidarykite failą **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT diegimo aplanke (pvz., **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ir pakeiskite toliau nurodyto elemento reikšmę iš **false** į **true**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="5b2ee-176">Paleidus tikrinimo atvejus, žurnalų failus galima rasti čia: **C:\\Vartotojai\\\<Vartotojo vardas\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![Aplankas GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="5b2ee-178">Jei prieš pakeičiant vertę, esančią .config faile, buvo tikrinimo atvejų, tų tikrinimo atvejų žurnalai nebus generuojami, kol nesugeneruosite naujų tikrinimo vykdymo failų.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![Komanda Generuoti tik tikrinimo vykdymo failus meniu Naujas](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="5b2ee-180">Momentinė kopija</span><span class="sxs-lookup"><span data-stu-id="5b2ee-180">Snapshot</span></span>

<span data-ttu-id="5b2ee-181">Ši funkcija užfiksuoja veiksmų, kurie buvo atlikti įrašant užduotį, ekrano kopijas.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="5b2ee-182">Norėdami naudoti šią funkciją atidarykite failą **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT diegimo aplanke (pvz., **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ir pakeiskite toliau nurodyto elemento reikšmę iš **false** į **true**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="5b2ee-183">Dalyje **C:\\Vartotojai\\\<Vartotojo vardas\>\\AppData\\Roaming\\regressionTool\\atkūrimas** sukuriamas atskiras aplankas, skirtas kiekvienam paleistam atvejui.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![Tikrinimo atvejo momentinės kopijos aplankas](./media/use_rsa_tool_12.png)

<span data-ttu-id="5b2ee-185">Kiekviename iš šių aplankų galite rasti veiksmų, kurie buvo atlikti, kai buvo paleisti tikrinimo atvejai, momentines kopijas.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![Momentinės kopijos failai](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="5b2ee-187">Priskyrimas</span><span class="sxs-lookup"><span data-stu-id="5b2ee-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="5b2ee-188">Scenarijus</span><span class="sxs-lookup"><span data-stu-id="5b2ee-188">Scenario</span></span>

1. <span data-ttu-id="5b2ee-189">Produkto dizaino įrankis sukuria naują išleistą produktą.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="5b2ee-190">Gamybos vadovas inicijuoja gamybos užsakymą, kad atsargų lygį pakeltų dviem vienetais.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="5b2ee-191">Gamyba pradeda ir baigia gamybos užsakymą bei patikrina, ar turimas kiekis yra du vienetai.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="5b2ee-192">Pardavimo komanda gauna keturių naujo produkto vienetų užsakymą.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="5b2ee-193">Todėl pardavimo komanda atnaujina grynuosius poreikius naudodami dinaminį planą.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="5b2ee-194">Kadangi papildomų pajėgumų nėra, numatytoji užsakymo strategija nustatyta kaip „pirkti, o ne gaminti“.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="5b2ee-195">Todėl sukuriamas suplanuotas pirkimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="5b2ee-196">Pirkėjas įtraukia tiekėją, sutvirtina suplanuotą pirkimo užsakymą, o tada patvirtina pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="5b2ee-197">Kai įsigytos prekės pristatomos į parduotuvę, parduotuvės operatorius ieško susijusio pirkimo užsakymo ir gauna prekes.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="5b2ee-198">Kadangi užsakymas yra baigtas, prekes galima paimti ir supakuoti į pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="5b2ee-199">„Finance“ registruoja pirkimo SF ir pardavimo SF.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="5b2ee-200">Tolesnėje iliustracijoje vaizduojamas šio scenarijaus srautas.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-200">The following illustration shows the flow for this scenario.</span></span>

![Tikrinimo scenarijaus srautas](./media/use_rsa_tool_14.png)

<span data-ttu-id="5b2ee-202">Tolesnėje iliustracijoje vaizduojami šio scenarijaus veiklos procesai RSAT.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![Tikrinimo scenarijaus veiklos procesai](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="5b2ee-204">Strategija – pagrindinis mokymasis</span><span class="sxs-lookup"><span data-stu-id="5b2ee-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="5b2ee-205">Duomenys</span><span class="sxs-lookup"><span data-stu-id="5b2ee-205">Data</span></span>

- <span data-ttu-id="5b2ee-206">Įsitikinkite, kad turite reprezentatyvius duomenis (gamybos / auksinės konfigūracijos duomenų kopiją ir migravo duomenų kopiją).</span><span class="sxs-lookup"><span data-stu-id="5b2ee-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="5b2ee-207">Kai generuojate naujus duomenis naudodami užduočių įrašymo priemonę, sukurkite tikrinimo pavadinimus, kurie derės su esamais pavadinimais (pavyzdžiui, naudokite prefiksą **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="5b2ee-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="5b2ee-208">Naudokite „Azure“ tam tikro laiko atkūrimą, kad iš naujo paleistumėte tikrinimus ne 1 pakopos aplinkose.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="5b2ee-209">Nors galite naudoti „Excel“ funkcijas **ATSITIKTINIS** ir **DABAR**, kad sugeneruotumėte unikalų derinį, prireiks gana daug pastangų.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="5b2ee-210">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-210">Here is an example.</span></span>

    ```
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="5b2ee-211">Užduoties įrašymo priemonė</span><span class="sxs-lookup"><span data-stu-id="5b2ee-211">Task recorder</span></span>

- <span data-ttu-id="5b2ee-212">Apibrėžkite scenarijus prieš pradėdami įrašyti.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="5b2ee-213">Gerai valdomas projektas turi iš anksto apibrėžtus tikrinimo scenarijus.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="5b2ee-214">Norėdami sukurti tikrinimo atvejį, pagalvokite, kiek nuspėjamas šių tikrinimo scenarijų rezultatas.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="5b2ee-215">Išskaidykite įrašus, jei jie atlikti skirtingais vaidmenimis arba jei laukimo laikas ar išorinis įvykis yra prieš kitą veiksmą.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="5b2ee-216">Venkite pasirinkti reikšmes sąrašuose.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="5b2ee-217">Vietoje to naudokite teksto formatus, pvz., **FIFO**, **AudioRM** ir **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="5b2ee-218">Pasirinkus sąraše, įrašoma sąrašo reikšmės padėtis, o ne pati reikšmė.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="5b2ee-219">Jei prekės yra įtrauktos į tą sąrašą, reikšmės padėtis gali pasikeisti.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="5b2ee-220">Todėl jūsų įraše bus naudojamas kitoks parametras ir likusi scenarijaus dalis gali būti paveikta.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="5b2ee-221">Pagalvokite apie kelių vartotojų elgseną.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-221">Think about multi-user behavior.</span></span> <span data-ttu-id="5b2ee-222">Pavyzdžiui, nemanykite, kad jūsų naujai sukurtas pardavimo užsakymas visada bus parenkamas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="5b2ee-223">Vietoje to visada naudokite filtrą, kad rastumėte tinkamą užsakymą.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="5b2ee-224">Norėdami užduočių įrašymo priemonės funkciją Kopijuoti, kad įrašytumėte naujai sukurto produkto pavadinimą ir jį būtų galima naudoti grandininio tikrinimo atvejais.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="5b2ee-225">Norėdami nustatyti kontrolės punktus, kurie patikrina, ar veiksmai buvo vykdyti tinkamai, naudokite užduočių įrašymo priemonės funkciją Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="5b2ee-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="5b2ee-226">RSAT</span></span>

- <span data-ttu-id="5b2ee-227">Norėdami vykdyti tikrinimą kitoje įmonėje, galite pakeisti įmonę „Excel“ parametro failo skirtuke **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="5b2ee-228">Įsitikinkite, kad parametrai ir duomenys yra prieinami naujai pasirinktoje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="5b2ee-229">Galite pakeisti tikrinimo vartotoją „Excel“ parametro failo skirtuke **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="5b2ee-230">Nurodykite vartotojo, kuris vykdys tikrinimo atvejį, el. pašto ID.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="5b2ee-231">Tokiu būdu tikrinimo atvejį galima vykdyti naudojant nurodyto vartotojo saugos teises.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="5b2ee-232">Norėdami palaukti prieš pradėdami tikrinimą, galite nustatyti pauzę „Excel“ parametro failo skirtuke **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="5b2ee-233">Ši pauzė gali būti naudojama paketinėje užduotyje (pvz., jei darbo eiga turi būti vykdoma prieš atliekant kitus veiksmus).</span><span class="sxs-lookup"><span data-stu-id="5b2ee-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="5b2ee-234">Išplėstinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="5b2ee-234">Advanced scripting</span></span>

### <a name="command-line"></a><span data-ttu-id="5b2ee-235">Komandinė eilutė</span><span class="sxs-lookup"><span data-stu-id="5b2ee-235">Command line</span></span>

<span data-ttu-id="5b2ee-236">RSAT galima iškviesti lange **Komandinė eilutė**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-236">RSAT can be called from a **Command Prompt** window.</span></span>

> [!NOTE]
> <span data-ttu-id="5b2ee-237">Patikrinkite, ar aplinkos kintamasis **TestRoot** nustatytas kaip RSAT diegimo kelias.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="5b2ee-238">(Programoje „Microsoft Windows“ atidarykite **valdymo skydą**, pasirinkite **Sistema ir sauga \> Sistema \> Išplėstiniai sistemos parametrai** ir pasirinkite **Aplinkos kintamieji**.)</span><span class="sxs-lookup"><span data-stu-id="5b2ee-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="5b2ee-239">Atidarykite langą **Komandinė eilutė** kaip administratorius.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-239">Open a **Command Prompt** window as an admin.</span></span>
2. <span data-ttu-id="5b2ee-240">Paleiskite įrankį iš diegimo katalogo.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-240">Run the tool from the installation directory.</span></span>

    ```
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="5b2ee-241">Išvardykite visas komandas.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-241">List all commands.</span></span>

    ```
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a><span data-ttu-id="5b2ee-242">„Windows PowerShell“ pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="5b2ee-242">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="5b2ee-243">Tikrinimo atvejo vykdymas cikle</span><span class="sxs-lookup"><span data-stu-id="5b2ee-243">Run a test case in a loop</span></span>

<span data-ttu-id="5b2ee-244">Turite tikrinimo scenarijų, kuris sukuria naują klientą.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-244">You have a test script that creates a new customer.</span></span> <span data-ttu-id="5b2ee-245">Naudojant scenarijų šis tikrinimo atvejis gali būti vykdomas ciklu, nustatant toliau nurodytų duomenų atsitiktinumą prie kiekvieno pakartojimo vykdymą.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-245">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="5b2ee-246">Kliento ID</span><span class="sxs-lookup"><span data-stu-id="5b2ee-246">Customer ID</span></span>
- <span data-ttu-id="5b2ee-247">Kliento pavadinimas</span><span class="sxs-lookup"><span data-stu-id="5b2ee-247">Customer name</span></span>
- <span data-ttu-id="5b2ee-248">Kliento adresas</span><span class="sxs-lookup"><span data-stu-id="5b2ee-248">Customer address</span></span>

<span data-ttu-id="5b2ee-249">Kliento ID bus formato *ATCUS\<skaičius\>*, kai \<skaičius\> yra reikšmė tarp **000000001** ir **999999999**.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-249">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="5b2ee-250">Tolesnis pavyzdys naudoja vieną parametrą, **pradžia**, kad apibrėžtų pirmą naudojamą skaičių.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-250">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="5b2ee-251">Jis naudoja antrą parametrą, **Nr.**, kad apibrėžtų klientų, kurie turi būti sukurti, skaičių.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-251">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="5b2ee-252">Kiekvieno pakartojimo metu „Excel“ parametro failo parametrai pakeičiami naudojant funkciją UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-252">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="5b2ee-253">Tada RSAT komandinė eilutė iškviečiama funkcijoje RunTestCase.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-253">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="5b2ee-254">Atidarykite „Microsoft Windows PowerShell Integrated Scripting Environment“ (ISE) administratorius režimu ir įklijuokite toliau nurodytą kodą į langą, pavadintą **Untitled1.ps1.**</span><span class="sxs-lookup"><span data-stu-id="5b2ee-254">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```
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

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="5b2ee-255">Vykdykite scenarijų, kuris priklauso nuo duomenų „Microsoft Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="5b2ee-255">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="5b2ee-256">Toliau pateiktame pavyzdyje naudojamas „Open Data Protocol“ („OData“) iškvietimas, kad būtų galima rasti pirkimo užsakymo būseną.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-256">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="5b2ee-257">Jei būsena nėra **išrašyta SF**, galite, pavyzdžiui, iškviesti RSAT tikrinimo atvejį, kuris užregistruos SF.</span><span class="sxs-lookup"><span data-stu-id="5b2ee-257">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```
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
