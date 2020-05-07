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
ms.openlocfilehash: d5d9dbce0c74d32107db6bbae033b921e4201693
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275655"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="fe033-103">Bendroji trikčių šalinimo informacija</span><span class="sxs-lookup"><span data-stu-id="fe033-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="fe033-104">Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Common Data Service“ programų bendroji trikčių šalinimo informacija.</span><span class="sxs-lookup"><span data-stu-id="fe033-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe033-105">Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų.</span><span class="sxs-lookup"><span data-stu-id="fe033-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="fe033-106">Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.</span><span class="sxs-lookup"><span data-stu-id="fe033-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="fe033-107">Kai bandote įdiegti dvigubo rašymo paketą naudodami įrankį „Package Deployer“, nerodoma pasiekiamų sprendimų</span><span class="sxs-lookup"><span data-stu-id="fe033-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="fe033-108">Kai kurios įrankio „Package Deployer“ versijos yra nesuderinamos su dvigubo rašymo sprendimo paketu.</span><span class="sxs-lookup"><span data-stu-id="fe033-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="fe033-109">Norėdami sėkmingai įdiegti paketą, įsitikinkite, kad naudojate įrankio „Package Deployer“ [9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) arba naujesnę versiją.</span><span class="sxs-lookup"><span data-stu-id="fe033-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="fe033-110">Įdiegę įrankį „Package Deployer“, įdiekite sprendimo paketą atlikdami šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fe033-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="fe033-111">Atsisiųskite naujausią sprendimo paketo failą iš Yammer.com.</span><span class="sxs-lookup"><span data-stu-id="fe033-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="fe033-112">Atsisiuntus paketo ZIP failą, spustelėkite jį dešiniuoju pelės klavišu ir pasirinkite **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="fe033-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="fe033-113">Pažymėkite žymės langelį **Atblokuoti**, tada pasirinkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="fe033-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="fe033-114">Jei nematote žymės langelio **Atblokuoti**, ZIP failas jau yra atblokuotas ir galite praleisti šį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="fe033-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![Ypatybių dialogo langas](media/unblock_option.png)

2. <span data-ttu-id="fe033-116">Išskleiskite paketo ZIP failą ir nukopijuokite visus failus, esančius aplanke **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438**.</span><span class="sxs-lookup"><span data-stu-id="fe033-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Aplanko „Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438” turinys](media/extract_package.png)

3. <span data-ttu-id="fe033-118">Įklijuokite visus nukopijuotus failus į „Package Deployer” įrankio aplanką **Įrankiai**.</span><span class="sxs-lookup"><span data-stu-id="fe033-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="fe033-119">Norėdami pasirinkti „Common Data Service” aplinką ir įdiegti sprendimus, vykdykite **PackageDeployer.exe**.</span><span class="sxs-lookup"><span data-stu-id="fe033-119">Run **PackageDeployer.exe** to select the Common Data Service environment and install the solutions.</span></span>

    ![Aplanko „Įrankiai” turinys](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a><span data-ttu-id="fe033-121">Įgalinkite ir peržiūrėkite priedo sekimo žurnalą „Common Data Service”, kad peržiūrėtumėte klaidos informaciją</span><span class="sxs-lookup"><span data-stu-id="fe033-121">Enable and view the plug-in trace log in Common Data Service to view error details</span></span>

<span data-ttu-id="fe033-122">**Reikiamas vaidmuo, norint įjungti sekimo žurnalą ir peržiūrėti klaidas:** sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="fe033-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="fe033-123">Norėdami įjungti sekimo žurnalą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fe033-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="fe033-124">Prisijunkite prie „Finance and Operations” programos, atidarykite puslapį **Parametrai**, tada dalyje **Sistema** pasirinkite **Administravimas**.</span><span class="sxs-lookup"><span data-stu-id="fe033-124">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="fe033-125">Puslapyje **Administravimas** pasirinkite **Sistemos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="fe033-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="fe033-126">Skirtuko **Tinkinimas** lauke **Priedo ir pasirinktinės darbo eigos veiklos sekimas** pasirinkite **Viskas**, kad įgalintumėte priedo sekimo žurnalą.</span><span class="sxs-lookup"><span data-stu-id="fe033-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** field, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="fe033-127">Jei norite registruoti sekimo žurnalus tik tada, kai įvyksta išimtys, vietoje to galite pasirinkti **Išimtis**.</span><span class="sxs-lookup"><span data-stu-id="fe033-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="fe033-128">Norėdami peržiūrėti sekimo žurnalą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fe033-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="fe033-129">Prisijunkite prie „Finance and Operations” programos, atidarykite puslapį **Parametrai**, tada dalyje **Tinkinimas** pasirinkite **Priedo sekimo žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="fe033-129">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="fe033-130">Raskite sekimo žurnalus, kuriuose laukas **Tipo pavadinimas** nustatytas kaip **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span><span class="sxs-lookup"><span data-stu-id="fe033-130">Find the trace logs where the **Type Name** field is set to **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span></span>
3. <span data-ttu-id="fe033-131">Dukart spustelėkite elementą, kad peržiūrėtumėte visą žurnalą, tada „FastTab” **Vykdymas** peržiūrėkite tekstą **Pranešimų blokas**.</span><span class="sxs-lookup"><span data-stu-id="fe033-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="fe033-132">Norėdami šalinti tiesioginio sinchronizavimo triktis „Finance and Operations” programose, įgalinkite derinimo režimą</span><span class="sxs-lookup"><span data-stu-id="fe033-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="fe033-133">**Reikiamas vaidmuo, norint peržiūrėti klaidas:** sistemos administratoriaus dvigubos rašymo klaidos, sukurtos „Common Data Service”, gali atsirasti „Finance and Operations” programoje.</span><span class="sxs-lookup"><span data-stu-id="fe033-133">**Required role to view the errors:** System admin Dual-write errors that originate in Common Data Service can appear in the Finance and Operations app.</span></span> <span data-ttu-id="fe033-134">Kai kuriais atvejais visas klaidos pranešimo tekstas nepasiekiamas, nes pranešimas yra per ilgas arba jame yra asmens identifikavimo informacijos (PII).</span><span class="sxs-lookup"><span data-stu-id="fe033-134">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="fe033-135">Galite įjungti daugiažodį klaidų registravimą atlikdami šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fe033-135">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="fe033-136">Visų „Finance and Operations” programų projektų konfigūracijų objekte **DualWriteProjectConfiguration** yra ypatybė **IsDebugMode**.</span><span class="sxs-lookup"><span data-stu-id="fe033-136">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** entity.</span></span> <span data-ttu-id="fe033-137">Atidarykite objektą **DualWriteProjectConfiguration** naudodami „Excel“ papildinį.</span><span class="sxs-lookup"><span data-stu-id="fe033-137">Open the **DualWriteProjectConfiguration** entity by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="fe033-138">Galite lengvai atidaryti objektą, „Excel” papildinyje įjungdami režimą **Dizainas** ir į darbalapį įtraukdami **DualWriteProjectConfigurationEntity**.</span><span class="sxs-lookup"><span data-stu-id="fe033-138">An easy way to open the entity is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="fe033-139">Daugiau informacijos žr. [Objektų duomenų atidarymas programoje „Excel“ ir jų atnaujinimas naudojant „Excel“ papildinį](../../office-integration/use-excel-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="fe033-139">For more information, see [Open entity data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="fe033-140">Nustatykite projekto ypatybę **IsDebugMode** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="fe033-140">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="fe033-141">Vykdyti scenarijų, kuris generuoja klaidas.</span><span class="sxs-lookup"><span data-stu-id="fe033-141">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="fe033-142">Daugiažodžiai žurnalai pasiekiami lentelėje „DualWriteErrorLog”.</span><span class="sxs-lookup"><span data-stu-id="fe033-142">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="fe033-143">Norėdami peržiūrėti duomenis lentelės naršyklėje, naudokite šį URL (atitinkamai pakeiskite **XXX**):</span><span class="sxs-lookup"><span data-stu-id="fe033-143">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="fe033-144">Patikrinkite sinchronizavimo klaidas „Finance and Operations” programos virtualiojoje mašinoje</span><span class="sxs-lookup"><span data-stu-id="fe033-144">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="fe033-145">**Reikiamas vaidmuo, norint peržiūrėti klaidas:** sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="fe033-145">**Required role to view the errors:** System administrator</span></span>

1. <span data-ttu-id="fe033-146">Prisijunkite prie „Microsoft Dynamics“ portale „Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="fe033-146">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="fe033-147">Atidarykite LCS projektą, kurį pasirinkote dvigubo rašymo testavimui atlikti.</span><span class="sxs-lookup"><span data-stu-id="fe033-147">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="fe033-148">Pasirinkite plytelę **Aplinkos diegimo debesyje įrankis**.</span><span class="sxs-lookup"><span data-stu-id="fe033-148">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="fe033-149">Norėdami prisijungti prie „Finance and Operations” programos virtualiosios mašinos, naudokite nuotolinį darbalaukį.</span><span class="sxs-lookup"><span data-stu-id="fe033-149">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="fe033-150">Naudokite vietinę paskyrą, kurį yra rodoma LCS.</span><span class="sxs-lookup"><span data-stu-id="fe033-150">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="fe033-151">Atidarykite įvykių peržiūros programą.</span><span class="sxs-lookup"><span data-stu-id="fe033-151">Open Event viewer.</span></span>
6. <span data-ttu-id="fe033-152">Pasirinkite **Programų ir paslaugų žurnalai \> „Microsoft“ \> „Dynamics“ \> „AX-DualWriteSync“ \> Veikia**.</span><span class="sxs-lookup"><span data-stu-id="fe033-152">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="fe033-153">Peržiūrėti naujausių klaidų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="fe033-153">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="fe033-154">Atsieti ir susieti kitą „Common Data Service” aplinką iš „Finance and Operations” programos</span><span class="sxs-lookup"><span data-stu-id="fe033-154">Unlink and link another Common Data Service environment from a Finance and Operations app</span></span>

<span data-ttu-id="fe033-155">**Būtinas vaidmuo, norint atsieti aplinką:** „Finance and Operations” programų arba „Common Data Service” sistemos administratorius.</span><span class="sxs-lookup"><span data-stu-id="fe033-155">**Required role to unlink the environment:** System administrator for either Finance and Operations app or Common Data Service.</span></span>

1. <span data-ttu-id="fe033-156">Prisijungimas prie „Finance and Operations” programos.</span><span class="sxs-lookup"><span data-stu-id="fe033-156">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="fe033-157">Eikite į **Darbo sritys \> Duomenų valdymas** ir pasirinkite plytelę **Dvigubas rašymas**.</span><span class="sxs-lookup"><span data-stu-id="fe033-157">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="fe033-158">Pasirinkite visus veikiančius susiejimus, tada pasirinkite **Stabdyti**.</span><span class="sxs-lookup"><span data-stu-id="fe033-158">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="fe033-159">Pasirinkite **Atsieti aplinką**.</span><span class="sxs-lookup"><span data-stu-id="fe033-159">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="fe033-160">Kad patvirtintumėte operaciją, pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="fe033-160">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="fe033-161">Dabar galite susieti naują aplinką.</span><span class="sxs-lookup"><span data-stu-id="fe033-161">You can now link a new environment.</span></span>

## <a name="unable-to-view-the-sales-order-line-information-form"></a><span data-ttu-id="fe033-162">Nepavyko peržiūrėti pardavimo užsakymo eilutės informacijos formos</span><span class="sxs-lookup"><span data-stu-id="fe033-162">Unable to view the sales order line Information form</span></span> 

<span data-ttu-id="fe033-163">Sukurę pardavimo užsakymą „Dynamics 365 Sales”, paspaudę **+ Įtraukti produktus** galite būti nukreipti į „Dynamics 365 Project Operations” užsakymo eilutės formą.</span><span class="sxs-lookup"><span data-stu-id="fe033-163">When you create a sales order in Dynamics 365 Sales, clicking on **+ Add products** might redirect you to the Dynamics 365 Project Operations order line form.</span></span> <span data-ttu-id="fe033-164">Nėra būdo toje formoje peržiūrėti pardavimo užsakymo eilutės formą **Informacija**.</span><span class="sxs-lookup"><span data-stu-id="fe033-164">There is no way from that form to view the sales order line **Information** form.</span></span> <span data-ttu-id="fe033-165">Parinktis **Informacija** neatsiranda toliau esančiame išplečiamajame lauke **Nauja užsakymo eilutė**.</span><span class="sxs-lookup"><span data-stu-id="fe033-165">The option for **Information** does not appear in the dropdown below **New Order Line**.</span></span> <span data-ttu-id="fe033-166">Taip nutinka, nes jūsų aplinkoje įdiegta „Project Operations”.</span><span class="sxs-lookup"><span data-stu-id="fe033-166">This happens because Project Operations has been installed in your environment.</span></span>

<span data-ttu-id="fe033-167">Norėdami iš naujo įgalinti formos parinktį **Informacija**, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fe033-167">To re-enable the **Information** form option, follow these steps:</span></span>
1. <span data-ttu-id="fe033-168">Pereikite į objektą **Užsakymo eilutė**.</span><span class="sxs-lookup"><span data-stu-id="fe033-168">Navigate to the **Order Line** entity.</span></span>
2. <span data-ttu-id="fe033-169">Formų mazge raskite formą **Informacija**.</span><span class="sxs-lookup"><span data-stu-id="fe033-169">Find the **Information** form under the forms node.</span></span> 
3. <span data-ttu-id="fe033-170">Pasirinkite formą **Informacija** ir spustelėkite **Įgalinti saugos vaidmenis**.</span><span class="sxs-lookup"><span data-stu-id="fe033-170">Select the **Information** form and click **Enable security roles**.</span></span> 
4. <span data-ttu-id="fe033-171">Pakeiskite saugos parametro parinktį į **Rodyti visiems**.</span><span class="sxs-lookup"><span data-stu-id="fe033-171">Change the security setting to **Display to everyone**.</span></span>
