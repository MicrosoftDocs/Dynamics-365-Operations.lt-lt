---
title: „Common Data Service“ objektai
description: „Microsoft Dynamics 365 Human Resources“ naudoja „Common Data Service“, kad įgalintų išplečiamumo ir integravimo scenarijus.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 988fa0b6d39a49b973626a8a0abe83c546f42297
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530011"
---
# <a name="common-data-service-entities"></a>„Common Data Service“ objektai

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

„Microsoft Dynamics 365 Human Resources“ naudoja „Common Data Service“, kad įgalintų išplečiamumo ir integravimo scenarijus.

Daugiau informacijos apie „Common Data Service“ rasite dalyje [Kas yra „Common Data Service“](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Šie „Human Resources“ objektai pasiekiami „Common Data Service“.

## <a name="benefit-entities"></a>Išmokų objektai

| Vardas ir pavardė | Objektas |
| --- | --- |
| Išmokos apskaičiavimo dažnumas | cdm_benefitcalculationfrequency |
| Išmokų skaičiavimo dažnumo mokėjimo laikotarpis | cdm_benefitcalculationfrequencypayperiod |
| Išmokų apskaičiavimo tarifas | cdm_benefitcalculationrate |
| Išmokų apskaičiavimo tarifų informacija | cdm_benefitcalculationratedetail |
| Išmokų parinktis | cdm_benefitoption |
| Išmokų planas | cdm_benefitplan (neįgalintas pasirinktinių laukų palaikymo atveju) |
| Išmokos tipas | cdm_benefittype |

## <a name="business-process-tasks-entities"></a>Verslo procesų užduočių objektai

| Vardas ir pavardė | Objektas |
| --- | --- |
| Verslo proceso kalendorius | cdm_businessprocesscalendar |
| Verslo proceso grupės priskyrimas | cdm_businessprocessgroupassignment |
| Verslo proceso bibliotekos užduočių grupė | cdm_businessprocesslibrarytaskgroup |
| Verslo proceso etapas | cdm_businessprocessstage |
| Kontrolinio sąrašo šablono antraštė | cdm_businessprocesstemplateheader |
| Kontrolinio sąrašo užduotis | cdm_businessprocesstemplatetask |

## <a name="compensation-entities"></a>Kompensavimo objektai

| Vardas ir pavardė | Objektas |
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
| Darbininko pastovioji atlyginimo dalis | cdm_workerfixedcompensation |

## <a name="organization-entities"></a>Organizacijos objektai

| Vardas ir pavardė | Objektas |
| --- | --- |
| Skyrius | cdm_department |
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
> **Pareigų tipas**, **Darbuotojo pareigoms priskyrimas** ir **Įdarbinimas** finansinės dimensijos suteikia vienos krypties integraciją su „Common Data Service“. Finansinių dimensijų naujinimai dabar negali būti sinchronizuojami iš „Common Data Service“ į „Human Resources“. 

## <a name="leave-and-absence-entities"></a>Atostogų ir neatvykimų objektai

| Vardas ir (arba) pavardė | Objektas |
| --- | --- |
| Atostogų banko operacija | cdm_leavebanktransaction |
| Atostogų registracija | cdm_leaveenrollment |
| Atostogų planas | cdm_leaveplan |
| Atostogų prašymas | cdm_leaverequest |
| Atostogų užklausos informacija | cdm_leaverequestdetail |
| Atostogų tipas | cdm_leavetype |
| Atostogų tipo priežasties kodas | cdm_leavetypereasoncode |

## <a name="payroll-entities"></a>Algalapio objektai

| Vardas ir pavardė | Objektas |
| --- | --- |
| Mokėjimo ciklas | cdm_paycycle |
| Mokėjimo laikotarpis | cdm_payperiod |
| Algalapio pajamų kodas | cdm_payrollearningcode |
| Banko sąskaitos išmoka | cdm_bankaccountdisbursement |
| Mokesčių regionas | cdm_taxregion |

## <a name="worker-entities"></a>Darbininko subjektai

| Vardas ir pavardė | Objektas |
| --- | --- |
| Darbininkas | cdm_worker |
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

## <a name="worker-setup-entities"></a>Darbininkų sąrankos objektai

| Vardas ir pavardė | Objektas |
| --- | --- |
| Seniai dirbančiojo būsena | cdm_veteranstatus |
| Etninė kilmė | cdm_ethnicorigin |
| Priežasties kodas | cdm_reasoncode |
| Asmens identifikavimą išduodanti agentūra | cdm_personidentificationissuingagency |

## <a name="competency-entities"></a>Kompetencijos objektai

| Vardas ir pavardė | Objektas |
| --- | --- |
| Įgūdžių tipas | cdm_skilltype |

## <a name="entity-relationship-models"></a>Objekto ryšių modeliai

### <a name="worker"></a>Darbininkas

![Darbininkas](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Užduotis ir pareigos

![Užduotis ir pareigos](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Išmokos

![Išmokos](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompensacija

![Kompensacija](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Išeiti

![Išeiti](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Darbo kalendorius

![Darbo kalendorius](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>Taip pat žiūrėkite

[Duomenų integravimo technologijos pasirinkimas](hr-admin-integration-choose-technology.md)</br>
[„Common Data Service“ integravimo konfigūravimas](hr-admin-integration-common-data-service.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]