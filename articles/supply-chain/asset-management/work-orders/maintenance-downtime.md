---
title: Prižiūrimo turto prastova
description: Šioje temoje aprašoma prižiūrimo turto prastova modulyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918249"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="eda68-103">Prižiūrimo turto prastova</span><span class="sxs-lookup"><span data-stu-id="eda68-103">Maintenance downtime</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="eda68-104">Galite kurti darbo užsakyme pasirinkto turto prižiūrimo turto prastovos registracijas.</span><span class="sxs-lookup"><span data-stu-id="eda68-104">You can create maintenance downtime registrations on the asset selected on a work order.</span></span> <span data-ttu-id="eda68-105">Tai naudinga, jei norite registruoti vienos arba keleto gamybos srityje esančių mašinų prižiūrimo turto prastovą.</span><span class="sxs-lookup"><span data-stu-id="eda68-105">This is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="eda68-106">Pirma kuriate norimus naudoti prižiūrimo turto prastovos priežasčių kodus, pavyzdžiui, gedimą ir planinį sustabdymą.</span><span class="sxs-lookup"><span data-stu-id="eda68-106">First, you create the maintenance downtime reason codes that you want to use, for example, breakdown and planned stop.</span></span> <span data-ttu-id="eda68-107">Tai daroma pasirinkus **Prižiūrimo turto prastovos priežasčių kodai**.</span><span class="sxs-lookup"><span data-stu-id="eda68-107">This is done in **Maintenance downtime reason codes**.</span></span> <span data-ttu-id="eda68-108">Paskui galite kurti prižiūrimo turto prastovos registracijas, pasirinkę **Prižiūrimo turto prastova**, ir įtraukti atitinkamus priežasčių kodus.</span><span class="sxs-lookup"><span data-stu-id="eda68-108">Next, you can create maintenance downtime registrations in **Maintenance downtime** and add the relevant reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="eda68-109">Prižiūrimo turto prastovos priežasčių kodų kūrimas</span><span class="sxs-lookup"><span data-stu-id="eda68-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="eda68-110">Spustelėkite **Turto valdymas** > **Sąranka** > **Darbo užsakymai** > **Prižiūrimo turto prastovos priežasčių kodai**.</span><span class="sxs-lookup"><span data-stu-id="eda68-110">Click **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="eda68-111">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="eda68-111">Click **New**.</span></span>

3. <span data-ttu-id="eda68-112">Į lauką **Prižiūrimo turto prastovos priežasties kodas** įterpkite ID.</span><span class="sxs-lookup"><span data-stu-id="eda68-112">Insert an ID in the **Maintenance downtime reason code** field.</span></span>

4. <span data-ttu-id="eda68-113">Lauke **Pavadinimas** įveskite priežasties kodo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="eda68-113">Insert a name for the reason code in the **Name** field.</span></span>

5. <span data-ttu-id="eda68-114">Pažymėkite žymės langelį **Įtraukti į KPI**, jei priežasties kodas turėtų būti įtrauktas į turto KPI skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="eda68-114">Select the **KPI include** check box if the reason code should be included in asset KPI calculations.</span></span> <span data-ttu-id="eda68-115">Paprastai planiniai gamybos sustabdymai neturėtų būti įtraukiami į KPI skaičiavimus, nes jie nedaro įtakos numatomiems rezultatams.</span><span class="sxs-lookup"><span data-stu-id="eda68-115">Generally, planned production stops should not be included in KPI calculations as they do not impact expected performance.</span></span>

6. <span data-ttu-id="eda68-116">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="eda68-116">Click **Save**.</span></span>

![1 pav.](media/15-work-orders.png)


<span data-ttu-id="eda68-118">Sukūrę norimus naudoti prižiūrimo turto prastovos priežasčių kodus, galite kurti darbo užsakymų ir turto prižiūrimo turto prastovos registracijas.</span><span class="sxs-lookup"><span data-stu-id="eda68-118">When you have created the maintenance downtime reason codes you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="eda68-119">Prižiūrimo turto prastovos registracijų kūrimas</span><span class="sxs-lookup"><span data-stu-id="eda68-119">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="eda68-120">Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="eda68-120">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="eda68-121">Pasirinkite darbo užsakymą ir spustelėkite **Prižiūrimo turto prastova**.</span><span class="sxs-lookup"><span data-stu-id="eda68-121">Select the work order and click **Maintenance downtime**.</span></span>

3. <span data-ttu-id="eda68-122">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="eda68-122">Click **New**.</span></span>

4. <span data-ttu-id="eda68-123">Įterpkite prižiūrimo turto prastovos registracijos datą ir laiko intervalą laukuose **Nuo** ir **Iki**.</span><span class="sxs-lookup"><span data-stu-id="eda68-123">Insert date and time interval for the maintenance downtime registration in the **From** and **To** fields.</span></span>

5. <span data-ttu-id="eda68-124">Kai paliekate lauką **Iki**, trukmė valandomis automatiškai įterpiamą į lauką **Trukmė**.</span><span class="sxs-lookup"><span data-stu-id="eda68-124">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

6. <span data-ttu-id="eda68-125">Lauke **Prižiūrimo turto prastovos priežasties kodas** pasirinkite priežasties kodą.</span><span class="sxs-lookup"><span data-stu-id="eda68-125">Select a reason code in the **maintenance downtime reason code** field.</span></span>

7. <span data-ttu-id="eda68-126">Jei norite įtraukti daugiau registracijų, pakartokite 3–6 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="eda68-126">Repeat steps 3-6 if you want to add more registrations.</span></span>

8. <span data-ttu-id="eda68-127">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="eda68-127">Click **Save**.</span></span>


![2 paveikslėlis](media/16-work-orders.png)


<span data-ttu-id="eda68-129">Kalendorius, naudojamas apskaičiuojant prižiūrimo turto prastovos registraciją, priklauso nuo jūsų pasirinkimo turto ir parametrų sąrankoje.</span><span class="sxs-lookup"><span data-stu-id="eda68-129">The calendar used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="eda68-130">Jei turto išteklius pasirenkamas perėjus į **Visas turtas** > FastTab **Ilgalaikis turtas** > lauką **Išteklius**, naudojama susijusios išteklių grupės kalendoriaus sąranka, kaip parodyta toliau pateikiamame paveikslėlyje.</span><span class="sxs-lookup"><span data-stu-id="eda68-130">If a resource is selected on an asset in **All assets** > **Fixed asset** FastTab > **Resource** field, the calendar set up for the associated resource group is used, as shown in the following figure.</span></span>

![3 paveikslėlis](media/17-work-orders.png)


<span data-ttu-id="eda68-132">Jei turto išteklius nepasirenkamas, naudojamas standartinis kalendorius, pasirinktas **Turto valdymo parametrai**, kaip parodyta toliau pateikiamame paveikslėlyje.</span><span class="sxs-lookup"><span data-stu-id="eda68-132">If no resource is selected on the asset, the standard calendar selected in **Asset management parameters** is used, as shown in the following figure.</span></span>

![4 paveikslėlis](media/18-work-orders.png)


<span data-ttu-id="eda68-134">Spustelėkite **Įmonių turto valdymas** > **Užklausos** > **Prižiūrimo turto prastova**, kad pamatytumėte visų prižiūrimo turto prastovos registracijų apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="eda68-134">Click **Enterprise asset management** > **Inquiries** > **Maintenance downtime** to see an overview of all maintenance downtime registrations.</span></span>

>[!NOTE]
><span data-ttu-id="eda68-135">Visi modulyje **Turto valdymas** naudojami kalendoriai nustatomi pasirinkus **Organizacijos administravimas** > **Sąranka** > **Kalendoriai** > **Kalendoriai**.</span><span class="sxs-lookup"><span data-stu-id="eda68-135">All calendars used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

