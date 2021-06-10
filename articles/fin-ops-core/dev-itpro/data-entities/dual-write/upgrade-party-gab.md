---
title: Naujinimas į šalies ir visuotinės adresų knygelės modelius
description: Šioje temoje aprašoma, kaip atnaujinti dvigubo rašymo į šalies ir visuotinės adresų knygelės modelius duomenis.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 90ddbe704ab21d62752b581a813601e8986c2103
ms.sourcegitcommit: 180548e3c10459776cf199989d3753e0c1555912
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/28/2021
ms.locfileid: "6112678"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="29f58-103">Naujinimas į šalies ir visuotinės adresų knygelės modelį</span><span class="sxs-lookup"><span data-stu-id="29f58-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="29f58-104">[„Microsoft Azure” duomenų gamyklos šablonas](https://aka.ms/dual-write-gab-adf) padeda jums atnaujinti esamus **Paskyros**, **Kontakto** ir **Tiekėjo** lentelių duomenis dvigubame rašyme į šalies ir visuotinės adresų knygelės modelius.</span><span class="sxs-lookup"><span data-stu-id="29f58-104">The [Microsoft Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="29f58-105">Šablonas suderina duomenis iš „Finance and Operations” ir „Customer Engagement” programų.</span><span class="sxs-lookup"><span data-stu-id="29f58-105">The template reconciles the data from both finance and operations apps and customer engagement applications.</span></span> <span data-ttu-id="29f58-106">Proceso pabaigoje bus sukurti laukai **Šalis** ir **Kontaktai**, skirti **Šalies** įrašams, ir tie laukai bus susieti su **Paskyros**, **Kontakto** ir **Tiekėjo** įrašais „Customer Engagement” programose.</span><span class="sxs-lookup"><span data-stu-id="29f58-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="29f58-107">Sugeneruojamas .csv failas („`FONewParty.csv`”), kad „Finance and Operations” programoje būtų galima kurti naujus **Šalies** įrašus.</span><span class="sxs-lookup"><span data-stu-id="29f58-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the finance and operations app.</span></span> <span data-ttu-id="29f58-108">Šioje temoje pateikiamos instrukcijos apie tai, kaip naudoti Duomenų gamyklos šabloną ir atnaujinti savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="29f58-108">This topic provides instructions about how to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="29f58-109">Jei neturite jokių tinkinimų, galite naudoti šabloną tokį, koks jis ir yra.</span><span class="sxs-lookup"><span data-stu-id="29f58-109">If you don’t have any customizations, you can use the template as is.</span></span> <span data-ttu-id="29f58-110">Jei laukams **Paskyra**, **Kontaktas** ir **Tiekėjas** turite tinkinimus, tada turite modifikuoti šabloną pagal šias instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="29f58-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!NOTE]
> <span data-ttu-id="29f58-111">Šablonas atnaujina tik **Šalies** duomenis.</span><span class="sxs-lookup"><span data-stu-id="29f58-111">The template only upgrades the **Party** data.</span></span> <span data-ttu-id="29f58-112">Būsimame leidime bus įtraukti pašto ir elektroniniai adresai.</span><span class="sxs-lookup"><span data-stu-id="29f58-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="29f58-113">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="29f58-113">Prerequisites</span></span>

<span data-ttu-id="29f58-114">Norint atnaujinti šalies ir visuotinės adresų knygelės modelius, reikalingi šie būtinieji komponentai:</span><span class="sxs-lookup"><span data-stu-id="29f58-114">The following prerequisites are required to upgrade to the party and global address book model:</span></span>

+ [<span data-ttu-id="29f58-115">„Azure” prenumerata</span><span class="sxs-lookup"><span data-stu-id="29f58-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="29f58-116">Prieiga prie šablono</span><span class="sxs-lookup"><span data-stu-id="29f58-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="29f58-117">Privalote būti dvigubo rašymo klientas.</span><span class="sxs-lookup"><span data-stu-id="29f58-117">You must be an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="29f58-118">Parengimas atnaujinimui</span><span class="sxs-lookup"><span data-stu-id="29f58-118">Prepare for the upgrade</span></span>
<span data-ttu-id="29f58-119">Pasiruošti atnaujinimui reikalingos toliau nurodytų veiklos:</span><span class="sxs-lookup"><span data-stu-id="29f58-119">The following activities are needed to prepare for the upgrade:</span></span>

+ <span data-ttu-id="29f58-120">**Visiškas sinchronizavimas**: Abi aplinkos yra visiškai sinchronizuotoje būsenoje lakuose **Paskyra (Klientas)**, **Kontaktas** ir **Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="29f58-120">**Fully synced**: Both environments are in a fully synced state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="29f58-121">**Integravimo raktai**: lentelės **Paskyra (Klientas)**, **Kontaktas** ir **Tiekėjas** „Customer Engagement” programose naudoja integravimo raktus, kurie yra visiškai parengti naudoti.</span><span class="sxs-lookup"><span data-stu-id="29f58-121">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="29f58-122">Jeigu tinkinote integravimo raktus, turite tinkinti ir šabloną.</span><span class="sxs-lookup"><span data-stu-id="29f58-122">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="29f58-123">**Šalies numeris**: Visi laukų **Paskyra (Klientas)**, **Kontaktas** ir **Tiekėjas** įrašai, kurie bus išplėtoti, turi **Šalies** numerį.</span><span class="sxs-lookup"><span data-stu-id="29f58-123">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="29f58-124">Įrašų, neturinčių **Šalies** numerio, bus nepaisoma.</span><span class="sxs-lookup"><span data-stu-id="29f58-124">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="29f58-125">Jeigu norite išplėtoti šiuos įrašus, prieš pradėdami plėtojimo procesą, į juos įtraukite **Šalies** numerį.</span><span class="sxs-lookup"><span data-stu-id="29f58-125">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="29f58-126">**Sistemos triktis**: Plėtojimo proceso metu turėsite atjungti „Finance and Operations” ir „Customer Engagement” aplinkas.</span><span class="sxs-lookup"><span data-stu-id="29f58-126">**System outage**: During the upgrade process, you will have to take both the finance and operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="29f58-127">**Momentinė kopija**: Pasidarykite „Finance and Operations” ir „Customer Engagement” programų momentines kopijas.</span><span class="sxs-lookup"><span data-stu-id="29f58-127">**Snapshot**: Take snapshots of both the finance and operations apps and customer engagement apps.</span></span> <span data-ttu-id="29f58-128">Naudokite momentines kopijas ankstesnės būsenos atkūrimui, jei to reikia.</span><span class="sxs-lookup"><span data-stu-id="29f58-128">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="29f58-129">Visuotinis diegimas</span><span class="sxs-lookup"><span data-stu-id="29f58-129">Deployment</span></span>

1. <span data-ttu-id="29f58-130">Atsisiųskite šabloną iš [„Dynamics-365-FastTrack-Implementation-Assets”](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="29f58-130">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="29f58-131">Prisijunkite prie [„Microsoft Azure”](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="29f58-131">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="29f58-132">Sukurkite [išteklių grupę](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="29f58-132">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="29f58-133">Sukurkite [saugyklos paskyrą](/azure/storage/common/storage-account-create?tabs=azure-portal) jūsų sukurtoje išteklių grupėje.</span><span class="sxs-lookup"><span data-stu-id="29f58-133">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="29f58-134">Sukurkite [duomenų gamyklą](/azure/data-factory/quickstart-create-data-factory-portal) aukščiau jūsų sukurtoje išteklių grupėje.</span><span class="sxs-lookup"><span data-stu-id="29f58-134">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="29f58-135">Atidarykite duomenų gamyklą ir pasirinkite **Kurti & Stebėti** plytelę.</span><span class="sxs-lookup"><span data-stu-id="29f58-135">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="29f58-136">Skirtuke **Valdyti** pasirinkite **ARM šablonas**.</span><span class="sxs-lookup"><span data-stu-id="29f58-136">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="29f58-137">Pasirinkite **Importuoti ARM šabloną**, kad importuotumėte **Šalies** šabloną.</span><span class="sxs-lookup"><span data-stu-id="29f58-137">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="29f58-138">Importuokite šabloną į duomenų gamyklą.</span><span class="sxs-lookup"><span data-stu-id="29f58-138">Import the template into the data factory.</span></span> <span data-ttu-id="29f58-139">Įveskite šias reikšmes laukams **Projekto informacija** ir **Egzemplioriaus informacija**.</span><span class="sxs-lookup"><span data-stu-id="29f58-139">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="29f58-140">Laukas</span><span class="sxs-lookup"><span data-stu-id="29f58-140">Field</span></span> | <span data-ttu-id="29f58-141">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="29f58-141">Value</span></span>
    ---|---
    <span data-ttu-id="29f58-142">Prenumerata</span><span class="sxs-lookup"><span data-stu-id="29f58-142">Subscription</span></span> | <span data-ttu-id="29f58-143">„Azure” prenumerata</span><span class="sxs-lookup"><span data-stu-id="29f58-143">Azure subscription</span></span>
    <span data-ttu-id="29f58-144">Išteklių grupė</span><span class="sxs-lookup"><span data-stu-id="29f58-144">Resource group</span></span> | <span data-ttu-id="29f58-145">Pateikite tuos pačius išteklius, kuriuose sukurta saugyklos paskyra.</span><span class="sxs-lookup"><span data-stu-id="29f58-145">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="29f58-146">Regionas</span><span class="sxs-lookup"><span data-stu-id="29f58-146">Region</span></span> | <span data-ttu-id="29f58-147">Nurodykite regioną.</span><span class="sxs-lookup"><span data-stu-id="29f58-147">Specify region.</span></span>
    <span data-ttu-id="29f58-148">Gamyklos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-148">Factory Name</span></span> | <span data-ttu-id="29f58-149">Nurodykite gamyklos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="29f58-149">Specify factory name.</span></span>
    <span data-ttu-id="29f58-150">Su FO susietas „Service_service” pagrindinis raktas</span><span class="sxs-lookup"><span data-stu-id="29f58-150">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="29f58-151">Nurodykite programos raktą.</span><span class="sxs-lookup"><span data-stu-id="29f58-151">Specify the application's key.</span></span>
    <span data-ttu-id="29f58-152">„Azure Blob Storage_connection String”</span><span class="sxs-lookup"><span data-stu-id="29f58-152">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="29f58-153">„Azure“ didelių dvejetainių objektų saugyklos ryšio eilutė.</span><span class="sxs-lookup"><span data-stu-id="29f58-153">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="29f58-154">Su „Dynamics CRM” susietas „Service_password”</span><span class="sxs-lookup"><span data-stu-id="29f58-154">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="29f58-155">Vartotojo paskyros, kurią nurodėte kaip vartotojo vardą, slaptažodis.</span><span class="sxs-lookup"><span data-stu-id="29f58-155">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="29f58-156">Su FO susietas „Service_properties_type” „Properties_url”</span><span class="sxs-lookup"><span data-stu-id="29f58-156">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="29f58-157">Su FO susietas „Service_properties_type” „Properties_tenant”</span><span class="sxs-lookup"><span data-stu-id="29f58-157">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="29f58-158">Nurodykite nuomotojo informaciją (domeno vardą ar nuomotojo ID), pagal kurią egzistuoja jūsų programa.</span><span class="sxs-lookup"><span data-stu-id="29f58-158">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="29f58-159">Su FO susietas „Service_properties_type” „Properties_aad Resource Id”</span><span class="sxs-lookup"><span data-stu-id="29f58-159">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="29f58-160">Su FO susietas „Service_properties_type” „Properties_service Principal Id”</span><span class="sxs-lookup"><span data-stu-id="29f58-160">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="29f58-161">Nurodykite programos kliento ID.</span><span class="sxs-lookup"><span data-stu-id="29f58-161">Specify the application's client ID.</span></span>
    <span data-ttu-id="29f58-162">Su „Dynamics CRM” susietas „Service_properties_type” „Properties_username”</span><span class="sxs-lookup"><span data-stu-id="29f58-162">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="29f58-163">Vartotojo vardas, skirtas prisijungti prie „Dynamics 365”.</span><span class="sxs-lookup"><span data-stu-id="29f58-163">The username to connect to Dynamics 365.</span></span>

    <span data-ttu-id="29f58-164">Papildomos informacijos ieškokite toliau pateiktose temose:</span><span class="sxs-lookup"><span data-stu-id="29f58-164">For additional information, refer to the following topics:</span></span> 
    
    - [<span data-ttu-id="29f58-165">„Resource Manager” šablono skatinimas rankiniu būdu kiekvienai aplinkai</span><span class="sxs-lookup"><span data-stu-id="29f58-165">Manually promote a Resource Manager template for each environment</span></span>](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [<span data-ttu-id="29f58-166">Susietosios tarnybos ypatybės</span><span class="sxs-lookup"><span data-stu-id="29f58-166">Linked service properties</span></span>](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [<span data-ttu-id="29f58-167">Duomenų kopijavimas naudojant „Azure Data Factory”</span><span class="sxs-lookup"><span data-stu-id="29f58-167">Copy data using Azure Data Factory</span></span>](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. <span data-ttu-id="29f58-168">Atlikę diegimą, patikrinkite duomenų rinkinius, duomenų srautą ir susietą duomenų gamyklos paslaugą.</span><span class="sxs-lookup"><span data-stu-id="29f58-168">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Duomenų rinkiniai, duomenų srautas ir susieta paslauga](media/data-factory-validate.png)

11. <span data-ttu-id="29f58-170">Pereikite prie **Valdyti**.</span><span class="sxs-lookup"><span data-stu-id="29f58-170">Navigate to **Manage**.</span></span> <span data-ttu-id="29f58-171">Dalyje **Ryšiai** pasirinkite **Susieta paslauga**.</span><span class="sxs-lookup"><span data-stu-id="29f58-171">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="29f58-172">Pasirinkite **„DynamicsCrmLinkedService”**.</span><span class="sxs-lookup"><span data-stu-id="29f58-172">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="29f58-173">Formoje **Redaguoti susietą paslaugą („Dynamics CRM”)** įveskite šias reikšmes.</span><span class="sxs-lookup"><span data-stu-id="29f58-173">In the **Edit linked service (Dynamics CRM)** form, enter the following values.</span></span>

    <span data-ttu-id="29f58-174">Laukas</span><span class="sxs-lookup"><span data-stu-id="29f58-174">Field</span></span> | <span data-ttu-id="29f58-175">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="29f58-175">Value</span></span>
    ---|---
    <span data-ttu-id="29f58-176">Pavadinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-176">Name</span></span> | <span data-ttu-id="29f58-177">„DynamicsCrmLinkedService”</span><span class="sxs-lookup"><span data-stu-id="29f58-177">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="29f58-178">Aprašas</span><span class="sxs-lookup"><span data-stu-id="29f58-178">Description</span></span> | <span data-ttu-id="29f58-179">Susietos paslaugos, skirtos prisijungti prie CRM egzemplioriaus, kad būtų galima iškviesti objektų duomenis</span><span class="sxs-lookup"><span data-stu-id="29f58-179">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="29f58-180">Prisijungti per integracijos vykdymą</span><span class="sxs-lookup"><span data-stu-id="29f58-180">Connect via integration runtime</span></span> | <span data-ttu-id="29f58-181">„AutoResolvelntegrationRuntime”</span><span class="sxs-lookup"><span data-stu-id="29f58-181">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="29f58-182">Diegimo tipas</span><span class="sxs-lookup"><span data-stu-id="29f58-182">Deployment type</span></span> | <span data-ttu-id="29f58-183">Internete</span><span class="sxs-lookup"><span data-stu-id="29f58-183">Online</span></span>
    <span data-ttu-id="29f58-184">Paslaugos Uri</span><span class="sxs-lookup"><span data-stu-id="29f58-184">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="29f58-185">Autentifikavimo tipas</span><span class="sxs-lookup"><span data-stu-id="29f58-185">Authentication type</span></span> | <span data-ttu-id="29f58-186">„Office365”</span><span class="sxs-lookup"><span data-stu-id="29f58-186">Office365</span></span>
    <span data-ttu-id="29f58-187">Vartotojo vardas</span><span class="sxs-lookup"><span data-stu-id="29f58-187">User name</span></span> |
    <span data-ttu-id="29f58-188">Slaptažodis arba „Azure” raktų saugykla</span><span class="sxs-lookup"><span data-stu-id="29f58-188">Password or Azure Key Vault</span></span> | <span data-ttu-id="29f58-189">Slaptažodis</span><span class="sxs-lookup"><span data-stu-id="29f58-189">Password</span></span>
    <span data-ttu-id="29f58-190">Slaptažodis</span><span class="sxs-lookup"><span data-stu-id="29f58-190">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="29f58-191">Šablono vykdymas</span><span class="sxs-lookup"><span data-stu-id="29f58-191">Run the template</span></span>

1. <span data-ttu-id="29f58-192">Sustabdykite **Paskyros**, **Kontakto** ir **Tiekėjo** dvigubo rašymo susiejimus naudodami „Finance and Operations” programą.</span><span class="sxs-lookup"><span data-stu-id="29f58-192">Stop the following **Account**, **Contact**, and **Vendor** dual-write maps using the Finance and Operations app.</span></span>

    + <span data-ttu-id="29f58-193">Klientai V3(paskyros)</span><span class="sxs-lookup"><span data-stu-id="29f58-193">Customers V3(accounts)</span></span>
    + <span data-ttu-id="29f58-194">Klientai V3(kontaktai)</span><span class="sxs-lookup"><span data-stu-id="29f58-194">Customers V3(contacts)</span></span>
    + <span data-ttu-id="29f58-195">„CDS” kontaktai V2(kontaktai)</span><span class="sxs-lookup"><span data-stu-id="29f58-195">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="29f58-196">„CDS” kontaktai V2(kontaktai)</span><span class="sxs-lookup"><span data-stu-id="29f58-196">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="29f58-197">Tiekėjas V2 („msdyn_vendor”)</span><span class="sxs-lookup"><span data-stu-id="29f58-197">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="29f58-198">Užtikrinkite, kad susiejimai yra pašalinti iš „Dataverse” lentelės `msdy_dualwriteruntimeconfig`.</span><span class="sxs-lookup"><span data-stu-id="29f58-198">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="29f58-199">Įdiekite [Dvigubo rašymo į Šalies ir Visuotinę adresų knygelė sprendimus](https://aka.ms/dual-write-gab) iš „AppSource”.</span><span class="sxs-lookup"><span data-stu-id="29f58-199">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="29f58-200">Jei šiose „Finance and Operations” programos lentelėse yra duomenų, tada joms paleiskite **Pradinį sinchronizavimą**.</span><span class="sxs-lookup"><span data-stu-id="29f58-200">In the finance and operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="29f58-201">Pasisveikinimai</span><span class="sxs-lookup"><span data-stu-id="29f58-201">Salutations</span></span>
    + <span data-ttu-id="29f58-202">Asmeninių savybių tipai</span><span class="sxs-lookup"><span data-stu-id="29f58-202">Personal character types</span></span>
    + <span data-ttu-id="29f58-203">Baigiamoji mandagumo frazė</span><span class="sxs-lookup"><span data-stu-id="29f58-203">Complimentary closing</span></span>
    + <span data-ttu-id="29f58-204">Kontaktinio asmens pareigos</span><span class="sxs-lookup"><span data-stu-id="29f58-204">Contact person titles</span></span>
    + <span data-ttu-id="29f58-205">Sprendimų priėmimo vaidmenys</span><span class="sxs-lookup"><span data-stu-id="29f58-205">Decision making roles</span></span>
    + <span data-ttu-id="29f58-206">Lojalumo lygiai</span><span class="sxs-lookup"><span data-stu-id="29f58-206">Loyalty levels</span></span>

5. <span data-ttu-id="29f58-207">„Customer Engagement” programoje išjunkite šiuos papildinio veiksmus.</span><span class="sxs-lookup"><span data-stu-id="29f58-207">In the customer engagement app, disable the following plug-in steps.</span></span>

    + <span data-ttu-id="29f58-208">Paskyros atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-208">Account Update</span></span>
         + <span data-ttu-id="29f58-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Paskyros atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="29f58-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Paskyros atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="29f58-211">Kontakto atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-211">Contact Update</span></span>
         + <span data-ttu-id="29f58-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Kontakto atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="29f58-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Kontakto atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="29f58-214">msdyn_party Atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-214">msdyn_party Update</span></span>
         + <span data-ttu-id="29f58-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="29f58-216">msdyn_vendor Atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-216">msdyn_vendor Update</span></span>
         + <span data-ttu-id="29f58-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="29f58-218">„Customer Engagement” programoje uždrauskite šias darbo eigas:</span><span class="sxs-lookup"><span data-stu-id="29f58-218">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="29f58-219">Tiekėjų kūrimas lentelėje Klientai</span><span class="sxs-lookup"><span data-stu-id="29f58-219">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="29f58-220">Tiekėjų kūrimas lentelėje Klientai</span><span class="sxs-lookup"><span data-stu-id="29f58-220">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="29f58-221">Tiekėjų kūrimas asmens tipo lentelėje Kontaktai</span><span class="sxs-lookup"><span data-stu-id="29f58-221">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="29f58-222">Tiekėjų kūrimas tipo Asmuo lentelėje Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="29f58-222">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="29f58-223">Tiekėjų naujinimas lentelėje Klientai</span><span class="sxs-lookup"><span data-stu-id="29f58-223">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="29f58-224">Tiekėjų naujinimas lentelėje Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="29f58-224">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="29f58-225">Tiekėjų naujinimas tipo Asmuo lentelėje Kontaktai</span><span class="sxs-lookup"><span data-stu-id="29f58-225">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="29f58-226">Tiekėjų naujinimas tipo Asmuo lentelėje Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="29f58-226">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="29f58-227">Duomenų gamykloje vykdykite šabloną pasirinkdami **Paleisti dabar**, kaip parodyta šiame paveikslėlyje.</span><span class="sxs-lookup"><span data-stu-id="29f58-227">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="29f58-228">Šis procesas gali užtrukti keletą valandų, priklausomai nuo duomenų tūrio.</span><span class="sxs-lookup"><span data-stu-id="29f58-228">This process might take a few hours to complete based on the data volume.</span></span>

    ![Paleidiklio vykdymas](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="29f58-230">Jei laukams **Paskyra**, **Kontaktas** ir **Tiekėjas** turite tinkinimus, tada jums reikia modifikuoti šabloną.</span><span class="sxs-lookup"><span data-stu-id="29f58-230">If you have customizations for **Account**, **Contact**, and **Vendor**, then you need to modify the template.</span></span>

8. <span data-ttu-id="29f58-231">Importuokite naujus **Šalies** įrašus „Finance and Operations” programoje.</span><span class="sxs-lookup"><span data-stu-id="29f58-231">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="29f58-232">Atsisiųskite `FONewParty.csv` failą iš „Azure“ didelių dvejetainių objektų saugyklos.</span><span class="sxs-lookup"><span data-stu-id="29f58-232">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="29f58-233">Kelias yra `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="29f58-233">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="29f58-234">Konvertuokite „`FONewParty.csv`” failą į „Excel” failą ir importuokite „Excel” failą į „Finance and Operations” programą.</span><span class="sxs-lookup"><span data-stu-id="29f58-234">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the finance and operations app.</span></span> <span data-ttu-id="29f58-235">Jei csv importavimas jums tinka, galite importuoti csv failą tiesiogiai.</span><span class="sxs-lookup"><span data-stu-id="29f58-235">If the csv import works for you, you can import the csv file directly.</span></span> <span data-ttu-id="29f58-236">Importavimas gali užtrukti kelias valandas, priklausomai nuo duomenų tūrio.</span><span class="sxs-lookup"><span data-stu-id="29f58-236">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="29f58-237">Daugiau informacijos rasite [Duomenų importavimo ir eksportavimo užduočių apžvalga](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="29f58-237">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![„Dataverse” šalies įrašų importavimas](media/data-factory-import-party.png)

9. <span data-ttu-id="29f58-239">„Customer Engagement” programose įgalinkite šiuos papildinio veiksmus:</span><span class="sxs-lookup"><span data-stu-id="29f58-239">In the customer engagement apps, enable the following plug-in steps:</span></span>

    + <span data-ttu-id="29f58-240">Paskyros atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-240">Account Update</span></span>
         + <span data-ttu-id="29f58-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Paskyros atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="29f58-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Paskyros atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="29f58-243">Kontakto atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-243">Contact Update</span></span>
         + <span data-ttu-id="29f58-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Kontakto atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="29f58-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Kontakto atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="29f58-246">msdyn_party Atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-246">msdyn_party Update</span></span>
         + <span data-ttu-id="29f58-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="29f58-248">msdyn_vendor Atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-248">msdyn_vendor Update</span></span>
         + <span data-ttu-id="29f58-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="29f58-250">„Customer Engagement” suaktyvinkite šias darbo eigas, jei išjungėte jas ankstesniais veiksmais:</span><span class="sxs-lookup"><span data-stu-id="29f58-250">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="29f58-251">Tiekėjų kūrimas lentelėje Klientai</span><span class="sxs-lookup"><span data-stu-id="29f58-251">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="29f58-252">Tiekėjų kūrimas lentelėje Klientai</span><span class="sxs-lookup"><span data-stu-id="29f58-252">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="29f58-253">Tiekėjų kūrimas asmens tipo lentelėje Kontaktai</span><span class="sxs-lookup"><span data-stu-id="29f58-253">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="29f58-254">Tiekėjų kūrimas tipo Asmuo lentelėje Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="29f58-254">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="29f58-255">Tiekėjų naujinimas lentelėje Klientai</span><span class="sxs-lookup"><span data-stu-id="29f58-255">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="29f58-256">Tiekėjų naujinimas lentelėje Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="29f58-256">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="29f58-257">Tiekėjų naujinimas tipo Asmuo lentelėje Kontaktai</span><span class="sxs-lookup"><span data-stu-id="29f58-257">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="29f58-258">Tiekėjų naujinimas tipo Asmuo lentelėje Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="29f58-258">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="29f58-259">Vykdykite su **Šalimi** susijusias schemas, kaip nurodyta [Šalies ir visuotinėje adresų knygelėje](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="29f58-259">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="29f58-260">Trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="29f58-260">Troubleshooting</span></span>

1. <span data-ttu-id="29f58-261">Jeigu procesas nepavyksta, iš naujo paleiskite duomenų gamyklą, pradedant nuo nesėkmingos veiklos.</span><span class="sxs-lookup"><span data-stu-id="29f58-261">If the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="29f58-262">Kai kuriuos duomenų gamyklos sugeneruotus failus galite naudoti duomenų tikrinimo tikslais.</span><span class="sxs-lookup"><span data-stu-id="29f58-262">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="29f58-263">Duomenų gamykla veikia pagal kableliais atskirtus csv failus.</span><span class="sxs-lookup"><span data-stu-id="29f58-263">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="29f58-264">Jeigu kuri nors lauko vertė turi kablelius, tai gali trukdyti rezultatams.</span><span class="sxs-lookup"><span data-stu-id="29f58-264">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="29f58-265">Jums reikia pašalinti kablelius.</span><span class="sxs-lookup"><span data-stu-id="29f58-265">You need to remove the commas.</span></span>
4. <span data-ttu-id="29f58-266">Skirtuke **Stebėjimas** pateikiama informacija apie visus veiksmus ir apdorotus duomenis.</span><span class="sxs-lookup"><span data-stu-id="29f58-266">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="29f58-267">Pasirinkite konkretų veiksmą jo suderinimui.</span><span class="sxs-lookup"><span data-stu-id="29f58-267">Select a specific step to debug it.</span></span>

    ![Stebėjimo skirtukas](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="29f58-269">Sužinokite daugiau apie šabloną</span><span class="sxs-lookup"><span data-stu-id="29f58-269">Learn more about the template</span></span>

<span data-ttu-id="29f58-270">Papildomos informacijos apie šabloną galite rasti [Komentarai apie „Azure Data Factory” šabloną „readme” faile](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span><span class="sxs-lookup"><span data-stu-id="29f58-270">You can find additional information about the template in [Comments for Azure Data Factory template readme](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span></span>
