---
title: Trikčių šalinimas pradinės sąrankos metu
description: Šioje temoje pateikiama trikčių šalinimo informacija, kuri gali padėti išspręsti problemas, kurios gali kilti pradinės dvigubos rašymo integracijos tarp „Finance and Operations” programų ir „Common Data Service” sąrankos metu.
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
ms.openlocfilehash: 76e104c9ebd7db7ebcbaf214e84be6c4353e8a73
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275446"
---
# <a name="troubleshoot-issues-during-initial-setup"></a><span data-ttu-id="818af-103">Trikčių šalinimas pradinės sąrankos metu</span><span class="sxs-lookup"><span data-stu-id="818af-103">Troubleshoot issues during initial setup</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="818af-104">Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Common Data Service“ programų trikčių šalinimo informacija.</span><span class="sxs-lookup"><span data-stu-id="818af-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="818af-105">Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, kurios gali kilti pradinės dvigubos rašymo integracijos sąrankos metu.</span><span class="sxs-lookup"><span data-stu-id="818af-105">Specifically, it provides information that can help you fix issues that might occur during the initial setup of dual-write integration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="818af-106">Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų.</span><span class="sxs-lookup"><span data-stu-id="818af-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="818af-107">Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.</span><span class="sxs-lookup"><span data-stu-id="818af-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-link-a-finance-and-operations-app-to-common-data-service"></a><span data-ttu-id="818af-108">Negalite susieti „Finance and Operations” programos su „Common Data Service”</span><span class="sxs-lookup"><span data-stu-id="818af-108">You can't link a Finance and Operations app to Common Data Service</span></span>

<span data-ttu-id="818af-109">**Reikiamas vaidmuo, norint nustatyti dvigubo rašymo funkciją:** „Finance and Operations” programų ir „Common Data Service” sistemos administratorius.</span><span class="sxs-lookup"><span data-stu-id="818af-109">**Required role to set up dual-write:** System administrator in Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="818af-110">Klaidos puslapyje **Susiejimo su „Common Data Service” sąranka** dažniausiai atsiranda dėl neužbaigtos sąrankos arba su teisėmis susijusių problemų.</span><span class="sxs-lookup"><span data-stu-id="818af-110">Errors on the **Setup link to Common Data Service** page are usually caused by incomplete setup or permissions issues.</span></span> <span data-ttu-id="818af-111">Įsitikinkite, kad puslapyje **Susiejimo su „Common Data Service” sąranka** atlikta visiška būsenos patikra, kaip parodyta tolesnėje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="818af-111">Make sure that the whole health check passes on the **Setup link to Common Data Service** page, as shown in the following illustration.</span></span> <span data-ttu-id="818af-112">Negalite susieti dvigubo rašymo, neatlikę visiškos būsenos patikros.</span><span class="sxs-lookup"><span data-stu-id="818af-112">You can't link dual-write unless the whole health check passes.</span></span>

![Sėkmingai atlikta būsenos patikra](media/health_check.png)

<span data-ttu-id="818af-114">Jei norite susieti „Finance and Operations” ir „Common Data Service” aplinkas, privalote turėti „Azure AD” nuomotojo administratoriaus kredencialus.</span><span class="sxs-lookup"><span data-stu-id="818af-114">You must have Azure AD tenant admin credentials to link the Finance and Operations and Common Data Service environments.</span></span> <span data-ttu-id="818af-115">Susiejus aplinkas, vartotojai gali prisijungti, naudodami savo paskyros kredencialus, ir atnaujinti esamą objekto schemą.</span><span class="sxs-lookup"><span data-stu-id="818af-115">After you link the environments, users can sign in by using their account credentials and update an existing entity map.</span></span>

## <a name="error-when-you-open-the-link-to-common-data-service-page"></a><span data-ttu-id="818af-116">Atidarant puslapį „Susiejimo su „Common Data Service” sąranka“ įvyko klaida</span><span class="sxs-lookup"><span data-stu-id="818af-116">Error when you open the Link to Common Data Service page</span></span>

<span data-ttu-id="818af-117">**Reikiami kredencialai, norint išspręsti problemą:** „Azure AD” nuomotojo administratorius</span><span class="sxs-lookup"><span data-stu-id="818af-117">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="818af-118">Kai „Finance and Operations” programoje atidarote puslapį „**Susiejimo su „Common Data Service”** sąranka“, galite gauti tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="818af-118">You might receive the following error message when you open the **Link to Common Data Service** page in a Finance and Operations app:</span></span>

<span data-ttu-id="818af-119">*Atsakymo būsenos kodas nenurodo sėkmės: 404 (nerasta).*</span><span class="sxs-lookup"><span data-stu-id="818af-119">*Response status code does not indicate success: 404 (Not Found).*</span></span>

<span data-ttu-id="818af-120">Ši klaida įvyksta, kai sutikimo veiksmas neužbaigtas.</span><span class="sxs-lookup"><span data-stu-id="818af-120">This error occurs when the consent step hasn't been completed.</span></span> <span data-ttu-id="818af-121">Norėdami patikrinti, ar sutikimo veiksmas užbaigtas, prisijunkite prie portal.Azure.com, naudodami „Azure AD” nuomotojo administratoriaus paskyrą, ir patikrinkite, ar trečiosios šalies programa, kurios ID yra **33976c19-1db5-4c02-810e-c243db79efde**, atsiranda „Azure AD” sąraše **„Enterprise“ programos**.</span><span class="sxs-lookup"><span data-stu-id="818af-121">To validate whether the consent step has been completed, sign in to portal.Azure.com by using the Azure AD tenant admin account, and see whether the third-party app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** appears in the Azure AD **Enterprise applications** list.</span></span> <span data-ttu-id="818af-122">Jei neatsiranda, turite suteikti programos sutikimą.</span><span class="sxs-lookup"><span data-stu-id="818af-122">If it doesn't, you must provide app consent.</span></span>

<span data-ttu-id="818af-123">Norėdami suteikti programos sutikimą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="818af-123">To provide app consent, follow these steps.</span></span>

1. <span data-ttu-id="818af-124">Naudodami administratoriaus kredencialus, atidarykite šį URL.</span><span class="sxs-lookup"><span data-stu-id="818af-124">Open the following URL by using your admin credentials.</span></span> <span data-ttu-id="818af-125">Būsite paraginti pateikti sutikimą.</span><span class="sxs-lookup"><span data-stu-id="818af-125">You should be prompted for consent.</span></span>

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. <span data-ttu-id="818af-126">Norėdami nurodyti, kad sutinkate, kad trečiosios šalies programa, kurios ID yra **33976c19-1db5-4c02-810e-c243db79efde** būtų diegiama jūsų nuomotojuje, pasirinkite **Priimti**.</span><span class="sxs-lookup"><span data-stu-id="818af-126">Select **Accept** to indicate that you're giving your consent to install the app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** in your tenant.</span></span>

    > [!TIP]
    > <span data-ttu-id="818af-127">Ši programa reikalauja susieti „Common Data Service” ir „Finance and Operations” programas.</span><span class="sxs-lookup"><span data-stu-id="818af-127">This app is required to link Common Data Service and Finance and Operations apps.</span></span> <span data-ttu-id="818af-128">Jei atliekant šį veiksmą kyla problemų, atidarykite savo naršyklę inkognito režimu („Google Chrome”) arba „InPrivate” režimu („Microsoft Edge”).</span><span class="sxs-lookup"><span data-stu-id="818af-128">If you have trouble with this step, open your browser in incognito mode (in Google Chrome) or InPrivate mode (in Microsoft Edge).</span></span>

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a><span data-ttu-id="818af-129">Patikrinkite, ar susiejimo metu yra tinkamai nustatyti įmonės duomenys ir dvigubo rašymo komandos</span><span class="sxs-lookup"><span data-stu-id="818af-129">Verify that company data and dual-write teams are set up correctly during linking</span></span>

<span data-ttu-id="818af-130">Siekiant užtikrinti, kad dvigubas rašymas veiktų tinkamai, įmonės, kurias pasirenkate konfigūravimo metu, yra kuriamos „Common Data Service” aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="818af-130">To ensure that dual-write works correctly, the companies that you select during configuration are created in the Common Data Service environment.</span></span> <span data-ttu-id="818af-131">Pagal numatytuosius parametrus, šios įmonės yra tik skaitomas, o ypatybė **IsDualWriteEnable** yra nustatyta kaip **Teisinga**.</span><span class="sxs-lookup"><span data-stu-id="818af-131">By default, these companies are read-only, and the **IsDualWriteEnable** property is set to **True**.</span></span> <span data-ttu-id="818af-132">Be to, sukuriami numatytasis verslo struktūros vieneto savininkas ir komanda ir įtraukiamas įmonės pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="818af-132">In addition, the default owning business unit owner and team are created and include the company name.</span></span> <span data-ttu-id="818af-133">Prieš įgalindami schemas, patikrinkite, ar nurodytas numatytasis komandos savininkas.</span><span class="sxs-lookup"><span data-stu-id="818af-133">Before you enable the maps, verify that the default team owner is specified.</span></span> <span data-ttu-id="818af-134">Norėdami rasti objektą **Įmonės (CDM\_įmonė)**, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="818af-134">To find the **Companies (CDM\_Company)** entity, follow these steps.</span></span>

1. <span data-ttu-id="818af-135">Modeliu grįstos „Dynamics 365” programos viršutiniame dešiniajame kampe pasirinkite filtrą.</span><span class="sxs-lookup"><span data-stu-id="818af-135">In the model-driven app in Dynamics 365, select the filter in the upper-right corner.</span></span>
2. <span data-ttu-id="818af-136">Išplečiamajame sąraše pasirinkite **Įmonė**.</span><span class="sxs-lookup"><span data-stu-id="818af-136">In the drop-down list, select **Company**.</span></span>
3. <span data-ttu-id="818af-137">Norėdami pamatyti rezultatus, pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="818af-137">Select **Run** to see the results.</span></span>
4. <span data-ttu-id="818af-138">Pasirinkite įmonę, kuri buvo susieta konfigūruojant dvigubą rašymą.</span><span class="sxs-lookup"><span data-stu-id="818af-138">Select the company that was linked when you configured dual-write.</span></span>
5. <span data-ttu-id="818af-139">Patikrinkite, ar lauke **Numatytoji komanda savininkė** yra reikšmė.</span><span class="sxs-lookup"><span data-stu-id="818af-139">Verify that the **Default owning team** field has a value.</span></span> <span data-ttu-id="818af-140">Šioje iliustracijoje laukas **Numatytoji komanda savininkė** nustatytas kaip **USMF dvigubas rašymas**.</span><span class="sxs-lookup"><span data-stu-id="818af-140">In the following illustration, the **Default owning team** field is set to **USMF Dual Write**.</span></span>

    ![Numatytosios komandos savininkės tikrinimas](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-entities-or-companies-that-can-be-linked-for-dual-write"></a><span data-ttu-id="818af-142">Raskite juridinių subjektų ar įmonių, kurios gali būti susietos naudojant dvigubo rašymo funkciją, skaičiaus limitą</span><span class="sxs-lookup"><span data-stu-id="818af-142">Find the limit on the number of legal entities or companies that can be linked for dual-write</span></span>

<span data-ttu-id="818af-143">Kai bandote įgalinti schemas, galite gauti tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="818af-143">You might receive the following error message when you try to enable maps:</span></span>

<span data-ttu-id="818af-144">*Dvigubo rašymo funkcijos klaida – nepavyko registruoti priedo: \[(nepavyko gauti skaidinio schemos projektui DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Klaida. Viršijamas maksimalus susiejimui leidžiamų skaidinių skaičius DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], įvyko viena ar daugiau klaidų.*</span><span class="sxs-lookup"><span data-stu-id="818af-144">*Dual write failure - Plugin registration failed: \[(Unable to get partition map for project DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Error Exceeds the maximum partitions allowed for mapping DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], One or more errors occurred.*</span></span>

<span data-ttu-id="818af-145">Dabartinis limitas susiejant aplinkas yra maždaug 40 juridinių subjektų.</span><span class="sxs-lookup"><span data-stu-id="818af-145">The current limit when you link the environments is approximately 40 legal entities.</span></span> <span data-ttu-id="818af-146">Ši klaida įvyksta, jei bandote įgalinti schemas, o daugiau nei 40 juridinių subjektų yra susieti su aplinkomis.</span><span class="sxs-lookup"><span data-stu-id="818af-146">This error occurs if you try to enable maps, and more than 40 legal entities are linked between the environments.</span></span>
