---
title: Naujinimas į šalies ir visuotinės adresų knygelės modelius
description: Šioje temoje aprašoma, kaip atnaujinti dvigubo rašymo į šalies ir visuotinės adresų knygelės modelius duomenis.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 32128d48bfac195530d70b60e67cfd4921fc001e
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941088"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="96abf-103">Naujinimas į šalies ir visuotinės adresų knygelės modelius</span><span class="sxs-lookup"><span data-stu-id="96abf-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="96abf-104">[„Azure” duomenų gamyklos šablonas](https://aka.ms/dual-write-gab-adf) padeda jums atnaujinti esamus **Paskyros**, **Kontakto** ir **Tiekėjo** lentelės duomenis dvigubame rašyme į šalies ir visuotinės adresų knygelės modelius.</span><span class="sxs-lookup"><span data-stu-id="96abf-104">The [Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="96abf-105">Šablonas suderina duomenis iš „Finance and Operations” ir „Customer Engagement” programų.</span><span class="sxs-lookup"><span data-stu-id="96abf-105">The template reconciles the data from both Finance and Operations apps and customer engagement applications.</span></span> <span data-ttu-id="96abf-106">Proceso pabaigoje bus sukurti laukai **Šalis** ir **Kontaktai**, skirti **Šalies** įrašams, ir tie laukai bus susieti su **Paskyros**, **Kontakto** ir **Tiekėjo** įrašais „Customer Engagement” programose.</span><span class="sxs-lookup"><span data-stu-id="96abf-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="96abf-107">Sugeneruojamas .csv failas (`FONewParty.csv`), kad „Finance and Operations” programoje būtų galima kurti naujus **Šalies** įrašus.</span><span class="sxs-lookup"><span data-stu-id="96abf-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the Finance and Operations app.</span></span> <span data-ttu-id="96abf-108">Šioje temoje pateikiamos instrukcijos, kaip naudoti Duomenų gamyklos šabloną ir atnaujinti savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="96abf-108">This topic provides the instructions to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="96abf-109">Jei neturite jokių tinkinimų, galite naudoti šabloną tokį, koks jis yra.</span><span class="sxs-lookup"><span data-stu-id="96abf-109">If you don’t have any customizations, you can use the template as-is.</span></span> <span data-ttu-id="96abf-110">Jei laukams **Paskyra**, **Kontaktas** ir **Tiekėjas** turite tinkinimus, tada turite modifikuoti šabloną pagal šias instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="96abf-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!Note]
> <span data-ttu-id="96abf-111">Šablonas padeda atnaujinti tik **Šalies** duomenis.</span><span class="sxs-lookup"><span data-stu-id="96abf-111">The template helps to upgrade only the **Party** data.</span></span> <span data-ttu-id="96abf-112">Būsimame leidime bus įtraukti pašto ir elektroniniai adresai.</span><span class="sxs-lookup"><span data-stu-id="96abf-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="96abf-113">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="96abf-113">Prerequisites</span></span>

<span data-ttu-id="96abf-114">Reikalingi šie būtinieji komponentai:</span><span class="sxs-lookup"><span data-stu-id="96abf-114">These prerequisites are required:</span></span>

+ [<span data-ttu-id="96abf-115">„Azure” prenumerata</span><span class="sxs-lookup"><span data-stu-id="96abf-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="96abf-116">Prieiga prie šablono</span><span class="sxs-lookup"><span data-stu-id="96abf-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="96abf-117">Jūs – dvigubo rašymo klientas.</span><span class="sxs-lookup"><span data-stu-id="96abf-117">You are an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="96abf-118">Parengimas atnaujinimui</span><span class="sxs-lookup"><span data-stu-id="96abf-118">Prepare for the upgrade</span></span>

+ <span data-ttu-id="96abf-119">**Visiškai sinchronizuota**: Abi aplinkos yra visiškai sinchronizuotoje būsenoje laukams **Paskyra (Klientas)**, **Kontaktas** ir **Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="96abf-119">**Fully synched**: Both environments are fully synched state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="96abf-120">**Integravimo raktai**: lentelės **Paskyra (Klientas)**, **Kontaktas** ir **Tiekėjas** „Customer Engagement” programose naudoja integravimo raktus, kurie yra visiškai parengti naudoti.</span><span class="sxs-lookup"><span data-stu-id="96abf-120">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="96abf-121">Jeigu tinkinote integravimo raktus, turite tinkinti ir šabloną.</span><span class="sxs-lookup"><span data-stu-id="96abf-121">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="96abf-122">**Šalies numeris**: Visi laukų **Paskyra (Klientas)**, **Kontaktas** ir **Tiekėjas** įrašai, kurie bus išplėtoti, turi **Šalies** numerį.</span><span class="sxs-lookup"><span data-stu-id="96abf-122">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="96abf-123">Įrašų, neturinčių **Šalies** numerio, bus nepaisoma.</span><span class="sxs-lookup"><span data-stu-id="96abf-123">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="96abf-124">Jeigu norite išplėtoti šiuos įrašus, prieš pradėdami plėtojimo procesą, į juos įtraukite **Šalies** numerį.</span><span class="sxs-lookup"><span data-stu-id="96abf-124">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="96abf-125">**Sistemos triktis**: Plėtojimo proceso metu turėsite atjungti „Finance and Operations” ir „Customer Engagement” aplinkas.</span><span class="sxs-lookup"><span data-stu-id="96abf-125">**System outage**: During the upgrade process, you will have to take both the Finance and Operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="96abf-126">**Momentinė kopija**: Pasidarykite „Finance and Operations” ir „Customer Engagement” programų momentines kopijas.</span><span class="sxs-lookup"><span data-stu-id="96abf-126">**Snapshot**: Take snapshots of both the Finance and Operations and customer engagement apps.</span></span> <span data-ttu-id="96abf-127">Naudokite momentines kopijas ankstesnės būsenos atkūrimui, jei to reikia.</span><span class="sxs-lookup"><span data-stu-id="96abf-127">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="96abf-128">Visuotinis diegimas</span><span class="sxs-lookup"><span data-stu-id="96abf-128">Deployment</span></span>

1. <span data-ttu-id="96abf-129">Atsisiųskite šabloną iš [„Dynamics-365-FastTrack-Implementation-Assets”](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="96abf-129">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="96abf-130">Prisijunkite prie [„Microsoft Azure”](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="96abf-130">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="96abf-131">Sukurkite [išteklių grupę](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="96abf-131">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="96abf-132">Sukurkite [saugyklos paskyrą](/azure/storage/common/storage-account-create?tabs=azure-portal) jūsų sukurtoje išteklių grupėje.</span><span class="sxs-lookup"><span data-stu-id="96abf-132">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="96abf-133">Sukurkite [duomenų gamyklą](/azure/data-factory/quickstart-create-data-factory-portal) aukščiau jūsų sukurtoje išteklių grupėje.</span><span class="sxs-lookup"><span data-stu-id="96abf-133">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="96abf-134">Atidarykite duomenų gamyklą ir pasirinkite **Kurti & Stebėti** plytelę.</span><span class="sxs-lookup"><span data-stu-id="96abf-134">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="96abf-135">Skirtuke **Valdyti** pasirinkite **ARM šablonas**.</span><span class="sxs-lookup"><span data-stu-id="96abf-135">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="96abf-136">Pasirinkite **Importuoti ARM šabloną**, kad importuotumėte **Šalies** šabloną.</span><span class="sxs-lookup"><span data-stu-id="96abf-136">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="96abf-137">Importuokite šabloną į duomenų gamyklą.</span><span class="sxs-lookup"><span data-stu-id="96abf-137">Import the template into the data factory.</span></span> <span data-ttu-id="96abf-138">Įveskite šias reikšmes laukams **Projekto informacija** ir **Egzemplioriaus informacija**.</span><span class="sxs-lookup"><span data-stu-id="96abf-138">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="96abf-139">Laukas</span><span class="sxs-lookup"><span data-stu-id="96abf-139">Field</span></span> | <span data-ttu-id="96abf-140">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="96abf-140">Value</span></span>
    ---|---
    <span data-ttu-id="96abf-141">Prenumerata</span><span class="sxs-lookup"><span data-stu-id="96abf-141">Subscription</span></span> | <span data-ttu-id="96abf-142">„Azure” prenumerata</span><span class="sxs-lookup"><span data-stu-id="96abf-142">Azure subscription</span></span>
    <span data-ttu-id="96abf-143">Išteklių grupė</span><span class="sxs-lookup"><span data-stu-id="96abf-143">Resource group</span></span> | <span data-ttu-id="96abf-144">Pateikite tuos pačius išteklius, kuriuose sukurta saugyklos paskyra.</span><span class="sxs-lookup"><span data-stu-id="96abf-144">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="96abf-145">Regionas</span><span class="sxs-lookup"><span data-stu-id="96abf-145">Region</span></span> | <span data-ttu-id="96abf-146">Nurodykite regioną.</span><span class="sxs-lookup"><span data-stu-id="96abf-146">Specify region.</span></span>
    <span data-ttu-id="96abf-147">Gamyklos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-147">Factory Name</span></span> | <span data-ttu-id="96abf-148">Nurodykite gamyklos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="96abf-148">Specify factory name.</span></span>
    <span data-ttu-id="96abf-149">Su FO susietas „Service_service” pagrindinis raktas</span><span class="sxs-lookup"><span data-stu-id="96abf-149">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="96abf-150">Nurodykite programos raktą.</span><span class="sxs-lookup"><span data-stu-id="96abf-150">Specify the application's key.</span></span>
    <span data-ttu-id="96abf-151">„Azure Blob Storage_connection String”</span><span class="sxs-lookup"><span data-stu-id="96abf-151">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="96abf-152">„Azure“ didelių dvejetainių objektų saugyklos ryšio eilutė.</span><span class="sxs-lookup"><span data-stu-id="96abf-152">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="96abf-153">Su „Dynamics CRM” susietas „Service_password”</span><span class="sxs-lookup"><span data-stu-id="96abf-153">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="96abf-154">Vartotojo paskyros, kurią nurodėte kaip vartotojo vardą, slaptažodis.</span><span class="sxs-lookup"><span data-stu-id="96abf-154">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="96abf-155">Su FO susietas „Service_properties_type” „Properties_url”</span><span class="sxs-lookup"><span data-stu-id="96abf-155">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="96abf-156">Su FO susietas „Service_properties_type” „Properties_tenant”</span><span class="sxs-lookup"><span data-stu-id="96abf-156">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="96abf-157">Nurodykite nuomotojo informaciją (domeno vardą ar nuomotojo ID), pagal kurią egzistuoja jūsų programa.</span><span class="sxs-lookup"><span data-stu-id="96abf-157">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="96abf-158">Su FO susietas „Service_properties_type” „Properties_aad Resource Id”</span><span class="sxs-lookup"><span data-stu-id="96abf-158">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="96abf-159">Su FO susietas „Service_properties_type” „Properties_service Principal Id”</span><span class="sxs-lookup"><span data-stu-id="96abf-159">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="96abf-160">Nurodykite programos kliento ID.</span><span class="sxs-lookup"><span data-stu-id="96abf-160">Specify the application's client ID.</span></span>
    <span data-ttu-id="96abf-161">Su „Dynamics CRM” susietas „Service_properties_type” „Properties_username”</span><span class="sxs-lookup"><span data-stu-id="96abf-161">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="96abf-162">Vartotojo vardas, skirtas prisijungti prie „Dynamics”.</span><span class="sxs-lookup"><span data-stu-id="96abf-162">The username to connect to Dynamics.</span></span>

    <span data-ttu-id="96abf-163">Daugiau informacijos rasite [Rankiniu būdu pakelkite „Resource Manager” šabloną į aukštesnį lygį kiekvienai aplinkai](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Susietos paslaugos ypatybės](/azure/data-factory/connector-dynamics-ax#linked-service-properties) ir [Duomenų kopijavimas naudojant „Azure” duomenų gamyklą](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span><span class="sxs-lookup"><span data-stu-id="96abf-163">For more information, see [Manually promote a Resource Manager template for each environment](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Linked service properties](/azure/data-factory/connector-dynamics-ax#linked-service-properties), and [Copy data using Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span></span>

10. <span data-ttu-id="96abf-164">Atlikę diegimą, patikrinkite duomenų rinkinius, duomenų srautą ir susietą duomenų gamyklos paslaugą.</span><span class="sxs-lookup"><span data-stu-id="96abf-164">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Duomenų rinkiniai, duomenų srautas ir susieta paslauga](media/data-factory-validate.png)

11. <span data-ttu-id="96abf-166">Pereikite prie **Valdyti**.</span><span class="sxs-lookup"><span data-stu-id="96abf-166">Navigate to **Manage**.</span></span> <span data-ttu-id="96abf-167">Dalyje **Ryšiai** pasirinkite **Susieta paslauga**.</span><span class="sxs-lookup"><span data-stu-id="96abf-167">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="96abf-168">Pasirinkite **„DynamicsCrmLinkedService”**.</span><span class="sxs-lookup"><span data-stu-id="96abf-168">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="96abf-169">Formoje **Redaguoti susietą paslaugą („Dynamics CRM”)** įveskite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="96abf-169">In the **Edit linked service (Dynamics CRM)** form, enter the following values:</span></span>

    <span data-ttu-id="96abf-170">Laukas</span><span class="sxs-lookup"><span data-stu-id="96abf-170">Field</span></span> | <span data-ttu-id="96abf-171">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="96abf-171">Value</span></span>
    ---|---
    <span data-ttu-id="96abf-172">Pavadinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-172">Name</span></span> | <span data-ttu-id="96abf-173">„DynamicsCrmLinkedService”</span><span class="sxs-lookup"><span data-stu-id="96abf-173">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="96abf-174">Aprašas</span><span class="sxs-lookup"><span data-stu-id="96abf-174">Description</span></span> | <span data-ttu-id="96abf-175">Susietos paslaugos, skirtos prisijungti prie CRM egzemplioriaus, kad būtų galima iškviesti objektų duomenis</span><span class="sxs-lookup"><span data-stu-id="96abf-175">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="96abf-176">Prisijungti per integracijos vykdymą</span><span class="sxs-lookup"><span data-stu-id="96abf-176">Connect via integration runtime</span></span> | <span data-ttu-id="96abf-177">„AutoResolvelntegrationRuntime”</span><span class="sxs-lookup"><span data-stu-id="96abf-177">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="96abf-178">Diegimo tipas</span><span class="sxs-lookup"><span data-stu-id="96abf-178">Deployment type</span></span> | <span data-ttu-id="96abf-179">Internete</span><span class="sxs-lookup"><span data-stu-id="96abf-179">Online</span></span>
    <span data-ttu-id="96abf-180">Paslaugos Uri</span><span class="sxs-lookup"><span data-stu-id="96abf-180">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="96abf-181">Autentifikavimo tipas</span><span class="sxs-lookup"><span data-stu-id="96abf-181">Authentication type</span></span> | <span data-ttu-id="96abf-182">„Office365”</span><span class="sxs-lookup"><span data-stu-id="96abf-182">Office365</span></span>
    <span data-ttu-id="96abf-183">Vartotojo vardas</span><span class="sxs-lookup"><span data-stu-id="96abf-183">User name</span></span> |
    <span data-ttu-id="96abf-184">Slaptažodis arba „Azure” raktų saugykla</span><span class="sxs-lookup"><span data-stu-id="96abf-184">Password or Azure Key Vault</span></span> | <span data-ttu-id="96abf-185">Slaptažodis</span><span class="sxs-lookup"><span data-stu-id="96abf-185">Password</span></span>
    <span data-ttu-id="96abf-186">Slaptažodis</span><span class="sxs-lookup"><span data-stu-id="96abf-186">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="96abf-187">Šablono vykdymas</span><span class="sxs-lookup"><span data-stu-id="96abf-187">Run the template</span></span>

1. <span data-ttu-id="96abf-188">Sustabdykite **Paskyros**, **Kontakto** ir **Tiekėjo** dvigubą rašymą naudodami „Finance and Operations” programą.</span><span class="sxs-lookup"><span data-stu-id="96abf-188">Stop the following **Account**, **Contact**, and **Vendor** dual-write using the Finance and Operations app.</span></span>

    + <span data-ttu-id="96abf-189">Klientai V3(paskyros)</span><span class="sxs-lookup"><span data-stu-id="96abf-189">Customers V3(accounts)</span></span>
    + <span data-ttu-id="96abf-190">Klientai V3(kontaktai)</span><span class="sxs-lookup"><span data-stu-id="96abf-190">Customers V3(contacts)</span></span>
    + <span data-ttu-id="96abf-191">„CDS” kontaktai V2(kontaktai)</span><span class="sxs-lookup"><span data-stu-id="96abf-191">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="96abf-192">„CDS” kontaktai V2(kontaktai)</span><span class="sxs-lookup"><span data-stu-id="96abf-192">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="96abf-193">Tiekėjas V2 („msdyn_vendor”)</span><span class="sxs-lookup"><span data-stu-id="96abf-193">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="96abf-194">Užtikrinkite, kad susiejimai yra pašalinti iš „Dataverse” lentelės `msdy_dualwriteruntimeconfig`.</span><span class="sxs-lookup"><span data-stu-id="96abf-194">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="96abf-195">Įdiekite [Dvigubo rašymo į Šalies ir Visuotinę adresų knygelė sprendimus](https://aka.ms/dual-write-gab) iš „AppSource”.</span><span class="sxs-lookup"><span data-stu-id="96abf-195">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="96abf-196">Jei šiose „Finance and Operations” programos lentelėse yra duomenų, tada joms paleiskite **Pradinį sinchronizavimą**.</span><span class="sxs-lookup"><span data-stu-id="96abf-196">In the Finance and Operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="96abf-197">Pasisveikinimai</span><span class="sxs-lookup"><span data-stu-id="96abf-197">Salutations</span></span>
    + <span data-ttu-id="96abf-198">Asmeninių savybių tipai</span><span class="sxs-lookup"><span data-stu-id="96abf-198">Personal character types</span></span>
    + <span data-ttu-id="96abf-199">Baigiamoji mandagumo frazė</span><span class="sxs-lookup"><span data-stu-id="96abf-199">Complimentary closing</span></span>
    + <span data-ttu-id="96abf-200">Kontaktinio asmens pareigos</span><span class="sxs-lookup"><span data-stu-id="96abf-200">Contact person titles</span></span>
    + <span data-ttu-id="96abf-201">Sprendimų priėmimo vaidmenys</span><span class="sxs-lookup"><span data-stu-id="96abf-201">Decision making roles</span></span>
    + <span data-ttu-id="96abf-202">Lojalumo lygiai</span><span class="sxs-lookup"><span data-stu-id="96abf-202">Loyalty levels</span></span>

5. <span data-ttu-id="96abf-203">„Customer Engagement” programoje uždrauskite šiuos papildinių veiksmus.</span><span class="sxs-lookup"><span data-stu-id="96abf-203">In the customer engagement app, disable the following plugin steps.</span></span>

    + <span data-ttu-id="96abf-204">Paskyros atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-204">Account Update</span></span>
         + <span data-ttu-id="96abf-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Paskyros atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="96abf-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Paskyros atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="96abf-207">Kontakto atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-207">Contact Update</span></span>
         + <span data-ttu-id="96abf-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Kontakto atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="96abf-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Kontakto atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="96abf-210">msdyn_party Atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-210">msdyn_party Update</span></span>
         + <span data-ttu-id="96abf-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="96abf-212">msdyn_vendor Atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-212">msdyn_vendor Update</span></span>
         + <span data-ttu-id="96abf-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="96abf-214">„Customer Engagement” programoje uždrauskite šias darbo eigas:</span><span class="sxs-lookup"><span data-stu-id="96abf-214">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="96abf-215">Tiekėjų kūrimas lentelėje Klientai</span><span class="sxs-lookup"><span data-stu-id="96abf-215">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="96abf-216">Tiekėjų kūrimas lentelėje Klientai</span><span class="sxs-lookup"><span data-stu-id="96abf-216">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="96abf-217">Tiekėjų kūrimas asmens tipo lentelėje Kontaktai</span><span class="sxs-lookup"><span data-stu-id="96abf-217">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="96abf-218">Tiekėjų kūrimas tipo Asmuo lentelėje Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="96abf-218">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="96abf-219">Tiekėjų naujinimas lentelėje Klientai</span><span class="sxs-lookup"><span data-stu-id="96abf-219">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="96abf-220">Tiekėjų naujinimas lentelėje Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="96abf-220">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="96abf-221">Tiekėjų naujinimas tipo Asmuo lentelėje Kontaktai</span><span class="sxs-lookup"><span data-stu-id="96abf-221">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="96abf-222">Tiekėjų naujinimas tipo Asmuo lentelėje Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="96abf-222">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="96abf-223">Duomenų gamykloje vykdykite šabloną pasirinkdami **Paleisti dabar**, kaip parodyta šiame paveikslėlyje.</span><span class="sxs-lookup"><span data-stu-id="96abf-223">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="96abf-224">Šis procesas gali užtrukti keletą valandų, priklausomai nuo duomenų tūrio.</span><span class="sxs-lookup"><span data-stu-id="96abf-224">This process might take a few hours to complete based on the data volume.</span></span>

    ![Paleidiklio vykdymas](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="96abf-226">Jei laukams **Paskyra**, **Kontaktas** ir **Tiekėjas** turite tinkinimus, tada turite modifikuoti šabloną.</span><span class="sxs-lookup"><span data-stu-id="96abf-226">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template.</span></span>

8. <span data-ttu-id="96abf-227">Importuokite naujus **Šalies** įrašus „Finance and Operations” programoje.</span><span class="sxs-lookup"><span data-stu-id="96abf-227">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="96abf-228">Atsisiųskite `FONewParty.csv` failą iš „Azure“ didelių dvejetainių objektų saugyklos.</span><span class="sxs-lookup"><span data-stu-id="96abf-228">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="96abf-229">Kelias yra `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="96abf-229">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="96abf-230">Konvertuokite failą `FONewParty.csv` į „Excel” failą ir tada importuokite „Excel” failą į „Finance and Operations” programą.</span><span class="sxs-lookup"><span data-stu-id="96abf-230">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the Finance and Operations app.</span></span>  <span data-ttu-id="96abf-231">Jei csv importavimas jums tinka, galite csv failą importuoti tiesiogiai.</span><span class="sxs-lookup"><span data-stu-id="96abf-231">If the csv import works for you, you can import csv file directly.</span></span> <span data-ttu-id="96abf-232">Importavimas gali užtrukti kelias valandas, priklausomai nuo duomenų tūrio.</span><span class="sxs-lookup"><span data-stu-id="96abf-232">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="96abf-233">Daugiau informacijos rasite [Duomenų importavimo ir eksportavimo užduočių apžvalga](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="96abf-233">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![„Dataverse” šalies įrašų importavimas](media/data-factory-import-party.png)

9. <span data-ttu-id="96abf-235">„Customer Engagement” programose įgalinkite šiuos papildinių veiksmus:</span><span class="sxs-lookup"><span data-stu-id="96abf-235">In the customer engagement apps, enable the following plugin steps:</span></span>

    + <span data-ttu-id="96abf-236">Paskyros atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-236">Account Update</span></span>
         + <span data-ttu-id="96abf-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Paskyros atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="96abf-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Paskyros atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="96abf-239">Kontakto atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-239">Contact Update</span></span>
         + <span data-ttu-id="96abf-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Kontakto atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="96abf-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Kontakto atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="96abf-242">msdyn_party Atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-242">msdyn_party Update</span></span>
         + <span data-ttu-id="96abf-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="96abf-244">msdyn_vendor Atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-244">msdyn_vendor Update</span></span>
         + <span data-ttu-id="96abf-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="96abf-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="96abf-246">„Customer Engagement” suaktyvinkite šias darbo eigas, jei išjungėte jas ankstesniais veiksmais:</span><span class="sxs-lookup"><span data-stu-id="96abf-246">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="96abf-247">Tiekėjų kūrimas lentelėje Klientai</span><span class="sxs-lookup"><span data-stu-id="96abf-247">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="96abf-248">Tiekėjų kūrimas lentelėje Klientai</span><span class="sxs-lookup"><span data-stu-id="96abf-248">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="96abf-249">Tiekėjų kūrimas asmens tipo lentelėje Kontaktai</span><span class="sxs-lookup"><span data-stu-id="96abf-249">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="96abf-250">Tiekėjų kūrimas tipo Asmuo lentelėje Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="96abf-250">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="96abf-251">Tiekėjų naujinimas lentelėje Klientai</span><span class="sxs-lookup"><span data-stu-id="96abf-251">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="96abf-252">Tiekėjų naujinimas lentelėje Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="96abf-252">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="96abf-253">Tiekėjų naujinimas tipo Asmuo lentelėje Kontaktai</span><span class="sxs-lookup"><span data-stu-id="96abf-253">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="96abf-254">Tiekėjų naujinimas tipo Asmuo lentelėje Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="96abf-254">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="96abf-255">Vykdykite su **Šalimi** susijusias schemas, kaip nurodyta [Šalies ir visuotinėje adresų knygelėje](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="96abf-255">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="96abf-256">Trikčių diagnostika</span><span class="sxs-lookup"><span data-stu-id="96abf-256">Troubleshooting</span></span>

1. <span data-ttu-id="96abf-257">Jei procesas nepavyksta, iš naujo paleiskite duomenų gamyklą, pradedant nuo nesėkmingos veiklos.</span><span class="sxs-lookup"><span data-stu-id="96abf-257">In the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="96abf-258">Kai kuriuos duomenų gamyklos sugeneruotus failus galite naudoti duomenų tikrinimo tikslais.</span><span class="sxs-lookup"><span data-stu-id="96abf-258">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="96abf-259">Duomenų gamykla veikia pagal kableliais atskirtus csv failus.</span><span class="sxs-lookup"><span data-stu-id="96abf-259">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="96abf-260">Jeigu kuri nors lauko vertė turi kablelius, tai gali trukdyti rezultatams.</span><span class="sxs-lookup"><span data-stu-id="96abf-260">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="96abf-261">Jums reikia pašalinti kablelius.</span><span class="sxs-lookup"><span data-stu-id="96abf-261">You need to remove the commas.</span></span>
4. <span data-ttu-id="96abf-262">Skirtuke **Stebėjimas** pateikiama informacija apie visus veiksmus ir apdorotus duomenis.</span><span class="sxs-lookup"><span data-stu-id="96abf-262">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="96abf-263">Pasirinkite konkretų veiksmą jo suderinimui.</span><span class="sxs-lookup"><span data-stu-id="96abf-263">Select a specific step to debug it.</span></span>

    ![Stebėjimo skirtukas](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="96abf-265">Sužinokite daugiau apie šabloną</span><span class="sxs-lookup"><span data-stu-id="96abf-265">Learn more about the template</span></span>

<span data-ttu-id="96abf-266">Šablono komentarus galite rasti [„readme.md”](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) faile.</span><span class="sxs-lookup"><span data-stu-id="96abf-266">You can find comments for the template the [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) file.</span></span>