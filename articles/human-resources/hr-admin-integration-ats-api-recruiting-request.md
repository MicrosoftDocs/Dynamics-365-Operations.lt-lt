---
title: Įdarbinimo užklausa
description: Šioje temoje aprašomas samdytino užklausos objektas „Dynamics 365 Human Resources“.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a1f160d828c8fe5babb96d39afd911052767f67b
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068589"
---
# <a name="recruiting-request"></a>Įdarbinimo užklausa


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas samdytino užklausos objektas „Dynamics 365 Human Resources“.

Fizinis pavadinimas: mshr_hcmrecruitingrequestentity

### <a name="description"></a>aprašymas

Aprašo prašymą pasamdyti darbui.

### <a name="json-representation"></a>JSON atstovavimas

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_hiringmanagerpersonnelnumber": "String",
    "mshr_recruiterpartynumber": "String",
    "mshr_status": Int,
    "mshr_description": "String",
    "mshr_recruitingrequestlocationid": "String",
    "mshr_comments": "String",
    "mshr_jobid": "String",
    "mshr_titleid": "String",
    "mshr_jobfunctionid": "String",
    "mshr_defaultfulltimeequivalency": Decimal,
    "mshr_regulatoryjobcategory": Int,
    "mshr_jobtypeid": "String",
    "mshr_exemptstatus": Int,
    "mshr_estimatedstartdate": "Date",
    "mshr_externaldescription": "String",
    "mshr_compensationlevelid": "String",
    "mshr_compensationlowthreshold": Decimal,
    "mshr_compensationcontrolpoint": Decimal,
    "mshr_compensationhighthreshold": Decimal,
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "_mshr_fk_hiringmanager_id_value": "Guid",
    "_mshr_fk_recruiter_id_value": "Guid",
    "_mshr_fk_job_id_value": "Guid",
    "_mshr_fk_title_id_value": "Guid",
    "_mshr_fk_jobtype_id_value": "Guid",
    "_mshr_fk_compensationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequestentityid": "Guid",
    "_mshr_fk_recruitingrequestlocation_id_value": “Guid”
}
```

### <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | aprašymas |
| --- | --- | --- |
| **Įdarbinimo užklausos ID**<br>mshr_recruitingrequestid<br>*Eilutė* | Tik skaitomas<br>Būtina<br>Sukurta sistemos | Vartotojo perskaitomas unikalus idnetifikatorius užklausai rodomai HR paraiškoje. Skaičių seka. |
| **Įdarbinimo užklausos objekto ID**<br>mshr_hcmrecruitingrequestentityid<br>*GUID* | Tik skaitomas<br>Būtina<br>Sukurta sistemos | Sistemos sukurta GUID vertė siekiant unikaliai atpažinti įdarbinimo užklausą. |
| **Duomenų srities ID**<br>mshr_dataareaid<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai<br> | Nurodo jurdinį asmenį (bendrovę) įdarbinimo užklausai. |
| **Duomenų srities ID vertė**<br>_mshr_dataareaid_id_value<br>*GUID*<br> | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: cdm_companyid of cdm_company objektas | Sistemos sukurta GUID vertė rodanti juridnį asmenį (įmonę) įdarbinimo užklausai. |
| **Įdarbinančio vadovo asmens numeris**<br>mshr_hiringmanagerpersonnelnumber<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Samdančio vadovo personalo numeris susietas su šia samdymo užklausa. |
| **Įdarbinančio vadovo ID vertė**<br>_mshr_fk_hiringmanager_id_value<br>*GUID* | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: mshr_hcmworkerbaseentityid mshr_hcmworkerbaseentity objektas | Sistemos sukurta GUID vertė siekiant atpažinti vadovą susietą su įdarbinimo užklausa. |
| **Samdančios šalies numeris**<br>mshr_recruiterpartynumber<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Samdančio asmens (šalies) numeris pasirinktas užklausai. |
| **Samdančio asmens ID vertė**<br>_mshr_fk_recruiter_id_value<br>*GUID* | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: mshr_dirpersonentityid mshr_dirpersonentity objektas | Sistemos sukurta GUID vertė siekiant atpažinti samdantį asmenį susietą su įdarbinimo užklausa. |
| **Būsena**<br>mshr_status<br>*RecruitingRequestStatus* parinkties nustatymas | Skaitymas/rašymas<br>Būtina<br> | Rodo įdarbinimo užklausos būseną. |
| **Aprašas**<br>mshr_description<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Aprašo užklausą. |
| **Samdymo užklausos vietos ID**<br>mshr_recruitingrequestlocationid<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Vartotojo perskaitomas unikalus idnetifikatorius darbo vietai susietai su šia užklausa. |
| **Įdarbinimo vietos ID vertė**<br>_mshr_fk_recruitinglocation_id_value<br>*GUID* | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: mshr_hcmrecruitingrequestlocationentityid mshr_hcmrecruitingrequestlocationentity objektas | Sistemos sukurta GUID vertė siekiant atpažinti samdymo užklausos vietą pasirinktą užklausai. |
| **Komentarai**<br>mshr_comments<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Komentarai apie užklausą samdymo vadovų ir asmenų naudojimui. |
| **Užduoties ID**<br>mshr_jobid<br>*Eilutė* | Rašyti kartą<br>Būtina |   Vartotojo perskaitomas unikalus idnetifikatorius darbo darbui bendrintui su visomis pareigomis susijusiomis su šia užklausa. |
| **Darbo ID vertė**<br>_mshr_fk_job_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_hcmjobentityid mshr_hcmjobentity objektas | Sistemos sukurtas unikalus idnetifikatorius darbo darbui bendrintui su visomis pareigomis susijusiomis su šia įdarbinimo užklausa. |
| **Pavadinimo ID**<br>mshr_titleid<br>*Eilutė* | Tik skaitomas<br>Būtina | Vartotojo perskaitomas unikalus idnetifikatorius darbo pavadinimu susietu su šia užklausa. |
| **Pavadinimo ID vertė**<br>_mshr_fk_title_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_hcmtitleid mshr_hcmtitleentity objektas | Sistemos sukurtas unikalus identifikatorius darbo pavadinimui pasirinktam įdarbinimo užklausos. |
| **Darbo funkcijos ID**<br>mshr_jobfunctionid<br>*Eilutė* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_jobfunctionid mshr_hcmjobfunctionentity objektas | Vartotojo perskaitomas unikalus idnetifikatorius darbo funkcijai susietai su šia užklausa. |
| **Numatytas viso darbo laiko ekvivalentiškumas**<br>mshr_defaultfulltimeequivalency<br>*Dvigubas* | Tik skaitomas<br>Būtina | Viso darbo laiko ekvivalento vertė darbui, kai 1.0 rodo visą laiką dirbantį darbuotoją. |
| **Reguliavimo darbo kategorija**<br>mshr_regulatoryjobcategory<br>*RegulatoryJobCategory* nustatyta parinktis | Tik skaitomas<br>Pasirinktinai | EEO darbo funkcijos darbo kategorija pasirinktam darbui. Galiojančios vertės apimtos HcmRegulatoryJobCatetory (mshr_hcmregulatoryjobcategory) nustatyoje parinktyje. |
| **Darbo tipo ID**<br>mshr_jobtypeid<br>*Eilutė* | Tik skaitomas<br>Pasirinktinai | Darbo tipas susietas su pareigomis. Darbo tipai yra vartotojo nustatytos vertės prieinamos mshr_hcmjobtypeentity objekte. |
| **Darbo tipo ID vertė**<br>_mshr_fk_jobtype_id_value<br>*GUID* | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: mshr_hcmjobtypeentityid mshr_hcmjobtypenentity objektas | Sistemos sukurtas unikalus idnetifikatorius darbo tipas susietas su darbo samdymo užklausa. |
| **Neapmokestinimo būsena**<br>mshr_exemptstatus<br>*JobExemptStatus* parinkties nustatymas | Tik skaitomas<br>Pasirinktinai | FLSA išlygos statusas pagal darbo tipą. |
| **Apskaičiuota pradžios data**<br>mshr_estimatedstartdate<br>*Data* | Skaitymas/rašymas<br>Būtina | Apskaičiuota data, kai pretendentas pradės dirbti. |
| **Išorės aprašas**<br>mshr_externaldescription<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Kandidatui suteiktas darbo ar pareigų aprašas. | 
| **Užmokesčio apatinis slenkstis**<br>mshr_compensationlowthreshold<br>*Dvigubas* | Skaitymas/rašymas<br>Pasirinktinai | Apatinė užmokesčio lygio riba. |
| **Užmokesčio valdymo taškas**<br>mshr_compensationcontrolpoint<br>*Dvigubas* | Skaitymas/rašymas<br>Pasirinktinai | Užmokesčio lygio valdymo taškas. |
| **Užmokesčio viršutinis slenkstis**<br>mshr_compensationhighthreshold<br>*Dvigubas* | Skaitymas/rašymas<br>Pasirinktinai | Viršutinė užmokesčio lygio riba. |
| **Užmokesčio lygis**<br>mshr_compensationlevelid<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Užmokesčio už darbą lygis. Darbas gali būti nustatytas su keliais užmokesčio lygiais. Šis atributas rodo pasirinktą darbo užmokesčio lygį užklausai. |
| **Darbo užmokesčio ID**<br>_mshr_fk_jobcompensation_id_value<br>*GUID* | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: mshr_hcmjobcompensationentityid mshr_hcmjobcompensationentity objektas | Sistemos sukurtas unikalus idnetifikatorius užmokesčio lygiui, susietam su darbo samdymo užklausa. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>
[Pavyzdinė užklausa Samdymo prašymui](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
