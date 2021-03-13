---
title: Samdytinas pretendentas
description: Šioje temoje aprašomas samdytino pretendento objektas „Dynamics 365 Human Resources“.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eb16f9f46e3f5c58854ec06c3b89ec72dd7bae00
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125742"
---
# <a name="candidate-to-hire"></a>Samdytinas pretendentas

Šioje temoje aprašomas samdytino pretendento objektas „Dynamics 365 Human Resources“.

Fizinis pavadinimas: mshr_hcmcandidatetohireentity

## <a name="description"></a>aprašymas

Šis objektas pateikia išsamią kandidato informaciją, naudojamą siekiant sukurti darbuotoją „Dynamics 365 Human Resources“. Jis naudojamas perskaityti visus kandidato įrašus ir sukurti vidaus ir išorės kandidato įrašus, leidžiant jums sukurti asmeninę informaciją naujam pretendentui.

Kai kuriate išorės pretendento įrašą, kuris bus naujas asmens įrašas sistemoje, turite nenustatyti šalies (asmens) skaičiaus, kuriame publikuojate naujo pretendento įrašą. Naujo asmens objekto įrašas sukuriamas su naujo pretendento įrašu.

Jums sukūrus vidaus pretendento įrašą (kandidatas pareigoms, kuriame jau yra darbuotojo įrašas įmonėje), nustatykite šalies (asmens) numerį įrašui, kuris jau yra asmeniui mshr_partynumber ypatybės pretendento įraše, o ne nustatykite asmeninę informaciją (tokią kaip vardas, lytis ar gimimo data), kuris bus naudojamas siekiant sukurti naują asmens įrašą.

## <a name="json-representation"></a>JSON atstovavimas

```json
        {
            "mshr_candidateid": "String",
            "mshr_partynumber": "String",
            "mshr_partytype": "String",
            "mshr_recruitingrequestid": "String",
            "mshr_positionid": "String",
            "mshr_firstname": "String",
            "mshr_middlename": "String",
            "mshr_lastnameprefix": "String",
            "mshr_lastname": "String",
            "mshr_gender": Int,
            "mshr_birthdate": "Date",
            "mshr_citizenshipcountrycode": "String",
            "mshr_veteranstatusid": "String",
            "mshr_isdisabledveteran": Int,
            "mshr_availabilitydate": "Date",
            "mshr_iswillingtorelocate": Int,
            "mshr_comments": "String",
            "mshr_applicantintegrationresult": Int,
            "mshr_donothirereasoncodeid": "String",
            "mshr_dataareaid": "String",
            "_mshr_dataareaid_id_value": "Guid",
            "_mshr_fk_person_id_value": "Guid",
            "_mshr_fk_recruitingrequest_id_value": "Guid",
            "_mshr_fk_position_id_value": "Guid",
            "mshr_hcmcandidatetohireentityid": "Guid",
            "_mshr_fk_veteranstatus_id_value": "Guid",
            "_mshr_fk_reasoncode_id_value": "Guid",
            "mshr_militaryserviceenddate": "Guid",
            "mshr_militaryservicestartdate": "Guid"
        }
```

## <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | aprašymas |
| --- | --- | --- |
| **Samdytino pretendento objekto ID**<br>mshr_hcmcandidatetohireentityid<br>Guid | Tik skaitomas<br>Būtina<br>Sukurta sistemos | Sistemos sukurtas unikalus identifikatorius objekto įrašui. |
| **Pretendento ID**<br>mshr_candidateid<br>Eilutė | Tik skaitomas<br>Būtina<br>Sukurta sistemos | Unikalus identifikatorius objektui. |
| **Šalies numeris**<br>mshr_partynumber<br>Eilutė | Tik skaitomas<br>Būtina | Šalies (asmens) asmeninio įrašo pretendento numeris. |
| **Asmens ID vertė**<br>_mshr_fk_person_id_value<br>Guid | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_dirpersonentityid of mshr_direpersonentity | Sistemos sukurtas unikalus identifikatorius šalies (asmens) pretendento įrašui. |
| **Šalies tipas**<br>mshr_partytype<br>mshr_dirpartytype parinkties nustatymas | Tik skaitomas<br>Būtina | Šalies įrašo tipas, kaip nustatyta mshr_dirpartytype parinkties rinkinyje. Šiam objektui, tipas visada bus „Asmuo“. |
| **Įdarbinimo užklausos ID**<br>mshr_recruitingrequestid<br>Eilutė | Rašyti kartą<br>Pasirinktinai | Samdymo užklausos nuorodos, kurias šis pretendentas atitinka. |
| **Įdarbinimo užklausos ID vertė**<br>_mshr_fk_recruitingrequest_id_value<br>Guid | Skaitymas/rašymas<br>Pasirinktinai<br>Užsienio raktas: mshr_hcmrecruitingrequestentityid mshr_hcmrecruitingrequestentity | Sistemos sukurtas unikalus identifikatorius samdymo užklausos, kurią kandidatas atliko. |
| **Pareigų ID**<br>mshr_positionid<br>Eilutė | Skaitymas/rašymas<br>Pasirinktinai | Pareigų ID, kurioms pretendentas yra svarstomas. |
| **Pareigų ID vertė**<br>_mshr_fk_position_if_value<br>Guid | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: mshr_hcmpositionv2entityid mshr_hcmpositionv2entity | Sistemos sukurtas pareigų identifikatorius su pretendentu, kurioms jis svarstomas. |
| **Vardas**<br>mshr_firstname<br>Eilutė | Skaitymas/rašymas<br>Būtina | Pretendento vardas. |
| **Antras vardas**<br>mshr_middlename<br>Eilutė | Skaitymas/rašymas<br>Pasirinktinai | Pretendento antrasis vardas. |
| **Pavardės priešdėlis**<br>mshr_lastnameprefix<br>Eilutė | Skaitymas/rašymas<br>Pasirinktinai | Pretendento pavardės priešdėlis. |
| **Pavardė**<br>mshr_lastname<br>Eilutė | Skaitymas/rašymas<br>Pasirinktinai | Kandidato pavardė. |
| **Giminė**<br>mshr_gender<br>mshr_hcmpersongender parinkties nustatymas | Skaitymas/rašymas<br>Pasirinktinai | Pretendento lytis. |
| **Gimimo data**<br>mshr_birthdate<br>Datetime | Skaitymas/rašymas<br>Pasirinktinai | Pretendento gimimo data. |
| **Pilietybės šalies kodas**<br>mshr_citizenshipcountrycode<br>Eilutė | Skaitymas/rašymas<br>Pasirinktinai | Nurodo šalį, kurios piliečiu pretendentas yra. Galiojantys šalies kodai yra mshr_logisticaddresscountryregionentity. |
| **Veterano būsenos ID**<br>mshr_veteranstatusid<br>Eilutė | Skaitymas/rašymas<br>Pasirinktinai | Rodo pretendento veterano būseną. |
| **Veterano būsenos ID vertė**<br>_mshr_fk_veteranstatus_id_value<br>Guid | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: mshr_hcmveteranstatusentityid mshr_hcmveteranstatusentity | Sistemos sukurtas unikalus identifikatorius veterno būsenos objekto įrašui. |
| **Karinės tarnybos pradžios data**<br>mshr_militaryservicestartdate<br>Datetime | Skaitymas/rašymas<br>Pasirinktinai | Pretendento tarnavimo kariuomenėje pradžios data. |
| **Karinės tarnybos pabaigos data**<br>mshr_militaryserviceenddate<br>Datetime | Skaitymas/rašymas<br>Pasirinktinai | Pretendento tarnavimo kariuomenėje pabaigos data. |
| **Seniai dirbantysis su negalia**<br>mshr_isdisabledveteran<br>mshr_noyes parinkties nustatymas | Skaitymas/rašymas<br>Pasirinktinai | Nurodo, ar kandidatas yra neįgalus veteranas. |
| **Darbo pradžios data**<br>mshr_availabilitydate<br>Datetime | Skaitymas/rašymas<br>Pasirinktinai | Anksčiausia data, kai pretendentas gali pradėti dirbti. |
| **Yra suinteresuotas būti perkeltu**<br>mshr_iswillingtorelocate<br>mshr_noyes parinkties nustatymas | Skaitymas/rašymas<br>Pasirinktinai | Rodo, ar pretendentas yra suinteresuotas būti perkeltu pareigose. |
| **Komentarai**<br>mshr_comments<br>Eilutė | Skaitymas/rašymas<br>Pasirinktinai | Komentarai, kuriuos naudoja darbdavys ar samdantis vadovas. |
| **Paraiškos integravimo rezultatas**<br>mshr_applcantintegrationresult<br>mshr_applicantintegrationresult parinkties rinkinys | Skaitymas/rašymas<br>Būtina | Pretendento samdymo proceso susijusio su integravimu būsena. |
| **Nesamdymo priežasties kodo ID**<br>mshr_donothirereasoncodeid<br>Eilutė | Skaitymas/rašymas<br>Pasirinktinai | Priežasties kodas pasirinktinai pateiktas, kai būsena (paraiškos integravimo rezultatas) yra nustatytas į „Nepasamdytas“. |
| **Priežasties kodo ID vertė**<br>_mshr_fk_reasoncode_id_value<br>Guid | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: mshr_hcmreasoncodeentityid mshr_hcmreasoncodeentity objektas | Sistemos sukurtas unikalus identifikatorius **Nesamdyti** priežasties kodui. |
| **Duomenų srities ID**<br>mshr_dataareaid<br>Eilutė | Skaitymas/rašymas<br>Pasirinktinai |  Nurodo juridinį asmenį (įmonę). |
| **Duomenų srities ID vertė**<br>_mshr_dataareaid_id_value<br>Guid | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: cdm_companyid of cdm_company objektas | Sistemos sukurta GUID vertė rodanti juridnį asmenį (įmonę). |

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>
[Samdomo pretendento pavyzdžio užklausa](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
