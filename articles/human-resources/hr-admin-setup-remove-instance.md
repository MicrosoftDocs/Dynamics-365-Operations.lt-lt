---
title: Egzemplioriaus šalinimas
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5c5f875ad9361c31af4fbe863488b881cdd97a6e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009891"
---
# <a name="remove-an-instance"></a><span data-ttu-id="7ea72-102">Egzemplioriaus šalinimas</span><span class="sxs-lookup"><span data-stu-id="7ea72-102">Remove an instance</span></span>

<span data-ttu-id="7ea72-103">Šiame straipsnyje pateikiami veiksmai, skirti „Microsoft Dynamics 365 Human Resources“ bandomosios versijos arba gamybos aplinkai pašalinti.</span><span class="sxs-lookup"><span data-stu-id="7ea72-103">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="7ea72-104">Bandomosios versijos aplinkos šalinimas</span><span class="sxs-lookup"><span data-stu-id="7ea72-104">Remove a test drive environment</span></span>

<span data-ttu-id="7ea72-105">„Human Resources“ bandomosios versijos konfigūruojamos taikant 60 dienų galiojimo laiko strategiją.</span><span class="sxs-lookup"><span data-stu-id="7ea72-105">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="7ea72-106">Tačiau bandomųjų versijų savininkai turi galimybę anksčiau laiko užbaigti bandomosios versijos naudojimo laikotarpį atlikę toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7ea72-106">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="7ea72-107">Pereikite į [„Power Apps“ administravimo centrą](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="7ea72-107">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="7ea72-108">Pasirinkite **Aplinkos**.</span><span class="sxs-lookup"><span data-stu-id="7ea72-108">Select **Environments**.</span></span>
3. <span data-ttu-id="7ea72-109">Pasirinkite bandomosios versijos aplinką, kurios pavadinimas skamba panašiai į šį: TestDrive – alias@domain</span><span class="sxs-lookup"><span data-stu-id="7ea72-109">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="7ea72-110">Pasirinkite **Naikinti** ir patvirtinkite sprendimą.</span><span class="sxs-lookup"><span data-stu-id="7ea72-110">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="7ea72-111">Esama bandomosios versijos aplinka bus pašalinta.</span><span class="sxs-lookup"><span data-stu-id="7ea72-111">The existing test drive environment will be removed.</span></span> <span data-ttu-id="7ea72-112">Šalinimui pasibaigus galite užsiregistruoti naujoje bandomosios versijos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="7ea72-112">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="7ea72-113">Gamybos aplinkos šalinimas</span><span class="sxs-lookup"><span data-stu-id="7ea72-113">Remove a production environment</span></span>

<span data-ttu-id="7ea72-114">Šiame straipsnyje laikoma, kad įsigijote „Human Resources“ iš debesies sprendimų teikėjo (CSP) arba pagal įmonės architektūros (EA) sutartį.</span><span class="sxs-lookup"><span data-stu-id="7ea72-114">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="7ea72-115">Kadangi viena „Human Resources“ aplinka laikoma atskiroje „Power Apps“ aplinkoje, reikėtų atsižvelgti į dvi galimybes.</span><span class="sxs-lookup"><span data-stu-id="7ea72-115">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="7ea72-116">Pirmosios galimybės atveju pašalinama visa „Power Apps“ aplinka, antrosios – tik „Human Resources“ aplinka.</span><span class="sxs-lookup"><span data-stu-id="7ea72-116">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="7ea72-117">Pirmoji galimybė labiau tinka tuo atveju, kai „Power Apps“ aplinką sukuriate tik „Humas Resources“ konfigūravimo tikslais, o diegimą dar tik esate pradėję arba dar neturite jokių sukurtų integravimų.</span><span class="sxs-lookup"><span data-stu-id="7ea72-117">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="7ea72-118">Antroji galimybė tinka tuo atveju, kai turite sukurtą „Power Apps“ aplinką, užpildytą raiškiaisiais duomenimis, kurie naudojami „Power Apps “ ir „Power Automate“.</span><span class="sxs-lookup"><span data-stu-id="7ea72-118">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="7ea72-119">Prieš pašalindami „Power Apps“ aplinką įsitikinkite, kad ji nenaudojama raiškiųjų duomenų integravimams už „Human Resources“ apimties ribų.</span><span class="sxs-lookup"><span data-stu-id="7ea72-119">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="7ea72-120">Be to, atminkite, kad numatytųjų „Power Apps“ aplinkų pašalinti negalima.</span><span class="sxs-lookup"><span data-stu-id="7ea72-120">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="7ea72-121">Jei norite pašalinti visą „Power Apps“ aplinką, įskaitant „Human Resources“ bei susijusių programų ir srautų aplinką, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7ea72-121">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="7ea72-122">Pereikite į [„Power Apps“ administravimo centrą](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="7ea72-122">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="7ea72-123">Pasirinkite **Aplinkos**.</span><span class="sxs-lookup"><span data-stu-id="7ea72-123">Select **Environments**.</span></span>
3. <span data-ttu-id="7ea72-124">Pasirinkite šalintiną aplinką.</span><span class="sxs-lookup"><span data-stu-id="7ea72-124">Select the environment to be removed.</span></span>
4. <span data-ttu-id="7ea72-125">Pasirinkite **Naikinti** ir patvirtinkite sprendimą.</span><span class="sxs-lookup"><span data-stu-id="7ea72-125">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="7ea72-126">Palaukite, kol naikinimas bus baigtas.</span><span class="sxs-lookup"><span data-stu-id="7ea72-126">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="7ea72-127">Prisijunkite prie [„Lifecycle Services“](https://lcs.dynamics.com/Logon/Index) (LCS) naudodami paskyrą, kurią naudojote užsiprenumeruodami „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="7ea72-127">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="7ea72-128">Pasirinkite „Human Resources“ projektą, kuriame yra reikiama aplinka.</span><span class="sxs-lookup"><span data-stu-id="7ea72-128">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="7ea72-129">LCS projekte pasirinkite plytelę **Programos „Human Resources“ valdymas**.</span><span class="sxs-lookup"><span data-stu-id="7ea72-129">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="7ea72-130">Pasirinkite šalintiną egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="7ea72-130">Select the instance to remove.</span></span> 
10. <span data-ttu-id="7ea72-131">Pasirinkite **Pašalinti egzempliorių** ir patvirtinkite savo sprendimą.</span><span class="sxs-lookup"><span data-stu-id="7ea72-131">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="7ea72-132">Norėdami „Human Resources“ aplinką pašalinti iš esamos „Power Apps“ aplinkos, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7ea72-132">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="7ea72-133">Atkreipkite dėmesį, kad į pagalbos tarnybą ir „Human Resources DevOps“ komandą reikia kreiptis laikinai, kol ši funkcija bus įgalinta tiesiogiai LCS.</span><span class="sxs-lookup"><span data-stu-id="7ea72-133">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="7ea72-134">Kreipkitės į palaikymo tarnybą, kad inicijuotumėte pašalinimo užklausą.</span><span class="sxs-lookup"><span data-stu-id="7ea72-134">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="7ea72-135">Palaikymo tarnybos komanda pašalinimo užklausą inicijuos kartu su „Human Resources DevOps“ komanda.</span><span class="sxs-lookup"><span data-stu-id="7ea72-135">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="7ea72-136">Gavę pranešimą, kad aplinka pašalinta, tęskite toliau.</span><span class="sxs-lookup"><span data-stu-id="7ea72-136">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="7ea72-137">Prisijunkite prie LCS naudodami paskyrą, kurią naudojote prisijungti prie „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="7ea72-137">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="7ea72-138">Pasirinkite „Human Resources“ projektą, kuriame yra reikiama aplinka.</span><span class="sxs-lookup"><span data-stu-id="7ea72-138">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="7ea72-139">LCS projekte pasirinkite plytelę **Programos „Human Resources“ valdymas**.</span><span class="sxs-lookup"><span data-stu-id="7ea72-139">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="7ea72-140">Pasirinkite egzempliorių, kurį norite pašalinti ir kuris turi būti pažymėtas diegimo būsena **Nepavyko**.</span><span class="sxs-lookup"><span data-stu-id="7ea72-140">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="7ea72-141">Pasirinkite **Pašalinti egzempliorių** ir patvirtinkite savo sprendimą.</span><span class="sxs-lookup"><span data-stu-id="7ea72-141">Select **Remove instance** and confirm your decision.</span></span> 
