---
title: Tiesioginio sinchronizavimo trikčių šalinimas
description: Šioje temoje pateikiama trikčių šalinimo informacija, kuri gali padėti išspręsti problemas, susijusias su tiesioginiu sinchronizavimu.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 82bdcc71196c22689cc65601f98187aaa9e5e9d6
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997307"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="1524c-103">Tiesioginio sinchronizavimo trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="1524c-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="1524c-104">Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Common Data Service“ programų trikčių šalinimo informacija.</span><span class="sxs-lookup"><span data-stu-id="1524c-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="1524c-105">Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, susijusias su tiesioginiu sinchronizavimu.</span><span class="sxs-lookup"><span data-stu-id="1524c-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1524c-106">Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų.</span><span class="sxs-lookup"><span data-stu-id="1524c-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="1524c-107">Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.</span><span class="sxs-lookup"><span data-stu-id="1524c-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="1524c-108">Tiesioginis sinchronizavimas pateikia klaidą „403 draudžiama“, kai kuriate įrašą „Finance and Operations” programoje</span><span class="sxs-lookup"><span data-stu-id="1524c-108">Live synchronization throws a 403 Forbidden error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="1524c-109">Kai „Finance and Operations” programoje kuriate įrašą, galite gauti tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="1524c-109">You might receive the following error message when you create a record in a Finance and Operations app:</span></span>

<span data-ttu-id="1524c-110">*\[{\\"klaida\\":{\\"kodas\\":\\"0x80072560\\",\\"pranešimas\\":\\"Vartotojas nėra organizacijos narys.\\"}}\], Nuotolinis serveris pateikė klaidą: (403) draudžiama."}}".*</span><span class="sxs-lookup"><span data-stu-id="1524c-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="1524c-111">Norėdami išspręsti problemą, atlikite veiksmus, pateiktus skyriuje [Sistemos reikalavimai ir būtinosios sąlygos](requirements-and-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="1524c-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="1524c-112">Norėdami atlikti šiuos veiksmus, dvigubo rašymo programos vartotojai, sukurti „Common Data Service”, privalo turėti sistemos administratoriaus vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="1524c-112">To complete those steps, the dual-write application users who are created in Common Data Service must have the system admin role.</span></span> <span data-ttu-id="1524c-113">Numatytoji komanda savininkė taip pat turi turėti sistemos administratoriaus vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="1524c-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="1524c-114">Tiesioginis bet kokio objekto sinchronizavimas nuolat pateikia panašią klaidą, kai kuriate įrašą „Finance and Operations” programoje</span><span class="sxs-lookup"><span data-stu-id="1524c-114">Live synchronization for any entity consistently throws a similar error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="1524c-115">**Reikiamas vaidmuo, norint spręsti problemą:** sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="1524c-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="1524c-116">Kaskart bandydami įrašyti objekto duomenis „Finance and Operations” programoje, galite gauti klaidos pranešimą, panašų į pateiktą toliau:</span><span class="sxs-lookup"><span data-stu-id="1524c-116">You might receive an error message like the following every time that you try to save entity data in a Finance and Operations app:</span></span>

<span data-ttu-id="1524c-117">*Nepavyksta įrašyti duomenų bazės pakeitimų. Darbo vienetas negali įvykdyti operacijos. Nepavyksta įrašyti duomenų į objekto uoms. Įrašyti į UnitOfMeasureEntity nepavyko, nes nepavyko sinchronizuoti klaidos pranešimo su objekto uoms.*</span><span class="sxs-lookup"><span data-stu-id="1524c-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="1524c-118">Norėdami išspręsti problemą, turite įsitikinti, kad būtini nuorodos duomenys yra ir „Finance and Operations” programoje, ir „Common Data Service”.</span><span class="sxs-lookup"><span data-stu-id="1524c-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Common Data Service.</span></span> <span data-ttu-id="1524c-119">Pavyzdžiui, jei klientas, kuriame esate „Finance and Operations” programoje, priklauso konkrečiai klientų grupei, įsitikinkite, kad ši klientų grupė yra „Common Data Service”.</span><span class="sxs-lookup"><span data-stu-id="1524c-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Common Data Service.</span></span>

<span data-ttu-id="1524c-120">Jei duomenys yra abiejose programose ir patvirtinote, kad problema nėra susijusi su duomenimis, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="1524c-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="1524c-121">Sustabdykite susijusį objektą.</span><span class="sxs-lookup"><span data-stu-id="1524c-121">Stop the related entity.</span></span>
2. <span data-ttu-id="1524c-122">Prisijunkite prie „Finance and Operations” programos ir įsitikinkite, kad neveikiančio objekto įrašai yra DualWriteProjectConfiguration ir DualWriteProjectFieldConfiguration lentelėse.</span><span class="sxs-lookup"><span data-stu-id="1524c-122">Sign in to the Finance and Operations app, and make sure that records for the failing entity exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="1524c-123">Pavyzdžiui, čia vaizduojama, kaip atrodo užklausa, jei objektas **Klientai** neveikia.</span><span class="sxs-lookup"><span data-stu-id="1524c-123">For example, here is what the query looks like if the **Customers** entity is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="1524c-124">Jei net jums sustabdžius objekto susiejimą, yra neveikiančio objekto įrašų, panaikinkite įrašus, susijusius su neveikiančiu objektu.</span><span class="sxs-lookup"><span data-stu-id="1524c-124">If there are records for the failing entity even after you stop the entity mapping, delete the records that are related to the failing entity.</span></span> <span data-ttu-id="1524c-125">Norėdami panaikinti įrašą, lentelėje DualWriteProjectConfiguration pasižymėkite stulpelį **projectname** ir lentelėje DualWriteProjectFieldConfiguration raskite įrašą naudodami projekto pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="1524c-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the record in the DualWriteProjectFieldConfiguration table by using the project name to delete the record.</span></span>
4. <span data-ttu-id="1524c-126">Pradėkite susiejimą su objektu.</span><span class="sxs-lookup"><span data-stu-id="1524c-126">Start the entity mapping.</span></span> <span data-ttu-id="1524c-127">Patikrinkite, ar sinchronizuojant duomenis nekyla problemų.</span><span class="sxs-lookup"><span data-stu-id="1524c-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="1524c-128">Skaitymo arba rašymo teisių klaidų tvarkymas, kuriant duomenis „Finance and Operations” programoje</span><span class="sxs-lookup"><span data-stu-id="1524c-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="1524c-129">Kai kuriate duomenis „Finance and Operations” programoje, galite gauti klaidos pranešimą „Netinkama užklausa“, panašų į toliau pateiktą pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="1524c-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![Klaidos pranešimo „Netinkama užklausa“ pavyzdys](media/error_record_id_source.png)

<span data-ttu-id="1524c-131">Norėdami išspręsti šią problemą, turite priskirti tinkamą saugos vaidmenį susieto „Dynamics 365 Sales” arba „Dynamics 365 Customer Service” verslo struktūros vieneto komandai, kad įgalintumėte trūkstamą teisę.</span><span class="sxs-lookup"><span data-stu-id="1524c-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="1524c-132">„Finance and Operations” programoje raskite verslo struktūros vienetą, susietą duomenų integravimo ryšio rinkinyje.</span><span class="sxs-lookup"><span data-stu-id="1524c-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![Organizacijos susiejimas](media/mapped_business_unit.png)

2. <span data-ttu-id="1524c-134">Prisijunkite prie aplinkos modeliu grįstoje „Dynamics 365” programoje, pereikite į **Parametras \> Sauga** ir raskite susieto verslo struktūros vieneto komandą.</span><span class="sxs-lookup"><span data-stu-id="1524c-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security** , and find the team of the mapped business unit.</span></span>

    ![Susieto verslo struktūros vieneto komanda](media/setting_security_page.png)

3. <span data-ttu-id="1524c-136">Atidarykite komandos puslapį, kad jį redaguotumėte, tada pasirinkite **Tvarkyti vaidmenis** , kad atidarytumėte dialogo langą **Tvarkyti komandos vaidmenis**.</span><span class="sxs-lookup"><span data-stu-id="1524c-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![Vaidmenų tvarkymo mygtukas](media/manage_team_roles.png)

4. <span data-ttu-id="1524c-138">Priskirkite vaidmenį, turintį skaitymo / rašymo teisę, skirtą atitinkamiems objektams, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1524c-138">Assign the role that has the read/write privilege for the relevant entities, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-common-data-service-environment"></a><span data-ttu-id="1524c-139">Sinchronizavimo problemų aplinkoje, kurioje neseniai buvo pakeista „Common Data Service” aplinka, sprendimas</span><span class="sxs-lookup"><span data-stu-id="1524c-139">Fix synchronization issues in an environment that has a recently changed Common Data Service environment</span></span>

<span data-ttu-id="1524c-140">**Reikiamas vaidmuo, norint spręsti problemą:** sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="1524c-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="1524c-141">Kai „Finance and Operations” programoje kuriate duomenis, galite gauti tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="1524c-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="1524c-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":" **Nepavyksta sugeneruoti mokamosios krovos objektui CustCustomerV3Entity** ","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Nepavyko sukurti mokamosios krovos, įvyko klaida „Netinkamas URI“: URI yra tuščias."}\],"isErrorCountUpdated":true}*</span><span class="sxs-lookup"><span data-stu-id="1524c-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":" **Unable to generate payload for entity CustCustomerV3Entity** ","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="1524c-143">Čia vaizduojama, kaip atrodo klaida modeliu grįstoje „Dynamics 365” programoje:</span><span class="sxs-lookup"><span data-stu-id="1524c-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="1524c-144">*Įvyko netikėta ISV kodo klaida. (ErrorType = ClientError) Netikėta priedo išimtis (vykdyti): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: nepavyko apdoroti objekto sąskaitos – nepavyko užmegzti ryšio, nes šalis, prie kurios buvo jungiamasi, tinkamai neatsakė praėjus tam tikram laiko tarpui, arba užmegztas ryšys nutruko, nes prijungtas pagrindinis kompiuteris neatsakė*</span><span class="sxs-lookup"><span data-stu-id="1524c-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="1524c-145">Ši klaida įvyksta, kai „Common Data Service” aplinka netinkamai paleidžiama iš naujo tuo pačiu laiku, kai bandote sukurti duomenis „Finance and Operations” programoje.</span><span class="sxs-lookup"><span data-stu-id="1524c-145">This error occurs when the Common Data Service environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="1524c-146">Norėdami ištaisyti klaidą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1524c-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="1524c-147">Prisijunkite prie „Finance and Operations” virtualiosios mašinos (VM), atidarykite SQL serverio valdymo studiją (SSMS) ir ieškokite įrašų lentelėje DUALWRITEPROJECTCONFIGURATIONENTITY, kur **internalentityname** lygu **Klientai V3** ir **externalentityname** lygu **paskyros**.</span><span class="sxs-lookup"><span data-stu-id="1524c-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for records in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="1524c-148">Štai kaip atrodo užklausa.</span><span class="sxs-lookup"><span data-stu-id="1524c-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="1524c-149">Naudokite projekto pavadinimą iš ankstesnės užklausos rezultatų, kad vykdytumėte kitą užklausą.</span><span class="sxs-lookup"><span data-stu-id="1524c-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="1524c-150">Įsitikinkite, kad stulpelyje **externalenvironmentURL** yra tinkamas „Common Data Service” arba programos URL.</span><span class="sxs-lookup"><span data-stu-id="1524c-150">Make sure that the **externalenvironmentURL** column has the correct Common Data Service or app URL.</span></span> <span data-ttu-id="1524c-151">Panaikinkite visus pasikartojančius įrašus, kurie nurodo netinkamą „Common Data Service” URL.</span><span class="sxs-lookup"><span data-stu-id="1524c-151">Delete any duplicate records that point to the wrong Common Data Service URL.</span></span> <span data-ttu-id="1524c-152">Panaikinkite atitinkamus įrašus DUALWRITEPROJECTFIELDCONFIGURATION ir DUALWRITEPROJECTCONFIGURATION lentelėse.</span><span class="sxs-lookup"><span data-stu-id="1524c-152">Delete the corresponding records in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="1524c-153">Sustabdykite susiejimą su objektu, tada paleiskite jį iš naujo</span><span class="sxs-lookup"><span data-stu-id="1524c-153">Stop the entity mapping, and then restart it</span></span>
