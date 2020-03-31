---
title: Parduotuvės darbo valandų kūrimas ir atnaujinimas
description: Šioje temoje aprašyta, kaip kurti ir atnaujinti parduotuvės darbo valandas naudojant „Commerce Headquarters“.
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 96ae5f33b1ab5fda98da4fc48b1fb883ca4d54b8
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024483"
---
# <a name="create-and-update-store-hours"></a><span data-ttu-id="d1229-103">Parduotuvės darbo valandų kūrimas ir atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="d1229-103">Create and update store hours</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="d1229-104">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="d1229-104">Overview</span></span>

<span data-ttu-id="d1229-105">Mažmenininkai vienoje vietoje gali kurti, prižiūrėti ir valdyti skirtingų parduotuvių įvairiuose geografiniuose regionuose darbo valandas.</span><span class="sxs-lookup"><span data-stu-id="d1229-105">From a single place, retailers can create, maintain, and manage the store hours for different stores across geographic regions.</span></span> <span data-ttu-id="d1229-106">Tada parduotuvės darbo valandos gali būti rodomos elektroninio kasos aparato (EKA) terminaluose.</span><span class="sxs-lookup"><span data-stu-id="d1229-106">The store hours can then be shown on point of sale (POS) terminals.</span></span> <span data-ttu-id="d1229-107">Tokiu būdu kasininkai gali su klientais bendrinti parduotuvės darbo valandas ir geriau padėti pirkėjams, kuriuos domina atsargos kitose parduotuvėse.</span><span class="sxs-lookup"><span data-stu-id="d1229-107">In this way, cashiers can share store hours with customers and better help shoppers who are interested in inventory in other stores.</span></span> <span data-ttu-id="d1229-108">Parduotuvės darbo valandos taip pat gali būti spausdinamos ant kvitų, jei vėliau klientai norėtų sugrįžti į parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="d1229-108">The store hours can also be printed on receipts, in case customers want to return to the store later.</span></span>

<span data-ttu-id="d1229-109">Skirtinguose kanaluose galima sukonfigūruoti įvairias parduotuvės darbo valandas.</span><span class="sxs-lookup"><span data-stu-id="d1229-109">Multiple store hours can be configured across different channels.</span></span> <span data-ttu-id="d1229-110">Šie kanalai apima fizines parduotuves, skambučių centrus, mobiliuosius įrenginius ir el. prekybos svetaines.</span><span class="sxs-lookup"><span data-stu-id="d1229-110">These channels include brick-and-mortar stores, call centers, mobile devices, and e-Commerce sites.</span></span>

<span data-ttu-id="d1229-111">Jei klientas turi kitos parduotuvės paėmimo užsakymą, kasininkas gali pasirinkti datas, kada toje parduotuvėje bus galima paimti prekes.</span><span class="sxs-lookup"><span data-stu-id="d1229-111">If a customer has a pickup order for a different store, the cashier can select dates when the pickup will be available in that store.</span></span> <span data-ttu-id="d1229-112">Parduotuvių peržvalgoje bus pateikta nuoroda į datas ir parduotuvių darbo laiką.</span><span class="sxs-lookup"><span data-stu-id="d1229-112">The store lookup will provide a reference to the dates and store times.</span></span> <span data-ttu-id="d1229-113">Kasininkas gali pasirinkti datą ir vietą bei atspausdinti paėmimo kvitą, kuriame bus nurodytos parduotuvės darbo valandos.</span><span class="sxs-lookup"><span data-stu-id="d1229-113">The cashier can select a date and location, and can also print a pickup receipt that includes the store hours.</span></span>

<span data-ttu-id="d1229-114">Ši funkcija pasiekiama „Microsoft Dynamics 365 Retail“ 8.1.2 ir naujesnėse versijose.</span><span class="sxs-lookup"><span data-stu-id="d1229-114">This functionality is available in Microsoft Dynamics 365 Retail versions 8.1.2 and later.</span></span>

## <a name="configure-store-hours"></a><span data-ttu-id="d1229-115">Parduotuvės darbo valandų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="d1229-115">Configure store hours</span></span>

<span data-ttu-id="d1229-116">Atlikite toliau nurodytus veiksmus, kad sukonfigūruotumėte parduotuvės darbo valandas.</span><span class="sxs-lookup"><span data-stu-id="d1229-116">Follow these steps to configure store hours.</span></span>

1. <span data-ttu-id="d1229-117">Eikite į **Mažmeninė prekyba ir prekyba** \> **Kanalų sąranka** \> **Parduotuvės darbo valandos**.</span><span class="sxs-lookup"><span data-stu-id="d1229-117">Go to **Retail and Commerce** \> **Channel Setup** \> **Store hours**.</span></span>
2. <span data-ttu-id="d1229-118">Pasirinkite **Naujas**, kad sukurtumėte naują parduotuvės darbo valandų šabloną.</span><span class="sxs-lookup"><span data-stu-id="d1229-118">Select **New** to create a new store hours template.</span></span> <span data-ttu-id="d1229-119">Norėdami naudoti esamą šabloną, pasirinkite šabloną kairiojoje srityje.</span><span class="sxs-lookup"><span data-stu-id="d1229-119">To use an existing template, select the template in the left pane.</span></span>
3. <span data-ttu-id="d1229-120">Dialogo lange **Intervalo įtraukimas** nustatykite datos intervalą, parduotuvės darbo valandas ir reikalingas šventines dienas.</span><span class="sxs-lookup"><span data-stu-id="d1229-120">In the **Add range** dialog box, define the date range, the store hours, and any holidays that are required.</span></span>

    - <span data-ttu-id="d1229-121">Jei parduotuvės darbo valandos nesikeičia, lauke **Pabaigos data** pasirinkite **Niekada nesibaigia**.</span><span class="sxs-lookup"><span data-stu-id="d1229-121">If store hours don't change, select **Never ends** in the **End date** field.</span></span>
    - <span data-ttu-id="d1229-122">Jei nustatomos konkretaus mėnesio, savaitės ar dienos parduotuvės darbo valandos, laukuose **Pradžios data** ir **Pabaigos data** nustatykite reikiamas datas.</span><span class="sxs-lookup"><span data-stu-id="d1229-122">If the store hours are for a specific month, week, or day, set the appropriate dates in the **Start Date** and **End date** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d1229-123">Gali sukurti kelis šablonus, kurių pradžios ir pabaigos datos persidengia.</span><span class="sxs-lookup"><span data-stu-id="d1229-123">You can create multiple templates that have overlapping start and end dates.</span></span> <span data-ttu-id="d1229-124">Todėl, pavyzdžiui, galite nustatyti skirtingose laiko juostose esančių parduotuvių darbo valandas.</span><span class="sxs-lookup"><span data-stu-id="d1229-124">Therefore, you can, for example, define store hours for stores in different time zones.</span></span>

    <span data-ttu-id="d1229-125">![Intervalo įtraukimo dialogo langas](../dev-itpro/media/Storehours1.png "Intervalo įtraukimo dialogo langas")</span><span class="sxs-lookup"><span data-stu-id="d1229-125">![Add range dialog box](../dev-itpro/media/Storehours1.png "Add range dialog box")</span></span>

4. <span data-ttu-id="d1229-126">Parduotuvės darbo valandų šabloną susiekite su parduotuvėmis, kuriose jis bus naudojamas.</span><span class="sxs-lookup"><span data-stu-id="d1229-126">Associate the store hours template with the stores where it will be used.</span></span> <span data-ttu-id="d1229-127">Dialogo lange **Pasirinkti organizacijos mazgus** pasirinkite parduotuves, regionus ir organizacijas, su kuriomis turėtų būti susietas šablonas.</span><span class="sxs-lookup"><span data-stu-id="d1229-127">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>

    - <span data-ttu-id="d1229-128">Su kiekviena parduotuve galima susieti tik vieną parduotuvės darbo valandų šabloną.</span><span class="sxs-lookup"><span data-stu-id="d1229-128">Only one store hours template can be associated with each store.</span></span>
    - <span data-ttu-id="d1229-129">Pasirinkite parduotuves, regionus ar organizacijas naudodami rodyklių mygtukus.</span><span class="sxs-lookup"><span data-stu-id="d1229-129">Use the arrow buttons to select stores, regions, or organizations.</span></span> <span data-ttu-id="d1229-130">Kalendorius bus pasiekiamas parduotuvėms ar parduotuvių grupėms ir matomas EKA.</span><span class="sxs-lookup"><span data-stu-id="d1229-130">The calendar will be available to the stores or store groups, and it will be visible at the POS for reference.</span></span>

    <span data-ttu-id="d1229-131">![Organizacijos mazgų pasirinkimo dialogo langas](../dev-itpro/media/Storehours2.png "Pasirinkti organizacijos mazgų dialogo langą")</span><span class="sxs-lookup"><span data-stu-id="d1229-131">![Choose organization nodes dialog box](../dev-itpro/media/Storehours2.png "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="d1229-132">Puslapyje **Paskirstymo grafikas** vykdykite **1070** ir **1090** užduotis, kad parduotuvės darbo valandos būtų pasiekiamos EKA.</span><span class="sxs-lookup"><span data-stu-id="d1229-132">On the **Distribution schedule** page, run the **1070** and **1090** jobs to make the store hours available to the POS.</span></span>

## <a name="add-store-hours-to-printed-receipts"></a><span data-ttu-id="d1229-133">Parduotuvės darbo valandų įtraukimas į išspausdintus kvitus</span><span class="sxs-lookup"><span data-stu-id="d1229-133">Add store hours to printed receipts</span></span>

<span data-ttu-id="d1229-134">Norėdami parduotuvės darbo valandas įtraukti į išspausdintus EKA kvitus, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d1229-134">Follow these steps to add store hours to the printed POS receipts.</span></span>

1. <span data-ttu-id="d1229-135">Atidarykite kvito dizaino įrankį.</span><span class="sxs-lookup"><span data-stu-id="d1229-135">Open the receipt designer.</span></span>
2. <span data-ttu-id="d1229-136">Apatiniame kairiajame kampe pasirinkite **Poraštė**.</span><span class="sxs-lookup"><span data-stu-id="d1229-136">Select **Footer** in the lower-left corner.</span></span>
3. <span data-ttu-id="d1229-137">Elementą **Parduotuvės darbo valandos** iš kairiosios srities nuvilkite į kvito šablono apačioje esančią poraštę.</span><span class="sxs-lookup"><span data-stu-id="d1229-137">Drag the **Store hours** element from the left pane to the footer at the bottom of the receipt template.</span></span>
4. <span data-ttu-id="d1229-138">Jei reikia, galite redaguoti elemento **Parduotuvės darbo valandos** numatytąją žymą.</span><span class="sxs-lookup"><span data-stu-id="d1229-138">You can edit the default label on the **Store hours** element as you require.</span></span>
5. <span data-ttu-id="d1229-139">Įrašykite kvitą ir uždarykite kvitų dizaino įrankį.</span><span class="sxs-lookup"><span data-stu-id="d1229-139">Save the receipt, and close the receipt designer.</span></span>
6. <span data-ttu-id="d1229-140">Puslapyje **Paskirstymo grafikas** vykdykite **1070** ir **1090** užduotis.</span><span class="sxs-lookup"><span data-stu-id="d1229-140">On the **Distribution schedule** page, run the **1070** and **1090** jobs.</span></span>
7. <span data-ttu-id="d1229-141">Prisijunkite prie EKA.</span><span class="sxs-lookup"><span data-stu-id="d1229-141">Sign in to the POS.</span></span>
8. <span data-ttu-id="d1229-142">Užbaikite pardavimą ir pasirinkite spausdinti kvitą.</span><span class="sxs-lookup"><span data-stu-id="d1229-142">Complete a sale, and select to print a receipt.</span></span>

<span data-ttu-id="d1229-143">Dabar EKA kvituose nurodomos parduotuvės darbo valandos.</span><span class="sxs-lookup"><span data-stu-id="d1229-143">POS receipts now include the store hours.</span></span> <span data-ttu-id="d1229-144">Jei į šabloną buvo įtraukta šventinių dienų, jos rodomos ant kvito.</span><span class="sxs-lookup"><span data-stu-id="d1229-144">If any holidays were included in the template, they are shown on the receipt.</span></span>

<span data-ttu-id="d1229-145">![Kvito pavyzdys](../dev-itpro/media/Storehours3.png "Kvito pavyzdys")</span><span class="sxs-lookup"><span data-stu-id="d1229-145">![Receipt example](../dev-itpro/media/Storehours3.png "Receipt example")</span></span>