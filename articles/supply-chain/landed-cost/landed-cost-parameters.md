---
title: Iškrovimo kainos parametrų nustatymas
description: Šioje temoje aprašoma, kaip nustatyti bendruosius informacijos ir konfigūravimo nustatymus, kurie naudojami iškrovimo kainos modulyje registravimui, būsenos atnaujinimams, numeracijai ir elgesiui.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 973f23a18166abeb05bdea660ef69230d9a8c4c0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833910"
---
# <a name="landed-cost-parameters-setup"></a>Iškrovimo kainos parametrų nustatymas

[!include [banner](../../includes/banner.md)]

Naudodami puslapį **Iškrovimo kainos parametrai** galite nustatyti bendrąją informaciją ir konfigūracijos nustatymus, naudojamus visame modulyje **Iškrovimo kaina** registravimui, būsenos atnaujinimams, numeracijai ir elgesiui. Parametrų nustatymas bendrai naudojamas tarp juridinių subjektų ir jį gali modifikuoti administratorius.

## <a name="open-the-landed-cost-parameters-page"></a>Atidarykite į iškrovimo kainos parametrų puslapį

Norėdami dirbti su parametrais, eikite į **Iškrovimo kaina \> Nustatymas \>Iškrovimo kainos parametrai**, o tada nustatykite laukelius, kaip aprašyta tolesniuose poskyriuose.

![Gabenimo išlaidų parametrų puslapis](media/landed-cost-parameters.png "Gabenimo išlaidų parametrų puslapis")

## <a name="general-tab"></a>Skirtukas Bendra

### <a name="general-fasttab"></a>Bendras „FastTab“ skirtukas

Šioje lentelėje aprašomi laukeliai, esantys „FastTab“ skirtuke **Bendra**, kuris yra skirtuke **Bendra**, puslapyje **Iškrovimo kainos parametrai**.

| Parametras | aprašymas |
|---|---|
| Naudoti gabenimo kursą | Siuntimo tarifas nustatomas nustatytam laikotarpiui ir naudojamas prekių, kurios naudoja kelias valiutas, savikainai nustatyti. Šią parinktį nustatykite kaip *Taip*, kad naudotumėte siuntimo tarifą. |
| Valiutos kurso tipas | Numatytasis valiutų kursų rinkinys, naudojamas reiso ir reiso išlaidų kelių valiutų skaičiavimams. |
| Atnaujinti pirkimo užsakymo kiekį | Pasirinkite, kas įvyks naudotojui pakeitus kiekį pirkimo užsakymo eilutėje:<ul><li>**Priimti** – reiso kiekis koreguojamas automatiškai.</li><li>**Įspėjimas** – jei eilutė pridėta prie reiso, rodomas įspėjimas, bet reiso kiekis atnaujinamas.</li><li>**Klaida** – jei eilutė pridėta prie reiso, rodomas klaidos pranešimas, o pirkimo užsakymo atnaujinti negalima. Todėl užsakymo eilutę pirmiausia reikia pašalinti iš reiso.</li></ul> |
| Automatiškai atnaujinti dėžių skaičių | Kai ši pasirinktis nustatyta kaip *Taip*, visas kartonines dėžes galima sudėti ir rodyti reiso ir konteinerio lygiuose. Kai nustatyta *Ne*, dėžių skaičius iš pradžių nustatomas kaip 0 (nulis), o prireikus jį galima redaguoti rankiniu būdu. |

### <a name="costing-fasttab"></a>Įkainojimo „FastTab“ skirtukas

Šioje lentelėje aprašomi laukeliai, esantys „FastTab“ skirtuke **Įkainojimas**, kuris yra skirtuke **Bendra**, puslapyje **Iškrovimo kainos parametrai**.

| Parametras | aprašymas |
|---|---|
| Registravimo specifikacija | DK pasirinkite vertės koregavimą:<ul><li>**Iš viso** – KD registruojamas bendrasis skaičius.</li><li>**Prekių grupė** – koregavimas nurodomas kiekvienai prekių grupei.</li><li>**Prekės numeris** – koregavimas nurodomas kiekvienai prekei. Šioje vertėje nurodoma daugiausia informacijos.</li></ul> |
| Leisti nulines išlaidas | Šią parinktį nustatykite kaip *Ne*, kad parodytumėte klaidą, jei naudotojas bandys reiso SF ar pirkimo užsakymui registruoti savikainos vertinimą, neįtraukiant vertės numatomai reiso savikainai. Klaidos pranešimas rodo, kad negalima paskirti 0 (nulinės) savikainos, o SF registruoti nepavyks. Tokiu atveju naudotojas gali rankiniu būdu atnaujinti vertinimą (arba perkonfigūruoti automatinę savikainą), o tada perkelti atnaujintą vertę arba ištrinti savikainą, jei ji netaikoma.<p>Šią parinktį nustatykite kaip *Taip*, jei norite, kad reiso savikaina būtų tuščia. Šiuo atveju, 0 (nulinė) kaina bus paskirta pagal savikainos sritį. Gavus reisą tiekėjo savikainos SF bus galima apdoroti pagal nulinės kainos savikainą.</p><p>Rekomenduojame vertinimą sukonfigūruoti automatiniame savikainos įraše, kad nebūtų rodoma nulinė kainos savikaina. Nors šis įvertinimas nėra visiškai tikslus, jis vis tiek turi būti tikslesnis, nei numatoma nulinė savikaina.</p> |
| Koregavimo registravimo data | Kai registruojate mokėtinų sumų reiso savikainos SF, sudengimų lentelė (atsargų koregavimai) taip pat atnaujinami. Pasirinkite datą, kuri, kaip numatyta, nustatoma puslapyje **Reiso savikainos pasirinkimas**, kai dirbate SF žurnale:<ul><li>**Operacijos data** – naudokite žurnalo datą (registravimo datą).</li><li>**Pirkimo užsakymo SF data** – naudokite atsargų (pirkimo užsakymo) SF finansų registravimo datą.</li><li>**Pasirinkta data** – naudotojas gali nustatyti registravimo datą. Nors data gali būti palikta tuščia, ji vis dar tuščia, kai užregistruojama išlaidų SF, o naudotojas gauna klaidą.</li></ul> |
| Naudoti pirkimo sąskaitos faktūros kvitą | Šią parinktį nustačius kaip *Taip*, išlaidų kaupimo operacijos naudos tą patį kvito numerį, kuris naudojamas pirkimo SF. Nustačius *Ne*, sistema naudos kitą galimą skaičių **Savikainos kaupimo kvito** numeracijai, kuri yra nustatyta skirtuke **Numeracija**, puslapyje **Iškrovimo kainos parametrai**.<p>Ši parinktis veikia tik kai pirkimo užsakymui išrašoma SF, jei pasirinktis **Registruoti DK mokesčių sąskaitoje** yra nustatyta kaip *Taip* skirtuke **SF**, esančiame **Mokėtinų sumų parametrai** puslapyje.</p> |
| Blokuoti rankinį registravimą tarpuskaitos sąskaitoje | Šią parinktį nustatykite kaip *Taip*, kad nebūtų registruojama kliringo sąskaitose, kai operacija nėra susieta su reisu, tiekėjo SF žurnalo veiksmų srityje pasirinkus **Funkcijos \> Pasirinkti reiso savikainą**. Rekomenduojame šią parinktį nustatyti kaip *Taip*, kad reiso ir kliringo sąskaitą būtų galima teisingai nustatyti. |
| Naudoti išlaidų tipo kredito kaupimo sąskaitą | Šią parinktį nustačius kaip *Taip*, savikainai kaupti kaip išlaidoms bus naudojama mokesčio kaupimo sąskaita, kuri konfigūruojama atitinkamam savikainos tipo kodui puslapyje **Savikainos tipo kodai**.<p>Ši parinktis veikia tik kai pirkimo užsakymui išrašoma SF, jei pasirinktis **Registruoti DK mokesčių sąskaitoje** yra nustatyta kaip *Taip* skirtuke **SF**, esančiame **Mokėtinų sumų parametrai** puslapyje. |
| Uosto koregavimai kaip nuokrypis | Šią parinktį nustačius kaip *Taip*, nepaisoma standartinių funkcijų ir priverstinai atliekamos atliekų koregavimo operacijos, susijusios su nuokrypiais tarp įvertintos savikainos, kuri registruojama nuokrypio sąskaitoje.<p>Šią parinktį nustačius kaip *Ne*, su nuokrypiais susijusios atsargų koregavimo operacijos tvarkomos pagal įkainojimo būdo konfigūraciją ir savikainos tipo kodą. Standartinės savikainos nuokrypiai vis tiek registruojami nuokrypio sąskaitoje. Perkeliant svertinį vidurkį (WMA) nuokrypiai bus registruojami į nuokrypio sąskaitą arba į atsargas.</p><p>Ši parinktis veikia tik kai pirkimo užsakymui išrašoma SF, jei pasirinktis **Registruoti DK mokesčių sąskaitoje** yra nustatyta kaip *Taip* skirtuke **SF**, esančiame **Mokėtinų sumų parametrai** puslapyje.</p> |

### <a name="validation-fasttab"></a>Tikrinimo „FastTab“ skirtukas

Šioje lentelėje aprašomi laukeliai, esantys „FastTab“ skirtuke **Tikrinimas**, kuris yra skirtuke **Bendra**, puslapyje **Iškrovimo kainos parametrai**.

| Parametras | aprašymas |
|---|---|
| Kelios išlaidų sąskaitos faktūros | Pasirinkite, kas atsitinka, jei toms pačioms papildomoms išlaidoms apdorojama daugiau nei viena SF pagal reisą, registravimo lapą ar konteinerį.<ul><li>**Priimti** – sistema turėtų leisti naudoti kelias savikainos SF.</li><li>**Įspėjimas** – rodomas įspėjimas.</li><li>**Klaida** – rodomas klaidos pranešimas.</li></ul> |
| Keli tiekėjai sąskaitos lape | Pasirinkite, kas turi įvykti, jei prie registracijos lapo pridedamas daugiau nei vieno tiekėjo pirkimo užsakymas.<ul><li>**Priimti** – sistema turėtų leisti atlikti veiksmą.</li><li>**Įspėjimas** – rodomas įspėjimas, bet veiksmą vis tiek galima atlikti.</li><li>**Klaida** – rodomas klaidos pranešimas, o veiksmo atlikti neleidžiama.</li></ul><p>Jūsų muitinės brokeris arba vietos įstatymai gali nustatyti konkrečią šio laukelio vertę.</p> |
| Keliagubo pristatymo leistino nuokrypio režimas | Pasirinkite, kas vyksta, jei į tą reisą įtraukiami pirkimo užsakymo, kuriame naudojamas kitas pristatymo būdas nei reisas, prekės.<ul><li>**Priimti** – sistema turėtų leisti atlikti veiksmą.</li><li>**Įspėjimas** – rodomas įspėjimas, bet veiksmą vis tiek galima atlikti.</li><li>**Klaida** – rodomas klaidos pranešimas, o veiksmo atlikti neleidžiama.</li></ul> |
| Kelių sandėlių leistinas nuokrypis | Pasirinkite, kas vyksta, jei reise yra kelios užsakymo eilutės, kurias reikia pristatyti į skirtingus sandėlius. Šias užsakymo eilutes galima paskirstyti vienam ar daugiau pirkimo užsakymų.<ul><li>**Priimti** – sistema turėtų leisti atlikti veiksmą.</li><li>**Įspėjimas** – rodomas įspėjimas.</li><li>**Klaida** – rodomas klaidos pranešimas.</li></ul> |
| Trūksta tūrio | Pasirinkti, kas vyksta, jei naudotojas prideda prekę be reiso tūrio.<ul><li>**Priimti** – sistema turėtų priimti prekę.</li><li>**Įspėjimas** – rodomas įspėjimas.</li><li>**Klaida** – rodomas klaidos pranešimas.</li></ul><p>Jei tūriai naudojami savikainai apskaičiuoti ir priskirti, rekomenduojame pasirinkti *Įspėjimas* arba *Klaida*.</p> |
| Paslaugų teikėjas be reiso išlaidų | Pasirinkite, kas vyksta, jei naudotojas bando apdoroti paslaugų teikėjo, kuris nebuvo susietas su reisu, SF. <ul><li>**Priimti** – sistema turėtų leisti atlikti veiksmą.</li><li>**Įspėjimas** – rodomas įspėjimas.</li><li>**Klaida** – rodomas klaidos pranešimas.</li></ul><p>Rekomenduojame pasirinkti *Įspėjimas*.</p> |

### <a name="defaults-fasttab"></a>Numatytųjų verčių „FastTab“ skirtukas

Šioje lentelėje aprašomi laukeliai, esantys „FastTab“ skirtuke **Numatytosios vertės**, kuris yra skirtuke **Bendra**, puslapyje **Iškrovimo kainos parametrai**.

| Parametras | aprašymas |
|---|---|
| Žurnalo pavadinimas | Pasirinkite numatytąjį žurnalą, kurį turėtų naudoti funkcija *Kurti atvykimo žurnalą*. |
| Reiso būsena | Pasirinkite būseną, kurią reisas turi turėti, kad naudotojai galėtų nustatyti jo nuomos siuntimo konteinerį sistemoje. Šis veiksmas paprastai vyksta, kai tai yra tranzito arba rampos prekės. |
| Kelionės šablonas | Pasirinkti numatytąjį veiklos ciklo šabloną, kuris bus naudojamas naujiems nuomos siuntimo konteineriams. Paprastai turėsite pasirinkti veiklos ciklo šabloną su nuomos savikaina. |
| Judėjimas | Jei per didelis / per mažas pristatymo kiekis yra nurodyto nuokrypio ribose, perkėlimo žurnalas apdorojamas automatiškai. Pasirinkite norimą naudoti numatytąjį perkėlimo žurnalą. Pasirinkto perkėlimo žurnalo pavadinimo laukelis **Korespondentinė sąskaita** turi turėti vertę. |
| Perkelti | Apdorojus nepakankamą pristatymą trūkstamo kiekio kvitas perkeliamas į trūkstamo kiekio sandėlį. Pasirinkite norimą naudoti numatytąjį perkėlimo žurnalą. |
| Išjungti ne reisų pirkimo užsakymus | Pirkimo užsakymams, kurie nėra pridėti prie reiso, išjunkite iškrovimo kainos perteklinio / nepakankamo kiekio pristatymo funkciją. |
| Išjungti ne tranzito prekių pirkimo užsakymus | Pirkimo užsakymams, kurie nenaudoja prekių tranzito prekių funkcijai, išjunkite iškrovimo kainos perteklinio / nepakankamo kiekio pristatymo funkciją. |
| Tranzito prekių perviršio atidėjimo laikotarpis | Nurodykite dienų skaičių po pirmojo siuntimo konteinerio gavimo, kai tam siuntimo konteineriui dar galima užpildyti papildomus gavimus. |

## <a name="status-updates-tab"></a>Būsenos atnaujinimo skirtukas

Sistema būsenos vertes naudoja kiekvieno reiso būsenai nurodyti. Reiso būsenos vertes galima automatiškai taikyti reisams naudojant reiso sekimą arba periodines paketines užduotis. Taip pat galima rankiniu būdu jas pritaikyti atidarant reisą ir pasirenkant būseną grupėje **Reiso atnaujinimas**, veiksmų srityje esančiame skirtuke **Valdymas**. 

Galima sukurti tiek reiso būsenos verčių, kiek norite. Tačiau keturis iš jų būtina nustatyti naudojimui specialiu tikslu skirtuke **Būsenos atnaujinimai**, esančiame puslapyje **Iškrovimo kainos parametrai**. Toliau pateikiamoje lentelėje aprašomi laukeliai, kuriuos ten galima naudoti.

| Parametras | aprašymas |
|---|---|
| Įkainota | Pasirinkite reiso būseną, kuri identifikuoja, kad reisas buvo baigtas. |
| Gabenama | Pasirinkite reiso būseną, kuri identifikuoja, kad reisas yra tranzite. |
| Paruošta įkainojimui | Pasirinkite reiso būseną, kuri identifikuoja, kad reisas paruoštas įkainojimui. Ši būsena naudojama apdorojus reiso visas atsargų pirkimo SF ir reiso išlaidų SF, kurių laukelis **Reiso savikainos kreditas** nustatomas kaip *Tiekėjas*. Reisų, kurių įkainojimo procesas nesėkmingas, būsena yra *Parengta įkainoti*.|
| Iš anksto įkainota | Pasirinkite reiso būseną, kuri identifikuoja, kad reisas įkainojamas iš anksto. Ši būsena naudojama, kai nauja išlaidų operacija įtraukiama į reisą po to, kai ji jau įkainota. Naujas išlaidų operacijas galima pridėti prie anksčiau įkainotų reisų, kai gauta antroji transportavimo SF arba netikėta mokesčių nuolaida. Ši būsena automatiškai taikoma, kai prie įkainoto reiso pridedama nauja reiso savikaina. |

## <a name="voyage-creator-tab"></a>Reiso kūrimo skirtukas

Toliau esančioje lentelėje aprašomi skyriai skirtuke **Reiso kūrimas**, puslapyje **Iškrovimo kainos parametrai**.

| Skyrius | aprašymas |
|---|---|
| Nuokrypiai | Laukeliai **Už tūrio leistino nuokrypio ribų** ir **Už leistino svorio nuokrypio ribų** apibrėžia ribines reikšmes, kurias viršijus prekės laikomos per didelio tūrio arba svorio. Kai naudotojas puslapyje **Reiso rengyklė** prideda prekes, jei tūris arba svoris viršija ten nustatytą vertę, sistemoje rodomas įspėjimas. Kiekvieno laukelio vertė išreiškiama kaip procentinė didžiausio tūrio arba svorio procentinė dalis, nustatyta susijusiam siuntimo konteinerio tipui. Rekomenduojame, kad vertė būtų nuo 5 iki 10 procentų didžiausio tūrio arba svorio. |
| Sąskaitos lapo kūrimo sąranka | Reiso kūrimo proceso metu sistema gali sukurti kelis registravimo lapus. Naudodami šį skyrių nurodykite, kada reikėtų sukurti naują registravimo lapą. Kiekvienai šio skyriaus eilutei sistema patikrins nurodytą lentelę ir laukelį ir sukurs kiekvienos unikalios laukelio vertės registravimo lapą. |

## <a name="cost-estimates-tab"></a>Savikainos vertinimo skirtukas

Skirtuke **Savikainos vertinimas**, esančiame puslapyje **Iškrovimo kainos parametrai** pateikimas tik vienas laukelis: **Numatytoji įkainojimo versija**. Šis laukelis taikomas tik tada, kai įkainojimo būdas yra *Standartinis įkainojimas*. Pasirinkite numatytąją įkainojimo versiją, kurią naudosite periodinei užduočiai *Prekės savikainos kainos atnaujinimas*. Šį nustatymą galite tekti keisti kaskart prasidėjus naujiems finansiniams metams.

## <a name="inventory-dimensions-tab"></a>Atsargų dimensijų skirtukas

Skirtuką **Atsargų dimensijos**, esantį puslapyje **Iškrovimo kainos parametrai** naudokite valdydami tai, kurias turimas atsargų dimensijas reikėtų rodyti kaip numatyta kiekvienam iškrovimo kainos puslapyje, kuriame naudojamos dimensijos.

Pasirinkite dimensiją, tada parinktį **Reiso eilutės**, **Tranzito prekės** ir (arba) **Savikainos vertinimas** nustatykite kaip *Taip* kiekvienam puslapiui, kuriam kaip numatyta bus rodoma ta dimensija. Prireikus pakartokite šį veiksmą su kitomis dimensijomis.

Šio skirtuko parametrai nustato numatytąsias kiekvieno juridinio subjekto puslapio dimensijas. Tačiau naudotojai, dirbantys vienu iš skirtųjų puslapių, gali keisti numatytąsias dimensijas veiksmų srityje pasirinkdami **Atsargos \> Rodyti dimensijas**.

## <a name="number-sequences-tab"></a>Numeracijų skirtukas

Skirtuke **Numeracija**, esančiame puslapyje **Iškrovimo kainos parametrai** nurodoma kiekvieno tipo nuorodos numeracija, kurios reikalauja iškrovimo kaina, tačiau kuri nėra bendrinama visuose juridiniuose subjektuose. Kiekvienai sąrašo nuorodai pasirinkite numeracijos kodą.

> [!NOTE]
> Kelių įmonių konfigūracijoje kiekvienai įmonei (juridiniam subjektui) reikia sukurti skirtingas numeracijas.

## <a name="shared-number-sequences-tab"></a>Bendros numeracijos skirtukas

Skirtuke **Bendra numeracija**, esančiame puslapyje **Iškrovimo kainos parametrai** nurodoma kiekvieno tipo nuorodos numeracija, kuri bendrinama keliuose iškrovimo kainos juridiniuose objektuose. Šiuo metu sąraše yra tik viena numeracija. Ši numeracija naudojama reiso ID.

Puslapyje **Visi reisai** naudotojai gali peržiūrėti visus reisus, visuose juridiniuose subjektuose. Tačiau, norint redaguoti ir apdoroti reisą, naudotojai turi būti pasirinkto įrašo juridiniame subjekte.

## <a name="feature-visibility-tab"></a>Funkcijų matomumo skirtukas

Iškrovimo kaina keliuose dažnai naudojamuose puslapiuose „Microsoft Dynamics 365 Supply Chain Management“ prideda savybių (laukelių ir funkcijų). Šiuose puslapiuose yra puslapių, susijusių su tiekėjo pagrindiniais duomenimis, išleistais produktais, pirkimo užsakymais, perkėlimo užsakymais ir sandėlio nustatymu. Jei naudojate iškrovimo kainą, kad šiomis funkcijomis galėtumėte pasinaudoti, jos turi būti matomos visur. Jei nenaudojate iškrovimo kainos, galite paslėpti funkcijas, kad jos netrukdytų.

Skirtuke **Funkcijų matomumas**, esančiame puslapyje **Iškrovimo kainos parametrai**, parinktį **Įjungti** nustatykite kaip *Taip*, kad iškrovimo kainos funkcijos būtų matomos tada, kai jas galima naudoti. Nustatykite *Ne*, kad paslėptumėte funkcijas bendrai naudojamuose puslapiuose už iškrovimo kainos ribų. Tačiau net parinktį nustačius kaip *Ne*, pats modulis su puslapiu **Iškrovimo kainos parametrai** lieka prieinamas naudotojams, kurie turi tinkamus leidimus juo naudotis.
