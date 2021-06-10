---
title: Duomenų bazės registravimo konfigūravimas ir valdymas
description: Galite sekti lentelių ir laukų pakeitimus „Dynamics 365 Human Resources” naudodami duomenų bazės registravimą.
author: andreabichsel
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae974436469c00a3df6fd40d9d60521a0883a917
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054817"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="0eb6d-103">Duomenų bazės registravimo konfigūravimas ir valdymas</span><span class="sxs-lookup"><span data-stu-id="0eb6d-103">Configure and manage database logging</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0eb6d-104">Galite sekti lentelių ir laukų pakeitimus „Dynamics 365 Human Resources” naudodami duomenų bazės registravimą.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="0eb6d-105">Šioje temoje aprašoma, kaip:</span><span class="sxs-lookup"><span data-stu-id="0eb6d-105">This topic describes how to:</span></span>

- <span data-ttu-id="0eb6d-106">Tvarkyti duomenų bazės registravimo saugą ir efektyvumą</span><span class="sxs-lookup"><span data-stu-id="0eb6d-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="0eb6d-107">Nustatyti duomenų bazės registravimą</span><span class="sxs-lookup"><span data-stu-id="0eb6d-107">Set up database logging</span></span>
- <span data-ttu-id="0eb6d-108">Valyti duomenų bazės žurnalus</span><span class="sxs-lookup"><span data-stu-id="0eb6d-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="0eb6d-109">Duomenų bazės registravimo peržiūrą</span><span class="sxs-lookup"><span data-stu-id="0eb6d-109">Overview of database logging</span></span>

<span data-ttu-id="0eb6d-110">Duomenų bazės registravimo funkcija stebi „Microsoft Dynamics 365 Human Resources” lentelių ir laukų pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="0eb6d-111">Šie pakeitimai apima įterpimo, atnaujinimo arba naikinimo veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="0eb6d-112">Duomenų bazės registravimas išsaugo lentelių arba laukų, esančių duomenų bazės žurnalo lentelėje, keitimų įrašą.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="0eb6d-113">Verslas duomenų bazės registravimą naudoja šiais tikslais:</span><span class="sxs-lookup"><span data-stu-id="0eb6d-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="0eb6d-114">Kurti konkrečių lentelių, kuriose yra slaptos informacijos, keitimų audito įrašą.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="0eb6d-115">Sekti vienkartines operacijas.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-115">Tracking single transactions.</span></span> <span data-ttu-id="0eb6d-116">Duomenų bazės registravimas nėra skirtas automatinėms operacijoms, paleidžiamoms paketinėse užduotyse.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="0eb6d-117">Duomenų bazės registravimo sauga</span><span class="sxs-lookup"><span data-stu-id="0eb6d-117">Security for database logging</span></span>

<span data-ttu-id="0eb6d-118">Duomenų bazės žurnaluose gali būti slaptų duomenų.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="0eb6d-119">Riboti prieigą, kad būtų galima naudoti tik tuos saugos vaidmenis, kuriems reikalinga prieiga prie žurnalo duomenų.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="0eb6d-120">Duomenų bazės registravimas ir našumas</span><span class="sxs-lookup"><span data-stu-id="0eb6d-120">Database logging and performance</span></span>

<span data-ttu-id="0eb6d-121">Nors verslo perspektyva yra vertingas, duomenų bazės registravimas gali būti brangus išteklių naudojimo ir valdymo srityje.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="0eb6d-122">Duomenų bazės registravimą galima naudoti šiais tikslais:</span><span class="sxs-lookup"><span data-stu-id="0eb6d-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="0eb6d-123">Duomenų bazės žurnalo lentelė gali greitai plėstis ir padidinti duomenų bazės dydį.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="0eb6d-124">Augimas priklauso nuo užregistruotų duomenų kiekio, kurį nusprendėte saugoti.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="0eb6d-125">Pagal numatytuosius nustatymus, duomenų bazės žurnalo lentelėje palaikomi tik 30 dienų žurnalo duomenys.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="0eb6d-126">Duomenų bazės registravimas gali neigiamai paveikti ilgai trunkančius automatinius procesus, pvz., ilgai trunkančius duomenų importavimus.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="0eb6d-127">Geriausia praktika</span><span class="sxs-lookup"><span data-stu-id="0eb6d-127">Best practices</span></span>

<span data-ttu-id="0eb6d-128">Norėdami padidinti našumą, apribokite žurnalo įrašus pasirinkdami konkrečius laukus registruoti, o ne ištisas lenteles.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="0eb6d-129">Norint palaikyti bendrą našumą, duomenų bazės registravimas apribotas 20 lentelių.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="0eb6d-130">Tik naujinimai gali būti registruojami atskiruose laukuose.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="0eb6d-131">Nustatyti duomenų bazės registravimą</span><span class="sxs-lookup"><span data-stu-id="0eb6d-131">Set up database logging</span></span>

<span data-ttu-id="0eb6d-132">Galite naudoti **Duomenų bazės pakeitimų registravimas** vedlį, kad nustatytumėte duomenų bazės registravimą.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="0eb6d-133">Vedlys suteikia lanksčią galimybę nustatyti lentelių arba laukų registravimą.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="0eb6d-134">Eikite į **Sistemos administravimas > Saitai > Duomenų bazė > Duomenų bazės žurnalo nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="0eb6d-135">Pasirinkite **Nauja**, kad įjungtumėte **Registravimo duomenų bazės pakeitimai** vedlį.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="0eb6d-136">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-136">Select **Next**.</span></span> 
3. <span data-ttu-id="0eb6d-137">Vedlio puslapyje Lentelės ir laukai pasirinkite lenteles ir laukus, kuriuose norite įgalinti duomenų **bazės** registravimą, ir pasirinkite **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-137">On the **Tables and fields** page of the wizard, select the the tables and fields on which you want to enable database logging, and select **Next**.</span></span>

   > [!Note]
   > <span data-ttu-id="0eb6d-138">Duomenų bazės registravimas negalimas visose Personalo duomenų bazės lentelėse.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-138">Database logging is not available on all tables in the Human Resources database.</span></span> <span data-ttu-id="0eb6d-139">Pasirinkus Rodyti visas lenteles sąraše išplečiamas lentelių ir laukų sąrašas, kad būtų parodytos visos duomenų bazės lentelės, kuriose galimas duomenų bazės registravimas, bet tai bus viso duomenų bazių lentelių sąrašo **subrinkinyje**.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-139">Selecting **Show all tables** below the list expands the list of tables and fields to show all database tables for which database logging is available, but this will be a subset of the full list of database tables.</span></span>

4. <span data-ttu-id="0eb6d-140">Vedlio pakeitimų tipų puslapyje pasirinkite duomenų operacijas, kurių kiekvienos lentelės ir laukų keitimus norite sekti, ir **pasirinkite** **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-140">On the **Types of change** page of the wizard, select the data operations for which you want to track changes for each of the tables and fields, and select **Next**.</span></span> <span data-ttu-id="0eb6d-141">Informacijos apie duomenų operacijas, kurias galima registruoti, ieškokite toliau esančioje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-141">See the table below for a description of the data operations that are available for logging.</span></span>
5. <span data-ttu-id="0eb6d-142">Puslapyje **Baigti** peržiūrėkite atliktus keitimus ir pasirinkite **Baigti**.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-142">On the **Finish** page, review the changes that will be made, and select **Finish**.</span></span>

| <span data-ttu-id="0eb6d-143">Operacija</span><span class="sxs-lookup"><span data-stu-id="0eb6d-143">Operation</span></span> | <span data-ttu-id="0eb6d-144">Aprašas</span><span class="sxs-lookup"><span data-stu-id="0eb6d-144">Description</span></span> |
| -- | -- |
| <span data-ttu-id="0eb6d-145">Sekti naujas operacijas</span><span class="sxs-lookup"><span data-stu-id="0eb6d-145">Track new transactions</span></span> | <span data-ttu-id="0eb6d-146">Kurti naujų lentelėje sukurtų įrašų žurnalą.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-146">Create a log for new records that are created in the table.</span></span> |
| <span data-ttu-id="0eb6d-147">Atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="0eb6d-147">Update</span></span> | <span data-ttu-id="0eb6d-148">Kurti lentelių įrašų naujinimų žurnalą arba atnaujinimų į atskirai pasirinktus lentelės laukus žurnalą.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-148">Create a log for updates to table records, or updates to individually selected fields in the table.</span></span> <span data-ttu-id="0eb6d-149">Jei pasirenkate registruoti lentelės atnaujinimus, žurnalo įrašas sukuriamas kiekvieną kartą, kai atnaujinamas bet kurio lentelės įrašo laukas.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-149">If you select to log updates for the table, then a log record is created each time an update is made to any field of any record on the table.</span></span> <span data-ttu-id="0eb6d-150">Jei pasirenkate registruoti tam tikrų laukų atnaujinimus, žurnalo įrašas sukuriamas tik tų lentelės įrašų laukų atnaujinimų metu.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-150">If you select to log updates for specific fields, then a log record is created only when updates are made to those fields of table records.</span></span> |
| <span data-ttu-id="0eb6d-151">Panaikinti</span><span class="sxs-lookup"><span data-stu-id="0eb6d-151">Delete</span></span> | <span data-ttu-id="0eb6d-152">Kurti iš lentelės panaikintų įrašų žurnalą.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-152">Create a log for records deleted from the table.</span></span> |
| <span data-ttu-id="0eb6d-153">Pervadinti raktą</span><span class="sxs-lookup"><span data-stu-id="0eb6d-153">Rename key</span></span> | <span data-ttu-id="0eb6d-154">Pervardijus lentelės raktą, sukurti žurnalo įrašą.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-154">Create a log record when a table key is renamed.</span></span> |


## <a name="clean-up-database-logs"></a><span data-ttu-id="0eb6d-155">Valyti duomenų bazės žurnalus</span><span class="sxs-lookup"><span data-stu-id="0eb6d-155">Clean up database logs</span></span>

<span data-ttu-id="0eb6d-156">Galite naikinti dalį arba visus duomenų bazės žurnalus naudodami šias parinktis:</span><span class="sxs-lookup"><span data-stu-id="0eb6d-156">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="0eb6d-157">Pasirinkite konkrečios lentelės visus žurnalus.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-157">Select all logs for a particular table.</span></span>
- <span data-ttu-id="0eb6d-158">Pasirinkite konkrečius duomenų bazės žurnalo tipus.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-158">Select specific types of database log.</span></span>
- <span data-ttu-id="0eb6d-159">Pasirinkite datą ir laiką, kada buvo sukurtas žurnalas.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-159">Select a date and time that a log was created.</span></span>

<span data-ttu-id="0eb6d-160">Norėdami nustatyti duomenų bazės žurnalo valymą, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="0eb6d-160">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="0eb6d-161">Eikite į **Sistemos administravimas > Saitai > Duomenų bazė > Duomenų bazės žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-161">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="0eb6d-162">Pasirinkite **Valyti žurnalą**.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-162">Select **Clean up log**.</span></span>

2. <span data-ttu-id="0eb6d-163">Pasirinkite žurnalų, kuriuos reikia panaikinti, pasirinkimo būdą įvesdami vieną iš šių pasirinkčių:</span><span class="sxs-lookup"><span data-stu-id="0eb6d-163">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="0eb6d-164">Lentelės ID</span><span class="sxs-lookup"><span data-stu-id="0eb6d-164">Table ID</span></span>
   - <span data-ttu-id="0eb6d-165">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="0eb6d-165">Type of log</span></span>
   - <span data-ttu-id="0eb6d-166">Sukūrimo data ir laikas</span><span class="sxs-lookup"><span data-stu-id="0eb6d-166">Created date and time</span></span>

3. <span data-ttu-id="0eb6d-167">Naudokite **Duomenų bazės žurnalo valymas** skirtuką, kad nustatytumėte, kada paleisti žurnalo valymo užduotį.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-167">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="0eb6d-168">Pagal numatytuosius nustatymus, duomenų bazės žurnalai prieinami 30 dienų.</span><span class="sxs-lookup"><span data-stu-id="0eb6d-168">By default, database logs are available for 30 days.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
