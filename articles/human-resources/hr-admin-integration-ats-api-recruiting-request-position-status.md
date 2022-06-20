---
title: Samdymo užklausos pareigų būsena
description: Šiame straipsnyje aprašoma įdarbinimo užklausos pareigų būsenos pasirinktis, nustatyta Dynamics 365 Human Resources.
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
ms.openlocfilehash: 736bdbfb8759ab61202d1f17e3cdc8294be0ba84
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846420"
---
# <a name="recruiting-request-position-status"></a>Samdymo užklausos pareigų būsena


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašoma įdarbinimo užklausos pareigų būsenos pasirinktis, nustatyta Dynamics 365 Human Resources.

Fizinis pavadinimas: mshr_hcmrecruitingrequestpositionstatus

Toks numeravimas suteikia parinktį nustatytą visų pareigų būsenos vertėms samdymo užklausai Samdymo užklausos pareigų objekte.

| Reikšmė | Žyma | Aprašas |
| --- | --- | --- |
| 200000000 | Atviri | Pareigos samdymo užklausoje yra atviros samdymui. Tai nerodo, kad šiuo metu nėra jokio aktyvaus pareigų priskyrimo pareigoms. Samdymo metu pareigose gali būti darbuotojas. Tai rodo tik tai, kad pareigos yra prieinamos samdymui samdymo užklausos kontekste. |
| 200000001 | Užpildyta | Darbuotojas buvo atrinktas pareigų priskyrimui. |
| 200000002 | Atšaukti | Samdymo užklausa šioms pareigoms buvo atšaukta. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>
[Pavyzdinė užklausa Samdymo prašymui](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
