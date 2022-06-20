---
title: Samdymo užklausos būsena
description: Šiame straipsnyje aprašoma įdarbinimo užklausos būsenos pasirinktis, nustatyta Dynamics 365 Human Resources.
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
ms.openlocfilehash: 6a8cb8bc61786425c996b976a2914e7b650e3941
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859610"
---
# <a name="recruiting-request-status"></a>Samdymo užklausos būsena


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašoma įdarbinimo užklausos būsenos pasirinktis, nustatyta Dynamics 365 Human Resources.

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
