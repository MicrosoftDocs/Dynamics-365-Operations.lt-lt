---
title: Gamybos cecho vykdymo sąsajos konfigūravimas
description: Šiame straipsnyje aprašoma, kaip sukurti vieną ar daugiau gamybos laiko vykdymo sąsajos konfigūracijų. Atidarius gamybos cecho vykdymo sąsają, ji automatiškai įkelia pasirinktą konfigūraciją ir užduoties filtrą, būdingus naršyklei ir įrenginiui. Konfigūracijoje nustatote strategijas, kurios turi būti taikomos konkrečiam naudojimui.
author: johanhoffmann
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f740b68128b90fc7c9ce2f74edc4f3c06f03debd
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/15/2022
ms.locfileid: "9167768"
---
# <a name="configure-the-production-floor-execution-interface"></a>Gamybos cecho vykdymo sąsajos konfigūravimas

[!include [banner](../includes/banner.md)]

Cecho darbuotojai naudoja gamybos cecho vykdymo sąsają savo kasdieniams darbams registruoti, pvz., užduočių pradžios laikui fiksuoti, atsiliepimams apie užduotis pateikti, netiesioginėms veikloms registruoti ir pranešti apie neatvykimą į darbą. Šios registracijos yra itin svarbios stebint eigą bei išlaidas gamybos užsakymams ir darbuotojų atlyginimo dydžio skaičiavimo pagrindas.

Atidarius gamybos cecho vykdymo sąsają, ji automatiškai įkelia pasirinktą konfigūraciją ir užduoties filtrą, būdingus naršyklei ir įrenginiui. Konfigūracijoje nustatote strategijas, kurios turi būti taikomos konkrečiam naudojimui. Štai keletas panaudojimo pavyzdžių.

- Naudodami įmonės salėje esantį įrenginį darbuotojai registruojasi atėję į biurą ir išeidami iš jo.
- Naudodami ceche esantį įrenginį mašinų operatoriai registruojasi pradedami ir užbaigdami užduotis. Jie taip pat registruoja pertraukas ir netiesioginę veiklą.

Šiame straipsnyje aprašomos įvairios gamybos laiko vykdymo sąsajos konfigūravimo kiekviename jūsų svetainėje naudojamame įrenginyje parinktys.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Įjunkite gamybos aukšto vykdymo sąsają ir su ja susijusias pasirenkamas funkcijas

Pati gamybos laiko vykdymo sąsaja ir keletas pasirinktinių šiame straipsnyje aprašytų parametrų turi būti įjungta sistemoje prieš naudojant juos. Naudokite [Funkcijos valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) puslapį tam, kad įjungtumėte bet kurią funkciją aprašyta tolesniuose poskyriuose.

### <a name="the-production-floor-execution-interface"></a>Gamybos aukšto vykdymo sąsaja

Tai yra pagrindinė šiame straipsnyje aprašyta funkcija ir ji yra būtina visų kitų šiame skyriuje paminėtų funkcijų sąlyga. Kaip ir tiekimo grandinės valdymas 10.0.25, jis yra privalomas ir jo negalima išjungti. Jei naudojate senesnę nei 10.0.25 versiją, *·*[tada](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) administratoriai gali įjungti arba išjungti šią funkciją ieškodami gamybos laiko vykdymo funkcijos funkcijų valdymo darbo srityje.

### <a name="generate-license-plates"></a>Kurti licencijos plokšteles

Šios funkcijos leidžia licencijos plokštelės funkcijas veikti gamybos aukšto vykdymo sąsajoje. Jei norėtumėte jas naudoti, įjunkite tolesnes funkcijas [funkcijų valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (tokia tvarka):

1. *Užbaigtos ataskaitos numerio lentelė įtraukta į užduoties kortelės įrenginį*<br>(Kaip ir tiekimo grandinės valdymo versija 10.0.21, ši funkcija įjungiama pagal numatytąjį nustatymą. Kaip ir tiekimo grandinės valdymo versija 10.0.25, ši funkcija yra privaloma.)
1. *Įgalinkite automatinį numerio lentelės numerio generavimą, kai Užduoties kortelės įrenginyje pranešama apie pabaigimą*<br>(Kaip ir tiekimo grandinės valdymo versija 10.0.25, ši funkcija yra privaloma.)

### <a name="print-labels"></a>Spausdinti etiketes

Šios funkcijos leidžia žymės spausdinimo funkcijas veikti gamybos aukšto vykdymo sąsajoje. Jei norėtumėte jas naudoti, įjunkite tolesnes funkcijas [funkcijų valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (tokia tvarka):

1. *Užbaigtos ataskaitos numerio lentelė įtraukta į užduoties kortelės įrenginį*<br>(Kaip ir tiekimo grandinės valdymo versija 10.0.21, ši funkcija įjungiama pagal numatytąjį nustatymą. Kaip ir tiekimo grandinės valdymo versija 10.0.25, ši funkcija yra privaloma.)
1. *Spausdinti etiketę iš užduoties kortelės įrenginio*<br>(Kaip ir tiekimo grandinės valdymo versija 10.0.25, ši funkcija yra privaloma.)

### <a name="allow-locking-the-touch-screen"></a>Leisti užrakinti jutiklinį ekraną

Ši funkcija leidžia darbuotojams užrakinti jutiklinius ekranus, kad jie galėtų juos detinguoti.

Kaip ir tiekimo grandinės valdymo versija 10.0.21 ši funkcija įjungiama pagal numatytąjį nustatymą. Kaip ir tiekimo grandinės valdymas 10.0.25 ši funkcija yra privaloma ir jos išjungti negalima. Jei naudojate senesnę nei 10.0.25 versiją, tada administratoriai gali įjungti arba išjungti šią funkciją ieškodami funkcijos, kad užduoties kortelės įrenginys *ir užduoties kortelių mokėjimo terminalas būtų užrakinti taip, kad būtų galima juos*[dearizuoti](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) funkcijų valdymo darbo srityje.

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Turto valdymo funkcijos gamybos vietos vykdymo sąsajai

Ši funkcija įtraukia turto valdymo skirtuką į gamybos vietos vykdymo sąsają. Darbuotojai gali naudoti šį skirtuką norėdami pasirinkti turtą, prijungtą prie įrenginio išteklių, kurie yra pasirinktame užduočių sąrašo filtre. Darbuotojas gali peržiūrėti pasirinkto įrenginio turto būseną ir sveikatą iš skaitiklio verčių (ne daugiau keturių pasirinktų skaitiklių). Norėdami naudoti šią funkciją, įjunkite tolesnę funkciją [Funkcijos valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Turto valdymo funkcijos gamybos vietos vykdymo sąsajai*<br>(Kaip ir tiekimo grandinės valdymo versija 10.0.25, ši funkcija veikia pagal numatytąjį nustatymą.)

### <a name="enable-job-search"></a>Užduoties ieškos įgalinimas

Ši funkcija leidžia į užduočių sąrašą įtraukti ieškos lauką. Darbuotojai gali rasti konkrečią užduotį įvesdami užduoties ID arba rasti visas konkretaus užsakymo užduotis įvesdami užsakymo ID. Darbuotojai gali įvesti ID naudodami klaviatūrą arba nuskaitę brūkšninį kodą. Norėdami ją naudoti, įjunkite tolesnę funkciją [Funkcijos valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Gamybos vietos vykdymo sąsajos užduočių ieška*<br>(Kaip ir tiekimo grandinės valdymo versija 10.0.25, ši funkcija veikia pagal numatytąjį nustatymą.)

### <a name="enable-reporting-on-co-products-and-by-products"></a>Sudėtinių ir šalutinių produktų ataskaitos įgalinimas.

Ši funkcija leidžia darbuotojams naudoti gamybos vietos vykdymo sąsają pateikti informaciją apie partijinių užsakymų eigą. Ši ataskaita apima ataskaitos teikimą apie sudėtinius ir šalutinius produktus. Jei norite naudoti šią funkciją, funkcijų valdymas įjunkite šią [funkciją](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Ataskaita apie sudėtinius ir šalutinius produktus iš gamybos vietos vykdymo sąsajos*

### <a name="enable-the-display-of-full-serial-batch-and-license-plate-numbers"></a>Įgalinti visų serijos, paketo ir numerio lentelės numerių rodymą

Ši funkcija gamybos laiko vykdymo sąsajoje pagerina serijos, paketo ir numerio lentelės numerių sąrašų peržiūros patirtį. Ekrano pakeitimai iš kortelės rodinio, rodantis ribotą simbolių skaičių sąrašo rodinyje, kuriame yra pakankamai vietos, kad būtų galima parodyti visas vertes. Sąrašas taip pat siūlo galimybę ieškoti konkrečių skaičių.

Kaip ir tiekimo grandinės valdymo versija 10.0.25 ši funkcija įjungiama pagal numatytąjį nustatymą. Administratoriai šią *funkciją gali įjungti arba išjungti ieškodami gamybos laiko vykdymo sąsajos funkcijose rodyti visus serijos,*[paketo ir numerio lentelės numerius funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo srityje.

### <a name="enable-registering-of-material-consumption"></a>Įjungti medžiagų suvartojimo registrą

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Ši funkcija leidžia darbuotojams naudoti gamybos laiko vykdymo sąsają medžiagų suvartojimui, paketo numeriams ir serijos numeriams registruoti. Kai kurie gamintojai, ypač proceso pramonės šakose, turi aiškiai užregistruoti medžiagų kiekį, suvartojamą kiekvienam paketo ar gamybos užsakymui. Pavyzdžiui, darbuotojai gali naudoti svarstyklių skalę, kad galėtų sverti suvartojamą medžiagos kiekį. Kad būtų užtikrintas visos medžiagų kiekis, šios organizacijos taip pat turi užregistruoti paketų numerius, suvartotus kiekvienam produktui pagaminti.

Yra dvi šios priemonės versijos. Viena palaiko prekes, *kurios neįgalintos* naudoti sandėlio valdymo procesų (WMS). Kita palaiko prekes, *kurios* įgalintos naudoti WMS. Norėdami naudoti šią funkciją, funkcijų valdymo dalyje (šia tvarka) įjunkite vieną arba abi funkcijas atsižvelgdami į tai, [ar](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) yra WMS įgalintos prekės:

- *Registruoti medžiagų suvartojimą gamybos laiko vykdymo sąsajoje (ne WMS)*
- *(Peržiūros versija) Užregistruokite medžiagų suvartojimą gamybos vietos vykdymo sąsajoje (veikia WMS)*

> [!IMPORTANT]
> Galima naudoti tik ne WMS priemonę. Tačiau jei naudojate WMS, turite įgalinti abi funkcijas.

### <a name="enable-reporting-on-catch-weight-items"></a>Įgalinti esamo svorio prekių ataskaitas

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Darbuotojai gali naudoti gamybos laiko vykdymo sąsają esamo svorio prekių paketinių užsakymų vykdymo eigai pranešti. Paketiniai užsakymai kuriami pagal formules, kurias galima apibrėžti kaip esamo svorio prekes kaip sudėties prekes, sudėtinius produktus ir pagal produktus. Formulę taip pat galima apibrėžti, kad ji turėtų formulės eilutes, skirtas ingredientams, kurie apibrėžti kaip esamo svorio. Esamo svorio prekės turi sekti atsargas pagal du matavimo vienetus: esamo svorio kiekį ir atsargų kiekį. Pavyzdžiui, maisto pramonėje dėžes galima nurodyti kaip esamo svorio prekę, kur esamo svorio kiekis naudojamas dėžių kiekiui sekti, o atsargų kiekis naudojamas dėžių svoriui sekti.

Jei norite naudoti šią funkciją, funkcijų valdymas įjunkite šią [funkciją](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *(Peržiūros versija) Ataskaita apie esamo svorio prekes iš gamybos vietos vykdymo sąsajos*

### <a name="enable-the-my-day-dialog"></a>Įgalinti dialogo langą "Mano diena"

Dialogo **lange Mano diena** darbuotojams pateikiama darbuotojų kasdieninių registracijų ir dabartinių apmokėto laiko, apmokėtų viršvalandžių, neatvykimo ir apmokėto neatvykimo balansų peržiūra.

Jei norite naudoti šią funkciją, funkcijų valdymas įjunkite šią [funkciją](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Gamybos vietos vykdymo sąsajos rodinys „Mano diena“*

### <a name="enable-teams"></a>Įgalinti komandas

Kai tai pačiai gamybos užduočiai priskirti keli darbuotojai, jie gali sudaryti komandą. Komanda gali paskirti vieną darbuotoją kaip vadininką. Likę darbuotojai automatiškai tampa to vad vadymi asistentais. Gautai komandai užduoties būseną turi užregistruoti tik vadovas. Laiko įrašai taikomi visiems komandos nariams.

Jei norite naudoti šią funkciją, funkcijų valdymas įjunkite šią [funkciją](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Gamybos komandos gamybos vietos vykdymo sąsajoje*

### <a name="enable-additional-configuration-in-the-production-floor-execution-interface"></a>Įgalinti papildomą konfigūraciją gamybos laiko vykdymo sąsajoje

Ši funkcija įtraukia toliau nurodytų funkcijų parametrus į gamybos laiko **vykdymo puslapio konfigūravimą**:

- Automatiškai atidaryti dialogo **langą Pradėti** užduotį, kai ieška baigiama.
- Automatiškai atidaryti ataskaitos **eigos dialogo** langą, kai ieška baigiama.
- Iš anksto užpildyti likusį kiekį ataskaitos **eigos** dialogo lange.
- Įgalinkite medžiagų suvartojimo koregavimus dialogo **lange Ataskaitos** eiga. (Šiai funkcijai atlikti taip pat reikia *Registruoti medžiagų suvartojimą gamybos laiko vykdymo sąsajos (ne WMS) priemonėje* .)
- Įgalinti ieškas pagal projekto ID.

Informacija apie parametrų naudojimą pateikiama toliau šiame straipsnyje.

Jei norite naudoti šią funkciją, funkcijų valdymas įjunkite šią [funkciją](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Papildoma konfigūracija gamybos vietos vykdymo sąsajoje*


## <a name="work-with-production-floor-execution-configurations"></a>Darbas su gamybos cecho vykdymo konfigūracijomis

Norėdami sukurti ir prižiūrėti gamybos laiko vykdymo konfigūracijas, eikite į Gamybos **kontrolės nustatymas \>\> Gamybos vykdymas Konfigūruoti \> gamybos laiko vykdymą**. Puslapyje **Gamybos cecho vykdymo konfigūravimas** rodomas esamų konfigūracijų sąrašas. Šiame puslapyje galite atlikti toliau pateiktus veiksmus.

- Pasirinkite bet kurią gamybos cecho konfigūraciją, nurodytą kairiajame stulpelyje, ir ją peržiūrėkite bei redaguokite.
- Veiksmų srityje pasirinkite Naujas **, kad** į sąrašą įtraukumėte naują konfigūraciją. Tada įveskite pavadinimą lauke **Konfigūracija**, kad identifikuotumėte naują konfigūraciją. Pavadinimas, kurį įvedate, turi būti unikalus visų konfigūracijų ir vėliau jo redaguoti negalėsite. **Į lauką** Aprašas galite pasirinktinai įvesti konfigūracijos aprašymą.

Po to sukonfigūruokite įvairius pasirinktos konfigūracijos parametrus, kaip aprašyta toliau aprašytus poskyrius.

### <a name="the-general-fasttab"></a>Bendras „FastTab“ skirtukas

Šie parametrai galimi bendrajame **"** FastTab":

- **Tik atėjimo ir išėjimo** iš darbo *parinktis* nustatykite šią pasirinktį norėdami sukurti supaprastintą sąsają, kuri leidžia naudoti tik atėjimo į darbą ir išėjimo iš darbo funkcijas. Šis parametras uždraus daugelį kitų šio puslapio pasirinkčių. Prieš įgalindami šią parinktį, pirmiausia turite pašalinti visas eilutes iš „FastTab” **Skirtuko pasirinkimas**.
- **Įgalinti iešką** – nustatykite šią pasirinktį *kaip* Taip, jei į užduočių sąrašą norite įtraukti ieškos lauką. Darbuotojai gali rasti konkrečią užduotį įvesdami užduoties ID arba įvesdami užsakymo ID, gali rasti visas tam tikro užsakymo užduotis. Darbuotojai gali įvesti ID naudodami klaviatūros arba brūkšninio kodo nuskaitymą.
- **Įgalinkite iešką pagal projekto ID** – *nustatykite* šią pasirinktį kaip Taip, norėdami įgalinti darbuotojus ieškoti pagal projekto ID (be užduoties ID ir užsakymo ID) gamybos laiko vykdymo sąsajos ieškos lauke. Šią pasirinktį galite nustatyti kaip *Taip* tik tada, kai nustatyta **parinktis** Įgalinti iešką taip *pat*.
- **Automatiškai atidaryti pradžios dialogo langą** – *kai ši pasirinktis nustatyta kaip Taip*, užduoties pradžios dialogo langas atidaromas automatiškai, **kai** darbuotojai užduočiai ieškoti naudoja ieškos juostą.
- **Automatiškai atidarytas ataskaitos eigos** dialogo langas – *kai ši parinktis nustatyta kaip Taip*, ataskaitos eigos dialogo langas automatiškai atidaromas, **kai** darbuotojai užduočiai rasti naudoja ieškos juostą.
- **Įgalinti medžiagų koregavimas** – nustatykite šią pasirinktį *kaip Taip*, norėdami **įgalinti** **mygtuką Koreguoti medžiagą ataskaitų eigos** dialogo lange. Darbuotojai gali pasirinkti šį mygtuką, norėdami koreguoti užduoties medžiagų suvartojimą.
- **Teikti kiekio ataskaitą išeinant iš darbo** – nustatykite šią parinktį į *Taip*, kad darbuotojai būtų paraginti pateikti atsiliepimų apie vykdomas užduotis prieš išeidami iš darbo. Kai parinktis nustatyta į *Ne*, darbuotojai nebus raginami.
- **Užrakinti darbuotoją** – kai ši parinktis nustatyta į *Ne*, darbuotojai bus atjungiami iš karto jiems pateikus registraciją (pvz., naujos užduoties). Tada sąsaja grįš į prisijungimo puslapį. Kai ši parinktis nustatyta į *Taip*, darbuotojai bus prisiregistravę gamybos laiko vykdymo sąsajoje. Tačiau darbuotojas gali išsiregistruoti rankiniu būdu, kad kitas darbuotojas prisiregistruotų, kol gamybos laiko vykdymo sąsaja ir toliau veiks pagal tą patį sistemos vartotojo abonementą. Daugiau informacijos apie šių tipų paskyras žr. [Priskirti vartotojai](config-job-card-device.md#assigned-users).
- **Naudoti faktinį registravimo laiką** – nustatykite šią parinktį į *Taip*, norėdami nustatyti kiekvienos naujos registracijos laiką į laiką, kada darbuotojas pateikė registraciją. Jei ši parinktis nustatyta į *Ne*, naudojamas prisijungimo laikas. Paprastai norėsite nustatyti šią parinktį į *Taip*, jei nustatėte parinktis **Užrakinti darbuotoją** ir (arba) **Vienas darbuotojas** į *Taip* ir jei darbuotojai dažnai būna prisijungę ilgesnį laikotarpį.
- **Vienas darbuotojas** – nustatykite šią pasirinktį kaip *Taip*, jei tik vienas darbuotojas naudoja kiekvieną gamybos laiko vykdymo sąsają, kurioje ši konfigūracija yra aktyvi. Nustačius šią parinktį į *Taip*, parinktis **Užrakinti darbuotoją** automatiškai nustatoma į *Taip*. Be to, pasirinkus šį parametrą pašalinamas darbuotojo reikalavimas (ir galimybė) prisijungti naudojant ženklo ID (arba kitą panašų ID). Vietoj to Dynamics 365 Supply Chain Management *darbuotojas prisiregistruoja "Microsoft*" naudodamas sistemos vartotojo sąskaitą, susietą su užregistruotu laiku (*iš* darbuotojų lentelės), ir prisiregistruoja prie gamybos laiko vykdymo sąsajos kaip tas darbuotojas tuo pačiu metu.
- **Leisti užrakinti jutiklinį** ekraną – *nustatykite* šią pasirinktį į Taip, norėdami leisti darbuotojams užrakinti jutiklinį gamybos laiko vykdymo sąsajos ekraną, kad jie galėtų ją santizuoti. Kai ši parinktis nustatyta kaip *Taip*, į prisijungimo **puslapį įtraukiamas** mygtuko sąstingio sąsk. Kai darbuotojas pasirenka šį mygtuką, jutiklinis ekranas laikinai užrakinamas, kad būtų išvengta netyčinių įvesčių. Taip pat rodomas skaičiavimo atgal laikmatis. Tada darbuotojas gali saugiai nuvalyti įrenginį ir ekraną. Kai atgalinis skaičiavimas baigiasi, jutiklinis ekranas vėl automatiškai atrakinamas.
- **Ekrano užrakto trukmė** – kai parinktis **Leisti užrakinti jutiklinį ekraną** nustatyta į *Taip*, naudokite šią parinktį norėdami nurodyti, kiek sekundžių jutiklinis ekranas bus išjungtas, kad būtų galima jį nuvalyti. Trukmė turi būti nuo 5 iki 120 sekundžių.
- **Generuoti numerio lentelę** – nustatykite šią *pasirinktį* kaip Taip, norėdami sugeneruoti naują numerio lentelę kiekvieną kartą, kai darbuotojas naudoja gamybos laiko vykdymo sąsają, kad ataskaitoje būtų baigta. Numerio lentelėje nurodytas numeris generuojamas naudojant skaičių seką, kuri nustatyta puslapyje **Sandėlio valdymo parametrai**. Kai ši parinktis nustatyta į *Ne*, darbuotojai turi nurodyti esamą numerio lentelę pranešdami apie baigtą užduotį.
- **Spausdinti** žymą – nustatykite šią pasirinktį *kaip* Taip, norėdami išspausdinti numerio lentelės žymę, kai darbuotojas naudoja gamybos laiko vykdymo sąsają ataskaitoje kaip baigtai. Žymos konfigūracija nustatoma dokumento maršruto planavimo dalyje, kaip nurodyta [Numerio lentelės žymų dokumentų maršrutų planavimo maketas](../warehousing/document-routing-layout-for-license-plates.md).

### <a name="the-tab-selection-fasttab"></a>Skirtuko pasirinkimo "FastTab"

Naudokite skirtuko pasirinkimo " **FastTab"** parametrus, norėdami pasirinkti, kuriuos skirtukus gamybos laiko vykdymo sąsaja turėtų rodyti, kai dabartinė konfigūracija yra aktyvi. Galite projektuoti tiek skirtukų, kiek jums reikia, o tada, naudodami "FastTab" įrankių juostos mygtukus, juos pridėti ir išdėstyti taip, kaip jums reikia. Daugiau informacijos apie tai, kaip kurti skirtukus ir dirbti su čia parametrais, [ieškokite Gamybos laiko vykdymo sąsajos kūrimas](production-floor-execution-tabs.md).

### <a name="the-report-progress-fasttab"></a>Ataskaitos eigos "FastTab"

Šie parametrai galimi ataskaitos eigos **"** FastTab":

- **Įgalinti koregavimo medžiagą** – nustatykite šią pasirinktį *kaip Taip*, norėdami įtraukti **mygtuką** Koreguoti medžiagą į **ataskaitos eigos** dialogo langą. Darbuotojai gali pasirinkti šį mygtuką, norėdami koreguoti užduoties medžiagų suvartojimą.
- **Numatytasis likęs** kiekis – nustatykite šią pasirinktį *kaip* Taip, jei norite iš anksto užpildyti numatomą likusį gamybos užduoties **kiekį ataskaitos eigos dialogo** lange.

## <a name="clean-up-job-configurations"></a>Užduočių konfigūracijų valymas

Kai cecho prižiūrėtojas nustato gamybos cecho vykdymo sąsają, jis pasirenka konfigūraciją ir užduoties filtrą. Šie pasirinkimai saugomi „Supply Chain Management” nuorodų lentelėje, o naršyklė naudoja ID, saugomą vietiniame slapuke, kad būtų galima rasti teisingą tos lentelės eilutę. Be to, lentelė registruoja datą ir laiką, kada darbuotojas paskutinį kartą prisijungė prie kiekvieno įrenginio.

Paketinė užduotis periodiškai išvalo įrenginių, neužregistravusių veiklos per pastarąsias 60 dienų, nuorodų lentelės įrašus. Taip pat galite bet kada rankiniu būdu valyti įrašus, atlikdami toliau pateiktus veiksmus.

1. Eikite į **Gamybos kontrolė \> Sąranka \> Gamybos vykdymas \> Gamybos cecho vykdymo konfigūravimas**.
1. Veiksmų srityje pasirinkite **Valyti kliento konfigūracijas**.
1. Dialogo lange **Valyti kliento konfigūracijas** nustatykite lauką **Dienų skaičius** į neaktyvumo dienų skaičių (iki šios dienos), į kurį reikia atsižvelgti. Pašalinsite visas įrenginių, kurie nebuvo aktyvūs tuo metu, konfigūracijas ir prisijungimo įrašus.
1. Pasirinkite **Gerai**, norėdami išvalyti atitinkamas konfigūracijas pagal parametrą **Dienų skaičius**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
