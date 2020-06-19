---
title: „Regression Suite Automation Tool“ mokymo programos naudojimas
description: Šioje temoje parodoma, kaip naudoti „Regression Suite Automation Tool“ (RSAT). Joje aprašomos įvairios funkcijos ir pateikiami pavyzdžiai, kuriuose naudojami išplėstiniai scenarijai.
author: robinarh
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 0c2babc3144cae5c68075bd853a2587505263776
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410155"
---
# <a name="regression-suite-automation-tool-tutorial"></a><span data-ttu-id="bcad9-104">„Regression Suite Automation Tool“ mokymas</span><span class="sxs-lookup"><span data-stu-id="bcad9-104">Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="bcad9-105">Naudodamiesi interneto naršyklės įrankiais atsisiųskite ir įrašykite šį puslapį PDF formatu.</span><span class="sxs-lookup"><span data-stu-id="bcad9-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="bcad9-106">Šioje mokymo priemonėje paaiškinamos kai kurios išplėstinės „Regression Suite Automation Tool“ (RSAT) funkcijos, pateikiamas demonstracinis priskyrimas ir aprašoma strategija bei pagrindiniai mokymosi aspektai.</span><span class="sxs-lookup"><span data-stu-id="bcad9-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span> 

## <a name="notable-features-of-rsat-and-task-recorder"></a><span data-ttu-id="bcad9-107">Įsidėmėtinos RSAT ir užduočių įrašymo priemonės funkcijos</span><span class="sxs-lookup"><span data-stu-id="bcad9-107">Notable Features of RSAT and Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="bcad9-108">Patikrinti lauko reikšmę</span><span class="sxs-lookup"><span data-stu-id="bcad9-108">Validate a field value</span></span>

<span data-ttu-id="bcad9-109">RSAT leidžia įtraukti tikrinimo veiksmus jūsų testavimo atveju, kad galėtumėte tikrinti numatomas vertes.</span><span class="sxs-lookup"><span data-stu-id="bcad9-109">RSAT allows you to include validation steps within your test case to validate expected values.</span></span> <span data-ttu-id="bcad9-110">Daugiau informacijos apie šią funkciją žr. straipsnyje [Numatomų verčių tikrinimas](../../dev-itpro/perf-test/rsat/rsat-validate-expected.md).</span><span class="sxs-lookup"><span data-stu-id="bcad9-110">For information about this feature, see the article [Validate expected values](../../dev-itpro/perf-test/rsat/rsat-validate-expected.md).</span></span>

<span data-ttu-id="bcad9-111">Toliau pateiktame pavyzdyje parodyta, kaip galima naudoti šią funkciją norint patikrinti, ar turimos atsargos yra daugiau nei 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="bcad9-111">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="bcad9-112">Įmonės **USMF** demonstraciniuose duomenyse sukurkite užduoties įrašą, sudarytą iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="bcad9-112">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="bcad9-113">Eikite į **Produkto informacijos valdymas \> Produktai \> Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="bcad9-113">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="bcad9-114">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="bcad9-115">Pvz., filtruokite lauko **Prekės numeris** reikšme **1000**.</span><span class="sxs-lookup"><span data-stu-id="bcad9-115">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="bcad9-116">Pasirinkite **Turimos atsargos**.</span><span class="sxs-lookup"><span data-stu-id="bcad9-116">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="bcad9-117">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="bcad9-118">Pvz., filtruokite lauko **Vieta** reikšme **1**.</span><span class="sxs-lookup"><span data-stu-id="bcad9-118">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="bcad9-119">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="bcad9-119">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="bcad9-120">Patikrinkite, ar lauko **Iš viso turima** yra reikšmė yra **411,0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="bcad9-120">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="bcad9-121">Įrašykite užduoties įrašą ir pridėkite jį prie testavimo atvejo, esančio „Azure Devops”.</span><span class="sxs-lookup"><span data-stu-id="bcad9-121">Save the task recording and attach it to your test case in Azure Devops.</span></span>
3. <span data-ttu-id="bcad9-122">Įtraukite tikrinimo atvejį į tikrinimo planą ir įkelkite tikrinimo atvejį į RSAT.</span><span class="sxs-lookup"><span data-stu-id="bcad9-122">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="bcad9-123">Atidarykite „Excel“ parametrų failą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-123">Open the Excel parameter file.</span></span> <span data-ttu-id="bcad9-124">Skirtuke **InventOnhandItem** matysite skiltį **Tikrinti InventOnhandItem**, kurioje pateiktas laukas **Operatorius**.</span><span class="sxs-lookup"><span data-stu-id="bcad9-124">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Laukas Operatorius](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="bcad9-126">Norėdami patikrinti, ar turimos atsargos visada bus didesnės nei 0, pakeiskite lauko **Vertė** reikšmę iš **411** į **0**, o lauko **Operatorius** reikšmę – iš lygybės ženklo (**=**) į ženklą „daugiau nei“ (**\>**).</span><span class="sxs-lookup"><span data-stu-id="bcad9-126">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Pakeistos laukų Vertė ir Operatorius reikšmės](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="bcad9-128">Įrašykite ir uždarykite „Excel“ parametro failą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-128">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="bcad9-129">Pasirinkite **Įkelti**, kad įrašytumėte keitimus, atliktus „Excel“ parametro faile, į „Azure DevOps“.</span><span class="sxs-lookup"><span data-stu-id="bcad9-129">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="bcad9-130">Dabar, jei nurodytos atsargų prekės reikšmė lauke **Iš viso turima** yra didesnė nei 0 (nulis), tikrinimai pavyks, nepriklausomai nuo faktinės turimų atsargų vertės.</span><span class="sxs-lookup"><span data-stu-id="bcad9-130">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="saved-variables-and-chaining-of-test-cases"></a><span data-ttu-id="bcad9-131">Įrašyti kintamieji ir testavimo atvejų sujungimas</span><span class="sxs-lookup"><span data-stu-id="bcad9-131">Saved variables and chaining of test cases</span></span>

<span data-ttu-id="bcad9-132">Viena iš pagrindinių RSAT funkcijų – testavimo atvejų sujungimas, t. y. testavimo galimybė perkelti kintamuosius į kitus testus.</span><span class="sxs-lookup"><span data-stu-id="bcad9-132">One of the key features of RSAT is the chaining of test cases, that is, the ability of a test to pass variables to other tests.</span></span> <span data-ttu-id="bcad9-133">Daugiau informacijos žr. straipsnyje [Kopijuoti kintamuosius į sujungtus testavimo atvejus](../../dev-itpro/perf-test/rsat/rsat-chain-test-cases.md).</span><span class="sxs-lookup"><span data-stu-id="bcad9-133">For more information, see the article [Copy variables to chain test cases](../../dev-itpro/perf-test/rsat/rsat-chain-test-cases.md).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="bcad9-134">Išvesto testo atvejis</span><span class="sxs-lookup"><span data-stu-id="bcad9-134">Derived test case</span></span>

<span data-ttu-id="bcad9-135">RSAT leidžia naudoti tą patį užduoties įrašą su keliais testavimo atvejais, o tai leidžia vykdyti užduotį naudojant skirtingas duomenų konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="bcad9-135">RSAT lets you use the same task recording with multiple test cases, enabling a task to run with different data configurations.</span></span> <span data-ttu-id="bcad9-136">Daugiau informacijos žr. straipsnyje [Išvestiniai testavimo atvejai](../../dev-itpro/perf-test/rsat/rsat-derived-test-cases.md).</span><span class="sxs-lookup"><span data-stu-id="bcad9-136">See the article [Derived test cases](../../dev-itpro/perf-test/rsat/rsat-derived-test-cases.md) for more information.</span></span>

### <a name="validate-notifications-and-messages"></a><span data-ttu-id="bcad9-137">Pranešimų tikrinimas</span><span class="sxs-lookup"><span data-stu-id="bcad9-137">Validate notifications and messages</span></span>

<span data-ttu-id="bcad9-138">Šią funkciją galima naudoti norint patikrinti, ar įvyko veiksmas.</span><span class="sxs-lookup"><span data-stu-id="bcad9-138">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="bcad9-139">Pavyzdžiui, kai sukuriamas, įvertinamas ir pradedamas gamybos užsakymas, programa rodo pranešimą „Gamyba – pradžia“, kad praneštų, jog pradėtas gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="bcad9-139">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Pranešimas Gamyba – pradžia](./media/use_rsa_tool_05.png)

<span data-ttu-id="bcad9-141">Šį pranešimą galite patikrinti naudodami RSAT – įveskite pranešimo tekstą atitinkamo įrašo „Excel“ parametro failo skirtuke **MessageValidation**.</span><span class="sxs-lookup"><span data-stu-id="bcad9-141">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Skirtukas Pranešimo tikrinimas](./media/use_rsa_tool_06.png)

<span data-ttu-id="bcad9-143">Paleidus tikrinimo atvejį, pranešimas „Excel“ parametro faile palyginamas su rodomu pranešimu.</span><span class="sxs-lookup"><span data-stu-id="bcad9-143">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="bcad9-144">Jei pranešimai nesutampa, tikrinimo atvejis nepavyks.</span><span class="sxs-lookup"><span data-stu-id="bcad9-144">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="bcad9-145">„Excel“ parametro failo skirtuke **MessageValidation** galite įvesti daugiau nei vieną pranešimą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-145">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="bcad9-146">Pranešimai taip pat gali būti klaidos arba įspėjantys, o ne informaciniai pranešimai.</span><span class="sxs-lookup"><span data-stu-id="bcad9-146">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="snapshot"></a><span data-ttu-id="bcad9-147">Momentinė kopija</span><span class="sxs-lookup"><span data-stu-id="bcad9-147">Snapshot</span></span>

<span data-ttu-id="bcad9-148">Ši funkcija užfiksuoja veiksmų, kurie buvo atlikti įrašant užduotį, ekrano kopijas.</span><span class="sxs-lookup"><span data-stu-id="bcad9-148">This feature takes screenshots of the steps that were performed during task recording.</span></span> <span data-ttu-id="bcad9-149">Ji naudinga audito arba programinių klaidų taisymo tikslais.</span><span class="sxs-lookup"><span data-stu-id="bcad9-149">It is useful for auditing or debugging purposes.</span></span>

- <span data-ttu-id="bcad9-150">Norėdami naudoti šią funkciją atidarykite failą **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT diegimo aplanke (pvz., **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ir pakeiskite toliau nurodyto elemento reikšmę iš **false** į **true**.</span><span class="sxs-lookup"><span data-stu-id="bcad9-150">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="bcad9-151">Kai vykdote testavimo atvejį, RSAT sugeneruoja veiksmų momentines kopijas (vaizdus), esančias darbo kataloge, testavimo atvejų atkūrimo aplanke.</span><span class="sxs-lookup"><span data-stu-id="bcad9-151">When your run the test case, RSAT will generate snapshots (images) of the steps in the playback folder of the test cases in the working diretory.</span></span> <span data-ttu-id="bcad9-152">Jei naudojate senesnę RSAT versiją, vaizdai įrašomi **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, kiekvienam vykdomam testavimo atvejui sukuriamas atskiras aplankas.</span><span class="sxs-lookup"><span data-stu-id="bcad9-152">If you are using an older version of RSAT, the images are saved to **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

## <a name="assignment"></a><span data-ttu-id="bcad9-153">Priskyrimas</span><span class="sxs-lookup"><span data-stu-id="bcad9-153">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="bcad9-154">Scenarijus</span><span class="sxs-lookup"><span data-stu-id="bcad9-154">Scenario</span></span>

1. <span data-ttu-id="bcad9-155">Produkto dizaino įrankis sukuria naują išleistą produktą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-155">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="bcad9-156">Gamybos vadovas inicijuoja gamybos užsakymą, kad atsargų lygį pakeltų dviem vienetais.</span><span class="sxs-lookup"><span data-stu-id="bcad9-156">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="bcad9-157">Gamyba pradeda ir baigia gamybos užsakymą bei patikrina, ar turimas kiekis yra du vienetai.</span><span class="sxs-lookup"><span data-stu-id="bcad9-157">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="bcad9-158">Pardavimo komanda gauna keturių naujo produkto vienetų užsakymą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-158">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="bcad9-159">Todėl pardavimo komanda atnaujina grynuosius poreikius naudodami dinaminį planą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-159">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="bcad9-160">Kadangi papildomų pajėgumų nėra, numatytoji užsakymo strategija nustatyta kaip „pirkti, o ne gaminti“.</span><span class="sxs-lookup"><span data-stu-id="bcad9-160">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="bcad9-161">Todėl sukuriamas suplanuotas pirkimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="bcad9-161">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="bcad9-162">Pirkėjas įtraukia tiekėją, sutvirtina suplanuotą pirkimo užsakymą, o tada patvirtina pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-162">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="bcad9-163">Kai įsigytos prekės pristatomos į parduotuvę, parduotuvės operatorius ieško susijusio pirkimo užsakymo ir gauna prekes.</span><span class="sxs-lookup"><span data-stu-id="bcad9-163">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="bcad9-164">Kadangi užsakymas yra baigtas, prekes galima paimti ir supakuoti į pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-164">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="bcad9-165">„Finance“ registruoja pirkimo SF ir pardavimo SF.</span><span class="sxs-lookup"><span data-stu-id="bcad9-165">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="bcad9-166">Tolesnėje iliustracijoje vaizduojamas šio scenarijaus srautas.</span><span class="sxs-lookup"><span data-stu-id="bcad9-166">The following illustration shows the flow for this scenario.</span></span>

![Tikrinimo scenarijaus srautas](./media/use_rsa_tool_14.png)

<span data-ttu-id="bcad9-168">Tolesnėje iliustracijoje rodoma šio scenarijaus verslo procesų hierarchija LCS verslo procesų modeliavimo įrankyje.</span><span class="sxs-lookup"><span data-stu-id="bcad9-168">The following illustration shows the business processes hierarchy for this scenario in the LCS Business Process Modeler.</span></span>

![Tikrinimo scenarijaus veiklos procesai](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="bcad9-170">Strategija – pagrindinis mokymasis</span><span class="sxs-lookup"><span data-stu-id="bcad9-170">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="bcad9-171">Duomenys</span><span class="sxs-lookup"><span data-stu-id="bcad9-171">Data</span></span>

- <span data-ttu-id="bcad9-172">Įsitikinkite, kad turite reprezentatyvius duomenis (gamybos / auksinės konfigūracijos duomenų kopiją ir migravo duomenų kopiją).</span><span class="sxs-lookup"><span data-stu-id="bcad9-172">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="bcad9-173">Kai generuojate naujus duomenis naudodami užduočių įrašymo priemonę, sukurkite tikrinimo pavadinimus, kurie derės su esamais pavadinimais (pavyzdžiui, naudokite prefiksą **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="bcad9-173">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="bcad9-174">Naudokite „Azure“ tam tikro laiko atkūrimą, kad iš naujo paleistumėte tikrinimus ne 1 pakopos aplinkose.</span><span class="sxs-lookup"><span data-stu-id="bcad9-174">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="bcad9-175">Nors galite naudoti „Excel“ funkcijas **ATSITIKTINIS** ir **DABAR**, kad sugeneruotumėte unikalų derinį, prireiks gana daug pastangų.</span><span class="sxs-lookup"><span data-stu-id="bcad9-175">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="bcad9-176">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="bcad9-176">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="bcad9-177">Užduoties įrašymo priemonė</span><span class="sxs-lookup"><span data-stu-id="bcad9-177">Task recorder</span></span>

- <span data-ttu-id="bcad9-178">Apibrėžkite scenarijus prieš pradėdami įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bcad9-178">Define scenarios before you start recording.</span></span> <span data-ttu-id="bcad9-179">Gerai valdomas projektas turi iš anksto apibrėžtus tikrinimo scenarijus.</span><span class="sxs-lookup"><span data-stu-id="bcad9-179">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="bcad9-180">Norėdami sukurti tikrinimo atvejį, pagalvokite, kiek nuspėjamas šių tikrinimo scenarijų rezultatas.</span><span class="sxs-lookup"><span data-stu-id="bcad9-180">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="bcad9-181">Išskaidykite įrašus, jei jie atlikti skirtingais vaidmenimis arba jei laukimo laikas ar išorinis įvykis yra prieš kitą veiksmą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-181">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="bcad9-182">Venkite pasirinkti reikšmes sąrašuose.</span><span class="sxs-lookup"><span data-stu-id="bcad9-182">Avoid selecting values in lists.</span></span> <span data-ttu-id="bcad9-183">Vietoje to naudokite teksto formatus, pvz., **FIFO**, **AudioRM** ir **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="bcad9-183">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="bcad9-184">Pasirinkus sąraše, įrašoma sąrašo reikšmės padėtis, o ne pati reikšmė.</span><span class="sxs-lookup"><span data-stu-id="bcad9-184">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="bcad9-185">Jei prekės yra įtrauktos į tą sąrašą, reikšmės padėtis gali pasikeisti.</span><span class="sxs-lookup"><span data-stu-id="bcad9-185">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="bcad9-186">Todėl jūsų įraše bus naudojamas kitoks parametras ir likusi scenarijaus dalis gali būti paveikta.</span><span class="sxs-lookup"><span data-stu-id="bcad9-186">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="bcad9-187">Pagalvokite apie kelių vartotojų elgseną.</span><span class="sxs-lookup"><span data-stu-id="bcad9-187">Think about multi-user behavior.</span></span> <span data-ttu-id="bcad9-188">Pavyzdžiui, nemanykite, kad jūsų naujai sukurtas pardavimo užsakymas visada bus parenkamas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="bcad9-188">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="bcad9-189">Vietoje to visada naudokite filtrą, kad rastumėte tinkamą užsakymą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-189">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="bcad9-190">Norėdami užduočių įrašymo priemonės funkciją Kopijuoti, kad įrašytumėte naujai sukurto produkto pavadinimą ir jį būtų galima naudoti grandininio tikrinimo atvejais.</span><span class="sxs-lookup"><span data-stu-id="bcad9-190">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="bcad9-191">Norėdami nustatyti kontrolės punktus, kurie patikrina, ar veiksmai buvo vykdyti tinkamai, naudokite užduočių įrašymo priemonės funkciją Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="bcad9-191">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="bcad9-192">RSAT</span><span class="sxs-lookup"><span data-stu-id="bcad9-192">RSAT</span></span>

- <span data-ttu-id="bcad9-193">Norėdami vykdyti tikrinimą kitoje įmonėje, galite pakeisti įmonę „Excel“ parametro failo skirtuke **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="bcad9-193">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="bcad9-194">Įsitikinkite, kad parametrai ir duomenys yra prieinami naujai pasirinktoje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="bcad9-194">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="bcad9-195">Galite pakeisti tikrinimo vartotoją „Excel“ parametro failo skirtuke **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="bcad9-195">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="bcad9-196">Nurodykite vartotojo, kuris vykdys tikrinimo atvejį, el. pašto ID.</span><span class="sxs-lookup"><span data-stu-id="bcad9-196">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="bcad9-197">Tokiu būdu tikrinimo atvejį galima vykdyti naudojant nurodyto vartotojo saugos teises.</span><span class="sxs-lookup"><span data-stu-id="bcad9-197">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="bcad9-198">Norėdami palaukti prieš pradėdami tikrinimą, galite nustatyti pauzę „Excel“ parametro failo skirtuke **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="bcad9-198">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="bcad9-199">Ši pauzė gali būti naudojama paketinėje užduotyje (pvz., jei darbo eiga turi būti vykdoma prieš atliekant kitus veiksmus).</span><span class="sxs-lookup"><span data-stu-id="bcad9-199">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="bcad9-200">Išplėstinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="bcad9-200">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="bcad9-201">CLI</span><span class="sxs-lookup"><span data-stu-id="bcad9-201">CLI</span></span>

<span data-ttu-id="bcad9-202">RSAT galima iškviesti lange **Komandinė eilutė** arba **„PowerShell“**.</span><span class="sxs-lookup"><span data-stu-id="bcad9-202">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="bcad9-203">Patikrinkite, ar aplinkos kintamasis **TestRoot** nustatytas kaip RSAT diegimo kelias.</span><span class="sxs-lookup"><span data-stu-id="bcad9-203">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="bcad9-204">(Programoje „Microsoft Windows“ atidarykite **valdymo skydą**, pasirinkite **Sistema ir sauga \> Sistema \> Išplėstiniai sistemos parametrai** ir pasirinkite **Aplinkos kintamieji**.)</span><span class="sxs-lookup"><span data-stu-id="bcad9-204">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="bcad9-205">Atidarykite langą **Komandinė eilutė** arba **„PowerShell“** kaip administratorius.</span><span class="sxs-lookup"><span data-stu-id="bcad9-205">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="bcad9-206">Nueikite į RSAT įdiegimo katalogą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-206">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="bcad9-207">Išvardykite visas komandas.</span><span class="sxs-lookup"><span data-stu-id="bcad9-207">List all commands.</span></span>

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

#### <a name=""></a><span data-ttu-id="bcad9-208">?</span><span class="sxs-lookup"><span data-stu-id="bcad9-208">?</span></span> 
<span data-ttu-id="bcad9-209">Rodoma pagalba apie visas galimas komandas ir jų parametrus.</span><span class="sxs-lookup"><span data-stu-id="bcad9-209">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a><span data-ttu-id="bcad9-210">Neprivalomi parametrai</span><span class="sxs-lookup"><span data-stu-id="bcad9-210">Optional parameters</span></span>

**``command``**


<span data-ttu-id="bcad9-211">Kur ``[command]`` yra viena iš toliau nurodytų komandų.</span><span class="sxs-lookup"><span data-stu-id="bcad9-211">Where ``[command]`` is one of the commands specified below.</span></span>


#### <a name="about"></a><span data-ttu-id="bcad9-212">about</span><span class="sxs-lookup"><span data-stu-id="bcad9-212">about</span></span>
<span data-ttu-id="bcad9-213">Rodoma dabartinė versija.</span><span class="sxs-lookup"><span data-stu-id="bcad9-213">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="bcad9-214">cls</span><span class="sxs-lookup"><span data-stu-id="bcad9-214">cls</span></span>
<span data-ttu-id="bcad9-215">Išvalomas ekranas.</span><span class="sxs-lookup"><span data-stu-id="bcad9-215">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a><span data-ttu-id="bcad9-216">atsisiųsti</span><span class="sxs-lookup"><span data-stu-id="bcad9-216">download</span></span>
<span data-ttu-id="bcad9-217">Į išvesties katalogą atsiunčiami nurodyto testavimo atvejo priedai.</span><span class="sxs-lookup"><span data-stu-id="bcad9-217">Downloads attachments for the specified test case to the output directory.</span></span> <span data-ttu-id="bcad9-218">Norėdami gauti visus galimus testavimo atvejus, galite naudoti komandą ``list``.</span><span class="sxs-lookup"><span data-stu-id="bcad9-218">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="bcad9-219">Kaip **test_case_id** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.</span><span class="sxs-lookup"><span data-stu-id="bcad9-219">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="bcad9-220">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="bcad9-220">Required parameters</span></span>
<span data-ttu-id="bcad9-221">**``test_case_id``** Nurodo testavimo atvejo ID.</span><span class="sxs-lookup"><span data-stu-id="bcad9-221">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="bcad9-222">**``output_dir``** Nurodo išvesties katalogą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-222">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="bcad9-223">Katalogas privalo būti.</span><span class="sxs-lookup"><span data-stu-id="bcad9-223">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="bcad9-224">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="bcad9-224">Examples</span></span>

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a><span data-ttu-id="bcad9-225">redaguoti</span><span class="sxs-lookup"><span data-stu-id="bcad9-225">edit</span></span>
<span data-ttu-id="bcad9-226">Leidžia programoje „Excel“ atverti parametrų failą ir jį redaguoti.</span><span class="sxs-lookup"><span data-stu-id="bcad9-226">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="bcad9-227">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="bcad9-227">Required parameters</span></span>
<span data-ttu-id="bcad9-228">**``excel_file``** Turi būti nurodytas visas esamo „Excel“ failo kelias.</span><span class="sxs-lookup"><span data-stu-id="bcad9-228">**``excel_file``** Must contain a full path to an existing Excel file.</span></span>

##### <a name="examples"></a><span data-ttu-id="bcad9-229">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="bcad9-229">Examples</span></span>
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a><span data-ttu-id="bcad9-230">generate</span><span class="sxs-lookup"><span data-stu-id="bcad9-230">generate</span></span>
<span data-ttu-id="bcad9-231">Išvesties kataloge sugeneruojami nurodyto testavimo atvejo testavimo vykdymo ir parametrų failai.</span><span class="sxs-lookup"><span data-stu-id="bcad9-231">Generates test execution and parameter files for the specified test case in the output directory.</span></span>
<span data-ttu-id="bcad9-232">Norėdami gauti visus galimus testavimo atvejus, galite naudoti komandą ``list``.</span><span class="sxs-lookup"><span data-stu-id="bcad9-232">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="bcad9-233">Kaip **test_case_id** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.</span><span class="sxs-lookup"><span data-stu-id="bcad9-233">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="bcad9-234">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="bcad9-234">Required parameters</span></span>
<span data-ttu-id="bcad9-235">**``test_case_id``** Nurodo testavimo atvejo ID.</span><span class="sxs-lookup"><span data-stu-id="bcad9-235">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="bcad9-236">**``output_dir``** Nurodo išvesties katalogą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-236">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="bcad9-237">Katalogas privalo būti.</span><span class="sxs-lookup"><span data-stu-id="bcad9-237">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="bcad9-238">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="bcad9-238">Examples</span></span>
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a><span data-ttu-id="bcad9-239">generatederived</span><span class="sxs-lookup"><span data-stu-id="bcad9-239">generatederived</span></span>
<span data-ttu-id="bcad9-240">Sugeneruojamas naujas testavimo atvejis, išvestas iš pateikto testavimo atvejo.</span><span class="sxs-lookup"><span data-stu-id="bcad9-240">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="bcad9-241">Norėdami gauti visus galimus testavimo atvejus, galite naudoti komandą ``list``.</span><span class="sxs-lookup"><span data-stu-id="bcad9-241">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="bcad9-242">Kaip **test_case_id** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.</span><span class="sxs-lookup"><span data-stu-id="bcad9-242">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a><span data-ttu-id="bcad9-243">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="bcad9-243">Required parameters</span></span>
<span data-ttu-id="bcad9-244">**``parent_test_case_id``** Nurodo pirminio testavimo atvejo ID.</span><span class="sxs-lookup"><span data-stu-id="bcad9-244">**``parent_test_case_id``** Represents the parent test case ID.</span></span>  
<span data-ttu-id="bcad9-245">**``test_plan_id``** Nurodo testavimo plano ID.</span><span class="sxs-lookup"><span data-stu-id="bcad9-245">**``test_plan_id``** Represents the test plan ID.</span></span>  
<span data-ttu-id="bcad9-246">**``test_suite_id``** Nurodo testavimo paketo ID.</span><span class="sxs-lookup"><span data-stu-id="bcad9-246">**``test_suite_id``** Represents the test suite ID.</span></span>

##### <a name="examples"></a><span data-ttu-id="bcad9-247">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="bcad9-247">Examples</span></span>
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a><span data-ttu-id="bcad9-248">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="bcad9-248">generatetestonly</span></span>
<span data-ttu-id="bcad9-249">Išvesties kataloge sugeneruojamas tik nurodyto testavimo atvejo testavimo vykdymo failas.</span><span class="sxs-lookup"><span data-stu-id="bcad9-249">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="bcad9-250">Norėdami gauti visus galimus testavimo atvejus, galite naudoti komandą ``list``.</span><span class="sxs-lookup"><span data-stu-id="bcad9-250">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="bcad9-251">Kaip **test_case_id** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.</span><span class="sxs-lookup"><span data-stu-id="bcad9-251">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="bcad9-252">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="bcad9-252">Required parameters</span></span>
<span data-ttu-id="bcad9-253">**``test_case_id``** Nurodo testavimo atvejo ID.</span><span class="sxs-lookup"><span data-stu-id="bcad9-253">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="bcad9-254">**``output_dir``** Nurodo išvesties katalogą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-254">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="bcad9-255">Katalogas privalo būti.</span><span class="sxs-lookup"><span data-stu-id="bcad9-255">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="bcad9-256">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="bcad9-256">Examples</span></span>
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a><span data-ttu-id="bcad9-257">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="bcad9-257">generatetestsuite</span></span>
<span data-ttu-id="bcad9-258">Išvesties kataloge sugeneruojami visi nurodyto paketo testavimo atvejai.</span><span class="sxs-lookup"><span data-stu-id="bcad9-258">Generates all test cases for the specified suite in the output directory.</span></span>
<span data-ttu-id="bcad9-259">Norėdami gauti visus galimus testavimo paketus, galite naudoti komandą ``listtestsuitenames``.</span><span class="sxs-lookup"><span data-stu-id="bcad9-259">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="bcad9-260">Kaip **test_suite_name** parametrą naudokite bet kokią vertę iš stulpelio.</span><span class="sxs-lookup"><span data-stu-id="bcad9-260">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="bcad9-261">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="bcad9-261">Required parameters</span></span>
<span data-ttu-id="bcad9-262">**``test_suite_name``** Nurodo testavimo paketo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-262">**``test_suite_name``** Represents the test suite name.</span></span>  
<span data-ttu-id="bcad9-263">**``output_dir``** Nurodo išvesties katalogą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-263">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="bcad9-264">Katalogas privalo būti.</span><span class="sxs-lookup"><span data-stu-id="bcad9-264">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="bcad9-265">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="bcad9-265">Examples</span></span>
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a><span data-ttu-id="bcad9-266">help</span><span class="sxs-lookup"><span data-stu-id="bcad9-266">help</span></span>
<span data-ttu-id="bcad9-267">Identiška elementui [?](#section)</span><span class="sxs-lookup"><span data-stu-id="bcad9-267">Identical to the [?](#section)</span></span> <span data-ttu-id="bcad9-268">command</span><span class="sxs-lookup"><span data-stu-id="bcad9-268">command</span></span>


#### <a name="list"></a><span data-ttu-id="bcad9-269">sąrašas</span><span class="sxs-lookup"><span data-stu-id="bcad9-269">list</span></span>
<span data-ttu-id="bcad9-270">Išvardijami visi galimi testavimo atvejai.</span><span class="sxs-lookup"><span data-stu-id="bcad9-270">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a><span data-ttu-id="bcad9-271">listtestplans</span><span class="sxs-lookup"><span data-stu-id="bcad9-271">listtestplans</span></span>
<span data-ttu-id="bcad9-272">Išvardijami visi galimi testavimo planai.</span><span class="sxs-lookup"><span data-stu-id="bcad9-272">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a><span data-ttu-id="bcad9-273">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="bcad9-273">listtestsuite</span></span>
<span data-ttu-id="bcad9-274">Išvardijami nurodyto testavimo paketo testavimo atvejai.</span><span class="sxs-lookup"><span data-stu-id="bcad9-274">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="bcad9-275">Norėdami gauti visus galimus testavimo paketus, galite naudoti komandą ``listtestsuitenames``.</span><span class="sxs-lookup"><span data-stu-id="bcad9-275">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="bcad9-276">Kaip **suite_name** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.</span><span class="sxs-lookup"><span data-stu-id="bcad9-276">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="bcad9-277">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="bcad9-277">Required parameters</span></span>
<span data-ttu-id="bcad9-278">**``suite_name``** Norimo paketo pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="bcad9-278">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="bcad9-279">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="bcad9-279">Examples</span></span>
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a><span data-ttu-id="bcad9-280">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="bcad9-280">listtestsuitenames</span></span>
<span data-ttu-id="bcad9-281">Išvardijami visi galimi testavimo paketai.</span><span class="sxs-lookup"><span data-stu-id="bcad9-281">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a><span data-ttu-id="bcad9-282">playback</span><span class="sxs-lookup"><span data-stu-id="bcad9-282">playback</span></span>
<span data-ttu-id="bcad9-283">Atkuriamas testavimo atvejis naudojant „Excel“ failą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-283">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="bcad9-284">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="bcad9-284">Required parameters</span></span>
<span data-ttu-id="bcad9-285">**``excel_file``** Visas kelias iki „Excel“ failo.</span><span class="sxs-lookup"><span data-stu-id="bcad9-285">**``excel_file``** A full path to the Excel file.</span></span> <span data-ttu-id="bcad9-286">Failas privalo būti.</span><span class="sxs-lookup"><span data-stu-id="bcad9-286">File must exist.</span></span> 

##### <a name="examples"></a><span data-ttu-id="bcad9-287">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="bcad9-287">Examples</span></span>
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a><span data-ttu-id="bcad9-288">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="bcad9-288">playbackbyid</span></span>
<span data-ttu-id="bcad9-289">Vienu metu atkuriami keli testavimo atvejai.</span><span class="sxs-lookup"><span data-stu-id="bcad9-289">Plays back multiple test cases at once.</span></span>
<span data-ttu-id="bcad9-290">Norėdami gauti visus galimus testavimo atvejus, galite naudoti komandą ``list``.</span><span class="sxs-lookup"><span data-stu-id="bcad9-290">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="bcad9-291">Kaip **test_case_id** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.</span><span class="sxs-lookup"><span data-stu-id="bcad9-291">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a><span data-ttu-id="bcad9-292">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="bcad9-292">Required parameters</span></span>
<span data-ttu-id="bcad9-293">**``test_case_id1``** Esamo testavimo atvejo ID.</span><span class="sxs-lookup"><span data-stu-id="bcad9-293">**``test_case_id1``** ID of exisiting test case.</span></span>  
<span data-ttu-id="bcad9-294">**``test_case_id2``** Esamo testavimo atvejo ID.</span><span class="sxs-lookup"><span data-stu-id="bcad9-294">**``test_case_id2``** ID of exisiting test case.</span></span>  
<span data-ttu-id="bcad9-295">**``test_case_idN``** Esamo testavimo atvejo ID.</span><span class="sxs-lookup"><span data-stu-id="bcad9-295">**``test_case_idN``** ID of exisiting test case.</span></span>  

##### <a name="examples"></a><span data-ttu-id="bcad9-296">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="bcad9-296">Examples</span></span>
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a><span data-ttu-id="bcad9-297">playbackmany</span><span class="sxs-lookup"><span data-stu-id="bcad9-297">playbackmany</span></span>
<span data-ttu-id="bcad9-298">Naudojant „Excel“ failus vienu metu atkuriama daug testavimo atvejų.</span><span class="sxs-lookup"><span data-stu-id="bcad9-298">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a><span data-ttu-id="bcad9-299">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="bcad9-299">Required parameters</span></span>
<span data-ttu-id="bcad9-300">**``excel_file1``** Visas kelias iki „Excel“ failo.</span><span class="sxs-lookup"><span data-stu-id="bcad9-300">**``excel_file1``** Full path to the Excel file.</span></span> <span data-ttu-id="bcad9-301">Failas privalo būti.</span><span class="sxs-lookup"><span data-stu-id="bcad9-301">File must exist.</span></span>  
<span data-ttu-id="bcad9-302">**``excel_file2``** Visas kelias iki „Excel“ failo.</span><span class="sxs-lookup"><span data-stu-id="bcad9-302">**``excel_file2``** Full path to the Excel file.</span></span> <span data-ttu-id="bcad9-303">Failas privalo būti.</span><span class="sxs-lookup"><span data-stu-id="bcad9-303">File must exist.</span></span>  
<span data-ttu-id="bcad9-304">**``excel_fileN``** Visas kelias iki „Excel“ failo.</span><span class="sxs-lookup"><span data-stu-id="bcad9-304">**``excel_fileN``** Full path to the Excel file.</span></span> <span data-ttu-id="bcad9-305">Failas privalo būti.</span><span class="sxs-lookup"><span data-stu-id="bcad9-305">File must exist.</span></span>  

##### <a name="examples"></a><span data-ttu-id="bcad9-306">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="bcad9-306">Examples</span></span>
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a><span data-ttu-id="bcad9-307">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="bcad9-307">playbacksuite</span></span>
<span data-ttu-id="bcad9-308">Atkuriami visi testavimo atvejai iš nurodyto testavimo paketo.</span><span class="sxs-lookup"><span data-stu-id="bcad9-308">Plays back all test cases from the specified test suite.</span></span> <span data-ttu-id="bcad9-309">Norėdami gauti visus galimus testavimo paketus, galite naudoti komandą ``listtestsuitenames``.</span><span class="sxs-lookup"><span data-stu-id="bcad9-309">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="bcad9-310">Kaip **suite_name** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.</span><span class="sxs-lookup"><span data-stu-id="bcad9-310">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="bcad9-311">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="bcad9-311">Required parameters</span></span>
<span data-ttu-id="bcad9-312">**``suite_name``** Norimo paketo pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="bcad9-312">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="bcad9-313">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="bcad9-313">Examples</span></span>
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a><span data-ttu-id="bcad9-314">quit</span><span class="sxs-lookup"><span data-stu-id="bcad9-314">quit</span></span>
<span data-ttu-id="bcad9-315">Uždaroma programa.</span><span class="sxs-lookup"><span data-stu-id="bcad9-315">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a><span data-ttu-id="bcad9-316">upload</span><span class="sxs-lookup"><span data-stu-id="bcad9-316">upload</span></span>
<span data-ttu-id="bcad9-317">Nusiunčiami visi nurodyto testavimo paketo ar testavimo atvejų failai.</span><span class="sxs-lookup"><span data-stu-id="bcad9-317">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a><span data-ttu-id="bcad9-318">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="bcad9-318">Required parameters</span></span>
<span data-ttu-id="bcad9-319">**``suite_name``** Bus nusiųsti visi nurodyto testavimo paketo failai.</span><span class="sxs-lookup"><span data-stu-id="bcad9-319">**``suite_name``** All files belonging to the specified test suite will be uploaded.</span></span>
<span data-ttu-id="bcad9-320">**``testcase_id``** Bus nusiųsti visi nurodyto (-ų) testavimo atvejo (-ų) failai.</span><span class="sxs-lookup"><span data-stu-id="bcad9-320">**``testcase_id``** All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="bcad9-321">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="bcad9-321">Examples</span></span>
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a><span data-ttu-id="bcad9-322">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="bcad9-322">uploadrecording</span></span>
<span data-ttu-id="bcad9-323">Nusiunčiamas tik nurodytų testavimo atvejų įrašo failas.</span><span class="sxs-lookup"><span data-stu-id="bcad9-323">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a><span data-ttu-id="bcad9-324">Būtini parametrai</span><span class="sxs-lookup"><span data-stu-id="bcad9-324">Required parameters</span></span>
<span data-ttu-id="bcad9-325">**``testcase_id``** Bus nusiųstas nurodytų testavimo atvejų įrašo failas.</span><span class="sxs-lookup"><span data-stu-id="bcad9-325">**``testcase_id``** Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="bcad9-326">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="bcad9-326">Examples</span></span>
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a><span data-ttu-id="bcad9-327">usage</span><span class="sxs-lookup"><span data-stu-id="bcad9-327">usage</span></span>
<span data-ttu-id="bcad9-328">Rodomi du būdai, kaip iškviesti šią programą: naudojant numatytąjį parametrų failą arba pateikiant parametrų failą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-328">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a><span data-ttu-id="bcad9-329">„Windows PowerShell“ pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="bcad9-329">Windows PowerShell examples</span></span>

[!IMPORTANT] <span data-ttu-id="bcad9-330">Toliau nurodyti pavyzdiniai scenarijai yra pateikiami iliustravimo tikslais ir nėra palaikomi „Microsoft”.</span><span class="sxs-lookup"><span data-stu-id="bcad9-330">The example scripts below are provided AS IS for illustration purposes and are not supported by Microsoft.</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="bcad9-331">Tikrinimo atvejo vykdymas cikle</span><span class="sxs-lookup"><span data-stu-id="bcad9-331">Run a test case in a loop</span></span>

<span data-ttu-id="bcad9-332">Turite tikrinimo scenarijų, kuris sukuria naują klientą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-332">You have a test script that creates a new customer.</span></span> <span data-ttu-id="bcad9-333">Naudojant scenarijų šis tikrinimo atvejis gali būti vykdomas ciklu, nustatant toliau nurodytų duomenų atsitiktinumą prie kiekvieno pakartojimo vykdymą.</span><span class="sxs-lookup"><span data-stu-id="bcad9-333">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="bcad9-334">Kliento ID</span><span class="sxs-lookup"><span data-stu-id="bcad9-334">Customer ID</span></span>
- <span data-ttu-id="bcad9-335">Kliento pavadinimas</span><span class="sxs-lookup"><span data-stu-id="bcad9-335">Customer name</span></span>
- <span data-ttu-id="bcad9-336">Kliento adresas</span><span class="sxs-lookup"><span data-stu-id="bcad9-336">Customer address</span></span>

<span data-ttu-id="bcad9-337">Kliento ID formatas bus *ATCUS\<number\>*, kur \<number\> yra reikšmė nuo **000000001** iki **999999999**.</span><span class="sxs-lookup"><span data-stu-id="bcad9-337">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="bcad9-338">Tolesnis pavyzdys naudoja vieną parametrą, **pradžia**, kad apibrėžtų pirmą naudojamą skaičių.</span><span class="sxs-lookup"><span data-stu-id="bcad9-338">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="bcad9-339">Jis naudoja antrą parametrą, **Nr.**, kad apibrėžtų klientų, kurie turi būti sukurti, skaičių.</span><span class="sxs-lookup"><span data-stu-id="bcad9-339">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="bcad9-340">Kiekvieno pakartojimo metu „Excel“ parametro failo parametrai pakeičiami naudojant funkciją UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="bcad9-340">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="bcad9-341">Tada RSAT komandinė eilutė iškviečiama funkcijoje RunTestCase.</span><span class="sxs-lookup"><span data-stu-id="bcad9-341">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="bcad9-342">Atidarykite „Microsoft Windows PowerShell Integrated Scripting Environment“ (ISE) administratorius režimu ir įklijuokite toliau nurodytą kodą į langą, pavadintą **Untitled1.ps1.**</span><span class="sxs-lookup"><span data-stu-id="bcad9-342">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

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
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="bcad9-343">Vykdykite scenarijų, kuris priklauso nuo duomenų „Microsoft Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="bcad9-343">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="bcad9-344">Toliau pateiktame pavyzdyje naudojamas „Open Data Protocol“ („OData“) iškvietimas, kad būtų galima rasti pirkimo užsakymo būseną.</span><span class="sxs-lookup"><span data-stu-id="bcad9-344">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="bcad9-345">Jei būsena nėra **išrašyta SF**, galite, pavyzdžiui, iškviesti RSAT tikrinimo atvejį, kuris užregistruos SF.</span><span class="sxs-lookup"><span data-stu-id="bcad9-345">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

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
