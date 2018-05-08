---
title: Vienas kvitas
description: "Naudodamiesi finansinių žurnalų (bendrojo žurnalo, ilgalaikio turto žurnalo, tiekėjo mokėjimų žurnalo ir t. t.) funkcija Vienas kvitas vieno kvito kontekste galite įvesti kelias papildomos knygos operacijas."
author: kweekley
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9f996131830f9bd4efd534143b3fb761c5ccc756
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="one-voucher"></a>Vienas kvitas

[!include [banner](../includes/banner.md)]

> [!NOTE]
>  Šia funkcija bus galima naudotis programos „Dynamics 365 for Finance and Operations“ versijoje 8.0, kuri bus išleista 2018 m. pavasario leidime.   

<a name="what-is-one-voucher"></a>Kas yra „Vienas kvitas“?
======================

Naudodamiesi esama finansinių žurnalų (bendrojo žurnalo, ilgalaikio turto žurnalo, tiekėjo mokėjimų žurnalo ir t. t.) funkcija vieno kvito kontekste galite įvesti kelias papildomos knygos operacijas. Ši funkcija vadinama „Vienas kvitas“. Vieną kvitą galima sukurti vienu iš toliau nurodytų būdų.

-   Nustatykite žurnalo pavadinimą (**Didžioji knyga** \> **Žurnalo sąranka** \>**Žurnalų pavadinimai**), kad būtų naudojama lauko **Naujas kvitas** nuostata **Tik vienas kvito numeris**. * Nuo šiol kiekviena į žurnalą įtraukta eilutė įtraukiama tame pačiame kvite. Kadangi kiekviena eilutė įtraukiama į tą patį kvitą, kvitą galima įvesti kaip kelių eilučių kvitą, kaip toje pačioje eilutėje nurodytą sąskaitą / korespondentinę sąskaitą arba kaip kombinaciją.

[![Viena eilutė](./media/same-line.png)](./media/same-line.png)
 
> [!IMPORTANT] 
> *  Atkreipkite dėmesį, kad vieno kvito aprašas NEAPIMA žurnalų pavadinimų, kurie yra nustatyti kaip **Tik vienas kvito numeris**, o vartotojas tada įveda kvitą, kuris apima tik DK sąskaitų tipus.  Šiame dokumente „vienas kvitas“ reiškia, kad viename kvite yra daugiau nei vienas tiekėjas, klientas, bankas, ilgalaikis turtas arba projektas. 

-   Jei nenurodyta korespondentinė sąskaita, įveskite kelių eilučių kvitą.

[![Kelių eilučių kvitas](./media/Multi-line.png)](./media/Multi-line.png)

-   Įveskite kvitą, kuriame nurodomas sąskaitos ir poslinko sąskaitos papildomos knygos sąskaitos tipas, pavyzdžiui, tiekėjas / tiekėjas, klientas / klientas, tiekėjas / klientas arbas bankas / bankas.

[![Papildomos knygos kvitas](./media/subledger.png)](./media/subledger.png)

<a name="issues-with-one-voucher"></a>Su funkcija Vienas kvitas susijusios problemos
=======================

Naudojantis funkcija Vienas kvitas iškyla problemų atsiskaitant, skaičiuojant mokesčius, derinant papildomą knygą su didžiąja knyga, rengiant finansines ataskaitas ir ne tik. (Pavyzdžiui, norėdami gauti daugiau informacijos apie atsiskaitant galinčias iškilti problemas, žr. [Vienas kvitas su keliais kliento arba tiekėjo įrašais](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records).) Norint, kad šie procesai ir ataskaitos tinkamai veiktų, reikia nurodyti operacijos informaciją. Nors kai kurie scenarijai gali veikti tinkamai, remiantis jūsų organizacijos sąranka, dažnai iškyla problemų viename kvite įvedant kelias operacijas.

Pavyzdžiui, registruojate toliau nurodytą kelių eilučių kvitą.

[![Pavyzdys](./media/example.png)](./media/example.png)

Po to darbo srityje **Finansinės įžvalgos** sugeneruojate ataskaitą **Išlaidos pagal tiekėją**. Ataskaitoje išlaidų sąskaitos balansai priskiriami tiekėjo grupei ir tiekėjui. Generuodama ataskaitą sistema negali nustatyti, kurios tiekėjų grupės / tiekėjai patyrė 250,00 vienetų apimties išlaidas. Kadangi trūksta operacijos informacijos, sistema daro prielaidą, kad visas 250,00 vienetų apimties išlaidas patyrė pirmas kvite nurodytas tiekėjas. Tada rodoma, kad 250,00 vienetų apimties išlaidos, kurios įtrauktos į pagrindinės sąskaitos 600120 balansą, priskirtos tai tiekėjų grupei / tiekėjui. Labai tikėtina, kad pirmasis tiekėjas kvite nurodytas neteisingai, todėl ataskaita neteisinga.

[![Išlaidos](./media/expenses.png)](./media/expenses.png)

<a name="the-future-of-one-voucher"></a>Funkcijos Vienas kvitas ateitis
=========================

Dėl pirmiau nurodytų problemų funkcija Vienas kvitas naudotis nebebus galima. Tačiau, kadangi esama nuo šios funkcijos priklausančių funkcinių spragų, funkcija kurį laiką dar bus naudojama. Laikysimės toliau nurodyto tvarkaraščio. 

- **2018 m. pavasario leidimas** – pagal numatytuosius parametrus naudojantis didžiosios knygos parametru funkcija bus išjungta. Tačiau galite įjungti funkciją, jei jūsų organizacijoje yra scenarijus, kuriame esama toliau šioje temoje nurodytų verslo scenarijų spragų.

  -   Jei klientas turi verslo scenarijų, pagal kurį funkcija Vienas kvitas nereikalinga, neįjunkite funkcijos. Jei bus naudojamasi šia funkcija, negalėsime išspręsti toliau šioje temoje nurodytose srityse kylančių „klaidų“, net jei esama kitų sprendimų.

  -   Nebenaudokite funkcijos Vienas kvitas integracijoms į „Microsoft Dynamics 365 Finance and Operations“, nebent būtų reikalinga naudoti šią funkciją dėl vienos iš funkcinių spragų.

- **2018 m. rudens ir vėlesni leidimai** – funkcinės spragos bus užpildytos. Užpildžius funkcines spragas funkcija Vienas kvitas išjungiama visam laikui.

- > [!IMPORTANT]
  > Atkreipkite dėmesį, kad parinktis **Tik vienas kvito numeris** NEBUVO pašalinta iš žurnalo pavadinimo sąrankos.  Ši parinktis vis dar palaikoma, kai kvite nurodyti tik DK sąskaitų tipai.  Klientai turi būti atsargūs naudodami šį parametrą, nes kvitas nebus registruojamas, jei jie naudos parinktį **Tik vienas kvito numeris** ir įves daugiau nei vieną klientą, tiekėją, banką, ilgalaikį turtą arba projektą.  Be to, klientai vis dar gali įvesti antrinės DK sąskaitų tipus, pvz., mokėjimą naudojant vieną kvitą, kuriame nurodyti sąskaitų tipai Tiekėjas / Bankas.  

<a name="why-use-one-voucher"></a>Kodėl verta naudotis funkcija Vienas kvitas?
====================

Remdamiesi pokalbiais su klientais parengėme toliau pateikiamą sąrašą, kuriame išvardijami scenarijai, kai klientai naudojasi funkcija Vienas kvitas arba nurodomos priežastys, kodėl jie šia funkcija naudojasi. Kai kurių iš šių verslo reikalavimų galima laikytis tik naudojant funkciją Vienas kvitas. Tačiau daugelis alternatyvių scenarijų gali atitikti tuos pačius verslo reikalavimus.

<a name="scenarios-that-require-one-voucher"></a>Scenarijai, pagal kuriuos reikia naudotis funkcija Vienas kvitas
----------------------------------

Toliau nurodytus scenarijus galima įvykdyti tik naudojantis funkcija Vienas kvitas. 2018 m. rudens ir vėlesniuose leidimuose funkcinės spragos bus užpildytos pristatant kitas funkcijas.

-   **Tiekėjo arba kliento mokėjimų registravimas banko sąskaitoje suvestinės forma**

    -   Organizacija perduoda tiekėjų ir sumų sąrašą savo bankui, o bankas naudoja šį sąrašą apmokėdamas sumas tiekėjams organizacijos vardu. Banko sąskaitoje bankas registruoja mokėjimų sumą kaip vieną išėmimą.

>   Tiekėjų mokėjimų suvestinė palaikoma tik naudojant funkciją Vienas kvitas. Kiekvienas tiekėjas įvedamas kaip atskira eilutė, kad duomenys išliktų papildomoje mokėtinų sumų knygoje, bet visų mokėjimų sumų suvestinė perkeliama į vieną banko sumos eilutę. Todėl papildomoje banko knygoje išėmimas rodomas kaip viena sumų suvestinė.

-   Organizacija deponuoja klientų mokėjimus arba bankas deponuoja klientų mokėjimus organizacijos vardu ir depozitas rodomas banko sąskaitoje kaip fiksuota suma.

>   Kliento mokėjimų suvestinė paprastai palaikoma naudojantis depozito funkcija. Tačiau jei naudojate „tarpinį“ mokėjimo būdą, šis scenarijus palaikomas tik naudojantis funkcija Vienas kvitas. Klientų mokėjimai įvedami tokiu pat būdu kaip aprašyta sudaroma tiekėjų mokėjimų suvestinė.

-   **Verslo įvykio operacijų grupavimui skirtas mechanizmas**

    -   Organizacija turi vieną verslo įvykį, kuris įjungia kelias operacijas. Tačiau apskaitos skyrius nori peržiūrėti apskaitos įrašus kartu, kad būtų užtikrinama geresnė kontrolė.

>   Jei organizacija turi kartu peržiūrėti verslo įvykio apskaitos įrašus, ji turi naudotis funkcija Vienas kvitas. 

- **Šaliai būdingos funkcijos**

  -   Šiuo metu naudojantis Lenkijos vieno administravimo dokumento (SAD) funkcija reikia naudoti vieną kvitą. Kol nebus galima naudotis šios funkcijos grupavimo parinktimi, turite ir toliau naudotis funkcija Vienas kvitas. Gali būti papildomų šaliai būdingų funkcijų, kuriomis naudojantis reikia naudotis funkcija Vienas kvitas.

- **Kliento išankstinio mokėjimo žurnalas, kuriame keliose „eilutėse“ nurodyti mokesčiai**

  -   Klientas atlieka išankstinį užsakymo apmokėjimą ir užsakymo eilutėse nurodyti skirtingi mokesčiai, kurie turi būti įrašyti atliekant išankstinį mokėjimą. Išankstinis kliento mokėjimas yra viena operacija, kuri imituoja užsakymo eilutes, kad kiekvienoje sumos eilutėje būtų galima įrašyti atitinkamą mokestį.

Pagal šį scenarijų viename kvite nurodyti klientai yra tas pats klientas, nes operacija imituoja kliento užsakymo eilutes. Išankstinis mokėjimas turi būti įvestas viename kvite, nes mokesčių skaičiavimas turi būti atliekamas kliento atlikto vieno mokėjimo „eilutėse“.

-   **Ilgalaikio turto priežiūra: nusidėvėjimas atgaline data, turto skaidymas, nusidėvėjimo skaičiavimas likviduojant**

Atliekant toliau nurodytas ilgalaikio turto operacijas viename kvite taip pat sukuriamos kelios operacijos.
-   Atliekamas papildomas turto įsigijimas ir skaičiuojamas nusidėvėjimas „atgaline data“.
-   Turtas suskaidomas.
-   Įjungiamas parametras, naudojamas norint apskaičiuoti nusidėvėjimą likviduojant, po to turtas likviduojamas.

<a name="scenarios-that-dont-require-one-voucher"></a>Scenarijai, kai funkcija Vienas kvitas naudotis nereikia
----------------------------------------

Toliau nurodytus scenarijus galima įvykdyti kitais būdais ir neturėtų būti naudojamasi funkcija Vienas kvitas.

-   **Kliento mokėjimų registravimas banko sąskaitoje suvestinės forma**

Organizacija deponuoja klientų mokėjimus arba bankas deponuoja klientų mokėjimus organizacijos vardu ir depozitas rodomas banko sąskaitoje kaip fiksuota suma.

Kai nesinaudojama tarpiniu mokėjimo būdu, kliento mokėjimų suvestinė palaikoma naudojantis depozito funkcija.

-   **Užskaita**

Atliekant užskaitą tiekėjo ir kliento balansai užskaitomi tarpusavyje vienas per kitą, nes tiekėjas ir klientas yra ta pati šalis. Taikant šį metodą sumažėja organizacijos ir kliento / tiekėjo šalies apsikeičiamų pinigų srautai.

Užskaitą galima atlikti atskiruose kvituose įvedant didėjimą ir mažėjimą ir registruojant DK tarpuskaitos poslinkį.

-   **Suvestinės registravimas didžiojoje knygoje**

Organizacijos didžiosiose knygose dažnai nori registruoti suvestines, kad sumažintų duomenų kiekį. Tačiau organizacijas paprastai vis tiek reikalauja, kad būtų išlaikomi operacijų duomenys. Kai registruojama vieno kvito suvestinė, operacijų duomenys nežinomi ir jų negalima tavrkyti.

   -   Kadangi šiuo metu operacijų duomenų tvarkyti negalima, rekomenduojame registruojant suvestinę funkcija Vienas kvitas nesinaudoti.
   -   Kai funkcija Vienas kvitas bus nebepalaikoma, žurnaluose galime įdiegti sistemas Šaltinio dokumentas ir Apskaita. Tada, naudojantis šiomis sistemomis, bus tvarkomi operacijų duomenys ir palaikomas suvestinės išsaugojimas didžiojoje knygoje.

-   **Kelių neregistruotų mokėjimų atlikimas toje pačioje sąskaitoje faktūroje**

Šiuo scenarijumi paprastai naudojasi mažmeninės prekybos organizacijos, kai norėdami atsiskaityti už pirkinius klientai gali naudotis keliais mokėjimo būdais. Pagal šį scenarijų organizacija turi galėti įrašyti kelis neužregistruotus mokėjimus ir apmokėti juos pagal kliento parengtą sąskaitą faktūrą.

Naudojantis nauja funkcija, kuri buvo įtraukta į „Microsoft Dynamics 365 for Operations“ versiją 1611 (2016 m. lapkritį) vienoje sąskaitoje faktūroje galima atlikti kelis neregistruotus mokėjimus. Viename kvite jau nebebūtina įvesti kelių klientų mokėjimų.

-   **Banko išrašo operacijų importavimas**

Bankai dažnai atlieka ir gauna mokėjimus organizacijos vardu, o šios operacijos įrašomos programoje „Finance and Operations“ naudojant iš banko gautą failą. Organizacijos dažnai nori, kad šios operacijos būtų sugrupuotos faile naudojant banko išrašo numerį. Kadangi banko išraše rodoma išsami informacija apie kiekvieną operaciją, papildomoje banko knygoje suvestinė nebūtina.

Operacijas galima grupuoti naudojant kitus žurnalo laukus, pavyzdžiui, žurnalo paketo numerį arba dokumento numerį.

-   **Perkelti balansus**

Organizacijai gali tekti perkelti balansą iš vieno tiekėjo kitam tiekėjui, kadangi įvyko klaida arba kitas tiekėjas perėmė atsakomybę. Tokio tipo perkėlimai taip pat atliekami sąskaitos tipams, pvz., klientų ir banko sąskaitoms.

Balanso perkėlimas iš vienos sąskaitos (tiekėjo, kliento, banko sąskaitos ir t. t.) į kitą sąskaitą gali būti atliekamas naudojant atskirus kvitus, o poslinkį galima užregistruoti DK tarpuskaitoje.

-   **Pradžios balansų įvedimas**

Organizacijos dažnai įveda papildomos knygos sąskaitų (tiekėjų, klientų, ilgalaikio turto ir t. t.) pradžios balansus kaip vieno kvito operaciją. Kiekvienos papildomos knygos sąskaitos pradžios balansus galima įvesti kaip atskirus kvitus, o poslinkį galima užregistruoti DK tarpuskaitoje.

-   **Užregistruotų klientų arba tiekėjų dokumentų apskaitos įrašo koregavimas**

Organizacijai gali tekti koreguoti užregistruotos SF apskaitos įraše nurodytą gautinų arba mokėtinų sumų DK sąskaitą, tačiau ši SF negali būti atšaukta arba koreguojama naudojant kitą mechanizmą.

Jei būtina koreguoti gautinų arba mokėtinų sumų DK sąskaitą, tai turi būti atliekama tiesiogiai DK sąskaitoje. Koregavimo negalima atlikti registruojant per tiekėją arba klientą. Taikant šį metodą koregavimus reikia atlikti „prastovos laiku“, kad DK sąskaitoje trumpam būtų galima atlikti neautomatinį įvedimą.

-   **„Sistema tai leidžia“**

Organizacijos dažnai naudojasi funkcija Vienas kvitas tik todėl, kad sistema leidžia ja naudotis, nesuprasdamos, ką tai reiškia.

