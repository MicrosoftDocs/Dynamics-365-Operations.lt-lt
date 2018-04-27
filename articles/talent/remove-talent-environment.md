---
title: "„Talent“ aplinkos šalinimas"
description: "Šioje temoje pateikiami veiksmai, skirti „Microsoft Dynamics 365 for Talent“ bandomosios versijos arba gamybos aplinkai pašalinti."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d1870c84d4d5e7402bae44d192ce7587c2f67fe7
ms.openlocfilehash: 0e7748b079b1cd5c069917d46e05cd281ea6aa01
ms.contentlocale: lt-lt
ms.lasthandoff: 04/05/2018

---
# <a name="remove-a-talent-environment"></a><span data-ttu-id="6cbae-103">„Talent“ aplinkos šalinimas</span><span class="sxs-lookup"><span data-stu-id="6cbae-103">Remove a Talent environment</span></span>

<span data-ttu-id="6cbae-104">Šioje temoje pateikiami veiksmai, skirti „Microsoft Dynamics 365 for Talent“ bandomosios versijos arba gamybos aplinkai pašalinti.</span><span class="sxs-lookup"><span data-stu-id="6cbae-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 for Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="6cbae-105">Bandomosios versijos aplinkos šalinimas</span><span class="sxs-lookup"><span data-stu-id="6cbae-105">Removing a test drive environment</span></span>

<span data-ttu-id="6cbae-106">„Talent“ bandomosios versijos konfigūruojamos taikant 60 dienų galiojimo laiko strategiją.</span><span class="sxs-lookup"><span data-stu-id="6cbae-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="6cbae-107">Tačiau bandomųjų versijų savininkai turi galimybę anksčiau laiko užbaigti bandomosios versijos naudojimo laikotarpį atlikę toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6cbae-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="6cbae-108">Eikite į [„PowerApps“ administravimo centrą](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="6cbae-108">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="6cbae-109">Pasirinkite **Aplinkos**.</span><span class="sxs-lookup"><span data-stu-id="6cbae-109">Select **Environments**.</span></span>
3. <span data-ttu-id="6cbae-110">Pasirinkite bandomosios versijos aplinką, kurios pavadinimas skamba panašiai į šį: bandomoji versija – alias@domain</span><span class="sxs-lookup"><span data-stu-id="6cbae-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="6cbae-111">Pasirinkite **Naikinti** ir patvirtinkite sprendimą.</span><span class="sxs-lookup"><span data-stu-id="6cbae-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="6cbae-112">Esama bandomosios versijos aplinka bus pašalinta.</span><span class="sxs-lookup"><span data-stu-id="6cbae-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="6cbae-113">Šalinimui pasibaigus galite užsiregistruoti naujoje bandomosios versijos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="6cbae-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="6cbae-114">Gamybos aplinkos šalinimas</span><span class="sxs-lookup"><span data-stu-id="6cbae-114">Removing a production environment</span></span>

<span data-ttu-id="6cbae-115">Šioje temoje laikoma, kad įsigijote „Talent“ iš debesies sprendimų teikėjo (CSP) arba pagal įmonės architektūros (EA) sutartį.</span><span class="sxs-lookup"><span data-stu-id="6cbae-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="6cbae-116">Kadangi viena „Talent“ aplinka laikoma atskiroje „PowerApps“ aplinkoje, reikėtų atsižvelgti į dvi galimybes.</span><span class="sxs-lookup"><span data-stu-id="6cbae-116">Since a single Talent environment is “contained” within a single PowerApps environment, there are two options to consider.</span></span> <span data-ttu-id="6cbae-117">Pirmosios galimybės atveju pašalinama visa „PowerApps“ aplinka, antrosios – tik „Talent“ aplinka.</span><span class="sxs-lookup"><span data-stu-id="6cbae-117">The first option involves removing the entire PowerApps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="6cbae-118">Pirmoji galimybė labiau tinka tuo atveju, kai „PowerApps“ aplinką sukuriate tik „Talent“ parengimo tikslais, o diegimus dar tik esate pradėję arba dar neturite jokių sukurtų integravimų.</span><span class="sxs-lookup"><span data-stu-id="6cbae-118">The first option is preferred when you have created a PowerApps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="6cbae-119">Antroji galimybė tinka tuo atveju, kai turite sukurtą „PowerApps“ aplinką, užpildytą raiškiaisiais duomenimis, kurie naudojami „PowerApps“ ir srautuose.</span><span class="sxs-lookup"><span data-stu-id="6cbae-119">The second option is appropriate when you have an established PowerApps environment populated with rich data that's leveraged in PowerApps and Flows.</span></span>

> [!Important]
> <span data-ttu-id="6cbae-120">Prieš pašalindami „PowerApps“ aplinką įsitikinkite, kad ji nenaudojama raiškiųjų duomenų integravimams už „Talent“ apimties ribų.</span><span class="sxs-lookup"><span data-stu-id="6cbae-120">Before removing the PowerApps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="6cbae-121">Be to, atminkite, kad numatytųjų „PowerApps“ aplinkų pašalinti negalima.</span><span class="sxs-lookup"><span data-stu-id="6cbae-121">Also note that the default PowerApps environments cannot be removed.</span></span> 

<span data-ttu-id="6cbae-122">Jei norite pašalinti visą PowerApps aplinką, įskaitant „Talent“ bei susijusių programų ir srautų aplinką, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6cbae-122">To remove the entire PowerApps environment, including Talent and the associated Apps and Flows:</span></span>

1. <span data-ttu-id="6cbae-123">Eikite į [„PowerApps“ administravimo centrą](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="6cbae-123">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="6cbae-124">Pasirinkite **Aplinkos**.</span><span class="sxs-lookup"><span data-stu-id="6cbae-124">Select **Environments**.</span></span>
3. <span data-ttu-id="6cbae-125">Pasirinkite šalintiną aplinką.</span><span class="sxs-lookup"><span data-stu-id="6cbae-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="6cbae-126">Pasirinkite **Naikinti** ir patvirtinkite sprendimą.</span><span class="sxs-lookup"><span data-stu-id="6cbae-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="6cbae-127">Palaukite, kol naikinimas bus baigtas.</span><span class="sxs-lookup"><span data-stu-id="6cbae-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="6cbae-128">Prisijunkite prie [„Lifecycle Services“](https://lcs.dynamics.com/Logon/Index) (LCS) naudodami abonementą, kurį naudojote užsiprenumeruodami „Talent“.</span><span class="sxs-lookup"><span data-stu-id="6cbae-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="6cbae-129">Pasirinkite „Talent“ projektą, kuriame yra reikiama aplinka.</span><span class="sxs-lookup"><span data-stu-id="6cbae-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="6cbae-130">LCS projekte pasirinkite plytelę **Programos „Talent“ valdymas**.</span><span class="sxs-lookup"><span data-stu-id="6cbae-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="6cbae-131">Pasirinkite šalintiną egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="6cbae-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="6cbae-132">Pasirinkite **Pašalinti egzempliorių** ir patvirtinkite savo sprendimą.</span><span class="sxs-lookup"><span data-stu-id="6cbae-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="6cbae-133">Norėdami „Talent“ aplinką pašalinti iš esamos „PowerApps“ aplinkos, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6cbae-133">To remove a Talent environment from an existing PowerApps environment, complete the following steps.</span></span> <span data-ttu-id="6cbae-134">Atkreipkite dėmesį, kad į pagalbos tarnybą ir „Talent DevOps“ komandą reikia kreiptis laikinai, kol ši funkcija bus įgalinta tiesiogiai LCS.</span><span class="sxs-lookup"><span data-stu-id="6cbae-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="6cbae-135">Kreipkitės į palaikymo tarnybą, kad inicijuotumėte pašalinimo užklausą.</span><span class="sxs-lookup"><span data-stu-id="6cbae-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="6cbae-136">Palaikymo tarnybos komanda pašalinimo užklausą inicijuos kartu su „Talent DevOps“ komanda.</span><span class="sxs-lookup"><span data-stu-id="6cbae-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="6cbae-137">Gavę pranešimą, kad aplinka pašalinta, tęskite toliau.</span><span class="sxs-lookup"><span data-stu-id="6cbae-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="6cbae-138">Prisijunkite prie LCS naudodami abonementą, kurį naudojote užsiprenumeruodami „Talent“.</span><span class="sxs-lookup"><span data-stu-id="6cbae-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="6cbae-139">Pasirinkite „Talent“ projektą, kuriame yra reikiama aplinka.</span><span class="sxs-lookup"><span data-stu-id="6cbae-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="6cbae-140">LCS projekte pasirinkite plytelę **Programos „Talent“ valdymas**.</span><span class="sxs-lookup"><span data-stu-id="6cbae-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="6cbae-141">Pasirinkite egzempliorių, kurį norite pašalinti ir kuris turi būti pažymėtas diegimo būsena **Nepavyko**.</span><span class="sxs-lookup"><span data-stu-id="6cbae-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="6cbae-142">Pasirinkite **Pašalinti egzempliorių** ir patvirtinkite savo sprendimą.</span><span class="sxs-lookup"><span data-stu-id="6cbae-142">Select **Remove instance** and confirm your decision.</span></span> 


