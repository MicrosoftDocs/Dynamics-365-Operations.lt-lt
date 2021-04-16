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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44e23a076733bac782a0366aeba3456911522abe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803638"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="dccfd-103">MyLeaveRequests apžvalga</span><span class="sxs-lookup"><span data-stu-id="dccfd-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="dccfd-104">Objektas MyLeaveRequests programoje „Microsoft Dynamics 365 Human Resources“ pateikia sistemoje esančių atostogų užklausų sąrašą, apribotą iki užklausų, pasiekiamų dabartiniam vartotojui, siunčiančiam užklausą šiam objektui.</span><span class="sxs-lookup"><span data-stu-id="dccfd-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="dccfd-105">Raktas</span><span class="sxs-lookup"><span data-stu-id="dccfd-105">Key</span></span>

  | <span data-ttu-id="dccfd-106">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="dccfd-106">Property Name</span></span> | <span data-ttu-id="dccfd-107">Duomenų tipas</span><span class="sxs-lookup"><span data-stu-id="dccfd-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="dccfd-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="dccfd-108">dataAreaId</span></span>    | <span data-ttu-id="dccfd-109">Eilutė</span><span class="sxs-lookup"><span data-stu-id="dccfd-109">String</span></span>    |
  | <span data-ttu-id="dccfd-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="dccfd-110">RequestId</span></span>     | <span data-ttu-id="dccfd-111">Eilutė</span><span class="sxs-lookup"><span data-stu-id="dccfd-111">String</span></span>    |
  | <span data-ttu-id="dccfd-112">„LeaveType”</span><span class="sxs-lookup"><span data-stu-id="dccfd-112">LeaveType</span></span>     | <span data-ttu-id="dccfd-113">Eilutė</span><span class="sxs-lookup"><span data-stu-id="dccfd-113">String</span></span>    |
  | <span data-ttu-id="dccfd-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="dccfd-114">LeaveDate</span></span>     | <span data-ttu-id="dccfd-115">Data</span><span class="sxs-lookup"><span data-stu-id="dccfd-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="dccfd-116">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="dccfd-116">Properties</span></span>

  | <span data-ttu-id="dccfd-117">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="dccfd-117">Property Name</span></span>     | <span data-ttu-id="dccfd-118">Duomenų tipas</span><span class="sxs-lookup"><span data-stu-id="dccfd-118">Data Type</span></span> | <span data-ttu-id="dccfd-119">Būtinas</span><span class="sxs-lookup"><span data-stu-id="dccfd-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="dccfd-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="dccfd-120">dataAreaId</span></span>        | <span data-ttu-id="dccfd-121">Eilutė</span><span class="sxs-lookup"><span data-stu-id="dccfd-121">String</span></span>    | <span data-ttu-id="dccfd-122">X</span><span class="sxs-lookup"><span data-stu-id="dccfd-122">X</span></span>        |
  | <span data-ttu-id="dccfd-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="dccfd-123">RequestId</span></span>         | <span data-ttu-id="dccfd-124">Eilutė</span><span class="sxs-lookup"><span data-stu-id="dccfd-124">String</span></span>    | <span data-ttu-id="dccfd-125">X</span><span class="sxs-lookup"><span data-stu-id="dccfd-125">X</span></span>        |
  | <span data-ttu-id="dccfd-126">„LeaveType”</span><span class="sxs-lookup"><span data-stu-id="dccfd-126">LeaveType</span></span>         | <span data-ttu-id="dccfd-127">Eilutė</span><span class="sxs-lookup"><span data-stu-id="dccfd-127">String</span></span>    | <span data-ttu-id="dccfd-128">X</span><span class="sxs-lookup"><span data-stu-id="dccfd-128">X</span></span>        |
  | <span data-ttu-id="dccfd-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="dccfd-129">LeaveDate</span></span>         | <span data-ttu-id="dccfd-130">Data</span><span class="sxs-lookup"><span data-stu-id="dccfd-130">Date</span></span>      | <span data-ttu-id="dccfd-131">X</span><span class="sxs-lookup"><span data-stu-id="dccfd-131">X</span></span>        |
  | <span data-ttu-id="dccfd-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="dccfd-132">ReasonCodeId</span></span>      | <span data-ttu-id="dccfd-133">Eilutė</span><span class="sxs-lookup"><span data-stu-id="dccfd-133">String</span></span>    |          |
  | <span data-ttu-id="dccfd-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="dccfd-134">PersonnelNumber</span></span>   | <span data-ttu-id="dccfd-135">Eilutė</span><span class="sxs-lookup"><span data-stu-id="dccfd-135">String</span></span>    | <span data-ttu-id="dccfd-136">X</span><span class="sxs-lookup"><span data-stu-id="dccfd-136">X</span></span>        |
  | <span data-ttu-id="dccfd-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="dccfd-137">RequestDate</span></span>       | <span data-ttu-id="dccfd-138">Data</span><span class="sxs-lookup"><span data-stu-id="dccfd-138">Date</span></span>      | <span data-ttu-id="dccfd-139">X</span><span class="sxs-lookup"><span data-stu-id="dccfd-139">X</span></span>        |
  | <span data-ttu-id="dccfd-140">Komentuoti</span><span class="sxs-lookup"><span data-stu-id="dccfd-140">Comment</span></span>           | <span data-ttu-id="dccfd-141">Eilutė</span><span class="sxs-lookup"><span data-stu-id="dccfd-141">String</span></span>    |          |
  | <span data-ttu-id="dccfd-142">Būsena</span><span class="sxs-lookup"><span data-stu-id="dccfd-142">Status</span></span>            | <span data-ttu-id="dccfd-143">Išvardijimas</span><span class="sxs-lookup"><span data-stu-id="dccfd-143">Enum</span></span>      | <span data-ttu-id="dccfd-144">X</span><span class="sxs-lookup"><span data-stu-id="dccfd-144">X</span></span>        |
  | <span data-ttu-id="dccfd-145">Suma</span><span class="sxs-lookup"><span data-stu-id="dccfd-145">Amount</span></span>            | <span data-ttu-id="dccfd-146">Tikrasis</span><span class="sxs-lookup"><span data-stu-id="dccfd-146">Real</span></span>      |          |
  | <span data-ttu-id="dccfd-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="dccfd-147">HalfDayDefinition</span></span> | <span data-ttu-id="dccfd-148">Išvardijimas</span><span class="sxs-lookup"><span data-stu-id="dccfd-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="dccfd-149">Veiksmai</span><span class="sxs-lookup"><span data-stu-id="dccfd-149">Actions</span></span>

 | <span data-ttu-id="dccfd-150">Veiksmo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="dccfd-150">Action Name</span></span>                               | <span data-ttu-id="dccfd-151">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="dccfd-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="dccfd-152">pateikti</span><span class="sxs-lookup"><span data-stu-id="dccfd-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="dccfd-153">Pateikti užklausą, kurią reikia apdoroti naudojant darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="dccfd-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="dccfd-154">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="dccfd-154">See also</span></span>

- [<span data-ttu-id="dccfd-155">Prašymo išeiti atostogų pateikimas darbo eigai</span><span class="sxs-lookup"><span data-stu-id="dccfd-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="dccfd-156">Autentifikavimas</span><span class="sxs-lookup"><span data-stu-id="dccfd-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]