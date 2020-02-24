---
title: MyLeaveRequests apžvalga
description: ''
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 66f161d6736b1bb544d02871d9d51b2949b1cfa0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009935"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="9c5ee-102">MyLeaveRequests apžvalga</span><span class="sxs-lookup"><span data-stu-id="9c5ee-102">MyLeaveRequests overview</span></span>

<span data-ttu-id="9c5ee-103">Objektas MyLeaveRequests programoje „Microsoft Dynamics 365 Human Resources“ pateikia sistemoje esančių atostogų užklausų sąrašą, apribotą iki užklausų, pasiekiamų dabartiniam vartotojui, siunčiančiam užklausą šiam objektui.</span><span class="sxs-lookup"><span data-stu-id="9c5ee-103">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="9c5ee-104">Raktas</span><span class="sxs-lookup"><span data-stu-id="9c5ee-104">Key</span></span>

  | <span data-ttu-id="9c5ee-105">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="9c5ee-105">Property Name</span></span> | <span data-ttu-id="9c5ee-106">Duomenų tipas</span><span class="sxs-lookup"><span data-stu-id="9c5ee-106">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="9c5ee-107">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="9c5ee-107">dataAreaId</span></span>    | <span data-ttu-id="9c5ee-108">Eilutė</span><span class="sxs-lookup"><span data-stu-id="9c5ee-108">String</span></span>    |
  | <span data-ttu-id="9c5ee-109">RequestId</span><span class="sxs-lookup"><span data-stu-id="9c5ee-109">RequestId</span></span>     | <span data-ttu-id="9c5ee-110">Eilutė</span><span class="sxs-lookup"><span data-stu-id="9c5ee-110">String</span></span>    |
  | <span data-ttu-id="9c5ee-111">„LeaveType”</span><span class="sxs-lookup"><span data-stu-id="9c5ee-111">LeaveType</span></span>     | <span data-ttu-id="9c5ee-112">Eilutė</span><span class="sxs-lookup"><span data-stu-id="9c5ee-112">String</span></span>    |
  | <span data-ttu-id="9c5ee-113">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="9c5ee-113">LeaveDate</span></span>     | <span data-ttu-id="9c5ee-114">Data</span><span class="sxs-lookup"><span data-stu-id="9c5ee-114">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="9c5ee-115">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="9c5ee-115">Properties</span></span>

  | <span data-ttu-id="9c5ee-116">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="9c5ee-116">Property Name</span></span>     | <span data-ttu-id="9c5ee-117">Duomenų tipas</span><span class="sxs-lookup"><span data-stu-id="9c5ee-117">Data Type</span></span> | <span data-ttu-id="9c5ee-118">Būtinas</span><span class="sxs-lookup"><span data-stu-id="9c5ee-118">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="9c5ee-119">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="9c5ee-119">dataAreaId</span></span>        | <span data-ttu-id="9c5ee-120">Eilutė</span><span class="sxs-lookup"><span data-stu-id="9c5ee-120">String</span></span>    | <span data-ttu-id="9c5ee-121">X</span><span class="sxs-lookup"><span data-stu-id="9c5ee-121">X</span></span>        |
  | <span data-ttu-id="9c5ee-122">RequestId</span><span class="sxs-lookup"><span data-stu-id="9c5ee-122">RequestId</span></span>         | <span data-ttu-id="9c5ee-123">Eilutė</span><span class="sxs-lookup"><span data-stu-id="9c5ee-123">String</span></span>    | <span data-ttu-id="9c5ee-124">X</span><span class="sxs-lookup"><span data-stu-id="9c5ee-124">X</span></span>        |
  | <span data-ttu-id="9c5ee-125">„LeaveType”</span><span class="sxs-lookup"><span data-stu-id="9c5ee-125">LeaveType</span></span>         | <span data-ttu-id="9c5ee-126">Eilutė</span><span class="sxs-lookup"><span data-stu-id="9c5ee-126">String</span></span>    | <span data-ttu-id="9c5ee-127">X</span><span class="sxs-lookup"><span data-stu-id="9c5ee-127">X</span></span>        |
  | <span data-ttu-id="9c5ee-128">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="9c5ee-128">LeaveDate</span></span>         | <span data-ttu-id="9c5ee-129">Data</span><span class="sxs-lookup"><span data-stu-id="9c5ee-129">Date</span></span>      | <span data-ttu-id="9c5ee-130">X</span><span class="sxs-lookup"><span data-stu-id="9c5ee-130">X</span></span>        |
  | <span data-ttu-id="9c5ee-131">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="9c5ee-131">ReasonCodeId</span></span>      | <span data-ttu-id="9c5ee-132">Eilutė</span><span class="sxs-lookup"><span data-stu-id="9c5ee-132">String</span></span>    |          |
  | <span data-ttu-id="9c5ee-133">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="9c5ee-133">PersonnelNumber</span></span>   | <span data-ttu-id="9c5ee-134">Eilutė</span><span class="sxs-lookup"><span data-stu-id="9c5ee-134">String</span></span>    | <span data-ttu-id="9c5ee-135">X</span><span class="sxs-lookup"><span data-stu-id="9c5ee-135">X</span></span>        |
  | <span data-ttu-id="9c5ee-136">RequestDate</span><span class="sxs-lookup"><span data-stu-id="9c5ee-136">RequestDate</span></span>       | <span data-ttu-id="9c5ee-137">Data</span><span class="sxs-lookup"><span data-stu-id="9c5ee-137">Date</span></span>      | <span data-ttu-id="9c5ee-138">X</span><span class="sxs-lookup"><span data-stu-id="9c5ee-138">X</span></span>        |
  | <span data-ttu-id="9c5ee-139">Komentuoti</span><span class="sxs-lookup"><span data-stu-id="9c5ee-139">Comment</span></span>           | <span data-ttu-id="9c5ee-140">Eilutė</span><span class="sxs-lookup"><span data-stu-id="9c5ee-140">String</span></span>    |          |
  | <span data-ttu-id="9c5ee-141">Būsena</span><span class="sxs-lookup"><span data-stu-id="9c5ee-141">Status</span></span>            | <span data-ttu-id="9c5ee-142">Išvardijimas</span><span class="sxs-lookup"><span data-stu-id="9c5ee-142">Enum</span></span>      | <span data-ttu-id="9c5ee-143">X</span><span class="sxs-lookup"><span data-stu-id="9c5ee-143">X</span></span>        |
  | <span data-ttu-id="9c5ee-144">Suma</span><span class="sxs-lookup"><span data-stu-id="9c5ee-144">Amount</span></span>            | <span data-ttu-id="9c5ee-145">Tikrasis</span><span class="sxs-lookup"><span data-stu-id="9c5ee-145">Real</span></span>      |          |
  | <span data-ttu-id="9c5ee-146">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="9c5ee-146">HalfDayDefinition</span></span> | <span data-ttu-id="9c5ee-147">Išvardijimas</span><span class="sxs-lookup"><span data-stu-id="9c5ee-147">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="9c5ee-148">Veiksmai</span><span class="sxs-lookup"><span data-stu-id="9c5ee-148">Actions</span></span>

 | <span data-ttu-id="9c5ee-149">Veiksmo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="9c5ee-149">Action Name</span></span>                               | <span data-ttu-id="9c5ee-150">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="9c5ee-150">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="9c5ee-151">pateikti</span><span class="sxs-lookup"><span data-stu-id="9c5ee-151">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="9c5ee-152">Pateikti užklausą, kurią reikia apdoroti naudojant darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="9c5ee-152">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="9c5ee-153">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="9c5ee-153">See also</span></span>

- [<span data-ttu-id="9c5ee-154">Prašymo išeiti atostogų pateikimas darbo eigai</span><span class="sxs-lookup"><span data-stu-id="9c5ee-154">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="9c5ee-155">Autentifikavimas</span><span class="sxs-lookup"><span data-stu-id="9c5ee-155">Authentication</span></span>](hr-developer-api-authentication.md)