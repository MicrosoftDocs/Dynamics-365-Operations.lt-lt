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
ms.openlocfilehash: 09d985e5c6816ec0c718aaf418f4e85fb828f1c6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769688"
---
# <a name="integrated-customer-master"></a>Bendrieji integruoto kliento duomenys

[!include [banner](../includes/banner.md)]

Klientų įrašai paprastai naudojami daugiau negu vienoje programoje. Pavyzdžiui, pardavimo veikla gali pateikti komercinio kliento įrašus per „Sales” programą, o el. prekybos ar mažmeninės prekybos pardavimas gali pateikti kliento įrašus per „Finance and Operations” programą. Neatsižvelgiant į kliento įrašo kilmę, jis integruojamas fone už programų ribų ir infrastruktūros skirtumų. Integruoto kliento bendrieji duomenys padeda atlikti bendrųjų duomenų įsisavinimo scenarijus ir teikia išsamų kliento vaizdą „Dynamics 365“ programų pakete.

## <a name="customer-data-flow"></a>Kliento duomenų srautas

*Klientas* yra aiškiai apibrėžta koncepcija programose. Todėl kliento duomenų integravimas yra susijęs su klientų koncepcijos harmonizavimu tarp dviejų programų. Tolesnėje iliustracijoje pateiktas kliento duomenų srautas.

![Kliento duomenų srautas](media/dual-write-customer-data-flow.png)

Klientai gali būti suskirstyti į du tipus: komerciniai/organizaciniai klientai ir vartotojai/galutiniai vartotojai. Šie du klientų tipai „Finance and Operations“ ir Common Data Service yra saugomi ir tvarkomi skirtingai.

„Finance and Operations“ tiek komercinių/organizacinių klientų, tiek vartotojų/galutinių vartotojų duomenys naudojami vienoje lentelėje, pavadintoje **CustTable** (CustomerCustomerV3Entity), ir jie klasifikuojami pagal atributą **Tipas**. (Jei **Tipas** nustatytas kaip **Organizacija**, klientas yra komercinis/organizacinis klientas, o jei **Tipas** nustatytas kaip **Asmuo**, klientas yra vartotojas/galutinis vartotojas.) Pagrindinio kontaktinio asmens informacija tvarkoma naudojant objektą SMMContactPersonEntity.

Common Data Service komercinių/organizacinių klientų duomenys tvarkomi objekte Sąskaita ir jie yra identifikuojami kaip klientai, kai atributas **RelationshipType** yra nustatytas į **Klientas**. Tiek vartotojus/galutinius vartotojus, tiek kontaktinius asmenis atstovauja objektas Kontaktas. Siekiant aiškiai atskirti vartotoją/galutinį vartotoją ir kontaktinį asmenį, objekte **Kontaktas** yra Bulio logikos žymė, pavadinta **Pardavimas**. Jeigu **Pardavimas** yra **Teisinga**, kontaktas yra vartotojas/galutinis vartotojas, ir tam užsakymui gali būti kuriami pasiūlymai ir užsakymai. Kai **Pardavimas** yra **Klaidinga**, kontaktas yra tik pirminis kliento kontaktinis asmuo.

Jeigu pasiūlyme ar užsakymo procese dalyvauja ne pardavimo kontaktas, **Pardavimas** nustatomas į **Teisinga**, kad kontaktas būtų pažymėtas kaip pardavimo kontaktas. Kontaktas, kuris tapo pardavimo kontaktu, lieka pardavimo kontaktu.

## <a name="templates"></a>Šablonai

Kliento duomenys apima visą informaciją apie klientą, pvz., klientų grupę, adresus, kontaktinę informaciją, mokėjimo profilį, sąskaitos faktūros profilį ir lojalumo būseną. Objektų susiejimų rinkinys veikia kartu atliekant kliento duomenų sąveiką, kaip parodyta tolesnėje lentelėje.

„Finance and Operations” programos | Kitos „Dynamics 365” programos         | Aprašymas
----------------------------|---------------------------------|------------
CDS kontaktai V2             | kontaktai                        | Naudojant šį šabloną sinchronizuojama visa tiek klientų, tiek tiekėjų pirminė, antrinė ir tretinė kontaktinė informacija.
Klientų grupės             | msdyn_customergroups            | Naudojant šį šabloną sinchronizuojama klientų grupių informacija.
Kliento mokėjimo būdas     | msdyn_customerpaymentmethods    | Naudojant šį šabloną sinchronizuojama klientų mokėjimo būdų informacija.
Klientai V3                | sąskaitos                        | Naudojant šį šabloną sinchronizuojama komercinių ir organizacijos klientų bendroji informacija.
Klientai V3                | kontaktai                        | Naudojant šį šabloną sinchronizuojmi vartotojų ir galutinių vartotojų klientų bendrieji duomenys.
Lojalumo kortelė                | msdyn_loyaltycards              | Naudojant šį šabloną sinchronizuojama klientų lojalumo kortelių informacija.
Pavadinimo afiksai                | msdyn_nameaffixes               | Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų pavadinimų afiksų nuorodos duomenys.
Mokėjimo dienos eilutės CDS V2    | msdyn_paymentdaylines           | Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo dienų eilučių nuorodos duomenys.
Mokėjimo dienos CDS            | msdyn_paymentdays               | Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo dienų nuorodos duomenys.
Mokėjimo grafiko eilutės      | msdyn_paymentschedulelines      | Sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo grafikų eilučių nuorodos duomenys.
Mokėjimo grafikas            | msdyn_paymentschedules          | Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo grafikų nuorodos duomenys.
Mokėjimo sąlygos            | msdyn_paymentterms              | Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo sąlygų nuorodos duomenys.

[!include [banner](../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](dual-write/CDSContactsV2-contacts.md)]

[!include [mapping customer group](dual-write/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](dual-write/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](dual-write/CustomersV3-accounts.md)]

[!include [mapping customer contacts](dual-write/CustomersV3-contacts.md)]

[!include [mapping loyalty card](dual-write/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](dual-write/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](dual-write/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](dual-write/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](dual-write/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](dual-write/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](dual-write/TermsofPayment-msdyn-paymentterms.md)]
