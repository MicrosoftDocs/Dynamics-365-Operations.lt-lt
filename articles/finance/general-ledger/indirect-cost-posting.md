---
title: Netiesioginių išlaidų registravimas
description: Šiame straipsnyje paaiškinama, kaip registruoti netiesiogines išlaidas, kurti išlaidų grupes ir įtraukti mazgus į netiesioginių išlaidų įkainojimo lapą.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CostSheetDesigner, BOMCostGroup, ProjCategory, CostingVersion, CostSheetCalculationFactor
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 04af10760ec50d60cbbc31c233109dffb786933c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868437"
---
# <a name="indirect-cost-posting"></a>Netiesioginių išlaidų registravimas

Netiesioginės išlaidos – tai išlaidos, kurios nėra tiesiogiai susijusios su jokia viena gamybos proceso veikla. Pavyzdžiai apima administravimo išlaidas, pvz., darbuotojų atlyginimus, apskaitos padalinio išlaidas ir pridėtines išlaidas, pvz., nuomos, paslaugų ir įrenginių išlaidas.

## <a name="calculating-indirect-costs"></a>Netiesioginių išlaidų skaičiavimas

Microsoft Dynamics 365 finansai neturi automatizuoto būdo netiesioginių išlaidų kursui skaičiuoti. Turite nustatyti savo netiesiogines išlaidas, sukurti netiesioginių išlaidų kodus ir prižiūrėti visų netiesioginių išlaidų tarifą įkainojimo lape.

Tikslus netiesioginių išlaidų apskaičiavimo procesas įmonėje gali šiek tiek skirtis. Tačiau apskritai procesą sudaro šie pagrindiniai veiksmai:

1. Sukurti netiesioginių išlaidų, kurios bus pripažįstamos gamyboje, sąrašą. Šiame sąraše gali būti nuoma, administravimo išlaidos, apskaitos mokesčiai ir juridiniai mokesčiai. Jos neturėtų apimti žaliavų išlaidų ar darbo išlaidų, kurios atpažįstamos gamybos maršrutuose.
2. Sumuoti visas netiesiogines išlaidas. Galite grupuoti panašius netiesioginių išlaidų tipus arba juos atskirti. Kiekvienos sukonfigūruotos netiesioginės išlaidos gali turėti skirtingas pagrindines sąskaitas, naudojamas registruojant DK.
3. Palyginkite netiesiogines išlaidas su koeficientu, kuris taip pat vadinamas absorbavimo pagrindu. Faktorius gali būti bet kas, ką pasirenkate. Pateikiami keli į bendri pavyzdžiai:

    - Įplaukos
    - Bendras pagamintas kiekis
    - Nustatymo laikas
    - Apdorojimo laikas

    Galite pasirinkti laikotarpį, kurio netiesiogines išlaidas norite skaičiuoti, pvz., kas mėnesį, ketvirtį arba kasmet. Jūsų netiesioginių išlaidų suma ir koeficiento suma turi būti tokia pati kaip laiko suma. Ši formulė naudojama netiesioginių išlaidų tarifui apskaičiuoti:

    *Netiesioginių išlaidų tarifas* = *Bendrosios netiesioginės išlaidos Bendrosios*&divide;*išlaidos Bendrasis koeficientas*

4. Kurti netiesioginių išlaidų grupes.
5. Konfigūruoti įkainojimo lapą su savo tarifais.
6. Išlaikykite įkainojimo versijos netiesioginių išlaidų išlaidas.

> [!NOTE]
> Galite naudoti kaštų **apskaitos modulį**, norėdami sukaupti išlaidas ir nustatyti pridėtines išlaidas iš skirtingų šaltinių, pvz., gamybos, projektų ir DK. Daugiau informacijos rasite Kaštų [apskaita](/cost-accounting/cost-accounting-home-page.md).

> [!IMPORTANT]
> Skirtingi reguliavimo įstaigas galite paskelbti nurodymus apie išlaidų, kurias galima įtraukti kaip netiesiogines išlaidas ar pridėtines išlaidas į savo baigtų prekių išlaidas, tipus. Prieš pradedant konfigūruoti netiesiogines išlaidas, rekomenduojame pasitikrinti savo buhalterius ir vietinius nuostatus, kad įsitikintumėte, jog atitinkate reikalavimus.

## <a name="create-cost-groups-for-indirect-costs"></a>Netiesioginių išlaidų grupių kūrimas

Turite sukurti bent vieną išlaidų grupę, kurią naudosite netiesioginėms išlaidoms. Nėra jokio išlaidų grupių, kurias galite naudoti, skaičiaus apribojimo. Apsvarstykite, kaip skaičiuojate išlaidas ir ar skirtingų išlaidų tipų tarifai yra skirtingi. Pavyzdžiui, jūsų organizacija gamina maisto produktus. Kai kurios žaliavos ir baigtos prekės yra sausos prekės ir yra viena netiesioginė sandėliavimo kaina. Kitų žaliavų ir baigtų prekių išlaidos pasibaigė, o jų netiesioginės išlaidos didesnės. Šiuo atveju galite norėti sukurti dvi išlaidų grupes: sausų medžiagų **ir oro** **medžiagų pridėtines išlaidas**.

Norėdami sukurti netiesioginių išlaidų grupę, atlikite šiuos veiksmus.

1. Eikite į **Gamybos valdymo &gt; nustatymo &gt; maršrutų &gt; išlaidų grupes**.
2. Pasirinkite **Naujas,** jei norite sukurti grupę.
3. Lauke Išlaidų **grupė įveskite** unikalų išlaidų grupės pavadinimą, pvz., **MATOVH**.
4. Lauke Pavadinimas **įveskite** išlaidų grupės aprašymą, pvz., Medžiagų **pridėtinės išlaidos**.
5. Lauke Išlaidų **grupės tipas pasirinkite** Netiesioginė **·**.
6. Pasirinktinai: veikimo būdo lauke **pasirinkite** Fiksuotos išlaidos **arba** Kintamos išlaidos.**·**

## <a name="configure-the-costing-sheet-for-indirect-costs"></a>Konfigūruoti netiesioginių išlaidų įkainojimo lapą

Sukūrę vieną ar daugiau išlaidų grupių, galite konfigūruoti savo įkainojimo lapą su netiesioginėmis išlaidomis ir apibrėžti skaičiavimą. Galite norėti įkainojimo lape sugrupuoti netiesiogines išlaidas. Norėdami grupuoti netiesiogines išlaidas, įkainojimo lape galite sukurti papildomą antraštę. Turite sukurti bent vieną mazgą kiekvienai įkainojimo lapo išlaidų grupei. Kiekvienai netiesioginių išlaidų grupei galite pridėti vieną daugiau netiesioginių išlaidų skaičiavimų.

### <a name="indirect-cost-node-types"></a>Netiesioginių išlaidų mazgų tipai

Šiame skyriuje aprašomi įvairūs netiesioginių išlaidų mazgų tipai.

#### <a name="surcharge"></a>Papildomos išlaidos

**Papildomas** mokestis yra vienas iš dažniausiai pasitaikančių netiesioginių išlaidų tipų. Ji apskaičiuoja išlaidų procentinę dalį pagal gamybos užsakymo išlaidų absorbavimo pagrindą. Nurodykite absorbavimo pagrindą pasirinkdami išlaidų grupes, kurios įkainojimo lape susietos su jūsų medžiagų ar laiko komponentais.

Pavyzdžiui, 3 procentų papildomas mokestis gali būti pridėtas prie visų gamybos užsakymo žaliavų gamybos išlaidų.

#### <a name="rate"></a>Tarifas

Netiesioginės tarifo tipo **išlaidos** naudojamos norint pridėti fiksuotą išlaidų sumą prie gamybos užsakymo, remiantis gamybos užsakymo išlaidų absorbavimo pagrindu. Tarifas gali būti paremtas vienu iš trijų potipių:

- **Procesas** – tarifas paremtas maršruto paleidimo laiku.
- **Nustatymas** – tarifas priklauso nuo maršruto nustatymo laiko.
- **Kiekis** – tarifas paremtas pagamintu kiekiu.

Nurodykite absorbavimo pagrindą pasirinkdami išlaidų grupes, susijusias su medžiagų ar laiko komponentais įkainojimo lape.

Pvz., kiekvienam gamybos užsakymui pridedama fiksuota 2,00 JAV dolerių suma (USD), remiantis darbo išlaidų grupės maršruto vykdymo laiku įkainojimo lape.

#### <a name="output-unit-based"></a>Pagal išvesties vienetą

Tipo Išeigos **vienetas** **netiesioginės** išlaidos apskaičiuojamos dauginant sumą, kuri nurodyta įkainojimo lapo FastTab, iš pasirinkto potipio. Kaip netiesioginių išlaidų daugiklį galite pasirinkti baigtos prekės kiekį, svorį arba tūrį.

Pavyzdžiui, naudojate kiekį, norėdami apskaičiuoti 1.50 USD kiekvieno pagaminto kiekio nusidėvėjimo kiekiui. Kitas pavyzdys– tūrį naudojate norėdami 2.00 USD apie baigtų prekių vietos, kuri atiteks jūsų konteineriams, kiekio mažinimo išlaidas.

#### <a name="input-unit-based"></a>Pagal įvesties vienetą

Netiesioginės įvesties **vieneto tipo** išlaidos apskaičiuojamos dauginant žaliavų kiekį, kuris suvartojamas gamybos užsakyme, iš sumos. Norėdami apskaičiuoti bendrą sumą, galite naudoti gamybos užsakymo įvesties svorį arba tūrį. Galite apriboti skaičiavimą iki medžiagų subrinkinio, **pasirinkdami** vieną ar daugiau išlaidų grupių įkainojimo lapo "FastTab" absorbavimo pagrindu.

Pavyzdžiui, naudojate konkrečios išlaidų grupės, susijusios su efektyviais produktais, žaliavų tūrį, 1.00 USD prie gamybos užsakymo.

### <a name="create-a-total-node-for-indirect-costs-in-the-costing-sheet"></a>Sukurti bendrą netiesioginių išlaidų mazgą įkainojimo lape

Norėdami įkainojimo lape sukurti bendrą netiesioginių išlaidų mazgą, atlikite šiuos veiksmus.

1. Eikite į Išlaidų **valdymo netiesioginių &gt; išlaidų apskaitos strategijų nustatymo įkainojimo &gt; lapą**.
2. Medyje pasirinkite mazgą, nurodantį pagamintų prekių išlaidas.
3. Pasirinkite **Naujas,** kad sukurtumėte mazgą.
4. Lauke Pasirinkti **mazgo tipą** pasirinkite Bendroji **suma**.
5. Lauke Kodas **įveskite** unikalų mazgo ID, pvz., Gamybos **pridėtinės išlaidos**.
6. Pažymėkite žymės **langelį** Antraštė.
7. Pažymėkite žymės **langelį** Bendroji suma.
8. Pasirinkite **Gerai**.

### <a name="create-an-indirect-cost-group-node-in-the-costing-sheet"></a>Netiesioginių išlaidų grupės mazgo kūrimas įkainojimo lape

Norėdami sukurti netiesioginių išlaidų grupės mazgą įkainojimo lape, atlikite šiuos veiksmus.

1. Eikite į Išlaidų **valdymo netiesioginių &gt; išlaidų apskaitos strategijų nustatymo įkainojimo &gt; lapą**.
2. Medyje pasirinkite mazgą, kuriame norite sukurti netiesiogines išlaidas. Pavyzdžiui, pasirinkite bendrą gamybos pridėtinių išlaidų **mazgą**.
3. Pasirinkite **Naujas,** kad sukurtumėte mazgą.
4. Lauke Pasirinkti **mazgo tipą** pasirinkite Išlaidų **grupė**.
5. Kodo lauke **įveskite** unikalų mazgo ID, pvz., **TRANSP**.
6. Aprašymo **lauke** įveskite trumpą aprašymą, pvz., transportavimo **pridėtines išlaidas**.
7. Pasirinkite **Gerai**.
8. Lauke Išlaidų **grupė pasirinkite išlaidų** grupę, pvz. **, OVH1: transportavimo pridėtinės išlaidos**.

### <a name="create-a-surcharge-indirect-cost"></a>Sukurti papildomo mokesčio netiesiogines išlaidas

Norėdami sukurti papildomas netiesiogines išlaidas įkainojimo lape, atlikite šiuos veiksmus.

1. Eikite į Išlaidų **valdymo netiesioginių &gt; išlaidų apskaitos strategijų nustatymo įkainojimo &gt; lapą**.
2. Medyje pasirinkite netiesioginių išlaidų grupės mazgą, kuriame norite sukurti netiesiogines išlaidas. Pvz., pasirinkite visą TRANSP – **transportavimo pridėtinių išlaidų mazgą**.
3. Pasirinkite **Naujas,** kad sukurtumėte mazgą.
4. Lauke Pasirinkti **mazgo tipą** pasirinkite Papildomas **mokestis**.
5. Lauke Kodas įveskite **unikalų** mazgo ID, pvz., Transportavimo papildomas **mokestis**.
6. Pasirinkite **Gerai**.
7. Potipio **lauke** pasirinkite Bendroji **suma**.
8. Norėdami sukurti **išlaidų kodą**, absorbavimo **pagrindu "** FastTab" pasirinkite Naujas.
9. Lauke Kodas **pasirinkite** išlaidų grupę, kuri bus naudojama skaičiuojant papildomą mokestį.
10. Pasirinktinai: kiekvienai papildomai išlaidų grupei, kurią norite naudoti skaičiavimui, pakartokite 8–9 veiksmus.
11. Papildomo mokesčio **"** FastTab" pasirinkite **Naujas**, norėdami sukurti tarifą.
12. Versijos lauke **pasirinkite** įkainojimo versiją, į kurią norite įtraukti papildomą mokestį.
13. Pasirinktinai: lauke Svetainė **įveskite** svetainę, kurios papildomą mokestį norite taikyti.
14. Lauke Procentas **įveskite procentą**, kurį reikia skaičiuoti pagal gamybos užsakymus iš išlaidų grupių, apibrėžtų absorbavimo **pagrindo "** FastTab".
15. Dk registravimo "**FastTab" pasirinkite pagrindinę sąskaitą,** kurią naudosite laukams Įvertintos netiesioginės **išlaidos,** **Įvertinta suvartotų netiesioginių išlaidų savikaina,** NG, **·** **Netiesioginių išlaidų pereis registravimas ir Suvartotų netiesioginių išlaidų išlaidos, NG** laukai.
16. Pasirinktinai: finansinių **dimensijų** "FastTab" nurodykite visas finansines dimensijas, kurios pagal numatytuosius nustatymus turi būti įvedamos operacijose, kai jos registruojamos DK.

Ankstesnė procedūra nurodo, kaip sukurti papildomo mokesčio tipo netiesiogines **išlaidas**. Panašūs veiksmai naudojami kuriant kitų tipų netiesiogines išlaidas. Toliau pateikiami skyriai aprašo kiekvieno tipo skirtumus.

#### <a name="rate"></a>Tarifas

- Atlikdami 4 veiksmą, vietoj papildomo **mokesčio pasirinkite Tarifą** **.**
- Atlikdami 7 veiksmą, vietoj **Bendrosios** **pasirinkite** Procesas **, Nustatymas** arba **Kiekis**.
- Atlikdami 11 veiksmą, naudokite **tarifo** "FastTab", o ne papildomo **mokesčio "** FastTab".
- Atlikdami 14 veiksmą, lauke **Suma įveskite sumą**, o ne procentus **lauke** Procentas.

#### <a name="output-unit-based"></a>Pagal išvesties vienetą

- Atlikdami 4 veiksmą, vietoj papildomo mokesčio **pasirinkite Išeigos** vienetas **·**.
- Atlikdami 7 veiksmą, vietoj **Bendrosios** pasirinkite **Kiekis**, Svoris **arba** **Tūris**.
- Praleisti 8–10 veiksmus.
- Atlikdami 11 veiksmą, naudokite **tarifo** "FastTab", o ne papildomo **mokesčio "** FastTab".

#### <a name="input-unit-based"></a>Pagal įvesties vienetą

- Žingsnyje 4 pasirinkite Įvesties vienetas **vietoj** Papildomo **mokesčio**.
- Atlikdami 7 veiksmą, vietoj **Sumos pasirinkite** Svoris **arba** **Tūris**.
- Atlikdami 11 veiksmą, naudokite **tarifo** "FastTab", o ne papildomo **mokesčio "** FastTab".
