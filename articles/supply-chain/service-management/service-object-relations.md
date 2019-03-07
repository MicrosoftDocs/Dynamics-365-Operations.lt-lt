---
title: Aptarnavimo objekto ryšiai
description: Galite sukurti aptarnavimo objekto ryšius tarp aptarnavimo objekto ir aptarnavimo sutarties arba aptarnavimo užsakymo.
author: ShylaThompson
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 03047b3eccf3c90d4cf7426ddaec83f10dbea1b0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "314376"
---
# <a name="service-object-relations"></a><span data-ttu-id="20c94-103">Aptarnavimo objekto ryšiai</span><span class="sxs-lookup"><span data-stu-id="20c94-103">Service object relations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20c94-104">Galite sukurti aptarnavimo objekto ryšius tarp aptarnavimo objekto ir aptarnavimo sutarties arba aptarnavimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="20c94-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="20c94-105">Kurdami ryšį, aptarnavimo objektą pridėkite prie aptarnavimo sutarties arba aptarnavimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="20c94-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="20c94-106">Sukūrę ryšį, aptarnavimo objektą galite pridėti prie bet kurių aptarnavimo sutarties arba aptarnavimo užsakymo eilučių.</span><span class="sxs-lookup"><span data-stu-id="20c94-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="20c94-107">KS šablonai</span><span class="sxs-lookup"><span data-stu-id="20c94-107">Template BOMs</span></span>

<span data-ttu-id="20c94-108">Taip pat galite nurodyti objekto ryšio KS šabloną.</span><span class="sxs-lookup"><span data-stu-id="20c94-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="20c94-109">KS šablonas yra objekto, kuriam atliekate aptarnavimą, komplektacijos specifikacija.</span><span class="sxs-lookup"><span data-stu-id="20c94-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="20c94-110">Aptarnavimo vizito metu pakeitę aptarnavimo objekto komponento dalį, šį pakeitimą galite užregistruoti aptarnavimo KS, naudodami formą Aptarnavimo objektai.</span><span class="sxs-lookup"><span data-stu-id="20c94-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="20c94-111">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="20c94-111">Example</span></span>

<span data-ttu-id="20c94-112">Sukuriate dviejų liftų aptarnavimo kliento pageidaujamoje teritorijoje sutartį.</span><span class="sxs-lookup"><span data-stu-id="20c94-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="20c94-113">Aptarnavimo sutarties identifikatorius yra ID SAL-001.</span><span class="sxs-lookup"><span data-stu-id="20c94-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="20c94-114">Liftai formoje Aptarnavimo objektai nustatomi kaip objektai, EL-S/1000 ir EL-L/1000.</span><span class="sxs-lookup"><span data-stu-id="20c94-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="20c94-115">Prie aptarnavimo sutarties pridedate aptarnavimo objektus, EL-S/1000 ir EL-L/1000.</span><span class="sxs-lookup"><span data-stu-id="20c94-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="20c94-116">Keisdami komponentų dalis, norite registruoti aptarnavimo objekto KS pakeitimus, todėl prie aptarnavimo objekto ryšio pridedate aptarnavimo KS, kaip apibrėžta šioje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="20c94-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="20c94-117">Aptarnavimo objektas</span><span class="sxs-lookup"><span data-stu-id="20c94-117">Service object</span></span> | <span data-ttu-id="20c94-118">Ryšys – Aptarnavimo sutartis</span><span class="sxs-lookup"><span data-stu-id="20c94-118">Relation – Service agreement</span></span> | <span data-ttu-id="20c94-119">Aptarnavimo KS</span><span class="sxs-lookup"><span data-stu-id="20c94-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="20c94-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="20c94-120">EL-S/1000</span></span>      | <span data-ttu-id="20c94-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="20c94-121">ID SAL-001</span></span>                   | <span data-ttu-id="20c94-122">KS-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="20c94-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="20c94-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="20c94-123">EL-L/1000</span></span>      | <span data-ttu-id="20c94-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="20c94-124">ID SAL-001</span></span>                   | <span data-ttu-id="20c94-125">KS-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="20c94-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="20c94-126">Kadangi egzistuoja sutarties aptarnavimo objekto ryšiai, dabar galite sukurti aptarnavimo sutarties eilutes su šiais objektais, kaip parodyta šioje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="20c94-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="20c94-127">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="20c94-127">Transaction type</span></span> | <span data-ttu-id="20c94-128">Kategorija</span><span class="sxs-lookup"><span data-stu-id="20c94-128">Category</span></span>           | <span data-ttu-id="20c94-129">Aptarnavimo objektas</span><span class="sxs-lookup"><span data-stu-id="20c94-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="20c94-130">Valandos</span><span class="sxs-lookup"><span data-stu-id="20c94-130">Hour</span></span>             | <span data-ttu-id="20c94-131">Patikrinimas</span><span class="sxs-lookup"><span data-stu-id="20c94-131">Inspection</span></span>         | <span data-ttu-id="20c94-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="20c94-132">EL-S/1000</span></span>      |
| <span data-ttu-id="20c94-133">Valandos</span><span class="sxs-lookup"><span data-stu-id="20c94-133">Hour</span></span>             | <span data-ttu-id="20c94-134">Pavarų dėžės valymas</span><span class="sxs-lookup"><span data-stu-id="20c94-134">Gear box cleaning</span></span>  | <span data-ttu-id="20c94-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="20c94-135">EL-S/1000</span></span>      |
| <span data-ttu-id="20c94-136">Prekė</span><span class="sxs-lookup"><span data-stu-id="20c94-136">Item</span></span>             | <span data-ttu-id="20c94-137">Valymo medžiagos</span><span class="sxs-lookup"><span data-stu-id="20c94-137">Cleaning materials</span></span> | <span data-ttu-id="20c94-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="20c94-138">EL-S/1000</span></span>      |
| <span data-ttu-id="20c94-139">Valandos</span><span class="sxs-lookup"><span data-stu-id="20c94-139">Hour</span></span>             | <span data-ttu-id="20c94-140">Patikrinimas</span><span class="sxs-lookup"><span data-stu-id="20c94-140">Inspection</span></span>         | <span data-ttu-id="20c94-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="20c94-141">EL-L/1000</span></span>      |
| <span data-ttu-id="20c94-142">Valandos</span><span class="sxs-lookup"><span data-stu-id="20c94-142">Hour</span></span>             | <span data-ttu-id="20c94-143">Pavarų dėžės valymas</span><span class="sxs-lookup"><span data-stu-id="20c94-143">Gearbox cleaning</span></span>   | <span data-ttu-id="20c94-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="20c94-144">EL-L/1000</span></span>      |
| <span data-ttu-id="20c94-145">Prekė</span><span class="sxs-lookup"><span data-stu-id="20c94-145">Item</span></span>             | <span data-ttu-id="20c94-146">Valymo medžiagos</span><span class="sxs-lookup"><span data-stu-id="20c94-146">Cleaning materials</span></span> | <span data-ttu-id="20c94-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="20c94-147">EL-L/1000</span></span>      |

<span data-ttu-id="20c94-148">Vykstant aptarnavimo vizitui, turite pakeisti lifto EL-S/1000 pavarų dėžę.</span><span class="sxs-lookup"><span data-stu-id="20c94-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="20c94-149">Norėdami pakeisti objekto komponento dalį, galite pereiti į KS konstruktorių, naudodami nustatytą dabartinio aptarnavimo sutarties aptarnavimo objekto ryšį.</span><span class="sxs-lookup"><span data-stu-id="20c94-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="20c94-150">Prieiga prie KS konstruktoriaus, naudojant aptarnavimo objekto ryšį</span><span class="sxs-lookup"><span data-stu-id="20c94-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="20c94-151">Aptarnavimo sutartys</span><span class="sxs-lookup"><span data-stu-id="20c94-151">Service agreements</span></span>
2. <span data-ttu-id="20c94-152">Dukart spustelėkite aptarnavimo sutartį arba spustelėkite Aptarnavimo sutartis, kad sukurtumėte naują aptarnavimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="20c94-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="20c94-153">Spustelėkite skirtuką Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="20c94-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="20c94-154">Norėdami prie aptarnavimo sutarties pridėti KS šabloną, spustelėkite Aptarnavimo objektai.</span><span class="sxs-lookup"><span data-stu-id="20c94-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="20c94-155">Formoje Aptarnavimo objektai spustelėkite Kūrimo įrankis – atidarysite kūrimo įrankio formą, kuruoje galėsite keisti šabloninę KS.</span><span class="sxs-lookup"><span data-stu-id="20c94-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="20c94-156">Automatiškai kuriami aptarnavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="20c94-156">Automatically created service orders</span></span>

<span data-ttu-id="20c94-157">Jei automatiškai kuriate aptarnavimo sutarties aptarnavimo užsakymus, sutartyje esantys aptarnavimo objekto ryšiai taip pat sukuriami aptarnavimo užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="20c94-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>

