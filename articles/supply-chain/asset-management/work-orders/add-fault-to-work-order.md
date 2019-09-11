---
title: Gedimo įtraukimas į darbo užsakymą
description: Šioje temoje aprašoma, kaip įtraukti gedimų registracijas į darbo užsakymus turto valdyme.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875803"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="3edf9-103">Gedimo įtraukimas į darbo užsakymą</span><span class="sxs-lookup"><span data-stu-id="3edf9-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="3edf9-104">Galite įtraukti gedimų sąranką į darbo užsakymą gedimų dizaino įrankyje.</span><span class="sxs-lookup"><span data-stu-id="3edf9-104">You can add faults set up in the fault designer to a work order.</span></span> <span data-ttu-id="3edf9-105">Darbo užsakyme pažymėtame turte turi būti nurodyti turto tipai, kurie turi vieną arba daugiau susijusių gedimo įrašų.</span><span class="sxs-lookup"><span data-stu-id="3edf9-105">The asset selected in the work order must contain asset types that have one or more fault records connected to it.</span></span> <span data-ttu-id="3edf9-106">Apie sąranką daugiau skaitykite skyriuje [Gedimų valdymas](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="3edf9-106">Read more about setup in the [Fault management](../setup-for-work-orders/fault-management.md) section.</span></span>

1. <span data-ttu-id="3edf9-107">Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="3edf9-107">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="3edf9-108">Sąraše pažymėkite darbo užsakymą, į kurį norite įtraukti gedimo registraciją, ir spustelėkite **Turto gedimas**.</span><span class="sxs-lookup"><span data-stu-id="3edf9-108">In the list, select the work order on which you want to make a fault registration and click **Asset fault**.</span></span>

3. <span data-ttu-id="3edf9-109">„FastTab“ **Požymiai** spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="3edf9-109">On the **Symptoms** FastTab, click **Add line**.</span></span> <span data-ttu-id="3edf9-110">Gedimo numeris pagal eilės tvarką automatiškai įtraukiamas į lauką **Gedimas**.</span><span class="sxs-lookup"><span data-stu-id="3edf9-110">A sequential fault number is automatically inserted in the **Fault** field.</span></span>

4. <span data-ttu-id="3edf9-111">Lauke **Gedimo požymis** pažymėkite susijusį požymį.</span><span class="sxs-lookup"><span data-stu-id="3edf9-111">Select the relevant symptom in the **Fault symptom** field.</span></span>

5. <span data-ttu-id="3edf9-112">Pažymėkite **Gedimo sritis** ir **Gedimo tipas**.</span><span class="sxs-lookup"><span data-stu-id="3edf9-112">Select **Fault area** and **Fault type**.</span></span>

6. <span data-ttu-id="3edf9-113">Į lauką **Gedimo data** automatiškai įtraukiama esama data.</span><span class="sxs-lookup"><span data-stu-id="3edf9-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="3edf9-114">Jei reikia, galite pažymėti kitą datą.</span><span class="sxs-lookup"><span data-stu-id="3edf9-114">You can select another date, if necessary.</span></span>

7. <span data-ttu-id="3edf9-115">„FastTab“ **Pažymėto simptomo priežastys** įtraukite eilutę, aprašančią problemos priežastį.</span><span class="sxs-lookup"><span data-stu-id="3edf9-115">On the **Causes for selected symptom** FastTab, add a line describing the cause of the problem.</span></span>

8. <span data-ttu-id="3edf9-116">„FastTab“ **Pažymėto simptomo šalinimo priemonės** įtraukite eilutę, aprašančią galimą problemos sprendimą.</span><span class="sxs-lookup"><span data-stu-id="3edf9-116">On the **Remedies for selected symptom** FastTab, add a line describing a possible solution to the problem.</span></span>

9. <span data-ttu-id="3edf9-117">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3edf9-117">Click **Save**.</span></span>

![1 pav.](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="3edf9-119">Turto gedimų rodinys</span><span class="sxs-lookup"><span data-stu-id="3edf9-119">View asset faults</span></span>

<span data-ttu-id="3edf9-120">Sąraše **Turto gedimai** galite peržiūrėti visus užregistruotus turto gedimus.</span><span class="sxs-lookup"><span data-stu-id="3edf9-120">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="3edf9-121">Spustelėkite **Turto valdymas** > **Užklausos** > **Turto gedimas** > **Turto gedimai**, kad atidarytumėte sąrašą.</span><span class="sxs-lookup"><span data-stu-id="3edf9-121">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults** to open the list.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="3edf9-122">Turto gedimo ataskaitos spausdinimas</span><span class="sxs-lookup"><span data-stu-id="3edf9-122">Print asset fault report</span></span>

<span data-ttu-id="3edf9-123">Sąrašo puslapyje **Visas turtas** galite atspausdinti turto gedimo ataskaitą, kurioje rodomi visos gedimų registracijos ir grafinė gedimų statistikos apžvalga.</span><span class="sxs-lookup"><span data-stu-id="3edf9-123">From the **All assets** list page, you can print an asset fault report displaying all fault registrations as well as a graphic overview of fault statistics.</span></span>

1. <span data-ttu-id="3edf9-124">Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Turtas** > **Visas turtas**.</span><span class="sxs-lookup"><span data-stu-id="3edf9-124">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="3edf9-125">Sąraše **Turtas** pažymėkite turtą, kurio gedimų ataskaitą norite atspausdinti.</span><span class="sxs-lookup"><span data-stu-id="3edf9-125">In the **Assets** list, select the asset for which you want to print a fault report.</span></span>

3. <span data-ttu-id="3edf9-126">Skirtuke **Bendra**> **Ataskaitų skyrius** spustelėkite **Turto gedimas**.</span><span class="sxs-lookup"><span data-stu-id="3edf9-126">On the **General** tab > **Reports section**, click **Asset fault**.</span></span>

4. <span data-ttu-id="3edf9-127">Įveskite konkretų periodą arba pažymėkite gedimo tipą.</span><span class="sxs-lookup"><span data-stu-id="3edf9-127">Insert a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="3edf9-128">Spustelėkite **Gerai** norėdami atspausdinti ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="3edf9-128">Click **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="3edf9-129">Taip pat galite atspausdinti kelių turtų arba turto tipų gedimo ataskaitą spustelėdami **Turto valdymas** > **Ataskaitos** > **Turtas** > **Turto gedimas**.</span><span class="sxs-lookup"><span data-stu-id="3edf9-129">You can also print a fault report for several assets or asset types by clicking **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

