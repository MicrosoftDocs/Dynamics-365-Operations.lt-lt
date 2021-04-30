---
title: Susiekite parduotuves ir komandas, jeigu yra išankstinių komandų „Microsoft Teams” platformoje
description: Šioje temoje aprašoma, kaip susieti parduotuves ir atitinkamas komandas „Dynamics 365 Commerce” būstinėje, jei jūsų organizacija jau sukūrė komandas „Microsoft Teams” platformoje prieš integruojant „Commerce”.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a711c1057b87bd792755ef91a84d1c28879c590
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908500"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a><span data-ttu-id="627af-103">Susiekite parduotuves ir komandas, jeigu yra išankstinių komandų „Microsoft Teams” platformoje</span><span class="sxs-lookup"><span data-stu-id="627af-103">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="627af-104">Šioje temoje aprašoma, kaip susieti parduotuves ir atitinkamas komandas „Dynamics 365 Commerce” būstinėje, jei jūsų organizacija jau sukūrė komandas „Microsoft Teams” platformoje prieš integruojant „Commerce”.</span><span class="sxs-lookup"><span data-stu-id="627af-104">This topic covers how to map stores and corresponding teams in Dynamics 365 Commerce headquarters if your organization has already created teams in Microsoft Teams before Commerce integration.</span></span>

<span data-ttu-id="627af-105">Gali būti, jog jūsų organizacija sukūrė komandas kai kurioms arba visoms jūsų parduotuvėms dar prieš „Dynamics 365 Commerce” ir „Microsoft Teams” integravimą.</span><span class="sxs-lookup"><span data-stu-id="627af-105">Your organization may have teams created for some or all of your stores before integrating Dynamics 365 Commerce and Microsoft Teams.</span></span> <span data-ttu-id="627af-106">Tokiu atveju, norėdami nustatyti užduočių sinchronizavimą tarp „Commerce” EKA ir „Microsoft Teams”, turite susieti parduotuves ir atitinkamas komandas „Commerce” būstinėje.</span><span class="sxs-lookup"><span data-stu-id="627af-106">If this is the case, to establish task synchronization between Commerce POS and Microsoft Teams you must provide the mapping of stores and corresponding team in Commerce headquarters.</span></span>

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a><span data-ttu-id="627af-107">Parduotuvių ir atitinkamų komandų susiejimas „Commerce” būstinėje</span><span class="sxs-lookup"><span data-stu-id="627af-107">Map stores and corresponding teams in Commerce headquarters</span></span> 

<span data-ttu-id="627af-108">Norėdami susieti parduotuves ir atitinkamas komandas „Commerce” būstinėje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="627af-108">To map stores and corresponding teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="627af-109">Eikite į **Sistemos Administravimas \> Darbo sritis \> Duomenų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="627af-109">Go to **System Administration \> Workspace \> Data management**.</span></span>
1. <span data-ttu-id="627af-110">Pasirinkite **Eksportuoti**.</span><span class="sxs-lookup"><span data-stu-id="627af-110">Select **Export**.</span></span> 
1. <span data-ttu-id="627af-111">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="627af-111">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="627af-112">Dalyje **Grupės pavadinimas** įveskite „Eksportuoti „Teams” susiejimą”.</span><span class="sxs-lookup"><span data-stu-id="627af-112">Under **Group name**, enter "Export Teams mapping".</span></span>
1. <span data-ttu-id="627af-113">„FastTab” **Pasirinkti objektai** pasirinkite **Įtraukti objektą**.</span><span class="sxs-lookup"><span data-stu-id="627af-113">On the **Selected entities** FastTab, select **Add entity**.</span></span> <span data-ttu-id="627af-114">Atsiranda dialogo langas **Įtraukti objektą**.</span><span class="sxs-lookup"><span data-stu-id="627af-114">The **Add entity** dialog box appears.</span></span>  
1. <span data-ttu-id="627af-115">Išplečiamajame sąraše **Objekto pavadinimas** pasirinkite **„Teams” susiejimas tarp šaltinio ir komandos**.</span><span class="sxs-lookup"><span data-stu-id="627af-115">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="627af-116">Išplečiamajame sąraše **Paskirties duomenų formatas** pasirinkite **„CSV”**.</span><span class="sxs-lookup"><span data-stu-id="627af-116">In the **Target data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="627af-117">Pasirinkite **Įtraukti**, o tada pasirinkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="627af-117">Select **Add**, and then select **Close**.</span></span>
1. <span data-ttu-id="627af-118">Veiksmų srities viršutinėje kairėje pusėje, pasirinkite **Eksportuoti dabar**.</span><span class="sxs-lookup"><span data-stu-id="627af-118">On the top left under the Action Pane, select **Export now**.</span></span>
1. <span data-ttu-id="627af-119">Dalyje **Objekto apdorojimo būsena** pasirinkite **Atsisiųsti failą**.</span><span class="sxs-lookup"><span data-stu-id="627af-119">Under **Entity processing status**, select **Download file**.</span></span>
1. <span data-ttu-id="627af-120">Eksportuotame CSV failuose į laukus **ŠALTINIO TIPAS**, **ŠALTINIO ID** ir **KOMANDOS ID** įveskite tokias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="627af-120">In the exported CSV file, enter values for **SOURCETYPE**, **SOURCEID**, and **TEAMID** as follows:</span></span>
    - <span data-ttu-id="627af-121">Į **ŠALTINIO TIPAS** įveskite „Mažmeninės prekybos parduotuvė”.</span><span class="sxs-lookup"><span data-stu-id="627af-121">For **SOURCETYPE**, enter "RetailStore".</span></span> 
    - <span data-ttu-id="627af-122">Į **ŠALTINIO ID** įveskite parduotuvės numerį (pavyzdžiui, „000135” San Fransisko parduotuvei).</span><span class="sxs-lookup"><span data-stu-id="627af-122">For **SOURCEID**, enter the store number (for example, "000135" for the San Francisco store).</span></span> <span data-ttu-id="627af-123">Parduotuvių numerius galite rasti **Mažmeninė prekyba ir komercija \> Kanalai \> Parduotuvės**.</span><span class="sxs-lookup"><span data-stu-id="627af-123">You can find store numbers at **Retail and Commerce \> Channels \> Stores**.</span></span>
    - <span data-ttu-id="627af-124">Į **KOMANDOS ID** įveskite atitinkamos komandos ID iš „Microsoft Teams” (pavyzdžiui, „5f8bc92b-6aa8-451e-85d1-3949c01ddc6c”).</span><span class="sxs-lookup"><span data-stu-id="627af-124">For **TEAMID**, enter the corresponding team ID from Microsoft Teams (for example, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span></span> <span data-ttu-id="627af-125">Komandos ID informaciją galite rasti [svetainėje admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="627af-125">You can find team ID information at [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span></span>
1. <span data-ttu-id="627af-126">Įrašykite CSV failą į savo vietinį kompiuterį.</span><span class="sxs-lookup"><span data-stu-id="627af-126">Save the CSV file to your local machine.</span></span>
1. <span data-ttu-id="627af-127">Eikite į **Sistemos Administravimas \> Darbo sritis \> Duomenų valdymas**, o tada pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="627af-127">Go to **System Administration \> Workspace \> Data management**, and then select **Import**.</span></span>
1. <span data-ttu-id="627af-128">„FastTab” **Pasirinkti objektai** pasirinkite **Įtraukti failą**.</span><span class="sxs-lookup"><span data-stu-id="627af-128">On the **Selected entities** FastTab, select **Add file**.</span></span> <span data-ttu-id="627af-129">Atsiranda dialogo langas **Įtraukti failą**.</span><span class="sxs-lookup"><span data-stu-id="627af-129">The **Add file** dialog box appears.</span></span>
1. <span data-ttu-id="627af-130">Išplečiamajame sąraše **Objekto pavadinimas** pasirinkite **„Teams” susiejimas tarp šaltinio ir komandos**.</span><span class="sxs-lookup"><span data-stu-id="627af-130">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="627af-131">Išplečiamajame sąraše **Šaltinio duomenų formatas** pasirinkite **„CSV”**.</span><span class="sxs-lookup"><span data-stu-id="627af-131">In the **Source data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="627af-132">Pasirinkite **Įkelti ir įtraukti**, tada pasirinkite anksčiau įrašytą CSV failą ir **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="627af-132">Select **Upload and add**, select the CSV file that you saved previously, and then select **Open**.</span></span>
1. <span data-ttu-id="627af-133">Dialogo lange **Įtraukti failą** pasirinkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="627af-133">In the **Add file** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="627af-134">Veiksmų srityje pasirinkite **Įrašyti**, o tada pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="627af-134">On the Action Pane, select **Save** , and then select **Import**.</span></span>

<span data-ttu-id="627af-135">Šiame pavyzdyje rodoma „Commerce” esanti **Komandų susiejimo eksportavimo** grupė su **Įtraukti objektą** elementais ir išryškintomis CSV failo antraštėmis.</span><span class="sxs-lookup"><span data-stu-id="627af-135">The following example image shows the **Export teams mapping** group in Commerce with **Add entity** elements and the exported CSV file headers highlighted.</span></span>

![Komandų susiejimo eksportavimo grupė su objekto įtraukimo elementais ir išryškintomis CSV failo antraštėmis](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> <span data-ttu-id="627af-137">Atlikę ankstesnius veiksmus, atlikite skyriuje [Užduočių valdymo sinchronizavimas tarp „Microsoft Teams” ir EKA](synchronize-tasks-teams-pos.md) nurodytus veiksmus, jei norite sinchronizuoti užduočių valdymą.</span><span class="sxs-lookup"><span data-stu-id="627af-137">After you complete the preceeding steps, follow the steps in [Synchronize task management between Microsoft Teams and POS](synchronize-tasks-teams-pos.md) to synchronize task management.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="627af-138">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="627af-138">Additional resources</span></span>

[<span data-ttu-id="627af-139">„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="627af-139">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="627af-140">„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo įgalinimas</span><span class="sxs-lookup"><span data-stu-id="627af-140">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="627af-141">„Microsoft Teams” parengimas iš „Dynamics 365 Commerce”</span><span class="sxs-lookup"><span data-stu-id="627af-141">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="627af-142">Užduočių valdymo sinchronizavimas tarp „Microsoft Teams” ir „Dynamics 365 Commerce” EKA</span><span class="sxs-lookup"><span data-stu-id="627af-142">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="627af-143">Vartotojų vaidmenų tvarkymas Microsoft Teams” platformoje</span><span class="sxs-lookup"><span data-stu-id="627af-143">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="627af-144">„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo DUK</span><span class="sxs-lookup"><span data-stu-id="627af-144">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
