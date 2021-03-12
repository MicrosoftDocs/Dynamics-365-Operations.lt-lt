---
title: Užduočių valdymo konfigūravimas
description: Šioje temoje aprašoma, kaip konfigūruoti užduočių valdymo funkcijas programoje „Microsoft Dynamics 365 Commerce”.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: e880305d02fd9f10464fe3f65a2774a44da258c6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006240"
---
# <a name="configure-task-management"></a><span data-ttu-id="cbb1f-103">Užduočių valdymo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="cbb1f-103">Configure task management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cbb1f-104">Šioje temoje aprašoma, kaip konfigūruoti užduočių valdymo funkcijas programoje „Microsoft Dynamics 365 Commerce”.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-104">This topic describes how to configure task management features in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cbb1f-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="cbb1f-105">Overview</span></span>

<span data-ttu-id="cbb1f-106">Prieš „Dynamics 365 Commerce” vadybininkams ir darbuotojams pradedant naudotis „Commerce“ užduočių valdymo funkcijomis, reikia sukonfigūruoti užduočių valdymą.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-106">Before Dynamics 365 Commerce managers and employees can use the task management features in Commerce, task management must be configured.</span></span> <span data-ttu-id="cbb1f-107">Konfigūruojant atliekami tokie veiksmai: teisių suteikimas vadybininkams ir darbuotojams, teisių paskirstymas elektroninio kasos aparato (EKA) klientams, EKA pranešimų nustatymas ir plytelės **Užduotys** konfigūravimas EKA programos pagrindiniame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-107">Configuration steps include granting permissions to managers and employees, distributing permissions to point of sale (POS) clients, setting up POS notifications, and configuring the **Tasks** tile on the home page of a POS application.</span></span>

## <a name="configure-permissions-for-store-managers"></a><span data-ttu-id="cbb1f-108">Parduotuvių vadybininkų teisių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="cbb1f-108">Configure permissions for store managers</span></span>

<span data-ttu-id="cbb1f-109">Kiekvienas konkrečioje parduotuvėje dirbantis darbuotojas gali peržiūrėti visas šiai parduotuvei priskirtas užduotis.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-109">Every worker in a given store can view all tasks that are assigned to that store.</span></span> <span data-ttu-id="cbb1f-110">Jis taip pat gali naujinti jam priskirtų užduočių būsenas.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-110">They can also update the status of the tasks that are assigned to them.</span></span> <span data-ttu-id="cbb1f-111">Tačiau tokie asmenys, kaip parduotuvės vadybininkai, privalo turėti užduočių valdymo teises, kad galėtų valdyti parduotuvei priskirtas užduotis ir kurti vienos paskirties užduotis.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-111">However, personas such as store managers must have task management permissions to manage tasks that are assigned to the store and to create single-purpose tasks.</span></span>

<span data-ttu-id="cbb1f-112">Norėdami konfigūruoti parduotuvių vadybininkų užduočių valdymo teises, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-112">To configure task management permissions for store managers, follow these steps.</span></span>

1. <span data-ttu-id="cbb1f-113">Eikite į **Mažmeninė prekyba ir prekyba \> Darbuotojai \> Teisių grupės**.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-113">Go to **Retail and Commerce \> Employees \> Permission groups**.</span></span>
1. <span data-ttu-id="cbb1f-114">Pasirinkite konkrečią teisių grupę (pvz., **Vadybininkas**), tada pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-114">Select a specific permission group (for example, **Manager**), and then select **Edit**.</span></span>
1. <span data-ttu-id="cbb1f-115">„FastTab“ skirtuke **Teisės** parinktyje **Leisti užduočių valdymą** nustatykite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-115">On the **Permissions** FastTab, set the **Allow task management** option to **Yes**.</span></span>
1. <span data-ttu-id="cbb1f-116">„FastTab“ skirtuke **Pranešimai** įtraukite operaciją **Užduočių valdymas** ir lauke **Rodyti užsakymą** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-116">On the **Notifications** FastTab, add the **Task management** operation, and enter a value in the **Display order** field.</span></span> <span data-ttu-id="cbb1f-117">Pavyzdžiui, įveskite **2**, jei operacijoje **Užsakymo įvykdymas** jau yra lauko **Rodyti užsakymą** reikšmė **1**.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-117">For example, enter **2** if the **Order fulfillment** operation already has a **Display order** value of **1**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="cbb1f-118">Jei ne vadybininkai privalo turėti EKA užduočių valdymo teisių, galite suteikti teisę atskiram asmeniui.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-118">If a non-manager persona must have task management permissions in the POS, you can grant permission to the individual.</span></span> <span data-ttu-id="cbb1f-119">Arba galite sukurti naują ne vadybininkams skirtą leidimų grupę ir parinktyje **Leisti užduočių valdymą** nustatyti **Taip**.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-119">Alternatively, you can create a new permission group for non-managers and set the **Allow task management** option to **Yes**.</span></span>

<span data-ttu-id="cbb1f-120">Toliau pateiktame paveikslėlyje vaizduojama, kaip konfigūruoti parduotuvių vadybininkų užduočių valdymo teises.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-120">The following illustration shows how to configure task management permissions for store managers.</span></span>

![Parduotuvių vadybininkų užduočių valdymo teisių konfigūravimas](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a><span data-ttu-id="cbb1f-122">Darbuotojų teisių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="cbb1f-122">Configure permissions for employees</span></span>

<span data-ttu-id="cbb1f-123">Darbuotojai privalo turėti teises, kad galėtų kurti užduočių sąrašus, valdyti priskyrimo kriterijus ir konfigūruoti užduočių sąrašo pasikartojimą.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-123">Employees must have permissions to create task lists, manage assignment criteria, and configure the recurrence of any task list.</span></span> <span data-ttu-id="cbb1f-124">Norėdami konfigūruoti šias teises, turite priskirti darbuotojams vaidmenį **Mažmeninės prekybos užduočių vadovas**.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-124">To configure these permissions, you assign employees to the **Retail task manager** role.</span></span>

<span data-ttu-id="cbb1f-125">Norėdami konfigūruoti darbuotojo teises, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-125">To configure permissions for an employee, follow these steps.</span></span>

1. <span data-ttu-id="cbb1f-126">Eikite į **Mažmeninė prekyba ir prekyba \> Darbuotojai \> Vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-126">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="cbb1f-127">Pasirinkite darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-127">Select an employee.</span></span>
1. <span data-ttu-id="cbb1f-128">„FastTab“ skirtuke **Vartotojo vaidmenys** pasirinkite **Priskirti vaidmenis**.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-128">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="cbb1f-129">Dialogo lange **Priskirti vaidmenis vartotojui** pasirinkite vaidmenį **Mažmeninės prekybos užduočių vadovas**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-129">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

## <a name="distribute-permissions-to-pos-clients"></a><span data-ttu-id="cbb1f-130">Teisių EKA klientams paskirstymas</span><span class="sxs-lookup"><span data-stu-id="cbb1f-130">Distribute permissions to POS clients</span></span>

<span data-ttu-id="cbb1f-131">Prieš darbuotojams pradedant naudotis EKA klientais, šių klientų teisės turi būti paskirstytos ir sinchronizuotos.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-131">Before employees can use POS clients, permissions must be distributed and synced to those clients.</span></span>

<span data-ttu-id="cbb1f-132">Norėdami paskirstyti teises EKA klientams, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-132">To distribute permissions to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="cbb1f-133">Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-133">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="cbb1f-134">Pasirinkite paskirstymo grafiką **1060** (**Darbuotojai**), tada pasirinkite **Vykdyti dabar**.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-134">Select the **1060** (**Staff**) distribution schedule, and then select **Run now**.</span></span>
1. <span data-ttu-id="cbb1f-135">Pasirinkite paskirstymo grafiką **1070** (**Kanalo konfigūracija**), tada pasirinkite **Vykdyti dabar**.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-135">Select the **1070** (**Channel configuration**) distribution schedule, and then select **Run now**.</span></span>

## <a name="configure-pos-notifications-for-tasks"></a><span data-ttu-id="cbb1f-136">Užduotims skirtų EKA pranešimų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="cbb1f-136">Configure POS notifications for tasks</span></span>

<span data-ttu-id="cbb1f-137">Užduočių valdymas turi būti sukonfigūruotas taip, kad pranešimai būtų pasiekiami EKA programoje.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-137">Task management must be configured so that notifications are available in the POS application.</span></span>

<span data-ttu-id="cbb1f-138">Norėdami konfigūruoti EKA pranešimus užduotims, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-138">To configure POS notifications for tasks, follow these steps.</span></span>

1. <span data-ttu-id="cbb1f-139">Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA \> EKA operacijos**.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-139">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="cbb1f-140">Raskite operaciją **1400** (**Užduočių valdymas**) ir pažymėkite žymės langelį **Įjungti pranešimus**.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-140">Find operation **1400** (**Task management**), and select the **Enable notifications** check box for it.</span></span>

<span data-ttu-id="cbb1f-141">Toliau pateiktame paveikslėlyje rodoma operacija **Užduočių valdymas** puslapyje **EKA operacijos**.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-141">The following illustration shows the **Task management** operation on the **POS operations** page.</span></span>

![Užduočių valdymo operacija EKA operacijų puslapyje](media/HQ-POS-Tasks-Notifications.png)

<span data-ttu-id="cbb1f-143">Daugiau informacijos apie tai, kaip sukonfigūruoti EKA pranešimus, žr. [Rodyti užsakymų pranešimus elektroniniame kasos aparate (EKA)](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="cbb1f-143">For more information about how to configure POS notifications, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a><span data-ttu-id="cbb1f-144">Plytelės Užduotys EKA programos pagrindiniame puslapyje konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="cbb1f-144">Configure the Tasks tile on a POS application home page</span></span>

<span data-ttu-id="cbb1f-145">Prieš konfigūruodami plytelę **Užduotys** EKA programos pagrindiniame puslapyje, žr. [Elektroninio kasos aparato (EKA) ekrano maketai](pos-screen-layouts.md), kad sužinotumėte, kaip konfigūruoti ir įtraukti naujų mygtukų į EKA ekrano maketą.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-145">Before you configure the **Tasks** tile on the home page of a POS application, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information about how to configure and add new buttons to a POS screen layout.</span></span>

<span data-ttu-id="cbb1f-146">Norėdami konfigūruoti plytelę **Užduotys** EKA programos pagrindiniame puslapyje, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-146">To configure the **Tasks** tile on a POS application home page, follow these steps.</span></span>

1. <span data-ttu-id="cbb1f-147">Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA \> Ekrano maketai**.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-147">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
1. <span data-ttu-id="cbb1f-148">Pasirinkite ekrano maketą, maketo dydį ir mygtukyną.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-148">Select a screen layout, select a layout size, and select a button grid.</span></span>
1. <span data-ttu-id="cbb1f-149">„FastTab“ skirtuke **Mygtukynas** pasirinkite **Dizaineris**, kad redaguotumėte pasirinktą mygtukyną.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-149">On the **Button grids** FastTab, select **Designer** to edit the selected button grid.</span></span>
1. <span data-ttu-id="cbb1f-150">Įtraukite plytelę **Užduotys** į atitinkamą pagrindinio ekrano skyrių.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-150">Add a **Tasks** tile to the appropriate section of the home page.</span></span>

<span data-ttu-id="cbb1f-151">Toliau pateikiamoje iliustracijoje rodomas plytelės **Užduotys** EKA pagrindiniame puslapyje pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="cbb1f-151">The following illustration shows an example of a **Tasks** tile on a POS home page.</span></span>

![Plytelė Užduotys EKA pagrindiniame puslapyje](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a><span data-ttu-id="cbb1f-153">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="cbb1f-153">Additional resources</span></span>

[<span data-ttu-id="cbb1f-154">Užduočių valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="cbb1f-154">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="cbb1f-155">Užduočių sąrašų kūrimas ir užduočių įtraukimas</span><span class="sxs-lookup"><span data-stu-id="cbb1f-155">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="cbb1f-156">Užduočių sąrašų priskyrimas parduotuvėms arba darbuotojams</span><span class="sxs-lookup"><span data-stu-id="cbb1f-156">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="cbb1f-157">Užduočių valdymas EKA programoje</span><span class="sxs-lookup"><span data-stu-id="cbb1f-157">Task management in POS</span></span>](task-mgmt-POS.md)
