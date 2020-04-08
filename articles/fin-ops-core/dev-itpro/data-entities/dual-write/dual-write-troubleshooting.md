---
title: Bendroji trikčių šalinimo informacija
description: Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Common Data Service“ programų bendroji trikčių šalinimo informacija.
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
ms.openlocfilehash: f7ee0b5aa4e72614205e129acd986376b33efc70
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172696"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="f36e6-103">Bendroji trikčių šalinimo informacija</span><span class="sxs-lookup"><span data-stu-id="f36e6-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="f36e6-104">Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Common Data Service“ programų bendroji trikčių šalinimo informacija.</span><span class="sxs-lookup"><span data-stu-id="f36e6-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f36e6-105">Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų.</span><span class="sxs-lookup"><span data-stu-id="f36e6-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="f36e6-106">Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.</span><span class="sxs-lookup"><span data-stu-id="f36e6-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="f36e6-107">Kai bandote įdiegti dvigubo rašymo paketą naudodami įrankį „Package Deployer“, nerodoma pasiekiamų sprendimų</span><span class="sxs-lookup"><span data-stu-id="f36e6-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="f36e6-108">Kai kurios įrankio „Package Deployer“ versijos yra nesuderinamos su dvigubo rašymo sprendimo paketu.</span><span class="sxs-lookup"><span data-stu-id="f36e6-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="f36e6-109">Norėdami sėkmingai įdiegti paketą, įsitikinkite, kad naudojate įrankio „Package Deployer“ [9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) arba naujesnę versiją.</span><span class="sxs-lookup"><span data-stu-id="f36e6-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="f36e6-110">Įdiegę įrankį „Package Deployer“, įdiekite sprendimo paketą atlikdami šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f36e6-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="f36e6-111">Atsisiųskite naujausią sprendimo paketo failą iš Yammer.com.</span><span class="sxs-lookup"><span data-stu-id="f36e6-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="f36e6-112">Atsisiuntus paketo ZIP failą, spustelėkite jį dešiniuoju pelės klavišu ir pasirinkite **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="f36e6-113">Pažymėkite žymės langelį **Atblokuoti**, tada pasirinkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="f36e6-114">Jei nematote žymės langelio **Atblokuoti**, ZIP failas jau yra atblokuotas ir galite praleisti šį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="f36e6-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![Ypatybių dialogo langas](media/unblock_option.png)

2. <span data-ttu-id="f36e6-116">Išskleiskite paketo ZIP failą ir nukopijuokite visus failus, esančius aplanke **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Aplanko „Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438” turinys](media/extract_package.png)

3. <span data-ttu-id="f36e6-118">Įklijuokite visus nukopijuotus failus į „Package Deployer” įrankio aplanką **Įrankiai**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="f36e6-119">Norėdami pasirinkti „Common Data Service” aplinką ir įdiegti sprendimus, vykdykite **PackageDeployer.exe**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-119">Run **PackageDeployer.exe** to select the Common Data Service environment and install the solutions.</span></span>

    ![Aplanko „Įrankiai” turinys](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a><span data-ttu-id="f36e6-121">Įgalinkite ir peržiūrėkite priedo sekimo žurnalą „Common Data Service”, kad peržiūrėtumėte klaidos informaciją</span><span class="sxs-lookup"><span data-stu-id="f36e6-121">Enable and view the plug-in trace log in Common Data Service to view error details</span></span>

<span data-ttu-id="f36e6-122">**Reikiamas vaidmuo, norint įjungti sekimo žurnalą ir peržiūrėti klaidas:** sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="f36e6-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="f36e6-123">Norėdami įjungti sekimo žurnalą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f36e6-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="f36e6-124">Prisijunkite prie „Finance and Operations” programos, atidarykite puslapį **Parametrai**, tada dalyje **Sistema** pasirinkite **Administravimas**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-124">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="f36e6-125">Puslapyje **Administravimas** pasirinkite **Sistemos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="f36e6-126">Skirtuko **Tinkinimas** lauke **Priedo ir pasirinktinės darbo eigos veiklos sekimas** pasirinkite **Viskas**, kad įgalintumėte priedo sekimo žurnalą.</span><span class="sxs-lookup"><span data-stu-id="f36e6-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** field, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="f36e6-127">Jei norite registruoti sekimo žurnalus tik tada, kai įvyksta išimtys, vietoje to galite pasirinkti **Išimtis**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="f36e6-128">Norėdami peržiūrėti sekimo žurnalą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f36e6-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="f36e6-129">Prisijunkite prie „Finance and Operations” programos, atidarykite puslapį **Parametrai**, tada dalyje **Tinkinimas** pasirinkite **Priedo sekimo žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-129">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="f36e6-130">Raskite sekimo žurnalus, kuriuose laukas **Tipo pavadinimas** nustatytas kaip **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-130">Find the trace logs where the **Type Name** field is set to **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span></span>
3. <span data-ttu-id="f36e6-131">Dukart spustelėkite elementą, kad peržiūrėtumėte visą žurnalą, tada „FastTab” **Vykdymas** peržiūrėkite tekstą **Pranešimų blokas**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="f36e6-132">Norėdami šalinti tiesioginio sinchronizavimo triktis „Finance and Operations” programose, įgalinkite derinimo režimą</span><span class="sxs-lookup"><span data-stu-id="f36e6-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="f36e6-133">**Reikiamas vaidmuo, norint peržiūrėti klaidas:** sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="f36e6-133">**Required role to view the errors:** System admin</span></span>

<span data-ttu-id="f36e6-134">Dvigubo rašymo funkcijos klaidos, sukurtos „Common Data Service”, gali atsirasti „Finance and Operations” programoje.</span><span class="sxs-lookup"><span data-stu-id="f36e6-134">Dual-write errors that originate in Common Data Service can appear in the Finance and Operations app.</span></span> <span data-ttu-id="f36e6-135">Kai kuriais atvejais visas klaidos pranešimo tekstas nepasiekiamas, nes pranešimas yra per ilgas arba jame yra asmens identifikavimo informacijos (PII).</span><span class="sxs-lookup"><span data-stu-id="f36e6-135">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="f36e6-136">Galite įjungti daugiažodį klaidų registravimą atlikdami šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f36e6-136">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="f36e6-137">Visų „Finance and Operations” programų projektų konfigūracijų objekte **DualWriteProjectConfiguration** yra ypatybė **IsDebugMode**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-137">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** entity.</span></span> <span data-ttu-id="f36e6-138">Atidarykite objektą **DualWriteProjectConfiguration** naudodami „Excel“ papildinį.</span><span class="sxs-lookup"><span data-stu-id="f36e6-138">Open the **DualWriteProjectConfiguration** entity by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="f36e6-139">Galite lengvai atidaryti objektą, „Excel” papildinyje įjungdami režimą **Dizainas** ir į darbalapį įtraukdami **DualWriteProjectConfigurationEntity**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-139">An easy way to open the entity is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="f36e6-140">Daugiau informacijos žr. [Objektų duomenų atidarymas programoje „Excel“ ir jų atnaujinimas naudojant „Excel“ papildinį](../../office-integration/use-excel-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="f36e6-140">For more information, see [Open entity data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="f36e6-141">Nustatykite projekto ypatybę **IsDebugMode** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-141">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="f36e6-142">Vykdyti scenarijų, kuris generuoja klaidas.</span><span class="sxs-lookup"><span data-stu-id="f36e6-142">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="f36e6-143">Daugiažodžiai žurnalai pasiekiami lentelėje „DualWriteErrorLog”.</span><span class="sxs-lookup"><span data-stu-id="f36e6-143">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="f36e6-144">Norėdami peržiūrėti duomenis lentelės naršyklėje, naudokite šį URL (atitinkamai pakeiskite **XXX**):</span><span class="sxs-lookup"><span data-stu-id="f36e6-144">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="f36e6-145">Patikrinkite sinchronizavimo klaidas „Finance and Operations” programos virtualiojoje mašinoje</span><span class="sxs-lookup"><span data-stu-id="f36e6-145">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="f36e6-146">**Reikiamas vaidmuo, norint peržiūrėti klaidas:** sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="f36e6-146">**Required role to view the errors:** System admin</span></span>

1. <span data-ttu-id="f36e6-147">Prisijunkite prie „Microsoft Dynamics“ portale „Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="f36e6-147">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="f36e6-148">Atidarykite LCS projektą, kurį pasirinkote dvigubo rašymo testavimui atlikti.</span><span class="sxs-lookup"><span data-stu-id="f36e6-148">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="f36e6-149">Pasirinkite plytelę **Aplinkos diegimo debesyje įrankis**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-149">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="f36e6-150">Norėdami prisijungti prie „Finance and Operations” programos virtualiosios mašinos, naudokite nuotolinį darbalaukį.</span><span class="sxs-lookup"><span data-stu-id="f36e6-150">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="f36e6-151">Naudokite vietinę paskyrą, kurį yra rodoma LCS.</span><span class="sxs-lookup"><span data-stu-id="f36e6-151">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="f36e6-152">Atidarykite įvykių peržiūros programą.</span><span class="sxs-lookup"><span data-stu-id="f36e6-152">Open Event viewer.</span></span>
6. <span data-ttu-id="f36e6-153">Pasirinkite **Programų ir paslaugų žurnalai \> „Microsoft“ \> „Dynamics“ \> „AX-DualWriteSync“ \> Veikia**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-153">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="f36e6-154">Peržiūrėti naujausių klaidų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="f36e6-154">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="f36e6-155">Atsieti ir susieti kitą „Common Data Service” aplinką iš „Finance and Operations” programos</span><span class="sxs-lookup"><span data-stu-id="f36e6-155">Unlink and link another Common Data Service environment from a Finance and Operations app</span></span>

<span data-ttu-id="f36e6-156">**Reikiami kredencialai, norint atsieti aplinką:** „Azure AD” nuomotojo administratorius</span><span class="sxs-lookup"><span data-stu-id="f36e6-156">**Required credentials to unlink the environment:** Azure AD tenant admin</span></span>

1. <span data-ttu-id="f36e6-157">Prisijungimas prie „Finance and Operations” programos.</span><span class="sxs-lookup"><span data-stu-id="f36e6-157">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="f36e6-158">Eikite į **Darbo sritys \> Duomenų valdymas** ir pasirinkite plytelę **Dvigubas rašymas**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-158">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="f36e6-159">Pasirinkite visus veikiančius susiejimus, tada pasirinkite **Stabdyti**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-159">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="f36e6-160">Pasirinkite **Atsieti aplinką**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-160">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="f36e6-161">Kad patvirtintumėte operaciją, pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-161">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="f36e6-162">Dabar galite susieti naują aplinką.</span><span class="sxs-lookup"><span data-stu-id="f36e6-162">You can now link a new environment.</span></span>
