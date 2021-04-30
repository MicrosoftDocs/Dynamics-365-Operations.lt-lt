---
title: DUK apie įgyvendinimo pradžią
description: Šioje temoje pateikiami dažnai užduodami klausimai apie tai, kaip įgyvendinti „Dynamics 365 Human Resources” diegimo projektą.
author: rachel-profitt
ms.date: 10/13/2020
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
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e1b4b336953ef6bd74da009b3bb44fbcf2eab5a8
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892328"
---
# <a name="go-live-faq"></a><span data-ttu-id="c4f97-103">DUK apie įgyvendinimo pradžią</span><span class="sxs-lookup"><span data-stu-id="c4f97-103">Go-live FAQ</span></span> 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c4f97-104">Šioje temoje pateikiami dažnai užduodami klausimai apie tai, kaip įgyvendinti „Dynamics 365 Human Resources” diegimo projektą.</span><span class="sxs-lookup"><span data-stu-id="c4f97-104">This topic lists frequently asked questions about how to go live with a Dynamics 365 Human Resources implementation project.</span></span> 

## <a name="when-can-i-configure-and-request-my-production-environment"></a><span data-ttu-id="c4f97-105">Kada galiu konfigūruoti ir pateikti užklausą dėl mano gamybos aplinkos?</span><span class="sxs-lookup"><span data-stu-id="c4f97-105">When can I configure and request my production environment?</span></span> 

<span data-ttu-id="c4f97-106">Paprastai gamybos aplinka įdiegiama, jei ji atitinka toliau pateiktus kriterijus.</span><span class="sxs-lookup"><span data-stu-id="c4f97-106">Typically, a production environment is deployed after meeting the following criteria:</span></span>

- <span data-ttu-id="c4f97-107">Visi tinkinimai yra užkoduoti ir baigti.</span><span class="sxs-lookup"><span data-stu-id="c4f97-107">All customizations are code-complete.</span></span>
- <span data-ttu-id="c4f97-108">Vartotojo priėmimo testavimas (UAT) baigtas.</span><span class="sxs-lookup"><span data-stu-id="c4f97-108">User acceptance testing (UAT) is complete.</span></span>
- <span data-ttu-id="c4f97-109">Klientas atsijungė nuo sprendimo.</span><span class="sxs-lookup"><span data-stu-id="c4f97-109">The customer has signed off on the solution.</span></span>
- <span data-ttu-id="c4f97-110">Nėra įgyvendinimo blokavimo problemų.</span><span class="sxs-lookup"><span data-stu-id="c4f97-110">There are no blocking issues for go-live.</span></span> 

<span data-ttu-id="c4f97-111">Kai kvalifikuoti klientai yra šiame etape, „Microsoft FastTrack” komanda bendradarbiauja su projekto komanda, kad atliktų įgyvendinimo įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="c4f97-111">When qualified customers are at this stage, the Microsoft FastTrack team will work with the project team to do a go-live assessment.</span></span> 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a><span data-ttu-id="c4f97-112">Kokios būtinosios gamybos aplinkos diegimo sąlygos?</span><span class="sxs-lookup"><span data-stu-id="c4f97-112">What are the prerequisites to deploying a production environment?</span></span> 

<span data-ttu-id="c4f97-113">Norėdami gauti būtinųjų sąlygų sąrašą, žr.  [Rengimasis įgyvendinimo pradžiai](hr-admin-go-live-prepare.md).</span><span class="sxs-lookup"><span data-stu-id="c4f97-113">For a list of the prerequisites, see [Prepare for go-live](hr-admin-go-live-prepare.md).</span></span> 

## <a name="what-is-a-go-live-assessment"></a><span data-ttu-id="c4f97-114">Kas yra įgyvendinimo įvertinimas?</span><span class="sxs-lookup"><span data-stu-id="c4f97-114">What is a go-live assessment?</span></span>  

<span data-ttu-id="c4f97-115">Įgyvendinimo įvertinimas yra  [„Microsoft FastTrack” programos](/dynamics365/fasttrack/) dalis.</span><span class="sxs-lookup"><span data-stu-id="c4f97-115">The go-live assessment is part of the [Microsoft FastTrack program](/dynamics365/fasttrack/).</span></span> <span data-ttu-id="c4f97-116">Šios peržiūros metu sprendimų architektas įvertina, ar įgyvendinimo projektas parengtas sėkmingam pritaikymui ir įgyvendinimui.</span><span class="sxs-lookup"><span data-stu-id="c4f97-116">During this review, a solution architect assesses whether an implementation project is ready for a successful cutover and go-live.</span></span> <span data-ttu-id="c4f97-117">Ši peržiūra yra privaloma kiekvienam įgyvendinimo projektui, kad galima būtų pateikti įgyvendinimo gamybos aplinkoje užklausą.</span><span class="sxs-lookup"><span data-stu-id="c4f97-117">This review is mandatory for every implementation project before you can request to go live in a production environment.</span></span> 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a><span data-ttu-id="c4f97-118">Mūsų smėlio dėžės aplinkos diegiamos centrinės JAV duomenų centre.</span><span class="sxs-lookup"><span data-stu-id="c4f97-118">Our Sandbox environments are deployed in the Central US datacenter.</span></span> <span data-ttu-id="c4f97-119">Norime, kad mūsų gamybos aplinkos būtų diegiamos Vakarų JAV duomenų centre.</span><span class="sxs-lookup"><span data-stu-id="c4f97-119">We want our Production environments to be deployed in the West US datacenter.</span></span> <span data-ttu-id="c4f97-120">Ar mano gamybos konfigūracijoje galiu pasirinkti Vakarų JAV kaip duomenų centrą?</span><span class="sxs-lookup"><span data-stu-id="c4f97-120">Can I select West US as the datacenter in my Production configuration?</span></span> 

<span data-ttu-id="c4f97-121">LCS nedraudžia pasirinkti kito duomenų centro, kai diegiate „Human Resources” aplinką, tačiau primygtinai rekomenduojame nesirinkti kito duomenų centro.</span><span class="sxs-lookup"><span data-stu-id="c4f97-121">LCS doesn't restrict you from selecting a different data center when you deploy a Human Resources environment, but we strongly recommend not selecting a different data center.</span></span>  

<span data-ttu-id="c4f97-122">Jei norite, kad jūsų gamybos aplinka būtų Vakarų JAV duomenų centre, pirmiausia turite iš naujo įdiegti jūsų smėlio dėžės aplinkas į Vakarų JAV duomenų centrą, patikrinti jas ir išsiregistruoti.</span><span class="sxs-lookup"><span data-stu-id="c4f97-122">If you want your Production environment to be in the West US datacenter, you should first redeploy your Sandbox environments to the West US datacenter, test them, and sign off.</span></span> 

<span data-ttu-id="c4f97-123">Informacijos apie teisingo duomenų centro pasirinkimą žr. [Tinklo reikalavimai](../fin-ops-core/fin-ops/get-started/system-requirements.md#network-requirements).</span><span class="sxs-lookup"><span data-stu-id="c4f97-123">For information about selecting the correct datacenter, see [Network requirements](../fin-ops-core/fin-ops/get-started/system-requirements.md#network-requirements).</span></span> 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a><span data-ttu-id="c4f97-124">Kokio lygio prieigą prie „Azure“ išteklių turiu mano „Human Resources” aplinkose?</span><span class="sxs-lookup"><span data-stu-id="c4f97-124">What level of access do I have to the Azure resources for my Human Resources environments?</span></span>  

<span data-ttu-id="c4f97-125">Prieiga prie „Human Resources” aplinkų yra ribota.</span><span class="sxs-lookup"><span data-stu-id="c4f97-125">Access to the Human Resources environments is limited.</span></span> <span data-ttu-id="c4f97-126">Neturite prieigos prie virtualiosios mašinos (VM) arba „Microsoft“ informacinių interneto paslaugų (IIS).</span><span class="sxs-lookup"><span data-stu-id="c4f97-126">You can't access the virtual machine (VM) or Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="c4f97-127">Taip pat neturite prieigos prie duomenų bazės per „Microsoft SQL Server” valdymo studiją.</span><span class="sxs-lookup"><span data-stu-id="c4f97-127">You also can't access the database through Microsoft SQL Server Management Studio.</span></span> 

<span data-ttu-id="c4f97-128">Nors negalite tiesiogiai pasiekti „Azure” išteklių ar „Dynamics 365 Human Resources” aplinkos, yra papildomų funkcijų, kurias galite naudoti norėdami pasiekti jūsų duomenis.</span><span class="sxs-lookup"><span data-stu-id="c4f97-128">Although you can't access your Azure resources or Dynamics 365 Human Resources environment directly, there are additional features you can use to access your data:</span></span>

- <span data-ttu-id="c4f97-129">„Azure SQL” duomenų bazę galite įdiegti savo „Azure” nuomotojuje ir naudoti savo duomenų bazės naudojimo (BYOD) funkciją duomenims sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="c4f97-129">You can deploy an Azure SQL database in your own Azure tenant and use the Bring Your Own Database (BYOD) feature to synchronize data.</span></span> <span data-ttu-id="c4f97-130">Daugiau informacijos žr. [Savo duomenų bazės naudojimas (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span><span class="sxs-lookup"><span data-stu-id="c4f97-130">For more information, see [Bring your own database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span></span>

- <span data-ttu-id="c4f97-131">Galite naudoti „Dataverse” integravimą, norėdami sinchronizuoti pasirinktus objektus su „Dataverse” duomenų baze.</span><span class="sxs-lookup"><span data-stu-id="c4f97-131">You can use Dataverse integration to synchronize select entities into the Dataverse database.</span></span> <span data-ttu-id="c4f97-132">Dėl daugiau informacijos, žr. [„Dataverse“ lentelės](hr-developer-entities.md).</span><span class="sxs-lookup"><span data-stu-id="c4f97-132">For more information, see [Dataverse tables](hr-developer-entities.md).</span></span> 

## <a name="how-often-is-my-production-database-backed-up"></a><span data-ttu-id="c4f97-133">Kaip dažnai sukuriamos mano gamybos duomenų bazės atsarginės kopijos?</span><span class="sxs-lookup"><span data-stu-id="c4f97-133">How often is my production database backed up?</span></span> 

<span data-ttu-id="c4f97-134">Duomenų bazių atsarginės kopijos kuriamos automatiškai toliau pateiktu dažnumu.</span><span class="sxs-lookup"><span data-stu-id="c4f97-134">Databases are protected by automatic backups at the following frequencies:</span></span>

| <span data-ttu-id="c4f97-135">Atsarginės kopijos tipas</span><span class="sxs-lookup"><span data-stu-id="c4f97-135">Type of backup</span></span> | <span data-ttu-id="c4f97-136">Dažnumas</span><span class="sxs-lookup"><span data-stu-id="c4f97-136">Frequency</span></span> |
| --- | --- |
| <span data-ttu-id="c4f97-137">Visos duomenų bazės atsarginė kopija</span><span class="sxs-lookup"><span data-stu-id="c4f97-137">Full database backup</span></span> | <span data-ttu-id="c4f97-138">Savaitinis</span><span class="sxs-lookup"><span data-stu-id="c4f97-138">Weekly</span></span> |
| <span data-ttu-id="c4f97-139">Diferencinės duomenų bazės atsarginė kopija</span><span class="sxs-lookup"><span data-stu-id="c4f97-139">Differential database backup</span></span> | <span data-ttu-id="c4f97-140">Kas 12-24 val.</span><span class="sxs-lookup"><span data-stu-id="c4f97-140">Every 12-24 hours</span></span> |
| <span data-ttu-id="c4f97-141">Operacijų žurnalo atsarginė kopija</span><span class="sxs-lookup"><span data-stu-id="c4f97-141">Transaction log backup</span></span> | <span data-ttu-id="c4f97-142">Kas 5-10 min.</span><span class="sxs-lookup"><span data-stu-id="c4f97-142">Every 5 to 10 minutes</span></span> |

<span data-ttu-id="c4f97-143">„Microsoft“ saugo pakankamai atsarginių kopijų taško laike atkūrimui (PITR) per paskutiniąsias 14 dienų.</span><span class="sxs-lookup"><span data-stu-id="c4f97-143">Microsoft retains sufficient backups to allow for Point in Time Restore (PITR) within the last 14 days.</span></span> 

<span data-ttu-id="c4f97-144">Daugiau informacijos žr.  [Sužinokite apie automatiškai sukurtas SQL duomenų bazės atsargines kopijas](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span><span class="sxs-lookup"><span data-stu-id="c4f97-144">For more information, see [Learn about automatic SQL Database backups](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span></span> 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a><span data-ttu-id="c4f97-145">Ar galiu pateikti užklausą dėl mano gamybos duomenų bazės atsarginės kopijos?</span><span class="sxs-lookup"><span data-stu-id="c4f97-145">Can I request a copy of the backup of my production database?</span></span> 

<span data-ttu-id="c4f97-146">Nr.</span><span class="sxs-lookup"><span data-stu-id="c4f97-146">No.</span></span> <span data-ttu-id="c4f97-147">Tačiau galite pateikti duomenų bazės atnaujinimo paslaugos užklausą, kad nukopijuotumėte jūsų gamybos aplinką į jūsų smėlio dėžės aplinką.</span><span class="sxs-lookup"><span data-stu-id="c4f97-147">You can submit a database refresh service request to copy your Production environment to your Sandbox environment, however.</span></span> <span data-ttu-id="c4f97-148">„Azure SQL” duomenų bazę galite įdiegti savo „Azure” nuomotojuje ir naudoti BYOD funkciją duomenims iš jūsų gamybos aplinkos sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="c4f97-148">You can deploy an Azure SQL database in your own Azure tenant and use the BYOD feature to synchronize data from your Production environment.</span></span> <span data-ttu-id="c4f97-149">Daugiau informacijos žr. [Savo duomenų bazės naudojimas (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span><span class="sxs-lookup"><span data-stu-id="c4f97-149">For more information, see [Bring your own database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span></span> 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a><span data-ttu-id="c4f97-150">Kaip galiu perkelti mano smėlio dėžės aplinką į gamybos aplinką, norėdamas atlikti įgyvendinimą?</span><span class="sxs-lookup"><span data-stu-id="c4f97-150">How do I move my Sandbox environment to Production for go-live?</span></span> 

<span data-ttu-id="c4f97-151">Kadangi kopijavimo funkcija nepasiekiama perkeliant jūsų aplinką iš smėlio dėžės į gamybos aplinką, turite naudoti duomenų paketus, kad perkeltumėte duomenis į jūsų gamybos aplinką.</span><span class="sxs-lookup"><span data-stu-id="c4f97-151">Because a copy feature isn't available to move your environment from a Sandbox to a Production environment, you must use data packages to move data into your Production environment.</span></span>  

<span data-ttu-id="c4f97-152">Viso projekto metu rekomenduojame išlaikyti aiškų objektų, sukonfigūruotų jūsų smėlio dėžėje, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="c4f97-152">We recommend maintaining a clear list of entities configured in your Sandbox throughout the project.</span></span> <span data-ttu-id="c4f97-153">Tada patikrinkite visų duomenų paketų, kurių reikia įgyvendinimui, pritaikymą ir perkėlimą.</span><span class="sxs-lookup"><span data-stu-id="c4f97-153">Then test the process of cutover and migration of any data packages needed for your go-live.</span></span> <span data-ttu-id="c4f97-154">Kai esate pasiruošę įgyvendinimui, turite rankiniu būdu perkelti visus duomenų paketus į gamybos aplinką.</span><span class="sxs-lookup"><span data-stu-id="c4f97-154">You must manually move any data packages into the Production environment when you are ready to go live.</span></span> 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a><span data-ttu-id="c4f97-155">Ką daryti, jei mano gamybos aplinka neveikia?</span><span class="sxs-lookup"><span data-stu-id="c4f97-155">What should I do if my Production environment is down?</span></span> 

<span data-ttu-id="c4f97-156">Norėdami pranešti apie gamybos sutrikimus, vykdykite procesą, aprašytą  [Pranešimas apie gamybos sutrikimus](../fin-ops-core/dev-itpro/lifecycle-services/report-production-outage.md).</span><span class="sxs-lookup"><span data-stu-id="c4f97-156">To report a Production outage, follow the process described in [Report a production outage](../fin-ops-core/dev-itpro/lifecycle-services/report-production-outage.md).</span></span> 

 ## <a name="see-also"></a><span data-ttu-id="c4f97-157">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="c4f97-157">See also</span></span>

 [<span data-ttu-id="c4f97-158">Rengimasis įgyvendinimo pradžiai</span><span class="sxs-lookup"><span data-stu-id="c4f97-158">Prepare for go-live</span></span>](hr-admin-go-live-prepare.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]