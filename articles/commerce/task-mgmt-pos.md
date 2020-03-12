---
title: Užduočių valdymas EKA programoje
description: Šioje temoje aprašomas užduočių valdymas „Microsoft Dynamics 365 Commerce“ elektroninio kasos aparato (EKA) programoje.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cc685fcd584fe2ab5cd9282e8fbefbd284d5b2a2
ms.sourcegitcommit: 80cbb7d22267aa6a0ae0568d0063fb95556958a5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036791"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="54d55-103">Užduočių valdymas EKA programoje</span><span class="sxs-lookup"><span data-stu-id="54d55-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="54d55-104">Šioje temoje aprašomas užduočių valdymas „Microsoft Dynamics 365 Commerce“ elektroninio kasos aparato (EKA) programoje.</span><span class="sxs-lookup"><span data-stu-id="54d55-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

## <a name="overview"></a><span data-ttu-id="54d55-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="54d55-105">Overview</span></span>

<span data-ttu-id="54d55-106">„Dynamics 365 Commerce“ EKA programoje yra užduočių valdymo funkcijų, kurios leidžia parduotuvės vadybininkams ir darbuotojams tvarkyti užduotis ir naujinti užduočių būseną.</span><span class="sxs-lookup"><span data-stu-id="54d55-106">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="54d55-107">Parduotuvės darbuotojai gali pasiekti užduotis, pasirinkdami EKA pagrindiniame puslapyje esančią plytelę **Užduotys** arba pasirinkdami užduočių pranešimus.</span><span class="sxs-lookup"><span data-stu-id="54d55-107">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="54d55-108">Pagal numatytuosius nustatymus parduotuvės darbuotojai perkeliami į skirtuką **Mano užduotys**, kur gali peržiūrėti jiems priskirtas užduotis.</span><span class="sxs-lookup"><span data-stu-id="54d55-108">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="54d55-109">Tačiau jie gali lengvai pereiti prie skirtukų **Pradelstos užduotys**, **Atviros užduotys** ir **Užduočių sąrašai**.</span><span class="sxs-lookup"><span data-stu-id="54d55-109">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="54d55-110">Parduotuvių vadybininkams skirtos užduočių operacijos</span><span class="sxs-lookup"><span data-stu-id="54d55-110">Task operations for store managers</span></span>

<span data-ttu-id="54d55-111">Parduotuvės vadybininkai gali atlikti šias užduočių operacijas EKA programoje, naudodami komandų juostos mygtukus:</span><span class="sxs-lookup"><span data-stu-id="54d55-111">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="54d55-112">**Priskirti** – pasirinktų užduočių priskyrimas parduotuvės darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="54d55-112">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="54d55-113">**Užduoties būsena** – pažymėtų užduočių būsenos keitimas.</span><span class="sxs-lookup"><span data-stu-id="54d55-113">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="54d55-114">**Filtruoti** – pagal numatytuosius nustatymus rodomos tik aktyvios užduotys.</span><span class="sxs-lookup"><span data-stu-id="54d55-114">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="54d55-115">Tačiau taikydami filtrus vadybininkai gali peržiūrėti visas užduotis, net užduotis, kurios yra baigtos arba atšauktos.</span><span class="sxs-lookup"><span data-stu-id="54d55-115">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="54d55-116">**Nauja užduotis** – užduoties kūrimas pagal esamą užduočių sąrašą arba vienos paskirties užduoties kūrimas.</span><span class="sxs-lookup"><span data-stu-id="54d55-116">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="54d55-117">Parduotuvės darbuotojai gali atlikti šias užduočių operacijas EKA programoje, naudodami komandų juostos mygtukus:</span><span class="sxs-lookup"><span data-stu-id="54d55-117">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="54d55-118">**Užduoties būsena** – pažymėtų užduočių būsenos keitimas.</span><span class="sxs-lookup"><span data-stu-id="54d55-118">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="54d55-119">**Filtruoti** – pagal numatytuosius nustatymus rodomos tik aktyvios užduotys.</span><span class="sxs-lookup"><span data-stu-id="54d55-119">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="54d55-120">Tačiau taikydami filtrus darbuotojai gali peržiūrėti visas užduotis, net užduotis, kurios yra baigtos arba atšauktos.</span><span class="sxs-lookup"><span data-stu-id="54d55-120">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="54d55-121">Toliau pateiktame paveikslėlyje vaizduojamas „Commerce“ EKA programos skirtukas **Mano užduotys**.</span><span class="sxs-lookup"><span data-stu-id="54d55-121">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Skirtukas „Mano užduotys“ „Commerce“ EKA programoje](media/POS-task-management.png)

<span data-ttu-id="54d55-123">Tolesnėje iliustracijoje pavaizduotas skirtukas **Užduočių sąrašai**.</span><span class="sxs-lookup"><span data-stu-id="54d55-123">The following illustration shows the **Task lists** tab.</span></span>

![Skirtukas „Užduočių sąrašai“ „Commerce“ EKA programoje](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="54d55-125">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="54d55-125">Additional resources</span></span>

[<span data-ttu-id="54d55-126">Užduočių valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="54d55-126">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="54d55-127">Užduočių valdymo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="54d55-127">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="54d55-128">Užduočių sąrašų kūrimas ir užduočių įtraukimas</span><span class="sxs-lookup"><span data-stu-id="54d55-128">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="54d55-129">Užduočių sąrašų priskyrimas parduotuvėms arba darbuotojams</span><span class="sxs-lookup"><span data-stu-id="54d55-129">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)
