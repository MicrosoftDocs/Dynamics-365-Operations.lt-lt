---
title: Egzemplioriaus šalinimas
description: Šiame straipsnyje pateikiami veiksmai, skirti „Microsoft Dynamics 365 Human Resources“ bandomosios versijos arba gamybos aplinkai pašalinti.
author: andreabichsel
manager: AnnBe
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0a8eac74f0d840251ab56445dd5af4d19d3c0490
ms.sourcegitcommit: f759d361fa505323b8b171a98024dca9cc9fa0f0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/07/2020
ms.locfileid: "3668330"
---
# <a name="remove-an-instance"></a><span data-ttu-id="73f30-103">Egzemplioriaus šalinimas</span><span class="sxs-lookup"><span data-stu-id="73f30-103">Remove an instance</span></span>

<span data-ttu-id="73f30-104">Šiame straipsnyje pateikiami veiksmai, skirti „Microsoft Dynamics 365 Human Resources“ bandomosios versijos arba gamybos aplinkai pašalinti.</span><span class="sxs-lookup"><span data-stu-id="73f30-104">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="73f30-105">Bandomosios versijos aplinkos šalinimas</span><span class="sxs-lookup"><span data-stu-id="73f30-105">Remove a test drive environment</span></span>

<span data-ttu-id="73f30-106">„Human Resources“ bandomosios versijos konfigūruojamos taikant 60 dienų galiojimo laiko strategiją.</span><span class="sxs-lookup"><span data-stu-id="73f30-106">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="73f30-107">Tačiau bandomųjų versijų savininkai turi galimybę anksčiau laiko užbaigti bandomosios versijos naudojimo laikotarpį atlikę toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="73f30-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="73f30-108">Pereikite į [„Power Apps“ administravimo centrą](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="73f30-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="73f30-109">Pasirinkite **Aplinkos**.</span><span class="sxs-lookup"><span data-stu-id="73f30-109">Select **Environments**.</span></span>
3. <span data-ttu-id="73f30-110">Pasirinkite bandomosios versijos aplinką, kurios pavadinimas skamba panašiai į šį: TestDrive – alias@domain</span><span class="sxs-lookup"><span data-stu-id="73f30-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="73f30-111">Pasirinkite **Naikinti** ir patvirtinkite sprendimą.</span><span class="sxs-lookup"><span data-stu-id="73f30-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="73f30-112">Esama bandomosios versijos aplinka bus pašalinta.</span><span class="sxs-lookup"><span data-stu-id="73f30-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="73f30-113">Šalinimui pasibaigus galite užsiregistruoti naujoje bandomosios versijos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="73f30-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="73f30-114">Gamybos aplinkos šalinimas</span><span class="sxs-lookup"><span data-stu-id="73f30-114">Remove a production environment</span></span>

<span data-ttu-id="73f30-115">Šiame straipsnyje laikoma, kad įsigijote „Human Resources“ iš debesies sprendimų teikėjo (CSP) arba pagal įmonės architektūros (EA) sutartį.</span><span class="sxs-lookup"><span data-stu-id="73f30-115">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="73f30-116">Kadangi viena „Human Resources“ aplinka laikoma atskiroje „Power Apps“ aplinkoje, reikėtų atsižvelgti į dvi galimybes.</span><span class="sxs-lookup"><span data-stu-id="73f30-116">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="73f30-117">Pirmosios galimybės atveju pašalinama visa „Power Apps“ aplinka, antrosios – tik „Human Resources“ aplinka.</span><span class="sxs-lookup"><span data-stu-id="73f30-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="73f30-118">Pirmoji galimybė labiau tinka tuo atveju, kai „Power Apps“ aplinką sukuriate tik „Humas Resources“ konfigūravimo tikslais, o diegimą dar tik esate pradėję arba dar neturite jokių sukurtų integravimų.</span><span class="sxs-lookup"><span data-stu-id="73f30-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="73f30-119">Antroji galimybė tinka tuo atveju, kai turite sukurtą „Power Apps“ aplinką, užpildytą raiškiaisiais duomenimis, kurie naudojami „Power Apps “ ir „Power Automate“.</span><span class="sxs-lookup"><span data-stu-id="73f30-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="73f30-120">Prieš pašalindami „Power Apps“ aplinką įsitikinkite, kad ji nenaudojama raiškiųjų duomenų integravimams už „Human Resources“ apimties ribų.</span><span class="sxs-lookup"><span data-stu-id="73f30-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="73f30-121">Be to, atminkite, kad numatytųjų „Power Apps“ aplinkų pašalinti negalima.</span><span class="sxs-lookup"><span data-stu-id="73f30-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="73f30-122">Jei norite pašalinti visą „Power Apps“ aplinką, įskaitant „Human Resources“ bei susijusių programų ir srautų aplinką, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="73f30-122">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="73f30-123">Pereikite į [„Power Apps“ administravimo centrą](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="73f30-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="73f30-124">Pasirinkite **Aplinkos**.</span><span class="sxs-lookup"><span data-stu-id="73f30-124">Select **Environments**.</span></span>
3. <span data-ttu-id="73f30-125">Pasirinkite šalintiną aplinką.</span><span class="sxs-lookup"><span data-stu-id="73f30-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="73f30-126">Pasirinkite **Naikinti** ir patvirtinkite sprendimą.</span><span class="sxs-lookup"><span data-stu-id="73f30-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="73f30-127">Palaukite, kol naikinimas bus baigtas.</span><span class="sxs-lookup"><span data-stu-id="73f30-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="73f30-128">Prisijunkite prie [„Lifecycle Services“](https://lcs.dynamics.com/Logon/Index) (LCS) naudodami paskyrą, kurią naudojote užsiprenumeruodami „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="73f30-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="73f30-129">Pasirinkite „Human Resources“ projektą, kuriame yra reikiama aplinka.</span><span class="sxs-lookup"><span data-stu-id="73f30-129">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="73f30-130">LCS projekte pasirinkite plytelę **Programos „Human Resources“ valdymas**.</span><span class="sxs-lookup"><span data-stu-id="73f30-130">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="73f30-131">Pasirinkite šalintiną egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="73f30-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="73f30-132">Pasirinkite **Pašalinti egzempliorių** ir patvirtinkite savo sprendimą.</span><span class="sxs-lookup"><span data-stu-id="73f30-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="73f30-133">Norėdami „Human Resources“ aplinką pašalinti iš esamos „Power Apps“ aplinkos, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="73f30-133">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="73f30-134">Atkreipkite dėmesį, kad į pagalbos tarnybą ir „Human Resources DevOps“ komandą reikia kreiptis laikinai, kol ši funkcija bus įgalinta tiesiogiai LCS.</span><span class="sxs-lookup"><span data-stu-id="73f30-134">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="73f30-135">Kreipkitės į palaikymo tarnybą, kad inicijuotumėte pašalinimo užklausą.</span><span class="sxs-lookup"><span data-stu-id="73f30-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="73f30-136">Palaikymo tarnybos komanda pašalinimo užklausą inicijuos kartu su „Human Resources DevOps“ komanda.</span><span class="sxs-lookup"><span data-stu-id="73f30-136">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="73f30-137">Gavę pranešimą, kad aplinka pašalinta, tęskite toliau.</span><span class="sxs-lookup"><span data-stu-id="73f30-137">Continue after you receive word that the environment has been removed.</span></span>
4. <span data-ttu-id="73f30-138">Prisijunkite prie LCS naudodami paskyrą, kurią naudojote prisijungti prie „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="73f30-138">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="73f30-139">Pasirinkite „Human Resources“ projektą, kuriame yra reikiama aplinka.</span><span class="sxs-lookup"><span data-stu-id="73f30-139">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="73f30-140">LCS projekte pasirinkite plytelę **Programos „Human Resources“ valdymas**.</span><span class="sxs-lookup"><span data-stu-id="73f30-140">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="73f30-141">Pasirinkite norimą pašalinti instanciją, kuri turi būti pažymėta talpinimo **Pašalinta** statusu.</span><span class="sxs-lookup"><span data-stu-id="73f30-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Deleted**.</span></span>
8. <span data-ttu-id="73f30-142">Pasirinkite **Pašalinti egzempliorių** ir patvirtinkite savo sprendimą.</span><span class="sxs-lookup"><span data-stu-id="73f30-142">Select **Remove instance** and confirm your decision.</span></span> 

## <a name="recover-a-soft-deleted-environment"></a><span data-ttu-id="73f30-143">Švelniai pašalintos aplinkos atkūrimas</span><span class="sxs-lookup"><span data-stu-id="73f30-143">Recover a soft-deleted environment</span></span>

<span data-ttu-id="73f30-144">Jei pašalinate „Power Apps“ aplinką, prie kurios yra prijunta žmogiškųjų išteklių aplinka. žmogiškųjų išteklių aplinkos būsena „Lifecycle Services“ bus **Švelniai pašalinta**.</span><span class="sxs-lookup"><span data-stu-id="73f30-144">If you delete the Power Apps environment that your Human Resources environment is connected to, the status of the Human Resources environment in Lifecycle Services will be **Soft deleted**.</span></span> <span data-ttu-id="73f30-145">Tokiu atveju, naudotojai negalės prisijungti prie žmogiškųjų išteklių.</span><span class="sxs-lookup"><span data-stu-id="73f30-145">In this case, users can't connect to Human Resources.</span></span>

<span data-ttu-id="73f30-146">Aplinkos atkūrimui:</span><span class="sxs-lookup"><span data-stu-id="73f30-146">To restore the environment:</span></span>

1. <span data-ttu-id="73f30-147">Vadovaukitės instrukcijomis [Atkurti „Power Apps“ aplinką](/power-platform/admin/recover-environment.md).</span><span class="sxs-lookup"><span data-stu-id="73f30-147">Follow the instructions in [Recover the Power Apps environment](/power-platform/admin/recover-environment.md).</span></span>

2. <span data-ttu-id="73f30-148">Susisiekite su pagalbos skyriumi dėl žmogiškųjų išteklių aplinkos atkūrimo.</span><span class="sxs-lookup"><span data-stu-id="73f30-148">Contact Support to restore the Human Resources environment.</span></span> <span data-ttu-id="73f30-149">Norėdami gauti daugiau informacijos, [Gauti pagalbos](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="73f30-149">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

> [!Warning]
> <span data-ttu-id="73f30-150">„Power Apps“ aplinkos yra saugojamos tik septynias dienas po pašalinimo.</span><span class="sxs-lookup"><span data-stu-id="73f30-150">Power Apps environments are only saved for seven days after deletion.</span></span> <span data-ttu-id="73f30-151">Privalote atkurti aplinką per septynių dienų laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="73f30-151">You must recover the environment within the seven day period.</span></span>
