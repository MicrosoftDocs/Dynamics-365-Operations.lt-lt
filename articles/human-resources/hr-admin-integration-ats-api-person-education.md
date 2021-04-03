---
title: Asmens išsilavinimas
description: Šioje temoje aprašomas asmens išsilavinimo objektas „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: cfa05fe6816c6b24034f8f015bf6e42d665ef1dc
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466501"
---
# <a name="person-education"></a>Asmens išsilavinimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas asmens išsilavinimo objektas „Dynamics 365 Human Resources“.

Fizinis pavadinimas: mshr_hcmpersoneducationentity

## <a name="description"></a>aprašymas

Objekte yra asmens išsilavinimo istorija, kuris yra kandidatas. Išsilavinimas yra susietas su asmens įrašu, įjungiant išsilavinimą susietą su bet kuriais kitais vaidmenimis, sukurtais asmeniui kartu su kandidato įrašu (darbuotoju, rangovu ir t.t.).

## <a name="json-representation"></a>JSON atstovavimas

```json
{
    "mshr_creditbasis": Int,
    "mshr_creditscompleted": Decimal,
    "mshr_creditsearned": Decimal,
    "mshr_creditsneeded": Decimal,
    "mshr_description": "String",
    "mshr_duration": Decimal,
    "mshr_durationunit": Int,
    "mshr_educationdisciplineid": "String",
    "mshr_educationinstitutionid": "String",
    "mshr_educationlevelid": "String",
    "mshr_enddate": "Date",
    "mshr_gradepointaverage": Decimal,
    "mshr_gradescale": "String",
    "mshr_notes": "String",
    "mshr_secondaryemphasis": "String",
    "mshr_startdate": "Date",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_educationinstitution_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmpersoneducationentityid": "Guid"
}
```

## <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | aprašymas |
| --- | --- | --- |
| **Asmens išsilavinimo objekto ID**<br>mshr_hcmpersoneducationentityid<br>*GUID* | Tik skaitomas<br>Būtina | Sistemos sukurtas unikalus asmens identifikatoriaus išsilavinimo objekto įrašas. |
| **Šalies numeris**<br>mshr_partynumber<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Unikalus identifikatorius šalies (asmens) pretendento įrašui. |
| **Asmens ID vertė**<br>_mshr_fk_person_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_dirpersonentityid of mshr_dirpersonentity | Sistemos sukurtas unikalus identifikatorius kandidato asmens įrašui. |
| **Kredito pagrindas**<br>mshr_creditbasis<br>*mshr_hcmeducationcreditbasis parinkties nustatymas* | Skaitymas/rašymas<br>Pasirinktinai | Išsilavinimo laipsnio kredito pagrindas. |
| **Užbaigti kreditai**<br>mshr_creditscompleted<br>*Dešimtainis* | Skaitymas/rašymas<br>Pasirinktinai | Užbaigti išsilavinimo kreditai. |
| **Uždirbti kreditai**<br>mshr_creditsearned<br>*Dešimtainis* | Skaitymas/rašymas<br>Pasirinktinai | Uždirbtų kreditų skaičius išsilavinimo metu įraše gaunamo laipsnio kontekste. |
| **Būtini kreditai**<br>mshr_creditsneeded<br>*Dešimtainis* | Skaitymas/rašymas<br>Pasirinktinai | Būtinų kreditų skaičius išsilavinimo metu įraše gaunamo laipsnio kontekste. |
| **Aprašas**<br>mshr_description<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Kandidato laipsnio aprašas. |
| **Išsilavinimo lygio ID**<br>mshr_educationlevelid<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Išsilavinimo lygio ID. | 
| **Išsilavinimo lygio ID vertė**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: mshr_hcmeducationdegreeentityid mshr_hcmeducationdegreeentity objektas | Sistemos sukurtas unikalus identifikatorius išsliavimo laipsnio įrašui. Identifikatorius suteikia laipsnius ir išsilavinimo lygius, nustatytus organizacijai. |
| **Išsilavinimo disciplinos ID**<br>mshr_educationdisciplineid<br>*Eilutė* | Skaitymas/rašymas<br>Būtina<br>Užsienio raktas: išsilavinimo disciplina | Išsilavinimo disciplinos ID. |
| **Išsilavinimo disciplinos ID vertė**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_hcmeducationdisciplineentityid mshr_hcmeducationdisciplineentity | Sistemos sukurtas unikalus identifikatorius išsilavinimo disciplinos įrašui. |
| **Antrinis pabrėžimas**<br>mshr_secondaryemphasis<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Gauto laipsnio antrinis pabrėžimas. |
| **Išsilavinimo įstaigos ID**<br>mshr_educationinstitutionid<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Lankytos įstaigos ID. |
| **Išsilavinimo įstaigos ID vertė**<br>_mshr_fk_educationinstitution_id_value<br>*GUID* | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: mshr_hcmeducationinstitutionentityid mshr_hcmeducationinstitutionentity | Sistemos sukurtas išsilavinimo įstaigos identifikatorius. |
| **Pradžios data**<br>mshr_startdate<br>*Data laikas* | Skaitymas/rašymas<br>Pasirinktinai | Įgyto laipsnio išsilavinimo pradžios data. |
| **Pabaigos data**<br>mshr_enddate<br>*Data laikas* | Skaitymas/rašymas<br>Būtina | Data, kai laipsnis buvo išduotas. |
| **Trukmė**<br>mshr_duration<br>*Dešimtainis* | Skaitymas/rašymas<br>Pasirinktinai | Išsilavinimo įrašo trukmė. |
| **Trukmės vienetas**<br>mshr_durationunit<br>*mshr_periodunit parinkties nustatymas* | Skaitymas/rašymas<br>Pasirinktinai | Laiko vienetas, susietas su išsilavinimo įrašo trukme. |
| **Laipsnio balų vidurkis**<br>mshr_gradepointaverage<br>*Dešimtainis* | Skaitymas/rašymas<br>Pasirinktinai | Gautų balų vidurkis laipsniui. |
| **Balų skalė**<br>mshr_gradescale<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Skalė naudojama laipsnio taškų vidurkiui. |
| **Pastabos**<br>mshr_notes<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Komentarai, kuriuos naudoja darbdavys ar samdantis vadovas. |
| **Pirminis laukelis**<br>mshr_primaryfield<br>*Eilutė* | Tik skaitomas<br>Būtina | Laukeliai, kurie naudojami kaip kitas pagrindinis objekto įrašo identifikatorius. Šalies numerio, išsilavinimo disciplinos ID, išsilavinimo įstaigos ID ir išsilavinimo lygio ID derinys. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>
[Samdomo pretendento pavyzdžio užklausa](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]