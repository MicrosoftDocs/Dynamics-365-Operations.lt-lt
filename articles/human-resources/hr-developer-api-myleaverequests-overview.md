---
title: MyLeaveRequests apžvalga
description: Objektas MyLeaveRequests programoje „Microsoft Dynamics 365 Human Resources“ pateikia sistemoje esančių atostogų užklausų sąrašą, apribotą iki užklausų, pasiekiamų dabartiniam vartotojui, siunčiančiam užklausą šiam objektui.
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
ms.openlocfilehash: 4bf3b298af9eb39e03514a4005afb43a42908e47
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419651"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="0a6c0-103">MyLeaveRequests apžvalga</span><span class="sxs-lookup"><span data-stu-id="0a6c0-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="0a6c0-104">Objektas MyLeaveRequests programoje „Microsoft Dynamics 365 Human Resources“ pateikia sistemoje esančių atostogų užklausų sąrašą, apribotą iki užklausų, pasiekiamų dabartiniam vartotojui, siunčiančiam užklausą šiam objektui.</span><span class="sxs-lookup"><span data-stu-id="0a6c0-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="0a6c0-105">Raktas</span><span class="sxs-lookup"><span data-stu-id="0a6c0-105">Key</span></span>

  | <span data-ttu-id="0a6c0-106">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="0a6c0-106">Property Name</span></span> | <span data-ttu-id="0a6c0-107">Duomenų tipas</span><span class="sxs-lookup"><span data-stu-id="0a6c0-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="0a6c0-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="0a6c0-108">dataAreaId</span></span>    | <span data-ttu-id="0a6c0-109">Eilutė</span><span class="sxs-lookup"><span data-stu-id="0a6c0-109">String</span></span>    |
  | <span data-ttu-id="0a6c0-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="0a6c0-110">RequestId</span></span>     | <span data-ttu-id="0a6c0-111">Eilutė</span><span class="sxs-lookup"><span data-stu-id="0a6c0-111">String</span></span>    |
  | <span data-ttu-id="0a6c0-112">„LeaveType”</span><span class="sxs-lookup"><span data-stu-id="0a6c0-112">LeaveType</span></span>     | <span data-ttu-id="0a6c0-113">Eilutė</span><span class="sxs-lookup"><span data-stu-id="0a6c0-113">String</span></span>    |
  | <span data-ttu-id="0a6c0-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="0a6c0-114">LeaveDate</span></span>     | <span data-ttu-id="0a6c0-115">Data</span><span class="sxs-lookup"><span data-stu-id="0a6c0-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="0a6c0-116">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="0a6c0-116">Properties</span></span>

  | <span data-ttu-id="0a6c0-117">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="0a6c0-117">Property Name</span></span>     | <span data-ttu-id="0a6c0-118">Duomenų tipas</span><span class="sxs-lookup"><span data-stu-id="0a6c0-118">Data Type</span></span> | <span data-ttu-id="0a6c0-119">Būtinas</span><span class="sxs-lookup"><span data-stu-id="0a6c0-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="0a6c0-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="0a6c0-120">dataAreaId</span></span>        | <span data-ttu-id="0a6c0-121">Eilutė</span><span class="sxs-lookup"><span data-stu-id="0a6c0-121">String</span></span>    | <span data-ttu-id="0a6c0-122">X</span><span class="sxs-lookup"><span data-stu-id="0a6c0-122">X</span></span>        |
  | <span data-ttu-id="0a6c0-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="0a6c0-123">RequestId</span></span>         | <span data-ttu-id="0a6c0-124">Eilutė</span><span class="sxs-lookup"><span data-stu-id="0a6c0-124">String</span></span>    | <span data-ttu-id="0a6c0-125">X</span><span class="sxs-lookup"><span data-stu-id="0a6c0-125">X</span></span>        |
  | <span data-ttu-id="0a6c0-126">„LeaveType”</span><span class="sxs-lookup"><span data-stu-id="0a6c0-126">LeaveType</span></span>         | <span data-ttu-id="0a6c0-127">Eilutė</span><span class="sxs-lookup"><span data-stu-id="0a6c0-127">String</span></span>    | <span data-ttu-id="0a6c0-128">X</span><span class="sxs-lookup"><span data-stu-id="0a6c0-128">X</span></span>        |
  | <span data-ttu-id="0a6c0-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="0a6c0-129">LeaveDate</span></span>         | <span data-ttu-id="0a6c0-130">Data</span><span class="sxs-lookup"><span data-stu-id="0a6c0-130">Date</span></span>      | <span data-ttu-id="0a6c0-131">X</span><span class="sxs-lookup"><span data-stu-id="0a6c0-131">X</span></span>        |
  | <span data-ttu-id="0a6c0-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="0a6c0-132">ReasonCodeId</span></span>      | <span data-ttu-id="0a6c0-133">Eilutė</span><span class="sxs-lookup"><span data-stu-id="0a6c0-133">String</span></span>    |          |
  | <span data-ttu-id="0a6c0-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="0a6c0-134">PersonnelNumber</span></span>   | <span data-ttu-id="0a6c0-135">Eilutė</span><span class="sxs-lookup"><span data-stu-id="0a6c0-135">String</span></span>    | <span data-ttu-id="0a6c0-136">X</span><span class="sxs-lookup"><span data-stu-id="0a6c0-136">X</span></span>        |
  | <span data-ttu-id="0a6c0-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="0a6c0-137">RequestDate</span></span>       | <span data-ttu-id="0a6c0-138">Data</span><span class="sxs-lookup"><span data-stu-id="0a6c0-138">Date</span></span>      | <span data-ttu-id="0a6c0-139">X</span><span class="sxs-lookup"><span data-stu-id="0a6c0-139">X</span></span>        |
  | <span data-ttu-id="0a6c0-140">Komentuoti</span><span class="sxs-lookup"><span data-stu-id="0a6c0-140">Comment</span></span>           | <span data-ttu-id="0a6c0-141">Eilutė</span><span class="sxs-lookup"><span data-stu-id="0a6c0-141">String</span></span>    |          |
  | <span data-ttu-id="0a6c0-142">Būsena</span><span class="sxs-lookup"><span data-stu-id="0a6c0-142">Status</span></span>            | <span data-ttu-id="0a6c0-143">Išvardijimas</span><span class="sxs-lookup"><span data-stu-id="0a6c0-143">Enum</span></span>      | <span data-ttu-id="0a6c0-144">X</span><span class="sxs-lookup"><span data-stu-id="0a6c0-144">X</span></span>        |
  | <span data-ttu-id="0a6c0-145">Suma</span><span class="sxs-lookup"><span data-stu-id="0a6c0-145">Amount</span></span>            | <span data-ttu-id="0a6c0-146">Tikrasis</span><span class="sxs-lookup"><span data-stu-id="0a6c0-146">Real</span></span>      |          |
  | <span data-ttu-id="0a6c0-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="0a6c0-147">HalfDayDefinition</span></span> | <span data-ttu-id="0a6c0-148">Išvardijimas</span><span class="sxs-lookup"><span data-stu-id="0a6c0-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="0a6c0-149">Veiksmai</span><span class="sxs-lookup"><span data-stu-id="0a6c0-149">Actions</span></span>

 | <span data-ttu-id="0a6c0-150">Veiksmo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="0a6c0-150">Action Name</span></span>                               | <span data-ttu-id="0a6c0-151">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="0a6c0-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="0a6c0-152">pateikti</span><span class="sxs-lookup"><span data-stu-id="0a6c0-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="0a6c0-153">Pateikti užklausą, kurią reikia apdoroti naudojant darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="0a6c0-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="0a6c0-154">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="0a6c0-154">See also</span></span>

- [<span data-ttu-id="0a6c0-155">Prašymo išeiti atostogų pateikimas darbo eigai</span><span class="sxs-lookup"><span data-stu-id="0a6c0-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="0a6c0-156">Autentifikavimas</span><span class="sxs-lookup"><span data-stu-id="0a6c0-156">Authentication</span></span>](hr-developer-api-authentication.md)