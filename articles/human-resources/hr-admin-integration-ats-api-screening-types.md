---
title: Atrankos tipai
description: Šiame straipsnyje aprašomas atrankos tipų objektas, skirtas Dynamics 365 Human Resources.
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
ms.openlocfilehash: 95f4a3dce6851c7080ac665f5922e3b5877fa9f3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880544"
---
# <a name="screening-types"></a>Atrankos tipai


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašomas atrankos tipų objektas, skirtas Dynamics 365 Human Resources.

Fizinis pavadinimas: mshr_hcmscreeningtypeentity

## <a name="description"></a>aprašymas

Šis objektas aprašo atrankų tipus, kurie nustatyti bendrovės išankstiniam įdarbinimui ir vykstančiam darbuotojų atrankos procesams.

## <a name="json-representation"></a>JSON atstovavimas

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | aprašymas |
| --- | --- | --- |
| **Atrankos tipo objekto ID**<br>mshr_hcmscreeningtypeentityid<br>*GUID* | Tik skaitomas<br>Būtina<br>Sukurta sistemos | Unikalus pirminis identifikatorius asmens tipo įrašui. |
| **Atrankos tipo ID**<br>mshr_screeningtypeid<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Vartotojo nustatytas unikalus identifikatorius atrankos tipui. |
| **Aprašas**<br>mshr_description<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Atrankos tipo aprašas. |
| **Dažnio vienetas**<br>mshr_frequencyunit<br>*mshr_hcmfrequencyunit parinkties nustatymas* | Skaitymas/rašymas<br>Būtina | Aprašo dažnumą, kuriuo atranka turi būti užbaigta paskirto asmens. |
| **Kurti iš**<br>mshr_generatefrom<br>*mshr_hcmfrequencygeneratefrom parinkties nustatymas* | Skaitymas/rašymas<br>Būtina | Jei dažnumo vertė yra bet kokia kita vertė nei „Tik vieną kartą“, Kurti iš vertė nustato datą, nuo kurios bus skaičiuojamas kitas atrankos įvykis. |
| **Dažnio intervalas**<br>mshr_frequencyinterval<br>*Sveikasis skaičius* | Skaitymas/rašymas<br>Būtina | Jei dažnumo vertė yra bet kokia kita vertė nei „Tik vieną kartą“, turite nustatyti intervalą laiko vienetams tarp kiekvieno atrankos įvykio. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>
[Samdomo pretendento pavyzdžio užklausa](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
