---
title: Užduočių sąrašų kūrimas ir užduočių įtraukimas
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ kurti užduočių sąrašus ir įtraukti į juos užduotis.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: f3fcfae9f4ab458b4f14f18859f22fc25bf98623
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027629"
---
# <a name="create-task-lists-and-add-tasks"></a><span data-ttu-id="38835-103">Užduočių sąrašų kūrimas ir užduočių įtraukimas</span><span class="sxs-lookup"><span data-stu-id="38835-103">Create task lists and add tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="38835-104">Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ kurti užduočių sąrašus ir įtraukti į juos užduotis.</span><span class="sxs-lookup"><span data-stu-id="38835-104">This topic describes how to create task lists and add tasks to them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="38835-105">*Užduotis* apibrėžia konkretų darbą arba veiksmą, kurį reikia atlikti iki nurodyto termino.</span><span class="sxs-lookup"><span data-stu-id="38835-105">A *task* defines a specific piece of work or an action that someone must complete on or before a specified due date.</span></span> <span data-ttu-id="38835-106">Programoje „Dynamics 365 Commerce” į užduotį galima įtraukti išsamių instrukcijų ir informacijos apie kontaktinį asmenį.</span><span class="sxs-lookup"><span data-stu-id="38835-106">In Dynamics 365 Commerce, a task can include detailed instructions and information about a contact person.</span></span> <span data-ttu-id="38835-107">Į ją taip pat galima įtraukti tarnybinio biuro operacijų, elektroninio kasos aparato (EKA) operacijų arba svetainių puslapių saitų, siekiant patobulinti našumą ir suteikti kontekstą, reikalingą užduoties savininkui efektyviai atlikti užduotį.</span><span class="sxs-lookup"><span data-stu-id="38835-107">It can also include links to back-office operations, point of sale (POS) operations, or site pages, to help improve productivity and provide the context that the task owner requires to complete the task efficiently.</span></span>

<span data-ttu-id="38835-108">*Užduočių sąrašas* yra užduočių, kurios turi būti atliktos vykdant verslo procesą, rinkinys.</span><span class="sxs-lookup"><span data-stu-id="38835-108">A *task list* is a collection of tasks that must be completed as part of a business process.</span></span> <span data-ttu-id="38835-109">Pavyzdžiui, gali būti užduočių sąrašas, skirtas naujam darbuotojui įvykdyti supažindinimo metu, užduočių sąrašas, skirtas kasininkams, dirbantiems vakarinėmis pamainomis, arba užduočių sąrašas, kurį reikia įvykdyti, siekiant paruošti parduotuvę būsimam švenčių laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="38835-109">For example, there might be a task list that a new worker must complete during onboarding, a task list for cashiers who work evening shifts, or a task list that must be completed to prepare the store for an upcoming holiday season.</span></span> <span data-ttu-id="38835-110">„Commerce“ kiekvienas užduočių sąrašas, kuriame yra tikslinė data, gali būti priskirtas neribotam parduotuvių ar darbuotojų skaičiui, be to, jį galima konfigūruoti, kad pasikartotų.</span><span class="sxs-lookup"><span data-stu-id="38835-110">In Commerce, every task list that has a target date can be assigned to any number of stores or employees, and it can be configured to recur.</span></span>

<span data-ttu-id="38835-111">Ir vadybininkai, ir darbuotojai gali kurti užduočių sąrašus „Commerce“ tarnybiniame biure ir priskirti juos parduotuvių grupei.</span><span class="sxs-lookup"><span data-stu-id="38835-111">Both managers and workers can create task lists in Commerce back office, and then assign them to a set of stores.</span></span>

## <a name="create-a-task-list"></a><span data-ttu-id="38835-112">Užduočių sąrašo kūrimas</span><span class="sxs-lookup"><span data-stu-id="38835-112">Create a task list</span></span>

<span data-ttu-id="38835-113">Norėdami sukurti užduočių sąrašą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="38835-113">To create a task list, follow these steps.</span></span>

1. <span data-ttu-id="38835-114">Eikite į **Mažmeninė prekyba ir prekyba \> Užduočių valdymas \> Užduočių valdymo administravimas**.</span><span class="sxs-lookup"><span data-stu-id="38835-114">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="38835-115">Pasirinkite **Naujas**, tada laukuose **Pavadinimas**, **Aprašas** ir **Savininkas** įveskite vertes.</span><span class="sxs-lookup"><span data-stu-id="38835-115">Select **New**, and then enter values in the **Name**, **Description**, and **Owner** fields.</span></span>
1. <span data-ttu-id="38835-116">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="38835-116">Select **Save**.</span></span>

## <a name="add-tasks-to-a-task-list"></a><span data-ttu-id="38835-117">Užduočių įtraukimas į užduočių sąrašą</span><span class="sxs-lookup"><span data-stu-id="38835-117">Add tasks to a task list</span></span>

<span data-ttu-id="38835-118">Norėdami įtraukti užduočių į užduočių sąrašą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="38835-118">To add tasks to a task list, follow these steps.</span></span>
 
1. <span data-ttu-id="38835-119">Esamo užduočių sąrašo „FastTab“ skirtuke **Užduotys** pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="38835-119">On the **Tasks** FastTab of an existing task list, select **New** to add a task.</span></span>
1. <span data-ttu-id="38835-120">Dialogo lango **Kurti naują užduotį** lauke **Pavadinimas** įveskite užduoties pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="38835-120">In the **Create a new task** dialog box, in the **Name** field, enter a name for the task.</span></span>
1. <span data-ttu-id="38835-121">Lauke **Termino poslinkis nuo tikslinės datos** įveskite teigiamą arba neigiamą sveikąją vertę.</span><span class="sxs-lookup"><span data-stu-id="38835-121">In the **Due data offset from target date** field, enter a positive or negative integer value.</span></span> <span data-ttu-id="38835-122">Pavyzdžiui, įveskite **-2**, jei užduotis turi būti užbaigta likus dviem dienoms iki užduočių sąrašo termino datos.</span><span class="sxs-lookup"><span data-stu-id="38835-122">For example, enter **-2** if the task should be completed two days before the task list's due date.</span></span>
1. <span data-ttu-id="38835-123">Lauke **Pastabos** įveskite išsamias instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="38835-123">In the **Notes** field, enter detailed instructions.</span></span>
1. <span data-ttu-id="38835-124">Lauke **Kontaktinis asmuo** įveskite srities eksperto, į kurį užduoties savininkas, prireikus, gali kreiptis pagalbos, vardą ir pavardę.</span><span class="sxs-lookup"><span data-stu-id="38835-124">In the **Contact person** field, enter the name of a subject matter expert that the task owner can contact if the task owner needs help.</span></span>
1. <span data-ttu-id="38835-125">Lauke **Užduoties saitas** įveskite saitą, pagrįstą užduoties pobūdžiu.</span><span class="sxs-lookup"><span data-stu-id="38835-125">In the **Task link** field, enter a link, based on the nature of the task.</span></span>

> [!TIP]
> <span data-ttu-id="38835-126">Nors kurdami užduočių sąrašą galite naudoti lauką **Priskirta**, kad kam nors priskirtumėte užduočių, rekomenduojame vengti priskirti užduotis, kai kuriamas užduočių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="38835-126">Although you can use the **Assigned to** field to assign tasks to someone while you're creating a task list, we recommend that you avoid assigning tasks during task list creation.</span></span> <span data-ttu-id="38835-127">Vietoj to priskirkite užduotis, sukūrę atskiroms parduotuvėms skirtų sąrašo egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="38835-127">Instead, assign the tasks after the list is instantiated for individual stores.</span></span>

## <a name="use-task-links-to-help-improve-worker-productivity"></a><span data-ttu-id="38835-128">Užduočių saitų naudojimas, siekiant tobulinti darbuotojų efektyvumą</span><span class="sxs-lookup"><span data-stu-id="38835-128">Use task links to help improve worker productivity</span></span>

<span data-ttu-id="38835-129">„Commerce“ leidžiama susieti užduotis su konkrečiomis EKA operacijomis, pvz., su pardavimo ataskaitos vykdymu, mokomojo vaizdo įrašo, skirto naujiems darbuotojams orientuoti, peržiūra arba tarnybinio biuro operacijos atlikimu.</span><span class="sxs-lookup"><span data-stu-id="38835-129">Commerce lets you link tasks to specific POS operations, such as running a sales report, viewing an online training video for new employee orientation, or performing a back-office operation.</span></span> <span data-ttu-id="38835-130">Ši funkcija padeda užduočių savininkams gauti informacijos, kurios reikia norint efektyviai atlikti užduotį.</span><span class="sxs-lookup"><span data-stu-id="38835-130">This feature helps task owners get the information that they need to complete a task efficiently.</span></span>

<span data-ttu-id="38835-131">Norėdami įtraukti užduočių saitų kurdami užduotį, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="38835-131">To add task links while you create a task, follow these steps.</span></span>

1. <span data-ttu-id="38835-132">Esamo užduočių sąrašo „FastTab“ skirtuke **Užduotys** pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="38835-132">On the **Tasks** FastTab of an existing task list, select **Edit**.</span></span>
1. <span data-ttu-id="38835-133">Dialogo lango **Redaguoti užduotį** lauke **Užduoties saitas** pasirinkite vieną ar daugiau toliau pateikiamų parinkčių.</span><span class="sxs-lookup"><span data-stu-id="38835-133">In the **Edit task** dialog box, in the **Task link** field, select one or more of the following options:</span></span>

    - <span data-ttu-id="38835-134">Pasirinkite **Meniu elementas**, kad konfigūruotumėte tarnybinio biuro operaciją, pvz., „Produkto rinkiniai“.</span><span class="sxs-lookup"><span data-stu-id="38835-134">Select **Menu item** to configure a back-office operation, such as "Product kits."</span></span>
    - <span data-ttu-id="38835-135">Pasirinkite **EKA operacija**, kad konfigūruotumėte EKA operaciją, pvz., „Pardavimo ataskaitos”.</span><span class="sxs-lookup"><span data-stu-id="38835-135">Select **POS Operation** to configure a POS operation, such as "Sales reports."</span></span>
    - <span data-ttu-id="38835-136">Pasirinkite **URL**, kad konfigūruotumėte absoliučią URL.</span><span class="sxs-lookup"><span data-stu-id="38835-136">Select **URL** to configure an absolute URL.</span></span>

<span data-ttu-id="38835-137">Toliau pateiktame paveikslėlyje parodytas užduočių saitų žymėjimas dialogo lange **Redaguoti užduotį**.</span><span class="sxs-lookup"><span data-stu-id="38835-137">The following illustration shows the selection of task links in the **Edit task** dialog box.</span></span>

![Užduočių saitų žymėjimas dialogo lange „Redaguoti užduotį“](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a><span data-ttu-id="38835-139">EKA operacijos konfigūravimas, kad ją būtų galima susieti su užduotimi</span><span class="sxs-lookup"><span data-stu-id="38835-139">Configure a POS operation so that it can be linked to a task</span></span>

<span data-ttu-id="38835-140">Norėdami konfigūruoti EKA operaciją, kad ją būtų galima susieti su užduotimi, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="38835-140">To configure a POS operation so that it can be linked to a task, follow these steps.</span></span>

1. <span data-ttu-id="38835-141">Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA \> EKA operacijos**.</span><span class="sxs-lookup"><span data-stu-id="38835-141">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="38835-142">Pasirinkite **Redaguoti**, raskite EKA operaciją, tada pažymėkite jos žymės langelį **Įgalinti užduočių valdymą**.</span><span class="sxs-lookup"><span data-stu-id="38835-142">Select **Edit**, find the POS operation, and then select the **Enable Task Management** check box for it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="38835-143">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="38835-143">Additional resources</span></span>

[<span data-ttu-id="38835-144">Užduočių valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="38835-144">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="38835-145">Užduočių valdymo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="38835-145">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="38835-146">Užduočių sąrašų priskyrimas parduotuvėms arba darbuotojams</span><span class="sxs-lookup"><span data-stu-id="38835-146">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="38835-147">Užduočių valdymas EKA programoje</span><span class="sxs-lookup"><span data-stu-id="38835-147">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
