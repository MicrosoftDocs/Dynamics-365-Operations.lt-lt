---
title: Integravimo su „Finance“ konfigūravimas
description: Šiame straipsnyje aprašomas integravimas tarp ir Dynamics 365 Human Resources "Dynamics 365 Finance".
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8be7cbf92c11036d334516116f0895c426380954
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875864"
---
# <a name="configure-integration-with-finance"></a>Integravimo su „Finance“ konfigūravimas


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Norėdami integruotis Dynamics 365 Human Resources su "Dynamics 365 Finance", duomenų integratoriaus finansų šablonu galite naudoti [Personalo valdymo skyrių](/powerapps/administrator/data-integrator). Šablonas „Iš „Human Resources“ į „Finance“ suaktyvina užduočių, pareigų ir darbuotojų duomenų srautą. Šablonas leidžia duomenų srautą iš „Human Resources“ į „Finance“, tačiau neleidžia duomenų srauto iš „Finance“ į „Human Resources“.

![Iš „Human Resources“ į „Finance“ integravimo srautas.](./media/hr-admin-integration-finance-flow.png)

Sprendime „Iš „Human Resources“ į „Finance“ pateikiami tolesni duomenų sinchronizavimo tipai.

- „Human Resources“ darbo vietų tvarkymas ir jų sinchronizavimas iš „Human Resources“ į „Finance“
- „Human Resources“ pareigų ir pareigų priskyrimų tvarkymas ir jų sinchronizavimas iš „Human Resources“ į „Finance“
- Tvarkykite „Human Resources“ įdarbinimus ir sinchronizuokite juos iš „Human Resources“ į „Finance“
- Tvarkykite „Human Resources“ darbininkus bei darbininkų adresus ir sinchronizuokite juos iš „Human Resources“ į „Finance“.

## <a name="system-requirements-for-human-resources"></a>„Human Resources“ sistemos reikalavimai

Integravimo sprendimui reikia tokių „Human Resource“ ir „Finance“ versijų: 

- Dynamics 365 Human Resources Dataverse
- "Dynamics 365" 7.2 ir vėlesnė finansų versija

## <a name="template-and-tasks"></a>Šablonai ir užduotys

Prieiga prie šablono „Iš „Human Resources“ į „Finance“.

1. Atidarykite [„Power Apps“ administravimo centrą](https://admin.powerapps.com/). 

2. Pasirinkite **Projektai** ir viršutiniame dešiniajame kampe pasirinkite **Naujas projektas**. Sukurkite naują kiekvieno juridinio subjekto, kurį norite integruoti į „Finance“, projektą.

3. Pasirinkite **„Human Resources“ („Human Resources Dataverse“ į „Finance“)**, norėdami sinchronizuoti įrašus iš „Human Resources “ į „Finance“.

Šis šablonas naudojamas norint sinchronizuoti tolesnius įrašus iš „Human Resources“ į „Finance“.

- **Užduoties funkcijos į kompensavimo užduoties funkciją**
- **Padaliniai į valdymo vienetą**
- **Užduoties tipai į Kompensavimo užduoties tipą**
- **Darbai į darbus**
- **Užduotys į užduoties išsamią informaciją**
- **Pareigų tipai į pareigų tipą**
- **Darbo pareigos į pagrindines pareigas**
- **Darbo pareigos į pareigų išsamią informaciją**
- **Darbo pareigos į pareigų trukmę**
- **Darbo pareigos į pareigų hierarchijas**
- **Darbininkai į darbininką**
- **Įdarbinimai į įdarbinimą**
- **Įdarbinimai į įdarbinimo išsamią informaciją**
- **Darbininko pareigų priskyrimas į darbininko pareigų priskyrimus**
- **Darbininko adresai adresai į darbininko pašto adresą V2**

## <a name="template-mappings"></a>Šablono susiejimai

Tolesnių šablonų susiejimo lentelėse užduoties pavadinimą sudaro objektai, naudojami kiekviename prašyme. Šaltinis („Human Resources“) yra kairėje pusėje, o paskirties vieta („Finance“) yra dešinėje pusėje.

### <a name="job-functions-to-compensation-job-function"></a>Užduoties funkcijos į kompensavimo užduoties funkciją

| „Dataverse“ lentelė (šaltinis) | „Finance“ objektas (paskirties vieta) |
|-------------------------------------|---------------------------------------------|
| cdm_name (cdm_Job funkcijos pavadinimas)  | JOBFUNCTIONID   (JOBFUNCTIONID)            |
| cdm_description   (cdm_description) | APRAŠAS   (APRAŠAS)                 |

### <a name="departments-to-operating-unit"></a>Padaliniai į valdymo vienetą

| „Dataverse“ lentelė (šaltinis)           | „Finance“ objektas (paskirties vieta) |
|-----------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                           | PAVADINIMAS (PAVADINIMAS)                                 |
| cdm_departmentnumber   (cdm_departmentnumber) | OPERATINGUNITNUMBER   (OPERATINGUNITNUMBER) |
|                                               | OPERATINGUNITTYPE   (OPERATINGUNITTYPE)     |
| cdm_description   (cdm_description)           | NAMEALIAS   (NAMEALIAS)                     |

### <a name="job-types-to-compensation-job-type"></a>Užduoties tipai į Kompensavimo užduoties tipą

| „Dataverse“ lentelė (šaltinis)   | „Finance“ objektas (paskirties vieta) |
|---------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                   | JOBTYPEID   (JOBTYPEID)                     |
| cdm_description   (cdm_description)   | APRAŠAS   (APRAŠAS)                 |
| cdm_exemptstatus   (cdm_exemptstatus) | EXEMPTSTATUS   (EXEMPTSTATUS)               |

### <a name="jobs-to-jobs"></a>Darbai į darbus

| „Dataverse“ lentelė (šaltinis)                           | „Finance“ objektas (paskirties vieta)           |
|---------------------------------------------------------------|-------------------------------------------------------|
| cdm_name (cdm_name)                                           | JOBID (JOBID)                                         |
| cdm_maximumnumberofpositions   (cdm_maximumnumberofpositions) | MAXIMUMNUMBEROFPOSITIONS   (MAXIMUMNUMBEROFPOSITIONS) |
| cdm_allowedunlimitedpositions   (cdm_allowunlimitedpositions) | ALLOWUNLIMITEDPOSITIONS   (ALLOWUNLIMITEDPOSITIONS)   |
| cdm_description   (cdm_description)                           | APRAŠAS   (APRAŠAS)                           |
| cdm_jobdescription   (cdm_jobdescription)                     | JOBDESCRIPTION   (JOBDESCRIPTIONS)                    |

### <a name="jobs-to-job-detail"></a>Užduotys į užduoties išsamią informaciją

| „Dataverse“ lentelė (šaltinis)                             | „Finance“ objektas (paskirties vieta) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                                             | JOBID (JOBID)                               |
| cdm_jobtypeid.cdm_name   (užduoties tipas (užduoties tipo pavadinimas))             | JOBTYPEID   (JOBTYPEID)                     |
| cdm_jobfunctionid.cdm_name   (užduoties funkcija (užduoties funkcijos pavadinimas)) | FUNCTIONID   (FUCNTIONID)                   |
| cdm_validfrom   (galioja nuo)                                    | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (galioja iki)                                        | VALIDTO (VALIDTO)                           |
| cdm_defaultfulltimeequivalent   (numatytasis viso laiko ekvivalentas)   | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)   |

### <a name="position-types-to-position-type"></a>Pareigų tipai į pareigų tipą

| „Dataverse“ lentelė (šaltinis)       | „Finance“ objektas (paskirties vieta) |
|-------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                       | POSITIONTYPEID   (POSITIONTYPEID)           |
| cdm_description   (cdm_description)       | APRAŠAS   (APRAŠAS)                 |
| cdm_classification (cdm_classification) | KLASIFIKACIJA (KLASIFIKACIJA)           |

### <a name="job-positions-to-base-position"></a>Darbo pareigos į pagrindines pareigas

| „Dataverse“ lentelė (šaltinis)           | „Finance“ objektas (paskirties vieta) |
|-----------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber (Pareigų numeris) | POSICIONID (POSICIONID)                      |

### <a name="job-positions-to-position-details"></a>Darbo pareigos į pareigų išsamią informaciją

| „Dataverse“ lentelė (šaltinis)              | „Finance“ objektas (paskirties vieta)       |
|--------------------------------------------------------------------------|---------------------------------------------------|
| cdm_jobpositionnumber (Pareigų numeris)                            | POSICIONID (POSICIONID)                             |
| cdm_jobid.cdm_name   (užduotis (pavadinimas))                                        | JOBID (JOBID)                                    |
| cdm_description   (cdm_description)                                        | APRAŠAS   (APRAŠAS)                       |
| cdm_departmentid.cdm_departmentnumber   (padalinys (padalinio numeris)) | DEPARTMENTNUMBER   (DEPARTMENTNUMBER)             |
| cdm_positiontypeid.cdm_name   (pareigų tipas (pavadinimas))                     | POSITIONTYPEID   (POSITIONTYPEID)                 |
| cdm_avaialableforassignment   (galima priskirti)                 | AVAILABLEFORASSIGNMENT   (AVAILABLEFORASSIGNMENT) |
| cdm_validfrom   (galioja nuo)                                            | VALIDFROM   (VALIDFROM)                           |
| cdm_validto (galioja iki)                                                 | VALIDTO (VALIDTO)                               |
| cdm_fulltimeequivalent   (Viso laiko ekvivalentas)                           | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)         |

### <a name="job-positions-to-position-durations"></a>Darbo pareigos į pareigų trukmę

| „Dataverse“ lentelė (šaltinis)             | „Finance“ objektas (paskirties vieta) |
|-------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (Pareigų numeris)   | POSICIONID (POSICIONID)                      |
| Apskaičiuotas   aktyvinimas (apskaičiuotas aktyvinimas) | VALIDFROM (VALIDFROM)                        |
| Apskaičiuotas   išėjimas į pensiją (apskaičiuotas išėjimas į pensiją) | VALIDTO (VALIDTO)                         |

### <a name="job-positions-to-position-hierarchies"></a>Darbo pareigos į pareigų hierarchijas

| „Dataverse“ lentelė (šaltinis)        | „Finance“ objektas (paskirties vieta) |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (Pareigų numeris)                                                 | POSICIONID(POSICIONID)                      |
| cdm_parentjobpositionid.cdrjobposicionnumber   (cdm_parentjobpositionid.cdmarjobposicionnumber) | PARENTPOSICIONID (PARENTPOSICIONID)         |
| cdm_validfrom   (galioja nuo)                                                                  | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (galioja iki)                                                                      | VALIDTO (VALIDTO)                           |
| HIERARCHYTYPENAME   (HIERARCHYTYPENAME)                                                       | HIERARCHYTYPENAME   (HIERARCHYTYPENAME)     |


### <a name="workers-to-worker"></a>Darbininkai į darbininką
| „Dataverse“ lentelė (šaltinis)           | „Finance“ objektas (paskirties vieta)       |
|-----------------------------------------------|---------------------------------------------------|
| cdm_birthdate   (cdm_birthdate)               | BIRTHDATE   (BIRTHDATE)                           |
| cdm_gender   (cdm_gender)                     | LYTIS (LYTIS)                                   |
| cdm_primaryaddress   (cdm_primaryaddress)     | PRIMARYCONTACTEMAIL   (PRIMARYCONTACTEMAIL)      |
| cdm_primarytelephone   (cdm_primarytelephone) | PRIMARYCONTACTPHONE   (PRIMARYCONTACTPHONE)       |
| cdm_facebookidentity   (cdm_facebookidentity) | PRIMARYCONTACTFACEBOOK   (PRIMARYCONTACTFACEBOOK) |
| cdm_twitteridentity   (cdm_twitteridentity)   | PRIMARYCONTACTTWITTER   (PRIMARYCONTACTTWITTER)   |
| cdm_linkedinIdentity   (cdm_linkedinIdentity) | PRIMARYCONTACTLINKEDIN   (PRIMARYCONTACTLINKEDIN) |
| cdm_websiteurl   (cdm_websiteurl)             | PRIMARYCONTACTURL   (PRIMARYCONTACTURL)           |
| cdm_firstname   (cdm_firstname)               | FIRSTNAME   (FIRSTNAME)                           |
| cdm_middlename   (cdm_middlename)             | MIDDLENAME   (MIDDLENAME)                         |
| cdm_lastname   (cdm_lastname)                 | LASTNAME (LASTNAME)                               |
| cdm_workernumber   (cdm_workernumber)         | PERSONNELNUMBER   (PERSONNELNUMBER)               |
| cdm_type (cdm_type)                           | WORKERTYPE   (WORKERTYPE)                         |
| cdm_state   (cdm_state)                       | WORKSTATUS   (WORKERSTATUS)                       |

### <a name="employments-to-employment"></a>Įdarbinimai į įdarbinimą

| „Dataverse“ lentelė (šaltinis)                             | „Finance“ objektas (paskirties vieta) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE) |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)     |
| cdm_workertype   (cdm_workertype)                               | WORKERTYPE   (WORKERTYPE)                   |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)         |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)             |

### <a name="employments-to-employment-detail"></a>Įdarbinimai į įdarbinimo išsamią informaciją

| „Dataverse“ lentelė (šaltinis)                             | „Finance“ objektas (paskirties vieta)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE)   |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)       |
| cdm_validfrom   (galioja nuo)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (galioja   iki)                                        | VALIDTO (VALIDTO)                             |
| cdm_workerstartdate   (cdm_workerstartdate)                     | WORKERSTARTDATE   (WORKERSTARTDATE)           |
| cdm_lastdateworked   (cdm_lastdateworked)                       | LASTDATEWORKED   (LASTDATEWORKED)             |
| cdm_transitiondate   (cdm_transitiondate)                       | TRANSITIONDATE   (TRANSITIONDATE)             |
| cdm_employerunitofnotice   (cdm_employerunitofnotice)           | EMPLOYERUNITOFNOTICE   (EMPLOYERUNITOFNOTICE) |
| cdm_workerunitofnotice   (cdm_workerunitofnotice)               | WORKERUNITOFNOTICE   (WORKERUNITOFNOTICE)     |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)               |
| cdm_employernoticeamount   (cdm_employernoticeamount)           | EMPLOYERNOTICEAMOUNT   (EMPLOYERNOTICEAMOUNT) |
| cdm_workernoticeamount   (cdm_workernoticeamount )              | WORKERNOTICEAMOUNT   (WORKERNOTICEAMOUNT)     |

### <a name="position-worker-assignment-to-position-worker-assignments"></a>Darbininko pareigų priskyrimas į darbininko pareigų priskyrimus

| „Dataverse“ lentelė (šaltinis)                             | „Finance“ objektas (paskirties vieta)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_jobpositionnumber   (Pareigų numeris)                   | POSICIONID(POSICIONID)                        |
| cdm_validfrom   (galioja nuo)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (galioja iki)                                        | VALIDTO (VALIDTO)                             |

### <a name="worker-addresses-to-worker-postal-address-v2"></a>Darbininko adresai adresai į darbininko pašto adresą V2

| „Dataverse“ lentelė (šaltinis)                             | „Finance“ objektas (paskirties vieta)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSLOCATIONROLES   (ADDRESSLOCATIONROLES) |
| cdm_line1   (cdm_line1)                                         | ADDRESSSTREET   (ADDRESSSTREET)               |
| cdm_city (cdm_city)                                             | ADDRESSCITY   (ADDRESSCITY)                   |
| cdm_stateorprovince   (cdm_stateorprovince)                     | ADDRESSSTATE   (ADDRESSSTATE)                 |
| cdm_postalcode   (cdm_postalcode)                               | ADDRESSZIPCODE(ADDRESSZIPCODE)                |
| cdm_countryregion   (cdm_countryregion)                         | ADDRESSCOUNTRYREGION(ADDRESSCOUNTRYREGION)    |
| cdm_addressnumber   (cdm_addressnumber)                         | ADDRESSLOCATIONID(ADDRESSLOCATIONID)          |
| cdm_ispreferred   (cdm_ispreferred)                             | ISPRIMARY   (ISPRIMARY)                       |
| cdm_county   (cdm_county)                                       | ADDRESSCOUNTYID(ADDRESSCOUNTYID)              |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSDESCRIPTION(ADDRESSDESCRIPTION)        |

## <a name="integration-considerations"></a>Integravimo aplinkybės

Integruojant duomenis iš „Human Resources“ į „Finance“, integravimu bus bandoma sugretinti įrašus pagal ID. Jei įrašai sutampa, duomenų integravimo priemonė perrašo duomenis „Finance“ reikšmėmis iš „Human Resources“. Tačiau problema gali kilti, jei logiškai tai yra skirtingi įrašai ir tas pats ID buvo sugeneruotas naudojant „Human Resources“ arba „Finance“ pagal atitinkamą numeraciją.

Problema gali įvykti su **Darbininkas**, kuriam naudojamas **Personalo numeris** siekiant gretinti, ir **Pareigos**. Užduotims nenaudojamos numeracijos. Todėl, jei tas pats užduoties ID yra ir Personalo, ir finansų, Personalo informacija perrašo "Dynamics 365" finansų informaciją. 

Norėdami išvengti pasikartojančių ID problemų, galite pridėti priešvardį [numeracijoje](/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json) arba numeracijoje nustatyti pradžios numerį, kuris nepatenka į kitos sistemos numeracijos intervalą. 

Vietos ID, naudojamas darbuotojo adresui, nėra numeracijos dalis. Integruojant darbuotojo adresą iš „Human Resources“ į „Finance“, jei darbuotojo adresas jau yra „Finance“, gali būti sukurtas pasikartojantis adreso įrašas. 

Toliau pateiktoje iliustracijoje vaizduojamas šablono susiejimo pavyzdys duomenų integratoriuje. 

![Šablono Susiejimas.](./media/IntegrationMapping.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
