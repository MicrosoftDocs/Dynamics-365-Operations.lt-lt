---
title: Bendrieji integruoto tiekėjo duomenys
description: Šioje temoje aprašomas tiekėjo duomenų integravimas tarp „Finance and Operations“ ir „Common Data Service“.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 45808bc35aba04df6fcaf6b1cbfcc2461b0b65cb
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789220"
---
## <a name="integrated-vendor-master"></a>Bendrieji integruoto tiekėjo duomenys

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Terminas *Tiekėjas* reiškia tiekėjo organizaciją arba įmonės savininką, kuris yra tiekimo grandinės proceso dalis ir kuris tiekia prekes verslui. Nors *tiekėjas* yra apibrėžta koncepcija „Microsoft Dynamics 365 for Finance and Operations“, tiekėjo koncepcijos nėra „Dynamics 365 for Customer Engagement“. Vietoje to kai kuriose įmonėse naudojamas paskyros objektas, skirtas saugoti kliento ir tiekėjo informaciją. Kitos įmonės naudoja pasirinktinę tiekėjo koncepciją. „Common Data Service“ integracija palaiko abu šiuos modelius. Todėl galima įjungti bet kurį modelį, atsižvelgiant į savo verslo scenarijų.

Tiekėjo duomenų integravimas tarp „Finance and Operations“ ir „Customer Engagement“ suteikia galimybę valdyti duomenis. Neatsižvelgiant į tiekėjo duomenų kilmę, jis integruojamas fone už programų ribų ir infrastruktūros skirtumų. 

### <a name="vendor-data-flow"></a>Tiekėjo duomenų srautas

Jei tiekėjo valdymui norite naudoti „Customer Engagement“ ir pageidaujate atskirti tiekėjo informaciją nuo kliento informacijos, galite naudoti naująjį tiekėjo modelį.

![Tiekėjo duomenų srautas](media/dual-write-vendor-data-flow.png)

Jei tiekėjo valdymui norite naudoti „Customer Engagement“ ir pageidaujate toliau naudoti paskyros objektą tiekėjo informacijai saugoti, galite naudoti naująjį išplėstąjį tiekėjo modelį. Šiame modelyje išplėsta tiekėjo informacija, pvz., tiekėjų grupė ir tiekėjo registravimo profilis, saugoma tiekėjo informacijoje.

![Išplėstas tiekėjo duomenų srautas](media/dual-write-vendor-detail.jpg)

Tiekėjo kontaktinė informacija primena kliento kontaktinę informaciją. Kontaktinio asmens informacija saugoma ir gaunama iš tų pačių objektų.

## <a name="templates"></a>Šablonai

Tiekėjo duomenys apima visą informaciją apie tiekėją, pvz., tiekėjų grupę, adresus, kontaktinę informaciją, mokėjimo profilį, sąskaitos faktūros profilį. Objektų susiejimų rinkinys veikia kartu atliekant tiekėjo duomenų sąveiką, kaip parodyta tolesnėje lentelėje.

„Finance and Operations”  | „Customer Engagement“ programa
------------------------|---------------------------------
V2 tiekėjas               | Paskyra
V2 tiekėjas               | Msdyn\_vendors
CDS kontaktai V2         | Susisiekti
Tiekėjų grupės           | Msdyn\_vendorgroups
Tiekėjo mokėjimo būdas   | Msdyn\_vendorpaymentmethods
Mokėjimo grafikas        | Msdyn\_paymentschedules
Mokėjimo grafikas        | Msdyn\_paymentschedulelines
Mokėjimo diena CDS         | Msdyn\_paymentdays
Mokėjimo dienų eilutės CDS   | Msdyn\_paymentdaylines
Mokėjimo sąlygos        | Msdyn\_paymentterms
Pavadinimo afiksai            | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="vendor-v2-and-account"></a>V2 tiekėjas ir paskyra 

Įmonės, kurios naudoja paskyros objektą, kad galėtų saugoti tiekėjo informaciją, gali ir toliau jį naudoti tokiu pačiu būdu. Jos taip pat gali naudotis aiškiomis tiekėjo funkcijomis, kurios teikiamos pasitelkus „Finance and Operations“ integraciją.

## <a name="vendor-v2-and-msdyn_vendors"></a>V2 tiekėjas ir Msdyn\_vendors

Įmonės, kurios naudoja pasirinktinį sprendimą tiekėjams gali pasinaudoti pradine tiekėjo koncepcija, kuri yra pristatyta „Common Data Service“ ir teikiama dėl „Finance and Operations“ integracijos. 

<!-- ![vendor mappings](media/dual-write-vendors-1.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-2.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-3.png) -->

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
VENDORACCOUNTNUMBER | = | msdyn\_vendoraccountnumber
VENDORGROUPID | = | msdyn\_vendorgroupid.msdyn\_vendorgroup
VENDORORGANIZATIONNAME | = | msdyn\_name
VENDORPARTYTYPE | \>\< | msdyn\_isperson
PERSONFIRSTNAME | = | msdyn\_firstname
PERSONLASTNAME | = | msdyn\_lastname
CREDITLIMIT | = | msdyn\_vendorcreditlimit
ISFOREIGNENTITY | \>\< | msdyn\_isforeignentity
ISONETIMEVENDOR | \>\< | msdyn\_isonetimevendor
ADDRESSBUILDINGCOMPLIMENT | = | msdyn\_addressbuildingcompliment
PERSONCHILDRENNAMES | = | msdyn\_childrennames
ADDRESSCITY | = | msdyn\_addresscity
ADDRESSCOUNTRYREGIONID | = | msdyn\_addresscountryregionid
ADDRESSCOUNTRYREGIONISOCODE | = | msdyn\_addresscountryregionisocode
ADDRESSCOUNTYID | = | msdyn\_addresscountyid
CREDITRATING | = | msdyn\_creditrating
ADDRESSDESCRIPTION | = | msdyn\_addressdescription
ADDRESSDISTRICTNAME | = | msdyn\_addressdistrictname
DUNSNUMBER | = | msdyn\_dunsnumber
ETHNICORIGINID | = | msdyn\_ethnicorigin
FORMATTEDPRIMARYADDRESS | = | msdyn\_formattedprimaryaddress
PERSONHOBBIES | = | msdyn\_hobbies
PERSONINITIALS | = | msdyn\_initials
LANGUAGEID | = | msdyn\_languageid
PERSONLASTNAMEPREFIX | = | msdyn\_lastnameprefix
PERSONMIDDLENAME | = | msdyn\_middlename
ORGANIZATIONNUMBER | = | msdyn\_organizationnumber
OURACCOUNTNUMBER | = | msdyn\_ourvendoraccountnumber
PAYMENTID | = | msdyn\_paymentid
PERSONPHONETICFIRSTNAME | = | msdyn\_phoneticfirstname
PERSONPHONETICMIDDLENAME | = | msdyn\_phoneticmiddlename
PERSONPHONETICLASTNAME | = | msdyn\_phoneticlastname
ORGANIZATIONPHONETICNAME | = | msdyn\_organizationphoneticname
ADDRESSPOSTBOX | = | msdyn\_addresspostbox
PRIMARYURL | = | msdyn\_primarycontacturl
PRIMARYEMAILADDRESS | = | msdyn\_primaryemailaddress
PRIMARYEMAILADDRESSDESCRIPTION | = | msdyn\_primaryemailaddressdescription
PRIMARYFACEBOOK | = | msdyn\_primaryfacebook
PRIMARYFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYFAXNUMBER | = | msdyn\_primaryfaxnumber
PRIMARYFAXNUMBERDESCRIPTION | = | msdyn\_primaryfaxnumberdescription
PRIMARYFAXNUMBEREXTENSION | = | msdyn\_primaryfaxnumberextension
PRIMARYLINKEDIN | = | msdyn\_primarylinkedin
PRIMARYLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescription
PRIMARYPHONENUMBER | = | msdyn\_pimaryphonenumber
PRIMARYPHONENUMBERDESCRIPTION | = | msdyn\_primaryphonenumberdescription
PRIMARYPHONENUMBEREXTENSION | = | msdyn\_primaryphonenumberextension
PRIMARYTELEX | = | msdyn\_primarytelex
PRIMARYTELEXDESCRIPTION | = | msdyn\_primarytelexdescription
PRIMARYTWITTER | = | msdyn\_primarytwitter
PRIMARYTWITTERDESCRIPTION | = | msdyn\_primarytwitterdescription
PRIMARYURLDESCRIPTION | = | msdyn\_primaryurldescription
PERSONPROFESSIONALSUFFIX | = | msdyn\_professionalsuffix
PERSONPROFESSIONALTITLE | = | msdyn\_professionatitle
ADDRESSSTATEID | = | msdyn\_addressstateid
ADDRESSSTREET | = | msdyn\_addressstreet
ADDRESSSTREETNUMBER | = | msdyn\_addressstreetnumber
VENDORKNOWNASNAME | = | msdyn\_vendorknownasname
ADDRESSZIPCODE | = | msdyn\_addresszipcode
DEFAULTPAYMENTDAYNAME | = | msdyn\_defaultpaymentdayname.msdyn\_name
DEFAULTPAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
DEFAULTPAYMENTTERMSNAME | = | msdyn\_paymentterms.msdyn\_name
HASONLYTAKENBIDS | \>\< | msdyn\_hasonlytakenbids
ISMINORITYOWNED | \>\< | msdyn\_isminorityowned
ISVENDORLOCALLYOWNED | \>\< | msdyn\_isvendorlocallyowned
ISSERVICEVETERANOWNED | \>\< | msdyn\_isserviceveteranowned
ISOWNERDISABLED | \>\< | msdyn\_ownerisdisabled
ISWOMANOWNER | \>\< | msdyn\_womanowner
PERSONANNIVERSARYDAY | = | msdyn\_personanniversaryday
PERSONANNIVERSARYYEAR | = | msdyn\_anniversaryyear
PERSONBIRTHDAY | = | msdyn\_birthday
PERSONBIRTHYEAR | = | msdyn\_birthyear
ORGANIZATIONEMPLOYEEAMOUNT | = | msdyn\_numberofemployees
VENDORHOLDRELEASEDATE | = | msdyn\_vendoronholdreleasedate
VENDORPARTYNUMBER | = | msdyn\_vendorpartynumber
ADDRESSLOCATIONID | = | msdyn\_addresslocationid
PERSONANNIVERSARYMONTH | = | msdyn\_vendorpersonanniversarymonth
PERSONBIRTHMONTH | = | msdyn\_vendorpersonbirthmonth
PERSONMARITALSTATUS | \>\< | msdyn\_maritalstatus
ADDRESSLATITUDE | \>\> | msdyn\_addresslatitude
ADDRESSLONGITUDE | \>\> | msdyn\_addresslongitude
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
CURRENCYCODE | = | msdyn\_currencycode.isocurrencycode
ISVENDORLOCATEDINHUBZONE | \>\< | msdyn\_isvendorlocatedinhubzone
DEFAULTVENDORPAYMENTMETHODNAME | = | msdyn\_vendorpaymentmethod.msdyn\_name
INVOICEVENDORACCOUNTNUMBER | = | msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber
PERSONGENDER | \>\< | msdyn\_gender
AREPRICESINCLUDINGSALESTAX | \>\< | msdyn\_priceincludessalestax
SALESTAXGROUPCODE | = | msdyn\_taxgroup.msdyn\_name
VENDORPRICETOLERANCEGROUPID | = | msdyn\_pricetolerancegroup.msdyn\_groupid

## <a name="contacts"></a>Kontaktai

Šis šablonas sinchronizuoja visą pagrindinių, antrinių ir tretinių klientų ir tiekėjų kontaktinę informaciją tarp „Finance and Operations“ ir „Customer Engagement“. Informaciją apie objekto susiejimą žr. [Integruotasis kliento šablonas](dual-write-customer.md#contacts).

## <a name="vendor-groups"></a>Tiekėjų grupės

Šis šablonas sinchronizuoja tiekėjų grupių informaciją tarp „Finance and Operations“ ir „Customer Engagement“.

<!-- ![vendor groups mappings](media/dual-write-vendor-groups.png) -->

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
DEFAULTPAYMENTTERMNAME | = | msdyn\_paymentterms.msdyn\_name
APRAŠAS | = | msdyn\_description
VENDORGROUPID | = | msdyn\_vendorgroup
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymentpermname.msdyn\_name

### <a name="vendor-payment-method"></a>Tiekėjo mokėjimo būdas

Šis šablonas sinchronizuoja tiekėjo mokėjimo būdo informaciją tarp „Finance and Operations“ ir „Customer Engagement“.

<!-- ![vendor payment method mappings](media/dual-write-vendor-payment-method.png) -->

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
PAVADINIMAS | = | msdyn\_name
APRAŠAS | = | msdyn\_description
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
ALLOWPAYMENTCOPIES | \>\< | msdyn\_allowpaymentcopies
PAYMENTTYPE | \>\< | msdyn\_paymenttype
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
ACCOUNTTYPE | \>\< | msdyn\_accounttype
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingposting
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_postdatedcheckclearingposting
PROMISSORYNOTEDRAFTTYPE | \>\< | msdyn\_promissorynotedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

