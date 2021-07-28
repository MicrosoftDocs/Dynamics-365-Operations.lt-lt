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
ms.openlocfilehash: 1ff65a0518232275f7c5d0b4a70d04f77e4936c5
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314118"
---
# <a name="payroll-worker-address"></a>Algalapio darbuotojo adresas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas Darbuotojo algalapio adreso objektas „Dynamics 365 Human Resources“.

Faktinis pavadinimas: „mshr_payrollworkeraddressentity”.

### <a name="description"></a>Aprašas

Šis objektas pateikia nurodyto darbuotojo algalapio buvimo vietą ir algalapio darbo vietą.

## <a name="properties"></a>Ypatybės

| Ypatybė</br>**Faktinis pavadinimas**</br>**_Tipas_** | Naudoti | Aprašas |
| --- | --- | --- |
| **Miestas**</br>mshr_city</br>*Eilutė* | Tik skaitomas</br>Būtina | Adrese nurodytas miestas.   |
| **Darbuotojo numeris**</br>„mshr_personnelnumber”</br>*Eilutė* | Tik skaitomas</br>Būtina | Unikalus darbuotojo personalo numeris.  |
| **Šalies regionas**</br>mshr_countryregionid</br>*Eilutė* | Tik skaitomas</br>Būtina | Adrese nurodytas šalies regionas.  |
| **Galioja nuo**</br>„mshr_postaladdressvalidfrom”</br>*Datos ir Laiko poslinkis* | Tik skaitomas </br>Būtina | Data, nuo kurios galioja adresas. |
| **Dirbo adresu** </br> „mshr_isworkedinaddressbr” </br>*[„mshr_NoYes” parinkties nustatymas](hr-admin-integration-payroll-api-no-yes.md)* | Tik skaitomas</br>Būtina | Nurodo, ar adresas yra tas, kuriuo dirba darbuotojas. |
| **Apygarda**</br>mshr_county</br>*Eilutė* | Tik skaitomas</br>Būtina | Adrese nurodyta apygarda.  |
| **Algalapio darbuotojo adreso ID**</br>„mshr_payrollworkeraddressentityid”</br>*GUID* | Būtina</br>Sistemos sugeneruota | Sistemos sukurta GUID reikšmė, skirta unikaliai atpažinti adresą.  |
| **Pirminis laukas**</br>mshr_primaryfield</br>*Eilutė* | Tik skaitomas</br>Būtina |  |
| **Gatvė**</br>mshr_street</br>*Eilutė* | Tik skaitomas</br>Būtina | Adrese nurodyta gatvė. |
| **Galioja iki**</br>„mshr_postaladdressvalidto”</br>*Datos ir Laiko poslinkis* | Tik skaitomas </br>Būtina | Data, iki kurios galioja adresas.  |
| **Vietos ID**</br>mshr_locationidbr>*Eilutė* | Tik skaitomas <br>Būtina | Adreso ID.  |
| **Pašto kodas (ZIP)**</br>mshr_zipcode<br>*Eilutė* | Tik skaitomas <br>Būtina |Darbuotojui apibrėžtas identifikacijos numeris.  |
| **Gyveno adresu**</br>„mshr_islivedinaddressbr” </br> *[„mshr_NoYes” parinkties nustatymas](hr-admin-integration-payroll-api-no-yes.md)* | Tik skaitomas</br>Būtina | Nurodo, ar adresas yra tas, kuriuo gyvena darbuotojas. |
| **Apskritis**</br>mshr_state</br>*Eilutė* | Tik skaitomas</br>Būtina | Adrese nurodyta valstija.  |

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
