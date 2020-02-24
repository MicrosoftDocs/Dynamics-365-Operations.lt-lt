---
title: Prašymo išeiti atostogų pateikimas darbo eigai
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
ms.openlocfilehash: 008ee231ca9f0459e332b17cea9f2a3f3e3cc2a5
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009986"
---
# <a name="submit-a-leave-request-to-workflow"></a>Prašymo išeiti atostogų pateikimas darbo eigai

„Microsoft Dynamics 365 Human Resources“ galite naudoti „MyLeaveRequests submit()“ taikomojo programavimo sąsają (API), kad pateiktumėte atostogų prašymų į darbo eigą. Ši API pateikiamas kaip veiksmas „MyLeaveRequestst OData“ objekte.

## <a name="prerequisites"></a>Būtinieji komponentai

Atostogų užklausa turi būti įrašyta duomenų bazėje ir turi būti atgaunama per „MyLeaveRequests“ objektą.

## <a name="permissions"></a>Teisės

Norint iškviesti šią API reikia vienos iš šių teisių. Daugiau informacijos apie teises ir kaip jas pasirinkti, žr. [Autentifikavimas](hr-developer-api-authentication.md).

| Teisės tipas                    | Teisės (nuo mažiausių teisių iki didžiausių teisių) |
|------------------------------------|--------------------------------------------------------|
| Perduota (darbo arba mokyklos paskyra) | vartotojas\_apsimetimas                                    |

## <a name="https-request"></a>HTTPS užklausa

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

Užklausa atitinka „OData“ standartus. Parametrai {requestId}, {leaveType}, {leaveDate} ir {dataArea} nurodomi laukams, kurie sudaro sudėtinį objekto „MyLeaveRequests“ srities raktą.

> [!NOTE]
> Jei objekto „MyLeaveRequests“ laukai priklauso atskirai atostogų užklausos eilutei, iškvietus pateikimą, API pateiks visą atostogų užklausą (visas eilutes) į darbo eigą.

### <a name="request-headers"></a>Užklausų antraštės

| Antraštė         | Value                     |
|----------------|---------------------------|
| Autorizavimas  | Pateikėjo {token} (privaloma) |
| Turinio tipas   | programa / json          |

### <a name="request-body"></a>Užklausos tekstas

Naudodami šį metodą, nepateikite užklausos teksto.

### <a name="response"></a>Atsiliepimas

Sėkmingas atsakymas visuomet yra atsakymas **204 nėra turinio**.

Neautorizuotos kvietyklės gaus atsakymą **401 neautorizuota** arba **403 draudžiama**.

Jei pateikti nepavyko (pvz., dėl patvirtinimo), atsakymas bus **500 serverio klaida**, o atsakymo tekste bus JSON objektas ir daugiau informacijos.

## <a name="example"></a>Pavyzdys

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

## <a name="validation-and-error-messages"></a>Tikrinimas ir klaidų pranešimai

Iškviesdama pateikimo API, prieš pateikdama, „Human Resources“ atlieka verslo logikos patikrinimą, užtikrindama, kad atostogų užklausa yra tinkamos pateikti būsenos. Jei patikrinti nepavyksta, kaip atsakymą galbūt gausite tokius klaidos pranešimus:

 - Pateikus užklausą, „{LeaveTypeId}“ balansas nukris žemiau leidžiamo minimalaus balanso ​{date}.
 - Baigtos būsenos atostogų užklausos pateikti nepavyksta.
 - Nepavyksta pateikti ar įrašyti užklausos, nes nebuvo atlikta pakeitimų. Pridėkite arba atnaujinkite sumą arba atostogų tipą ir bandykite dar kartą.
 - Įvestoje atostogų užklausoje yra viena ar daugiau tos pačios datos dienų ir atostogų tipų kaip ir esamoje laukiančioje užklausoje. Atšaukite esamą užklausą, kad atliktumėte pakeitimus.
 - Priežasties kodas {ReasonCodeId} netaikomas jokiam prašyme nurodytam atostogų tipui.
 - Atostogų tipui {LeaveTypeId} būtinas priežasties kodas. Pasirinkti tinkamą tipą ir priežasties kodą.
 - Atostogų laikas nebuvo sėkmingai pateiktas. Atostogų laikas buvo įrašytas kaip užklausos juodraštis.

## <a name="see-also"></a>Taip pat žiūrėkite

- [MyLeaveRequests apžvalga](hr-developer-api-myleaverequests-overview.md)
- [Autentifikavimas](hr-developer-api-authentication.md)