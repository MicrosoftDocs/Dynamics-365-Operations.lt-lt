---
title: Užduočių sąrašų kūrimas ir užduočių įtraukimas
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ kurti užduočių sąrašus ir įtraukti į juos užduotis.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 1cab31784db9f3242dce20e98762088436a5a8f8
ms.sourcegitcommit: 80cbb7d22267aa6a0ae0568d0063fb95556958a5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036837"
---
# <a name="create-task-lists-and-add-tasks"></a><span data-ttu-id="0e9af-103">Užduočių sąrašų kūrimas ir užduočių įtraukimas</span><span class="sxs-lookup"><span data-stu-id="0e9af-103">Create task lists and add tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0e9af-104">Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ kurti užduočių sąrašus ir įtraukti į juos užduotis.</span><span class="sxs-lookup"><span data-stu-id="0e9af-104">This topic describes how to create task lists and add tasks to them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0e9af-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="0e9af-105">Overview</span></span>

<span data-ttu-id="0e9af-106">*Užduotis* apibrėžia konkretų darbą arba veiksmą, kurį reikia atlikti iki nurodyto termino.</span><span class="sxs-lookup"><span data-stu-id="0e9af-106">A *task* defines a specific piece of work or an action that someone must complete on or before a specified due date.</span></span> <span data-ttu-id="0e9af-107">Programoje „Dynamics 365 Commerce” į užduotį galima įtraukti išsamių instrukcijų ir informacijos apie kontaktinį asmenį.</span><span class="sxs-lookup"><span data-stu-id="0e9af-107">In Dynamics 365 Commerce, a task can include detailed instructions and information about a contact person.</span></span> <span data-ttu-id="0e9af-108">Į ją taip pat galima įtraukti tarnybinio biuro operacijų, elektroninio kasos aparato (EKA) operacijų arba svetainių puslapių saitų, siekiant patobulinti našumą ir suteikti kontekstą, reikalingą užduoties savininkui efektyviai atlikti užduotį.</span><span class="sxs-lookup"><span data-stu-id="0e9af-108">It can also include links to back-office operations, point of sale (POS) operations, or site pages, to help improve productivity and provide the context that the task owner requires to complete the task efficiently.</span></span>

<span data-ttu-id="0e9af-109">*Užduočių sąrašas* yra užduočių, kurios turi būti atliktos vykdant verslo procesą, rinkinys.</span><span class="sxs-lookup"><span data-stu-id="0e9af-109">A *task list* is a collection of tasks that must be completed as part of a business process.</span></span> <span data-ttu-id="0e9af-110">Pavyzdžiui, gali būti užduočių sąrašas, skirtas naujam darbuotojui įvykdyti supažindinimo metu, užduočių sąrašas, skirtas kasininkams, dirbantiems vakarinėmis pamainomis, arba užduočių sąrašas, kurį reikia įvykdyti, siekiant paruošti parduotuvę būsimam švenčių laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="0e9af-110">For example, there might be a task list that a new worker must complete during onboarding, a task list for cashiers who work evening shifts, or a task list that must be completed to prepare the store for an upcoming holiday season.</span></span> <span data-ttu-id="0e9af-111">„Commerce“ kiekvienas užduočių sąrašas, kuriame yra tikslinė data, gali būti priskirtas neribotam parduotuvių ar darbuotojų skaičiui, be to, jį galima konfigūruoti, kad pasikartotų.</span><span class="sxs-lookup"><span data-stu-id="0e9af-111">In Commerce, every task list that has a target date can be assigned to any number of stores or employees, and it can be configured to recur.</span></span>

<span data-ttu-id="0e9af-112">Ir vadybininkai, ir darbuotojai gali kurti užduočių sąrašus „Commerce“ tarnybiniame biure ir priskirti juos parduotuvių grupei.</span><span class="sxs-lookup"><span data-stu-id="0e9af-112">Both managers and workers can create task lists in Commerce back office, and then assign them to a set of stores.</span></span>

## <a name="create-a-task-list"></a><span data-ttu-id="0e9af-113">Užduočių sąrašo kūrimas</span><span class="sxs-lookup"><span data-stu-id="0e9af-113">Create a task list</span></span>

<span data-ttu-id="0e9af-114">Norėdami sukurti užduočių sąrašą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0e9af-114">To create a task list, follow these steps.</span></span>

1. <span data-ttu-id="0e9af-115">Eikite į **Mažmeninė prekyba ir prekyba \> Užduočių valdymas \> Užduočių valdymo administravimas**.</span><span class="sxs-lookup"><span data-stu-id="0e9af-115">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="0e9af-116">Pasirinkite **Naujas**, tada laukuose **Pavadinimas**, **Aprašas** ir **Savininkas** įveskite vertes.</span><span class="sxs-lookup"><span data-stu-id="0e9af-116">Select **New**, and then enter values in the **Name**, **Description**, and **Owner** fields.</span></span>
1. <span data-ttu-id="0e9af-117">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="0e9af-117">Select **Save**.</span></span>

## <a name="add-tasks-to-a-task-list"></a><span data-ttu-id="0e9af-118">Užduočių įtraukimas į užduočių sąrašą</span><span class="sxs-lookup"><span data-stu-id="0e9af-118">Add tasks to a task list</span></span>

<span data-ttu-id="0e9af-119">Norėdami įtraukti užduočių į užduočių sąrašą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0e9af-119">To add tasks to a task list, follow these steps.</span></span>
 
1. <span data-ttu-id="0e9af-120">Esamo užduočių sąrašo „FastTab“ skirtuke **Užduotys** pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="0e9af-120">On the **Tasks** FastTab of an existing task list, select **New** to add a task.</span></span>
1. <span data-ttu-id="0e9af-121">Dialogo lango **Kurti naują užduotį** lauke **Pavadinimas** įveskite užduoties pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="0e9af-121">In the **Create a new task** dialog box, in the **Name** field, enter a name for the task.</span></span>
1. <span data-ttu-id="0e9af-122">Lauke **Termino poslinkis nuo tikslinės datos** įveskite teigiamą arba neigiamą sveikąją vertę.</span><span class="sxs-lookup"><span data-stu-id="0e9af-122">In the **Due data offset from target date** field, enter a positive or negative integer value.</span></span> <span data-ttu-id="0e9af-123">Pavyzdžiui, įveskite **-2**, jei užduotis turi būti užbaigta likus dviem dienoms iki užduočių sąrašo termino datos.</span><span class="sxs-lookup"><span data-stu-id="0e9af-123">For example, enter **-2** if the task should be completed two days before the task list's due date.</span></span>
1. <span data-ttu-id="0e9af-124">Lauke **Pastabos** įveskite išsamias instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="0e9af-124">In the **Notes** field, enter detailed instructions.</span></span>
1. <span data-ttu-id="0e9af-125">Lauke **Kontaktinis asmuo** įveskite srities eksperto, į kurį užduoties savininkas, prireikus, gali kreiptis pagalbos, vardą ir pavardę.</span><span class="sxs-lookup"><span data-stu-id="0e9af-125">In the **Contact person** field, enter the name of a subject matter expert that the task owner can contact if he or she needs help.</span></span>
1. <span data-ttu-id="0e9af-126">Lauke **Užduoties saitas** įveskite saitą, pagrįstą užduoties pobūdžiu.</span><span class="sxs-lookup"><span data-stu-id="0e9af-126">In the **Task link** field, enter a link, based on the nature of the task.</span></span>

> [!TIP]
> <span data-ttu-id="0e9af-127">Nors kurdami užduočių sąrašą galite naudoti lauką **Priskirta**, kad kam nors priskirtumėte užduočių, rekomenduojame vengti priskirti užduotis, kai kuriamas užduočių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="0e9af-127">Although you can use the **Assigned to** field to assign tasks to someone while you're creating a task list, we recommend that you avoid assigning tasks during task list creation.</span></span> <span data-ttu-id="0e9af-128">Vietoj to priskirkite užduotis, sukūrę atskiroms parduotuvėms skirtų sąrašo egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="0e9af-128">Instead, assign the tasks after the list is instantiated for individual stores.</span></span>

## <a name="use-task-links-to-help-improve-worker-productivity"></a><span data-ttu-id="0e9af-129">Užduočių saitų naudojimas, siekiant tobulinti darbuotojų efektyvumą</span><span class="sxs-lookup"><span data-stu-id="0e9af-129">Use task links to help improve worker productivity</span></span>

<span data-ttu-id="0e9af-130">„Commerce“ leidžiama susieti užduotis su konkrečiomis EKA operacijomis, pvz., su pardavimo ataskaitos vykdymu, mokomojo vaizdo įrašo, skirto naujiems darbuotojams orientuoti, peržiūra arba tarnybinio biuro operacijos atlikimu.</span><span class="sxs-lookup"><span data-stu-id="0e9af-130">Commerce lets you link tasks to specific POS operations, such as running a sales report, viewing an online training video for new employee orientation, or performing a back-office operation.</span></span> <span data-ttu-id="0e9af-131">Ši funkcija padeda užduočių savininkams gauti informacijos, kurios reikia norint efektyviai atlikti užduotį.</span><span class="sxs-lookup"><span data-stu-id="0e9af-131">This feature helps task owners get the information that they need to complete a task efficiently.</span></span>

<span data-ttu-id="0e9af-132">Norėdami įtraukti užduočių saitų kurdami užduotį, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0e9af-132">To add task links while you create a task, follow these steps.</span></span>

1. <span data-ttu-id="0e9af-133">Esamo užduočių sąrašo „FastTab“ skirtuke **Užduotys** pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="0e9af-133">On the **Tasks** FastTab of an existing task list, select **Edit**.</span></span>
1. <span data-ttu-id="0e9af-134">Dialogo lango **Redaguoti užduotį** lauke **Užduoties saitas** pasirinkite vieną ar daugiau toliau pateikiamų parinkčių.</span><span class="sxs-lookup"><span data-stu-id="0e9af-134">In the **Edit task** dialog box, in the **Task link** field, select one or more of the following options:</span></span>

    - <span data-ttu-id="0e9af-135">Pasirinkite **Meniu elementas**, kad konfigūruotumėte tarnybinio biuro operaciją, pvz., „Produkto rinkiniai“.</span><span class="sxs-lookup"><span data-stu-id="0e9af-135">Select **Menu item** to configure a back-office operation, such as "Product kits."</span></span>
    - <span data-ttu-id="0e9af-136">Pasirinkite **EKA operacija**, kad konfigūruotumėte EKA operaciją, pvz., „Pardavimo ataskaitos”.</span><span class="sxs-lookup"><span data-stu-id="0e9af-136">Select **POS Operation** to configure a POS operation, such as "Sales reports."</span></span>
    - <span data-ttu-id="0e9af-137">Pasirinkite **URL**, kad konfigūruotumėte absoliučią URL.</span><span class="sxs-lookup"><span data-stu-id="0e9af-137">Select **URL** to configure an absolute URL.</span></span>

<span data-ttu-id="0e9af-138">Toliau pateiktame paveikslėlyje parodytas užduočių saitų žymėjimas dialogo lange **Redaguoti užduotį**.</span><span class="sxs-lookup"><span data-stu-id="0e9af-138">The following illustration shows the selection of task links in the **Edit task** dialog box.</span></span>

![Užduočių saitų žymėjimas dialogo lange „Redaguoti užduotį“](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a><span data-ttu-id="0e9af-140">EKA operacijos konfigūravimas, kad ją būtų galima susieti su užduotimi</span><span class="sxs-lookup"><span data-stu-id="0e9af-140">Configure a POS operation so that it can be linked to a task</span></span>

<span data-ttu-id="0e9af-141">Norėdami konfigūruoti EKA operaciją, kad ją būtų galima susieti su užduotimi, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0e9af-141">To configure a POS operation so that it can be linked to a task, follow these steps.</span></span>

1. <span data-ttu-id="0e9af-142">Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA \> EKA operacijos**.</span><span class="sxs-lookup"><span data-stu-id="0e9af-142">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="0e9af-143">Pasirinkite **Redaguoti**, raskite EKA operaciją, tada pažymėkite jos žymės langelį **Įgalinti užduočių valdymą**.</span><span class="sxs-lookup"><span data-stu-id="0e9af-143">Select **Edit**, find the POS operation, and then select the **Enable Task Management** check box for it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0e9af-144">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="0e9af-144">Additional resources</span></span>

[<span data-ttu-id="0e9af-145">Užduočių valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="0e9af-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="0e9af-146">Užduočių valdymo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="0e9af-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="0e9af-147">Užduočių sąrašų priskyrimas parduotuvėms arba darbuotojams</span><span class="sxs-lookup"><span data-stu-id="0e9af-147">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="0e9af-148">Užduočių valdymas EKA programoje</span><span class="sxs-lookup"><span data-stu-id="0e9af-148">Task management in POS</span></span>](task-mgmt-POS.md)