---
title: Eilutės apibrėžimo langelių keitimas
description: Šiame straipsnyje aprašoma informacija, reikalinga kiekvienam finansinės ataskaitos eilutės aprašo langeliui, ir paaiškina, kaip šią informaciją įvesti.
author: aprilolson
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.custom: 58881
ms.assetid: 0af492df-a84e-450c-8045-78ef1211abaf
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1c125369a5b2134759bf3650175276acf42b69e0
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802829"
---
# <a name="modify-row-definition-cells"></a>Eilutės apibrėžimo langelių keitimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma informacija, reikalinga kiekvienam finansinės ataskaitos eilutės aprašo langeliui, ir paaiškina, kaip šią informaciją įvesti.

## <a name="specify-a-row-code-in-a-row-definition"></a>Eilutės kodo nurodymas eilutės apibrėžime

Eilutės apibrėžimuose numeriai arba žymės eilutės kodo langelyje **identifikuoja** kiekvieną eilutės apibrėžimo eilutę. Galima nustatyti, kad eilutės kodas nurodytų skaičiavimų ir bendrųjų sumų duomenis.

### <a name="row-code-requirements"></a>Eilutės kodo reikalavimai

Eilutės kodą būtina nurodyti visoms eilutėms. Eilutės aprašyme galite maišyti skaitinius, raidinius-skaitinius ir išjungtus (tuščius) eilutės kodus. Eilutės kodas gali būti bet koks teigiamas sveikasis skaičius (mažesnis negu 100 000 000) arba tą eilutę identifikuojanti aprašomoji etiketė. Aprašomoji etiketė turi būti sudaryta laikantis šių taisyklių:

- Etiketė turi prasidėti abėcėlės raide (nuo a iki ž arba nuo A iki Ž) ir tai gali būti bet kokia iki 16 simbolių ilgio skaičių ir raidžių kombinacija.

    > [!NOTE]
    > Etiketėje gali būti pabraukimo simbolis (\_), bet specialiųjų simbolių naudoti neleidžiama.

- Etiketėje negalima naudoti nė vieno iš šių rezervuotų žodžių: AND, OR, IF, THEN, ELSE, PERIODS, TO, BASEROW, UNIT, NULL, CPO arba RPO.

Šie pavyzdžiai yra tinkami eilutės kodai:

- 320
- TL\_NET\_INCOME
- TL\_NET\_94

### <a name="change-a-row-code-in-a-row-definition"></a>Eilutės kodo keitimas eilutės apibrėžime

1. Ataskaitų konstruktoriuje spustelėkite **Eilučių apibrėžimai**, tada atidarykite eilutės apibrėžimą, kad jį keisite.
2. Atitinkamos eilutės stulpelyje Eilutės kodas įveskite naują **vertę** langelyje.

### <a name="reset-numeric-row-codes"></a>Skaitinių eilutės kodų nustatymas iš naujo

1. Ataskaitų konstruktoriuje spustelėkite **Eilučių apibrėžimai**, tada atidarykite eilutės apibrėžimą, kad jį keisite.
2. Meniu Redaguoti **spustelėkite** Eilučių numeravimą **iš naujo**.
3. Dialogo lange **Pernumeruoti** eilutes nurodykite naujas pradžios eilutės kodo vertes ir eilutės kodo padidėjimą. Galite iš naujo nustatyti skaitinių eilutės kodų reikšmes, kad jos būtų vienodo ilgio. Tačiau ataskaitų dizaino įrankis pernumeruoja tik tuos eilutės kodus, kurie prasideda skaičiais (pavyzdžiui, 130 arba 246). Raidėmis prasidedantys eilutės kodai (pavyzdžiui, INCOME\_93 arba TP0693) nepernumeruojami.

> [!NOTE]
> Kai pernumeruojate eilutės kodus, ataskaitų dizaino įrankis automatiškai atnaujina nuorodas **TOT** ir **CAL**. Pavyzdžiui, jei eilutėje **TOT** nurodomas intervalas, kuris prasideda eilutės kodu 100, o jūs pernumeruojate eilutes, pradėdami nuo 90, pradžios nuoroda **TOT** pasikeičia iš 100 į 90.

## <a name="add-a-description"></a>Aprašo įtraukimas
Aprašymo langelyje pateikiamas ataskaitos eilutėje, pvz., „Įplaukos“ arba „Grynosios pajamos“, nurodytų finansinių duomenų aprašymas. Langelio **Aprašymas** tekstas rodomas ataskaitoje tiksliai toks, kokį jį įvedate eilutės apibrėžime.

> [!NOTE]
> Ataskaitos aprašymo stulpelio plotis nustatomas stulpelio apibrėžime. Jei eilutės apibrėžimo stulpelio **Aprašymas** tekstas yra ilgas, patikrinkite stulpelio **DESC** plotį. Naudojant dialogo langą **Įterpti eilutes iš** stulpelio **Aprašymas** reikšmės yra finansinių duomenų segmentų reikšmės arba dimensijų reikšmės. Galite įterpti eilučių norėdami įtraukti aprašomąjį tekstą, pvz., skyriaus antraštę arba skyriaus sumą, ir įtraukti formatavimą, pvz., eilutę prieš sumos eilutę. Jei ataskaitoje pateikiamas ataskaitų medis, galite įtraukti papildomą tekstą, kuris apibrėžtas ataskaitų medžio ataskaitiniams vienetams. Taip pat galite apriboti papildomą tekstą tam tikru ataskaitiniu vienetu.

### <a name="add-the-description-for-a-line-on-a-report"></a>Ataskaitos eilutės aprašo įtraukimas

1. Ataskaitų konstruktoriuje spustelėkite **Eilučių apibrėžimai**, tada atidarykite eilutės apibrėžimą, kad jį keisite.
2. Pasirinkite langelį **Aprašymas**, tada įveskite ataskaitos eilutės pavadinimą.
3. Taikykite formatavimą.

### <a name="add-additional-text-from-a-reporting-tree-in-the-description"></a>Papildomo ataskaitų medžio teksto įtraukimas į aprašymą

1. Ataskaitų konstruktoriuje spustelėkite **Eilučių apibrėžimai**, tada atidarykite eilutės apibrėžimą, kad jį keisite.
2. Įveskite papildomo teksto kodą ir bet kurį kitą tekstą į atitinkamą langelį **Aprašymas**.
3. Taikykite formatavimą.

### <a name="limit-the-additional-text-to-a-specific-reporting-unit"></a>Papildomo teksto apribojimas tam tikru ataskaitiniu vienetu

1. Ataskaitų konstruktoriuje spustelėkite **Eilučių apibrėžimai**, tada atidarykite eilutės apibrėžimą, kad jį keisite.
2. Raskite eilutę, kurioje turėtų būti sukurtas papildomas tekstas, tada dukart spustelėkite stulpelio **Susijusios formulės / eilutės / vienetai** langelį.
3.  **Ataskaitų vieneto pasirinkimo** dialogo lange, ataskaitų **medžio lauke**, pasirinkite ataskaitų medį.
4. Lauke **Apribojimo ataskaitinio vieneto pasirinkimas** išplėskite arba sutraukite ataskaitų medį, tada pasirinkite ataskaitinį vienetą.

## <a name="add-a-format-code"></a>Formato kodo įtraukimas
Formato **kodo** langelis siūlo pasirinkti iš anksto suformatuotas tos eilutės turinio pasirinktis. Jei langelio **Formatas** kodas laukas tuščias, eilutė interpretuojama kaip finansinių duomenų informacijos eilutė.

> [!NOTE]
> Jei ataskaitoje yra ne sumą formatuojančių eilučių, susijusių su sumos eilutėmis, kurios buvo sulaikytos (pvz., dėl nulinio balanso), norėdami, kad nebūtų spausdinamos pavadinimo ir formato eilutės, galite naudoti stulpelį **Susijusios formulės / eilutės / vienetai**.

### <a name="add-a-format-code-to-a-report-row"></a>Formato kodo įtraukimas į ataskaitos eilutę

1. Ataskaitų konstruktoriuje spustelėkite **Eilučių apibrėžimai**, tada pasirinkite eilutės apibrėžimą, norimą modifikuoti.
2. Dukart spustelėkite langelį **Formato** kodas.
3. Sąraše pasirinkite formato kodą. Šioje lentelėje aprašomi formato kodai ir jų veiksmai.

    | Formato kodas                   | Formato kodo interpretavimas | Veiksmas |
    |-------------------------------|-----------------------------------|--------|
    | (Nėra)                        |                                   | Išvalo formato **kodo** langelį. |
    | IŠ VISO                           | Bendroji suma                             | Nurodoma eilutė, kuri stulpelyje **Susijusios formulės / eilutės / vienetai** naudoja matematinius ženklus. Bendrosioms sumoms naudojami paprasti ženklai, pavyzdžiui **+** arba **-**. |
    | KPL                           | Skaičiavimas                       | Nurodoma eilutė, kuri stulpelyje **Susijusios formulės / eilutės / vienetai** naudoja matematinius ženklus. Skaičiavimams naudojami sudėtingi ženklai, pavyzdžiui, **+**, **-**, **\**_, _*/** ir **IF / THEN / ELSE** sakiniai. |
    | DES                           | aprašymas                       | Nurodoma ataskaitos antraštės eilutė arba tuščia eilutė. |
    | LFT RGT CEN                   | Kairė Dešinė Centras                 | Ataskaitos puslapyje sulygiuojamas eilutės aprašymo tekstas, neatsižvelgiant į teksto išdėstymą stulpelio apraše. |
    | CBR                           | Pagrindinės eilutės keitimas                   | Nurodoma eilutė, kuri nustato pagrindinę stulpelio skaičiavimų eilutę. |
    | STULPELIS                        | Stulpelio lūžis                      | Ataskaitoje pradedamas naujas stulpelis. |
    | PUSLAPIS                          | Puslapio lūžis                        | Ataskaitoje pradedamas naujas puslapis. |
    | \---                          | Vienas pabraukimas                  | Po visais ataskaitos sumos stulpeliais nubrėžiama viena linija. |
    | ===                           | Du pabraukimai                  | Po visais ataskaitos sumos stulpeliais nubrėžiamos dvi linijos. |
    | LINE1                         | Plona linija                         | Per visą puslapį nubrėžiama viena plona linija. |
    | LINE2                         | Stora linija                        | Puslapyje nubrėžiama viena stora linija. |
    | LINE3                         | Punktyrinė linija                       | Per visą puslapį nubrėžiama viena punktyrinė linija. |
    | LINE4                         | Stora ir plona linijos          | Per visą puslapį nubrėžiamos dvi linijos. Viršutinė linija stora, o apatinė – plona. |
    | LINE5                         | Plona ir stora linijos          | Per visą puslapį nubrėžiamos dvi linijos. Viršutinė linija plona, o apatinė – stora. |
    | BXB BXC                       | Eilutė kvadrate                         | Aplink ataskaitų eilutes, kurios prasideda eilute **BXB** ir baigiasi eilute **BXC**, apibrėžiamas kvadratas. |
    | LIK.                           | Pastaba                            | Identifikuojama komentaro eilutė, kuri neturi būti spausdinama ataskaitoje. Pavyzdžiui, pastabos eilutėje gali būti paaiškinti naudojami formatavimo būdai. |
    | SORT ASORT SORTDESC ASORTDESC | Rūšiuoti                              | Rūšiuojamos išlaidos arba įplaukos, rūšiuojama faktinė arba biudžeto nuokrypio ataskaita pagal didžiausią nuokrypį arba rūšiuojami eilučių aprašymai abėcėlės tvarka. |

## <a name="specify-related-formulasrowsunits"></a>Susijusių formulių / eilučių / vienetų nurodymas
Susijusios **formulės / eilutės / vienetai naudojami** keliais tikslais. Priklausomai nuo eilutės tipo, langelis **Susijusios formulės / eilutės / vienetai** gali atlikti vieną iš šių funkcijų:

- Nustatyti eilutes, kurios turėtų būti įtraukiamos į skaičiavimą, kai naudojate formato kodą **TOT** arba **KPL**.
- Susieti formatavimo eilutę su sumos eilute, kad formatavimas būtų spausdinamas tik tada, kai spausdinama susijusi suma.
- Apriboti eilutę iki konkretaus ataskaitinio vieneto.
- Aprašyti pagrindinę skaičiavimų eilutę, kai naudojate formato kodą **BASEROW**.
- Nurodyti eilutes, kurios turi būti rūšiuojamos, kai naudojate vieną iš rūšiavimo formato kodų.

### <a name="use-a-row-total-in-a-row-definition"></a>Eilutės bendrosios sumos naudojimas eilutės apibrėžime

Naudokite eilutės bendrosios sumos formulę, norėdami pridėti arba atimti kitų eilučių sumas. Formulė, naudojama norint sukurti eilutės bendrąją sumą, gali būti sudaryta iš ženklų + ir -, kad būtų sujungiami atskiri eilučių kodai ir intervalai. Intervalai nurodomi dvitaškiu (:). Formulę gali sudaryti iki 1024 simbolių. Standartinės sumavimo formulės pavyzdys: 400+420+430+450+460LIABILITIES+EQUITY520:546520:546-LIABILITIES

### <a name="components-of-a-row-total-formula"></a>Eilučių bendrosios sumos formulės komponentai

Kuriant eilučių bendrosios sumos formulę būtina naudoti eilučių kodus, kad dabartiniame eilučių apraše būtų galima nurodyti, kurias eilutes reikia įtraukti, o kurias atimti, ir turite naudoti funkcijas, kuriomis nurodomas eilučių derinimas. Bendrosios sumos eilutes ir sumos eilutes galima derinti įvairiai.

> [!NOTE]
> Neįtraukiamos visos į diapazoną patenkančios bendrosios sumos eilutės. Norėdami sukurti bendrąją sumą, galite nurodyti eilučių intervalą. Jei pirmoji intervalo eilutė yra bendrosios sumos eilutė, ta eilutė įtraukiama į naują bendrąją sumą. Toliau pateikiamoje lentelėje aprašoma, kaip eilutės bendrosios sumos formulėse naudojami ženklai.

| Operatorius | Formulės pavyzdys | aprašymas                                                 |
|----------|-----------------|-------------------------------------------------------------|
| +        | 100+330         | Eilutėje 100 esanti suma pridedama prie eilutėje 330 esančios sumos.        |
| :        | 100:330         | Sudedamos visų eilučių (nuo 100 iki 330) bendrosios sumos.    |
| -        | 100-330         | Eilutėje 100 esanti suma atimama iš eilutėje 330 esančios sumos. |

### <a name="create-a-row-total"></a>Eilučių bendrosios sumos kūrimas

1. Ataskaitų konstruktoriuje spustelėkite **Eilučių apibrėžimai**, tada atidarykite eilutės apibrėžimą, kad jį keisite.
2. Dukart spustelėkite eilutės apibrėžimo **langelį** Formatas ir pasirinkite **TOT**.
3. Langelyje **Susijusios formulės / eilutės / vienetai** įveskite bendrosios sumos formulę.

### <a name="relate-a-format-row-to-an-amount-row"></a>Formato eilutės susiejimas su sumos eilute

Eilutės apibrėžimo stulpelio **Formatas atveju DES**, **LFT**, **RGT**, **RGT**, YRA ir **formato kodai,** **---** taikomi ne sumos eilutėms. **===**  Norėdami, kad šis formatavimas nebūtų spausdinamas, kai sulaikomos susijusios eilutės (pavyzdžiui, todėl, kad sumos eilutėse yra nulinių reikšmių arba nėra laikotarpio aktyvumo), turite susieti formato eilutes su atitinkamomis sumų eilutėmis. Ši funkcija naudinga, kai norite neleisti spausdinti antraščių arba formatavimo, kuris yra susijęs su tarpinėmis sumomis, kai nėra jokios spausdintinos laikotarpio informacijos.

> [!NOTE]
> Išvalydami parinktį rodyti eilutes be sumų taip pat galite neleisti spausdinti išsamių sumos eilučių. Ši pasirinktis yra ataskaitos aprašo skirtuke **Parametrai**. Pagal numatytuosius nustatymus, išsamios sąskaitos, kurių balansas lygus nuliui arba kurios neturi jokios laikotarpio veiklos, ataskaitose sulaikomos. Norėdami rodyti šias operacijos informacijos sąskaitas, pažymėkite ataskaitos aprašo skirtuko **Parametrai** žymės langelį **Rodyti eilutes be sumų**.

### <a name="relate-a-format-row-to-an-amount-row"></a>Formato eilutės susiejimas su sumos eilute

1. Ataskaitų konstruktoriuje spustelėkite **Eilutės apibrėžimai** ir pasirinkite eilutės apibrėžimą, norimą modifikuoti.
2. Formatavimo eilutės langelyje **Susijusius formulės / eilutės / vienetai** įveskite sulaikomos sumos eilutės kodą.

    > [!NOTE]
    > Kad sumos eilutė nebūtų rodoma, eilutės balansas turi būti 0 (nulis). Balansą turinti eilutė nesulaikoma.

3. Meniu **Rinkmena** spustelėkite **Įrašyti**.

### <a name="example-of-preventing-printing-of-rows"></a>Pavyzdys, kaip neleisti spausdinti eilučių

Toliau pateiktame pavyzdyje **vartotojas** nori neleisti spausdinti antraštės ir pabraukimo simboliais jos ataskaitos grynųjų pinigų eilutėje, nes nė vienoje iš grynųjų pinigų sąskaitų nebuvo veiklos. Todėl eilutės 220 (kuri, kaip nurodo formato kodas **---**, yra formatavimo eilutė) langelyje **Susijusios formulės / Eilutės / Vienetai** naudotojas įveda skaičių **250**, kuris yra jo norimos sulaikyti sumos eilutės kodas.

[![„RelatedRowsRowDefinition”.](./media/relatedrowsrowdefinition-1024x144.png)](./media/relatedrowsrowdefinition.png)

## <a name="select-the-base-row-for-a-column-calculation"></a>Pagrindinės stulpelio skaičiavimo eilutės pasirinkimas
Ryšių ataskaitos eilutės apibrėžime priskirkite vieną ar kelias pagrindines eilutes naudodami formato kodą **CBR** (keisti pagrindinę eilutę). Tada pagal stulpelio aprašo apskaičiavimą nurodoma pagrindinė eilutė. Toliau pateikiami keletas įprastų CBR skaičiavimų pavyzdžių.

- Bendrųjų įplaukų procentas, kadangi jis susijęs su atskirais įplaukų elementais
- Bendrųjų išlaidų procentas, kadangi jis susijęs su atskirais išlaidų elementais
- Bruto maržos procentas, kadangi jis susijęs su padalinio ar skyriaus informacija.

Eilutės apibrėžime nurodoma viena arba kelios pagrindinės eilutės, tada stulpelio apibrėžime nustatomas ryšys, kuriuo pagrindinė eilutė paskelbiama. Stulpelio formulėje naudojamas kodas yra **BASEROW**. Su kodu **BASEROW** naudojami šie pagrindiniai matematiniai veiksmai: dalinti, dauginti, pridėti ar atimti. Dažniausiai naudojamas veiksmas yra dalinti iš **BASEROW**, kai rezultatas rodomas procentais. Stulpelio skaičiavimuose, kurių formulėje naudojamas kodas **BASEROW**, susijusiems pagrindinių eilučių kodams naudojamas eilutės apibrėžimas. **CBR** eilutės apibūdinamos nurodant:

- **CBR** eilutės nespausdinamos baigtoje ataskaitoje.
- **CBR** formato kodas ir jo susijęs eilutės kodas rodomi virš eilutės arba skyriaus, kuriame rodomi susiję skaičiavimai.

Stulpelio apraše stulpelio tipas **CALC** rodo stulpelį, nustatantį formulę eilutėje **Formulė**. Ši formulė veikia šio ataskaitos stulpelio duomenis ir naudoja raktažodį Baserow, pagal kurį atliekami pagrindiniai eilutės formato kodų **CBR** skaičiavimai. Eilutės apibrėžimo formato kodas **CBR** nurodo stulpelių, kurie kiekvienoje ataskaitos eilutėje apskaičiuoja procentą arba padaugina iš pagrindinės eilutės, pagrindinę eilutę. Eilutės formate galite turėti kelis **CBR** formato kodus, pvz., vieną gryniesiems pardavimams, vieną bruto pardavimams ir vieną bendrosioms išlaidoms. Paprastai formato kodas **CBR** naudojamas norint sukurti su bendrosios sumos eilute lyginamų sąskaitų procentą. Pagrindinė eilutė naudojama atliekant visus skaičiavimus, kol nurodoma kita pagrindinė eilutė. Turite nurodyti pradžios **CBR** formato kodą ir pabaigos **CBR** formato kodą. Pvz., norėdami nurodyti išlaidas kaip grynojo pardavimo procentą, galite padalinti kiekvienos išlaidų eilutės reikšmę iš grynojo pardavimo eilutės reikšmės. Šiuo atveju grynojo pardavimo eilutė yra pagrindinė eilutė. Galite pateikti stulpelio apibrėžimą, kuriame nurodomi šių metų ir šių metų iki šios dienos rezultatai kartu su kiekvieno rezultato pagrindiniu procentu, kaip parodyta toliau pateiktame pavyzdyje. Pradėkite nuo išsamaus pajamų išrašo.

### <a name="select-the-base-row-in-a-row-definition-for-a-column-calculation"></a>Stulpelio skaičiavimui skirtos eilutės apibrėžimo pagrindinės eilutės pasirinkimas

1. Ataskaitų konstruktoriuje spustelėkite **Stulpelio apibrėžimai**, tada atidarykite pajamų išrašo stulpelio aprašą.
2. Įtraukite naują stulpelį į stulpelio aprašą ir nustatykite stulpelio tipą **CALC**.
3. Naujo stulpelio langelyje **Formulė** įveskite formulę **X/BASEROW**, kurioje **X** yra **FD** stulpelio tipas, kurio procentas rodomas.
4. Du kartus spustelėkite langelį **Formato / valiutos perrašymo** .
5.  **Sąrašo Formatas dialogo lange Perrašyti** pasirinkite **Procentas**, **tada** spustelėkite **Gerai**.
6. Norėdami įrašyti stulpelio apibrėžimą nauju pavadinimu, meniu **Failas** spustelėkite **Įrašyti kaip**. Prie dabartinio failo pavadinimo pridėkite **CBR** (pvz., **CUR\_YTD\_CBR**). Šis stulpelio apibrėžimas yra jūsų pagrindinės eilutės stulpelio apibrėžimas.
7. Ataskaitų konstruktoriuje spustelėkite **Eilutės apibrėžimai**, tada atidarykite eilutės apibrėžimą, kad modifikuodami jį naudodami pagrindinės eilutės skaičiavimą.
8. Virš eilutės, kurioje turėtų prasidėti pagrindinės eilutės skaičiavimas, įterpkite naują eilutę.
9. Dukart spustelėkite eilutės **apibrėžimo** langelį Formatas ir pasirinkite **CBR**.
10. Langelyje **Susijusios formulės / eilutės / vienetai** įveskite pagrindinės eilutės kodo numerį.

### <a name="example-of-base-row-calculation"></a>Pagrindinės eilutės skaičiavimo pavyzdys

Toliau pateikiamame eilutės apibrėžimo pavyzdyje eilutėje 100 rodoma, kad pagrindinė skaičiavimų eilutė yra eilutė 280.

[![Pagrindinės eilutės skaičiavimo pavyzdys.](./media/cbrrowdefinition.png)](./media/cbrrowdefinition.png)

Toliau pateikiamame stulpelio aprašo pavyzdyje skaičiavimams naudojamas **CBR** formato kodas. Stulpelio C skaičiavimas padalina ataskaitos stulpelio B reikšmę iš stulpelio B eilutės 280 reikšmės. Stulpelio B formato nepaisymas atspausdina skaičiavimo rezultatą procentais. Taip pat kiekviena stulpelio E suma yra stulpelio D suma grynojo pardavimo procentais.

[![Stulpelio aprašo pavyzdys.](./media/cbrcolumndefinition2.png)](./media/cbrcolumndefinition2.png)

Toliau pateikiamame pavyzdyje rodoma ataskaita, kuri gali būti sugeneruota pagal ankstesnius skaičiavimus.

[![Ataskaitos pavyzdys pagal ankstesnius skaičiavimo pavyzdžius.](./media/cbrreport-1024x272.png)](./media/cbrreport.png)

## <a name="select-a-sorting-code-for-a-row-definition"></a>Eilutės aprašo rūšiavimo kodo pasirinkimas
Rūšiavimo kodai rūšiuoja sąskaitas arba reikšmes, faktines arba biudžeto nuokrypio ataskaitas pagal didžiausią nuokrypį arba eilučių aprašymus abėcėlės tvarka. Galimi šie rikiavimo kodai:

- **SORT** – ataskaitos rūšiuojamos didėjančia tvarka, pagal nurodyto stulpelio reikšmes.
- **ASORT** – ataskaitos rūšiuojamos didėjančia tvarka, pagal nurodyto stulpelio reikšmių absoliučiąją reikšmę. Kitaip tariant, rūšiuojant reikšmes kiekvienos reikšmės ženklo nepaisoma. Šis formato kodas rikiuoja reikšmes pagal nuokrypio dydį, nepaisant to, ar nuokrypis teigiamas arba neigiamas.
- **SORTDESC** – ataskaitos rūšiuojamos mažėjančia tvarka, pagal nurodyto stulpelio reikšmes.
- **ASORTDESC** – ataskaitos rūšiuojamos mažėjančia tvarka, pagal nurodyto stulpelio reikšmių absoliučiąją reikšmę.

### <a name="select-a-sorting-code"></a>Rūšiavimo kodo pasirinkimas

1. Ataskaitų konstruktoriuje spustelėkite **Eilučių apibrėžimai**, tada atidarykite eilutės apibrėžimą, kad jį keisite.
2. Du kartus spustelėkite langelį **Formato kodas** ir pasirinkite rūšiavimo kodą.
3. Langelyje **Susijusios formulės / eilutės / vienetai** nurodykite rūšiuojamų eilučių kodų diapazoną. Norėdami nurodyti diapazoną, įveskite pirmą eilutės kodą, dvitaškį (:), tada paskutinį eilutės kodą. Pavyzdžiui, įveskite **160:490**, jeigu norite nurodyti, kad diapazonas yra nuo 160 eilutės iki 490 eilutės.
4. Langelyje **Stulpelio** apribojimas įveskite ataskaitos stulpelio, kurį norite naudoti rūšiuojant, raidę.

    > [!NOTE]
    > Rūšiavimui skaičiuoti naudokite tik sumos eilutes.

### <a name="examples-of-ascending-and-descending-column-values"></a>Didėjančių ir mažėjančių stulpelių reikšmių pavyzdžiai

Toliau pateiktame pavyzdyje ataskaitos D stulpelio vertės rūšiuojamos didėjančia tvarka, nuo 160 iki 490 eilutės. Be to, ataskaitos G stulpelio absoliučiosios vertės rūšiuojamos mažėjančia tvarka, nuo 610 iki 940 eilutės.

| Eilutės kodas | Aprašymas                             | Formato kodas | Susijusios formulės / eilutės / vienetai | Įprastas balansas | Stulpelio apribojimas | Susieti su finansinėmis dimensijomis |
|----------|-----------------------------------------|-------------|-----------------------------|----------------|--------------------|------------------------------|
| 100      | Surūšiuota pagal mėnesio nuokrypį, didėjančia tvarka       | DES         |                |                |                    |                              |
| 130      |                                        | SORT        | 160:490                     |                | D                  |                              |
| 160      | Pardavimas                                   |             |                             | C              |                    | 4100                         |
| 190      | Pardavimo grąžinimai                        |             |                             |                |                    | 4110                         |
|          | ...                             |             |                             |                |                    |                              |
| 490      | Palūkanų pajamos              |             |                             | C              |                    | 7000                         |
| 520      |                                     | DES         |                             |                |                    |                              |
| 550      | Surūšiuota pagal absoliutųjį nuokrypį nuo metų pradžios, mažėjančia tvarka | DES         |             |                |                    |                              |
| 580      |                              | ASORTDESC   | 610:940                     |                | Ž                  |                              |
| 610      | Pardavimas                     |             |                             | M              |                    | 4100                         |
| 640      | Pardavimo grąžinimai                |             |                             |                |                    | 4110                         |
|          | ...                       |             |                             |                |                    |                              |
| 940      | Palūkanų pajamos               |             |                             | „C”              |                    | 7000                         |


## <a name="specify-a-format-override-cell"></a>Nurodyti formato nepaisymo langelį
Formato **nepaisymo** langelis nurodo formatą, naudojamą eilutėje spausdinant ataskaitą. Šis formatavimas pakeičia formatavimą, nurodytą stulpelio apraše ir ataskaitos apraše. Pagal numatytuosius nustatymus, tuose aprašuose nurodytas formatavimas yra valiuta. Jei vienoje ataskaitos eilutėje nurodomas turto vienetų skaičius, pavyzdžiui, pastatų skaičius, o kitoje eilutėje nurodoma to turto piniginė vertė, galite nepaisyti valiutos formatavimo ir įvesti skaitinį eilutės formatavimą, kuriame nurodomas pastatų skaičius. Šią informaciją nurodykite dialogo lange **Formato nepaisymo** . Galimos pasirinktys priklauso nuo pasirinktos formato kategorijos. Dialogo lango srityje **Pavyzdys** rodomi formatų pavyzdžiai. Galimos šios formato kategorijos:

- Valiutos formatavimas
- Skaitinis formatavimas
- Procentinis formatavimas
- Pasirinktinis formatas

### <a name="override-cell-formatting"></a>Langelių formatavimo nepaisymas

1. Ataskaitų konstruktoriuje atidarykite eilutės apibrėžimą, norėdami modifikuoti.
2. Eilutėje, kurios formatas bus nepaisomas, du kartus spustelėkite langelį stulpelyje Formato **nepaisymo** .
3. Dialogo lange **Formato nepaisymo** pasirinkite formatavimo pasirinktis, kurios bus naudojamas tai ataskaitos eilutei.
4. Spustelėkite **GERAI**.

### <a name="currency-formatting"></a>Valiutos formatavimas

Valiutos formatavimas taikomas finansinei sumai ir apima valiutos simbolį. Galimos toliau nurodytos parinktys.

- **Valiutos simbolis** – ataskaitoje naudojamas valiutos simbolis. Ši reikšmė nepaiso įmonės informacijos nuostatos **Regiono pasirinktys**.
- **Neigiami skaičiai** – neigiami skaičiai gali būti su minuso ženklu (-), jie gali būti rodomi skliausteliuose, arba jie gali būti su trikampio ženklu (∆).
- **Po kablelio** – skaitmenų skaičius po dešimtainio skyriklio.
- **Nulinės vertės nepaisymo tekstas** – tekstas, kuris įtraukiamas į ataskaitą, kai suma lygi 0 (nuliui). Šis tekstas rodomas kaip paskutinė srities **Pavyzdys** eilutė.

    > [!NOTE]
    > Jei sulaikomas nulinių reikšmių spausdinimas arba nėra laikotarpio veiklos, šis tekstas panaikinamas.

### <a name="numeric-formatting"></a>Skaitinis formatavimas

Skaitinis formatavimas taikomas bet kokiai sumai ir neapima valiutos simbolio. Galimos toliau nurodytos pasirinktys:

- **Neigiami skaičiai** – neigiami skaičiai gali būti su minuso ženklu (-), jie gali būti rodomi skliausteliuose, arba jie gali būti su trikampio ženklu (∆).
- **Po kablelio** – skaitmenų skaičius po dešimtainio skyriklio.
- **Nulinės vertės nepaisymo tekstas** – tekstas, kuris įtraukiamas į ataskaitą, kai suma lygi 0 (nuliui). Šis tekstas rodomas kaip paskutinė srities **Pavyzdys** eilutė.

    > [!NOTE]
    > Jei sulaikomas nulinių reikšmių spausdinimas arba nėra laikotarpio veiklos, šis tekstas panaikinamas.

### <a name="percentage-formatting"></a>Procentinis formatavimas

Procentinis formatavimas apima procento ženklą (%). Galimos toliau nurodytos pasirinktys:

- **Neigiami skaičiai** – neigiami skaičiai gali būti su minuso ženklu (-), jie gali būti rodomi skliausteliuose, arba jie gali būti su trikampio ženklu (∆).
- **Po kablelio** – po dešimtainio skyriklio rodomų skaitmenų skaičius.
- **Nulinės vertės nepaisymo tekstas** – tekstas, kuris įtraukiamas į ataskaitą, kai suma lygi 0 (nuliui). Šis tekstas rodomas kaip paskutinė srities **Pavyzdys** eilutė.

    > [!NOTE]
    > Jei sulaikomas nulinių reikšmių spausdinimas arba nėra laikotarpio veiklos, šis tekstas panaikinamas.

### <a name="custom-formatting"></a>Pasirinktinis formatavimas

Naudokite pasirinktinio formatavimo kategoriją, norėdami sukurti pasirinktinio formato nepaisymą. Galimos toliau nurodytos pasirinktys:

- **Tipas** – pasirinktinis formatas.
- **Nulinės vertės nepaisymo tekstas** – tekstas, kuris įtraukiamas į ataskaitą, kai suma lygi 0 (nuliui). Šis tekstas rodomas kaip paskutinė srities **Pavyzdys** eilutė.

    > [!NOTE]
    > Jei sulaikomas nulinių reikšmių spausdinimas arba nėra laikotarpio veiklos, šis tekstas panaikinamas.

Dalyje Tipas turėtų būti nurodyta teigiama reikšmė, o po to – neigiama reikšmė. Paprastai įvedate panašų teigiamas ir neigiamas reikšmes atskiriantį formatą. Pavyzdžiui, norėdami nurodyti, kad teigiamos ir neigiamos reikšmės turi du skaitmenis po kablelio, bet neigiamos reikšmės rodomos skliausteliuose, įveskite **0.00;(0.00)**. Toliau pateikiamoje lentelėje rodomi pasirinktiniai formatai, kuriuos galite naudoti norėdami valdyti savo reikšmių formatą. Visi pavyzdžiai pradedami reikšme 1234.56.

| Formatuoti                         | Teigiama   | Neigiamas     | Nulis    |
|--------------------------------|------------|--------------|---------|
| 0                              | 1235       | –1235        | 0       |
| 0; 0                            | 1235       | 1235         | 0       |
| 0; (0); –                        | 1235       | 1235         | -       |
| \#,\#\#\#;(\#,\#\#\#);""       | 1 235      | (1,235)      | (tuščia) |
| \#,\#\#0.00;(\#,\#\#0.00);zero | 1 234,56   | (1 234,56)   | nulis    |
| 0.00%;(0.00%)                  | 123456.00% | (123456.00%) | 0.00%   |

## <a name="specify-a-normal-balance-cell"></a>Įprastinio balanso langelio nurodymas
Eilutės apibrėžimo langelis **Įprastinis balansas** valdo eilutės sumų ženklą. Norėdami atšaukti eilutės ženklą arba, jei įprastas sąskaitos balansas yra kreditas, **tos eilutės įprastame** balanso langelyje įveskite **C** . Naudojant ataskaitų dizaino įrankį pakeičiamas visų tos eilutės kredito balanso sąskaitų ženklas. Kai ataskaitų dizaineris konvertuoja šias sąskaitas, jis pašalina debeto/kredito charakteristikas iš visų sumų ir todėl bendrą sumą atlieka nesudėtingai. Pvz., norėdami apskaičiuoti grynąsias pajamas, iš pajamų atimkite išlaidas. Dažniausiai susumuotoms ir apskaičiuotoms eilutėms kodas **C** įtakos neturi. Tačiau XCR spausdinimo valdiklis **stulpelio apibrėžime atšaukia bet kurios eilutės,** kurioje yra C **įprasto balanso stulpelyje**, **ženklą.**  Šis formatavimas yra ypač svarbus, kai norite visus netinkamus nuokrypius rodyti kaip neigiamas sumas. Jei suskaičiuotas arba apskaičiuotas numeris turi netinkamą ženklą, **įveskite C**  **į** eilutės įprasto balanso langelį, kad ženklas būtų atšauktas.

## <a name="specify-a-row-modifier-cell"></a>Nurodyti eilutės modifikatoriaus langelį
Eilutės apibrėžimo **langelio Eilutės modifikatorius** turinys nepaiso finansinių metų, laikotarpių ir kitos informacijos, nurodytos tos eilutės stulpelio apibrėžime. Pasirinktas modifikatorius taikomas kiekvienai eilutės sąskaitai. Kiekvieną eilutę galite keisti, naudodami vieną ar kelis iš šių modifikatorių tipų:

- Sąskaitos modifikatoriai
- Knygos kodo modifikatoriai
- Sąskaitos ir operacijos atributai

### <a name="override-a-column-definition"></a>Stulpelio aprašo nepaisymas

1. Ataskaitų konstruktoriuje atidarykite eilutės apibrėžimą, norėdami modifikuoti.
2. Eilutėje, kurioje norite nepaisyti stulpelio apibrėžimo, du kartus spustelėkite langelį **Eilutės modifikatorius** .
3. Dialogo lange **Eilutės modifikatorius** pasirinkite pasirinktį lauke **Sąskaitos modifikatorius** . Pasirinkčių aprašymą rasite skyriuje „Sąskaitos modifikatoriai“.
4. Lauke **Knygos kodo modifikatorius** pasirinkite naudotiną eilutės knygos kodą.
5. Norėdami įtraukti įrašą, skirtą kiekvienam atributui, kuris turi būti įtrauktas su eilutės kodu, dalyje **Atributai** atlikite šiuos veiksmus:

    1. du kartus spustelėkite langelį **Atributas** ir pasirinkite atributo pavadinimą.

        > [!IMPORTANT]
        > Pakeiskite numerio ženklą (\#) skaitine verte.

    2. Dukart spustelėkite langelį **Nuo** ir įveskite pirmąją intervalo reikšmę.
    3. Dukart spustelėkite langelį **Iki** ir įveskite paskutiniąją intervalo reikšmę.

6. Spustelėkite **GERAI**.

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

### <a name="account-and-transaction-attributes"></a>Sąskaitų ir operacijų atributai

Kai kurios apskaitos sistemos palaiko finansinių duomenų sąskaitos atributus ir operacijos atributus. Šie atributai veikia kaip virtualieji sąskaitos segmentai ir juose gali būti papildoma informacija apie sąskaitą arba operaciją. Ši papildoma informacija gali būti sąskaitos ID, paketo ID, pašto indeksai ar kiti atributai. Jei jūsų apskaitos sistema palaiko atributus, eilutės apraše kaip eilutės modifikatorius galite naudoti sąskaitos atributus arba operacijos atributus. Informacijos apie tai, kaip nepaisyti eilutės informacijos rasite pirmiau pateiktame šio straipsnio skyriuje „Stulpelio aprašo nepaisymas“.

## <a name="specify-a-link-to-financial-dimensions-cell"></a>Nurodyti finansinių dimensijų langelio saitą
Finansinių **dimensijų langelio saitas** yra finansinių duomenų, kuriuos reikia įtraukti į kiekvieną ataskaitos eilutę, saitai. Šiame langelyje yra dimensijų reikšmės. Norėdami atidaryti dialogo **langą** Dimensijos, du kartus spustelėkite saitą su **finansinių dimensijų** langeliu.

> [!NOTE]
> Ataskaitos konstruktoriuje negalima pasirinkti sąskaitų, Microsoft Dynamics dimensijų arba laukų iš 365 finansų sistemos, kurioje yra bet kurie iš šių rezervuotų simbolių: &, \*, \[, \] {, arba }. Norėdami nurodyti eilutės, kuri jau yra eilutės apibrėžime, informaciją pridėkite prie saito **su finansinių dimensijų langeliu** . Norėdami įtraukti naujas eilutes, kurios susijusios su finansiniais duomenimis, naudokite dialogo langą **Įterpti eilutes iš**, kad ataskaitos apraše galėtumėte sukurti naujas eilutes. Stulpelio pavadinimas keičiasi, priklausomai nuo to, kaip stulpelis konfigūruojamas, kaip parodyta toliau pateikiamoje lentelėje.

| Pasirinktas saito tipas       | Saito stulpelio aprašas pasikeičia į šį |
|----------------------------------|----------------------------------------------------|
| Finansinės dimensijos             | Saitas su finansinėmis dimensijomis                       |
| Ataskaitos darbalapis                 | Finansinių ataskaitų ataskaita                         |

### <a name="specify-a-dimension-or-range"></a>Dimensijos ar diapazono nurodymas

1. Ataskaitų konstruktoriuje atidarykite eilutės apibrėžimą, norėdami modifikuoti.
2. Dukart spustelėkite langelį stulpelyje Susieti **su finansinėmis dimensijomis** .
3. Dialogo lange **Dimensijos** dukart spustelėkite dimensijos pavadinimo langelį.
4. Dimensijos dialogo lange pasirinkite **Atskira ar intervalas**.
5. Lauke **Iš** įveskite pradžios dimensiją arba spustelėkite ![Naršyti.](media/browse.gif "Naršyti") galimų dimensijų paieškai. Norėdami įvesti dimensijų intervalą, lauke **Iki** įveskite pabaigos dimensiją.
6. Spustelėkite **Gerai** ir uždarykite dimensijos dialogo langą. Dialogo lange **Dimensijos** rodoma atnaujinta dimensija arba intervalas.
7. Spustelėkite **Gerai** ir uždarykite dialogo langą **Dimensijos**.

## <a name="display-zero-balance-accounts-in-a-row-definition"></a>Sąskaitų su nuliniu balansu rodymas eilutės apraše
Pagal numatytuosius nustatymus ataskaitų dizaino įrankis nespausdina jokių eilučių, kurios neturi atitinkamo finansinių duomenų balanso. Todėl galite sukurti vienos eilutės aprašą, kuriame būtų pateiktos visos fizinio segmento reikšmės arba visos dimensijų reikšmės, tada naudoti tą eilutės aprašą bet kuriame iš savo padalinių.

### <a name="modify-zero-balance-settings"></a>Nulinis balanso parametrų modifikavimas

1. Ataskaitų konstruktoriuje atidarykite ataskaitos aprašą, norėdami modifikuoti.
2. Skirtuko **Parametrai** dalyje **Kitas formatavimas** pasirinkite ataskaitos apraše naudojamo eilutės aprašo pasirinktis.
3. Meniu **Rinkmena** spustelėkite **Įrašyti**, kad įrašytumėte savo pakeitimus.

## <a name="use-wildcard-characters-and-ranges-in-a-row-definition"></a>Pakaitos simbolių ir intervalų naudojimas eilutės apraše
Dialogo lange **Dimensijos** įvedus fizinio segmento reikšmę pakaitos simbolį (? arba \*) galima įterpti bet kurioje segmento vietoje. Naudojantis ataskaitų dizaino įrankiu išrenkamos visos nurodytų vietų reikšmės neatsižvelgiant į pakaitos simbolius. Pvz., eilutės apraše yra tik fizinio segmento riekšmės, o fiziniai segmentai yra keturių simbolių. Jei eilutėje įvedate **6???**, nurodote, kad ataskaitų dizaino įrankis įtrauktų visas sąskaitas, kurių fizinio segmento reikšmė prasideda 6. Jei įvedate **6\**_, rodomi tie patys rezultatai, bet į rezultatus taip pat įtraukiamos kintančio pločio reikšmės, pavyzdžiui, _* 60** ir **600000**. Ataskaitų dizaino įrankis pakeičia kiekvieną pakaitos simbolį (?) visomis galimomis reikšmėmis, įskaitant raides ir specialiuosius simbolius. Pvz., kai intervalas nuo **12?0** iki **12?4**, reikšmės **12?0** pakaitos simbolis pakeičiamas mažiausia simbolių rinkinio reikšme, o reikšmės **12?4** pakaitos simbolis pakeičiamas didžiausia simbolių rinkinio reikšme.

> [!NOTE]
> Turėtumėte vengti naudoti pakaitos simbolius į intervalą patenkančiose pradžios ir pabaigos sąskaitose. Jei naudojate pakaitos simbolius pradžios arba pabaigos sąskaitoje, galite gauti nenumatytų rezultatų.

### <a name="single-segment-or-single-dimension-ranges"></a>Vieno segmento arba vienos dimensijos intervalai

Galite nurodyti segmentų reikšmių arba dimensijų reikšmių intervalą. Nurodyti intervalą naudinga todėl, kad jums nereikės atnaujinti eilutės aprašo kiekvieną kartą, kai į finansinius duomenis įtraukiama nauja segmento reikšmė arba dimensijos reikšmė. Pavyzdžiui, kai intervalas **+Sąskaita=\[6100:6900\]**, į eilutės sumą įtraukiamos reikšmės iš sąskaitų, kurių skaičiai nuo 6100 iki 6900. Kai intervale yra pakaitos simbolis (?), ataskaitų dizaino įrankis neįvertina intervalo pagal kiekvieną simbolį. Vietoj to nustatomos mažiausia ir didžiausia intervalo reikšmės, tada įtraukiamos pabaigos reikšmės ir tarp jų esančios reikšmės.

> [!NOTE]
> Ataskaitos konstruktoriuje negalima pasirinkti sąskaitų, Microsoft Dynamics dimensijų arba laukų iš 365 finansų sistemos, kurioje yra bet kurie iš šių rezervuotų simbolių: &, \*, \[, \] {, arba }. Galite įtraukti ampersandą (>) tik tada, kai automatiškai kursite **eilučių apibrėžimus naudodami dialogo langą Įterpti eilutes iš** dimensijų.

### <a name="multiple-segment-or-multiple-dimension-ranges"></a>Kelių segmentų arba kelių dimensijų intervalai

Įvedus intervalą, kai naudojamos kelių dimensijų reikšmių kombinacijos, intervalo palyginimas atliekamas ..\\financial-dimensions\\dimension-by-dimension pagrindu. Intervalo palyginimo negalima atlikti pagal kiekvieną simbolį arba pagal segmento dalį. Pavyzdžiui, intervalas  **+Sąskaita=\[5000:6000\], Padalinys=\[1000:2000\], Išlaidų centras=\[00\]** apima tik tas sąskaitas, kurios atitinka kiekvieną segmentą. Pagal šį scenarijų pirmosios dimensijos intervalas turi būti nuo 5000 iki 6000, antros dimensijos intervalas – nuo 1000 iki 2000, o paskutinė dimensija turi būti 00. Pavyzdžiui, **+Sąskaita=\[5100\], Padalinys=\[1100\], Išlaidų centras=\[01\]** į ataskaitą neįtraukiama, nes paskutinis segmentas nepatenka į nurodytą intervalą. Jei segmento reikšmėje yra tarpų, tą reikšmę rašykite laužtiniuose skliaustuose (\[ \]). Keturių simbolių segmentui tinkamos šios reikšmės: **\[ 234\], \[123 \], \[1 34\]**. Dimensijos reikšmės turi būti rašomos laužtiniuose skliaustuose (\[ \]), o ataskaitų dizaino įrankis parašo šiuos skliaustus už jus. Kai į kelių segmentų arba kelių dimensijų intervalą įtraukti pakaitos simboliai (? arba \*), nustatomos mažiausia ir didžiausia viso kelių segmentų arba kelių dimensijų intervalo reikšmės, o po to įtraukiamos pabaigos reikšmės ir tarp jų esančios reikšmės. Jei intervalas ilgas, pvz., visos sąskaitos nuo 40000 iki 99999, jei įmanoma, turite nurodyti tinkamą pradžios sąskaitą ir pabaigos sąskaitą.

> [!NOTE] 
> Ataskaitos konstruktoriuje negalima pasirinkti sąskaitų, Microsoft Dynamics dimensijų arba laukų iš 365 finansų sistemos, kurioje yra bet kurie iš šių rezervuotų simbolių: &, \*, \[, \] {, arba }. Galite įtraukti ampersandą (>) tik tada, kai automatiškai kursite **eilučių apibrėžimus naudodami dialogo langą Įterpti eilutes iš** dimensijų.

## <a name="add-or-subtract-from-other-accounts-in-a-row-definition"></a>Pridėti prie kitų eilutės aprašo sąskaitų arba iš jų atimti
Norėdami sudėti vienos sąskaitos pinigines sumas ir kitos sąskaitos pinigines sumas arba jas vieną iš kitos atimti, galite naudoti langelio **Saitas su finansinėmis dimensijomis** pliuso ženklą (+) arba minuso ženklą (-). Toliau pateikiamoje lentelėje nurodomi priimtini formatai, naudojami sudedant arba atimant saitus su finansiniais duomenimis.

| Operacija                                            | Naudokite šį formatą                                                                                              |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Pridėkite dvi visiškai paruoštas sąskaitas.      | +Padalinys=\[000\], Sąskaita=\[1205\], Skyrius=\[00\]+Padalinys=\[100\], Sąskaita=\[1205\], Skyrius=\[00\] |
| Pridėkite dvi segmentų reikšmes.                    | +Sąskaita=\[1205\]+Sąskaita=\[1210\]                                                                           |
| Pridėkite segmentų reikšmes, kuriose yra pakaitos simbolių.  | +Sąskaita=\[120?+Sąskaita=\[11??\]                                                                     |
| Pridėkite visiškai paruoštų sąskaitų intervalą.              | +Padalinys=\[000:100\], Sąskaita=\[1205\], Skyrius=\[00\]                                           |
| Pridėkite segmentų reikšmių intervalą.                | +Sąskaita=\[1200:1205\]                                                                                       |
| Pridėkite segmentų reikšmių, kuriose yra pakaitos simbolių, intervalą.         | +Sąskaita=\[120?:130?\]                                                           |
| Atimkite vieną visiškai paruoštą sąskaitą ir kitos visiškai paruoštos sąskaitos.              | +Padalinys=\[000\], Sąskaita=\[1205\], Skyrius=\[00\]-Padalinys=\[100\], Sąskaita=\[1205\], Skyrius=\[00\] |
| Atimkite vieną segmento reikšmę iš kitos segmento reikšmės.          | +Sąskaita=\[1205\]-Sąskaita=\[1210\]                                                               |
| Atimkite segmento reikšmę, kurioje yra pakaitos simbolis iš kitos segmento reikšmės. | +Sąskaita=\[1200\]-Sąskaita=\[11??\]                                        |
| Atimkite visiškai paruoštų sąskaitų intervalą.                               | -Padalinys=\[000:100\], Sąskaita=\[1200:1205\], Skyrius=\[00:01\]                   |
| Atimkite segmentų reikšmių intervalą.                   | -Sąskaita=\[1200:1205\]                                                                                       |
| Atimkite segmentų reikšmių, kuriose yra pakaitos simbolių, intervalą.                    | -Sąskaita=\[120?:130?\]                                               |

Nors galite keisti sąskaitas tiesiogiai, norėdami taikyti tinkamą formatavimą savo finansinių duomenų saitams, taip pat galite naudoti dialogo langą **Dimensijos**. Bet kurioje iš reikšmių gali būti pakaitos simbolių (? arba \*). Tačiau ataskaitų dizaino įrankis negali pasirinkti „Microsoft Dynamics“ ERP sistemos sąskaitų, dimensijų arba laukų, kuriuose yra vienas iš šių rezervuotų simbolių: &; \*, \[, \], {, arba }.

> [!NOTE]
> Norėdami atimti vertes, turite jas apskliausti. Pavyzdžiui, jei įvedate **450?-(4509)**, rodoma **+Sąskaita=\[4509\]-Sąskaita=\[450?\]** ir jūs nurodote, kad ataskaitų dizaino įrankis atimtų 4509 sąskaitos segmento sumą iš bet kurio skaičiais 450 prasidedančio sąskaitos segmento sumos.

### <a name="add-or-subtract-accounts-from-other-accounts"></a>Sąskaitų pridėjimas prie kitų sąskaitų arba atėmimas iš kitų sąskaitų

1. Ataskaitų konstruktoriuje atidarykite eilutės apibrėžimą, norėdami modifikuoti.
2. Atitinkamos eilutės stulpelyje Saitas su finansinėmis dimensijomis **du kartus spustelėkite langelį** .
3. Pirmoje dialogo lango **Dimensijos** eilutėje atlikite šiuos veiksmus:

    1. Pirmame lauke pasirinkite visas dimensijas (numatytąsias) **arba** spustelėkite, kad atidarytumėte dialogo langą Tvarkyti dimensijų rinkinius, kur galėsite kurti, modifikuoti, kopijuoti ar naikinti rinkinį.
    2. Dukart spustelėkite langelį **Operatorius +/-** ir pasirinkite pliuso (**+**) arba minuso (**-**) operatorių, kuris taikomas vienai ar kelioms eilutės dimensijų reikšmėms arba rinkiniams.
    3. Atitinkamame dimensijų reikšmės stulpelyje dukart spustelėkite langelį, kad atidarytumėte dialogo langą **Dimensijos**, ir pasirinkite, ar ši dimensijos reikšmė yra atskira, skirta intervalui, dimensijų reikšmių rinkiniui, ar sumavimo sąskaitoms. Dialogo lango **Dimensijos** laukų aprašus galite rasti skyriuje „Dimensijos dialogo lango aprašymas“.
    4. Stulpeliuose **Nuo** ir **Iki** įveskite segmentų reikšmes.

4. Norėdami pridėti daugiau operacijų, kartokite 2–3 veiksmus.

> [!NOTE]
> Operatorius taikomas visoms eilutės dimensijoms.

## <a name="description-of-the-dimensions-dialog-box"></a>Dimensijų dialogo lango aprašymas
Toliau pateikiamoje lentelėje aprašomi dialogo lango **Dimensijos** laukai.

| Prekė                | Prekės/Paslaugos pavadinimas |
|---------------------|-------------|
| Atskira reikšmė arba intervalas | Lauke **Nuo** įveskite sąskaitos pavadinimą arba spustelėkite **Naršyti** mygtuką ![Naršyti.](media/browse.gif "Naršyti") sąskaitos naršymui. Norėdami pasirinkti intervalą, įveskite reikšmę arba ieškokite jos lauke **Iki**. |
| Dimensijų reikšmių rinkinys | Lauke **Pavadinimas** įveskite dimensijų reikšmių rinkinio pavadinimą. Norėdami kurti, modifikuoti, kopijuoti arba panaikinti rinkinį, spustelėkite **Dimensijų reikšmių rinkinių tvarkymas**. Formulės **laukas** užpildomas formule iš saito **su šios dimensijos** reikšmės, nustatytos eilutės apibrėžime, finansinių dimensijų langeliu. |
| Sąskaitų sumavimas   | Lauke **Pavadinimas** įveskite sumavimo sąskaitų dimensiją arba ieškokite jos. Formulės **lauke** automatiškai įvedama formulė, pateikiama **ataskaitos apraše,** kai yra nuoroda į finansinių dimensijų elementą šiai sumavimo sąskaitai. |

## <a name="add-dimension-value-sets-in-a-row-definition"></a>Dimensijų reikšmių rinkinių įtraukimas į eilutės aprašą
Dimensijų reikšmių rinkinys yra pavadinimą turinti dimensijų reikšmių grupė. Dimensijos reikšmių rinkinyje gali būti tik vienos dimensijos reikšmės, tačiau jūs galite naudoti dimensijos reikšmių rinkinį keliuose eilučių aprašuose, stulpelių aprašuose, ataskaitos medžio aprašuose ir ataskaitos aprašuose. Taip pat galite sujungti dimensijos reikšmių rinkinius ataskaitos apraše. Kai norint pakeisti savo finansinius duomenis reikia pakeisti dimensijos reikšmių rinkinį, galite atnaujinti dimensijos reikšmių rinkinio aprašą ir tas atnaujinimas taikomas visoms dimensijų vertės rinkinį naudojančioms sritims. Pavyzdžiui, jei dažnai nurodote su jūsų finansiniais duomenimis sietinų reikšmių intervalą, pvz., reikšmes nuo 5100 iki 5600, galite priskirti šį intervalą sąskaitų rinkiniui, kurio pavadinimas Pardavimas. Sukūrę dimensijos verčių rinkinį, galite pasirinkti šį rinkinį kaip finansinių duomenų saitą. Kitas pavyzdys: jei reikšmių diapazonas nuo 5100 iki 5600 priskirtas rinkiniui Pardavimas, o reikšmė 4175 priskirta rinkiniui Nuolaidos, bendrą pardavimo sumą galite nustatyti iš pardavimo reikšmės atėmę nuolaidų reikšmę. Ši operacija pažymima **(5100:5600)-4175**.

### <a name="create-a-set-of-dimension-values"></a>Dimensijos reikšmių rinkinio kūrimas

1. Ataskaitų konstruktoriuje atidarykite eilutę, stulpelį arba medžio aprašą, kad jį būtų galima modifikuoti.
2. Meniu Redaguoti **spustelėkite** Tvarkyti dimensijų **verčių rinkinius**.
3.  **Dimensijos verčių rinkinio valdymo** dialogo lange lauke **Dimensija** pasirinkite norimą kurti dimensijos vertės tipą, tada spustelėkite **Naujas**.
4. Dialogo lange **Naujas** įveskite rinkinio pavadinimą ir aprašą.
5. Dukart spustelėkite stulpelio **Nuo** langelį.
6. Dialogo lango **Sąskaita** sąraše pasirinkite sąskaitos pavadinimą arba ieškokite įrašo lauke **Paieška**. Tada spustelėkite **Gerai**.
7. Norėdami sukurti tam operatoriui skirtą formulę, stulpelyje **Iki** pakartokite 5–6 veiksmus.
8. Užbaigę formulę, spustelėkite **Gerai**.
9. Dialogo lange **Valdyti dimensijų rinkinius** spustelėkite **Uždaryti**.

### <a name="update-a-set-of-dimension-values"></a>Dimensijos verčių rinkinio naujinimas

1. Ataskaitų konstruktoriuje atidarykite eilutę, stulpelį arba medžio aprašą, kad jį būtų galima modifikuoti.
2. Meniu Redaguoti **spustelėkite** Tvarkyti dimensijų **verčių rinkinius**.
3.  **Dimensijos verčių rinkinio dialogo** lange, lauke **Dimensija**, pasirinkite dimensijos tipą.
4. Sąraše pasirinkite atnaujinamą dimensijos reikšmių rinkinį, tada spustelėkite **Modifikuoti**.
5. Dialogo lange **Modifikuoti** modifikuokite į rinkinį įtraukiamas formulės reikšmes.

    > [!NOTE]
    > Jei pridedate naujų sąskaitų arba dimensijų, būtinai pakeiskite esamus dimensijos reikšmių rinkinius, kad būtų įtraukti pakeitimai.

6. Dukart spustelėkite langelį ir pasirinkite atitinkamą operatorių, sąskaitą **Nuo** ir sąskaitą **Iki**.
7. Norėdami uždaryti dialogo langą **Modifikuoti** ir įrašyti pakeitimus, spustelėkite **Gerai**.

### <a name="copy-a-dimension-set"></a>Dimensijų rinkinio kopijavimas

1. Ataskaitų konstruktoriuje atidarykite eilutę, stulpelį arba medžio aprašą, kad jį būtų galima modifikuoti.
2. Meniu Redaguoti **spustelėkite** Tvarkyti dimensijų **verčių rinkinius**.
3.  **Dimensijos verčių rinkinio dialogo** lange, lauke **Dimensija**, pasirinkite dimensijos tipą.
4. Sąraše pasirinkite kopijavimo rinkinį ir spustelėkite Įrašyti **kaip**.
5. Įveskite naują nukopijuoto rinkinio pavadinimą ir spustelėkite **Gerai**.

### <a name="delete-a-dimension-set"></a>Dimensijų rinkinio naikinimas

1. Ataskaitų konstruktoriuje atidarykite eilutę, stulpelį arba medžio aprašą, kad jį būtų galima modifikuoti.
2. Meniu Redaguoti **spustelėkite** Tvarkyti dimensijų **verčių rinkinius**.
3.  **Dimensijos verčių rinkinio dialogo** lange, lauke **Dimensija**, pasirinkite dimensijos tipą.
4. Pasirinkite norimą naikinti rinkinį ir spustelėkite **Naikinti**. Spustelėkite **Taip**, kad visam laikui panaikintumėte dimensijos verčių rinkinį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Finansinės ataskaitos](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
