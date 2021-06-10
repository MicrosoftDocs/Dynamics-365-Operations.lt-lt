---
title: Prašymo išeiti atostogų pateikimas darbo eigai
description: „Microsoft Dynamics 365 Human Resources“ galite naudoti „MyLeaveRequests submit()“ taikomojo programavimo sąsają (API), kad pateiktumėte atostogų prašymų į darbo eigą.
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
ms.openlocfilehash: 9b3151cb042012a167854a1e69b55b36981dab19
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054577"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="6869c-103">Prašymo išeiti atostogų pateikimas darbo eigai</span><span class="sxs-lookup"><span data-stu-id="6869c-103">Submit a leave request to workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6869c-104">„Microsoft Dynamics 365 Human Resources“ galite naudoti „MyLeaveRequests submit()“ taikomojo programavimo sąsają (API), kad pateiktumėte atostogų prašymų į darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="6869c-104">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="6869c-105">Ši API pateikiamas kaip veiksmas „MyLeaveRequestst OData“ objekte.</span><span class="sxs-lookup"><span data-stu-id="6869c-105">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6869c-106">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="6869c-106">Prerequisites</span></span>

<span data-ttu-id="6869c-107">Atostogų užklausa turi būti įrašyta duomenų bazėje ir turi būti atgaunama per „MyLeaveRequests“ objektą.</span><span class="sxs-lookup"><span data-stu-id="6869c-107">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="6869c-108">Teisės</span><span class="sxs-lookup"><span data-stu-id="6869c-108">Permissions</span></span>

<span data-ttu-id="6869c-109">Norint iškviesti šią API reikia vienos iš šių teisių.</span><span class="sxs-lookup"><span data-stu-id="6869c-109">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="6869c-110">Daugiau informacijos apie teises ir kaip jas pasirinkti, žr. [Autentifikavimas](hr-developer-api-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="6869c-110">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="6869c-111">Teisės tipas</span><span class="sxs-lookup"><span data-stu-id="6869c-111">Permission type</span></span>                    | <span data-ttu-id="6869c-112">Teisės (nuo mažiausių teisių iki didžiausių teisių)</span><span class="sxs-lookup"><span data-stu-id="6869c-112">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="6869c-113">Perduota (darbo arba mokyklos paskyra)</span><span class="sxs-lookup"><span data-stu-id="6869c-113">Delegated (work or school account)</span></span> | <span data-ttu-id="6869c-114">vartotojas\_apsimetimas</span><span class="sxs-lookup"><span data-stu-id="6869c-114">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="6869c-115">HTTPS užklausa</span><span class="sxs-lookup"><span data-stu-id="6869c-115">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="6869c-116">Užklausa atitinka „OData“ standartus.</span><span class="sxs-lookup"><span data-stu-id="6869c-116">The request conforms to OData standards.</span></span> <span data-ttu-id="6869c-117">Parametrai {requestId}, {leaveType}, {leaveDate} ir {dataArea} nurodomi laukams, kurie sudaro sudėtinį objekto „MyLeaveRequests“ srities raktą.</span><span class="sxs-lookup"><span data-stu-id="6869c-117">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="6869c-118">Jei objekto „MyLeaveRequests“ laukai priklauso atskirai atostogų užklausos eilutei, iškvietus pateikimą, API pateiks visą atostogų užklausą (visas eilutes) į darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="6869c-118">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="6869c-119">Užklausų antraštės</span><span class="sxs-lookup"><span data-stu-id="6869c-119">Request headers</span></span>

| <span data-ttu-id="6869c-120">Antraštė</span><span class="sxs-lookup"><span data-stu-id="6869c-120">Header</span></span>         | <span data-ttu-id="6869c-121">Value</span><span class="sxs-lookup"><span data-stu-id="6869c-121">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="6869c-122">Autorizavimas</span><span class="sxs-lookup"><span data-stu-id="6869c-122">Authorization</span></span>  | <span data-ttu-id="6869c-123">Pateikėjo {token} (privaloma)</span><span class="sxs-lookup"><span data-stu-id="6869c-123">Bearer {token} (required)</span></span> |
| <span data-ttu-id="6869c-124">Turinio tipas</span><span class="sxs-lookup"><span data-stu-id="6869c-124">Content-Type</span></span>   | <span data-ttu-id="6869c-125">programa / json</span><span class="sxs-lookup"><span data-stu-id="6869c-125">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="6869c-126">Užklausos tekstas</span><span class="sxs-lookup"><span data-stu-id="6869c-126">Request body</span></span>

<span data-ttu-id="6869c-127">Naudodami šį metodą, nepateikite užklausos teksto.</span><span class="sxs-lookup"><span data-stu-id="6869c-127">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="6869c-128">Atsiliepimas</span><span class="sxs-lookup"><span data-stu-id="6869c-128">Response</span></span>

<span data-ttu-id="6869c-129">Sėkmingas atsakymas visuomet yra atsakymas **204 nėra turinio**.</span><span class="sxs-lookup"><span data-stu-id="6869c-129">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="6869c-130">Neautorizuotos kvietyklės gaus atsakymą **401 neautorizuota **arba** 403 draudžiama**.</span><span class="sxs-lookup"><span data-stu-id="6869c-130">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="6869c-131">Jei pateikti nepavyko (pvz., dėl patvirtinimo), atsakymas bus **500 serverio klaida**, o atsakymo tekste bus JSON objektas ir daugiau informacijos.</span><span class="sxs-lookup"><span data-stu-id="6869c-131">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="6869c-132">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="6869c-132">Example</span></span>

```http
POST https://aos-rts-sf-550e5c091f6-prod-westus2.hr.talent.dynamics.com/namespaces/b2eb8003-334f-4a84-ab63-edbe23569090/data/MyLeaveRequests(RequestId='USMF-000065', LeaveType='Vacation', LeaveDate=2019-10-04T12:00:00Z, dataAreaId='USMF')/Microsoft.Dynamics.DataEntities.submit
```

```json
{
  "error": {
    "code": "",
    "message": "An error has occurred.",
    "innererror": {
      "message": "Exception occurred while executing action submit on Entity MyLeaveRequest: The request would put the 'Vacation' balance below the allowed minimum balance on 9/10/2019.",
      "type": "System.InvalidOperationException",
      "stacktrace": "   at Microsoft.Dynamics.Platform.Integration.Services.OData.Action.ActionInvokable.Invoke()   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateProcessor.ActionInvocation(ChangeOperationContext context, ActionInvokable action)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.<>c__DisplayClass13_0.<ScheduleInvokable>b__0(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActionsInCompanyContext(IEnumerable`1 actionList, ChangeOperationContext operationContext)\r\n   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActions(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.SaveChanges()   at Microsoft.Dynamics.Platform.Integration.Services.OData.AxODataDelegatingHandler.<SaveChangesAsync>d__3.MoveNext()"
    }
  }
}
```

## <a name="validation-and-error-messages"></a><span data-ttu-id="6869c-133">Tikrinimas ir klaidų pranešimai</span><span class="sxs-lookup"><span data-stu-id="6869c-133">Validation and error messages</span></span>

<span data-ttu-id="6869c-134">Iškviesdama pateikimo API, prieš pateikdama, „Human Resources“ atlieka verslo logikos patikrinimą, užtikrindama, kad atostogų užklausa yra tinkamos pateikti būsenos.</span><span class="sxs-lookup"><span data-stu-id="6869c-134">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="6869c-135">Jei patikrinti nepavyksta, kaip atsakymą galbūt gausite tokius klaidos pranešimus:</span><span class="sxs-lookup"><span data-stu-id="6869c-135">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="6869c-136">Pateikus užklausą, „{LeaveTypeId}“ balansas nukris žemiau leidžiamo minimalaus balanso ​{date}.</span><span class="sxs-lookup"><span data-stu-id="6869c-136">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="6869c-137">Baigtos būsenos atostogų užklausos pateikti nepavyksta.</span><span class="sxs-lookup"><span data-stu-id="6869c-137">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="6869c-138">Nepavyksta pateikti ar įrašyti užklausos, nes nebuvo atlikta pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="6869c-138">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="6869c-139">Pridėkite arba atnaujinkite sumą arba atostogų tipą ir bandykite dar kartą.</span><span class="sxs-lookup"><span data-stu-id="6869c-139">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="6869c-140">Įvestoje atostogų užklausoje yra viena ar daugiau tos pačios datos dienų ir atostogų tipų kaip ir esamoje laukiančioje užklausoje.</span><span class="sxs-lookup"><span data-stu-id="6869c-140">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="6869c-141">Atšaukite esamą užklausą, kad atliktumėte pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="6869c-141">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="6869c-142">Priežasties kodas {ReasonCodeId} netaikomas jokiam prašyme nurodytam atostogų tipui.</span><span class="sxs-lookup"><span data-stu-id="6869c-142">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="6869c-143">Atostogų tipui {LeaveTypeId} būtinas priežasties kodas.</span><span class="sxs-lookup"><span data-stu-id="6869c-143">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="6869c-144">Pasirinkti tinkamą tipą ir priežasties kodą.</span><span class="sxs-lookup"><span data-stu-id="6869c-144">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="6869c-145">Atostogų laikas nebuvo sėkmingai pateiktas.</span><span class="sxs-lookup"><span data-stu-id="6869c-145">The time off was not submitted successfully.</span></span> <span data-ttu-id="6869c-146">Atostogų laikas buvo įrašytas kaip užklausos juodraštis.</span><span class="sxs-lookup"><span data-stu-id="6869c-146">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="6869c-147">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="6869c-147">See also</span></span>

- [<span data-ttu-id="6869c-148">MyLeaveRequests apžvalga</span><span class="sxs-lookup"><span data-stu-id="6869c-148">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="6869c-149">Autentifikavimas</span><span class="sxs-lookup"><span data-stu-id="6869c-149">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]