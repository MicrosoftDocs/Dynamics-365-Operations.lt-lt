---
title: Samdymo užklausos pareigų būsena
description: Šioje temoje aprašoma samdymo užklausos pareigų būsenos parinktis nustatyta „Dynamics 365 Human Resources“.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3f7bae64f58f0bdc1603b3c1b5493f1ebcfa8de9
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126055"
---
# <a name="recruiting-request-position-status"></a>Samdymo užklausos pareigų būsena

Šioje temoje aprašoma samdymo užklausos pareigų būsenos parinktis nustatyta „Dynamics 365 Human Resources“.

Fizinis pavadinimas: mshr_hcmrecruitingrequestpositionstatus

Toks numeravimas suteikia parinktį nustatytą visų pareigų būsenos vertėms samdymo užklausai Samdymo užklausos pareigų objekte.

| Reikšmė | Žyma:  | aprašymas |
| --- | --- | --- |
| 200000000 | Atviri | Pareigos samdymo užklausoje yra atviros samdymui. Tai nerodo, kad šiuo metu nėra jokio aktyvaus pareigų priskyrimo pareigoms. Samdymo metu pareigose gali būti darbuotojas. Tai rodo tik tai, kad pareigos yra prieinamos samdymui samdymo užklausos kontekste. |
| 200000001 | Užpildyta | Darbuotojas buvo atrinktas pareigų priskyrimui. |
| 200000002 | Atšaukti | Samdymo užklausa šioms pareigoms buvo atšaukta. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>
[Pavyzdinė užklausa Samdymo prašymui](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]