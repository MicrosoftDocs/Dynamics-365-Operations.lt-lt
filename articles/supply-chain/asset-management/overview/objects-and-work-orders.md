---
title: Turtas ir darbo užsakymai
description: Šioje temoje aprašomas turtas ir darbo užsakymai modulyje „Turto valdymas“.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c2500a695fcffe0d60ac13b1b74cda4322b0e14
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206897"
---
# <a name="assets-and-work-orders"></a><span data-ttu-id="6e307-103">Turtas ir darbo užsakymai</span><span class="sxs-lookup"><span data-stu-id="6e307-103">Assets and work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6e307-104">Šioje temoje aprašomas turtas ir darbo užsakymai modulyje „Turto valdymas“.</span><span class="sxs-lookup"><span data-stu-id="6e307-104">This topic describes assets and work orders in Asset Management.</span></span> <span data-ttu-id="6e307-105">Turtas ir darbo užsakymai yra pagrindinės modulio „Turto valdymas“ dalys.</span><span class="sxs-lookup"><span data-stu-id="6e307-105">Assets and work orders are the central parts of Asset Management.</span></span> <span data-ttu-id="6e307-106">*Turtas* yra mašina arba mašinos dalis, kurią reikia nuolat prižiūrėti ir teikti aptarnavimo paslaugas.</span><span class="sxs-lookup"><span data-stu-id="6e307-106">An *asset* is a machine or machine part that requires continuous maintenance and service.</span></span> <span data-ttu-id="6e307-107">Turtas gali būti kuriamas taikant hierarchinę struktūrą ir gali būti siejamas su funkcinėmis vietomis.</span><span class="sxs-lookup"><span data-stu-id="6e307-107">Assets can be created in a hierarchical structure, and they can be related to functional locations.</span></span> <span data-ttu-id="6e307-108">Priežiūros užduotys gali būti planuojamos visais lygiais turto struktūroje.</span><span class="sxs-lookup"><span data-stu-id="6e307-108">Maintenance jobs can be planned at all levels in the asset structure.</span></span>

<span data-ttu-id="6e307-109">Konfigūruojami įvairūs kiekvieno turto duomenys, pvz., produkto informacija ir turto specifikacija, taip pat reikiami priežiūros planai.</span><span class="sxs-lookup"><span data-stu-id="6e307-109">Various data, such as product information and asset specification, and required maintenance plans are set up on each asset.</span></span> <span data-ttu-id="6e307-110">Toliau pateiktame paveikslėlyje rodoma turto duomenų ir turto priskyrimo užduočių tipams apžvalga.</span><span class="sxs-lookup"><span data-stu-id="6e307-110">The following illustration shows an overview of asset data and the affiliation of assets to job types.</span></span> <span data-ttu-id="6e307-111">Raudonas tekstas naudojamas pavyzdžiams, rodantiems paveldėjimą ir priklausomybes, pateikti.</span><span class="sxs-lookup"><span data-stu-id="6e307-111">Red text is used for examples that show inheritance and dependencies.</span></span>

![Diagrama, rodanti turto duomenis, susijusius su užduočių tipais](media/05-overview-image.png)

<span data-ttu-id="6e307-113">Kiekvienas darbo užsakymas turi darbo užsakymo tipą, pvz., prevencinė priežiūra, koreguojamoji priežiūra arba patikra.</span><span class="sxs-lookup"><span data-stu-id="6e307-113">Every work order has a work order type, such preventive maintenance, corrective maintenance, or inspection.</span></span> <span data-ttu-id="6e307-114">Darbo užsakymą sudaro viena ar daugiau darbo užsakymo užduočių.</span><span class="sxs-lookup"><span data-stu-id="6e307-114">The work order contains one or more work order jobs.</span></span> <span data-ttu-id="6e307-115">Kiekviena darbo užsakymo užduotis apibrėžia užduotį, kurią reikia atlikti su turtu ir susijusiu užduoties tipu.</span><span class="sxs-lookup"><span data-stu-id="6e307-115">Every work order job defines a job that must be performed on an asset and a related job type.</span></span> <span data-ttu-id="6e307-116">Susijusių užduočių tipų pavyzdžiai yra 10 000 km, 50 000 km, kapitalinis remontas po 1 metų ir saugos patikra.</span><span class="sxs-lookup"><span data-stu-id="6e307-116">Examples of related job types include 10,000 km, 50,000 km, 1-year overhaul, and safety inspection.</span></span> <span data-ttu-id="6e307-117">Vienas darbo užsakymas gali būti siejamas su keliais turtais.</span><span class="sxs-lookup"><span data-stu-id="6e307-117">One work order can be related to multiple assets.</span></span>

<span data-ttu-id="6e307-118">Toliau pateiktame paveikslėlyje rodoma rakto duomenų darbo užsakyme apžvalga.</span><span class="sxs-lookup"><span data-stu-id="6e307-118">The following illustration shows an overview of the key data in a work order.</span></span>

![Diagrama, rodanti pagrindinius darbo užsakymo duomenis](media/06-overview-image.png)

<span data-ttu-id="6e307-120">Darbo užsakymą galima susieti su kitu darbo užsakymu, o užduočių tipuose gali būti kitų užduočių, kurie sudaro darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="6e307-120">A work order can be related to another work order, and job types can contain succeeding jobs that create a work order.</span></span> <span data-ttu-id="6e307-121">Apskritai, priklausomybės tarp darbo užsakymų nėra.</span><span class="sxs-lookup"><span data-stu-id="6e307-121">In general, there are no dependencies between work orders.</span></span> <span data-ttu-id="6e307-122">Todėl gali keistis darbo užsakymų ciklo būsena ir juos galima planuoti nepriklausomai vieną nuo kito.</span><span class="sxs-lookup"><span data-stu-id="6e307-122">Therefore, they can change their work order lifecycle state and can be scheduled independently of each other.</span></span>

<span data-ttu-id="6e307-123">Darbo užsakymai gali būti kuriami įvairiais būdais, susijusiais su korekcine, prevencine arba einamąja priežiūra.</span><span class="sxs-lookup"><span data-stu-id="6e307-123">Work orders can be created in various ways that are related to corrective, preventive, or reactive maintenance.</span></span> <span data-ttu-id="6e307-124">Kategorijas taip pat galite kurti neautomatiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="6e307-124">You can also create work orders manually.</span></span> <span data-ttu-id="6e307-125">Toliau pateiktame paveikslėlyje parodyta automatinio arba neautomatinio darbo užsakymų kūrimo proceso apžvalga.</span><span class="sxs-lookup"><span data-stu-id="6e307-125">The following illustration shows an overview of the process for automatic or manual creation of work orders.</span></span>

![Diagrama, rodanti automatinį arba rankinį darbo užsakymų kūrimą](media/07-overview-image.png)

<span data-ttu-id="6e307-127">Kai norite planuoti ir vykdyti darbo užsakymo priežiūros užduotį, reikia atlikti keletą veiksmų.</span><span class="sxs-lookup"><span data-stu-id="6e307-127">Several steps must be completed when you want to schedule and run a maintenance job on a work order.</span></span> <span data-ttu-id="6e307-128">Toliau pateiktame paveikslėlyje parodyta darbo užsakymo vykdymo apžvalga.</span><span class="sxs-lookup"><span data-stu-id="6e307-128">The following illustration shows an overview of the processing for a work order.</span></span>

![Diagrama, rodanti darbo užsakymo vykdymo apžvalgą](media/08-overview-image.png)

> [!NOTE]
> <span data-ttu-id="6e307-130">Kai dirbate programoje Dynamics 365 Supply Chain Management ir modulyje **Turto valdymas**, norėdami sukurti naują įrašą, pasirenkate **Naujas**, norėdami atnaujinti esamą įrašą, pasirenkate **Redaguoti** ir norėdami įrašyti naujus ar redaguotus duomenis, pasirenkate **Saugoti**.</span><span class="sxs-lookup"><span data-stu-id="6e307-130">In general, when you work in Dynamics 365 Supply Chain Management and the **Asset Management** module, you select **New** to create a new record, you select **Edit** to update an existing record, and you select **Save** to save new or edited data.</span></span>
