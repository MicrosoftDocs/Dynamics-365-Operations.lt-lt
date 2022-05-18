---
title: „Dataverse“ lentelės
description: „Microsoft Dynamics 365 Human Resources“ naudoja „Dataverse“, kad įgalintų išplečiamumo ir integravimo scenarijus.
author: twheeloc
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 702a4063e45dfc64f1edb4351f9bf80491338502
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692260"
---
# <a name="dataverse-tables"></a>„Dataverse“ lentelės


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

„Microsoft Dynamics 365 Human Resources“ naudoja „Dataverse“, kad įgalintų išplečiamumo ir integravimo scenarijus.

> [!NOTE]
> „Human Resources“ objektai atitinka „Dataverse“ lenteles. Dėl daugiau informacijos apie „Dataverse“ (anksčiau vadintą „Common Data Service“) ir terminologijos naujinimus, žr. [Kas yra „Microsoft Dataverse“?](/powerapps/maker/data-platform/data-platform-intro)

Tolesnės „Dataverse“ lentelės yra prieinamos pagal „Human Resources“ objektus.

## <a name="benefit-tables"></a>Išmokų lentelės

| Pavadinimas / vardas ir (arba) pavardė | Lentelė |
| --- | --- |
| Išmokos apskaičiavimo dažnumas | cdm_benefitcalculationfrequency |
| Išmokų skaičiavimo dažnumo mokėjimo laikotarpis | cdm_benefitcalculationfrequencypayperiod |
| Išmokų apskaičiavimo tarifas | cdm_benefitcalculationrate |
| Išmokų apskaičiavimo tarifų informacija | cdm_benefitcalculationratedetail |
| Išmokų parinktis | cdm_benefitoption |
| Išmokų planas | cdm_benefitplan (neįgalintas pasirinktinių laukų palaikymo atveju) |
| Išmokos tipas | cdm_benefittype |

## <a name="business-process-tasks-tables"></a>Verslo proceso užduočių lentelės

| Pavadinimas / vardas ir (arba) pavardė | Lentelė |
| --- | --- |
| Verslo proceso kalendorius | cdm_businessprocesscalendar |
| Verslo proceso grupės priskyrimas | cdm_businessprocessgroupassignment |
| Verslo proceso bibliotekos užduočių grupė | cdm_businessprocesslibrarytaskgroup |
| Verslo proceso etapas | cdm_businessprocessstage |
| Kontrolinio sąrašo šablono antraštė | cdm_businessprocesstemplateheader |
| Kontrolinio sąrašo užduotis | cdm_businessprocesstemplatetask |

## <a name="compensation-tables"></a>Užmokesčio lentelės

| Pavadinimas / vardas ir (arba) pavardė | Lentelė |
| --- | --- |
| Pastoviosios atlyginimo dalies planas | cdm_compensationfixedplan |
| Kompensavimo tinklelis | cdm_compensationgrid |
| Kompensacijos lygis | cdm_compensationlevel |
| Kompensavimo išmokų dažnumas | cdm_compensationpayfrequency |
| Kompensavimo atskaitos taškų nustatymas | cdm_compensationreferencepointsetup |
| Kompensavimo atskaitos taškų nustatymo eilutė | cdm_compensationreferencepointsetupline |
| Kompensacijos sritis | cdm_compensationregion |
| Kompensavimo struktūra | cdm_compensationstructure |
| Kompensacijų kitimo planas | cdm_compensationvariableplan |
| Kompensacijų kitimo plano lygis | cdm_compensationvariableplanlevel |
| Kompensacijų kitimo plano tipas | cdm_compensationvariableplantype |
| Pastoviosios atlyginimo dalies įvykis | cdm_fixedcompensationevent |
| Kintamosios atlyginimo dalies paskirstymo taisyklė | cdm_vestingrule |
| Darbuotojo pastovioji atlyginimo dalis | cdm_workerfixedcompensation |

## <a name="organization-tables"></a>Organizacijos lentelės

| Pavadinimas / vardas ir (arba) pavardė | Lentelė |
| --- | --- |
| Padalinys | cdm_department |
| Įdarbinimas | cdm_employment |
| Įmonė | cdm_company |
| Pareigos | cdm_job |
| Darbo funkcija | cdm_jobfunction |
| Pareigos | cdm_jobposition |
| Pareigų tipas | cdm_positiontype |
| Darbininko paskyrimas į pareigas | cdm_positionworkerassignmentmap |
| Pareigų dimensija | cdm_jobpositiondimension|
| Darbo tipas | cdm_jobtype |
| Kalba | cdm_language |
| Kreipinys | cdm_title |

> [!NOTE]
> **Pareigų tipas**, **Darbuotojo pareigoms priskyrimas** ir **Įdarbinimas** finansinės dimensijos suteikia vienos krypties integraciją su „Dataverse“. Finansinių dimensijų naujinimai dabar negali būti sinchronizuojami iš „Dataverse“ į „Human Resources“. 

## <a name="leave-and-absence-tables"></a>Atostogų ir nebuvimo lentelės

| Pavadinimas / vardas ir (arba) pavardė | Lentelė |
| --- | --- |
| Atostogų banko operacija | cdm_leavebanktransaction |
| Atostogų registracija | cdm_leaveenrollment |
| Atostogų planas | cdm_leaveplan |
| Atostogų prašymas | cdm_leaverequest |
| Atostogų užklausos informacija | cdm_leaverequestdetail |
| Atostogų tipas | cdm_leavetype |
| Atostogų tipo priežasties kodas | cdm_leavetypereasoncode |

## <a name="payroll-tables"></a>Algalapio lentelės

| Pavadinimas / vardas ir (arba) pavardė | Lentelė |
| --- | --- |
| Mokėjimo ciklas | cdm_paycycle |
| Mokėjimo laikotarpis | cdm_payperiod |
| Algalapio pajamų kodas | cdm_payrollearningcode |
| Banko sąskaitos išmoka | cdm_bankaccountdisbursement |
| Mokesčių regionas | cdm_taxregion |

## <a name="worker-tables"></a>Darbuotojo lentelės

| Pavadinimas / vardas ir (arba) pavardė | Lentelė |
| --- | --- |
| Darbuotojas | cdm_worker |
| Darbininko adresas | cdm_workeraddress |
| Darbininko asmeninė informacija | cdm_workerpersonaldetail |
| Darbininko asmens tapatybės numeris | cdm_workerpersonidentificationnumber |
| Darbininko asmens tapatybės tipas | cdm_workerpersonidentificationtype |
| Darbo kalendorius | cdm_workcalendar |
| Darbo kalendoriaus diena | cdm_workcalendarday |
| Darbo kalendoriaus šventė |cdm_workcalendarholiday |
| Darbo kalendoriaus šventės eilutė | cdm_workcalendarholidayline |
| Darbo kalendoriaus laiko intervalas | cdm_workcalendartimeinterval (neįgalintas pasirinktinių laukų palaikymo atveju) |
| Darbininko banko sąskaita | cdm_workerbankaccount |

## <a name="worker-setup-tables"></a>Darbuotojo nustatymo lentelės

| Pavadinimas / vardas ir (arba) pavardė | Lentelė |
| --- | --- |
| Seniai dirbančiojo būsena | cdm_veteranstatus |
| Etninė kilmė | cdm_ethnicorigin |
| Priežasties kodas | cdm_reasoncode |
| Asmens identifikavimo pažymėjimus išduodanti įstaiga | cdm_personidentificationissuingagency |

## <a name="competency-tables"></a>Kompetencijos lentelės

| Pavadinimas / vardas ir (arba) pavardė | Lentelė |
| --- | --- |
| Įgūdžių tipas | cdm_skilltype |

## <a name="table-relationship-models"></a>Lentelės ryšių modeliai

### <a name="worker"></a>Darbuotojas

![Darbininkas.](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Užduotis ir pareigos

![Užduotis ir pareigos.](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Nauda

![Nauda.](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompensacija

![Kompensacija.](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Atostogos

![Atostogos.](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Darbo kalendorius

![Darbo kalendorius.](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>Taip pat žiūrėkite

[Duomenų integravimo technologijos pasirinkimas](hr-admin-integration-choose-technology.md)<br>
[„Dataverse“ integravimo konfigūravimas](hr-admin-integration-common-data-service.md)<br>
[Konfigūruokite „Dataverse“ virtualias lenteles](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[„Human Resources“ virtualių lentelių DUK](hr-admin-virtual-entity-faq.md)<br>
[Kas yra „Microsoft Dataverse“?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Terminologijos naujinimai](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
