---
title: Samdomo pretendento pavyzdžio užklausa
description: Šiame straipsnyje pateikiamas kandidato samdyti objektą pavyzdys Dynamics 365 Human Resources.
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
ms.openlocfilehash: 2dd744665d4f0b6c64f4ee45a01c237081018514
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848349"
---
# <a name="example-query-for-candidate-to-hire"></a>Samdomo pretendento pavyzdžio užklausa


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje pateikiamas kandidato samdyti objektą pavyzdys Dynamics 365 Human Resources.

Šiame straipsnyje pateikiamas pavyzdys, apibūdinantis, kaip *galite naudoti išsamius įterpimo įrašus*, kad sukurtumėte visą naujos kandidato įrašo informaciją vienos API operacijos metu. Dėl išsamesnės informacijos apie gilius intarpus, žr. [Kurti susijusius įrašus vienoje operacijoje](/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).

Objektas **mshr_hcmcandidatetohireentity** yra unikalus dėl ryšių **mshr_dirpersonentity** su objektu. Daugelis ypatybių **mshr_hcmcandidatetohireentity** (pavyzdžiui, **mshr_firstname**, **mshr_lastname** ir **mshr_birthdate**) yra išvedamos iš **mshr_dirpersonentity** įrašo. Jei publikuojate naują kandidato įrašą į **mshr_hcmcandidatetohireentity** nenaudodami gilių intarpų, galite nustatyti vertes šioms ypatybėms tiesiai **mshr_hcmcandidatetohireentity** įraše. Susietas **mshr_dirpersonentity** įrašas yra sukuriamas tik nustatytose ypatybių vertėse. Tuomet galite sukurti kitus susijusius objektų įrašus (tokius kaip įgūdžiai ar išsilavinimas) kaip atskirus API skambučius.

Jei vis tik norite naudoti gilius intarpus siekiant sukurti visus objektus vienoje operacijoje, ypatybės nurodytos **mshr_dirpersonentity** objekte turi būti nustatytos įdėtos operacijos lygyje.

Šis pavyzdys rodo, kaip galite sukurti pretendento įrašą, susieto asmens įrašą ir asmens įgūdžius ir išsilavinimą trijuose įdėtuose lygiuose naudodami gilius intarpus vienoje API operacijoje.

> [!NOTE]
> Pavyzdys neapima visų ypatybių visuose API objektuose. Jis pateiktas tik parodomaisiais tikslais.

**Prašymas**

```http

POST [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "mshr_dataareaid": "usmf",
    "mshr_recruitingrequestid": "USMF-000141",
    "mshr_positionid": "000601",
    "mshr_iswillingtorelocate": 200000000,
    "mshr_availabilitydate": "2021-03-18",
    "mshr_comments": "Evelyn's experience is exactly what we need for this position.",
    "mshr_FK_Person_id":
        {
            "mshr_firstname": "Evelyn",
            "mshr_lastname": "Chambers",
            "mshr_namesequencedisplayas": "FirstMiddleLast",
            "mshr_FK_HcmPersonSkillEntity_Person":
            [
                {
                    "mshr_skillid": "CustFocus",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                },
                {
                    "mshr_skillid": "CashFlow",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                }
            ],
            "mshr_FK_HcmPersonEducationEntity_Person": [
                {
                    "mshr_creditbasis": 200000000,
                    "mshr_enddate": "2021-02-22T00:00:00Z",
                    "mshr_educationlevelid": "Bachelor",
                    "mshr_creditsearned": 0,
                    "mshr_startdate": "2017-02-21T00:00:00Z",
                    "mshr_creditscompleted": 0,
                    "mshr_educationinstitutionid": "Cottonwood Univ",
                    "mshr_educationdisciplineid": "Business Mgmt",
                    "mshr_durationunit": 200000000
                }              
            ]
        }
}
```

**Atsiliepimas**

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
