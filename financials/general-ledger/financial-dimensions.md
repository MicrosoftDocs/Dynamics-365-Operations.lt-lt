---
title: "Finansinės dimensijos"
description: "Šiame straipsnyje paaiškinami skirtingi finansinių dimensijų tipai ir tai, kaip jie nustatomi."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 01f189b8de3f0cc707dcc54f4cde75aed95b8e3f
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="financial-dimensions"></a>Finansinės dimensijos

[!include[banner](../includes/banner.md)]


Šiame straipsnyje paaiškinami skirtingi finansinių dimensijų tipai ir tai, kaip jie nustatomi.

Naudokite puslapį Finansinės dimensijos kurdami finansines dimensijas, kurias galite naudoti kaip sąskaitų planų sąskaitos segmentus. Yra dviejų tipų finansinės dimensijos: pasirinktinės dimensijos ir objekto remiamos dimensijos. Pasirinktinės dimensijos yra bendrai naudojamos juridinių subjektų, o vertes įveda ir tvarko vartotojas. Objekto remiamos dimensijos yra dimensijos, kurių vertės nurodomos kitur sistemoje, pvz., dalyse Klientai ar Parduotuvės. Kai kurios objekto remiamos dimensijos yra bendrai naudojamos keliuose juridiniuose subjektuose, o kai kurios būdingos konkrečiai įmonei. 

Sukūrę finansines dimensijas, naudokite puslapį Finansinių dimensijų reikšmės, kad kiekvienai finansinei dimensijai priskirtumėte papildomų ypatybių. 

Nors galite naudoti finansines dimensijas, atstovaujančias juridinius subjektus, nesukurdami juridinių subjektų programoje „Microsoft Dynamics 365 for Operations“, finansinės dimensijos nėra skirtos juridinių subjektų veiklos ar verslo poreikiams. Susijusių vienetų apskaitos funkcija programoje „Microsoft Dynamics 365 for Operations“ yra skirta tik apskaitos įrašams, kuriuos sukuria kiekviena operacija. 

Prieš nustatydami finansines dimensijas kaip juridinius subjektus, įvertinkite savo verslo procesus toliau nurodytose srityse ir nustatykite, ar šis nustatymas veiks jūsų organizacijoje:

-   Atsargos
-   Pardavimai ir pirkimai tarp finansinių dimensijų ir juridiniai subjektai
-   PVM skaičiavimas ir atskaitomybė
-   Veiklos ataskaitos

Kai kuriuose apribojimų pavyzdžiuose yra:

-   PVM funkciją galite naudoti tik su juridiniais subjektais, o ne su finansinėmis dimensijomis.
-   Kai kuriose ataskaitose neįtrauktos finansinės dimensijos, tad ne visada galima teikti ataskaitas pagal finansines dimensijas, nebent šios ataskaitos būtų modifikuotos.

**Pasirinktinės dimensijos** 

Norėdami kurti vartotojo nustatomą finansinę dimensiją, lauke Naudoti vertes iš pasirinkite &lt; Pasirinktinė dimensija &gt;. Taip pat galite nurodyti sąskaitos šabloną, ribojantį informacijos, kurią galite įvesti kaip dimensijos reikšmes, kiekį ir tipą. Galite įvesti simbolius, kurie išlieka vienodi visose dimensijos reikšmėse, pvz., raides arba brūkšnelį. Taip pat galite įvesti skaičiaus ženklus (\##) ir konjunkcijos ženklus (&) kaip vietos rezervavimo ženklus vietoj raidžių ir skaitmenų, kurie bus skirtingi kaskart sukūrus dimensijos reikšmę. Naudokite skaičiaus ženklą (\#) kaip skaitmens vietos rezervavimo ženklą, o konjunkcijos ženklą (&) – kaip raidės vietos rezervavimo ženklą. 

**Pavyzdys:** 

Norėdami apriboti dimensijos reikšmę iki raidžių CC ir trijų skaitmenų, įveskite CC-\#\#\# kaip formato šabloną. Šį lauką galima naudoti tik pasirinkus parinktį &lt; Pasirinktinė dimensija &gt; lauke Naudoti vertes iš. 

**Objekto remiamos dimensijos** 

Norėdami sukurti objekto remiamą finansinę dimensiją, lauke Naudoti vertes iš pasirinkite sistemos nurodytą objektą, kuriuo bus pagrįsta finansinė dimensija. Finansinės dimensijos reikšmės sukuriamos pagal šį pasirinkimą. Pavyzdžiui, norėdami sukurti projektų dimensijų reikšmes, pasirinkite Projektai. Bus sukurtos kiekvieno projekto pavadinimo dimensijos reikšmės. Dimensijų verčių puslapyje rodomos objekto vertės ir, jei jos susijusios su konkrečia įmone, įmonė, kurios vertė nurodyta. 

**Dimensijų aktyvinimas** 

Suaktyvinus finansinę dimensiją lentelė atnaujinama ir joje pateikiamas finansinės dimensijos pavadinimas, o panaikintos dimensijos pašalinamos. Dimensijų reikšmes galima įvesti prieš suaktyvinant finansinę dimensiją, bet finansinės dimensijos negalima niekur naudoti, kol ji yra suaktyvinama. Pavyzdžiui, finansinės dimensijos į sąskaitos struktūrą įtraukti negalima, kol finansinė dimensija suaktyvinama. Aktyvinus spustelėjant bus atnaujintos visos dimensijos, kurių būsena pasikeitė. 

**Vertimai** 

Vertimo puslapiuose galima įvesti pasirinktos finansinės dimensijos tekstą, kuris bus rodomas skirtingomis kalbomis. Puslapyje Pagrindinės sąskaitos vertimas galite įvesti pagrindinės sąskaitos tekstą, kuris bus rodomas skirtingomis kalbomis. 

**Juridinio subjekto nepaisymai** 

Ne visos dimensijos tinkamos visiems juridiniams asmenims, o kai kurios gali būti aktualios tik tam tikrą laikotarpį. Tokiu atveju skyrius Juridinio subjekto nepaisymas gali būti naudojamas nustatyti, kuriose įmonėse dimensijos turi būti sustabdytos, kas jų savininkas ir kurį laikotarpį dimensija yra aktyvi.






