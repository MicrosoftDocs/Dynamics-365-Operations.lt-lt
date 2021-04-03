---
title: „Finance and Operations“ programų plėtočių problemų sprendimas
description: Šioje temoje pateikiama trikčių šalinimo informacija, kuri gali padėti išspręsti problemas, susijusias su „Finance and Operations” programų naujinimais.
author: RamaKrishnamoorthy
manager: AnnBe
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
ms.openlocfilehash: ae54ffc9f7a97793dfaddc29f5aae66e5b06c931
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561207"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="1cbe6-103">„Finance and Operations“ programų plėtočių problemų sprendimas</span><span class="sxs-lookup"><span data-stu-id="1cbe6-103">Troubleshoot issues from upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="1cbe6-104">Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Dataverse“ programų trikčių šalinimo informacija.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="1cbe6-105">Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, susijusias su „Finance and Operations” programų naujinimais.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1cbe6-106">Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="1cbe6-107">Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="1cbe6-108">Duomenų bazės sinchronizavimo klaidos</span><span class="sxs-lookup"><span data-stu-id="1cbe6-108">Database synchronization errors</span></span>

<span data-ttu-id="1cbe6-109">**Reikiamas vaidmuo, norint spręsti problemą:** sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="1cbe6-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="1cbe6-110">Kai bandote naudoti **„DualWriteProjectConfiguration”** lentelę, kad atnaujintumėte „Finance and Operations” programą į „Platform Update 30“, galite gauti klaidos pranešimą, panašų į šį pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** table to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="1cbe6-111">Norėdami ištaisyti klaidą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="1cbe6-112">Prisijunkite prie „Finance and Operations” programos virtualiosios mašinos.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="1cbe6-113">Atidarykite „Visual Studio” kaip administratorius, taip pat atidarykite programos objektų medį (AOT).</span><span class="sxs-lookup"><span data-stu-id="1cbe6-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="1cbe6-114">Ieškoti **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="1cbe6-115">Programos objektų medyje (AOT) dešiniuoju pelės mygtuku spustelėkite **DualWriteProjectConfiguration** ir pasirinkite **Įtraukti į naują projektą**.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="1cbe6-116">Pasirinkite **Gerai**, kad sukurtumėte naują projektą, kuriame naudojamos numatytosios parinktys.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="1cbe6-117">Sprendimų naršyklėje dešiniuoju pelės klavišu spustelėkite **Projekto ypatybės** ir nustatykite **Kuriant sinchronizuoti duomenų bazę** kaip **Teisinga**.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="1cbe6-118">Sukurkite projektą ir patvirtinkite, kad sėkmingai pavyko sukurti.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="1cbe6-119">**„Dynamics 365”** meniu pasirinkite **Sinchronizuoti duomenų bazę**.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="1cbe6-120">Norėdami sinchronizuoti visą duomenų bazę, pasirinkite **Sinchronizuoti**.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="1cbe6-121">Sėkmingai atlikę visos duomenų bazės sinchronizavimą, iš naujo įvykdykite duomenų bazės sinchronizavimo veiksmą „Microsoft Dynamics Lifecycle Services (LCS)” portale ir, jei taikytina, naudokite neautomatizuoto naujinimo scenarijus, kad galėtumėte tęsti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-table-columns-issue-on-maps"></a><span data-ttu-id="1cbe6-122">Trūksta lentelės stulpelių schemose</span><span class="sxs-lookup"><span data-stu-id="1cbe6-122">Missing table columns issue on maps</span></span>

<span data-ttu-id="1cbe6-123">**Reikiamas vaidmuo, norint spręsti problemą:** sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="1cbe6-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="1cbe6-124">**Dvigubo rašymo** funkcijos puslapyje galite gauti klaidos pranešimų, panašių į toliau pateiktą pavyzdį:</span><span class="sxs-lookup"><span data-stu-id="1cbe6-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="1cbe6-125">*Trūksta šaltinio lauko \<field name\> schemoje.*</span><span class="sxs-lookup"><span data-stu-id="1cbe6-125">*Missing source field \<field name\> in the schema.*</span></span>

![Trūkstamo šaltinio stulpelio klaidos pranešimo pavyzdys](media/error_missing_field.png)

<span data-ttu-id="1cbe6-127">Norėdami išspręsti problemą, pirmiausia atlikite šiuos veiksmus, kad įsitikintumėte, kad stulpeliai yra lentelėje.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-127">To fix the issue, first follow these steps to make sure that the columns are in the table.</span></span>

1. <span data-ttu-id="1cbe6-128">Prisijunkite prie „Finance and Operations” programos VM.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="1cbe6-129">Eikite į **Darbo sritys \> Duomenų valdymas**, pasirinkite plytelę **Sistemos parametrai**, tada skirtuke **Lentelės parametrai** pasirinkite **Atnaujinti lentelių sąrašą** tam, kad atnaujintumėte lenteles.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Table settings** tab, select **Refresh table list** to refresh the tables.</span></span>
3. <span data-ttu-id="1cbe6-130">Eikite į **Darbo sritys \> Duomenų valdymas**, pasirinkite skirtuką **Duomenų lentelės** ir įsitikinkite, kad lentelė yra sąraše.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-130">Go to **Workspaces \> Data management**, select the **Data tables** tab, and make sure that the table is listed.</span></span> <span data-ttu-id="1cbe6-131">Jei lentelės nėra sąraše, prisijunkite prie „Finance and Operations” programos VM ir įsitikinkite, kad lentelė yra pasiekiama.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-131">If the table isn't listed, sign in to the VM for the Finance and Operations app, and make sure the table is available.</span></span>
4. <span data-ttu-id="1cbe6-132">Eikite į „Finance and Operations” programos **dvigubo rašymo puslapį** ir atidarykite puslapį **Susiejimas su lentele**.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-132">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="1cbe6-133">Pasirinkite **Atnaujinti lentelių sąrašą** tam, kad susiejimų su lentele stulpeliai būtų užpildyti automatiškai.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-133">Select **Refresh table list** to automatically fill the columns in the table mappings.</span></span>

<span data-ttu-id="1cbe6-134">Jei problema išlieka, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1cbe6-135">Šie veiksmai padės jums pašalinti lentelę ir vėl ją pridėti.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-135">These steps guide you through the process of deleting a table and then adding it again.</span></span> <span data-ttu-id="1cbe6-136">Norėdami išvengti problemų, tiksliai atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="1cbe6-137">„Finance and Operations” programoje eikite į **Darbo sritys \> Duomenų valdymas** ir pasirinkite plytelę **Duomenų lentelės**.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data tables** tile.</span></span>
2. <span data-ttu-id="1cbe6-138">Raskite lentelę, kuriai trūksta atributo.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-138">Find the table that is missing the attribute.</span></span> <span data-ttu-id="1cbe6-139">Įrankių juostoje spustelėkite **Modifikuoti paskirties vietos susiejimą**.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-139">Click **Modify target mapping** in the toolbar.</span></span>
3. <span data-ttu-id="1cbe6-140">Srityje **Susieti išdėstymą su paskirties vieta** spustelėkite **Generuoti susiejimą**.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-140">On the **Map staging to target** pane, click **Generate mapping**.</span></span>
4. <span data-ttu-id="1cbe6-141">Eikite į „Finance and Operations” programos **dvigubo rašymo puslapį** ir atidarykite puslapį **Susiejimas su lentele**.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-141">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="1cbe6-142">Jei atributas nėra automatiškai užpildomas schemoje, įtraukite jį neautomatiniu būdu spustelėdami mygtuką **Įtraukti atributą**, o tada – **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-142">If the attribute is not auto-populated on the map, add it manually by clicking **Add attribute** button and then clicking **Save**.</span></span> 
6. <span data-ttu-id="1cbe6-143">Pasirinkite schemą ir spustelėkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="1cbe6-143">Select the map and click **Run**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]