---
title: Gamybos nustatymo reikalavimai
description: Šiame straipsnyje pateikiama informacija apie nustatymo reikalavimus prieš dirbant su Gamybos kontrole.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 55820d7376750c210d2b7f214f705ffcb222c6cd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212508"
---
# <a name="production-setup-requirements"></a><span data-ttu-id="59319-103">Gamybos nustatymo reikalavimai</span><span class="sxs-lookup"><span data-stu-id="59319-103">Production setup requirements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59319-104">Šiame straipsnyje pateikiama informacija apie nustatymo reikalavimus prieš dirbant su Gamybos kontrole.</span><span class="sxs-lookup"><span data-stu-id="59319-104">This article provides information about setup requirements before you can work with Production control.</span></span> 

<span data-ttu-id="59319-105">Gamybos kontrolė yra integruota su kitų modulių funkcijomis.</span><span class="sxs-lookup"><span data-stu-id="59319-105">Production control is integrated with features in other modules.</span></span> <span data-ttu-id="59319-106">Šis tarpusavio ryšys leidžia pakeisti gamybos užsakymus ir užtikrinti, kad jie būtų automatiškai atnaujinami visuose kituose susijusiuose sistemos procesuose ir skaičiavimuose.</span><span class="sxs-lookup"><span data-stu-id="59319-106">This interconnectivity lets you change production orders and make sure that they are automatically updated in all other related processes and calculations in the system.</span></span> <span data-ttu-id="59319-107">Toliau nurodyti sąrankos procesai išvardyti tokia tvarka, kokia juos turėtumėte atlikti.</span><span class="sxs-lookup"><span data-stu-id="59319-107">The following setup processes are listed in the order that you should complete them in.</span></span>

## <a name="required-baseline-setup-in-other-modules"></a><span data-ttu-id="59319-108">Kituose modeliuose būtinas pradinis nustatymas</span><span class="sxs-lookup"><span data-stu-id="59319-108">Required baseline setup in other modules</span></span>
<span data-ttu-id="59319-109">Prieš dirbant su Gamybos kontrole, turi būti nustatyta informacija kituose moduliuose.</span><span class="sxs-lookup"><span data-stu-id="59319-109">Information in other modules must be set up before you can work with Production control.</span></span> <span data-ttu-id="59319-110">Ši sąranka apima toliau nurodytas užduotis.</span><span class="sxs-lookup"><span data-stu-id="59319-110">This setup includes the following tasks:</span></span>

-   <span data-ttu-id="59319-111">Nustatyti bendrą įmonės informaciją.</span><span class="sxs-lookup"><span data-stu-id="59319-111">Set up general company information.</span></span>
-   <span data-ttu-id="59319-112">Nustatyti DK.</span><span class="sxs-lookup"><span data-stu-id="59319-112">Set up the general ledger.</span></span>
-   <span data-ttu-id="59319-113">Apibrėžti prekių grupes.</span><span class="sxs-lookup"><span data-stu-id="59319-113">Define item groups.</span></span>
-   <span data-ttu-id="59319-114">Prekių grupėms nustatyti DK sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="59319-114">Set up ledger accounts for item groups.</span></span>
-   <span data-ttu-id="59319-115">Srityje Atsargų valdymas nustatyti atsargų prekių lentelę.</span><span class="sxs-lookup"><span data-stu-id="59319-115">Set up the inventory item table in Inventory management.</span></span>
-   <span data-ttu-id="59319-116">Srityje Atsargų valdymas sukurti komplektavimo specifikacijas (KS) ir KS versijas.</span><span class="sxs-lookup"><span data-stu-id="59319-116">Create bills of materials (BOMs) and BOM versions in Inventory management.</span></span>

## <a name="required-calendar-and-resource-setup"></a><span data-ttu-id="59319-117">Būtina kalendoriaus ir išteklių sąranka</span><span class="sxs-lookup"><span data-stu-id="59319-117">Required calendar and resource setup</span></span>
<span data-ttu-id="59319-118">Prieš naudodami Gamybos kontrolę, atidarykite modulį Organizacijos administravimas ir toliau nurodyta tvarka sukurkite bei apibrėžkite kalendorių ir operacijų išteklius.</span><span class="sxs-lookup"><span data-stu-id="59319-118">Before you use Production control, open Organization administration, and create and define the calendar and operations resources in the following order:</span></span>

1.  <span data-ttu-id="59319-119">**Darbo laiko šablonai** – nustatyti darbo laiko šablonus, siekiant apibrėžti laiką, kuris galimas gamybai planuoti.</span><span class="sxs-lookup"><span data-stu-id="59319-119">**Working time templates** – Set up working time templates to define the times that are available for production scheduling.</span></span>
2.  <span data-ttu-id="59319-120">**Kalendoriai** – nustatyti darbo valandų kalendorius, siekiant apibrėžti, kurios metų dienos galimos gamybai planuoti.</span><span class="sxs-lookup"><span data-stu-id="59319-120">**Calendars** – Set up working time calendars to define the days of the year that are available for production scheduling.</span></span>
3.  <span data-ttu-id="59319-121">**Išteklių grupės** – nustatyti išteklių grupes, siekiant grupuoti operacijų išteklius, kad, vykdant planavimą, būtų galima matyti visų laisvų pajėgumų apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="59319-121">**Resource groups** – Set up resource groups to group the operations resources, so that you can get an overview of any free capacity when you run scheduling.</span></span> <span data-ttu-id="59319-122">Prieš nustatant operacijų išteklius, nustatyti išteklių grupių nereikia.</span><span class="sxs-lookup"><span data-stu-id="59319-122">You don't have to set up resource groups before you set up operations resources.</span></span> <span data-ttu-id="59319-123">Tačiau rekomenduojame žinoti, kaip, nustatant gamybos kontrolę, grupuoti išteklius.</span><span class="sxs-lookup"><span data-stu-id="59319-123">However, we recommend that you understand how to group resources when you set up Production control.</span></span>
4.  <span data-ttu-id="59319-124">**Ištekliai** – nustatyti operacijų išteklius, siekiant apibrėžti skirtingus išteklius, naudojamus gamybos procesui užbaigti ir pajėgumams planuoti.</span><span class="sxs-lookup"><span data-stu-id="59319-124">**Resources** – Set up operations resources to define the resources that are used to complete the production process and plan for capacity.</span></span>

## <a name="required-production-parameters-setup"></a><span data-ttu-id="59319-125">Būtinas gamybos parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="59319-125">Required production parameters setup</span></span>
<span data-ttu-id="59319-126">**Gamybos kontrolės parametrai** – nustatyti pagrindinius gamybos parametrus, siekiant apibrėžti, kaip sistema tvarko ir apdoroja gamybos užsakymus.</span><span class="sxs-lookup"><span data-stu-id="59319-126">**Production control parameters** – Set up basic production parameters to define how the system handles and processes production orders.</span></span> <span data-ttu-id="59319-127">Apibrėžti, kaip gamybos užsakymai kuriami, vertinami, planuojami ir naudojami.</span><span class="sxs-lookup"><span data-stu-id="59319-127">Define how production orders are created, estimated, scheduled, and consumed.</span></span> <span data-ttu-id="59319-128">Taip pat galima pasirinkti norimą grįžtamojo ryšio rūšį ir kaip turėtų būti atliekama išlaidų apskaita.</span><span class="sxs-lookup"><span data-stu-id="59319-128">You can also select what kind of feedback you want and how cost accounting is done.</span></span>

## <a name="required-journal-name-identification"></a><span data-ttu-id="59319-129">Būtinas žurnalo pavadinimo identifikavimas</span><span class="sxs-lookup"><span data-stu-id="59319-129">Required journal name identification</span></span>
<span data-ttu-id="59319-130">**Gamybos žurnalų pavadinimai** – nurodyti gamybos žurnalų pavadinimus, kurie naudojami įrašyti ir registruoti operacijoms.</span><span class="sxs-lookup"><span data-stu-id="59319-130">**Production journal names** – Specify the production journal names that are used to record and post transactions.</span></span>

## <a name="setup-if-you-use-operations"></a><span data-ttu-id="59319-131">Nustatyti, jei naudojamos operacijos</span><span class="sxs-lookup"><span data-stu-id="59319-131">Setup if you use operations</span></span>
<span data-ttu-id="59319-132">Operacijos rodo tam tikrą veiklą, atliekamą siekiant pagaminti galutinį produktą.</span><span class="sxs-lookup"><span data-stu-id="59319-132">Operations represent the specific activities that are completed to produce the finished product.</span></span> <span data-ttu-id="59319-133">**Pastaba:** norėdami pagaminti prekę, turite žinoti reikiamų veiklų tipus ir tvarką bei prioritetus.</span><span class="sxs-lookup"><span data-stu-id="59319-133">**Note:** You must know the types of activities that are required in order to produce your item, and the order and priorities of those activities.</span></span> <span data-ttu-id="59319-134">Taip pat turite žinoti, kurie ištekliai naudojami, ir kiek.</span><span class="sxs-lookup"><span data-stu-id="59319-134">You must also know which resources are involved, and how many.</span></span>

1.  <span data-ttu-id="59319-135">**Operacijos** – nustatyti operacijas, rodančias užduotis, kurios turi būti atliktos galutinei prekei pagaminti.</span><span class="sxs-lookup"><span data-stu-id="59319-135">**Operations** – Set up operations to represent the tasks that must be completed to produce the finished item.</span></span>
2.  <span data-ttu-id="59319-136">**Ryšiai** – nustatyti operacijų ryšius, siekiant nustatyti tikslias ypatybes.</span><span class="sxs-lookup"><span data-stu-id="59319-136">**Relations** – Set up operation relations to establish detailed properties.</span></span> <span data-ttu-id="59319-137">Norėdami nustatyti operacijų ryšius, puslapyje **Operacijos** spustelėkite **Ryšiai**.</span><span class="sxs-lookup"><span data-stu-id="59319-137">To define operation relations, click **Relations** on the **Operations** page.</span></span>

## <a name="setup-if-you-use-routes"></a><span data-ttu-id="59319-138">Nustatyti, jei naudojami maršrutai</span><span class="sxs-lookup"><span data-stu-id="59319-138">Setup if you use routes</span></span>
<span data-ttu-id="59319-139">Jei naudojate maršrutus, operacijos turi būti apibrėžtos kiekvienam nustatytam gamybos maršrutui.</span><span class="sxs-lookup"><span data-stu-id="59319-139">If you're working with routes, operations must be defined for every production route that you set up.</span></span> <span data-ttu-id="59319-140">Maršrutas rodo kelią, kurį prekė įveikia nuo operacijos iki operacijos, nuo gamybos proceso pradžios iki pabaigos.</span><span class="sxs-lookup"><span data-stu-id="59319-140">The route represents the path that the item takes from operation to operation, from the start of the production process to the end.</span></span>

1.  <span data-ttu-id="59319-141">**Išlaidų kategorijos** – nustatyti išlaidų kategorijas, siekiant apibrėžti nustatytų procesų valandines išlaidas ir sąrankos laiką.</span><span class="sxs-lookup"><span data-stu-id="59319-141">**Cost categories** – Set up cost categories to define the cost per hour of specified processes and setup times.</span></span>
2.  <span data-ttu-id="59319-142">**Išlaidų grupės** – nustatyti išlaidų grupes, siekiant sukurti ir prižiūrėti skirtingus išlaidų tipus.</span><span class="sxs-lookup"><span data-stu-id="59319-142">**Cost groups** – Set up cost groups to create and maintain different types of costing.</span></span>
3.  <span data-ttu-id="59319-143">**Maršrutų grupės** – nustatyti maršrutų grupes, siekiant apibrėžti parametrus, kurie yra susiję su maršrutų grupėmis.</span><span class="sxs-lookup"><span data-stu-id="59319-143">**Route groups** – Set up route groups to define parameters that are related to groups of routes.</span></span> <span data-ttu-id="59319-144">Prieš kuriant gamybos maršrutus, reikia nustatyti maršrutų grupes.</span><span class="sxs-lookup"><span data-stu-id="59319-144">You must set up route groups before you can create production routes.</span></span>
4.  <span data-ttu-id="59319-145">**Maršrtai** – nustatyti gamybos maršrutus ir apibrėžti numatytąsias nuostatas, siekiant kontroliuoti maršruto operacijų planavimą, įkainojimą ir kainodarą bei kontroliuoti eigos ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="59319-145">**Routes** – Set up production routes, and define default settings to control scheduling, costing, and pricing of route operations, and to control progress reporting.</span></span>
5.  <span data-ttu-id="59319-146">**Maršrutai** – nustatyti maršrutų versijas, siekiant įgalinti prekių nuokrypius gamyboje.</span><span class="sxs-lookup"><span data-stu-id="59319-146">**Routes** – Set up route versions to enable item variations in production.</span></span>

## <a name="optional-advanced-settings"></a><span data-ttu-id="59319-147">Neprivalomos išplėstinės nuostatos</span><span class="sxs-lookup"><span data-stu-id="59319-147">Optional advanced settings</span></span>
1.  <span data-ttu-id="59319-148">**Gamybos grupės** – nustatyti gamybos grupes, siekiant nustatyti gamybos užsakymo ir DK sąskaitų ryšius.</span><span class="sxs-lookup"><span data-stu-id="59319-148">**Production groups** – Set up production groups to establish relationships between the production order and ledger accounts.</span></span> <span data-ttu-id="59319-149">DK sąskaitos naudojamos registruoti arba grupuoti ataskaitų užsakymams.</span><span class="sxs-lookup"><span data-stu-id="59319-149">The ledger accounts are used to post or group orders for reporting.</span></span>
2.  <span data-ttu-id="59319-150">**Gamybos telkiniai** – sukurti gamybos telkinius, siekiant sugrupuoti gamybos užsakymus, kad būtų galima apdoroti skubius gamybos užsakymus arba panaikinti ir registruoti užsakymų grupes.</span><span class="sxs-lookup"><span data-stu-id="59319-150">**Production pools** – Create production pools to group production orders so that you can process urgent production orders, or delete and post groups of orders.</span></span>
3.  <span data-ttu-id="59319-151">**Ypatybės** – apibrėžti ypatybes, siekiant sukurti specialius atributus, kuriuos būtų galima priskirti savo ištekliams ir taip kontroliuoti gamybos tvarką.</span><span class="sxs-lookup"><span data-stu-id="59319-151">**Properties** – Define properties to create special attributes that you can assign to your resources to control the order of productions.</span></span> <span data-ttu-id="59319-152">Šie atributai yra sujungti su darbo laiko šablonu.</span><span class="sxs-lookup"><span data-stu-id="59319-152">These attributes are connected to the working time template.</span></span>




