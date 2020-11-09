---
title: „Common Data Service“ virtualių objektų konfigūravimas
description: Šioje temoje aprašyta, kaip konfigūruoti „Dynamics 365 Human Resources“ virtualius objektus. Generuokite ir atnaujinkite esamus virtualius objektus, taip pat analizuokite sugeneruotus ir prieinamus objektus.
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0d6f79ea569a7a9b0d25e73e8666bf9ba19095d0
ms.sourcegitcommit: a8665c47696028d371cdc4671db1fd8fcf9e1088
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/21/2020
ms.locfileid: "4058159"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="cae8a-104">„Common Data Service“ virtualių objektų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="cae8a-104">Configure Common Data Service virtual entities</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="cae8a-105">„Dynamics 365 Human Resources“ yra „Common Data Service“ virtualus duomenų šaltinis.</span><span class="sxs-lookup"><span data-stu-id="cae8a-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="cae8a-106">Jis leidžia atlikti visas kūrimo, skaitymo, atnaujinimo ir naikinimo (CRUD) operacijas naudojantis „Common Data Service“ ir „Microsoft Power Platform“.</span><span class="sxs-lookup"><span data-stu-id="cae8a-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="cae8a-107">Virtualių objektų duomenys yra saugomi ne „Common Data Service“, bet programos duomenų bazėje.</span><span class="sxs-lookup"><span data-stu-id="cae8a-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="cae8a-108">Norėdami, kad CRUD operacijas su „Human Resources“ objektais būtų galima atlikti naudojantis „Common Data Service“, turite padaryti, kad objektai „Common Data Service“ būtų prieinami kaip virtualūs objektai.</span><span class="sxs-lookup"><span data-stu-id="cae8a-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="cae8a-109">Tai leis jums atlikti CRUD operacijas su „Human Resources“ duomenimis naudojantis „Common Data Service“ ir „Microsoft Power Platform“.</span><span class="sxs-lookup"><span data-stu-id="cae8a-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="cae8a-110">Operacijos taip pat palaiko „Human Resources“ visos verslo logikos patvirtinimą, siekiant užtikrinti duomenų vientisumą, kai į objektus rašomi duomenys.</span><span class="sxs-lookup"><span data-stu-id="cae8a-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="cae8a-111">Prieinami „Human Resources“ virtualūs objektai</span><span class="sxs-lookup"><span data-stu-id="cae8a-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="cae8a-112">Visi „Open Data Protocol“ („OData“) objektai, esantys „Human Resources“, yra prieinami kaip virtualūs objektai „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="cae8a-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="cae8a-113">Jie taip pat yra prieinami „Power Platform“.</span><span class="sxs-lookup"><span data-stu-id="cae8a-113">They're also available in Power Platform.</span></span> <span data-ttu-id="cae8a-114">Dabar galite kurti programas ir patirtis naudodami duomenis tiesiogiai iš „Human Resources“ kartu su visomis CRUD galimybėmis ir nekopijuodami bei nesinchronizuodami duomenų su „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="cae8a-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="cae8a-115">Norėdami kurti išorines svetaines, kurios leidžia įgyvendinti bendradarbiavimo scenarijus vykdant „Human Resources“ verslo procesus, galite naudoti „Power Apps“ portalus.</span><span class="sxs-lookup"><span data-stu-id="cae8a-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="cae8a-116">Galite peržiūrėti aplinkoje įjungtų virtualių objektų sąrašą ir pradėti dirbti su subjektais [„Power Apps“](https://make.powerapps.com), naudodami sprendimą **Dynamics 365 HR Virtual Entities**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![„Dynamics 365 HR“ virtualūs objektai, esantys „Power Apps“](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="cae8a-118">Virtualūs objektai ir natūralūs objektai</span><span class="sxs-lookup"><span data-stu-id="cae8a-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="cae8a-119">Virtualūs objektai, skirti „Human Resources“, nėra tokie patys kaip natūralūs „Common Data Service“ objektai, sukurti „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="cae8a-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="cae8a-120">Natūralūs „Human Resources“ objektai generuojami atskirai ir yra tvarkomi „Common Data Service“ „HCM Common“ sprendimo.</span><span class="sxs-lookup"><span data-stu-id="cae8a-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="cae8a-121">Dirbant su natūraliais objektais, duomenys saugomi „Common Data Service“ ir turi būti sinchronizuoti su „Human Resources“ programos duomenų baze.</span><span class="sxs-lookup"><span data-stu-id="cae8a-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="cae8a-122">Natūralių „Common Data Service“ objektų, skirtų „Human Resources“, sąrašą žr. [„Common Data Service“ objektai](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="cae8a-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="cae8a-123">Sąranka</span><span class="sxs-lookup"><span data-stu-id="cae8a-123">Setup</span></span>

<span data-ttu-id="cae8a-124">Atlikite šiuos nustatymo veiksmus, kad įjungtumėte virtualius objektus savo aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="cae8a-124">Follow these setup steps to enable virtual entities in your environment.</span></span> 

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="cae8a-125">Užregistruokite programą „Microsoft Azure“</span><span class="sxs-lookup"><span data-stu-id="cae8a-125">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="cae8a-126">Pirmiausia turite užregistruoti programą „Azure“ portale, kad „Microsoft“ tapatumo platforma galėtų teikti autentifikavimo ir autorizavimo paslaugas programai ir vartotojams.</span><span class="sxs-lookup"><span data-stu-id="cae8a-126">First, you need to register the app in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="cae8a-127">Daugiau informacijos apie tai, kaip užregistruoti programas „Azure“, žr. [„Quickstart“: programos registravimas naudojant „Microsoft“ tapatumo platformą](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="cae8a-127">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="cae8a-128">Atidarykite [„Microsoft Azure“ portalą](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="cae8a-128">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="cae8a-129">„Azure“ paslaugų sąraše pasirinkite **Programų registracijos**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-129">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="cae8a-130">Pasirinkite **Nauja registracija**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-130">Select **New registration**.</span></span>

4. <span data-ttu-id="cae8a-131">Lauke **Pavadinimas** įveskite apibūdinantį programos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="cae8a-131">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="cae8a-132">Pavyzdžiui, „ **Dynamics 365 Human Resources“ virtualūs objektai**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-132">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="cae8a-133">Lauke **Nukreipimo URI** įveskite „Human Resources“ objekto vardų srities URL.</span><span class="sxs-lookup"><span data-stu-id="cae8a-133">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="cae8a-134">Pasirinkite **Registruotis**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-134">Select **Register**.</span></span>

7. <span data-ttu-id="cae8a-135">Baigus registraciją, „Azure“ portale rodoma programos registracijos sritis **Apžvalga** , kurioje nurodytas **Programos (kliento) ID**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-135">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="cae8a-136">Pasižymėkite **Programos (kliento) ID**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-136">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="cae8a-137">Šią informaciją turėsite įvesti, kai vykdysite [virtualaus objekto duomenų šaltinio konfigūravimą](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="cae8a-137">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="cae8a-138">Kairiojoje naršymo srityje pasirinkite **Sertifikatai ir slaptieji raktai**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-138">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="cae8a-139">Puslapio srityje **Kliento slaptieji raktai** pasirinkite **Naujas kliento slaptasis raktas**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-139">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="cae8a-140">Pateikite aprašymą, pasirinkite trukmę ir pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-140">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="cae8a-141">Pasižymėkite slaptojo rakto vertę.</span><span class="sxs-lookup"><span data-stu-id="cae8a-141">Record the secret's value.</span></span> <span data-ttu-id="cae8a-142">Šią informaciją turėsite įvesti, kai vykdysite [virtualaus objekto duomenų šaltinio konfigūravimą](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="cae8a-142">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="cae8a-143">Šiuo metu būtinai išsisaugokite slaptojo rakto vertę.</span><span class="sxs-lookup"><span data-stu-id="cae8a-143">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="cae8a-144">Palikus šį puslapį, slaptasis raktas daugiau niekada nebus rodomas.</span><span class="sxs-lookup"><span data-stu-id="cae8a-144">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="cae8a-145">Įdiekite „Dynamics 365 HR Virtual Entity“ programą</span><span class="sxs-lookup"><span data-stu-id="cae8a-145">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="cae8a-146">Įdiekite „Dynamics 365 HR Virtual Entity“ programą savo „Power Apps“ aplinkoje, kad įdiegtumėte virtualaus objekto sprendimo paketą „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="cae8a-146">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="cae8a-147">Atidarykite [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="cae8a-147">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="cae8a-148">Sąraše **Aplinkos** pasirinkite „Power Apps“ aplinką, susijusią su „Human Resources“ egzemplioriumi.</span><span class="sxs-lookup"><span data-stu-id="cae8a-148">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="cae8a-149">Puslapio srityje **Ištekliai** pasirinkite **„Dynamics 365“ programos**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-149">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="cae8a-150">Pasirinkite veiksmą **Įdiegti programą**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-150">Select the **Install app** action.</span></span>

5. <span data-ttu-id="cae8a-151">Pasirinkite **Dynamics 365 HR Virtual Entity** , o tada pasirinkite **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-151">Select **Dynamics 365 HR Virtual Entity** , and select **Next**.</span></span>

6. <span data-ttu-id="cae8a-152">Peržiūrėkite ir pažymėkite, kad sutinkate su paslaugų teikimo sąlygomis.</span><span class="sxs-lookup"><span data-stu-id="cae8a-152">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="cae8a-153">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-153">Select **Install**.</span></span>

<span data-ttu-id="cae8a-154">Diegimas trunka kelias minutes.</span><span class="sxs-lookup"><span data-stu-id="cae8a-154">The install takes a few minutes.</span></span> <span data-ttu-id="cae8a-155">Baigus, pereikite prie tolesnių veiksmų.</span><span class="sxs-lookup"><span data-stu-id="cae8a-155">When it completes, continue to the next steps.</span></span>

![Įdiekite „Dynamics 365 HR Virtual Entity“ programą iš „Power Platform“ administravimo centro](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="cae8a-157">Sukonfigūruokite virtualaus objekto duomenų šaltinį</span><span class="sxs-lookup"><span data-stu-id="cae8a-157">Configure the virtual entity data source</span></span> 

<span data-ttu-id="cae8a-158">Kitas veiksmas yra sukonfigūruoti virtualaus objekto duomenų šaltinį „Power Apps“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="cae8a-158">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="cae8a-159">Atidarykite [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="cae8a-159">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="cae8a-160">Sąraše **Aplinkos** pasirinkite „Power Apps“ aplinką, susijusią su „Human Resources“ egzemplioriumi.</span><span class="sxs-lookup"><span data-stu-id="cae8a-160">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="cae8a-161">Puslapio srityje **Informacija** pasirinkite **Aplinkos URL**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-161">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="cae8a-162">Srityje **Spendimo būklės telkinys** pasirinkite piktogramą **Išplėstinė paieška** , esančią programos viršutiniame dešiniajame kampe.</span><span class="sxs-lookup"><span data-stu-id="cae8a-162">In the **Solution Health Hub** , select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="cae8a-163">Puslapyje **Išplėstinė paieška** , išskleidžiamajame sąraše **Ieškoti** , pasirinkite „ **Finance and Operations“ virtualaus duomenų šaltinio konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-163">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="cae8a-164">Pasirinkite **Rezultatai**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-164">Select **Results**.</span></span>

7. <span data-ttu-id="cae8a-165">Pasirinkite įrašą **„Microsoft“ HR duomenų šaltinis**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-165">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="cae8a-166">Įveskite reikiamą duomenų šaltinio konfigūracijos informaciją.</span><span class="sxs-lookup"><span data-stu-id="cae8a-166">Enter the required information for the data source configuration.</span></span>

   - <span data-ttu-id="cae8a-167">**Paskirties URL** : jūsų „Human Resources“ vardų srities URL.</span><span class="sxs-lookup"><span data-stu-id="cae8a-167">**Target URL** : The URL of your Human Resources namespace.</span></span>
   - <span data-ttu-id="cae8a-168">**Nuomotojo ID** : „Azure Active Directory“ („Azure AD“) nuomotojo ID.</span><span class="sxs-lookup"><span data-stu-id="cae8a-168">**Tenant ID** : The Azure Active Directory (Azure AD) tenant ID.</span></span>
   - <span data-ttu-id="cae8a-169">**AAD programos ID** : programos (kliento) ID, sukurtas programai, užregistruotai „Microsoft Azure“ portale.</span><span class="sxs-lookup"><span data-stu-id="cae8a-169">**AAD Application ID** : The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="cae8a-170">Šią informaciją gavote anksčiau, atlikdami veiksmą [Užregistruokite programą „Microsoft Azure“](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="cae8a-170">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>
   - <span data-ttu-id="cae8a-171">**AAD programos slaptasis raktas** : kliento slaptasis raktas, sukurtas programai, užregistruotai „Microsoft Azure“ portale.</span><span class="sxs-lookup"><span data-stu-id="cae8a-171">**AAD Application Secret** : The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="cae8a-172">Šią informaciją gavote anksčiau, atlikdami veiksmą [Užregistruokite programą „Microsoft Azure“](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="cae8a-172">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

9. <span data-ttu-id="cae8a-173">Pasirinkite **Įrašyti ir uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-173">Select **Save & Close**.</span></span>

   ![„Microsoft“ HR duomenų šaltinis](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="cae8a-175">Suteikite programos teises „Human Resources“</span><span class="sxs-lookup"><span data-stu-id="cae8a-175">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="cae8a-176">„Human Resources“ suteikite teises dviem „Azure AD“ programoms:</span><span class="sxs-lookup"><span data-stu-id="cae8a-176">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="cae8a-177">Programai, sukurtai jūsų nuomotojui „Microsoft Azure“ portale</span><span class="sxs-lookup"><span data-stu-id="cae8a-177">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="cae8a-178">„Dynamics 365 HR Virtual Entity“ programai, įdiegtai „Power Apps“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="cae8a-178">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="cae8a-179">„Human Resources“ atidarykite puslapį **„Azure Active Directory“ programos**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-179">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="cae8a-180">Pasirinkite **Nauja** , kad sukurtumėte naują programos įrašą:</span><span class="sxs-lookup"><span data-stu-id="cae8a-180">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="cae8a-181">Lauke **Kliento ID** įveskite programos, kurią užregistravote „Microsoft Azure“ portale, kliento ID.</span><span class="sxs-lookup"><span data-stu-id="cae8a-181">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="cae8a-182">Lauke **Pavadinimas** įveskite programos, kurią užregistravote „Microsoft Azure“ portale, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="cae8a-182">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="cae8a-183">Lauke **Vartotojo ID** pasirinkite vartotojo, kuriam suteiktos „Human Resources“ ir „Power Apps“ aplinkos administravimo teisės, vartotojo ID.</span><span class="sxs-lookup"><span data-stu-id="cae8a-183">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="cae8a-184">Pasirinkite **Nauja** , kad sukurtumėte antrą programos įrašą:</span><span class="sxs-lookup"><span data-stu-id="cae8a-184">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="cae8a-185">**Kliento ID** : f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="cae8a-185">**Client Id** : f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="cae8a-186">**Pavadinimas** : Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="cae8a-186">**Name** : Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="cae8a-187">Lauke **Vartotojo ID** pasirinkite vartotojo, kuriam suteiktos „Human Resources“ ir „Power Apps“ aplinkos administravimo teisės, vartotojo ID.</span><span class="sxs-lookup"><span data-stu-id="cae8a-187">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="cae8a-188">Generuokite virtualius objektus</span><span class="sxs-lookup"><span data-stu-id="cae8a-188">Generate virtual entities</span></span>

<span data-ttu-id="cae8a-189">Baigus nustatymą, galite pasirinkti virtualius objektus, kuriuos norite generuoti ir įjungti savo „Common Data Service“ egzemplioriuje.</span><span class="sxs-lookup"><span data-stu-id="cae8a-189">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="cae8a-190">„Human Resources“ atidarykite puslapį **„Common Data Service“ (CDS) integravimas**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-190">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="cae8a-191">Pasirinkite skirtuką **Virtualūs objektai**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-191">Select the **Virtual entities** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="cae8a-192">Perjungiklis **Įgalinti virtualų objektą** bus automatiškai nustatytas į **Taip** , baigus visus būtinus nustatymus.</span><span class="sxs-lookup"><span data-stu-id="cae8a-192">The **Enable the virtual entity** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="cae8a-193">Jei perjungiklis nustatytas į **Ne** , peržiūrėkite ankstesniuose šio dokumento skyriuose aprašytus veiksmus, norėdami užtikrinti, kad visi būtinieji nustatymo veiksmai yra baigti.</span><span class="sxs-lookup"><span data-stu-id="cae8a-193">If the toggle is set to **No** , review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="cae8a-194">Pasirinkti objektą ar objektus, kuriuos norite generuoti „Common Data Service”.</span><span class="sxs-lookup"><span data-stu-id="cae8a-194">Select the entity or entities you want to generate in Common Data Service.</span></span>

4. <span data-ttu-id="cae8a-195">Pasirinkite **Generuoti / atnaujinti**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-195">Select **Generate/refresh**.</span></span>

![„Common Data Service“ integravimas](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a><span data-ttu-id="cae8a-197">Objekto generavimo būsenos tikrinimas</span><span class="sxs-lookup"><span data-stu-id="cae8a-197">Check entity generation status</span></span>

<span data-ttu-id="cae8a-198">Virtualūs objektai generuojami „Common Data Service” naudojant asinchroninį fone vykstantį procesą.</span><span class="sxs-lookup"><span data-stu-id="cae8a-198">Virtual entities are generated in Common Data Service through an asynchronous background process.</span></span> <span data-ttu-id="cae8a-199">Proceso atnaujinimai rodomi veiksmų centre.</span><span class="sxs-lookup"><span data-stu-id="cae8a-199">Updates on the process display in the action center.</span></span> <span data-ttu-id="cae8a-200">Išsami informacija apie procesą, įskaitant klaidos žurnalus, rodoma puslapyje **Proceso automatizavimai**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-200">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="cae8a-201">„Human Resources“ atidarykite puslapį **Proceso automatizavimai**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-201">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="cae8a-202">Pasirinkite skirtuką **Fone vykstantys procesai**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-202">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="cae8a-203">Pasirinkite **Virtualaus objekto apklausos asinchroninės operacijos fone vykstantį procesą**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-203">Select **Virtual entity poll async operation background process**.</span></span>

4. <span data-ttu-id="cae8a-204">Pasirinkite **Peržiūrėti naujausius rezultatus**.</span><span class="sxs-lookup"><span data-stu-id="cae8a-204">Select **View most recent results**.</span></span>

<span data-ttu-id="cae8a-205">Išslenkančioje srityje rodomi naujausi proceso vykdymo rezultatai.</span><span class="sxs-lookup"><span data-stu-id="cae8a-205">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="cae8a-206">Galite peržiūrėti proceso žurnalą, įskaitant visas iš „Common Data Service” grąžintas klaidas.</span><span class="sxs-lookup"><span data-stu-id="cae8a-206">You can view the log for the process, including any errors returned from Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="cae8a-207">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="cae8a-207">See also</span></span>

[<span data-ttu-id="cae8a-208">Kas yra „Common Data Service“?</span><span class="sxs-lookup"><span data-stu-id="cae8a-208">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="cae8a-209">Objekto apžvalga</span><span class="sxs-lookup"><span data-stu-id="cae8a-209">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="cae8a-210">Objekto ryšių apžvalga</span><span class="sxs-lookup"><span data-stu-id="cae8a-210">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="cae8a-211">Kurti ir redaguoti virtualius objektus, kuriuose yra duomenų iš išorinio duomenų šaltinio</span><span class="sxs-lookup"><span data-stu-id="cae8a-211">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="cae8a-212">Kas yra „Power Apps“ portalai?</span><span class="sxs-lookup"><span data-stu-id="cae8a-212">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="cae8a-213">Programų kūrimo „Power Apps“ apžvalga</span><span class="sxs-lookup"><span data-stu-id="cae8a-213">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
