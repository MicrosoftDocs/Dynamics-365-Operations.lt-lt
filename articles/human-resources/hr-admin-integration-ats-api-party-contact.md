---
title: Šalies kontaktai
description: Šioje temoje aprašomas šalies kontakto objektas „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: f5a942ef93af4348404c74d8b15d98ae6fa796ff
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466741"
---
# <a name="party-contact"></a>Šalies kontaktai

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas šalies kontakto objektas „Dynamics 365 Human Resources“.

Fizinis pavadinimas: mshr_dirpartycontactentities

## <a name="description"></a>aprašymas

Šis objektas aprašo pretendento kontaktinę informaciją, įskaitant telefono numerį, el. paštą ir socialinės medijos paskyras.

## <a name="json-representation"></a>JSON atstovavimas

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_type": Int,
    "mshr_countryregioncode": "String",
    "mshr_locator": "String",
    "mshr_locatorextension": "String",
    "mshr_purpose": "String",
    "mshr_ismobilephone": Int,
    "mshr_isinstantmessage": Int,
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "String",
    "mshr_dirpartycontactentityid": "String"
}
```

## <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | aprašymas |
| --- | --- | --- |
| **Šalies kontakto objekto ID**<br>mshr_dirpartycontactentityid<br>*Eilutė* | Tik skaitomas<br>Būtina | Sistemos sukurtas unikalus identifikatorius objekto įrašui. |
| **Šalies numeris**<br>mshr_partynumber<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Susijusios šalies (asmens) įrašo ID. |
| **Asmens ID vertė**<br>_mshr_fk_person_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_dirpersonentityid of mshr_dirpersonentity | Sistemos sukurtas šalies (asmens) identifikatoriaus objekto įrašas. |
| **Vietos ID**<br>mshr_locationid<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Adreso įrašo vietos ID. Nustatymas mshr_logisticspostaladdresslocationcdsentity objekte. |
| **Aprašas**<br>mshr_description<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Kontaktinės informacijos aprašas. |
| **Tipas**<br>mshr_type<br>*mshr_logisticselectronicaddressmethodtype parinkties nustatymas* | Skaitymas/rašymas<br>Būtina | Išsamios kontaktinės informacijos tipas. |
| **Šalies regiono kodas**<br>mshr_countryregioncode<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Adreso šalis arba regionas. |
| **Lokatorius**<br>mshr_locator<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Išsami kontaktinė informacija. Pavyzdžiui, jei tipas yra **El. pašto adresas**, tuomet šiame laukelyje yra kandidato el. pašto adresas. |
| **Lokatoriaus plėtinys**<br>mshr_locatorextension<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Lokatoriaus plėtinys. Pavyzdžiui, jei tipas yra **Telefonas**, tuomet ši nuosavybė turės telefono numerio plėtinį. |
| **Yra „Mobile“**<br>mshr_ismobile<br>*mshr_noyes parinkties nustatymas* | Skaitymas/rašymas<br>Būtina | Nurodo, ar telefono numeris yra mobilus numeris. |
| **Yra greita žinutė**<br>mshr_isinstantmessage<br>*mshr_noyes parinkties nustatymas* | Skaitymas/rašymas<br>Būtina | Nurodo, ar telefono numeris yra įjungtas greitoms žinutėms. |
| **Pagrindinis**<br>mshr_isprimary<br>*mshr_noyes parinkties nustatymas* | Skaitymas/rašymas<br>Būtina | Nustato pirminį kontakto tipo kontaktą. Turi būti tik vienas pirminis įrašas kontakto tipui. |
| **Yra privatus**<br>mshr_isprivate<br>*mshr_noyes parinkties nustatymas* | Skaitymas/rašymas<br>Būtina | Nustato, ar šis adresas yra privatus asmens su nustatytu vaidmeniu adresas. |
| **Paskirtis**<br>mshr_purpose<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Kontaktinės informacijos vaidmuo/tikslas. |
| **Pirminis laukelis**<br>mshr_primaryfield<br>*Eilutė* | Tik skaitomas<br>Būtina | Laukeliai, kurie naudojami kaip pirminis objekto įrašo identifikatorius. Šalies numerio, tipo, aprašo ir lokatoriaus derinys. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>
[Samdomo pretendento pavyzdžio užklausa](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]