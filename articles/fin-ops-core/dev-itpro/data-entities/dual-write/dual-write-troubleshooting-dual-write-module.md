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
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172765"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="b36ef-103">Trikčių, susijusių su dvigubo rašymo moduliu „Finance and Operations” programose, šalinimas</span><span class="sxs-lookup"><span data-stu-id="b36ef-103">Troubleshoot issues with the Dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="b36ef-104">Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Common Data Service“ programų trikčių šalinimo informacija.</span><span class="sxs-lookup"><span data-stu-id="b36ef-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="b36ef-105">Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, naudojant **dvigubo rašymo** modulį „Finance and Operations” programose.</span><span class="sxs-lookup"><span data-stu-id="b36ef-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b36ef-106">Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų.</span><span class="sxs-lookup"><span data-stu-id="b36ef-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="b36ef-107">Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.</span><span class="sxs-lookup"><span data-stu-id="b36ef-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="b36ef-108">Negalite įkelti dvigubo rašymo modulio „Finance and Operations” programoje</span><span class="sxs-lookup"><span data-stu-id="b36ef-108">You can't load the Dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="b36ef-109">Jeigu negalite atidaryti **dvigubo rašymo** puslapio darbo srityje **Duomenų valdymas** pasirinkdami plytelę **Dvigubas rašymas**, tikriausiai duomenų integravimo paslauga neveikia.</span><span class="sxs-lookup"><span data-stu-id="b36ef-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="b36ef-110">Norėdami paprašyti iš naujo paleisti duomenų integravimo paslaugą, sukurkite palaikymo bilietą.</span><span class="sxs-lookup"><span data-stu-id="b36ef-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a><span data-ttu-id="b36ef-111">Bandant sukurti naują susiejimą su objektu įvyko klaida</span><span class="sxs-lookup"><span data-stu-id="b36ef-111">Error when you try to create a new entity mapping</span></span>

<span data-ttu-id="b36ef-112">**Reikiami kredencialai, norint išspręsti problemą:** „Azure AD” nuomotojo administratorius</span><span class="sxs-lookup"><span data-stu-id="b36ef-112">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="b36ef-113">Kai bandote konfigūruoti naują dvigubo rašymo objektą, galite gauti tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="b36ef-113">You might receive the following error message when you try to configure a new entity for dual-write:</span></span>

<span data-ttu-id="b36ef-114">*Atsakymo būsenos kodas nenurodo sėkmės: 401 (neautorizuota)*</span><span class="sxs-lookup"><span data-stu-id="b36ef-114">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>

<span data-ttu-id="b36ef-115">Ši klaida įvyksta, nes tik „Azure AD” nuomotojo administratorius gali pridėti naują susiejimą su objektu.</span><span class="sxs-lookup"><span data-stu-id="b36ef-115">This error occurs because only an Azure AD tenant admin can add a new entity mapping.</span></span>

<span data-ttu-id="b36ef-116">Norėdami išspręsti šią problemą, prisijunkite prie „Finance and Operations” programos kaip „Azure AD” nuomotojo administratorius.</span><span class="sxs-lookup"><span data-stu-id="b36ef-116">To fix the issue, sign in to the Finance and Operations app as an Azure AD admin tenant.</span></span> <span data-ttu-id="b36ef-117">Taip pat turite eiti į web.PowerApps.com ir iš naujo patikrinti ryšį.</span><span class="sxs-lookup"><span data-stu-id="b36ef-117">You must also go to web.PowerApps.com and revalidate your connection.</span></span>

## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="b36ef-118">Atidarant dvigubo rašymo vartotojo sąsają įvyko klaida</span><span class="sxs-lookup"><span data-stu-id="b36ef-118">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="b36ef-119">Kai bandote pasiekti dvigubą rašymą iš darbo srities **Duomenų valdymas**, galbūt gausite tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="b36ef-119">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="b36ef-120">*Nepavyko užmegzti ryšio su login.microsoftonline.com*.</span><span class="sxs-lookup"><span data-stu-id="b36ef-120">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="b36ef-121">Norėdami išspręsti šią problemą, prisijunkite, naudodami „Microsoft Edge” langą „InPrivate”, inkognito langą „Chromium” arba inkognito langą „Google Chrome”.</span><span class="sxs-lookup"><span data-stu-id="b36ef-121">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="b36ef-122">Taip pat turite atblokuoti arba išvalyti trečiosios šalies slapukus.</span><span class="sxs-lookup"><span data-stu-id="b36ef-122">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="b36ef-123">Susiejant dvigubo rašymo aplinką arba pridedant naują susiejimą su objektu įvyko klaida</span><span class="sxs-lookup"><span data-stu-id="b36ef-123">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="b36ef-124">**Reikiami kredencialai, norint išspręsti problemą:** „Azure AD” nuomotojo administratorius</span><span class="sxs-lookup"><span data-stu-id="b36ef-124">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="b36ef-125">Kai susiejate arba kuriate schemas, gali įvykti tokia klaida:</span><span class="sxs-lookup"><span data-stu-id="b36ef-125">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="b36ef-126">*Atsakymo būsenos kodas nenurodo sėkmės: 403 (tokenexchange).<br> Seanso ID: \<jūsų seanso id\><br> Šakninės veiklos ID: \<jūsų šakninės veiklos id\>*</span><span class="sxs-lookup"><span data-stu-id="b36ef-126">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="b36ef-127">Ši klaida gali įvykti, jei neturite pakankamai teisių susieti dvigubą rašymą arba kurti schemas.</span><span class="sxs-lookup"><span data-stu-id="b36ef-127">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="b36ef-128">Norėdami sieti aplinkas ir pridėti naujų siejimų su objektu, turite naudoti „Azure AD” nuomotojo administratoriaus paskyrą.</span><span class="sxs-lookup"><span data-stu-id="b36ef-128">You must use an Azure AD tenant admin account to link environments and add new entity mappings.</span></span> <span data-ttu-id="b36ef-129">Tačiau atlikę sąranką galite naudoti ne administratoriaus paskyrą, kad stebėtumėte būseną ir redaguotumėte susiejimus.</span><span class="sxs-lookup"><span data-stu-id="b36ef-129">However, after setup, you can use a non-admin account to monitor status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="b36ef-130">Stabdant susiejimą su objektu įvyko klaida</span><span class="sxs-lookup"><span data-stu-id="b36ef-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="b36ef-131">Kai bandote sustabdyti susiejimus su objektu, galite gauti tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="b36ef-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="b36ef-132">*\[Draudžiama\], \[{"būsena":403,"šaltinis":"","pranešimas":"atpažinimo ženklo keitimo klaida: vartotojui neleidžiama pasiekti ryšį dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], nuotolinis serveris pateikė klaidą: (403) draudžiama.*</span><span class="sxs-lookup"><span data-stu-id="b36ef-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="b36ef-133">Ši klaida įvyksta, kai nėra susietos „Common Data Service” aplinkos.</span><span class="sxs-lookup"><span data-stu-id="b36ef-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="b36ef-134">Norėdami išspręsti šią problemą, sukurkite duomenų integravimo komandai skirtą bilietą.</span><span class="sxs-lookup"><span data-stu-id="b36ef-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="b36ef-135">Pridėkite tinklo sekimą, kad duomenų integravimo komanda galėtų pažymėti vidines schemas kaip **Nevykdomos**.</span><span class="sxs-lookup"><span data-stu-id="b36ef-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>
