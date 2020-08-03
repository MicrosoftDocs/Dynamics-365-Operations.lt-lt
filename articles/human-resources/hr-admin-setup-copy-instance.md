---
title: Egzemplioriaus kopijavimas
description: Galite naudoti „Microsoft Dynamics Lifecycle Services“ (LCS), kad nukopijuotumėte „Microsoft Dynamics 365 Human Resources“ duomenų bazę į smėlio dėžės aplinką.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: b14baf49517f5d606038af20366944788b22eba2
ms.sourcegitcommit: 1ec931f8fe86bde27f6def36ea214a2a05fb22f6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/13/2020
ms.locfileid: "3554330"
---
# <a name="copy-an-instance"></a><span data-ttu-id="83530-103">Egzemplioriaus kopijavimas</span><span class="sxs-lookup"><span data-stu-id="83530-103">Copy an instance</span></span>

<span data-ttu-id="83530-104">Galite naudoti „Microsoft Dynamics Lifecycle Services“ (LCS), kad nukopijuotumėte „Microsoft Dynamics 365 Human Resources“ duomenų bazę į smėlio dėžės aplinką.</span><span class="sxs-lookup"><span data-stu-id="83530-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="83530-105">Jei turite kitą smėlio dėžės aplinką, taip pat galite kopijuoti duomenų bazę iš šios aplinkos į tikslinę smėlio dėžės aplinką.</span><span class="sxs-lookup"><span data-stu-id="83530-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="83530-106">Norėdami nukopijuoti egzempliorių, turite užtikrinti, kad atitinkamos šios sąlygos:</span><span class="sxs-lookup"><span data-stu-id="83530-106">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="83530-107">„Human Resources“ egzempliorius, kurį norite perrašyti, turi būti smėlio dėžės aplinka.</span><span class="sxs-lookup"><span data-stu-id="83530-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="83530-108">Aplinkos, iš kurių kopijuojate, turi būti tame pačiame regione.</span><span class="sxs-lookup"><span data-stu-id="83530-108">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="83530-109">Negalite kopijuoti skirtinguose regionuose.</span><span class="sxs-lookup"><span data-stu-id="83530-109">You can't copy across regions.</span></span>

- <span data-ttu-id="83530-110">Turite būti paskirties aplinkos administratorius, kad nukopijavę egzempliorių galėtumėte prisijungti prie jo.</span><span class="sxs-lookup"><span data-stu-id="83530-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="83530-111">Kai kopijuojate „Human Resources“ duomenų bazę, nenukopijuojate elementų (programų arba duomenų), esančių „Microsoft PowerApps“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="83530-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="83530-112">Norėdami gauti informacijos apie tai, kaip kopijuoti „PowerApps“ aplinkos elementus, žr. [Aplinkos kopijavimas](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="83530-112">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="83530-113">„PowerApps“ egzempliorius, kurį norite perrašyti, turi būti smėlio dėžės aplinka.</span><span class="sxs-lookup"><span data-stu-id="83530-113">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="83530-114">Norėdami pakeisti „PowerApps“ gamybos aplinką į smėlio dėžės aplinką, turite būti visuotinis nuomotojo administratorius.</span><span class="sxs-lookup"><span data-stu-id="83530-114">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="83530-115">Daugiau informacijos apie „PowerApps“ aplinkos keitimą žr. [Egzemplioriaus keitimas](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="83530-115">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="83530-116">„Human Resources“ duomenų bazės kopijavimo poveikis</span><span class="sxs-lookup"><span data-stu-id="83530-116">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="83530-117">Šie įvykiai įvyksta, kai kopijuojate „Human Resources“ duomenų bazę:</span><span class="sxs-lookup"><span data-stu-id="83530-117">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="83530-118">Kopijavimo procesu trinama esama duomenų bazė, esanti paskirties aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="83530-118">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="83530-119">Kai kopijavimo procesas baigtas, negalėsite atkurti esamos duomenų bazės.</span><span class="sxs-lookup"><span data-stu-id="83530-119">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="83530-120">Paskirties aplinka nebus pasiekiama, kol nebus baigtas kopijavimo procesas.</span><span class="sxs-lookup"><span data-stu-id="83530-120">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="83530-121">Dokumentai, esantys „Microsoft Azure“ didelių dvejetainių objektų saugykloje, nėra kopijuojami iš vienos aplinkos į kitą.</span><span class="sxs-lookup"><span data-stu-id="83530-121">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="83530-122">Todėl visi pridėti dokumentai ir šablonai nebus nukopijuoti ir liks šaltinio aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="83530-122">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="83530-123">Visi vartotojai išskyrus administratoriaus teises turintį vartotoją ir kiti vidinių paslaugų vartotojų klientai nebus pasiekiami.</span><span class="sxs-lookup"><span data-stu-id="83530-123">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="83530-124">Todėl administratoriaus teises turintis vartotojas gali panaikinti arba paslėpti duomenis, prieš tai, kai prie sistemos galės prisijungti kiti vartotojai.</span><span class="sxs-lookup"><span data-stu-id="83530-124">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="83530-125">Administratoriaus teises turintis vartotojas turi atlikti būtinus konfigūravimo keitimus, pvz., iš naujo sujungti integravimo galinius punktus su konkrečiomis tarnybomis arba konkrečiais URL.</span><span class="sxs-lookup"><span data-stu-id="83530-125">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="83530-126">„Human Resources“ duomenų bazės kopijavimas</span><span class="sxs-lookup"><span data-stu-id="83530-126">Copy the Human Resources database</span></span>

<span data-ttu-id="83530-127">Norėdami atlikti šią užduotį, pirmiausia nukopijuokite egzempliorių, tada prisijunkite prie „Microsoft Power Platform“ administravimo centro, kad nukopijuotumėte savo „PowerApps“ aplinką.</span><span class="sxs-lookup"><span data-stu-id="83530-127">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="83530-128">Kai kopijuojate egzempliorių, duomenų bazė ištrinama paskirties egzemplioriuje.</span><span class="sxs-lookup"><span data-stu-id="83530-128">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="83530-129">Šio proceso metu paskirties egzemplioriaus naudoti negalima.</span><span class="sxs-lookup"><span data-stu-id="83530-129">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="83530-130">Prisijunkite prie LCS ir pasirinkite LCS projektą, kuriame yra egzempliorius, kurį norite kopijuoti.</span><span class="sxs-lookup"><span data-stu-id="83530-130">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="83530-131">LCS projekte pasirinkite plytelę **Programos „Human Resources“ valdymas**.</span><span class="sxs-lookup"><span data-stu-id="83530-131">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="83530-132">Pasirinkite kopijuotiną egzempliorių ir pasirinkite **Kopijuoti**.</span><span class="sxs-lookup"><span data-stu-id="83530-132">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="83530-133">Užduočių srityje **Kopijuoti egzempliorių** pasirinkite egzempliorių, kurį norite perrašyti, tada – **Kopijuoti**.</span><span class="sxs-lookup"><span data-stu-id="83530-133">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="83530-134">Palaukite, kol lauko **Kopijuoti būseną** reikšmė bus atnaujinta į **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="83530-134">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="83530-135">Perrašytino egzemplioriaus pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="83530-135">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="83530-136">Pažymėkite **„Power Platform“** ir prisijunkite prie „Microsoft Power Platform“ admininstravimo centro.</span><span class="sxs-lookup"><span data-stu-id="83530-136">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="83530-137">„Power Platform“ pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="83530-137">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="83530-138">Pasirinkite kopijuotiną „PowerApps“ aplinką ir pasirinkite **Kopijuoti**.</span><span class="sxs-lookup"><span data-stu-id="83530-138">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="83530-139">Kai kopijavimo procesas baigtas, prisijunkite prie paskirties egzemplioriaus ir įjunkite „Common Data Service“ integravimą.</span><span class="sxs-lookup"><span data-stu-id="83530-139">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="83530-140">Daugiau informacijos ir instrukcijų žr. [„Common Data Service“ integravimo konfigūravimas](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="83530-140">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="83530-141">Duomenų elementai ir būsenos</span><span class="sxs-lookup"><span data-stu-id="83530-141">Data elements and statuses</span></span>

<span data-ttu-id="83530-142">Kai kopijuojate „Human Resources“ egzempliorių, šie duomenų elementai nebus nukopijuoti:</span><span class="sxs-lookup"><span data-stu-id="83530-142">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="83530-143">El. pašto adresai lentelėje **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="83530-143">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="83530-144">Paketinių užduočių retrospektyva lentelėse **BatchJobHistory**, **BatchHistory** ir **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="83530-144">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="83530-145">Paprastųjų pašto siuntų protokolo (SMTP) slaptažodis lentelėje **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="83530-145">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="83530-146">SMTP perdavimo serveris lentelėje **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="83530-146">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="83530-147">Spausdinimo valdymo parametrai lentelėse **PrintMgmtSettings** ir **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="83530-147">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="83530-148">Aplinkai būdingi įrašai lentelėse **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** ir **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="83530-148">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="83530-149">Dokumentų priedai, esantys „DocuValue“ lentelėje.</span><span class="sxs-lookup"><span data-stu-id="83530-149">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="83530-150">Šiuose prieduose yra „Microsoft Office“ šablonų, perrašytų šaltinio aplinkoje</span><span class="sxs-lookup"><span data-stu-id="83530-150">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="83530-151">Ryšio eilutės lentelėje **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="83530-151">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="83530-152">Kai kurie šių elementų nėra nukopijuoti, nes jie yra tik aplinkai būdingi.</span><span class="sxs-lookup"><span data-stu-id="83530-152">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="83530-153">Pavyzdžiai apima įrašus **BatchServerConfig** ir **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="83530-153">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="83530-154">Kiti elementai nėra nukopijuoti dėl palaikymo bilietų apimties.</span><span class="sxs-lookup"><span data-stu-id="83530-154">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="83530-155">Pavyzdžiui, pasikartojančius el. laiškus galima siųsti, nes SMTP vis dar yra įjungtas vartotojo priėmimo testavimo (smėlio dėžės) aplinkoje, netinkamo integravimo pranešimai gali būti siunčiami, nes vis dar yra įgalintos paketinės užduotys, o vartotojai gali būti įjungti prieš administratoriams atliekant valymo veiksmus po atnaujinimo.</span><span class="sxs-lookup"><span data-stu-id="83530-155">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="83530-156">Be to, kai kopijuojate egzempliorių, pasikeičia šios būsenos:</span><span class="sxs-lookup"><span data-stu-id="83530-156">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="83530-157">Visi vartotojai, išskyrus administratorių, nustatyti kaip **Išjungtas**.</span><span class="sxs-lookup"><span data-stu-id="83530-157">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="83530-158">Visos paketinės užduotys, išskyrus kai kurias sistemos užduotis, yra nustatytos kaip **Sulaikyti**.</span><span class="sxs-lookup"><span data-stu-id="83530-158">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="83530-159">Aplinkos administratorius</span><span class="sxs-lookup"><span data-stu-id="83530-159">Environment admin</span></span>

<span data-ttu-id="83530-160">Visi paskirties smėlio dėžės aplinkos vartotojai, įskaitant administratorius, pakeičiami šaltinio aplinkos vartotojais.</span><span class="sxs-lookup"><span data-stu-id="83530-160">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="83530-161">Prieš tai kai nukopijuojate egzempliorių, įsitikinkite, kad šaltinio aplinkoje esate Administratorius.</span><span class="sxs-lookup"><span data-stu-id="83530-161">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="83530-162">Jei nesate, baigę kopijuoti, negalėsite prisijungti prie paskirties smėlio dėžės aplinkos.</span><span class="sxs-lookup"><span data-stu-id="83530-162">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="83530-163">Visi ne administratoriaus teises turintys vartotojai paskirties smėlio dėžės aplinkoje yra išjungti, kad būtų užkirstas kelias nepageidaujamiems prisijungimams smėlio dėžės aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="83530-163">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="83530-164">Jei reikia, administratoriai gali iš naujo įgalinti vartotojus.</span><span class="sxs-lookup"><span data-stu-id="83530-164">Administrators can reenable users if needed.</span></span>
