---
title: Aptarnavimo objekto ryšiai
description: Galite sukurti aptarnavimo objekto ryšius tarp aptarnavimo objekto ir aptarnavimo sutarties arba aptarnavimo užsakymo.
author: ShylaThompson
manager: tfehr
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 913b3c30bf972de7cc3dde73280e4f2f2be38507
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974340"
---
# <a name="service-object-relations"></a><span data-ttu-id="afece-103">Aptarnavimo objekto ryšiai</span><span class="sxs-lookup"><span data-stu-id="afece-103">Service object relations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afece-104">Galite sukurti aptarnavimo objekto ryšius tarp aptarnavimo objekto ir aptarnavimo sutarties arba aptarnavimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="afece-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="afece-105">Kurdami ryšį, aptarnavimo objektą pridėkite prie aptarnavimo sutarties arba aptarnavimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="afece-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="afece-106">Sukūrę ryšį, aptarnavimo objektą galite pridėti prie bet kurių aptarnavimo sutarties arba aptarnavimo užsakymo eilučių.</span><span class="sxs-lookup"><span data-stu-id="afece-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="afece-107">KS šablonai</span><span class="sxs-lookup"><span data-stu-id="afece-107">Template BOMs</span></span>

<span data-ttu-id="afece-108">Taip pat galite nurodyti objekto ryšio KS šabloną.</span><span class="sxs-lookup"><span data-stu-id="afece-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="afece-109">KS šablonas yra objekto, kuriam atliekate aptarnavimą, komplektacijos specifikacija.</span><span class="sxs-lookup"><span data-stu-id="afece-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="afece-110">Aptarnavimo vizito metu pakeitę aptarnavimo objekto komponento dalį, šį pakeitimą galite užregistruoti aptarnavimo KS, naudodami formą Aptarnavimo objektai.</span><span class="sxs-lookup"><span data-stu-id="afece-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="afece-111">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="afece-111">Example</span></span>

<span data-ttu-id="afece-112">Sukuriate dviejų liftų aptarnavimo kliento pageidaujamoje teritorijoje sutartį.</span><span class="sxs-lookup"><span data-stu-id="afece-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="afece-113">Aptarnavimo sutarties identifikatorius yra ID SAL-001.</span><span class="sxs-lookup"><span data-stu-id="afece-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="afece-114">Liftai formoje Aptarnavimo objektai nustatomi kaip objektai, EL-S/1000 ir EL-L/1000.</span><span class="sxs-lookup"><span data-stu-id="afece-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="afece-115">Prie aptarnavimo sutarties pridedate aptarnavimo objektus, EL-S/1000 ir EL-L/1000.</span><span class="sxs-lookup"><span data-stu-id="afece-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="afece-116">Keisdami komponentų dalis, norite registruoti aptarnavimo objekto KS pakeitimus, todėl prie aptarnavimo objekto ryšio pridedate aptarnavimo KS, kaip apibrėžta šioje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="afece-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="afece-117">Aptarnavimo objektas</span><span class="sxs-lookup"><span data-stu-id="afece-117">Service object</span></span> | <span data-ttu-id="afece-118">Ryšys – Aptarnavimo sutartis</span><span class="sxs-lookup"><span data-stu-id="afece-118">Relation – Service agreement</span></span> | <span data-ttu-id="afece-119">Aptarnavimo KS</span><span class="sxs-lookup"><span data-stu-id="afece-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="afece-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="afece-120">EL-S/1000</span></span>      | <span data-ttu-id="afece-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="afece-121">ID SAL-001</span></span>                   | <span data-ttu-id="afece-122">KS-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="afece-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="afece-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="afece-123">EL-L/1000</span></span>      | <span data-ttu-id="afece-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="afece-124">ID SAL-001</span></span>                   | <span data-ttu-id="afece-125">KS-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="afece-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="afece-126">Kadangi egzistuoja sutarties aptarnavimo objekto ryšiai, dabar galite sukurti aptarnavimo sutarties eilutes su šiais objektais, kaip parodyta šioje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="afece-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="afece-127">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="afece-127">Transaction type</span></span> | <span data-ttu-id="afece-128">Kategorija</span><span class="sxs-lookup"><span data-stu-id="afece-128">Category</span></span>           | <span data-ttu-id="afece-129">Aptarnavimo objektas</span><span class="sxs-lookup"><span data-stu-id="afece-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="afece-130">Valandos</span><span class="sxs-lookup"><span data-stu-id="afece-130">Hour</span></span>             | <span data-ttu-id="afece-131">Patikrinimas</span><span class="sxs-lookup"><span data-stu-id="afece-131">Inspection</span></span>         | <span data-ttu-id="afece-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="afece-132">EL-S/1000</span></span>      |
| <span data-ttu-id="afece-133">Valandos</span><span class="sxs-lookup"><span data-stu-id="afece-133">Hour</span></span>             | <span data-ttu-id="afece-134">Pavarų dėžės valymas</span><span class="sxs-lookup"><span data-stu-id="afece-134">Gear box cleaning</span></span>  | <span data-ttu-id="afece-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="afece-135">EL-S/1000</span></span>      |
| <span data-ttu-id="afece-136">Prekė</span><span class="sxs-lookup"><span data-stu-id="afece-136">Item</span></span>             | <span data-ttu-id="afece-137">Valymo medžiagos</span><span class="sxs-lookup"><span data-stu-id="afece-137">Cleaning materials</span></span> | <span data-ttu-id="afece-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="afece-138">EL-S/1000</span></span>      |
| <span data-ttu-id="afece-139">Valandos</span><span class="sxs-lookup"><span data-stu-id="afece-139">Hour</span></span>             | <span data-ttu-id="afece-140">Patikrinimas</span><span class="sxs-lookup"><span data-stu-id="afece-140">Inspection</span></span>         | <span data-ttu-id="afece-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="afece-141">EL-L/1000</span></span>      |
| <span data-ttu-id="afece-142">Valandos</span><span class="sxs-lookup"><span data-stu-id="afece-142">Hour</span></span>             | <span data-ttu-id="afece-143">Pavarų dėžės valymas</span><span class="sxs-lookup"><span data-stu-id="afece-143">Gearbox cleaning</span></span>   | <span data-ttu-id="afece-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="afece-144">EL-L/1000</span></span>      |
| <span data-ttu-id="afece-145">Prekė</span><span class="sxs-lookup"><span data-stu-id="afece-145">Item</span></span>             | <span data-ttu-id="afece-146">Valymo medžiagos</span><span class="sxs-lookup"><span data-stu-id="afece-146">Cleaning materials</span></span> | <span data-ttu-id="afece-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="afece-147">EL-L/1000</span></span>      |

<span data-ttu-id="afece-148">Vykstant aptarnavimo vizitui, turite pakeisti lifto EL-S/1000 pavarų dėžę.</span><span class="sxs-lookup"><span data-stu-id="afece-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="afece-149">Norėdami pakeisti objekto komponento dalį, galite pereiti į KS konstruktorių, naudodami nustatytą dabartinio aptarnavimo sutarties aptarnavimo objekto ryšį.</span><span class="sxs-lookup"><span data-stu-id="afece-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="afece-150">Prieiga prie KS konstruktoriaus, naudojant aptarnavimo objekto ryšį</span><span class="sxs-lookup"><span data-stu-id="afece-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="afece-151">Aptarnavimo sutartys</span><span class="sxs-lookup"><span data-stu-id="afece-151">Service agreements</span></span>
2. <span data-ttu-id="afece-152">Dukart spustelėkite aptarnavimo sutartį arba spustelėkite Aptarnavimo sutartis, kad sukurtumėte naują aptarnavimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="afece-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="afece-153">Spustelėkite skirtuką Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="afece-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="afece-154">Norėdami prie aptarnavimo sutarties pridėti KS šabloną, spustelėkite Aptarnavimo objektai.</span><span class="sxs-lookup"><span data-stu-id="afece-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="afece-155">Formoje Aptarnavimo objektai spustelėkite Kūrimo įrankis – atidarysite kūrimo įrankio formą, kuruoje galėsite keisti šabloninę KS.</span><span class="sxs-lookup"><span data-stu-id="afece-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="afece-156">Automatiškai kuriami aptarnavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="afece-156">Automatically created service orders</span></span>

<span data-ttu-id="afece-157">Jei automatiškai kuriate aptarnavimo sutarties aptarnavimo užsakymus, sutartyje esantys aptarnavimo objekto ryšiai taip pat sukuriami aptarnavimo užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="afece-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>

