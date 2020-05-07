---
title: Trikčių, susijusių su dvigubo rašymo moduliu „Finance and Operations” programose, šalinimas
description: Šioje temoje pateikiama trikčių šalinimo informacija, kuri gali padėti išspręsti problemas, susijusias su dvigubo rašymo moduliu „Finance and Operations” programose.
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
ms.openlocfilehash: 853791d5ffc1d92b9fbafa2acc13cd5543c38196
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275538"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="dd746-103">Trikčių, susijusių su dvigubo rašymo moduliu „Finance and Operations” programose, šalinimas</span><span class="sxs-lookup"><span data-stu-id="dd746-103">Troubleshoot issues with the dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dd746-104">Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Common Data Service“ programų trikčių šalinimo informacija.</span><span class="sxs-lookup"><span data-stu-id="dd746-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="dd746-105">Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, naudojant **dvigubo rašymo** modulį „Finance and Operations” programose.</span><span class="sxs-lookup"><span data-stu-id="dd746-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd746-106">Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų.</span><span class="sxs-lookup"><span data-stu-id="dd746-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="dd746-107">Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.</span><span class="sxs-lookup"><span data-stu-id="dd746-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="dd746-108">Negalite įkelti dvigubo rašymo modulio „Finance and Operations” programoje</span><span class="sxs-lookup"><span data-stu-id="dd746-108">You can't load the dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="dd746-109">Jeigu negalite atidaryti **dvigubo rašymo** puslapio darbo srityje **Duomenų valdymas** pasirinkdami plytelę **Dvigubas rašymas**, tikriausiai duomenų integravimo paslauga neveikia.</span><span class="sxs-lookup"><span data-stu-id="dd746-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="dd746-110">Norėdami paprašyti iš naujo paleisti duomenų integravimo paslaugą, sukurkite palaikymo bilietą.</span><span class="sxs-lookup"><span data-stu-id="dd746-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-map"></a><span data-ttu-id="dd746-111">Bandant sukurti naują objekto schemą įvyko klaida</span><span class="sxs-lookup"><span data-stu-id="dd746-111">Error when you try to create a new entity map</span></span>

<span data-ttu-id="dd746-112">**Reikiami kredencialai, norint išspręsti problemą:** tas pats vartotojas, nustatęs dvigubą rašymą.</span><span class="sxs-lookup"><span data-stu-id="dd746-112">**Required credentials to fix the issue:** The same user that setup dual-write.</span></span>

<span data-ttu-id="dd746-113">Kai bandote konfigūruoti naują dvigubo rašymo objektą, galite gauti toliau pateiktą klaidos pranešimą.</span><span class="sxs-lookup"><span data-stu-id="dd746-113">You might receive the following error message when you try to configure a new entity for dual-write.</span></span> <span data-ttu-id="dd746-114">Vienintelis vartotojas, galintis sukurti schemą, yra vartotojas, nustatęs dvigubo rašymo ryšį.</span><span class="sxs-lookup"><span data-stu-id="dd746-114">The only user that can create a map is the user who setup the dual-write connection.</span></span>

<span data-ttu-id="dd746-115">*Atsakymo būsenos kodas nenurodo sėkmės: 401 (neautorizuota)*</span><span class="sxs-lookup"><span data-stu-id="dd746-115">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>


## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="dd746-116">Atidarant dvigubo rašymo vartotojo sąsają įvyko klaida</span><span class="sxs-lookup"><span data-stu-id="dd746-116">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="dd746-117">Kai bandote pasiekti dvigubą rašymą iš darbo srities **Duomenų valdymas**, galbūt gausite tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="dd746-117">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="dd746-118">*Nepavyko užmegzti ryšio su login.microsoftonline.com*.</span><span class="sxs-lookup"><span data-stu-id="dd746-118">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="dd746-119">Norėdami išspręsti šią problemą, prisijunkite, naudodami „Microsoft Edge” langą „InPrivate”, inkognito langą „Chromium” arba inkognito langą „Google Chrome”.</span><span class="sxs-lookup"><span data-stu-id="dd746-119">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="dd746-120">Taip pat turite atblokuoti arba išvalyti trečiosios šalies slapukus.</span><span class="sxs-lookup"><span data-stu-id="dd746-120">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="dd746-121">Susiejant dvigubo rašymo aplinką arba pridedant naują susiejimą su objektu įvyko klaida</span><span class="sxs-lookup"><span data-stu-id="dd746-121">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="dd746-122">**Reikiamas vaidmuo, norint išspręsti problemą:** „Finance and Operations” programų ir „Common Data Service” sistemos administratorius.</span><span class="sxs-lookup"><span data-stu-id="dd746-122">**Required role to fix the issue:** System administrator in both Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="dd746-123">Kai susiejate arba kuriate schemas, gali įvykti tokia klaida:</span><span class="sxs-lookup"><span data-stu-id="dd746-123">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="dd746-124">*Atsakymo būsenos kodas nenurodo sėkmės: 403 (tokenexchange).<br> Seanso ID: \<jūsų seanso id\><br> Šakninės veiklos ID: \<jūsų šakninės veiklos id\>*</span><span class="sxs-lookup"><span data-stu-id="dd746-124">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="dd746-125">Ši klaida gali įvykti, jei neturite pakankamai teisių susieti dvigubą rašymą arba kurti schemas.</span><span class="sxs-lookup"><span data-stu-id="dd746-125">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="dd746-126">Ši klaida taip pat gali įvykti, jei „Common Data Service” aplinka buvo nustatyta iš naujo neatsiejus dvigubo rašymo.</span><span class="sxs-lookup"><span data-stu-id="dd746-126">This error can also occur if the Common Data Service environment was reset without unlinking dual-write.</span></span> <span data-ttu-id="dd746-127">Bet kuris vartotojas, kuriam priskirtas sistemos administratorius vaidmuo „Finance and Operations” programose ir „Common Data Service”, gali susieti aplinkas.</span><span class="sxs-lookup"><span data-stu-id="dd746-127">Any user with system administrator role in both Finance and Operations apps and Common Data Service can link the environments.</span></span> <span data-ttu-id="dd746-128">Tik vartotojas, nustatęs dvigubo rašymo ryšį, gali įtraukti naujų objektų schemų.</span><span class="sxs-lookup"><span data-stu-id="dd746-128">Only the user who setup the dual-write connection can add new entity maps.</span></span> <span data-ttu-id="dd746-129">Atlikus nustatymą, bet kuris vartotojas, kuriam priskirtas sistemos administratorius vaidmuo, gali stebėti būseną ir redaguoti susiejimus.</span><span class="sxs-lookup"><span data-stu-id="dd746-129">After setup, any user with system administrator role can monitor the status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="dd746-130">Stabdant susiejimą su objektu įvyko klaida</span><span class="sxs-lookup"><span data-stu-id="dd746-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="dd746-131">Kai bandote sustabdyti susiejimus su objektu, galite gauti tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="dd746-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="dd746-132">*\[Draudžiama\], \[{"būsena":403,"šaltinis":"","pranešimas":"atpažinimo ženklo keitimo klaida: vartotojui neleidžiama pasiekti ryšį dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], nuotolinis serveris pateikė klaidą: (403) draudžiama.*</span><span class="sxs-lookup"><span data-stu-id="dd746-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="dd746-133">Ši klaida įvyksta, kai nėra susietos „Common Data Service” aplinkos.</span><span class="sxs-lookup"><span data-stu-id="dd746-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="dd746-134">Norėdami išspręsti šią problemą, sukurkite duomenų integravimo komandai skirtą bilietą.</span><span class="sxs-lookup"><span data-stu-id="dd746-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="dd746-135">Pridėkite tinklo sekimą, kad duomenų integravimo komanda galėtų pažymėti vidines schemas kaip **Nevykdomos**.</span><span class="sxs-lookup"><span data-stu-id="dd746-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>

## <a name="error-while-trying-to-start-an-entity-mapping"></a><span data-ttu-id="dd746-136">Bandant pradėti objektų susiejimą įvyko klaida</span><span class="sxs-lookup"><span data-stu-id="dd746-136">Error while trying to start an entity mapping</span></span>

<span data-ttu-id="dd746-137">Bandydami nustatyti susiejimo būseną į **Vykdoma**, galite gauti klaidos pranešimą, panašų į pateiktą toliau:</span><span class="sxs-lookup"><span data-stu-id="dd746-137">You might receive an error like the following when you try to set that state of a mapping to **Running**:</span></span>

<span data-ttu-id="dd746-138">*Nepavyko baigti pradinių duomenų sinchronizavimo. Klaida: dvigubo rašymo triktis – nepavyko registruoti priedo. Nepavyko sukurti dvigubo rašymo peržvalgos metaduomenų. Klaidos objekto nuoroda nenustatyta kaip objekto egzempliorius.*</span><span class="sxs-lookup"><span data-stu-id="dd746-138">*Unable to complete initial data sync. Error: dual-write failure - plugin registration failed: Unable to build dual-write lookup metadata. Error object reference not set to an instance of an object.*</span></span>

<span data-ttu-id="dd746-139">Šios klaidos sprendimas priklauso nuo klaidos priežasties.</span><span class="sxs-lookup"><span data-stu-id="dd746-139">The fix for this error depends on the cause of the error:</span></span>

+ <span data-ttu-id="dd746-140">Jei susiejime yra priklausomieji susiejimai, įsitikinkite, kad įgalinote šio objekto susiejimo priklausomuosius susiejimus.</span><span class="sxs-lookup"><span data-stu-id="dd746-140">If the mapping has dependent mappings, then make sure to enable the dependent mappings of this entity mapping.</span></span>
+ <span data-ttu-id="dd746-141">Gali trūkti susiejimo šaltinio arba paskirties laukų.</span><span class="sxs-lookup"><span data-stu-id="dd746-141">The mapping might be missing source or destination fields.</span></span> <span data-ttu-id="dd746-142">Jei „Finance and Operations” programoje trūksta lauko, atlikite veiksmus, aprašytus skyriuje [Trūkstamų objektų laukų problema schemose](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span><span class="sxs-lookup"><span data-stu-id="dd746-142">If a field in the Finance and Operations app is missing, then follow the steps in the section [Missing entity fields issue on maps](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span></span> <span data-ttu-id="dd746-143">Jei „Common Data Service” trūksta lauko, spustelėkite susiejimo mygtuką **Atnaujinti objektus**, kad laukai būtų automatiškai įvesti į susiejimą.</span><span class="sxs-lookup"><span data-stu-id="dd746-143">If a field in Common Data Service is missing, then click **Refresh entities** button on the mapping so that the fields are automatically populated back into the mapping.</span></span>
