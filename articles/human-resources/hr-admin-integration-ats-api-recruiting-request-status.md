---
title: Samdymo užklausos būsena
description: Šioje temoje aprašoma samdymo užklausos būsenos parinktis nustatyta „Dynamics 365 Human Resources“.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d845179077fc2e04dfb3bd05eaa70b0a2a016121
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067106"
---
# <a name="recruiting-request-status"></a>Samdymo užklausos būsena


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašoma samdymo užklausos būsenos parinktis nustatyta „Dynamics 365 Human Resources“.

Fizinis pavadinimas: mshr_hcmrecruitingrequeststatus

Toks numeravimas suteikia parinktį nustatytą samdymo užklausos verčių būsenai.

| Reikšmė | Žyma | Aprašas |
| --- | --- | --- |
| 200000000 | Juodraštis | Užklausa yra šablonas ir nėra parengta įjungtam samdymui. |
| 200000001 | Peržiūrima | Užklausa buvo pateikta ir yra nukreipta darbo eigos patvirtinimui. Prieinama tik įjungus darbo eigą. |
| 200000002 | Laukia | Užklausa laukia darbo eigos veiksmo. Prieinama tik įjungus darbo eigą. |
| 200000003 | Atšaukti | Užklausa atšaukta. Prieinama tik įjungus darbo eigą. |
| 200000004 | Uždrausta | Užklausa buvo atmesta. Prieinama tik įjungus darbo eigą. |
| 200000005 | Aktyvios | Bet kuri darbo eiga yra užbaigta ir patvirtinta, o užklausa parengta įjungtam samdmymui. |
| 200000006 | Uždaryta | Samdymo užklausa yra užverta. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>
[Pavyzdinė užklausa Samdymo prašymui](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
