---
title: Integravimas su „LinkedIn Talent Hub“
description: Šioje temoje paaiškinama, kaip nustatyti „Microsoft Dynamics 365 Human Resources” ir „LinkedIn Talent Hub“ integravimą.
author: jaredha
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: efcac2bd82956015eb822c6a493b8625a35cd194
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805063"
---
# <a name="integrate-with-linkedin-talent-hub"></a><span data-ttu-id="35bd9-103">Integravimas su „LinkedIn Talent Hub“</span><span class="sxs-lookup"><span data-stu-id="35bd9-103">Integrate with LinkedIn Talent Hub</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="35bd9-104">[„LinkedIn Talent Hub”](https://business.linkedin.com/talent-solutions/talent-hub) yra pretendentų sekimo sistemos (ATS) platforma.</span><span class="sxs-lookup"><span data-stu-id="35bd9-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) is an applicant tracking system (ATS) platform.</span></span> <span data-ttu-id="35bd9-105">Ji leidžia vykdyti darbuotojų iešką bei valdyti ir samdyti darbuotojus vienoje vietoje.</span><span class="sxs-lookup"><span data-stu-id="35bd9-105">It lets you source, manage, and hire employees all in one place.</span></span> <span data-ttu-id="35bd9-106">Integruodami „Microsoft Dynamics 365 Human Resources” su „LinkedIn Talent Hub” galite lengvai sukurti pretendentų, pasamdytų pareigoms, darbuotojų įrašus „Human Resources”.</span><span class="sxs-lookup"><span data-stu-id="35bd9-106">By integrating Microsoft Dynamics 365 Human Resources with LinkedIn Talent Hub, you can easily create employee records in Human Resources for applicants who have been hired for a position.</span></span>

## <a name="setup"></a><span data-ttu-id="35bd9-107">Sąranka</span><span class="sxs-lookup"><span data-stu-id="35bd9-107">Setup</span></span>

<span data-ttu-id="35bd9-108">Sistemos administratorius turi užbaigti sąrankos užduotis, kad būtų galima integruoti su „LinkedIn Talent Hub”.</span><span class="sxs-lookup"><span data-stu-id="35bd9-108">A system administrator must complete setup tasks to enable integration with LinkedIn Talent Hub.</span></span> <span data-ttu-id="35bd9-109">Pirmiausia „Power Apps” aplinkoje turite nustatyti vartotoją ir saugos vaidmenį, kad galėtumėte suteikti „LinkedIn Talent Hub” atitinkamas teises duomenims įrašyti į „Human Resources”.</span><span class="sxs-lookup"><span data-stu-id="35bd9-109">First, in the Power Apps environment, you must set up a user and security role to grant LinkedIn Talent Hub the appropriate permissions to write data into Human Resources.</span></span>

### <a name="link-your-environment-to-linkedin-talent-hub"></a><span data-ttu-id="35bd9-110">Jūsų aplinkos susiejimas su „LinkedIn Talent Hub”</span><span class="sxs-lookup"><span data-stu-id="35bd9-110">Link your environment to LinkedIn Talent Hub</span></span>

1. <span data-ttu-id="35bd9-111">Atidarykite [„LinkedIn Talent Hub”](https://business.linkedin.com/talent-solutions/talent-hub).</span><span class="sxs-lookup"><span data-stu-id="35bd9-111">Open [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span></span>

2. <span data-ttu-id="35bd9-112">Vartotojo išplečiamajame meniu pasirinkite **Produkto parametrai**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-112">On the user drop-down menu, select **Product Settings**.</span></span>

3. <span data-ttu-id="35bd9-113">Kairiojoje naršymo srityje, dalyje **Išplėstiniai nustatymai**, pasirinkite **Integravimas**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-113">In the left navigation pane, in the **Advanced** section, select **Integrations**.</span></span>

4. <span data-ttu-id="35bd9-114">Pasirinkite „Microsoft Dynamics 365 Human Resources” integravimo parinktį **Įgalioti**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-114">Select **Authorize** for the Microsoft Dynamics 365 Human Resources integration.</span></span>

5. <span data-ttu-id="35bd9-115">Puslapyje **„Dynamics 365 Human Resources”** pasirinkite aplinką, kurią norite susieti su „LinkedIn Talent Hub”, tada pasirinkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-115">On the **Dynamics 365 Human Resources** page, select the environment to link LinkedIn Talent Hub to, and then select **Link**.</span></span>

    ![„LinkedIn Talent Hub” parengimas](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > <span data-ttu-id="35bd9-117">Galite susieti tik su aplinkomis, kuriose jūsų vartotojo abonementas turi administratoriaus prieigą prie „Human Resources” aplinkos ir susijusios „Power Apps” aplinkos.</span><span class="sxs-lookup"><span data-stu-id="35bd9-117">You can link only to environments where your user account has administrator access to both the Human Resources environment and the associated Power Apps environment.</span></span> <span data-ttu-id="35bd9-118">Jei „Human Resources” susiejimo puslapyje nėra pateiktų aplinkų, įsitikinkite, kad turite licencijuotų „Human Resources” aplinkų nuomotojuje ir kad vartotojui, kuriuo prisijungėte prie susiejimo puslapio, suteiktos „Human Resources” aplinkos ir „Power Apps” aplinkos administratoriaus teisės.</span><span class="sxs-lookup"><span data-stu-id="35bd9-118">If no environments are listed on the Human Resources link page, make sure that you have licensed Human Resources environments on the tenant, and that the user that you signed in to the link page as has administrator permissions to both the Human Resources environment and the Power Apps environment.</span></span>

### <a name="create-a-power-apps-security-role"></a><span data-ttu-id="35bd9-119">„Power Apps” saugos vaidmens kūrimas</span><span class="sxs-lookup"><span data-stu-id="35bd9-119">Create a Power Apps security role</span></span>

1. <span data-ttu-id="35bd9-120">Atidarykite [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="35bd9-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="35bd9-121">Sąraše **Aplinkos** pasirinkite aplinką, susietą su „Human Resources” aplinka, su kuria norite susieti jūsų „LinkedIn Talent Hub” egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="35bd9-121">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="35bd9-122">Pasirinkite **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-122">Select **Settings**.</span></span>

4. <span data-ttu-id="35bd9-123">Išplėskite mazgą **Vartotojai ir teisės** ir pasirinkite **Saugos vaidmenys**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-123">Expand the **Users + Permissions** node, and select **Security Roles**.</span></span>

5. <span data-ttu-id="35bd9-124">Puslapio **Saugos vaidmenys** įrankių juostoje pasirinkite **Naujas vaidmuo**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-124">On the **Security Roles** page, on the toolbar, select **New role**.</span></span>

6. <span data-ttu-id="35bd9-125">Skirtuke **Išsami informacija** įveskite vaidmens pavadinimą, pvz., **„LinkedIn Talent Hub” HRIS integravimas**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-125">On the **Details** tab, enter a name for the role, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>

7. <span data-ttu-id="35bd9-126">Skirtuke **Tinkinimas** pasirinkite organizacijos lygio teisę **Skaitymas** toliau pateiktiems objektams.</span><span class="sxs-lookup"><span data-stu-id="35bd9-126">On the **Customization** tab, select organization-level **Read** permission for the following entities:</span></span>

    - <span data-ttu-id="35bd9-127">Objektas</span><span class="sxs-lookup"><span data-stu-id="35bd9-127">Entity</span></span>
    - <span data-ttu-id="35bd9-128">Laukas</span><span class="sxs-lookup"><span data-stu-id="35bd9-128">Field</span></span>
    - <span data-ttu-id="35bd9-129">Ryšys</span><span class="sxs-lookup"><span data-stu-id="35bd9-129">Relationship</span></span>

8. <span data-ttu-id="35bd9-130">Įrašykite ir uždarykite saugos vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="35bd9-130">Save and close the security role.</span></span>

### <a name="create-a-power-apps-application-user"></a><span data-ttu-id="35bd9-131">„Power Apps” programos vartotojo kūrimas</span><span class="sxs-lookup"><span data-stu-id="35bd9-131">Create a Power Apps application user</span></span>

<span data-ttu-id="35bd9-132">Reikia sukurti „LinkedIn Talent Hub” adapterio programos vartotoją, kad adapteriui būtų suteiktos teisės įrašyti kandidatų įrašus į „Power Apps” aplinką.</span><span class="sxs-lookup"><span data-stu-id="35bd9-132">An application user must be created for the LinkedIn Talent Hub adapter to grant permissions to the adapter to write candidate records into the Power Apps environment.</span></span>

1. <span data-ttu-id="35bd9-133">Atidarykite [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="35bd9-133">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="35bd9-134">Sąraše **Aplinkos** pasirinkite aplinką, susietą su „Human Resources” aplinka, su kuria norite susieti jūsų „LinkedIn Talent Hub” egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="35bd9-134">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="35bd9-135">Pasirinkite **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-135">Select **Settings**.</span></span>

4. <span data-ttu-id="35bd9-136">Išplėskite mazgą **Vartotojai ir teisės** ir pasirinkite **Vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-136">Expand the **Users + Permissions** node, and select **Users**.</span></span>

5. <span data-ttu-id="35bd9-137">Pasirinkite **Valdyti „Dynamics 365” vartotojus**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-137">Select **Manage users in Dynamics 365**.</span></span>

6. <span data-ttu-id="35bd9-138">Naudokite išplečiamąjį meniu, esantį virš sąrašo, norėdami pakeisti rodinį iš numatytojo rodinio **Įgalinti vartotojai** į **Programos vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-138">Use the drop-down menu above the list to change the view from the default **Enabled Users** view to **Application Users**.</span></span>

    ![Rodinys Programos vartotojai](./media/hr-admin-integration-power-apps-application-users.jpg)

7. <span data-ttu-id="35bd9-140">Įrankių juostoje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-140">On the toolbar, select **New**.</span></span>

8. <span data-ttu-id="35bd9-141">Puslapyje **Naujas vartotojas** atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="35bd9-141">On the **New user** page, follow these steps:</span></span>

    1. <span data-ttu-id="35bd9-142">Pakeiskite lauko **Vartotojo tipas** reikšmę į **Programos vartotojas**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-142">Change the value of the **User type** field to **Application User**.</span></span>
    2. <span data-ttu-id="35bd9-143">Nustatykite lauką **Vartotojo vardas** į **„Dynamics365 HR LinkedIn” HRIS integravimas**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-143">Set the **User Name** field to **Dynamics365 HR LinkedIn HRIS Integration**.</span></span>
    3. <span data-ttu-id="35bd9-144">Nustatykite lauką **Programos ID** į **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-144">Set the **Application ID** field to **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    4. <span data-ttu-id="35bd9-145">Įveskite reikšmes laukuose **Vardas**, **Pavardė** ir **Pagrindinis el. pašto adresas**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-145">Enter any value in the **First Name**, **Last Name**, and **Primary Email** fields.</span></span>
    5. <span data-ttu-id="35bd9-146">Įrankių juostoje pasirinkite **Įrašyti ir uždaryti** (Save \& Close).</span><span class="sxs-lookup"><span data-stu-id="35bd9-146">On the toolbar, select **Save \& Close**.</span></span>

### <a name="assign-a-security-role-to-the-new-user"></a><span data-ttu-id="35bd9-147">Saugos vaidmens priskyrimas naujam vartotojui</span><span class="sxs-lookup"><span data-stu-id="35bd9-147">Assign a security role to the new user</span></span>

<span data-ttu-id="35bd9-148">Įrašę ir uždarę naują programos vartotoją, aprašytą ankstesniame skyriuje, būsite grąžinti į puslapį **Vartotojų sąrašas**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-148">After you save and close the new application user in the previous section, you're returned to the **Users list** page.</span></span>

1. <span data-ttu-id="35bd9-149">Puslapyje **Vartotojų sąrašas** pakeiskite rodinį į **Programos vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-149">On the **Users list** page, change the view to **Application Users**.</span></span>

2. <span data-ttu-id="35bd9-150">Pasirinkite programos vartotoją, kurį sukūrėte ankstesniame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="35bd9-150">Select the application user that you created in the previous section.</span></span>

3. <span data-ttu-id="35bd9-151">Įrankių juostoje pasirinkite **Valdyti vaidmenis**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-151">On the toolbar, select **Manage Roles**.</span></span>

4. <span data-ttu-id="35bd9-152">Pasirinkite integracijos saugos vaidmenį, kurį sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="35bd9-152">Select the security role that you created earlier for the integration.</span></span>

5. <span data-ttu-id="35bd9-153">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-153">Select **OK**.</span></span>

### <a name="add-an-azure-active-directory-app-in-human-resources"></a><span data-ttu-id="35bd9-154">„Azure Active Directory” programos įtraukimas į „Human Resources“</span><span class="sxs-lookup"><span data-stu-id="35bd9-154">Add an Azure Active Directory app in Human Resources</span></span>

1. <span data-ttu-id="35bd9-155">„Dynamics 365 Human Resources“ atidarykite puslapį **„Azure Active Directory“ programos**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-155">In Dynamics 365 Human Resources, open the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="35bd9-156">Įtraukite naują įrašą į sąrašą ir nustatykite toliau pateiktus laukus.</span><span class="sxs-lookup"><span data-stu-id="35bd9-156">Add a new record to the list, and set the following fields:</span></span>

    - <span data-ttu-id="35bd9-157">**Kliento ID**: įveskite **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-157">**Client ID**: Enter **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    - <span data-ttu-id="35bd9-158">**Pavadinimas**: įveskite „Power Apps” saugos vaidmens, kurį sukūrėte anksčiau, pavadinimą, pvz., **„LinkedIn Talent Hub” HRIS integravimas**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-158">**Name**: Enter the name of the Power Apps security role that you created earlier, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>
    - <span data-ttu-id="35bd9-159">**Vartotojo ID**: pasirinkite vartotoją, kuris turi teises įrašyti duomenis personalo valdyme.</span><span class="sxs-lookup"><span data-stu-id="35bd9-159">**User ID**: Select a user who has permissions to write data in Personnel Management.</span></span>

### <a name="create-the-table-in-dataverse"></a><span data-ttu-id="35bd9-160">Kurti lenteles „Dataverse“</span><span class="sxs-lookup"><span data-stu-id="35bd9-160">Create the table in Dataverse</span></span>

> [!IMPORTANT]
> <span data-ttu-id="35bd9-161">Integravimas su „LinkedIn Talent Hub“ priklauso nuo virtalių lentelių  Dataverse“ „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="35bd9-161">The integration with LinkedIn Talent Hub depends on virtual tables in Dataverse for Human Resources.</span></span> <span data-ttu-id="35bd9-162">Kaip išankstines sąlygas šiam veiksmui nustatymuose, turite konfigūruoti virtualias lenteles.</span><span class="sxs-lookup"><span data-stu-id="35bd9-162">As a prerequisite for this step in the setup, you must configure virtual tables.</span></span> <span data-ttu-id="35bd9-163">Dėl informacijos apie tai, kaip konfigūruoti virtualias lenteles, žr. [Konfigūruoti „Dataverse“ virtualias lenteles](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="35bd9-163">For information about how to configure virtual tables, see [Configure Dataverse virtual tables](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

1. <span data-ttu-id="35bd9-164">„Human Resources“, atverkite **„Dataverse“ integravimo** puslapį.</span><span class="sxs-lookup"><span data-stu-id="35bd9-164">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="35bd9-165">Rinkitės **Virtualių lentelių** skirtuką.</span><span class="sxs-lookup"><span data-stu-id="35bd9-165">Select the **Virtual tables** tab.</span></span>

3. <span data-ttu-id="35bd9-166">Filtruokite objektų sąrašą pagal objektų žymas, norėdami rasti **„LinkedIn” eksportuotas kandidatas**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-166">Filter the entity list by entity label to find **LinkedIn exported candidate**.</span></span>

4. <span data-ttu-id="35bd9-167">Pasirinkite objektą ir pasirinkite **Generuoti / atnaujinti**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-167">Select the entity, and then select **Generate/refresh**.</span></span>

## <a name="exporting-candidate-records"></a><span data-ttu-id="35bd9-168">Kandidatų įrašų eksportavimas</span><span class="sxs-lookup"><span data-stu-id="35bd9-168">Exporting candidate records</span></span>

<span data-ttu-id="35bd9-169">Užbaigus nustatymus, įdarbintojai ir žmogiškųjų išteklių (HR) darbuotojai gali naudoti **Eksportuoti į HRIS** funkciją „LinkedIn Talent Hub“ siekiant eksportuoti pasamdyto kandidato įrašus iš „LinkedIn Talent Hub“ į „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="35bd9-169">After the setup is completed, recruiters and human resources (HR) professionals can use the **Export to HRIS** function in LinkedIn Talent Hub to export hired candidate records from LinkedIn Talent Hub to Human Resources.</span></span>

### <a name="export-records-from-linkedin-talent-hub"></a><span data-ttu-id="35bd9-170">Įrašų eksportavimas iš „LinkedIn Talent Hub”</span><span class="sxs-lookup"><span data-stu-id="35bd9-170">Export records from LinkedIn Talent Hub</span></span>

<span data-ttu-id="35bd9-171">Kai kandidatas pereina įdarbinimo procesą ir yra pasamdomas, galima eksportuoti kandidato įrašą iš „LinkedIn Talent Hub“ į „Human Resources”.</span><span class="sxs-lookup"><span data-stu-id="35bd9-171">After a candidate has moved through the recruiting process and has been hired, you can export the candidate record from LinkedIn Talent Hub to Human Resources.</span></span>

1. <span data-ttu-id="35bd9-172">„LinkedIn Talent Hub” atidarykite projektą, kuriam pasamdėte naują darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="35bd9-172">In LinkedIn Talent Hub, open the project that you hired the new employee for.</span></span>

2. <span data-ttu-id="35bd9-173">Pasirinkite kandidato įrašą.</span><span class="sxs-lookup"><span data-stu-id="35bd9-173">Select a candidate record.</span></span>

3. <span data-ttu-id="35bd9-174">Pasirinkite **Keisti etapą** ir pasirinkite **Pasamdytas**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-174">Select **Change stage**, and then select **Hired**.</span></span>

4. <span data-ttu-id="35bd9-175">Kandidato daugtaškio meniu (**...**) pasirinkite **Eksportuoti į HRIS**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-175">On the ellipsis menu (**...**) for the candidate, select **Export to HRIS**.</span></span>

5. <span data-ttu-id="35bd9-176">Srityje **Eksportuoti į HRIS** įveskite informaciją, kurią reikia eksportuoti.</span><span class="sxs-lookup"><span data-stu-id="35bd9-176">In the **Export to HRIS** pane, enter the information that must be exported:</span></span>

    - <span data-ttu-id="35bd9-177">Lauke **HRIS teikėjas** pasirinkite **„Microsoft Dynamics 365 Human Resources”**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-177">In the **HRIS provider** field, select **Microsoft Dynamics 365 Human Resources**.</span></span>
    - <span data-ttu-id="35bd9-178">Lauke **Pradžios data** pasirinkite naujo darbuotojo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="35bd9-178">In the **Start date** field, select a value for the new employee.</span></span>
    - <span data-ttu-id="35bd9-179">Lauke **Pareigos** įveskite naujo darbuotojo pareigas.</span><span class="sxs-lookup"><span data-stu-id="35bd9-179">In the **Job title** field, enter a job title for the new employee's job.</span></span>
    - <span data-ttu-id="35bd9-180">Lauke **Vieta** įveskite vietą, kurioje darbuotojas dirbs.</span><span class="sxs-lookup"><span data-stu-id="35bd9-180">In the **Location** field, enter the location where the employee will be based.</span></span>
    - <span data-ttu-id="35bd9-181">Įveskite arba patvirtinkite darbuotojo el. pašto adresą.</span><span class="sxs-lookup"><span data-stu-id="35bd9-181">Enter or verify the employee's email address.</span></span>

![Sritis Eksportuoti į HRIS, esanti „LinkedIn Talent Hub”](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a><span data-ttu-id="35bd9-183">Parengimo užbaigimas „Human Resources”</span><span class="sxs-lookup"><span data-stu-id="35bd9-183">Complete onboarding in Human Resources</span></span>

<span data-ttu-id="35bd9-184">Kandidatų įrašai, eksportuoti iš „LinkedIn Talent Hub” į „Human Resources”, atsiranda puslapio **Personalo valdymas** dalyje **Samdytini kandidatai**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-184">Candidate records that are exported from LinkedIn Talent Hub to Human Resources appear in the **Candidates to hire** section of the **Personnel management** page.</span></span>

1. <span data-ttu-id="35bd9-185">„Human Resources“ atidarykite puslapį **Personalo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-185">In Human Resources, open the **Personnel management** page.</span></span>

2. <span data-ttu-id="35bd9-186">Dalyje **Samdytini kandidatai** pasirinkite pasirinkto kandidato parinktį **Samdyti**.</span><span class="sxs-lookup"><span data-stu-id="35bd9-186">In the **Candidates to hire** section, select **Hire** for the selected candidate.</span></span>

3. <span data-ttu-id="35bd9-187">Dialogo lange **Samdyti naują darbuotoją** peržiūrėkite įrašą ir įtraukite reikiamos informacijos.</span><span class="sxs-lookup"><span data-stu-id="35bd9-187">In the **Hire new worker** dialog box, review the record, and add any required information.</span></span> <span data-ttu-id="35bd9-188">Taip pat galite pasirinkti pareigų numerį, kuriam kandidatas buvo pasamdytas.</span><span class="sxs-lookup"><span data-stu-id="35bd9-188">You can also select the position number that the candidate has been hired for.</span></span>

<span data-ttu-id="35bd9-189">Įvedę reikiamą informaciją, galite tęsti jūsų standartinius darbuotojų įrašų kūrimo ir darbuotojų parengimo procesus.</span><span class="sxs-lookup"><span data-stu-id="35bd9-189">After the required information has been entered, you can continue with your standard processes for creating employee records and onboarding employees.</span></span>

<span data-ttu-id="35bd9-190">Toliau pateikta informacija importuojama ir įtraukiama į naują darbuotojo įrašą.</span><span class="sxs-lookup"><span data-stu-id="35bd9-190">The following details are imported and included on the new employee record:</span></span>

- <span data-ttu-id="35bd9-191">Vardas</span><span class="sxs-lookup"><span data-stu-id="35bd9-191">First name</span></span>
- <span data-ttu-id="35bd9-192">Pavardė</span><span class="sxs-lookup"><span data-stu-id="35bd9-192">Last name</span></span>
- <span data-ttu-id="35bd9-193">Įdarbinimo pradžios data</span><span class="sxs-lookup"><span data-stu-id="35bd9-193">Employment start date</span></span>
- <span data-ttu-id="35bd9-194">El. pašto adresas</span><span class="sxs-lookup"><span data-stu-id="35bd9-194">Email address</span></span>
- <span data-ttu-id="35bd9-195">Telefono numeris</span><span class="sxs-lookup"><span data-stu-id="35bd9-195">Phone number</span></span>

## <a name="see-also"></a><span data-ttu-id="35bd9-196">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="35bd9-196">See also</span></span>

[<span data-ttu-id="35bd9-197">Konfigūruokite „Dataverse“ virtualias lenteles</span><span class="sxs-lookup"><span data-stu-id="35bd9-197">Configure Dataverse virtual tables</span></span>](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="35bd9-198">Kas yra „Microsoft Dataverse“?</span><span class="sxs-lookup"><span data-stu-id="35bd9-198">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)


[!INCLUDE[footer-include](../includes/footer-banner.md)]