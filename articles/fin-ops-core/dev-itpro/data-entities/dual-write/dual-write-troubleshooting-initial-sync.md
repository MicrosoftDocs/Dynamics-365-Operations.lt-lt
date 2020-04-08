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
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172719"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="0d68f-103">Trikčių šalinimas pradinio sinchronizavimo metu</span><span class="sxs-lookup"><span data-stu-id="0d68f-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="0d68f-104">Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Common Data Service“ programų trikčių šalinimo informacija.</span><span class="sxs-lookup"><span data-stu-id="0d68f-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="0d68f-105">Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, kurios gali kilti pradinio sinchronizavimo metu.</span><span class="sxs-lookup"><span data-stu-id="0d68f-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="0d68f-106">Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų.</span><span class="sxs-lookup"><span data-stu-id="0d68f-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="0d68f-107">Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.</span><span class="sxs-lookup"><span data-stu-id="0d68f-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="0d68f-108">Patikrinkite, ar nėra pradinio sinchronizavimo klaidų „Finance and Operations” programoje</span><span class="sxs-lookup"><span data-stu-id="0d68f-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="0d68f-109">Įgalinus susiejimo šablonus, schemų būsena turi būti **Vykdoma**.</span><span class="sxs-lookup"><span data-stu-id="0d68f-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="0d68f-110">Jei būsena yra **Nevykdoma**, pradinio sinchronizavimo metu įvyko klaidų.</span><span class="sxs-lookup"><span data-stu-id="0d68f-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="0d68f-111">Norėdami peržiūrėti klaidas, pasirinkite skirtuką **Pradinio sinchronizavimo informacija** puslapyje **Dvigubas rašymas**.</span><span class="sxs-lookup"><span data-stu-id="0d68f-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Pradinio sinchronizavimo informacijos skirtukas](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="0d68f-113">Negalite užbaigti pradinio sinchronizavimo: 400 netinkama užklausa</span><span class="sxs-lookup"><span data-stu-id="0d68f-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="0d68f-114">**Reikiamas vaidmuo, norint spręsti problemą:** sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="0d68f-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="0d68f-115">Kai bandote vykdyti susiejimą ir pradinį sinchronizavimą, galite gauti tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="0d68f-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="0d68f-116">*Nuotolinis serveris pateikė klaidą: (400 netinkama užklausa), AX eksportavimo funkcija susidūrė su klaida*</span><span class="sxs-lookup"><span data-stu-id="0d68f-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="0d68f-117">Čia pateikiamas viso klaidos pranešimo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="0d68f-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="0d68f-118">Jei šį klaida įvyksta nuolat ir negalite užbaigti pradinio sinchronizavimo, atlikite šiuos veiksmus, kad išspręstumėte problemą.</span><span class="sxs-lookup"><span data-stu-id="0d68f-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="0d68f-119">Prisijunkite prie „Finance and Operations” programos virtualiosios mašinos.</span><span class="sxs-lookup"><span data-stu-id="0d68f-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="0d68f-120">Atidarykite „Microsoft“ valdymo konsolę.</span><span class="sxs-lookup"><span data-stu-id="0d68f-120">Open Microsoft Management Console.</span></span> 
3. <span data-ttu-id="0d68f-121">Eidami į sritį **Paslaugos**, įsitikinkite, kad veikia „Microsoft Dynamics 365” duomenų importavimo / eksportavimo sistemos paslauga.</span><span class="sxs-lookup"><span data-stu-id="0d68f-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="0d68f-122">Jeigu ji buvo sustabdyta, paleiskite ją iš naujo, nes ji yra reikalinga pradiniam sinchronizavimui atlikti.</span><span class="sxs-lookup"><span data-stu-id="0d68f-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="0d68f-123">Pradinio sinchronizavimo klaida: 403 draudžiama</span><span class="sxs-lookup"><span data-stu-id="0d68f-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="0d68f-124">Pradinio sinchronizavimo metu galite gauti tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="0d68f-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="0d68f-125">*\[Draudžiama\], nuotolinis serveris pateikė klaidą: (403 draudžiama), AX eksportavimo funkcija susidūrė su klaida*</span><span class="sxs-lookup"><span data-stu-id="0d68f-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="0d68f-126">Norėdami ištaisyti klaidą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0d68f-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="0d68f-127">Prisijungimas prie „Finance and Operations” programos.</span><span class="sxs-lookup"><span data-stu-id="0d68f-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="0d68f-128">Puslapyje **„Azure Active Directory” programos** panaikinkite klientą **DtAppID** ir vėl jį pridėkite.</span><span class="sxs-lookup"><span data-stu-id="0d68f-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![„Azure AD” programų sąrašas](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a><span data-ttu-id="0d68f-130">Nuorodos klaidos pradinio sinchronizavimo metu</span><span class="sxs-lookup"><span data-stu-id="0d68f-130">Self-reference failures during initial synchronization</span></span>

<span data-ttu-id="0d68f-131">Jeigu bet kurie jūsų susiejimų turi savo pačių nuorodų, galite gauti klaidos pranešimą, panašų į šį pavyzdį:</span><span class="sxs-lookup"><span data-stu-id="0d68f-131">You might receive an error message that resembles the following example if any of your mappings have self-references:</span></span>

<span data-ttu-id="0d68f-132">*Tiekėjo V2 klaida: įrašo ID: naujas įrašas, ErrorMessage: nepavyko išspręsti lauko guid: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Peržvalgos vertė nerasta. CN-001. Naudodami šį (šiuos) URL patikrinkite, ar yra nuorodos duomenys: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span><span class="sxs-lookup"><span data-stu-id="0d68f-132">*On the Vendors V2, the following error: Record Id: new record, ErrorMessage: Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup value was not found: CN-001. Try this URL(s) to check if the reference data exists: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span></span>

<span data-ttu-id="0d68f-133">Šio tipo klaida įvyksta atliekant susiejimų, kuriuose yra savo pačių nuorodų, pradinį sinchronizavimą.</span><span class="sxs-lookup"><span data-stu-id="0d68f-133">This type of error occurs during initial synchronization of mappings that have self-references.</span></span> <span data-ttu-id="0d68f-134">Ankstesniame pavyzdyje sąskaitos faktūros laukas nurodo tiekėjo objektą.</span><span class="sxs-lookup"><span data-stu-id="0d68f-134">In the preceding example, the field invoice account references the vendor entity.</span></span>

<span data-ttu-id="0d68f-135">Jei norite išspręsti šią problemą, galbūt turėsite vykdyti susiejimą du kartus, kol pradinis sinchronizavimas bus atliktas sėkmingai.</span><span class="sxs-lookup"><span data-stu-id="0d68f-135">To fix the issue, you might have to run the mapping two times before the initial synchronization is successful.</span></span>

