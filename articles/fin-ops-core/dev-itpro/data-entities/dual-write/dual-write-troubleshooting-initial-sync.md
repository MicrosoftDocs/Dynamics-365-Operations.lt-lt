---
title: Trikčių šalinimas pradinio sinchronizavimo metu
description: Šioje temoje pateikiama trikčių šalinimo informacija, kuri gali padėti išspręsti problemas, kurios gali kilti pradinio sinchronizavimo metu.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 709a3c332bb6d086910b257fee9cdec8d2bc81a2
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941060"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="a7954-103">Trikčių šalinimas pradinio sinchronizavimo metu</span><span class="sxs-lookup"><span data-stu-id="a7954-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a7954-104">Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Dataverse“ programų trikčių šalinimo informacija.</span><span class="sxs-lookup"><span data-stu-id="a7954-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="a7954-105">Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, kurios gali kilti pradinio sinchronizavimo metu.</span><span class="sxs-lookup"><span data-stu-id="a7954-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a7954-106">Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų.</span><span class="sxs-lookup"><span data-stu-id="a7954-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="a7954-107">Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.</span><span class="sxs-lookup"><span data-stu-id="a7954-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="a7954-108">Patikrinkite, ar nėra pradinio sinchronizavimo klaidų „Finance and Operations” programoje</span><span class="sxs-lookup"><span data-stu-id="a7954-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="a7954-109">Įgalinus susiejimo šablonus, schemų būsena turi būti **Vykdoma**.</span><span class="sxs-lookup"><span data-stu-id="a7954-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="a7954-110">Jei būsena yra **Nevykdoma**, pradinio sinchronizavimo metu įvyko klaidų.</span><span class="sxs-lookup"><span data-stu-id="a7954-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="a7954-111">Norėdami peržiūrėti klaidas, pasirinkite skirtuką **Pradinio sinchronizavimo informacija** puslapyje **Dvigubas rašymas**.</span><span class="sxs-lookup"><span data-stu-id="a7954-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Pradinio sinchronizavimo informacijos skirtuko klaida](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="a7954-113">Negalite užbaigti pradinio sinchronizavimo: 400 netinkama užklausa</span><span class="sxs-lookup"><span data-stu-id="a7954-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="a7954-114">**Reikiamas vaidmuo, norint spręsti problemą:** sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="a7954-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="a7954-115">Kai bandote vykdyti susiejimą ir pradinį sinchronizavimą, galite gauti tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="a7954-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="a7954-116">*(\[Netinkama užklausa\], nuotolinis serveris grąžino klaidą: (400) netinkam užklausa.), AX eksportavimo funkcijoje atsirado klaida*</span><span class="sxs-lookup"><span data-stu-id="a7954-116">*(\[Bad Request\], The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="a7954-117">Čia pateikiamas viso klaidos pranešimo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="a7954-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="a7954-118">Jei šį klaida įvyksta nuolat ir negalite užbaigti pradinio sinchronizavimo, atlikite šiuos veiksmus, kad išspręstumėte problemą.</span><span class="sxs-lookup"><span data-stu-id="a7954-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="a7954-119">Prisijunkite prie „Finance and Operations” programos virtualiosios mašinos.</span><span class="sxs-lookup"><span data-stu-id="a7954-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="a7954-120">Atidarykite „Microsoft“ valdymo konsolę.</span><span class="sxs-lookup"><span data-stu-id="a7954-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="a7954-121">Eidami į sritį **Paslaugos**, įsitikinkite, kad veikia „Microsoft Dynamics 365” duomenų importavimo / eksportavimo sistemos paslauga.</span><span class="sxs-lookup"><span data-stu-id="a7954-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="a7954-122">Jeigu ji buvo sustabdyta, paleiskite ją iš naujo, nes ji yra reikalinga pradiniam sinchronizavimui atlikti.</span><span class="sxs-lookup"><span data-stu-id="a7954-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="a7954-123">Pradinio sinchronizavimo klaida: 403 draudžiama</span><span class="sxs-lookup"><span data-stu-id="a7954-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="a7954-124">Pradinio sinchronizavimo metu galite gauti tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="a7954-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="a7954-125">*\[Draudžiama\], nuotolinis serveris pateikė klaidą: (403 draudžiama), AX eksportavimo funkcija susidūrė su klaida*</span><span class="sxs-lookup"><span data-stu-id="a7954-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="a7954-126">Norėdami ištaisyti klaidą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a7954-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="a7954-127">Prisijungimas prie „Finance and Operations” programos.</span><span class="sxs-lookup"><span data-stu-id="a7954-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="a7954-128">Puslapyje **„Azure Active Directory” programos** panaikinkite klientą **DtAppID** ir vėl jį pridėkite.</span><span class="sxs-lookup"><span data-stu-id="a7954-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![DtAppID klientas „Azure AD” programų sąraše](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="a7954-130">Nepavykusi auto-nuoroda arba ciklinių nuorodų klaidos pradinio sinchronizavimo metu</span><span class="sxs-lookup"><span data-stu-id="a7954-130">Self-reference or circular reference failures during initial synchronization</span></span>

<span data-ttu-id="a7954-131">Jeigu bet kurie iš jūsų susiejimų turi nuorodų į save ar ciklinių nuorodų, galite gauti klaidos pranešimų.</span><span class="sxs-lookup"><span data-stu-id="a7954-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="a7954-132">Klaidos skirstomos į toliau pateiktas kategorijas.</span><span class="sxs-lookup"><span data-stu-id="a7954-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="a7954-133">Klaidos Tiekėjuose V2–to–msdyn_tiekėjai lentelės susiejimas</span><span class="sxs-lookup"><span data-stu-id="a7954-133">Errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="a7954-134">Klaidos Klientuose V3–to–Paskyros lentelės susiejimas</span><span class="sxs-lookup"><span data-stu-id="a7954-134">Errors in the Customers V3–to–Accounts table mapping</span></span>](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="a7954-135">Išspręsti problemas Tiekėjuose V2–to–msdyn_tiekėjai lentelės susiejimas</span><span class="sxs-lookup"><span data-stu-id="a7954-135">Resolve errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>

<span data-ttu-id="a7954-136">Gali atsirasti pradinės sinchronizacijos klaidų susiejant **Tiekėjai V2** su **msdyn\_tiekėjai**, jei lentelės turi egzistuojančių eilučių, kai yra verčių **PirminioKontaktinioAsmensId** ir **SąskaitosFaktūrosTiekėjoPaskyrosNumeris** stulpeliuose.</span><span class="sxs-lookup"><span data-stu-id="a7954-136">You might encounter initial synchronization errors for the mapping of **Vendors V2** to **msdyn\_vendors** if the tables have existing rows where there are values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns.</span></span> <span data-ttu-id="a7954-137">Šios klaidos atsiranda, nes **SąskaitosFaktūrosTiekėjoPaskyrosNumeris** yra nuorodos į save stulpelis, o **PirminioKontaktinioAsmensId** yra ciklinė nuoroda tiekėjo susiejime.</span><span class="sxs-lookup"><span data-stu-id="a7954-137">These errors occur because **InvoiceVendorAccountNumber** is a self-referencing column, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="a7954-138">Gauti klaidos pranešimai bus šios formos.</span><span class="sxs-lookup"><span data-stu-id="a7954-138">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="a7954-139">*Nepavyko išspręsti lauko GUID: \<field\>. Peržvalga nerasta: \<value\>. Pabandykite šį (-iuos) URL adresą (-us), kad patikrintumėte, ar yra nuorodos duomenys: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="a7954-139">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="a7954-140">Štai keletas pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="a7954-140">Here are some examples:</span></span>

- <span data-ttu-id="a7954-141">*Nepavyko išspręsti lauko GUID: msdyn\_tiekėjopirminiskontaktinisasmuo.msdyn\_kontaktinioasmensid. Peržvalga nerasta: 000056. Pabandykite šį (-iuos) URL adresą (-us), kad patikrintumėte, ar egzistuoja nuorodos duomenys: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="a7954-141">*Couldn't resolve the guid for the field: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="a7954-142">*Nepavyko išspręsti lauko GUID: msdyn\_sąskaitosfaktūrostiekėjopaskyrosnumeris.msdyn\_tiekėjopaskyrosnumeris. Peržvalga nerasta: V24-1. Pabandykite šį (-iuos) URL adresą (-us), kad patikrintumėte, ar egzistuoja nuorodos duomenys: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span><span class="sxs-lookup"><span data-stu-id="a7954-142">*Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span></span>

<span data-ttu-id="a7954-143">Jei eilutės tiekėjo lentelėje turi verčių **PirminioKontaktinioAsmensId** ir **SąskaitosFaktūrosTiekėjoPaskyrosNumeris** stulpeliuose, vykdykite šiuos žingsnius, kad užbaigtumėte pradinį sinchronizavimą.</span><span class="sxs-lookup"><span data-stu-id="a7954-143">If any rows in the vendor table have values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns, follow these steps to complete the initial synchronization.</span></span>

1. <span data-ttu-id="a7954-144">„Finance and Operations” programoje panaikinkite **PirminioKontaktinioAsmensId** ir **SąskaitosFaktūrosTiekėjoPaskyrosNumeris** stulpelius iš susiejimo ir tada jį įrašykite.</span><span class="sxs-lookup"><span data-stu-id="a7954-144">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns from the mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="a7954-145">Dvigubo rašymo susiejimo puslapyje **Tiekėjai V2 (msdyn\_tiekėjai)**, **Lentelės susiejimai** skirtuke, kairiajame filtre pasirinkite **„Finance and Operations” programos.Tiekėjai V2**.</span><span class="sxs-lookup"><span data-stu-id="a7954-145">On the dual-write mapping page for **Vendors V2 (msdyn\_vendors)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="a7954-146">Dešiniajame filtre pasirinkite **Pardavimai.Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="a7954-146">In the right filter, select **Sales.Vendor**.</span></span>
    2. <span data-ttu-id="a7954-147">Paieškoje įveskite **pirminis kontaktinis asmuo** tam, kad surastumėte **PirminioKontaktinioAsmensId** šaltinio stulpelį.</span><span class="sxs-lookup"><span data-stu-id="a7954-147">Search for **primarycontactperson** to find the **PrimaryContactPersonId** source column.</span></span>
    3. <span data-ttu-id="a7954-148">Pasirinkite **Veiksmai** ir pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="a7954-148">Select **Actions**, and then select **Delete**.</span></span>

        ![PirminioKontaktinioAsmensId stulpelio naikinimas](media/vend_selfref3.png)

    4. <span data-ttu-id="a7954-150">Pakartokite šiuos veiksmus, kad panaikintumėte **SąskaitosFaktūrosTiekėjoPaskyrosNumeris** stulpelį.</span><span class="sxs-lookup"><span data-stu-id="a7954-150">Repeat these steps to delete the **InvoiceVendorAccountNumber** column.</span></span>

        ![SąskaitosFaktūrosTiekėjoPaskyrosNumerio stulpelio naikinimas](media/vend-selfref4.png)

    5. <span data-ttu-id="a7954-152">Įrašykite savo pakeitimus susiejime.</span><span class="sxs-lookup"><span data-stu-id="a7954-152">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="a7954-153">Išjunkite **Tiekėjai V2** lentelės keitimų sekimą.</span><span class="sxs-lookup"><span data-stu-id="a7954-153">Turn off change tracking for the **Vendors V2** table.</span></span>

    1. <span data-ttu-id="a7954-154">**Duomenų valdymas** darbo srityje pasirinkite **Duomenų lentelės** plytelę.</span><span class="sxs-lookup"><span data-stu-id="a7954-154">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="a7954-155">Pasirinkite **Tiekėjai V2** lentelę.</span><span class="sxs-lookup"><span data-stu-id="a7954-155">Select the **Vendors V2** table.</span></span>
    3. <span data-ttu-id="a7954-156">Veiksmų srityje pasirinkite **Parinktys**, tada – **Keitimų sekimas**.</span><span class="sxs-lookup"><span data-stu-id="a7954-156">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Keitimų sekimo parinkties pasirinkimas](media/selfref_options.png)

    4. <span data-ttu-id="a7954-158">Pasirinkite **Išjungti keitimų sekimą**.</span><span class="sxs-lookup"><span data-stu-id="a7954-158">Select **Disable Change Tracking**.</span></span>

        ![Išjungti keitimų sekimą pasirinkimas](media/selfref_tracking.png)

3. <span data-ttu-id="a7954-160">Paleiskite pradinę sinchronizaciją, skirtą **Tiekėjai V2 (msdyn\_tiekėjai)** siejimui.</span><span class="sxs-lookup"><span data-stu-id="a7954-160">Run initial synchronization for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="a7954-161">Pradinė sinchronizacija turėtų pavykti sėkmingai be klaidų.</span><span class="sxs-lookup"><span data-stu-id="a7954-161">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="a7954-162">Paleiskite pradinę **CDS Kontaktai V2 (kontaktai)** susiejimo sinchronizaciją.</span><span class="sxs-lookup"><span data-stu-id="a7954-162">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="a7954-163">Turite sinchronizuoti šį susiejimą, jei norite sinchronizuoti pirminių kontaktų stulpelį tiekėjų lentelėje, nes taip pat turite atlikti kontaktų eilučių sinchronizavimą.</span><span class="sxs-lookup"><span data-stu-id="a7954-163">You must sync this mapping if you want to sync the primary contact column on the vendors table, because initial synchronization must also be done for the contact rows.</span></span>
5. <span data-ttu-id="a7954-164">Pridėkite **PirminioKontaktinioAsmensId** ir **SąskaitosFaktūrosTiekėjoPaskyrosNumeris** stulpelius vėl į **Tiekėjai V2 (msdyn\_tiekėjai)** susiejimą ir tada jį įrašykite.</span><span class="sxs-lookup"><span data-stu-id="a7954-164">Add the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns back to the **Vendors V2 (msdyn\_vendors)** mapping, and then save the mapping.</span></span>
6. <span data-ttu-id="a7954-165">Vėl paleiskite pradinę sinchronizaciją, skirtą **Tiekėjai V2 (msdyn\_tiekėjai)** susiejimui.</span><span class="sxs-lookup"><span data-stu-id="a7954-165">Run initial synchronization again for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="a7954-166">Kadangi keitimų sekimas išjungtas, visos eilutės bus sinchronizuotos.</span><span class="sxs-lookup"><span data-stu-id="a7954-166">Because change tracking is turned off, all the rows will be synced.</span></span>
7. <span data-ttu-id="a7954-167">Vėl įjunkite **Tiekėjai V2** lentelės keitimų sekimą.</span><span class="sxs-lookup"><span data-stu-id="a7954-167">Turn change tracking back on for the **Vendors V2** table.</span></span>

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="a7954-168">„Klientai V3 į Paskyras lentelės susiejimą” klaidų šalinimas</span><span class="sxs-lookup"><span data-stu-id="a7954-168">Resolve errors in the Customers V3–to–Accounts table mapping</span></span>

<span data-ttu-id="a7954-169">Gali atsirasti pradinės sinchronizacijos klaidų susiejant **Klientai V3** su **Paskyros**, jei lentelėse yra eilučių, kuriose yra verčių **KontaktinioAsmensID** ir **SąskaitosFaktūrosPaskyra** stulpeliuose.</span><span class="sxs-lookup"><span data-stu-id="a7954-169">You might encounter initial synchronization errors for the mapping of **Customers V3** to **Accounts** if the tables have existing rows where there are values in the **ContactPersonID** and **InvoiceAccount** columns.</span></span> <span data-ttu-id="a7954-170">Šios klaidos atsiranda, nes **SąskaitosFaktūrosPaskyra** yra nuorodos į save stulpelis, o **KontaktinioAsmensID** yra ciklinė nuoroda tiekėjo susiejime.</span><span class="sxs-lookup"><span data-stu-id="a7954-170">These errors occur because **InvoiceAccount** is a self-referencing column, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="a7954-171">Gauti klaidos pranešimai bus šios formos.</span><span class="sxs-lookup"><span data-stu-id="a7954-171">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="a7954-172">*Nepavyko išspręsti lauko GUID: \<field\>. Peržvalga nerasta: \<value\>. Pabandykite šį (-iuos) URL adresą (-us), kad patikrintumėte, ar yra nuorodos duomenys: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="a7954-172">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="a7954-173">Štai keletas pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="a7954-173">Here are some examples:</span></span>

- <span data-ttu-id="a7954-174">*Nepavyko išspręsti lauko GUID: pirminiokontaktoid.msdyn\_kontaktinioasmensid. Peržvalga nerasta: 000056. Pabandykite šį (-iuos) URL adresą (-us), kad patikrintumėte, ar egzistuoja nuorodos duomenys: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="a7954-174">*Couldn't resolve the guid for the field: primarycontactid.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="a7954-175">*Nepavyko išspręsti lauko GUID: msdyn\_atsiskaitymopaskyra.paskyrosnumeris. Peržvalga nerasta: 1206-1. Pabandykite šį (-iuos) URL adresą (-us), kad patikrintumėte, ar egzistuoja nuorodos duomenys: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span><span class="sxs-lookup"><span data-stu-id="a7954-175">*Couldn't resolve the guid for the field: msdyn\_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span></span>

<span data-ttu-id="a7954-176">Jei eilutės kliento lentelėje turi verčių **KontaktinioAsmensId** ir **SąskaitosFaktūrosPaskyra** stulpeliuose, atlikite šiuos veiksmus, kad užbaigtumėte pradinį sinchronizavimą.</span><span class="sxs-lookup"><span data-stu-id="a7954-176">If any rows in the customer table have values in the **ContactPersonID** and **InvoiceAccount** columns, follow these steps to complete the initial synchronization.</span></span> <span data-ttu-id="a7954-177">Galite naudoti šį metodą bet kurioms paruoštoms eilutėms, pvz., **Paskyros** ir **Kontaktai**.</span><span class="sxs-lookup"><span data-stu-id="a7954-177">You can use this approach for any out-of-box tables, such **Accounts** and **Contacts**.</span></span>

1. <span data-ttu-id="a7954-178">„Finance and Operations“ programoje panaikinkite laukus **KontaktinioAsmensID** ir **SąskaitosFaktūrosPaskyra** stulpelius iš **Klientai V3 (paskyros)** susiejimo ir tada jį įrašykite.</span><span class="sxs-lookup"><span data-stu-id="a7954-178">In the Finance and Operations app, delete the **ContactPersonID** and **InvoiceAccount** columns from the **Customers V3 (accounts)** mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="a7954-179">Dvigubo rašymo susiejimo puslapyje, skirtame **Klientai V3 (paskyros)** **Lentelių susiejimai** skirtuke kairiajame filtre pasirinkite **Finance and Operations programa.Klientai V3**.</span><span class="sxs-lookup"><span data-stu-id="a7954-179">On the dual-write mapping page for **Customers V3 (accounts)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="a7954-180">Dešiniajame filtre pasirinkite **Dataverse.Paskyra**.</span><span class="sxs-lookup"><span data-stu-id="a7954-180">In the right filter, select **Dataverse.Account**.</span></span>
    2. <span data-ttu-id="a7954-181">Paieškoje įveskite **kontaktinis asmuo**, kad surastumėte **KontaktinioAsmensID** šaltinio stulpelį.</span><span class="sxs-lookup"><span data-stu-id="a7954-181">Search for **contactperson** to find the **ContactPersonID** source column.</span></span>
    3. <span data-ttu-id="a7954-182">Pasirinkite **Veiksmai** ir pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="a7954-182">Select **Actions**, and then select **Delete**.</span></span>

        ![„KontaktinioAsmensID” stulpelio naikinimas](media/cust_selfref3.png)

    4. <span data-ttu-id="a7954-184">Pakartokite šiuos veiksmus, kad panaikintumėte **„SąskaitosFaktūrosPaskyra”** stulpelį.</span><span class="sxs-lookup"><span data-stu-id="a7954-184">Repeat these steps to delete the **InvoiceAccount** column.</span></span>

        ![„SąskaitosFaktūrosPaskyros” stulpelio naikinimas](media/cust_selfref4.png)

    5. <span data-ttu-id="a7954-186">Įrašykite savo pakeitimus susiejime.</span><span class="sxs-lookup"><span data-stu-id="a7954-186">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="a7954-187">Išjunkite **Klientai V3** lentelės keitimų sekimą.</span><span class="sxs-lookup"><span data-stu-id="a7954-187">Turn off change tracking for the **Customers V3** table.</span></span>

    1. <span data-ttu-id="a7954-188">**Duomenų valdymas** darbo srityje pasirinkite **Duomenų lentelės** plytelę.</span><span class="sxs-lookup"><span data-stu-id="a7954-188">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="a7954-189">Pasirinkite **Klientai V3** lentelę.</span><span class="sxs-lookup"><span data-stu-id="a7954-189">Select the **Customers V3** table.</span></span>
    3. <span data-ttu-id="a7954-190">Veiksmų srityje pasirinkite **Parinktys**, tada – **Keitimų sekimas**.</span><span class="sxs-lookup"><span data-stu-id="a7954-190">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Keitimų sekimo parinkties pasirinkimas](media/selfref_options.png)

    4. <span data-ttu-id="a7954-192">Pasirinkite **Išjungti keitimų sekimą**.</span><span class="sxs-lookup"><span data-stu-id="a7954-192">Select **Disable Change Tracking**.</span></span>

        ![Išjungti keitimų sekimą pasirinkimas](media/selfref_tracking.png)

3. <span data-ttu-id="a7954-194">Paleiskite pradinę **Klientai V3 (Paskyros)** susiejimo sinchronizaciją.</span><span class="sxs-lookup"><span data-stu-id="a7954-194">Run initial synchronization for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="a7954-195">Pradinė sinchronizacija turėtų pavykti sėkmingai be klaidų.</span><span class="sxs-lookup"><span data-stu-id="a7954-195">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="a7954-196">Paleiskite pradinę **CDS Kontaktai V2 (kontaktai)** susiejimo sinchronizaciją.</span><span class="sxs-lookup"><span data-stu-id="a7954-196">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a7954-197">Yra du tokiu pačiu pavadinimu žemėlapiai.</span><span class="sxs-lookup"><span data-stu-id="a7954-197">There are two maps that have the same name.</span></span> <span data-ttu-id="a7954-198">Būtinai pasirinkite žemėlapį, turintį tokį aprašą **Išsami informacija** skirtuke: **Dvigubo rašymo šablonas, skirto FO.CDS Tiekėjo Kontaktai V2 su to CDS.Kontaktai sinchronizacijai atlikti. Reikalingas naujas paketas \[Dynamics365PraplėstaTiekimoGrandinė\].**</span><span class="sxs-lookup"><span data-stu-id="a7954-198">Be sure to select the map that has the following description on the **Details** tab: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span>

5. <span data-ttu-id="a7954-199">Pridėkite **„SąskaitosFaktūrosPaskyra”** ir **„KontaktinioAsmensId”** stulpelius vėl į **Klientai V3 (Paskyros)** susiejimą ir tada įrašykite jį.</span><span class="sxs-lookup"><span data-stu-id="a7954-199">Add the **InvoiceAccount** and **ContactPersonId** columns back to the **Customers V3 (Accounts)** mapping, and then save the mapping.</span></span> <span data-ttu-id="a7954-200">Abu **„SąskaitosFaktūrosPaskyra”** ir **„KontaktinioAsmensId”** stulpeliai dabar įtraukti į tiesioginio sinchronizavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="a7954-200">Both the **InvoiceAccount** column and the **ContactPersonId** column are now part of live synchronization mode again.</span></span> <span data-ttu-id="a7954-201">Kitame veiksme atliksite šių stulpelių sinchronizavimą.</span><span class="sxs-lookup"><span data-stu-id="a7954-201">In the next step, you will do the initial synchronization for these columns.</span></span>
6. <span data-ttu-id="a7954-202">Vėl paleiskite pradinę **Klientai V3 (Paskyros)** susiejimo sinchronizaciją.</span><span class="sxs-lookup"><span data-stu-id="a7954-202">Run initial synchronization again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="a7954-203">Kadangi keitimų sekimas yra išjungtas, **SąskaitosFaktūrosPaskyra** ir **KontaktinioAsmensId** duomenys iš „Finance and Operations“ programos į „Dataverse“ bus sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="a7954-203">Because change tracking is turned off, the data for **InvoiceAccount** and **ContactPersonId** will be synced from the Finance and Operations app to Dataverse.</span></span>
7. <span data-ttu-id="a7954-204">Norėdami sinchronizuoti **SąskaitosFaktūrosPaskyra** ir **KontaktinioAsmensId** duomenis iš „Dataverse“ į „Finance and Operations“ programą, turite naudoti duomenų integravimo projektą.</span><span class="sxs-lookup"><span data-stu-id="a7954-204">To sync the data for **InvoiceAccount** and **ContactPersonId** from Dataverse to the Finance and Operations app, you must use a data integration project.</span></span>

    1. <span data-ttu-id="a7954-205">„Power Apps“ sukurkite duomenų integravimo projektą tarp **Pardavimai.Paskyra** ir **Finance and Operations programos.Klientai V3** lentelių.</span><span class="sxs-lookup"><span data-stu-id="a7954-205">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** tables.</span></span> <span data-ttu-id="a7954-206">Duomenų kryptis turi būti iš „Dataverse“ į „Finance and Operations“ programą.</span><span class="sxs-lookup"><span data-stu-id="a7954-206">The data direction must be from Dataverse to the Finance and Operations app.</span></span> <span data-ttu-id="a7954-207">Kadangi **SąskaitosFaktūrosPaskyra** yra naujas atributas dvigubo rašymo funkcijoje, galite praleisti jos pradinę sinchronizaciją.</span><span class="sxs-lookup"><span data-stu-id="a7954-207">Because **InvoiceAccount** is a new attribute in dual-write, you might want to skip initial synchronization for it.</span></span> <span data-ttu-id="a7954-208">Prireikus daugiau informacijos, žr. [Duomenų integravimas į Dataverse](/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="a7954-208">For more information, see [Integrate data into Dataverse](/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="a7954-209">Toliau pateiktame paveikslėlyje parodytas projektas, kuris atnaujina **KlientoPaskyra** ir **KontaktinioAsmensId**.</span><span class="sxs-lookup"><span data-stu-id="a7954-209">The following illustration shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![Duomenų integravimo projektas, skirtas Kliento paskyrai ir KontaktinioAsmensId atnaujinti](media/cust_selfref6.png)

    2. <span data-ttu-id="a7954-211">Pridėkite įmonės kriterijus į filtrą, esantį „Dataverse“, kad tik eilutės, atitinkančios filtro kriterijus, būtų atnaujintos „Finance and Operations“ programoje.</span><span class="sxs-lookup"><span data-stu-id="a7954-211">Add the company criteria in the filter on the Dataverse side, so that only rows that match the filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="a7954-212">Norėdami pridėti filtrą, pažymėkite filtro mygtuką.</span><span class="sxs-lookup"><span data-stu-id="a7954-212">To add a filter, select the filter button.</span></span> <span data-ttu-id="a7954-213">Tada **Redaguoti užklausą** dialogo lange galite pridėti filtro užklausą, pavyzdžiui, **\_msdyn\_įmonė\_vertės lyg. '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="a7954-213">Then, in the **Edit query** dialog box, you can add a filter query such as **\_msdyn\_company\_value eq '\<guid\>'**.</span></span> 

        > <span data-ttu-id="a7954-214">[PASTABA] Jei filtro mygtuko nėra, sukurkite palaikymo kvitą, kad paprašytumėte duomenų integravimo komandos įjungti filtro funkciją jūsų nuomotojui.</span><span class="sxs-lookup"><span data-stu-id="a7954-214">[NOTE] If the filter button isn't present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span>

        <span data-ttu-id="a7954-215">Jei neįvesite filtro užklausos, skirtos **\_msdyn\_įmonės\_vertė**, visos eilutės bus sinchronizuotos.</span><span class="sxs-lookup"><span data-stu-id="a7954-215">If you don't enter a filter query for **\_msdyn\_company\_value**, all the rows will be synced.</span></span>

        ![Filtro užklausos pridėjimas](media/cust_selfref7.png)

    <span data-ttu-id="a7954-217">Pradinė eilučių sinchronizacija baigta.</span><span class="sxs-lookup"><span data-stu-id="a7954-217">The initial synchronization of the rows is now completed.</span></span>

8. <span data-ttu-id="a7954-218">„Finance and Operations” programoje vėl įjunkite **Klientai V3** lentelės keitimų sekimą.</span><span class="sxs-lookup"><span data-stu-id="a7954-218">In the Finance and Operations app, turn change tracking back on for the **Customers V3** table.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]