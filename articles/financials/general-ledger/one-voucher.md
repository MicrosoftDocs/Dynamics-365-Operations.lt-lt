---
title: Vienas kvitas
description: Naudodamiesi finansinių žurnalų (bendrojo žurnalo, ilgalaikio turto žurnalo, tiekėjo mokėjimų žurnalo ir t. t.) funkcija Vienas kvitas vieno kvito kontekste galite įvesti kelias papildomos knygos operacijas.
author: kweekley
manager: AnnBe
ms.date: 11/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.openlocfilehash: ada04948c4775091091cc30664dd7d9405b4f9da
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553205"
---
# <a name="one-voucher"></a>Vienas kvitas

[!include [banner](../includes/banner.md)]


## <a name="what-is-one-voucher"></a>Kas yra „Vienas kvitas“?

Naudodamiesi esama finansinių žurnalų (bendrojo žurnalo, ilgalaikio turto žurnalo, tiekėjo mokėjimų žurnalo ir t. t.) funkcija vieno kvito kontekste galite įvesti kelias papildomos knygos operacijas (kliento, tiekėjo, ilgalaikio turto, projekto ir banko). „Microsoft“ šią funkcija vadina *Vienas kvitas*. Vieną kvitą galima sukurti vienu iš toliau nurodytų būdų.

- Nustatykite žurnalo pavadinimą (**Didžioji knyga** \> **Žurnalo sąranka** \> **Žurnalų pavadinimai**), kad laukui **Naujas kvitas** būtų nustatytas parametras **Tik vienas kvito numeris**. Nuo šiol kiekviena į žurnalą įtraukta eilutė įtraukiama tame pačiame kvite. Dėl to tą patį kvitą galima įvesti kaip kelių eilučių kvitą, kaip toje pačioje eilutėje nurodytą sąskaitą / korespondentinę sąskaitą arba kaip kombinaciją.

    [![Viena eilutė](./media/same-line.png)](./media/same-line.png)

    > [!IMPORTANT]
    > Vieno kvito aprašas **neapima** atvejų, kai žurnalų pavadinimams nustatytas parametras **Tik vienas kvito numeris**, tačiau vartotojas tada įveda kvitą, apimantį tik DK sąskaitų tipus. Šioje temoje išsireiškimas „vienas kvitas“ reiškia, kad viename kvite yra daugiau nei vienas tiekėjas, klientas, bankas, ilgalaikis turtas arba projektas.

- Jei nenurodyta korespondentinė sąskaita, įveskite kelių eilučių kvitą.

    [![Kelių eilučių kvitas](./media/Multi-line.png)](./media/Multi-line.png)

- Įveskite kvitą, kuriame nurodomas sąskaitos ir poslinko sąskaitos papildomos knygos sąskaitos tipas, pavyzdžiui, **Tiekėjas**/**Tiekėjas**, **Klientas**/**Klientas**, **Tiekėjas**/**Klientas** arba **Bankas**/**Bankas**.

    [![Papildomos knygos kvitas](./media/subledger.png)](./media/subledger.png)

## <a name="issues-with-one-voucher"></a>Su funkcija Vienas kvitas susijusios problemos

Naudojantis funkcija Vienas kvitas iškyla problemų atsiskaitant, skaičiuojant mokesčius, atšaukiant operaciją, derinant papildomą knygą su didžiąja knyga, rengiant finansines ataskaitas ir ne tik. (Norėdami gauti daugiau informacijos apie atsiskaitant galinčias iškilti problemas (pavyzdžiui), žr. [Vienas kvitas su keliais kliento arba tiekėjo įrašais](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records).) Norint, kad šie procesai ir ataskaitos tinkamai veiktų, reikia nurodyti operacijos informaciją. Nors kai kurie scenarijai gali veikti tinkamai, priklausomai nuo jūsų organizacijos sąrankos, dažnai iškyla problemų viename kvite įvedant kelias operacijas.

Pavyzdžiui, registruojate toliau nurodytą kelių eilučių kvitą.

[![Pavyzdys](./media/example.png)](./media/example.png)

Po to darbo srityje **Finansinės įžvalgos** sugeneruojate ataskaitą **Išlaidos pagal tiekėją**. Šioje ataskaitoje išlaidų sąskaitos balansai sugrupuoti pagal tiekėjo grupę, o tada pagal tiekėją. Kai ataskaita sugeneruojama, sistema negali nustatyti, kurios tiekėjų grupės / tiekėjai patyrė 250,00 vienetų apimties išlaidų. Kadangi trūksta operacijos informacijos, sistema daro prielaidą, kad visas 250,00 vienetų apimties išlaidas patyrė pirmas kvite nurodytas tiekėjas. Todėl 250,00 vienetų apimties išlaidos, kurios įtrauktos į pagrindinės sąskaitos 600120 balansą, rodomos toje tiekėjų grupėje / tiekėjo srityje. Tačiau labai tikėtina, kad pirmasis tiekėjas kvite nurodytas neteisingai. Dėl to gali būti, kad ataskaita yra neteisinga.

[![Išlaidos](./media/expenses.png)](./media/expenses.png)

## <a name="the-future-of-one-voucher"></a>Funkcijos Vienas kvitas ateitis

Dėl pirmiau minėtų problemų funkcija Vienas kvitas naudotis nebebus galima. Tačiau esama nuo šios funkcijos priklausančių funkcinių spragų, todėl nebus taip, kad funkcija visiškai negalėtumėte naudotis visą laiką. Bus naudojamas toliau nurodytas grafikas.

- **2018 m. pavasario leidimas** – pagal numatytuosius parametrus, naudojantis parametru **Leisti kelias vieno kvito operacijas**, pasiekiamu skirtuke **Bendra**, kuris pateikiamas puslapyje **DK parametrai**, funkcija bus išjungta. Tačiau, jei jūsų organizacijoje yra scenarijus, kuriame yra viena iš šioje temoje nurodytų funkcinių spragų, funkciją įjungti galite.

    - Jei klientai turi verslo scenarijų, pagal kurį funkcija Vienas kvitas nereikalinga, jie šios funkcijos įjungti neturėtų. Jei bus naudojamasi šia funkcija, „Microsoft“ negalės išspręsti toliau šioje temoje nurodytose srityse kylančių klaidų, net jei esama kitų sprendimų.
    - Nebenaudokite funkcijos Vienas kvitas integracijoms į „Microsoft Dynamics 365 for Finance and Operations“, nebent būtų reikalinga naudoti šią funkciją dėl vienos iš funkcinių spragų.

- **Vėlesni leidimai** – visos funkcinės spragos bus užpildytos. **Užpildžius funkcines spragas ir įtraukus naujų funkcijų, iki funkcijos Vienas kvitas išjungimo visam laikui bus likę bent metai**, nes klientams ir nepriklausomiems programinės įrangos tiekėjams (ISV) reikia palikti pakankamai laiko tam, kad jie galėtų prisitaikyti prie naujų funkcijų. Pavyzdžiui, jiems gali reikėti atnaujinti savo verslo procesus, objektus ir integracijas.

> [!IMPORTANT]
> Parinktis **Tik vienas kvito numeris** **nebuvo** pašalinta iš žurnalo pavadinimo sąrankos. Ši parinktis vis dar palaikoma, kai kvite nurodyti tik DK sąskaitų tipai. Klientai turi būti atsargūs naudodami šį parametrą, nes kvitas nebus registruojamas, jei naudojant parinktį **Tik vienas kvito numeris** jie įves daugiau nei vieną klientą, tiekėją, banką, ilgalaikį turtą arba projektą. Be to, klientai vis dar gali įvesti mišrius antrinės DK sąskaitos tipus, pvz., mokėjimą naudojant vieną kvitą, kuriame nurodyti sąskaitų tipai **Tiekėjas**/**Bankas**.

## <a name="why-use-one-voucher"></a>Kodėl verta naudotis funkcija Vienas kvitas?

Remdamasi pokalbiais su klientais, „Microsoft“ parengė toliau pateikiamą sąrašą, kuriame išvardijami scenarijai, kai klientai naudojasi funkcija Vienas kvitas arba nurodomos priežastys, kodėl jie šia funkcija naudojasi. Kai kurių iš šių verslo reikalavimų galima laikytis tik naudojant funkciją Vienas kvitas. Tačiau daugelis alternatyvių scenarijų gali atitikti tuos pačius verslo reikalavimus.

### <a name="scenarios-that-require-one-voucher"></a>Scenarijai, pagal kuriuos reikia naudotis funkcija Vienas kvitas

Toliau nurodytus scenarijus galima įvykdyti tik naudojantis funkcija Vienas kvitas. Jei jūsų organizacijoje naudojamas kuris nors iš šių scenarijų, turite įgalinti parinktį, leisiančią į vieną kvitą įversti keletą operacijų. Tą padaryti galite pakeitę parametrą **Leisti kelias vieno kvito operacijas**, pateiktą puslapyje **DK parametrai**. Vėlesniuose leidimuose funkcinės spragos bus užpildytos pristatant kitas funkcijas.

### <a name="post-vendor-or-customer-payments-in-summary-form-to-a-bank-account"></a>Tiekėjo arba kliento mokėjimų registravimas banko sąskaitoje suvestinės forma

**Scenarijus** Organizacija perduoda tiekėjų ir sumų sąrašą savo bankui, o bankas naudoja šį sąrašą apmokėdamas sumas tiekėjams organizacijos vardu. Banko sąskaitoje bankas registruoja mokėjimų sumą kaip vieną išėmimą.

Tiekėjų mokėjimų suvestinė palaikoma tik naudojant funkciją Vienas kvitas. Kiekvienas tiekėjas įvedamas atskiroje eilutėje, kad būtų galima tvarkyti papildomoje knygoje Mokėtinos sumos pateiktą išsamią informaciją. Tačiau visų mokėjimų sumų suvestinė perkeliama į vieną banko sumos eilutę. Todėl papildomoje banko knygoje išėmimas rodomas kaip viena sumų suvestinė.

**Scenarijus** Organizacija deponuoja klientų mokėjimus arba bankas deponuoja klientų mokėjimus organizacijos vardu ir depozitas rodomas banko sąskaitoje kaip fiksuota suma.

Kliento mokėjimų suvestinė paprastai palaikoma naudojantis depozito funkcija. Tačiau jei naudojate „tarpinį“ mokėjimo būdą, šis scenarijus palaikomas tik naudojantis funkcija Vienas kvitas. Klientų mokėjimai įvedami tokiu pat būdu kaip aprašyta sudaroma tiekėjų mokėjimų suvestinė.

### <a name="mechanism-to-group-transactions-from-a-business-event"></a>Verslo įvykio operacijų grupavimui skirtas mechanizmas

**Scenarijus** Organizacija turi vieną verslo įvykį, kuris įjungia kelias operacijas. Tačiau apskaitos skyrius nori peržiūrėti apskaitos įrašus kartu, kad būtų užtikrinama geresnė kontrolė.

Jei organizacija turi kartu peržiūrėti verslo įvykio apskaitos įrašus, ji turi naudotis funkcija Vienas kvitas. 

### <a name="country-specific-features"></a>Šaliai būdingos funkcijos

**Scenarijus** Šiuo metu naudojantis Lenkijos vieno administravimo dokumento (SAD) funkcija reikia naudoti vieną kvitą. Kol nebus galima naudotis šios funkcijos grupavimo parinktimi, turite ir toliau naudotis funkcija Vienas kvitas. Gali būti papildomų šaliai būdingų funkcijų, kuriomis naudojantis reikia naudotis funkcija Vienas kvitas.

### <a name="customer-prepayment-payment-journal-that-has-taxes-on-multiple-lines"></a>Kliento išankstinio mokėjimo žurnalas, kuriame keliose „eilutėse“ nurodyti mokesčiai

Pagal šį scenarijų viename kvite nurodyti klientai yra tas pats klientas, nes operacija imituoja kliento užsakymo eilutes. Išankstinis mokėjimas turi būti įvestas viename kvite, nes mokesčių skaičiavimas turi būti atliekamas kliento atlikto vieno mokėjimo „eilutėse“.

### <a name="customer-reimbursement"></a>Kliento kompensacija

**Scenarijus** Klientas atlieka išankstinį užsakymo apmokėjimą, o užsakymo eilutėse nurodyti skirtingi mokesčiai, kurie turi būti įrašyti atliekant išankstinį mokėjimą. Išankstinis kliento mokėjimas yra viena operacija, kuri imituoja užsakymo eilutes, kad kiekvienoje sumos eilutėje būtų galima įrašyti atitinkamą mokestį.

Jei periodinė kompensacijos užduotis vykdoma modulyje Gautinos sumos, sukuriama operacija, kad balansą būtų galima perkelti iš kliento srities į tiekėjo sritį. Esant šiam scenarijui, funkciją Vienas kvitas naudoti reikia, kad klientui būtų galima išmokėti kompensaciją.

### <a name="fixed-asset-maintenance-catch-up-depreciation-split-asset-calculate-depreciation-on-disposal"></a>Ilgalaikio turto priežiūra: nusidėvėjimas atgaline data, turto skaidymas, nusidėvėjimo skaičiavimas likviduojant
Atliekant toliau nurodytas ilgalaikio turto operacijas, viename kvite taip pat sukuriamos kelios operacijos.

- Atliekamas papildomas turto įsigijimas ir skaičiuojamas nusidėvėjimas atgaline data.
- Turtas suskaidomas.
- Įjungiamas parametras, naudojamas norint apskaičiuoti nusidėvėjimą likviduojant, po to turtas likviduojamas.
- Turto paslaugos data yra ankstesnė nei įsigijimo data. Dėl to registruojamas nusidėvėjimo koregavimas.

### <a name="bills-of-exchange-and-promissory-notes"></a> Įsakomieji ir paprastieji vekseliai
Įsakomųjų ir paprastųjų vekselių atveju funkciją Vienas kvitas naudoti reikia, nes atliekant operacijas kliento arba tiekėjo balansas, remiantis mokėjimo būsena, iš vienos DK sąskaitos Gautinos sumos / Mokėtinos sumos perkeliamos į kitą.

## <a name="scenarios-that-dont-require-one-voucher"></a>Scenarijai, kai funkcija Vienas kvitas naudotis nereikia

Toliau nurodytus scenarijus galima įvykdyti kitais būdais, nenaudojant funkcijos Vienas kvitas.

### <a name="post-customer-payments-in-summary-form-to-the-bank-account"></a>Kliento mokėjimų registravimas banko sąskaitoje suvestinės forma

Organizacija deponuoja klientų mokėjimus arba bankas deponuoja klientų mokėjimus organizacijos vardu ir depozitas rodomas banko sąskaitoje kaip fiksuota suma.

Kai mokėjimo būdui netaikoma tarpinė parinktis, kliento mokėjimų suvestinė palaikoma naudojantis depozito funkcija.

### <a name="netting"></a>Užskaita

Atliekant užskaitą tiekėjo ir kliento balansai užskaitomi tarpusavyje vienas per kitą, nes tiekėjas ir klientas yra ta pati šalis. Taikant šį metodą sumažėja organizacijos ir kliento / tiekėjo šalies apsikeičiamų pinigų srautai.

Užskaitą galima atlikti atskiruose kvituose įvedant didėjimą ir mažėjimą, tada užregistravus DK tarpuskaitos poslinkį.

### <a name="post-in-summary-to-the-general-ledger"></a>Suvestinės registravimas didžiojoje knygoje

Organizacijos didžiosiose knygose atlikti registraciją dažnai nori suvestinės formoje, kad sumažėtų duomenų kiekis. Tačiau tokios organizacijos paprastai vis tiek reikalauja, kad būtų išlaikomi operacijos duomenys. Kai registracija atliekama suvestinės formoje naudojant vieną kvitą, operacijų duomenys nežinomi ir jų negalima tvarkyti.

- Kadangi šiuo metu operacijų duomenų tvarkyti negalima, rekomenduojame, kad atlikdama registraciją suvestinės formoje organizacija **nenaudotų** funkcijos Vienas kvitas.
- Kai funkcija Vienas kvitas bus pašalinta, žurnaluose bus galima įdiegti sistemas Šaltinio dokumentas ir Apskaita. Tada, naudojantis šiomis sistemomis, bus tvarkomi operacijų duomenys ir palaikomas suvestinės išsaugojimas didžiojoje knygoje.


### <a name="settle-multiple-unposted-payments-to-the-same-invoice"></a>Kelių neregistruotų mokėjimų atlikimas toje pačioje sąskaitoje faktūroje

Šiuo scenarijumi paprastai naudojasi mažmeninės prekybos organizacijos, kai norėdami atsiskaityti už pirkinius klientai gali naudotis keliais mokėjimo būdais. Pagal šį scenarijų organizacija turi galėti įrašyti kelis neužregistruotus mokėjimus ir apmokėti juos pagal kliento parengtą sąskaitą faktūrą.

Naudojantis nauja funkcija, kuri buvo įtraukta į „Microsoft Dynamics 365 for Operations“ versiją 1611 (2016 m. lapkritį) vienoje sąskaitoje faktūroje galima atlikti kelis neregistruotus mokėjimus. Viename kvite jau nebebūtina įvesti kelių klientų mokėjimų.

### <a name="import-bank-statement-transactions"></a>Banko išrašo operacijų importavimas

Bankai dažnai atlieka ir gauna mokėjimus organizacijos vardu, o šios operacijos įrašomos programoje „Finance and Operations“ naudojant iš banko gautą failą. Organizacijos dažnai nori, kad šios operacijos būtų sugrupuotos faile naudojant banko išrašo numerį. Kadangi banko išraše rodoma išsami informacija apie kiekvieną operaciją, papildomoje banko knygoje suvestinė nebūtina.

Operacijas galima grupuoti naudojant kitus žurnalo laukus, pavyzdžiui, žurnalo paketo numerį arba dokumento numerį.


### <a name="transfer-balances"></a>Perkelti balansus

Organizacijai gali tekti perkelti balansą iš vieno tiekėjo kitam tiekėjui, kadangi įvyko klaida arba kitas tiekėjas perėmė atsakomybę. Tokio tipo perkėlimai taip pat atliekami sąskaitos tipams, pvz., sąskaitoms **Klientas** ir **Bankas**.

Balanso perkėlimas iš vienos sąskaitos (tiekėjo, kliento, banko ir t. t.) į kitą sąskaitą gali būti atliekamas naudojant atskirus kvitus, o poslinkį galima užregistruoti DK tarpuskaitoje.

### <a name="enter-beginning-balances"></a>Pradžios balansų įvedimas

Organizacijos dažnai įveda papildomos knygos sąskaitų (tiekėjų, klientų, ilgalaikio turto ir t. t.) pradžios balansus kaip vieno kvito operaciją. Kiekvienos papildomos knygos sąskaitos pradžios balansus galima įvesti kaip atskirus kvitus, o poslinkį galima užregistruoti DK tarpuskaitoje.

### <a name="correct-the-accounting-entry-of-a-posted-customer-or-vendor-document"></a>Užregistruotų klientų arba tiekėjų dokumentų apskaitos įrašo koregavimas

Organizacijai gali tekti koreguoti užregistruotos SF apskaitos įraše nurodytą gautinų arba mokėtinų sumų DK sąskaitą, tačiau ši SF negali būti atšaukta arba koreguojama naudojant kitą mechanizmą.

Jei būtina koreguoti Gautinų arba Mokėtinų sumų DK sąskaitą, tai turi būti atliekama tiesiogiai DK sąskaitoje. Koregavimo negalima atlikti registruojant per tiekėją arba klientą. Taikant šį metodą koregavimus reikia atlikti „prastovos laiku“, kad DK sąskaitoje trumpam būtų galima atlikti neautomatinį įvedimą.

### <a name="the-system-allows-it"></a>„Sistema tai leidžia“

Organizacijos dažnai naudojasi funkcija Vienas kvitas tik todėl, kad sistema leidžia ja naudotis, nesuprasdamos, ką tai reiškia.