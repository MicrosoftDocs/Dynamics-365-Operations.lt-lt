---
title: Asmuo
description: Šioje temoje aprašomas asmens objektas „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: 31a60dcf26d014e3588152254d84182218096172
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054601"
---
# <a name="person"></a>Asmuo

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas asmens objektas „Dynamics 365 Human Resources“.

Fizinis pavadinimas: mshr_dirpersonentity

### <a name="description"></a>aprašymas

Objekte pateikiama asmeninė informacija apie asmenį kandidatą.

## <a name="json-representation"></a>JSON atstovavimas

```json
{
    "mshr_partynumber": "String",
    "mshr_name": "String",
    "mshr_namealias": "String",
    "mshr_knownas": "String",
    "mshr_languageid": "String",
    "mshr_addressbooks": "String",
    "mshr_anniversaryday": Int,
    "mshr_anniversarymonth": Int,
    "mshr_anniversaryyear": Int,
    "mshr_birthday": Int,
    "mshr_birthmonth": Int,
    "mshr_birthyear": Int,
    "mshr_childrennames": "String",
    "mshr_gender": Int,
    "mshr_hobbies": "String",
    "mshr_initials": "String",
    "mshr_maritalstatus": Int,
    "mshr_phoneticfirstname": "String",
    "mshr_phoneticlastname": "String",
    "mshr_phoneticmiddlename": "String",
    "mshr_personalsuffix": "String",
    "mshr_personaltitle": "String",
    "mshr_professionalsuffix": "String",
    "mshr_professionaltitle": "String",
    "mshr_fullprimaryaddress": "String",
    "mshr_addresscity": "String",
    "mshr_addresscountryregionid": "String",
    "mshr_addresscountryregionisocode": "String",
    "mshr_addresscounty": "String",
    "mshr_addressdistrictname": "String",
    "mshr_addresslatitude": Decimal,
    "mshr_addresslocationid": "000003212",
    "mshr_addresslocationroles": "Home",
    "mshr_addresslongitude": Decimal,
    "mshr_addressstate": "String",
    "mshr_addressstreet": "String",
    "mshr_addressvalidfrom": "Date",
    "mshr_addressvalidto": "Date",
    "mshr_addresszipcode": "String",
    "mshr_addressisprivate": Int,
    "mshr_addressdescription": "String",
    "mshr_primarycontactemail": "String",
    "mshr_primarycontactemaildescription": "String",
    "mshr_primarycontactemailisim": Int,
    "mshr_primarycontactemailpurpose": "String",
    "mshr_primarycontactfax": "String",
    "mshr_primarycontactfaxdescription": "String",
    "mshr_primarycontactfaxextension": "String",
    "mshr_primarycontactfaxpurpose": "String",
    "mshr_primarycontactphone": "String",
    "mshr_primarycontactphonedescription": "String",
    "mshr_primarycontactphoneextension": "String",
    "mshr_primarycontactphoneismobile": Int,
    "mshr_primarycontactphonepurpose": "String",
    "mshr_primarycontacttelex": "String",
    "mshr_primarycontacttelexdescription": "String",
    "mshr_primarycontacttelexpurpose": "String",
    "mshr_primarycontacturl": "String",
    "mshr_primarycontacturldescription": "String",
    "mshr_primarycontacturlpurpose": "String",
    "mshr_primarycontactfacebook": "String",
    "mshr_primarycontactfacebookdescription": "String",
    "mshr_primarycontactfacebookisprivate": Int,
    "mshr_primarycontactfacebookpurpose": "String",
    "mshr_primarycontactlinkedin": "String",
    "mshr_primarycontactlinkedindescription": "String",
    "mshr_primarycontactlinkedinisprivate": Int,
    "mshr_primarycontactlinkedinpurpose": "String",
    "mshr_primarycontacttwitter": "String",
    "mshr_primarycontacttwitterdescription": "String",
    "mshr_primarycontacttwitterisprivate": Int,
    "mshr_primarycontacttwitterpurpose": "String",
    "mshr_partytype": "String",
    "mshr_namesequencedisplayas": "String",
    "mshr_firstname": "String",
    "mshr_lastnameprefix": "String",
    "mshr_lastname": "String",
    "mshr_middlename": "String",
    "mshr_electroniclocationid": "String",
    "mshr_dirpersonentityid": "Guid",
    "mshr_addresstimezone": Int
}
```

## <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | aprašymas |
| --- | --- | --- |
| **Asmens objekto ID**<br>mshr_dirpersonentityid<br>*GUID* | Tik skaitomas<br>Būtina<br>Sukurta sistemos | Sistemos sukurtas unikalus identifikatorius objekto įrašui. |
| **Šalies numeris**<br>mshr_partynumber<br>*Eilutė* | Tik skaitomas<br>Būtina<br>Sukurta sistemos | Vartotojo perskaitomas, sistemos sukurtas unikalus asmens identifikatorius.  |
| **Pavadinimas / vardas ir (arba) pavardė**<br>mshr_name<br>*Eilutė* | Tik skaitomas<br>Būtina | Laukelio vertė, kuri yra vardo, antro vardo, pavardės priesagos ir pavardės derinys tvarka nustatyta **Vardo seka rodoma kaip** laukelyje. |
| **Pravardė**<br>mshr_namealias<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Pravardė, kuri asmeniui gali būti duota. |
| **Žinomas kaip**<br>mshr_knownas<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Pavadinimas, kuris gali būti naudojamas asmeniui, jei dažniausiai jis žinomas kitu vardu. |
| **Kalbos ID**<br>mshr_languageid<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens kalbos ID kaip pagrindinės kalbos, kaip nustatyta ISO 639-1 formate. |
| **Adresų knygelės**<br>mshr_addressbooks<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Adresų knyga, kuriai asmuo gali būti priskirtas. Adresų knyga, kuri buvo nustatyta organizacijai įvardytai mshr_diraddressbooksentity objekte. |
| **Jubiliejaus diena**<br>mshr_anniversaryday<br>*Int* | Skaitymas/rašymas<br>Pasirinktinai | Asmens jubiliejaus diena. |
| **Jubiliejaus mėnuo**<br>mshr_anniversarymonth<br>*mshr_monthsofyear parinkties nustatymas* | Skaitymas/rašymas<br>Pasirinktinai | Asmens jubiliejaus mėnuo. |
| **Jubiliejaus metai**<br>mshr_anniversaryyear<br>*Int* | Skaitymas/rašymas<br>Pasirinktinai | Asmens jubiliejaus metai. |
| **Gimimo diena**<br>mshr_birthday<br>*Int* | Skaitymas/rašymas<br>Pasirinktinai | Asmens gimimo diena. |
| **Gimimo mėnuo**<br>mshr_birthmonth<br>*mshr_monthsofyear parinkties nustatymas* | Skaitymas/rašymas<br>Pasirinktinai | Asmens gimimo mėnuo. |
| **Gimimo metai**<br>mshr_birthyear<br>*Int* | Skaitymas/rašymas<br>Pasirinktinai | Asmens gimimo metai. |
| **Vaikų vardai**<br>mshr_childrennames<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens vaikų vardų eilutė. Nėra jokio apribojimo. |
| **Giminė**<br>mshr_gender<br>*mshr_hcmpersongender parinkties nustatymas* | Skaitymas/rašymas<br>Pasirinktinai | Asmens lytis. |
| **Pomėgiai**<br>mshr_hobbies<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens hobiai. |
| **Inicialai**<br>mshr_initials<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens vardo inicialai. |
| **Civilinis statusas**<br>mshr_maritalstatus<br>*mshr_hcmpersonmaritalstatus parinkties nustatymas* | Skaitymas/rašymas<br>Pasirinktinai | Asmens civilinis statutas. |
| **Fonetinis vardas**<br>mshr_phoneticfirstname<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Fonetinis asmens vardo tarimas. |
| **Fonetinė pavardė**<br>mshr_phoneticlastname<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Fonetinis asmens pavardės tarimas. |
| **Fonetinis antras vardas**<br>mshr_phoneticmiddlename<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Fonetinis asmens pavardės tarimas. |
| **Asmens priesaga**<br>mshr_personalsuffix<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens priesaga. Galiojančios vertės mshr_dirnameaffixentity objekte, kai mshr_type yra Suffix (200000001). |
| **Asmens pavadinimas**<br>mshr_personaltitle<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens pavadinimas. Galiojančios vertės mshr_dirnameaffixentity objekte, kai mshr_type yra Title (200000000).
| **Profesinė priesaga**<br>mshr_professionalsuffix<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Profesinė priesaga. |
| **Profesinis pavadinimas**<br>mshr_professionaltitle<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Profesinis pavadinimas. |
| **Visas pagrindinis adresas**<br>mshr_fullprimaryaddress<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens visas pagrindinis adresas, pagrindinio adreso laukelių ryšys. |
| **Adreso miestas**<br>mshr_addresscity<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens pagrindinio adreso miestas. Nustatymas mshr_logisticsaddresscityentity objekte. |
| **Adreso šalies regionas**<br>mshr_addresscountryregionid<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Pagrindinio asmens adreso šalis / regionas. Galiojančios vertės mshr_logisticsaddresscountryregionentity objektas. |
| **Adreso šalies regiono ISO kodas**<br>mshr_addresscountryregionisocode<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | ISO šalies asmens pagrindinio adreso kodas. |
| **Adreso šalis**<br>mshr_addresscounty<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens pagrindinio adreso šalis. Nustatymas mshr_logisticsaddresscountyentity objekte. |
| **Adreso apskrities pavadinimas**<br>mshr_addressdistrictname<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens apskrities pagrindinio adreso šalis. Nustatymas mshr_logisticsaddressdistrictentity objekte. |
| **Adreso platuma**<br>mshr_addresslatitude<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens pagrindinio adreso platuma. |
| **Adreso vietos ID**<br>mshr_addresslocationid<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Unikalus identifikatorius asmens pagrindinio adreso vietai. Galiojančios vertės mshr_logisticspostaladdresslocationcdsentity objekte. |
| **Adreso vietos vaidmenys**<br>mshr_addresslocationroles<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Vietos vaidmuo asmens pagrindiniam adresui. Nustatymas mshr_logisticslocationrolecdsentity objekte. |
| **Adreso ilguma**<br>mshr_addresslongitude<br>*Eilutė* |  Skaitymas/rašymas<br>Pasirinktinai | Asmens pagrindinio adreso ilguma. |
| **Adreso būsena**<br>mshr_addressstate<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens pagrindinio adreso būsena. Nustatymas mshr_logisticsaddressstateentity objekte. |
| **Adreso gatvė**<br>mshr_addressstreet<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens pagrindinio adreso gatvė. |
| **Adresas galiojantis nuo**<br>mshr_addressvalidfrom<br>*Data* | Skaitymas/rašymas<br>Pasirinktinai | Data, nuo kurios asmens pagrindinis adresas galioja. |
| **Adresas galiojantis iki**<br>mshr_addressvalidto<br>*Data* | Skaitymas/rašymas<br>Pasirinktinai | Data, iki kurios asmens pagrindinis adresas galioja. |
| **Adreso Zip kodas**<br>mshr_addresszipcode<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens pagrindinio adreso pašto kodas. Nustatymas mshr_logisticsaddresspostalcodeentity objekte. |
| **Adresas privatus**<br>mshr_addressisprivate<br>*mshr_noyes parinkties nustatymas* | Skaitymas/rašymas<br>Pasirinktinai | Nustato, ar asmens pagrindinis adresas bendrinamas su kitais organizacijoje. |
| **Adreso aprašas**<br>mshr_addressdescription<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens pagrindinio adreso aprašas. |
| **Pagrindinis kontaktinis el. pašto adresas**<br>mshr_primarycontactemail<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens pagrindinio adreso el. paštas. |
| **Pagrindinis kontaktinis el. pašto aprašas**<br>mshr_primarycontactemaildescription<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Aprašas pateiktas pagrindiniam el. pašto adresui. |
| **Pagrindinis kontaktinis el. pašto yra IM**<br>mshr_primarycontactemailisim<br>*mshr_noyes parinkties nustatymas* | Skaitymas/rašymas<br>Pasirinktinai | Nustato, ar pagrindinis el. pašto adresas yra prieinamas greitiems pranešimams. |
| **Pagrindinis kontaktinis el. pašto tikslas**<br>mshr_primarycontactemailpurpose<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Pagrindinio el. pašto adreso tikslas. Nustatymas mshr_logisticslocationroleentity objekte. |
| **Pagrindinis kontaktinis faksas**<br>mshr_primarycontactfax<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Pagrindinis fakso numeris. |
| **Pagrindinis kontaktinis fako aprašas**<br>mshr_primarycontactfaxdescription<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Pagrindinio fakso numerio aprašas. |
| **Pagrindinis kontaktinis fako plėtinys**<br>mshr_primarycontactfaxextension<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Pagrindinio fakso numerio plėtinys. |
| **Pagrindinis kontaktinis fakso tikslas**<br>mshr_primarycontactfaxpurpose<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Pagrindinio fakso numerio tikslas. Nustatymas mshr_logisticslocationroleentity objekte.
| **Pagrindinis kontaktinis telefono numeris**<br>mshr_primarycontactphone<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Pagrindinio telefono numeris. |
| **Pagrindinis kontaktinis telefono numerio aprašas**<br>mshr_primarycontactphonedescription<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Pagrindinio telefono numerio aprašas. |
| **Pagrindinis kontaktinis telefono numerio plėtinys**<br>mshr_primarycontactphoneextension<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Pagrindinio telefono numerio plėtinys. |
| **Pagrindinis kontaktinis telefono numeris yra mobilus**<br>mshr_primarycontactphoneismobile<br>*mshr_noyes parinkties nustatymas* | Skaitymas/rašymas<br>Pasirinktinai | Nurodo, ar pagrindinis telefono numeris yra mobilus. |
| **Pagrindinis kontaktinis telefono numerio tikslas**<br>mshr_primarycontactphonepurpose<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Pagrindinio telefono numerio tikslas. Nustatymas mshr_logisticslocationroleentity objekte. |
| **Pagrindinis kontaktinis teleksas**<br>mshr_primarycontacttelex<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Pagrindinis telekso numeris. |
| **Pagrindinis kontaktinis telekso aprašas**<br>mshr_primarycontacttelexdescription<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Aprašas pateiktas asmens pagrindiniam telekso numeriui. |
| **Pagrindinis kontaktinis telekso tikslas**<br>mshr_primarycontacttelexpurpose<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Pagrindinio asmens telekso numerio tikslas. Nustatymas mshr_logisticslocationroleentity objekte. |
| **Pagrindinis kontaktinis URL**<br>mshr_primarycontacturl<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Pirminis URL. |
| **Pagrindinis kontaktinis URL aprašas**<br>mshr_primarycontacturldescription<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens pagrindinio URL aprašas. |
| **Pagrindinis kontaktinis URL tikslas**<br>mshr_primarycontacturldescription<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Pagrindinio asmens URL tikslas. Nustatymas mshr_logisticslocationroleentity objekte. |
| **Pagrindinis kontaktinis „Facebook“**<br>mshr_primarycontactfacebook<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Pagrindinė „Facebook“ paskyra. Identifikuotas pagal vartotojo ID. |
| **Pagrindinio kontaktinio „Facebook“ aprašas**<br>mshr_primarycontactfacebookdescription<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Aprašas pateiktas asmens pagrindinei „Facebook“ paskyrai. |
| **Pagrindinis kontaktinis „Facebook“ yra privatus**<br>mshr_primarycontactfacebookisprivate<br>*mshr_noyes parinkties nustatymas* | Skaitymas/rašymas<br>Pasirinktinai | Nustato, ar pagrindinė „Facebook“ paskyra yra matoma kitiems vartotojams. |
| **Pagrindinis kontaktinis „Facebook“ tikslas**<br>mshr_primarycontactfacebookpurpose<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Pagrindinės asmens „Facebook“ paskyros tikslas. Nustatymas mshr_logisticslocationroleentity objekte. |
| **Pagrindinis kontaktinis „LinkedIn“**<br>mshr_primarycontactlinkedin<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Pagrindinė „Linkedin“ paskyra. Identifikuotas pagal vartotojo vardą. |
| **Pagrindinis kontaktinis „LinkedIn“ aprašas**<br>mshr_primarycontactlinkedindescription<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Aprašas pateiktas asmens pagrindinei „LinkedIn“ paskyrai. |
| **Pagrindinis kontaktinis „LinkedIn“ yra privatus**<br>mshr_primarycontactlinkedinisprivate<br>*mshr_noyes parinkties nustatymas* | Skaitymas/rašymas<br>Pasirinktinai | Nustato, ar asmens pagrindinė „LinkedIn“ paskyros informacija yra bendrinama su kitais vartotojais. |
| **Pagrindinis kontaktinis „LinkedIn“ tikslas**<br>mshr_primarycontactlinkedinpurpose<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Pagrindinės asmens „LinkedIn“ paskyros tikslas. Nustatymas mshr_logisticslocationroleentity objekte. |
| **Pagrindinis kontaktinis „Twitter“**<br>mshr_primarycontacttwitter<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens pagrindinė „Twitter“ paskyra. Identifikuotas pagal @username. |
| **Pagrindinis kontaktinis „Twitter“ aprašas**<br>mshr_primarycontacttwitterdescription<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Aprašas pateiktas asmens pagrindinei „Twitter“ paskyrai. |
| **Pagrindinis kontaktinis „Twitter“ yra privatus**<br>mshr_primarycontacttwitterisprivate<br>*mshr_noyes parinkties nustatymas* | Skaitymas/rašymas<br>Pasirinktinai | Nustato, ar asmens pagrindinė „Twitter“ paskyros informacija yra bendrinama su kitais vartotojais. |
| **Pagrindinis kontaktinis „Twitter“ tikslas**<br>mshr_primarycontacttwitterpurpose<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Pagrindinės asmens „Twitter“ paskyros tikslas. Nustatymas mshr_logisticslocationroleentity objekte. |
| **Šalies tipas**<br>mshr_partytype<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens šalies tipas. Visuomet bus **Asmuo** pretendentams. |
| **Vardo seka rodoma kaip**<br>mshr_namesequencedisplayas<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Seka, pagal kurią asmens vardo ypatybės yra susijusios su forma Vardas (mshr_name) ypatybės verte. |
| **Vardas**<br>mshr_firstname<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Asmens vardas. |
| **Antras vardas**<br>mshr_middlename<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens antrasis vardas. |
| **Pavardės priešdėlis**<br>mshr_lastnameprefix<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens pavardės priesaga. |
| **Pavardė**<br>mshr_lastname<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens pavardė. |
| **Elektroninės vietos ID**<br>mshr_electroniclocationid<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens elektroninės vietos ID. |
| **Adreso laiko zona**<br>mshr_addresstimezone<br>*Int* | Skaitymas/rašymas<br>Pasirinktinai | Asmens pagrindinio adreso laiko zona. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>
[Samdomo pretendento pavyzdžio užklausa](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]