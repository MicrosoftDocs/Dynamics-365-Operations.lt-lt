---
title: Asmens profesinė patirtis
description: Šiame straipsnyje aprašomas asmens profesinės patirties subjektas Dynamics 365 Human Resources.
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
ms.openlocfilehash: d306213e4c647ecd4be98598cba92376aba0d5bb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856431"
---
# <a name="person-professional-experience"></a>Asmens profesinė patirtis


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašomas asmens profesinės patirties subjektas Dynamics 365 Human Resources.

Fizinis pavadinimas: mshr_hcmpersonprofessionalexperienceentity

## <a name="description"></a>aprašymas

Šis objektas aprašo pretendento profesinę patirtį ar darbo istoriją.

## <a name="json-representation"></a>JSON atstovavimas

```json
{
    "mshr_partynumber": "String",
    "mshr_employerposition": "String",
    "mshr_startdate": "Date",
    "mshr_allowcontactemployer": Int,
    "mshr_employerlocation": "String",
    "mshr_employername": "String",
    "mshr_enddate": "Date",
    "mshr_note": "String",
    "mshr_phone": "String",
    "mshr_url": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonprofessionalexperienceentityid": "Guid"
}
```

## <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | aprašymas |
| --- | --- | --- |
| **Asmens profesinė patirties objekto ID**<br>mshr_hcmpersonprofessionalexperienceentityid<br>*GUID* | Tik skaitomas<br>Būtina | Sistemos sukurtas unikalus identifikatorius objekto įrašui. |
| **Šalies numeris**<br>mshr_partynumber<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Unikalus identifikatorius asmens pretendento įrašui. |
| **Asmens ID vertė**<br>_mshr_fk_person_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_dirpersonentityid of mshr_dirpersonentity | Sistemos sukurtas unikalus asmens identifikatoriaus objekto įrašas. |
| **Darbuotojo pareigos**<br>mshr_employerposition<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Pareigų pavadinimas, kurį pretendentas turi būdamas samdomu. |
| **Darbuotojo vardas**<br>mshr_employername<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Darbdavio vardas. |
| **Darbdavio vieta**<br>mshr_employerlocation<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Darbdavio vieta. Maks. ilgis: 60. Nenustatytas ar nebūtinas joks konkretus formatas. |
| **Telefonas**<br>mshr_phone<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Darbdavio telefono numeris. |
| **URL**<br>mshr_url<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Darbdavio svetainės URL. |
| **Pradžios data**<br>mshr_startdate<br>*Data laikas* | Skaitymas/rašymas<br>Būtina | Pretendento įdarbinimo pradžios data. |
| **Pabaigos data**<br>mshr_enddate<br>*Data laikas* | Skaitymas/rašymas<br>Pasirinktinai | Kandidato įdarbinimo pabaigos data arba kandidatui leidimas dirbti, jei jis dar dirba. |
| **Leisti darbdabio kontaktą**<br>mshr_allowcontactemployer<br>*mshr_hrmblankyesno parinkties nustatymas* | Skaitymas/rašymas<br>Pasirinktinai | Reiškia, ar kandidatas leidžia susisiekti su ankstesniu darbdaviu. |
| **Pastabos**<br>mshr_note<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Komentarai, kuriuos naudoja darbdavys ar samdantis vadovas. |
| **Pirminis laukelis**<br>mshr_primaryfield<br>*Eilutė* | Tik skaitomas<br>Būtina | Laukeliai, kurie naudojami kaip pirminis objekto įrašo identifikatorius. Šalies numerio, pradžios datos, darbdavio pareigų ir darbuotojo vardo derinys. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>
[Samdomo pretendento pavyzdžio užklausa](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
