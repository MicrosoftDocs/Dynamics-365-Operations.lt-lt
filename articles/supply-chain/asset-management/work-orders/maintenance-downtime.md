---
title: Darbo užsakymų prižiūrimo turto prastova
description: Šioje temoje aprašoma, kaip galite kurti darbo užsakyme pasirinkto turto prižiūrimo turto prastovos registracijas.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 263a044a0a378e95ea271ac1c6f468f9e3287f26
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/14/2020
ms.locfileid: "3802730"
---
# <a name="maintenance-downtime-for-work-orders"></a><span data-ttu-id="c72b1-103">Darbo užsakymų prižiūrimo turto prastova</span><span class="sxs-lookup"><span data-stu-id="c72b1-103">Maintenance downtime for work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="c72b1-104">Galite kurti darbo užsakyme pasirinkto turto prižiūrimo turto prastovos registracijas.</span><span class="sxs-lookup"><span data-stu-id="c72b1-104">You can create maintenance downtime registrations on the asset that is selected on a work order.</span></span> <span data-ttu-id="c72b1-105">Ši galimybė naudinga, jei norite registruoti vienos arba keleto gamybos srityje esančių mašinų prižiūrimo turto prastovą.</span><span class="sxs-lookup"><span data-stu-id="c72b1-105">This capability is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="c72b1-106">Pirma kuriate norimus naudoti prižiūrimo turto prastovos priežasčių kodus, pavyzdžiui, **gedimą** ir **planinį sustabdymą**.</span><span class="sxs-lookup"><span data-stu-id="c72b1-106">You first create the maintenance downtime reason codes that you want to use, such as **Breakdown** and **Planned stop**.</span></span> <span data-ttu-id="c72b1-107">Tai daroma puslapyje **Prižiūrimo turto prastovos priežasčių kodai**.</span><span class="sxs-lookup"><span data-stu-id="c72b1-107">This step is done on the **Maintenance downtime reason codes** page.</span></span> <span data-ttu-id="c72b1-108">Paskui puslapyje **Prižiūrimo turto prastova** galite kurti prižiūrimo turto prastovos registracijas ir įtraukti atitinkamus prižiūrimo turto prastovos priežasčių kodus.</span><span class="sxs-lookup"><span data-stu-id="c72b1-108">You can then create maintenance downtime registrations on the **Maintenance downtime** page and add the relevant maintenance downtime reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="c72b1-109">Prižiūrimo turto prastovos priežasčių kodų kūrimas</span><span class="sxs-lookup"><span data-stu-id="c72b1-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="c72b1-110">Pasirinkite **Turto valdymas** > **Sąranka** > **Darbo užsakymai** > **Prižiūrimo turto prastovos priežasčių kodai**.</span><span class="sxs-lookup"><span data-stu-id="c72b1-110">Select **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="c72b1-111">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="c72b1-111">Select **New**.</span></span>

3. <span data-ttu-id="c72b1-112">Lauke **Prižiūrimo turto prastovos priežasties kodas** įveskite prižiūrimo turto prastovos priežasties kodo ID.</span><span class="sxs-lookup"><span data-stu-id="c72b1-112">In the **Maintenance downtime reason code** field, enter an ID for the maintenance downtime reason code.</span></span>

4. <span data-ttu-id="c72b1-113">Tada lauke **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c72b1-113">In the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="c72b1-114">Pažymėkite žymės langelį **Įtraukti į KPI**, jei priežasties kodas turi būti įtrauktas į turto pagrindinių efektyvumo indikatorių (KPI) skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="c72b1-114">Select the **KPI include** check box if the reason code should be included in calculations of key performance indicators (KPIs) for the asset.</span></span> <span data-ttu-id="c72b1-115">Paprastai planiniai gamybos sustabdymai neturėtų būti įtraukiami į KPI skaičiavimus, nes jie nedaro įtakos numatomiems rezultatams.</span><span class="sxs-lookup"><span data-stu-id="c72b1-115">In general, planned production stops should not be included in KPI calculations, because they don't affect expected performance.</span></span>

6. <span data-ttu-id="c72b1-116">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="c72b1-116">Select **Save**.</span></span>

<span data-ttu-id="c72b1-117">Paveikslėlyje pavaizduotas puslapio **Prižiūrimo turto prastovos priežasčių kodai** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="c72b1-117">The illustration below shows an example of the **Maintenance downtime reason codes** page.</span></span>

![1 pav.](media/15-work-orders.png)

<span data-ttu-id="c72b1-119">Sukūrę norimus naudoti prižiūrimo turto prastovos priežasčių kodus, galite kurti darbo užsakymų ir turto prižiūrimo turto prastovos registracijas.</span><span class="sxs-lookup"><span data-stu-id="c72b1-119">After you've created the maintenance downtime reason codes that you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="c72b1-120">Prižiūrimo turto prastovos registracijų kūrimas</span><span class="sxs-lookup"><span data-stu-id="c72b1-120">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="c72b1-121">Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="c72b1-121">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="c72b1-122">Pasirinkite darbo užsakymą, tada skirtuke **Darbo užsakymas**, grupėje **Turtas**, pasirinkite **Prižiūrimo turto prastova**.</span><span class="sxs-lookup"><span data-stu-id="c72b1-122">Select the work order, and then, on the **Work order** tab, in the **Asset** group, select **Maintenance downtime**.</span></span>

3. <span data-ttu-id="c72b1-123">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="c72b1-123">Select **New**.</span></span>

4. <span data-ttu-id="c72b1-124">Laukuose **Nuo** ir **Iki** įterpkite prižiūrimo turto prastovos registracijos datą ir laiko intervalą.</span><span class="sxs-lookup"><span data-stu-id="c72b1-124">In the **From** and **To** fields, define the date and time interval for the maintenance downtime registration.</span></span>

>[!NOTE]
><span data-ttu-id="c72b1-125">Kai paliekate lauką **Iki**, trukmė valandomis automatiškai įterpiamą į lauką **Trukmė**.</span><span class="sxs-lookup"><span data-stu-id="c72b1-125">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

5. <span data-ttu-id="c72b1-126">Lauke **Prižiūrimo turto prastovos priežasties kodas** pasirinkite priežasties kodą.</span><span class="sxs-lookup"><span data-stu-id="c72b1-126">In the **maintenance downtime reason code** field, select a reason code.</span></span>

6. <span data-ttu-id="c72b1-127">Norėdami pridėti daugiau registravimų, kartokite 3–5 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c72b1-127">Repeat steps 3 through 5 to add more registrations.</span></span>

7. <span data-ttu-id="c72b1-128">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="c72b1-128">Select **Save**.</span></span>

<span data-ttu-id="c72b1-129">Toliau pateikiamoje iliustracijoje rodomas prižiūrimo turto prastovos registravimo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="c72b1-129">The illustration below shows an example of maintenance downtime registration.</span></span>

![2 pav.](media/16-work-orders.png)

<span data-ttu-id="c72b1-131">Kalendorius, naudojamas apskaičiuojant prižiūrimo turto prastovos registraciją, priklauso nuo jūsų pasirinkimo turto ir parametrų sąrankoje.</span><span class="sxs-lookup"><span data-stu-id="c72b1-131">The calendar that is used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="c72b1-132">Jei turto išteklius pasirenkamas perėjus į puslapio **Visas turtas** „FastTab” **Ilgalaikis turtas** lauką **Ištekliai**, naudojama susijusios išteklių grupės kalendoriaus sąranka, kaip parodyta toliau pateikiamame paveikslėlyje.</span><span class="sxs-lookup"><span data-stu-id="c72b1-132">If a resource is selected on an asset in the **Resource** field on the **Fixed asset** FastTab of the **All assets** page, the calendar that is set up for the associated resource group is used, as shown in the following illustration.</span></span>

![3 pav.](media/17-work-orders.png)

<span data-ttu-id="c72b1-134">Jei turto išteklius nepasirenkamas, naudojamas standartinis kalendorius, pasirinktas puslapyje **Turto valdymo parametrai**, kaip parodyta toliau pateikiamame paveikslėlyje.</span><span class="sxs-lookup"><span data-stu-id="c72b1-134">If no resource is selected on the asset, the standard calendar that is selected on the **Asset management parameters** page is used, as shown in the following illustration.</span></span>

![4 pav.](media/18-work-orders.png)

<span data-ttu-id="c72b1-136">Spustelėkite **Turto valdymas** > **Užklausos** > **Prižiūrimo turto prastova**, kad pamatytumėte visų prižiūrimo turto prastovos registracijų apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="c72b1-136">To see an overview of all maintenance downtime registrations, click **Asset management** > **Inquiries** > **Maintenance downtime**.</span></span>

>[!NOTE]
><span data-ttu-id="c72b1-137">Visi modulyje **Turto valdymas** naudojami kalendoriai nustatomi pasirinkus **Organizacijos administravimas** > **Sąranka** > **Kalendoriai** > **Kalendoriai**.</span><span class="sxs-lookup"><span data-stu-id="c72b1-137">All calendars that are used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

