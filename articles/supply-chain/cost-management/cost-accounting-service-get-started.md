---
title: Darbo su kaštų apskaitos paslauga pradžia (privati peržiūra)
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
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 1f602116edabc424b6cbee541e268df017912d3c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011852"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a><span data-ttu-id="8d969-103">Darbo su kaštų apskaitos paslauga pradžia (privati peržiūra)</span><span class="sxs-lookup"><span data-stu-id="8d969-103">Get started with the cost accounting service (private preview)</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="8d969-104">Šioje temoje nurodytos funkcijos yra privačiosios peržiūros versijos leidimo dalis.</span><span class="sxs-lookup"><span data-stu-id="8d969-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="8d969-105">Šios temos turinys ir aprašomos funkcijos gali būti keičiami.</span><span class="sxs-lookup"><span data-stu-id="8d969-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="8d969-106">Norėdami apie peržiūros leidimus gauti daugiau informacijos, žr. [DUK apie vienos versijos paslaugų naujinimus](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="8d969-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="8d969-107">Kaštų apskaitos paslauga leidžia atlikti kelias atsargų apskaitas kaštų apskaitos didžiosiose knygose, kurias nustatėte.</span><span class="sxs-lookup"><span data-stu-id="8d969-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="8d969-108">Galite susieti kiekvieną kaštų apskaitos didžiąją knygą su *konvencija*.</span><span class="sxs-lookup"><span data-stu-id="8d969-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="8d969-109">Konvencija yra toliau pateiktų apskaitos strategijų tipų rinkinys.</span><span class="sxs-lookup"><span data-stu-id="8d969-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="8d969-110">Savikainos objektas</span><span class="sxs-lookup"><span data-stu-id="8d969-110">Cost object</span></span>
- <span data-ttu-id="8d969-111">Įeigos matavimo vieneto pagrindas</span><span class="sxs-lookup"><span data-stu-id="8d969-111">Input measurement basis</span></span>
- <span data-ttu-id="8d969-112">Savikainos srauto numanymas</span><span class="sxs-lookup"><span data-stu-id="8d969-112">Cost flow assumption</span></span>
- <span data-ttu-id="8d969-113">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="8d969-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="8d969-114">Netgi po to, kai įjungėte kaštų apskaitos paslaugą, galite atlikti atsargų apskaitą „Microsoft Dynamics 365 Supply Chain Management”, kaip įprasta.</span><span class="sxs-lookup"><span data-stu-id="8d969-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="8d969-115">Kaštų apskaitos paslauga yra papildinys.</span><span class="sxs-lookup"><span data-stu-id="8d969-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="8d969-116">Turite paslaugą įdiegti iš „Microsoft Dynamics Lifecycle Services” (LCS), kad jos funkcijos būtų prieinamos.</span><span class="sxs-lookup"><span data-stu-id="8d969-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="8d969-117">Todėl prieš įjungdami paslaugą gamybos aplinkose galite pasirinkti, kad ji būtų vertinama tikrinimo aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="8d969-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="8d969-118">Kaštų apskaitos paslauga šiuo metu nepalaiko visų išlaidų valdymo funkcijų, kurios yra „Dynamics 365 Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="8d969-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="8d969-119">Todėl svarbu, kad įvertintumėte, ar funkcijų rinkinys, kurį šiuo metu galima naudoti, atitiks jūsų reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="8d969-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a><span data-ttu-id="8d969-120">Kaip gauti kaštų apskaitos paslaugą (privati peržiūra)</span><span class="sxs-lookup"><span data-stu-id="8d969-120">How to get the cost accounting service (private preview)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d969-121">Norėdami naudoti kaštų apskaitos paslaugą, turite turėti plačiai pasiekiamą aplinką su įgalintais LCS (ne „OneBox” aplinką) ir „Dynamics 365 Supply Chain Management” 10.0.11 arba naujesnę versiją.</span><span class="sxs-lookup"><span data-stu-id="8d969-121">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="8d969-122">Norėdami užsiregistruoti privačiai kaštų apskaitos paslaugos peržiūrai, atsiųskite savo LCS aplinkos ID el. paštu [Kaštų apskaitos paslauga (privati peržiūra)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span><span class="sxs-lookup"><span data-stu-id="8d969-122">To sign up for the cost accounting service private preview, please send your LCS environment ID by email to [Cost accounting service (private preview)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span></span> <span data-ttu-id="8d969-123">Patvirtinę jūsų dalyvavimą programoje, atsiųsime jums tolesnį el. laišką, kuriame bus kaštų apskaitos paslaugos beta raktas.</span><span class="sxs-lookup"><span data-stu-id="8d969-123">On approving you for the program, we will send you a follow up email that contains a cost accounting service beta key.</span></span> <span data-ttu-id="8d969-124">Gavę beta raktą, galite pradėti [papildinio diegimą](#install).</span><span class="sxs-lookup"><span data-stu-id="8d969-124">On receiving the beta key, you can proceed by [installing the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="8d969-125">Licencijavimas</span><span class="sxs-lookup"><span data-stu-id="8d969-125">Licensing</span></span>

<span data-ttu-id="8d969-126">Kaštų apskaitos paslauga licencijuojama kartu su standartinėmis atsargų apskaitos funkcijomis, kurios pasiekiamos „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="8d969-126">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="8d969-127">Nereikia pirkti papildomos licencijos, norint naudoti kaštų apskaitos paslaugą.</span><span class="sxs-lookup"><span data-stu-id="8d969-127">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="8d969-128">Papildinio įdiegimas</span><span class="sxs-lookup"><span data-stu-id="8d969-128">Install the add-in</span></span>

<span data-ttu-id="8d969-129">Norėdami naudoti kaštų apskaitos paslaugą, įdiekite „Supply Chain Management” kaštų apskaitos paslaugos papildinį, kaip aprašyta tolesnėje procedūroje.</span><span class="sxs-lookup"><span data-stu-id="8d969-129">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="8d969-130">[Užsiregistruokite](#sign-up) kaštų apskaitos paslaugai gauti (privati peržiūra).</span><span class="sxs-lookup"><span data-stu-id="8d969-130">[Sign up](#sign-up) for the cost accounting service (private preview).</span></span>

1. <span data-ttu-id="8d969-131">Prisijunkite prie LCS.</span><span class="sxs-lookup"><span data-stu-id="8d969-131">Sign in to LCS.</span></span>

1. <span data-ttu-id="8d969-132">Eikite į **Peržiūros funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="8d969-132">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="8d969-133">Pasirinkite pliuso ženklą (**+**).</span><span class="sxs-lookup"><span data-stu-id="8d969-133">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="8d969-134">Lauke **Kodas** įveskite jūsų kaštų apskaitos paslaugos papildinio beta raktą.</span><span class="sxs-lookup"><span data-stu-id="8d969-134">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="8d969-135">(Raktą turite gauti el. paštu.)</span><span class="sxs-lookup"><span data-stu-id="8d969-135">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="8d969-136">Pasirinkite **Atblokuoti**.</span><span class="sxs-lookup"><span data-stu-id="8d969-136">Select **Unblock**.</span></span>

1. <span data-ttu-id="8d969-137">Atidarykite LCS aplinką, į kurią norite įtraukti paslaugą.</span><span class="sxs-lookup"><span data-stu-id="8d969-137">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="8d969-138">Eikite į **Išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="8d969-138">Go to **Full details**.</span></span>

1. <span data-ttu-id="8d969-139">Slinkite žemyn iki „FastTab“ **Aplinkos papildiniai**.</span><span class="sxs-lookup"><span data-stu-id="8d969-139">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="8d969-140">Pasirinkite **Diegti naują papildinį**.</span><span class="sxs-lookup"><span data-stu-id="8d969-140">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="8d969-141">Pasirinkite **Kaštų apskaitos paslauga**.</span><span class="sxs-lookup"><span data-stu-id="8d969-141">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="8d969-142">Vadovaukitės diegimo vadovu ir sutikite su sąlygomis ir nuostatomis.</span><span class="sxs-lookup"><span data-stu-id="8d969-142">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="8d969-143">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="8d969-143">Select **Install**.</span></span>

1. <span data-ttu-id="8d969-144">„FastTab” **Aplinkos papildiniai** turėtumėte matyti, kad kaštų apskaitos paslauga įdiegta.</span><span class="sxs-lookup"><span data-stu-id="8d969-144">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="8d969-145">Po kelių minučių būsena turėtų pasikeisti iš **Diegiama** į **Įdiegta**.</span><span class="sxs-lookup"><span data-stu-id="8d969-145">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="8d969-146">(Gali reikėti atnaujinti puslapį, kad pamatytumėte šį pakeitimą.) Tada kaštų apskaitos paslauga parengta naudoti.</span><span class="sxs-lookup"><span data-stu-id="8d969-146">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="8d969-147">Integravimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="8d969-147">Set up the integration</span></span>

<span data-ttu-id="8d969-148">Norėdami nustatyti kaštų apskaitos paslaugos ir „Dynamics 365 Supply Chain Management” integravimą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="8d969-148">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="8d969-149">Eikite į **Sistemos administravimas > Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="8d969-149">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="8d969-150">Pasirinkite **Tikrinti, ar yra naujinimų**.</span><span class="sxs-lookup"><span data-stu-id="8d969-150">Select **Check for updates**.</span></span>

1. <span data-ttu-id="8d969-151">Atidarykite skirtuką **Visi** ir ieškokite funkcijos pavadinimu *Kaštų apskaitos paslauga*.</span><span class="sxs-lookup"><span data-stu-id="8d969-151">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="8d969-152">Pasirinkite **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="8d969-152">Select **Enable now**.</span></span>

1. <span data-ttu-id="8d969-153">Eiti į **Kaštų valdymas > Kaštų apskaitos paslauga > Nustatymas > Kaštų apskaitos paslaugos parametrai > Integravimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="8d969-153">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="8d969-154">Lauke **Programos ID** įveskite toliau nurodytą kodą.</span><span class="sxs-lookup"><span data-stu-id="8d969-154">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="8d969-155">„08231eb2-a501-4edb-b3c5-aede5e5e0c3f“</span><span class="sxs-lookup"><span data-stu-id="8d969-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="8d969-156">Lauke **Duomenų paslaugos galinis punktas** įveskite toliau nurodytą URL.</span><span class="sxs-lookup"><span data-stu-id="8d969-156">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="8d969-157">Lauke **Kaštų apskaitos paslaugos galinis punktas** įveskite toliau nurodytą URL.</span><span class="sxs-lookup"><span data-stu-id="8d969-157">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="8d969-158">Kaštų apskaitos paslauga dabar parengta naudoti.</span><span class="sxs-lookup"><span data-stu-id="8d969-158">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="8d969-159">Susiję ištekliai</span><span class="sxs-lookup"><span data-stu-id="8d969-159">Related resources</span></span>

[<span data-ttu-id="8d969-160">Kaštų apskaitos paslaugos pagrindinis puslapis</span><span class="sxs-lookup"><span data-stu-id="8d969-160">Cost accounting service home page</span></span>](cost-accounting-service-home.md)
