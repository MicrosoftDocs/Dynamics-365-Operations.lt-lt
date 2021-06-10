---
title: Sertifikato tipas
description: Šioje temoje aprašomas sertifikatos tipo objektas „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: b8e979f242eb689b730b7f8a8684b3e697adbee6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054697"
---
# <a name="certificate-type"></a>Sertifikato tipas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas sertifikatos tipo objektas „Dynamics 365 Human Resources“.

Fizinis pavadinimas: mshr_hcmcertificatetypeentity

## <a name="description"></a>aprašymas

Šis objektas nustato profesionalių sertifikato tipų sąrašą, kuris nustatytas žmogiškuosiuose ištekliuose. Objektas nėra būdingas juridiniam asmeniui (įmonei).

## <a name="json-representation"></a>JSON atstovavimas

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | aprašymas |
| --- | --- | --- |
| **Sertifikato tipo objekto ID**<br>mshr_hcmcertificatetypeentityid<br>*GUID* | Tik skaitomas<br>Būtina 
Sukurta sistemos | Unikalus pirminis identifikatorius sertifikato tipui. |
| **Sertifikato tipas**<br>mshr_certificatetype<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Unikalus vartotojo perskaitomas identifikatorius sertifikato tipui. |
| **Aprašas**<br>mshr_description<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Sertifikato tipo aprašas. |
| **Reikalauti naujinimo**<br>mshr_requirerenewal<br>*mshr_noyes parinkties nustatymas* | Skaitymas/rašymas<br>Pasirinktinai | Nurodo, ar naujinimo reikia sertifikatui. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>
[Samdomo pretendento pavyzdžio užklausa](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]