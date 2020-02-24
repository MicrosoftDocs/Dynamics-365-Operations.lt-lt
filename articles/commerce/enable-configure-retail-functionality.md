---
title: Pradinių duomenų inicijavimas naujose „Retail“ aplinkose
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
ms.openlocfilehash: e2833c32d557ec3d2dc80808222d1d47860ce6ea
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023458"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a><span data-ttu-id="398fa-103">Pradinių duomenų inicijavimas naujose „Retail“ aplinkose</span><span class="sxs-lookup"><span data-stu-id="398fa-103">Initialize seed data in new Retail environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="398fa-104">Šiame straipsnyje aprašyti duomenys, kurie kuriami „Dynamics 365 Commerce“ inicijavimo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="398fa-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Commerce.</span></span>

<span data-ttu-id="398fa-105">Kai naudodami „Microsoft Dynamics Lifecycle Services“ (LCS) įdiegiate sprendimą „Commerce“, turite inicijuoti „Commerce“ konfigūravimą ir sukurti pagrindinius konfigūravimo duomenis.</span><span class="sxs-lookup"><span data-stu-id="398fa-105">After the Commerce solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the Commerce configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="398fa-106">Prieš inicijuodami „Commerce“ konfigūravimą, įsitikinkite, kad nurodėte visų juridinių subjektų, kuriuose nustatysite parduotuves, kalbą ir pašto adresą.</span><span class="sxs-lookup"><span data-stu-id="398fa-106">Before you initialize the commerce configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up stores.</span></span> <span data-ttu-id="398fa-107">Šį veiksmą reikia atlikti su visais juridiniais subjektais, kuriuose naudojate „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="398fa-107">This step must be completed for each legal entity that you use for commerce.</span></span>

<span data-ttu-id="398fa-108">Norėdami inicijuoti „Commerce“ konfigūravimą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="398fa-108">To initialize the configuration, follow these steps.</span></span>

1. <span data-ttu-id="398fa-109">Paleiskite „Commerce“ klientą.</span><span class="sxs-lookup"><span data-stu-id="398fa-109">Start the Commerce client.</span></span>
2. <span data-ttu-id="398fa-110">Spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Būstinės sąranka** &gt; **Parametrai** &gt; **Prekybos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="398fa-110">Click **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce parameters**.</span></span>
3. <span data-ttu-id="398fa-111">Spustelėkite **Inicijuoti**.</span><span class="sxs-lookup"><span data-stu-id="398fa-111">Click **Initialize**.</span></span>

<span data-ttu-id="398fa-112">Inicijuojant sukuriami toliau pateikti numatytieji konfigūravimo duomenys.</span><span class="sxs-lookup"><span data-stu-id="398fa-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="398fa-113">„Commerce“ duomenų apsikeitimo valdymo užduotys ir antrinės užduotys</span><span class="sxs-lookup"><span data-stu-id="398fa-113">Commerce scheduler jobs and subjobs</span></span>
- <span data-ttu-id="398fa-114">„Commerce“ kanalo schema</span><span class="sxs-lookup"><span data-stu-id="398fa-114">Commerce channel schema</span></span>
- <span data-ttu-id="398fa-115">„Commerce“ paskirstymo grafikai</span><span class="sxs-lookup"><span data-stu-id="398fa-115">Commerce distribution schedules</span></span>
- <span data-ttu-id="398fa-116">Numatytieji ekrano maketai, apimantys mygtukynus, vaizdus ir temas</span><span class="sxs-lookup"><span data-stu-id="398fa-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="398fa-117">Laiko juostos informacija</span><span class="sxs-lookup"><span data-stu-id="398fa-117">Time zone information</span></span>
- <span data-ttu-id="398fa-118">Elektroninio kasos aparato (EKA) operacijos</span><span class="sxs-lookup"><span data-stu-id="398fa-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="398fa-119">EKA teisės</span><span class="sxs-lookup"><span data-stu-id="398fa-119">POS permissions</span></span>
- <span data-ttu-id="398fa-120">Kanalo ataskaitos</span><span class="sxs-lookup"><span data-stu-id="398fa-120">Channel reports</span></span>
- <span data-ttu-id="398fa-121">Atributo metaduomenys</span><span class="sxs-lookup"><span data-stu-id="398fa-121">Attribute metadata</span></span>
- <span data-ttu-id="398fa-122">Objektų tikrinimo šablonai</span><span class="sxs-lookup"><span data-stu-id="398fa-122">Entity validation templates</span></span>
- <span data-ttu-id="398fa-123">Paketinė užduotis, skirta „Commerce Data Exchange“ seansų retrospektyvai šalinti</span><span class="sxs-lookup"><span data-stu-id="398fa-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="398fa-124">Be to, įjungiama prisiregistravimo prie „Commerce“ duomenų bazės funkcija, susijusi su mokėjimo kortelių pramone (PCI).</span><span class="sxs-lookup"><span data-stu-id="398fa-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Commerce database.</span></span>

> [!NOTE]
> <span data-ttu-id="398fa-125">„Commerce“ duomenų apsikeitimo valdymą galima konfigūruoti atskirai.</span><span class="sxs-lookup"><span data-stu-id="398fa-125">There is an option to separately configure the Commerce scheduler.</span></span> <span data-ttu-id="398fa-126">Ši parinktis suteikia galimybę iš naujo nustatyti „Commerce“ duomenų apsikeitimo valdymo konfigūracijos numatytuosius parametrus.</span><span class="sxs-lookup"><span data-stu-id="398fa-126">This option lets you reset the Commerce scheduler configuration to its default settings.</span></span>

<span data-ttu-id="398fa-127">Baigę inicijavimą turite sukonfigūruoti papildomus „Commerce“ duomenis.</span><span class="sxs-lookup"><span data-stu-id="398fa-127">After initialization is completed, you must configure additional commerce data.</span></span> <span data-ttu-id="398fa-128">Štai keletas pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="398fa-128">Here are some examples:</span></span>

- <span data-ttu-id="398fa-129">„Commerce“ parametrai</span><span class="sxs-lookup"><span data-stu-id="398fa-129">Commerce parameters</span></span>
- <span data-ttu-id="398fa-130">„Commerce“ planuoklės parametrai</span><span class="sxs-lookup"><span data-stu-id="398fa-130">Commerce scheduler parameters</span></span>
- <span data-ttu-id="398fa-131">„Commerce“ kanalai</span><span class="sxs-lookup"><span data-stu-id="398fa-131">Commerce channels</span></span>
- <span data-ttu-id="398fa-132">Registrai ir įrenginiai</span><span class="sxs-lookup"><span data-stu-id="398fa-132">Registers and devices</span></span>
- <span data-ttu-id="398fa-133">Asortimentai</span><span class="sxs-lookup"><span data-stu-id="398fa-133">Assortments</span></span>
