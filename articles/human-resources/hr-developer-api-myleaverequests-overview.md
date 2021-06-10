---
title: MyLeaveRequests apžvalga
description: Objektas MyLeaveRequests programoje „Microsoft Dynamics 365 Human Resources“ pateikia sistemoje esančių atostogų užklausų sąrašą, apribotą iki užklausų, pasiekiamų dabartiniam vartotojui, siunčiančiam užklausą šiam objektui.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f29d5cf1469b58b4ea1837dc82b9513f5c002609
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054961"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="8eb4a-103">MyLeaveRequests apžvalga</span><span class="sxs-lookup"><span data-stu-id="8eb4a-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8eb4a-104">Objektas MyLeaveRequests programoje „Microsoft Dynamics 365 Human Resources“ pateikia sistemoje esančių atostogų užklausų sąrašą, apribotą iki užklausų, pasiekiamų dabartiniam vartotojui, siunčiančiam užklausą šiam objektui.</span><span class="sxs-lookup"><span data-stu-id="8eb4a-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="8eb4a-105">Raktas</span><span class="sxs-lookup"><span data-stu-id="8eb4a-105">Key</span></span>

  | <span data-ttu-id="8eb4a-106">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="8eb4a-106">Property Name</span></span> | <span data-ttu-id="8eb4a-107">Duomenų tipas</span><span class="sxs-lookup"><span data-stu-id="8eb4a-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="8eb4a-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="8eb4a-108">dataAreaId</span></span>    | <span data-ttu-id="8eb4a-109">Eilutė</span><span class="sxs-lookup"><span data-stu-id="8eb4a-109">String</span></span>    |
  | <span data-ttu-id="8eb4a-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="8eb4a-110">RequestId</span></span>     | <span data-ttu-id="8eb4a-111">Eilutė</span><span class="sxs-lookup"><span data-stu-id="8eb4a-111">String</span></span>    |
  | <span data-ttu-id="8eb4a-112">„LeaveType”</span><span class="sxs-lookup"><span data-stu-id="8eb4a-112">LeaveType</span></span>     | <span data-ttu-id="8eb4a-113">Eilutė</span><span class="sxs-lookup"><span data-stu-id="8eb4a-113">String</span></span>    |
  | <span data-ttu-id="8eb4a-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="8eb4a-114">LeaveDate</span></span>     | <span data-ttu-id="8eb4a-115">Data</span><span class="sxs-lookup"><span data-stu-id="8eb4a-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="8eb4a-116">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="8eb4a-116">Properties</span></span>

  | <span data-ttu-id="8eb4a-117">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="8eb4a-117">Property Name</span></span>     | <span data-ttu-id="8eb4a-118">Duomenų tipas</span><span class="sxs-lookup"><span data-stu-id="8eb4a-118">Data Type</span></span> | <span data-ttu-id="8eb4a-119">Būtinas</span><span class="sxs-lookup"><span data-stu-id="8eb4a-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="8eb4a-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="8eb4a-120">dataAreaId</span></span>        | <span data-ttu-id="8eb4a-121">Eilutė</span><span class="sxs-lookup"><span data-stu-id="8eb4a-121">String</span></span>    | <span data-ttu-id="8eb4a-122">X</span><span class="sxs-lookup"><span data-stu-id="8eb4a-122">X</span></span>        |
  | <span data-ttu-id="8eb4a-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="8eb4a-123">RequestId</span></span>         | <span data-ttu-id="8eb4a-124">Eilutė</span><span class="sxs-lookup"><span data-stu-id="8eb4a-124">String</span></span>    | <span data-ttu-id="8eb4a-125">X</span><span class="sxs-lookup"><span data-stu-id="8eb4a-125">X</span></span>        |
  | <span data-ttu-id="8eb4a-126">„LeaveType”</span><span class="sxs-lookup"><span data-stu-id="8eb4a-126">LeaveType</span></span>         | <span data-ttu-id="8eb4a-127">Eilutė</span><span class="sxs-lookup"><span data-stu-id="8eb4a-127">String</span></span>    | <span data-ttu-id="8eb4a-128">X</span><span class="sxs-lookup"><span data-stu-id="8eb4a-128">X</span></span>        |
  | <span data-ttu-id="8eb4a-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="8eb4a-129">LeaveDate</span></span>         | <span data-ttu-id="8eb4a-130">Data</span><span class="sxs-lookup"><span data-stu-id="8eb4a-130">Date</span></span>      | <span data-ttu-id="8eb4a-131">X</span><span class="sxs-lookup"><span data-stu-id="8eb4a-131">X</span></span>        |
  | <span data-ttu-id="8eb4a-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="8eb4a-132">ReasonCodeId</span></span>      | <span data-ttu-id="8eb4a-133">Eilutė</span><span class="sxs-lookup"><span data-stu-id="8eb4a-133">String</span></span>    |          |
  | <span data-ttu-id="8eb4a-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="8eb4a-134">PersonnelNumber</span></span>   | <span data-ttu-id="8eb4a-135">Eilutė</span><span class="sxs-lookup"><span data-stu-id="8eb4a-135">String</span></span>    | <span data-ttu-id="8eb4a-136">X</span><span class="sxs-lookup"><span data-stu-id="8eb4a-136">X</span></span>        |
  | <span data-ttu-id="8eb4a-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="8eb4a-137">RequestDate</span></span>       | <span data-ttu-id="8eb4a-138">Data</span><span class="sxs-lookup"><span data-stu-id="8eb4a-138">Date</span></span>      | <span data-ttu-id="8eb4a-139">X</span><span class="sxs-lookup"><span data-stu-id="8eb4a-139">X</span></span>        |
  | <span data-ttu-id="8eb4a-140">Komentuoti</span><span class="sxs-lookup"><span data-stu-id="8eb4a-140">Comment</span></span>           | <span data-ttu-id="8eb4a-141">Eilutė</span><span class="sxs-lookup"><span data-stu-id="8eb4a-141">String</span></span>    |          |
  | <span data-ttu-id="8eb4a-142">Būsena</span><span class="sxs-lookup"><span data-stu-id="8eb4a-142">Status</span></span>            | <span data-ttu-id="8eb4a-143">Išvardijimas</span><span class="sxs-lookup"><span data-stu-id="8eb4a-143">Enum</span></span>      | <span data-ttu-id="8eb4a-144">X</span><span class="sxs-lookup"><span data-stu-id="8eb4a-144">X</span></span>        |
  | <span data-ttu-id="8eb4a-145">Suma</span><span class="sxs-lookup"><span data-stu-id="8eb4a-145">Amount</span></span>            | <span data-ttu-id="8eb4a-146">Tikrasis</span><span class="sxs-lookup"><span data-stu-id="8eb4a-146">Real</span></span>      |          |
  | <span data-ttu-id="8eb4a-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="8eb4a-147">HalfDayDefinition</span></span> | <span data-ttu-id="8eb4a-148">Išvardijimas</span><span class="sxs-lookup"><span data-stu-id="8eb4a-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="8eb4a-149">Veiksmai</span><span class="sxs-lookup"><span data-stu-id="8eb4a-149">Actions</span></span>

 | <span data-ttu-id="8eb4a-150">Veiksmo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="8eb4a-150">Action Name</span></span>                               | <span data-ttu-id="8eb4a-151">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="8eb4a-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="8eb4a-152">pateikti</span><span class="sxs-lookup"><span data-stu-id="8eb4a-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="8eb4a-153">Pateikti užklausą, kurią reikia apdoroti naudojant darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="8eb4a-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8eb4a-154">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="8eb4a-154">See also</span></span>

- [<span data-ttu-id="8eb4a-155">Prašymo išeiti atostogų pateikimas darbo eigai</span><span class="sxs-lookup"><span data-stu-id="8eb4a-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="8eb4a-156">Autentifikavimas</span><span class="sxs-lookup"><span data-stu-id="8eb4a-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]