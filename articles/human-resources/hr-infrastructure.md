---
title: Dynamics 365 Human Resources infrastruktūros suliejimas – išleisti 10.0.25 atnaujinimą
description: Šioje temoje pateikiama informacija apie Microsoft Dynamics 365 Human Resources leidimą nr. 10.0.25, dėl kurio infrastruktūros suliejimas sukuria pirmąją pajėgumų bangą.
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
ms.openlocfilehash: 9d574f760960241e4d79a988b1b671f224cb345f
ms.sourcegitcommit: 6f6ec4f4ff595bf81f0b8b83f66442d5456efa87
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/25/2022
ms.locfileid: "8487800"
---
# <a name="dynamics-365-human-resources-infrastructure-merge---release-10025-update"></a>Dynamics 365 Human Resources infrastruktūros suliejimas – išleisti 10.0.25 atnaujinimą

10.0.25 paleidimas sukuria pirmąją pajėgumų bangą infrastruktūros struktūroje. Atliekant infrastruktūros suliejimą Microsoft Dynamics 365 Human Resources bus sulieta su finansų ir operacijų infrastruktūra. Tačiau ji ir toliau bus licencijuota kaip nepriklausoma programa, pvz.Dynamics 365 Finance, ir Dynamics 365 Supply Chain Management. Daugiau informacijos apie infrastruktūros suliejimą rasite infrastruktūros suliejimo [Dynamics 365 Human Resources DUK](../human-resources/hr-infrastructure-merge-faq.md).

Sulieti personalo vartotojai bus pastovūs šiais būdais:

- [Aplinkos valdymas ir integravimas yra nuoseklūs personalo ir finansų bei operacijų programėlių.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/consistent-environment-management-integrations-between-human-resources-finance-operations-apps)

    - Valdykite aplinkas Microsoft Dynamics ciklo tarnybose, problemų iešką ir Regression Suite Automation Tool.
    - Yra vienas kodo pagrindas, kuriame naujos personalo funkcijos paleidžiamos kaip įprasto vienos versijos atnaujinimo proceso dalis.
    - Būdas, kuriuo naujiniai, naujinimai ir karštosios pataisos taikomos aplinkose, yra nuoseklios.

- [Patobulintos extensibility pasirinktys.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/improve-extensibility-options)

    - Jei reikia, galite toliau Microsoft Power Platform naudoti įrankius, kad pratęstumėte.
    - Funkcijas galima išplėsti naudojant formas, lenteles, metodus ir programos programavimo sąsajas (API).
    - Galite kurti ir išplėsti objektus.

    Daugiau informacijos apie galimas plėtinio pasirinktis [ieškokite "Dynamics 365" išplėtimo peržiūra](../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md).

- [Sukurkite vieną personalo galimybių rinkinį programoje "Dynamics 365".](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/create-one-set-human-resources-capabilities-within-dynamics-365)

    Leidime 10.0.25 funkcinės galimybės, kurios egzistuoja tik personalo srityje, buvo prieinamos finansų ir operacijų infrastruktūrai. Kad klientai galėtų pasinaudoti šiomis galimybėmis finansų ir operacijų aplinkoje, funkcijų valdymas turi įgalinti šias personalo funkcijas.

    | Funkcijos pavadinimas | Apžvalga | Išleidimo būsena | 
    |--------------|----------|----------------| 
    | Tarnybos metų skaičiavimas | Nustatymo parinktis leidžia pasirinkti datą, kuri naudojama paslaugos **skaičiavimo** metams. | Bendrai prieinama | 
    | Darbo eigos patirties patobulinimai | Ši funkcija užtikrina patobulintą vartotojų darbo eigos pateikimo ir patvirtinimų patirtį. | Bendrai prieinama | 
    | Spausdinti našumo apžvalgas | Našumo peržiūras galite išspausdinti PDF formatu. | Bendrai prieinama | 
    | Pasirinktiniai saitai tvarkytuvo **savitarnoje** | Galite kurti pasirinktinius saitus, rodomus Vadybininko **savitarnos** skyriuje **Susiję saitai**. | Bendrai prieinama | 
    | Kryžminės bendrovės kompensavimo peržiūra | Vartotojai gali peržiūrėti kompensavimo planus vadybininko **savitarnoje** tarp visų juridinių subjektų ir neįjungdami įmonių. | Bendrai prieinama | 
    | Konfigūruoti keletą kompensavimo lygių pagal užduotį\*&dagger; | Užduotys dabar palaiko keletą atlyginimo lygių. | Peržiūros versija | 
    | Užduočių valdymas\* | Galite sukurti kontrolinius sąrašus ir užduotis, skirtas inžine ir perėjimo procesams. | Peržiūros versija | 
    | Supaprastintas darbuotojo duomenų įvedimas | Ši funkcija pateikia atnaujintą vartotojo patirtį esamame darbuotojo **puslapyje**. | Peržiūros versija | 
    | Žmogiškųjų išteklių vartotojų patirties patobulinimai | Žr. lentelę kitame skyriuje.  | Peržiūros versija | 

\* Šią funkciją reikia įjungti prieš personalo vartotojų **patirties patobulinimo funkciją**.

&dagger; Įgalinus šią funkciją jos išjungti negalima.

## <a name="human-resource-user-experience-enhancements"></a>Personalo vartotojo patirties patobulinimai

| Funkcijos pavadinimas | Apžvalga | 
|--------------|----------| 
| Panaikinti įdarbinimą | Galite panaikinti darbuotojo įdarbinimtį. | 
| Užduočių šeimos | Galite sekti užduočių, kurios apima panašų darbą ir kurioms reikia panašios mokymo, įgūdžių, žinių ir kompetencijos, grupę. | 
| Papildomi įdarbinimo laukai | Įtraukti šie laukai: Įdarbinimo **kategorija**, **Įdarbinimo tipas** ir **Įdarbinimo būsena**. | 
| **Darbuotojų be įdarbinimo** puslapis | Puslapyje rodomas darbuotojų, kurie neturi įdarbinimo įrašo, sąrašas. | 
| Pareigų dimensijos vartotojo patirties atnaujinimas | Yra patobulintos vartotojo patirties priskiriant pareigų dimensijas juridiniam subjektui. | 
| Adreso keitimai personalo **valdymo darbo** srityje | Ši funkcija pateikia visų adreso pakeitimų, kurie įvyko per nurodytą dienų skaičių, skaičių, kaip nurodyta **personalo parametrų** puslapyje. | 
| Galintys galioti įrašai personalo **valdymo darbo** srityje | Ši funkcija pateikia prekių, kurių galiojimo laikas baigėsi arba baigiasi sertifikatų, identifikavimo duomenų, bandomojų bandymų, atrankos ar bandymų galiojimą, sąrašą. | 
| **Pareigų hierarchijos tikrinimo** puslapis | Ciklinių nuorodų tikrinimas atliekamas pareigų eilučių hierarchijoje. | 
| Šaliai būsūs atlyginimų informacija | Papildomus algalapio laukus galima rasti darbuotojo **įdarbinimo** puslapyje, atsižvelgiant į juridinio subjekto, kuriame darbuotojai dirba, šalį arba regioną. | 
| Atitikimo ataskaitų patobulinimai | Galimos papildomos ataskaitų pasirinktys, galimos EEO-1, Vets 4212 ir OSHA300a. | 
| Personalo valdymo **darbo srities** atnaujinimai | Buvo atnaujinti adreso keitimai ir besibaigintys įrašai. Be to, naujuose skirtukuose pateikiamas darbuotojo ir pareigų veiksmų sąrašas. | 
