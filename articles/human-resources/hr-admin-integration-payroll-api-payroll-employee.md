---
title: Algalapio darbuotojas
description: Šioje temoje pateikiama informacija ir Algalapio darbuotojo objekto užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.
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
ms.openlocfilehash: 87efbf7063de373e1e0b844ff1b942cdaab4a021
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055057"
---
# <a name="payroll-employee"></a>Algalapio darbuotojas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje pateikiama informacija ir Algalapio darbuotojo objekto užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.

## <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | Aprašas |
| --- | --- | --- |
| **Personalo numeris**<br>„mshr_personnelnumber”<br>*Eilutė* | Tik skaitomas<br>Būtina | Unikalus darbuotojo personalo numeris. |
| **Pirminis laukas**<br>mshr_primaryfield<br>*Eilutė* | Būtina<br>Sistemos sugeneruota |  |
| **Pavardė**<br>mshr_lastname<br>*Eilutė* | Tik skaityti<br>Būtina | Darbuotojo pavardė. |
| **Juridinio subjekto ID**<br>„mshr_legalentityID”<br>*Eilutė* | Tik skaitomas<br>Būtina | Nurodo juridinį asmenį (įmonę). |
| **Galioja nuo**<br>„mshr_namevalidfrom”<br>*Datos ir Laiko poslinkis* | Tik skaitomas <br>Būtina | Data, nuo kurios galioja darbuotojo informacija.  |
| **Giminė**<br>mshr_gender<br>*„Int32”* | Tik skaitomas<br>Būtina | Darbuotojo lytis. |
| **Algalapio darbuotojo objekto ID**<br>„mshr_payrollemployeeentityid”<br>*GUID* | Būtina<br>Sistemos sugeneruota | Sistemos sukurta GUID reikšmė, skirta unikaliai atpažinti darbuotoją. |
| **Įdarbinimo pradžios data**<br>„mshr_employmentstartdate”<br>*Datos ir laiko poslinkis* | Tik skaitomas<br>Būtina | Darbuotojo įdarbinimo pradžios data. |
| **Identifikacijos tipo ID**<br>mshr_identificationtypeid<br>*Eilutė* |Tik skaitomas<br>Būtina | Darbuotojui apibrėžtas identifikacijos tipas. |
| **Įdarbinimo pabaigos data**<br>„mshr_employmentenddate”<br>*Datos ir laiko poslinkis* | Tik skaitomas<br>Būtina |Darbuotojo įdarbinimo pabaiga.  |
| **Srities Duomenys ID**<br>„mshr_dataareaid_id”<br>*GUID* | Būtina <br>Sistemos sugeneruota | Sistemos sukurta GUID vertė, rodanti juridinį subjektą (įmonę). |
| **Galioja iki**<br>„mshr_namevalidto”<br>*Datos ir Laiko poslinkis* |  Tik skaitomas<br>Būtina | Data, iki kurios galioja darbuotojo informacija. |
| **Gimimo data**<br>mshr_birthdate<br>*Datos ir Laiko poslinkis* | Tik skaitomas <br>Būtina | Darbuotojo gimimo data |
| **Identifikacijos numeris iki**<br>mshr_identificationnumber<br>*Eilutė* | Tik skaitomas <br>Būtina |Darbuotojui apibrėžtas identifikacijos numeris.  |
| **Vardas**<br>mshr_firstname<br>*Eilutė* | Tik skaitomas<br>Būtina | Darbuotojo vardas. |
| **Antras vardas**<br>mshr_middlename<br>*Eilutė* | Tik skaitomas<br>Būtina |Darbuotojo antras vardas.  |

## <a name="example-query-for-payroll-employee"></a>Algalapio darbuotojo užklausos pavyzdys

**Prašymas**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_identificationtypeid eq @idtype and mshr_namevalidfrom le @asofdate and mshr_namevalidto ge @asofdate&@personnelnumber='000041'&@idtype='SSN'&@asofdate=2021-04-01
```

**Atsiliepimas**

```json
{
         "mshr_legalentityid": "USMF",
            "mshr_personnelnumber": "000041",
            "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
            "mshr_employmentenddate": "2154-12-31T23:59:59Z",
            "mshr_firstname": "Cassie",
            "mshr_middlename": "Lassie",
            "mshr_lastname": "Hicks",
            "mshr_namevalidfrom": "2021-03-12T20:34:25Z",
            "mshr_namevalidto": "2154-12-31T23:59:59Z",
            "mshr_birthdate": "1987-09-12T00:00:00Z",
            "mshr_gender": 200000002,
            "mshr_identificationtypeid": "SSN",
            "mshr_identificationnumber": "888-99-9342",
            "mshr_dataareaid": "USMF",
            "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
            "_mshr_fk_worker_id_value": "000000ad-0000-0000-d5ff-004105000000",
            "_mshr_fk_employment_id_value": "00000d0d-0000-0000-0600-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollemployeeentityid": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_dataareaid_id_value": null
}
```
