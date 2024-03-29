---
title: Kompensavimo išmokos dažnumas
description: Šiame straipsnyje pateikiama informacija ir kompensavimo mokėjimo dažnumo objekto pavyzdys Dynamics 365 Human Resources.
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
ms.openlocfilehash: 9afe27776797b2355a32226bbd7fa514b5c5d962
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894620"
---
# <a name="compensation-pay-frequency"></a>Kompensavimo išmokos dažnumas


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašomas kompensavimo mokėjimo dažnio objektas Dynamics 365 Human Resources.

Fizinis pavadinimas: mshr_hcmpayrateconversionentity.

### <a name="description"></a>Aprašymas

Šis objektas pateikia informaciją apie atlygio konvertavimą pagal tam tikrą atlyginimo užmokesčio dažnumą.

## <a name="properties"></a>Ypatybės

| Ypatybė</br>**Faktinis pavadinimas**</br>**_Tipas_** | Naudoti | Aprašymas |
| --- | --- | --- |
| **Metinio užmokesčio tarifo konvertavimas**</br>mshr_annualconversionfactor</br>*Dešimtainis* | Tik skaitomas | Metinis mokėjimo dažnumo konvertavimo koeficientas. |
| **Aprašas**</br>mshr_description</br>*Eilutė* | Tik skaitomas | Konvertavimo santykio aprašas. |
| **Valandinio užmokesčio tarifo konvertavimas**</br>mshr_hourlyconversionfactor</br>*Dešimtainis* | Tik skaitomas | Valandinis mokėjimo dažnumo konvertavimo koeficientas. |
| **Mėnesinis užmokesčio tarifo konvertavimas**</br>mshr_monthlyconversionfactor</br>*Dešimtainis* | Tik skaitomas | Mėnesinis mokėjimo dažnumo konvertavimo koeficientas. |
| **Užmokesčio tarifo konvertavimas**</br>mshr_payrateconversion</br>*Eilutė* | Tik skaitomas | Unikali eilutė konvertavimo koeficientui identifikuoti. |
| **Laikotarpis**</br>mshr_period</br>*laikotarpio parinkčių rinkinys* | Tik skaitomas | Pagrindinis d to užmokesčio tarifo konvertavimo laikotarpis. |
| **Savaitinio užmokesčio tarifo konvertavimas**</br>mshr_weeklyconversionfactor</br>*Dešimtainis* | Tik skaitomas | Savaitinis mokėjimo dažnumo konvertavimo koeficientas. |
| **Srities Duomenys ID**</br>mshr_dataareaid</br>*Eilutė* | Tik skaitomas | Nurodo juridinį asmenį (įmonę). |
| **Kompensavimo išmokos dažnumo objekto ID**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Sistemos sugeneruota | Sistemos sugeneruota visuotinai unikali identifikatoriaus (GUID) vertė, norint unikaliai identifikuoti įrašą. |

## <a name="example-query-for-payroll-employee"></a>Algalapio darbuotojo užklausos pavyzdys

**Prašymas**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hcmpayrateconversionentities?$filter=mshr_payrateconversion eq 'Annual' and mshr_dataareaid eq 'usmf'
```

**Atsiliepimas**

```json
{
    "mshr_annualconversionfactor": 1,
    "mshr_description": "Annual",
    "mshr_hourlyconversionfactor": 0.0004807692,
    "mshr_monthlyconversionfactor": 0.0833333333,
    "mshr_payrateconversion": "Annual",
    "mshr_period": 200000000,
    "mshr_weeklyconversionfactor": 0.0192307692,
    "mshr_dataareaid": "usmf",
    "mshr_hcmpayrateconversionentityid": "0000056e-0000-0000-b027-fef003000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Taip pat žiūrėkite

[Algalapių integravimo API įžanga](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
