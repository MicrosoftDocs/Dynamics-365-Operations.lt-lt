---
title: "Uždarymas metų pabaigoje"
description: "Šioje temoje aprašomi nustatymai ir veiksmai, reikalingi DK uždarymo metų pabaigoje procesui vykdyti."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 50a6a23febc725eb05d30d5db4f97ca699607461
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017

---

# <a name="year-end-close"></a>Uždarymas metų pabaigoje

[!include[banner](../includes/banner.md)]


Šioje temoje aprašomi nustatymai ir veiksmai, reikalingi DK uždarymo metų pabaigoje procesui vykdyti. 

Finansinių metų pabaigoje turite vykdyti uždarymo metų pabaigoje procesą, kad pradiniai balansai būtų perkelti į naujus metus. Tikėtina, kad dauguma organizacijų uždarymo metų pabaigoje procesą vykdys kelis kartus. Vykdant procesą pirmą kartą balansai perkeliami į naujus finansinius metus. Tada uždarymo metų pabaigoje procesą iš naujo galima vykdyti tiek kartų, kiek reikia, kad balansai iš koregavimo įrašų būtų perkelti į naujus finansinius metus. 

Uždarymo metų pabaigoje proceso metu sukuriami du galimų operacijų tipai. Atidarymo operacija sugeneruojama visada ir naudojama kuriant naujų finansinių metų pradinius balansus. Atidarymo operacija parodo naujų finansinių metų DK sąskaitos balansus ir DK sąskaitos pelno bei nuostolių balansus, DK sąskaitoje pateiktus nepaskirstyto naujais finansiniais metais pelno laukelyje. Uždarymo operacija sukuriama pasirenkamai, kad tų uždaromų finansinių metų pelno ir nuostolių sąskaitų balansai būtų lygūs nuliui.

## <a name="prepare-to-run-the-year-end-close"></a>Pasiruošimas uždarymo metų pabaigoje proceso vykdymui
Prieš vykdydami uždarymo metų pabaigoje procesą patikrinkite toliau nurodytų elementų parametrus. 

Puslapyje **Pagrindinės sąskaita**

-   Patikrinkite, ar tinkamai apibrėžtas kiekvienai pagrindinei sąskaitai skirtas **Pagrindinės sąskaitos tipas**. Pagrindinės sąskaitos tipas naudojamas siekiant nustatyti, ar pagrindinės sąskaitos balansas į atidarymo operacijos metu nepanaudotą pelną bus perkeltas kaip pradinis ar uždarymo balansas.
-   Laukas **Atidarymo sąskaita** uždarymo metų pabaigoje proceso metu gali būti naudojamas perkeliant pagrindinės sąskaitos balansą į naują pagrindinę sąskaitą. Nauja pagrindinė sąskaita įvedama lauke **Atidarymo sąskaita**. Paprastai ši sąskaita bus naudojama pagrindinių sąskaitų balansui, kai nesuaktyvinta pagrindinė sąskaita, o nauja sąskaita bus naudojama naujais finansiniais metais.

Puslapio **DK parametrai** dalyje **Finansinių metų uždarymas**:

-   Parinktis **Naikinti metų operacijų uždarymą** naudojama nurodant, ar reikia panaikinti praeito uždarymo metų pabaigoje proceso metu sistemos sugeneruotą atidarymo operaciją, kai uždarymo metų pabaigoje procesas vykdomas iš naujo. Jei ši parinktis nustatyta ties **Taip**, ankstesnė atidarymo operacija bus panaikinta ir, atsižvelgus į naujus esamus balansus, bus sukurta nauja atidarymo operacija. Jei ši parinktis nustatyta ties **Ne**, ankstesnė atidarymo operacija panaikinta nebus, bet bus sukurta papildoma atidarymo operacija, skirta perkelti balansus į priekį iš koregavimo operacijų, užregistruotų įvykdžius ankstesnį uždarymo metu pabaigoje procesą.
-   Parinktis **Kurti uždarymo operacijas** perkėlimo metu naudojama kuriant uždaromų finansinių metų uždarymo operacijas, kad tų uždaromų finansinių metų pelno ir nuostolių sąskaitų balansai būtų lygūs nuliui. Jei ši parinktis nustatyta ties **Taip**, bus sukurtos tiek atidarymo, tiek ir uždarymo operacijos. Jei ši parinktis nustatyta ties **Ne**, kitais finansiniais metais bus sukurta tik atidarymo operacija, kad balansai būtų perkelti. Pelno ir nuostolių balansai tų finansinių metų pabaigoje bus paliekami.
-   Parinktis **Nustatyti finansinių metų būseną kaip Uždaryta visam laikui** naudojama būsenai Finansiniai metai uždaryti visam laikui nustatyti. Šį parametrą naudokite atsargiai, nes laikotarpių, kuriems nustatyta būsena Uždaryta visam laikui, iš naujo atidaryti negalima, siekiant neleisti užregistruoti tų finansinių metų pakeitimų. Geriausia šią parinktį nustatyti į **Ne**.
-   Parinktis **Turi būti įrašytas kvito numeris** naudojama apibrėžiant, ar vykdant uždarymo metų pabaigoje procesą turi būti reikalaujama nurodyti kvito numerį. Geriausia reikalauti, kad kvito numeris būtų nurodomas, nes tada paprasčiau nustatyti atidarymo operaciją.

Puslapyje **Finansinis kalendorius**:

-   Nauji finansiniai metai turi būti sukurti prieš pradedant vykdyti uždarymo metų pabaigoje procesą. Kiti finansiniai metai reikalingi, kad atidarymo laikotarpiu būtų sukurti pradžios balansai.

Puslapyje **DK kalendorius**:

-   Pasirinktinai: kiekvienam uždaromų finansinių metų ataskaitiniam laikotarpiui galima nustatyti būseną **Sustabdyta**, kad būtų neleista įvesti naujų operacijų. Nustačius koregavimo įrašus, laikotarpius, kuriems nustatyta būsena Sustabdyta, galima atidaryti iš naujo, kad būtų užregistruoti koregavimo įrašai, net jei uždarymo metų pabaigoje procesas jau buvo pradėtas vykdyti.

## <a name="define-year-end-close-templates"></a>Uždarymo metų pabaigoje šablonų apibrėžimas
Sukonfigūravus sistemą, galima pradėti vykdyti uždarymo metų pabaigoje procesą. Puslapyje **Uždarymas metų pabaigoje** galima apibrėžti šabloną, skirtą juridinių subjektų, kuriems bus atliekamas uždarymo metų pabaigoje procesas, grupę. Šablonas bus naudojamas kiekvieno uždarymo metų pabaigoje metu, bet organizacijai pasikeitus jį bus galima modifikuoti. 

Pirmiausia apibrėžkite šablono **Grupės pavadinimą** ir pasirinkite finansinį kalendorių. Grupės pavadinimas turėtų identifikuoti įtrauktą juridinių subjektų grupę.  Pavyzdžiui, šablonus galima nustatyti atsižvelgiant į geografiją ir sukuriant atskiras Šiaurės Amerikos juridinių subjektų, Europos, Vidurinių Rytų ir Afrikos juridinių subjektų bei Azijos ir Ramiojo vandenyno regiono juridinių subjektų grupes. 

Tada juridinius subjektus galima įtraukti į šabloną. Juridiniai subjektai gali būti įtraukti pasirenkant organizacijos hierarchiją arba pasirenkant juridinius subjektus. Pasirinkus organizacijos hierarchiją, į šabloną bus įtraukti tik pasirinkto finansinio kalendoriaus hierarchijoje esantys juridiniai subjektai. Jei įtraukimui į šabloną naudosite juridinius subjektus, bus galima įtraukti tik to paties fiskalinio kalendoriaus juridinius subjektus. Reikia naudoti tą patį fiskalinį kalendorių, nes uždarymo metų pabaigoje procesas vykdomas pasirinkus finansinius metus, kurie gali skirtis priklausomai nuo kalendoriaus. 

Įtraukus juridinius subjektus, kiekvienam juridiniam subjektui apibrėžkite nepaskirstyto pelno pagrindines sąskaitas. Laukas **Paskutinio uždarymo metų pabaigoje data** bus atnaujintas kaskart pradėjus vykdyti juridinio subjekto uždarymo metų pabaigoje procesą. 

Skirtukas **Finansinė dimensija** naudojamas apibrėžiant kurios finansinės dimensijos bus naudojamos atliekant atidarymo operaciją. Atkreipkite dėmesį, kad jūsų apibrėžiami parametrai yra susiję tik su tinklelyje **Juridiniai subjektai** pasirinktu juridiniu subjektu. Šią procedūrą reikės kartoti kiekvienam tinklelyje esančiam juridiniam subjektui. 

Parinktis **Perkelti balanso dimensijas** naudojama apibrėžiant, ar finansines operacijų, užregistruotų balanso sąskaitose, dimensijas reikia prižiūrėti atidarymo operacijos metu. Geriausia šią parinktį nustatyti į **Taip**. Parinktis **Perkelti pelno ir nuostolių dimensijas** naudojama apibrėžiant, kurios finansinės operacijos, užregistruotos pelno ir nuostolių sąskaitoje, bus perkeltos į nepaskirstyto pelno pagrindinę sąskaitą. Pirmiausia identifikuokite su pasirinktu juridiniu subjektu susijusias finansines dimensijas. Į šią parinktį įtraukite bet kokias per metus užregistruotas finansines dimensijas, net jei finansinė dimensija nepriklauso aktyviai sąskaitos struktūrai. Tada kiekvieną dimensiją apibrėžkite kaip **Uždaryti vieną** arba **Uždaryti viską**.  Numatytoji parinktis yra **Uždaryti viską**, kurios paskirtis – prižiūrėti pradines finansinės dimensijos vertes iš užregistruotų operacijų ir panaudoti jas kuriant nepaskirstyto pelno sąskaitos pradinius balansus. Bus sukurti kiekvienai unikaliai finansinių dimensijų verčių kombinacijai skirti atskiri nepaskirstyto pelno pradiniai balansai. Pasirinkus parinktį **Uždaryti vieną**, visos užregistruotos tos finansinės dimensijos operacijos bus apibendrinamos kaip nepaskirstyto pelno pradiniai balansai, skirti dimensijos vertei, įvestai po parinkties **Uždaryti vieną** esančiame laukelyje. Pavyzdžiui, tarkime, kad visos tų finansinių metų operacijos buvo užregistruotos naudojant sąskaitos Pagrindinė sąskaita – Padalinys struktūrą. Šablono dalyje Finansinės dimensijos padalinys bus pasirinkta parinktis **Uždaryti vieną** ir įvesta vertė 100. Jei bendros visų operacijų, užregistruotų padaliniuose 200, 300 ir 400, pajamos siekia 100 000 JAV dolerių, bus sukurtas vienas pradinio nepaskirstyto pelno balansas, lygus 100. Pasirinkus parinktį **Uždaryti vieną** ir finansinės dimensijos vertės lauką palikus tuščią, visos operacijos bus užregistruotos kaip nepaskirstytas pelnas, o tos dimensijos vertės laukas bus tuščias. 

Uždarymo metų pabaigoje procesas vykdomas nesilaikant sąskaitos struktūrų. Taip yra todėl, kad paskyros struktūras finansiniais metais galima keisti bet kada, o dėl šių pokyčių identifikuoti susijusią paskyros struktūrą pavyksta ne visada.  Sukūrus atidarymo operacijas, balansai bus perkelti kartu su finansinėmis dimensijomis, kaip apibrėžta uždarymo metų pabaigoje šablone. Į pradinių balansų vertes galima įtraukti finansines dimensijas, nebeesančias dabartinės sąskaitos struktūroje, taip pat ir nebegaliojančias dabartinės sąskaitos struktūros segmentų kombinacijas. Jei jūsų organizacija nori išskirti finansinę nepaskirstyto pelno pradinio balanso dimensiją, tą finansinę dimensiją nustatykite kaip  **Uždaryti vieną**, o dimensijos vertės lauką palikite tuščią.

## <a name="run-the-year-end-close-process"></a>Uždarymo metų pabaigoje proceso vykdymo pradžia
Sukūrus uždarymo metų pabaigoje šablonus, uždarymo metų pabaigoje procesas pradedamas vykdyti veiksmų srityje pasirinkus **Atidaryti fiskalinį laikotarpį**. Pasirinkite visus arba dalį šablone pateiktų juridinių subjektų, kuriems norite taikyti uždarymo metų pabaigoje procesą. Pirmą kartą vykdant finansinių metų uždarymo metų pabaigoje procesą, greičiausiai norėsite pasirinkti, kad būtų sukurti visų teisinių subjektų pradiniai balansai. Jei uždarymo metų pabaigoje procesą vykdote iš naujo, galite pasirinkti, kad procesas būtų taikomas tik tiems juridiniams subjektams, kurių koregavimo įrašai buvo užregistruoti. 

Pasirinkite finansinius metus, kuriems norėtumėte taikyti uždarymo metų pabaigoje procesą. Jei tų finansinių metų paskutinis laikotarpis turi daugiau nei vieną uždarymo laikotarpį, bus pasiekiamas laukas **Laikotarpio pavadinimas**, kad galėtumėte pasirinkti, kurį laikotarpį registruoti uždarymo operacijai, jei sąrankoje apibrėžta sukurti tokią operaciją. 

Įveskite kvito numerį (atsižvelgiant į DK parametrų sąranką kvito numerį gali būti reikalaujama įvesti arba ne). Tas pats kvito numeris bus naudojamas visiems tų metų uždarymo procese pasirinktiems juridiniams subjektams. Kvito numeris sugeneruojamas nenaudojant numeracijos. Geriausia kvito numerį įvesti net ir tada, kai to daryti nereikalaujama. Įvedus kvito numerį galima lengviau rasti tų finansinių metų atidarymo operaciją. Neįvedus kvito numerio atidarymo operacijos kvito laukas liks tuščias. 

Jei norėtumėte atšaukti ankstesnį uždarymo metų pabaigoje procesą, taikomą pasirinktiems finansiniams metams, parinktį **Anuliuoti ankstesnį uždarymą** nustatykite ties **Taip**. Uždarymo metų pabaigoje procesas bus atšauktas, tačiau jį vėl bus galima vykdyti iš naujo bet kuriuo metu. Atšaukus uždarymo metų pabaigoje procesą, laukas **Paskutinio uždarymo metų pabaigoje data** bus negalimas. 

Pagal numatytuosius parametrus uždarymo metų pabaigoje procesas vykdomas paketiniu režimu. Geriausia šį procesą vykdyti paketinių režimu, kad vartotojas galėtų grįžti prie kitos veiklos. Atlikus uždarymo metų pabaigoje procesą, laukas **Paskutinio uždarymo metų pabaigoje data** bus atnaujinta nurodant seanso datą.

Norėdami gauti daugiau informacijos, žr. [DK uždarymas laikotarpio pabaigoje](close-general-ledger-at-period-end.md).




