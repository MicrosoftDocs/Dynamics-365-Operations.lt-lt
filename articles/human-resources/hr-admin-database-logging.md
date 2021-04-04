---
title: Duomenų bazės registravimo konfigūravimas ir valdymas
description: Galite sekti lentelių ir laukų pakeitimus „Dynamics 365 Human Resources” naudodami duomenų bazės registravimą.
author: andreabichsel
manager: tfehr
ms.date: 06/10/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8057ebd0bc061c6bf78d8674c45e0885ffce681c
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467654"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="224ad-103">Duomenų bazės registravimo konfigūravimas ir valdymas</span><span class="sxs-lookup"><span data-stu-id="224ad-103">Configure and manage database logging</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="224ad-104">Galite sekti lentelių ir laukų pakeitimus „Dynamics 365 Human Resources” naudodami duomenų bazės registravimą.</span><span class="sxs-lookup"><span data-stu-id="224ad-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="224ad-105">Šioje temoje aprašoma, kaip:</span><span class="sxs-lookup"><span data-stu-id="224ad-105">This topic describes how to:</span></span>

- <span data-ttu-id="224ad-106">Tvarkyti duomenų bazės registravimo saugą ir efektyvumą</span><span class="sxs-lookup"><span data-stu-id="224ad-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="224ad-107">Nustatyti duomenų bazės registravimą</span><span class="sxs-lookup"><span data-stu-id="224ad-107">Set up database logging</span></span>
- <span data-ttu-id="224ad-108">Valyti duomenų bazės žurnalus</span><span class="sxs-lookup"><span data-stu-id="224ad-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="224ad-109">Duomenų bazės registravimo peržiūrą</span><span class="sxs-lookup"><span data-stu-id="224ad-109">Overview of database logging</span></span>

<span data-ttu-id="224ad-110">Duomenų bazės registravimo funkcija stebi „Microsoft Dynamics 365 Human Resources” lentelių ir laukų pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="224ad-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="224ad-111">Šie pakeitimai apima įterpimo, atnaujinimo arba naikinimo veiksmus.</span><span class="sxs-lookup"><span data-stu-id="224ad-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="224ad-112">Duomenų bazės registravimas išsaugo lentelių arba laukų, esančių duomenų bazės žurnalo lentelėje, keitimų įrašą.</span><span class="sxs-lookup"><span data-stu-id="224ad-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="224ad-113">Verslas duomenų bazės registravimą naudoja šiais tikslais:</span><span class="sxs-lookup"><span data-stu-id="224ad-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="224ad-114">Kurti konkrečių lentelių, kuriose yra slaptos informacijos, keitimų audito įrašą.</span><span class="sxs-lookup"><span data-stu-id="224ad-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="224ad-115">Sekti vienkartines operacijas.</span><span class="sxs-lookup"><span data-stu-id="224ad-115">Tracking single transactions.</span></span> <span data-ttu-id="224ad-116">Duomenų bazės registravimas nėra skirtas automatinėms operacijoms, paleidžiamoms paketinėse užduotyse.</span><span class="sxs-lookup"><span data-stu-id="224ad-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="224ad-117">Duomenų bazės registravimo sauga</span><span class="sxs-lookup"><span data-stu-id="224ad-117">Security for database logging</span></span>

<span data-ttu-id="224ad-118">Duomenų bazės žurnaluose gali būti slaptų duomenų.</span><span class="sxs-lookup"><span data-stu-id="224ad-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="224ad-119">Riboti prieigą, kad būtų galima naudoti tik tuos saugos vaidmenis, kuriems reikalinga prieiga prie žurnalo duomenų.</span><span class="sxs-lookup"><span data-stu-id="224ad-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="224ad-120">Duomenų bazės registravimas ir našumas</span><span class="sxs-lookup"><span data-stu-id="224ad-120">Database logging and performance</span></span>

<span data-ttu-id="224ad-121">Nors verslo perspektyva yra vertingas, duomenų bazės registravimas gali būti brangus išteklių naudojimo ir valdymo srityje.</span><span class="sxs-lookup"><span data-stu-id="224ad-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="224ad-122">Duomenų bazės registravimą galima naudoti šiais tikslais:</span><span class="sxs-lookup"><span data-stu-id="224ad-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="224ad-123">Duomenų bazės žurnalo lentelė gali greitai plėstis ir padidinti duomenų bazės dydį.</span><span class="sxs-lookup"><span data-stu-id="224ad-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="224ad-124">Augimas priklauso nuo užregistruotų duomenų kiekio, kurį nusprendėte saugoti.</span><span class="sxs-lookup"><span data-stu-id="224ad-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="224ad-125">Pagal numatytuosius nustatymus, duomenų bazės žurnalo lentelėje palaikomi tik 30 dienų žurnalo duomenys.</span><span class="sxs-lookup"><span data-stu-id="224ad-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="224ad-126">Duomenų bazės registravimas gali neigiamai paveikti ilgai trunkančius automatinius procesus, pvz., ilgai trunkančius duomenų importavimus.</span><span class="sxs-lookup"><span data-stu-id="224ad-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="224ad-127">Geriausia praktika</span><span class="sxs-lookup"><span data-stu-id="224ad-127">Best practices</span></span>

<span data-ttu-id="224ad-128">Norėdami padidinti našumą, apribokite žurnalo įrašus pasirinkdami konkrečius laukus registruoti, o ne ištisas lenteles.</span><span class="sxs-lookup"><span data-stu-id="224ad-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="224ad-129">Norint palaikyti bendrą našumą, duomenų bazės registravimas apribotas 20 lentelių.</span><span class="sxs-lookup"><span data-stu-id="224ad-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="224ad-130">Tik naujinimai gali būti registruojami atskiruose laukuose.</span><span class="sxs-lookup"><span data-stu-id="224ad-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="224ad-131">Nustatyti duomenų bazės registravimą</span><span class="sxs-lookup"><span data-stu-id="224ad-131">Set up database logging</span></span>

<span data-ttu-id="224ad-132">Galite naudoti **Duomenų bazės pakeitimų registravimas** vedlį, kad nustatytumėte duomenų bazės registravimą.</span><span class="sxs-lookup"><span data-stu-id="224ad-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="224ad-133">Vedlys suteikia lanksčią galimybę nustatyti lentelių arba laukų registravimą.</span><span class="sxs-lookup"><span data-stu-id="224ad-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="224ad-134">Eikite į **Sistemos administravimas > Saitai > Duomenų bazė > Duomenų bazės žurnalo nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="224ad-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="224ad-135">Pasirinkite **Nauja**, kad įjungtumėte **Registravimo duomenų bazės pakeitimai** vedlį.</span><span class="sxs-lookup"><span data-stu-id="224ad-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="224ad-136">Baikite vykdyti vedlio žingsnius.</span><span class="sxs-lookup"><span data-stu-id="224ad-136">Complete the wizard.</span></span>

## <a name="clean-up-database-logs"></a><span data-ttu-id="224ad-137">Valyti duomenų bazės žurnalus</span><span class="sxs-lookup"><span data-stu-id="224ad-137">Clean up database logs</span></span>

<span data-ttu-id="224ad-138">Galite naikinti dalį arba visus duomenų bazės žurnalus naudodami šias parinktis:</span><span class="sxs-lookup"><span data-stu-id="224ad-138">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="224ad-139">Pasirinkite konkrečios lentelės visus žurnalus.</span><span class="sxs-lookup"><span data-stu-id="224ad-139">Select all logs for a particular table.</span></span>
- <span data-ttu-id="224ad-140">Pasirinkite konkrečius duomenų bazės žurnalo tipus.</span><span class="sxs-lookup"><span data-stu-id="224ad-140">Select specific types of database log.</span></span>
- <span data-ttu-id="224ad-141">Pasirinkite datą ir laiką, kada buvo sukurtas žurnalas.</span><span class="sxs-lookup"><span data-stu-id="224ad-141">Select a date and time that a log was created.</span></span>

<span data-ttu-id="224ad-142">Norėdami nustatyti duomenų bazės žurnalo valymą, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="224ad-142">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="224ad-143">Eikite į **Sistemos administravimas > Saitai > Duomenų bazė > Duomenų bazės žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="224ad-143">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="224ad-144">Pasirinkite **Valyti žurnalą**.</span><span class="sxs-lookup"><span data-stu-id="224ad-144">Select **Clean up log**.</span></span>

2. <span data-ttu-id="224ad-145">Pasirinkite žurnalų, kuriuos reikia panaikinti, pasirinkimo būdą įvesdami vieną iš šių pasirinkčių:</span><span class="sxs-lookup"><span data-stu-id="224ad-145">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="224ad-146">Lentelės ID</span><span class="sxs-lookup"><span data-stu-id="224ad-146">Table ID</span></span>
   - <span data-ttu-id="224ad-147">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="224ad-147">Type of log</span></span>
   - <span data-ttu-id="224ad-148">Sukūrimo data ir laikas</span><span class="sxs-lookup"><span data-stu-id="224ad-148">Created date and time</span></span>

3. <span data-ttu-id="224ad-149">Naudokite **Duomenų bazės žurnalo valymas** skirtuką, kad nustatytumėte, kada paleisti žurnalo valymo užduotį.</span><span class="sxs-lookup"><span data-stu-id="224ad-149">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="224ad-150">Pagal numatytuosius nustatymus, duomenų bazės žurnalai prieinami 30 dienų.</span><span class="sxs-lookup"><span data-stu-id="224ad-150">By default, database logs are available for 30 days.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]