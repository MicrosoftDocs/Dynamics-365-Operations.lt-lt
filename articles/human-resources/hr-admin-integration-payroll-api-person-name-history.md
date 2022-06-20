---
title: Asmens vardų ir pavardžių retrospektyva
description: Šiame straipsnyje pateikiama informacija ir asmens vardų retrospektyvos objekto, pavyzdžiui, užklausa Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e34b0d7bebd1c4037347161087ff3a4485a58878
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875777"
---
# <a name="person-name-history"></a>Asmens vardų ir pavardžių retrospektyva


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašomas asmens vardų retrospektyvos objektas, kurio pavadinimas yra Dynamics 365 Human Resources

Fizinis pavadinimas: mshr_dirpersonnamehistoricalentity.

### <a name="description"></a>Aprašymas

Šis objektas pateikia informaciją apie tam kurio vardo istorijos išmokų planą.

> [!IMPORTANT] 
> **Vardo**, **Vidurinio vardo**, **Pavardės**, **Vardas galioja nuo** ir **Vardas galioja iki** laukų nebegalima naudoti šiame algalapio darbuotojo objekte. Jie buvo panaikinti siekiant užtikrinti, kad vienas duomenų efektyvus duomenų šaltinis remtųsi šiuo objektu.

## <a name="properties"></a>Ypatybės

| Ypatybė</br>**Faktinis pavadinimas**</br>**_Tipas_** | Naudoti | Aprašymas |
| --- | --- | --- |
| **Vardas**</br>mshr_firstname</br>*Eilutė* | Tik skaitomas | Vardas. |
| **Pavardės priešvardis**</br>mshr_lastnameprefix</br>*Eilutė*) | Tik skaitomas | Pavardės priešdėlis. |
| **Pavardė**</br>mshr_lastname</br>*Eilutė*) | Tik skaitomas | Pavardė. |
| **Antras vardas**</br>mshr_middlename</br>*Eilutė*) | Tik skaitomas | Antras vardas. |
| **Galioja iki**</br>„mshr_validto”</br>*Eilutė*) | Tik skaitomas | Data, nuo kurios galioja vardas. |
| **Šalies numeris**</br>mshr_partynumber</br>*Eilutė* | Tik skaitomas | Vartotojo perskaitomas, sistemos sukurtas unikalus asmens identifikatorius. |
| **Pirminis laukas**</br>mshr_primaryfield</br>*Eilutė* | Tik skaitomas | Unikalus įrašo identifikatorius. |
| **Asmens vardų retrospektyvos objekto ID**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Sistemos sugeneruota | Sistemos sugeneruota visuotinai unikali identifikatoriaus (GUID) vertė, norint unikaliai identifikuoti įrašą. |

## <a name="relations"></a>Ryšiai

| Ypatybės vertė | Susijęs objektas | Naršymo ypatybė | Rinkimo tipas |
| --- | --- | --- | --- |
| Netaikoma | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | Netaikoma | mshr_FK_PayrollEmployeeEntity_Name |

## <a name="example-query-for-payroll-employee"></a>Algalapio darbuotojo užklausos pavyzdys

**Prašymas**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_dirpersonnamehistoricalentities?$filter=mshr_partynumber eq 'HR000001606'
```

**Atsiliepimas**

```json
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "middle",
    "mshr_validto": "2021-09-10T21:23:53Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | ",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-c12b-014105000000",
    "mshr_validfrom": null
},
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | 9/10/2021 09:23:54 pm",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-d20b-000010000000",
    "mshr_validfrom": "2021-09-10T21:23:54Z"
}
```

## <a name="see-also"></a>Taip pat žiūrėkite

[Algalapių integravimo API įžanga](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
