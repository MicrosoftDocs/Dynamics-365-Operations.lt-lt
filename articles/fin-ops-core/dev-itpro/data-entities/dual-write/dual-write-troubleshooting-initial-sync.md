---
title: Trikčių šalinimas pradinio sinchronizavimo metu
description: Šioje temoje pateikiama trikčių šalinimo informacija, kuri gali padėti išspręsti problemas, kurios gali kilti pradinio sinchronizavimo metu.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410086"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="65a6b-103">Trikčių šalinimas pradinio sinchronizavimo metu</span><span class="sxs-lookup"><span data-stu-id="65a6b-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="65a6b-104">Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Common Data Service“ programų trikčių šalinimo informacija.</span><span class="sxs-lookup"><span data-stu-id="65a6b-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="65a6b-105">Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, kurios gali kilti pradinio sinchronizavimo metu.</span><span class="sxs-lookup"><span data-stu-id="65a6b-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65a6b-106">Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų.</span><span class="sxs-lookup"><span data-stu-id="65a6b-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="65a6b-107">Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.</span><span class="sxs-lookup"><span data-stu-id="65a6b-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="65a6b-108">Patikrinkite, ar nėra pradinio sinchronizavimo klaidų „Finance and Operations” programoje</span><span class="sxs-lookup"><span data-stu-id="65a6b-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="65a6b-109">Įgalinus susiejimo šablonus, schemų būsena turi būti **Vykdoma**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="65a6b-110">Jei būsena yra **Nevykdoma**, pradinio sinchronizavimo metu įvyko klaidų.</span><span class="sxs-lookup"><span data-stu-id="65a6b-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="65a6b-111">Norėdami peržiūrėti klaidas, pasirinkite skirtuką **Pradinio sinchronizavimo informacija** puslapyje **Dvigubas rašymas**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Pradinio sinchronizavimo informacijos skirtukas](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="65a6b-113">Negalite užbaigti pradinio sinchronizavimo: 400 netinkama užklausa</span><span class="sxs-lookup"><span data-stu-id="65a6b-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="65a6b-114">**Reikiamas vaidmuo, norint spręsti problemą:** sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="65a6b-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="65a6b-115">Kai bandote vykdyti susiejimą ir pradinį sinchronizavimą, galite gauti tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="65a6b-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="65a6b-116">*Nuotolinis serveris pateikė klaidą: (400 netinkama užklausa), AX eksportavimo funkcija susidūrė su klaida*</span><span class="sxs-lookup"><span data-stu-id="65a6b-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="65a6b-117">Čia pateikiamas viso klaidos pranešimo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="65a6b-117">Here is an example of the full error message.</span></span>

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

<span data-ttu-id="65a6b-118">Jei šį klaida įvyksta nuolat ir negalite užbaigti pradinio sinchronizavimo, atlikite šiuos veiksmus, kad išspręstumėte problemą.</span><span class="sxs-lookup"><span data-stu-id="65a6b-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="65a6b-119">Prisijunkite prie „Finance and Operations” programos virtualiosios mašinos.</span><span class="sxs-lookup"><span data-stu-id="65a6b-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="65a6b-120">Atidarykite „Microsoft“ valdymo konsolę.</span><span class="sxs-lookup"><span data-stu-id="65a6b-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="65a6b-121">Eidami į sritį **Paslaugos**, įsitikinkite, kad veikia „Microsoft Dynamics 365” duomenų importavimo / eksportavimo sistemos paslauga.</span><span class="sxs-lookup"><span data-stu-id="65a6b-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="65a6b-122">Jeigu ji buvo sustabdyta, paleiskite ją iš naujo, nes ji yra reikalinga pradiniam sinchronizavimui atlikti.</span><span class="sxs-lookup"><span data-stu-id="65a6b-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="65a6b-123">Pradinio sinchronizavimo klaida: 403 draudžiama</span><span class="sxs-lookup"><span data-stu-id="65a6b-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="65a6b-124">Pradinio sinchronizavimo metu galite gauti tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="65a6b-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="65a6b-125">*\[Draudžiama\], nuotolinis serveris pateikė klaidą: (403 draudžiama), AX eksportavimo funkcija susidūrė su klaida*</span><span class="sxs-lookup"><span data-stu-id="65a6b-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="65a6b-126">Norėdami ištaisyti klaidą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="65a6b-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="65a6b-127">Prisijungimas prie „Finance and Operations” programos.</span><span class="sxs-lookup"><span data-stu-id="65a6b-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="65a6b-128">Puslapyje **„Azure Active Directory” programos** panaikinkite klientą **DtAppID** ir vėl jį pridėkite.</span><span class="sxs-lookup"><span data-stu-id="65a6b-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![„Azure AD” programų sąrašas](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="65a6b-130">Nuorodų į save arba ciklinių nuorodų klaidos pradinio sinchronizavimo metu</span><span class="sxs-lookup"><span data-stu-id="65a6b-130">Self-reference or circular-reference failures during initial synchronization</span></span>

<span data-ttu-id="65a6b-131">Jeigu bet kurie iš jūsų susiejimų turi nuorodų į save ar ciklinių nuorodų, galite gauti klaidos pranešimų.</span><span class="sxs-lookup"><span data-stu-id="65a6b-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="65a6b-132">Klaidos skirstomos į toliau pateiktas kategorijas.</span><span class="sxs-lookup"><span data-stu-id="65a6b-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="65a6b-133">Objektų „Tiekėjai V2“ ir „msdyn_vendors“ susiejimas</span><span class="sxs-lookup"><span data-stu-id="65a6b-133">Vendors V2 to msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="65a6b-134">Objektų „Klientai V3“ ir „Paskyros“ susiejimas</span><span class="sxs-lookup"><span data-stu-id="65a6b-134">Customers V3 to Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="65a6b-135">Objektų „Tiekėjai V2ׅ“ ir „msdyn_vendors“ susiejimo klaidos šalinimas</span><span class="sxs-lookup"><span data-stu-id="65a6b-135">Resolve an error in Vendors V2 to msdyn_vendors entity mapping</span></span>

<span data-ttu-id="65a6b-136">Atlikdami **Tiekėjai V2** susiejimą su **msdyn_vendors** gali kilti toliau pateiktų pradinio sinchronizavimo klaidų, jei objektai turi esamų įrašų su vertėmis laukuose **PrimaryContactPersonId** ir **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-136">You might run into the following initial sync errors on the **Vendors V2** to **msdyn_vendors** mapping if the entities have existing records with values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="65a6b-137">Taip yra todėl, kad susiejant tiekėją **InvoiceVendorAccountNumber** yra nuorodos į save laukas, o **PrimaryContactPersonId** yra ciklinė nuoroda.</span><span class="sxs-lookup"><span data-stu-id="65a6b-137">This because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="65a6b-138">*Nepavyko išspręsti lauko guid: <field>. Peržvalga nerasta: <value>. Naudodami šį (šiuos) URL patikrinkite, ar yra nuorodos duomenys: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="65a6b-138">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

<span data-ttu-id="65a6b-139">Štai keletas pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="65a6b-139">Here are a couple of examples:</span></span>

- <span data-ttu-id="65a6b-140">*Nepavyko išspręsti lauko guid: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Peržvalga nerasta: 000056. Naudodami šį (šiuos) URL patikrinkite, ar yra nuorodos duomenys: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="65a6b-140">*Couldn't resolve the guid for the field: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="65a6b-141">*Nepavyko išspręsti lauko guid: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. Peržvalga nerasta: V24-1. Naudodami šį (šiuos) URL patikrinkite, ar yra nuorodos duomenys: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span><span class="sxs-lookup"><span data-stu-id="65a6b-141">*Couldn't resolve the guid for the field: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span></span>

<span data-ttu-id="65a6b-142">Jei jūs tiekėjo objekte turite įrašų su vertėmis šiuose laukuose, vadovaukitės tolesniame skyriuje pateiktais veiksmais, kad sėkmingai atliktumėte pradinį sinchronizavimą.</span><span class="sxs-lookup"><span data-stu-id="65a6b-142">If you have records with values in these fields in the vendor entity follow the steps in the below section to complete initial sync successfully.</span></span>

1. <span data-ttu-id="65a6b-143">Finance and Operations programoje panaikinkite laukus **PrimaryContactPersonId** ir **InvoiceVendorAccountNumber** iš susiejimo ir įrašykite pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="65a6b-143">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping and save the changes.</span></span>

    1. <span data-ttu-id="65a6b-144">Pereikite į **Tiekėjai V2 (msdyn_vendors)** dvigubo rašymo susiejimo puslapį ir pasirinkite skirtuką **Objektų susiejimai**. Kairiajame filtre pasirinkite **Finance and Operations programos.Tiekėjai V2**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-144">Navigate to the dual-write mapping page for **Vendors V2 (msdyn_vendors)**, and select the **Entity mappings** tab. In the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="65a6b-145">Dešiniajame filtre pasirinkite **Pardavimai.Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-145">In the right filter, select **Sales.Vendor**.</span></span>

    2. <span data-ttu-id="65a6b-146">Paieškoje įveskite **primarycontactperson**, kad surastumėte šaltinio lauką **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-146">Search for **primarycontactperson** to find the source field **PrimaryContactPersonId**.</span></span>
    
    3. <span data-ttu-id="65a6b-147">Spustelėkite mygtuką **Veiksmai** ir pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-147">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![nuoroda į save ar ciklinė nuoroda 3](media/vend_selfref3.png)
    
    4. <span data-ttu-id="65a6b-149">Pakartokite veiksmus, kad panaikintumėte lauką **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-149">Repeat to delete the **InvoiceVendorAccountNumber** field.</span></span>
    
        ![nuoroda į save ar ciklinė nuoroda 4](media/vend-selfref4.png)
    
    5. <span data-ttu-id="65a6b-151">Įrašykite susiejimo pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="65a6b-151">Save the mapping changes.</span></span>

2. <span data-ttu-id="65a6b-152">Išjunkite objekto **Tiekėjai V2** keitimų sekimą.</span><span class="sxs-lookup"><span data-stu-id="65a6b-152">Disable the change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="65a6b-153">Eikite į **Duomenų valdymas \> Duomenų objektai**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-153">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="65a6b-154">Pasirinkite objektą **Tiekėjai V2**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-154">Select the **Vendors V2** entity.</span></span>
    
    3. <span data-ttu-id="65a6b-155">Meniu juostoje spustelėkite **Parinktys**, tada – **Keisti sekimą**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-155">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![nuoroda į save ar ciklinė nuoroda 5](media/selfref_options.png)
    
    4. <span data-ttu-id="65a6b-157">Spustelėkite **Išjungti keitimų sekimą**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-157">Click **Disable Change Tracking**.</span></span>
    
        ![nuoroda į save ar ciklinė nuoroda 6](media/selfref_tracking.png)

3. <span data-ttu-id="65a6b-159">Paleiskite pradinį **Tiekėjai V2 (msdyn_vendors)** susiejimo sinchronizavimą.</span><span class="sxs-lookup"><span data-stu-id="65a6b-159">Run the initial sync of **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="65a6b-160">Pradinis sinchronizavimas turėtų būtį įvykdytas sėkmingai ir be klaidų.</span><span class="sxs-lookup"><span data-stu-id="65a6b-160">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="65a6b-161">Paleiskite pradinį **CDS Kontaktai V2 (kontaktai)** susiejimo sinchronizavimą.</span><span class="sxs-lookup"><span data-stu-id="65a6b-161">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="65a6b-162">Turite sinchronizuoti šį susiejimą, jei norite sinchronizuoti tiekėjų objekto pagrindinio kontakto lauką, nes kontaktų įrašams taip pat turi būti atliekamas pradinis sinchronizavimas.</span><span class="sxs-lookup"><span data-stu-id="65a6b-162">You must sync this mapping if you want to sync primary contact field on vendors entity as the contacts records also need to be initial synced.</span></span>

5. <span data-ttu-id="65a6b-163">Įtraukite laukus **PrimaryContactPersonId** ir **InvoiceVendorAccountNumber** atgal į **Tiekėjai V2 (msdyn_vendors)** susiejimą ir įrašykite jį.</span><span class="sxs-lookup"><span data-stu-id="65a6b-163">Add the fields **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** back to the **Vendors V2 (msdyn_vendors)** mapping and save the mapping.</span></span>

6. <span data-ttu-id="65a6b-164">Dar kartą paleiskite pradinį **Tiekėjai V2 (msdyn_vendors)** susiejimo sinchronizavimą.</span><span class="sxs-lookup"><span data-stu-id="65a6b-164">Run the initial sync again for the **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="65a6b-165">Visi įrašai bus sinchronizuoti, nes keitimų sekimas yra išjungtas.</span><span class="sxs-lookup"><span data-stu-id="65a6b-165">All the records will be synced, because change tracking is disabled.</span></span>

7. <span data-ttu-id="65a6b-166">Įjunkite objekto **Tiekėjai V2** keitimų sekimą.</span><span class="sxs-lookup"><span data-stu-id="65a6b-166">Enable change tracking for the **Vendors V2** entity.</span></span>

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="65a6b-167">Objektų „Klientai V3“ ir „Paskyros“ susiejimo klaidų šalinimas</span><span class="sxs-lookup"><span data-stu-id="65a6b-167">Resolve an error in Customers V3 to Accounts entity mapping</span></span>

<span data-ttu-id="65a6b-168">Atlikdami **Klientai V3** susiejimą su **Paskyros** gali kilti toliau pateiktų pradinio sinchronizavimo klaidų, jei objektai turi įrašų su vertėmis laukuose **ContactPersonID** ir **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-168">You might run into the following initial sync errors on the **Customers V3** to **Accounts** mapping if the entities have existing records with values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="65a6b-169">Taip yra todėl, kad susiejant tiekėją **InvoiceAccount** yra nuorodos į save laukas, o **ContactPersonID** yra ciklinė nuoroda.</span><span class="sxs-lookup"><span data-stu-id="65a6b-169">This because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="65a6b-170">*Nepavyko išspręsti lauko guid: <field>. Peržvalga nerasta: <value>. Naudodami šį (šiuos) URL patikrinkite, ar yra nuorodos duomenys: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="65a6b-170">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

- <span data-ttu-id="65a6b-171">*Nepavyko išspręsti lauko guid: primarycontactid.msdyn_contactpersonid. Peržvalga nerasta: 000056. Naudodami šį (šiuos) URL patikrinkite, ar yra nuorodos duomenys: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="65a6b-171">*Couldn't resolve the guid for the field: primarycontactid.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="65a6b-172">*Nepavyko išspręsti lauko guid: msdyn_billingaccount.accountnumber. Peržvalga nerasta: 1206-1. Naudodami šį (šiuos) URL patikrinkite, ar yra nuorodos duomenys: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account$filter=accountnumber eq '1206-1'*</span><span class="sxs-lookup"><span data-stu-id="65a6b-172">*Couldn't resolve the guid for the field: msdyn_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span></span>

<span data-ttu-id="65a6b-173">Jei jūs kliento objekte turite įrašų su vertėmis šiuose laukuose, vadovaukitės tolesniame skyriuje pateiktais veiksmais, kad sėkmingai atliktumėte pradinį sinchronizavimą.</span><span class="sxs-lookup"><span data-stu-id="65a6b-173">If you have records with values in these fields in the customer entity follow the steps in the below section to complete initial sync successfully.</span></span> <span data-ttu-id="65a6b-174">Galite naudoti šį metodą bet kuriems iš karto pasiekiamiems objektams, pvz., „Paskyros“ ir „Kontaktai“.</span><span class="sxs-lookup"><span data-stu-id="65a6b-174">You can use this approach for any out-of-the-box entities such Accounts and Contacts.</span></span>

1. <span data-ttu-id="65a6b-175">„Finance and Operations“ programoje panaikinkite laukus **ContactPersonID** ir **InvoiceAccount** iš **Klientai V3 (paskyros)** susiejimo ir įrašykite pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="65a6b-175">In the Finance and Operations app, delete the fields **ContactPersonID** and **InvoiceAccount** from the **Customers V3 (accounts)** mapping and save the mapping.</span></span>

    1. <span data-ttu-id="65a6b-176">Eikite į **Klientai V3 (paskyros)** dvigubo rašymo susiejimo puslapį ir pasirinkite skirtuką **Objektų susiejimai**. Kairiajame filtre pasirinkite **Finance and Operations programa.Tiekėjai V3**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-176">Navigate to the dual-write mapping page for **Customers V3 (accounts)**, select the **Entity mappings** tab. In the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="65a6b-177">Dešiniajame filtre pasirinkite **Common Data Service.Paskyra**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-177">In the right filter, select **Common Data Service.Account**.</span></span>

    2. <span data-ttu-id="65a6b-178">Paieškoje įveskite **contactperson**, kad surastumėte šaltinio lauką **ContactPersonID**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-178">Search for **contactperson** to find the source field **ContactPersonID**.</span></span>
    
    3. <span data-ttu-id="65a6b-179">Spustelėkite mygtuką **Veiksmai** ir pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-179">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![nuoroda į save ar ciklinė nuoroda 3](media/cust_selfref3.png)
    
    4. <span data-ttu-id="65a6b-181">Pakartokite, kad panaikintumėte lauką **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-181">Repeat to delete the **InvoiceAccount** field.</span></span>
    
        ![nuoroda į save ar ciklinė nuoroda](media/cust_selfref4.png)
    
    5. <span data-ttu-id="65a6b-183">Įrašykite susiejimo pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="65a6b-183">Save the mapping changes.</span></span>

2. <span data-ttu-id="65a6b-184">Išjunkite objekto **Klientai V3** keitimų sekimą.</span><span class="sxs-lookup"><span data-stu-id="65a6b-184">Disable the change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="65a6b-185">Eikite į **Duomenų valdymas \> Duomenų objektai**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-185">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="65a6b-186">Pasirinkite objektą **Klientai V3**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-186">Select the **Customers V3** entity.</span></span>
    
    3. <span data-ttu-id="65a6b-187">Meniu juostoje spustelėkite **Parinktys**, tada – **Keisti sekimą**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-187">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![nuoroda į save ar ciklinė nuoroda 5](media/selfref_options.png)
    
    4. <span data-ttu-id="65a6b-189">Spustelėkite **Išjungti keitimų sekimą**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-189">Click **Disable Change Tracking**.</span></span>
    
        ![nuoroda į save ar ciklinė nuoroda 6](media/selfref_tracking.png)

3. <span data-ttu-id="65a6b-191">Paleiskite pradinį **Klientai V3 (Paskyros)** susiejimo sinchronizavimą.</span><span class="sxs-lookup"><span data-stu-id="65a6b-191">Run the initial sync for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="65a6b-192">Pradinis sinchronizavimas turėtų būtį įvykdytas sėkmingai ir be klaidų.</span><span class="sxs-lookup"><span data-stu-id="65a6b-192">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="65a6b-193">Paleiskite pradinį **CDS Kontaktai V2 (kontaktai)** susiejimo sinchronizavimą.</span><span class="sxs-lookup"><span data-stu-id="65a6b-193">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="65a6b-194">Yra 2 schemos su tuo pačiu pavadinimu.</span><span class="sxs-lookup"><span data-stu-id="65a6b-194">There are 2 maps with the same name.</span></span> <span data-ttu-id="65a6b-195">Pasirinkite tą, kurios aprašymas yra **Dvigubo rašymo šablonas, skirtas sinchronizuoti FO.CDS Tiekėjo kontaktai V2 su CDS.Kontaktai. Reikalingas naujas paketas \[Dynamics365SupplyChainExtended\] .**</span><span class="sxs-lookup"><span data-stu-id="65a6b-195">Select the one with the description **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span> <span data-ttu-id="65a6b-196">schemos skirtuke **Išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-196">on the **Details** tab of the map.</span></span>

5. <span data-ttu-id="65a6b-197">Įtraukite laukus **InvoiceAccount** ir **ContactPersonId** atgal į **Klientai V3 (Paskyros)** susiejimą ir įrašykite jį.</span><span class="sxs-lookup"><span data-stu-id="65a6b-197">Add the fields **InvoiceAccount** and **ContactPersonId** back to the **Customers V3 (Accounts)** mapping and save the mapping.</span></span> <span data-ttu-id="65a6b-198">Dabar laukai **InvoiceAccount** ir **ContactPersonId** vėl įtraukti į tiesioginio sinchronizavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="65a6b-198">Now, both the **InvoiceAccount** field and the **ContactPersonId** field are again part of live sync mode.</span></span> <span data-ttu-id="65a6b-199">Kitame veiksme užbaigiate pradinį šių laukų sinchronizavimą.</span><span class="sxs-lookup"><span data-stu-id="65a6b-199">In the next step, you complete the initial sync for these fields.</span></span>

6. <span data-ttu-id="65a6b-200">Vėl paleiskite pradinį **Klientai V3 (Paskyros)** susiejimo sinchronizavimą.</span><span class="sxs-lookup"><span data-stu-id="65a6b-200">Run the initial sync again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="65a6b-201">Kadangi keitimų sekimas yra išjungtas, paleidus sinchronizavimą bus sinchronizuoti **InvoiceAccount** ir **ContactPersonId** duomenys iš „Finance and Operations“ programos į „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="65a6b-201">Because change tracking is disabled, running the sync will sync the data for **InvoiceAccount** and **ContactPersonId** from the Finance and Operations app to Common Data Service.</span></span>

7. <span data-ttu-id="65a6b-202">Norėdami sinchronizuoti **InvoiceAccount** ir **ContactPersonId** duomenis iš „Common Data Service“ į „Finance and Operations“, naudokite duomenų integravimo projektą.</span><span class="sxs-lookup"><span data-stu-id="65a6b-202">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations, you use a data integration project.</span></span>

    1. <span data-ttu-id="65a6b-203">„Power Apps“ sukurkite duomenų integravimo projektą tarp **Pardavimai.Paskyra** ir **Finance and Operations programos.Klientai V3** objektų.</span><span class="sxs-lookup"><span data-stu-id="65a6b-203">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="65a6b-204">Duomenų kryptis turi būti iš „Common Data Service“ į „Finance and Operations“ programą.</span><span class="sxs-lookup"><span data-stu-id="65a6b-204">The data direction must be from Common Data Service to the Finance and Operations app.</span></span>  <span data-ttu-id="65a6b-205">Kadangi **InvoiceAccount** yra naujas atributas dvigubo rašymo funkcijoje, rekomenduojama praleisti pradinį šio atributo sinchronizavimą.</span><span class="sxs-lookup"><span data-stu-id="65a6b-205">Because **InvoiceAccount** is a new attribute in dual-write, you may want to skip initial sync for this attribute.</span></span> <span data-ttu-id="65a6b-206">Prireikus daugiau informacijos, žr. [Duomenų integravimas į Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="65a6b-206">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="65a6b-207">Toliau pateiktame paveikslėlyje parodytas projektas, kuris atnaujina **CustomerAccount** ir **ContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-207">The following image shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![nuoroda į save ar ciklinė nuoroda](media/cust_selfref6.png)

    2. <span data-ttu-id="65a6b-209">Įtraukite įmonės kriterijus į „Common Data Service“ filtrą, nes programoje „Finance and Operations“ bus atnaujinti tik tie įrašai, kurie atitinka filtro kriterijus.</span><span class="sxs-lookup"><span data-stu-id="65a6b-209">Add the company criteria in the filter on Common Data Service side, because only the records that match filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="65a6b-210">Norėdami įtraukti filtrą, spustelėkite filtro piktogramą.</span><span class="sxs-lookup"><span data-stu-id="65a6b-210">To add a filter, click the filter icon.</span></span> <span data-ttu-id="65a6b-211">Dialogo lange **Redaguoti užklausą** galite įtraukti filtro užklausą, pvz., **_msdyn_company_value eq '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="65a6b-211">In the **Edit query** dialog, you can add a filter query like **_msdyn_company_value eq '\<guid\>'**.</span></span> <span data-ttu-id="65a6b-212">Jei filtro piktogramos nėra, sukurkite palaikymo kvitą, kad paprašytumėte duomenų integravimo komandos įjungti filtro funkciją jūsų nuomotojui.</span><span class="sxs-lookup"><span data-stu-id="65a6b-212">If the filter icon is not present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span> <span data-ttu-id="65a6b-213">Jei neįvesite **_msdyn_company_value** filtro užklausos, visi įrašai bus sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="65a6b-213">If you do not enter a filter query for **_msdyn_company_value**, then all the records are synced.</span></span>

        ![nuoroda į save ar ciklinė nuoroda](media/cust_selfref7.png)

        <span data-ttu-id="65a6b-215">Tai yra pradinio įrašų sinchronizavimo pabaiga.</span><span class="sxs-lookup"><span data-stu-id="65a6b-215">This completes the initial sync of the records.</span></span>

8. <span data-ttu-id="65a6b-216">Įjunkite objekto **Klientai V3** keitimų sekimą „Finance and Operations“ programoje.</span><span class="sxs-lookup"><span data-stu-id="65a6b-216">Enable change tracking for the **Customers V3** entity in the Finance and Operations app.</span></span>

