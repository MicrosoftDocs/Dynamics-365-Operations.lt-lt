---
title: "Finansinių ataskaitų duomenų srities atstatymas atkūrus duomenų bazę"
description: "Šioje temoje paaiškinama, kaip galima atstatyti finansinių ataskaitų duomenų sritį atkūrus „Microsoft Dynamics 365 for Finance and Operations“ duomenų bazę."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 08a420a776f47119a5dc47f9119545aa448ffdbd
ms.contentlocale: lt-lt
ms.lasthandoff: 08/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="9c7a5-103">Finansinių ataskaitų duomenų srities atstatymas atkūrus duomenų bazę</span><span class="sxs-lookup"><span data-stu-id="9c7a5-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9c7a5-104">Šioje temoje paaiškinama, kaip galima atstatyti finansinių ataskaitų duomenų sritį atkūrus „Microsoft Dynamics 365 for Finance and Operations“ duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="9c7a5-105">Jei atkuriate „Finance and Operations“ duomenų bazę iš atsarginės kopijos arba duomenų bazės iš kitos aplinkos, atlikite temoje nurodytus veiksmus, kad užtikrintumėte tinkamą finansinių ataskaitų nustatymo naudojimą atkurtoje „Finance and Operations“ duomenų bazėje.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
<!--If you have questions about resetting the financial reporting data mart for a reason outside of restoring a Finance and Operations database, refer to the [Resetting the Management Reporter data mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) for more information. -->
> [!Note] 
> <span data-ttu-id="9c7a5-106">Šio proceso veiksmai palaikomi naudojant „Dynamics 365 for Operation“ 2016 m. gegužės mėn. leidimą (programos versija 7.0.1265.23014 ir finansinės ataskaitos versija 7.0.10000.4) ir naujesnius leidimus.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="9c7a5-107">Jeigu naudojate ankstesnį „Finance and Operations“ leidimą, pagalbos kreipkitės į mūsų palaikymo komandą.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="9c7a5-108">Ataskaitų aprašų eksportavimas</span><span class="sxs-lookup"><span data-stu-id="9c7a5-108">Export report definitions</span></span>
<span data-ttu-id="9c7a5-109">Pirmiausia atlikite toliau nurodytus veiksmus ir eksportuokite ataskaitų dizaino įrankyje esančius ataskaitos dizainus.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="9c7a5-110">Įjungę atskaitos dizaino įrankį eikite į **Įmonė** &gt; **Kūrimo bloko grupės**.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="9c7a5-111">Norėdami eksportuoti, pasirinkite kūrimo blokų grupę ir spustelėkite **Eksportuoti**.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-111">Select the building block group to export, and click **Export**.</span></span> 
    > [!Note] 
    > <span data-ttu-id="9c7a5-112">Naudojant „Finance and Operations“ palaikoma tik viena kūrimo blokų grupė – **Numatytoji**.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
3.  <span data-ttu-id="9c7a5-113">Pasirinkite norimus eksportuoti ataskaitos aprašus:</span><span class="sxs-lookup"><span data-stu-id="9c7a5-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="9c7a5-114">Norėdami eksportuoti visus ataskaitos aprašus ir susietus kūrimo blokus, spustelėkite **Žymėti viską**.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="9c7a5-115">Norėdami eksportuoti konkrečias ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius, spustelėkite atitinkamą skirtuką ir tada pasirinkite norimus eksportuoti elementus.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="9c7a5-116">Norėdami skirtuke pasirinkti keletą elementų, paspauskite ir laikykite nuspaudę CTRL klavišą.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-116">Press and hold the Ctrl key to select multiple items in a tab.</span></span> <span data-ttu-id="9c7a5-117">Pažymėjus norimas eksportuoti ataskaitas pažymimos susietos eilutės, stulpeliai, medžiai ir dimensijų rinkiniai.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-117">When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="9c7a5-118">Spustelėkite **Eksportuoti**.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-118">Click **Export**.</span></span>
5.  <span data-ttu-id="9c7a5-119">Įveskite failo pavadinimą ir pasirinkite saugią vietą, kurioje norite įrašyti eksportuotus ataskaitos aprašus.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-119">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="9c7a5-120">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-120">Click **Save**.</span></span>

<span data-ttu-id="9c7a5-121">Failą galima nukopijuoti arba įkelti į saugią vietą, kad būtų galima jį importuoti į kitą aplinką kitu laiku.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-121">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="9c7a5-122">Informaciją apie tai, kaip naudoti „Microsoft Azure“ saugyklos abonementą, galima rasti [Perkelti duomenis naudojant „AzCopy“ komandų eilučių programą](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="9c7a5-122">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="9c7a5-123">Pasirašius „Finance and Operations“ sutartį „Microsoft“ nesuteikia saugyklos paskyros.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-123">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="9c7a5-124">Turite įsigyti saugyklos abonementą arba naudoti saugyklos abonementą iš atskiros „Azure“ prenumeratos.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-124">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="9c7a5-125">Atkreipkite dėmesį į D disko elgseną „Azure“ virtualiuosiuose įrenginiuose.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-125">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="9c7a5-126">Nelaikykite čia savo eksportuotų kūrimo blokų grupių visam laikui.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-126">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="9c7a5-127">Norėdami gauti daugiau informacijos apie laikinus diskus, žr. [„Windows Azure“ virtualiųjų įrenginių laikinųjų diskų supratimas](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="9c7a5-127">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="9c7a5-128">Tarnybų stabdymas</span><span class="sxs-lookup"><span data-stu-id="9c7a5-128">Stop services</span></span>
<span data-ttu-id="9c7a5-129">Norėdami prisijungti prie visų aplinkos kompiuterių naudokite nuotolinį darbalaukį, o norėdami sustabdyti toliau nurodytas „Windows“ tarnybas – services.msc.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-129">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="9c7a5-130">Žiniatinklio tarnybos publikavimo paslauga (visuose AOS kompiuteriuose)</span><span class="sxs-lookup"><span data-stu-id="9c7a5-130">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="9c7a5-131">„Microsoft Dynamics 365 for Finance and Operations“ paketų valdymo tarnyba (tik neasmeniniuose AOS kompiuteriuose)</span><span class="sxs-lookup"><span data-stu-id="9c7a5-131">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="9c7a5-132">„Management Reporter 2012“ proceso tarnyba (tik BI kompiuteriuose)</span><span class="sxs-lookup"><span data-stu-id="9c7a5-132">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="9c7a5-133">Šios tarnybos turi atvirus ryšius su „Finance and Operations“ duomenų baze.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-133">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="9c7a5-134">Nustatyti iš naujo</span><span class="sxs-lookup"><span data-stu-id="9c7a5-134">Reset</span></span>
#### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="9c7a5-135">Raskite ir atsisiųskite naujausią MinorVersionDataUpgrade.zip paketą</span><span class="sxs-lookup"><span data-stu-id="9c7a5-135">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="9c7a5-136">Raskite naujausią MinorVersionDataUpgrade.zip paketą atsižvelgdami į nurodymus, pateiktus [Naujausių duomenų naujinimo diegimo paketų atsisiuntimas](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span><span class="sxs-lookup"><span data-stu-id="9c7a5-136">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> <span data-ttu-id="9c7a5-137">Nurodymuose paaiškinama, kaip rasti ir atsisiųsti tinkamą duomenų atnaujinimo pakuotės versiją.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-137">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="9c7a5-138">Naujinant nėra būtina atsisiųsti MinorVersionDataUpgrade.zip paketo.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-138">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="9c7a5-139">Būtina atlikti veiksmus nurodytus skyriuje „Naujausių duomenų naujinimo diegimo paketų atsisiuntimas“ neatliekant jokių kitų straipsnyje nurodytų veiksmų, kad gautumėte MinorVersionDataUpgrade.zip paketo kopiją.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-139">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

#### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="9c7a5-140">Scenarijų vykdymas pagal „Finance and Operations“ duomenų bazę</span><span class="sxs-lookup"><span data-stu-id="9c7a5-140">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="9c7a5-141">Toliau nurodytus scenarijus vykdykite pagal „Finance and Operations“ duomenų bazę (ne pagal finansinių ataskaitų duomenų bazę).</span><span class="sxs-lookup"><span data-stu-id="9c7a5-141">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="9c7a5-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="9c7a5-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="9c7a5-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="9c7a5-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="9c7a5-144">Naudojant šiuos scenarijus užtikrinama, kad naudojami tinkami vartotojų, vaidmenų ir keitimų sekimo paametrai.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-144">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="9c7a5-145">„PowerShell“ komandos vykdymas norint iš naujo nustatyti duomenų bazę</span><span class="sxs-lookup"><span data-stu-id="9c7a5-145">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="9c7a5-146">Toliau nurodytą komandą vykdykite tiesiogiai AOS kompiuteryje, kad iš naujo nustatytumėte „Finance and Operations“ ir finansinių ataskaitų integravimą.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-146">Execute the following command, directly on the AOS computer, to reset the integration between Finance and Operations and financial reporting:</span></span>

1.  <span data-ttu-id="9c7a5-147">Atidarykite „Windows PowerShell“ kaip administratorius.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-147">Open Windows PowerShell as Administrator.</span></span>
2.  <span data-ttu-id="9c7a5-148">Vykdyti: F:</span><span class="sxs-lookup"><span data-stu-id="9c7a5-148">Execute: F:</span></span>
3.  <span data-ttu-id="9c7a5-149">Vykdyti: cd F:\\MRApplicationService\\MRInstallDirectory</span><span class="sxs-lookup"><span data-stu-id="9c7a5-149">Execute: cd F:\\MRApplicationService\\MRInstallDirectory</span></span>
4.  <span data-ttu-id="9c7a5-150">Vykdyti: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span><span class="sxs-lookup"><span data-stu-id="9c7a5-150">Execute: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span></span>
5.  <span data-ttu-id="9c7a5-151">Vykdyti: Nustatyti iš naujo-DatamartIntegration -Priežastis KITA -ReasonDetail „&lt;mano nustatymo iš naujo priežastis&gt;“</span><span class="sxs-lookup"><span data-stu-id="9c7a5-151">Execute: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”</span></span>
    -   <span data-ttu-id="9c7a5-152">Jūsų bus paprašyta įvesti „Y“, kad patvirtintumėte.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-152">You will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="9c7a5-153">Parametrų paaiškinimas:</span><span class="sxs-lookup"><span data-stu-id="9c7a5-153">Explanation of parameters:</span></span>

-   <span data-ttu-id="9c7a5-154">Tinkamos dalies -Priežastis reikšmės yra šios: SERVICING, BADDATA, OTHER.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-154">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="9c7a5-155">Parametras -ReasonDetail yra laisvos formos.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-155">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="9c7a5-156">Priežastis ir „reasonDetail“ bus įrašyti atliekant telemetriją / aplinkos stebėjimą.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-156">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="9c7a5-157">Tarnybų paleidimas</span><span class="sxs-lookup"><span data-stu-id="9c7a5-157">Start services</span></span>
<span data-ttu-id="9c7a5-158">Naudokite services.msc norėdami iš naujo paleisti pirmiau sustabdytas tarnybas:</span><span class="sxs-lookup"><span data-stu-id="9c7a5-158">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="9c7a5-159">Žiniatinklio tarnybos publikavimo paslauga (visuose AOS kompiuteriuose)</span><span class="sxs-lookup"><span data-stu-id="9c7a5-159">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="9c7a5-160">„Microsoft Dynamics 365 for Finance and Operations“ paketų valdymo tarnyba (tik neasmeniniuose AOS kompiuteriuose)</span><span class="sxs-lookup"><span data-stu-id="9c7a5-160">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="9c7a5-161">„Management Reporter 2012“ proceso tarnyba (tik BI kompiuteriuose)</span><span class="sxs-lookup"><span data-stu-id="9c7a5-161">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="9c7a5-162">Ataskaitų aprašų importavimas</span><span class="sxs-lookup"><span data-stu-id="9c7a5-162">Import report definitions</span></span>
<span data-ttu-id="9c7a5-163">Importuokite savo ataskaitos dizainus iš ataskaitų dizaino įrankio naudodami eksportuojant sukurtą failą.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-163">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="9c7a5-164">Įjungę atskaitos dizaino įrankį eikite į **Įmonė** &gt; **Kūrimo bloko grupės**.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-164">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="9c7a5-165">Norėdami eksportuoti, pasirinkite kūrimo blokų grupę ir spustelėkite **Eksportuoti**.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-165">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="9c7a5-166">Naudojant „Finance and Operations“ palaikoma tik viena kūrimo blokų grupė – **Numatytoji**.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-166">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="9c7a5-167">Pasirinkite kūrimo bloką **Numatytasis** ir spustelėkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-167">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="9c7a5-168">Pasirinkite failą, kuriame yra eksportuoti ataskaitos aprašai, ir spustelėkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-168">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="9c7a5-169">Dialogo lange Importuoti pasirinkite norimus importuoti ataskaitos aprašus.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-169">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="9c7a5-170">Norėdami importuoti visus ataskaitos aprašus ir palaikomus kūrimo blokus, spustelėkite **Žymėti viską**.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-170">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="9c7a5-171">Norėdami importuoti konkrečias ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius, pasirinkite norimas importuoti ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-171">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="9c7a5-172">Spustelėkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="9c7a5-172">Click **Import**.</span></span>





