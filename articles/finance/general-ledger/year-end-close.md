---
title: Metų pabaigos uždarymas
description: Šiame straipsnyje aprašomi reikalingi DK metų pabaigos uždarymo proceso parametrai ir veiksmai.
author: kweekley
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: kfend
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 032c572ec7b29bb6b2823ddde0c4fa76e5f8fcf1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883219"
---
# <a name="year-end-close"></a>Metų pabaigos uždarymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomi reikalingi DK metų pabaigos uždarymo proceso parametrai ir veiksmai.

Finansinių metų pabaigoje turite vykdyti uždarymo metų pabaigoje procesą, kad pradiniai balansai būtų perkelti į naujus metus. Tikėtina, kad dauguma organizacijų uždarymo metų pabaigoje procesą vykdys kelis kartus. Pirmasis vykdymas perkelia balansus į naujus finansinius metus. Tada procesą galima vykdyti iš naujo tiek kartų, kiek reikia, kad balansai iš koregavimo įrašų būtų perkelti į naujus finansinius metus.

Uždarymo metų pabaigoje proceso metu sukuriami du galimų operacijų tipai. Atidarymo operacija sugeneruojama visada ir naudojama kuriant naujų finansinių metų pradinius balansus. Atidarymo operacija parodo naujų finansinių metų DK sąskaitos balansus ir DK sąskaitos pelno bei nuostolių balansus, DK sąskaitoje pateiktus nepaskirstyto naujais finansiniais metais pelno laukelyje. Uždarymo operacija sukuriama pasirenkamai, kad tų uždaromų finansinių metų pelno ir nuostolių sąskaitų balansai būtų lygūs nuliui.

## <a name="prepare-to-run-the-year-end-close"></a>Pasiruošimas uždarymo metų pabaigoje proceso vykdymui

Prieš vykdydami uždarymo metų pabaigoje procesą patikrinkite toliau nurodytų elementų parametrus.

Puslapyje **Pagrindinės sąskaita**

- Patikrinkite, ar **Pagrindinės sąskaitos tipo** laukas tinkamai nustatytas kiekvienai pagrindinei sąskaitai. Pagrindinės sąskaitos tipas nustato, ar pagrindinės sąskaitos balansas į atidarymo operacijos metu nepanaudotą pelną bus perkeltas kaip pradinis ar uždarymo balansas.
- Pagrindinės sąskaitos balansas gali būti perkeltas į naują pagrindinę sąskaitą metų pabaigos uždarymo metu. Įveskite naują pagrindinę sąskaitą į **Atidarymo sąskaitos** lauką. Įprastai ši sąskaita yra naudojama pagrindinių sąskaitų balansui, kai nesuaktyvinta pagrindinė sąskaita, o nauja sąskaita bus naudojama naujais finansiniais metais.

Puslapio **DK parametrai** dalyje **Finansinių metų uždarymas**:

- Parinktis **Naikinti esamus metų pabaigos įrašus pakartotinai uždarant metus** naudojama nurodant, ar reikia panaikinti praeito uždarymo metų pabaigoje proceso metu sistemos sugeneruotą atidarymo operaciją, kai uždarymo metų pabaigoje procesas yra vykdomas iš naujo. Jei ši parinktis nustatyta į **Taip**, ankstesnės atidarymo ir pasirinktinė uždarymo operacijos bus panaikintos ir bus sukurta nauja atidarymo arba uždarymo operacija, atsižvelgiant į dabartinius balansus. Jei ši parinktis nustatyta į **Ne**, ankstesnės atidarymo ir pasirinktinė uždarymo operacijos išliks ir bus sukurta papildoma atidarymo arba uždarymo operacija, skirta perkelti balansams iš koregavimo operacijų, užregistruotų įvykdžius ankstesnį uždarymo metu pabaigoje procesą.
- Perkėlimo **metu parinktis** Kurti uždarymo operacijas naudojama uždaroų finansinių metų uždarymo operacijoms kurti, kad visų pagrindinių sąskaitų balansai būtų 0 (nulis). Jei ši parinktis nustatyta į **Taip**, sukuriamos tiek atidarymo, tiek uždarymo operacijos. Jei ši parinktis nustatyta į **Ne**, kitais finansiniais metais sukuriama tik atidarymo operacija, kad balansai būtų perkelti. Pagrindinės sąskaitos balansai liktų finansinių metų pabaigoje.
- Parinktis **Nustatyti finansinių metų būseną kaip Uždaryta visam laikui** naudojama būsenai Finansiniai metai uždaryti visam laikui nustatyti. Šią parinktį naudokite atidžiai, nes laikotarpių, turinčių visam laikui uždarytą būseną, negalima atidaryti iš naujo. Todėl koregavimai negali būti registruojami į finansinius metus. Geriausia šią parinktį reikėtų nustatyti į **Ne**.
- Parinktis **Kvito numeris turi būti užpildytas** buvo pašalinta. Dabar yra reikalingas kvitas, kai vyksta metų pabaigos uždarymo procesas. Tuo metu kvito numeris yra įvedamas rankiniu būdu.

Puslapyje **Finansinis kalendorius**:

- Nauji finansiniai metai turi būti sukurti prieš pradedant vykdyti metų pabaigos uždarymo procesą. Kitu atveju pradinių balansų negalima sukurti atidarymo laikotarpiu.

Puslapyje **DK kalendorius**:

- Pasirinktinai: kiekvienam uždaromų finansinių metų ataskaitiniam laikotarpiui galima nustatyti būseną **Sustabdyta**, kad nebūtų leidžiama įvesti naujų operacijų. Nustačius koregavimo įrašus, Sustabdytos būsenos laikotarpius galima atidaryti iš naujo, kad būtų galima užregistruoti koregavimo įrašus, net jei uždarymo metų pabaigoje procesas jau buvo pradėtas vykdyti.

**Metų pabaigos uždarymo šablono nustatymo** puslapyje:

- Kai funkcija **Didžiosios knygos metų pabaigos patobulinimai** įjungta, metų pabaigos uždarymo šablono nustatymo procesas atskiriamas nuo metų pabaigos uždarymo proceso. Šabloną galima nustatyti **Metų pabaigos uždarymo šablono nustatymo** puslapyje (**Didžioji knyga \> Didžiosios knygos nustatymas \> Metų pabaigos uždarymo šablono nustatymas**) arba jis gali būti pasiektas iš metų pabaigos uždarymo proceso.

## <a name="define-year-end-close-templates"></a>Uždarymo metų pabaigoje šablonų apibrėžimas

Sukonfigūravus sistemą, galima pradėti vykdyti uždarymo metų pabaigoje procesą. Puslapyje **Uždarymo metų pabaigoje šablono nustatymas** galima apibrėžti šabloną, skirtą juridinių subjektų, kuriems bus atliekamas uždarymo metų pabaigoje procesas, grupei. Šablonas bus pakartotinai naudojamas kiekvieno uždarymo metų pabaigoje metu, bet jūsų organizacijai pasikeitus jį bus galima modifikuoti.

Pirmiausia nustatykite lauką **Grupės pavadinimas** šablonui ir pasirinkite finansinį kalendorių. Grupės pavadinimas turėtų identifikuoti įtrauktų juridinių subjektų grupę. Nustatydami juridinių subjektų grupes atsiminkite, kad juridinius subjektus galima įtraukti į tą pačią grupę tik jei jiems pasirinktas tas pats finansinis kalendorius. Pavyzdžiui, šablonus galima nustatyti pagal geografiją, taip pat galima sukurti atskiras Šiaurės Amerikos, Europos, Vidurinių Rytų ir Afrikos (EMEA) bei Azijos ir Ramiojo vandenyno regiono (APAC) juridinių subjektų grupes.

Tada juridinius subjektus galima įtraukti į šabloną. Juridiniai subjektai gali būti įtraukti pasirenkant organizacijos hierarchiją arba pasirenkant juridinius subjektus. Pasirinkus organizacijos hierarchiją, į šabloną bus įtraukti tik pasirinkto finansinio kalendoriaus hierarchijoje esantys juridiniai subjektai. Jei įtraukimui į šabloną naudosite juridinius subjektus, bus galima įtraukti tik to paties fiskalinio kalendoriaus juridinius subjektus. Reikia naudoti tą patį fiskalinį kalendorių, nes uždarymo metų pabaigoje procesas vykdomas pasirinkus finansinius metus, kurie gali skirtis priklausomai nuo kalendoriaus.

Įtraukus juridinius subjektus, kiekvienam juridiniam subjektui apibrėžkite nepaskirstyto pelno pagrindines sąskaitas.

Skirtukas **Finansinė dimensija** naudojamas apibrėžiant kurios finansinės dimensijos bus naudojamos atidarymo operacijai. Atkreipkite dėmesį, kad nustatymas šiame skirtuke yra taikomas tik tinklelyje **Juridiniai subjektai** pasirinktam juridiniam subjektui. Šią procedūrą turėsite pakartoti kiekvienam tinklelyje esančiam juridiniam subjektui.

Parinktis **Perkelti balanso dimensijas** naudojama nurodant, ar balanso sąskaitose užregistruotų operacijų finansines dimensijas reikia taikyti atidarymo operacijai. Geriausia šią parinktį reikėtų nustatyti į **Taip**. Balanso dimensijų nustatymas neturi įtakos esamiems nepaskirstyto pelno didžiosios knygos sąskaitų balansams. Šie balansai nustatomi pagal pelno ir nuostolio dimensijas, kurios apibrėžtos kitame skyriuje. Pavyzdžiui, 2019 finansiniai metai buvo pirmieji uždaryti metai, o parinktis **Uždaryti viską** buvo panaudota pasirinkti **Skyriaus** ir **Išlaidų centro** dimensijas uždarymui. Šiuo atveju kiekvienai padalinio ir išlaidų centro kombinacijai buvo sukurta atskira nepaskirstyto pelno sąskaita. Kai metų pabaigos uždarymas vykdomas 2020 finansiniams metams, nepaskirstytas ankstesnių metų pelnas išlieka toks pat, kaip ir užregistruotas, net jei **Perkelti balanso dimensijas** nustatyta į **Ne**. Balansai, užregistruoti kaip nepaskirstytas pelnas iš ankstesnių metų pabaigos uždarymų, niekada nekeičiami.

Skyrius **Perkelti pelno ir nuostolių dimensijas** naudojama nurodant, kurios operacijų, užregistruotų pelno ir nuostolių sąskaitose, finansinės dimensijos bus perkeltos į nepaskirstyto pelno pagrindinę sąskaitą. Pirmiausia identifikuokite finansines dimensijas, susijusias su pasirinktu juridiniu subjektu. Šios finansinės dimensijos apima bet kokias tais metais užregistruotas finansines dimensijas, net jei finansinė dimensija nėra aktyvios sąskaitos struktūros dalis. Tada kiekvieną dimensiją apibrėžkite kaip **Uždaryti vieną** arba **Uždaryti viską**. Numatytoji pasirinktis yra **Uždaryti viską**. Ši parinktis išlaiko pradines finansinės dimensijos vertes iš užregistruotų operacijų ir panaudoja jas kuriant nepaskirstyto pelno sąskaitos pradinius balansus. Bus sukurti kiekvienai unikaliai finansinių dimensijų verčių kombinacijai skirti atskiri nepaskirstyto pelno pradiniai balansai. Jei pasirinkta **Uždaryti vieną**, visos užregistruotos operacijos, turinčios tą finansinę dimensiją, bus apibendrinamos kaip nepaskirstyto pelno pradiniai balansai, skirti dimensijos vertei, įvestai po lauke, pasirodančiame po **Uždaryti vieną**. Pavyzdžiui, visos tų finansinių metų operacijos buvo užregistruotos naudojant sąskaitos struktūrą **Pagrindinė sąskaita – Padalinys**. Finansinei dimensijai **Padalinys** šablone pasirinkta **Uždaryti vieną**, o **„100”** įvedamas kaip dimensijos vertė. Jei bendros visų operacijų, kurios yra užregistruotos padaliniuose 200, 300 ir 400, pajamos siekia $ 100 000 JAV dolerių, bus sukurtas vienas pradinis balansas, skirtas **Nepaskirstytam pelnui – 100**. Jei pasirenkate **Uždaryti vieną**, bet paliekate finansinės dimensijos vertę tuščią, visos operacijos bus užregistruotos kaip nepaskirstytas pelnas, o tos dimensijos vertė bus tuščia.

## <a name="run-the-year-end-close-process"></a>Uždarymo metų pabaigoje proceso vykdymo pradžia

Sukūrę metų pabaigos uždarymo šablonus, galite inicijuoti metų pabaigos uždarymo procesą **Metų pabaigos uždarymo** puslapyje (**Didžioji knyga \> Uždarymo laikotarpis \> Metų pabaigos uždarymas**). Prieš paleisdami metų pabaigos uždarymą, galite pridėti naujų metų pabaigos uždarymo šablonų arba modifikuoti esamus šablonus pasirinkdami **Metų pabaigos uždarymo šablono nustatymą**, kad atidarytumėte šablonų nustatymo puslapį.

Pasirinkite metų pabaigos uždarymo šabloną, o tada veiksmų srityje pasirinkite **Vykdyti metų pabaigos uždarymą**. Iš šablono pasirinkite visus arba dalį juridinių subjektų, kuriems vykdote uždarymo metų pabaigoje procesą. Jei uždarymo metų pabaigoje procesą vykdote pirmą kartą finansiniais metais, greičiausiai pasirinksite visus juridinius subjektus, kad jiems visiems sukurtumėte pradinius balansus. Jei uždarymo metų pabaigoje procesą vykdėte anksčiau, galbūt norėsite kad procesas būtų vykdomas tik tiems juridiniams subjektams, kuriems buvo užregistruoti koregavimo įrašai.

Tada pasirinkite finansinius metus, kuriems taikysime uždarymo metų pabaigoje procesą. Jei yra daugiau nei vienas paskutinio finansinių metų laikotarpio uždarymo laikotarpis, galima naudoti **Laikotarpio pavadinimo** lauką. Tada galite pasirinkti uždarymo laikotarpį, kad registruotumėte uždarymo operaciją, jei nustatymas apibrėžtas sukurti uždarymo operaciją.

Tada įveskite kvito numerį. Tas pats kvito numeris bus naudojamas visiems tų metų uždarymo procese jūsų pasirinktiems juridiniams subjektams. Kvito numeris nėra generuojamas naudojant numeraciją.

Pagal numatytuosius parametrus, uždarymo metų pabaigoje procesas vykdomas paketiniu režimu. Todėl, jį inicijavę galite grįžti į kitas veiklas.

Kadangi sąskaitos struktūros gali keistis per finansinius metus, ne visada galima identifikuoti atitinkamą sąskaitos struktūrą. Todėl uždarymo metų pabaigoje procesas nesilaiko sąskaitos struktūrų. Sukūrus atidarymo operacijas, balansai perkeliami kartu su finansinėmis dimensijomis, kaip apibrėžta metų pabaigos uždarymo šablone. Pradinių balansų įrašuose gali būti finansinių dimensijų, kurių nebėra dabartinės sąskaitos struktūroje, taip pat ir nebegaliojančias dabartinės sąskaitos struktūros segmentų kombinacijas. Jei jūsų organizacija nori išskirti nepaskirstyto pelno pradinio balanso finansinę dimensiją, tą finansinę dimensiją apibrėžkite kaip **Uždaryti vieną**, o dimensijos reikšmės lauką palikite tuščią.

Užbaigus procesą, sukuriamas kiekvieno juridinio subjekto ir finansinių metų derinio įrašas. Matysite tik tų juridinių asmenų, prie kurių turite prieigą, įrašus. Kiekviename įraše yra sistemos data ir laikas, kada buvo paleistas procesas, ir tiesioginis saitas į kvitus, sukurtus metų pabaigos uždarymui.

[![Įrašai, sukurti metų pabaigos uždarymo retrospektyvos „FastTab” puslapyje Metų pabaigos uždarymas](./media/run-yr-end-close.png)](./media/run-yr-end-close.png)

Jei metų pabaigos uždarymą paleisite pakartotinai, pamatysite vieną arba kelis kiekvieno juridinio subjekto ir finansinių metų derinio įrašus, priklausomai nuo parinkties **Naikinti esamus metų pabaigos įrašus pakartotinai uždarant metus** nustatymo **Didžiosios knygos parametrai** puslapyje:

- Jei parinktis nustatyta į **Taip**, ankstesnis metų pabaigos uždarymo kvitas yra panaikinamas. Įrašas pažymimas kaip **Atšauktas** bei data ir laiku, kai atšaukimas buvo atliktas. Taip pat, pašalinama kvito numerio nuoroda. Užbaigus metų pabaigos uždarymą, bus sukurtas naujas sukurto naujo kvito įrašas.
- Jei parinktis nustatyta į **Ne**, ankstesnio metų pabaigos uždarymo įrašas lieka kartu su saitu į kvitą. Kaskart, kai pakartotinai bus vykdomas metų pabaigos uždarymas, bus sukurtas naujas įrašas, kartu su saitu į naujus kvitus.

## <a name="reverse-the-year-end-close-process"></a>Uždarymo metų pabaigoje proceso atšaukimas

Puslapyje **Metų pabaigos uždarymas** galite atšaukti metų pabaigos uždarymą. Pasirinkite juridinio subjekto ir finansinių metų, kuriuos reikia atšaukti, derinio įrašą, o tada pasirinkite **Atšaukti metų pabaigos uždarymą**. Atšaukimo procesas panaikina visus atidarymo ir uždarymo kvitus, sukurtus finansiniais metais. Įrašas pažymimas kaip **Atšauktas** bei data ir laiku, kai atšaukimas buvo atliktas. Taip pat, pašalinama kvito numerio nuoroda. Kaip ir metų pabaigos uždarymo procesas, atšaukimas vykdomas paketiniu režimu.

Virš tinklelio esantis žymės langelis **Rodyti atšauktą** leidžia jums paslėpti arba rodyti atšauktų metų pabaigos uždarymo procesų įrašus. Kai paleidžiate **Atvirkštinio metų pabaigos uždarymo procesą**, jums gali reikėti pažymėti **Rodyti atšauktą** žymės langelį, kad pamatytumėte įrašą. Norėdami peržiūrėti kitą informaciją, jūs galite nustatyti papildomus filtrus.

[![Žymės langelio Rodyti atšauktą naudojimas, norint pamatyti atšauktų uždarymo metų pabaigoje procesų įrašus Metų pabaigos uždarymo puslapyje](./media/rvrs-yr-end-close.png)](./media/rvrs-yr-end-close.png)

Daugiau informacijos žr. [DK uždarymas laikotarpio pabaigoje](close-general-ledger-at-period-end.md) ir [Uždaryti finansinius metus](tasks/close-fiscal-year.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
