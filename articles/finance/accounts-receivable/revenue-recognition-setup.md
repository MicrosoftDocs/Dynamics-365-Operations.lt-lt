---
title: Įplaukų pripažinimo nustatymai
description: Šioje temoje aprašomos įplaukų pripažinimo nustatymų parinktys ir jų reikšmės.
author: kweekley
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 73acfc92777b8fe07b89bea782e13213d38000cd
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570338"
---
# <a name="revenue-recognition-setup"></a>Įplaukų pripažinimo nustatymai
[!include [banner](../includes/banner.md)]

Įtrauktas naujas modulis **Įplaukų pripažinimas**, kuriame yra meniu elementai visiems reikalingiems nustatymams. Šioje temoje aprašomos nustatymų parinktys ir jų reikšmės.

> [!NOTE]
> Įplaukų pripažinimo funkcija negali būti įjungta naudojant funkcijų valdymą. Dabar norėdami ją įjungti, turite naudoti konfigūracijos raktus.

Modulyje **Įplaukų pripažinimas** yra šios nustatymų parinktys:

- Įplaukų pripažinimo žurnalai
- Įplaukų pripažinimo parametrai
- Įplaukų grafikai 
- Atsargų nustatymas

    - Patvirtintų produktų prekių grupės
    - Įplaukų grafiko nustatymas
    - Įplaukų vertės nustatymas

        - Registravimo šablonai
        - Grupavimai

    - Grupavimo komponentai
    - Grupavimo prekė

- Projekto nustatymai

## <a name="revenue-recognition-journals"></a>Įplaukų pripažinimo žurnalai

Įplaukų pripažinimui buvo įvestas naujas žurnalo tipas. Žurnalas yra būtinas ir naudojamas dviem atvejais.

Pirmuoju atveju, įvykdžius visus sutartinius įsipareigojimus, atidėtos įplaukos pripažįstamos sukuriant įplaukų pripažinimo žurnalą, pagrįstą išsamia įplaukų grafiko informacija. Žurnale yra apskaitos įrašas, kuriuo atidėtų įplaukų DK sąskaitos likutis perkeliamas į įplaukų DK sąskaitą.

Antruoju atveju, žurnalas sukuriamas įvykdžius perskirstymą. Perskirstymas vykdomas, kai pardavimo užsakymo eilutė pridedama prie pardavimo užsakymo, kurio SF jau išrašyta, arba kai sukuriamas naujas pardavimo užsakymas, apimantis eilutę, kuri yra pradinės sutarties dalis. Jei SF buvo užregistruota prieš įtraukiant naują pardavimo užsakymo eilutę, užregistruotai kliento SF turi būti sukuriamas koregavimo apskaitos įrašas.

Žurnalas nustatomas puslapyje **Žurnalo pavadinimai** (**Įplaukų pripažinimas \> Nustatymai \> Žurnalo pavadinimai**). Žurnalo tipą reikia nustatyti į **Įplaukų pripažinimas**. Įplaukų pripažinimo žurnalas leidžia pasirinkti registravimo sluoksnį, kuriame norite registruoti.

## <a name="parameters-for-revenue-recognition"></a>Įplaukų pripažinimo parametrai

Įplaukų pripažinimo parametrai konfigūruojami puslapio **Didžiosios knygos parametrai** (**Įplaukų pripažinimas \> Nustatymai \> Didžiosios knygos parametrai**) skirtuke **Įplaukų pripažinimas**. Galimi šie parametrai:

- **Įplaukų pripažinimo žurnalo pavadinimas** – pasirinkite žurnalą, sukurtą įplaukų pripažinimui. Žurnalas reikalingas, kai įplaukos pripažįstamos pagal įplaukų grafiką arba kai atliekate pardavimo užsakymo, kurio SF jau išrašyta, perskirstymą.
- **Įgalinti nuolaidos paskirstymo metodą** – nustatykite šią parinktį į **Taip** norėdami apibrėžti įplaukų vertę paskirstant realią rinkos vertę, apibrėžtą kiekvieno išleisto produkto įplaukų vertėje. Šis paskirstymas apima bet kurios eilutės nuolaidų paskirstymą visoms prekėms. Nustačius šią parinktį į **Ne**, sistemoje naudojama kainų mediana, apibrėžta kiekvieno išleisto produkto įplaukų vertėje. Nustačius šią parinktį į **Ne** ir nenustačius išleistų produktų kainų medianos, įplaukų vertės paskirstymas neatliekamas.
- **Įtraukti antraštės nuolaidas** – nustatykite šią parinktį į **Taip**, jei norite apibrėžti įplaukų vertę paskirstant antraštės nuolaidas visiems produktams. Nustačius šią parinktį į **Ne**, antraštės nuolaida neįtraukiama į įplaukų vertės paskirstymą.
- **Išjungti sutarties sąlygas** – nustatykite šią parinktį į **Taip**, jei produktus, kurių įplaukų tipas **Palaikymas pasibaigus sutarčiai**, galima išleisti net jei sutarties pradžios ir pabaigos datos jiems neapibrėžtos. Dažniausiai sutarties pradžios ir pabaigos datos yra būtinos prekėms, kurių įplaukų tipas **Palaikymas pasibaigus sutarčiai**. Kai sutarties pradžios ir pabaigos datos nėra apibrėžtos, išsami informacija apie įplaukų grafiką registruojant apskaičiuojama naudojant pasikartojimų skaičių ir SF datą.
- **Perskirstant registruoti SF taisymus į Gautinas sumas** – perskirstant jau užregistruotas SF, reikia pataisyti užregistruotos SF apskaitos įrašą. Naudokite šią parinktį, norėdami nurodyti, kaip atliekamas taisymas.

    - Nustatykite šią parinktį į **Ne**, norėdami apriboti taisomosios operacijos registravimą didžiojoje knygoje. Nustačius šią parinktį į **Ne**, vidiniam apskaitos koregavimui Gautinose sumose papildomų dokumentų nesukuriama. Kai SF yra apmokėta, sudengimo proceso metu naudojamas senas apskaitos įrašas bet kokioms mokėjimų nuolaidoms, gautam pelnui ar patirtiems nuostoliams registruoti.
    - Nustatykite šią parinktį į **Taip**, kad būtų automatiškai sukurtas atšaukimo dokumentas ir nauja SF taisymo operacijai Gautinose sumose. Kadangi šis taisymas yra vidinis apskaitos taisymas, nauji dokumentai klientui nesiunčiami / apie juos nepranešama. Atšaukimo dokumentas sudengiamas su originalia SF ir klientas apmoka naują pataisytą SF. Atkreipkite dėmesį, kad visi trys dokumentai yra rodomi ataskaitose, pvz., kliento išraše.

[![Informacija apie sąranką](./media/revenue-recognition-setup-info.png)](./media/revenue-recognition-setup-info.png)

## <a name="revenue-schedules"></a>Įplaukų grafikai

Įplaukų grafikas turi būti sukurtas kiekvienam įvykiui, kurio įplaukos gali būti atidėtos. Pavyzdžiui, jei jūsų organizacija siūlo palaikymą šešių, 12, 18 ir 24 mėnesių laikotarpiais, turite sukurti kiekvieno laikotarpio įplaukų grafiką. Įplaukų grafiko nustatymas apibrėžia, kaip įplaukų vertė paskirstoma pasirinktais laikotarpiais. Jis taip pat apibrėžia numatytąsias datas, įvedamas įplaukų grafike, sukuriamame SF registravimo metu.

Jei įplaukas pripažįstate etapais, rekomenduojame sudaryti įplaukų pripažinimo grafiką atsižvelgiant į etapų skaičių, neatsižvelgiant į pripažinimo datas. Sukūrę grafikus, galite juos redaguoti taip, kad jie atspindėtų numatomas etapų datas. Šiuos įrašus galima sulaikyti, kol būsite informuoti, jog baigėsi etapas, ir bus galima pripažinti įplaukas.

Įplaukų grafikai kuriami puslapyje **Įplaukų grafikai** (**Įplaukų pripažinimas \> Nustatymai \> Įplaukų grafikai**).

[![Įplaukų grafikai](./media/revenue-recognition-revenue-schedules.png)](./media/revenue-recognition-revenue-schedules.png)

Įveskite aprašomąsias reikšmes laukuose **Įplaukų grafikas** ir **Aprašas**. Registruojant SF, įplaukų grafikas sukuriamas naudojant šiuos papildomus parametrus:

- **Pasikartojimai** – įveskite mėnesių ar pasikartojimų skaičių įplaukų atidėjimui.
- **Automatinis sulaikymas** – pasirinkite šį žymės langelį, jei visos įplaukų grafiko eilutės turėtų būti automatiškai sulaikomos registruojant SF. Sulaikymas turi būti pašalinamas rankiniu būdu iš kiekvienos grafiko eilutės, kad būtų galima pripažinti eilutės atidėtas įplaukas.
- **Automatinės sutarties sąlygos** – pasirinkite šį žymės langelį, jei sutarties pradžios ir pabaigos datos turėtų būti nustatomos automatiškai. Šios datos yra automatiškai nustatomos tik išleistiems produktams, kurių įplaukų tipas **Palaikymas pasibaigus sutarčiai**. Sutarties pradžios data automatiškai nustatoma į pardavimo užsakymo eilutės pageidaujamą siuntimo datą, o sutarties pabaigos data automatiškai nustatoma į datą prie pradžios datos pridedant mėnesių ar pasikartojimų skaičių, apibrėžtą nustatant įplaukų grafiką. Pavyzdžiui, pardavimo užsakymų eilutėje esančiam produktui suteikiama vienerių metų garantija. Numatytasis įplaukų grafikas yra **12 mėn.** (12 mėnesių), o šiam įplaukų grafikui pasirinktas žymės langelis **Automatinės sutarties sąlygos**. Jei pardavimo užsakymo eilutėje pageidaujama siuntimo data yra 2019 m. gruodžio 16 d., numatytoji sutarties pradžios data yra 2019 m. gruodžio 16 d., o numatytoji sutarties pabaigos data yra 2020 m. gruodžio 15 d.
- **Pripažinimo pagrindas** – pripažinimo pagrindas apibrėžia, kaip įplaukų vertė paskirstoma pasikartojimuose.

    - **Kas mėnesį pagal datas** – suma paskirstoma pagal faktines kiekvieno mėnesio dienas.
    - **Kas mėnesį** – suma paskirstoma lygiomis dalimis mėnesių skaičiui, apibrėžtam pasikartojimuose.
    - **Pasikartojimai** – suma paskirstoma lygiomis dalimis pasikartojimuose, tačiau gali apimti papildomą laikotarpį, jei kaip pripažinimo konvenciją pasirinksite **Faktinė pradžios data**.

- **Pripažinimo konvencija** – pripažinimo konvencija apibrėžia numatytąsias datas, nustatytas SF įplaukų grafike.

    - **Faktinė pradžios data** – grafikas sukuriamas naudojant sutarties pradžios datą (\[PCS\] prekių palaikymui pasibaigus sutarčiai) arba SF datą (pagrindinėms ir nepagrindinėms prekėms).
    - **Mėnesio 1 d.** – data pirmoje grafiko eilutėje yra sutarties pradžios data (arba SF data). Tačiau visos tolesnės grafikų eilutės yra sukuriamos mėnesio 1 d.
    - **Mėnesio vidurio padalijimas** – data pirmoje grafiko eilutėje priklauso nuo SF datos. Jei SF yra užregistruota pirmą-penkioliktą mėnesio dieną, įplaukų grafikas sukuriamas naudojant pirmą mėnesio dieną. Jei SF yra užregistruota šešioliktą ar vėlesnę mėnesio dieną, įplaukų grafikas sukuriamas naudojant pirmą kito mėnesio dieną.
    - **Kito mėnesio 1 d.** – grafiko data yra pirma kito mėnesio diena.

Pasirinkite mygtuką **Įplaukų grafiko išsami informacija**, norėdami peržiūrėti bendruosius laikotarpius ir procentinius dydžius, pripažįstamus kiekvienu laikotarpiu. Pagal numatytuosius nustatymus **Pripažinti procentinį dydį** reikšmė padalijama po lygiai laikotarpių skaičiui. Jei pripažinimo pagrindas nustatytas į **Kas mėnesį** arba **Pasikartojimai**, pripažinimo procentinę dalį galima keisti. Keičiant pripažinimo procentinę dalį, įspėjimas praneša, kad suma „Iš viso“ nelygi 100 procentų. Gavę pranešimą galite toliau redaguoti eilutes. Tačiau prieš uždarant puslapį procentinė dalis „Iš viso“ turi būti lygi 100 proc.

[![Įplaukų grafiko išsami informacija](./media/revenue-recognition-revenue-schedule-details.png)](./media/revenue-recognition-revenue-schedule-details.png)

## <a name="inventory-setup"></a>Atsargų nustatymas

Įplaukas už išleistus produktus galite pripažinti pardavimo užsakymuose, bet ne pagal pardavimo užsakymų kategorijas ar laisvos formos SF, jei į dokumentą nėra įtraukta prekių. Pasirinkimai, kuriuos atliekate nustatydami išleistus produktus, apibrėžia, kaip pripažįstamos įplaukos už prekę. Pavyzdžiui, pasirinkimai apibrėžia, ar paskirstoma įplaukų vertė ir ar įplaukos atidedamos naudojant įplaukų grafiką.

Nustatymus galima pradėti „FastTab“ **Įplaukų pripažinimas** puslapyje **prekių grupė** (**Įplaukų pripažinimas \> Nustatymai \> Atsargų ir produktų nustatymai \> Prekių grupė**). Šiame puslapyje yra keli sąrankos laukai. Šie laukai naudojami numatytoms vertėms nustatyti tik sistemoje sukurtiems naujiems išleistiems produktams. Sukūrus naujus produktus, čia nustatytos reikšmės pagal numatytuosius nustatymus įvedamos prekių grupei. Galite perrašyti išleistų produktų numatytąsias vertes puslapyje **Išleisti produktai** (**Įplaukų pripažinimas \> Nustatymai \> Atsargų ir produktų nustatymai \> Išleisti produktai**). Nustatytos išleistų produktų numatytosios vertės tuomet perkeliamos į pardavimo užsakymą.

## <a name="item-groups-and-released-products"></a>Patvirtintų produktų prekių grupės

### <a name="define-the-revenue-schedule"></a>Apibrėžti įplaukų grafiką

Įplaukos pardavimo užsakymo eilutėje atidedamos, jei išleisto produkto įplaukų grafikas yra apibrėžtas ir pagal numatytuosius nustatymus naudojamas pardavimo užsakymo eilutėje. Jei nustatymai produktui turėtų būti naudojami kaip numatytieji, įplaukų grafiką galite apibrėžti „FastTab“ **Įplaukų pripažinimas** puslapyje **prekių grupė** (**Įplaukų pripažinimas \> Nustatymai \> Atsargų ir produktų nustatymai \> Prekių grupė**). Taip pat galite apibrėžti išleisto produkto nustatymus „FastTab“ **Įplaukų pripažinimas** puslapyje **Išleisti produktai** (**Įplaukų pripažinimas \> Nustatymai \> Atsargų nustatymai \> Išleisti produktai**).

Lauke **Įplaukų grafikas** pasirinkite įplaukų grafiką, kuriame nurodomas laikotarpis, kuriam turi būti atidėtos įplaukos. Įplaukų grafikas automatiškai įvedamas pardavimo užsakymo eilutėje, o grafiko išsami informacija sukuriama užregistravus pardavimo užsakymo SF.

### <a name="define-the-revenue-price"></a>Apibrėžti įplaukų vertę

Prekių grupes ir išleistus produktus galima nustatyti naudojant kainos medianos metodą arba nuolaidos paskirstymo metodą. Abiems metodams reikia įvairių nustatymų puslapyje: **Išleisti produktai**:

- **Ar įplaukų paskirstymas aktyvus** – nustatykite šią parinktį į **Taip**, norėdami į įplaukų paskirstymo skaičiavimą įtraukti išleistą produktą. Nustačius šią parinktį į **Ne**, išleistas produktas naudoja kainų medianos metodą, jei kainų mediana yra apibrėžta. Jei kainų mediana neapibrėžta, įplaukoms ar atidėtoms įplaukoms registruoti naudojama vieneto kaina pardavimo užsakymo eilutėje.
- **Įplaukų tipas** – pasirinkite įplaukų tipą, apibrėžiantį išleistą produktą:

    - **Pagrindinė** – prekė yra pagrindinis organizacijos įplaukų šaltinis. Tai – numatytojo parametro reikšmė.
    - **Nepagrindinė** – prekė nėra pagrindinis organizacijos įplaukų šaltinis. Kai naudojami kainų medianos nustatymai, kaina sudaroma pagal kainų medianą ir tuomet paskirstoma. Pavyzdžiui, pagrindinės prekės kaina yra fiksuota ir jai reikia pripažinti įplaukas. Jei yra nuolaida, ji gali būti daroma nuo įplaukų už pagrindines prekes, tačiau **tik** iki fiksuotos kainos sumos. Likusi nuolaidos dalis paimama iš įplaukų už nepagrindines prekes. Arba nuolaida gali būti nedaroma nuo įplaukų už pagrindines prekes.
    - **Palaikymas pasibaigus sutarčiai** – prekė palaiko kitus elementus, įtrauktus į pardavimą klientui. Įplaukų vertė paskirstoma pagrindiniams ir nepagrindiniams produktams, įtrauktiems į pardavimą. Priklausomai nuo sąrankos, PCS prekėms gali būti nereikalaujama, kad sutarties pradžios ir pabaigos datos būtų apibrėžtos pardavimo užsakymo eilutėje.

- **Neįtraukti į taikymą nuo** – nustatykite šią parinktį į **Taip**, norėdami nurodyti, jog prekės kainų medianos, esančios žemiau apibrėžtos mažiausios ar aukščiau didžiausios procentinės dalies, koreguoti negalima. Bet kuri įplaukų vertė bus išvedama pagal kito išleisto produkto, įtraukto į pardavimo užsakymą, įplaukų vertę. Nustačius šią parinktį į **Ne**, prekės kainų medianą galima koreguoti arba nuo jos taikyti nuolaidą. Atkreipkite dėmesį, jog parduodant daugiau nei vieną prekę nustatyta kainų mediana, bent vienas išleista produktas turi būti nustatytas, kur parinktis **Neįtraukti į taikymą nuo** nustatyta į **Ne**. Tokiu atveju, yra bent viena prekė, kuriai gali būti paskirstomi visi įplaukų vertės skirtumai.
- **Kainų mediana** – nustatykite šią parinktį į **Taip**, kad nurodytumėte, jog prekės įplaukų vertė turėtų būti pakoreguota taip, kad ji būtų lygi kainų medianai, jei ji yra mažesnė už jūsų nurodytą minimalios vertės leistiną nuokrypį arba didesnė už maksimalios vertės leistiną nuokrypį, ir kad išimties suma, nuo kurios gali būti taikoma nuolaida, turėtų būti paskirstyta eilutėms, kuriose yra produktų, kurių parinktis **Neįtraukti į taikyti nuo** parinktis nustatyta į **Ne**.

    - **Maksimalios vertės leistinas nuokrypis** – įveskite leidžiamą procentinę dalį virš kainų medianos.
    - **Minimalios vertės leistinas nuokrypis** – įveskite leidžiamą procentinę dalį žemiau kainų medianos.

Baigę konfigūruoti išleisto produkto nustatymus, turite rankiniu būdu apibrėžti įplaukų vertę įvedant tikrąją vertę ar kainų medianą (jei naudojate kainų medianos metodą) puslapyje **Įplaukų vertės** (eikite į **Įplaukų pripažinimas \> Nustatymai \> Atsargų nustatymai \> Išleisti produktai**, tada veiksmų srityje skirtuke **Parduoti**, grupėje **Įplaukų pripažinimas** pasirinkite **Įplaukų vertės**).

[![Įplaukų vertės](./media/revenue-recognition-revenue-prices.png)](./media/revenue-recognition-revenue-prices.png)

Įplaukų vertė, kuri šiame puslapyje yra apibrėžta rankiniu būdu, naudojama apibrėžti įplaukų vertės paskirstymą kiekvienam pardavimo užsakymui pagal apibrėžtus kriterijus. Kiekvienas kriterijus yra suderinamas su pardavimo užsakymo eilute, siekiant apibrėžti įplaukų vertę, kuri turėtų būti naudojama paskirstymo proceso metu.

- **Prekės kodas** ir **Prekės ryšys** – įplaukų vertę galima apibrėžti atskiram produktui arba produktų grupei. Pasirinkę **Lentelė** lauke **Prekės kodas**, lauke **Prekės ryšys** pasirinkite išleistą produktą. Pasirinkę **Grupė** lauke **Prekės kodas**, lauke **Prekės ryšys** pasirinkite prekių grupę.
- **Sąskaitos kodas** ir **Sąskaitos/grupės numeris** – įplaukų vertę galima apibrėžti visiems klientams, atskiram klientui ar klientų grupei. Pasirinkus **Visi** lauke **Sąskaitos kodas**, kaina naudojama visiems klientams. Pasirinkę **Lentelė** lauke **Sąskaitos kodas**, lauke **Sąskaitos/grupės numeris** pasirinkite klientą. Pasirinkę **Grupė** lauke **Sąskaitos kodas**, lauke **Sąskaitos/grupės numeris** pasirinkite klientų grupę.
- **Valiuta** – turite įvesti atskirą įplaukų vertę kiekvienai valiutai, kurią įvedate į pardavimo užsakymą. Pavyzdžiui, jei šiuo metu parduodate JAV doleriais, Kanados doleriais ir eurais, turite apibrėžti įplaukų vertę visomis trimis valiutomis. Įplaukų vertė nėra konvertuojama iš vienos valiutos, kaip apskaitos valiuta, į kitas operacijos valiutas, kurias naudojate.
- **Suma ar sąrašo procentinė dalis** – nurodykite, ar įplaukų vertė yra nustatyta kaip suma, ar kaip sąrašo kainos procentinė dalis. Pasirinkus **Sąrašo procentinė dalis**, vartotojai vietoj sumos gali įvesti kainų medianą kaip sąrašo kainos procentinę dalį. **Sąrašo procentinė dalis** reikšmė naudojama tik išleistiems produktams, nustatytiems kaip PCS prekės.
- **Įplaukų paskirstymo kaina** – priklausomai nuo reikšmės, kurią pasirinkote lauke **Suma ar sąrašo procentinė dalis**, įveskite sumą ar procentinę dalį, kad atvaizduotumėte įplaukų vertę, naudojamą paskirstyti įplaukas visuose pardavimo užsakymo elementuose.
- **Nuo datos** ir **Iki datos** – įveskite datų intervalą, kuriame yra aktyvi įplaukų vertė. Šie laukai nėra privalomi.

Jei parinktis **Įgalinti nuolaidos paskirstymo metodą** puslapyje **Didžiosios knygos parametrai** nustatyta į **Taip** ir jei jūsų išleisto produkto laukas **Įplaukų tipas** nustatytas į **Palaikymas pasibaigus sutarčiai**, taip pat turite nurodyti prekes, palaikomas išleisto produkto. Šie nustatymai atliekami puslapyje **Nustatyti pagrindus** (eikite į **Įplaukų pripažinimas \> Nustatymai \> Atsargų nustatymai \> Išleisti produktai** ir tada veiksmų srityje, skirtuke **Parduoti**, grupėje **Įplaukų pripažinimas** pasirinkite **Nustatyti pagrindus**).

Puslapyje **Nustatyti pagrindus** įtraukite kiekvienos prekių grupės, kurią prekė palaiko, įrašą. Vykdant įplaukų paskirstymą, įplaukų vertė bus paskirstoma visose pagrindinėse ir nepagrindinėse PCS prekės dalyse.

### <a name="posting-profiles"></a>Registravimo šablonai

Trys papildomi registravimo tipai palaiko galimybę atidėti įplaukas. Šie registravimo tipai nustatomi puslapio **Registravimas** skirtuke **Pardavimo užsakymas** (**Įplaukų pripažinimas \> Nustatymai \> Atsargų ir produktų grupė \> Registravimas**).

- **Atidėtos įplaukos** – įveskite pagrindinę sąskaitą įplaukų vertei, kuri registruojama atidėtose įplaukose (vietoj įplaukų). Įplaukų vertė yra atidėta, jei pardavimo užsakymo eilutėje yra įplaukų grafikas.
- **Atidėta parduotų prekių savikaina** – įveskite pagrindinę sąskaitą parduotų prekių savikainos sumai, registruojamai atidėtoje parduotų prekių savikainoje, jei įplaukos taip pat atidėtos.
- **Dalinis SF įplaukų sudengimas** – įveskite pagrindinę sąskaitą tarpuskaitos sąskaitai, naudojamai kai pardavimo užsakymo SF dalinai išrašyta arba kai vykdomas perskirstymas. Likutis šioje sąskaitoje grįžta į 0 (nulį), kai išrašomos visos pardavimo užsakymų SF.

### <a name="bundles"></a>Grupavimai

Grupavimo prekės yra unikalūs išleisti produktai, nustatyti taip, kad į juos būtų įtraukti komponentai. Šis nustatymas atliekamas naudojant komplektavimo specifikacijos (KS) funkciją. Kai grupavimo prekė įvedama į pardavimo užsakymą, atskiri komponentai naudojami įplaukų vertėms ir įplaukų grafikams apibrėžti. Tačiau spausdinami kliento dokumentai, pvz., pardavimo užsakymas ir SF, rodo grupavimo prekę.

#### <a name="bundle-components"></a>Grupavimo komponentai

Komponentai, įtraukti į grupavimą, turi būti nustatomi puslapyje **Išleidžiami produktai** (**Įplaukų pripažinimas \> Nustatymai \> Atsargų ir produktų nustatymai \> Išleisti produktai**). Šie komponentai yra išleidžiami produktai, jie turi būti nustatyti tokiu pat būdu kaip produktai, kurie yra įtraukti į KS. Pavyzdžiui, išleista produktas gali būti **Prekė** arba **Paslaugos** tipo prekė, bet jis turi būti priskirtas prekių modelio grupei, kurioje parinktis **Laikomas produktas** nustatyta į **Taip**. Daugiau informacijos žr. KS prekių nustatymų dokumentacijoje.

Be to, turi būti nustatyti įplaukų pripažinimo komponentai, lygiai taip pat, kaip produktai, kuriuos galima parduoti atskirai pardavimo užsakyme. Pavyzdžiui, įsitikinkite, kad kiekvienam komponentui apibrėžta teisinga įplaukų vertė, ir kad kainos pagrindas nustatytas PCS prekėms.

#### <a name="bundle-items"></a>Grupavimo prekės

Nustatant grupavimo prekę, turite nustatyti du laukus puslapyje **Išleidžiami produktai** (**Įplaukų pripažinimas \> Nustatymai \> Atsargų ir produktų nustatymai \> Išleisti produktai**):

- „FastTab“ **Inžinierius** lauke **Produkto tipas** prekę reikia nustatyti kaip KS prekę.
- „FastTab“ **Bendra** lauke **Grupavimas** prekė turi būti pažymėta kaip grupavimo prekė.

Komponentai turi būti priskirti grupavimo / KS pirminei prekei puslapyje **KS versijos** (eikite į **įplaukų pripažinimas \> Nustatymai \> Atsargų ir produktų nustatymai \> Išleisti produktai**, tada veiksmų srityje, skirtuke **Inžinierius**, **KS** grupėje pasirinkite **KS versijos**). Daugiau informacijos žr. KS nustatymų dokumentacijoje.

[![Išleisti produktai, KS grafikai](./media/revenue-recognition-bom-scheduleds.jpg)](./media/revenue-recognition-bom-scheduleds.jpg)

Jei grupavimo pirminė prekė ir grupavimo komponentai nustatyti kaip paskirstyti, sugrupuotų įplaukų vertė bus paskirstyta komponentams, atsižvelgiant į jų įplaukų įnašo procentinę dalį.

## <a name="project-setup"></a>Projekto nustatymai

Įplaukų pripažinimą taip pat galima naudoti pardavimo užsakymams, sukurtiems naudojant laiko ir medžiagų projektą. Pardavimo užsakymams, kurie gaunami iš projektų, tereikia nustatyti pagrindines sąskaitas projekto registravimo šablonuose, kurie naudojami registruoti projekto SF. Pagrindinės sąskaitos apibrėžiamos puslapyje **DK registravimo nustatymai** (**Įplaukų pripažinimas \> Nustatymai \> Projekto nustatymai \> DK registravimo nustatymai**).

- **Atidėtos SF įplaukos** (pagal **Įplaukų sąskaitos**) – įveskite pagrindinę įplaukų vertės sąskaitą, kurioje registruojamos atidėtosios įplaukos (o ne įplaukos). Įplaukų vertė yra atidėta, jei pardavimo užsakymo eilutėje yra įplaukų grafikas.
- **Atidėtos išlaidos** (pagal **Išlaidų sąskaitos**) – įveskite pagrindinę sąskaitą parduotų prekių savikainos sumai, kuri užregistruojama PPK išlaidose, jei įplaukos taip pat yra atidėtos.
