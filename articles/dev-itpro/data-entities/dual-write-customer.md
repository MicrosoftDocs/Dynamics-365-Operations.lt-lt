---
title: Bendrieji integruoto kliento duomenys
description: Šioje temoje aprašomas klientų duomenų integravimas tarp „Finance and Operations“ ir Common Data Service.
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
ms.openlocfilehash: a8030d9d1f1f3636a679d334afddad0f573a824e
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789221"
---
## <a name="integrated-customer-master"></a>Bendrieji integruoto kliento duomenys

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Klientų įrašai paprastai naudojami daugiau negu vienoje programoje. Pavyzdžiui, pardavimo veikla gali pateikti komercinio kliento įrašus per Microsoft Dynamics 365 for Sales programą, o el. prekybos ar mažmeninės prekybos pardavimas gali pateikti kliento įrašus per Dynamics 365 for Finance and Operations programą. Neatsižvelgiant į kliento įrašo kilmę, jis integruojamas fone už programų ribų ir infrastruktūros skirtumų. Integruoto kliento bendrieji duomenys padeda atlikti bendrųjų duomenų įsisavinimo scenarijus ir teikia išsamų kliento vaizdą „Dynamics 365“ programų pakete.

## <a name="customer-data-flow"></a>Kliento duomenų srautas

*Klientas* yra aiškiai apibrėžta koncepcija tiek „Finance and Operations“, tiek Common Data Service. Todėl kliento duomenų integravimas yra susijęs su klientų koncepcijos harmonizavimu tarp „Finance and Operations ir Common Data Service programų. Tolesnėje iliustracijoje pateiktas kliento duomenų srautas.

![Kliento duomenų srautas](media/dual-write-customer-data-flow.png)

Klientai gali būti suskirstyti į du tipus: komerciniai/organizaciniai klientai ir vartotojai/galutiniai vartotojai. Šie du klientų tipai „Finance and Operations“ ir Common Data Service yra saugomi ir tvarkomi skirtingai.

„Finance and Operations“ tiek komercinių/organizacinių klientų, tiek vartotojų/galutinių vartotojų duomenys naudojami vienoje lentelėje, pavadintoje **CustTable** (CustomerCustomerV3Entity), ir jie klasifikuojami pagal atributą **Tipas**. (Jei **Tipas** nustatytas kaip **Organizacija**, klientas yra komercinis/organizacinis klientas, o jei **Tipas** nustatytas kaip **Asmuo**, klientas yra vartotojas/galutinis vartotojas.) Pagrindinio kontaktinio asmens informacija tvarkoma naudojant objektą SMMContactPersonEntity.

Common Data Service komercinių/organizacinių klientų duomenys tvarkomi objekte Sąskaita ir jie yra identifikuojami kaip klientai, kai atributas **RelationshipType** yra nustatytas į **Klientas**. Tiek vartotojus/galutinius vartotojus, tiek kontaktinius asmenis atstovauja objektas Kontaktas. Siekiant aiškiai atskirti vartotoją/galutinį vartotoją ir kontaktinį asmenį, objekte **Kontaktas** yra Bulio logikos žymė, pavadinta **Pardavimas**. Jeigu **Pardavimas** yra **Teisinga**, kontaktas yra vartotojas/galutinis vartotojas, ir tam užsakymui gali būti kuriami pasiūlymai ir užsakymai. Kai **Pardavimas** yra **Klaidinga**, kontaktas yra tik pirminis kliento kontaktinis asmuo.

Jeigu pasiūlyme ar užsakymo procese dalyvauja ne pardavimo kontaktas, **Pardavimas** nustatomas į **Teisinga**, kad kontaktas būtų pažymėtas kaip pardavimo kontaktas. Kontaktas, kuris tapo pardavimo kontaktu, lieka pardavimo kontaktu.

## <a name="templates"></a>Šablonai

Kliento duomenys apima visą informaciją apie klientą, pvz., klientų grupę, adresus, kontaktinę informaciją, mokėjimo profilį, sąskaitos faktūros profilį ir lojalumo būseną. Objektų susiejimų rinkinys veikia kartu atliekant kliento duomenų sąveiką, kaip parodyta tolesnėje lentelėje.

„Finance and Operations”    | „Customer Engagement“ programa
--------------------------|---------------------------------
Klientas V3               | Paskyra
Klientas V3               | Susisiekti
CDS kontaktai V2           | Susisiekti
Klientų grupės           | Msdyn\_customergroups
Kliento mokėjimo būdas   | Msdyn\_customerpaymentmethods
Lojalumo kortelė              | Msdyn\_loyaltycards
Mokėjimo grafikas          | Msdyn\_paymentschedules
Mokėjimo grafikas          | Msdyn\_paymentschedulelines
Mokėjimo diena CDS           | Msdyn\_paymentdays
Mokėjimo dienų eilutės CDS     | Msdyn\_paymentdaylines
Mokėjimo sąlygos          | Msdyn\_paymentterms
Pavadinimo afiksai              | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="customer-v3-to-account"></a>Klientas V3 su sąskaita

Šis šablonas sinchronizuoja komerciniams ir organizaciniams klientams skirtą kliento pagrindinę informaciją tarp „Finance and Operations“ ir Common Data Service.

<!-- ![](media/dual-write-account-1.png) -->

<!-- ![](media/dual-write-account-2.png) -->

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
CUSTOMERACCOUNT | = | accountnumber
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
CREDITLIMIT | = | creditlimit
DELIVERYADDRESSCITY | = | address1\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
DELIVERYADDRESSCOUNTY | = | address1\_county
DELIVERYADDRESSLATITUDE | \> | address1\_latitude
DELIVERYADDRESSLONGITUDE | \> | address1\_longitude
DELIVERYADDRESSZIPCODE | = | address1\_postalcode
ORGANIZATIONNAME | = | pavadinimas
ORGANIZATIONNUMBEROFEMPLOYEES | = | numberofemployees
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTTWITTER | = | primarytwitterid
PRIMARYCONTACTURL | = | websiteurl
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | aprašas
CREDITLIMITISMANDATORY | \>\< | msdyn\_creditlimitismandatory
CREDITRATING | = | msdyn\_creditrating
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
INVOICEACCOUNT | = | msdyn\_billingaccount.accountnumber
INVOICEADDRESS | \>\< | msdyn\_invoiceaddress
ISONETIMECUSTOMER | \>\< | msdyn\_onetimecustomer
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PAYMENTDAY | = | msdyn\_paymentday.msdyn\_name
PAYMENTMETHOD | = | msdyn\_customerpaymentmethod.msdyn\_name
PAYMENTSCHEDULE | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTTERMS | = | msdyn\_paymentterm.msdyn\_name
PAYMENTTERMSBASEDAYS | = | msdyn\_paymenttermsbasedays
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
PRIMARYCONTACTLINKEDIN | = | msdyn\_primarylinkedinid
TAXEXEMPTNUMBER | = | msdyn\_taxexemptnumber
VENDORACCOUNT | = | msdyn\_vendor.msdyn\_vendoraccountnumber
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
LANGUAGEID | \<\< | nėra
DELIVERYADDRESSSTREET | = | address1\_line1
DELIVERYADDRESSSTATE | = | address1\_stateorprovince
nėra | \>\> | address1\_addresstypecode
nėra | \>\> | customertypecode
PARTYTYPE | \<\< | nėra
PARTYNUMBER | = | msdyn\_partynumber

## <a name="customer-v3-to-contact"></a>Klientas V3 su kontaktu

Šis šablonas sinchronizuoja klientų ir galutinių vartotojų bendruosius duomenis tarp „Finance and Operations“ ir „Customer Engagement“.

<!-- ![](media/dual-write-contact-1.png) -->
<!-- ![](media/dual-write-contact-2.png) -->

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
nėra | \>\> | msdyn\_sellable
PARTYTYPE | \<\< | nėra
PARTYNUMBER | = | msdyn\_partynumber
CUSTOMERACCOUNT | = | msdyn\_contactpersonid
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
PERSONFIRSTNAME | = | firstname
PERSONLASTNAME | = | lastname
PERSONMIDDLENAME | = | middlename
PERSONPROFESSIONALTITLE | = | jobtitle
PERSONGENDER | \>\< | gendercode
PERSONMARITALSTATUS | \>\< | familystatuscode
LANGUAGEID | \<\< | nėra
ADDRESSCITY | = | address1\_city
ADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
ADDRESSCOUNTY | = | address1\_county
ADDRESSLATITUDE | \> | address1\_latitude
ADDRESSLONGITUDE | \> | address1\_longitude
ADDRESSLOCATIONROLES | \<\< | nėra
ADDRESSSTATE | = | address1\_stateorprovince
ADDRESSSTREET | = | address1\_line1
ADDRESSZIPCODE | = | address1\_postalcode
ADRESOSPOSTBOX | = | address1\_postofficebox
nėra | \>\> | address1\_addresstypecode
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
nėra | \>\> | address2\_addresstypecode
DELIVERYADDRESSCITY | = | address3\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address3\_country
DELIVERYADDRESSCOUNTY | = | address3\_county
DELIVERYADDRESSLATITUDE | \> | address3\_latitude
DELIVERYADDRESSLONGITUDE | \>\> | address3\_longitude
DELIVERYADDRESSSTATE | = | address3\_stateorprovince
DELIVERYADDRESSSTREET | = | address3\_line1
DELIVERYADDRESSZIPCODE | = | address3\_postalcode
nėra | \>\> | address3\_addresstypecode
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTLINKEDIN | = | msdyn\_primaryinkedinid
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTER | = | msdyn\_primarytwitterid
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURL | = | websiteurl
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | aprašas

## <a name="contacts"></a>Kontaktai

Šis šablonas sinchronizuoja visą pagrindinių, antrinių ir tretinių klientų ir tiekėjų kontaktinę informaciją tarp „Finance and Operations“ ir „Customer Engagement“.

<!-- ![](media/dual-write-contacts.png) -->

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn\_partynumber
ASSOCIATEDCONTACTTYPE | \<\< | nėra
FIRSTNAME | = | firstname
MIDDLENAME | = | middlename
LASTNAME | = | lastname
ASSOCIATEDCONTACTNUMBER | = | msdyn\_vendorcontactid.msdyn\_vendoraccountnumber
PRIMARYADDRESSCITY | = | address1\_city
PRIMARYADDRESSCOUNTRYREGIONID | = | address1\_country
PRIMARYADDRESSCOUNTYID | = | address1\_county
PRIMARYFAXNUMBER | = | fax
PRIMARYADDRESSSTATEID | = | address1\_stateorprovince
PRIMARYADDRESSSTREET | = | address1\_line1
PRIMARYADDRESSZIPCODE | = | address1\_postalcode
PRIMARYPHONENUMBER | = | telephone1
PRIMARYEMAILADDRESS | = | emailaddress1
EMPLOYMENTDEPARTMENT | = | department
PASTABOS | = | aprašas
LYTIS | \>\< | gendercode
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid
PRIMARYURL | = | websiteurl
MARITALSTATUS | \>\< | familystatuscode
ISRECEIVINGDIRECTMAIL | \>\< | donotemail
EMPLOYMENTPROFESSION | = | jobtitle
SPOUSENAME | = | spousesname
nėra | \>\> | msdyn\_contactforvendor
nėra | \>\> | msdyn\_contactpersonid

## <a name="customer-groups"></a>Klientų grupės

Šis šablonas sinchronizuoja klientų grupių informaciją tarp „Finance and Operations“ ir „Customer Engagement“.

<!-- ![](media/dual-write-customer-groups.png) -->

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
CUSTOMERGROUPID | = | msdyn\_groupid
APRAŠAS | = | msdyn\_description
ISSALESTAXINCLUDEDINPRICE | \>\< | msdyn\_issalestaxincludedinprice
PAYMENTTERMID | = | msdyn\_paymenttermid.msdyn\_name
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymenttermname.msdyn\_name

## <a name="customer-payment-methods"></a>Kliento mokėjimo būdai

Šis šablonas sinchronizuoja kliento mokėjimo būdo informaciją tarp „Finance and Operations“ ir „Customer Engagement“.

<!-- ![](media/dual-write-customer-payment-methods.png) -->

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
PAVADINIMAS | = | msdyn\_name
ACCOUNTTYPE | \>\< | msdyn\_accounttype
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingpostingenabled
ISSEPA | \>\< | msdyn\_issepa
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
APRAŠAS | = | msdyn\_description
PAYMENTTYPE | \>\< | msdyn\_paymenttype
CREATEANDDRAWBILLOFEXCHANGEDURINGINVOICEPOSTING | \>\< | msdyn\_invoiceupdate
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_enablepostdatescheckclearingposting
BILLOFEXCHANGEDRAFTTYPE | \>\< | msdyn\_billofexchangedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

## <a name="loyalty-cards"></a>Lojalumo kortelės

Šis šablonas sinchronizuoja klientų lojalumo kortelių informaciją tarp „Finance and Operations“ ir „Customer Engagement“.

<!-- ![](media/dual-write-loyalty-cards.png) -->

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
CARDNUMBER | = | msdyn\_cardnumber
CARDTENDERTYPE | \>\< | msdyn\_cardtendertype
PARTYNUMBER | = | msdyn\_partynumber
REPLACEMENTCARDNUMBER | \> | msdyn\_replacementcardnumber
OMOPERATINGUNITNUMBER | = | msdyn\_operatingunitnumber
LOYALTYENROLLMENTDATE | = | msdyn\_enrollmentdate

## <a name="payment-schedules"></a>Mokėjimo grafikai

Šis šablonas sinchronizuoja klientų ir tiekėjų mokėjimo grafiko nuorodos duomenis tarp „Finance and Operations“ ir „Customer Engagement“.

<!-- ![](media/dual-write-payment-schedules.png) -->

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
PAVADINIMAS | = | msdyn\_name
APRAŠAS | = | msdyn\_description
ALLOCATIONMETHOD | \>\< | msdyn\_allocationmethod
PAYMENTFREQUENCYUNITS | \>\< | msdyn\_paymentfrequencyunit
PAYMENTFREQUENCY | = | msdyn\_paymentfrequency
NUMBEROFPAYMENTS | = | msdyn\_numberofpayments
FIXEDPAYMENTAMOUNT | = | msdyn\_fixedpaymentamount
MINIMUMPAYMENTAMOUNT | = | msdyn\_minimumpaymentamount
SALESTAXALLOCATIONMETHOD | \>\< | msdyn\_salestaxallocationmethod
PASTABOS | = | msdyn\_note

## <a name="payment-schedule-lines"></a>Mokėjimo grafiko eilutės

Sinchronizuoja klientų ir tiekėjų mokėjimo grafiko eilučių nuorodos duomenis tarp „Finance and Operations“ ir „Customer Engagement“.

<!-- ![](media/dual-write-payment-schedule-lines.png) -->

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTSCHEDULENAME | \> | msdyn\_name
LINENUMBER | = | msdyn\_linenumber
PERIODSAFTERDUEDATE | = | msdyn\_periodsafterduedate
PERCENTORAMOUNT | \>\< | msdyn\_percentoramount
PERCENTORAMOUNTVALUE | = | msdyn\_percentoramountvalue

## <a name="payment-days"></a>Mokėjimo dienos

Šis šablonas sinchronizuoja klientų ir tiekėjų mokėjimo dienų nuorodos duomenis tarp „Finance and Operations“ ir „Customer Engagement“.

<!-- ![](media/dual-write-payment-days.png) -->

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
PAVADINIMAS | = | msdyn\_name
APRAŠAS | = | msdyn\_description

## <a name="payment-day-lines"></a>Mokėjimo dienų eilutės

Šis šablonas sinchronizuoja klientų ir tiekėjų mokėjimo dienų eilučių nuorodos duomenis tarp „Finance and Operations“ ir „Customer Engagement“.

<!-- ![](media/dual-write-payment-day-lines.png) -->

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
CDSINTEGRATIONKEY | = | msdyn\_paymentdaylineid
FREQUENCY | \>\< | msdyn\_frequency
DAYOFWEEK | \>\< | msdyn\_dayofweek
DAYOFMONTH | = | msdyn\_dayofmonth
PAVADINIMAS | = | msdyn\_paymentday.msdyn\_name

## <a name="payment-terms"></a>Mokėjimo sąlygos

Šis šablonas sinchronizuoja klientų ir tiekėjų mokėjimo terminų (mokėjimo terminai) nuorodos duomenis tarp „Finance and Operations“ ir „Customer Engagement“.

<!-- ![](media/dual-write-payment-terms.png) -->

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
APRAŠAS | = | msdyn\_description
PAVADINIMAS | = | msdyn\_name
NUMBEROFMONTHS | = | msdyn\_numberofmonth
CUTOFFDAYOFMONTH | = | msdyn\_cutoffdayofmonth
ISCASHPAYMENT | \>\< | msdyn\_iscashpayment
NUMBEROFDAYS | = | msdyn\_days
ISCERTIFIEDCOMPANYCHECK | \>\< | msdyn\_iscertifiedcompanycheck
ISDEFAULTPAYMENTTERM | \>\< | msdyn\_isdefaultpaymentterm
CREDITCARDPAYMENTTYPE | \>\< | msdyn\_creditcardpaymenttype
CREDITCARDCREDITCHECKTYPE | \>\< | msdyn\_creditcardcreditchecktype
PAYMENTDAYNAME | = | msdyn\_paymentdayname.msdyn\_name
PAYMENTMETHODTYPE | \>\< | msdyn\_paymentmethodtype
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedulename.msdyn\_name

## <a name="name-affixes"></a>Pavadinimo afiksai

Šis šablonas sinchronizuoja klientų ir tiekėjų pavadinimo afiksų nuorodos duomenis tarp „Finance and Operations“ ir „Customer Engagement“.

<!-- ![](media/dual-write-name-affixes.png) -->

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
AFFIX | = | msdyn\_affix
TIPAS | \>\< | msdyn\_affixtype
APRAŠAS | = | msdyn\_description
