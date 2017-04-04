---
title: "Finansinės dimensijos"
description: "Šiame straipsnyje paaiškinami skirtingi finansinių dimensijų tipai ir tai, kaip jie nustatomi."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25871
ms.assetid: af54621c-c8be-4b72-b6df-dcf886c40ce4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: f849b98cac88d182875aca88aaf04cd3575ed99f
ms.lasthandoff: 03/31/2017


---

# <a name="financial-dimensions"></a>Finansinės dimensijos

Šiame straipsnyje paaiškinami skirtingi finansinių dimensijų tipai ir tai, kaip jie nustatomi.

Naudokite puslapį Finansinės dimensijos kurdami finansines dimensijas, kurias galite naudoti kaip sąskaitų planų sąskaitos segmentus. Yra dviejų tipų finansinės dimensijos: pasirinktinės dimensijos ir objekto remiamos dimensijos. Pasirinktinės dimensijos yra bendrai naudojamos juridinių subjektų, o vertes įveda ir tvarko vartotojas. Objekto remiamos dimensijos yra dimensijos, kurių vertės nurodomos kitur sistemoje, pvz., dalyse Klientai ar Parduotuvės. Kai kurios objekto remiamos dimensijos yra bendrai naudojamos keliuose juridiniuose subjektuose, o kai kurios būdingos konkrečiai įmonei. 

Sukūrę finansines dimensijas, naudokite puslapį Finansinių dimensijų reikšmės, kad kiekvienai finansinei dimensijai priskirtumėte papildomų ypatybių. 

Atstovauti juridiniai asmenys nesukuriant teisės subjektai Microsoft Dynamics 365 operacijoms gali naudoti finansinės dimensijos, finansinės dimensijos nepritaikytos spręsti veiklos ar verslo poreikius juridinių asmenų. Interunit apskaitos funkcionalumą Microsoft Dynamics 365 operacijoms yra skirtos spręsti tik apskaitos įrašai, kurios kuriamos pagal kiekvieną sandorį. 

Prieš nustatydami finansines dimensijas kaip juridinius subjektus, įvertinkite savo verslo procesus toliau nurodytose srityse ir nustatykite, ar šis nustatymas veiks jūsų organizacijoje:

-   Atsargos
-   Pardavimai ir pirkimai tarp finansinių dimensijų ir juridiniai subjektai
-   PVM skaičiavimas ir atskaitomybė
-   Veiklos ataskaitos

Kai kuriuose apribojimų pavyzdžiuose yra:

-   PVM funkciją galite naudoti tik su juridiniais subjektais, o ne su finansinėmis dimensijomis.
-   Kai kuriose ataskaitose neįtrauktos finansinės dimensijos, tad ne visada galima teikti ataskaitas pagal finansines dimensijas, nebent šios ataskaitos būtų modifikuotos.

**Custom dimensions** 

Norėdami sukurti vartotojo apibrėžiamų finansinių aspektų, naudoti reikšmes iš lauko, pasirinkite &lt;Custom aspektas&gt;. Taip pat galite nurodyti sąskaitos šabloną, ribojantį informacijos, kurią galite įvesti kaip dimensijos reikšmes, kiekį ir tipą. Galite įvesti simbolius, kurie išlieka vienodi visose dimensijos reikšmėse, pvz., raides arba brūkšnelį. Taip pat galite įvesti skaičių ženklais (\#) ir jungimo (&) kaip vietos rezervavimo ženklus, raides ir skaičius, kad bus pakeisti kiekvieną kartą, kai sukuriamas dimensijos vertė. Naudoti numerio ženklas (\#) kaip vietos rezervavimo ženklas, skaičių ir ampersendą (&) kaip vietos žymeną, skirtą laišką. 

**Pavyzdys:** 

Norėdami apriboti dimensijos vertės CC raidės ir tris skaičius, įvedate CC -\#\#\# kaip formos šablonas. Šį lauką galima naudoti tik pasirinkus &lt;Custom dimensijos &gt;naudoti reikšmes iš lauko. 

**Įmonė remia matmenys** 

Norėdami sukurti objekto remiamas finansinių aspektų, naudoti reikšmes iš lauko, pasirinkite sistemos subjektą pagrįsti finansinių aspektų. Finansinės dimensijos reikšmės sukuriamos pagal šį pasirinkimą. Pavyzdžiui, norėdami sukurti projektų dimensijų reikšmes, pasirinkite Projektai. Bus sukurtos kiekvieno projekto pavadinimo dimensijos reikšmės. Dimensijų verčių puslapyje rodomos objekto vertės ir, jei jos susijusios su konkrečia įmone, įmonė, kurios vertė nurodyta. 

**Aktyvinti dimensijų** 

Suaktyvinus finansinę dimensiją lentelė atnaujinama ir joje pateikiamas finansinės dimensijos pavadinimas, o panaikintos dimensijos pašalinamos. Dimensijų reikšmes galima įvesti prieš suaktyvinant finansinę dimensiją, bet finansinės dimensijos negalima niekur naudoti, kol ji yra suaktyvinama. Pavyzdžiui, finansinės dimensijos į sąskaitos struktūrą įtraukti negalima, kol finansinė dimensija suaktyvinama. Aktyvinus spustelėjant bus atnaujintos visos dimensijos, kurių būsena pasikeitė. 

**Translations** 

Teksto vertimo puslapis leidžia įvesti tekstą ir jį rodo skirtingų kalbų pasirinktų finansinių aspektų. Puslapyje Pagrindinės sąskaitos vertimas galite įvesti pagrindinės sąskaitos tekstą, kuris bus rodomas skirtingomis kalbomis. 

**Legal entity overrides** 

Ne visi matmenys galioja visi juridiniai asmenys, ir kai gali būti aktuali tik už tam tikrą laikotarpį. Tokiu atveju skyrius Juridinio subjekto nepaisymas gali būti naudojamas nustatyti, kuriose įmonėse dimensijos turi būti sustabdytos, kas jų savininkas ir kurį laikotarpį dimensija yra aktyvi.




