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
ms.openlocfilehash: c2c14a0cc935ad166a2c6600f1e96c3e09ab16ca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465515"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="8b645-103">MyLeaveRequests apžvalga</span><span class="sxs-lookup"><span data-stu-id="8b645-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8b645-104">Objektas MyLeaveRequests programoje „Microsoft Dynamics 365 Human Resources“ pateikia sistemoje esančių atostogų užklausų sąrašą, apribotą iki užklausų, pasiekiamų dabartiniam vartotojui, siunčiančiam užklausą šiam objektui.</span><span class="sxs-lookup"><span data-stu-id="8b645-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="8b645-105">Raktas</span><span class="sxs-lookup"><span data-stu-id="8b645-105">Key</span></span>

  | <span data-ttu-id="8b645-106">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="8b645-106">Property Name</span></span> | <span data-ttu-id="8b645-107">Duomenų tipas</span><span class="sxs-lookup"><span data-stu-id="8b645-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="8b645-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="8b645-108">dataAreaId</span></span>    | <span data-ttu-id="8b645-109">Eilutė</span><span class="sxs-lookup"><span data-stu-id="8b645-109">String</span></span>    |
  | <span data-ttu-id="8b645-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="8b645-110">RequestId</span></span>     | <span data-ttu-id="8b645-111">Eilutė</span><span class="sxs-lookup"><span data-stu-id="8b645-111">String</span></span>    |
  | <span data-ttu-id="8b645-112">„LeaveType”</span><span class="sxs-lookup"><span data-stu-id="8b645-112">LeaveType</span></span>     | <span data-ttu-id="8b645-113">Eilutė</span><span class="sxs-lookup"><span data-stu-id="8b645-113">String</span></span>    |
  | <span data-ttu-id="8b645-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="8b645-114">LeaveDate</span></span>     | <span data-ttu-id="8b645-115">Data</span><span class="sxs-lookup"><span data-stu-id="8b645-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="8b645-116">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="8b645-116">Properties</span></span>

  | <span data-ttu-id="8b645-117">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="8b645-117">Property Name</span></span>     | <span data-ttu-id="8b645-118">Duomenų tipas</span><span class="sxs-lookup"><span data-stu-id="8b645-118">Data Type</span></span> | <span data-ttu-id="8b645-119">Būtinas</span><span class="sxs-lookup"><span data-stu-id="8b645-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="8b645-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="8b645-120">dataAreaId</span></span>        | <span data-ttu-id="8b645-121">Eilutė</span><span class="sxs-lookup"><span data-stu-id="8b645-121">String</span></span>    | <span data-ttu-id="8b645-122">X</span><span class="sxs-lookup"><span data-stu-id="8b645-122">X</span></span>        |
  | <span data-ttu-id="8b645-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="8b645-123">RequestId</span></span>         | <span data-ttu-id="8b645-124">Eilutė</span><span class="sxs-lookup"><span data-stu-id="8b645-124">String</span></span>    | <span data-ttu-id="8b645-125">X</span><span class="sxs-lookup"><span data-stu-id="8b645-125">X</span></span>        |
  | <span data-ttu-id="8b645-126">„LeaveType”</span><span class="sxs-lookup"><span data-stu-id="8b645-126">LeaveType</span></span>         | <span data-ttu-id="8b645-127">Eilutė</span><span class="sxs-lookup"><span data-stu-id="8b645-127">String</span></span>    | <span data-ttu-id="8b645-128">X</span><span class="sxs-lookup"><span data-stu-id="8b645-128">X</span></span>        |
  | <span data-ttu-id="8b645-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="8b645-129">LeaveDate</span></span>         | <span data-ttu-id="8b645-130">Data</span><span class="sxs-lookup"><span data-stu-id="8b645-130">Date</span></span>      | <span data-ttu-id="8b645-131">X</span><span class="sxs-lookup"><span data-stu-id="8b645-131">X</span></span>        |
  | <span data-ttu-id="8b645-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="8b645-132">ReasonCodeId</span></span>      | <span data-ttu-id="8b645-133">Eilutė</span><span class="sxs-lookup"><span data-stu-id="8b645-133">String</span></span>    |          |
  | <span data-ttu-id="8b645-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="8b645-134">PersonnelNumber</span></span>   | <span data-ttu-id="8b645-135">Eilutė</span><span class="sxs-lookup"><span data-stu-id="8b645-135">String</span></span>    | <span data-ttu-id="8b645-136">X</span><span class="sxs-lookup"><span data-stu-id="8b645-136">X</span></span>        |
  | <span data-ttu-id="8b645-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="8b645-137">RequestDate</span></span>       | <span data-ttu-id="8b645-138">Data</span><span class="sxs-lookup"><span data-stu-id="8b645-138">Date</span></span>      | <span data-ttu-id="8b645-139">X</span><span class="sxs-lookup"><span data-stu-id="8b645-139">X</span></span>        |
  | <span data-ttu-id="8b645-140">Komentuoti</span><span class="sxs-lookup"><span data-stu-id="8b645-140">Comment</span></span>           | <span data-ttu-id="8b645-141">Eilutė</span><span class="sxs-lookup"><span data-stu-id="8b645-141">String</span></span>    |          |
  | <span data-ttu-id="8b645-142">Būsena</span><span class="sxs-lookup"><span data-stu-id="8b645-142">Status</span></span>            | <span data-ttu-id="8b645-143">Išvardijimas</span><span class="sxs-lookup"><span data-stu-id="8b645-143">Enum</span></span>      | <span data-ttu-id="8b645-144">X</span><span class="sxs-lookup"><span data-stu-id="8b645-144">X</span></span>        |
  | <span data-ttu-id="8b645-145">Suma</span><span class="sxs-lookup"><span data-stu-id="8b645-145">Amount</span></span>            | <span data-ttu-id="8b645-146">Tikrasis</span><span class="sxs-lookup"><span data-stu-id="8b645-146">Real</span></span>      |          |
  | <span data-ttu-id="8b645-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="8b645-147">HalfDayDefinition</span></span> | <span data-ttu-id="8b645-148">Išvardijimas</span><span class="sxs-lookup"><span data-stu-id="8b645-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="8b645-149">Veiksmai</span><span class="sxs-lookup"><span data-stu-id="8b645-149">Actions</span></span>

 | <span data-ttu-id="8b645-150">Veiksmo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="8b645-150">Action Name</span></span>                               | <span data-ttu-id="8b645-151">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="8b645-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="8b645-152">pateikti</span><span class="sxs-lookup"><span data-stu-id="8b645-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="8b645-153">Pateikti užklausą, kurią reikia apdoroti naudojant darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="8b645-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8b645-154">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="8b645-154">See also</span></span>

- [<span data-ttu-id="8b645-155">Prašymo išeiti atostogų pateikimas darbo eigai</span><span class="sxs-lookup"><span data-stu-id="8b645-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="8b645-156">Autentifikavimas</span><span class="sxs-lookup"><span data-stu-id="8b645-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]