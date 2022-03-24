---
title: Palaiko parametruotus ER duomenų modelių skambučius
description: Šioje temoje paaiškinama, kaip įdiegti parametruotus elektroninių ataskaitų (ER) duomenų modelių skambučius.
author: NickSelin
ms.date: 03/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula, ERDataModelDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 968b0769607e9fdbed57c25b727ed44988a92913
ms.sourcegitcommit: 399d0d3f8e2ebb81b6b9d640365ebe182690bab2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/15/2022
ms.locfileid: "8419516"
---
# <a name="support-parameterized-calls-of-er-data-models"></a>Palaiko parametruotus ER duomenų modelių skambučius

[!include [banner](../includes/banner.md)]

Norėdami generuoti verslo dokumentus, sukonfigūruokite [elektroninių ataskaitų (ER)](general-electronic-reporting.md) sprendimą, kuriame yra šie ER komponentai:

- **[Formatas](er-overview-components.md#format-component)** – šis komponentas nurodo verslo dokumento struktūrą.
- **Formato konvertavimas** – šis komponentas kontroliuoja, kaip verslo dokumentas užpildomas vykdyklėje.
- **[Modelio susiejimas](er-overview-components.md#model-mapping-component)** – šis komponentas nurodo, kokie duomenys iš programos pereis į formato konvertavimą.
- **[Duomenų modelis](er-overview-components.md#data-model-component)** – šis komponentas perduoda informaciją tarp atskirų komponentų.

Kai vykdote ER formatą, kiekvienas formato elementas paleidžiamas, pradedant nuo šakninio formato elemento. Kai vykdomas formato elementas turi [susiejimą](general-electronic-reporting.md#configuring-data-model-mappings-for-outgoing-documents) su duomenų šaltiniu, duomenų šaltinis paleidžiamas, kad būtų pateikti numatomi duomenys, ir naudojamas formato elementui įrašyti. Iškvietus modelio *tipo* duomenų šaltinį, atitinkamas modelio susiejimas iškvieiamas norint ištraukti duomenis iš programos, remiantis modelio susiejimo parametrais.

Anksčiau šie modelio susiejimo skambučiai nepavyko nustatyti, kad jie būtų priklausomi nuo paleismo formato logikos. Palaikomas tik šis duomenų srautas.

<table>
<tbody>
<tr align="center">
<td>
<b>Formatas</b><br>
Formatų&nbsp; lėt.:<br>
„&nbsp;“
</td>
<td>
<i>Susiejimas</i><br>
&gt;&nbsp; Prašymą&nbsp;&gt;<br>
&lt;&nbsp;vertė&nbsp;&lt;
</td>
<td><b>Formatavimo&nbsp; atvaizdavimas</b><br>
Duomenų šaltinis<br>
„&nbsp;“
</td>
<td>
<i>Datamodel&nbsp;</i><br>
&gt;&nbsp; Prašymą&nbsp;&gt;<br>
&lt;&nbsp;vertė&nbsp;&lt;
</td>
<td>
<b>Modelio&nbsp; struktūravimas</b><br>
Duomenų&nbsp; šaltinis<br>
„&nbsp;“
</td>
<td>
<i>Susiejimas</i><br>
&gt;&nbsp; Prašymą&nbsp;&gt;<br>
&lt;&nbsp;vertė&nbsp;&lt;
</td>
<td>
<b>Lentelė</b><br>
Įrašyti<br>
Laukas
</td>
</tr>
</tbody>
</table>

Tačiau 10.0.15 ir vėlesnėje versijoje galite konfigūruoti duomenų modelio laukus, kurie gali būti iškviesti tik tada, kai pateiktos sukonfigūruotų parametrų vertės. Kai toks laukas konfigūruojamas ir iškvieuojamas iš formato komponento, reikiami parametrai turi būti pateikiami formato susiejimu kaip iškvietimo argumentai. Tokiais atvejais argumentų vertes galima nurodyti remiantis konkretaus formato vertėmis. Todėl duomenų modelio skambučiams **galite naudoti dinaminį** vykdyklės parametrų naudojimą, kad būtų galima palaikyti šį duomenų srautą.

<table>
<tbody>
<tr align="center">
<td>
<b>Formatas</b><br>
Formatelement1&nbsp;&nbsp;<br>
<br>
Formatelement2&nbsp;&nbsp;<br>
„&nbsp;“<br>
„&nbsp;“
</td>
<td>
<i>Susiejimas</i><br>
&gt;&nbsp; 1 užklausa&nbsp;&nbsp;&gt;<br>
&lt;&nbsp; 1&nbsp; vertė&nbsp;&lt;<br>
&gt;&nbsp; 2 užklausa&nbsp;&nbsp;&gt;<br>
&lt;&nbsp; reikšmę3&nbsp;&nbsp;&lt;<br>
„&nbsp;“
</td>
<td>
<b>Formatmapping&nbsp;</b><br>
&nbsp; 1 duomenų&nbsp; šaltinis<br>
„&nbsp;“<br>
<b>value2=Betk(value1)</b><br>
„&nbsp;“<br>
„&nbsp;“
</td>
<td>
<i>Datamodel&nbsp;</i><br>
&gt;&nbsp; 1 laukas&nbsp;&gt;<br>
&lt;&nbsp; 1&nbsp; vertė&nbsp;&lt;<br>
<b>&gt;&nbsp; field2(value2)&nbsp;&gt;</b><br>
&lt;&nbsp; reikšmę3&nbsp;&nbsp;&lt;<br>
„&nbsp;“
</td>
<td>
<b>Modelio&nbsp; struktūravimas</b><br>
&nbsp; 1 duomenų&nbsp; šaltinis<br>
<br>
&nbsp; 2 duomenų&nbsp; šaltinis<br>
„&nbsp;“<br>
„&nbsp;“
</td>
<td>
<i>Susiejimas</i><br>
&gt;&nbsp; 1 užklausa&nbsp;&nbsp;&gt;<br>
&lt;&nbsp; 1&nbsp; vertė&nbsp;&lt;<br>
&gt;&nbsp; 2 užklausa&nbsp;&nbsp;&gt;<br>
&lt;&nbsp; reikšmę3&nbsp;&nbsp;&lt;<br>
„&nbsp;“
</td>
<td>
<b>Table1&nbsp;</b><br>
&nbsp; 1 įrašas<br>
&nbsp; 1 laukas<br>
<b>Table2&nbsp;</b><br>
&nbsp; 2 įrašas<br>
&nbsp; 2 laukas
</td>
</tr>
</tbody>
</table>

Nauja funkcija leidžia parametrizuoti iškvietimą į bet kurį įrašo arba įrašų sąrašo tipo [*duomenų*](er-formula-supported-data-types-composite.md#record)[*modelio lauką*](er-formula-supported-data-types-composite.md#record-list). Duomenų modelio lauko parametrai palaiko šiuos duomenų tipus:

- [Bulio logika](er-formula-supported-data-types-primitive.md#boolean)
- [Konteineris](er-formula-supported-data-types-composite.md#container)
- [Data](er-formula-supported-data-types-primitive.md#date)
- [DateTime](er-formula-supported-data-types-primitive.md#datetime)
- [GUID](er-formula-supported-data-types-primitive.md#guid)
- [Int64](er-formula-supported-data-types-primitive.md#int64)
- [Sveikasis skaičius](er-formula-supported-data-types-primitive.md#integer)
- [Tikrasis](er-formula-supported-data-types-primitive.md#real)
- [Eilutė](er-formula-supported-data-types-primitive.md#string)

Galite nurodyti kiekvieną duomenų modelio lauko parametrą, kuriam argumentas gali būti pateikiamas kaip viena apibrėžto duomenų tipo vertė, ir šių [*·*](er-formula-supported-data-types-composite.md#record-list) verčių sąrašą.

> [!NOTE]
> Duomenų modelio lauko parametro numatytoji vertė nepalaikoma. Jei prie duomenų modelio lauko pridedate parametrą ir to duomenų modelio versija jau buvo išleista ir paskelbta, [turite](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) iš naujo sukurti visus atitinkamus šio modelio susiejimus ir formatus į naują šio modelio versiją, nes šis duomenų modelio keitimas nesuderinamas su ankstesnėmis versijomis.

Galite konfigūruoti parametrizuotus duomenų modelio laukus, kad jie būtų konkretus modelio susiejimo skambučių formatui. Šis būdas gali padėti sumažinti modelių susiejimų, kuriuos reikia sukonfigūruoti pagal daugelį vieno duomenų modelio formatų, skaičių. Taip pat galite naudoti šį būdą, norėdami padidinti formatų vykdymo efektyvumą ir sumažinti laiką, reikalingą verslo dokumentams generuoti. Norėdami sužinoti daugiau apie šią funkciją, atlikite šioje temoje esantį pavyzdį.

## <a name="example-use-parameterized-calls-of-er-data-models"></a>Pavyzdys: Naudoti parametrizuotus ER duomenų modelių iškmes parametrus

Toliau pateikiamais veiksmais paaiškinama, kaip vartotojas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmenyje gali sukurti ER sprendimą, kuriame yra duomenų modelis, modelio išdėstymas ir formato ER komponentas, sukonfigūruotas iškviesti modelio konvertavimą iš formato, pateikiant iškvietimo argumentą, kurio vertė apskaičiuojama apdorojimo laiku naudojant paleisto formato formulę. 

Šie žingsniai gali būti užbaigti **DEMF** bendrovėje. Kodo modifikacijų nereikia. 

Šiame pavyzdyje jūs sukursite reikalingas [Litware](general-electronic-reporting.md#Configuration), Inc.**pavyzdžio įmonės ER** konfigūracijas. Įsitikinkite, kad **Litware, Inc.** (`http://www.litware.com`) PAVYZDŽIO įmonės konfigūracijos teikėjas yra įtrauktas į ER sistemos sąrašą ir kad jis pažymėtas kaip **Aktyvus**. Jei šio konfigūracijos teikėjo nėra arba **jei** jis nepažymėtas kaip Aktyvus, [atlikite konfigūracijos teikėjo kūrimo veiksmus ir pažymėkite jį kaip aktyvų](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="business-scenario"></a>Verslo scenarijus

Yra ER sprendimas, kuriame yra formatas, kurį galite naudoti elektroniniam dokumentui generuoti audito tikslais. Šiame formate yra mokesčių operacijos, susijusios su pardavimo užsakymais ir pirkimo užsakymais, ir kurių išsami informacija, pvz., operacijos data ir mokesčio vertė. Kaip ir naujais finansiniais metais pakeista šio dokumento struktūra. Dabar turite pateikti išplėstinį dokumentą, kuriame pateikta papildoma visų šalių (klientų ir tiekėjų), kurių operacijos pateikiamos sugeneruotose ataskaitose, informacija (pavadinimai). Todėl turite modifikuoti savo ER sprendimą, kad jis sugeneruotų dokumentus, atitinkančius šį naują reikalavimą.

### <a name="configure-the-er-framework"></a>ER sistemos konfigūracija

Atlikite veiksmus, aprašytus skyriuje [Konfigūruoti ER sistemą](er-quick-start2-customize-report.md#ConfigureFramework), kad nustatytumėte minimalų ER parametrų rinkinį. Prieš pradėdami naudoti ER sistemą, kad kurdami naują ER sprendimą, turite užbaigti šį nustatymą.

### <a name="design-a-domain-specific-data-model"></a>Suprojektuoti domeno konkretų duomenų modelį

Turite sukurti naują ER konfigūraciją, kurioje būtų būtinas duomenų modelio komponentas. Šis duomenų modelis vėliau bus naudojamas kaip duomenų šaltinis, kai sukursite ER formatą audito ataskaitai generuoti.

Norėdami importuoti reikiamą duomenų modelį iš "Microsoft" teikiamo XML failo, atlikite šiuos veiksmus.

1. Atsisiųskite [pavyzdžio audito modelį.version.1.xml](https://download.microsoft.com/download/7/1/9/719b0132-fed7-4c73-8afa-90cac29c2fee/Sample-audit-model.version.1.xml) failą ir įrašykite jį į vietinį kompiuterį.
2. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
3. **Elektroninės ataskaitos** darbo srityje pasirinkite **Ataskaitos konfigūravimai**.
4. **Konfigūracijos puslapio** veiksmų srityje iš XML failo pasirinkite **Mainų** \> **įkėlimą**.
5. Pasirinkite **Naršyti**, raskite ir pasirinkite audito **modelio pavyzdžio.version.1.xml failą**.
6. Pasirinkite **OK** tam, kad importuotumėte konfigūravimą.

    ![Importuota ER duomenų modelio konfigūracija konfigūracijos puslapyje.](./media/er-data-model-parameterized-calls-imported-model.png)

Toliau esanti iliustracija rodo redaguojamą konfigūruojamo duomenų modelio versiją duomenų modelio **dizaino įrankio** puslapyje.

![ER duomenų modelio struktūra duomenų modelio dizaino įrankio puslapyje.](./media/er-data-model-parameterized-calls-model1.png)

Šiuo metu modelis sukurtas rodyti tik tas mokesčių operacijas, kurios turi reikiamą informaciją.

### <a name="design-a-model-mapping-for-the-configured-data-model"></a>Suprojektuokite konfigūruoto duomenų modelio žemėlapį

Kaip elektroninių ataskaitų kūrėjo vaidmens vartotojas turite sukurti naują ER konfigūraciją, kurioje būtų audito duomenų modelio pavyzdžio susiejimo komponentas. Šis komponentas įdiegia sukonfigūruotą "Microsoft" duomenų modelį Dynamics 365 Finance ir yra konkretus tai programai. Privalote konfigūruoti modelio žemėlapio komponentą tam, kad nurodytumėte programos objektus, kurie turi būti naudojami konfigūruoto duomenų modelio užpildymui su programos duomenimis vykdymo metu. Norėdami baigti šią užduotį turite suprasti, kaip mokesčių verslo domeno duomenų struktūra yra įdiegta finansuose.

Norėdami importuoti reikiamą modelio susiejimą iš "Microsoft" teikiamo XML failo, atlikite šiuos veiksmus.

1. Atsisiųskite [audito modelio susiejimo pavyzdį.version.1.1.xml](https://download.microsoft.com/download/c/0/3/c03a4673-b1b1-4ef8-96d0-bf96518be6e0/Sample-audit-model-mapping.version.1.1.xml) failas ir įrašykite jį į savo vietinį kompiuterį.
2. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
3. **Elektroninės ataskaitos** darbo srityje pasirinkite **Ataskaitos konfigūravimai**.
4. **Konfigūracijos puslapio** veiksmų srityje iš XML failo pasirinkite **Mainų** \> **įkėlimą**.
5. Pasirinkite **Naršyti**, raskite ir pasirinkite audito modelio **susiejimo pavyzdžio failą.version.1.1.xml** failas.
6. Pasirinkite **OK** tam, kad importuotumėte konfigūravimą.

    ![Importuota ER modelio susiejimo konfigūracija konfigūracijos puslapyje.](./media/er-data-model-parameterized-calls-imported-mapping.png)

Toliau esanti iliustracija rodo redaguojamą konfigūruojamo modelio susiejimo versiją modelio susiejimo **dizaino įrankio** puslapyje.

![ER modelio susiejimo struktūra modelio susiejimo dizainerio puslapyje.](./media/er-data-model-parameterized-calls-mapping1.png)

Šiuo metu modelio susiejimas yra skirtas rodyti mokesčių operacijas, kurios turi reikiamą informaciją. Jis išrenda šią informaciją iš programos `TaxTrans` lentelės naudodamas sukonfigūruotus ir `TaxTrans``TaxTransFiltered` ER duomenų šaltinius.

### <a name="design-a-new-format"></a>Sukurti naują formatą

Kaip vartotojas elektroninės ataskaitos funkcijų konsultanto vaidmenyje, turite sukurti naują ER konfigūraciją, kurioje būtų formato komponentas. Turite sukonfigūruoti formato komponentą, kad sugeneruotose ataskaitose būtų užpildytos mokesčių operacijos, kuriose yra visa reikiama informacija.

Norėdami importuoti reikiamą formatą iš Microsoft teikiamo XML failo, atlikite šiuos veiksmus.

1. Atsisiųskite [pavyzdžio audito formatą.version.1.1.xml](https://download.microsoft.com/download/e/b/7/eb7e126e-2bb3-4bbb-a735-ffd4c48920b1/Sample-audit-format.version.1.1.xml) failą ir įrašykite jį į vietinį kompiuterį.
2. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
3. **Elektroninės ataskaitos** darbo srityje pasirinkite **Ataskaitos konfigūravimai**.
4. **Konfigūracijos puslapio** veiksmų srityje iš XML failo pasirinkite **Mainų** \> **įkėlimą**.
5. Pasirinkite **Naršyti**, raskite ir pasirinkite pavyzdžio **audito formatą.version.1.1.xml** failas.
6. Pasirinkite **OK** tam, kad importuotumėte konfigūravimą.

    ![Importuota ER formato konfigūracija konfigūracijos puslapyje.](./media/er-data-model-parameterized-calls-imported-format.png)

Toliau esanti iliustracija rodo redaguojamą konfigūruojamo formato versiją formato **konstruktoriaus** puslapyje.

![ER formato struktūra formato konstruktoriaus puslapyje.](./media/er-data-model-parameterized-calls-format1.png)

ER formatas sukonfigūruotas generuoti ataskaitą kaip tekstinį failą kableliais atskirtų verčių (CSV) formatu.

### <a name="run-the-imported-format"></a>Importuoto formato vykdymas

1. Konfigūracijos puslapyje **pasirinkite** pavyzdžio audito **formato konfigūraciją**, tada veiksmų srityje pasirinkite **Vykdyti**.
2. Elektroninės ataskaitos **parametrų dialogo** lange, skirtuke Įrašai **, kuriuos norite įtraukti**, pasirinkite **Filtras**.
3. Nurodykite kvitų **PIV-110000004 ir INV-10000001** **sąlygas**.
4. Pasirinkite **Gerai**.
5. Pasirinkite **Gerai**.
6. Peržiūrėti sugeneruotą dokumentą, kuriame yra pasirinktų kvitų mokesčių operacijos.

    ![Sugeneruoto dokumento su mokesčių operacijomis peržiūra.](./media/er-data-model-parameterized-calls-output1.png)

### <a name="adjust-the-imported-er-solution"></a>Koreguoti importuotą ER sprendimą

Pagal naują reikalavimą dokumente, kurį turite pateikti, turi būti klientų ir tiekėjų, kurių operacijos yra įtrauktos, pavadinimai. Todėl būtina modifikuoti importuotą ER sprendimą, kad jis sugeneruotų dokumentą, atitinkaį šį naują reikalavimą.

Nuspręskite, kaip norite įdiegti reikiamas importuotų ER komponentų modifikacijas.

Šis principas yra įgyvendinti šiuos pakeitimus:

- Savo duomenų modelyje pridėkite naują `Transaction.Party.Name` eilutės tipo duomenų *modelio lauką*.
- Susiedami modelį konfigūruokite naujo duomenų modelio lauko susiejimą naudodami galimų lentelių ryšius, `DirPartyTable``Name` kad pasiekite reikiamą programos lentelės įrašą ir iš jo surasti lauko vertę.

Nors šis būdas veiks, SQL duomenų bazėje gali kilti efektyvumo problemų, `TaxTrans` nes operacijų lentelėje yra daug įrašų. Šiuo atveju, skambučių skaičius turi būti lygus `DirPartyTable` įrašų skaičius lentelėje, kuri `TaxTrans` gali sukelti efektyvumo problemų.

Taip pat galite atlikti šiuos pakeitimus:

- Savo duomenų modelyje pridėkite naują šakninį `Party` ir naują lauką`Party.Name`.
- Susiedami modelį pridėkite naują duomenų šaltinį, kuris prisijungs prie visų lentelių įrašų, `DirPartyTable` naudojamų lentelių ryšiuose, kad būtų galima pasiekti reikiamą programos lentelės įrašą, `TaxTrans` pradedant nuo lentelės.

Nors šis būdas veiks, gali kilti problemų dėl atminties suvartojimo. Net jei naujas [JOIN](er-join-data-sources.md) duomenų šaltinis paleistas kaip viena SQL užklausa programos duomenų bazei, kad išvengtumėte duomenų bazės našumo problemų, rezultatą reikia rasti programos serverio atmintyje. Kadangi įrašų skaičius ir laukų skaičius šiuose įrašuose bus gana didelis, šis būdas gali labai sunkus atminties suvartojimas. Dar galima pateikti atminties vykdyklės išimtį.

Pakeitimus galite įdiegti, kai vykdomas formatas atminties atmintyje renka unikalius klientų ir tiekėjų identifikavimo kodus visoms mokesčių operacijoms, kurios bus pateikiamos sugeneruotoje ataskaitoje. Kadangi turi būti saugomi tik unikalūs kodai, galutinis kodų rinkinys nebus pakankamai didelis, kad paveiktų atminties suvartojimą. Kodų rinkinys bus perduotas į modelio susiejimą kaip kito modelio tipo duomenų šaltinio iškvietimo *argumentas*. Atsižvelgiant į šį iškvietimą, modelio susiejimas paleis naują ER duomenų šaltinį, kuris padaro vieną SQL užklausą programos duomenų bazei surasti, iš lentelės, `DirPartyTable` įrašo tik tų šalių, kurių kodai pateikiami pateiktame kodų sąraše.

### <a name="adjust-the-imported-data-model"></a>Koreguoti importuotą duomenų modelį

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. **Konfigūracijos puslapio** konfigūracijos medžio kairiojoje srityje pasirinkite Pavyzdžio **audito modelis**.
3. **"FastTab"** versijose pasirinkite **2 versiją**, kurios būsena – Juodraštis **[...](general-electronic-reporting.md#component-versioning)**.
4. „FastTab“ pasirinkite **Konfigūracijos komponentai**.
5. Pasirinkite **konstruktorių**, kad atidarytumėte duomenų modelį redaguoti.
6. Duomenų modelio **puslapyje** įsitikinkite, kad laukas `Root` pasirinktas, o tada pasirinkite **Naujas**.
7. Išplečiamajame dialogo lange atlikite toliau nurodytus veiksmus.

    1. Naujo mazgo **kaip laukų** grupėje pasirinkite aktyvaus mazgo **pasirinktį Antrinis**.
    2. Lauke Pavadinimas **įveskite Šalis** **.**
    3. Lauke **Elemento tipas** pasirinkite **Įrašų sąrašas**.
    4. Norėdami **baigti** pridėti naują lauką, pasirinkite Įtraukti.

8. Įsitikinkite, kad `Root.Party` laukas pasirinktas, o tada skirtuke **Mazgas** pasirinkite **Parametrai**.
9. Parametrų **dialogo** lange atlikite šiuos veiksmus:

    1. Skirtuke **Parametrai** pasirinkite **Naujas**.
    2. Lauke Pavadinimas **įveskite** **PartyRefRecId**.
    3. **Lauke Tipas** pasirinkite **Int64**.
    4. Pažymėkite žymės **langelį** Sąrašas.
    5. Norėdami **baigti** įvesti parametrus, pasirinkite Gerai.

    > [!NOTE]
    > Ką tik sukonfigūravote `Root.Party` duomenų modelio lauką kaip lauką, kuris iškviečia, kai reikšmė pateikiama **parametre PartyRefRecId**. Ši vertė turi būti įrašų, kuriuose yra Int64 `Value` duomenų tipo *laukas*, sąraše.

    ![Parametrų dialogo langas.](./media/er-data-model-parameterized-calls-model2a.png)

10. Įsitikinkite, kad `Root.Party` laukas vis dar pasirinktas, tada pasirinkite **Naujas**.
11. Išplečiamajame dialogo lange atlikite toliau nurodytus veiksmus.

    1. Naujo mazgo **kaip laukų** grupėje pasirinkite aktyvaus mazgo **pasirinktį Antrinis**.
    2. **Lauke Pavadinimas** įveskite **Pavadinimas**.
    3. Lauke **Elemento tipas** pasirinkite **Eilutė**.
    4. Norėdami **baigti** pridėti naują lauką, pasirinkite Įtraukti.

12. Pasirinkite **Įrašyti** ir uždarykite duomenų **modelio** puslapį.

    ![Pakoreguoto ER duomenų modelio struktūra duomenų modelio dizaino įrankio puslapyje.](./media/er-data-model-parameterized-calls-model2b.png)

13. 2 versijos "FastTab" versijose **pasirinkite** **Keisti būseną** **Baigta**.\>**·** Tada pasirinkite **Gerai**.

    > [!NOTE]
    > Jūsų duomenų modelio pakeitimai **saugomi** **antrame** audito modelio duomenų modelio komponento, kuris yra antroje audito modelio ER konfigūracijos versijoje, tikslinimo metu.

![Atnaujinta ER duomenų modelio konfigūracija konfigūracijos puslapyje.](./media/er-data-model-parameterized-calls-updated-model.png)

### <a name="adjust-the-imported-model-mapping"></a>Koreguoti importuoto modelio susiejimą

1. **Konfigūracijos puslapio** konfigūracijos medžio kairiojoje srityje išplėskite audito modelio **pavyzdį**.
2. Pasirinkite **audito modelio susiejimo** pavyzdį, **tada** "FastTab" versijose pasirinkite antrą susiejimo versiją, pagrįstą pirma duomenų modelio versija (**1.2** versija) ir kurios būsena yra **Juodraštis**.
3. Pasirinkite **Pritaikyti kitoje vietoje**.
4. Paskirties versijos **lauke** palikite **2 pavyzdinio** audito **modelio pagrindinio modelio** versiją.
5. Pasirinkite Gerai **,** norėdami iš naujo sukurti ir sulygiuoti savo modelio susiejimą su naujausiais duomenų modelio pakeitimais.

    Atkreipkite dėmesį, kad jūsų **redaguojamo modelio susiejimo versijos numeris pasikeitė iš 1.2** **į 2.2** ir nurodo, kad dabar antra modelio versija yra naudojama kaip pagrindas.

6. Pasirinkite **Dizaino įrankis**.
7. Modelio ir **duomenų šaltinio susiejimo puslapyje dabartiniam** modelio susiejimui **pasirinkite** konstruktorių.
8. Norėdami pridėti naują duomenų šaltinį programos lentelei pasiekti, atlikite `DirPartyTable` šiuos veiksmus:

    1. **Duomenų šaltinio tipo srityje** pasirinkite Lentelės **Dynamics 365 for Operations\> įrašai**.
    2. **Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.
    3. Lauke Pavadinimas **įveskite** **PartyTable**.
    4. Lentelės lauke **įveskite** **DirPartyTable**.
    5. Norėdami **baigti** įtraukti naują duomenų šaltinį, pasirinkite Gerai.

9. Norėdami įtraukti naują duomenų šaltinį į užklausos įrašus `DirPartyTable`, paremtus pridėtu įrašų identifikavimo kodų sąrašu, atlikite šiuos veiksmus:

    1. Duomenų šaltinio **tipo srityje pasirinkite** Bendrasis tuščias **konteineris \>**.
    2. **Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.
    3. **Lauke Pavadinimas** įveskite **Duomenis**.
    4. Norėdami **baigti** įtraukti naują duomenų šaltinį, pasirinkite Gerai.
    5. **Duomenų šaltinių** srityje pasirinkite duomenų **duomenų** šaltinį.
    6. **Duomenų šaltinio tipo srityje** pasirinkite Funkcijos apskaičiuotas **\> laukas**.
    7. Duomenų šaltinių **srityje** pasirinkite **Įtraukti**.
    8. Lauke Pavadinimas **įveskite** **DirParty**.
    9. Pasirinkite **Redaguoti formulę**.
    10. Formulės dizaino **įrankio** puslapyje pasirinkite **Parametrai**.
    11. Parametrų **dialogo** lange atlikite šiuos veiksmus:

        1. Skirtuke **Parametrai** pasirinkite **Naujas**.
        2. Lauke Pavadinimas **įveskite** **DirPartyId**.
        3. **Lauke Tipas** pasirinkite **Int64**.
        4. Pažymėkite žymės **langelį** Sąrašas.
        5. Pasirinkite **Gerai**.

        > [!NOTE]
        > Jūs ką tik sukonfigūravote šį apskaičiuotą lauką, kad vykdymo metu jis imtų vieno parametro, konfigūruojamo kaip įrašų sąrašas, kuriame yra vienas Int64`Value` tipo laukas, argumentą.*·*

    12. Lauke **Formulė** įveskite toliau nurodytą išraišką.

        `FILTER(PartyTable, VALUEINLARGE(PartyTable.RecId, DirPartyId, DirPartyId.Value))`

        > [!NOTE]
        > Ką tik sukonfigūravote `DirParty``DirPartyTable``DirPartyId` apskaičiuotą lauką, kad būtų galima surasti tik įrašus, kuriuose įrašo identifikacijos kodai yra įtraukti į sąrašą, kuris pateikiamas kaip argumentas `DirParty` iškvietus lauką.

        ![Formulė, pagal kurią galima surasti šalių pavadinimus programos lentelėje, formulės dizaino įrankio puslapyje.](./media/er-data-model-parameterized-calls-formula1.png)

    13. Pasirinkite **Įrašyti** ir uždarykite puslapį **Formulių dizaino įrankis**.
    14. Norėdami **baigti** įtraukti naują duomenų **šaltinį**, pasirinkite Įrašyti, tada pasirinkite Gerai.

10. Norėdami susieti naują duomenų šaltinį su naujo duomenų modelio lauku, kad duomenų modelis būtų naudojamas šalių pavadinimams rodyti, atlikite šiuos veiksmus:

    1. **Duomenų modelio srityje** pasirinkite duomenų `Root.Party` modelio lauką.
    2. **Duomenų modelis** juostoje pasirinkite **Redaguoti**.
    3. **Formulės dizainerio** puslapio lauke **Formulė** įveskite išraišką `Data.DirParty(PartyRefRecId)`.
    4. Pasirinkite **Įrašyti** ir uždarykite puslapį **Formulių dizaino įrankis**.

        > [!NOTE]
        > Ką tik sukonfigūravote `Data.DirParty``Root.Party` susiejimą iškviesti sukonfigūruotą duomenų šaltinį ir pateikti įrašo identifikacijos kodų, kurie bus nurodyti formatu iškvie pasirinkus duomenų modelio lauką, sąrašą.

    5. **Duomenų modelio srityje** pasirinkite duomenų `Root.Party.Name` modelio lauką.
    6. **Duomenų modelis** juostoje pasirinkite **Redaguoti**.
    7. Formulės dizaino **įrankio** puslapio duomenų šaltinio **srityje** išplėskite **Data \> DirParty** ir pasirinkite **Pavadinimas**.
    8. Pasirinkite **Įtraukti duomenų šaltinį**.
    9. Pasirinkite **Įrašyti** ir uždarykite puslapį **Formulių dizaino įrankis**.

    ![Pakoreguoto ER modelio susiejimo struktūra modelio susiejimo dizainerio puslapyje.](./media/er-data-model-parameterized-calls-mapping2.png)

11. Pasirinkite **Įrašyti** ir uždarykite modelio susiejimo **dizaino įrankio** puslapį.
12. Uždarykite puslapį **Duomenų šaltinio susiejimo modelis**.
13. Versijos "**FastTab**", **2.2 versijoje**, pasirinkite **Keisti būseną \> Baigta**. Tada pasirinkite **Gerai**.

### <a name="adjust-the-imported-format"></a>Koreguoti importuotą formatą

1. **Konfigūracijos puslapyje pasirinkite** pavyzdžio **audito formatą**.
2. "FastTab **" versijose pasirinkite** 1.2 versiją **, kurios būsena Juodraštis** **.**
3. Pasirinkite **Pritaikyti kitoje vietoje**.
4. Paskirties versijos **lauke** palikite **2 pavyzdinio** audito **modelio pagrindinio modelio** versiją.
5. Pasirinkite Gerai **,** norėdami iš naujo sukurti ir sulygiuoti formatą su naujausiais duomenų modelio pakeitimais.
6. Pasirinkite **Dizaino įrankis**.
7. Formato dizainerio **puslapio**, kuris yra kairiojoje srityje esančioje formato struktūros medyje, pasirinkite Išplėsti **/ sutraukti**.
8. Norėdami įtraukti naują formato elementą, kad būtų surinkti šalių, kurių operacijos pateikiamos sugeneruotose ataskaitose, įrašų identifikavimo kodus, atlikite šiuos veiksmus.

    1. Formato struktūros medyje pasirinkite Elementą **Report.Row.Trans** seka.
    2. Pasirinkite **Įtraukti**.
    3. Dialogo lange **Įtraukti** pasirinkite Duomenų **šaltinio \> elementas**.
    4. Dialogo lango **Komponento** ypatybės lauke **Pavadinimas** įveskite **ID**.
    5. Lauke Duomenų **tipas** pasirinkite **Int64**.
    6. Pasirinkite **Gerai**.

    > [!NOTE]
    > Duomenų **šaltinio prekės \> elementas** gali būti naudojamas vidiniams skaičiavimams ir duomenų transformacijai atlikti tik einamojo formato aprėptimi. Todėl, įtraukdami šį formato elementą, nesukeičiate sugeneruoto dokumento turinio.

9. Norėdami įtraukti naujų formato elementų, kad į sugeneruotas ataskaitas būtų galima įvesti šalių pavadinimus, atlikite šiuos veiksmus:

    1. **Pasirinkite elementą Report.Row** seka.
    2. Pasirinkite **Įtraukti**.
    3. Dialogo lange **Įtraukti** pasirinkite Teksto **\> seka**.
    4. Dialogo lango **Komponento** ypatybės lauke Pavadinimas **įveskite** Šalis **·**.
    5. Pasirinkite **Gerai**.
    6. **Pasirinkite Report.Row. Šalies** sekos elementą.
    7. Pasirinkite **Įtraukti**.
    8. Dialogo lange **Įtraukti** pasirinkite Teksto **\> eilutė**.
    9. Dialogo lango **Komponento** ypatybės lauke **Pavadinimas** įveskite **Pavadinimas**.
    10. Pasirinkite **Gerai**.

10. Norėdami įtraukti naują duomenų šaltinį šalių, kurių operacijos pateikiamos sugeneruotose ataskaitose, įrašų identifikavimo kodams rinkti, atlikite šiuos veiksmus:

    1. Susiejimo **skirtuke** pasirinkite Įtraukti **šakninį.**
    2. Dialogo lange **Įtraukti duomenų** šaltinį pasirinkite Funkcijų **duomenų \> rinkinys**.
    3. **Duomenų rinkinio duomenų šaltinio ypatybės dialogo** lango lauke **Pavadinimas** įveskite **PartyId**.
    4. **Lauke Prekės tipas** pasirinkite **Int64**.
    5. Pasirinkite **Gerai**.

11. Norėdami įtraukti naują susiejimą, kad būtų surinkti šalių, kurių operacijos pateikiamos sugeneruotose ataskaitose, įrašų identifikavimo kodus, atlikite šiuos veiksmus:

    1. Formato struktūros medyje pasirinkite duomenų **Report.Row.Trans.Id** elementą.
    2. Pasirinkite **Redaguoti formulę**.
    3. Formulės dizainerio **puslapyje** įveskite išraišką `PartyIds.Collect(model.Transaction.Party.RecId)`.
    4. Pasirinkite **Įrašyti** ir uždarykite puslapį **Formulių dizaino įrankis**.

12. Norėdami įtraukti naujų susiejimų, kad į sugeneruotas ataskaitas būtų galima įvesti šalių pavadinimus, atlikite šiuos veiksmus:

    1. Formato struktūros medyje pasirinkite **Report.Party sekos** elementą.
    2. Pasirinkite **Redaguoti formulę**.
    3. Formulės dizainerio **puslapyje** įveskite išraišką `model.Party(PartyIds.Result)`.
    4. Pasirinkite **Įrašyti** ir uždarykite puslapį **Formulių dizaino įrankis**.
    5. Formato struktūros medyje pasirinkite sekos **Report.Party.Name** elementą.
    6. Skirtuke **Susiejimas** pasirinkite duomenų `model.Party.Name` modelio lauką.
    7. Pasirinkite **Susieti**.

    ![Pakoreguoto ER formato struktūra formato dizainerio puslapyje.](./media/er-data-model-parameterized-calls-format2.png)

13. Pasirinkite **Įrašyti** ir uždarykite puslapį Formato **konstruktorius**.
14. Uždarykite puslapį **Duomenų šaltinio susiejimo modelis**.
15. Versijos "**FastTab",** 2.2 versijoje **, pasirinkite** Keisti **būseną**\> Baigta **.** Tada pasirinkite **Gerai**.

### <a name="run-the-adjusted-format"></a>Paleisti pakoreguotą formatą

1. Konfigūracijos puslapyje **pasirinkite** **Pavyzdžio audito formatas**, tada veiksmų srityje pasirinkite **Vykdyti**.
2. Elektroninės ataskaitos **parametrų dialogo** lange, skirtuke Įrašai **, kuriuos norite įtraukti**, pasirinkite **Filtras**.
3. Nurodykite kvitų **PIV-110000004 ir INV-10000001** **sąlygas**.
4. Pasirinkite **Gerai**.
5. Pasirinkite **Gerai**.
6. Peržiūrėti sugeneruotą dokumentą, kuriame yra pasirinktų kvitų mokesčių operacijos ir atitinkamo kliento bei tiekėjo pavadinimai.

    ![Sugeneruoto dokumento su mokesčių operacijomis ir šalių pavadinimais peržiūra.](./media/er-data-model-parameterized-calls-output2.png)

7. Eikite **į Mokėtinų** \> **sumų tiekėjus** \> **Visi** tiekėjai ir **peržiūrėkite pasirinkto PIV-110000004** informaciją, įskaitant tiekėjo pavadinimą.

    ![Peržiūrėkite pirkimo kvito informaciją visuose tiekėjų ir SF žurnalo puslapiuose.](./media/er-data-model-parameterized-calls-review1.gif)

8. Eiti į **Gautinų** \> **sumų klientus** \> **Visi** klientai **ir peržiūrėti pasirinkto INV-10000001** kvito informaciją bei kliento vardą.

    ![Peržiūrėkite pardavimo kvito informaciją visuose klientų ir užregistruotų PVM puslapiuose.](./media/er-data-model-parameterized-calls-review2.gif)

Norėdami gauti daugiau informacijos apie šio ER sprendimo vykdymą, naudokite ER integruotą našumo [sekimo](trace-execution-er-troubleshoot-perf.md) analizatorių.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Apskaičiuoto lauko tipo ER duomenų šaltinių parametrizuotų kvietimų palaikymas](er-calculated-field-type.md)
- [ER formatų vykdymo sekimas siekiant diagnozuoti našumo problemas](trace-execution-er-troubleshoot-perf.md)
- [DUOMENŲ RINKIMO duomenų šaltinių naudojimas elektroninių ataskaitų formatuose](er-data-collection-data-sources.md)
- [ValueInLarge ER funkcija](er-functions-logical-valueinlarge.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
