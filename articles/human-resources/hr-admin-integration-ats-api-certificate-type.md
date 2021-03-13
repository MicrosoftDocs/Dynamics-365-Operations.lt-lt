---
title: Sertifikato tipas
description: Šioje temoje aprašomas sertifikatos tipo objektas „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: 1d2d53a628ef43d50bd83fd6b62807f44eddd653
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125718"
---
# <a name="certificate-type"></a>Sertifikato tipas

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

