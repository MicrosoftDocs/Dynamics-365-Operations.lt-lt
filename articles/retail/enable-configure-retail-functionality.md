---
title: "Pradinių duomenų inicijavimas „Retail“ aplinkoje"
description: "Šiame straipsnyje aprašyti duomenys, kurie kuriami „Microsoft Dynamics 365 for Retail“ inicijavimo proceso metu."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: d3c81aaa675352eb679c1e1540f947c1d1da804b
ms.contentlocale: lt-lt
ms.lasthandoff: 01/17/2018

---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a><span data-ttu-id="4a707-103">Pradinių duomenų inicijavimas „Retail“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="4a707-103">Initialize seed data in a new Retail environment</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="4a707-104">Šiame straipsnyje aprašyti duomenys, kurie kuriami „Microsoft Dynamics 365 for Retail“ inicijavimo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="4a707-104">This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="4a707-105">Kai naudodami „Microsoft Dynamics Lifecycle Services“ (LCS) įdiegiate mažmeninės prekybos sprendimą, turite inicijuoti mažmeninės prekybos konfigūravimą ir sukurti pagrindinius konfigūravimo duomenis.</span><span class="sxs-lookup"><span data-stu-id="4a707-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span> <span data-ttu-id="4a707-106">**Svarbu:** prieš inicijuodami mažmeninės prekybos konfigūravimą, įsitikinkite, kad nurodėte visų juridinių subjektų, kuriuose nustatysite mažmeninės prekybos parduotuves, kalbą ir pašto adresą.</span><span class="sxs-lookup"><span data-stu-id="4a707-106">**Important:** Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="4a707-107">Šį veiksmą reikia atlikti su visais juridiniais subjektais, kuriuose naudojate mažmeninėje prekyboje.</span><span class="sxs-lookup"><span data-stu-id="4a707-107">This step must be completed for each legal entity that you use for retail.</span></span> <span data-ttu-id="4a707-108">Norėdami inicijuoti mažmeninės prekybos konfigūravimą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4a707-108">To initialize the retail configuration, follow these steps.</span></span>

1.  <span data-ttu-id="4a707-109">Paleiskite „Dynamics 365 for Retail“ klientą.</span><span class="sxs-lookup"><span data-stu-id="4a707-109">Start the Dynamics 365 for Retail client.</span></span>
2.  <span data-ttu-id="4a707-110">Spustelėkite **Mažmeninė prekyba** &gt; **„Headquarters“ sąranka** &gt; **Parametrai** &gt; **Mažmeninės prekybos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="4a707-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3.  <span data-ttu-id="4a707-111">Spustelėkite **Inicijuoti**.</span><span class="sxs-lookup"><span data-stu-id="4a707-111">Click **Initialize**.</span></span>

<span data-ttu-id="4a707-112">Inicijuojant sukuriami toliau pateikti numatytieji konfigūravimo duomenys.</span><span class="sxs-lookup"><span data-stu-id="4a707-112">Initialization creates the following default configuration data:</span></span>

-   <span data-ttu-id="4a707-113">Duomenų apsikeitimo valdymo užduotys ir antrinės užduotys</span><span class="sxs-lookup"><span data-stu-id="4a707-113">Retail scheduler jobs and subjobs</span></span>
-   <span data-ttu-id="4a707-114">Mažmeninės prekybos kanalo schema</span><span class="sxs-lookup"><span data-stu-id="4a707-114">Retail channel schema</span></span>
-   <span data-ttu-id="4a707-115">Mažmeninės prekybos paskirstymo grafikai</span><span class="sxs-lookup"><span data-stu-id="4a707-115">Retail distribution schedules</span></span>
-   <span data-ttu-id="4a707-116">Numatytieji ekrano maketai, apimantys mygtukynus, vaizdus ir temas</span><span class="sxs-lookup"><span data-stu-id="4a707-116">Default screen layouts, which include button grids, images, and themes</span></span>
-   <span data-ttu-id="4a707-117">Laiko juostos informacija</span><span class="sxs-lookup"><span data-stu-id="4a707-117">Time zone information</span></span>
-   <span data-ttu-id="4a707-118">Elektroninio kasos aparato (EKA) operacijos</span><span class="sxs-lookup"><span data-stu-id="4a707-118">Point-of-sale (POS) operations</span></span>
-   <span data-ttu-id="4a707-119">EKA teisės</span><span class="sxs-lookup"><span data-stu-id="4a707-119">POS permissions</span></span>
-   <span data-ttu-id="4a707-120">Kanalo ataskaitos</span><span class="sxs-lookup"><span data-stu-id="4a707-120">Channel reports</span></span>
-   <span data-ttu-id="4a707-121">Atributo metaduomenys</span><span class="sxs-lookup"><span data-stu-id="4a707-121">Attribute metadata</span></span>
-   <span data-ttu-id="4a707-122">Objektų tikrinimo šablonai</span><span class="sxs-lookup"><span data-stu-id="4a707-122">Entity validation templates</span></span>
-   <span data-ttu-id="4a707-123">Paketinė užduotis, skirta „Commerce Data Exchange“ seansų retrospektyvai šalinti</span><span class="sxs-lookup"><span data-stu-id="4a707-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="4a707-124">Be to, įjungiama prisiregistravimo prie „Dynamics 365 for Retail“ duomenų bazės funkcija, susijusi su mokėjimo kortelių pramone (PCI).</span><span class="sxs-lookup"><span data-stu-id="4a707-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Retail database.</span></span> <span data-ttu-id="4a707-125">**Pastaba:** duomenų apsikeitimo valdymą galima konfigūruoti atskirai.</span><span class="sxs-lookup"><span data-stu-id="4a707-125">**Note:** There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="4a707-126">Ši parinktis suteikia galimybę iš naujo nustatyti mažmeninės prekybos duomenų apsikeitimo valdymo konfigūracijos numatytuosius parametrus.</span><span class="sxs-lookup"><span data-stu-id="4a707-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span> <span data-ttu-id="4a707-127">Baigę inicijavimą turite sukonfigūruoti papildomus mažmeninės prekybos duomenis.</span><span class="sxs-lookup"><span data-stu-id="4a707-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="4a707-128">Štai keletas pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="4a707-128">Here are some examples:</span></span>

-   <span data-ttu-id="4a707-129">Mažmeninės prekybos parametrai</span><span class="sxs-lookup"><span data-stu-id="4a707-129">Retail parameters</span></span>
-   <span data-ttu-id="4a707-130">Duomenų apsikeitimo valdymo parametrai</span><span class="sxs-lookup"><span data-stu-id="4a707-130">Retail scheduler parameters</span></span>
-   <span data-ttu-id="4a707-131">Mažmeninės prekybos kanalai</span><span class="sxs-lookup"><span data-stu-id="4a707-131">Retail channels</span></span>
-   <span data-ttu-id="4a707-132">Registrai ir įrenginiai</span><span class="sxs-lookup"><span data-stu-id="4a707-132">Registers and devices</span></span>
-   <span data-ttu-id="4a707-133">Asortimentai</span><span class="sxs-lookup"><span data-stu-id="4a707-133">Assortments</span></span>





