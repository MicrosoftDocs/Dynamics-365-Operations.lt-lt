---
title: Ataskaitų dizaino įrankio ataskaitų medžio apibrėžtys
description: Šiame straipsnyje aprašomi ataskaitų medžio apibrėžimai. Ataskaitų medžio apibrėžimas yra ataskaitos komponentas, apibūdinantis organizacijos struktūrą.
author: jinniew
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 57592
ms.assetid: 747faa47-9a23-4277-bc11-8d0a1267c3a4
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: cf5062cfc7ce47a2356c72462da805e8d0d6a756
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727796"
---
# <a name="reporting-tree-definitions-in-financial-reports"></a>Ataskaitų dizaino įrankio ataskaitų medžio apibrėžtys

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija ataskaitų medžių aprašus. Ataskaitų medžio aprašas yra ataskaitos komponentas, arba kūrimo blokas, kuris padeda nustatyti organizacijos struktūrą ir hierarchiją.

„Financial Reporting” palaiko lanksčias ataskaitas, todėl lengva jas keisti keičiantis verslo struktūrai. Ataskaitos yra kuriamos iš įvairių komponentų, arba kūrimo blokų. Vienas iš šių kūrimo blokų yra ataskaitų medžio aprašas. Ataskaitų kūrimo aprašas padeda nustatyti organizacijos struktūrą ir hierarchiją. Kelių dimensijų hierarchijų struktūra pagrįsta finansinių duomenų dimensijų ryšiais. Jis suteikia informacijos ataskaitinių vienetų lygiu ir suvestinės lygiu visiems medžio vienetams. Ataskaitų medžio aprašus galima derinti su stulpelių aprašais ir ataskaitos aprašais, taip sukuriant kūrimo blokų grupę, kurią gali naudoti kelios įmonės. Ataskaitinis vienetas naudojamas kiekviename langelyje organizacijos diagramoje. Ataskaitiniu vienetu gali būti atskiras skyrius iš finansinių duomenų arba aukštesnio lygio suvestinės vienetas, pateikiantis kitų ataskaitinių vienetų informaciją. Ataskaitos apraše, kuriame yra ataskaitų medis, sukuriama kiekvieno ataskaitinio vieneto ir suvestinės lygio ataskaita. Visose šiose ataskaitose naudojami eilučių ir stulpelių aprašai, nustatyti ataskaitos apraše, nebent ataskaitos apraše nurodyta naudoti ataskaitos medį iš eilutės aprašo. Eilučių ir stulpelių aprašai yra svarbūs finansinių ataskaitų dizaino ir funkcijų komponentai. Ataskaitų medžiai padidina komponentų galimybes ir palaiko lanksčias ataskaitas keičiantis verslo struktūrai. Finansinės ataskaitos, kurios nėra pagrįstos ataskaitų medžiu, naudoja tik kai kurias finansinių ataskaitų galimybes. Norėdami peržiūrėti savo organizacijos duomenis įvairiais būdais, galite kartu naudoti kelis ataskaitų medžio aprašus, kurių eilutės ir stulpelio aprašai sutampa.

## <a name="reporting-tree-best-practices"></a>Geriausia praktika naudojant ataskaitų medį
Prieš kurdami ataskaitų medį, pasidomėkite geriausia praktika.

- Pirmiausia nustatykite, kurių ataskaitų dimensijų reikia jūsų juridiniam subjektui arba įmonei.
- Apsvarstykite, kaip nustatėte savo struktūrą, o tada sudarykite savo įmonės organizacijos struktūros diagramą. Organizacijos struktūros diagrama padės įsivaizduoti, kaip grupuoti ataskaitinius vienetus į vieną ar kelis ataskaitų medžius.
- Pradėkite nuo žemiausio galimo išsamumo lygio, pavyzdžiui, skyrių ir projektų, kurie yra apibrėžti finansiniuose duomenyse. Pridėkite prie išsamumo lygio tiek langelių, kiek reikia, norėdami parodyti aukštesnio lygio padalinius ar regionus. Kiekviename sukurtame ataskaitų medyje kiekvienas langelis reiškia galimą ataskaitinį vienetą.
- Taip pat turite apsvarstyti, kokiu būdu geriausia kurti medžius. Galite naudoti automatinio kūrimo procesą ataskaitų medžiui generuoti arba galite patys kurti ataskaitų medį. Prieš kuriant medžius svarbu suprasti abu būdus.
- Galite naudoti ataskaitinius vienetus, kurie yra apibrėžti jūsų finansinių duomenų sistemoje, norėdami pridėti ataskaitinius vienetus prie ataskaitų medžio aprašo.

## <a name="create-multiple-reporting-trees"></a>Kelių ataskaitų medžių kūrimas
Galite sukurti neribotą skaičių ataskaitų medžių, kad galėtumėte peržiūrėti organizacijos duomenis įvairiais būdais. Ataskaitų medį gali sudaryti bet koks padalinių ir suvestinės vienetų derinys. Ataskaitos apraše vienu metu gali būti saitas tik su vienu ataskaitų medžiu. Pertvarkydami ataskaitinių vienetų struktūrą galite sukurti įvairių ataskaitų medžių. Tada galite naudoti tą patį eilučių ir stulpelių aprašą su kiekvienu ataskaitų medžiu. Tokiu būdu galite greitai kurti įvairius finansinių ataskaitų maketus. Sukūrę kelis ataskaitų medžius, kiekvieną mėnesį galėsite spausdinti finansinių ataskaitų sekas, kuriose įvairiais būdais analizuojamos ir pateikiamos jūsų įmonės operacijos. Norėdami daugiau informacijos žr. ataskaitinių vienetų struktūros pavyzdžius šio straipsnio pabaigoje.

## <a name="create-a-reporting-tree-definition"></a>Ataskaitų medžio aprašo kūrimas
Ataskaitų medžio apraše yra šioje lentelėje aprašytų stulpelių.

| Ataskaitų medžio stulpelis | Aprašymas |
|-----------------------|-------------|
| Įmonė               | Ataskaitinio vieneto įmonės pavadinimas. **\@ANY** vertė, paprastai priskiriama tik suvestinės lygiu, teikia galimybę naudoti ataskaitų medį visoms įmonėms. Visoms antrinėms šakoms priskiriama įmonė. |
| Vieneto pavadinimas             | Kodas, nurodantis šį ataskaitinį vienetą grafiniame ataskaitų medyje. Būtinai sukurkite unikalią kodavimo sistemą, kuri būtų nuosekli ir lengvai suprantama vartotojams. |
| Vieneto aprašas      | Ataskaitos aprašo skirtuke **Antraštės ir poraštės** įvedus kodą **UnitDesc**, ataskaitos antraštėje arba poraštėje bus rodomas ataskaitinio vieneto pavadinimas. Įvedus **UnitDesc** eilutės apibrėžimo langelyje **Aprašas**, pavadinimas bus rodomas ataskaitos eilutės apraše. |
| Dimensijos            | Ataskaitinis vienetas, kurio informacija imama tiesiai iš finansinių duomenų. Jis nustato sąskaitos ir susijusių segmentų loginį išdėstymą ir ilgį. Šiame stulpelyje kiekviena ataskaitinio vieneto eilutė turi turėti dimensiją. Taip pat galite padėti dimensiją ataskaitinio vieneto eilutėje (pavyzdžiui, išlaidų, tiesiogiai susijusių su tuo vienetu). Įvedus dimensiją suvestinio vieneto eilutėje, sąskaitų, naudojamų pirminiuose vienetuose, negalima naudoti antriniuose vienetuose. Priešingu atveju sumos gali dubliuotis. |
| Eilučių aprašai       | Ataskaitinio vieneto eilutės aprašo pavadinimas. Visiems ataskaitų medžio vienetams naudojamas tas pats eilučių aprašas. Generuojant ataskaitą šis eilučių aprašas naudojamas visiems ataskaitiniams vienetams. Eilučių aprašas gali apimti kelių finansinių dimensijų saitus. Jeigu eilučių aprašas nurodytas ataskaitų medyje, pažymėkite ataskaitos aprašo skirtuko **Ataskaita** žymės langelį **Naudoti eilučių aprašą iš ataskaitų medžio**. |
| Finansinių dimensijų saitas| Finansinių dimensijų saitas, skirtas ataskaitų vieneto naudojimui. Finansinių dimensijų saitai apibrėžiami eilučių aprašui, kad būtų galima identifikuoti finansines dimensijas, su kuriomis galima susieti informaciją. |
| Puslapio parinktys          | Šis stulpelis valdo tai, ar ataskaitinio vieneto išsamią informaciją bus draudžiama peržiūrint arba spausdinant ataskaitą. |
| Apibendrinamoji reikšmė, %              | Ataskaitinio vieneto procentinė dalis, kuri bus paskirstyta pirminiams vienetams. Procentinė dalis, kurią įvedate šiame stulpelyje, taikoma kiekvienai eilutės aprašo eilutei prieš pridedant eilutėje esančią reikšmę prie pirminės ataskaitos. Pavyzdžiui, jei antrinį vienetą reikia padalyti po lygiai dviem skyriams, kiekvienoje eilutėje esančios sumos būtų dauginamos iš 50 procentų prieš reikšmę įtraukiant į skyriaus ataskaitą. Vienas ataskaitinis vienetas negali turėti dviejų pirminių vienetų. Norėdami paskirstyti sumas iš ataskaitinio vieneto dviem pirminiams vienetams, sukurkite kitą ataskaitinį vienetą su ta pačia dimensija, kad būtų įtraukti papildomi 50 procentų. Įveskite visas procentines dalis be dešimtainio skyriklio. Pvz., **25** nurodo, kad 25 procentai paskiriami pirminiam vienetui. Jei įtrauksite dešimtainį skyriklį (**,25**), 0,25 proc. bus paskiriami pirminiam vienetui. Norėdami naudoti procentinę dalį, mažesnę nei 1 procentas, ataskaitos apraše naudokite parinktį **Leisti apibendrinamąją reikšmę &lt; 1 %**. Ši parinktis yra dialogo lango **Ataskaitos parametrai** skirtuke **Papildomos parinktys**. Šis dialogo langas pasiekiamas naudojant ataskaitos aprašo skirtuko **Parametrai** mygtuką **Kita**. |
| Vieneto sauga         | Apribojimai vartotojams ir grupėms pasiekti ataskaitinio vieneto informaciją. |
| Papildomas tekstas       | Tekstas, įtraukiamas į ataskaitą. |

Norėdami sukurti ataskaitų medžio aprašą, atlikite tokius veiksmus.

1. Atidarykite ataskaitos dizaino įrankį.
2. Spustelėkite **Failas** &gt; **Naujas** &gt; **Ataskaitų medžio aprašas**.
3. Spustelėkite **Redaguoti** &gt; **Įterpti ataskaitinių vienetų iš dimensijų**.
4. Dialogo lange **Įterpti ataskaitinių vienetų iš dimensijų** pažymėkite kiekvienos dimensijos, kurią norite įtraukti į ataskaitų medį, žymės langelį. Dialogo lange **Įterpti ataskaitinių vienetų iš dimensijų** yra toliau nurodyti skyriai.

    | Skyrius                          | Prekės/Paslaugos pavadinimas |
    |----------------------------------|-------------|
    | Ataskaitų dimensijų segmentavimas | Naudodami mygtukus **Skaidyti segmentus** ir **Sujungti segmentus** galite keisti segmentų skaičių ir ilgį.<blockquote>[!NOTE] Galite sujungti tik išskaidytus segmentus. Norėdami jungti kelias dimensijas, dimensijų reikšmėse naudokite pakaitos simbolius.</blockquote> |
    | Įtraukti / simbolio padėtis       | Šioje dalyje išvardintos dimensijos, apibrėžtos finansiniuose duomenyse, ir rodomas simbolių, sudarančių ilgiausią apibrėžtą kiekvienos dimensijos reikšmę, skaičius. Pažymėkite dimensijos žymės langelį, jei norite įtraukti tą dimensiją į ataskaitų medžio hierarchiją. |
    | Segmentų hierarchija ir diapazonai     | Šioje dalyje pateikiama dimensijų hierarchija. Dimensijas galima perkelti sąraše norint pakeisti jų ataskaitų tvarką. Nurodykite kiekvienos dimensijos reikšmių diapazoną laukuose **Nuo dimensijos** ir **Iki dimensijos**. Jei nenurodysite diapazono, į ataskaitų medį bus įterptos visos dimensijų reikšmės.<blockquote>[!NOTE] Jei naudojate daugiau kaip vieną dimensiją, rezultatuose bus pateikti tik dimensijų rinkiniai, kuriuose buvo paskelbta.</blockquote> |

    Norėdami peržiūrėti paveikslėlį, kuriame rodomas **Įterpti ataskaitinių vienetų iš dimensijų** pavyzdys, žr. tolesnį šio straipsnio skyrių „Dialogo lango Įterpti ataskaitinių vienetų iš dimensijų pavyzdys“.

5. Norėdami sukurti papildomų segmentų (pavyzdžiui, suskaidyti vieną segmentą į du trumpesnius segmentus), spustelėkite reikiamą vietą lauke **Simbolio padėtis** ir tada spustelėkite **Skaidyti segmentus**.
6. Norėdami sulieti du segmentus į vieną segmentą, spustelėkite abiejų segmentų langelius, kad juos sujungtumėte, ir tada spustelėkite **Jungti segmentus**.
7. Hierarchijos apibrėžia, kaip dimensijos perduoda viena kitai informaciją ir kiekvienos dimensijos diapazoną. Norėdami keisti dimensijų hierarchiją srityje **Segmentų hierarchija ir diapazonai**, pažymėkite dimensija, kurią norite perkelti, ir tada spustelėkite **Perkelti aukštyn** arba **Perkelti žemyn**.
8. Norėdami apibrėžti dimensijos reikšmių diapazoną, kurį norite įtraukti į naują ataskaitų medį, srityje **Segmentų hierarchija ir diapazonai** atlikite toliau nurodytus veiksmus.

    1. Tos dimensijos lauke **Nuo dimensijos** įveskite pirmą diapazono reikšmę.
    2. Lauke **Iki dimensijos** įveskite paskutinę reikšmę diapazone.

9. Pakartokite 7 ir 8 veiksmus su kiekviena dimensija srityje **Segmento hierarchija ir diapazonai**.
10. Baigę apibrėžti, kaip ataskaitiniai vienetai bus įtraukiami į naują ataskaitų medį, spustelėkite **Gerai**.
11. Spustelėkite **Failas** &gt; **Įrašyti**, kad įrašytumėte ataskaitų medį. Įveskite unikalų ataskaitų medžio pavadinimą ir aprašą ir tada spustelėkite **Gerai**.

### <a name="open-an-existing-reporting-tree-definition"></a>Atidarykite esamą ataskaitų medžio aprašą

1. Ataskaitų konstruktoriaus naršymo srityje spustelėkite **Ataskaitų medžio aprašai**.
2. Dukart spustelėkite pavadinimą ataskaitų medžio sąraše, kad jį atidarytumėte.
3. Norėdami peržiūrėti kūrimo blokus, susietus su ataskaitų medžiu, dešiniuoju pelės klavišu spustelėkite ataskaitų medžio aprašą ir tada pasirinkite **Susiejimai**.

### <a name="roll-up-data-in-a-reporting-tree"></a>Sumuojami duomenys ataskaitų medyje

Naudodami ataskaitų medį, galite telkti sumas iš antrinių ataskaitinių vienetų pirminių ataskaitinių vienetų lygiu. Šis telkimas vadinamas duomenų sumavimu. Galite įtraukti sumas į pirminius vienetus ataskaitų medyje vadovaudamiesi šiomis taisyklėmis.

- Ataskaitų medyje antriniai vienetai turi turėti dimensijų, nebent tai vieno lygio ataskaitų medis. Pirminiai vienetai ataskaitų medyje paprastai neturi dimensijų.

    > [!NOTE]
    > Apibrėžus antrinių ir pirminių vienetų dimensijas, ataskaitoje gali atsirasti besidubliuojančių duomenų.

- Ataskaitų vienetai, kurie ataskaitų medyje turi dimensijų, atitinka dimensijas, naudojamas eilučių ir stulpelių aprašuose. Dimensijų derinys nustato to vieneto grąžinamas sumas. Pavyzdžiui, vėlesniame šio straipsnio 2 pavyzdyje 6 ir 7 eilutės grąžins tik atitinkamai padalinių 00 ir 01 reikšmes.
- Pirminių ataskaitinių vienetų, kurie neturi dimensijų ataskaitų medyje, sumos nustatomos iš antrinio vieneto ataskaitos ir sumuojamos į nurodyto pirminio vieneto sumą. Pavyzdžiui, jei pirminis vienetas (žr. „Contoso USA“ 2 duomenų sumavimo pavyzdyje) turi du antrinius vienetus (022 ir 023) ir neturi dimensijų, sugeneruojama kiekvieno antrinio ir pirminio vieneto ataskaita. Pirminio vieneto bendroji suma yra dviejų antrinių vienetų sumų suma.

### <a name="manage-reporting-units"></a>Ataskaitinių vienetų valdymas

Kiekvieno ataskaitų medžio aprašo rodinys unikalus. Yra grafinis vaizdas, skirtas pirminio ir antrinio vienetų hierarchijai vizualizuoti, ir darbalapio rodinys, kuriame rodoma konkreti kiekvieno ataskaitinio vieneto informacija. Grafinis vaizdas ir darbalapio rodinys yra susiję. Viename rodinyje pasirinkus ataskaitinį vienetą, jis taip pat pasirinkamas kitame rodinyje. Galite kurti kelių dimensijų hierarchijas pagal finansinių duomenų dimensijų ryšius. Kurdami ataskaitų medžio aprašą, galite naudoti tuos pačius eilučių aprašus kelis kartus tiek generuodami padalinio pajamų išrašą, tiek konsoliduotą suvestinės pajamų išrašą. Dimensijas, apibrėžtas eilutės apraše, galima derinti su dimensijomis ataskaitų medžio apraše, kad būtų pateikta įvairių jūsų organizacijos efektyvumo rodinių.

### <a name="reporting-unit-structure"></a>Ataskaitinio vieneto struktūra

Finansinėse ataskaitose naudojami toliau nurodytų tipų ataskaitiniai vienetai.

- Išsamios informacijos informaciją ima tiesiai iš finansinių duomenų.
- Suvestinės vienetas apibendrina duomenis iš žemesnio lygio vienetų.

Pirminis ataskaitinis vienetas yra suvestinės vienetas, kuris sujungia apibendrintą informacijos vieneto informaciją. Suvestinės vienetas gali būti tiek informacijos vienetas, tiek suvestinės vienetas. Todėl suvestinės vienetas gali imti informaciją iš žemesnio lygio vieneto arba finansinių duomenų. Pirminis vienetas gali būti antrinis aukštesnio lygio pirminio vieneto vienetas. Antrinis ataskaitinis vienetas gali būti informacijos vienetas, gaunantis informaciją tiesiogiai iš finansinių duomenų. Antrinis ataskaitinis vienetas taip pat gali būti tarpinis suvestinės vienetas. Kitaip tariant, jis gali būti žemesnio lygio vieneto pirminis vienetas ir aukštesnio lygio suvestinės vieneto antrinis vienetas. Dažniausiai ataskaitiniai vienetai turi pirminius vienetus su tuščiu langeliu stulpelyje **Dimensijos** ir antrinius vienetus su saitais į konkrečius arba pakaitos dimensijų derinius.

### <a name="organize-reporting-units"></a>Ataskaitinių vienetų tvarkymas

Ataskaitų medžio aprašo organizacinę struktūrą galite pertvarkyti perkeldami ataskaitinius vienetus grafiniame rodinyje. Taip pat galite perkelti ataskaitinius vienetus į aukštesnį arba žemesnį ataskaitų medžio lygį.

1. Ataskaitų konstruktoriuje atidarykite ataskaitų medžio aprašą, kurį norite modifikuoti.
2. Grafiniame ataskaitų medžio aprašo rodinyje pasirinkite ataskaitinį vienetą.
3. Nuvilkite vienetą į naują vietą. Arba spustelėkite vienetą dešiniuoju pelės klavišu ir tada pasirinkite **Perkelti ataskaitinį vienetą į aukštesnį lygį** arba **Perkelti ataskaitinį vienetą žemesnį lygį**.
4. Norėdami įrašyti pakeitimus, spustelėkite **Failas** &gt; **Įrašyti**.

### <a name="add-text-about-a-reporting-unit"></a>Pridėti tekstą apie ataskaitinį vienetą

Papildomas teksto įrašas yra statinė teksto eilutė, kurią sudaro iki 255 simbolių, įtraukianti į ataskaitų medžio aprašą informacijos. Pvz., papildomas tekstas gali būti trumpas įmonės aprašymas. Galite sukurti iki dešimties kiekvieno ataskaitinio vieneto, esančio ataskaitų medyje, papildomų teksto įrašų. Ataskaitinio vieneto, kuriam priskiriamas tekstas, ataskaitoje rodomas papildomas tekstas. Galite pridėti teksto įrašų iš eilutės aprašo stulpelio **Aprašas** ir iš ataskaitos aprašo skirtuko **Antraštės ir poraštės**.

1. Ataskaitų konstruktoriuje atidarykite ataskaitų medžio aprašą, kurį norite modifikuoti.
2. Dukart spustelėkite papildomą ataskaitinio vieneto eilutės langelį **Papildomas tekstas**.
3. Pirmojoje dialogo lango **Papildomas tekstas** tuščioje eilutėje įveskite tekstą. Pirmoji eilutė, kurioje yra teksto nurodome kaip UnitText1, neatsižvelgiant į jos padėtį dialogo lange **Papildomas tekstas**.
4. Norėdami prie ataskaitinio vieneto pridėti daugiau teksto įrašų, įveskite tekstą tuščioje eilutėje.
5. Spustelėkite **GERAI**.

### <a name="remove-additional-text-from-a-reporting-unit"></a>Papildomo teksto pašalinimas iš ataskaitinio vieneto

1. Naudodami ataskaitų dizaino įrankį atidarykite norimą modifikuoti ataskaitų medžio aprašą.
2. Du kartus spustelėkite ataskaitinio vieneto eilutės langelį **Papildomas tekstas**.
3. Dialogo lange **Papildomas tekstas** pažymėkite įrašą, kurį norite pašalinti, tada spustelėkite **Valyti** Arba įrašą spustelėkite dešiniuoju pelės klavišu ir pasirinkite **Iškirpti**.
4. Spustelėkite **GERAI**.

### <a name="restrict-access-to-a-reporting-unit"></a>Prieigos prie ataskaitinio vieneto apribojimas

Galite neleisti tam tikriems vartotojams ir grupėms pasiekti ataskaitinį vienetą. Taip pat gali nustatyti apribojimus, kad jie būtų taikomi ataskaitinio vieneto antriniams ataskaitiniams vienetams.

1. Ataskaitų konstruktoriuje atidarykite ataskaitų medžio aprašą, kurį norite modifikuoti.
2. Dukart spustelėkite ataskaitinio vieneto eilutės, prie kurios norite apriboti prieigą, langelį **Vieneto sauga**.
3. Dialogo lange **Vieneto sauga** spustelėkite **Vartotojai ir grupės**.
4. Pasirinkite vartotojus arba grupes, kurios turės prieigą prie ataskaitinio vieneto, ir tada spustelėkite **Gerai**.
5. Norėdami apriboti prieigą prie antrinių ataskaitinių vienetų, pažymėkite žymės langelį **Apsaugoti ataskaitinius vienetus**.
6. Spustelėkite **GERAI**.

### <a name="remove-access-to-a-reporting-unit"></a>Prieigos prie ataskaitinio vieneto pašalinimas

1. Ataskaitų konstruktoriuje atidarykite ataskaitų medžio aprašą, kurį norite modifikuoti.
2. Dukart spustelėkite ataskaitinio vieneto eilutės, prieigą prie kurios norite pašalinti, langelį **Vieneto sauga**.
3. Dialogo lange **Vieneto sauga** pasirinkite pavadinimą, tada spustelėkite **Pašalinti**.
4. Spustelėkite **Gerai**.

## <a name="examples"></a>Pavyzdžiai
### <a name="reporting-unit-structure--example-1"></a>Ataskaitinio vieneto struktūra – 1 pavyzdys

Toliau pateikiama ataskaitinių vienetų struktūra šiame ataskaitų medyje.

- Ataskaitinis vienetas „Contoso Japan“ yra pirminis antrinių vienetų „Contoso Japan Sales“ ir „Contoso Japan Consulting“ vienetas.
- Padalinio vienetas „Contoso Japan Sales“ kartu yra antrinis „Contoso Japan“ vienetas ir pirminis vienetų Pardavimas vidaus rinkoje ir Automatinis pardavimas vienetas.
- Žemiausio lygio informacijos ataskaitiniai vienetai (Pardavimas vidaus rinkoje, Automatinis pardavimas, Klientų paslaugos ir Operacijos) atitinka finansinių duomenų skyrius. Šie ataskaitiniai vienetai yra šešėliuotoje diagramos srityje.
- Aukštesnio lygio suvestinės vienetai apibendrina informaciją iš informacijos vienetų.

[!["Contoso" suvestinės ataskaitos struktūra – 1 pavyzdys.](./media/contosoentertainmentsummaryreportstructure.png)](./media/contosoentertainmentsummaryreportstructure.png)

### <a name="reporting-unit-structure--example-2"></a>Ataskaitinio vieneto struktūra – 2 pavyzdys

Šioje diagramoje pateikiamas ataskaitų medis, kuriame parodyta organizacinė struktūra, suskirstyta pagal verslo funkcijas.

[!["Contoso" suvestinės ataskaitos struktūra – 2 pavyzdys.](./media/summaryofallunitscontoso.png)](./media/summaryofallunitscontoso.png)

### <a name="example-of-the-insert-reporting-units-from-dimensions-dialog-box"></a>Dialogo lango Įterpti ataskaitinių vienetų iš dimensijų pavyzdys

Tolesnėje iliustracijoje pateikiamas dialogo lango **Įterpti ataskaitinių vienetų iš dimensijų** pavyzdys. Šiame pavyzdyje rezultatai pateiks verslo struktūros vienetų, išlaidų centrų ir padalinių derinį.

[![Įterpti ataskaitinius vienetus.](./media/insertreportingunits.png)](./media/insertreportingunits.png)

Gautas ataskaitų medžio aprašas surūšiuotas pagal verslo vienetą, tada – pagal išlaidų centrą, o tada – pagal padalinį. Penktojo ataskaitinio vieneto dimensija yra **Verslo struktūros vienetas = \[001\], Išlaidų centras =\[\], Padalinys = \[022\]** ir ji nurodo nustatytų 001 verslo struktūros vieneto ir 022 padalinio sąskaitų ataskaitinį vienetą.

[![Ataskaitų medžio pavyzdys.](./media/reportingtree-1024x646.png)](./media/reportingtree.png)

### <a name="examples-of-data-roll-up"></a>Duomenų sumavimo pavyzdžiai

Šiuose pavyzdžiuose parodyta galima informacija, naudojama ataskaitų medžio apraše, kaip duomenų sumavimo pavyzdys.

#### <a name="example-1"></a>1 pavyzdys

[![Įmonės išsieiga.](./media/mutlicompanyrollup.png)](./media/mutlicompanyrollup.png)

#### <a name="example-2"></a>2 pavyzdys

[![Kryžminės įmonės padalinio susumuoti.](./media/crosscompanydepartmentrollup.png)](./media/crosscompanydepartmentrollup.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Finansinės ataskaitos](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
