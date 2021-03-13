---
title: MyLeaveRequests apžvalga
description: Objektas MyLeaveRequests programoje „Microsoft Dynamics 365 Human Resources“ pateikia sistemoje esančių atostogų užklausų sąrašą, apribotą iki užklausų, pasiekiamų dabartiniam vartotojui, siunčiančiam užklausą šiam objektui.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ca5bc225400338e76faee41a279e91fc00ce570
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115541"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="1b8c5-103">MyLeaveRequests apžvalga</span><span class="sxs-lookup"><span data-stu-id="1b8c5-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="1b8c5-104">Objektas MyLeaveRequests programoje „Microsoft Dynamics 365 Human Resources“ pateikia sistemoje esančių atostogų užklausų sąrašą, apribotą iki užklausų, pasiekiamų dabartiniam vartotojui, siunčiančiam užklausą šiam objektui.</span><span class="sxs-lookup"><span data-stu-id="1b8c5-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="1b8c5-105">Raktas</span><span class="sxs-lookup"><span data-stu-id="1b8c5-105">Key</span></span>

  | <span data-ttu-id="1b8c5-106">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="1b8c5-106">Property Name</span></span> | <span data-ttu-id="1b8c5-107">Duomenų tipas</span><span class="sxs-lookup"><span data-stu-id="1b8c5-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="1b8c5-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="1b8c5-108">dataAreaId</span></span>    | <span data-ttu-id="1b8c5-109">Eilutė</span><span class="sxs-lookup"><span data-stu-id="1b8c5-109">String</span></span>    |
  | <span data-ttu-id="1b8c5-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="1b8c5-110">RequestId</span></span>     | <span data-ttu-id="1b8c5-111">Eilutė</span><span class="sxs-lookup"><span data-stu-id="1b8c5-111">String</span></span>    |
  | <span data-ttu-id="1b8c5-112">„LeaveType”</span><span class="sxs-lookup"><span data-stu-id="1b8c5-112">LeaveType</span></span>     | <span data-ttu-id="1b8c5-113">Eilutė</span><span class="sxs-lookup"><span data-stu-id="1b8c5-113">String</span></span>    |
  | <span data-ttu-id="1b8c5-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="1b8c5-114">LeaveDate</span></span>     | <span data-ttu-id="1b8c5-115">Data</span><span class="sxs-lookup"><span data-stu-id="1b8c5-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="1b8c5-116">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="1b8c5-116">Properties</span></span>

  | <span data-ttu-id="1b8c5-117">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="1b8c5-117">Property Name</span></span>     | <span data-ttu-id="1b8c5-118">Duomenų tipas</span><span class="sxs-lookup"><span data-stu-id="1b8c5-118">Data Type</span></span> | <span data-ttu-id="1b8c5-119">Būtinas</span><span class="sxs-lookup"><span data-stu-id="1b8c5-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="1b8c5-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="1b8c5-120">dataAreaId</span></span>        | <span data-ttu-id="1b8c5-121">Eilutė</span><span class="sxs-lookup"><span data-stu-id="1b8c5-121">String</span></span>    | <span data-ttu-id="1b8c5-122">X</span><span class="sxs-lookup"><span data-stu-id="1b8c5-122">X</span></span>        |
  | <span data-ttu-id="1b8c5-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="1b8c5-123">RequestId</span></span>         | <span data-ttu-id="1b8c5-124">Eilutė</span><span class="sxs-lookup"><span data-stu-id="1b8c5-124">String</span></span>    | <span data-ttu-id="1b8c5-125">X</span><span class="sxs-lookup"><span data-stu-id="1b8c5-125">X</span></span>        |
  | <span data-ttu-id="1b8c5-126">„LeaveType”</span><span class="sxs-lookup"><span data-stu-id="1b8c5-126">LeaveType</span></span>         | <span data-ttu-id="1b8c5-127">Eilutė</span><span class="sxs-lookup"><span data-stu-id="1b8c5-127">String</span></span>    | <span data-ttu-id="1b8c5-128">X</span><span class="sxs-lookup"><span data-stu-id="1b8c5-128">X</span></span>        |
  | <span data-ttu-id="1b8c5-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="1b8c5-129">LeaveDate</span></span>         | <span data-ttu-id="1b8c5-130">Data</span><span class="sxs-lookup"><span data-stu-id="1b8c5-130">Date</span></span>      | <span data-ttu-id="1b8c5-131">X</span><span class="sxs-lookup"><span data-stu-id="1b8c5-131">X</span></span>        |
  | <span data-ttu-id="1b8c5-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="1b8c5-132">ReasonCodeId</span></span>      | <span data-ttu-id="1b8c5-133">Eilutė</span><span class="sxs-lookup"><span data-stu-id="1b8c5-133">String</span></span>    |          |
  | <span data-ttu-id="1b8c5-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="1b8c5-134">PersonnelNumber</span></span>   | <span data-ttu-id="1b8c5-135">Eilutė</span><span class="sxs-lookup"><span data-stu-id="1b8c5-135">String</span></span>    | <span data-ttu-id="1b8c5-136">X</span><span class="sxs-lookup"><span data-stu-id="1b8c5-136">X</span></span>        |
  | <span data-ttu-id="1b8c5-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="1b8c5-137">RequestDate</span></span>       | <span data-ttu-id="1b8c5-138">Data</span><span class="sxs-lookup"><span data-stu-id="1b8c5-138">Date</span></span>      | <span data-ttu-id="1b8c5-139">X</span><span class="sxs-lookup"><span data-stu-id="1b8c5-139">X</span></span>        |
  | <span data-ttu-id="1b8c5-140">Komentuoti</span><span class="sxs-lookup"><span data-stu-id="1b8c5-140">Comment</span></span>           | <span data-ttu-id="1b8c5-141">Eilutė</span><span class="sxs-lookup"><span data-stu-id="1b8c5-141">String</span></span>    |          |
  | <span data-ttu-id="1b8c5-142">Būsena</span><span class="sxs-lookup"><span data-stu-id="1b8c5-142">Status</span></span>            | <span data-ttu-id="1b8c5-143">Išvardijimas</span><span class="sxs-lookup"><span data-stu-id="1b8c5-143">Enum</span></span>      | <span data-ttu-id="1b8c5-144">X</span><span class="sxs-lookup"><span data-stu-id="1b8c5-144">X</span></span>        |
  | <span data-ttu-id="1b8c5-145">Suma</span><span class="sxs-lookup"><span data-stu-id="1b8c5-145">Amount</span></span>            | <span data-ttu-id="1b8c5-146">Tikrasis</span><span class="sxs-lookup"><span data-stu-id="1b8c5-146">Real</span></span>      |          |
  | <span data-ttu-id="1b8c5-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="1b8c5-147">HalfDayDefinition</span></span> | <span data-ttu-id="1b8c5-148">Išvardijimas</span><span class="sxs-lookup"><span data-stu-id="1b8c5-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="1b8c5-149">Veiksmai</span><span class="sxs-lookup"><span data-stu-id="1b8c5-149">Actions</span></span>

 | <span data-ttu-id="1b8c5-150">Veiksmo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="1b8c5-150">Action Name</span></span>                               | <span data-ttu-id="1b8c5-151">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="1b8c5-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="1b8c5-152">pateikti</span><span class="sxs-lookup"><span data-stu-id="1b8c5-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="1b8c5-153">Pateikti užklausą, kurią reikia apdoroti naudojant darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="1b8c5-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="1b8c5-154">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="1b8c5-154">See also</span></span>

- [<span data-ttu-id="1b8c5-155">Prašymo išeiti atostogų pateikimas darbo eigai</span><span class="sxs-lookup"><span data-stu-id="1b8c5-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="1b8c5-156">Autentifikavimas</span><span class="sxs-lookup"><span data-stu-id="1b8c5-156">Authentication</span></span>](hr-developer-api-authentication.md)