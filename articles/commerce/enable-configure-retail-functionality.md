---
title: Pradinių duomenų inicijavimas naujose „Commerce“ aplinkose
description: Šiame straipsnyje aprašyti duomenys, kurie kuriami „Dynamics 365 Commerce“ inicijavimo proceso metu.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: 24d4d49c51738203bb89a9844d57f644b8afd4b7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414257"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a><span data-ttu-id="c25de-103">Pradinių duomenų inicijavimas naujose „Commerce“ aplinkose</span><span class="sxs-lookup"><span data-stu-id="c25de-103">Initialize seed data in new Commerce environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c25de-104">Šiame straipsnyje aprašyti duomenys, kurie kuriami „Dynamics 365 Commerce“ inicijavimo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="c25de-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c25de-105">Kai naudodami „Microsoft Dynamics Lifecycle Services“ (LCS) įdiegiate sprendimą „Commerce“, turite inicijuoti „Commerce“ konfigūravimą ir sukurti pagrindinius konfigūravimo duomenis.</span><span class="sxs-lookup"><span data-stu-id="c25de-105">After the Commerce solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the Commerce configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c25de-106">Prieš inicijuodami „Commerce“ konfigūravimą, įsitikinkite, kad nurodėte visų juridinių subjektų, kuriuose nustatysite parduotuves, kalbą ir pašto adresą.</span><span class="sxs-lookup"><span data-stu-id="c25de-106">Before you initialize the commerce configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up stores.</span></span> <span data-ttu-id="c25de-107">Šį veiksmą reikia atlikti su visais juridiniais subjektais, kuriuose naudojate „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="c25de-107">This step must be completed for each legal entity that you use for commerce.</span></span>

<span data-ttu-id="c25de-108">Norėdami inicijuoti „Commerce“ konfigūravimą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c25de-108">To initialize the configuration, follow these steps.</span></span>

1. <span data-ttu-id="c25de-109">Paleiskite „Commerce“ klientą.</span><span class="sxs-lookup"><span data-stu-id="c25de-109">Start the Commerce client.</span></span>
2. <span data-ttu-id="c25de-110">Spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Būstinės sąranka** &gt; **Parametrai** &gt; **Prekybos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="c25de-110">Click **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce parameters**.</span></span>
3. <span data-ttu-id="c25de-111">Spustelėkite **Inicijuoti**.</span><span class="sxs-lookup"><span data-stu-id="c25de-111">Click **Initialize**.</span></span>

<span data-ttu-id="c25de-112">Inicijuojant sukuriami toliau pateikti numatytieji konfigūravimo duomenys.</span><span class="sxs-lookup"><span data-stu-id="c25de-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="c25de-113">„Commerce“ duomenų apsikeitimo valdymo užduotys ir antrinės užduotys</span><span class="sxs-lookup"><span data-stu-id="c25de-113">Commerce scheduler jobs and subjobs</span></span>
- <span data-ttu-id="c25de-114">„Commerce“ kanalo schema</span><span class="sxs-lookup"><span data-stu-id="c25de-114">Commerce channel schema</span></span>
- <span data-ttu-id="c25de-115">„Commerce“ paskirstymo grafikai</span><span class="sxs-lookup"><span data-stu-id="c25de-115">Commerce distribution schedules</span></span>
- <span data-ttu-id="c25de-116">Numatytieji ekrano maketai, apimantys mygtukynus, vaizdus ir temas</span><span class="sxs-lookup"><span data-stu-id="c25de-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="c25de-117">Laiko juostos informacija</span><span class="sxs-lookup"><span data-stu-id="c25de-117">Time zone information</span></span>
- <span data-ttu-id="c25de-118">Elektroninio kasos aparato (EKA) operacijos</span><span class="sxs-lookup"><span data-stu-id="c25de-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="c25de-119">EKA teisės</span><span class="sxs-lookup"><span data-stu-id="c25de-119">POS permissions</span></span>
- <span data-ttu-id="c25de-120">Kanalo ataskaitos</span><span class="sxs-lookup"><span data-stu-id="c25de-120">Channel reports</span></span>
- <span data-ttu-id="c25de-121">Atributo metaduomenys</span><span class="sxs-lookup"><span data-stu-id="c25de-121">Attribute metadata</span></span>
- <span data-ttu-id="c25de-122">Objektų tikrinimo šablonai</span><span class="sxs-lookup"><span data-stu-id="c25de-122">Entity validation templates</span></span>
- <span data-ttu-id="c25de-123">Paketinė užduotis, skirta „Commerce Data Exchange“ seansų retrospektyvai šalinti</span><span class="sxs-lookup"><span data-stu-id="c25de-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="c25de-124">Be to, įjungiama prisiregistravimo prie „Commerce“ duomenų bazės funkcija, susijusi su mokėjimo kortelių pramone (PCI).</span><span class="sxs-lookup"><span data-stu-id="c25de-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Commerce database.</span></span>

> [!NOTE]
> <span data-ttu-id="c25de-125">„Commerce“ duomenų apsikeitimo valdymą galima konfigūruoti atskirai.</span><span class="sxs-lookup"><span data-stu-id="c25de-125">There is an option to separately configure the Commerce scheduler.</span></span> <span data-ttu-id="c25de-126">Ši parinktis suteikia galimybę iš naujo nustatyti „Commerce“ duomenų apsikeitimo valdymo konfigūracijos numatytuosius parametrus.</span><span class="sxs-lookup"><span data-stu-id="c25de-126">This option lets you reset the Commerce scheduler configuration to its default settings.</span></span>

<span data-ttu-id="c25de-127">Baigę inicijavimą turite sukonfigūruoti papildomus „Commerce“ duomenis.</span><span class="sxs-lookup"><span data-stu-id="c25de-127">After initialization is completed, you must configure additional commerce data.</span></span> <span data-ttu-id="c25de-128">Štai keletas pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="c25de-128">Here are some examples:</span></span>

- <span data-ttu-id="c25de-129">„Commerce“ parametrai</span><span class="sxs-lookup"><span data-stu-id="c25de-129">Commerce parameters</span></span>
- <span data-ttu-id="c25de-130">„Commerce“ planuoklės parametrai</span><span class="sxs-lookup"><span data-stu-id="c25de-130">Commerce scheduler parameters</span></span>
- <span data-ttu-id="c25de-131">„Commerce“ kanalai</span><span class="sxs-lookup"><span data-stu-id="c25de-131">Commerce channels</span></span>
- <span data-ttu-id="c25de-132">Registrai ir įrenginiai</span><span class="sxs-lookup"><span data-stu-id="c25de-132">Registers and devices</span></span>
- <span data-ttu-id="c25de-133">Asortimentai</span><span class="sxs-lookup"><span data-stu-id="c25de-133">Assortments</span></span>
