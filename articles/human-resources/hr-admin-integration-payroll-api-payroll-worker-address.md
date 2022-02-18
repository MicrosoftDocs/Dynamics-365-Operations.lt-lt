---
title: Algalapio darbuotojo adresas
description: Šioje temoje pateikiama informacija ir Algalapio darbuotojo adreso objekto užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 70e42cbf657a28327699d927731edd36de7c4a64
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069762"
---
# <a name="payroll-worker-address"></a>Algalapio darbuotojo adresas


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas Darbuotojo algalapio adreso objektas „Dynamics 365 Human Resources“.

Faktinis pavadinimas: „mshr_payrollworkeraddressentity”.

### <a name="description"></a>Aprašas

Šis objektas pateikia nurodyto darbuotojo algalapio buvimo vietą ir algalapio darbo vietą.

## <a name="properties"></a>Ypatybės

| Ypatybė</br>**Faktinis pavadinimas**</br>**_Tipas_** | Naudoti | Aprašymas |
| --- | --- | --- |
| **Darbuotojo numeris**</br>„mshr_personnelnumber”</br>*Eilutė* | Tik skaitomas | Unikalus darbuotojo personalo numeris. |
| **Vietos ID**</br>mshr_locationidbr>*Eilutė* | Tik skaitomas | Adreso ID. |
| **Gyveno adresu**</br>„mshr_islivedinaddressbr” </br> *[„mshr_NoYes” parinkties nustatymas](hr-admin-integration-payroll-api-no-yes.md)* | Tik skaitomas | Vertė, nurodanti, ar adresas yra darbuotojo vieta. |
| **Dirbo adresu** </br> „mshr_isworkedinaddressbr” </br>*[„mshr_NoYes” parinkties nustatymas](hr-admin-integration-payroll-api-no-yes.md)* | Tik skaitomas | Vertė, nurodanti, ar adresas yra darbuotojo vieta. |
| **Šalies regionas**</br>mshr_countryregionid</br>*Eilutė* | Tik skaitomas</br>Būtina | Adrese nurodytas šalies regionas ar šalis. |
| **Pašto kodas (ZIP)**</br>mshr_zipcode<br>*Eilutė* | Tik skaitomas | Darbuotojui apibrėžtas identifikacijos numeris. |
| **Gatvė**</br>mshr_street</br>*Eilutė* | Tik skaitomas | Adrese nurodyta gatvė. |
| **Miestas**</br>mshr_city</br>*Eilutė* | Tik skaitomas | Adrese nurodytas miestas. |
| **Apskritis**</br>mshr_state</br>*Eilutė* | Tik skaitomas | Adrese nurodyta šalies valstija ar apskritis. |
| **Apskritis**</br>mshr_county</br>*Eilutė* | Tik skaitomas | Adrese nurodyta šalis. |
| **Galioja nuo**</br>„mshr_postaladdressvalidfrom”</br>*Datos ir Laiko poslinkis* | Tik skaitomas | Data, nuo kurios galioja adresas. |
| **Galioja iki**</br>„mshr_postaladdressvalidto”</br>*Datos ir Laiko poslinkis* | Tik skaitomas | Data, nuo kurios galioja adresas. |
| **Pirminis laukas**</br>mshr_primaryfield</br>*Eilutė* | Tik skaitomas | Pirminis laukas. |
| **Algalapio darbuotojo adreso ID**</br>„mshr_payrollworkeraddressentityid”</br>*GUID* | Sistemos sugeneruota | Sistemos sugeneruota visuotinai unikali identifikatoriaus (GUID) vertė, norint unikaliai identifikuoti adresą. |

## <a name="relations"></a>Ryšiai

| Ypatybės vertė | Susijęs objektas | Naršymo ypatybė | Rinkimo tipas |
| --- | --- | --- | --- |
| _mshr_fk_worker_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Worker_id | mshr_FK_PayrollEmployeeEntity_Address |

## <a name="example-query"></a>Pavyzdinė užklausa

**Prašymas**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Atsiliepimas**

```json
{
    "mshr_personnelnumber": "000041",
    "mshr_locationid": "000000538",
    "mshr_islivedinaddress": 200000001,
    "mshr_isworkedinaddress": 200000000,
    "mshr_countryregionid": "USA",
    "mshr_zipcode": "99025",
    "mshr_street": "6543 Cypress Ave",
    "mshr_city": "Tacoma",
    "mshr_state": "WA",
    "mshr_county": "KING",
    "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
    "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
    "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
    "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```

## <a name="see-also"></a>Taip pat žiūrėkite

[Algalapių integravimo API įžanga](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
