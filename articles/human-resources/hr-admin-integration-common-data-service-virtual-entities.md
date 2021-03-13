---
title: Konfigūruokite „Dataverse“ virtualias lenteles
description: Šioje temoje parodoma, kaip konfigūruoti virtualias lenteles „Dynamics 365 Human Resources“. Kurti ir naujinti esamas virtualias lenteles ir analizuoti sukurtas ir prieinamas lenteles.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
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
ms.openlocfilehash: cd299b51e38cc30c3e18f3ef9de1f43fa817b840
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113603"
---
# <a name="configure-dataverse-virtual-tables"></a><span data-ttu-id="89b58-104">Konfigūruokite „Dataverse“ virtualias lenteles</span><span class="sxs-lookup"><span data-stu-id="89b58-104">Configure Dataverse virtual tables</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="89b58-105">„Dynamics 365 Human Resources“ yra „Microsoft Dataverse“ virtualus duomenų šaltinis.</span><span class="sxs-lookup"><span data-stu-id="89b58-105">Dynamics 365 Human Resources is a virtual data source in Microsoft Dataverse.</span></span> <span data-ttu-id="89b58-106">Jis leidžia atlikti visas kūrimo, skaitymo, atnaujinimo ir naikinimo (CRUD) operacijas naudojantis „Dataverse“ ir „Microsoft Power Platform“.</span><span class="sxs-lookup"><span data-stu-id="89b58-106">It provides full create, read, update, and delete (CRUD) operations from Dataverse and Microsoft Power Platform.</span></span> <span data-ttu-id="89b58-107">Duomenys virtualioms lentelėms nėra laikomi „Dataverse“, bet programos duomenų bazėje.</span><span class="sxs-lookup"><span data-stu-id="89b58-107">The data for virtual tables isn't stored in Dataverse, but in the application database.</span></span>

<span data-ttu-id="89b58-108">CRUD operacijas įjungti „Human Resources“ objektuose iš „Dataverse“, turite padaryti objektus prieinamus kaip virtualias lenteles „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="89b58-108">To enable CRUD operations on Human Resources entities from Dataverse, you must make the entities available as virtual tables in Dataverse.</span></span> <span data-ttu-id="89b58-109">Tai leis jums atlikti CRUD operacijas su „Human Resources“ duomenimis naudojantis „Dataverse“ ir „Microsoft Power Platform“.</span><span class="sxs-lookup"><span data-stu-id="89b58-109">This lets you perform CRUD operations from Dataverse and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="89b58-110">Operacijos taip pat palaiko „Human Resources“ visos verslo logikos patvirtinimą, siekiant užtikrinti duomenų vientisumą, kai į objektus rašomi duomenys.</span><span class="sxs-lookup"><span data-stu-id="89b58-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

> [!NOTE]
> <span data-ttu-id="89b58-111">„Human Resources“ objektai atitinka „Dataverse“ lenteles.</span><span class="sxs-lookup"><span data-stu-id="89b58-111">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="89b58-112">Dėl daugiau informacijos apie „Dataverse“ (anksčiau vadintą „Common Data Service“) ir terminologijos naujinimus, žr. [Kas yra „Microsoft Dataverse“?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="89b58-112">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

## <a name="available-virtual-tables-for-human-resources"></a><span data-ttu-id="89b58-113">Prieinamos virtualios lentelės „Human Resources“</span><span class="sxs-lookup"><span data-stu-id="89b58-113">Available virtual tables for Human Resources</span></span>

<span data-ttu-id="89b58-114">Visi atvirų duomenų protokolo (ODat) objektai „Human Resources“ yra prieinami kaip virtualios lentelės „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="89b58-114">All Open Data Protocol (OData) entities in Human Resources are available as virtual tables in Dataverse.</span></span> <span data-ttu-id="89b58-115">Jie taip pat yra prieinami „Power Platform“.</span><span class="sxs-lookup"><span data-stu-id="89b58-115">They're also available in Power Platform.</span></span> <span data-ttu-id="89b58-116">Dabar galite kurti programas ir patirtis naudodami duomenis tiesiogiai iš „Human Resources“ kartu su visomis CRUD galimybėmis ir nekopijuodami bei nesinchronizuodami duomenų su „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="89b58-116">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Dataverse.</span></span> <span data-ttu-id="89b58-117">Norėdami kurti išorines svetaines, kurios leidžia įgyvendinti bendradarbiavimo scenarijus vykdant „Human Resources“ verslo procesus, galite naudoti „Power Apps“ portalus.</span><span class="sxs-lookup"><span data-stu-id="89b58-117">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="89b58-118">Galite peržiūrėti virtualių lentelių aplinkoje sąrašą ir pradėti darbą su lentelėmis [„Power Apps“](https://make.powerapps.com), **„Dynamics 365 HR Virtual Tables“** sprendime.</span><span class="sxs-lookup"><span data-stu-id="89b58-118">You can view the list of virtual tables enabled in the environment, and begin working with the tables in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Tables** solution.</span></span>

![„Dynamics 365 HR Virtual Tables“ „Power Apps“](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a><span data-ttu-id="89b58-120">Virtualio lentelės prieš įgimtas lenteles</span><span class="sxs-lookup"><span data-stu-id="89b58-120">Virtual tables versus native tables</span></span>

<span data-ttu-id="89b58-121">Virtualios lentelės „Human Resources“ nėra tokios pačios kaip įgimtos „Dataverse“ lentelės sukurtos „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="89b58-121">Virtual tables for Human Resources aren't the same as the native Dataverse tables created for Human Resources.</span></span> 

<span data-ttu-id="89b58-122">Įgimtos lentelės „Human Resources“ yra sukuriamos atskirai ir laikomos HCM bendrame sprendime „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="89b58-122">The native tables for Human Resources are generated separately and maintained in the HCM Common solution in Dataverse.</span></span> <span data-ttu-id="89b58-123">Su įgimtomis lentelėmis, duomenys yra laikomi „Dataverse“ ir juos reikia sinchronizuoti su „Human Resources“ programos duomenų baze.</span><span class="sxs-lookup"><span data-stu-id="89b58-123">With native tables, the data is stored in Dataverse and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="89b58-124">Dėl įgimtų lentelų sąrašo „Dataverse“ „Human Resources“, žr. [„Dataverse“ lenteles](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="89b58-124">For a list of the native Dataverse tables for Human Resources, see [Dataverse tables](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="89b58-125">Sąranka</span><span class="sxs-lookup"><span data-stu-id="89b58-125">Setup</span></span>

<span data-ttu-id="89b58-126">Atlikite šiuos žingsnius, kad įjungtumėte virtualias lenteles jūsų aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="89b58-126">Follow these setup steps to enable virtual tables in your environment.</span></span>

### <a name="enable-virtual-tables-in-human-resources"></a><span data-ttu-id="89b58-127">Įjungti virtualias lenteles „Human Resources“</span><span class="sxs-lookup"><span data-stu-id="89b58-127">Enable virtual tables in Human Resources</span></span>

<span data-ttu-id="89b58-128">Pirmiausia, turite įjungti virtualias lenteles **Funkcijų valdymo** darbo srityje.</span><span class="sxs-lookup"><span data-stu-id="89b58-128">First, you must enable virtual tables in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="89b58-129">Programoje „Human Resources“ pasirinkite **Sistemos administravimas**.</span><span class="sxs-lookup"><span data-stu-id="89b58-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="89b58-130">Pasirinkite plytelę **Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="89b58-130">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="89b58-131">Rinkitės **Virtualios lentelės palaikymą HR „Dataverse“** ir tada rinkitės **Įjungti**.</span><span class="sxs-lookup"><span data-stu-id="89b58-131">Select **Virtual table support for HR in Dataverse**, and then select **Enable**.</span></span>

<span data-ttu-id="89b58-132">Dėl daugiau informacijos apie funkcijų įjungimą ir išjungimą, žr. [Valdyti funkcijas](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="89b58-132">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="89b58-133">Užregistruokite programą „Microsoft Azure“</span><span class="sxs-lookup"><span data-stu-id="89b58-133">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="89b58-134">Turite registruoti savo žmogiškųjų išteklių elementą „Azure“ portale tam, kad „Microsoft“ tapatybės platforma galėtų pateikti autentifikavimą ir autentifikavimo paslaugas programai ir vartotojams.</span><span class="sxs-lookup"><span data-stu-id="89b58-134">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="89b58-135">Daugiau informacijos apie tai, kaip užregistruoti programas „Azure“, žr. [„Quickstart“: programos registravimas naudojant „Microsoft“ tapatumo platformą](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="89b58-135">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="89b58-136">Atidarykite [„Microsoft Azure“ portalą](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="89b58-136">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="89b58-137">„Azure“ paslaugų sąraše pasirinkite **Programų registracijos**.</span><span class="sxs-lookup"><span data-stu-id="89b58-137">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="89b58-138">Pasirinkite **Nauja registracija**.</span><span class="sxs-lookup"><span data-stu-id="89b58-138">Select **New registration**.</span></span>

4. <span data-ttu-id="89b58-139">Lauke **Pavadinimas** įveskite apibūdinantį programos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="89b58-139">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="89b58-140">Pavyzdžiui, **„Dynamics 365 Human Resources“ virtualios lentelės**.</span><span class="sxs-lookup"><span data-stu-id="89b58-140">For example, **Dynamics 365 Human Resources Virtual Tables**.</span></span>

5. <span data-ttu-id="89b58-141">Lauke **Nukreipimo URI** įveskite „Human Resources“ objekto vardų srities URL.</span><span class="sxs-lookup"><span data-stu-id="89b58-141">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="89b58-142">Pasirinkite **Registruotis**.</span><span class="sxs-lookup"><span data-stu-id="89b58-142">Select **Register**.</span></span>

7. <span data-ttu-id="89b58-143">Baigus registraciją, „Azure“ portale rodoma programos registracijos sritis **Apžvalga**, kurioje nurodytas **Programos (kliento) ID**.</span><span class="sxs-lookup"><span data-stu-id="89b58-143">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="89b58-144">Pasižymėkite **Programos (kliento) ID**.</span><span class="sxs-lookup"><span data-stu-id="89b58-144">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="89b58-145">Jūs įvesite šią informaciją, kai [Konfigūruosite virtualios lentelės duomenų šaltinį](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="89b58-145">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

8. <span data-ttu-id="89b58-146">Kairiojoje naršymo srityje pasirinkite **Sertifikatai ir slaptieji raktai**.</span><span class="sxs-lookup"><span data-stu-id="89b58-146">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="89b58-147">Puslapio srityje **Kliento slaptieji raktai** pasirinkite **Naujas kliento slaptasis raktas**.</span><span class="sxs-lookup"><span data-stu-id="89b58-147">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="89b58-148">Pateikite aprašymą, pasirinkite trukmę ir pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="89b58-148">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="89b58-149">Pasižymėkite slaptojo rakto vertę.</span><span class="sxs-lookup"><span data-stu-id="89b58-149">Record the secret's value.</span></span> <span data-ttu-id="89b58-150">Jūs įvesite šią informaciją, kai [Konfigūruosite virtualios lentelės duomenų šaltinį](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="89b58-150">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="89b58-151">Šiuo metu būtinai išsisaugokite slaptojo rakto vertę.</span><span class="sxs-lookup"><span data-stu-id="89b58-151">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="89b58-152">Palikus šį puslapį, slaptasis raktas daugiau niekada nebus rodomas.</span><span class="sxs-lookup"><span data-stu-id="89b58-152">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a><span data-ttu-id="89b58-153">Įdiekite „Dynamics 365 HR Virtual Tables“ programą</span><span class="sxs-lookup"><span data-stu-id="89b58-153">Install the Dynamics 365 HR Virtual Table app</span></span>

<span data-ttu-id="89b58-154">Įdiekite „Dynamics 365 HR Virtual Table“ programą savo „Power Apps“ aplinkoje, kad talpintumėte virtualios lentelės sprendimo paketą į „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="89b58-154">Install the Dynamics 365 HR Virtual Table app in your Power Apps environment to deploy the virtual table solution package to Dataverse.</span></span>

1. <span data-ttu-id="89b58-155">Atidarykite [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="89b58-155">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="89b58-156">Sąraše **Aplinkos** pasirinkite „Power Apps“ aplinką, susijusią su „Human Resources“ egzemplioriumi.</span><span class="sxs-lookup"><span data-stu-id="89b58-156">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="89b58-157">Puslapio srityje **Ištekliai** pasirinkite **„Dynamics 365“ programos**.</span><span class="sxs-lookup"><span data-stu-id="89b58-157">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="89b58-158">Pasirinkite veiksmą **Įdiegti programą**.</span><span class="sxs-lookup"><span data-stu-id="89b58-158">Select the **Install app** action.</span></span>

5. <span data-ttu-id="89b58-159">Rinkitės **„Dynamics 365 HR Virtual Table“** ir rinkitės **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="89b58-159">Select **Dynamics 365 HR Virtual Table**, and select **Next**.</span></span>

6. <span data-ttu-id="89b58-160">Peržiūrėkite ir pažymėkite, kad sutinkate su paslaugų teikimo sąlygomis.</span><span class="sxs-lookup"><span data-stu-id="89b58-160">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="89b58-161">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="89b58-161">Select **Install**.</span></span>

<span data-ttu-id="89b58-162">Diegimas trunka kelias minutes.</span><span class="sxs-lookup"><span data-stu-id="89b58-162">The install takes a few minutes.</span></span> <span data-ttu-id="89b58-163">Baigus, pereikite prie tolesnių veiksmų.</span><span class="sxs-lookup"><span data-stu-id="89b58-163">When it completes, continue to the next steps.</span></span>

![Įdiekite „Dynamics 365 HR Virtual Table“ programą iš „Power Platform“ administravimo centro](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-table-data-source"></a><span data-ttu-id="89b58-165">Konfigūruokite virtualios lentelės duomenų šaltinį</span><span class="sxs-lookup"><span data-stu-id="89b58-165">Configure the virtual table data source</span></span> 

<span data-ttu-id="89b58-166">Kitas žingsnis yra konfigūruoti virtualios lentelės duomenų šaltinį „Power Apps“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="89b58-166">The next step is to configure the virtual table data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="89b58-167">Atidarykite [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="89b58-167">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="89b58-168">Sąraše **Aplinkos** pasirinkite „Power Apps“ aplinką, susijusią su „Human Resources“ egzemplioriumi.</span><span class="sxs-lookup"><span data-stu-id="89b58-168">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="89b58-169">Puslapio srityje **Informacija** pasirinkite **Aplinkos URL**.</span><span class="sxs-lookup"><span data-stu-id="89b58-169">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="89b58-170">Srityje **Spendimo būklės telkinys** pasirinkite piktogramą **Išplėstinė paieška**, esančią programos viršutiniame dešiniajame kampe.</span><span class="sxs-lookup"><span data-stu-id="89b58-170">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="89b58-171">Puslapyje **Išplėstinė paieška**, išskleidžiamajame sąraše **Ieškoti**, pasirinkite „**Finance and Operations“ virtualaus duomenų šaltinio konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="89b58-171">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="89b58-172">Pasirinkite **Rezultatai**.</span><span class="sxs-lookup"><span data-stu-id="89b58-172">Select **Results**.</span></span>

7. <span data-ttu-id="89b58-173">Pasirinkite įrašą **„Microsoft“ HR duomenų šaltinis**.</span><span class="sxs-lookup"><span data-stu-id="89b58-173">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="89b58-174">Įveskite būtiną informaciją duomenų šaltinių konfigūravimui:</span><span class="sxs-lookup"><span data-stu-id="89b58-174">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="89b58-175">**Paskirties URL**: jūsų „Human Resources“ vardų srities URL.</span><span class="sxs-lookup"><span data-stu-id="89b58-175">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="89b58-176">Tikslo URL formatas yra:</span><span class="sxs-lookup"><span data-stu-id="89b58-176">The format of the target URL is:</span></span>
     
     <span data-ttu-id="89b58-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="89b58-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="89b58-178">Pvz.:</span><span class="sxs-lookup"><span data-stu-id="89b58-178">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="89b58-179">Įsitikinkite, kad įtrauksite "**/**" simbolį URL gale siekiant išvengti klaidos gavimo.</span><span class="sxs-lookup"><span data-stu-id="89b58-179">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="89b58-180">**Nuomotojo ID**: „Azure Active Directory“ („Azure AD“) nuomotojo ID.</span><span class="sxs-lookup"><span data-stu-id="89b58-180">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="89b58-181">**AAD programos ID**: programos (kliento) ID, sukurtas programai, užregistruotai „Microsoft Azure“ portale.</span><span class="sxs-lookup"><span data-stu-id="89b58-181">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="89b58-182">Šią informaciją gavote anksčiau, atlikdami veiksmą [Užregistruokite programą „Microsoft Azure“](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="89b58-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="89b58-183">**AAD programos slaptasis raktas**: kliento slaptasis raktas, sukurtas programai, užregistruotai „Microsoft Azure“ portale.</span><span class="sxs-lookup"><span data-stu-id="89b58-183">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="89b58-184">Šią informaciją gavote anksčiau, atlikdami veiksmą [Užregistruokite programą „Microsoft Azure“](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="89b58-184">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![„Microsoft“ HR duomenų šaltinis](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="89b58-186">Pasirinkite **Įrašyti ir uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="89b58-186">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="89b58-187">Suteikite programos teises „Human Resources“</span><span class="sxs-lookup"><span data-stu-id="89b58-187">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="89b58-188">„Human Resources“ suteikite teises dviem „Azure AD“ programoms:</span><span class="sxs-lookup"><span data-stu-id="89b58-188">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="89b58-189">Programai, sukurtai jūsų nuomotojui „Microsoft Azure“ portale</span><span class="sxs-lookup"><span data-stu-id="89b58-189">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="89b58-190">„Dynamics 365 HR Virtual Table“ programa įdiegta iš „Power Apps“ aplinkos</span><span class="sxs-lookup"><span data-stu-id="89b58-190">The Dynamics 365 HR Virtual Table app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="89b58-191">„Human Resources“ atidarykite puslapį **„Azure Active Directory“ programos**.</span><span class="sxs-lookup"><span data-stu-id="89b58-191">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="89b58-192">Pasirinkite **Nauja**, kad sukurtumėte naują programos įrašą:</span><span class="sxs-lookup"><span data-stu-id="89b58-192">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="89b58-193">Lauke **Kliento ID** įveskite programos, kurią užregistravote „Microsoft Azure“ portale, kliento ID.</span><span class="sxs-lookup"><span data-stu-id="89b58-193">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="89b58-194">Lauke **Pavadinimas** įveskite programos, kurią užregistravote „Microsoft Azure“ portale, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="89b58-194">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="89b58-195">Lauke **Vartotojo ID** pasirinkite vartotojo, kuriam suteiktos „Human Resources“ ir „Power Apps“ aplinkos administravimo teisės, vartotojo ID.</span><span class="sxs-lookup"><span data-stu-id="89b58-195">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="89b58-196">Pasirinkite **Nauja**, kad sukurtumėte antrą programos įrašą:</span><span class="sxs-lookup"><span data-stu-id="89b58-196">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="89b58-197">**Kliento ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="89b58-197">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="89b58-198">**Pavadinimas**: „Dynamics 365 HR Virtual Table“</span><span class="sxs-lookup"><span data-stu-id="89b58-198">**Name**: Dynamics 365 HR Virtual Table</span></span>
    - <span data-ttu-id="89b58-199">Lauke **Vartotojo ID** pasirinkite vartotojo, kuriam suteiktos „Human Resources“ ir „Power Apps“ aplinkos administravimo teisės, vartotojo ID.</span><span class="sxs-lookup"><span data-stu-id="89b58-199">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-tables"></a><span data-ttu-id="89b58-200">Kurti virtualias lenteles</span><span class="sxs-lookup"><span data-stu-id="89b58-200">Generate virtual tables</span></span>

<span data-ttu-id="89b58-201">Kai nustatymas užbaigtas, galite rinktis virtualias lenteles, kurias norite kurti ir įjungti savo „Dataverse“ objekte.</span><span class="sxs-lookup"><span data-stu-id="89b58-201">When setup completes, you can select the virtual tables you want to generate and enable in your Dataverse instance.</span></span>

1. <span data-ttu-id="89b58-202">„Human Resources“, atverkite **„Dataverse“ integravimo** puslapį.</span><span class="sxs-lookup"><span data-stu-id="89b58-202">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="89b58-203">Rinkitės **Virtualių lentelių** skirtuką.</span><span class="sxs-lookup"><span data-stu-id="89b58-203">Select the **Virtual tables** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="89b58-204">**Įjungti virtualias lenteles** jungiklis bus nustatytas į **Taip** automatiškai, kai visi būtini veiksmai bus užbaigti.</span><span class="sxs-lookup"><span data-stu-id="89b58-204">The **Enable virtual tables** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="89b58-205">Jei perjungiklis nustatytas į **Ne**, peržiūrėkite ankstesniuose šio dokumento skyriuose aprašytus veiksmus, norėdami užtikrinti, kad visi būtinieji nustatymo veiksmai yra baigti.</span><span class="sxs-lookup"><span data-stu-id="89b58-205">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="89b58-206">Rinkitės lentelę ar lenteles, kurias norite kurti „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="89b58-206">Select the table or tables you want to generate in Dataverse.</span></span>

4. <span data-ttu-id="89b58-207">Pasirinkite **Generuoti / atnaujinti**.</span><span class="sxs-lookup"><span data-stu-id="89b58-207">Select **Generate/refresh**.</span></span>

![„Dataverse“ integravimas](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-table-generation-status"></a><span data-ttu-id="89b58-209">Tikrinti lentelės kūrimo būseną</span><span class="sxs-lookup"><span data-stu-id="89b58-209">Check table generation status</span></span>

<span data-ttu-id="89b58-210">Virtualios lentelės sukurtos „Dataverse“ per nesinchronišką fono procesą.</span><span class="sxs-lookup"><span data-stu-id="89b58-210">Virtual tables are generated in Dataverse through an asynchronous background process.</span></span> <span data-ttu-id="89b58-211">Proceso atnaujinimai rodomi veiksmų centre.</span><span class="sxs-lookup"><span data-stu-id="89b58-211">Updates on the process display in the action center.</span></span> <span data-ttu-id="89b58-212">Išsami informacija apie procesą, įskaitant klaidos žurnalus, rodoma puslapyje **Proceso automatizavimai**.</span><span class="sxs-lookup"><span data-stu-id="89b58-212">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="89b58-213">„Human Resources“ atidarykite puslapį **Proceso automatizavimai**.</span><span class="sxs-lookup"><span data-stu-id="89b58-213">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="89b58-214">Pasirinkite skirtuką **Fone vykstantys procesai**.</span><span class="sxs-lookup"><span data-stu-id="89b58-214">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="89b58-215">Rinkitės **Virtualios lentelės apklausos nesinchroniško veiksmo fono procesas**.</span><span class="sxs-lookup"><span data-stu-id="89b58-215">Select **Virtual table poll async operation background process**.</span></span>

4. <span data-ttu-id="89b58-216">Pasirinkite **Peržiūrėti naujausius rezultatus**.</span><span class="sxs-lookup"><span data-stu-id="89b58-216">Select **View most recent results**.</span></span>

<span data-ttu-id="89b58-217">Išslenkančioje srityje rodomi naujausi proceso vykdymo rezultatai.</span><span class="sxs-lookup"><span data-stu-id="89b58-217">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="89b58-218">Galite peržiūrėti proceso žurnalą, įskaitant visas iš „Dataverse” grąžintas klaidas.</span><span class="sxs-lookup"><span data-stu-id="89b58-218">You can view the log for the process, including any errors returned from Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="89b58-219">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="89b58-219">See also</span></span>

[<span data-ttu-id="89b58-220">Kas yra „Dataverse“?</span><span class="sxs-lookup"><span data-stu-id="89b58-220">What is Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="89b58-221">Lentelės „Dataverse“</span><span class="sxs-lookup"><span data-stu-id="89b58-221">Tables in Dataverse</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="89b58-222">Lentelės ryšių apžvalga</span><span class="sxs-lookup"><span data-stu-id="89b58-222">Table relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="89b58-223">Kurti ir redaguoti virtualias lenteles, kuriose yra duomenys iš išorės duomenų šaltinio</span><span class="sxs-lookup"><span data-stu-id="89b58-223">Create and edit virtual tables that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="89b58-224">Kas yra „Power Apps“ portalai?</span><span class="sxs-lookup"><span data-stu-id="89b58-224">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="89b58-225">Programų kūrimo „Power Apps“ apžvalga</span><span class="sxs-lookup"><span data-stu-id="89b58-225">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
