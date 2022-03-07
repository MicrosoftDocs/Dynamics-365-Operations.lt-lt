---
title: Algalapio darbuotojas
description: Šioje temoje pateikiama informacija ir Algalapio darbuotojo objekto užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.
author: jcart
ms.date: 08/25/2021
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
ms.openlocfilehash: 7f43476cd044a9cc2e11412aac4af1cff2f9e511
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559538"
---
# <a name="payroll-employee"></a>Algalapio darbuotojas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas Darbuotojo algalapio objektas „Dynamics 365 Human Resources“.

Faktinis pavadinimas: „mshr_payrollemployeeentity”.

### <a name="description"></a>Aprašas

Šiame objekte pateikta informacija apie darbuotoją. Privalote nustatyti [algalapio integravimo parametrus](hr-admin-integration-payroll-api-parameters.md) prieš naudodami šį objektą.

>[!IMPORTANT] 
>**Vardo**, **Vidurinio vardo**, **Pavardės**, **Vardas galioja nuo** ir **Vardas galioja iki** laukų nebegalima naudoti šiame objekte. Taip užtikrinama, kad yra tik vienas duomenų šaltinis, kuris atims šiam objektui atsarginį duomenų šaltinį.
>Šie laukai bus galimi **Tiesioginio asmens vardo retrospektyviniame objekte** kuris buvo išleistas 43 platformos naujinime. Yra „OData” ryšys yra iš **PayrollEmployeeEntity** į **DirPersonNameHistoricalEntity**. 

## <a name="properties"></a>Ypatybės

| Ypatybė</br>**Faktinis pavadinimas**</br>**_Tipas_** | Naudoti | Aprašas |
| --- | --- | --- |
| **Juridinio subjekto ID**</br>mshr_legalentityid</br>*Eilutė* | Tik skaitomas | Nurodo juridinį asmenį (įmonę). |
| **Darbuotojo numeris**</br>„mshr_personnelnumber”</br>*Eilutė* | Tik skaitomas | Unikalus darbuotojo personalo numeris. |
| **Įdarbinimo pradžios data**</br>„mshr_employmentstartdate”</br>*Datos ir laiko poslinkis* | Tik skaitomas | Darbuotojo įdarbinimo pradžios data. |
| **Įdarbinimo pabaigos data**</br>„mshr_employmentenddate”</br>*Datos ir laiko poslinkis* | Tik skaitomas |Darbuotojo įdarbinimo pabaiga.  |
| **Gimimo data**</br>mshr_birthdate</br>*Datos ir Laiko poslinkis* | Tik skaitomas | Darbuotojo gimimo data. |
| **Giminė**</br>mshr_gender</br>[mshr_hcmpersongender parinkties nustatymas](hr-admin-integration-payroll-api-gender.md) | Tik skaitomas | Darbuotojo lytis. |
| **Įdarbinimo tipas**</br>mshr_employmenttype</br>[mshr_hcmemploymenttype parinkties nustatymas](hr-admin-integration-payroll-api-hcmemploymenttype.md) | Tik skaitomas | Įdarbinimo tipas. |
| **Identifikacijos tipo ID**</br>mshr_identificationtypeid</br>*Eilutė* |Tik skaitomas | Darbuotojui apibrėžtas identifikacijos tipas. |
| **Identifikacijos numeris iki**</br>mshr_identificationnumber</br>*Eilutė* | Tik skaitomas |Darbuotojui apibrėžtas identifikacijos numeris. |
| **Parengta mokėti**</br>mshr_readytopay</br>[mshr_noyes parinkties nustatymas](hr-admin-integration-payroll-api-no-yes.md) | Tik skaitomas | Nurodo, ar darbuotojas pažymėtas kaip parengtas mokėti. |
| **Algalapio darbuotojo objekto ID**</br>„mshr_payrollemployeeentityid”</br>*GUID* | Sistemos sugeneruota | Sistemos sugeneruota visuotinai unikali identifikatoriaus (GUID) vertė, norint unikaliai identifikuoti darbuotoją. |

## <a name="relations"></a>Ryšiai

|Ypatybės vertė | Susijęs objektas | Naršymo ypatybė | Rinkimo tipas |
| --- | --- | --- | --- |
| _mshr_fk_employment_id_value | mshr_hcmemploymentdetailentity | mshr_FK_Employment_id | mshr_FK_HcmEmploymentDetailEntity_PayrollEmployee |
| „_mshr_fk_fixedcompplan_id_value” | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Employee |
| _mshr_fk_name_id_value | mshr_dirpersonnamehistoricalentity | mshr_FK_Name_id | - |
| _mshr_fk_worker_id_value | mshr_hcmworkerbaseentity | mshr_FK_Worker_id | mshr_FK_HcmWorkerBaseEntity_PayrollEmployee |
| _mshr_fk_workerbankaccount_id_value | mshr_hcmworkerbankaccountentity | mshr_FK_WorkerBankAccount_id | mshr_FK_HcmWorkerBankAccountEntity_PayrollEmployee |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_Employee |
| _mshr_fk_address_id_value | [mshr_payrollworkeraddressentity](hr-admin-integration-payroll-api-payroll-worker-address.md) | mshr_FK_Address_id | mshr_FK_PayrollWorkerAddressEntity_Worker |

## <a name="example-query-for-payroll-employee"></a>Algalapio darbuotojo užklausos pavyzdys

**Prašymas**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq '000041'
```

**Atsiliepimas**

```json
{
    "mshr_legalentityid": "USMF",
    "mshr_personnelnumber": "000041",
    "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
    "mshr_employmentenddate": "2154-12-31T23:59:59Z",
    "mshr_birthdate": "1987-09-12T00:00:00Z",
    "mshr_gender": 200000002,
    "mshr_employmenttype": 200000000,
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_readytopay": 200000000,
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_employment_id_value": "00000d4e-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "00000598-0000-0000-4cd0-fda002000000",
    "_mshr_fk_name_id_value": "00000832-0000-0000-d700-014105000000",
    "_mshr_fk_worker_id_value": "000000af-0000-0000-d5ff-004105000000",
    "_mshr_fk_workerbankaccount_id_value": "000006f2-0000-0000-b7ff-004105000000",
    "mshr_payrollemployeeentityid": "00000666-0000-0000-d5ff-004105000000",
    "_mshr_fk_address_id_value": null,
    "_mshr_fk_variablecompaward_id_value": null,
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Taip pat žiūrėkite

[Algalapių integravimo API įžanga](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
