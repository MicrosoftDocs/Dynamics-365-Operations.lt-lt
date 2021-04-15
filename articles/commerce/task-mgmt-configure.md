---
title: Užduočių valdymo konfigūravimas
description: Šioje temoje aprašoma, kaip konfigūruoti užduočių valdymo funkcijas programoje „Microsoft Dynamics 365 Commerce”.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 742d49b1b7b46952d0a8bb6c8a33cde2a35d124f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791707"
---
# <a name="configure-task-management"></a><span data-ttu-id="1f9e2-103">Užduočių valdymo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="1f9e2-103">Configure task management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1f9e2-104">Šioje temoje aprašoma, kaip konfigūruoti užduočių valdymo funkcijas programoje „Microsoft Dynamics 365 Commerce”.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-104">This topic describes how to configure task management features in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1f9e2-105">Prieš „Dynamics 365 Commerce” vadybininkams ir darbuotojams pradedant naudotis „Commerce“ užduočių valdymo funkcijomis, reikia sukonfigūruoti užduočių valdymą.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-105">Before Dynamics 365 Commerce managers and employees can use the task management features in Commerce, task management must be configured.</span></span> <span data-ttu-id="1f9e2-106">Konfigūruojant atliekami tokie veiksmai: teisių suteikimas vadybininkams ir darbuotojams, teisių paskirstymas elektroninio kasos aparato (EKA) klientams, EKA pranešimų nustatymas ir plytelės **Užduotys** konfigūravimas EKA programos pagrindiniame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-106">Configuration steps include granting permissions to managers and employees, distributing permissions to point of sale (POS) clients, setting up POS notifications, and configuring the **Tasks** tile on the home page of a POS application.</span></span>

## <a name="configure-permissions-for-store-managers"></a><span data-ttu-id="1f9e2-107">Parduotuvių vadybininkų teisių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="1f9e2-107">Configure permissions for store managers</span></span>

<span data-ttu-id="1f9e2-108">Kiekvienas konkrečioje parduotuvėje dirbantis darbuotojas gali peržiūrėti visas šiai parduotuvei priskirtas užduotis.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-108">Every worker in a given store can view all tasks that are assigned to that store.</span></span> <span data-ttu-id="1f9e2-109">Jis taip pat gali naujinti jam priskirtų užduočių būsenas.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-109">They can also update the status of the tasks that are assigned to them.</span></span> <span data-ttu-id="1f9e2-110">Tačiau tokie asmenys, kaip parduotuvės vadybininkai, privalo turėti užduočių valdymo teises, kad galėtų valdyti parduotuvei priskirtas užduotis ir kurti vienos paskirties užduotis.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-110">However, personas such as store managers must have task management permissions to manage tasks that are assigned to the store and to create single-purpose tasks.</span></span>

<span data-ttu-id="1f9e2-111">Norėdami konfigūruoti parduotuvių vadybininkų užduočių valdymo teises, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-111">To configure task management permissions for store managers, follow these steps.</span></span>

1. <span data-ttu-id="1f9e2-112">Eikite į **Mažmeninė prekyba ir prekyba \> Darbuotojai \> Teisių grupės**.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-112">Go to **Retail and Commerce \> Employees \> Permission groups**.</span></span>
1. <span data-ttu-id="1f9e2-113">Pasirinkite konkrečią teisių grupę (pvz., **Vadybininkas**), tada pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-113">Select a specific permission group (for example, **Manager**), and then select **Edit**.</span></span>
1. <span data-ttu-id="1f9e2-114">„FastTab“ skirtuke **Teisės** parinktyje **Leisti užduočių valdymą** nustatykite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-114">On the **Permissions** FastTab, set the **Allow task management** option to **Yes**.</span></span>
1. <span data-ttu-id="1f9e2-115">„FastTab“ skirtuke **Pranešimai** įtraukite operaciją **Užduočių valdymas** ir lauke **Rodyti užsakymą** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-115">On the **Notifications** FastTab, add the **Task management** operation, and enter a value in the **Display order** field.</span></span> <span data-ttu-id="1f9e2-116">Pavyzdžiui, įveskite **2**, jei operacijoje **Užsakymo įvykdymas** jau yra lauko **Rodyti užsakymą** reikšmė **1**.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-116">For example, enter **2** if the **Order fulfillment** operation already has a **Display order** value of **1**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="1f9e2-117">Jei ne vadybininkai privalo turėti EKA užduočių valdymo teisių, galite suteikti teisę atskiram asmeniui.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-117">If a non-manager persona must have task management permissions in the POS, you can grant permission to the individual.</span></span> <span data-ttu-id="1f9e2-118">Arba galite sukurti naują ne vadybininkams skirtą leidimų grupę ir parinktyje **Leisti užduočių valdymą** nustatyti **Taip**.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-118">Alternatively, you can create a new permission group for non-managers and set the **Allow task management** option to **Yes**.</span></span>

<span data-ttu-id="1f9e2-119">Toliau pateiktame paveikslėlyje vaizduojama, kaip konfigūruoti parduotuvių vadybininkų užduočių valdymo teises.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-119">The following illustration shows how to configure task management permissions for store managers.</span></span>

![Parduotuvių vadybininkų užduočių valdymo teisių konfigūravimas](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a><span data-ttu-id="1f9e2-121">Darbuotojų teisių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="1f9e2-121">Configure permissions for employees</span></span>

<span data-ttu-id="1f9e2-122">Darbuotojai privalo turėti teises, kad galėtų kurti užduočių sąrašus, valdyti priskyrimo kriterijus ir konfigūruoti užduočių sąrašo pasikartojimą.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-122">Employees must have permissions to create task lists, manage assignment criteria, and configure the recurrence of any task list.</span></span> <span data-ttu-id="1f9e2-123">Norėdami konfigūruoti šias teises, turite priskirti darbuotojams vaidmenį **Mažmeninės prekybos užduočių vadovas**.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-123">To configure these permissions, you assign employees to the **Retail task manager** role.</span></span>

<span data-ttu-id="1f9e2-124">Norėdami konfigūruoti darbuotojo teises, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-124">To configure permissions for an employee, follow these steps.</span></span>

1. <span data-ttu-id="1f9e2-125">Eikite į **Mažmeninė prekyba ir prekyba \> Darbuotojai \> Vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-125">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="1f9e2-126">Pasirinkite darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-126">Select an employee.</span></span>
1. <span data-ttu-id="1f9e2-127">„FastTab“ skirtuke **Vartotojo vaidmenys** pasirinkite **Priskirti vaidmenis**.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-127">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="1f9e2-128">Dialogo lange **Priskirti vaidmenis vartotojui** pasirinkite vaidmenį **Mažmeninės prekybos užduočių vadovas**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-128">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

## <a name="distribute-permissions-to-pos-clients"></a><span data-ttu-id="1f9e2-129">Teisių EKA klientams paskirstymas</span><span class="sxs-lookup"><span data-stu-id="1f9e2-129">Distribute permissions to POS clients</span></span>

<span data-ttu-id="1f9e2-130">Prieš darbuotojams pradedant naudotis EKA klientais, šių klientų teisės turi būti paskirstytos ir sinchronizuotos.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-130">Before employees can use POS clients, permissions must be distributed and synced to those clients.</span></span>

<span data-ttu-id="1f9e2-131">Norėdami paskirstyti teises EKA klientams, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-131">To distribute permissions to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="1f9e2-132">Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-132">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="1f9e2-133">Pasirinkite paskirstymo grafiką **1060** (**Darbuotojai**), tada pasirinkite **Vykdyti dabar**.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-133">Select the **1060** (**Staff**) distribution schedule, and then select **Run now**.</span></span>
1. <span data-ttu-id="1f9e2-134">Pasirinkite paskirstymo grafiką **1070** (**Kanalo konfigūracija**), tada pasirinkite **Vykdyti dabar**.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-134">Select the **1070** (**Channel configuration**) distribution schedule, and then select **Run now**.</span></span>

## <a name="configure-pos-notifications-for-tasks"></a><span data-ttu-id="1f9e2-135">Užduotims skirtų EKA pranešimų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="1f9e2-135">Configure POS notifications for tasks</span></span>

<span data-ttu-id="1f9e2-136">Užduočių valdymas turi būti sukonfigūruotas taip, kad pranešimai būtų pasiekiami EKA programoje.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-136">Task management must be configured so that notifications are available in the POS application.</span></span>

<span data-ttu-id="1f9e2-137">Norėdami konfigūruoti EKA pranešimus užduotims, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-137">To configure POS notifications for tasks, follow these steps.</span></span>

1. <span data-ttu-id="1f9e2-138">Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA \> EKA operacijos**.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-138">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="1f9e2-139">Raskite operaciją **1400** (**Užduočių valdymas**) ir pažymėkite žymės langelį **Įjungti pranešimus**.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-139">Find operation **1400** (**Task management**), and select the **Enable notifications** check box for it.</span></span>

<span data-ttu-id="1f9e2-140">Toliau pateiktame paveikslėlyje rodoma operacija **Užduočių valdymas** puslapyje **EKA operacijos**.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-140">The following illustration shows the **Task management** operation on the **POS operations** page.</span></span>

![Užduočių valdymo operacija EKA operacijų puslapyje](media/HQ-POS-Tasks-Notifications.png)

<span data-ttu-id="1f9e2-142">Daugiau informacijos apie tai, kaip sukonfigūruoti EKA pranešimus, žr. [Rodyti užsakymų pranešimus elektroniniame kasos aparate (EKA)](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="1f9e2-142">For more information about how to configure POS notifications, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a><span data-ttu-id="1f9e2-143">Plytelės Užduotys EKA programos pagrindiniame puslapyje konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="1f9e2-143">Configure the Tasks tile on a POS application home page</span></span>

<span data-ttu-id="1f9e2-144">Prieš konfigūruodami plytelę **Užduotys** EKA programos pagrindiniame puslapyje, žr. [Elektroninio kasos aparato (EKA) ekrano maketai](pos-screen-layouts.md), kad sužinotumėte, kaip konfigūruoti ir įtraukti naujų mygtukų į EKA ekrano maketą.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-144">Before you configure the **Tasks** tile on the home page of a POS application, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information about how to configure and add new buttons to a POS screen layout.</span></span>

<span data-ttu-id="1f9e2-145">Norėdami konfigūruoti plytelę **Užduotys** EKA programos pagrindiniame puslapyje, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-145">To configure the **Tasks** tile on a POS application home page, follow these steps.</span></span>

1. <span data-ttu-id="1f9e2-146">Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA \> Ekrano maketai**.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-146">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
1. <span data-ttu-id="1f9e2-147">Pasirinkite ekrano maketą, maketo dydį ir mygtukyną.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-147">Select a screen layout, select a layout size, and select a button grid.</span></span>
1. <span data-ttu-id="1f9e2-148">„FastTab“ skirtuke **Mygtukynas** pasirinkite **Dizaineris**, kad redaguotumėte pasirinktą mygtukyną.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-148">On the **Button grids** FastTab, select **Designer** to edit the selected button grid.</span></span>
1. <span data-ttu-id="1f9e2-149">Įtraukite plytelę **Užduotys** į atitinkamą pagrindinio ekrano skyrių.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-149">Add a **Tasks** tile to the appropriate section of the home page.</span></span>

<span data-ttu-id="1f9e2-150">Toliau pateikiamoje iliustracijoje rodomas plytelės **Užduotys** EKA pagrindiniame puslapyje pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="1f9e2-150">The following illustration shows an example of a **Tasks** tile on a POS home page.</span></span>

![Plytelė Užduotys EKA pagrindiniame puslapyje](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a><span data-ttu-id="1f9e2-152">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1f9e2-152">Additional resources</span></span>

[<span data-ttu-id="1f9e2-153">Užduočių valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="1f9e2-153">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="1f9e2-154">Užduočių sąrašų kūrimas ir užduočių įtraukimas</span><span class="sxs-lookup"><span data-stu-id="1f9e2-154">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="1f9e2-155">Užduočių sąrašų priskyrimas parduotuvėms arba darbuotojams</span><span class="sxs-lookup"><span data-stu-id="1f9e2-155">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="1f9e2-156">Užduočių valdymas EKA programoje</span><span class="sxs-lookup"><span data-stu-id="1f9e2-156">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
