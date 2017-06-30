---
title: "Ataskaitų dizaino įrankio ataskaitų medžio aprašai"
description: "Šiame straipsnyje pateikiama informacija ataskaitų medžių aprašus. Ataskaitų medžio aprašas yra ataskaitos komponentas, arba kūrimo blokas, kuris padeda nustatyti organizacijos struktūrą ir hierarchiją."
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 57592
ms.assetid: 747faa47-9a23-4277-bc11-8d0a1267c3a4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 331f3480b8454dac7da12be169ba017f36cefa06
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="reporting-tree-definitions-in-financial-reports"></a>Ataskaitų dizaino įrankio ataskaitų medžio aprašai

[!include[banner](../includes/banner.md)]


Šiame straipsnyje pateikiama informacija ataskaitų medžių aprašus. Ataskaitų medžio aprašas yra ataskaitos komponentas, arba kūrimo blokas, kuris padeda nustatyti organizacijos struktūrą ir hierarchiją.

Ataskaitų dizaino įrankis palaiko lanksčias ataskaitas, todėl lengva jas keisti keičiantis verslo struktūrai. Ataskaitos yra kuriamos iš įvairių komponentų, arba kūrimo blokų. Vienas iš šių kūrimo blokų yra ataskaitų medžio aprašas. Ataskaitų kūrimo aprašas padeda nustatyti organizacijos struktūrą ir hierarchiją. Kelių dimensijų hierarchijų struktūra pagrįsta finansinių duomenų dimensijų ryšiais. Jis suteikia informacijos ataskaitinių vienetų lygiu ir suvestinės lygiu visiems medžio vienetams. Ataskaitų medžio aprašus galima derinti su stulpelių aprašais ir ataskaitos aprašais, taip sukuriant kūrimo blokų grupę, kurią gali naudoti kelios įmonės. Ataskaitinis vienetas naudojamas kiekviename langelyje organizacijos diagramoje. Ataskaitinis vienetas gali būti atskiras skyrius iš finansinių duomenų arba aukštesnio lygio suvestinės vienetas, kurį sudaro informacija iš kitų ataskaitinių vienetų. Ataskaitos apraše, kuriame yra ataskaitų medis, sukuriama kiekvieno ataskaitinio vieneto ir suvestinės lygio ataskaita. Visose šiose ataskaitose naudojami eilučių ir stulpelių aprašai, nustatyti ataskaitos apraše, nebent ataskaitos apraše nurodyta naudoti ataskaitos medį iš eilutės aprašo. Eilučių ir stulpelių aprašai yra svarbūs finansinių ataskaitų dizaino ir funkcijų komponentai. Ataskaitų medžiai padidina komponentų galimybes ir palaiko lanksčias ataskaitas keičiantis verslo struktūrai. Finansinės ataskaitos, kurios nėra pagrįstos ataskaitų medžiu, naudoja tik kai kurias finansinių ataskaitų galimybes. Norėdami peržiūrėti savo organizacijos duomenis įvairiais būdais, galite kartu naudoti kelis ataskaitų medžio aprašus, kurių eilutės ir stulpelio aprašai sutampa.

## <a name="reporting-tree-best-practices"></a>Geriausia praktika naudojant ataskaitų medį
Prieš kurdami ataskaitų medį, pasidomėkite geriausia praktika.

-   Pirmiausia nustatykite, kurių ataskaitų dimensijų reikia jūsų juridiniam subjektui arba įmonei.
-   Apsvarstykite, kaip nustatėte savo struktūrą, o tada sudarykite savo įmonės organizacijos struktūros diagramą. Organizacijos struktūros diagrama padės įsivaizduoti, kaip ataskaitinius vienetus sugrupuoti į vieną ar daugiau ataskaitų medžių.
-   Pradėkite nuo žemiausio galimo išsamumo lygio, pavyzdžiui, skyrių ir projektų, kurie yra apibrėžti finansiniuose duomenyse. Pridėkite prie išsamumo lygio tiek langelių, kiek reikia, norėdami parodyti aukštesnio lygio padalinius ar regionus. Kiekviename sukurtame ataskaitų medyje kiekvienas langelis reiškia galimą ataskaitinį vienetą.
-   Taip pat turite apsvarstyti, kokiu būdu geriausia kurti medžius. Galite naudoti automatinio kūrimo procesą ataskaitų medžiui generuoti arba galite patys kurti ataskaitų medį. Prieš kuriant medžius svarbu suprasti abu būdus.
-   Galite naudoti ataskaitinius vienetus, kurie yra apibrėžti jūsų finansinių duomenų sistemoje, norėdami pridėti ataskaitinius vienetus prie ataskaitų medžio aprašo.

## <a name="create-multiple-reporting-trees"></a> Kelių ataskaitų medžių kūrimas
Galite sukurti neribotą skaičių ataskaitų medžių, kad galėtumėte peržiūrėti organizacijos duomenis įvairiais būdais. Kiekvieną ataskaitų medį gali sudaryti bet koks skyrių ir suvestinės vienetų derinys. Ataskaitos apraše vienu metu gali būti saitas tik su vienu ataskaitų medžiu. Pertvarkydami ataskaitinių vienetų struktūrą galite sukurti įvairių ataskaitų medžių. Tada galite naudoti tą patį eilučių ir stulpelių aprašą su kiekvienu ataskaitų medžiu. Tokiu būdu galite greitai kurti įvairius finansinių ataskaitų maketus. Sukūrę kelis ataskaitų medžius, kiekvieną mėnesį galėsite spausdinti finansinių ataskaitų sekas, kuriose įvairiais būdais analizuojamos ir pateikiamos jūsų įmonės operacijos. Norėdami daugiau informacijos žr. ataskaitinių vienetų struktūros pavyzdžius šio straipsnio pabaigoje.

## <a name="create-a-reporting-tree-definition"></a> Ataskaitų medžio aprašo kūrimas
Ataskaitų medžio apraše yra šioje lentelėje aprašytų stulpelių.

| Ataskaitų medžio stulpelis | aprašymas|
|---|---|
| Įmonė               | Ataskaitinio vieneto įmonės pavadinimas. Reikšmė **@ANY**, kuri paprastai priskiriama tik suvestinės lygiui, leidžia ataskaitų medį naudoti visoms įmonėms. Visi antriniai filialai turi jiems priskirtas įmonės.|
| Vieneto pavadinimas             | Kodas, nurodantis šį ataskaitinį vienetą grafiniame ataskaitų medyje. Būtinai sukurkite unikalią kodavimo sistemą, kuri būtų nuosekli ir lengvai suprantama vartotojams. |
| Vieneto aprašas      | Ataskaitos aprašo skirtuke **Antraštės ir poraštės** įvedus kodą **UnitDesc**, ataskaitos antraštėje arba poraštėje bus rodomas ataskaitinio vieneto pavadinimas. Įvedus **UnitDesc** eilutės apibrėžimo langelyje **Aprašas**, pavadinimas bus rodomas ataskaitos eilutės apraše.|
| Dimensijos            | Ataskaitinis vienetas, kurio informacija imama tiesiai iš finansinių duomenų. Jis nustato sąskaitos ir susijusių segmentų loginį išdėstymą ir ilgį. Šiame stulpelyje kiekviena ataskaitinio vieneto eilutė turi turėti dimensiją. Taip pat galite padėti dimensiją ataskaitinio vieneto eilutėje (pavyzdžiui, išlaidų, tiesiogiai susijusių su tuo vienetu). Įvedus dimensiją suvestinio vieneto eilutėje, sąskaitų, naudojamų pirminiuose vienetuose, negalima naudoti antriniuose vienetuose. Priešingu atveju sumos gali dubliuotis.|
| Eilučių aprašai       | Ataskaitinio vieneto eilutės aprašo pavadinimas. Tas pats eilutės apibrėžimas naudojamas kiekvienam ataskaitų medžio vienetui. Kuriant ataskaitą, šis eilutės aprašas naudojamas kiekvienam ataskaitiniam vienetui. Eilutės apraše gali būti keletas finansinių dimensijų saitų. Jei ataskaitų medyje nurodytas eilutės aprašas, ataskaitos aprašo skirtuke **Ataskaita** pažymėkite žymės langelį **Naudoti eilutės aprašą iš ataskaitų medžio**.|
| Eilutės saitas              | Eilutės saitas, skirtas naudoti ataskaitiniam vienetui. Apibrėžiami eilutės aprašo eilutės saitai, nurodantys finansines dimensijas, su kuriomis reikia susieti.|
| Išorinis saitas         | Eilutės saitas, skirtas naudoti šiam ataskaitiniam vienetui. Apibrėžiami eilutės aprašo eilutės saitai, nurodantys ataskaitą, su kuria reikia susieti.|
| Išorinis failas         | Finansinių ataskaitų darbalapio failo kelias, iš kurio reikia nuskaityti duomenis.|
| Puslapio parinktys          | Šis stulpelis valdo tai, ar ataskaitinio vieneto išsamią informaciją bus draudžiama peržiūrint arba spausdinant ataskaitą.|
| Apibendrinamoji reikšmė, %              | Ataskaitinio vieneto procentinė dalis, kuri bus paskirstyta pirminiams vienetams. Procentinė dalis, kurią įvedate šiame stulpelyje, taikoma kiekvienai eilutės aprašo eilutei prieš pridedant eilutėje esančią reikšmę prie pirminės ataskaitos. Pavyzdžiui, jei antrinį vienetą reikia padalyti po lygiai dviem skyriams, kiekvienoje eilutėje esančios sumos būtų dauginamos iš 50 procentų prieš reikšmę įtraukiant į skyriaus ataskaitą. Vienas ataskaitinis vienetas negali turėti dviejų pirminių vienetų. Norėdami paskirstyti sumas iš ataskaitinio vieneto dviem pirminiams vienetams, sukurkite kitą ataskaitinį vienetą su ta pačia dimensija, kad būtų įtraukti papildomi 50 procentų. Įveskite visas procentines dalis be dešimtainio skyriklio. Pvz., **25** nurodo, kad 25 procentai paskiriami pirminiam vienetui. Jei įtrauksite dešimtainį skyriklį (**,25**), 0,25 proc. bus paskiriami pirminiam vienetui. Norėdami naudoti procentinę dalį, mažesnę nei 1 procentas, ataskaitos apraše naudokite parinktį **Leisti apibendrinamąją reikšmę &lt; 1 %**. Ši parinktis yra dialogo lango **Ataskaitos parametrai** skirtuke **Papildomos parinktys**. Šis dialogo langas pasiekiamas naudojant ataskaitos aprašo skirtuko **Parametrai** mygtuką **Kita**. |
| Vieneto sauga         | Apribojimai vartotojams ir grupėms pasiekti ataskaitinio vieneto informaciją.|
| Papildomas tekstas       | Tekstas, įtraukiamas į ataskaitą.|

Norėdami sukurti ataskaitų medžio aprašą, atlikite tokius veiksmus.

1.  Atidarykite ataskaitos dizaino įrankį.
2.  Spustelėkite **Failas** &gt; **Naujas** &gt; **Ataskaitų medžio aprašas**.
3.  Spustelėkite **Redaguoti** &gt; **Įterpti ataskaitinių vienetų iš dimensijų**.
4.  Dialogo lange **Įterpti ataskaitinių vienetų iš dimensijų** pažymėkite kiekvienos dimensijos, kurią norite įtraukti į ataskaitų medį, žymės langelį. Dialogo lange **Įterpti ataskaitinių vienetų iš dimensijų** yra toliau nurodyti skyriai.

    | Skyrius                          | Prekės/Paslaugos pavadinimas                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
    |----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Ataskaitų dimensijų segmentavimas | Segmentų skaičių ir ilgį keiskite naudodami mygtukus **Skaidyti segmentus** ir **Jungti segmentus**. **Pastaba.** Galite sujungti tik tuos segmentus, kuriuos suskaidėte. Norėdami jungti kelias dimensijas, dimensijų reikšmėse naudokite pakaitos simbolius.                                                                                                                                                                                                          |
    | Įtraukti / simbolio padėtis       | Šioje dalyje išvardintos dimensijos, apibrėžtos finansiniuose duomenyse, ir rodomas simbolių, sudarančių ilgiausią apibrėžtą kiekvienos dimensijos reikšmę, skaičius. Pažymėkite dimensijos žymės langelį, jei norite įtraukti tą dimensiją į ataskaitų medžio hierarchiją.                                                                                                                                                                                           |
    | Segmentų hierarchija ir diapazonai     | Šioje dalyje pateikiama dimensijų hierarchija. Dimensijas galima perkelti sąraše norint pakeisti jų ataskaitų tvarką. Nurodykite kiekvienos dimensijos reikšmių diapazoną laukuose **Nuo dimensijos** ir **Iki dimensijos**. Jei nenurodysite diapazono, į ataskaitų medį bus įterptos visos dimensijų reikšmės. **Pastaba.** Jei naudojate daugiau nei vieną dimensiją, rezultatuose gali būti grąžintos tik dimensijų kombinacijos, kurios buvo užregistruotos. |

    Norėdami peržiūrėti dialogo lango **Įterpti ataskaitinių vienetų iš dimensijų** pavyzdžio ekrano kopiją, žr. tolesnį šio straipsnio skyrių „Dialogo lango Įterpti ataskaitinių vienetų iš dimensijų pavyzdys“.
5.  Norėdami sukurti papildomų segmentų (pavyzdžiui, suskaidyti vieną segmentą į du trumpesnius segmentus), spustelėkite reikiamą vietą lauke **Simbolio padėtis** ir tada spustelėkite **Skaidyti segmentus**.
6.  Norėdami sulieti du segmentus į vieną segmentą, spustelėkite abiejų segmentų langelius, kad juos sujungtumėte, ir tada spustelėkite **Jungti segmentus**.
7.  Hierarchijos apibrėžia, kaip dimensijos perduoda viena kitai informaciją ir kiekvienos dimensijos diapazoną. Norėdami keisti dimensijų hierarchiją srityje **Segmentų hierarchija ir diapazonai**, pažymėkite dimensija, kurią norite perkelti, ir tada spustelėkite **Perkelti aukštyn** arba **Perkelti žemyn**.
8.  Norėdami apibrėžti dimensijos reikšmių diapazoną, kurį norite įtraukti į naują ataskaitų medį, srityje **Segmentų hierarchija ir diapazonai** atlikite toliau nurodytus veiksmus.
    1.  Tos dimensijos lauke **Nuo dimensijos** įveskite pirmą diapazono reikšmę.
    2.  Lauke **Iki dimensijos** įveskite paskutinę reikšmę diapazone.

9.  Pakartokite 7 ir 8 veiksmus su kiekviena dimensija srityje **Segmento hierarchija ir diapazonai**.
10. Baigę apibrėžti, kaip ataskaitiniai vienetai bus įtraukiami į naują ataskaitų medį, spustelėkite **Gerai**.
11. Spustelėkite **Failas** &gt; **Įrašyti**, kad įrašytumėte ataskaitų medį. Įveskite unikalų ataskaitų medžio pavadinimą ir aprašą ir tada spustelėkite **Gerai**.

### <a name="open-an-existing-reporting-tree-definition"></a>Atidarykite esamą ataskaitų medžio aprašą

1.  Ataskaitų konstruktoriaus naršymo srityje spustelėkite **Ataskaitų medžio aprašai**.
2.  Dukart spustelėkite pavadinimą ataskaitų medžio sąraše, kad jį atidarytumėte.
3.  Norėdami peržiūrėti kūrimo blokus, susietus su ataskaitų medžiu, dešiniuoju pelės klavišu spustelėkite ataskaitų medžio aprašą ir tada pasirinkite **Susiejimai**.

### <a name="roll-up-data-in-a-reporting-tree"></a>Sumuojami duomenys ataskaitų medyje

Naudodami ataskaitų medį, galite telkti sumas iš antrinių ataskaitinių vienetų pirminių ataskaitinių vienetų lygiu. Šis telkimas vadinamas duomenų sumavimu. Galite įtraukti sumas į pirminius vienetus ataskaitų medyje vadovaudamiesi šiomis taisyklėmis.

-   Ataskaitų medyje antriniai vienetai turi turėti dimensijų, nebent tai vieno lygio ataskaitų medis. Pirminiai vienetai ataskaitų medyje paprastai neturi dimensijų. **Pastaba.** Apibrėžus antrinių ir pirminių vienetų dimensijas, ataskaitoje gali atsirasti besidubliuojančių duomenų.
-   Ataskaitų vienetai, kurie ataskaitų medyje turi dimensijų, atitinka dimensijas, naudojamas eilučių ir stulpelių aprašuose. Dimensijų derinys nustato to vieneto grąžinamas sumas. Pavyzdžiui, vėlesniame šio straipsnio 2 pavyzdyje 6 ir 7 eilutės grąžins tik atitinkamai padalinių 00 ir 01 reikšmes.
-   Pirminių ataskaitinių vienetų, kurie neturi dimensijų ataskaitų medyje, sumos nustatomos iš antrinio vieneto ataskaitos ir sumuojamos į nurodyto pirminio vieneto sumą. Pavyzdžiui, jei pirminis vienetas (žr. „Contoso USA“ 2 duomenų sumavimo pavyzdyje) turi du antrinius vienetus (022 ir 023) ir neturi dimensijų, sugeneruojama kiekvieno antrinio ir pirminio vieneto ataskaita. Pirminio vieneto bendroji suma yra dviejų antrinių vienetų sumų suma.

### <a name="manage-reporting-units"></a>Ataskaitinių vienetų valdymas

Kiekvieno ataskaitų medžio aprašo rodinys unikalus. Yra grafinis vaizdas, skirtas pirminio ir antrinio vienetų hierarchijai vizualizuoti, ir darbalapio rodinys, kuriame rodoma konkreti kiekvieno ataskaitinio vieneto informacija. Grafinis vaizdas ir darbalapio rodinys yra susiję. Viename rodinyje pasirinkus ataskaitinį vienetą, jis taip pat pasirinkamas kitame rodinyje. Galite kurti kelių dimensijų hierarchijas pagal finansinių duomenų dimensijų ryšius. Kurdami ataskaitų medžio aprašą, galite naudoti tuos pačius eilučių aprašus kelis kartus tiek generuodami padalinio pajamų išrašą, tiek konsoliduotą suvestinės pajamų išrašą. Dimensijas, apibrėžtas eilutės apraše, galima derinti su dimensijomis ataskaitų medžio apraše, kad būtų pateikta įvairių jūsų organizacijos efektyvumo rodinių.

### <a name="reporting-unit-structure"></a> Ataskaitinio vieneto struktūra

Finansinėse ataskaitose naudojami toliau nurodytų tipų ataskaitiniai vienetai.

-   Informacijos vienetas ima informaciją tiesiogiai iš finansinių duomenų, iš „Excel“ darbalapio arba kito finansinių ataskaitų darbalapio.
-   Suvestinės vienetas apibendrina duomenis iš žemesnio lygio vienetų.

Pirminis ataskaitinis vienetas yra suvestinės vienetas, kuris sujungia apibendrintą informacijos vieneto informaciją. Suvestinės vienetas gali būti tiek informacijos vienetas, tiek suvestinės vienetas. Todėl suvestinės vienetas gali imti informaciją iš žemesnio lygio vieneto, finansinių duomenų arba „Excel“ darbalapio. Pirminis vienetas gali būti antrinis aukštesnio lygio pirminio vieneto vienetas. Antrinis ataskaitinis vienetas gali būti informacijos vienetas, gaunantis informaciją tiesiogiai iš finansinių duomenų arba „Excel“ darbalapio. Antrinis ataskaitinis vienetas taip pat gali būti tarpinis suvestinės vienetas. Kitaip tariant, jis gali būti žemesnio lygio vieneto pirminis vienetas ir aukštesnio lygio suvestinės vieneto antrinis vienetas. Dažniausiai ataskaitiniai vienetai turi pirminius vienetus su tuščiu langeliu stulpelyje **Dimensijos** ir antrinius vienetus su saitais į konkrečius arba pakaitos dimensijų derinius.

### <a name="organize-reporting-units"></a> Ataskaitinių vienetų tvarkymas

Ataskaitų medžio aprašo organizacinę struktūrą galite pertvarkyti perkeldami ataskaitinius vienetus grafiniame rodinyje. Taip pat galite perkelti ataskaitinius vienetus į aukštesnį arba žemesnį ataskaitų medžio lygį.

1.  Ataskaitų konstruktoriuje atidarykite ataskaitų medžio aprašą, kurį norite modifikuoti.
2.  Grafiniame ataskaitų medžio aprašo rodinyje pasirinkite ataskaitinį vienetą.
3.  Nuvilkite vienetą į naują vietą. Arba spustelėkite vienetą dešiniuoju pelės klavišu ir tada pasirinkite **Perkelti ataskaitinį vienetą į aukštesnį lygį** arba **Perkelti ataskaitinį vienetą žemesnį lygį**.
4.  Norėdami įrašyti pakeitimus, spustelėkite **Failas** &gt; **Įrašyti**.

### <a name="add-text-about-a-reporting-unit"></a> Pridėti tekstą apie ataskaitinį vienetą

Papildomas teksto įrašas yra statinė teksto eilutė, kurią sudaro iki 255 simbolių, įtraukianti į ataskaitų medžio aprašą informacijos. Pvz., papildomas tekstas gali būti trumpas įmonės aprašymas. Galite sukurti iki dešimties kiekvieno ataskaitinio vieneto, esančio ataskaitų medyje, papildomų teksto įrašų. Ataskaitinio vieneto, kuriam priskiriamas tekstas, ataskaitoje rodomas papildomas tekstas. Galite pridėti teksto įrašų iš eilutės aprašo stulpelio **Aprašas** ir iš ataskaitos aprašo skirtuko **Antraštės ir poraštės**.

1.  Ataskaitų konstruktoriuje atidarykite ataskaitų medžio aprašą, kurį norite modifikuoti.
2.  Dukart spustelėkite papildomą ataskaitinio vieneto eilutės langelį **Papildomas tekstas**.
3.  Pirmojoje dialogo lango **Papildomas tekstas** tuščioje eilutėje įveskite tekstą. Pirmoji eilutė, kurioje yra teksto nurodome kaip UnitText1, neatsižvelgiant į jos padėtį dialogo lange **Papildomas tekstas**.
4.  Norėdami prie ataskaitinio vieneto pridėti daugiau teksto įrašų, įveskite tekstą tuščioje eilutėje.
5.  Spustelėkite **GERAI**.

### <a name="remove-additional-text-from-a-reporting-unit"></a>Papildomo teksto pašalinimas iš ataskaitinio vieneto

1.  Ataskaitų konstruktoriuje atidarykite ataskaitų medžio aprašą, kurį norite modifikuoti.
2.  Dukart spustelėkite papildomą ataskaitinio vieneto eilutės langelį **Papildomas tekstas**.
3.  Dialogo lange **Papildomas tekstas** pažymėkite įrašą, kurį norite pašalinti, tada spustelėkite **Valyti** Arba įrašą spustelėkite dešiniuoju pelės klavišu ir pasirinkite **Iškirpti**.
4.  Spustelėkite **GERAI**.

### <a name="restrict-access-to-a-reporting-unit"></a>Prieigos prie ataskaitinio vieneto apribojimas

Galite neleisti tam tikriems vartotojams ir grupėms pasiekti ataskaitinį vienetą. Taip pat gali nustatyti apribojimus, kad jie būtų taikomi ataskaitinio vieneto antriniams ataskaitiniams vienetams.

1.  Ataskaitų konstruktoriuje atidarykite ataskaitų medžio aprašą, kurį norite modifikuoti.
2.  Dukart spustelėkite ataskaitinio vieneto eilutės, prieigą prie kurios norite apriboti, langelį **Vieneto sauga**.
3.  Dialogo lange **Vieneto sauga** spustelėkite **Vartotojai ir grupės**.
4.  Pasirinkite vartotojus arba grupes, kurios turės prieigą prie ataskaitinio vieneto, ir tada spustelėkite **Gerai**.
5.  Norėdami apriboti prieigą prie antrinių ataskaitinių vienetų, pažymėkite žymės langelį **Apsaugoti ataskaitinius vienetus**.
6.  Spustelėkite **GERAI**.

### <a name="remove-access-to-a-reporting-unit"></a>Prieigos prie ataskaitinio vieneto pašalinimas

1.  Ataskaitų konstruktoriuje atidarykite ataskaitų medžio aprašą, kurį norite modifikuoti.
2.  Dukart spustelėkite ataskaitinio vieneto eilutės, prieigą prie kurios norite pašalinti, langelį **Vieneto sauga**.
3.  Dialogo lange **Vieneto sauga** pasirinkite pavadinimą, tada spustelėkite **Pašalinti**.
4.  Spustelėkite **GERAI**.

### <a name="link-to-reports"></a>Saitas į ataskaitas

Eilutės apraše sukūrę **ataskaitos** stulpelį ir nurodę ataskaitą, kurią norite įtraukti į ataskaitą, turite atnaujinti ataskaitų medį pridėdami susietą stulpelį ir ataskaitos informaciją. Ataskaitą galima importuoti į bet kurį ataskaitinio medžio vienetą.

### <a name="identify-the-report-in-a-reporting-tree"></a>Ataskaitos nustatymas ataskaitų medyje

1.  Ataskaitų konstruktoriuje atidarykite ataskaitų medžio aprašą, kurį norite modifikuoti.
2.  Stulpelio **Eilučių aprašai** langeliuose rodoma informacija pagal pasirinktos eilutės informaciją, nes visuose ataskaitų medžio vienetuose reikia naudoti tą patį eilutės aprašą. Dukart spustelėkite langelį **Eilučių aprašai**, tada pasirinkite eilutės aprašą, kuriame yra informacijos apie ataskaitą.
3.  Ataskaitinio vieneto langelyje **Darbalapio saitas** pasirinkite saito pavadinimą, kuris atitinka ataskaitą.
4.  Ataskaitinio vieneto langelyje **Darbaknygės arba ataskaitos kelias** įveskite ataskaitos pavadinimą arba naršykite, kad pasirinktumėte ataskaitą.
5.  Norėdami nurodyti darbalapį ataskaitoje, įveskite darbalapio pavadinimą langelyje **Darbalapio pavadinimas**.
6.  Pakartokite 3–5 veiksmus su kiekvienu ataskaitiniu vienetu, kuris turėtų gauti duomenis iš ataskaitos. Siekdami, kad neteisingi duomenys nebūtų įtraukti į ataskaitą, įsitikinkite, kad atitinkamame ataskaitų medžio vienete rodomi teisingi ataskaitų pavadinimai.

## <a name="examples"></a>Pavyzdžiai
### <a name="reporting-unit-structure--example-1"></a>Ataskaitinio vieneto struktūra – 1 pavyzdys

Toliau pateikiama ataskaitinių vienetų struktūra šiame ataskaitų medyje.

-   Ataskaitinis vienetas „Contoso Japan“ yra pirminis antrinių vienetų „Contoso Japan Sales“ ir „Contoso Japan Consulting“ vienetas.
-   Padalinio vienetas „Contoso Japan Sales“ kartu yra antrinis „Contoso Japan“ vienetas ir pirminis vienetų Pardavimas vidaus rinkoje ir Automatinis pardavimas vienetas.
-   Žemiausio lygio informacijos ataskaitiniai vienetai (Pardavimas vidaus rinkoje, Automatinis pardavimas, Klientų paslaugos ir Operacijos) atitinka finansinių duomenų skyrius. Šie ataskaitiniai vienetai yra šešėliuotoje diagramos srityje.
-   Aukštesnio lygio suvestinės vienetai apibendrina informaciją iš informacijos vienetų.

[![ContosoEntertainmentSummaryReportStructure](./media/contosoentertainmentsummaryreportstructure.png)](./media/contosoentertainmentsummaryreportstructure.png)

### <a name="reporting-unit-structure--example-2"></a>Ataskaitinio vieneto struktūra – 2 pavyzdys

Šioje diagramoje pateikiamas ataskaitų medis, kuriame parodyta organizacinė struktūra, suskirstyta pagal verslo funkcijas. [![summaryofallunitscontoso](./media/summaryofallunitscontoso.png)](./media/summaryofallunitscontoso.png)

### <a name="example-of-the-insert-reporting-units-from-dimensions-dialog-box"></a>Dialogo lango Įterpti ataskaitinių vienetų iš dimensijų pavyzdys

Tolesnėje iliustracijoje pateikiamas dialogo lango **Įterpti ataskaitinių vienetų iš dimensijų** pavyzdys. Šiame pavyzdyje rezultatai pateiks verslo struktūros vienetų, išlaidų centrų ir padalinių derinį. [![InsertReportingUnits](./media/insertreportingunits.png)](./media/insertreportingunits.png) Gautas ataskaitų medžio aprašas surūšiuotas pagal verslo vienetą, tada – pagal išlaidų centrą, o tada – pagal padalinį. Penktojo ataskaitinio vieneto dimensija yra **Verslo struktūros vienetas = \[001\], Išlaidų centras =\[\], Padalinys = \[022\]** ir ji nurodo nustatytų 001 verslo struktūros vieneto ir 022 padalinio sąskaitų ataskaitinį vienetą. [![ReportingTree](./media/reportingtree-1024x646.png)](./media/reportingtree.png)

### <a name="examples-of-data-roll-up"></a>Duomenų sumavimo pavyzdžiai

Šiuose pavyzdžiuose parodyta galima informacija, naudojama ataskaitų medžio apraše, kaip duomenų sumavimo pavyzdys.

#### <a name="example-1"></a>1 pavyzdys

[![MutliCompanyRollUp](./media/mutlicompanyrollup.png)](./media/mutlicompanyrollup.png)

#### <a name="example-2"></a>2 pavyzdys

[![CrossCompanyDepartmentRollUp](./media/crosscompanydepartmentrollup.png)](./media/crosscompanydepartmentrollup.png)

# <a name="see-also"></a>Taip pat žiūrėkite

[Finansinės ataskaitos](financial-reporting-intro.md)




