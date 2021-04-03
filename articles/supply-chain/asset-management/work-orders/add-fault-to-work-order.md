---
title: Gedimo įtraukimas į darbo užsakymą
description: Šioje temoje aprašoma, kaip įtraukti gedimų registracijas į darbo užsakymus turto valdyme.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 489add5befe3660ad49e238b659bc8adbe1418a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263763"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="fa04c-103">Gedimo įtraukimas į darbo užsakymą</span><span class="sxs-lookup"><span data-stu-id="fa04c-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="fa04c-104">Į darbo užsakymą galite įtraukti gedimus, kurie buvo nustatyti gedimų dizaino įrankyje.</span><span class="sxs-lookup"><span data-stu-id="fa04c-104">You can add faults that were set up in the fault designer to a work order.</span></span> <span data-ttu-id="fa04c-105">Vienas ar daugiau gedimo įrašų turi būti susiję su turto tipais, naudojamais turtui, kuris yra pasirinktas darbo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="fa04c-105">One or more fault records must be connected to the asset types that are used for the asset that is selected in the work order.</span></span> <span data-ttu-id="fa04c-106">Daugiau informacijos apie sąranką žr. [Gedimų valdymas](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="fa04c-106">For more information about the setup, see [Fault management](../setup-for-work-orders/fault-management.md).</span></span>

1. <span data-ttu-id="fa04c-107">Pasirinkite **Turto valdymas** > **Bendra** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="fa04c-107">Select **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="fa04c-108">Pasirinkite darbo užsakymą, kad įjungtumėte gedimų registravimą, tada veiksmų srityje, esančioje skirtuke **Darbo užsakymas**, grupėje **Turtas**, pasirinkite **Turto gedimas**.</span><span class="sxs-lookup"><span data-stu-id="fa04c-108">Select the work order to make a fault registration on, and then, on the Action Pane, on the **Work order** tab, in the **Asset** group, select **Asset fault**.</span></span>

3. <span data-ttu-id="fa04c-109">„FastTab“ **Požymiai** pasirinkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="fa04c-109">On the **Symptoms** FastTab, select **Add line**.</span></span> <span data-ttu-id="fa04c-110">Iš eilės suteikiamas gedimo numeris automatiškai įvedamas į lauką **Gedimas**.</span><span class="sxs-lookup"><span data-stu-id="fa04c-110">A sequential fault number is automatically entered in the **Fault** field.</span></span>

4. <span data-ttu-id="fa04c-111">Lauke **Gedimo požymis** pasirinkite susijusį požymį.</span><span class="sxs-lookup"><span data-stu-id="fa04c-111">In the **Fault symptom** field, select the relevant symptom.</span></span>

5. <span data-ttu-id="fa04c-112">Laukuose **Gedimo sritis** ir **Gedimo tipas** pasirinkite atitinkamas vertes.</span><span class="sxs-lookup"><span data-stu-id="fa04c-112">In the **Fault area** and **Fault type** fields, select the appropriate values.</span></span>

6. <span data-ttu-id="fa04c-113">Į lauką **Gedimo data** automatiškai įtraukiama esama data.</span><span class="sxs-lookup"><span data-stu-id="fa04c-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="fa04c-114">Jei reikia, galite pasirinkti kitą datą.</span><span class="sxs-lookup"><span data-stu-id="fa04c-114">You can select a different date as you require.</span></span>

7. <span data-ttu-id="fa04c-115">„FastTab“ **Pažymėto požymio priežastys** įtraukite eilutę, aprašančią problemos priežastį.</span><span class="sxs-lookup"><span data-stu-id="fa04c-115">On the **Causes for selected symptom** FastTab, add a line to describe the cause of the issue.</span></span>

8. <span data-ttu-id="fa04c-116">„FastTab“ **Pažymėto požymio šalinimo priemonės** įtraukite eilutę, aprašančią galimą problemos sprendimą.</span><span class="sxs-lookup"><span data-stu-id="fa04c-116">On the **Remedies for selected symptom** FastTab, add a line to describe a possible solution to the issue.</span></span>

9. <span data-ttu-id="fa04c-117">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="fa04c-117">Select **Save**.</span></span>

<span data-ttu-id="fa04c-118">Toliau esančiame paveikslėlyje pateiktas gedimo registravimo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="fa04c-118">The illustration below shows an example of a fault registration.</span></span>

![1 pav.](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="fa04c-120">Turto gedimų rodinys</span><span class="sxs-lookup"><span data-stu-id="fa04c-120">View asset faults</span></span>

<span data-ttu-id="fa04c-121">Sąraše **Turto gedimai** galite peržiūrėti visus užregistruotus turto gedimus.</span><span class="sxs-lookup"><span data-stu-id="fa04c-121">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="fa04c-122">Sąrašo puslapyje **Turto gedimai** galite peržiūrėti visus užregistruotus turto gedimus.</span><span class="sxs-lookup"><span data-stu-id="fa04c-122">On the **Asset faults** list page, you can get an overview of all faults that have been registered on assets.</span></span> <span data-ttu-id="fa04c-123">Norėdami atidaryti puslapį, pasirinkite **Turto valdymas** > **Užklausos** > **Turto gedimas** > **Turto gedimai**.</span><span class="sxs-lookup"><span data-stu-id="fa04c-123">To open the page, select **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="fa04c-124">Turto gedimo ataskaitos spausdinimas</span><span class="sxs-lookup"><span data-stu-id="fa04c-124">Print asset fault report</span></span>

<span data-ttu-id="fa04c-125">Sąrašo puslapyje **Visas turtas** galite atspausdinti turto gedimo ataskaitą, kurioje nurodomi visos gedimų registracijos ir pateikiama grafinė gedimų statistikos apžvalga.</span><span class="sxs-lookup"><span data-stu-id="fa04c-125">From the **All assets** list page, you can print an asset fault report that shows all fault registrations and a graphical overview of fault statistics.</span></span>

1. <span data-ttu-id="fa04c-126">Pasirinkite **Turto valdymas** > **Bendra** > **Turtas** > **Visas turtas**.</span><span class="sxs-lookup"><span data-stu-id="fa04c-126">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="fa04c-127">Pasirinkite turtą, kuriam norite atspausdinti gedimų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="fa04c-127">Select the asset to print a fault report for.</span></span>

3. <span data-ttu-id="fa04c-128">Veiksmų srityje, skirtuke **Bendra**, grupėje **Ataskaitos**, pasirinkite **Turto gedimas**.</span><span class="sxs-lookup"><span data-stu-id="fa04c-128">On the Action Pane, on the **General** tab, in the **Reports** group, select **Asset fault**.</span></span>

4. <span data-ttu-id="fa04c-129">Įveskite konkretų laikotarpį arba pažymėkite gedimo tipą.</span><span class="sxs-lookup"><span data-stu-id="fa04c-129">Enter a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="fa04c-130">Pasirinkite **Gerai**, kad atspausdintumėte ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="fa04c-130">Select **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="fa04c-131">Norėdami atspausdinti kelių turtų arba turto tipų gedimų ataskaitą, pasirinkite **Turto valdymas** > **Ataskaitos** > **Turtas** > **Turto gedimas**.</span><span class="sxs-lookup"><span data-stu-id="fa04c-131">To print a fault report for several assets or asset types, select **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]