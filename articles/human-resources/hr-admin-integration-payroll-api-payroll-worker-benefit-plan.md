---
title: Darbuotojo atlyginimo algalapio planas
description: Šiame straipsnyje pateikiama išsami informacija ir atlyginimo darbuotojų išmokų plano objekto pavyzdys Dynamics 365 Human Resources.
author: twheeloc
ms.date: 07/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ef45855d9e60131ac065ae6e2769b71ae3f69537
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902291"
---
# <a name="payroll-worker-benefit-plan"></a>Darbuotojo atlyginimo algalapio planas


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašomas darbuotojo atlyginimo išmokų plano objektas Dynamics 365 Human Resources.

Faktinis pavadinimas: „mshr_payrollworkerbenefitplanentities”.

### <a name="description"></a>Aprašas

Šis objektas pateikia informaciją apie tam kurio darbuotojo išmokų planą.

## <a name="properties"></a>Ypatybės

| Ypatybė</br>**Faktinis pavadinimas**</br>**_Tipas_** | Naudoti | Aprašas |
| --- | --- | --- |
| **Darbuotojo numeris**</br>„mshr_personnelnumber”</br>*Eilutė* | Tik skaitomas</br>Būtina | Unikalus darbuotojo personalo numeris. |
| **Juridinio subjekto ID**</br>„mshr_legalentityID”</br>*Eilutė* | Tik skaitomas | Nurodo juridinį asmenį (įmonę). |
| **Laikotarpio ID**</br>mshr_periodid</br>*Eilutė* | Tik skaitomas | Laikotarpio identifikatorius. |
| **Plano ID**</br>„mshr_planid”</br>*Eilutė* | Tik skaitomas | Plano identifikatorius. |
| **Padengimo parinktis**</br>mshr_coverageoptionid</br>*Eilutė* | Tik skaitomas | Padengimo parinkties identifikavimas. |
| **Atskaitymo pradžios data**</br>mshr_deductionstartdatetime</br>*Datos ir laiko poslinkis* | Tik skaitomas | Atskaitymo pradžios data. |
| **Atskaitymo pabaigos data**</br>mshr_deductionenddatetime</br>*Datos ir laiko poslinkis* | Tik skaitomas | Atskaitymo pabaigos data. |
| **Būsena**</br>mshr_status</br>*[Darbuotojų Išmokų plano būsenos parinkties nustatymas](hr-admin-integration-payroll-api-benefit-employee-plan-status.md)* | Tik skaitomas | Atlyginimo būsenos planas. |
| **Galioja nuo**</br>„mshr_validfrom”</br>*Datos ir Laiko poslinkis* | Tik skaitomas | Laikas, nuo kurio galioja šis įrašas. |
| **Galioja iki**</br>„mshr_validto”</br>*Datos ir Laiko poslinkis* |  Tik skaitomas | Laikas, iki kurio galioja šis įrašas. |
| **Plano tipo ID**</br>mshr_plantypeid</br>*Eilutė* | Tik skaitomas | Plano tipo identifikatorius. |
| **Plano tipo kodas**</br>mshr_plantypecode</br>*[Išmokų plano tipo titulinio parinkties rinkinys](hr-admin-integration-payroll-api-benefit-plan-type-cover.md)* | Tik skaitomas | Plano tipo specifikacijos identifikatorius. |
| **Mokėjimo laikotarpių skaičius**</br>mshr_payperiod</br>*Sveikasis skaičius* | Tik skaitomas | Mokėjimo laikotarpių skaičius, nurodantis, kaip dažnai mokama išmokų teikėjui arba darbuotojams. Ši suma bus naudojama apskaičiuojant darbuotojo metinę išmokų atlyginimo sumą. |
| **Darbuotojo suma**</br>mshr_amountemployee</br>*Dešimtainis* | Tik skaitomas | Darbuotojo atlyginimas ar procentas. |
| **Darbdavio suma**</br>mshr_amountemployer</br>*Dešimtainis* | Tik skaitomas | Darbdavio atlyginimas ar procentas. |
| **Pirminis laukas**</br>mshr_primaryfield</br>*Eilutė* | Sistemos sugeneruota | Pirminis laukas. |
| **Darbuotojo ID vertė** </br>_mshr_fk_worker_id_value</br>*GUID* | Užsienio raktas: mshr_hcmworkerbaseentityid of mshr_hcmworkerbaseentity entity. | Sistemos sukurtas unikalus identifikatorius darbuotojui. |
| **Laikotarpio ID vertė**</br> _mshr_fk_period_id_value</br>*GUID* | Išorinis raktas: mshr_benefitperiodentityid objekto mshr_benefitperiodentity kodas. | Sistemos sukurtas unikalus identifikatorius laikotarpiui. |
| **Plano ID vertė**</br> _mshr_fk_plan_id_value</br>*GUID* | Išorinis raktas: mshr_benefitplanentityid of mshr_benefitplanentity ojektas. | Sistemos sukurtas unikalus identifikatorius planui. |
| **Plano tipo ID vertė**</br> _mshr_fk_plantype_id_value</br>*GUID* | Išorinis raktas: mshr_benefitplantypeentityid of mshr_benefitplantypeentity subjektas. | Sistemos sukurtas unikalus identifikatorius planui. |
| **Padengimo parinkties ID vertė**</br> _mshr_fk_coverageoption_id_value</br>*GUID* | Išorinis raktas: mshr_benefitcoverageoptionentityid of mshr_benefitcoverageoptionentity objektas. | Sistemos sukurtas unikalus identifikatorius planui. |
| **Algalapio darbuotojo išmokų plano objekto ID reikšmė**</br> mshr_payrollworkerbenefitplanentityid</br>*GUID* | Tik skaitomas </br> Sistemos sugeneruota | Sistemos sukurtas unikalus identifikatorius objekto įrašui. |

## <a name="example-query-for-payroll-worker-benefit-plan"></a>Algalapio darbuotojo išmokų plano pavyzdys

**Prašymas**

```http
GET [Organization URI]/api/data/v9.1/mshr_payrollworkerbenefitplanentities?$filter=mshr_personnelnumber eq '000020'
```

**Atsiliepimas**

```json
{
    "mshr_personnelnumber": "000020",
    "mshr_legalentityid": "USMF",
    "mshr_periodid": "2021",
    "mshr_planid": "Dental plan",
    "mshr_coverageoptionid": "Emp Only",
    "mshr_deductionstartdatetime": "2021-01-01T06:00:00Z",
    "mshr_deductionenddatetime": "2021-12-31T06:00:00Z",
    "mshr_status": 200000001,
    "mshr_validfrom": "2021-01-01T06:00:00Z",
    "mshr_validto": "2021-12-31T06:00:00Z",
    "mshr_plantypeid": "Dental",
    "mshr_plantypecode": 200000001,
    "mshr_payperiod": 12,
    "mshr_amountemployee": 47,
    "mshr_amountemployer": 57,
    "mshr_primaryfield": "000020 | USMF | 2021 | Dental plan",
    "_mshr_fk_worker_id_value": "000000ae-0000-0000-bfff-004105000000",
    "_mshr_fk_period_id_value": "00000807-0000-0000-ee02-005001000000",
    "_mshr_fk_plan_id_value": "00000c61-0000-0000-0200-005001000000",
    "_mshr_fk_plantype_id_value": "0000057c-0000-0000-0200-005001000000",
    "_mshr_fk_coverageoption_id_value": "00000391-0000-0000-0b00-005001000000",
    "mshr_payrollworkerbenefitplanentityid": "000006c4-0000-0000-bfff-004105000000"
}
```
## <a name="see-also"></a>Taip pat žiūrėkite

[Algalapių integravimo API įžanga](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
