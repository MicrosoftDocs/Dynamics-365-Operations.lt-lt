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
ms.openlocfilehash: 91360b07915ba10472768ac32b473e6daf7163fa8aed24e6aabaaa91f0ec7154
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723676"
---
# <a name="recruiting-request-status"></a>Samdymo užklausos būsena

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