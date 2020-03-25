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
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092042"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="2ffb6-103">MyLeaveRequests apžvalga</span><span class="sxs-lookup"><span data-stu-id="2ffb6-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="2ffb6-104">Objektas MyLeaveRequests programoje „Microsoft Dynamics 365 Human Resources“ pateikia sistemoje esančių atostogų užklausų sąrašą, apribotą iki užklausų, pasiekiamų dabartiniam vartotojui, siunčiančiam užklausą šiam objektui.</span><span class="sxs-lookup"><span data-stu-id="2ffb6-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="2ffb6-105">Raktas</span><span class="sxs-lookup"><span data-stu-id="2ffb6-105">Key</span></span>

  | <span data-ttu-id="2ffb6-106">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="2ffb6-106">Property Name</span></span> | <span data-ttu-id="2ffb6-107">Duomenų tipas</span><span class="sxs-lookup"><span data-stu-id="2ffb6-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="2ffb6-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="2ffb6-108">dataAreaId</span></span>    | <span data-ttu-id="2ffb6-109">Eilutė</span><span class="sxs-lookup"><span data-stu-id="2ffb6-109">String</span></span>    |
  | <span data-ttu-id="2ffb6-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="2ffb6-110">RequestId</span></span>     | <span data-ttu-id="2ffb6-111">Eilutė</span><span class="sxs-lookup"><span data-stu-id="2ffb6-111">String</span></span>    |
  | <span data-ttu-id="2ffb6-112">„LeaveType”</span><span class="sxs-lookup"><span data-stu-id="2ffb6-112">LeaveType</span></span>     | <span data-ttu-id="2ffb6-113">Eilutė</span><span class="sxs-lookup"><span data-stu-id="2ffb6-113">String</span></span>    |
  | <span data-ttu-id="2ffb6-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="2ffb6-114">LeaveDate</span></span>     | <span data-ttu-id="2ffb6-115">Data</span><span class="sxs-lookup"><span data-stu-id="2ffb6-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="2ffb6-116">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="2ffb6-116">Properties</span></span>

  | <span data-ttu-id="2ffb6-117">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="2ffb6-117">Property Name</span></span>     | <span data-ttu-id="2ffb6-118">Duomenų tipas</span><span class="sxs-lookup"><span data-stu-id="2ffb6-118">Data Type</span></span> | <span data-ttu-id="2ffb6-119">Būtinas</span><span class="sxs-lookup"><span data-stu-id="2ffb6-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="2ffb6-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="2ffb6-120">dataAreaId</span></span>        | <span data-ttu-id="2ffb6-121">Eilutė</span><span class="sxs-lookup"><span data-stu-id="2ffb6-121">String</span></span>    | <span data-ttu-id="2ffb6-122">X</span><span class="sxs-lookup"><span data-stu-id="2ffb6-122">X</span></span>        |
  | <span data-ttu-id="2ffb6-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="2ffb6-123">RequestId</span></span>         | <span data-ttu-id="2ffb6-124">Eilutė</span><span class="sxs-lookup"><span data-stu-id="2ffb6-124">String</span></span>    | <span data-ttu-id="2ffb6-125">X</span><span class="sxs-lookup"><span data-stu-id="2ffb6-125">X</span></span>        |
  | <span data-ttu-id="2ffb6-126">„LeaveType”</span><span class="sxs-lookup"><span data-stu-id="2ffb6-126">LeaveType</span></span>         | <span data-ttu-id="2ffb6-127">Eilutė</span><span class="sxs-lookup"><span data-stu-id="2ffb6-127">String</span></span>    | <span data-ttu-id="2ffb6-128">X</span><span class="sxs-lookup"><span data-stu-id="2ffb6-128">X</span></span>        |
  | <span data-ttu-id="2ffb6-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="2ffb6-129">LeaveDate</span></span>         | <span data-ttu-id="2ffb6-130">Data</span><span class="sxs-lookup"><span data-stu-id="2ffb6-130">Date</span></span>      | <span data-ttu-id="2ffb6-131">X</span><span class="sxs-lookup"><span data-stu-id="2ffb6-131">X</span></span>        |
  | <span data-ttu-id="2ffb6-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="2ffb6-132">ReasonCodeId</span></span>      | <span data-ttu-id="2ffb6-133">Eilutė</span><span class="sxs-lookup"><span data-stu-id="2ffb6-133">String</span></span>    |          |
  | <span data-ttu-id="2ffb6-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="2ffb6-134">PersonnelNumber</span></span>   | <span data-ttu-id="2ffb6-135">Eilutė</span><span class="sxs-lookup"><span data-stu-id="2ffb6-135">String</span></span>    | <span data-ttu-id="2ffb6-136">X</span><span class="sxs-lookup"><span data-stu-id="2ffb6-136">X</span></span>        |
  | <span data-ttu-id="2ffb6-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="2ffb6-137">RequestDate</span></span>       | <span data-ttu-id="2ffb6-138">Data</span><span class="sxs-lookup"><span data-stu-id="2ffb6-138">Date</span></span>      | <span data-ttu-id="2ffb6-139">X</span><span class="sxs-lookup"><span data-stu-id="2ffb6-139">X</span></span>        |
  | <span data-ttu-id="2ffb6-140">Komentuoti</span><span class="sxs-lookup"><span data-stu-id="2ffb6-140">Comment</span></span>           | <span data-ttu-id="2ffb6-141">Eilutė</span><span class="sxs-lookup"><span data-stu-id="2ffb6-141">String</span></span>    |          |
  | <span data-ttu-id="2ffb6-142">Būsena</span><span class="sxs-lookup"><span data-stu-id="2ffb6-142">Status</span></span>            | <span data-ttu-id="2ffb6-143">Išvardijimas</span><span class="sxs-lookup"><span data-stu-id="2ffb6-143">Enum</span></span>      | <span data-ttu-id="2ffb6-144">X</span><span class="sxs-lookup"><span data-stu-id="2ffb6-144">X</span></span>        |
  | <span data-ttu-id="2ffb6-145">Suma</span><span class="sxs-lookup"><span data-stu-id="2ffb6-145">Amount</span></span>            | <span data-ttu-id="2ffb6-146">Tikrasis</span><span class="sxs-lookup"><span data-stu-id="2ffb6-146">Real</span></span>      |          |
  | <span data-ttu-id="2ffb6-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="2ffb6-147">HalfDayDefinition</span></span> | <span data-ttu-id="2ffb6-148">Išvardijimas</span><span class="sxs-lookup"><span data-stu-id="2ffb6-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="2ffb6-149">Veiksmai</span><span class="sxs-lookup"><span data-stu-id="2ffb6-149">Actions</span></span>

 | <span data-ttu-id="2ffb6-150">Veiksmo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="2ffb6-150">Action Name</span></span>                               | <span data-ttu-id="2ffb6-151">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="2ffb6-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="2ffb6-152">pateikti</span><span class="sxs-lookup"><span data-stu-id="2ffb6-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="2ffb6-153">Pateikti užklausą, kurią reikia apdoroti naudojant darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="2ffb6-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="2ffb6-154">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="2ffb6-154">See also</span></span>

- [<span data-ttu-id="2ffb6-155">Prašymo išeiti atostogų pateikimas darbo eigai</span><span class="sxs-lookup"><span data-stu-id="2ffb6-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="2ffb6-156">Autentifikavimas</span><span class="sxs-lookup"><span data-stu-id="2ffb6-156">Authentication</span></span>](hr-developer-api-authentication.md)