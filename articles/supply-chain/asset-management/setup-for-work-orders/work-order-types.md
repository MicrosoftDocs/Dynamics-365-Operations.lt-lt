---
title: Darbo užsakymų tipai
description: Šioje temoje aiškinami darbo užsakymų tipai modulyje „Turto valdymas”.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b8e43908e3f13c9e4fd6fab6f1e17a171866b803
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888790"
---
# <a name="work-order-types"></a><span data-ttu-id="c3c0c-103">Darbo užsakymų tipai</span><span class="sxs-lookup"><span data-stu-id="c3c0c-103">Work order types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c3c0c-104">Darbo užsakymų tipai naudojami siekiant suskirstyti darbo užsakymus į kategorijas.</span><span class="sxs-lookup"><span data-stu-id="c3c0c-104">Work order types are used to categorize work orders.</span></span> <span data-ttu-id="c3c0c-105">Pavyzdžiui, galite turėti darbo užsakymų, susijusių su prevencine arba taisomąja priežiūra.</span><span class="sxs-lookup"><span data-stu-id="c3c0c-105">For example, you might have work orders that are related to preventive maintenance or corrective maintenance.</span></span>

<span data-ttu-id="c3c0c-106">Pagal darbo užsakymo tipą apibrėžiama sąsaja su darbo užsakymo ciklo modeliu.</span><span class="sxs-lookup"><span data-stu-id="c3c0c-106">A work order type defines an affiliation with a work order lifecycle model.</span></span> <span data-ttu-id="c3c0c-107">Pagal darbo užsakymo ciklo modelį apibrėžiamos darbo užsakymo ciklo būsenos, kurios gali būti nustatytos darbo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="c3c0c-107">A work order lifecycle model defines the work order lifecycle states that can be set on a work order.</span></span> <span data-ttu-id="c3c0c-108">(Darbo užsakymo ciklo būsenų pavyzdžiai, be kita ko, yra **Sukurtas**, **Vykdomas** ir **Užbaigtas**.)</span><span class="sxs-lookup"><span data-stu-id="c3c0c-108">(Examples of work order lifecycle states include **Created**, **In Process**, and **Finished**.)</span></span>

<span data-ttu-id="c3c0c-109">Daugiau informacijos apie darbo užsakymo ciklo būsenas ir projekto etapus žr. [Darbo užsakymo ciklo būsenos](work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="c3c0c-109">For more information about work order lifecycle states and project stages, see [Work order lifecycle states](work-order-lifecycle-states.md).</span></span>

1. <span data-ttu-id="c3c0c-110">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Darbo užsakymai** \> **Darbo užsakymų tipai**.</span><span class="sxs-lookup"><span data-stu-id="c3c0c-110">Select **Asset management** \> **Setup** \> **Work orders** \> **Work order types**.</span></span>
2. <span data-ttu-id="c3c0c-111">Norėdami sukurti darbo užsakymo tipą, pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="c3c0c-111">Select **New** to create a work order type.</span></span>
3. <span data-ttu-id="c3c0c-112">Lauke **Darbo užsakymo tipas** įveskite darbo užsakymo tipo ID.</span><span class="sxs-lookup"><span data-stu-id="c3c0c-112">In the **Work order type** field, enter an ID for the work order type.</span></span>
4. <span data-ttu-id="c3c0c-113">Tada lauke **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c3c0c-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="c3c0c-114">Lauke **Darbo užsakymo ciklo modelis** pasirinkite ciklo modelį.</span><span class="sxs-lookup"><span data-stu-id="c3c0c-114">In the **Work order lifecycle model** field, select a lifecycle model.</span></span>
5. <span data-ttu-id="c3c0c-115">Parinktyje **Vienas priežiūros darbuotojas** pasirinkite **Taip**, jeigu visos su šio tipo darbo užsakymu susijusios darbo užsakymo užduotys turėtų būti paskirtos tam pačiam priežiūros darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="c3c0c-115">Set the **One maintenance worker** option to **Yes** if all work order jobs that are related to a work order of this type should be scheduled to the same maintenance worker.</span></span>
6. <span data-ttu-id="c3c0c-116">Lauke **Išlaidų tipas** tinkamai pasirinkite **Taisomosios**, **Prevencinės** arba **Investicinės**.</span><span class="sxs-lookup"><span data-stu-id="c3c0c-116">In the **Cost type** field, select **Corrective**, **Preventive**, or **Investment**, as appropriate.</span></span> <span data-ttu-id="c3c0c-117">Visoms darbo užsakyme nurodytoms darbo užsakymo užduotims turi būti nustatytas toks pat išlaidų tipas.</span><span class="sxs-lookup"><span data-stu-id="c3c0c-117">All work order jobs on a work order must have the same cost type.</span></span>
7. <span data-ttu-id="c3c0c-118">Atitinkamose skyriaus **Privaloma** parinktyse pažymėkite **Taip**, kad patikslintumėte, kuri su gedimais arba prižiūrimo turto prastova susijusi informacija įtraukta į šio tipo darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="c3c0c-118">In the **Mandatory** section, set the relevant options to **Yes** to specify which fault-related or maintenance downtime–related information is added to a work order of this type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c3c0c-119">Parinktys skyriuje **Privaloma** yra susijusios su „FastTab” **Tikrinti** parinktimis puslapyje **Darbo užsakymo ciklo būsenos** (**Turto valdymas** \> **Sąranka** \> **Darbo užsakymai** \> **Ciklo būsenos**).</span><span class="sxs-lookup"><span data-stu-id="c3c0c-119">The options in the **Mandatory** section are related to the options on the **Validate** FastTab of the **Work order lifecycle states** page (**Asset management** \> **Setup** \> **Work orders** \> **Lifecycle states**).</span></span>

8. <span data-ttu-id="c3c0c-120">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="c3c0c-120">Select **Save**.</span></span>

![Darbo užsakymų tipai](media/16-setup-for-work-orders.png)
