---
title: Samdymo užklausos būsena
description: Šioje temoje aprašoma samdymo užklausos būsenos parinktis nustatyta „Dynamics 365 Human Resources“.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 888fbc511bffbecd837c929049006266191da5ba
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5806047"
---
# <a name="recruiting-request-status"></a>Samdymo užklausos būsena

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašoma samdymo užklausos būsenos parinktis nustatyta „Dynamics 365 Human Resources“.

Fizinis pavadinimas: mshr_hcmrecruitingrequeststatus

Toks numeravimas suteikia parinktį nustatytą samdymo užklausos verčių būsenai.

| Reikšmė | Žyma:  | aprašymas |
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