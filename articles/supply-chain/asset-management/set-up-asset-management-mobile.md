---
title: Turto valdymo mobiliosios darbo srities nustatymas
description: Šioje temoje aprašoma, kaip sukonfigūruoti „Microsoft Dynamics 365 Supply Chain Management” ir „Finance and Operations” („Dynamics 365”) mobiliąją programėlę ir paleisti Turto valdymo mobiliąją darbo sritį, kurią darbuotojai gali naudoti atlikti turto valdymo užduotis.
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: bc170df2fc58ae6b42fbc8834caad0bb7cd16f69
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837782"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a><span data-ttu-id="b9dbc-103">Turto valdymo mobiliosios darbo srities nustatymas</span><span class="sxs-lookup"><span data-stu-id="b9dbc-103">Set up the Asset management mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9dbc-104">Šioje temoje aprašoma, kaip sukonfigūruoti „Microsoft Dynamics 365 Supply Chain Management” ir „Finance and Operations” („Dynamics 365”) mobiliąją programėlę, kad paleistumėte **Turto valdymas** mobiliąją darbo sritį, kurioje darbuotojai gali atlikti turto valdymo užduotis.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-104">This topic describes how to set up Microsoft Dynamics 365 Supply Chain Management and the Finance and Operations (Dynamics 365) mobile app to run an **Asset management** mobile workspace that workers can use to perform asset management tasks.</span></span>

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a><span data-ttu-id="b9dbc-105">Techninės priežiūros darbuotojo vartotojų nustatymas „Supply Chain Management”</span><span class="sxs-lookup"><span data-stu-id="b9dbc-105">Set up maintenance worker users in Supply Chain Management</span></span>

<span data-ttu-id="b9dbc-106">Kiekvienas vartotojas, kuriam reikalinga prieiga prie **Turto valdymas** mobiliosios darbo srities, turi atlikti šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-106">For each user that requires access to the **Asset management** mobile workspace, follow these steps.</span></span>

1. <span data-ttu-id="b9dbc-107">„Supply Chain Management” eikite į **Žmogiškieji ištekliai \> Darbuotojai** ir įsitikinkite, kad egzistuoja pageidautino sukonfigūruoti vartotojo darbuotojo įrašas.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-107">In Supply Chain Management, go to **Human resources \> Workers**, and make sure that a worker record exists for the user that you want to set up.</span></span> <span data-ttu-id="b9dbc-108">Sukurkite būtiną naujo darbuotojo įrašą.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-108">Create a new worker record as required.</span></span>
1. <span data-ttu-id="b9dbc-109">Eikite į **Turto valdymas \> Sąranka \> Darbuotojai \> Darbuotojai** ir įsitikinkite, kad jūsų ankstesniu veiksmu nustatytas (ar sukurtas) darbuotojo įrašas yra susietas su techninės priežiūros darbuotojo įrašu.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-109">Go to **Asset management \> Setup \> Workers \> Workers**, and make sure that the worker record that you identified (or created) in the previous step is mapped to a maintenance worker record.</span></span> <span data-ttu-id="b9dbc-110">Sukurkite būtiną naują techninės priežiūros darbuotojo įrašą ir nustatykite **Darbuotojas** lauką darbuotojo įraše iš ankstesnio veiksmo.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-110">Create a new maintenance worker record as required, and set the **Worker** field to the worker record from the previous step.</span></span>
1. <span data-ttu-id="b9dbc-111">Eikite į **Turto valdymas \> Sąranka \> Darbuotojai \> Techninės priežiūros darbuotojų grupės** ir įsitikinkite, kad jūsų ankstesniu veiksmu nustatytas (ar sukurtas) techninės priežiūros darbuotojo įrašas yra susietas su techninės priežiūros darbuotojo įrašu.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-111">Go to **Asset management \> Setup \> Workers \> Maintenance worker groups**, and make sure that the maintenance worker record that you identified (or created) in the previous step belongs to a maintenance worker group.</span></span>
1. <span data-ttu-id="b9dbc-112">Eikite į **Sistemos administravimas \> Vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-112">Go to **System administration \> Users**.</span></span>
1. <span data-ttu-id="b9dbc-113">Tinklelyje pasirinkite atitinkamą vartotoją.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-113">Select the relevant user in the grid.</span></span>
1. <span data-ttu-id="b9dbc-114">„FastTab” **Vartotojo informacija** skirtuke nustatykite **Asmuo** lauką darbuotojo paskyroje, kurią norite susieti su dabartinio vartotojo paskyra.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-114">On the **User Details** FastTab, set the **Person** field to the worker account that you want to associate with the current user account.</span></span> <span data-ttu-id="b9dbc-115">Ši darbuotojo paskyra turi būti jūsų 1-ame veiksme nustatytas (ar sukurtas) darbuotojo įrašas ir susietas su 2-ojo veiksmo techninės priežiūros darbuotojo įrašu.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-115">This worker account should be the worker record that you identified (or created) in step 1 and mapped to a maintenance worker record in step 2.</span></span>

> [!NOTE]
> <span data-ttu-id="b9dbc-116">Vartotojo teisės ir saugos vaidmenys taikomi **Turto valdymo** mobiliosios darbo srities funkcijoms, o taip pat ir „Supply Chain Management” vartotojo sąsajos funkcijoms.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-116">User permissions and security roles apply to the features of the **Asset management** mobile workspace just as they apply to the features of the Supply Chain Management user interface.</span></span> <span data-ttu-id="b9dbc-117">Todėl kiekvienas jūsų nustatytas vartotojas, norintis pasiekti **Turto valdymas** mobiliąją darbo sritį, privalo turėti saugos vaidmenis, būtinas atlikti panašias operacijas tiesiogiai „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-117">Therefore, every user that you set up to access the **Asset management** mobile workspace must have the security roles that are required to perform similar operations directly in Supply Chain Management.</span></span>

## <a name="publish-the-asset-management-mobile-workspace"></a><span data-ttu-id="b9dbc-118">Turto valdymo mobiliosios darbo srities paskelbimas</span><span class="sxs-lookup"><span data-stu-id="b9dbc-118">Publish the Asset management mobile workspace</span></span>

<span data-ttu-id="b9dbc-119">Norėdami įgalinti turto valdymo funkcijas „Finance and Operations” („Dynamics 365”) mobiliojoje programėlėje, turite publikuoti **Turto valdymas** mobiliąją darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-119">To make asset management features available in the Finance and Operations (Dynamics 365) mobile app, you must publish the **Asset management** mobile workspace.</span></span>

1. <span data-ttu-id="b9dbc-120">„Supply Chain Management” pasirinkite **Parametrai** mygtuką (krumpliaračio piktograma viršutiniame dešiniajame kampe) ir meniu pasirinkite **Mobilioji programėlė**.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-120">In Supply Chain Management, select the **Settings** button (the gear symbol in upper-right corner), and then select **Mobile app** on the menu.</span></span>
1. <span data-ttu-id="b9dbc-121">Dialogo lange **Tvarkyti mobiliąją programėlę** suraskite plytelę **Turto valdymas**.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-121">In the **Manage mobile app** dialog box, find the **Asset Management** tile.</span></span> <span data-ttu-id="b9dbc-122">Joje pateiktas tekstas „Metaduomenyse – nepublikuota”, darbo sritis dar nebuvo publikuota.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-122">If it contains the text "In metadata - not published," the workspace hasn't yet been published.</span></span> <span data-ttu-id="b9dbc-123">Jei joje yra tekstas „Metaduomenyse – publikuota”, darbo sritis jau publikuota, o likusią procedūrą galite praleisti.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-123">If it contains the text "In metadata - published," the workspace has already been published, and you can skip the rest of this procedure.</span></span>

    <span data-ttu-id="b9dbc-124">![Mobiliosios programėlės tvarkymo dialogo langas](media/mobile-workspaces.png "Mobiliosios programėlės tvarkymo dialogo langas")</span><span class="sxs-lookup"><span data-stu-id="b9dbc-124">![Manage mobile app dialog box](media/mobile-workspaces.png "Manage mobile app dialog box")</span></span>

1. <span data-ttu-id="b9dbc-125">Pasirinkite **Turto valdymas** plytelę, tada įrankių pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-125">Select the **Asset Management** tile, and then select **Publish** on the toolbar.</span></span> <span data-ttu-id="b9dbc-126">Po kelių sekundžių turėtumėte gauti pranešimą, kad darbo sritis sėkmingai publikuota.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-126">After a few seconds, you should receive a notification that states that the workspace has been successfully published.</span></span> <span data-ttu-id="b9dbc-127">Be to, plytelės tekstas turi pasikeisti į „Metaduomenyse – publikuota”.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-127">Additionally, the text on the tile should change to "In metadata - published."</span></span>

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a><span data-ttu-id="b9dbc-128">„Finance and Operations” ("Dynamics 365") mobiliosios programėlės įdiegimas ir konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="b9dbc-128">Install and set up the Finance and Operations (Dynamics 365) mobile app</span></span>

1. <span data-ttu-id="b9dbc-129">Norėdami įdiegti **„Microsoft Finance and Operations” ("Dynamics 365")** programėlę savo mobiliajame įrenginyje, apsilankykite vienoje iš mobiliųjų programėlių parduotuvių:</span><span class="sxs-lookup"><span data-stu-id="b9dbc-129">Go to one of the following app stores to install the **Microsoft Finance and Operations (Dynamics 365)** app on your mobile device:</span></span>

    - [<span data-ttu-id="b9dbc-130">„Google Android” įrenginiams</span><span class="sxs-lookup"><span data-stu-id="b9dbc-130">For Google Android devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
    - [<span data-ttu-id="b9dbc-131">„iOS” įrenginiams</span><span class="sxs-lookup"><span data-stu-id="b9dbc-131">For Apple iOS devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

1. <span data-ttu-id="b9dbc-132">Atidarykite „Finance and Operations” ("Dynamics 365") programėlę.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-132">Open the Finance and Operations (Dynamics 365) app.</span></span> <span data-ttu-id="b9dbc-133">Turėtų pasirodyti prisijungimo puslapis.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-133">The sign-in page should appear.</span></span> <span data-ttu-id="b9dbc-134">**Prisijungti** lauke įveskite „Supply Chain Management” URL arba įveskite neseniai naudotą URL **Neseniai naudotos aplinkos**  sąraše ir bakstelėkite **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-134">In the **Sign in** field, enter your Supply Chain Management URL, or select a recent URL in the **Recent environments** list, and then tap **Connect**.</span></span>

    <span data-ttu-id="b9dbc-135">![Prisijungimo puslapis](media/mobile-app-sign-in.png "Prisijungimo puslapis")</span><span class="sxs-lookup"><span data-stu-id="b9dbc-135">![Sign-in page](media/mobile-app-sign-in.png "Sign-in page")</span></span>

1. <span data-ttu-id="b9dbc-136">Jei būsite paraginti patvirtinti ryšį, pažymėkite žymės langelį **Supratau**, tada spustelėkite **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-136">If you're prompted to confirm the connection, select the **I understand** check box, and then tap **Connect**.</span></span>
1. <span data-ttu-id="b9dbc-137">Puslapyje **Pasirinkti paskyrą** naudokite „Microsoft” paskyrą, kad prisijungtumėte prie mobiliosios programėlės.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-137">On the **Pick an account** page, use your Microsoft account to sign in to the mobile application.</span></span>

    <span data-ttu-id="b9dbc-138">Pasirodo puslapis **Darbo sritys**.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-138">The **Workspaces** page appears.</span></span> <span data-ttu-id="b9dbc-139">Joje pateikiama kiekviena mobilioji darbo sritis, kurią publikavo „Supply Chain Management” programa.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-139">It lists every mobile workspace that has been published by your Supply Chain Management instance.</span></span>

    <span data-ttu-id="b9dbc-140">![Darbo sričių sąrašas](media/mobile-app-workspaces.png "Darbo sričių sąrašas")</span><span class="sxs-lookup"><span data-stu-id="b9dbc-140">![List of workspaces](media/mobile-app-workspaces.png "List of workspaces")</span></span>

1. <span data-ttu-id="b9dbc-141">Jei turite pakeisti juridinį asmenį (įmonę), bakstelėkite meniu mygtuką (trys horizontalios linijos) viršutiniame kairiajame kampe ir tada bakstelėkite **Keisti įmonę**.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-141">If you must change the legal entity (company), tap the Menu button (sometimes referred to as the hamburger or the hamburger button) in the upper-left corner, and then tap **Change company**.</span></span>

    <span data-ttu-id="b9dbc-142">![Juridinio asmens keitimas](media/mobile-app-change-comp.png "Juridinio asmens keitimas")</span><span class="sxs-lookup"><span data-stu-id="b9dbc-142">![Changing the legal entity](media/mobile-app-change-comp.png "Changing the legal entity")</span></span>

1. <span data-ttu-id="b9dbc-143">**Darbo sritys** puslapyje pasirinkite darbo sritį, su kurią norite dirbti, kad ją atidarytumėte.</span><span class="sxs-lookup"><span data-stu-id="b9dbc-143">On the **Workspaces** page, select the workspace that you want to work with to open it.</span></span>

    <span data-ttu-id="b9dbc-144">![Turto valdymo mobilioji darbo sritis](media/mobile-app-asset-workspace.png "Turto valdymo mobilioji darbo sritis")</span><span class="sxs-lookup"><span data-stu-id="b9dbc-144">![Asset management mobile workspace](media/mobile-app-asset-workspace.png "Asset management mobile workspace")</span></span>

## <a name="work-with-the-asset-management-mobile-workspace"></a><span data-ttu-id="b9dbc-145">Darbas su Turto valdymo mobiliąja darbo sritimi</span><span class="sxs-lookup"><span data-stu-id="b9dbc-145">Work with the Asset management mobile workspace</span></span>

<span data-ttu-id="b9dbc-146">Daugiau informacijos apie tai, kaip dirbti su **Turto valdymas** mobiliąja darbo sritimi, žr. [žr. Turto valdymo mobiliosios darbo srities naudojimas](asset-management-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="b9dbc-146">For more information about how to work with the **Asset management** mobile workspace, see [Use the Asset management mobile workspace](asset-management-mobile-workspace.md).</span></span>

<span data-ttu-id="b9dbc-147">Norėdami gauti daugiau informacijos apie „Finance and Operations” („Dynamics 365”) mobiliąją programėlę, žr. [Mobiliosios programėlės pagrindinis puslapis](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="b9dbc-147">For more information about the Finance and Operations (Dynamics 365) mobile app, see the [Mobile app home page](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]