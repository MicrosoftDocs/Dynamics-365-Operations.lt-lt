---
title: Sertifikato tipas
description: Šiame straipsnyje aprašomas sertifikato tipo objektas, skirtas Dynamics 365 Human Resources.
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
ms.openlocfilehash: bfe7f06176098a504f8d2ad1c1431a6f60fe059c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886195"
---
# <a name="certificate-type"></a>Sertifikato tipas


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašomas sertifikato tipo objektas, skirtas Dynamics 365 Human Resources.

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
