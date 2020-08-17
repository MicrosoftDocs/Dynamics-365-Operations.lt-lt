---
title: Tiekėjo mokėjimo pasiūlymų automatizavimas
description: Šioje temoje paaiškinama, kaip organizacijos, kurios moka tiekėjams pagal pasikartojantį grafiką, gali automatizuoti tiekėjo mokėjimo pasiūlymų kūrimo procesą.
author: kweekley
manager: AnnBe
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: a1e3305bff99fa39240176ac9fc7aaee84b98e6c
ms.sourcegitcommit: be51e892003778e71b67fb409a8e16965c89b5ac
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/23/2020
ms.locfileid: "3618416"
---
# <a name="automate-vendor-payment-proposals"></a>Tiekėjo mokėjimo pasiūlymų automatizavimas

[!include [banner](../includes/banner.md)]

Dabar organizacijos, kurios moka tiekėjams pagal pasikartojantį grafiką, gali automatizuoti tiekėjo mokėjimo pasiūlymų kūrimo procesą. Tiekėjo mokėjimo pasiūlymų automatizuoti procesai apibrėžia šią informaciją:

- kada vykdomi mokėjimo pasiūlymai;
- pagal kokius kriterijus pasirenkamos sąskaitos faktūros, kurios turi būti apmokėtos;
- į kurį tiekėjo mokėjimų žurnalą saugomi susiję mokėjimai.

Mokėjimo pasiūlymų automatizuoti procesai neregistruoja mokėjimų automatiškai. Todėl galite ir toliau patvirtinti sukurtus mokėjimus naudodami tuos pačius tikrinimo ir darbo eigos procesus.

## <a name="define-the-occurrence-of-vendor-payment-proposals"></a>Tiekėjo mokėjimo pasiūlymų įvykio nustatymas

Tiekėjo mokėjimo pasiūlymo automatizavimo procesuose naudojama procesų automatizavimo sistema. Skirtingi verslo procesai naudoja šią sistemą, kad nustatytų pasirinkto proceso įvykį. Tiekėjo mokėjimo pasiūlymų automatizavimo procesai pasiekiami dalyje **Mokėtinos sumos \> Mokėjimų sąranka \> Procesų automatizavimas**.

Pirmiausia naudokite automatizavimo parinktį **Sukurti naują procesą** ir pasirinkite **Tiekėjo mokėjimo pasiūlymas**. Vedlys padės jums nustatyti tiekėjo mokėjimo pasiūlymą.

## <a name="general-page"></a>Puslapis „Bendra“

Vedlio puslapyje **Bendra** įveskite kuriamo tiekėjo mokėjimo pasiūlymo pavadinimą. Pavyzdžiui, jei mokate visiems vietiniams tiekėjams čekiu pirmadieniais, įveskite aprašomąjį pavadinimą, pvz., **Vietinis\_Čekiu**. Jūsų įvestas pavadinimas rodomas procesų automatizavimo savaitiniame rodinyje, darbo srityje **Tiekėjo mokėjimai**.

Tada nurodykite sukurto mokėjimų žurnalo savininką. Savininkas paprastai yra mokėtinų sumų (AP) mokėjimus tvarkantis darbuotojas, kuris yra atsakingas už mokėjimų žurnalą po to, kai jis sukuriamas.

Likę puslapio parametrai yra bendriniai ir naudojami norint nustatyti šios tiekėjo mokėjimo pasiūlymo versijos įvykių modelį. Pavyzdžiui, jei įvykis nustatytas pirmadienį atliekamiems mokėjimams čekiu, galite nustatyti, kad jis būtų vykdomas kas savaitę, ir pasirinkti pirmadienį kaip savaitės dieną, kurią jis vykdomas. Taip pat galite įvesti ankstyvą grafiko laiką, pvz., 2.00 val. ryto, kad automatizuotas procesas būtų užbaigtas prieš prasidedant kitai darbo dienai.

Svarbu suprasti, kad vedlys naudojamas siekiant nustatyti, kada tiekėjo mokėjimo pasiūlymas apdorojamas. Jūs nenustatote, kada tiekėjo mokėjimo pasiūlymai kuriami, spausdinami ir skelbiami. Savaitiniame rodinyje tiekėjo mokėjimo pasiūlymo proceso automatizavimo funkcija bus rodoma tomis dienomis, kurios pasirinktos įvykių modelyje.

Prireikus daugiau informacijos apie kitus puslapio **Bendra** laukus, žr. procesų automatizavimo dokumentaciją.

## <a name="vendor-payment-proposal-page"></a>Tiekėjo mokėjimo pasiūlymo puslapis

Kitas vedlio puslapis yra **Tiekėjo mokėjimo pasiūlymas**. Jis naudojamas nustatyti tiekėjo sąskaitų faktūrų, kurios turi būti apmokėtos, pasirinkimo kriterijus. Paprastai tos pačios pasirinktys yra tiekėjo mokėjimų žurnale esančiame mokėjimo pasiūlyme. Tačiau yra kelios išimtys. Pavyzdžiui, visos datos šiame puslapyje turi būti nustatytos kaip santykinės datos, nes mokėjimo pasiūlymo data pasikeičia kiekvieną kartą, kai vykdomas pasiūlymas.

### <a name="journal-name"></a>Žurnalo pavadinimas

Laukas **Žurnalo pavadinimas** apibrėžia žurnalo, kuriame yra kuriami tiekėjo mokėjimai, pavadinimą. Pagal tiekėjo mokėjimo pasiūlymo automatizavimo rezultatus bus sukurti mokėjimai nustatytame žurnale, bet žurnalas nebus registruojamas.

### <a name="from-date-and-to-date"></a>Pradžios data ir pabaigos data

Užuot nurodę pradžios ir pabaigos datas, kad pasirinktumėte sąskaitas faktūras pagal terminą arba mokėjimo nuolaidos datą, turite naudoti parinktį **Nustatyti pabaigos datos kriterijus** ir lauką **Pabaigos datos dienų skaičiaus koregavimas**, kad nustatytumėte pabaigos datą. Mokėjimo pasiūlymo automatizavimo procesuose nėra sąvokos „pradžios data“.

Pagal numatytuosius parametrus parinktis **Nustatyti pabaigos datos kriterijus** nustatyta kaip **Ne**. Jei naudojate šią numatytąją vertę, paleidus procesą bus pasirinktos visos mokėjimo sąskaitos faktūros, nes nebuvo nustatyta pabaigos data.

Jei nustatysite parinkties **Nustatyti pabaigos datos kriterijus** vertę **Taip**, naudokite lauką **Pabaigos datos dienų skaičiaus koregavimas**, kad nustatytumėte datą, kada pasirenkamos sąskaitos faktūros, kaip konkretų dienų skaičių prieš arba po proceso vykdymo datos. Skaičius gali būti teigiamas, neigiamas arba 0 (nulis). Tada sistema apmokės tas sąskaitas faktūras, kuriose terminai arba mokėjimo nuolaidų datos yra nurodytas dienų skaičius prieš arba po proceso vykdymo datos. Pavyzdžiui, visoms sąskaitoms faktūroms, kurios turi būti apmokėtos penktadienį arba ankščiau, mokėjimo seka trečiadienį sukuria mokėjimus čekiu visiems tiekėjams. Šiuo atveju nustatykite lauko **Pabaigos datos dienų skaičiaus koregavimas** vertę **2**. Kai mokėjimo pasiūlymo įvykis paleidžiamas trečiadienį, kovo 25 d., mokėjimui bus parinktos visos sąskaitos faktūros, kurių terminas arba mokėjimo nuolaidos data yra iki kovo 27 d.

### <a name="minimum-payment-date"></a>Minimali mokėjimo data

Minimali mokėjimo data yra anksčiausia data, kuri naudojama kuriant mokėjimus. Pirma turite nustatyti parinkties **Nustatyti minimalius mokėjimo datos kriterijus** vertę **Taip**. Šis parametras leidžia naudoti minimalios mokėjimo datos funkciją. Jei ši parinktis nustatyta į **Taip**, naudokite lauką **Minimalios mokėjimo datos dienų skaičiaus koregavimas**, kad nustatytumėte minimalią mokėjimo datą kaip konkretų dienų skaičių prieš arba po proceso vykdymo datos. Skaičius gali būti teigiamas, neigiamas arba 0 (nulis). Pavyzdžiui, mokėjimo seka generuoja mokėjimus trečiadienį, kad būtų įtraukti visi mokėjimai, kurių minimali mokėjimo data yra praėjęs pirmadienis. Šiuo atveju nustatykite lauką **Minimalios mokėjimo datos dienų skaičiaus koregavimas** vertę **–2**.

Čia pateikiamas pavyzdys, rodantis, kaip kartu veikia pabaigos datos ir minimalios mokėjimo datos laukai. Nustatyta, kad mokėjimo pasiūlymo automatizuotas procesas bus vykdomas trečiadienį. Laukas **Pabaigos datos dienų skaičiaus koregavimas** yra nustatomas kaip **1**, kad pabaigos data būtų nustatoma pagal terminą. Laukas **Minimalios mokėjimo datos dienų skaičiaus koregavimas** nustatomas į **–2**. Jei mokėjimo proceso automatizavimas prasideda trečiadienį, kovo 25 d., visos sąskaitos faktūros, kurių terminas yra iki kovo 26 d., bus įtrauktos į mokėjimo pasiūlymą. Mokėjimo pasiūlymai kuriami, kaip nurodyta toliau:

- Visų sąskaitų faktūrų, kurių terminas yra kovo 23 d. ar ankščiau, mokėjimo data bus kovo 23 d.
- Sąskaitų faktūrų, kurių terminas yra kovo 24 d., mokėjimo data bus kovo 24 d.
- Sąskaitų faktūrų, kurių terminas yra kovo 25 d., mokėjimo data bus kovo 25 d.
- Sąskaitų faktūrų, kurių terminas yra kovo 26 d., mokėjimo data bus kovo 26 d.

### <a name="summarized-payment-date"></a>Susumuoto mokėjimo data

Susumuoto mokėjimo data naudojama tik tada, kai sąskaitos faktūros apmokėjimo būdo laukas **Laikotarpis** yra nustatytas į **Bendras**. Jei apmokėjimo būdų laukas **Laikotarpis** nustatytas į **Bendras**, reikia nustatyti parinktį **Nustatyti susumuoto mokėjimo datos kriterijus** į **Taip**. Jei ši parinktis nustatyta į **Taip**, naudokite lauką **Susumuoto mokėjimo datos dienų skaičiaus koregavimas**, kad nustatytumėte susumuoto mokėjimo datą kaip konkretų dienų skaičių prieš arba po proceso vykdymo datos. Skaičius gali būti teigiamas, neigiamas arba 0 (nulis). Pavyzdžiui, ši seka generuoja mokėjimus trečiadienį, o įmonė nori sukurti susumuotą mokėjimą trečiadienį. Šiuo atveju nustatykite lauko **Susumuoto mokėjimo datos dienų skaičiaus koregavimas** vertę **0**.

### <a name="records-to-include"></a>Įtrauktini įrašai

Mokėjimo pasiūlymo filtro parinktis vis tiek galima nustatyti. Jeigu filtras nustatytas, filtro kriterijai nerodomi vedlio puslapyje. Tačiau juos galima peržiūrėti iš naujo atidarius filtrą.

Likę pasiūlymo laukai veikia taip pat kaip ir mokėjimo pasiūlymams tiekėjo mokėjimų žurnale. Norėdami gauti daugiau informacijos apie kitus laukus, žr. [Tiekėjo mokėjimų kūrimas naudojant mokėjimo pasiūlymą](create-vendor-payments-payment-proposal.md).

> [!NOTE]
> Kai kurie šaliai / regionui būdingi laukai ir kai kurie viešojo sektoriaus laukai dar neprieinami tiekėjo mokėjimo pasiūlymo automatizavimo procesuose.

Rekomenduojame pagal savo poreikius įvertinti, ar automatizavimas bus naudingas jūsų organizacijai.

## <a name="view-the-results-of-a-vendor-payment-proposal-automation"></a>Tiekėjo mokėjimo pasiūlymo automatizavimo rezultatų peržiūra

Po to, kai sukuriama tiekėjo mokėjimo pasiūlymo automatizavimo seka, kiekvieno mokėjimo įvykiai rodomi procesų automatizavimo savaitiniame rodinyje. Tiekėjo mokėjimams procesų automatizavimo savaitinis rodinys buvo pridėtas tiek prie darbo srities **Tiekėjo mokėjimai**, tiek prie puslapio **Procesų automatizavimas**.

[![Procesų automatizavimo savaitinis rodinys tiekėjo mokėjimų darbo srityje](./media/vendor-payment-proposal-1.png)](./media/vendor-payment-proposal-1.png)

Darbo srityje **Tiekėjo mokėjimai** esančiame proceso automatizavimo savaitiniame rodinyje rodomi tik tiekėjo mokėjimo pasiūlymų automatizavimo procesai. Joje parodomi visų juridinių subjektų, kurių saugos teises turi prisijungęs vartotojas, visi šios savaitės mokėjimų įvykiai. Pavyzdžiui, jei AP mokėjimus tvarkantis darbuotojas yra atsakingas už USMF ir USSI įmonių mokėjimus, jis / ji matys šių dviejų įmonių tiekėjo mokėjimo pasiūlymo automatizavimo įvykius, o kitų įmonių įvykių nematys.

[![USMF ir USSI įmonių procesų automatizavimo savaitinis rodinys](./media/vendor-payment-proposal-2.png)](./media/vendor-payment-proposal-2.png)

Kiekvienas atvejis nurodo įmonę, kurioje buvo arba bus sukurtas mokėjimų žurnalas. Jeigu mokėjimai sukuriami naudojant centralizuotus mokėjimus, rodoma įmonė yra įmonė, kurioje bus kuriami mokėjimai. Įvykis nebūtinai nurodo, kurios įmonės sąskaitos faktūros bus apmokamos.

Taip pat rodomas kiekvieno įvykio pavadinimas, kad būtų lengviau identifikuoti mokėjimo pasiūlymą.

Be to, rodoma kiekvieno įvykio būsena. Naudojamos šios būsenos:

- **Suplanuotas** – mokėjimo pasiūlymas suplanuotas, bet dar neįvykdytas.
- **Klaida** – mokėjimo pasiūlymas buvo vykdomas, bet įvyko klaida. Galite peržiūrėti klaidas paspaudę mygtuką **Peržiūrėti rezultatus**.
- **Baigta** – mokėjimo pasiūlymas buvo įvykdytas sėkmingai. Galite peržiūrėti mokėjimus pasirinkę saitą **Peržiūrėti mokėjimus**. Šis saitas atidaro mokėjimų žurnalą, kurį sukūrė įvykis.

Kai mokėjimai sukurti, galite peržiūrėti mokėjimų sumas žurnale. Visos sumos rodomos operacijos valiutomis. Pavyzdžiui, jei mokėjimų žurnale yra mokėjimų JAV doleriais ir Kanados doleriais, rodoma kiekvienos valiutos mokėjimo suma. 

Automatizuoto proceso metu sukurtą mokėjimų žurnalą galima panaikinti. Jei mokėjimas visiškai panaikinamas, įvyksta toliau išvardyti įvykiai:

- Savaitės procesų automatizavimo būsena išlieka **Baigta**.
- Proceso metu pašalinamos mokėjimų bendrosios sumos, o saitas **Peržiūrėti mokėjimus** pakeičiamas mygtuku **Peržiūrėti rezultatus**.
- Kai peržiūrėsite rezultatus, gausite pranešimą, kuriame nurodoma, kad pradinis žurnalas buvo panaikintas.

Panaikinus apmokėjimą, sąskaitos faktūros bus vėl atidarytos apmokėti. Tada galima sukurti naują įvykį, kad sąskaitos faktūros būtų vėl apmokėtos.

## <a name="edit-a-vendor-payment-proposal-automation"></a>Tiekėjo mokėjimo pasiūlymo automatizavimo proceso koregavimas

Procesų automatizavimo sistema leidžia redaguoti mokėjimą, sekas ir įvykius, kurie sukurti mokėjimo pasiūlymui. Sekas galima redaguoti puslapyje **Procesų automatizavimas** arba procesų automatizavimo savaitiniame rodinyje. Pavyzdžiui, jei AP vadovas (-ė) nusprendžia generuoti visus čekius vietiniams tiekėjams trečiadienį, o ne pirmadienį, jis / ji gali rasti įvykį savaitiniame rodinyje ir pasirinkti **Peržiūrėti / redaguoti – Sekos**. Jeigu redaguojate seką, sistema paragins jus nurodyti, ar reikia pakeisti visus esamus įvykius, ar tik naujus įvykius. Retrospektyviniai įvykiai, kurių būsena jau yra **Baigta** arba kurie baigti atsiradus būsenai **Klaida**, nebus pakeisti.

Taip pat galite įtraukti naują įvykį arba pakeisti esamą įvykį. Pavyzdžiui, kitas mokėjimo pasiūlymo atvejis yra planuojamas vykdyti trečiadienį, sausio 1 d., tačiau ši data yra šventė. Galite pakeisti įvykį procesų automatizavimo savaitiniame rodinyje arba puslapyje **Procesų automatizavimas**. Atidaromas puslapis, rodantis grafiko informaciją ir mokėjimo pasiūlymo kriterijus. Jame galite redaguoti suplanuotą laiką ir datą. Taip pat galite redaguoti mokėjimo pasiūlymo kriterijus, jei reikia atlikti pakeitimų. Pavyzdžiui, jeigu keičiate suplanuotą mokėjimo įvykio datą iš sausio 1 d. į sausio 2 d., taip pat rekomenduojama pakeisti pabaigos datos santykines datas.

Taip pat galite išjungti įvykį ar seką. Norėdami išjungti įvykį ir laikinai sustabdyti jo apdorojimą, pasirinkite jį procesų automatizavimo savaitiniame rodinyje, o tada pasirinkite **Išjungti**. Galite išjungti seką puslapyje **Procesų automatizavimas**.

## <a name="security-for-payment-proposal-automations"></a>Mokėjimo pasiūlymų automatizavimo procesų sauga

Buvo pridėtos toliau išvardytos pareigos ir teisės, susijusios su tiekėjo mokėjimo pasiūlymų automatizavimo procesais. Šios pareigos ir teisės yra numatytieji saugos parametrai, tačiau juos galima keisti pagal jūsų organizacijos reikalavimus. Pavyzdžiui, jei ne tik AP vadovas, bet ir AP mokėjimus tvarkantis darbuotojas gali redaguoti ir kurti grafiko įvykį, priskirkite pareigą **Grafiko įvykių tvarkymas** asmeniui, kuris turi AP mokėjimus tvarkančio darbuotojo vaidmenį.

| Pareiga                              | Vaidmuo                                                                       | Teisės |
|-----------------------------------|----------------------------------------------------------------------------|------------|
| Prižiūrėti grafiko sekas          | Mokėtinų sumų vadovas                                                   | Ši pareiga suteikia teises kurti ir tvarkyti mokėjimo pasiūlymo automatizavimo sekas ir įvykius naudojant toliau išvardytas teises:<ul><li>Prižiūrėti grafiko įvykius</li><li>Prižiūrėti grafiko sekas</li><li>ProcessScheduleOccurrenceListMaintain</li><li>Peržiūrėti įvykių savaitinį rodinį</li></ul> |
| Pateikti užklausą dėl grafiko įvykių | Mokėtinų sumų mokėjimus tvarkantis darbuotojas, mokėtinų sumų centralizuotus mokėjimus tvarkantis darbuotojas | Ši pareiga suteikia teises peržiūrėti mokėjimo pasiūlymo automatizavimo įvykius naudojant toliau išvardytas teises:<ul><li>Peržiūrėti grafiko įvykius</li><li>Peržiūrėti įvykių savaitinį rodinį</li></ul> |
| Pateikti užklausą dėl grafiko sekos      | Jokia                                                                       | Ši pareiga suteikia teises peržiūrėti sekų ir įvykių parametrus naudojant toliau išvardytas teises:<ul><li>Peržiūrėti grafiko įvykius</li><li>Peržiūrėti įvykių sąrašo puslapį</li><li>Peržiūrėti įvykių savaitinį rodinį</li></ul>|
| Prižiūrėti grafiko įvykius     | Jokia                                                                       | Ši pareiga suteikia teises kurti ir tvarkyti įvykį naudojant toliau išvardytas teises:<ul><li>Prižiūrėti grafiko įvykius</li><li>Peržiūrėti įvykių savaitinį rodinį</li></ul> |
