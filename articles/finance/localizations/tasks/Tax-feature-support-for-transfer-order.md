---
title: Mokesčių funkcijų palaikymos operacijų užsakymams
description: Šioje temoje paaiškinama naujos mokesčių priemonės perkėlimo užsakymų palaikymas naudojant mokesčių skaičiavimo tarnybą.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d1b99046b0e439c9dadbb240050e270a7b2a6914
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920960"
---
# <a name="tax-feature-support-for-transfer-orders"></a><span data-ttu-id="d8cda-103">Mokesčių funkcijų palaikymos operacijų užsakymams</span><span class="sxs-lookup"><span data-stu-id="d8cda-103">Tax feature support for transfer orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d8cda-104">Šioje temoje pateikiama informacija apie mokesčių skaičiavimą ir registravimo integravimą perkėlimo užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="d8cda-104">This topic provides information about tax calculation and posting integration in transfer orders.</span></span> <span data-ttu-id="d8cda-105">Ši funkcija leidžia nustatyti mokesčių skaičiavimą ir registravimą atsargų perkėlimo užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="d8cda-105">This functionality lets you set up tax calculation and posting in transfer orders for stock transfers.</span></span> <span data-ttu-id="d8cda-106">Pagal Europos Sąjungos (ES) pridėtinės vertės mokesčio (PVM) nuostatus, atsargų perkėlimas laikomas vidiniu bendrijos tiekimu ir įsigijimais bendrijos viduje.</span><span class="sxs-lookup"><span data-stu-id="d8cda-106">Under European Union (EU) value-added tax (VAT) regulations, stock transfers are considered intra-community supply and intra-community acquisitions.</span></span>

<span data-ttu-id="d8cda-107">Norėdami konfigūruoti ir naudoti šią funkciją, turite atlikti tris pagrindinius veiksmus:</span><span class="sxs-lookup"><span data-stu-id="d8cda-107">To configure and use this functionality, you must complete three main steps:</span></span>

1. <span data-ttu-id="d8cda-108">**RCS nustatymas: reguliavimo konfigūravimo tarnybose nustatykite mokesčių funkciją, mokesčių kodus ir mokesčių kodų taikomumą mokesčių** kodo nustatymui perkėlimo užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="d8cda-108">**RCS setup:** In Regulatory Configuration Service, set up the tax feature, tax codes, and tax codes applicability for tax code determination in transfer orders.</span></span>
2. <span data-ttu-id="d8cda-109">**„Finance“ nustatymas:** „Microsoft Dynamics 365 Finance“, įjunkite **Mokesčių operacijų užsakymas** funkcija, nustatykite mokesčių paslaugų parametrus inventoriui ir nustatykite pagrindinius mokesčių parametrus/</span><span class="sxs-lookup"><span data-stu-id="d8cda-109">**Finance setup:** In Microsoft Dynamics 365 Finance, turn on the **Tax in transfer order** feature, set up the tax service parameters for inventory, and set up core tax parameters.</span></span>
3. <span data-ttu-id="d8cda-110">**Atsargų nustatymas:** nustatykite perkėlimo užsakymo operacijų atsargų konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="d8cda-110">**Inventory setup:** Set up the inventory configuration for transfer order transactions.</span></span>

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a><span data-ttu-id="d8cda-111">Nustatyti mokesčių ir perkėlimo užsakymo operacijų RCS</span><span class="sxs-lookup"><span data-stu-id="d8cda-111">Set up RCS for tax and transfer order transactions</span></span>

<span data-ttu-id="d8cda-112">Norėdami nustatyti su perkėlimo užsakymu susijusių mokesčių, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d8cda-112">Follow these steps to set up the tax that is involved in a transfer order.</span></span> <span data-ttu-id="d8cda-113">Pavyzdyje, kuris rodomas čia, perkėlimo užsakymas iš Olandijos į Belgiją.</span><span class="sxs-lookup"><span data-stu-id="d8cda-113">In the example that is shown here, the transfer order is from the Netherlands to Belgium.</span></span>

1. <span data-ttu-id="d8cda-114">Mokesčių priemonių **puslapyje**, skirtuke **Versijos**, pasirinkite juodraščio priemonės versiją, tada pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-114">On the **Tax features** page, on the **Versions** tab, select the draft feature version, and then select **Edit**.</span></span>

    ![Redagavimo pasirinkimas](../media/image1.png)

2. <span data-ttu-id="d8cda-116">Mokesčių priemonių **nustatymo** puslapyje, skirtuke **Mokesčių** kodai, pasirinkite Įtraukti, **kad** sukurtumėte naujus mokesčių kodus.</span><span class="sxs-lookup"><span data-stu-id="d8cda-116">On the **Tax features setup** page, on the **Tax codes** tab, select **Add** to create new tax codes.</span></span> <span data-ttu-id="d8cda-117">Pavyzdžiui, sukurti trys mokesčių kodai: **NL-atleidimas,** **„BE-RC-21“** ir **„BE-RC+21“**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-117">For this example, three tax codes are created: **NL-Exempt**, **BE-RC-21**, and **BE-RC+21**.</span></span>

    - <span data-ttu-id="d8cda-118">Kai perkėlimo užsakymas siunčiamas iš Olandijos sandėlio, taikomas Olandijos PVM neapmokestinimo **kodas** (NL-Exempt).</span><span class="sxs-lookup"><span data-stu-id="d8cda-118">When a transfer order is shipped from a warehouse in the Netherlands, the Netherlands VAT exempted tax code (**NL-Exempt**) is applied.</span></span>
      
        <span data-ttu-id="d8cda-119">Kurti mokesčio kodą **NL neapmokestinama**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-119">Create the tax code **NL-Exempt**.</span></span>
        1. <span data-ttu-id="d8cda-120">Pasirinkite **Pridėti**, įveskite **NL-atleidimas** PVM kodo **lauke**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-120">Select **Add**, enter **NL-Exempt** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="d8cda-121">Pasirinkite **pagal grynąją** sumą mokesčio **komponento** lauke.</span><span class="sxs-lookup"><span data-stu-id="d8cda-121">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="d8cda-122">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-122">Select **Save**.</span></span>
        4. <span data-ttu-id="d8cda-123">Pasirinkite **Įtraukti** **Reitingavimo** lentelėje.</span><span class="sxs-lookup"><span data-stu-id="d8cda-123">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="d8cda-124">Swtich **yra** neapmokestinama į **Taip** **bendrajame** skyriuje.</span><span class="sxs-lookup"><span data-stu-id="d8cda-124">Swtich **Is Exempt** to **Yes** in the **General** section.</span></span>

        ![NL neapmokestinimo mokesčio kodas](../media/image2.png)

    - <span data-ttu-id="d8cda-126">Kai perkėlimo užsakymas gaunamas Belgijos sandėlyje, atvirkštinio apmokestinimo mechanizmas taikomas naudojant **„BE-RC-21“ ir** **„BE-RC+21“** mokesčių kodus.</span><span class="sxs-lookup"><span data-stu-id="d8cda-126">When a transfer order is received at a Belgium warehouse, the reverse charge mechanism is applied by using the **BE-RC-21** and **BE-RC+21** tax codes.</span></span>
        
        <span data-ttu-id="d8cda-127">Sukurkite mokesčio kodą **„BE-RC-21“**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-127">Create the tax code **BE-RC-21**.</span></span>      
        1. <span data-ttu-id="d8cda-128">Pasirinkite **Pridėti**, įveskite **„BE-RC-21“** PVM kodo **lauke**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-128">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="d8cda-129">Pasirinkite **pagal grynąją** sumą mokesčio **komponento** lauke.</span><span class="sxs-lookup"><span data-stu-id="d8cda-129">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="d8cda-130">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-130">Select **Save**.</span></span>
        4. <span data-ttu-id="d8cda-131">Pasirinkite **Įtraukti** **Reitingavimo** lentelėje.</span><span class="sxs-lookup"><span data-stu-id="d8cda-131">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="d8cda-132">Įveskite **-21** į mokesčio tarifo **lauką**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-132">Enter **-21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="d8cda-133">Swtich **yra atvirkštinis apmokestinimas** į **Taip** **bendrajame** skyriuje.</span><span class="sxs-lookup"><span data-stu-id="d8cda-133">Swtich **Is Reverse Charge** to **Yes** in the **General** section.</span></span>
        7. <span data-ttu-id="d8cda-134">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-134">Select **Save**.</span></span>

        ![BE-RC-21 mokesčių kodas, skirtas atvirkštinei mokesčių operacijai](../media/image3.png)
        
        <span data-ttu-id="d8cda-136">Sukurkite mokesčio kodą **„BE-RC+21“**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-136">Create the tax code **BE-RC+21**.</span></span>
        1. <span data-ttu-id="d8cda-137">Pasirinkite **Pridėti**, įveskite **„BE-RC-21“** PVM kodo **lauke**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-137">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="d8cda-138">Pasirinkite **pagal grynąją** sumą mokesčio **komponento** lauke.</span><span class="sxs-lookup"><span data-stu-id="d8cda-138">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="d8cda-139">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-139">Select **Save**.</span></span>
        4. <span data-ttu-id="d8cda-140">Pasirinkite **Įtraukti** **Reitingavimo** lentelėje.</span><span class="sxs-lookup"><span data-stu-id="d8cda-140">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="d8cda-141">Įveskite **21** į mokesčio tarifo **lauką**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-141">Enter **21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="d8cda-142">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-142">Select **Save**.</span></span>

        ![BE-RC+21 mokesčių kodas, skirtas atvirkštinei mokesčių operacijai](../media/image4.png)

3. <span data-ttu-id="d8cda-144">Nustatykite mokesčių kodų taikomumą.</span><span class="sxs-lookup"><span data-stu-id="d8cda-144">Define the applicability of the tax codes.</span></span>

    1. <span data-ttu-id="d8cda-145">Pasirinkite **Tvarkyti** stulpelius, tada pasirinkite stulpelius, kurie turėtų būti naudojami kuriant taikomumo lentelę.</span><span class="sxs-lookup"><span data-stu-id="d8cda-145">Select **Manage columns**, and then select columns that should be used to build the applicability table.</span></span>

        > [!NOTE]
        > <span data-ttu-id="d8cda-146">Būtinai įtraukite verslo **proceso ir** mokesčių **krypčių stulpelius į** lentelę.</span><span class="sxs-lookup"><span data-stu-id="d8cda-146">Be sure to add the **Business process** and **Tax directions** columns to the table.</span></span> <span data-ttu-id="d8cda-147">Abu stulpeliai yra labai svarbūs perkėlimo užsakymų mokesčių funkcijai.</span><span class="sxs-lookup"><span data-stu-id="d8cda-147">Both columns are essential to the functionality for tax in transfer orders.</span></span>

    2. <span data-ttu-id="d8cda-148">Taikyti taikomas taisykles.</span><span class="sxs-lookup"><span data-stu-id="d8cda-148">Add applicability rules.</span></span> <span data-ttu-id="d8cda-149">Neužpildyti **mokesčių** kodų, **mokesčių grupės ir prekių mokesčių grupės laukų palikti** **tuščius**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-149">Don't leave the **Tax codes**, **Tax group**, and **Item tax group** fields blank.</span></span>
        
        <span data-ttu-id="d8cda-150">Įtraukite naują perkėlimo užsakymo siuntimo taisyklę.</span><span class="sxs-lookup"><span data-stu-id="d8cda-150">Add a new rule for transfer order shipment.</span></span>
        1. <span data-ttu-id="d8cda-151">Pasirinkite **Įtraukti** **Taikomos taisyklės** lentelėje.</span><span class="sxs-lookup"><span data-stu-id="d8cda-151">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="d8cda-152">Verslo proceso **lauke pasirinkite** **Atsargos, kad taisyklė būtų taikoma perkėlimo** užsakymui.</span><span class="sxs-lookup"><span data-stu-id="d8cda-152">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="d8cda-153">Lauke **Siuntimo iš šalies/** regiono įveskite **„NLD“**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-153">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="d8cda-154">Lauke **Siuntimo į šalies/** regiono įveskite **„BEL“**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-154">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="d8cda-155">Mokesčių krypties **lauke pasirinkite** Išvestis, **kad taisyklė būtų taikoma perkėlimo užsakymo** siuntai.</span><span class="sxs-lookup"><span data-stu-id="d8cda-155">In the **Tax direction** field, select **Output** to make the rule applicable to transfer order shipment.</span></span>
        6. <span data-ttu-id="d8cda-156">Laukelyje **Mokesčių kodai** rinkitės **NL-neapmokestinama**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-156">In the **Tax codes** field, select **NL-Exempt**.</span></span>
        7. <span data-ttu-id="d8cda-157">Laukuose Mokesčių grupė ir Prekių mokesčių grupė įveskite susijusią PVM grupę ir prekės PVM **grupę** **apibrėžtą** jūsų finansų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="d8cda-157">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>
        
        <span data-ttu-id="d8cda-158">Įtraukite kitą perkėlimo užsakymo gavimo taisyklę.</span><span class="sxs-lookup"><span data-stu-id="d8cda-158">Add another rule for transfer order receipt.</span></span>
        1. <span data-ttu-id="d8cda-159">Pasirinkite **Įtraukti** **Taikomos taisyklės** lentelėje.</span><span class="sxs-lookup"><span data-stu-id="d8cda-159">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="d8cda-160">Verslo proceso **lauke pasirinkite** **Atsargos, kad taisyklė būtų taikoma perkėlimo** užsakymui.</span><span class="sxs-lookup"><span data-stu-id="d8cda-160">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="d8cda-161">Lauke **Siuntimo iš šalies/** regiono įveskite **„NLD“**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-161">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="d8cda-162">Lauke **Siuntimo į šalies/** regiono įveskite **„BEL“**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-162">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="d8cda-163">Mokesčių krypties **lauke pasirinkite** Įvestis, **kad taisyklė būtų taikoma perkėlimo užsakymo** gavimai.</span><span class="sxs-lookup"><span data-stu-id="d8cda-163">In the **Tax direction** field, select **Input** to make the rule applicable to transfer order receipt.</span></span>
        6. <span data-ttu-id="d8cda-164">Mokesčių **kodų** lauke pasirinkite **„BE-RC+21“** ir **„BE-RC-21“**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-164">In the **Tax codes** field, select **BE-RC+21** and **BE-RC-21**.</span></span>
        7. <span data-ttu-id="d8cda-165">Laukuose Mokesčių grupė ir Prekių mokesčių grupė įveskite susijusią PVM grupę ir prekės PVM **grupę** **apibrėžtą** jūsų finansų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="d8cda-165">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>

        ![Taikymo taisyklės](../media/image5.png)

4. <span data-ttu-id="d8cda-167">Užpildykite ir publikuokite naują mokesčių priemonės versiją.</span><span class="sxs-lookup"><span data-stu-id="d8cda-167">Complete and publish the new tax feature version.</span></span>

    <span data-ttu-id="d8cda-168">[![Naujos versijos būsenos keitimas](../media/image6.png)](../media/image6.png)</span><span class="sxs-lookup"><span data-stu-id="d8cda-168">[![Changing the status of the new version](../media/image6.png)](../media/image6.png)</span></span>

## <a name="set-up-finance-for-transfer-order-transactions"></a><span data-ttu-id="d8cda-169">Nustatyti „Finance“ ir perkėlimo užsakymo operacijas</span><span class="sxs-lookup"><span data-stu-id="d8cda-169">Set up Finance for transfer order transactions</span></span>

<span data-ttu-id="d8cda-170">Atlikite šiuos žingsnius, kad įjungtumėte ir nustatytumėte mokesčius operacijų užsakymams.</span><span class="sxs-lookup"><span data-stu-id="d8cda-170">Follow these steps to enable and set up taxes for transfer orders.</span></span>

1. <span data-ttu-id="d8cda-171">„Finance“ eikite į **Darbo sritis** \> **Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-171">In Finance, go to **Workspaces** \> **Feature management**.</span></span>
2. <span data-ttu-id="d8cda-172">Sąraše raskite ir pasirinkite mokestį perkėlimo užsakymo priemonėje, tada, norėdami **jį įjungti** **pasirinkite Įgalinti** dabar.</span><span class="sxs-lookup"><span data-stu-id="d8cda-172">In the list, find and select the **Tax in transfer order** feature, and then select **Enable now** to turn it on.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="d8cda-173">Perkėlimo **užsakymo mokesčio priemonė visiškai priklauso nuo mokesčių** tarnybos.</span><span class="sxs-lookup"><span data-stu-id="d8cda-173">The **Tax in transfer order** feature is fully dependent on the tax service.</span></span> <span data-ttu-id="d8cda-174">Todėl jį galima įjungti tik įdiegus mokesčių paslaugą.</span><span class="sxs-lookup"><span data-stu-id="d8cda-174">Therefore, it can be turned on only after you've installed the tax service.</span></span>

    ![Mokesčiai operacijų užsakymo funkcijoje](../media/image7.png)

3. <span data-ttu-id="d8cda-176">Įjunkite mokesčių paslaugą ir pasirinkite **atsargų** verslo procesą.</span><span class="sxs-lookup"><span data-stu-id="d8cda-176">Enable the tax service, and select the **Inventory** business process.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="d8cda-177">Turite atlikti šį žingsnį su kiekvienu finansų juridiniu subjektu, kur norite, kad būtų galima naudoti mokesčių paslaugą ir perkėlimo užsakymų mokesčių funkciją.</span><span class="sxs-lookup"><span data-stu-id="d8cda-177">You must complete this step for each legal entity in Finance where you want the tax service and the functionality for tax in transfer orders to be available.</span></span>

    1. <span data-ttu-id="d8cda-178">Eikite **į Mokesčių nustatymo** \> **mokesčių** \> **konfigūracijos** \> **mokesčių tarnybos nustatymą**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-178">Go to **Tax** \> **Setup** \> **Tax configuration** \> **Tax service setup**.</span></span>
    2. <span data-ttu-id="d8cda-179">Verslo **proceso lauke** pasirinkite **Atsargos**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-179">In the **Business process** field, select **Inventory**.</span></span>

    ![Verslo proceso lauko nustatymas](../media/image8.png)

4. <span data-ttu-id="d8cda-181">Patikrinkite, ar nustatytas atvirkštinio apmokestinimo mechanizmas.</span><span class="sxs-lookup"><span data-stu-id="d8cda-181">Verify that the reverse charge mechanism is set up.</span></span> <span data-ttu-id="d8cda-182">Eikite į DK nustatymo parametrus, tada skirtuke Atvirkštinis apmokestinimas patikrinkite, **ar** \> **nustatyta** \> **parinktis** **Įgalinti** **atvirkštinį apmokestinimą kaip** **Taip**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-182">Go to **General ledger** \> **Setup** \> **Parameters**, and then, on the **Reverse charge** tab, verify that the **Enable reverse charge** option is set to **Yes**.</span></span>

    ![Įjungti atvirkštinio apmokestinimo parinktį](../media/image9.png)

5. <span data-ttu-id="d8cda-184">Patikrinkite, ar susiję mokesčių kodai, mokesčių grupės, prekių mokesčių grupės ir PVM registracijos numeriai nustatyti finansuose pagal mokesčių tarnybos nurodymus.</span><span class="sxs-lookup"><span data-stu-id="d8cda-184">Verify that the related tax codes, tax groups, item tax groups, and VAT registration numbers have been set up in Finance according to the tax service guidance.</span></span>
6. <span data-ttu-id="d8cda-185">Nustatyti tarpinę tarpinę sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="d8cda-185">Set up an interim transit account.</span></span> <span data-ttu-id="d8cda-186">Šio veiksmo reikia atlikti tik tada, kai perkėlimo užsakymui taikomas mokestis nėra taikomas pvm mokėjimo arba atvirkštinio apmokestinimo mechanizmui.</span><span class="sxs-lookup"><span data-stu-id="d8cda-186">This step is required only when the tax that is applied to a transfer order isn't applicable to a tax exempted or reverse charge mechanism.</span></span>

    1. <span data-ttu-id="d8cda-187">Eikite į **Mokesčiai** \> **Nustatymas** \> **Pardavimo mokesčiai** \> **DK registravimo grupės**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-187">Go to **Tax** \> **Setup** \> **Sales tax** \> **Ledger posting groups**.</span></span>
    2. <span data-ttu-id="d8cda-188">Lauke **Tarpinis tranzitas** pasirinkite DK sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="d8cda-188">In the **Interim transit** field, select a ledger account.</span></span>

    ![Pasirinkti tarpinę tarpinę sąskaitą](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a><span data-ttu-id="d8cda-190">Nustatyti pagrindines atsargas perkėlimo užsakymo operacijoms</span><span class="sxs-lookup"><span data-stu-id="d8cda-190">Set up basic inventory for transfer order transactions</span></span>

<span data-ttu-id="d8cda-191">Norėdami nustatyti pagrindines atsargas perkėlimo užsakymo operacijoms įgalinti, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d8cda-191">Follow these steps to set up basic inventory to enable transfer order transactions.</span></span>

1. <span data-ttu-id="d8cda-192">Kurkite siuntimo iš ir siuntimo vietas savo sandėliams skirtingose šalyse ar regionuose ir pridėkite kiekvienos teritorijos pagrindinį adresą.</span><span class="sxs-lookup"><span data-stu-id="d8cda-192">Create ship-from and ship-to sites for your warehouses in different countries or regions, and add the primary address for each site.</span></span>

    1. <span data-ttu-id="d8cda-193">Eikite į **Sandėlio valdymas** \> **Sąranka** \> **Sandėlis** \> **Saitai**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-193">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Sites**.</span></span>
    2. <span data-ttu-id="d8cda-194">Pasirinkite **Nauja**, jei norite sukurti svetainę, kurią priskirsite sandėliui vėliau.</span><span class="sxs-lookup"><span data-stu-id="d8cda-194">Select **New** to create the site that you will assign to a warehouse later.</span></span>
    3. <span data-ttu-id="d8cda-195">Visoms kitoms svetainėms, kurias turite sukurti, atlikite 2 veiksmą.</span><span class="sxs-lookup"><span data-stu-id="d8cda-195">Repeat step 2 for all the other sites that you must create.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d8cda-196">Viena iš jūsų sukurtų teritorijų turi būti vadinama **tranzitu**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-196">One of the sites that you create should be named **Transit**.</span></span> <span data-ttu-id="d8cda-197">Vėlesniais šios procedūros veiksmais šią teritoriją priskirsite tranzito sandėliui, kad su mokesčiais susijusius atsargų kvitus būtų galima registruoti perkėlimo užsakymų operacijose „Siųsti" ir „Gauti".</span><span class="sxs-lookup"><span data-stu-id="d8cda-197">In later steps of this procedure, you will assign this site to the transit warehouse, so that tax-related inventory vouchers can be posted in "ship" and "receive" transactions for transfer orders.</span></span> <span data-ttu-id="d8cda-198">Tranzito vietos adresas nesusijęs su mokesčių apskaičiavimu.</span><span class="sxs-lookup"><span data-stu-id="d8cda-198">The address of the transit site is irrelevant to tax calculation.</span></span> <span data-ttu-id="d8cda-199">Dėl to, galite palikti jį tuščią.</span><span class="sxs-lookup"><span data-stu-id="d8cda-199">Therefore, you can leave it blank.</span></span>

    ![Saitų nustatymas](../media/image11.png)

2. <span data-ttu-id="d8cda-201">Kurti siuntimo iš, tranzito ir siuntimo sandėlius.</span><span class="sxs-lookup"><span data-stu-id="d8cda-201">Create ship-from, transit, and ship-to warehouses.</span></span> <span data-ttu-id="d8cda-202">Apskaičiuojant mokesčius bet kokia sandėlyje tvarkoma adreso informacija perrašys svetainės adresą.</span><span class="sxs-lookup"><span data-stu-id="d8cda-202">Any address information that is maintained in a warehouse will override the site address during tax calculation.</span></span>

    1. <span data-ttu-id="d8cda-203">Eikite į **Sandėlio valdymas** \> **Sąranka** \> **Sandėlis** \> **Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-203">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Warehouses**.</span></span>
    2. <span data-ttu-id="d8cda-204">Pasirinkite **Nauja**, jei norite sukurti svetainę ir priskirkite ją atitinkamam saitui.</span><span class="sxs-lookup"><span data-stu-id="d8cda-204">Select **New** to create a warehouse, and assign it to the corresponding site.</span></span>
    3. <span data-ttu-id="d8cda-205">Norėdami kiekvienai vietai sukurti sandėlį, pakartokite 2 veiksmą.</span><span class="sxs-lookup"><span data-stu-id="d8cda-205">Repeat step 2 to create a warehouse for each site as required.</span></span>

    ![Sandėlių nustatymas](../media/image12.png)

    > [!NOTE]
    > <span data-ttu-id="d8cda-207">Perkėlimo užsakymo operacijoms atlikti lauke Tranzito sandėlis turi būti pasirinktas siuntimo iš **sandėlio** sandėlio laukas.</span><span class="sxs-lookup"><span data-stu-id="d8cda-207">For a ship-from warehouse, a transit warehouse must be selected in the **Transit warehouse** field for transfer order transactions.</span></span>
    >
    > ![Tranzito sandėlio pasirinkimas](../media/image13.png)

3. <span data-ttu-id="d8cda-209">Patvirtinkite, ar atsargų publikavimo konfigūravimas yra nustatytas perlaidos užsakymo operacijoms.</span><span class="sxs-lookup"><span data-stu-id="d8cda-209">Verify that the inventory posting configuration is set up for transfer order transactions.</span></span>

    1. <span data-ttu-id="d8cda-210">Eikite į **Atsargų valdymas** \> **Sąranka** \> **Registravimas** \> **Registravimas**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-210">Go to **Inventory management** \> **Setup** \> **Posting** \> **Posting**.</span></span>
    2. <span data-ttu-id="d8cda-211">Skirtuke Atsargos patikrinkite, ar nustatyta DK **sąskaita atsargų** išdavimui ir atsargų **gavimo** **registravimui**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-211">On the **Inventory** tab, verify that a ledger account is set up for both **Inventory issue** and **Inventory receipt** posting.</span></span>

        ![Atsargų išdavimo ir atsargų gavimo registravimo nustatymas](../media/image14.png)

    3. <span data-ttu-id="d8cda-213">Patikrinkite, ar DK sąskaita nustatyta mokėtinų **sumų registravimui tarp vienetų**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-213">Verify that a ledger account is set up for **Inter-unit payable** posting.</span></span>

        ![Mokėtinų sumų registravimo tarp vienetų nustatymas](../media/image15.png)

    4. <span data-ttu-id="d8cda-215">Patikrinkite, ar DK sąskaita nustatyta mokėtinų **sumų publikavimui tarp gaunamų sumų**.</span><span class="sxs-lookup"><span data-stu-id="d8cda-215">Verify that a ledger account is set up for **Inter-unit receivable** posting.</span></span>

        ![Tarpinių gaunamų sumų publikavimo nustatymas](../media/image16.png)
