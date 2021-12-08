---
title: Asmens vardų ir pavardžių retrospektyva
description: Šioje temoje pateikiama informacija ir asmens vardo istorijos objekto užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.
author: marcelbf
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 418047a0643ee29b89763dbe2b030753f405b575
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559666"
---
# <a name="person-name-history"></a>Asmens vardų ir pavardžių retrospektyva

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas asmens vardo istorijos objektas „Dynamics 365 Human Resources“.

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