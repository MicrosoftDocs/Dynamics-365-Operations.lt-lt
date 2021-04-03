---
title: Egzemplioriaus kopijavimas
description: Galite naudoti „Microsoft Dynamics Lifecycle Services“ (LCS), kad nukopijuotumėte „Microsoft Dynamics 365 Human Resources“ duomenų bazę į smėlio dėžės aplinką.
author: andreabichsel
manager: tfehr
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e38abf3537d88bb147fbf0030999953025e5820f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466909"
---
# <a name="copy-an-instance"></a><span data-ttu-id="413bc-103">Egzemplioriaus kopijavimas</span><span class="sxs-lookup"><span data-stu-id="413bc-103">Copy an instance</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="413bc-104">Galite naudoti „Microsoft Dynamics Lifecycle Services“ (LCS), kad nukopijuotumėte „Microsoft Dynamics 365 Human Resources“ duomenų bazę į smėlio dėžės aplinką.</span><span class="sxs-lookup"><span data-stu-id="413bc-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="413bc-105">Jei turite kitą smėlio dėžės aplinką, taip pat galite kopijuoti duomenų bazę iš šios aplinkos į tikslinę smėlio dėžės aplinką.</span><span class="sxs-lookup"><span data-stu-id="413bc-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="413bc-106">Kad nukopijuotumėte egzempliorių, atminkite šiuos patarimus:</span><span class="sxs-lookup"><span data-stu-id="413bc-106">To copy an instance, keep the following tips in mind:</span></span>

- <span data-ttu-id="413bc-107">„Human Resources“ egzempliorius, kurį norite perrašyti, turi būti smėlio dėžės aplinka.</span><span class="sxs-lookup"><span data-stu-id="413bc-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="413bc-108">Aplinkos, iš kurių ir į kurias kopijuojate, privalo būti tame pačiame regione.</span><span class="sxs-lookup"><span data-stu-id="413bc-108">The environments you're copying from and to must be in the same region.</span></span> <span data-ttu-id="413bc-109">Negalite kopijuoti skirtinguose regionuose.</span><span class="sxs-lookup"><span data-stu-id="413bc-109">You can't copy across regions.</span></span>

- <span data-ttu-id="413bc-110">Turite būti paskirties aplinkos administratorius, kad nukopijavę egzempliorių galėtumėte prisijungti prie jo.</span><span class="sxs-lookup"><span data-stu-id="413bc-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="413bc-111">Kai kopijuojate „Human Resources“ duomenų bazę, nenukopijuojate elementų (programų arba duomenų), esančių „Microsoft Power Apps“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="413bc-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft Power Apps environment.</span></span> <span data-ttu-id="413bc-112">Norėdami gauti informacijos apie tai, kaip kopijuoti „Power Apps“ aplinkos elementus, žr. [Aplinkos kopijavimas](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="413bc-112">For information about how to copy elements in a Power Apps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="413bc-113">„Power Apps“ egzempliorius, kurį norite perrašyti, turi būti smėlio dėžės aplinka.</span><span class="sxs-lookup"><span data-stu-id="413bc-113">The Power Apps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="413bc-114">Norėdami pakeisti „Power Apps“ gamybos aplinką į smėlio dėžės aplinką, turite būti visuotinis nuomotojo administratorius.</span><span class="sxs-lookup"><span data-stu-id="413bc-114">You must be a global tenant admin to change a Power Apps production environment to a sandbox environment.</span></span> <span data-ttu-id="413bc-115">Daugiau informacijos apie „Power Apps“ aplinkos keitimą žr. [Egzemplioriaus keitimas](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="413bc-115">For more information about changing a Power Apps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

- <span data-ttu-id="413bc-116">Jei kopijuojate egzempliorių į savo smėlio dėžės aplinką ir norite integruoti savo smėlio dėžės aplinką į „Dataverse”, privalote pasirinktinius laukus iš naujo taikyti „Dataverse” lenteles.</span><span class="sxs-lookup"><span data-stu-id="413bc-116">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span> <span data-ttu-id="413bc-117">Žr. [Taikyti pasirinktinius laukus „Dataverse”](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span><span class="sxs-lookup"><span data-stu-id="413bc-117">See [Apply custom fields to Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="413bc-118">„Human Resources“ duomenų bazės kopijavimo poveikis</span><span class="sxs-lookup"><span data-stu-id="413bc-118">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="413bc-119">Šie įvykiai įvyksta, kai kopijuojate „Human Resources“ duomenų bazę:</span><span class="sxs-lookup"><span data-stu-id="413bc-119">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="413bc-120">Kopijavimo procesu trinama esama duomenų bazė, esanti paskirties aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="413bc-120">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="413bc-121">Kai kopijavimo procesas baigtas, negalėsite atkurti esamos duomenų bazės.</span><span class="sxs-lookup"><span data-stu-id="413bc-121">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="413bc-122">Paskirties aplinka nebus pasiekiama, kol nebus baigtas kopijavimo procesas.</span><span class="sxs-lookup"><span data-stu-id="413bc-122">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="413bc-123">Dokumentai, esantys „Microsoft Azure“ didelių dvejetainių objektų saugykloje, nėra kopijuojami iš vienos aplinkos į kitą.</span><span class="sxs-lookup"><span data-stu-id="413bc-123">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="413bc-124">Todėl bet kurie pridėti dokumentai ir šablonai nebus kopijuojami ir liks šaltinio aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="413bc-124">As a result, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="413bc-125">Visi vartotojai išskyrus administratoriaus teises turintį vartotoją ir kiti vidinių paslaugų vartotojų klientai nebus pasiekiami.</span><span class="sxs-lookup"><span data-stu-id="413bc-125">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="413bc-126">Administratoriaus vartotojas gali panaikinti arba paslėpti duomenis prieš suteikiant galimybę kitiems vartotojams vėl prisijungti prie sistemos.</span><span class="sxs-lookup"><span data-stu-id="413bc-126">The Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="413bc-127">Administratoriaus teises turintis vartotojas turi atlikti būtinus konfigūravimo keitimus, pvz., iš naujo sujungti integravimo galinius punktus su konkrečiomis tarnybomis arba konkrečiais URL.</span><span class="sxs-lookup"><span data-stu-id="413bc-127">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="413bc-128">„Human Resources“ duomenų bazės kopijavimas</span><span class="sxs-lookup"><span data-stu-id="413bc-128">Copy the Human Resources database</span></span>

<span data-ttu-id="413bc-129">Norėdami atlikti šią užduotį, pirmiausia nukopijuokite egzempliorių, tada prisijunkite prie „Microsoft Power Platform“ administravimo centro, kad nukopijuotumėte savo „Power Apps“ aplinką.</span><span class="sxs-lookup"><span data-stu-id="413bc-129">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your Power Apps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="413bc-130">Kai kopijuojate egzempliorių, duomenų bazė ištrinama paskirties egzemplioriuje.</span><span class="sxs-lookup"><span data-stu-id="413bc-130">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="413bc-131">Šio proceso metu paskirties egzemplioriaus naudoti negalima.</span><span class="sxs-lookup"><span data-stu-id="413bc-131">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="413bc-132">Prisijunkite prie LCS ir pasirinkite LCS projektą, kuriame yra egzempliorius, kurį norite kopijuoti.</span><span class="sxs-lookup"><span data-stu-id="413bc-132">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="413bc-133">LCS projekte pasirinkite plytelę **Programos „Human Resources“ valdymas**.</span><span class="sxs-lookup"><span data-stu-id="413bc-133">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="413bc-134">Pasirinkite kopijuotiną egzempliorių ir pasirinkite **Kopijuoti**.</span><span class="sxs-lookup"><span data-stu-id="413bc-134">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="413bc-135">Užduočių srityje **Kopijuoti egzempliorių** pasirinkite egzempliorių, kurį norite perrašyti, tada – **Kopijuoti**.</span><span class="sxs-lookup"><span data-stu-id="413bc-135">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="413bc-136">Palaukite, kol lauko **Kopijuoti būseną** reikšmė bus atnaujinta į **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="413bc-136">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="413bc-137">Perrašytino egzemplioriaus pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="413bc-137">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="413bc-138">Pažymėkite **„Power Platform“** ir prisijunkite prie „Microsoft Power Platform“ admininstravimo centro.</span><span class="sxs-lookup"><span data-stu-id="413bc-138">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="413bc-139">„Power Platform“ pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="413bc-139">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="413bc-140">Pasirinkite kopijuotiną „Power Apps“ aplinką ir pasirinkite **Kopijuoti**.</span><span class="sxs-lookup"><span data-stu-id="413bc-140">Select the Power Apps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="413bc-141">Kai kopijavimo procesas baigtas, prisijunkite prie paskirties egzemplioriaus ir įjunkite „Dataverse“ integravimą.</span><span class="sxs-lookup"><span data-stu-id="413bc-141">When the copy process is completed, sign in to the target instance, and enable Dataverse integration.</span></span> <span data-ttu-id="413bc-142">Daugiau informacijos ir instrukcijų žr. [„Dataverse“ integravimo konfigūravimas](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="413bc-142">For more information and instructions, see [Configure Dataverse integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="413bc-143">Duomenų elementai ir būsenos</span><span class="sxs-lookup"><span data-stu-id="413bc-143">Data elements and statuses</span></span>

<span data-ttu-id="413bc-144">Kai kopijuojate „Human Resources“ egzempliorių, šie duomenų elementai nebus nukopijuoti:</span><span class="sxs-lookup"><span data-stu-id="413bc-144">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="413bc-145">El. pašto adresai lentelėje **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="413bc-145">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="413bc-146">Paketinių užduočių retrospektyva lentelėse **BatchJobHistory**, **BatchHistory** ir **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="413bc-146">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="413bc-147">Paprastųjų pašto siuntų protokolo (SMTP) slaptažodis lentelėje **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="413bc-147">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="413bc-148">SMTP perdavimo serveris lentelėje **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="413bc-148">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="413bc-149">Spausdinimo valdymo parametrai lentelėse **PrintMgmtSettings** ir **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="413bc-149">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="413bc-150">Aplinkai būdingi įrašai lentelėse **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** ir **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="413bc-150">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="413bc-151">Dokumentų priedai, esantys „DocuValue“ lentelėje.</span><span class="sxs-lookup"><span data-stu-id="413bc-151">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="413bc-152">Šiuose prieduose yra „Microsoft Office“ šablonų, perrašytų šaltinio aplinkoje</span><span class="sxs-lookup"><span data-stu-id="413bc-152">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="413bc-153">Ryšio eilutės lentelėje **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="413bc-153">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="413bc-154">Kai kurie iš šių elementų negali būti kopijuojami, nes jie būdingi tam tikrai aplinkai.</span><span class="sxs-lookup"><span data-stu-id="413bc-154">Some of these elements aren't copied because they're environment-specific.</span></span> <span data-ttu-id="413bc-155">Pavyzdžiai apima įrašus **BatchServerConfig** ir **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="413bc-155">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="413bc-156">Kiti elementai nėra nukopijuoti dėl palaikymo bilietų apimties.</span><span class="sxs-lookup"><span data-stu-id="413bc-156">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="413bc-157">Pvz.:</span><span class="sxs-lookup"><span data-stu-id="413bc-157">For example:</span></span>

- <span data-ttu-id="413bc-158">Dubliuoti el. laiškai gali būti siunčiami, nes SMTP vis dar yra įgalintas vartotojo priėmimo bandymų (smėlio dėžės) aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="413bc-158">Duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment.</span></span>

- <span data-ttu-id="413bc-159">Negaliojantys integravimo pranešimai gali būti siunčiami, nes paketinės užduotys vis dar yra įgalintos.</span><span class="sxs-lookup"><span data-stu-id="413bc-159">Invalid integration messages might be sent because batch jobs are still enabled.</span></span>

- <span data-ttu-id="413bc-160">Vartotojai gali būti įgalinti prieš administratoriams atliekant valymo po atnaujinimo veiksmus.</span><span class="sxs-lookup"><span data-stu-id="413bc-160">Users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="413bc-161">Taip pat, šios būsenos keičiasi, kai nukopijuojate egzempliorių:</span><span class="sxs-lookup"><span data-stu-id="413bc-161">Also, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="413bc-162">Visi vartotojai, išskyrus administratorių, nustatyti kaip **Išjungtas**.</span><span class="sxs-lookup"><span data-stu-id="413bc-162">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="413bc-163">Visos paketinės užduotys, išskyrus kai kurias sistemos užduotis, yra nustatytos kaip **Sulaikyti**.</span><span class="sxs-lookup"><span data-stu-id="413bc-163">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="413bc-164">Aplinkos administratorius</span><span class="sxs-lookup"><span data-stu-id="413bc-164">Environment admin</span></span>

<span data-ttu-id="413bc-165">Visi paskirties smėlio dėžės aplinkos vartotojai, įskaitant administratorius, pakeičiami šaltinio aplinkos vartotojais.</span><span class="sxs-lookup"><span data-stu-id="413bc-165">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="413bc-166">Prieš tai kai nukopijuojate egzempliorių, įsitikinkite, kad šaltinio aplinkoje esate Administratorius.</span><span class="sxs-lookup"><span data-stu-id="413bc-166">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="413bc-167">Jeigu nesate, negalite prisijungti į paskirties smėlio dėžės aplinką po to, kai kopijavimas buvo atliktas.</span><span class="sxs-lookup"><span data-stu-id="413bc-167">If you aren't, you can't sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="413bc-168">Visi ne administratoriaus teises turintys vartotojai paskirties smėlio dėžės aplinkoje yra išjungti, kad būtų užkirstas kelias nepageidaujamiems prisijungimams smėlio dėžės aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="413bc-168">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="413bc-169">Jei reikia, administratoriai gali iš naujo įgalinti vartotojus.</span><span class="sxs-lookup"><span data-stu-id="413bc-169">Administrators can reenable users if needed.</span></span>

## <a name="apply-custom-fields-to-dataverse"></a><span data-ttu-id="413bc-170">Taikyti pasirinktinius laukus „Dataverse”</span><span class="sxs-lookup"><span data-stu-id="413bc-170">Apply custom fields to Dataverse</span></span>

<span data-ttu-id="413bc-171">Jei kopijuojate egzempliorių į savo smėlio dėžės aplinką ir norite integruoti savo smėlio dėžės aplinką į „Dataverse”, privalote pasirinktinius laukus iš naujo taikyti „Dataverse” lenteles.</span><span class="sxs-lookup"><span data-stu-id="413bc-171">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span>

<span data-ttu-id="413bc-172">Kiekvienam pasirinktiniam laukui, kurie rodomi „Dataverse” lentelėse, atlikite šiuos veiksmus: </span><span class="sxs-lookup"><span data-stu-id="413bc-172">For each custom field that's exposed on Dataverse tables, do the following steps:</span></span>

1. <span data-ttu-id="413bc-173">Eikite į pasirinktinį lauką ir pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="413bc-173">Go to the custom field and select **Edit**.</span></span>

2. <span data-ttu-id="413bc-174">Anuliuokite **Įgalinti** lauką kiekvienam cdm_\* objektui, kuriam įjungtas pasirinktinis laukas.</span><span class="sxs-lookup"><span data-stu-id="413bc-174">Unselect the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

3. <span data-ttu-id="413bc-175">Pasirinkite **Taikyti pakeitimus**.</span><span class="sxs-lookup"><span data-stu-id="413bc-175">Select **Apply Changes**.</span></span>

4. <span data-ttu-id="413bc-176">Dar kartą pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="413bc-176">Select **Edit** again.</span></span>

5. <span data-ttu-id="413bc-177">Pasirinkite **Įgalinti** lauką kiekvienam cdm_\* objektui, kuriam įjungtas pasirinktinis laukas.</span><span class="sxs-lookup"><span data-stu-id="413bc-177">Select the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

6. <span data-ttu-id="413bc-178">Dar kartą pasirinkite **Taikyti pakeitimus**.</span><span class="sxs-lookup"><span data-stu-id="413bc-178">Select **Apply Changes** again.</span></span>

<span data-ttu-id="413bc-179">Anuliavimo, pakeitimų taikymo, perrinkimo ir pakeitimų taikymo iš naujo procesas ragina schemos „Dataverse” atnaujinimus, kad būtų įtraukti pasirinktiniai laukai.</span><span class="sxs-lookup"><span data-stu-id="413bc-179">The process of unselecting, applying changes, reselecting, and reapplying changes prompts the schema to update in Dataverse to include the custom fields.</span></span>

<span data-ttu-id="413bc-180">Norėdami gauti daugiau informacijos apie pasirinktinius laukus, žr. [Darbas su pasirinktiniais laukais ir jų kūrimas](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span><span class="sxs-lookup"><span data-stu-id="413bc-180">For more information about custom fields, see [Create and work with custom fields](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span></span>

## <a name="see-also"></a><span data-ttu-id="413bc-181">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="413bc-181">See also</span></span>

[<span data-ttu-id="413bc-182">„Human Resources“ parengimas</span><span class="sxs-lookup"><span data-stu-id="413bc-182">Provision Human Resources</span></span>](hr-admin-setup-provision.md)</br>
[<span data-ttu-id="413bc-183">Egzemplioriaus šalinimas</span><span class="sxs-lookup"><span data-stu-id="413bc-183">Remove an instance</span></span>](hr-admin-setup-remove-instance.md)</br>
[<span data-ttu-id="413bc-184">Atnaujinimo procesas</span><span class="sxs-lookup"><span data-stu-id="413bc-184">Update process</span></span>](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]