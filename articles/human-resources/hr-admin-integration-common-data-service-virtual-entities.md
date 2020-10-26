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
ms.openlocfilehash: 0848b7556100fba38fcab0aa2a1a109e2e055fc9
ms.sourcegitcommit: b89baab13e530b5b1f079231619c628309a4742d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/05/2020
ms.locfileid: "3959580"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="20950-104">„Common Data Service“ virtualių objektų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="20950-104">Configure Common Data Service virtual entities</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="20950-105">„Dynamics 365 Human Resources“ yra „Common Data Service“ virtualus duomenų šaltinis.</span><span class="sxs-lookup"><span data-stu-id="20950-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="20950-106">Jis leidžia atlikti visas kūrimo, skaitymo, atnaujinimo ir naikinimo (CRUD) operacijas naudojantis „Common Data Service“ ir „Microsoft Power Platform“.</span><span class="sxs-lookup"><span data-stu-id="20950-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="20950-107">Virtualių objektų duomenys yra saugomi ne „Common Data Service“, bet programos duomenų bazėje.</span><span class="sxs-lookup"><span data-stu-id="20950-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="20950-108">Norėdami, kad CRUD operacijas su „Human Resources“ objektais būtų galima atlikti naudojantis „Common Data Service“, turite padaryti, kad objektai „Common Data Service“ būtų prieinami kaip virtualūs objektai.</span><span class="sxs-lookup"><span data-stu-id="20950-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="20950-109">Tai leis jums atlikti CRUD operacijas su „Human Resources“ duomenimis naudojantis „Common Data Service“ ir „Microsoft Power Platform“.</span><span class="sxs-lookup"><span data-stu-id="20950-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="20950-110">Operacijos taip pat palaiko „Human Resources“ visos verslo logikos patvirtinimą, siekiant užtikrinti duomenų vientisumą, kai į objektus rašomi duomenys.</span><span class="sxs-lookup"><span data-stu-id="20950-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="20950-111">Prieinami „Human Resources“ virtualūs objektai</span><span class="sxs-lookup"><span data-stu-id="20950-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="20950-112">Visi „Open Data Protocol“ („OData“) objektai, esantys „Human Resources“, yra prieinami kaip virtualūs objektai „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="20950-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="20950-113">Jie taip pat yra prieinami „Power Platform“.</span><span class="sxs-lookup"><span data-stu-id="20950-113">They're also available in Power Platform.</span></span> <span data-ttu-id="20950-114">Dabar galite kurti programas ir patirtis naudodami duomenis tiesiogiai iš „Human Resources“ kartu su visomis CRUD galimybėmis ir nekopijuodami bei nesinchronizuodami duomenų su „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="20950-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="20950-115">Norėdami kurti išorines svetaines, kurios leidžia įgyvendinti bendradarbiavimo scenarijus vykdant „Human Resources“ verslo procesus, galite naudoti „Power Apps“ portalus.</span><span class="sxs-lookup"><span data-stu-id="20950-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="20950-116">Galite peržiūrėti aplinkoje įjungtų virtualių objektų sąrašą ir pradėti dirbti su subjektais [„Power Apps“](https://make.powerapps.com), naudodami sprendimą **Dynamics 365 HR Virtual Entities**.</span><span class="sxs-lookup"><span data-stu-id="20950-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![„Dynamics 365 HR“ virtualūs objektai, esantys „Power Apps“](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="20950-118">Virtualūs objektai ir natūralūs objektai</span><span class="sxs-lookup"><span data-stu-id="20950-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="20950-119">Virtualūs objektai, skirti „Human Resources“, nėra tokie patys kaip natūralūs „Common Data Service“ objektai, sukurti „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="20950-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="20950-120">Natūralūs „Human Resources“ objektai generuojami atskirai ir yra tvarkomi „Common Data Service“ „HCM Common“ sprendimo.</span><span class="sxs-lookup"><span data-stu-id="20950-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="20950-121">Dirbant su natūraliais objektais, duomenys saugomi „Common Data Service“ ir turi būti sinchronizuoti su „Human Resources“ programos duomenų baze.</span><span class="sxs-lookup"><span data-stu-id="20950-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="20950-122">Natūralių „Common Data Service“ objektų, skirtų „Human Resources“, sąrašą žr. [„Common Data Service“ objektai](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="20950-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="20950-123">Sąranka</span><span class="sxs-lookup"><span data-stu-id="20950-123">Setup</span></span>

<span data-ttu-id="20950-124">Atlikite šiuos nustatymo veiksmus, kad įjungtumėte virtualius objektus savo aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="20950-124">Follow these setup steps to enable virtual entities in your environment.</span></span> 

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="20950-125">Užregistruokite programą „Microsoft Azure“</span><span class="sxs-lookup"><span data-stu-id="20950-125">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="20950-126">Pirmiausia turite užregistruoti programą „Azure“ portale, kad „Microsoft“ tapatumo platforma galėtų teikti autentifikavimo ir autorizavimo paslaugas programai ir vartotojams.</span><span class="sxs-lookup"><span data-stu-id="20950-126">First, you need to register the app in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="20950-127">Daugiau informacijos apie tai, kaip užregistruoti programas „Azure“, žr. [„Quickstart“: programos registravimas naudojant „Microsoft“ tapatumo platformą](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="20950-127">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="20950-128">Atidarykite [„Microsoft Azure“ portalą](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="20950-128">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="20950-129">„Azure“ paslaugų sąraše pasirinkite **Programų registracijos**.</span><span class="sxs-lookup"><span data-stu-id="20950-129">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="20950-130">Pasirinkite **Nauja registracija**.</span><span class="sxs-lookup"><span data-stu-id="20950-130">Select **New registration**.</span></span>

4. <span data-ttu-id="20950-131">Lauke **Pavadinimas** įveskite apibūdinantį programos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="20950-131">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="20950-132">Pavyzdžiui, „**Dynamics 365 Human Resources“ virtualūs objektai**.</span><span class="sxs-lookup"><span data-stu-id="20950-132">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="20950-133">Lauke **Nukreipimo URI** įveskite „Human Resources“ objekto vardų srities URL.</span><span class="sxs-lookup"><span data-stu-id="20950-133">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="20950-134">Pasirinkite **Registruotis**.</span><span class="sxs-lookup"><span data-stu-id="20950-134">Select **Register**.</span></span>

7. <span data-ttu-id="20950-135">Baigus registraciją, „Azure“ portale rodoma programos registracijos sritis **Apžvalga**, kurioje nurodytas **Programos (kliento) ID**.</span><span class="sxs-lookup"><span data-stu-id="20950-135">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="20950-136">Pasižymėkite **Programos (kliento) ID**.</span><span class="sxs-lookup"><span data-stu-id="20950-136">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="20950-137">Šią informaciją turėsite įvesti, kai vykdysite [virtualaus objekto duomenų šaltinio konfigūravimą](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="20950-137">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="20950-138">Kairiojoje naršymo srityje pasirinkite **Sertifikatai ir slaptieji raktai**.</span><span class="sxs-lookup"><span data-stu-id="20950-138">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="20950-139">Puslapio srityje **Kliento slaptieji raktai** pasirinkite **Naujas kliento slaptasis raktas**.</span><span class="sxs-lookup"><span data-stu-id="20950-139">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="20950-140">Pateikite aprašymą, pasirinkite trukmę ir pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="20950-140">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="20950-141">Pasižymėkite slaptojo rakto vertę.</span><span class="sxs-lookup"><span data-stu-id="20950-141">Record the secret's value.</span></span> <span data-ttu-id="20950-142">Šią informaciją turėsite įvesti, kai vykdysite [virtualaus objekto duomenų šaltinio konfigūravimą](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="20950-142">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="20950-143">Šiuo metu būtinai išsisaugokite slaptojo rakto vertę.</span><span class="sxs-lookup"><span data-stu-id="20950-143">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="20950-144">Palikus šį puslapį, slaptasis raktas daugiau niekada nebus rodomas.</span><span class="sxs-lookup"><span data-stu-id="20950-144">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="20950-145">Įdiekite „Dynamics 365 HR Virtual Entity“ programą</span><span class="sxs-lookup"><span data-stu-id="20950-145">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="20950-146">Įdiekite „Dynamics 365 HR Virtual Entity“ programą savo „Power Apps“ aplinkoje, kad įdiegtumėte virtualaus objekto sprendimo paketą „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="20950-146">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="20950-147">Atidarykite [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="20950-147">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="20950-148">Sąraše **Aplinkos** pasirinkite „Power Apps“ aplinką, susijusią su „Human Resources“ egzemplioriumi.</span><span class="sxs-lookup"><span data-stu-id="20950-148">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="20950-149">Puslapio srityje **Ištekliai** pasirinkite **„Dynamics 365“ programos**.</span><span class="sxs-lookup"><span data-stu-id="20950-149">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="20950-150">Pasirinkite veiksmą **Įdiegti programą**.</span><span class="sxs-lookup"><span data-stu-id="20950-150">Select the **Install app** action.</span></span>

5. <span data-ttu-id="20950-151">Pasirinkite **Dynamics 365 HR Virtual Entity**, o tada pasirinkite **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="20950-151">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="20950-152">Peržiūrėkite ir pažymėkite, kad sutinkate su paslaugų teikimo sąlygomis.</span><span class="sxs-lookup"><span data-stu-id="20950-152">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="20950-153">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="20950-153">Select **Install**.</span></span>

<span data-ttu-id="20950-154">Diegimas trunka kelias minutes.</span><span class="sxs-lookup"><span data-stu-id="20950-154">The install takes a few minutes.</span></span> <span data-ttu-id="20950-155">Baigus, pereikite prie tolesnių veiksmų.</span><span class="sxs-lookup"><span data-stu-id="20950-155">When it completes, continue to the next steps.</span></span>

![Įdiekite „Dynamics 365 HR Virtual Entity“ programą iš „Power Platform“ administravimo centro](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="20950-157">Sukonfigūruokite virtualaus objekto duomenų šaltinį</span><span class="sxs-lookup"><span data-stu-id="20950-157">Configure the virtual entity data source</span></span> 

<span data-ttu-id="20950-158">Kitas veiksmas yra sukonfigūruoti virtualaus objekto duomenų šaltinį „Power Apps“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="20950-158">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="20950-159">Atidarykite [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="20950-159">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="20950-160">Sąraše **Aplinkos** pasirinkite „Power Apps“ aplinką, susijusią su „Human Resources“ egzemplioriumi.</span><span class="sxs-lookup"><span data-stu-id="20950-160">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="20950-161">Puslapio srityje **Informacija** pasirinkite **Aplinkos URL**.</span><span class="sxs-lookup"><span data-stu-id="20950-161">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="20950-162">Srityje **Spendimo būklės telkinys** pasirinkite piktogramą **Išplėstinė paieška**, esančią programos viršutiniame dešiniajame kampe.</span><span class="sxs-lookup"><span data-stu-id="20950-162">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="20950-163">Puslapyje **Išplėstinė paieška**, išskleidžiamajame sąraše **Ieškoti**, pasirinkite „**Finance and Operations“ virtualaus duomenų šaltinio konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="20950-163">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="20950-164">Pasirinkite **Rezultatai**.</span><span class="sxs-lookup"><span data-stu-id="20950-164">Select **Results**.</span></span>

7. <span data-ttu-id="20950-165">Pasirinkite įrašą **„Microsoft“ HR duomenų šaltinis**.</span><span class="sxs-lookup"><span data-stu-id="20950-165">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="20950-166">Įveskite reikiamą duomenų šaltinio konfigūracijos informaciją.</span><span class="sxs-lookup"><span data-stu-id="20950-166">Enter the required information for the data source configuration.</span></span>

   - <span data-ttu-id="20950-167">**Paskirties URL**: jūsų „Human Resources“ vardų srities URL.</span><span class="sxs-lookup"><span data-stu-id="20950-167">**Target URL**: The URL of your Human Resources namespace.</span></span>
   - <span data-ttu-id="20950-168">**Nuomotojo ID**: „Azure Active Directory“ („Azure AD“) nuomotojo ID.</span><span class="sxs-lookup"><span data-stu-id="20950-168">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>
   - <span data-ttu-id="20950-169">**AAD programos ID**: programos (kliento) ID, sukurtas programai, užregistruotai „Microsoft Azure“ portale.</span><span class="sxs-lookup"><span data-stu-id="20950-169">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="20950-170">Šią informaciją gavote anksčiau, atlikdami veiksmą [Užregistruokite programą „Microsoft Azure“](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="20950-170">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>
   - <span data-ttu-id="20950-171">**AAD programos slaptasis raktas**: kliento slaptasis raktas, sukurtas programai, užregistruotai „Microsoft Azure“ portale.</span><span class="sxs-lookup"><span data-stu-id="20950-171">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="20950-172">Šią informaciją gavote anksčiau, atlikdami veiksmą [Užregistruokite programą „Microsoft Azure“](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="20950-172">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

9. <span data-ttu-id="20950-173">Pasirinkite **Įrašyti ir uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="20950-173">Select **Save & Close**.</span></span>

   ![„Microsoft“ HR duomenų šaltinis](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="20950-175">Suteikite programos teises „Human Resources“</span><span class="sxs-lookup"><span data-stu-id="20950-175">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="20950-176">„Human Resources“ suteikite teises dviem „Azure AD“ programoms:</span><span class="sxs-lookup"><span data-stu-id="20950-176">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="20950-177">Programai, sukurtai jūsų nuomotojui „Microsoft Azure“ portale</span><span class="sxs-lookup"><span data-stu-id="20950-177">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="20950-178">„Dynamics 365 HR Virtual Entity“ programai, įdiegtai „Power Apps“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="20950-178">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="20950-179">„Human Resources“ atidarykite puslapį **„Azure Active Directory“ programos**.</span><span class="sxs-lookup"><span data-stu-id="20950-179">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="20950-180">Pasirinkite **Nauja**, kad sukurtumėte naują programos įrašą:</span><span class="sxs-lookup"><span data-stu-id="20950-180">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="20950-181">Lauke **Kliento ID** įveskite programos, kurią užregistravote „Microsoft Azure“ portale, kliento ID.</span><span class="sxs-lookup"><span data-stu-id="20950-181">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="20950-182">Lauke **Pavadinimas** įveskite programos, kurią užregistravote „Microsoft Azure“ portale, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="20950-182">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="20950-183">Lauke **Vartotojo ID** pasirinkite vartotojo, kuriam suteiktos „Human Resources“ ir „Power Apps“ aplinkos administravimo teisės, vartotojo ID.</span><span class="sxs-lookup"><span data-stu-id="20950-183">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="20950-184">Pasirinkite **Nauja**, kad sukurtumėte antrą programos įrašą:</span><span class="sxs-lookup"><span data-stu-id="20950-184">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="20950-185">**Kliento ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="20950-185">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="20950-186">**Pavadinimas**: Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="20950-186">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="20950-187">Lauke **Vartotojo ID** pasirinkite vartotojo, kuriam suteiktos „Human Resources“ ir „Power Apps“ aplinkos administravimo teisės, vartotojo ID.</span><span class="sxs-lookup"><span data-stu-id="20950-187">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="20950-188">Generuokite virtualius objektus</span><span class="sxs-lookup"><span data-stu-id="20950-188">Generate virtual entities</span></span>

<span data-ttu-id="20950-189">Baigus nustatymą, galite pasirinkti virtualius objektus, kuriuos norite generuoti ir įjungti savo „Common Data Service“ egzemplioriuje.</span><span class="sxs-lookup"><span data-stu-id="20950-189">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="20950-190">Atidarykite [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="20950-190">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="20950-191">Sąraše **Aplinkos** pasirinkite „Power Apps“ aplinką, susijusią su „Human Resources“ egzemplioriumi.</span><span class="sxs-lookup"><span data-stu-id="20950-191">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="20950-192">Puslapio srityje **Informacija** pasirinkite **Aplinkos URL**.</span><span class="sxs-lookup"><span data-stu-id="20950-192">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="20950-193">Srityje **Spendimo būklės telkinys** pasirinkite piktogramą **Išplėstinė paieška**, esančią puslapio viršutiniame dešiniajame kampe.</span><span class="sxs-lookup"><span data-stu-id="20950-193">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the page.</span></span>

5. <span data-ttu-id="20950-194">Puslapyje **Išplėstinė paieška**, išskleidžiamajame sąraše **Ieškoti** pasirinkite **Galimi HR objektai**.</span><span class="sxs-lookup"><span data-stu-id="20950-194">On the **Advanced Find** page, in the **Look for** dropdown list, select **Available HR Entities**.</span></span>

6. <span data-ttu-id="20950-195">Norėdami rasti objektą ar objektus, kuriuos norite įjungti, naudokite filtro pasirinktis.</span><span class="sxs-lookup"><span data-stu-id="20950-195">Use the filter options to find the entity or entities you want to enable.</span></span>

7. <span data-ttu-id="20950-196">Sąraše pasirinkite objektą.</span><span class="sxs-lookup"><span data-stu-id="20950-196">Select an entity from the list.</span></span>

8. <span data-ttu-id="20950-197">Objekto puslapyje pakeiskite objekto ypatybės **Buvo sugeneruota** reikšmę į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="20950-197">On the entity page, change the **Has Been Generated** property to **Yes** for the entity.</span></span>

9. <span data-ttu-id="20950-198">Įrašykite ir uždarykite objekto puslapį.</span><span class="sxs-lookup"><span data-stu-id="20950-198">Save and close the entity page.</span></span>

> [!NOTE]
> <span data-ttu-id="20950-199">Naudodami puslapį **Keisti kelis įrašus** galite sugeneruoti kelis virtualius objektus iš karto.</span><span class="sxs-lookup"><span data-stu-id="20950-199">You can generate multiple virtual entities at once by using the **Change Multiple Records** page.</span></span> <span data-ttu-id="20950-200">Puslapyje pasirinkite kelis įrašus ir juostoje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="20950-200">Select multiple records on the page, and select **Edit** on the ribbon.</span></span> <span data-ttu-id="20950-201">Tada galite pakeisti visų pasirinktų įrašų ypatybę **Buvo sugeneruota**.</span><span class="sxs-lookup"><span data-stu-id="20950-201">You can then change the **Has Been Generated** property for all selected records.</span></span>

![Galimi HR objektai](./media/hr-admin-integration-virtual-entities-available.jpg)

> [!NOTE]
> <span data-ttu-id="20950-203">Tam, kad būtų galima supaprastinti virtualių objektų gamybos procesus būsimose versijose, apdorojimas bus vykdomas „Human Resources“ puslapyje.</span><span class="sxs-lookup"><span data-stu-id="20950-203">To streamline the process of generating virtual entities in future releases, the process will occur in a page in Human Resources.</span></span>

## <a name="see-also"></a><span data-ttu-id="20950-204">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="20950-204">See also</span></span>

[<span data-ttu-id="20950-205">Kas yra „Common Data Service“?</span><span class="sxs-lookup"><span data-stu-id="20950-205">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="20950-206">Objekto apžvalga</span><span class="sxs-lookup"><span data-stu-id="20950-206">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="20950-207">Objekto ryšių apžvalga</span><span class="sxs-lookup"><span data-stu-id="20950-207">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="20950-208">Kurti ir redaguoti virtualius objektus, kuriuose yra duomenų iš išorinio duomenų šaltinio</span><span class="sxs-lookup"><span data-stu-id="20950-208">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="20950-209">Kas yra „Power Apps“ portalai?</span><span class="sxs-lookup"><span data-stu-id="20950-209">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="20950-210">Programų kūrimo „Power Apps“ apžvalga</span><span class="sxs-lookup"><span data-stu-id="20950-210">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
