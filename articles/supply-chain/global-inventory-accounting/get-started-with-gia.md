---
title: Pradėkite darbą su Visuotine atsargų apskaita
description: Šioje temoje aprašoma, kaip pradėti darbą su Visuotine atsargų apskaita.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 59f9db309312bbbc88b4fa47c12c4c02f09e7c6d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301703"
---
# <a name="get-started-with-global-inventory-accounting"></a><span data-ttu-id="b65b3-103">Pradėkite darbą su Visuotine atsargų apskaita</span><span class="sxs-lookup"><span data-stu-id="b65b3-103">Get started with Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="b65b3-104">Visuotinė atsargų apskaita leidžia jums atlikti kelias atsargų apskaitas Visuotinės atsargų apskaitos didžiosiose knygose, kurias nustatėte.</span><span class="sxs-lookup"><span data-stu-id="b65b3-104">Global Inventory Accounting lets you do multiple inventory accountings in the Global Inventory Accounting ledgers that you've set up.</span></span> <span data-ttu-id="b65b3-105">Turite susieti kiekvieną Visuotinės atsargų apskaitos didžiąją knygą su *konvencija*.</span><span class="sxs-lookup"><span data-stu-id="b65b3-105">You must associate each Global Inventory Accounting ledger with a *convention*.</span></span> <span data-ttu-id="b65b3-106">Konvencija yra toliau pateiktų apskaitos strategijų tipų rinkinys.</span><span class="sxs-lookup"><span data-stu-id="b65b3-106">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="b65b3-107">Savikainos objektas</span><span class="sxs-lookup"><span data-stu-id="b65b3-107">Cost object</span></span>
- <span data-ttu-id="b65b3-108">Įeigos matavimo vieneto pagrindas</span><span class="sxs-lookup"><span data-stu-id="b65b3-108">Input measurement basis</span></span>
- <span data-ttu-id="b65b3-109">Savikainos srauto numanymas</span><span class="sxs-lookup"><span data-stu-id="b65b3-109">Cost flow assumption</span></span>
- <span data-ttu-id="b65b3-110">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="b65b3-110">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="b65b3-111">Netgi įjungę Visuotinę atsargų apskaitą, galite atlikti atsargų apskaitą „Microsoft Dynamics 365 Supply Chain Management” įprastu būdu.</span><span class="sxs-lookup"><span data-stu-id="b65b3-111">Even after you turn on Global Inventory Accounting, you can still do inventory accounting in Microsoft Dynamics 365 Supply Chain Management in the usual way.</span></span>

<span data-ttu-id="b65b3-112">Visuotinė atsargų apskaita yra papildinys.</span><span class="sxs-lookup"><span data-stu-id="b65b3-112">Global Inventory Accounting is an add-in.</span></span> <span data-ttu-id="b65b3-113">Turite ją įdiegti iš „Microsoft Dynamics Lifecycle Services” (LCS), kad jos funkcijos būtų prieinamos.</span><span class="sxs-lookup"><span data-stu-id="b65b3-113">To make its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="b65b3-114">Prieš įjungdami paslaugą gamybos aplinkose galite pasirinkti, kad ji būtų įvertinta testavimo aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="b65b3-114">You can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="b65b3-115">Visuotinė atsargų apskaita šiuo metu nepalaiko visų išlaidų valdymo priemonių, kurios yra įtrauktos į „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="b65b3-115">Global Inventory Accounting doesn't currently support all the cost management features that are built into Supply Chain Management.</span></span> <span data-ttu-id="b65b3-116">Todėl svarbu, kad įvertintumėte, ar funkcijų rinkinys, kurį šiuo metu galima naudoti, atitiks jūsų reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="b65b3-116">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a><span data-ttu-id="b65b3-117">Kaip gauti Visuotinės atsargų apskaitos viešąją peržiūros versija</span><span class="sxs-lookup"><span data-stu-id="b65b3-117">How to get the Global Inventory Accounting public preview</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b65b3-118">Norėdami naudoti Visuotinę atsargų apskaitą, privalote turėti LCS įgalintą didelio užimtumo aplinką (ne „OneBox” aplinką).</span><span class="sxs-lookup"><span data-stu-id="b65b3-118">To use Global Inventory Accounting, you must have an LCS-enabled high-availability environment (not a OneBox environment).</span></span> <span data-ttu-id="b65b3-119">Be to, turite paleisti 10.0.19 ar vėlesnę „Supply Chain Management” versiją.</span><span class="sxs-lookup"><span data-stu-id="b65b3-119">Additionally, you must be running Supply Chain Management version 10.0.19 or later.</span></span>

<span data-ttu-id="b65b3-120">Norėdami užsiregistruoti Visuotinės atsargų apskaitos viešajai peržiūros versijai, atsiųskite savo LCS aplinkos ID el. paštu [Visuotinės atsargų apskaitos komandai](mailto:GlobalInventoryAccounting@service.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="b65b3-120">To sign up for the Global Inventory Accounting public preview, send your LCS environment ID by email to the [Global Inventory Accounting team](mailto:GlobalInventoryAccounting@service.microsoft.com).</span></span> <span data-ttu-id="b65b3-121">Kai būsite patvirtinti programai, komanda išsiųs el. laišką, kuriame bus Visuotinės atsargų apskaitos beta raktas ir jūsų paslaugų galiniai punktai.</span><span class="sxs-lookup"><span data-stu-id="b65b3-121">After you're approved for the program, the team will send you a follow-up email that contains a Global Inventory Accounting beta key and your service endpoints.</span></span> <span data-ttu-id="b65b3-122">Gavę beta raktą, galite [įdiegti papildinį](#install).</span><span class="sxs-lookup"><span data-stu-id="b65b3-122">After you receive the beta key, you can [install the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="b65b3-123">Licencijavimas</span><span class="sxs-lookup"><span data-stu-id="b65b3-123">Licensing</span></span>

<span data-ttu-id="b65b3-124">Visuotinė atsargų apskaita licencijuojama kartu su standartinėmis atsargų apskaitos funkcijomis, kurios pasiekiamos „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="b65b3-124">Global Inventory Accounting is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="b65b3-125">Nereikia pirkti papildomos licencijos, norint naudoti Visuotinę atsargų apskaitą.</span><span class="sxs-lookup"><span data-stu-id="b65b3-125">You don't have to purchase an additional license to use Global Inventory Accounting.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b65b3-126">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="b65b3-126">Prerequisites</span></span>

### <a name="set-up-microsoft-power-platform-integration"></a><span data-ttu-id="b65b3-127">Nustatyti „Microsoft Power Platform“ integravimą</span><span class="sxs-lookup"><span data-stu-id="b65b3-127">Set up Microsoft Power Platform integration</span></span>

<span data-ttu-id="b65b3-128">Kad būtų galima įgalinti papildinio funkcionalumą, turite jį integruoti su „Microsoft Power Platform” atlikdami šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b65b3-128">Before you can enable add-in functionality, you must integrate with Microsoft Power Platform by following these steps.</span></span>

1. <span data-ttu-id="b65b3-129">Atidarykite LCS aplinką, į kurią norite įtraukti paslaugą.</span><span class="sxs-lookup"><span data-stu-id="b65b3-129">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="b65b3-130">Eikite į **Išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="b65b3-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="b65b3-131">**„Power Platform“ integravimas** srityje rinkitės **Nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="b65b3-131">In the **Power Platform Integration** section, select **Setup**.</span></span>
1. <span data-ttu-id="b65b3-132">Dialogo lange **„Power Platform” aplinkos nustatymas** pasirinkite žymės langelį, o tada – **Nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="b65b3-132">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="b65b3-133">Įprastai nustatymas trunka nuo 60 iki 90 minučių.</span><span class="sxs-lookup"><span data-stu-id="b65b3-133">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="b65b3-134">Baigus „Microsoft Power Platform” aplinkos nustatymą, puslapyje rodomas jūsų aplinkos pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="b65b3-134">After setup of the Microsoft Power Platform environment is completed, the page shows the name of your environment.</span></span> <span data-ttu-id="b65b3-135">Be to, **„Power Platform” integravimo** skyriuje rodomas sakinys: „'Power Platform' aplinkos nustatymas yra baigtas.”</span><span class="sxs-lookup"><span data-stu-id="b65b3-135">Additionally, the **Power Platform Integration** section shows the statement, "Power Platform environment setup is complete."</span></span> <span data-ttu-id="b65b3-136">Visuotinei atsargų apskaitai nereikia dvigubo rašymo prašymo.</span><span class="sxs-lookup"><span data-stu-id="b65b3-136">Global Inventory Accounting doesn't require a dual-write application.</span></span>

<span data-ttu-id="b65b3-137">Daugiau informacijos rasite [Nustatymas po aplinkos diegimo](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span><span class="sxs-lookup"><span data-stu-id="b65b3-137">For more information, see [Set up after environment deployment](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span></span>

### <a name="set-up-dataverse"></a><span data-ttu-id="b65b3-138">„Dataverse” nustatymas</span><span class="sxs-lookup"><span data-stu-id="b65b3-138">Set up Dataverse</span></span>

<span data-ttu-id="b65b3-139">Prieš nustatydami „Dataverse”, įtraukite Visuotinės atsargų apskaitos tarnybos principus savo nuomininkui atlikdami šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b65b3-139">Before you set up Dataverse, add the Global Inventory Accounting service principles to your tenant by following these steps.</span></span>

1. <span data-ttu-id="b65b3-140">Įdiekite „Azure AD“ modulį, skirtą „Windows” „PowerShell“ v2, kaip aprašyta skyriuje [„Azure Active Directory“ „PowerShell for Graph“ diegimas](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="b65b3-140">Install Azure AD Module for Windows PowerShell v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
1. <span data-ttu-id="b65b3-141">Paleiskite šią „PowerShell“ komandą.</span><span class="sxs-lookup"><span data-stu-id="b65b3-141">Run the following PowerShell command.</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

<span data-ttu-id="b65b3-142">Tada sukurkite programos vartotojus Visuotinei atsargų apskaitai „Dataverse” platformoje atlikdami šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b65b3-142">Next, create application users for Global Inventory Accounting in Dataverse by following these steps.</span></span>

1. <span data-ttu-id="b65b3-143">Atidarykite savo „Dataverse“ aplinkos URL.</span><span class="sxs-lookup"><span data-stu-id="b65b3-143">Open the URL of your Dataverse environment.</span></span>
1. <span data-ttu-id="b65b3-144">Eikite į **Išplėstiniai nustatymai \> Sistema \> Sauga \> Naudotojai** ir sukurkite programos naudotoją.</span><span class="sxs-lookup"><span data-stu-id="b65b3-144">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="b65b3-145">Naudokite lauką **Peržiūrėti**, kad pakeistumėte puslapio rodinį į *Programos naudotojai*.</span><span class="sxs-lookup"><span data-stu-id="b65b3-145">Use the **View** field to change the page view to *Application users*.</span></span>
1. <span data-ttu-id="b65b3-146">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b65b3-146">Select **New**.</span></span>
1. <span data-ttu-id="b65b3-147">Nustatykite lauką **Programos ID** į *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span><span class="sxs-lookup"><span data-stu-id="b65b3-147">Set the **Application ID** field to *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span></span>
1. <span data-ttu-id="b65b3-148">Pasirinkite **Priskirti vaidmenį**, tada pasirinkite *Sistemos administratorius*.</span><span class="sxs-lookup"><span data-stu-id="b65b3-148">Select **Assign Role**, and then select *System Administrator*.</span></span> <span data-ttu-id="b65b3-149">Jei yra vaidmuo pavadinimu *„Common Data Service“ naudotojas*, pasirinkite ir jį.</span><span class="sxs-lookup"><span data-stu-id="b65b3-149">If there is a role that is named *Common Data Service User*, select it too.</span></span>
1. <span data-ttu-id="b65b3-150">Pakartokite ankstesnius veiksmus, tačiau nustatykite **Programos ID** lauką kaip *„5f58fc56-0202-49a8-ac9e-0946b049718b”*.</span><span class="sxs-lookup"><span data-stu-id="b65b3-150">Repeat the preceding steps, but set the **Application ID** field to *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span></span>

<span data-ttu-id="b65b3-151">Daugiau informacijos žr. skyriuje [Programos naudotojo kūrimas](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="b65b3-151">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

<span data-ttu-id="b65b3-152">Jei numatytoji „Dataverse” diegimo kalba nėra anglų, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b65b3-152">If the default language of your Dataverse installation isn't English, follow these steps.</span></span>

1. <span data-ttu-id="b65b3-153">Eikite į **Išplėstiniai parametrai \> Administravimas \> Kalbos**.</span><span class="sxs-lookup"><span data-stu-id="b65b3-153">Go to **Advanced Setting \> Administration \> Languages**.</span></span>
1. <span data-ttu-id="b65b3-154">Pasirinkite *Anglų* (*LanguageCode (Kalbos kodas)=1033*), o tada – **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="b65b3-154">Select *English* (*LanguageCode=1033*), and then select **Apply**.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="b65b3-155">Papildinio įdiegimas</span><span class="sxs-lookup"><span data-stu-id="b65b3-155">Install the add-in</span></span>

<span data-ttu-id="b65b3-156">Atlikite šiuos veiksmus, kad įdiegtumėte priedą, skirtą Visuotinės atsargų apskaitos naudojimui.</span><span class="sxs-lookup"><span data-stu-id="b65b3-156">Follow these steps to install the add-in so that you can use Global Inventory Accounting.</span></span>

1. <span data-ttu-id="b65b3-157">[Prisiregistruokite](#sign-up) prie Visuotinės atsargų apskaitos viešosios peržiūros versijos.</span><span class="sxs-lookup"><span data-stu-id="b65b3-157">[Sign up](#sign-up) for the Global Inventory Accounting public preview.</span></span>
1. <span data-ttu-id="b65b3-158">Prisijunkite prie [LCS](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="b65b3-158">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="b65b3-159">Eikite į **Peržiūros funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="b65b3-159">Go to **Preview feature management**.</span></span>
1. <span data-ttu-id="b65b3-160">Pasirinkite pliuso ženklą (**+**).</span><span class="sxs-lookup"><span data-stu-id="b65b3-160">Select the plus sign (**+**).</span></span>
1. <span data-ttu-id="b65b3-161">Lauke **Kodas** įveskite jūsų Visuotinės atsargų apskaitos beta raktą.</span><span class="sxs-lookup"><span data-stu-id="b65b3-161">In the **Code** field, enter your add-in beta key for Global Inventory Accounting.</span></span> <span data-ttu-id="b65b3-162">(Turėjote gauti beta raktą el. paštu, kai užsiregistravote.)</span><span class="sxs-lookup"><span data-stu-id="b65b3-162">(You should have received your beta key by email when you signed up.)</span></span>
1. <span data-ttu-id="b65b3-163">Pasirinkite **Atblokuoti**.</span><span class="sxs-lookup"><span data-stu-id="b65b3-163">Select **Unblock**.</span></span>
1. <span data-ttu-id="b65b3-164">Atidarykite LCS aplinką, į kurią norite įtraukti paslaugą.</span><span class="sxs-lookup"><span data-stu-id="b65b3-164">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="b65b3-165">Eikite į **Išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="b65b3-165">Go to **Full details**.</span></span>
1. <span data-ttu-id="b65b3-166">Eikite į **„Power Platform” integravimas** ir pasirinkite **Nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="b65b3-166">Go to **Power Platform Integration**, and select **Setup**.</span></span>
1. <span data-ttu-id="b65b3-167">Dialogo lange **„Power Platform” aplinkos nustatymas** pasirinkite žymės langelį, o tada – **Nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="b65b3-167">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="b65b3-168">Įprastai nustatymas trunka nuo 60 iki 90 minučių.</span><span class="sxs-lookup"><span data-stu-id="b65b3-168">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="b65b3-169">Užbaigę „Microsoft Power Platform” aplinkos nustatymą, „FastTab” **Aplinkos papildiniai** pasirinkite **Diegti naują priedą**.</span><span class="sxs-lookup"><span data-stu-id="b65b3-169">After setup of the Microsoft Power Platform environment is completed, on the **Environment add-ins** FastTab, select **Install a new add-in**.</span></span>
1. <span data-ttu-id="b65b3-170">Pasirinkite **Visuotinė atsargų apskaita**.</span><span class="sxs-lookup"><span data-stu-id="b65b3-170">Select **Global inventory accounting**.</span></span>
1. <span data-ttu-id="b65b3-171">Vadovaukitės diegimo vadovu ir sutikite su sąlygomis ir nuostatomis.</span><span class="sxs-lookup"><span data-stu-id="b65b3-171">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="b65b3-172">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="b65b3-172">Select **Install**.</span></span>
1. <span data-ttu-id="b65b3-173">„FastTab” **Aplinkos papildiniai** turėtumėte matyti, kad Visuotinė atsargų apskaita yra diegiama.</span><span class="sxs-lookup"><span data-stu-id="b65b3-173">On the **Environment add-ins** FastTab, you should see that Global Inventory Accounting is being installed.</span></span> <span data-ttu-id="b65b3-174">Po kelių minučių būsena turėtų pasikeisti iš *Diegiama* į *Įdiegta*.</span><span class="sxs-lookup"><span data-stu-id="b65b3-174">After a few minutes, the status should change from *Installing* to *Installed*.</span></span> <span data-ttu-id="b65b3-175">(Gali reikėti atnaujinti puslapį, kad pamatytumėte šį pakeitimą.) Tada Visuotinė atsargų apskaita bus parengta naudoti.</span><span class="sxs-lookup"><span data-stu-id="b65b3-175">(You might have to refresh the page to see this change.) At that point, Global Inventory Accounting is ready to use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="b65b3-176">Integravimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="b65b3-176">Set up the integration</span></span>

<span data-ttu-id="b65b3-177">Norėdami nustatyti integravimą tarp Visuotinės atsargų apskaitos ir „Supply Chain Management”, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b65b3-177">Follow these steps to set up the integration between Global Inventory Accounting and Supply Chain Management.</span></span>

1. <span data-ttu-id="b65b3-178">Prisijunkite prie „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="b65b3-178">Sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="b65b3-179">Eikite į **Sistemos administravimas \> Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="b65b3-179">Go to **System administration \> Feature Management**.</span></span>
1. <span data-ttu-id="b65b3-180">Pasirinkite **Tikrinti, ar yra naujinimų**.</span><span class="sxs-lookup"><span data-stu-id="b65b3-180">Select **Check for updates**.</span></span>
1. <span data-ttu-id="b65b3-181">Skirtuke **Visi** ieškokite priemonės pavadinimu *Visuotinė atsargų apskaita*.</span><span class="sxs-lookup"><span data-stu-id="b65b3-181">On the **All** tab, search for the feature that is named *Global inventory accounting*.</span></span>
1. <span data-ttu-id="b65b3-182">Pasirinkite **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="b65b3-182">Select **Enable now**.</span></span>
1. <span data-ttu-id="b65b3-183">Eikite į **Visuotinė atsargų apskaita \> Nustatymas \> Visuotinės atsargų apskaitos parametrai \> Integravimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="b65b3-183">Go to **Global inventory accounting \> Setup \> Global inventory accounting parameters \> Integrations parameters**.</span></span>
1. <span data-ttu-id="b65b3-184">Laukuose **Duomenų paslaugos galinis punktas** ir **Visuotinės atsargų apskaitos galinis punktas** įveskite URL iš el. laiško, kurį jums atsiuntė Visuotinės atsargų apskaitos komanda, kai užsiregistravote peržiūros versijai.</span><span class="sxs-lookup"><span data-stu-id="b65b3-184">In the **Data service endpoint** and **Global inventory accounting endpoint** fields, enter the URLs from the email that the Global Inventory Accounting team sent when you signed up for the preview.</span></span>

<span data-ttu-id="b65b3-185">Visuotinė atsargų apskaita dabar yra parengta naudoti.</span><span class="sxs-lookup"><span data-stu-id="b65b3-185">Global Inventory Accounting is now ready to use.</span></span>
