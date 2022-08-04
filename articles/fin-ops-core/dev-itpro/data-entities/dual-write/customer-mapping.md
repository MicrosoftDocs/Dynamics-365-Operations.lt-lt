---
title: Bendrieji integruoto kliento duomenys
description: Šiame straipsnyje aprašomas kliento duomenų integravimas tarp finansų ir operacijų bei Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 1b16eab5c107a3176f0890372d397947698e71de
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111731"
---
# <a name="integrated-customer-master"></a>Bendrieji integruoto kliento duomenys

[!include [banner](../../includes/banner.md)]



Kliento duomenys gali būti tvarkomi daugiau nei vienoje „Dynamics 365” programoje. Pavyzdžiui, kliento eilutė gali būti sukurta naudojant pardavimo veiklą „Dynamics 365 Sales“ programoje („Customer Engagement“ programoje) arba eilutė gali būti sukurta naudojant mažmeninės prekybos veiklą „Dynamics 365 Commerce” programoje („Finance and Operations” programoje). Neatsižvelgiant į tai, kur paimti kliento duomenys, jie integruojami fone. Integruotas kliento šablonas suteikia lankstumo tvarkant kliento duomenis programoje „Dynamics 365“ ir teikia išsamų kliento vaizdą „Dynamics 365“ programų pakete.

## <a name="customer-data-flow"></a>Kliento duomenų srautas

*Klientas* yra aiškiai apibrėžta koncepcija programose. Todėl kliento duomenų integravimas yra susijęs su klientų koncepcijos harmonizavimu tarp dviejų programų. Tolesnėje iliustracijoje pateiktas kliento duomenų srautas.

![Kliento duomenų srautas.](media/dual-write-customer-data-flow.png)

Klientai gali būti suskirstyti į du tipus: komerciniai/organizaciniai klientai ir vartotojai/galutiniai vartotojai. Šie du klientų tipai yra saugomi ir kitaip tvarkomi finansų ir operacijų metu ir Dataverse.

Finansinėse ir operacijose tiek komerciniai / **organizacijos klientai, tiek vartotojai / galutiniai vartotojai yra suskirstyti į vieną lentelę, kuri vadinama CustTable** (CustCustomerV3Entity), **ir** jie yra klasifikuojami pagal atributą Tipas. (Jei **Tipas** nustatytas kaip **Organizacija**, klientas yra komercinis/organizacinis klientas, o jei **Tipas** nustatytas kaip **Asmuo**, klientas yra vartotojas/galutinis vartotojas.) Pagrindinio kontaktinio asmens informacija tvarkoma naudojant lentelę „SMMContactPersonEntity”.

„Dataverse” komercinių/organizacinių klientų duomenys tvarkomi lentelėje Sąskaita ir jie yra identifikuojami kaip klientai, kai atributas **„RelationshipType”** yra nustatytas į **Klientas**. Tiek vartotojus/galutinius vartotojus, tiek kontaktinius asmenis atstovauja lentelė Kontaktas. Siekiant aiškiai atskirti vartotoją/galutinį vartotoją ir kontaktinį asmenį, lentelėje **Kontaktas** yra Bulio logikos žymė, pavadinta **Pardavimas**. Jeigu **Pardavimas** yra **Teisinga**, kontaktas yra vartotojas/galutinis vartotojas, ir tam užsakymui gali būti kuriami pasiūlymai ir užsakymai. Kai **Pardavimas** yra **Klaidinga**, kontaktas yra tik pirminis kliento kontaktinis asmuo.

Jeigu pasiūlyme ar užsakymo procese dalyvauja ne pardavimo kontaktas, **Pardavimas** nustatomas į **Teisinga**, kad kontaktas būtų pažymėtas kaip pardavimo kontaktas. Kontaktas, kuris tapo pardavimo kontaktu, lieka pardavimo kontaktu.

## <a name="templates"></a>Šablonai

Kliento duomenys apima visą informaciją apie klientą, pvz., klientų grupę, adresus, kontaktinę informaciją, mokėjimo profilį, sąskaitos faktūros profilį ir lojalumo būseną. Lentelių susiejimų rinkinys veikia kartu atliekant kliento duomenų sąveiką, kaip parodyta tolesnėje lentelėje.

„Finance and operations” programos | „Customer engagement“ programos         | Aprašas
----------------------------|---------------------------------|------------
[CDS kontaktai V2](mapping-reference.md#115) | kontaktai | Naudojant šį šabloną sinchronizuojama visa tiek klientų, tiek tiekėjų pirminė, antrinė ir tretinė kontaktinė informacija.
[Klientų grupės](mapping-reference.md#126) | msdyn_customergroups | Naudojant šį šabloną sinchronizuojama klientų grupių informacija.
[Kliento mokėjimo būdas](mapping-reference.md#127) | msdyn_customerpaymentmethods | Naudojant šį šabloną sinchronizuojama klientų mokėjimo būdų informacija.
[Klientai V3](mapping-reference.md#101) | sąskaitos | Naudojant šį šabloną sinchronizuojama komercinių ir organizacijos klientų bendroji informacija.
[Klientai V3](mapping-reference.md#116) | kontaktai | Naudojant šį šabloną sinchronizuojmi vartotojų ir galutinių vartotojų klientų bendrieji duomenys.
[Pavadinimo afiksai](mapping-reference.md#155) | msdyn_nameaffixes | Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų pavadinimų afiksų nuorodos duomenys.
[Mokėjimo dienos eilutės CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo dienų eilučių nuorodos duomenys.
[Mokėjimo dienos CDS](mapping-reference.md#158) | msdyn_paymentdays | Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo dienų nuorodos duomenys.
[Mokėjimo grafiko eilutės](mapping-reference.md#159) | msdyn_paymentschedulelines | Sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo grafikų eilučių nuorodos duomenys.
[Mokėjimo grafikas](mapping-reference.md#160) | msdyn_paymentschedules | Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo grafikų nuorodos duomenys.
[Mokėjimo sąlygos](mapping-reference.md#161) | msdyn_paymentterms | Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo sąlygų nuorodos duomenys.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

