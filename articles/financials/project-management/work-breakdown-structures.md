---
title: Darbo paskirstymo struktūros
description: Darbo paskirstymo struktūra (WBS) yra projekto darbo, kuris bus atliekamas, aprašas. Tai – užduočių hierarchija, perteikianti projekto komandos supratimą apie darbo sudėtį ir kiekvieno komponento ar užduoties dydį, kainą ir trukmę.
author: KimANelson
manager: AnnBe
ms.date: 06/05/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df4bc39f8df80580261102941712622ed59262bd
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572355"
---
# <a name="work-breakdown-structures"></a>Darbo paskirstymo struktūros

[!include [banner](../includes/banner.md)]

Darbo paskirstymo struktūra (WBS) yra projekto darbo, kuris bus atliekamas, aprašas. Tai – užduočių hierarchija, perteikianti projekto komandos supratimą apie darbo sudėtį ir kiekvieno komponento ar užduoties dydį, kainą ir trukmę. WBS turi tris pagrindinius tikslus.

-   Užduotimis apibūdinti darbo paskirstymą ar sudėtį.
-   Planuoti projekto darbą.
-   Įvertinti kiekvienos užduoties kainą.

WBS išsamumo laipsnis priklauso nuo vertinant reikalingo tikslumo lygio ir reikalingo sekimo pagal tuos vertinimus lygio. Projektuose, kurių leistini grafiko ar kainos neatitikimai yra labai maži, reikia išsamesnės WBS ir pagal ją kruopščiai sekti darbo eigą bei kainą. Tokie projektai dažni statybų ir inžinerijos pramonėje. 

Priešingai, projektai tokiose pramonės šakose kaip žiniasklaida ir reklama, programinė įranga ir IT infrastruktūra, paprastai nesikartoja, ir produktyvumas yra susijęs su asmens, atliekančio užduotį, patirtimi ir kompetencija. Todėl šiose pramonės šakose WBS naudojama norint įvertinti projekto dydį, o ne išsamiai sekti to projekto eigą. 

WBS kūrimas yra intensyvus procesas, paprastai atliekamas per ilgą laikotarpį ir kurį atliekant reikia itin įvairių žmonių bendradarbiavimo ir informacijos. Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 for Finance and Operations“ naudojant WBS patobulinimus, galima patenkinti įvertinimų ir sekimo reikalavimus.

## <a name="prerequisites-for-creating-a-wbs"></a>WBS kūrimo būtinosios sąlygos
Norėdami sukurti WBS, turite gebėti sukurti darbo grafiką ir įvertinti darbo kainą.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Darbo grafiko kūrimo būtinosios sąlygos

Norėdami naudoti visas WBS funkcijų planavimo galimybes, atlikite tolesnę sąranką.

1.  Nustatykite numatytąjį kalendorių ir projekto kalendorių.
    1.  Spustelėkite **Projektų valdymas ir apskaita** &gt; **Sąranka** &gt; **Projektų valdymo ir apskaitos parametrai** &gt; **Planavimas**. **Numatytojo darbo kalendoriaus** lauke nurodykite numatytąjį kalendorių. Tai bus bet kokio naujai sukurto projekto numatytasis darbo kalendorius.
    2.  Numatytąjį kalendorių galite keisti konkrečiam projektui. Spustelėkite projekto informacijos puslapį ir „FastTab‟ **Projekto komanda ir planavimas** atnaujinkite **Planavimo kalendoriaus** lauką pasirinkdami kitą kalendorių.

2.  Nustatykite standartines darbo dienas ir darbo valandas. Kalendorius, kurį nustatote kaip savo projekto darbo kalendorių, WBS struktūroje bus naudojamas nustatyti tolesnei informacijai.

-   Darbo dienoms ir šventinėms dienoms.
-   Darbo valandų per dieną skaičiui.

Norėdami nustatyti kalendoriaus darbo dienas ir darbo valandas arba sukurti naują kalendorių, spustelėkite **Organizacijos administravimas** &gt; **Bendra** &gt; **Kalendoriai**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Darbo kainos įvertinimo būtinosios sąlygos

Norėdami naudoti visas WBS kainos įvertinimo galimybes, turėtumėte nustatyti darbuotojų, darbo kategorijų, išlaidų, mokesčių ir prekių išlaidas bei pardavimo kainas.

-   Norėdami nustatyti darbo, išlaidų ir mokesčių kategorijų išlaidas bei pardavimo kainą, spustelėkite **Projektų valdymas ir apskaita** &gt; **Sąranka** &gt; **Kainos**.
-   Norėdami nustatyti prekių išlaidas ir pardavimo kainą, kiekvienai prekei naudokite **Prekybos sutarčių** puslapį, esantį Produktų informacijos valdymo modulio sąrašo puslapyje **Išleisti produktai**.

## <a name="creating-a-wbs"></a>WBS kūrimas
Kuriant WBS, atliekamos trys veiklos.

1.  **Darbo skaidymas** – paskirskykite darbą į įvykdomas dalis ar užduotis.
2.  **Darbo grafikas** – įvertinkite laiką, kurio reikia atlikti užduočiai, nustatykite užduočių tarpusavio priklausomybes ir pasirinkite užduočių pradžios bei pabaigos datas.
3.  **Išlaidų įvertinimas** – įvertinkite kiekvienos užduoties išlaidas.

Tolesniuose skyriuose aptariama, kaip WBS galimybės gali padėti vykdyti kiekvieną iš šių veiklų.

### <a name="work-decomposition"></a>Darbo skaidymas

Darbo paskirstymas arba skaidymas paprastai yra pirmasis WBS kūrimo proceso veiksmas. WBS funkcijos palaiko tolesnes pagrindines darbo paskirstymo arba skaidymo konstrukcijas. 

**Projekto šakninė užduotis** projekto šakninė užduotis yra projekto aukščiausio lygio suvestinės užduotis. Po ja kuriamos visos kitos projekto užduotys. Šakninės užduoties pavadinimas visada nustatomas kaip projekto pavadinimas. Šakninio mazgo pastangomis, datomis ir trukme apibendrinamos po šaknine užduotimi esančių užduočių reikšmės. Šakninio mazgo ypatybių modifikuoti ir jo panaikinti negalima.

**Suvestinės ar konteinerio užduotys** suvestinė užduotis yra užduotis, po kuria yra antrinių užduočių ar sudedamųjų užduočių. Suvestinės užduotis neturi jokių savo darbo pastangų ar kainos. Suvestinės užduoties darbo pastangos ir kaina yra jos sudedamųjų užduočių darbo pastangų ir kainos suma. Anksčiausia sudedamųjų užduočių pradžios data naudojama kaip suvestinės užduoties pradžios data, o vėliausia sudedamųjų užduočių pabaigos data naudojama kaip pabaigos data. Galite modifikuoti suvestinės užduoties pavadinimą, tačiau negalite modifikuoti pastangų, datų ir trukmės planavimo ypatybių. Panaikinus suvestinės užduotį, taip pat panaikinamos visos jos sudedamosios užduotys. 

**Lapo mazgų užduotys** lapo mazgo užduotis sudaro detaliausią projekto darbo paketą. Lapo mazge nurodytos įvertintos pastangos, planuojamas išteklių skaičius, planuojama pradžios data ir pabaigos data bei trukmė. 

Atlikę tolesnes hierarchijos operacijas, galite įgalinti darbo hierarchijos kūrimą ar projekto skaidymą. 

**Nauja užduotis** Visos jūsų naujai sukurtos užduotys automatiškai pridedamos po šakniniu mazgu, ir joms automatiškai priskiriamas WBS numeris. WBS numeris perteikia užduoties lygį hierarchijoje. Užduotims pirmajame lygyje po projekto šaknine užduotimi naudojama numeravimo schema „1, 2, 3‟ ir t. t. Užduotims, esančioms po pirmuoju lygiu, naudojama numeravimo schema „1.1, 1.2, 1.3‟ ir t. t. Kiekviename lygyje, pridedamame po ankstesniu lygiu, pridedama nauja skaičių po taško seka. 

Šiuo metu WBS numeravimo tinkinti negalima. 

**Perkėlimo į žemesnį lygį užduotis** Kai užduotį perkeliate į žemesnį lygį, ji tampa antrine prieš ją esančios užduoties užduotimi. Naujosios antrinės užduoties WBS numeris automatiškai perskaičiuojamas pagal jos naujos pirminės užduoties WBS skaičių. Pirminė užduotis dabar yra suvestinės arba konteinerio užduotis, todėl tampa savo sudedamųjų užduočių suma. 

> [!NOTE] 
> Kai užduotis perkeliate į žemesnį lygį nei užduotis, kuri prieš šią operaciją buvo lapo mazgas, naujai sukurta suvestinės užduotis praranda savo datas, pastangas ir išteklių skaičių. Dabar ji naudoja savo naujųjų sudedamųjų užduočių reikšmių suvestinę. 

**Perkėlimo į aukštesnį lygį užduotis** Kai užduotį perkeliate į aukštesnį lygį, ji nebėra jos pirminės užduoties sudedamoji užduotis. Šios užduoties WBS numeris automatiškai perskaičiuojamas, kad atspindėtų užduoties naująjį lygį hierarchijoje. AnkstesnĖs pirminės užduoties pastangos, kaina ir datos perskaičiuojamos, ir ta užduotis neįtraukiama. 

**Perkelti aukštyn ir Perkelti žemyn** Spustelėję **Perkelti aukštyn** ir **Perkelti žemyn**, keičiate užduoties padėtį jos pirminės užduoties hierarchijoje. Užduoties padėtis neturi įtakos jos pastangoms, kainai, datoms ar trukmei. Tačiau užduoties WBS numeris automatiškai perskaičiuojamas, kad atspindėtų užduoties naująją padėtį.

### <a name="schedule-estimation"></a>Grafiko įvertinimas

Grafiko įvertinimas paprastai yra antrasis veiksmas kuriant WBS. Geriausia grafiko įvertinimą atlikti sukūrus užduotis. „Finance and Operations“ puslapį **Darbo paskirstymo struktūra** sudaro dvi dalys. Viršutinioji sritis skirta įvertinti grafikui, o apatinėje srityje yra **Įvertintų išlaidų ir įplaukų** skirtukas, kurį galite naudoti įvertinti išlaidoms. 
**Užduočių priklausomybės** WBS struktūroje tarp užduočių galite sukurti ankstesnį ryšį. Kai užduočiai priskiriate ankstesnių užduočių, tą užduotį galite pradėti tik tada, kai atliktos visos jos ankstesnės užduotys. Planuojama užduoties pradžios data automatiškai nustatoma į vėliausią visų jos ankstesnių užduočių datą. 

**Užduočių planavimas programoje „Microsoft Dynamics 365 for Finance and Operations“** Lapo mazgų užduočių planavimas nustatomas naudojant pateiktus veiksnius.

-   Ankstesnė veikla
-   Pastanga
-   Išteklių skaičius
-   Pradžios ir pabaigos datos

Lapo mazgo užduoties, neturinčios ankstesnių užduočių, pradžios data automatiškai nustatoma į projekto planavimo pradžios datą. Lapo mazgo užduoties trukmė visada apskaičiuojama kaip darbo dienų tarp jos pradžios iki pabaigos datų skaičius. 

*<strong><em>Planavimo taisyklės</em></strong>*  Kai įjungta automatinio planavimo pagalba, lapo mazgų užduočių planavimui taikomos tolesnės taisyklės.

-   Užduoties pradžios ir pabaigos datos turi būti darbo dienos, atsižvelgiant į projekto planavimo kalendorių.
-   Užduoties, turinčios ankstesnių užduočių, pradžios data automatiškai nustatoma į vėliausią visų jos ankstesnių užduočių pabaigos datą.
-   Užduoties pastangos automatiškai apskaičiuojamos kaip nurodyta toliau.

Žmonių skaičius x trukmė x valandų per standartinę projekto kalendoriaus darbo dieną skaičius. 

Kai kuriais atvejais galbūt norėsite nuo šių taisyklių nukrypti. Automatinį planavimą galite išjungti, kad „Finance and Operations‟ automatiškai nenustatinėtų ir netaisytų jokių lapo mazgų užduočių ypatybių. Kai įvedate užduoties informaciją, pažeidžiančią bet kokias planavimo taisykles, rodoma užduoties planavimo klaidos piktograma. Jei nenorite, kad būtų rodomos planavimo klaidos, spustelėkite **Planavimo klaidos rodomos** – funkciją išjungsite. 

> [!NOTE] 
> Suvestinės ar konteinerio užduoties reikšmės toliau apskaičiuojamos kaip sudedamųjų užduočių reikšmių suma, neatsižvelgiant į tai, ar automatinio planavimo pagalba įjungta, ar išjungta. 

**Planavimo klaidų taisymas** Kai įjungta automatinio planavimo pagalba, planavimo klaidos nėra tikėtinos. Tačiau, jei išjungiate automatinio planavimo pagalbą ir vėliau ją vėl įjungiate, WBS struktūroje gali atsirasti planavimo klaidų piktogramų. 

**Planavimo klaidų taisymas pagal užduotį** Kai dukart spustelite konkrečios užduoties grafiko klaidos piktogramą, dialogo lange rodomos visos tos užduoties planavimo klaidos. Galite nuspręsti, kurias užduoties planavimo klaidas taisyti. 

**Visų planavimo klaidų taisymas** Jei norite, kad „Finance and Operations‟ ištaisytų visas WBS planavimo klaidas, veiksmų srityje spustelėkite **Taisyti visus planavimo nesutapimus**. 

> [!NOTE] 
> Naudojant šią funkciją, WBS gali būti žymiai modifikuota. Klaidos taisomos tolesne tvarka.

1.  Modifikuojamos visų užduočių įvertintos pastangos, kad jos būtų lygios pajėgumui, kuris apibrėžtas projekto kalendoriuje.
2.  Modifikuojama kiekvienos užduoties pradžios data, kad užduotis prasidėtų atlikus visas jos ankstesnes užduotis.
3.  Modifikuojama kiekvienos užduoties pradžios data, kad būtų pašalinti ankstesnių užduočių pradžios datų tarpai.

### <a name="cost-estimation"></a>Savikainos įvertinimas

Kaip buvo minėta pirmiau šiame dokumente, kiekvienos lapo mazgo užduoties išlaidų įvertinimas įvedamas naudojant **Įvertintų išlaidų ir įplaukų** skirtuką, esantį apatinėje **Darbo paskirstymo struktūros** puslapio srityje. 

> [!NOTE] 
> Suvestinės ir konteinerio užduoties išlaidų įvertinimo modifikuoti negalima. Suvestinės užduoties išlaidų įvertinimas lygus jo lapo mazgų užduočių išlaidų įvertinimo sumai. Įvertintos bendrosios kiekvienos užduoties išlaidos apskaičiuojamos kaip tolesnių operacijų tipų įvertintų išlaidų suma.

-   Darbas
-   Prekė ar medžiaga
-   Išlaidos

**Mokesčio** operacijos tipas naudojamas įvertinti mokestinėms įplaukoms. Šis operacijos tipas neturi išlaidų komponento, todėl, vertinant išlaidas, į jį neatsižvelgiama. 

**Laisvos formos** operacijos tipas naudojamas fiksuoti fiksuotos vertės tipo projekto pardavimo vertei pagal sutartį. Vertinant išlaidas, į šį operacijos tipą taip pat neatsižvelgiama. 

Kai vertinante kiekvienos užduoties darbo, medžiagų ir išlaidų sumas, įvertintoms išlaidoms turite priskirti projekto kategoriją. 

**Darbo išlaidų įvertinimas** Kiekvienai lapo mazgo užduočiai priskiriamos darbo pastangos valandomis ir numatytoji kategorija. Todėl, nustatant užduoties grafiką, tos užduoties įvertintos darbo išlaidos automatiškai pridedamos į numatytąją darbo kategoriją. Šios įvertintos išlaidos rodomos **Įvertintų išlaidų ir įplaukų** skirtuke, esančiame tos užduoties **Eilutės informacijos** tinklelyje. Jei reikia daugiau darbo išlaidų įvertinimų, jų įtraukti galite šiame skirtuke. Jei padidinate arba sumažinate įvertintų darbo išlaidų valandas, automatiškai perskaičiuojamas užduoties grafikas. 

**Išlaidų ir medžiagų sumų įvertinimas** **Įvertintų išlaidų ir įplaukų** skirtuke taip pat galima įvertinti (jei reikia) užduoties išlaidų ir medžiagų sumas. 

Kiekvienos įvertinto darbo ar išlaidų eilutės išlaidos ir pardavimo kaina paremtos kiekvienos kategorijos sąranka, apibrėžta kainodaros lentelėse: **Projektų valdymas ir apskaita** &gt; **Sąranka** &gt; **Kainodara**. Prekių išlaidos ir pardavimo kaina pagal numatytąsias nuostatas pridedamos iš prekių ar prekybos sutarčių, nurodytų Produktų informacijos valdymo modulio sąrašo puslapyje **Išleisti produktai**.

## <a name="tracking-progress-on-the-wbs"></a>WBS eigos sekimas
Kai kuriose pramonės šakose projekto eiga pagal WBS sekama labai detaliu lygiu, o kitose eiga sekama aukštesniu WBS lygiu. Šiame skyriuje aprašoma, kaip pagal savo projekto reikalavimus galite naudoti WBS sekimą. 

Programoje „Finance and Operations“ yra trys projekto WBS rodiniai: Planavimo rodinys, Pastangų sekimo rodinys ir Išlaidų sekimo rodinys.

### <a name="planning-view"></a>Planavimo rodinys

Planavimo rodinyje rodomas planuojamas arba bazinis grafiko ir išlaidų informacijos įvertinimas. Nors nėra funkcijų, skirtų sekti projekto WBS versijai ir bazei, šio rodinio reikšmės skirtos perteikti bazinei versijai. Šios temos Grafiko įvertinimo ir Išlaidų įvertinimo skyriuose aprašomas šis rodinys ir tai, kaip jis naudojamas kurti WBS.

### <a name="effort-tracking-view"></a>Pastangų stebėjimo rodinys

Pastangų sekimo rodinyje rodomas WBS užduočių eigos sekimas. Jame sukauptos faktinės užduoties pastangų valandos lyginamos su suplanuotų pastangų valandomis. Pastangų sekimo rodinyje reikšmės gaunamos pagal tolesnes formules.

-   Eigos procentas = faktinės pastangos iki šiol ÷ suplanuotos užduoties pastangos
-   Likusios pastangos (taip pat vadinamos Įvertinta prieš baigiant \[ETC\]) = suplanuotos pastangos – faktinės pastangos iki šiol
-   Įvertinta baigus (EAC) = likusios pastangos + faktinės pastangos iki šiol
-   Numatytas pastangų nuokrypis = suplanuotos pastangos – EAC

Pastangų sekimo rodinyje rodoma užduoties pastangų nuokrypio projekcija, atsižvelgiant į tai, ar EAC yra daugiau už suplanuotas pastangas, ar mažiau.

-   Jei EAC yra daugiau nei suplanuotos pastangos, numatoma, kad užduočiai atlikti prireiks daugiau laiko nei iš pradžių planuota, ir užduotis vėluoja.
-   Jei EAC yra mažiau nei suplanuotos pastangos, numatoma, kad užduočiai atlikti prireiks mažiau laiko nei iš pradžių planuota, ir užduotis lenkia grafiką.

**Projekto vadovo pakartotinė pastangų projekcija** Kartais projekto vadovas arba kitas asmuo, sekantis projekto eigą, turės peržiūrėti pradinius užduoties įvertinimus. Dėl įvairių priežasčių užduotis gali būti atliekama greičiau arba lėčiau nei tikėtasi iš pradžių. Pvz., sumažinta aprėptis arba darbuotojai turi mažiau patirties negu planuota iš pradžių. Projekcijos yra tai, kaip projekto vadovas, atsižvelgdamas į dabartinę projekto būseną, suvokia įvertinimus. Apskritai nereikėtų keisti bazinių skaičių, nes projekto bazė perteikia plačiai paskelbtą dokumentą, kuriame įvertinamas projekto grafikas ir išlaidos, ir dėl kurio susitarė visos suinteresuotos projekto šalys. 

Užduočių pastangas projektų vadovai gali modifikuoti dviem būdais.

-   Modifikuoti likusias pastangas, kuriomis nustatyta automatiškai atnaujinti faktines likusias užduoties pastangas.
-   Modifikuoti eigos procentą, kuriuo nustatyta automatiškai atnaujinti tikrąją užduoties eigą.

Naudojant šiuos abu metodus, perskaičiuojama užduoties ETC, EAC, ir eigos procentas bei numatomas užduoties pastangų nuokrypis. Suvestinės užduočių EAC, ETC ir eigos procentas taip pat perskaičiuojami, o jų numatomas pastangų nuokrypis atnaujinamas. 

**Modifikuotos suvestinės užduočių pastangos** Galite modifikuoti suvestinės ar konteinerio užduočių pastangas. Nesvarbu, ar šias reikšmes modifikuosite naudodami likusias suvestinės užduočių pastangas, ar eigos procentą: automatiškai skaičiuojama tolesne tvarka.

1.  Skaičiuojama EAC, ETC ir užduoties eigos procentas.
2.  Naujoji EAC antrinėms užduotims paskirstoma vienodai kaip pradinė EAC suma.
3.  Skaičiuojama naujoji kiekvienos lapo mazgo užduoties EAC.
4.  Pagal naujają EAC reikšmę perskaičiuojamos visų paveiktų antrinių užduočių pastangos ir eigos procentas. Taip pat perskaičiuojamas leistinas užduočių pastangų nuokrypis.
5.  Taip pat iš lapo mazgų perskaičiuojama suvestinės užduočių EAC.

Pastangų sekimo rodinyje spustelėję **Išplėsti iki lygio**, nustatysite lygį, kuriuo sekti ir prižiūrėti jūsų WBS. Kai tik atidarysite Pastangų sekimo rodinį, WBS bus automatiškai išplėsta iki to lygio.

### <a name="cost-tracking-view"></a>Išlaidų stebėjimo rodinys

Išlaidų sekimo rodinyje rodomas užduoties išlaidų naudojimo sekimas. Šiame rodinyje iki šiol patirtos faktinės užduoties išlaidos lyginamos su suplanuotomis užduoties išlaidomis. Išlaidų sekimo rodinyje reikšmės gaunamos pagal tolesnes formules.

-   Sunaudotų išlaidų procentinė dalis = faktinės išlaidos iki šiol ÷ suplanuotos užduoties išlaidos
-   Išlaidos prieš baigiant (CTC) = suplanuotos išlaidos – faktinės išlaidos iki šiol
-   Įvertinta baigus (EAC) = CTC + faktinės išlaidos iki šiol
-   Numatomas išlaidų nuokrypis = suplanuotos išlaidos – EAC

Išlaidų sekimo rodinyje rodoma užduoties išlaidų nuokrypio projekcija, atsižvelgiant į tai, ar EAC yra daugiau už suplanuotas išlaidas, ar mažiau.

-   Jei EAC yra daugiau nei suplanuotos išlaidos, numatoma, kad užduočiai atlikti prireiks daugiau pinigų nei iš pradžių planuota, ir užduotis viršija biudžetą.
-   Jei EAC yra mažiau nei suplanuotos išlaidos, numatoma, kad užduočiai atlikti prireiks mažiau pinigų nei iš pradžių planuota, ir užduotis nesiekia biudžeto.

**Projekto vadovo pakartotinė išlaidų projekcija** Projektų vadovai turi naudoti CTC ir peržiūrėti pradinį užduoties išlaidų įvertinimą. Projekto vadovas gali modifikuoti CTC reikšmę ir ją nustatyti į išlaidų, kurių reikia atlikti šiai užduočiai, reikšmę. Jei modifikuojate CTC reikšmę, perskaičiuojamos užduoties CTC, EAC ir sunaudotų išlaidų procentinė dalis bei numatomas užduoties išlaidų nuokrypis. Suvestinės užduočių EAC, ETC ir sunaudotų išlaidų procentas taip pat perskaičiuojami, o jų numatomas išlaidų nuokrypis atnaujinamas. 

> [!NOTE] 
> Kai Pastangų sekimo rodinyje peržiūrite WBS užduoties pastangas, užduoties CTC, EAC, sunaudotų išlaidų procentinė dalis ir numatomas išlaidų nuokrypis perskaičiuojami Išlaidų sekimo rodinyje. Tačiau išlaidų peržiūra neturi įtakos Pastangų sekimo rodinio reikšmėms, nes išlaidos neperžiūrimos pagal operacijos tipą (darbo, medžiagų ar išlaidų) ar projekto kategoriją. 

**Suvestinės užduočių išlaidų projekcijų tikslinimas** Galite peržiūrėti suvestinės užduočių išlaidas, ir skaičiavimai automatiškai atliekami tolesne tvarka.

1.  Perskaičiuojama EAC, CTC ir užduoties sunaudotų išlaidų procentinė dalis.
2.  Naujoji EAC antrinėms užduotims paskirstoma vienodai kaip pradinė užduočių EAC.
3.  Apkaičiuojama naujoji kiekvienos užduoties EAC.
4.  Pagal EAC reikšmę perskaičiuojamos paveiktų antrinių užduočių CTS ir sunaudotų išlaidų procentinė dalis. Taip pat perskaičiuojamas leistinas užduočių išlaidų nuokrypis.
5.  Pagal šį pakeitimą perskaičiuojama visų suvestinės užduočių EAC.

Išlaidų sekimo rodinyje spustelėję **Išplėsti iki lygio**, nustatysite lygį, kuriuo sekti ir prižiūrėti jūsų WBS. Kai tik atidarysite Išlaidų sekimo rodinį, WBS bus išplėsta iki to lygio.

### <a name="earned-value-management"></a>Gautos vertės valdymas

Projekto eigai sekti galite naudoti gautos vertės metodą (EVM). Gautos vertės metriką galite peržiūrėti projekto vadovo vaidmenų centre. Gautos vertės diagramos komponentas rodo laipsniškai laike išdėstytas suplanuotos vertės ir faktinių išlaidų reikšmes. Iki šios datos gauta vertė rodoma kaip taškas. Laipsniškai laike išdėstyti gautos vertės duomenys šiuo metu negalimi. 

Gautos vertės diagramoje laiko etapas rodomas pagal savaitę ar pagal mėnesį. Šiame skyriuje aprašomi trys pagrindiniai EVM komponentai: suplanuota vertė, gauta vertė ir faktinės išlaidos. 

**Suplanuota vertė** EVM teorija teigia, kad planuojamos vertės brėžinys yra sparta, kuria projekto komanda planavo gauti projekto vertę. 

Žymėdama suplanuotą vertę, „Finance and Operations“ naudoja gavimo taisyklę 0:100. Pagal šią taisyklę užduoties vertė užduotyje registruojama iki jos pabaigos datos. Kol užduotis neatlikta 100 procentų, vertė neregistruojama. 

Projektų valdymo ir apskaitos modulyje įvedama lapo mazgų pabaigos data ir suplanuotos jos išlaidos. Kai suplanuotos vertės grafikas rodomas pagal savaitę, visų lapo mazgų užduočių suplanuota vertė visą projekto trukmę apibendrinama pagal savaitę. 

**Gauta vertė** EVM teorija teigia, kad gautos vertės brėžinys yra sparta, kuria projekto komanda faktiškai gauna projekto vertę. 

Žymėdama gautą vertę, „Finance and Operations“ naudoja gavimo taisyklę 0:100. Pagal šią taisyklę užduoties vertė užduotyje registruojama iki jos pabaigos datos. Kol užduotis neatlikta 100 procentų, vertė neregistruojama. 

Kai skaičiuojama gauta vertė, atsižvelgiama į kiekvienos užduoties eigos procentą. Pagal gavimo taisyklę 0:100, skaičiuojant iki tam tikro laikotarpio pabaigos gautą vertę, atsižvelgiama į tik tuo laikotarpiu atliktas užduotis. Skaičiuojama visų projekto užduočių, atliktų kuriant grafiką, gauta vertė. 

> [!NOTE] 
> Šiuo metu WBS sekimo sistema neturi duomenų struktūrų istoriniams kiekvienos užduoties eigos procentams saugoti. Todėl gauta vertė gali būti deklaruojama tik iki kubo apdorojimo laiko. Kubą apdorokite reguliariai, kad atnaujintumėte gautos vertės duomenis, rodomus vaidmenų centre. 

**Faktinės išlaidos** EVM teorija teigia, kad faktinių išlaidų brėžinys yra sparta, kuria projektui išleidžiami pinigai. 

Brėžti faktinių išlaidų linijai naudojamos operacijos, registruojamos projekte. Išlaidos sumuojamos pagal datą. Šie duomenys tada naudojami gautos vertės diagramoje pagal savaitę arba pagal mėnesį vaizduoti faktinėms išlaidoms.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Kaip naudoti suplanuotos vertės, gautos vertės ir faktinių išlaidų koncepcijas

**Grafiko nuokrypis** Planuodami laiko juostoje kuriate darbo prognozę. Todėl suplanuota vertė yra sparta, kuria projekto planuotojai manė, kad bus atliekamas projekto darbas. Vykdant projektą, atliekamas darbas ir projektas gauna vertę. Suplanuotą vertę lygindami su gauta verte, galite peržiūrėti, kaip vyksta projekto darbas. Šio lyginimo rezultatas vadinamas grafiko nuokrypiu. 

Jei suplanuota laikotarpio vertė yra didesnė už gautą vertę, atliktas projekto darbo kiekis yra mažesnis nei buvo planuota. Todėl projektas atsilieka nuo grafiko. Kadangi suplanuota vertė ir gauta vertė išreikštos pinigine išraiška, projekto delsos laikui taip pat suteikiama piniginė vertė. 

Jei suplanuota laikotarpio vertė yra mažesnė už gautą vertę, atliktas projekto darbo kiekis yra didesnis nei buvo planuota. Todėl projektas grafiką lenkia. Šiam lenkimo laikui taip pat suteikiama piniginė vertė.

**Išlaidų nuokrypis** Kadangi gauta vertė kaip daugiklį naudoja savikainą, ji nurodo atlikto projekto darbo išlaidas. Vykdant projektą, operacijų žurnale pateikiamas pinigų, faktiškai išleistų tam projektui, įrašas. Gautą vertę lygindami su faktinėmis išlaidomis, galite peržiūrėti išleidžiamų pinigų sumą ir ją palyginti su gaunama verte. Šio lyginimo rezultatas vadinamas išlaidų nuokrypiu. 

Jei faktinės išlaidos, patirtos per tam tikrą laikotarpį, yra didesnės už gautą vertę, pinigų buvo daugiau išleista nei gauta. Todėl projektas viršija biudžetą. 

Jei faktinės išlaidos, patirtos per tam tikrą laikotarpį, yra mažesnės už gautą vertę, pinigų buvo daugiau gauta nei išleista. Todėl projektas nesiekia biudžeto.

## <a name="wbs-templates"></a>WBS šablonai
Naudodami WBS šablonų funkcijas, galite kurti standartinius projektų šablonus. Jei, vykdant projektus, kuriuos siūlo jūsų įmonė, yra daug pasikartojančio darbo, pagalvokite, ar nereikėtų sukurti WBS šablono. 

WBS šabloną galite kurti iš esamo projekto WBS, kad, planuojant tą projektą surinktas žinias ir geriausią praktiką būtų galima dar kartą panaudoti būsimiems panašiems projektams. Tačiau kartais gali nebūti prasmės kaip šabloną naudoti visą WBS. Todėl šablonus galite kurti iš projekto WBS dalių.

### <a name="saving-a-projects-wbs-as-a-template"></a>Projekto WBS įrašymas kaip šablono

Kai sukuriate šabloną, jį importuoti į naują projekto WBS galite po šakniniu mazgu arba po bet kuria projekto WBS užduotimi.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>WBS šablono Importavimas į projekto WBS

Kai importuojate užduotis, šablono užduotys išdėstomos pagal užduoties, po kuria jos importuojamos, pradžios datą. Importavimo metu ankstesni šablono užduočių ryšiai naudojami apskaičiuoti importuojamų užduočių pradžios datoms. Paskirties projekto standartinis darbo kalendorius taikomas apskaičiuojant importuotų užduočių pabaigos datas, kad būtų išlaikytos dabartiniame projekto darbo kalendoriuje apibrėžtos darbo dienos ir standartinės darbo valandos. 

Įvertinimo eilučių išlaidų sumos ir pardavimo kainos taikomos norint užtikrinti, kad konkretaus projekto ar projekto sutarties kainų datos būtų galiojančios.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Skirtumai tarp projekto WBS ir WBS šablono

-   WBS šablonų užduotys neturi pradžios ir pabaigos datų.

WBS šablonuose nenustatytos darbo ir nedarbo dienos.

-   WBS šablonuose visada naudojamas planavimo kalendorius, nustatytas kaip numatytasis visų projektų kalendorius.

Numatytasis planavimo kalendorius naudojamas tik norint sužinoti standartinės darbo dienos valandas.

-   Ankstesni ryšiai nėra kopijuojami į WBS šabloną.

Kadangi WBS šablonai neturi datų, nereikia pradžios datos logikos, paremtos ankstesnės užduoties pabaigos data.

-   Kai WBS šablone sukuriama užduotis, automatiškai sukuriama darbo išlaidų įvertinimo eilutė. Pardavimo kaina ir išlaidų suma kopijuojama iš pasirinkto darbuotojo.

Išlaidų ir prekių sumą galima kurti rankiniu būdu, kaip ir projekto WBS struktūroje.

-   Kai, taikant tolesnę formulę, atsiranda nuokrypių, rodomos planavimo klaidos.

Pastangos = išteklių skaičius × trukmė × standartinės darbo dienos valandų skaičius 

Vienu metu visas planavimo klaidas galite ištaisyti spustelėdami **Taisyti visas planavimo klaidas**. 

Taip pat planavimo klaidas galite taisyti atskirai – spustelėkite kiekvienos užduoties įspėjimo piktogramą.



