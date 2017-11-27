---
title: "Finansinių ataskaitų duomenų srities atstatymas atkūrus duomenų bazę"
description: "Šioje temoje paaiškinama, kaip galima atstatyti finansinių ataskaitų duomenų sritį atkūrus „Microsoft Dynamics 365 for Finance and Operations“ duomenų bazę."
author: ShylaThompson
manager: AnnBe
ms.date: 08/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6e3f78fb2f6528449d2a411225cd0e14ca33443e
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="0ec11-103">Finansinių ataskaitų duomenų srities atstatymas atkūrus duomenų bazę</span><span class="sxs-lookup"><span data-stu-id="0ec11-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0ec11-104">Šioje temoje paaiškinama, kaip galima atstatyti finansinių ataskaitų duomenų sritį atkūrus „Microsoft Dynamics 365 for Finance and Operations“ duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="0ec11-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="0ec11-105">Jei atkuriate „Finance and Operations“ duomenų bazę iš atsarginės kopijos arba duomenų bazės iš kitos aplinkos, atlikite temoje nurodytus veiksmus, kad užtikrintumėte tinkamą finansinių ataskaitų nustatymo naudojimą atkurtoje „Finance and Operations“ duomenų bazėje.</span><span class="sxs-lookup"><span data-stu-id="0ec11-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
> [!Note] 
> <span data-ttu-id="0ec11-106">Šio proceso veiksmai palaikomi naudojant „Dynamics 365 for Operation“ 2016 m. gegužės mėn. leidimą (programos versija 7.0.1265.23014 ir finansinės ataskaitos versija 7.0.10000.4) ir naujesnius leidimus.</span><span class="sxs-lookup"><span data-stu-id="0ec11-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="0ec11-107">Jeigu naudojate ankstesnį „Finance and Operations“ leidimą, pagalbos kreipkitės į mūsų palaikymo komandą.</span><span class="sxs-lookup"><span data-stu-id="0ec11-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="0ec11-108">Ataskaitų aprašų eksportavimas</span><span class="sxs-lookup"><span data-stu-id="0ec11-108">Export report definitions</span></span>
<span data-ttu-id="0ec11-109">Pirmiausia atlikite toliau nurodytus veiksmus ir eksportuokite ataskaitų dizaino įrankyje esančius ataskaitos dizainus.</span><span class="sxs-lookup"><span data-stu-id="0ec11-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="0ec11-110">Įjungę atskaitos dizaino įrankį eikite į **Įmonė** &gt; **Kūrimo bloko grupės**.</span><span class="sxs-lookup"><span data-stu-id="0ec11-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="0ec11-111">Norėdami eksportuoti, pasirinkite kūrimo blokų grupę ir spustelėkite **Eksportuoti**.</span><span class="sxs-lookup"><span data-stu-id="0ec11-111">Select the building block group to export, and click **Export**.</span></span> 

    > [!Note] 
    > <span data-ttu-id="0ec11-112">Naudojant „Finance and Operations“ palaikoma tik viena kūrimo blokų grupė – **Numatytoji**.</span><span class="sxs-lookup"><span data-stu-id="0ec11-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="0ec11-113">Pasirinkite norimus eksportuoti ataskaitos aprašus:</span><span class="sxs-lookup"><span data-stu-id="0ec11-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="0ec11-114">Norėdami eksportuoti visus ataskaitos aprašus ir susietus kūrimo blokus, spustelėkite **Žymėti viską**.</span><span class="sxs-lookup"><span data-stu-id="0ec11-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="0ec11-115">Norėdami eksportuoti konkrečias ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius, spustelėkite atitinkamą skirtuką ir tada pasirinkite norimus eksportuoti elementus.</span><span class="sxs-lookup"><span data-stu-id="0ec11-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="0ec11-116">Norėdami pasirinkti keletą skirtuko elementų, paspauskite ir laikykite klavišą „Ctrl“. Pažymėjus norimas eksportuoti ataskaitas, pažymimos susietos eilutės, stulpeliai, medžiai ir dimensijų rinkiniai.</span><span class="sxs-lookup"><span data-stu-id="0ec11-116">Press and hold the Ctrl key to select multiple items in a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="0ec11-117">Spustelėkite **Eksportuoti**.</span><span class="sxs-lookup"><span data-stu-id="0ec11-117">Click **Export**.</span></span>
5.  <span data-ttu-id="0ec11-118">Įveskite failo pavadinimą ir pasirinkite saugią vietą, kurioje norite įrašyti eksportuotus ataskaitos aprašus.</span><span class="sxs-lookup"><span data-stu-id="0ec11-118">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="0ec11-119">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="0ec11-119">Click **Save**.</span></span>

<span data-ttu-id="0ec11-120">Failą galima nukopijuoti arba įkelti į saugią vietą, kad būtų galima jį importuoti į kitą aplinką kitu laiku.</span><span class="sxs-lookup"><span data-stu-id="0ec11-120">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="0ec11-121">Informaciją apie tai, kaip naudoti „Microsoft Azure“ saugyklos abonementą, galima rasti [Perkelti duomenis naudojant „AzCopy“ komandų eilučių programą](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="0ec11-121">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="0ec11-122">Pasirašius „Finance and Operations“ sutartį „Microsoft“ nesuteikia saugyklos paskyros.</span><span class="sxs-lookup"><span data-stu-id="0ec11-122">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="0ec11-123">Turite įsigyti saugyklos abonementą arba naudoti saugyklos abonementą iš atskiros „Azure“ prenumeratos.</span><span class="sxs-lookup"><span data-stu-id="0ec11-123">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="0ec11-124">Atkreipkite dėmesį į D disko elgseną „Azure“ virtualiuosiuose įrenginiuose.</span><span class="sxs-lookup"><span data-stu-id="0ec11-124">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="0ec11-125">Nelaikykite čia savo eksportuotų kūrimo blokų grupių visam laikui.</span><span class="sxs-lookup"><span data-stu-id="0ec11-125">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="0ec11-126">Norėdami gauti daugiau informacijos apie laikinus diskus, žr. [„Windows Azure“ virtualiųjų įrenginių laikinųjų diskų supratimas](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="0ec11-126">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="0ec11-127">Tarnybų stabdymas</span><span class="sxs-lookup"><span data-stu-id="0ec11-127">Stop services</span></span>
<span data-ttu-id="0ec11-128">Norėdami prisijungti prie visų aplinkos kompiuterių naudokite nuotolinį darbalaukį, o norėdami sustabdyti toliau nurodytas „Windows“ tarnybas – services.msc.</span><span class="sxs-lookup"><span data-stu-id="0ec11-128">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="0ec11-129">Žiniatinklio tarnybos publikavimo paslauga (visuose AOS kompiuteriuose)</span><span class="sxs-lookup"><span data-stu-id="0ec11-129">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="0ec11-130">„Microsoft Dynamics 365 for Finance and Operations“ paketų valdymo tarnyba (tik neasmeniniuose AOS kompiuteriuose)</span><span class="sxs-lookup"><span data-stu-id="0ec11-130">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="0ec11-131">„Management Reporter 2012“ proceso tarnyba (tik BI kompiuteriuose)</span><span class="sxs-lookup"><span data-stu-id="0ec11-131">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="0ec11-132">Šios tarnybos turi atvirus ryšius su „Finance and Operations“ duomenų baze.</span><span class="sxs-lookup"><span data-stu-id="0ec11-132">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="0ec11-133">Nustatyti iš naujo</span><span class="sxs-lookup"><span data-stu-id="0ec11-133">Reset</span></span>
### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="0ec11-134">Raskite ir atsisiųskite naujausią MinorVersionDataUpgrade.zip paketą</span><span class="sxs-lookup"><span data-stu-id="0ec11-134">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="0ec11-135">Raskite naujausią MinorVersionDataUpgrade.zip paketą atsižvelgdami į nurodymus, pateiktus [Naujausių duomenų naujinimo diegimo paketų atsisiuntimas](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span><span class="sxs-lookup"><span data-stu-id="0ec11-135">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span></span> <span data-ttu-id="0ec11-136">Nurodymuose paaiškinama, kaip rasti ir atsisiųsti tinkamą duomenų atnaujinimo pakuotės versiją.</span><span class="sxs-lookup"><span data-stu-id="0ec11-136">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="0ec11-137">Naujinant nėra būtina atsisiųsti MinorVersionDataUpgrade.zip paketo.</span><span class="sxs-lookup"><span data-stu-id="0ec11-137">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="0ec11-138">Būtina atlikti veiksmus nurodytus skyriuje „Naujausių duomenų naujinimo diegimo paketų atsisiuntimas“ neatliekant jokių kitų straipsnyje nurodytų veiksmų, kad gautumėte MinorVersionDataUpgrade.zip paketo kopiją.</span><span class="sxs-lookup"><span data-stu-id="0ec11-138">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="0ec11-139">Scenarijų vykdymas pagal „Finance and Operations“ duomenų bazę</span><span class="sxs-lookup"><span data-stu-id="0ec11-139">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="0ec11-140">Toliau nurodytus scenarijus vykdykite pagal „Finance and Operations“ duomenų bazę (ne pagal finansinių ataskaitų duomenų bazę).</span><span class="sxs-lookup"><span data-stu-id="0ec11-140">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="0ec11-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="0ec11-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="0ec11-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="0ec11-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="0ec11-143">Naudojant šiuos scenarijus užtikrinama, kad naudojami tinkami vartotojų, vaidmenų ir keitimų sekimo paametrai.</span><span class="sxs-lookup"><span data-stu-id="0ec11-143">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="0ec11-144">„PowerShell“ komandos vykdymas norint iš naujo nustatyti duomenų bazę</span><span class="sxs-lookup"><span data-stu-id="0ec11-144">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="0ec11-145">AOS kompiuteryje naudodami „PowerShell“ administratoriaus teisėmis vykdykite toliau nurodytas komandas, kad iš naujo nustatytumėte „Finance and Operations“ ir finansinių ataskaitų integravimą.</span><span class="sxs-lookup"><span data-stu-id="0ec11-145">On the AOS computer, execute the following commands in PowerShell as an Administrator to reset the integration between Finance and Operations and financial reporting:</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail “<my reason for resetting>”

```
> [!NOTE]
> <span data-ttu-id="0ec11-146">Įvykdžius komandas jūsų bus paprašyta įvesti „Y“, kad patvirtintumėte.</span><span class="sxs-lookup"><span data-stu-id="0ec11-146">After executing the commands, you will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="0ec11-147">Parametrų paaiškinimas:</span><span class="sxs-lookup"><span data-stu-id="0ec11-147">Explanation of parameters:</span></span>

-   <span data-ttu-id="0ec11-148">Tinkamos dalies -Priežastis reikšmės yra šios: SERVICING, BADDATA, OTHER.</span><span class="sxs-lookup"><span data-stu-id="0ec11-148">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="0ec11-149">Parametras -ReasonDetail yra laisvos formos.</span><span class="sxs-lookup"><span data-stu-id="0ec11-149">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="0ec11-150">Priežastis ir „reasonDetail“ bus įrašyti atliekant telemetriją / aplinkos stebėjimą.</span><span class="sxs-lookup"><span data-stu-id="0ec11-150">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="0ec11-151">Tarnybų paleidimas</span><span class="sxs-lookup"><span data-stu-id="0ec11-151">Start services</span></span>
<span data-ttu-id="0ec11-152">Naudokite services.msc norėdami iš naujo paleisti pirmiau sustabdytas tarnybas:</span><span class="sxs-lookup"><span data-stu-id="0ec11-152">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="0ec11-153">Žiniatinklio tarnybos publikavimo paslauga (visuose AOS kompiuteriuose)</span><span class="sxs-lookup"><span data-stu-id="0ec11-153">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="0ec11-154">„Microsoft Dynamics 365 for Finance and Operations“ paketų valdymo tarnyba (tik neasmeniniuose AOS kompiuteriuose)</span><span class="sxs-lookup"><span data-stu-id="0ec11-154">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="0ec11-155">„Management Reporter 2012“ proceso tarnyba (tik BI kompiuteriuose)</span><span class="sxs-lookup"><span data-stu-id="0ec11-155">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="0ec11-156">Ataskaitų aprašų importavimas</span><span class="sxs-lookup"><span data-stu-id="0ec11-156">Import report definitions</span></span>
<span data-ttu-id="0ec11-157">Importuokite savo ataskaitos dizainus iš ataskaitų dizaino įrankio naudodami eksportuojant sukurtą failą.</span><span class="sxs-lookup"><span data-stu-id="0ec11-157">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="0ec11-158">Įjungę atskaitos dizaino įrankį eikite į **Įmonė** &gt; **Kūrimo bloko grupės**.</span><span class="sxs-lookup"><span data-stu-id="0ec11-158">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="0ec11-159">Norėdami eksportuoti, pasirinkite kūrimo blokų grupę ir spustelėkite **Eksportuoti**.</span><span class="sxs-lookup"><span data-stu-id="0ec11-159">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="0ec11-160">Naudojant „Finance and Operations“ palaikoma tik viena kūrimo blokų grupė – **Numatytoji**.</span><span class="sxs-lookup"><span data-stu-id="0ec11-160">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="0ec11-161">Pasirinkite kūrimo bloką **Numatytasis** ir spustelėkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="0ec11-161">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="0ec11-162">Pasirinkite failą, kuriame yra eksportuoti ataskaitos aprašai, ir spustelėkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="0ec11-162">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="0ec11-163">Dialogo lange Importuoti pasirinkite norimus importuoti ataskaitos aprašus.</span><span class="sxs-lookup"><span data-stu-id="0ec11-163">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="0ec11-164">Norėdami importuoti visus ataskaitos aprašus ir palaikomus kūrimo blokus, spustelėkite **Žymėti viską**.</span><span class="sxs-lookup"><span data-stu-id="0ec11-164">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="0ec11-165">Norėdami importuoti konkrečias ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius, pasirinkite norimas importuoti ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius.</span><span class="sxs-lookup"><span data-stu-id="0ec11-165">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="0ec11-166">Spustelėkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="0ec11-166">Click **Import**.</span></span>





