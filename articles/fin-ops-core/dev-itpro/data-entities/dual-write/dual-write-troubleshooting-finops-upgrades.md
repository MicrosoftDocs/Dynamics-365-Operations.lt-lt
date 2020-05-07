---
title: Trikčių, susijusių su „Finance and Operations” programų naujinimais, šalinimas
description: Šioje temoje pateikiama trikčių šalinimo informacija, kuri gali padėti išspręsti problemas, susijusias su „Finance and Operations” programų naujinimais.
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
ms.openlocfilehash: 53df00de82b101aa02160d865a9c3bbebcfcae15
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275469"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="c270f-103">Trikčių, susijusių su „Finance and Operations” programų naujinimais, šalinimas</span><span class="sxs-lookup"><span data-stu-id="c270f-103">Troubleshoot issues related to upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="c270f-104">Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Common Data Service“ programų trikčių šalinimo informacija.</span><span class="sxs-lookup"><span data-stu-id="c270f-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="c270f-105">Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, susijusias su „Finance and Operations” programų naujinimais.</span><span class="sxs-lookup"><span data-stu-id="c270f-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c270f-106">Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų.</span><span class="sxs-lookup"><span data-stu-id="c270f-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="c270f-107">Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.</span><span class="sxs-lookup"><span data-stu-id="c270f-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="c270f-108">Duomenų bazės sinchronizavimo klaidos</span><span class="sxs-lookup"><span data-stu-id="c270f-108">Database synchronization errors</span></span>

<span data-ttu-id="c270f-109">**Reikiamas vaidmuo, norint spręsti problemą:** sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="c270f-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="c270f-110">Kai bandote naudoti objektą **DualWriteProjectConfiguration**, kad atnaujintumėte „Finance and Operations” programą į „Platform Update 30“, galite gauti klaidos pranešimą, panašų į šį pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="c270f-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** entity to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="c270f-111">Norėdami ištaisyti klaidą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c270f-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="c270f-112">Prisijunkite prie „Finance and Operations” programos virtualiosios mašinos.</span><span class="sxs-lookup"><span data-stu-id="c270f-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="c270f-113">Atidarykite  „Visual Studio” kaip administratorius, taip pat atidarykite programos objektų medį (AOT).</span><span class="sxs-lookup"><span data-stu-id="c270f-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="c270f-114">Ieškoti **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c270f-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="c270f-115">Programos objektų medyje (AOT) dešiniuoju pelės mygtuku spustelėkite **DualWriteProjectConfiguration** ir pasirinkite **Įtraukti į naują projektą**.</span><span class="sxs-lookup"><span data-stu-id="c270f-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="c270f-116">Pasirinkite **Gerai**, kad sukurtumėte naują projektą, kuriame naudojamos numatytosios parinktys.</span><span class="sxs-lookup"><span data-stu-id="c270f-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="c270f-117">Sprendimų naršyklėje dešiniuoju pelės klavišu spustelėkite **Projekto ypatybės** ir nustatykite **Kuriant sinchronizuoti duomenų bazę** kaip **Teisinga**.</span><span class="sxs-lookup"><span data-stu-id="c270f-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="c270f-118">Sukurkite projektą ir patvirtinkite, kad sėkmingai pavyko sukurti.</span><span class="sxs-lookup"><span data-stu-id="c270f-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="c270f-119">**„Dynamics 365”** meniu pasirinkite **Sinchronizuoti duomenų bazę**.</span><span class="sxs-lookup"><span data-stu-id="c270f-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="c270f-120">Norėdami sinchronizuoti visą duomenų bazę, pasirinkite **Sinchronizuoti**.</span><span class="sxs-lookup"><span data-stu-id="c270f-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="c270f-121">Sėkmingai atlikę visos duomenų bazės sinchronizavimą, iš naujo įvykdykite duomenų bazės sinchronizavimo veiksmą „Microsoft Dynamics Lifecycle Services (LCS)” portale ir, jei taikytina, naudokite neautomatizuoto naujinimo scenarijus, kad galėtumėte tęsti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="c270f-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-entity-fields-issue-on-maps"></a><span data-ttu-id="c270f-122">Trūkstamų objektų laukų problema schemose</span><span class="sxs-lookup"><span data-stu-id="c270f-122">Missing entity fields issue on maps</span></span>

<span data-ttu-id="c270f-123">**Reikiamas vaidmuo, norint spręsti problemą:** sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="c270f-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="c270f-124">**Dvigubo rašymo** funkcijos puslapyje galite gauti klaidos pranešimų, panašių į toliau pateiktą pavyzdį:</span><span class="sxs-lookup"><span data-stu-id="c270f-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="c270f-125">*Trūksta šaltinio lauko \<lauko pavadinimas\> schemoje.*</span><span class="sxs-lookup"><span data-stu-id="c270f-125">*Missing source field \<field name\> in the schema.*</span></span>

![Trūkstamo šaltinio lauko klaidos pranešimo pavyzdys](media/error_missing_field.png)

<span data-ttu-id="c270f-127">Norėdami išspręsti problemą, pirmiausia atlikite šiuos veiksmus, kad įsitikintumėte, kad laukai yra objekte.</span><span class="sxs-lookup"><span data-stu-id="c270f-127">To fix the issue, first follow these steps to make sure that the fields are in the entity.</span></span>

1. <span data-ttu-id="c270f-128">Prisijunkite prie „Finance and Operations” programos VM.</span><span class="sxs-lookup"><span data-stu-id="c270f-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="c270f-129">Eikite į **Darbo sritys \> Duomenų valdymas**, pasirinkite plytelę **Sistemos parametrai**, tada skirtuke **Objekto nustatymai** pasirinkite **Atnaujinti objektų sąrašą**, kad atnaujintumėte objektus.</span><span class="sxs-lookup"><span data-stu-id="c270f-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Entity settings** tab, select **Refresh entity list** to refresh the entities.</span></span>
3. <span data-ttu-id="c270f-130">Eikite į **Darbo sritys \> Duomenų valdymas**, pasirinkite skirtuką **Duomenų objektai** ir įsitikinkite, kad objektas yra sąraše.</span><span class="sxs-lookup"><span data-stu-id="c270f-130">Go to **Workspaces \> Data management**, select the **Data entities** tab, and make sure that the entity is listed.</span></span> <span data-ttu-id="c270f-131">Jei objekto nėra sąraše, prisijunkite prie „Finance and Operations” programos VM ir įsitikinkite, kad objektas yra pasiekiamas.</span><span class="sxs-lookup"><span data-stu-id="c270f-131">If the entity isn't listed, sign in to the VM for the Finance and Operations app, and make sure the entity is available.</span></span>
4. <span data-ttu-id="c270f-132">Eikite į „Finance and Operations” programos **dvigubo rašymo puslapį** ir atidarykite puslapį **Susiejimas su objektu**.</span><span class="sxs-lookup"><span data-stu-id="c270f-132">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="c270f-133">Pasirinkite **Atnaujinti objektų sąrašą**, kad susiejimų su objektu laukai būtų užpildyti automatiškai.</span><span class="sxs-lookup"><span data-stu-id="c270f-133">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>

<span data-ttu-id="c270f-134">Jei problema išlieka, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c270f-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c270f-135">Šie veiksmai padės jums pašalinti objektą ir vėl jį pridėti.</span><span class="sxs-lookup"><span data-stu-id="c270f-135">These steps guide you through the process of deleting an entity and then adding it again.</span></span> <span data-ttu-id="c270f-136">Norėdami išvengti problemų, tiksliai atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c270f-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="c270f-137">„Finance and Operations” programoje eikite į **Darbo sritys \> Duomenų valdymas** ir pasirinkite plytelę **Duomenų objektai**.</span><span class="sxs-lookup"><span data-stu-id="c270f-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data entities** tile.</span></span>
2. <span data-ttu-id="c270f-138">Raskite objektą, kuriam trūksta atributo.</span><span class="sxs-lookup"><span data-stu-id="c270f-138">Find the entity that is missing the attribute.</span></span> <span data-ttu-id="c270f-139">Įrankių juostoje spustelėkite **Modifikuoti paskirties vietos susiejimą**.</span><span class="sxs-lookup"><span data-stu-id="c270f-139">Click **Modify target mapping** in the toolbar.</span></span>
3. <span data-ttu-id="c270f-140">Srityje **Susieti išdėstymą su paskirties vieta** spustelėkite **Generuoti susiejimą**.</span><span class="sxs-lookup"><span data-stu-id="c270f-140">On the **Map staging to target** pane, click **Generate mapping**.</span></span>
4. <span data-ttu-id="c270f-141">Eikite į „Finance and Operations” programos **dvigubo rašymo puslapį** ir atidarykite puslapį **Susiejimas su objektu**.</span><span class="sxs-lookup"><span data-stu-id="c270f-141">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="c270f-142">Jei atributas nėra automatiškai užpildomas schemoje, įtraukite jį neautomatiniu būdu spustelėdami mygtuką **Įtraukti atributą**, o tada – **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="c270f-142">If the attribute is not auto-populated on the map, add it manually by clicking **Add attribute** button and then clicking **Save**.</span></span> 
6. <span data-ttu-id="c270f-143">Pasirinkite schemą ir spustelėkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="c270f-143">Select the map and click **Run**.</span></span>
