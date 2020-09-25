---
title: Bendrieji integruoto kliento duomenys
description: Šioje temoje aprašomas klientų duomenų integravimas tarp „Finance and Operations“ ir „Common Data Service“.
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
ms.openlocfilehash: 5643be99ac2c58f4da1a2a068e84bf526f8575cb
ms.sourcegitcommit: 164de749f394a133f223c526aa0c46bf922d1ea8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/04/2020
ms.locfileid: "3770017"
---
# <a name="integrated-customer-master"></a>Bendrieji integruoto kliento duomenys

[!include [banner](../../includes/banner.md)]


Kliento duomenys gali būti tvarkomi daugiau nei vienoje „Dynamics 365” programoje. Pavyzdžiui, kliento įrašas gali būti sukurtas naudojant pardavimo veiklą programoje „Dynamics 365 Sales“ (modeliu pagrįstoje „Dynamics 365“ programoje) arba įrašas gali būti sukurtas naudojant mažmeninės prekybos veiklą programoje „Dynamics 365 Commerce” („Finance and Operations” programoje). Neatsižvelgiant į tai, kur paimti kliento duomenys, jie integruojami fone. Integruotas kliento šablonas suteikia lankstumo tvarkant kliento duomenis programoje „Dynamics 365“ ir teikia išsamų kliento vaizdą „Dynamics 365“ programų pakete.

## <a name="customer-data-flow"></a>Kliento duomenų srautas

*Klientas* yra aiškiai apibrėžta koncepcija programose. Todėl kliento duomenų integravimas yra susijęs su klientų koncepcijos harmonizavimu tarp dviejų programų. Tolesnėje iliustracijoje pateiktas kliento duomenų srautas.

![Kliento duomenų srautas](media/dual-write-customer-data-flow.png)

Klientai gali būti suskirstyti į du tipus: komerciniai/organizaciniai klientai ir vartotojai/galutiniai vartotojai. Šie du klientų tipai „Finance and Operations“ ir „Common Data Service“ yra saugomi ir tvarkomi skirtingai.

„Finance and Operations“ tiek komercinių / organizacinių klientų, tiek vartotojų / galutinių vartotojų duomenys naudojami vienoje lentelėje, pavadintoje **CustTable** (CustCustomerV3Entity), ir jie klasifikuojami pagal atributą **Tipas**. (Jei **Tipas** nustatytas kaip **Organizacija**, klientas yra komercinis/organizacinis klientas, o jei **Tipas** nustatytas kaip **Asmuo**, klientas yra vartotojas/galutinis vartotojas.) Pagrindinio kontaktinio asmens informacija tvarkoma naudojant objektą SMMContactPersonEntity.

Common Data Service komercinių/organizacinių klientų duomenys tvarkomi objekte Sąskaita ir jie yra identifikuojami kaip klientai, kai atributas **RelationshipType** yra nustatytas į **Klientas**. Tiek vartotojus/galutinius vartotojus, tiek kontaktinius asmenis atstovauja objektas Kontaktas. Siekiant aiškiai atskirti vartotoją/galutinį vartotoją ir kontaktinį asmenį, objekte **Kontaktas** yra Bulio logikos žymė, pavadinta **Pardavimas**. Jeigu **Pardavimas** yra **Teisinga**, kontaktas yra vartotojas/galutinis vartotojas, ir tam užsakymui gali būti kuriami pasiūlymai ir užsakymai. Kai **Pardavimas** yra **Klaidinga**, kontaktas yra tik pirminis kliento kontaktinis asmuo.

Jeigu pasiūlyme ar užsakymo procese dalyvauja ne pardavimo kontaktas, **Pardavimas** nustatomas į **Teisinga**, kad kontaktas būtų pažymėtas kaip pardavimo kontaktas. Kontaktas, kuris tapo pardavimo kontaktu, lieka pardavimo kontaktu.

## <a name="templates"></a>Šablonai

Kliento duomenys apima visą informaciją apie klientą, pvz., klientų grupę, adresus, kontaktinę informaciją, mokėjimo profilį, sąskaitos faktūros profilį ir lojalumo būseną. Objektų susiejimų rinkinys veikia kartu atliekant kliento duomenų sąveiką, kaip parodyta tolesnėje lentelėje.

„Finance and Operations” programėlės | Kitos „Dynamics 365” programos         | Aprašymas
----------------------------|---------------------------------|------------
CDS kontaktai V2             | kontaktai                        | Naudojant šį šabloną sinchronizuojama visa tiek klientų, tiek tiekėjų pirminė, antrinė ir tretinė kontaktinė informacija.
Klientų grupės             | msdyn_customergroups            | Naudojant šį šabloną sinchronizuojama klientų grupių informacija.
Kliento mokėjimo būdas     | msdyn_customerpaymentmethods    | Naudojant šį šabloną sinchronizuojama klientų mokėjimo būdų informacija.
Klientai V3                | sąskaitos                        | Naudojant šį šabloną sinchronizuojama komercinių ir organizacijos klientų bendroji informacija.
Klientai V3                | kontaktai                        | Naudojant šį šabloną sinchronizuojmi vartotojų ir galutinių vartotojų klientų bendrieji duomenys.
Pavadinimo afiksai                | msdyn_nameaffixes               | Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų pavadinimų afiksų nuorodos duomenys.
Mokėjimo dienos eilutės CDS V2    | msdyn_paymentdaylines           | Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo dienų eilučių nuorodos duomenys.
Mokėjimo dienos CDS            | msdyn_paymentdays               | Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo dienų nuorodos duomenys.
Mokėjimo grafiko eilutės      | msdyn_paymentschedulelines      | Sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo grafikų eilučių nuorodos duomenys.
Mokėjimo grafikas            | msdyn_paymentschedules          | Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo grafikų nuorodos duomenys.
Mokėjimo sąlygos            | msdyn_paymentterms              | Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo sąlygų nuorodos duomenys.

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
