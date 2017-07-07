---
title: "Eilutės apibrėžimo langelių keitimas"
description: "Šiame straipsnyje aprašoma informacija, reikalinga kiekvienam finansinės ataskaitos eilutės aprašo langeliui, ir paaiškina, kaip šią informaciją įvesti."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 58881
ms.assetid: 0af492df-a84e-450c-8045-78ef1211abaf
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 770a1681e4fa9974b081d0c63a10eb1961f13014
ms.openlocfilehash: 40ae4e0774c5752d697baba6c8add8aaf44fbb6d
ms.contentlocale: lt-lt
ms.lasthandoff: 06/13/2017


---

# <a name="modify-row-definition-cells"></a>Eilutės apibrėžimo langelių keitimas

[!include[banner](../includes/banner.md)]


Šiame straipsnyje aprašoma informacija, reikalinga kiekvienam finansinės ataskaitos eilutės aprašo langeliui, ir paaiškina, kaip šią informaciją įvesti. 

# <a name="specify-a-row-code-in-a-row-definition"></a>Eilutės kodo nurodymas eilutės apibrėžime

Eilučių apibrėžimų langelyje **Eilutės kodas** pateikiami skaičiai arba etiketės nurodo kiekvieną eilutės apibrėžimo eilutę. Galite nurodyti, kad eilutės kodas būtų paremtas skaičiavimų ir bendrųjų sumų duomenimis.

### <a name="row-code-requirements"></a>Eilutės kodo reikalavimai

Eilutės kodas būtinas visoms eilutėms. Eilutės aprašyme galite maišyti skaitinius, raidinius-skaitinius ir išjungtus (tuščius) eilutės kodus. Eilutės kodas gali būti bet koks teigiamas sveikasis skaičius (mažesnis negu 100 000 000) arba tą eilutę identifikuojanti aprašomoji etiketė. Aprašomoji etiketė turi būti sudaryta laikantis šių taisyklių:

-   Etiketė turi prasidėti abėcėlės raide (nuo a iki ž arba nuo A iki Ž) ir tai gali būti bet kokia iki 16 simbolių ilgio skaičių ir raidžių kombinacija. 
    > [!NOTE]
    > Etiketėje gali būti pabraukimo simbolis (\_), bet specialiųjų simbolių naudoti neleidžiama.
-   Etiketėje negalima naudoti nė vieno iš šių rezervuotų žodžių: AND, OR, IF, THEN, ELSE, PERIODS, TO, BASEROW, UNIT, NULL, CPO arba RPO.

Šie pavyzdžiai yra tinkami eilutės kodai:

-   320
-   TL\_NET\_INCOME
-   TL\_NET\_94

### <a name="change-a-row-code-in-a-row-definition"></a>Eilutės kodo keitimas eilutės apibrėžime

1.  Ataskaitų dizaino įrankyje spustelėkite **Eilučių aprašai**, tada atidarykite norimą keisti eilutės aprašą.
2.  Atitinkamos eilutės stulpelio **Eilutės kodas** langelyje įveskite naują reikšmę.

### <a name="reset-numeric-row-codes"></a>Skaitinių eilutės kodų nustatymas iš naujo

1.  Ataskaitos dizaino įrankyje spustelėkite **Eilučių apibrėžimai**, tada atidarykite norimą keisti eilutės apibrėžimą.
2.  Meniu **Redaguoti** spustelėkite **Pernumeruoti eilutes**.
3.  Dialogo lange **Pernumeruoti eilutes** nurodykite naujas pradžios eilutės kodo ir eilutės kodo pokyčio reikšmes. Galite iš naujo nustatyti skaitinių eilutės kodų reikšmes, kad jos būtų vienodo ilgio. Tačiau ataskaitų dizaino įrankis pernumeruoja tik tuos eilutės kodus, kurie prasideda skaičiais (pavyzdžiui, 130 arba 246). Raidėmis prasidedantys eilutės kodai (pavyzdžiui, INCOME\_93 arba TP0693) nepernumeruojami. 
> [!NOTE]
> Kai pernumeruojate eilutės kodus, ataskaitų dizaino įrankis automatiškai atnaujina nuorodas **TOT** ir **CAL**. Pavyzdžiui, jei eilutėje **TOT** nurodomas intervalas, kuris prasideda eilutės kodu 100, o jūs pernumeruojate eilutes, pradėdami nuo 90, pradžios nuoroda **TOT** pasikeičia iš 100 į 90.

## <a name="add-a-description"></a>Aprašo įtraukimas
Aprašymo langelyje pateikiamas ataskaitos eilutėje, pvz., „Įplaukos“ arba „Grynosios pajamos“, nurodytų finansinių duomenų aprašymas. Langelio **Aprašymas** tekstas rodomas ataskaitoje tiksliai toks, kokį jį įvedate eilutės apibrėžime. 
> [!NOTE]
> Ataskaitos aprašymo stulpelio plotis nustatomas stulpelio apibrėžime. Jei eilutės apibrėžimo stulpelio **Aprašymas** tekstas yra ilgas, patikrinkite stulpelio **DESC** plotį. Naudojant dialogo langą **Įterpti eilutes iš** stulpelio **Aprašymas** reikšmės yra finansinių duomenų segmentų reikšmės arba dimensijų reikšmės. Galite įterpti eilutes, jeigu norite įtraukti aprašymą, pvz., skyriaus antraštę arba skyriaus bendrąją sumą, ir pridėti formatavimą, pvz., eilutę prieš bendrosios sumos eilutę. Jei ataskaitoje pateikiamas ataskaitų medis, galite įtraukti papildomą tekstą, kuris apibrėžtas ataskaitų medžio ataskaitiniams vienetams. Taip pat galite apriboti papildomą tekstą tam tikru ataskaitiniu vienetu.

### <a name="add-the-description-for-a-line-on-a-report"></a>Ataskaitos eilutės aprašo įtraukimas

1.  Ataskaitos dizaino įrankyje spustelėkite **Eilučių apibrėžimai**, tada atidarykite norimą keisti eilutės apibrėžimą.
2.  Pasirinkite langelį **Aprašymas**, tada įveskite ataskaitos eilutės pavadinimą.
3.  Taikykite formatavimą.

### <a name="add-additional-text-from-a-reporting-tree-in-the-description"></a>Papildomo ataskaitų medžio teksto įtraukimas į aprašymą

1.  Ataskaitos dizaino įrankyje spustelėkite **Eilučių apibrėžimai**, tada atidarykite norimą keisti eilutės apibrėžimą.
2.  Įveskite papildomo teksto kodą ir bet kurį kitą tekstą į atitinkamą langelį **Aprašymas**.
3.  Taikykite formatavimą.

### <a name="limit-the-additional-text-to-a-specific-reporting-unit"></a>Papildomo teksto apribojimas tam tikru ataskaitiniu vienetu

1.  Ataskaitos dizaino įrankyje spustelėkite **Eilučių apibrėžimai**, tada atidarykite norimą keisti eilutės apibrėžimą.
2.  Raskite eilutę, kurioje turėtų būti sukurtas papildomas tekstas, tada dukart spustelėkite stulpelio **Susijusios formulės / eilutės / vienetai** langelį.
3.  Dialogo lango **Ataskaitinio vieneto pasirinkimas** lauke **Ataskaitų medis** pasirinkite ataskaitų medį.
4.  Lauke **Apribojimo ataskaitinio vieneto pasirinkimas** išplėskite arba sutraukite ataskaitų medį, tada pasirinkite ataskaitinį vienetą.

## <a name="add-a-format-code"></a>Formato kodo įtraukimas
Langelyje **Formato kodas** pateikiamos kelios iš anksto suformatuotos pasirinktys, skirtos tos eilutės turiniui. Jei langelis **Formato kodas** tuščias, eilutė interpretuojama kaip finansinių duomenų informacijos eilutė. 
> [!NOTE]
> Jei ataskaitoje yra ne sumą formatuojančių eilučių, susijusių su sumos eilutėmis, kurios buvo sulaikytos (pvz., dėl nulinio balanso), norėdami, kad nebūtų spausdinamos pavadinimo ir formato eilutės, galite naudoti stulpelį **Susijusios formulės / eilutės / vienetai**.

### <a name="add-a-format-code-to-a-report-row"></a>Formato kodo įtraukimas į ataskaitos eilutę

1.  Ataskaitos dizaino įrankyje spustelėkite **Eilučių apibrėžimai**, tada pasirinkite norimą keisti eilutės apibrėžimą.
2.  Dukart spustelėkite langelį **Formato kodas**.
3.  Sąraše pasirinkite formato kodą. Šioje lentelėje aprašomi formato kodai ir jų veiksmai.
    | Formato kodas                   | Formato kodo interpretavimas | Veiksmas|
    |---|---|---|
    | (Nėra)                        |                                    | Išvalomas langelis **Formato kodas**.                                                                                                                                                                               |
    | IŠ VISO                           | Bendroji suma                              | Nurodoma eilutė, kuri stulpelyje **Susijusios formulės / eilutės / vienetai** naudoja matematinius ženklus. Bendrosioms sumoms naudojami paprasti ženklai, pavyzdžiui **+** arba **-**.                                                      |
    | KPL                           | Skaičiavimas                        | Nurodoma eilutė, kuri stulpelyje **Susijusios formulės / eilutės / vienetai** naudoja matematinius ženklus. Skaičiavimams naudojami sudėtingi ženklai, pavyzdžiui, **+**, **-**, **\***, **/** ir **IF / THEN / ELSE** sakiniai. |
    | DES                           | aprašymas                        | Nurodoma ataskaitos antraštės eilutė arba tuščia eilutė.                                                                                                                                                        |
    | LFT RGT CEN                   | Kairė Dešinė Centras                  | Ataskaitos puslapyje sulygiuojamas eilutės aprašymo tekstas, neatsižvelgiant į teksto išdėstymą stulpelio apraše.                                                                                               |
    | CBR                           | Pagrindinės eilutės keitimas                    | Nurodoma eilutė, kuri nustato pagrindinę stulpelio skaičiavimų eilutę.                                                                                                                                               |
    | STULPELIS                        | Stulpelio lūžis                       | Ataskaitoje pradedamas naujas stulpelis.                                                                                                                                                                             |
    | PUSLAPIS                          | Puslapio lūžis                         | Ataskaitoje pradedamas naujas puslapis.                                                                                                                                                                               |
    | ---                           | Vienas pabraukimas                   | Po visais ataskaitos sumos stulpeliais nubrėžiama viena linija.                                                                                                                                                     |
    | ===                           | Du pabraukimai                   | Po visais ataskaitos sumos stulpeliais nubrėžiamos dvi linijos.                                                                                                                                                     |
    | LINE1                         | Plona linija                          | Per visą puslapį nubrėžiama viena plona linija.                                                                                                                                                                      |
    | LINE2                         | Stora linija                         | Per visą puslapį nubrėžiama viena stora linija.                                                                                                                                                                     |
    | LINE3                         | Punktyrinė linija                        | Per visą puslapį nubrėžiama viena punktyrinė linija.                                                                                                                                                                    |
    | LINE4                         | Stora ir plona linijos           | Per visą puslapį nubrėžiamos dvi linijos. Viršutinė linija stora, o apatinė – plona.                                                                                                                       |
    | LINE5                         | Plona ir stora linijos           | Per visą puslapį nubrėžiamos dvi linijos. Viršutinė linija plona, o apatinė – stora.                                                                                                                       |
    | BXB BXC                       | Eilutė kvadrate                          | Aplink ataskaitų eilutes, kurios prasideda eilute **BXB** ir baigiasi eilute **BXC**, apibrėžiamas kvadratas.                                                                                                               |
    | LIK.                           | Pastaba                             | Nurodoma komentarų eilutė, kuri neturėtų būti spausdinama ataskaitoje. Pavyzdžiui, pastabų eilutėje gali būti paaiškinti jūsų formatavimo būdai.                                                            |
    | SORT ASORT SORTDESC ASORTDESC | Rūšiuoti                               | Rūšiuojamos išlaidos arba įplaukos, rūšiuojama faktinė arba biudžeto nuokrypio ataskaita pagal didžiausią nuokrypį arba rūšiuojami eilučių aprašymai abėcėlės tvarka.                                                                   |

## <a name="specify-related-formulasrowsunits"></a>Susijusių formulių / eilučių / vienetų nurodymas
Langelis **Susijusios formulės / eilutės / vienetai** skirtas keliems tikslams. Priklausomai nuo eilutės tipo, langelis **Susijusios formulės / eilutės / vienetai** gali atlikti vieną iš šių funkcijų:

-   Nustatyti eilutes, kurios turėtų būti įtraukiamos į skaičiavimą, kai naudojate formato kodą **TOT** arba **KPL**.
-   Susieti formatavimo eilutę su sumos eilute, kad formatavimas būtų spausdinamas tik tada, kai spausdinama susijusi suma.
-   Apriboti eilutę iki konkretaus ataskaitinio vieneto.
-   Aprašyti pagrindinę skaičiavimų eilutę, kai naudojate formato kodą **BASEROW**.
-   Nurodyti eilutes, kurios turi būti rūšiuojamos, kai naudojate vieną iš rūšiavimo formato kodų.

### <a name="use-a-row-total-in-a-row-definition"></a>Eilutės bendrosios sumos naudojimas eilutės apibrėžime

Naudokite eilutės bendrosios sumos formulę, norėdami pridėti arba atimti kitų eilučių sumas. Formulė, naudojama norint sukurti eilutės bendrąją sumą, gali būti sudaryta iš ženklų + ir -, kad būtų sujungiami atskiri eilučių kodai ir intervalai. Intervalai nurodomi dvitaškiu (:). Formulę gali sudaryti iki 1024 simbolių. Standartinės sumavimo formulės pavyzdys: 400+420+430+450+460LIABILITIES+EQUITY520:546520:546-LIABILITIES

### <a name="components-of-a-row-total-formula"></a>Eilutės bendrosios sumos formulės komponentai

Kurdami eilutės bendrosios sumos formulę turite naudoti eilutės kodus, kad nurodytumėte, kurias eilutes pridėti ar atimti dabartiniame eilutės apibrėžime, ir turite naudoti ženklus, kad nurodytumėte, kaip eilutės jungiamos. Bendrosios sumos ir sumos eilutes galima naudoti bet kokioje kombinacijoje. **Pastaba:** visos į intervalą patenkančios bendrosios sumos eilutės neįtraukiamos. Norėdami sukurti bendrąją sumą, galite nurodyti eilučių intervalą. Jei pirmoji intervalo eilutė yra bendrosios sumos eilutė, ta eilutė įtraukiama į naują bendrąją sumą. Toliau pateikiamoje lentelėje aprašoma, kaip eilutės bendrosios sumos formulėse naudojami ženklai.

| Operatorius | Formulės pavyzdys | aprašymas                                                 |
|----------|-----------------|-------------------------------------------------------------|
| +        | 100+330         | Eilutėje 100 esanti suma pridedama prie eilutėje 330 esančios sumos.        |
| :        | 100:330         | Sudedamos visų eilučių (nuo 100 iki 330) bendrosios sumos.    |
| -        | 100-330         | Eilutėje 100 esanti suma atimama iš eilutėje 330 esančios sumos. |

### <a name="create-a-row-total"></a>Eilutės bendrosios sumos kūrimas

1.  Ataskaitos dizaino įrankyje spustelėkite **Eilučių apibrėžimai**, tada atidarykite norimą keisti eilutės apibrėžimą.
2.  Dukart spustelėkite eilutės apibrėžimo langelį **Formato kodas**, tada pasirinkite **TOT**.
3.  Langelyje **Susijusios formulės / eilutės / vienetai** įveskite bendrosios sumos formulę.

### <a name="relate-a-format-row-to-an-amount-row"></a>Formato eilutės susiejimas su sumos eilute

Eilutės apibrėžimo stulpelyje **Formato kodas** formato kodai **DES**, **LFT**, **RGT**, **CEN**, **---** ir **===** formatuoja tik ne sumos eilutes. Norėdami, kad šis formatavimas nebūtų spausdinamas, kai sulaikomos susijusios eilutės (pavyzdžiui, todėl, kad sumos eilutėse yra nulinių reikšmių arba nėra laikotarpio aktyvumo), turite susieti formato eilutes su atitinkamomis sumų eilutėmis. Ši funkcija naudinga, kai norite neleisti spausdinti antraščių arba formatavimo, kuris yra susijęs su tarpinėmis sumomis, kai nėra jokios spausdintinos laikotarpio informacijos. 
    > [!NOTE]
    >  You can also prevent the detailed amount rows from being printed by clearing the option to display rows without amounts. This option is located on the **Settings** tab of the report definition. By default, transaction detail accounts that have a zero balance or no period activity are suppressed in reports. To show these transaction detail accounts, select the **Display rows without an amounts** check box on the **Settings** tab of the report definition.

### <a name="relate-a-format-row-to-an-amount-row"></a>Formato eilutės susiejimas su sumos eilute

1.  Ataskaitos dizaino įrankyje spustelėkite **Eilučių apibrėžimai**, tada pasirinkite norimą keisti eilutės apibrėžimą.
2.  Formatavimo eilutės langelyje **Susijusius formulės / eilutės / vienetai** įveskite sulaikomos sumos eilutės kodą. **Pastaba:** norint, kad sumos eilutė būtų sulaikyta, eilutės balansas turi būti 0 (nulis). Balansą turinti eilutė nesulaikoma.
3.  Meniu **Rinkmena** spustelėkite **Įrašyti**.

### <a name="example-of-preventing-printing-of-rows"></a>Pavyzdys, kaip neleisti spausdinti eilučių

Šiame pavyzdyje Phyllis nori neleisti spausdinti savo ataskaitos eilutės **Bendroji grynųjų suma** antraštės ir pabraukimų, nes nė vienoje iš grynųjų pinigų sąskaitų nebuvo jokios veiklos. Todėl eilutės 220 (kuri, kaip nurodo formato kodas **---**, yra formatavimo eilutė) langelyje **Susijusios formulės / Eilutės / Vienetai** ji įveda skaičių **250**, kuris yra jos norimos sulaikyti sumos eilutės kodas. [![RelatedRowsRowDefinition](./media/relatedrowsrowdefinition-1024x144.png)](./media/relatedrowsrowdefinition.png)

## <a name="select-the-base-row-for-a-column-calculation"></a>Pagrindinės stulpelio skaičiavimo eilutės pasirinkimas
Ryšių ataskaitos eilutės apibrėžime priskirkite vieną ar kelias pagrindines eilutes naudodami formato kodą **CBR** (keisti pagrindinę eilutę). Tada pagal stulpelio aprašo apskaičiavimą nurodoma pagrindinė eilutė. Toliau pateikiami keletas įprastų CBR skaičiavimų pavyzdžių.

-   Bendrųjų įplaukų procentas, kadangi jis susijęs su atskirais įplaukų elementais
-   Bendrųjų išlaidų procentas, kadangi jis susijęs su atskirais išlaidų elementais
-   Bruto maržos procentas, kadangi jis susijęs su padalinio ar skyriaus informacija.

Eilutės apibrėžime nurodoma viena arba kelios pagrindinės eilutės, tada stulpelio apibrėžime nustatomas ryšys, kuriuo pagrindinė eilutė paskelbiama. Stulpelio formulėje naudojamas kodas yra **BASEROW**. Su kodu **BASEROW** naudojami šie pagrindiniai matematiniai veiksmai: dalinti, dauginti, pridėti ar atimti. Dažniausiai naudojamas veiksmas yra dalinti iš **BASEROW**, kai rezultatas rodomas procentais. Stulpelio skaičiavimuose, kurių formulėje naudojamas kodas **BASEROW**, susijusiems pagrindinių eilučių kodams naudojamas eilutės apibrėžimas. **CBR** eilutės apibūdinamos nurodant:

-   **CBR** eilutės nespausdinamos baigtoje ataskaitoje.
-   **CBR** formato kodas ir jo susijęs eilutės kodas rodomi virš eilutės arba skyriaus, kuriame rodomi susiję skaičiavimai.

Stulpelio apibrėžime pateikiamas stulpelio tipas **CALC** nurodo stulpelį, kuris eilutėje **Formulė** nurodo formulę. Ši formulė veikia šio ataskaitos stulpelio duomenis ir naudoja raktažodį Baserow, pagal kurį atliekami pagrindiniai eilutės formato kodų **CBR** skaičiavimai. Eilutės apibrėžimo formato kodas **CBR** nurodo stulpelių, kurie kiekvienoje ataskaitos eilutėje apskaičiuoja procentą arba padaugina iš pagrindinės eilutės, pagrindinę eilutę. Eilutės formate galite turėti kelis **CBR** formato kodus, pvz., vieną gryniesiems pardavimams, vieną bruto pardavimams ir vieną bendrosioms išlaidoms. Paprastai formato kodas **CBR** naudojamas norint sukurti su bendrosios sumos eilute lyginamų sąskaitų procentą. Pagrindinė eilutė naudojama atliekant visus skaičiavimus, kol nurodoma kita pagrindinė eilutė. Turite nurodyti pradžios **CBR** formato kodą ir pabaigos **CBR** formato kodą. Pvz., norėdami nurodyti išlaidas kaip grynojo pardavimo procentą, galite padalinti kiekvienos išlaidų eilutės reikšmę iš grynojo pardavimo eilutės reikšmės. Šiuo atveju grynojo pardavimo eilutė yra pagrindinė eilutė. Galite pateikti stulpelio apibrėžimą, kuriame nurodomi šių metų ir šių metų iki šios dienos rezultatai kartu su kiekvieno rezultato pagrindiniu procentu, kaip parodyta toliau pateiktame pavyzdyje. Pradėkite nuo išsamaus pajamų išrašo.

### <a name="select-the-base-row-in-a-row-definition-for-a-column-calculation"></a>Stulpelio skaičiavimui skirtos eilutės apibrėžimo pagrindinės eilutės pasirinkimas

1.  Ataskaitos dizaino įrankyje spustelėkite **Stulpelio aprašai**, tada atidarykite įplaukų išrašo stulpelio aprašą.
2.  Įtraukite naują stulpelį į stulpelio aprašą ir nustatykite stulpelio tipą **CALC**.
3.  Naujo stulpelio langelyje **Formulė** įveskite formulę **X/BASEROW**, kurioje **X** yra **FD** stulpelio tipas, kurio procentas rodomas.
4.  Dukart spustelėkite langelį **Formato / valiutos nepaisymas**.
5.  Dialogo lango **Formato nepaisymas** sąraše **Formato kategorija** pasirinkite **Procentas**, tada spustelėkite **Gerai**.
6.  Norėdami įrašyti stulpelio apibrėžimą nauju pavadinimu, meniu **Failas** spustelėkite **Įrašyti kaip**. Prie dabartinio failo pavadinimo pridėkite **CBR** (pvz., **CUR\_YTD\_CBR**). Šis stulpelio apibrėžimas yra jūsų pagrindinės eilutės stulpelio apibrėžimas.
7.  Ataskaitos dizaino įrankyje spustelėkite **Eilučių apibrėžimai**, tada atidarykite eilutės apibrėžimą, kurį norite keisti naudodami pagrindinės eilutės skaičiavimą.
8.  Virš eilutės, kurioje turėtų prasidėti pagrindinės eilutės skaičiavimas, įterpkite naują eilutę.
9.  Dukart spustelėkite eilutės apibrėžimo langelį **Formato kodas**, tada pasirinkite **CBR**.
10. Langelyje **Susijusios formulės / eilutės / vienetai** įveskite pagrindinės eilutės kodo numerį.

### <a name="example-of-base-row-calculation"></a>Pagrindinės eilutės skaičiavimo pavyzdys

Toliau pateikiamame eilutės apibrėžimo pavyzdyje eilutėje 100 rodoma, kad pagrindinė skaičiavimų eilutė yra eilutė 280. [![Pagrindinės eilutės skaičiavimo pavyzdys.](./media/cbrrowdefinition.png)](./media/cbrrowdefinition.png) Toliau pateikiamame stulpelio aprašo pavyzdyje skaičiavimams naudojamas **CBR** formato kodas. Stulpelio C skaičiavimas padalina ataskaitos stulpelio B reikšmę iš stulpelio B eilutės 280 reikšmės. Stulpelio B formato nepaisymas atspausdina skaičiavimo rezultatą procentais. Taip pat kiekviena stulpelio E suma yra stulpelio D suma grynojo pardavimo procentais. [![Stulpelio aprašo pavyzdys.](./media/cbrcolumndefinition2.png)](./media/cbrcolumndefinition2.png) Toliau pateikiamame pavyzdyje rodoma ataskaita, kuri gali būti sugeneruota pagal ankstesnius skaičiavimus. [![Ataskaitos pavyzdys pagal ankstesnius skaičiavimo pavyzdžius.](./media/cbrreport-1024x272.png)](./media/cbrreport.png)

## <a name="select-a-sorting-code-for-a-row-definition"></a>Eilutės aprašo rūšiavimo kodo pasirinkimas
Rūšiavimo kodai rūšiuoja sąskaitas arba reikšmes, faktines arba biudžeto nuokrypio ataskaitas pagal didžiausią nuokrypį arba eilučių aprašymus abėcėlės tvarka. Galimi šie rūšiavimo kodai:

-   **SORT** – ataskaitos rūšiuojamos didėjančia tvarka, pagal nurodyto stulpelio reikšmes.
-   **ASORT** – ataskaitos rūšiuojamos didėjančia tvarka, pagal nurodyto stulpelio reikšmių absoliučiąją reikšmę. Kitaip tariant, rūšiuojant reikšmes kiekvienos reikšmės ženklo nepaisoma. Šis formato kodas rikiuoja reikšmes pagal nuokrypio dydį, nepaisant to, ar nuokrypis teigiamas arba neigiamas.
-   **SORTDESC** – ataskaitos rūšiuojamos mažėjančia tvarka, pagal nurodyto stulpelio reikšmes.
-   **ASORTDESC** – ataskaitos rūšiuojamos mažėjančia tvarka, pagal nurodyto stulpelio reikšmių absoliučiąją reikšmę.

### <a name="select-a-sorting-code"></a>Rūšiavimo kodo pasirinkimas

1.  Ataskaitos dizaino įrankyje spustelėkite **Eilučių apibrėžimai**, tada atidarykite norimą keisti eilutės apibrėžimą.
2.  Dukart spustelėkite langelį **Formato kodas**, tada pasirinkite rūšiavimo kodą.
3.  Langelyje **Susijusios formulės / eilutės / vienetai** nurodykite rūšiuojamų eilučių kodų diapazoną. Norėdami nurodyti diapazoną, įveskite pirmą eilutės kodą, dvitaškį (:), tada paskutinį eilutės kodą. Pavyzdžiui, įveskite **160:490**, jeigu norite nurodyti, kad diapazonas yra nuo 160 eilutės iki 490 eilutės.
4.  Langelyje **Stulpelio apribojimas** įveskite rūšiavimui naudojamą ataskaitos stulpelio raidę. 
    > [!NOTE]
    > Rūšiavimui skaičiuoti naudokite tik sumos eilutes.

### <a name="examples-of-ascending-and-descending-column-values"></a>Didėjančių ir mažėjančių stulpelių reikšmių pavyzdžiai

Toliau pateiktame pavyzdyje ataskaitos D stulpelio vertės rūšiuojamos didėjančia tvarka, nuo 160 iki 490 eilutės. Be to, ataskaitos G stulpelio absoliučiosios vertės rūšiuojamos mažėjančia tvarka, nuo 610 iki 940 eilutės.

| Eilutės kodas | Prekės/Paslaugos pavadinimas                                         | Formato kodas | Susijusios formulės / eilutės / vienetai | Standartinis balansas | Stulpelio apribojimas | Saitas su finansinėmis dimensijomis |
|----------|-----------------------------------------------------|-------------|-----------------------------|----------------|--------------------|------------------------------|
| 100      | Surūšiuota pagal mėnesio nuokrypį, didėjančia tvarka       | DES         |                             |                |                    |                              |
| 130      |                                                     | SORT        | 160:490                     |                | D                  |                              |
| 160      | Pardavimas                                               |             |                             | K              |                    | 4100                         |
| 190      | Pardavimo grąžinimai                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 490      | Palūkanų pajamos                                     |             |                             | K              |                    | 7000                         |
| 520      |                                                     | DES         |                             |                |                    |                              |
| 550      | Surūšiuota pagal absoliutųjį nuokrypį nuo metų pradžios, mažėjančia tvarka | DES         |                             |                |                    |                              |
| 580      |                                                     | ASORTDESC   | 610:940                     |                | Ž                  |                              |
| 610      | Pardavimas                                               |             |                             | K              |                    | 4100                         |
| 640      | Pardavimo grąžinimai                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 940      | Palūkanų pajamos                                     |             |                             | K              |                    | 7000                         |

Čia pateikiamas sugeneruotos ataskaitos pavyzdys.

|||||||||
|---|---|---|---|---|---|---|
|**Nuokrypio analizė (surūšiuota pagal nuokrypį)**|||||||

|**Pekino ir Atlantos regionai**|||||||

|**Septyniems mėnesiams iki 2013 m. liepos 31 d.**|||||||

||**Liepos mėn.**|**Nuo metų pradžios**|||||

||**Faktinė**|**Biudžeto**|**Nuokrypio**|**Faktinė**|**Biudžeto**|**Nuokrypio**|

|**Surūšiuota pagal mėnesio nuokrypį, didėjančia tvarka**|||||||

|PPK|873 872|236 144|(637 728)|4 864 274|1 590 315|(3 273 959)|

|Atlyginimai|97 624|65 573|(32 051)|653 884|441 664|(212 220)| |Pardavimo nuolaidos|36 383|24 152|(12 231)|241 562|162 670|(78 892)| |Pardavimo įplaukos|10 917|7 246|(3 671)|62 809|48 803|(14 006)| |Nuomos išlaidos|12 052|9 019|(3 033)|80 444|60 748|(19 696)| |Biuro išlaidos|5 023|3 291|(1 732)|33 420|22 098|(11 322)| |Kelionių išlaidos|7 656|7 641|(15)|51 062|51 469|407| |Pardavimas|1 240 119|410 389|829 730|7 139 288|2 764 549|4 374 739| |**Surūšiuota pagal absoliutųjį nuokrypį nuo metų pradžios, mažėjančia tvarka**||||||| |Pardavimas|1 240 119|410 389|829 730|7 139 288|2 764 549|4 374 739| |Kelionių išlaidos|7 656|7 641|(15)|51 062|51 469|407| |Biuro išlaidos|5 023|3 291|(1 732)|33 420|22 098|(11 322)| |Pardavimo įplaukos|10 917|7 246|(3 671)|62 809|48 803|(14 006)| |Nuomos išlaidos|12 052|9 019|(3 033)|80 444|60 748|(19 696)| |Pardavimo nuolaidos|36 383|24 152|(12 231)|241 562|162 670|(78 892)| |Atlyginimai|97 624|65 573|(32 051)|653 884|441 664|(212 220)| |PPK|873 872|236 144|(637 728)|4 864 274|1 590 315|(3 273 959)|

## <a name="specify-a-format-override-cell"></a>Formato nepaisymo langelio nurodymas
Langelyje **Formato nepaisymas** nurodomas formatavimas, kuris naudojamas eilutei, kai spausdinama ataskaita. Šis formatavimas pakeičia formatavimą, nurodytą stulpelio apraše ir ataskaitos apraše. Pagal numatytuosius nustatymus, tuose aprašuose nurodytas formatavimas yra valiuta. Jei vienoje ataskaitos eilutėje nurodomas turto vienetų skaičius, pavyzdžiui, pastatų skaičius, o kitoje eilutėje nurodoma to turto piniginė vertė, galite nepaisyti valiutos formatavimo ir įvesti skaitinį eilutės formatavimą, kuriame nurodomas pastatų skaičius. Šią informaciją nurodote dialogo lange **Formato nepaisymas**. Galimos pasirinktys priklauso nuo pasirinktos formato kategorijos. Dialogo lango srityje **Pavyzdys** rodomi formatų pavyzdžiai. Galimos šios formato kategorijos:

-   Valiutos formatavimas
-   Skaitinis formatavimas
-   Procentinis formatavimas
-   Pasirinktinis formatavimas

### <a name="override-cell-formatting"></a>Langelių formatavimo nepaisymas

1.  Ataskaitų dizaino įrankyje atidarykite norimą modifikuoti eilutės apibrėžimą.
2.  Eilutėje, kurioje turi būti nepaisoma formato, dukart spustelėkite stulpelio **Formato nepaisymas** langelį.
3.  Dialogo lange **Formato nepaisymas** pasirinkite tai ataskaitos eilutei naudojamas formatavimo pasirinktis.
4.  Spustelėkite **GERAI**.

### <a name="currency-formatting"></a>Valiutos formatavimas

Valiutos formatavimas taikomas finansinei sumai ir apima valiutos simbolį. Galimos toliau nurodytos pasirinktys:

-   **Valiutos simbolis** – ataskaitos valiutos simbolis. Ši reikšmė nepaiso įmonės informacijos nuostatos **Regiono pasirinktys**.
-   **Neigiami skaičiai** – neigiami skaičiai gali būti su minuso ženklu (-), jie gali būti rodomi skliausteliuose, arba jie gali būti su trikampio ženklu (∆).
-   **Po kablelio** – skaitmenų skaičius po dešimtainio skyriklio.
-   **Nulinės vertės nepaisymo tekstas** – tekstas, kuris įtraukiamas į ataskaitą, kai suma lygi 0 (nuliui). Šis tekstas rodomas kaip paskutinė srities **Pavyzdys** eilutė. 
    > [!NOTE]
    >  Jei sulaikomas nulinių reikšmių spausdinimas arba nėra laikotarpio veiklos, šis tekstas panaikinamas.

### <a name="numeric-formatting"></a>Skaitinis formatavimas

Skaitinis formatavimas taikomas bet kokiai sumai ir neapima valiutos simbolio. Galimos toliau nurodytos pasirinktys:

-   **Neigiami skaičiai** – neigiami skaičiai gali būti su minuso ženklu (-), jie gali būti rodomi skliausteliuose, arba jie gali būti su trikampio ženklu (∆).
-   **Po kablelio** – skaitmenų skaičius po dešimtainio skyriklio.
-   **Nulinės vertės nepaisymo tekstas** – tekstas, kuris įtraukiamas į ataskaitą, kai suma lygi 0 (nuliui). Šis tekstas rodomas kaip paskutinė srities **Pavyzdys** eilutė. 
    > [!NOTE]
    >  Jei sulaikomas nulinių reikšmių spausdinimas arba nėra laikotarpio veiklos, šis tekstas panaikinamas.

### <a name="percentage-formatting"></a>Procentinis formatavimas

Procentinis formatavimas apima procento ženklą (%). Galimos toliau nurodytos pasirinktys:

-   **Neigiami skaičiai** – neigiami skaičiai gali būti su minuso ženklu (-), jie gali būti rodomi skliausteliuose, arba jie gali būti su trikampio ženklu (∆).
-   **Po kablelio** – po dešimtainio skyriklio rodomų skaitmenų skaičius.
-   **Nulinės vertės nepaisymo tekstas** – tekstas, kuris įtraukiamas į ataskaitą, kai suma lygi 0 (nuliui). Šis tekstas rodomas kaip paskutinė srities **Pavyzdys** eilutė. 
    > [!NOTE]
    >  Jei sulaikomas nulinių reikšmių spausdinimas arba nėra laikotarpio veiklos, šis tekstas panaikinamas.

### <a name="custom-formatting"></a>Pasirinktinis formatavimas

Naudokite pasirinktinio formatavimo kategoriją, norėdami sukurti pasirinktinio formato nepaisymą. Galimos toliau nurodytos pasirinktys:

-   **Tipas** – pasirinktinis formatas.
-   **Nulinės vertės nepaisymo tekstas** – tekstas, kuris įtraukiamas į ataskaitą, kai suma lygi 0 (nuliui). Šis tekstas rodomas kaip paskutinė srities **Pavyzdys** eilutė. 
    > [!NOTE]
    >  Jei sulaikomas nulinių reikšmių spausdinimas arba nėra laikotarpio veiklos, šis tekstas panaikinamas.

Dalyje Tipas turėtų būti nurodyta teigiama reikšmė, o po to – neigiama reikšmė. Paprastai įvedate panašų teigiamas ir neigiamas reikšmes atskiriantį formatą. Pavyzdžiui, norėdami nurodyti, kad teigiamos ir neigiamos reikšmės turi du skaitmenis po kablelio, bet neigiamos reikšmės rodomos skliausteliuose, įveskite **0.00;(0.00)**. Toliau pateikiamoje lentelėje rodomi pasirinktiniai formatai, kuriuos galite naudoti norėdami valdyti savo reikšmių formatą. Visi pavyzdžiai pradedami reikšme 1234.56.

| Formatuoti                         | Teigiama   | Neigiamas     | Nulis    |
|--------------------------------|------------|--------------|---------|
| 0                              | 1235       | -1235        | 0       |
| 0;0                            | 1235       | 1235         | 0       |
| 0;(0);-                        | 1235       | 1235         | -       |
| \#,\#\#\#;(\#,\#\#\#);“”       | 1,235      | (1,235)      | (tuščia) |
| \#,\#\#0.00;(\#,\#\#0.00);zero | 1,234.56   | (1,234.56)   | nulis    |
| 0.00%;(0.00%)                  | 123456.00% | (123456.00%) | 0.00%   |

## <a name="specify-a-normal-balance-cell"></a>Įprastinio balanso langelio nurodymas
Eilutės apibrėžimo langelis **Įprastinis balansas** valdo eilutės sumų ženklą. Norėdami pakeisti eilutės ženklą, arba jeigu įprastinis sąskaitos balansas yra kreditas, tos eilutės langelyje **Įprastinis balansas** įveskite **C**. Naudojant ataskaitų dizaino įrankį pakeičiamas visų tos eilutės kredito balanso sąskaitų ženklas. Kai ataskaitų dizaino įrankis konvertuoja šias sąskaitas, pašalinama visų sumų debeto / kredito charakteristika, todėl sumavimas paprastas. Pvz., norėdami apskaičiuoti grynąsias pajamas, iš pajamų atimkite išlaidas. Dažniausiai susumuotoms ir apskaičiuotoms eilutėms kodas **C** įtakos neturi. Tačiau stulpelio aprašo spausdinimo valdiklis **XCR** pakeičia bet kurios eilutės, kurios stulpelyje **Įprastinis balansas** yra nurodyta **C**, ženklą. Šis formatavimas yra ypač svarbus, kai norite visus netinkamus nuokrypius rodyti kaip neigiamas sumas. Jei susumuotas arba apskaičiuotas skaičius turi klaidingą ženklą, norėdami pakeisti ženklą, eilutės langelyje **Įprastinis balansas** įveskite **C**.

## <a name="specify-a-row-modifier-cell"></a>Eilutės modifikatoriaus langelio nurodymas
Eilutės aprašo langelio **Eilutės modifikatorius** turinyje nepaisoma finansinių metų, laikotarpių ir kitos tos eilutės stulpelio apraše nurodytos informacijos. Pasirinktas modifikatorius taikomas kiekvienai eilutės sąskaitai. Kiekvieną eilutę galite keisti, naudodami vieną ar kelis iš šių modifikatorių tipų:

-   Sąskaitos modifikatoriai
-   Knygos kodo modifikatoriai
-   Sąskaitos ir operacijos atributai

### <a name="override-a-column-definition"></a>Stulpelio aprašo nepaisymas

1.  Ataskaitų dizaino įrankyje atidarykite norimą modifikuoti eilutės apibrėžimą.
2.  Eilutėje, kurioje norite nepaisyti stulpelio aprašo, dukart spustelėkite langelį **Eilutės modifikatorius**.
3.  Dialogo lango **Eilutės modifikatorius** lauke **Sąskaitos modifikatorius** pasirinkite pasirinktį. Pasirinkčių aprašymą rasite skyriuje „Sąskaitos modifikatoriai“.
4.  Lauke **Knygos kodo modifikatorius** pasirinkite naudotiną eilutės knygos kodą.
5.  Norėdami įtraukti įrašą, skirtą kiekvienam atributui, kuris turi būti įtrauktas su eilutės kodu, dalyje **Atributai** atlikite šiuos veiksmus:
    1.  Dukart spustelėkite langelį **Atributas** ir pasirinkite atributo pavadinimą. **Caution:** skaičiaus ženklą (\#) pakeiskite skaitine reikšme.
    2.  Dukart spustelėkite langelį **Nuo** ir įveskite pirmąją intervalo reikšmę.
    3.  Dukart spustelėkite langelį **Iki** ir įveskite paskutiniąją intervalo reikšmę.

6.  Spustelėkite **GERAI**.

### <a name="account-modifiers"></a>Sąskaitos modifikatoriai

Kai pasirenkate konkrečią sąskaitą, ataskaitų dizaino įrankis paprastai sujungia sąskaitą su finansiniais metais, laikotarpiais ir kita informacija, kurią nurodote stulpelio apraše. Kiekvienoje eilutėje galite naudoti skirtingą informaciją, pvz., skirtingus ataskaitinius laikotarpius. Toliau pateiktoje lentelėje rodomi galimi sąskaitos modifikatoriai. Skaičiaus ženklą (\#) pakeiskite reikšme, kuri lygi finansinių metų laikotarpių skaičiui arba yra už jį mažesnė.

| Sąskaitos modifikatorius | Kas spausdinama                                                                           |
|------------------|-------------------------------------------------------------------------------------------|
| /BB              | Sąskaitos pradžios balansas.                                                     |
| /\#              | Nurodyto laikotarpio balansas.                                                     |
| /-\#             | Laikotarpio, kuris yra \# laikotarpiais ankstesnis negu dabartinis laikotarpis, balansas.                  |
| /+\#             | Laikotarpio, kuris yra \# laikotarpiais vėlesnis negu dabartinis laikotarpis, balansas.                   |
| /C               | Dabartinio laikotarpio balansas.                                                       |
| /C-\#            | Laikotarpio, kuris yra \# laikotarpiais ankstesnis negu dabartinis laikotarpis, balansas.                  |
| /C+\#            | Laikotarpio, kuris yra \# laikotarpiais vėlesnis negu dabartinis laikotarpis, balansas.                   |
| /Y               | Dabartinio laikotarpio metų balansas iki nurodytos datos.                                      |
| /Y-\#            | Metų iki šios dienos balansas, skirtas laikotarpiui, kuris yra \# laikotarpiais ankstesnis negu dabartinis laikotarpis. |
| /Y+\#            | Metų iki šios dienos balansas, skirtas laikotarpiui, kuris yra \# laikotarpiais vėlesnis negu dabartinis laikotarpis.  |

### <a name="book-code-modifiers"></a>Knygos kodo modifikatoriai

Galite apriboti eilutę esamu knygos kodu. Stulpelio apraše turi būti bent vienas stulpelis **FD**, kuriame yra knygos kodas. 
> [!NOTE]
> Knygos kodo eilutės apribojimas panaikina tos eilutės stulpelio aprašo knygos kodo apribojimus.

### <a name="account-and-transaction-attributes"></a>Sąskaitos ir operacijos atributai

Kai kurios apskaitos sistemos palaiko finansinių duomenų sąskaitos atributus ir operacijos atributus. Šie atributai veikia kaip virtualieji sąskaitos segmentai ir juose gali būti papildoma informacija apie sąskaitą arba operaciją. Ši papildoma informacija gali būti sąskaitos ID, paketo ID, pašto indeksai ar kiti atributai. Jei jūsų apskaitos sistema palaiko atributus, eilutės apraše kaip eilutės modifikatorius galite naudoti sąskaitos atributus arba operacijos atributus. Informacijos apie tai, kaip nepaisyti eilutės informacijos rasite pirmiau pateiktame šio straipsnio skyriuje „Stulpelio aprašo nepaisymas“.

## <a name="specify-a-link-to-financial-dimensions-cell"></a>Langelio Saitas su finansinėmis dimensijomis nurodymas
Langelyje **Saitas su finansinėmis dimensijomis** pateikiamos nuorodos į finansinius duomenis, kurie turėtų būti įtraukti į kiekvieną ataskaitos eilutę. Šiame langelyje pateikiamos dimensijų reikšmės, bet vietoj segmento reikšmių arba dimensijų reikšmių arba papildomai prie jų galite nurodyti „Microsoft Excel“ darbalapio langelius. Norėdami atidaryti dialogo langą **Dimensijos**, dukart spustelėkite langelį **Saitas su finansinėmis dimensijomis**. 
> [!NOTE]
> Ataskaitų dizaino įrankis negali pasirinkti „Microsoft Dynamics“ ERP sistemos sąskaitų, dimensijų arba laukų, kuriuose yra vienas iš šių rezervuotų simbolių: &amp;, \*, \[, \], \{ arba \}. Norėdami nurodyti informaciją, kuri jau yra eilutės apibrėžime, įtraukite informaciją į langelį **Saitas su finansinėmis dimensijomis**. Norėdami įtraukti naujas eilutes, kurios susijusios su finansiniais duomenimis, naudokite dialogo langą **Įterpti eilutes iš**, kad ataskaitos apraše galėtumėte sukurti naujas eilutes. Stulpelio pavadinimas keičiasi, priklausomai nuo to, kaip stulpelis konfigūruojamas, kaip parodyta toliau pateikiamoje lentelėje.

| Pasirinktas saito tipas       | Saito stulpelio aprašas pasikeičia į šį |
|----------------------------------|----------------------------------------------------|
| Finansinės dimensijos             | Saitas su finansinėmis dimensijomis                       |
| Išorinis darbalapis               | Saitas su darbalapiu                                  |
| Finansinės dimensijos + darbalapis | Saitas su finansinėmis dimensijomis + darbalapis           |
| „Management Reporter“ ataskaita       | „Management Reporter“ ataskaita                         |

### <a name="specify-a-dimension-or-range"></a>Dimensijos ar intervalo nurodymas

1.  Ataskaitų dizaino įrankyje atidarykite norimą modifikuoti eilutės apibrėžimą.
2.  Dukart spustelėkite stulpelio **Saitas su finansinėmis dimensijomis** langelį.
3.  Dialogo lange **Dimensijos** dukart spustelėkite langelį po dimensijos pavadinimu.
4.  Dimensijos dialogo lange pasirinkite **Atskira ar intervalas**.
5.  Lauke **Nuo** įveskite pradžios dimensiją arba spustelėkite ![Naršyti](https://i-technet.sec.s-msft.com/dynimg/IC679490.gif "Naršyti") ir ieškokite galimų dimensijų. Norėdami įvesti dimensijų intervalą, lauke **Iki** įveskite pabaigos dimensiją.
6.  Spustelėkite **Gerai** ir uždarykite dimensijos dialogo langą. Dialogo lange **Dimensijos** rodoma atnaujinta dimensija arba intervalas.
7.  Spustelėkite **Gerai** ir uždarykite dialogo langą **Dimensijos**.

## <a name="display-zero-balance-accounts-in-a-row-definition"></a>Sąskaitų su nuliniu balansu rodymas eilutės apraše
Pagal numatytuosius nustatymus ataskaitų dizaino įrankis nespausdina jokių eilučių, kurios neturi atitinkamo finansinių duomenų balanso. Todėl galite sukurti vienos eilutės aprašą, kuriame būtų pateiktos visos fizinio segmento reikšmės arba visos dimensijų reikšmės, tada naudoti tą eilutės aprašą bet kuriame iš savo padalinių.

### <a name="modify-zero-balance-settings"></a>Nulinis balanso parametrų modifikavimas

1.  Ataskaitų dizaino įrankyje atidarykite norimą modifikuoti ataskaitos aprašą.
2.  Skirtuko **Parametrai** dalyje **Kitas formatavimas** pasirinkite ataskaitos apraše naudojamo eilutės aprašo pasirinktis.
3.  Meniu **Rinkmena** spustelėkite **Įrašyti**, kad įrašytumėte savo pakeitimus.

## <a name="use-wildcard-characters-and-ranges-in-a-row-definition"></a>Pakaitos simbolių ir intervalų naudojimas eilutės apraše
Dialogo lange **Dimensijos** įvedus fizinio segmento reikšmę pakaitos simbolį (? arba \*) galima įterpti bet kurioje segmento vietoje. Naudojantis ataskaitų dizaino įrankiu išrenkamos visos nurodytų vietų reikšmės neatsižvelgiant į pakaitos simbolius. Pvz., eilutės apraše yra tik fizinio segmento riekšmės, o fiziniai segmentai yra keturių simbolių. Jei eilutėje įvedate **6???**, nurodote, kad ataskaitų dizaino įrankis įtrauktų visas sąskaitas, kurių fizinio segmento reikšmė prasideda 6. Jei įvedate **6\***, rodomi tie patys rezultatai, bet į rezultatus taip pat įtraukiamos kintančio pločio reikšmės, pavyzdžiui, **60** ir **600000**. Ataskaitų dizaino įrankis pakeičia kiekvieną pakaitos simbolį (?) visomis galimomis reikšmėmis, įskaitant raides ir specialiuosius simbolius. Pvz., kai intervalas nuo **12?0** iki **12?4**, reikšmės **12?0** pakaitos simbolis pakeičiamas mažiausia simbolių rinkinio reikšme, o reikšmės **12?4** pakaitos simbolis pakeičiamas didžiausia simbolių rinkinio reikšme. 
> [!NOTE]
> Turėtumėte vengti naudoti pakaitos simbolius į intervalą patenkančiose pradžios ir pabaigos sąskaitose. Jei naudojate pakaitos simbolius pradžios arba pabaigos sąskaitoje, galite gauti nenumatytų rezultatų.

### <a name="single-segment-or-single-dimension-ranges"></a>Vieno segmento arba vienos dimensijos intervalai

Galite nurodyti segmentų reikšmių arba dimensijų reikšmių intervalą. Nurodyti intervalą naudinga todėl, kad jums nereikės atnaujinti eilutės aprašo kiekvieną kartą, kai į finansinius duomenis įtraukiama nauja segmento reikšmė arba dimensijos reikšmė. Pavyzdžiui, kai intervalas **+Sąskaita=\[6100:6900\]**, į eilutės sumą įtraukiamos reikšmės iš sąskaitų, kurių skaičiai nuo 6100 iki 6900. Kai intervale yra pakaitos simbolis (?), ataskaitų dizaino įrankis neįvertina intervalo pagal kiekvieną simbolį. Vietoj to nustatomos mažiausia ir didžiausia intervalo reikšmės, tada įtraukiamos pabaigos reikšmės ir tarp jų esančios reikšmės. 
> [!NOTE]
> Ataskaitų dizaino įrankis negali pasirinkti „Microsoft Dynamics“ ERP sistemos sąskaitų, dimensijų arba laukų, kuriuose yra vienas iš šių rezervuotų simbolių: &amp;, \*, \[, \], \{ arba \}. Ampersendą (&) įtraukti galite tik tada, kai naudodami dialogo langą **Įterpti eilutes iš dimensijų** automatiškai kuriate eilučių aprašus.

### <a name="multiple-segment-or-multiple-dimension-ranges"></a>Kelių segmentų arba kelių dimensijų intervalai

Įvedus intervalą, kai naudojamos kelių dimensijų reikšmių kombinacijos, intervalo palyginimas atliekamas ..\financial-dimensions\dimension-by-dimension pagrindu. Intervalo palyginimo negalima atlikti pagal kiekvieną simbolį arba pagal segmento dalį. Pavyzdžiui, intervalas  **+Sąskaita=\[5000:6000\], Padalinys=\[1000:2000\], Išlaidų centras=\[00\]** apima tik tas sąskaitas, kurios atitinka kiekvieną segmentą. Pagal šį scenarijų pirmosios dimensijos intervalas turi būti nuo 5000 iki 6000, antros dimensijos intervalas – nuo 1000 iki 2000, o paskutinė dimensija turi būti 00. Pavyzdžiui, **+Sąskaita=\[5100\], Padalinys=\[1100\], Išlaidų centras=\[01\]** į ataskaitą neįtraukiama, nes paskutinis segmentas nepatenka į nurodytą intervalą. Jei segmento reikšmėje yra tarpų, tą reikšmę rašykite laužtiniuose skliaustuose (\[ \]). Keturių simbolių segmentui tinkamos šios reikšmės: **\[ 234\], \[123 \], \[1 34\]**. Dimensijos reikšmės turi būti rašomos laužtiniuose skliaustuose (\[ \]), o ataskaitų dizaino įrankis parašo šiuos skliaustus už jus. Kai į kelių segmentų arba kelių dimensijų intervalą įtraukti pakaitos simboliai (? arba \*), nustatomos mažiausia ir didžiausia viso kelių segmentų arba kelių dimensijų intervalo reikšmės, o po to įtraukiamos pabaigos reikšmės ir tarp jų esančios reikšmės. Jei intervalas ilgas, pvz., visos sąskaitos nuo 40000 iki 99999, jei įmanoma, turite nurodyti tinkamą pradžios sąskaitą ir pabaigos sąskaitą. 
> [!NOTE]
> Ataskaitų dizaino įrankis negali pasirinkti „Microsoft Dynamics“ ERP sistemos sąskaitų, dimensijų arba laukų, kuriuose yra vienas iš šių rezervuotų simbolių: &amp;, \*, \[, \], \{ arba \}. Ampersendą (&) įtraukti galite tik tada, kai naudodami dialogo langą **Įterpti eilutes iš dimensijų** automatiškai kuriate eilučių aprašus.

## <a name="add-or-subtract-from-other-accounts-in-a-row-definition"></a>Pridėti prie kitų eilutės aprašo sąskaitų arba iš jų atimti
Norėdami sudėti vienos sąskaitos pinigines sumas ir kitos sąskaitos pinigines sumas arba jas vieną iš kitos atimti, galite naudoti langelio **Saitas su finansinėmis dimensijomis** pliuso ženklą (+) arba minuso ženklą (-). Toliau pateikiamoje lentelėje nurodomi priimtini formatai, naudojami sudedant arba atimant saitus su finansiniais duomenimis.

| Operacija  | Naudokite šį formatą  |
|------------|-----------------|
| Pridėkite dvi visiškai paruoštas sąskaitas.                                                       | +Padalinys=\[000\], Sąskaita=\[1205\], Skyrius=\[00\]+Padalinys=\[100\], Sąskaita=\[1205\], Skyrius=\[00\] |
| Pridėkite dvi segmentų reikšmes.                                                                 | +Sąskaita=\[1205\]+Sąskaita=\[1210\]                                                                           |
| Pridėkite segmentų reikšmes, kuriose yra pakaitos simbolių.                                    | +Sąskaita=\[120?+Sąskaita=\[11??\]                                                                             |
| Pridėkite visiškai paruoštų sąskaitų intervalą.                                                | +Padalinys=\[000:100\], Sąskaita=\[1205\], Skyrius=\[00\]                                                   |
| Pridėkite segmentų reikšmių intervalą.                                                          | +Sąskaita=\[1200:1205\]                                                                                       |
| Pridėkite segmentų reikšmių, kuriose yra pakaitos simbolių, intervalą.                         | +Sąskaita=\[120?:130?\]                                                                                       |
| Atimkite vieną visiškai paruoštą sąskaitą ir kitos visiškai paruoštos sąskaitos.              | +Padalinys=\[000\], Sąskaita=\[1205\], Skyrius=\[00\]-Padalinys=\[100\], Sąskaita=\[1205\], Skyrius=\[00\] |
| Atimkite vieną segmento reikšmę iš kitos segmento reikšmės.                                  | +Sąskaita=\[1205\]-Sąskaita=\[1210\]                                                                           |
| Atimkite segmento reikšmę, kurioje yra pakaitos simbolis iš kitos segmento reikšmės. | +Sąskaita=\[1200\]-Sąskaita=\[11??\]                                                                           |
| Atimkite visiškai paruoštų sąskaitų intervalą.                                           | -Padalinys=\[000:100\], Sąskaita=\[1200:1205\], Skyrius=\[00:01\]                                           |
| Atimkite segmentų reikšmių intervalą.                                                     | -Sąskaita=\[1200:1205\]                                                                                       |
| Atimkite segmentų reikšmių, kuriose yra pakaitos simbolių, intervalą.                    | -Sąskaita=\[120?:130?\]                                                                                       |

Nors galite keisti sąskaitas tiesiogiai, norėdami taikyti tinkamą formatavimą savo finansinių duomenų saitams, taip pat galite naudoti dialogo langą **Dimensijos**. Bet kurioje iš reikšmių gali būti pakaitos simbolių (? arba \*). Tačiau, taskaitų dizaino įrankis negali pasirinkti „Microsoft Dynamics“ ERP sistemos sąskaitų, dimensijų arba laukų, kuriuose yra vienas iš šių rezervuotų simbolių: &, \*, \[, \], { arba }. 
> [!NOTE]
> Norėdami atimti reikšmes, turite tas reikšmes rašyti skliausteliuose. Pavyzdžiui, jei įvedate **450?-(4509)**, rodoma **+Sąskaita=\[4509\]-Sąskaita=\[450?\]** ir jūs nurodote, kad ataskaitų dizaino įrankis atimtų 4509 sąskaitos segmento sumą iš bet kurio skaičiais 450 prasidedančio sąskaitos segmento sumos.

### <a name="add-or-subtract-accounts-from-other-accounts"></a>Sąskaitų pridėjimas prie kitų sąskaitų arba atėmimas iš kitų sąskaitų

1.  Ataskaitų dizaino įrankyje atidarykite norimą modifikuoti eilutės apibrėžimą.
2.  Atitinkamoje eilutėje dukart spustelėkite stulpelio **Saitas su finansinėmis dimensijomis** langelį.
3.  Pirmoje dialogo lango **Dimensijos** eilutėje atlikite šiuos veiksmus:
    1.  Pirmame lauke pasirinkite visas dimensijas (numatytasis parametras) arba spustelėkite, kad atidarytumėte dialogo langą **Dimensijų rinkinių tvarkymas**, kuriame galite kurti, modifikuoti, kopijuoti arba panaikinti rinkinį.
    2.  Dukart spustelėkite langelį **Operatorius +/-** ir pasirinkite pliuso (**+**) arba minuso (**-**) operatorių, kuris taikomas vienai ar kelioms eilutės dimensijų reikšmėms arba rinkiniams.
    3.  Atitinkamame dimensijų reikšmės stulpelyje dukart spustelėkite langelį, kad atidarytumėte dialogo langą **Dimensijos**, ir pasirinkite, ar ši dimensijos reikšmė yra atskira, skirta intervalui, dimensijų reikšmių rinkiniui, ar sumavimo sąskaitoms. Dialogo lango **Dimensijos** laukų aprašus galite rasti skyriuje „Dimensijos dialogo lango aprašymas“.
    4.  Stulpeliuose **Nuo** ir **Iki** įveskite segmentų reikšmes.

4.  Norėdami pridėti daugiau operacijų, kartokite 2–3 veiksmus.

> [!NOTE]
> Operatorius taikomas visoms eilutės dimensijoms.

## <a name="description-of-the-dimensions-dialog-box"></a>Dimensijų dialogo lango aprašymas
Toliau pateikiamoje lentelėje aprašomi dialogo lango **Dimensijos** laukai.

| Prekė                | Prekės/Paslaugos pavadinimas                                                                                                                                                                                                                                                                                             |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Atskira reikšmė arba intervalas | Lauke **Nuo** įveskite sąskaitos pavadinimą arba spustelėkite mygtuką **Naršyti** ![Naršyti](https://i-technet.sec.s-msft.com/dynimg/IC679490.gif "Naršyti") ir ieškokite sąskaitos. Norėdami pasirinkti intervalą, įveskite reikšmę arba ieškokite jos lauke **Iki**.                                             |
| Dimensijų reikšmių rinkinys | Lauke **Pavadinimas** įveskite dimensijų reikšmių rinkinio pavadinimą. Norėdami kurti, modifikuoti, kopijuoti arba panaikinti rinkinį, spustelėkite **Dimensijų reikšmių rinkinių tvarkymas**. Lauke **Formulė** pateikiama formulė iš langelio **Saitas su finansinėmis dimensijomis**, skirta šiam eilutės aprašo dimensijų reikšmių rinkiniui. |
| Sąskaitų sumavimas   | Lauke **Pavadinimas** įveskite sumavimo sąskaitų dimensiją arba ieškokite jos. Lauke **Formulė** pateikiama langelio **Saitas su finansinėmis dimensijomis** formulė, skirta ataskaitos aprašo sumavimo sąskaitai.                                                                       |

## <a name="add-dimension-value-sets-in-a-row-definition"></a>Dimensijų reikšmių rinkinių įtraukimas į eilutės aprašą
Dimensijų reikšmių rinkinys yra pavadinimą turinti dimensijų reikšmių grupė. Dimensijos reikšmių rinkinyje gali būti tik vienos dimensijos reikšmės, tačiau jūs galite naudoti dimensijos reikšmių rinkinį keliuose eilučių aprašuose, stulpelių aprašuose, ataskaitos medžio aprašuose ir ataskaitos aprašuose. Taip pat galite sujungti dimensijos reikšmių rinkinius ataskaitos apraše. Kai norint pakeisti savo finansinius duomenis reikia pakeisti dimensijos reikšmių rinkinį, galite atnaujinti dimensijos reikšmių rinkinio aprašą ir tas atnaujinimas taikomas visoms dimensijų vertės rinkinį naudojančioms sritims. Pavyzdžiui, jei dažnai nurodote su jūsų finansiniais duomenimis sietinų reikšmių intervalą, pvz., reikšmes nuo 5100 iki 5600, galite priskirti šį intervalą sąskaitų rinkiniui, kurio pavadinimas Pardavimas. Sukūrę dimensijos reikšmių rinkinį tą rinkinį galite pasirinkti kaip savo finansinių duomenų saitą. Kitas pavyzdys būtų, jei reikšmių intervalas nuo 5100 iki 5600 priskiriamas daliai Pardavimai, o 4175 priskiriamas daliai Nuolaidos, iš pardavmų sumų atimdami nuolaidos sumas galite nustatyti bendrąsias pardavimo sumas. Ši operacija pažymima **(5100:5600)-4175**.

### <a name="create-a-set-of-dimension-values"></a>Dimensijos reikšmių rinkinio kūrimas

1.  Ataskaitų dizaino įrankyje atidarykite norimą modifikuoti eilutę, stulpelį arba medžio aprašą.
2.  Meniu **Redaguoti** spustelėkite **Dimensijos reikšmių rinkinių tvarkymas**.
3.  Dialogo lango **Dimensijos reikšmių rinkinių tvarkymas** lauke **Dimensijos** pasirinkite kuriamo dimensijos reikšmių rinkinio tipą, tada spustelėkite **Naujas**.
4.  Dialogo lange **Naujas** įveskite rinkinio pavadinimą ir aprašą.
5.  Dukart spustelėkite stulpelio **Nuo** langelį.
6.  Dialogo lango **Sąskaita** sąraše pasirinkite sąskaitos pavadinimą arba ieškokite įrašo lauke **Paieška**. Tada spustelėkite **Gerai**.
7.  Norėdami sukurti tam operatoriui skirtą formulę, stulpelyje **Iki** pakartokite 5–6 veiksmus.
8.  Užbaigę formulę, spustelėkite **Gerai**.
9.  Dialogo lange **Dimensijų rinkinių tvarkymas** spustelėkite **Uždaryti**.

### <a name="update-a-set-of-dimension-values"></a>Dimensijos reikšmių rinkinio naujinimas

1.  Ataskaitų dizaino įrankyje atidarykite norimą modifikuoti eilutę, stulpelį arba medžio aprašą.
2.  Meniu **Redaguoti** spustelėkite **Dimensijos reikšmių rinkinių tvarkymas**.
3.  Dialogo lango **Dimensijos reikšmių rinkinių tvarkymas** lauke **Dimensijos** pasirinkite dimensijos tipą.
4.  Sąraše pasirinkite atnaujinamą dimensijos reikšmių rinkinį, tada spustelėkite **Modifikuoti**.
5.  Dialogo lange **Modifikuoti** modifikuokite į rinkinį įtraukiamas formulės reikšmes. 
    > [!NOTE]
    >  Jei pridedate naujų sąskaitų arba dimensijų, būtinai pakeiskite esamus dimensijos reikšmių rinkinius, kad būtų įtraukti pakeitimai.
6.  Dukart spustelėkite langelį ir pasirinkite atitinkamą operatorių, sąskaitą **Nuo** ir sąskaitą **Iki**.
7.  Norėdami uždaryti dialogo langą **Modifikuoti** ir įrašyti pakeitimus, spustelėkite **Gerai**.

### <a name="copy-a-dimension-set"></a>Dimensijų rinkinio kopijavimas

1.  Ataskaitų dizaino įrankyje atidarykite norimą modifikuoti eilutę, stulpelį arba medžio aprašą.
2.  Meniu **Redaguoti** spustelėkite **Dimensijos reikšmių rinkinių tvarkymas**.
3.  Dialogo lango **Dimensijos reikšmių rinkinių tvarkymas** lauke **Dimensijos** pasirinkite dimensijos tipą.
4.  Sąraše pasirinkite kopijuotiną rinkinį, tada spustelėkite **Įrašyti kaip**.
5.  Įveskite naują nukopijuoto rinkinio pavadinimą ir spustelėkite **Gerai**.

### <a name="delete-a-dimension-set"></a>Dimensijos rinkinio naikinimas

1.  Ataskaitų dizaino įrankyje atidarykite norimą modifikuoti eilutę, stulpelį arba medžio aprašą.
2.  Meniu **Redaguoti** spustelėkite **Dimensijos reikšmių rinkinių tvarkymas**.
3.  Dialogo lango **Dimensijos reikšmių rinkinių tvarkymas** lauke **Dimensijos** pasirinkite dimensijos tipą.
4.  Pasirinkite norimą naikinti rinkinį ir spustelėkite **Naikinti**. Spustelėkite **Taip**, jeigu norite visam laikui panaikinti dimensijos reikšmių rinkinį.


<a name="see-also"></a>Taip pat žiūrėkite
--------

[Finansinės ataskaitos](financial-reporting-intro.md)




