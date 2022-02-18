---
title: Dynamics 365 Human Resources infrastruktūros sujungimas – 10.0.25 versijos naujinimas
description: Šioje temoje pateikiama informacija apie „Microsoft“.Dynamics 365 Human Resources leidimas 10.0.25, kuris atneša pirmąją infrastruktūros sujungimo galimybių bangą.
author: twheeloc
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a80bedd0224f1e31dfec4e9f4c39ad1ed75d7f2f
ms.sourcegitcommit: 948978183a1da949e35585b28b8e85a63b6c12b1
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/25/2022
ms.locfileid: "8024572"
---
# <a name="dynamics-365-human-resources-infrastructure-merge---release-10025-update"></a>Dynamics 365 Human Resources infrastruktūros sujungimas – 10.0.25 versijos naujinimas

10.0.25 leidimas atneša pirmąją infrastruktūros sujungimo galimybių bangą. Infrastruktūros sujungimo metu „Microsoft“.Dynamics 365 Human Resources bus sujungta su „Finance and Operations“ infrastruktūra. Tačiau ji ir toliau bus licencijuojama kaip nepriklausoma programa, pvz Dynamics 365 Finance ir Dynamics 365 Supply Chain Management. Daugiau informacijos apie infrastruktūros sujungimą žr [Dynamics 365 Human Resources infrastruktūros sujungimo DUK](../human-resources/hr-infrastructure-merge-faq.md).

Sujungimas užtikrins nuoseklumą žmogiškųjų išteklių vartotojams šiais būdais:

- [Aplinkos valdymas ir integracijos yra suderinamos tarp žmogiškųjų išteklių ir finansų bei operacijų programų.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/consistent-environment-management-integrations-between-human-resources-finance-operations-apps)

    - Tvarkykite aplinką Microsoft Dynamics Gyvenimo ciklo paslaugos, problemų paieška ir Regression Suite Automation Tool.
    - Yra viena kodo bazė, kurioje išleidžiamos naujos žmogiškųjų išteklių funkcijos kaip įprasto vienos versijos atnaujinimo proceso dalis.
    - Aplinkoms taikomi naujinimai, naujinimai ir karštosios pataisos yra nuoseklūs.

- [Patobulintos išplėtimo galimybės.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/improve-extensibility-options.md)

    - Galite ir toliau naudoti Microsoft Power Platform įrankius pratęsti pagal poreikį.
    - Funkcionalumą galite išplėsti naudodami formas, lenteles, metodus ir taikomųjų programų sąsajas (API).
    - Galite kurti ir išplėsti objektus.

    Norėdami gauti daugiau informacijos apie galimas plėtinio parinktis, žr [„Dynamics 365“ išplėtimo apžvalga](../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md).

- [Sukurkite vieną žmogiškųjų išteklių galimybių rinkinį „Dynamics 365“.](/dynamics365-release-plan/2021wave2/human-resources/create-one-set-human-resources-capabilities-within-dynamics-365.md)

    10.0.25 versijoje „Finance and Operations“ infrastruktūroje buvo prieinamos funkcinės galimybės, kurios buvo tik žmogiškųjų išteklių skyriuje. Kad klientai galėtų pasinaudoti šiomis galimybėmis „Finance and Operations“ aplinkoje, funkcijų valdyme turi būti įgalintos toliau nurodytos žmogiškųjų išteklių funkcijos.

    | Funkcijos pavadinimas | Apžvalga | Išleidimo būsena | 
    |--------------|----------|----------------| 
    | Tarnybos metų skaičiavimas | Sąrankos parinktis leidžia pasirinkti datą, kuri bus naudojama **Tarnavimo metai** skaičiavimas. | Bendrai prieinama | 
    | Darbo eigos patirties patobulinimai | Ši funkcija suteikia geresnę vartotojo patirtį teikiant darbo eigos pateikimą ir patvirtinimą. | Bendrai prieinama | 
    | Spausdinti našumo apžvalgas | Galite atspausdinti veiklos apžvalgas PDF formatu. | Bendrai prieinama | 
    | Priskirtos nuorodos **Vadovo savitarna** | Galite sukurti pasirinktines nuorodas, kurios bus rodomos **Susijusios nuorodos** skyrių **Vadovo savitarna**. | Bendrai prieinama | 
    | Kryžminės bendrovės kompensavimo peržiūra | Vartotojai gali peržiūrėti kompensavimo planus **Vadovo savitarna** visiems juridiniams asmenims, nekeičiant įmonės. | Bendrai prieinama | 
    | Sukonfigūruokite kelis kompensavimo lygius pagal darbą\*&dagger; | Darbai dabar palaiko kelis atlyginimo lygius. | Peržiūra | 
    | Užduočių valdymas\* | Galite sukurti kontrolinius sąrašus ir užduotis, skirtus įtraukimo, išjungimo ir perėjimo procesui. | Peržiūra | 
    | Supaprastintas darbuotojo duomenų įvedimas | Ši funkcija suteikia atnaujintą esamą vartotojo patirtį **Darbininkas** puslapį. | Peržiūra | 
    | Žmogiškųjų išteklių vartotojų patirties patobulinimai | Žr. lentelę kitame skyriuje.  | Peržiūra | 

\* Ši funkcija turi būti įjungta prieš **Žmogiškųjų išteklių vartotojo patirties patobulinimai** funkcija.

&dagger; Šios funkcijos negalima išjungti, kai ji įjungta.

## <a name="human-resource-user-experience-enhancements"></a>Žmogiškųjų išteklių vartotojo patirties patobulinimai

| Funkcijos pavadinimas | Apžvalga | 
|--------------|----------| 
| Panaikinti įdarbinimą | Galite ištrinti darbuotojo įdarbinimą. | 
| Darbo šeimos | Galite stebėti darbų grupę, kuri apima panašų darbą ir reikalauja panašaus mokymo, įgūdžių, žinių ir patirties. | 
| Papildomos darbo sritys | Buvo pridėti šie laukai: **Užimtumo kategorija**, **tipas**, ir **Užimtumo statusas**. | 
| **Darbuotojai be darbo** puslapį | Puslapyje rodomas darbuotojų, kurie neturi darbo įrašo, sąrašas. | 
| Pozicijos dimensijos naudotojo patirties atnaujinimas | Yra patobulinta naudotojo patirtis priskiriant pozicijų matmenis vienam juridiniam asmeniui. | 
| Adresas pasikeitė **Personalo valdymas** darbo vieta | Ši funkcija pateikia visų adresų pakeitimų, įvykusių per nurodytą dienų skaičių, kaip apibrėžta **Žmogiškųjų išteklių parametrai** puslapį. | 
| Baigia galioti įrašai **Personalo valdymas** darbo vieta | Ši funkcija pateikia sąrašą elementų, kurių galiojimas pasibaigė arba baigsis sertifikatų, tapatybės nustatymo, bandomųjų terminų, patikrinimų ar testų galiojimo laikui. | 
| **Pozicijos hierarchijos patvirtinimas** puslapį | Patikrinama, ar nėra apskritų nuorodų padėties eilutės hierarchijoje. | 
| Konkrečios šalies darbo užmokesčio informacija | Papildomi darbo užmokesčio laukai yra prieinami **Darbuotojo užimtumas** puslapyje, priklausomai nuo juridinio asmens, kuriame dirba darbuotojai, šalies ar regiono. | 
| Atitikties ataskaitų teikimo patobulinimai | Galimos papildomos ataskaitų teikimo parinktys, skirtos EEO-1, Vets 4212 ir OSHA300a. | 
| Atnaujinimai **Personalo valdymas** darbo vieta | Buvo atlikti atnaujinimai, siekiant sekti adresų pasikeitimus ir pasibaigiančius įrašus. Be to, naujuose skirtukuose pateikiami darbuotojų ir pareigų veiksmai. | 
