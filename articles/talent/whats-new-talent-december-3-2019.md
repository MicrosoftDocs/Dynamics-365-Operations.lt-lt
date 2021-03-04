---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2019 m. gruodžio 3 d.)
description: Šiame straipsnyje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 12/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-12-03
ms.dyn365.ops.version: Talent
ms.openlocfilehash: bf1ad4ca2e0ab18aaa35a7410d80a54e7a2160ce
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528698"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-3-2019"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2019 m. gruodžio 3 d.)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šiame straipsnyje aprašomos naujos ir pakeistos „Dynamics 365 Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Attract“.

## <a name="changes-in-onboard"></a>Supažindinimo pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Onboard“.

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai

Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2646 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo palaikymo numerius „Microsoft Dynamics Lifecycle Services“ (LCS).

### <a name="feature-management-workspace"></a>Funkcijos valdymo darbo sritis

Darbo srityje **Funkcijų valdymas** pateikiamas priemonių, pristatytų kiekviename leidime, sąrašas. Pagal numatytuosius nustatymus naujos funkcijos yra išjungtos. Galite naudoti darbo sritį, norėdami jas įjungti ir peržiūrėti jų dokumentaciją. Daugiau informacijos apie funkcijų valdymą žr. [Funkcijos valdymo apžvalga](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Visos naujos funkcijos išlieka peržiūroje bent 30 dienų ir paprastai 30–60 dienų. Pagrindinės funkcijos paprastai pasiekiamos kiekvienų metų spalį ir balandį po peržiūros laikotarpio. Kai tik pradedame naujas galimybes darbo srityje **Funkcijų valdymas**, galite jas įjungti. Kai kurios funkcijos gali būti pagal numatytuosius parametrus.
 
Kartais integrali funkcija bus įjungta pagal numatytuosius nustatymus ir jos nebus galima išjungti (pavyzdžiui, darbo sritis **Funkcijų valdymas**).
 
Kai funkcija jau pasiekiama, ją galima įjungti arba išjungti gamybos aplinkose. Darbo sritis **Funkcijų valdymas** nurodo, kada peržiūros funkcija taps privaloma. Paprastai ši data yra spalio 1 d. arba balandžio 1 d., siekiant suderinti su pusmečio leidimų planais. Negalite išjungti privalomų funkcijų. Kol ji taps privaloma, šią funkciją galite įjungti ir išjungti visose aplinkose.

### <a name="add-automatic-scheduling-of-batch-job-history-cleanup-332528"></a>Įtraukti automatinį paketinės užduoties retrospektyvos valymo planavimą (332528)

Atlikus šį pakeitimą, **Paketinės užduoties retrospektyva** veikia kiekvieną naktį ir pašalina paketinės užduoties retrospektyvos elementus, senesnius nei 30 dienų.

### <a name="talent-doesnt-respond-in-worker-actions-when-identification-number-length-doesnt-match-the-identification-type-390971"></a>„Talent“ nereaguoja atliekant darbininko veiksmus, kai identifikavimo numerio ilgis nesutampa su identifikavimo tipu (390971)

Šiame leidime ištaisoma problema, iškylanti, kai identifikavimo numerio ilgis neatitinka identifikavimo tipo apibrėžimo. 

### <a name="fixed-compensation-doesnt-update-level-with-changes-to-position-details--348085"></a>Pastoviosios atlyginimo dalies lygyje nepateikiami pareigų informacijos pakeitimai (348085)

Šios savaitės leidime parinktyje **Kompensacijos pradžios data** nustatoma užduotis, susieta su pareigomis tuo metu, kai sukuriamas naujas darbuotojo pastoviosios atlyginimo dalies įrašas.

### <a name="workers-employees-and-contractors-lists-show-worker-type-as-both-when-they-should-only-be-worker-or-contractor-384473"></a>Darbininkų, darbuotojų ir rangovų sąrašuose rodomas darbininko tipas Abu, kai turėtų būti tik Darbuotojas arba Rangovas (384473)

Atlikus šį pakeitimą, tiksliai atspindimas įvesto darbininko tipas (rangovas arba darbuotojas).

### <a name="email-notifications-for-new-hire-actions-dont-contain-name-information-due-to-security-policies-383402"></a>Naujų samdos veiksmų el. pašto pranešimuose nėra vardų, pavardžių informacijos dėl saugos strategijų (383402)

Šiuo pakeitimu pataisoma informacija, rodoma vardo arba pavardės laukuose vietos rezervavimo ženkluose darbo eigoje, kai įgalinta išplėstinė sauga.

### <a name="system-allows-two-full-day-leave-requests-for-the-same-day-379284"></a>Sistema leidžia pateikti dvi visos dienos atostogų užklausas tą pačią dieną (379284)

Atlikus šį pakeitimą, negalima pateikti dviejų tos pačios dienos atostogų užklausų. 

### <a name="address-changes-list-should-be-sorted-by-effective-date-352798"></a>Adresų pakeitimų sąrašas turi būti rūšiuojamas pagal įsigaliojimo datą (352798)

Atlikus šį pakeitimą, adresų keitimo sąrašas dabar rūšiuojamas pagal **Įsigaliojimo data**.

### <a name="leave-requests-should-allow-deletes-from-common-data-service-to-talent-376999"></a>Turi būti leidžiama naikinti atostogų užklausas iš „Common Data Service“ ir „Talent“ (376999)

Atlikus šį pakeitimą, juodraštines ir atšauktas atostogų užklausas galima naikinti iš „Common Data Service“ ir paskui iš „Talent“.

### <a name="delete-earning-codes-is-allowed-when-the-same-earning-code-is-assigned-to-an-employee-371792"></a>Leidžiama naikinti pajamų kodus, kai darbuotojui priskirtas tas pats pajamų kodas (371792)

Šiame leidime, prieš panaikindami pajamų kodą sistemoje, pirmiausia turite panaikinti darbuotojo pajamų kodą.

### <a name="leave-and-absence-workflow-with-two-approval-stages-fails-to-complete--391116"></a>Nepavyksta atlikti dviejų etapų atostogų ir nebuvimo darbe darbo eigos (391116)

Atlikus šį pakeitimą, atliekami visi atostogų ir nebuvimo darbe darbo eigos veiksmai, kai užklausoje sukonfigūruotas daugiau nei vienas patvirtinimo etapas.

### <a name="issue-date-doesnt-sync-to-common-data-service-when-updated-or-entered-in-talent-397361"></a>Išdavimo data nesinchronizuojama su „Common Data Service“, kai ji atnaujinama arba įvedama sprendime „Talent“ (397361)

Šiame pakeitime išsprendžiama problema, kai **Asmens identifikavimas** įrašų išdavimo data nebuvo sinchronizuojama su „Common Data Service“ pagal sprendimą „Talent“.

### <a name="hierarchy-circular-reference-error-issued-when-assigning-a-manager-to-a-position-386659"></a>Hierarchijos ciklinės nuorodos klaida, pateikiama paskiriant vadybininką į pareigas (386659)

Šiame pakeitime pataisomas unikalus atvejis, kai ciklinės nuorodos klaida atsiranda paskiriant naują vadybininką į pareigas.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>„Common Data Service” objektai, kuriuose dabar palaikomi pasirinktiniai laukai

Toliau nurodytuose „Common Data Service“ objektuose dabar palaikomi pasirinktiniai laukai.

| Vardas ir pavardė | Objektas |
| --- | --- |
| Banko sąskaitos išmoka | cdm_bankaccountdisbursement |
| Išmokos apskaičiavimo dažnumas | cdm_benefitcalculationfrequency |
| Išmokų skaičiavimo dažnumo mokėjimo laikotarpis | cdm_benefitcalculationfrequencypayperiod |
| Išmokų apskaičiavimo tarifas | cdm_benefitcalculationrate |
| Išmokų apskaičiavimo tarifų informacija | cdm_benefitcalculationratedetail |
| Išmokų parinktis | cdm_benefitoption |
| Išmokų planas | cdm_benefitplan (neįgalintas pasirinktinių laukų palaikymo atveju) |
| Išmokos tipas | cdm_benefittype |
| Verslo proceso kalendorius | cdm_businessprocesscalendar |
| Verslo proceso grupės priskyrimas | cdm_businessprocessgroupassignment |
| Verslo proceso bibliotekos užduočių grupė | cdm_businessprocesslibrarytaskgroup |
| Verslo proceso etapas | cdm_businessprocessstage |
| Kontrolinio sąrašo šablono antraštė | cdm_businessprocesstemplateheader |
| Kontrolinio sąrašo užduotis | cdm_businessprocesstemplatetask |
| Įmonė | cdm_company |
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
| Skyrius | cdm_department |
| Įdarbinimas | cdm_employment |
| Etninė kilmė | cdm_ethnicorigin |
| Pastoviosios atlyginimo dalies įvykis | cdm_fixedcompensationevent |
| Pareigos | cdm_job |
| Darbo funkcija | cdm_jobfunction |
| Pareigos | cdm_jobposition |
| Darbo tipas | cdm_jobtype |
| Kalba | cdm_language |
| Banko išėjimo operacija | cdm_leavebanktransaction |
| Atostogų registracija | cdm_leaveenrollment |
| Atostogų planas | cdm_leaveplan |
| Atostogų prašymas | cdm_leaverequest |
| Atostogų užklausos informacija | cdm_leaverequestdetail |
| Atostogų tipas | cdm_leavetype |
| Atostogų tipo priežasties kodas | cdm_leavetypereasoncode |
| Mokėjimo ciklas | cdm_paycycle |
| Mokėjimo laikotarpis | cdm_payperiod |
| Algalapio pajamų kodas | cdm_payrollearningcode |
| Asmens identifikavimą išduodanti agentūra | cdm_personidentificationissuingagency |
| Pareigų tipas | cdm_positiontype |
| Darbininko paskyrimas į pareigas | cdm_positionworkerassignmentmap |
| Priežasties kodas | cdm_reasoncode |
| Įgūdžių tipas | cdm_skilltype |
| Mokesčių regionas | cdm_taxregion |
| Kintamosios atlyginimo dalies paskirstymo taisyklė | cdm_vestingrule |
| Seniai dirbančiojo būsena | cdm_veteranstatus |
| Darbo kalendorius | cdm_workcalendar |
| Darbo kalendoriaus diena | cdm_workcalendarday |
| Darbo kalendoriaus šventė |cdm_workcalendarholiday |
| Darbo kalendoriaus šventės eilutė | cdm_workcalendarholidayline |
| Darbo kalendoriaus laiko intervalas | cdm_workcalendartimeinterval (neįgalintas pasirinktinių laukų palaikymo atveju) |
| Darbininkas | cdm_worker |
| Darbininko adresas | cdm_workeraddress |
| Darbininko banko sąskaita | cdm_workerbankaccount |
| Darbininko pastovioji atlyginimo dalis | cdm_workerfixedcompensation |
| Darbininko asmeninė informacija | cdm_workerpersonaldetail |
| Darbininko asmens tapatybės numeris | cdm_workerpersonidentificationnumber |
| Darbininko asmens tapatybės tipas | cdm_workerpersonidentificationtype |

## <a name="in-preview"></a>Peržiūros režimu

Peržiūros funkcijos pasiekiamos tik aplinkose **Smėlio dėžė**.

### <a name="print-performance-reviews"></a>Veiklos efektyvumo vertinimų spausdinimas

Žr. [Veiklos efektyvumo vertinimų spausdinimas](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) dirbant su „Dynamics 365“: 2019 leidimo 2 bangos planu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]