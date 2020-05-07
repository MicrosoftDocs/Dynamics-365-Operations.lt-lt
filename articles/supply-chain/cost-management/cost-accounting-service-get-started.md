---
title: Darbo su kaštų apskaitos paslauga pradžia
description: Šioje temoje pateikiama licencijavimo informacija ir kaštų apskaitos paslaugos diegimo instrukcijos.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: cbbce7eaac264973bf0b95ad5175bf70ed2b4ae9
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276944"
---
# <a name="get-started-with-the-cost-accounting-service"></a><span data-ttu-id="ea1b5-103">Darbo su kaštų apskaitos paslauga pradžia</span><span class="sxs-lookup"><span data-stu-id="ea1b5-103">Get started with the cost accounting service</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="ea1b5-104">Šioje temoje nurodytos funkcijos yra privačiosios peržiūros versijos leidimo dalis.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="ea1b5-105">Šios temos turinys ir aprašomos funkcijos gali būti keičiami.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="ea1b5-106">Norėdami apie peržiūros leidimus gauti daugiau informacijos, žr. [DUK apie vienos versijos paslaugų naujinimus](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="ea1b5-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="ea1b5-107">Kaštų apskaitos paslauga leidžia atlikti kelias atsargų apskaitas kaštų apskaitos didžiosiose knygose, kurias nustatėte.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="ea1b5-108">Galite susieti kiekvieną kaštų apskaitos didžiąją knygą su *konvencija*.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="ea1b5-109">Konvencija yra toliau pateiktų apskaitos strategijų tipų rinkinys.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="ea1b5-110">Savikainos objektas</span><span class="sxs-lookup"><span data-stu-id="ea1b5-110">Cost object</span></span>
- <span data-ttu-id="ea1b5-111">Įeigos matavimo vieneto pagrindas</span><span class="sxs-lookup"><span data-stu-id="ea1b5-111">Input measurement basis</span></span>
- <span data-ttu-id="ea1b5-112">Savikainos srauto numanymas</span><span class="sxs-lookup"><span data-stu-id="ea1b5-112">Cost flow assumption</span></span>
- <span data-ttu-id="ea1b5-113">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="ea1b5-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="ea1b5-114">Netgi po to, kai įjungėte kaštų apskaitos paslaugą, galite atlikti atsargų apskaitą „Microsoft Dynamics 365 Supply Chain Management”, kaip įprasta.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="ea1b5-115">Kaštų apskaitos paslauga yra papildinys.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="ea1b5-116">Turite paslaugą įdiegti iš „Microsoft Dynamics Lifecycle Services” (LCS), kad jos funkcijos būtų prieinamos.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="ea1b5-117">Todėl prieš įjungdami paslaugą gamybos aplinkose galite pasirinkti, kad ji būtų vertinama tikrinimo aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="ea1b5-118">Kaštų apskaitos paslauga šiuo metu nepalaiko visų išlaidų valdymo funkcijų, kurios yra „Dynamics 365 Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="ea1b5-119">Todėl svarbu, kad įvertintumėte, ar funkcijų rinkinys, kurį šiuo metu galima naudoti, atitiks jūsų reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="licensing"></a><span data-ttu-id="ea1b5-120">Licencijavimas</span><span class="sxs-lookup"><span data-stu-id="ea1b5-120">Licensing</span></span>

<span data-ttu-id="ea1b5-121">Kaštų apskaitos paslauga licencijuojama kartu su standartinėmis atsargų apskaitos funkcijomis, kurios pasiekiamos „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-121">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="ea1b5-122">Nereikia pirkti papildomos licencijos, norint naudoti kaštų apskaitos paslaugą.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-122">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><span data-ttu-id="ea1b5-123">Papildinio įdiegimas</span><span class="sxs-lookup"><span data-stu-id="ea1b5-123">Install the add-in</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ea1b5-124">Norėdami naudoti kaštų apskaitos paslaugą, turite turėti plačiai pasiekiamą aplinką su įgalintais LCS (ne „OneBox” aplinką) ir „Dynamics 365 Supply Chain Management” 10.0.11 arba naujesnę versiją.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-124">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="ea1b5-125">Norėdami naudoti kaštų apskaitos paslaugą, įdiekite „Supply Chain Management” kaštų apskaitos paslaugos papildinį, kaip aprašyta tolesnėje procedūroje.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-125">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="ea1b5-126">Prisijunkite prie LCS.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-126">Sign in to LCS.</span></span>

1. <span data-ttu-id="ea1b5-127">Eikite į **Peržiūros funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-127">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="ea1b5-128">Pasirinkite pliuso ženklą (**+**).</span><span class="sxs-lookup"><span data-stu-id="ea1b5-128">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="ea1b5-129">Lauke **Kodas** įveskite jūsų kaštų apskaitos paslaugos papildinio beta raktą.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-129">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="ea1b5-130">(Raktą turite gauti el. paštu.)</span><span class="sxs-lookup"><span data-stu-id="ea1b5-130">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="ea1b5-131">Pasirinkite **Atblokuoti**.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-131">Select **Unblock**.</span></span>

1. <span data-ttu-id="ea1b5-132">Atidarykite LCS aplinką, į kurią norite įtraukti paslaugą.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-132">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="ea1b5-133">Eikite į **Išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-133">Go to **Full details**.</span></span>

1. <span data-ttu-id="ea1b5-134">Slinkite žemyn iki „FastTab“ **Aplinkos papildiniai**.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-134">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="ea1b5-135">Pasirinkite **Diegti naują papildinį**.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-135">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="ea1b5-136">Pasirinkite **Kaštų apskaitos paslauga**.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-136">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="ea1b5-137">Vadovaukitės diegimo vadovu ir sutikite su sąlygomis ir nuostatomis.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-137">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="ea1b5-138">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-138">Select **Install**.</span></span>

1. <span data-ttu-id="ea1b5-139">„FastTab” **Aplinkos papildiniai** turėtumėte matyti, kad kaštų apskaitos paslauga įdiegta.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-139">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="ea1b5-140">Po kelių minučių būsena turėtų pasikeisti iš **Diegiama** į **Įdiegta**.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-140">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="ea1b5-141">(Gali reikėti atnaujinti puslapį, kad pamatytumėte šį pakeitimą.) Tada kaštų apskaitos paslauga parengta naudoti.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-141">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="ea1b5-142">Integravimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="ea1b5-142">Set up the integration</span></span>

<span data-ttu-id="ea1b5-143">Norėdami nustatyti kaštų apskaitos paslaugos ir „Dynamics 365 Supply Chain Management” integravimą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-143">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="ea1b5-144">Eikite į **Sistemos administravimas > Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-144">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="ea1b5-145">Pasirinkite **Tikrinti, ar yra naujinimų**.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-145">Select **Check for updates**.</span></span>

1. <span data-ttu-id="ea1b5-146">Atidarykite skirtuką **Visi** ir ieškokite funkcijos pavadinimu *Kaštų apskaitos paslauga*.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-146">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="ea1b5-147">Pasirinkite **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-147">Select **Enable now**.</span></span>

1. <span data-ttu-id="ea1b5-148">Eiti į **Kaštų valdymas > Kaštų apskaitos paslauga > Nustatymas > Kaštų apskaitos paslaugos parametrai > Integravimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-148">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="ea1b5-149">Lauke **Programos ID** įveskite toliau nurodytą kodą.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-149">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="ea1b5-150">„08231eb2-a501-4edb-b3c5-aede5e5e0c3f“</span><span class="sxs-lookup"><span data-stu-id="ea1b5-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="ea1b5-151">Lauke **Duomenų paslaugos galinis punktas** įveskite toliau nurodytą URL.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-151">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="ea1b5-152">Lauke **Kaštų apskaitos paslaugos galinis punktas** įveskite toliau nurodytą URL.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-152">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="ea1b5-153">Kaštų apskaitos paslauga dabar parengta naudoti.</span><span class="sxs-lookup"><span data-stu-id="ea1b5-153">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="ea1b5-154">Susiję ištekliai</span><span class="sxs-lookup"><span data-stu-id="ea1b5-154">Related resources</span></span>

[<span data-ttu-id="ea1b5-155">Kaštų apskaitos paslaugos pagrindinis puslapis</span><span class="sxs-lookup"><span data-stu-id="ea1b5-155">Cost accounting service home page</span></span>](cost-accounting-service-home.md)
