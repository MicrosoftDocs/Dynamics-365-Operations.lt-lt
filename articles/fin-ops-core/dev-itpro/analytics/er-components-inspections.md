---
title: Sukonfigūruoto ER komponento patikrinimas, kad nekiltų vykdymo problemų
description: Šioje temoje paaiškinama, kaip patikrinti sukonfigūruotus elektroninių ataskaitų (ER) komponentus siekiant išvengti galinčių kilti vykdymo problemų.
author: NickSelin
manager: AnnBe
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72db7660c07b2f57f8609ab6c14964193e842d75
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688572"
---
# <a name="inspect-the-configured-er-component-to-prevent-runtime-issues"></a>Sukonfigūruoto ER komponento patikrinimas, kad nekiltų vykdymo problemų

[!include[banner](../includes/banner.md)]

Kiekvieną sukonfigūruotą [elektroninių ataskaitų (ER)](general-electronic-reporting.md) [formato](general-electronic-reporting.md#FormatComponentOutbound) ir [modelio susiejimo](general-electronic-reporting.md#data-model-and-model-mapping-components) komponentą galima [patikrinti](er-fillable-excel.md#validate-an-er-format) jį kuriant. Atliekant šį tikrinimą, atliekamas vientisumo patikrinimas siekiant išvengti galinčių kilti vykdymo problemų, pvz., vykdymo klaidų ir našumo suprastėjimo. Kiekvienai aptiktai problemai pateikiamas probleminio elemento kelias. Kai kurioms problemoms spręsti galima taikyti automatinę pataisą.

Numatyta, kad ER konfigūracijos, apimančios anksčiau minėtus komponentus, tikrinimas automatiškai taikomas tolesniais atvejais.

- [Importuojate](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) naują ER konfigūracijos [versiją](general-electronic-reporting.md#component-versioning) į savo „Microsoft Dynamics 365 Finance“ egzempliorių.
- Redaguojamos ER konfigūracijos [būseną](general-electronic-reporting.md#component-versioning) iš **Juodraštis** pakeičiate į **Baigta**.
- Redaguojamą ER konfigūraciją [pritaikote kitoje vietoje](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase), pritaikydami naują pagrindinę versiją.

Galite tiesiogiai vykdyti šį tikrinimą. Pasirinkite vieną iš tolesnių trijų parinkčių ir atlikite nurodytus veiksmus.

- 1 parinktis.

    1. Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.
    2. Konfigūracijos medyje, esančiame kairiojoje srityje, pasirinkite pageidaujamą ER konfigūraciją, kurioje yra ER formato arba ER modelio susiejimo komponentas.
    3. „FastTab“ **Versijos** pasirinkite norimą pasirinktos ER konfigūracijos versiją.
    4. Veiksmų srityje pasirinkite **Patvirtinti**.

- 2 ER formato parinktis.

    1. Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.
    2. Konfigūracijos medyje, esančiame kairiojoje srityje, pasirinkite pageidaujamą ER konfigūraciją, kurioje yra ER formato komponentas.
    3. „FastTab“ **Versijos** pasirinkite norimą pasirinktos ER konfigūracijos versiją.
    4. Veiksmų srityje pasirinkite **Dizaino įrankis**.
    5. Puslapio **Formato kūrimo įrankis** veiksmų srityje pasirinkite **Tikrinti**.

- 3 ER modelio susiejimo parinktis.

    1. Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.
    2. Konfigūracijos medyje, esančiame kairiojoje srityje, pasirinkite pageidaujamą ER konfigūraciją, kurioje yra ER modelio susiejimo komponentas.
    3. „FastTab“ **Versijos** pasirinkite norimą pasirinktos ER konfigūracijos versiją.
    4. Veiksmų srityje pasirinkite **Dizaino įrankis**.
    5. Veiksmų srities puslapyje **Duomenų šaltinio susiejimo modelis** pasirinkite **Dizaino įrankis**.
    6. Puslapio **Modelio susiejimo kūrimo įrankis** veiksmų srityje pasirinkite **Tikrinti**.

Norėdami praleisti tikrinimą, kai importuojama konfigūracija, atlikite šiuos veiksmus.

1. Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.
2. Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.
3. Parinktį **Importavus patikrinti konfigūraciją** nustatykite kaip **Ne**.

Norėdami praleisti tikrinimą, kai versijos būsena pakeičiama arba pritaikoma kitoje vietoje, atlikite šiuos veiksmus.

1. Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.
2. Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.
3. Parinktį **Praleisti tikrinimą konfigūracijos būsenos keitimo ir pritaikymo kitoje vietoje metu** nustatykite kaip **Taip**.

ER naudoja tolesnes kategorijas, kad būtų galima grupuoti vientisumo patikras.

- **Vykdomumas** – patikrinimai, kurie aptinka svarbias problemas, kurios gali įvykti vykdant. Šios problemos dažniausiai kyla **klaidų** lygmenyje. 
- **Našumas** – patikrinimai, nustatantys problemas, kurios gali lemti neefektyvų sukonfigūruotų ER komponentų vykdymą. Šios problemos dažniausiai kyla **įspėjimų** lygmenyje.
- **Duomenų vientisumas** – patikrinimai, nustatantys problemas, kurios gali lemti duomenų praradimą arba vykdymo problemas. Šios problemos dažniausiai kyla **įspėjimų** lygmenyje.

## <a name="list-of-inspections"></a>Patikrinimų sąrašas

Toliau pateikiamoje lentelėje apžvelgiami ER suteikiami patikrinimai. Norėdami gauti daugiau informacijos apie šiuos tikrinimus, naudokitės pirmo stulpelio saitais, kad pereitumėte prie atitinkamų šios temos skyrių. Šiuose skyriuose paaiškinami komponentų, kuriems ER suteikia patikrinimų, tipai ir tai, kaip galima iš naujo sukonfigūruoti ER komponentus, kad būtų išvengta problemų.

<table>
<thead>
<tr>
<th>Pavadinimas / vardas ir (arba) pavardė</th>
<th>Kategorija</th>
<th>Lygis</th>
<th>Laiškas</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href='#i1'>Tipo konvertavimas</a></td>
<td>Vykdomumas</td>
<td>Klaida</td>
<td>
<p>Negalima konvertuoti tipo &lt;tipas&gt; reiškinio į tipo &lt;type&gt; lauką.</p>
<p><b>Vykdymo klaida.</b> Tipo išimtis</p>
</td>
</tr>
<tr>
<td><a href='#i2'>Tipo suderinamumas</a></td>
<td>Vykdomumas</td>
<td>Klaida</td>
<td>
<p>Sukonfigūruoto reiškinio negalima naudoti kaip dabartinio formato elemento susiejimo su duomenų šaltiniu, nes šis reiškinys pateikia duomenų tipo &lt;tipas&gt; reikšmę, kuri nepatenka į duomenų tipus, kuriuos palaiko dabartinio formato elementas, kurio tipas – &lt;tipas&gt;.</p>
<p><b>Vykdymo klaida.</b> Tipo išimtis</p>
</td>
</tr>
<tr>
<td><a href='#i3'>Trūksta konfigūracijos elemento</a></td>
<td>Vykdomumas</td>
<td>Klaida</td>
<td>
<p>Kelias nerastas &lt;kelias&gt;.</p>
<p><b>Vykdymo klaida.</b> Nerastas konfigūracijos &lt;kelio&gt; elementas</p>
</td>
</tr>
<tr>
<td><a href='#i4'>Reiškinio vykdomumas naudojant funkciją FILTER</a></td>
<td>Vykdomumas</td>
<td>Klaida</td>
<td>
<p>Funkcijos FILTER sąrašo išraiška užklausų nepalaiko.</p>
<p><b>Vykdymo klaida.</b> Filtravimas nepalaikomas. Norėdami apie tai gauti daugiau informacijos, patvirtinkite konfigūraciją.</p>
</td>
</tr>
<tr>
<td rowspan='2'><a href='#i5'>GROUPBY duomenų šaltinio vykdomumas</a></td>
<td>Vykdomumas</td>
<td>Klaida</td>
<td>Kelias &lt;kelias&gt; nepalaiko užklausų.</td>
</tr>
<tr>
<td>Vykdomumas</td>
<td>Klaida</td>
<td>
<p>Funkcijos Grupuoti pagal negalima vykdyti naudojant užklausą.</p>
<p><b>Vykdymo klaida.</b> Funkcijos Grupuoti pagal negalima vykdyti naudojant užklausą.</p>
</td>
</tr>
<tr>
<td><a href='#i6'>JOIN duomenų šaltinio vykdomumas</a></td>
<td>Vykdomumas</td>
<td>Klaida</td>
<td>
<p>Negalima prijungti sąrašo &lt;kelio&gt;, kuris nėra užklausos filtras.</p>
<p><b>Vykdymo klaida.</b> Funkcijos Sujungta duomenų šaltinis turi būti neteisingai iškviestas filtro reiškinio laukas.</p>
</td>
</tr>
<tr>
<td><a href='#i7'>Funkcijų FILTER ir WHERE naudojimo tinkamumas</a></td>
<td>Našumas</td>
<td>Perspėjimas</td>
<td>Našumo atžvilgiu geriau naudoti reiškinio funkciją FILTER, o ne WHERE. Pasirinkite Taisyti, norėdami pakeisti automatiškai.</td>
</tr>
<tr>
<td><a href='#i8'>Funkcijų ALLITEMSQUERY ir ALLITEMS naudojimo tinkamumas</a></td>
<td>Našumas</td>
<td>Perspėjimas</td>
<td>Našumo atžvilgiu geriau naudoti reiškinio funkciją ALLITEMSQUERY, o ne ALLITEMS. Pasirinkite Taisyti, norėdami pakeisti automatiškai.</td>
</tr>
<tr>
<td><a href='#i9'>Pastabos apie tuščius sąrašo atvejus</a></td>
<td>Vykdomumas</td>
<td>Perspėjimas</td>
<td>
<p>Sąrašo &lt;kelias&gt; neapima tuščio sąrašo atvejo patikros, todėl vykdant gali įvykti klaida. Įtraukite tuščio sąrašo atvejo patikrą.</p>
<p><b>Vykdymo klaida.</b> Kelio &lt;kelias&gt; sąrašas yra tuščias</p>
<p><b><a href='#i9a'>Galima problema</a>.</b> Eilutė automatiškai užpildoma vieną kartą, nors duomenų šaltinyje, iš kurio ji užpildoma, yra keli įrašai.</p>
</td>
</tr>
<tr>
<td><a href='#i10'>Reiškinio vykdomumas naudojant funkciją FILTER (kaupimas talpykloje)</a></td>
<td>Vykdomumas</td>
<td>Klaida</td>
<td>
<p>Funkcijos FILTER negalima itaikyti pasirinktam duomenų šaltinio tipui. Tipo Lentelės įrašai duomenų šaltinis taikomas tik tada, kai jis nėra įtrauktas į talpyklą ir nėra neautomatiniu būdu įdėtų duomenų šaltinių.</p>
<p><b>Vykdymo klaida.</b> Filtravimas nepalaikomas. Norėdami apie tai gauti daugiau informacijos, patvirtinkite konfigūraciją.</p>
</td>
</tr>
<tr>
<td><a href='#i11'>Trūksta susiejimo</a></td>
<td>Vykdomumas</td>
<td>Perspėjimas</td>
<td>
<p>Kelyje &lt;kelias&gt; nėra susiejimo su jokiu duomenų šaltinyje naudojant modelio susiejimą.</p>
<p><b>Vykdymo klaida.</b> Kelias &lt;kelias&gt; nėra susietas</p>
</td>
</tr>
<tr>
<td><a href='#i12'>Nesusietas šablonas</a></td>
<td>Duomenų vientisumas</td>
<td>Perspėjimas</td>
<td>Failo &lt;vardas&gt; nesusietas su jokiais failo komponentais ir bus pašalintas pakeitus konfigūracijos versijos būseną.</td>
</tr>
<tr>
<td><a href='#i13'>Nesinchronizuotas formatas</a></td>
<td>Duomenų vientisumas</td>
<td>Perspėjimas</td>
<td>Nurodyto pavadinimo &lt;komponento pavadinimas&gt; nėra „Excel“ lape &lt;lapo pavadinimas&gt;</td>
</tr>
</tbody>
</table>

## <a name="type-conversion"></a><a id="i1"></a>Tipo konvertavimas

ER tikrina, ar duomenų modelio lauko duomenų tipas yra suderinamas su reiškinio, sukonfigūruoto kaip šio lauko susiejimas, duomenų tipu. Jei duomenų tipai yra nesuderinami, ER modelio susiejimo kūrimo įrankyje įvyksta tikrinimo klaida. Pranešime, kurį gaunate, teigiama, kad ER negali konvertuoti A tipo reiškinio į B tipo lauką.

Toliau pateikti veiksmai rodo, kaip gali kilti ši problema.

1. Pradėkite vienu metu konfigūruoti ER duomenų modelį ir ER modelio susiejimo komponentus.
2. Duomenų modelių medyje įtraukite lauką, pavadintą **X**, ir kaip duomenų tipą pasirinkite **Sveikasis skaičius**.

    ![Laukas X ir duomenų tipas Sveikasis skaičius įtraukti į duomenų režimų medį puslapyje Duomenų modelis](./media/er-components-inspections-01.png)

3. Modelio susiejimo duomenų šaltinių srityje įtraukite tipo **Apskaičiuotasis laukas** duomenų šaltinį.
4. Pavadinkite naująjį duomenų šaltinį **Y** ir jį sukonfigūruokite taip, kad jame būtų reiškinys `INTVALUE(100)`.
5. Susiekite **X** su **Y**.
6. Duomenų modelio kūrimo įrankyje pakeiskite lauko **X** duomenų tipą iš **Sveikasis skaičius** į **Int64**.
7. Pasirinkite **Tikrinti**, kad patikrintumėte redaguojamą modelio susiejimo komponentą puslapyje **Modelio susiejimo kūrimo įrankis**.

    ![Redaguojamo modelio susiejimo komponento tikrinimas puslapyje Modelio susiejimo kūrimo įrankis](./media/er-components-inspections-01.gif)

8. Pasirinkite **Tikrinti**, kad patikrintumėte pasirinktos ER konfigūracijos modelio susiejimo komponentą puslapyje **Konfigūracijos**.

    ![Modelio susiejimo komponento tikrinimas puslapyje Konfigūracijos](./media/er-components-inspections-01a.png)

9. Atkreipkite dėmesį, kad įvyksta tikrinimo klaida. Pranešime teigiama, kad tipo **Sveikasis skaičius** reikšmė, kurią pateikia duomenų šaltinio **Y** reiškinys `INTVALUE(100)`, negali būti saugoma tipo **Int64** duomenų modelio lauke **X**.

Tolesnėje iliustracijoje rodoma vykdymo klaida, kuri įvyksta, jei nepaisote įspėjimo ir pasirenkate **Vykdyti**, kad vykdytumėte formatą, kuris sukonfigūruotas naudoti modelio susiejimą.

![Vykdymo klaidos puslapyje Formato kūrimo įrankis](./media/er-components-inspections-01b.png)

### <a name="automatic-resolution"></a>Automatinis sprendimas

Nėra parinkties šiai problemai išspręsti automatiškai.

### <a name="manual-resolution"></a>Neautomatinis sprendimas

#### <a name="option-1"></a>1 pasirinktis

Atnaujinkite duomenų modelio struktūrą, keisdami duomenų modelio lauko duomenų tipą, kad jis atitiktų reiškinio, sukonfigūruoto šiam laukui susieti, duomenų tipą. Ankstesniame pavyzdyje lauko **X** duomenų tipas turi būti pakeistas atgal į **Sveikasis skaičius**.

#### <a name="option-2"></a>2 pasirinktis

Atnaujinkite modelio susiejimą, pakeisdami duomenų šaltinio reiškinį, susietą su duomenų modelio lauku. Ankstesniame pavyzdyje duomenų šaltinio **Y** reiškinį reikia pakeisti į `INT64VALUE(100)`.

## <a name="type-compatibility"></a><a id="i2"></a>Tipo suderinamumas

ER tikrina, ar formato elemento duomenų tipas yra suderinamas su reiškinio, sukonfigūruoto kaip šio formato elemento susiejimas, duomenų tipu. Jei duomenų tipai yra nesuderinami, ER operacijų kūrimo įrankyje įvyksta tikrinimo klaida. Gautame pranešime norodoma, kad sukonfigūruoto reiškinio negalima naudoti kaip dabartinio formato elemento susiejimo su duomenų šaltiniu, nes šis reiškinys pateikia A duomenų tipo reikšmę, kuri nepatenka į duomenų tipus, kuriuos palaiko dabartinio formato elementas, kurio tipas – B.

Toliau pateikti veiksmai rodo, kaip gali kilti ši problema.

1. Pradėkite vienu metu konfigūruoti ER duomenų modelį ir ER formato komponentus.
2. Duomenų modelių medyje įtraukite lauką, pavadintą **X**, ir kaip duomenų tipą pasirinkite **Sveikasis skaičius**.
3. Formato struktūros medyje įtraukite tipo **Skaitinis** formato elementą.
4. Pavadinkite naująjį formato elementą **Y**. Lauke **Skaitinis tipas** kaip duomenų tipą pasirinkite **Sveikasis skaičius**.
5. Susiekite **X** su **Y**.
6. Formato struktūros medyje **Y** formato elemento duomenų tipą pakeiskite iš **Sveikasis skaičius** į **Int64**.
7. Pasirinkite **Tikrinti**, kad patikrintumėte redaguojamą formato komponentą puslapyje **Formato kūrimo įrankis**.

    ![Tipo suderinamumo tikrinimas puslapyje Formato kūrimo įrankis](./media/er-components-inspections-02.gif)

8. Atkreipkite dėmesį, kad įvyksta tikrinimo klaida. Pranešime nurodoma, kad sukonfigūruotas reiškinys gali priimti tik **Int64** reikšmes. Todėl tipo **Sveikasis skaičius** **X** duomenų modelio lauko reiškmės negalima įvesti **Y** formato elemente.

### <a name="automatic-resolution"></a>Automatinis sprendimas

Nėra parinkties šiai problemai išspręsti automatiškai.

### <a name="manual-resolution"></a>Neautomatinis sprendimas

#### <a name="option-1"></a>1 pasirinktis

Atnaujinkite formato struktūrą, keisdami formato elemento **Skaitinis** duomenų tipą, kad jis atitiktų reiškinio, sukonfigūruoto šiam elementui susieti, duomenų tipą. Ankstesniame pavyzdyje **X** formato elemento **Skaitinis tipas** reikšmė turi būti pakeista atgal į **Sveikasis skaičius**.

#### <a name="option-2"></a>2 pasirinktis

Atnaujinkite **X** formato elemento formato susiejimą, pakeisdami reiškinį iš `model.X` į `INT64VALUE(model.X)`.

## <a name="missing-configuration-element"></a><a id="i3"></a>Trūksta konfigūracijos elemento

ER tikrina, ar susiejimo reiškiniai apima tik tuos duomenų šaltinius, kurie sukonfigūruoti redaguojamame ER komponente. Dėl kiekvieno susiejimo, apimančio duomenų šaltinį, kurio trūksta redaguojamame ER komponente, įvyksta tikrinimo klaida ER operacijų kūrimo įrankyje arba ER modelio susiejimo kūrimo įrankyje.

Toliau pateikti veiksmai rodo, kaip gali kilti ši problema.

1. Pradėkite vienu metu konfigūruoti ER duomenų modelį ir ER modelio susiejimo komponentus.
2. Duomenų modelių medyje įtraukite lauką, pavadintą **X**, ir kaip duomenų tipą pasirinkite **Sveikasis skaičius**.

    ![Duomenų modelių medis su lauku X ir duomenų tipu Sveikasis skaičius puslapyje Duomenų modelis](./media/er-components-inspections-01.png)

3. Modelio susiejimo duomenų šaltinių srityje įtraukite tipo **Apskaičiuotasis laukas** duomenų šaltinį.
4. Pavadinkite naująjį duomenų šaltinį **Y** ir jį sukonfigūruokite taip, kad jame būtų reiškinys `INTVALUE(100)`.
5. Susiekite **X** su **Y**.
6. Modelio susiejimo kūrimo įrankio duomenų šaltinių srityje panaikinkite duomenų šaltinį **Y**.
7. Pasirinkite **Tikrinti**, kad patikrintumėte redaguojamą modelio susiejimo komponentą puslapyje **Modelio susiejimo kūrimo įrankis**.

    ![Redaguojamo ER modelio susiejimo komponento tikrinimas puslapyje Modelio susiejimo kūrimo įrankis](./media/er-components-inspections-03.gif)

8. Atkreipkite dėmesį, kad įvyksta tikrinimo klaida. Pranešime nurodoma, kad **X** duomenų modelio lauke yra kelias, kuris nurodo į duomenų šaltinį **Y**, bet šis duomenų šaltinis nerastas.

### <a name="automatic-resolution"></a>Automatinis sprendimas

Pasirinkite **Atsieti**, kad automatiškai išspręstumėte šią problemą, pašalindami trūkstamą duomenų šaltinio susiejimą.

### <a name="manual-resolution"></a>Neautomatinis sprendimas

#### <a name="option-1"></a>1 pasirinktis

Atsiekite **X** duomenų modelio lauką, kad nebūtų nurodoma į neegzistuojantį duomenų šaltinį **Y**.

#### <a name="option-2"></a>2 pasirinktis

ER modelio susiejimo kūrimo įrankio duomenų šaltinių srityje vėl įtraukite duomenų šaltinį **Y**.

## <a name="executability-of-an-expression-with-filter-function"></a><a id="i4"></a>Reiškinio vykdomumas naudojant funkciją FILTER

Įtaisytoji ER funkcija [FILTER](er-functions-list-filter.md) naudojama norint pasiekti programos lenteles, rodinius arba duomenų objektus, pateikiant vieną SQL iškvietą, norint gauti reikalingus duomenis kaip įrašų sąrašą. Kaip šios funkcijos argumentas naudojamas tipo **Įrašų sąrašas** duomenų šaltinis, kuris nurodo iškvietos programos šaltinį. ER tikrina, ar galima nustatyti tiesioginę SQL užklausą duomenų šaltiniui, kuris nurodytas funkcijoje `FILTER`. Jei tiesioginės užklausos nustatyti negalima, ER modelio susiejimo kūrimo įrankyje įvyksta tikrinimo klaida. Gautame pranešime teigiama, kad ER reiškinio, apimančio funkciją `FILTER`, negalima vykdyti vykdymo metu. 

Toliau pateikti veiksmai rodo, kaip gali kilti ši problema.

1. Pradėkite konfigūruoti ER modelio susiejimo komponentą.
2. Įtraukite tipo **„Dynamics 365 for Operations“ \\ Lentelės įrašai** duomenų šaltinį.
3. Naująjį duomenų šaltinį pavadinkite **Vendor**. Lauke **Lentelė** pasirinkite **VendTable**, kad nurodytumėte, jog šiam duomenų šaltiniui reikės lentelės VendTable.
4. Įtraukite tipo **Apskaičiuotasis laukas** duomenų šaltinį.
5. Pavadinkite naująjį duomenų šaltinį **FilteredVendor** ir jį sukonfigūruokite taip, kad jame būtų reiškinys `FILTER(Vendor, Vendor.AccountNum="US-101")`.
6. Pasirinkite **Tikrinti**, kad patikrintumėte redaguojamąjį modelio susiejimo komponentą puslapyje **Modelio susiejimo kūrimo įrankis**, ir patikrinkite, ar reiškiniui `FILTER(Vendor, Vendor.AccountNum="US-101")` duomenų šaltinyje **Vendor** galima pateikti užklausų.
7. Modifikuokite duomenų šaltinį **Vendor**, įtraukdami įdėtąjį tipo **Apskaičiuotasis laukas** lauką, kad būtų galima gauti sutrumpintą tiekėjo sąskaitos numerį.
8. Pavadinkite naująjį įdėtąjį lauką **$AccNumber** ir jį sukonfigūruokite taip, kad jame būtų reiškinys `TRIM(Vendor.AccountNum)`.
9. Pasirinkite **Tikrinti**, kad patikrintumėte redaguojamąjį modelio susiejimo komponentą puslapyje **Modelio susiejimo kūrimo įrankis**, ir patikrinkite, ar reiškiniui `FILTER(Vendor, Vendor.AccountNum="US-101")` duomenų šaltinyje **Vendor** galima pateikti užklausų.

    ![Reiškinio tikrinimo užklausą galima pateikti puslapyje Modelio susiejimo kūrimo įrankis](./media/er-components-inspections-04.gif)

10. Atkreipkite dėmesį, kad įvyksta tikrinimo klaida, nes duomenų šaltinyje **Vendor** yra tipo **Apskaičiuotasis laukas** įdėtasis laukas, todėl negalima duomenų šaltinio **FilteredVendor** reiškinio konvertuoti į tiesioginį SQL sakinį.

Tolesnėje iliustracijoje rodoma vykdymo klaida, kuri įvyksta, jei nepaisote įspėjimo ir pasirenkate **Vykdyti**, kad vykdytumėte formatą, kuris sukonfigūruotas naudoti modelio susiejimą.

![Vykdymo klaidos, atsirandančios vykdant redaguojamąjį formatą puslapyje Formato kūrimo įrankis](./media/er-components-inspections-04a.png)

### <a name="automatic-resolution"></a>Automatinis sprendimas

Nėra parinkties šiai problemai išspręsti automatiškai.

### <a name="manual-resolution"></a>Neautomatinis sprendimas

#### <a name="option-1"></a>1 pasirinktis

Užuot į duomenų šaltinį **Vendor** įtraukę įdėtąjį tipo **Apskaičiuotasis laukas** lauką, įtraukite įdėtąjį lauką **$AccNumber** į duomenų šaltinį **FilteredVendor** ir jį sukonfigūruokite taip, kad jame būtų reiškinys `TRIM(FilteredVendor.AccountNum)`. Tokiu būdu reiškinys `FILTER(Vendor, Vendor.AccountNum="US-101")` gali būti vykdomas SQL lygmenyje ir įdėtąjį lauką **$AccNumber** apskaičiuoti vėliau.

#### <a name="option-2"></a>2 pasirinktis

Duomenų šaltinio **FilteredVendor** reiškinį iš `FILTER(Vendor, Vendor.AccountNum="US-101")` pakeiskite į `WHERE(Vendor, Vendor.AccountNum="US-101")`. Nerekomenduojame keisti lentelės, kurioje yra didelis duomenų kiekis (operacijų lentelės), reiškinio, nes visi įrašai bus iškviečiami, o reikiami įrašai pasirenkami naudojant atmintį. Todėl, naudojant šį metodą, gali suprastėti našumas. Daugiau informacijos ieškokite dalyje [ER funkcija WHERE](er-functions-list-where.md).

## <a name="executability-of-a-groupby-data-source"></a><a id="i5"></a>GROUPBY duomenų šaltinio vykdomumas

Duomenų šaltinis **GROUPBY** užklausos rezultatą padalija į įrašų grupes, paprastai tam, kad būtų galima atlikti vieną ar daugiau kiekvienos grupės telkimų. Kiekvienas duomenų šaltinis **GROUPBY** gali būti sukonfigūruotas taip, kad jis būtų vykdomas duomenų bazės lygiu arba atmintyje. Kai duomenų šaltinis **GROUPBY** sukonfigūruotas taip, kad būtų vykdomas duomenų bazės lygiu, ER patikrina, ar galima nustatyti tiesioginę SQL užklausą duomenų šaltiniui, kuris nurodytas tame duomenų šaltinyje. Jei tiesioginės užklausos nustatyti negalima, ER modelio susiejimo kūrimo įrankyje įvyksta tikrinimo klaida. Gautame pranešime teigiama, kad sukonfigūruoto duomenų šaltinio **GROUPBY** negalima vykdyti vykdymo metu.

Toliau pateikti veiksmai rodo, kaip gali kilti ši problema.

1. Pradėkite konfigūruoti ER modelio susiejimo komponentą.
2. Įtraukite tipo **„Dynamics 365 for Operations“ \\ Lentelės įrašai** duomenų šaltinį.
3. Pavadinkite naująjį duomenų šaltinį **Trans**. Lauke **Lentelė** pasirinkite **VendTrans**, kad nurodytumėte, jog šiam duomenų šaltiniui reikės lentelės VendTrans.
4. Įtraukite tipo **Grupuoti pagal** duomenų šaltinį.
5. Pavadinkite naująjį duomenų šaltinį **GroupedTrans** ir jį sukonfigūruokite toliau nurodytu būdu.

    - Kaip įrašų, kuriuos reikia sugrupuoti, šaltinį pasirinkite duomenų šaltinį **Trans**.
    - Lauke **Vykdymo vieta** pasirinkite **Užklausa**, kad nurodytumėte, jog norite šį duomenų šaltinį vykdyti duomenų bazės lygiu.

    ![Duomenų šaltinio konfigūravimas puslapyje „Grupuoti pagal“ parametrų redagavimas](./media/er-components-inspections-05a.gif)

6. Pasirinkite **Tikrinti**, kad patikrintumėte redaguojamąjį modelio susiejimo komponentą puslapyje **Modelio susiejimo kūrimo įrankis**, ir patikrinkite, ar sukonfigūruotam duomenų šaltiniui **GroupedTrans** galima pateikti užklausų.
7. Modifikuokite duomenų šaltinį **Trans**, įtraukdami įdėtąjį tipo **Apskaičiuotasis laukas** lauką, kad būtų galima gauti sutrumpintą tiekėjo sąskaitos numerį.
8. Pavadinkite naująjį duomenų šaltinį **$AccNumber** ir jį sukonfigūruokite taip, kad jame būtų reiškinys `TRIM(Trans.AccountNum)`.

    ![Duomenų šaltinio konfigūravimas puslapyje Modelio susiejimo kūrimo įrankis](./media/er-components-inspections-05a.png)

9. Pasirinkite **Tikrinti**, kad patikrintumėte redaguojamąjį modelio susiejimo komponentą puslapyje **Modelio susiejimo kūrimo įrankis**, ir patikrinkite, ar sukonfigūruotam duomenų šaltiniui **GroupedTrans** galima pateikti užklausų.

    ![Patikrinamas ER modelio susiejimo komponentas ir tai, ar sukonfigūruotam duomenų šaltiniui GroupedTrans galima pateikti užklausų puslapyje Modelio susiejimo kūrimo įrankis](./media/er-components-inspections-05b.png)

10. Atkreipkite dėmesį, kad įvyksta tikrinimo klaida, nes duomenų šaltinyje **Trans** yra tipo **Apskaičiuotasis laukas** įdėtasis laukas, todėl negalima duomenų šaltinio **GroupedTrans** iškvietos konvertuoti į tiesioginį SQL sakinį.

Tolesnėje iliustracijoje rodoma vykdymo klaida, kuri įvyksta, jei nepaisote įspėjimo ir pasirenkate **Vykdyti**, kad vykdytumėte formatą, kuris sukonfigūruotas naudoti modelio susiejimą.

![Vykdymo klaidos, atsirandančios nepaisant įspėjimo puslapyje Formato kūrimo įrankis](./media/er-components-inspections-05c.png)

### <a name="automatic-resolution"></a>Automatinis sprendimas

Nėra parinkties šiai problemai išspręsti automatiškai.

### <a name="manual-resolution"></a>Neautomatinis sprendimas

#### <a name="option-1"></a>1 pasirinktis

Užuot į duomenų šaltinį **Trans** įtraukę įdėtąjį tipo **Apskaičiuotasis laukas** lauką, įtraukite duomenų šaltinio **GroupedTrans** elemento **GroupedTrans.lines** įdėtąjį lauką **$AccNumber** ir jį sukonfigūruokite taip, kad jame būtų reiškinys `TRIM(GroupedTrans.lines.AccountNum)`. Tokiu būdu duomenų šaltinis **GroupedTrans** gali būti vykdomas SQL lygmenyje ir įdėtąjį lauką **$AccNumber** apskaičiuoti vėliau.

#### <a name="option-2"></a>2 pasirinktis

Pakeiskite duomenų šaltinio **GroupedTrans** lauko **Vykdymo vieta** reikšmę iš **Užklausa** į **Atmintyje**. Nerekomenduojame keisti lentelės, kurioje yra didelis duomenų kiekis (operacijų lentelės), reikšmės, nes visi įrašai bus iškviečiami, o grupavimas ir telkimas atliekami naudojant atmintį. Todėl, naudojant šį metodą, gali suprastėti našumas.

## <a name="executability-of-a-join-data-source"></a><a id="i6"></a>JOIN duomenų šaltinio vykdomumas

Duomenų šaltinis [JOIN](er-join-data-sources.md) sujungia įrašus iš dviejų ar daugiau duomenų bazių lentelių pagal susijusius laukus. Kiekvienas duomenų šaltinis **JOIN** gali būti sukonfigūruotas taip, kad jis būtų vykdomas duomenų bazės lygiu arba atmintyje. Kai duomenų šaltinis **JOIN** sukonfigūruotas taip, kad būtų vykdomas duomenų bazės lygiu, ER patikrina, ar galima nustatyti tiesioginę SQL užklausą duomenų šaltiniams, kurie nurodyti tame duomenų šaltinyje. Jei tiesioginės SQL užklausos su bent vienu nurodytu duomenų šaltiniu nustatyti negalima, ER modelio susiejimo kūrimo įrankyje įvyksta tikrinimo klaida. Gautame pranešime teigiama, kad sukonfigūruoto duomenų šaltinio **JOIN** negalima vykdyti vykdymo metu.

Toliau pateikti veiksmai rodo, kaip gali kilti ši problema.

1. Pradėkite konfigūruoti ER modelio susiejimo komponentą.
2. Įtraukite tipo **„Dynamics 365 for Operations“ \\ Lentelės įrašai** duomenų šaltinį.
3. Naująjį duomenų šaltinį pavadinkite **Vendor**. Lauke **Lentelė** pasirinkite **VendTable**, kad nurodytumėte, jog šiam duomenų šaltiniui reikės lentelės VendTable.
4. Įtraukite tipo **„Dynamics 365 for Operations“ \\ Lentelės įrašai** duomenų šaltinį.
5. Pavadinkite naująjį duomenų šaltinį **Trans**. Lauke **Lentelė** pasirinkite **VendTrans**, kad nurodytumėte, jog šiam duomenų šaltiniui reikės lentelės VendTrans.
6. Kaip įdėtąjį duomenų šaltinio **Vendor** lauką įtraukite tipo **Apskaičiuotasis laukas** duomenų šaltinį.
7. Pavadinkite naująjį duomenų šaltinį **FilteredTrans** ir jį sukonfigūruokite taip, kad jame būtų reiškinys `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`.
8. Įtraukite tipo **Jungti** duomenų šaltinį.
9. Pavadinkite naująjį duomenų šaltinį **JoinedList** ir jį sukonfigūruokite toliau nurodytu būdu.

    1. Kaip pirmą jungtinų įrašų rinkinį įtraukite duomenų šaltinį **Vendor**.
    2. Kaip antrą jungtinų įrašų rinkinį įtraukite duomenų šaltinį **Vendor.FilteredTrans**. Kaip tipą pasirinkite **INNER**.
    3. Lauke **Vykdyti** pasirinkite **Užklausa**, kad nurodytumėte, jog norite šį duomenų šaltinį vykdyti duomenų bazės lygiu.

    ![Duomenų šaltinio konfigūravimas puslapyje Jungimo kūrimo įrankis](./media/er-components-inspections-06a.gif)

10. Pasirinkite **Tikrinti**, kad patikrintumėte redaguojamąjį modelio susiejimo komponentą puslapyje **Modelio susiejimo kūrimo įrankis**, ir patikrinkite, ar sukonfigūruotam duomenų šaltiniui **JoinedList** galima pateikti užklausų.
11. Duomenų šaltinio **Vendor.FilteredTrans** reiškinį iš `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` pakeiskite į `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.
12. Pasirinkite **Tikrinti**, kad patikrintumėte redaguojamąjį modelio susiejimo komponentą puslapyje **Modelio susiejimo kūrimo įrankis**, ir patikrinkite, ar sukonfigūruotam duomenų šaltiniui **JoinedList** galima pateikti užklausų.

    ![Patikrinkite, redaguojamąjį modelio susiejimo komponentą ir patikrinkite, ar sukonfigūruotam duomenų šaltiniui JoinedList galima pateikti užklausų puslapyje Modelio susiejimo kūrimo įrankis.](./media/er-components-inspections-06b.png)

13. Atkreipkite dėmesį, kad įvyksta tikrinimo klaida, nes duomenų šaltinio **Vendor.FilteredTrans** reiškinio negalima konvertuoti į tiesioginę SQL iškvietą. Be to, tiesioginė SQL iškvieta neleidžia iškviesti duomenų šaltinio **JoinedList**, kuris bus konvertuotas į tiesioginį SQL sakinį.

    ![Vykdymo klaidos dėl duomenų šaltinio JoinedList nepavykusio tikrinimo puslapyje Modelio susiejimo kūrimo įrankis.](./media/er-components-inspections-06c.png)

Tolesnėje iliustracijoje rodoma vykdymo klaida, kuri įvyksta, jei nepaisote įspėjimo ir pasirenkate **Vykdyti**, kad vykdytumėte formatą, kuris sukonfigūruotas naudoti modelio susiejimą.

![Redaguojamojo formato paleidimas puslapyje Formato kūrimo įrankis](./media/er-components-inspections-06e.png)

### <a name="automatic-resolution"></a>Automatinis sprendimas

Nėra parinkties šiai problemai išspręsti automatiškai.

### <a name="manual-resolution"></a>Neautomatinis sprendimas

#### <a name="option-1"></a>1 pasirinktis

Duomenų šaltinio **Vendor.FilteredTrans** reiškinį `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` grąžinkite į `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`, kaip buvo rekomenduota įspėjime.

![Atnaujintas duomenų šaltinio reiškinys puslapyje Modelio susiejimo dizaino įrankis](./media/er-components-inspections-06d.png)

#### <a name="option-2"></a>2 pasirinktis

Pakeiskite duomenų šaltinio **JoinedList** lauko **Vykdyti** reikšmę iš **Užklausa** į **Atmintyje**. Nerekomenduojame keisti lentelės, kurioje yra didelis duomenų kiekis (operacijų lentelės), reikšmės, nes visi įrašai bus iškviečiami, o jungimas atliekamas naudojant atmintį. Todėl, naudojant šį metodą, gali suprastėti našumas. Rodomas patikrinimo įspėjimas, informuojantis apie šią riziką.

## <a name="preferability-of-filter-vs-where-function"></a><a id="i7"></a>Funkcijų FILTER ir WHERE naudojimo tinkamumas

Įtaisytoji ER funkcija [FILTER](er-functions-list-filter.md) naudojama norint pasiekti programos lenteles, rodinius arba duomenų objektus, pateikiant vieną SQL iškvietą, norint gauti reikalingus duomenis kaip įrašų sąrašą. Funkcija [WHERE](er-functions-list-where.md) iškviečia visus įrašus iš nurodyto šaltinio ir parenka įrašus atmintyje. Kaip abiejų funkcijų argumentas naudojamas tipo **Įrašų sąrašas** duomenų šaltinis, kuris nurodo įrašų gavimo šaltinį. ER tikrina, ar galima nustatyti tiesioginę SQL iškvietą duomenų šaltiniui, kuris nurodytas funkcijoje **WHERE**. Jei tiesioginės iškvietos nustatyti negalima, ER modelio susiejimo kūrimo įrankyje pateikiamas tikrinimo įspėjimas. Gautame pranešime rekomenduojama naudoti ne funkciją **WHERE**, o **FILTER**, kad būtų pagerintas efektyvumas.

Toliau pateikti veiksmai rodo, kaip gali kilti ši problema.

1. Pradėkite konfigūruoti ER modelio susiejimo komponentą.
2. Įtraukite tipo **„Dynamics 365 for Operations“ \\ Lentelės įrašai** duomenų šaltinį.
3. Pavadinkite naująjį duomenų šaltinį **Trans**. Lauke **Lentelė** pasirinkite **VendTrans**, kad nurodytumėte, jog šiam duomenų šaltiniui reikės lentelės VendTrans.
4. Kaip įdėtąjį duomenų šaltinio **Vendor** lauką įtraukite tipo **Apskaičiuotasis laukas** duomenų šaltinį.
5. Pavadinkite naująjį duomenų šaltinį **FilteredTrans** ir jį sukonfigūruokite taip, kad jame būtų reiškinys `WHERE(Trans, Trans.AccountNum="US-101")`.
6. Įtraukite tipo **„Dynamics 365 for Operations“ \\ Lentelės įrašai** duomenų šaltinį.
7. Naująjį duomenų šaltinį pavadinkite **Vendor**. Lauke **Lentelė** pasirinkite **VendTable**, kad nurodytumėte, jog šiam duomenų šaltiniui reikės lentelės VendTable.
8. Įtraukite tipo **Apskaičiuotasis laukas** duomenų šaltinį.
9. Pavadinkite naująjį duomenų šaltinį **FilteredVendor** ir jį sukonfigūruokite taip, kad jame būtų reiškinys `WHERE(Vendor, Vendor.AccountNum="US-101")`.
10. Pasirinkite **Tikrinti**, kad patikrintumėte redaguojamą modelio susiejimo komponentą puslapyje **Modelio susiejimo kūrimo įrankis**.

    ![Patikrinkite redaguojamąjį modelio susiejimo komponentą puslapyje Modelio susiejimo kūrimo įrankis](./media/er-components-inspections-07a.png)

11. Atkreipkite dėmesį, kad tikrinimo įspėjimuose rekomenduojama su duomenų šaltiniais **FilteredVendor** ir **FilteredTrans** naudoti funkciją **FILTER**, o ne **WHERE**.

    ![Tikrinimo įspėjimai, rekomenduojantys naudoti funkciją „filter“, o ne „where“ puslapyje Modelio susiejimo kūrimo įrankis](./media/er-components-inspections-07b.png)

### <a name="automatic-resolution"></a>Automatinis sprendimas

Pasirinkite **Taisyti**, kad visų duomenų šaltinių, kurie rodomi šio tipo tikrinimo skirtuko **Įspėjimai** tinklelyje, reiškinyje automatiškai pakeistumėte funkciją **WHERE** funkcija **FILTER**.

Taip pat galite pasirinkti atskiro įspėjimo tinklelyje eilutę, o tada – **Taisyti pažymėtus**. Šiuo atveju reiškinys automatiškai pakeičiamas tik tame duomenų šaltinyje, kuris paminėtas pasirinktame įspėjime.

![Elemento Taisyti pasirinkimas, kad funkcija „where“ būtų automatiškai pakeista funkcija „filter“ puslapyje Modelio susiejimo kūrimo įrankis](./media/er-components-inspections-07c.png)

### <a name="manual-resolution"></a>Neautomatinis sprendimas

Galite neautomatiniu būdu koreguoti visų duomenų šaltinių, nurodytų tikrinimo tinklelyje, reiškinius, pakeisdami funkciją **WHERE** funkcija **FILTER**.

## <a name="preferability-of-allitemsquery-vs-allitems-function"></a><a id="i8"></a>Funkcijų ALLITEMSQUERY ir ALLITEMS naudojimo tinkamumas

Integruotos ER funkcijos [ALLITEMS](er-functions-list-allitems.md) ir [ALLITEMSQUERY](er-functions-list-allitemsquery.md) naudojamos norint gauti lygiąją **įrašų sąrašo** reikšmę, kurią sudaro įrašų, nurodančių visus nurodytą kelią atitinkančius elemetus, sąrašas. ER tikrina, ar galima nustatyti tiesioginę SQL iškvietą duomenų šaltiniui, kuris nurodytas funkcijoje **ALLITEMS**. Jei tiesioginės iškvietos nustatyti negalima, ER modelio susiejimo kūrimo įrankyje pateikiamas tikrinimo įspėjimas. Gautame pranešime rekomenduojama naudoti ne funkciją **ALLITEMSQUERY**, o **ALLITEMS**, kad būtų pagerintas efektyvumas.

Toliau pateikti veiksmai rodo, kaip gali kilti ši problema.

1. Pradėkite konfigūruoti ER modelio susiejimo komponentą.
2. Įtraukite tipo **„Dynamics 365 for Operations“ \\ Lentelės įrašai** duomenų šaltinį.
3. Naująjį duomenų šaltinį pavadinkite **Vendor**. Lauke **Lentelė** pasirinkite **VendTable**, kad nurodytumėte, jog šiam duomenų šaltiniui reikės lentelės VendTable.
4. Įtraukite tipo **Apskaičiuotasis laukas** duomenų šaltinį, kad gautumėte kelių tiekėjų įrašų.
5. Pavadinkite naująjį duomenų šaltinį **FilteredVendor** ir jį sukonfigūruokite taip, kad jame būtų reiškinys `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`.
6. Įtraukite tipo **Apskaičiuotasis laukas** duomenų šaltinį, kad gautumėte visų filtruotų tiekėjų operacijas.
7. Pavadinkite naująjį duomenų šaltinį **FilteredVendorTrans** ir jį sukonfigūruokite taip, kad jame būtų reiškinys `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`.
8. Pasirinkite **Tikrinti**, kad patikrintumėte redaguojamą modelio susiejimo komponentą puslapyje **Modelio susiejimo kūrimo įrankis**.

    ![Puslapis Modelio susiejimo kūrimo įrankis, mygtukas Tikrinti](./media/er-components-inspections-08a.png)

9. Atkreipkite dėmesį, kad pateikiamas tikrinimo įspėjimas. Pranešime rekomenduojama su duomenų šaltiniu **FilteredVendorTrans** naudoti funkciją **ALLITEMSQUERY**, o ne **ALLITEMS**.

    ![Tikrinimo įspėjimas, nurodantis naudoti funkciją ALLITEMSQUERY, o ne ALLITEMS ER modelio susiejimo komponente, puslapyje Modelio susiejimo kūrimo įrankis](./media/er-components-inspections-08b.png)

### <a name="automatic-resolution"></a>Automatinis sprendimas

Pasirinkite **Taisyti**, kad visų duomenų šaltinių, kurie rodomi šio tipo tikrinimo skirtuko **Įspėjimai** tinklelyje, reiškinyje automatiškai pakeistumėte funkciją **ALLITEMS** funkcija **ALLITEMSQUERY**.

Taip pat galite pasirinkti atskiro įspėjimo tinklelyje eilutę, o tada – **Taisyti pažymėtus**. Šiuo atveju reiškinys automatiškai pakeičiamas tik tame duomenų šaltinyje, kuris paminėtas pasirinktame įspėjime.

![Puslapis Modelio susiejimo kūrimo įrankis, parinktis Taisyti pažymėtus pasirinkimas](./media/er-components-inspections-08c.png)

### <a name="manual-resolution"></a>Neautomatinis sprendimas

Galite neautomatiniu būdu koreguoti visų duomenų šaltinių, nurodytų tikrinimo tinklelyje, reiškinius, pakeisdami funkciją **ALLITEMS** funkcija **ALLITEMSQUERY**.

## <a name="consideration-of-empty-list-cases"></a><a id="i9"></a>Pastabos apie tuščius sąrašo atvejus

Galite sukonfigūruoti savo ER formato ar modelio susiejimo komponentą, kad būtų galima gauti tipo **Įrašų sąrašas** duomenų šaltinio lauko reikšmę. ER tikrina, ar jūsų dizainas numato atvejį, kai iškviestame duomenų šaltinyje nėra įrašų (t. y., jis tuščias), kad būtų išvengta vykdymo klaidų, kai reikšmė gaunama iš neegzistuojančio įrašo lauko.

Toliau pateikti veiksmai rodo, kaip gali kilti ši problema.

1. Pradėkite vienu metu konfigūruoti ER duomenų modelio, ER modelio susiejimo ir ER formato komponentus.
2. Duomenų modelių medyje įtraukite šakninį elementą, pavadintą **Root3**.
3. Modifikuokite elementą **Root3**, įtraukdami įdėtąjį tipo **Įrašų sąrašas** elementą.
4. Pavadinkite naują įdėtąjį elementą **Tiekėjas**.
5. Modifikuokite elementą **Tiekėjas** toliau nurodytu būdu.

    - Įtraukite įdėtąjį tipo **Eilutė** lauką ir pavadinkite jį **Name**.
    - Įtraukite įdėtąjį tipo **Eilutė** lauką ir pavadinkite jį **AccountNumber**.

    ![Įdėtųjų laukų įtraukimas puslapyje Duomenų modelis](./media/er-components-inspections-09a.png)

6. Modelio susiejimo duomenų šaltinių srityje įtraukite tipo **„Dynamics 365 for Operations“ \\ Lentelės įrašai** duomenų šaltinį.
7. Naująjį duomenų šaltinį pavadinkite **Vendor**. Lauke **Lentelė** pasirinkite **VendTable**, kad nurodytumėte, jog šiam duomenų šaltiniui reikės lentelės VendTable.
8. Įtraukite tipo **Bendra \\ Vartotojo įvesties parametras** duomenų šaltinį, kad būtų galima Ieškoti tiekėjo sąskaitos vykdymo dialogo lange.
9. Naująjį duomenų šaltinį pavadinkite **RequestedAccountNum**. Lauke **Žyma** įveskite **Tiekėjo sąskaitos numeris**. Lauke **Operacijų duomenų tipo pavadinimas** palikite numatytąją reikšmę **Aprašas**.
10. Įtraukite tipo **Apskaičiuotasis laukas** duomenų šaltinį, kad būtų taikomas tiekėjo, apie kurį klausiama, filtras.
11. Pavadinkite naująjį duomenų šaltinį **FilteredVendor** ir jį sukonfigūruokite taip, kad jame būtų reiškinys `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
12. Susiekite duomenų modelio elementus su sukonfigūruotas duomenų šaltiniais toliau nurodytu būdu.

    - Susiekite **FilteredVendor** su **Vendor**.
    - Susiekite **FilteredVendor.AccountNum** su **Vendor.AccountNumber**.
    - Susiekite **FilteredVendor.'name()'** su **Vendor.Name**.

    ![Duomenų modelio elementų susiejimas puslapyje Modelio susiejimo kūrimo įrankis](./media/er-components-inspections-09b.png)

13. Formato struktūros medyje įtraukite tolesnius elementus, kad būtų sugeneruotas siunčiamas XML formato dokumentas, kuriame būtų pateikta tiekėjo informacija.

    1. Įtraukite šakninį XML elementą **Statement**.
    2. XML elemente **Statement** įtraukite įdėtąjį XML elementą **Party**.
    3. XML elemente **Party** įtraukite tolesnius įdėtuosius XML atributus.

        - Pavadinimas / vardas ir (arba) pavardė
        - AccountNum

14. Susiekite formato elementus su pateiktais duomenų šaltiniais toliau nurodytu būdu.

    - Formato elementą **Statement\\Party\\Name** susiekite su duomenų šaltinio lauku **model.Vendor.Name**.
    - Formato elementą **Statement\\Party\\AccountNum** susiekite su duomenų šaltinio lauku **model.Vendor.AccountNumber**.

15. Pasirinkite **Tikrinti**, kad patikrintumėte redaguojamą formato komponentą puslapyje **Formato kūrimo įrankis**.

    ![Formato elementų, susietų su duomenų šaltiniais, tikrinimas puslapyje Formato kūrimo įrankis](./media/er-components-inspections-09c.png)

16. Atkreipkite dėmesį, kad įvyksta tikrinimo klaidų. Pranešime teigiama, kad, jei sąrašas **model.Vendor** tuščias, vykdant gali būti pateikta sukonfigūruotų formato komponentų **Statement\\Party\\Name** ir **Statement\\Party\\AccountNum** klaida.

    ![Tikrinimo klaida, kuria pranešama apie galimą sukonfigūruotų formato komponentų klaidą](./media/er-components-inspections-09d.png)

Tolesnėje iliustracijoje rodoma vykdymo klaida, kuri įvyksta, jei nepaisote įspėjimo, pasirenkate **Vykdyti**, kad vykdytumėte formatą, ir pasirenkate neegzistuojančio tiekėjo sąskaitos numerį. Kadangi pageidaujamo tiekėjo nėra, sąrašas **model.Vendor** bus tuščias (t. y., jame nebus įrašų).

![Vykdymo klaidos, įvykusios vykdant formato susiejimą](./media/er-components-inspections-09e.png)

### <a name="automatic-resolution"></a>Automatinis sprendimas

Skirtuke **Įspėjimai** esančio tinklelio pasirinktai eilutei galite parinkti **Atsieti**. Susiejimas, kuris nurodytas stulpelyje **Kelias**, automatiškai pašalinamas iš formato elementų.

### <a name="manual-resolution"></a>Neautomatinis sprendimas

#### <a name="option-1"></a>1 pasirinktis

Formato elementą **Statement\\Party\\Name** galite susieti su duomenų šaltinio elementu **model.Vendor**. Vykdymo metu šis susiejimas pirmiausia iškviečia duomenų šaltinį **model.Vendor**. Kai **model.Vendor** pateikia tuščią įrašų sąrašą, įdėtieji formato elementai nėra vykdomi. Todėl nepateikiama jokių tikrinimo įspėjimų dėl šios formato konfigūracijos.

![Formato elemento susiejimas su duomenų šaltinio elementu puslapyje Formato kūrimo įrankis](./media/er-components-inspections-09e.gif)

#### <a name="option-2"></a>2 pasirinktis

Pakeiskite formato elemento **Statement\\Party\\Name** susiejimą iš `model.Vendor.Name` į `FIRSTORNULL(model.Vendor).Name`. Atnaujintas susiejimas sąlygiškai konvertuoja pirmąjį tipo **Įrašų sąrašas** duomenų šaltinio **model.Vendor** įrašą į naują tipo **Įrašas** duomenų šaltinį. Šiame naujame duomenų šaltinyje yra tas pats laukų rinkinys.

- Jei duomenų šaltinyje **model.Vendor** yra bent vienas įrašas, šio įrašo laukai yra užpildomi duomenų šaltinio **model.Vendor** pirmojo įrašo laukų reikšmėmis. Šiuo atveju atnaujintas susiejimas pateikia tiekėjo vardą / pavadinimą.
- Kitu atveju kiekvienas sukurto įrašo laukas užpildomas numatytąja to lauko duomenų tipo reikšme. Šiuo atveju kaip numatytoji duomenų tipo **Eilutė** reikšmė pateikiama tuščia eilutė.

Todėl. kai formato elementas **Statement\\Party\\Name** susietas su reiškiniu `FIRSTORNULL(model.Vendor).Name`, dėl šio elemento nepateikiama jokių tikrinimo įspėjimų.

![Pakeitus susiejimą pašalinami tikrinimo įspėjimai puslapyje Formato kūrimo įrankis](./media/er-components-inspections-09f.gif)

#### <a name="option-3"></a>3 parinktis

Jei norite aiškiai nurodyti duomenis, įvestus į sugeneruotą dokumentą, kai tipo **Įrašų sąrašas** duomenų šaltinis **model.Vendor** nepateikia jokių įrašų (šiame pavyzdyje tai yra tekstas **Nėra**), pakeiskite formato elemento **Statement\\Party\\Name** susiejimą iš `model.Vendor.Name` į `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`. Taip pat galite naudoti reiškinį `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`.

### <a name="additional-consideration"></a><a id="i9a"></a>Papildomos pastabos

Be to, tikrinant įspėjama apie kitą galimą problemą. Pagal numatytuosius parametrus, kai susiejate formato elementus **Statement\\Party\\Name** ir **Statement\\Party\\AccountNum** su atitinkamais tipo **Įrašų sąrašas** duomenų šaltinio **model.Vendor** laukais, šie susiejimai bus vykdomi ir bus atsižvelgiama į atitinkamų duomenų šaltinio **model.Vendor** pirmojo įrašo laukus, jei šis sąrašas nebus tuščias.

Kadangi nesusiejote formato elemento **Statement\\Party** su duomenų šaltiniu **model.Vendor**, elementas **Statement\\Party** vykdant formatą nebus kartojamas kiekvienam duomenų šaltinio **model.Vendor** įrašui. Vietoj to sugeneruotas dokumentas bus užpildomas informacija tik iš pirmojo įrašų sąrašo įrašo, jei tame sąraše bus keli įrašai. Todėl gali kilti problemų, jei formatas skirtas atvejams, kai norima užpildyti sugeneruotą dokumentą informacija apie visus tiekėjus iš duomenų šaltinio **model.Vendor**. Norėdami išspręsti šią problemą, susiekite elementą **Statement\\Party** su duomenų šaltiniu **model.Vendor**.

## <a name="executability-of-an-expression-with-filter-function-caching"></a><a id="i10"></a>Reiškinio vykdomumas naudojant funkciją FILTER (kaupimas talpykloje)

Kelios integruotos ER funkcijos, įskaitant [FILTER](er-functions-list-filter.md) ir [ALLITEMSQUERY](er-functions-list-allitemsquery.md), naudojamos norint pasiekti programos lenteles, rodinius arba duomenų objektus, pateikiant vieną SQL iškvietą, norint gauti reikalingus duomenis kaip įrašų sąrašą. Kaip kiekvienos iš šių funkcijų argumentas naudojamas tipo **Įrašų sąrašas** duomenų šaltinis, kuris nurodo iškvietos programos šaltinį. ER tikrina, ar galima nustatyti tiesioginę SQL iškvietą duomenų šaltiniui, kuris nurodytas vienoje iš šių funkcijų. Jei tiesioginės iškvietos nustatyti negalima, nes duomenų šaltinis buvo pažymėtas kaip [laikomas talpykloje](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace), ER modelio susiejimo kūrimo įrankyje įvyksta tikrinimo klaida. Gautame pranešime teigiama, kad ER reiškinio, apimančio vieną iš šių funkcijų, negalima vykdyti vykdymo metu.

Toliau pateikti veiksmai rodo, kaip gali kilti ši problema.

1. Pradėkite konfigūruoti ER modelio susiejimo komponentą.
2. Įtraukite tipo **„Dynamics 365 for Operations“ \\ Lentelės įrašai** duomenų šaltinį.
3. Naująjį duomenų šaltinį pavadinkite **Vendor**. Lauke **Lentelė** pasirinkite **VendTable**, kad nurodytumėte, jog šiam duomenų šaltiniui reikės lentelės VendTable.
4. Įtraukite tipo **Bendra \\ Vartotojo įvesties parametras** duomenų šaltinį, kad būtų galima Ieškoti tiekėjo sąskaitos vykdymo dialogo lange.
5. Naująjį duomenų šaltinį pavadinkite **RequestedAccountNum**. Lauke **Žyma** įveskite **Tiekėjo sąskaitos numeris**. Lauke **Operacijų duomenų tipo pavadinimas** palikite numatytąją reikšmę **Aprašas**.
6. Įtraukite tipo **Apskaičiuotasis laukas** duomenų šaltinį, kad būtų taikomas tiekėjo, apie kurį klausiama, filtras.
7. Pavadinkite naująjį duomenų šaltinį **FilteredVendor** ir jį sukonfigūruokite taip, kad jame būtų reiškinys `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
8. Pažymėkite sukonfigūruotą duomenų šaltinį **Vendor** kaip laikomą talpykloje.

    ![Modelio susiejimo komponento konfigūravimas puslapyje Modelio susiejimo kūrimo įrankis](./media/er-components-inspections-10a.gif)

9. Pasirinkite **Tikrinti**, kad patikrintumėte redaguojamą modelio susiejimo komponentą puslapyje **Modelio susiejimo kūrimo įrankis**.

    ![Filtro funkcijos, taikomos talpyklos tiekėjo duomenų šaltiniui, tikrinimas puslapyje Modelio susiejimo kūrimo įrankis](./media/er-components-inspections-10a.png)

10. Atkreipkite dėmesį, kad įvyksta tikrinimo klaida. Pranešime nurodoma, kad funkcijos **FILTER** negalima taikyti talpykloje laikomam duomenų šaltiniui **Vendor**.

Tolesnėje iliustracijoje rodoma vykdymo klaida, kuri įvyksta, jei nepaisote įspėjimo ir pasirenkate **Vykdyti**, kad vykdytumėte formatą.

![Vykdymo klaida, įvykusi susiejant formatą puslapyje Formato kūrimo įrankis](./media/er-components-inspections-10b.png)

### <a name="automatic-resolution"></a>Automatinis sprendimas

Nėra parinkties šiai problemai išspręsti automatiškai.

### <a name="manual-resolution"></a>Neautomatinis sprendimas

#### <a name="option-1"></a>1 pasirinktis

Pašalinkite vėliavėlę **Talpykla** nuo duomenų šaltinio **Vendor**. Duomenų šaltinis **FilteredVendor** taps vykdomuoju, tačiau lentelėje VendTable nurodytas duomenų šaltinis **Vendor** bus pasiekiamas kiekvieną kartą, kai bus iškviestas duomenų šaltinis **FilteredVendor**.

#### <a name="option-2"></a>2 pasirinktis

Duomenų šaltinio **FilteredVendor** reiškinį iš `FILTER(Vendor, Vendor.AccountNum="US-101")` pakeiskite į `WHERE(Vendor, Vendor.AccountNum="US-101")`. Šiuo atveju lentelėje VendTable nurodytas duomenų šaltinis **Vendor** bus pasiekiamas tik pirmą kartą iškviečiant duomenų šaltinį **Vendor**. Tačiau įrašų parinkimas bus atliekamas atmintyje. Todėl, naudojant šį metodą, gali suprastėti našumas.

## <a name="missing-binding"></a><a id="i11"></a>Trūksta susiejimo

Kai konfigūruojate ER formato komponentą, bazinis ER duomenų modelis pasiūlomas kaip numatytasis to ER formato duomenų šaltinis. Vykdant sukonfigūruotą ER formatą, [numatytasis](er-country-dependent-model-mapping.md) bazinio modelio susiejimas naudojamas duomenų modeliui programos duomenimis užpildyti. ER formato kūrimo įrankyje rodomas įspėjimas, jei formato elementą susiejate su duomenų modelio elementu, kuris nėra susieta su jokiu duomenų šaltiniu modelio susiejime, kuris šiuo metu pasirinktas kaip numatytasis redaguojamo formato modelio susiejimas. Šio tipo susiejimo negalima vykdyti vykdymo metu, nes vykdomas formatas negali užpildyti susieto elemento programos duomenimis. Todėl vykdymo metu įvyksta klaida.

Toliau pateikti veiksmai rodo, kaip gali kilti ši problema.

1. Pradėkite vienu metu konfigūruoti ER duomenų modelio, ER modelio susiejimo ir ER formato komponentus.
2. Duomenų modelių medyje įtraukite šakninį elementą, pavadintą **Root3**.
3. Modifikuokite elementą **Root3**, įtraukdami naują įdėtąjį tipo **Įrašų sąrašas** elementą.
4. Pavadinkite naują įdėtąjį elementą **Tiekėjas**.
5. Modifikuokite elementą **Tiekėjas** toliau nurodytu būdu.

    - Įtraukite įdėtąjį tipo **Eilutė** lauką ir pavadinkite jį **Name**.
    - Įtraukite įdėtąjį tipo **Eilutė** lauką ir pavadinkite jį **AccountNumber**.

    ![Įdėtųjų laukų įtraukimas į tiekėjo elementą puslapyje Duomenų modelis](./media/er-components-inspections-11a.png)

6. Modelio susiejimo duomenų šaltinių srityje įtraukite tipo **„Dynamics 365 for Operations“ \\ Lentelės įrašai** duomenų šaltinį.
7. Naująjį duomenų šaltinį pavadinkite **Vendor**. Lauke **Lentelė** pasirinkite **VendTable**, kad nurodytumėte, jog šiam duomenų šaltiniui reikės lentelės VendTable.
8. Įtraukite tipo **Bendra \\ Vartotojo įvesties parametras** duomenų šaltinį, kad būtų pateikta užklausa apie tiekėjo sąskaitą vykdymo dialogo lange.
9 Naująjį duomenų šaltinį pavadinkite **RequestedAccountNum**. Lauke **Žyma** įveskite **Tiekėjo sąskaitos numeris**. Lauke **Operacijų duomenų tipo pavadinimas** palikite numatytąją reikšmę **Aprašas**.
10. Įtraukite tipo **Apskaičiuotasis laukas** duomenų šaltinį, kad būtų taikomas tiekėjo, apie kurį klausiama, filtras.
11. Pavadinkite naująjį duomenų šaltinį **FilteredVendor** ir jį sukonfigūruokite taip, kad jame būtų reiškinys `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
12. Susiekite duomenų modelio elementus su sukonfigūruotas duomenų šaltiniais toliau nurodytu būdu.

    - Susiekite **FilteredVendor** su **Vendor**.
    - Susiekite **FilteredVendor.AccountNum** su **Vendor.AccountNumber**.

    > [!NOTE]
    > Duomenų modelio **Vendor.Name** laukas lieka nesusietas.

    ![Duomenų modelio elementai, susieti su sukonfigūruotais duomenų šaltiniais, ir likęs duomenų modelio elementas puslapyje Modelio susiejimo kūrimo įrankis](./media/er-components-inspections-11b.png)

13. Formato struktūros medyje įtraukite tolesnius elementus, kad būtų sugeneruotas siunčiamas XML formato dokumentas, kuriame būtų pateikta informacija apie tiekėją, dėl kurio pateikta užklausa.

    1. Įtraukite šakninį XML elementą **Statement**.
    2. XML elemente **Statement** įtraukite įdėtąjį XML elementą **Party**.
    3. XML elemente **Party** įtraukite tolesnius įdėtuosius XML atributus.

        - Pavadinimas / vardas ir (arba) pavardė
        - AccountNum

14. Susiekite formato elementus su pateiktais duomenų šaltiniais toliau nurodytu būdu.

    - Formato elementą **Statement\\Party** susiekite su duomenų šaltinio **model.Vendor** elementu.
    - Formato elementą **Statement\\Party\\Name** susiekite su duomenų šaltinio lauku **model.Vendor.Name**.
    - Formato elementą **Statement\\Party\\AccountNum** susiekite su duomenų šaltinio lauku **model.Vendor.AccountNumber**.

15. Pasirinkite **Tikrinti**, kad patikrintumėte redaguojamą formato komponentą puslapyje **Formato kūrimo įrankis**.

    ![ER formato komponento tikrinimas puslapyje Formato kūrimo įrankis](./media/er-components-inspections-11c.png)

16. Atkreipkite dėmesį, kad pateikiamas tikrinimo įspėjimas. Pranešime nurodoma, kad duomenų šaltinio laukas **model.Vendor.Name** nėra susietas su jokiu modelio susiejimo duomenų šaltiniu, kuris sukonfigūruotas kaip naudojamas formato. Todėl formato elemento **Statement\\Party\\Name** negalima užpildyti vykdymo metu ir gali įvykti vykdymo išimtis.

    ![ER formato komponento tikrinimas puslapyje Formato kūrimo įrankis](./media/er-components-inspections-11d.png)

Tolesnėje iliustracijoje rodoma vykdymo klaida, kuri įvyksta, jei nepaisote įspėjimo ir pasirenkate **Vykdyti**, kad vykdytumėte formatą.

![Redaguojamojo formato paleidimas puslapyje Formato kūrimo įrankis](./media/er-components-inspections-11e.png)

### <a name="automatic-resolution"></a>Automatinis sprendimas

Nėra parinkties šiai problemai išspręsti automatiškai.

### <a name="manual-resolution"></a>Neautomatinis sprendimas

#### <a name="option-1"></a>1 pasirinktis

Modifikuokite sukonfigūruotą modelio susiejimą, įtraukdami duomenų šaltinio lauko **model.Vendor.Name** susiejimą.

#### <a name="option-2"></a>2 pasirinktis

Modifikuokite sukonfigūruotą formatą, pašalindami formato elemento **Statement\\Party\\Name** susiejimą.

## <a name="not-linked-template"></a><a id="i12"></a>Nesusietas šablonas

Kai [neautomatiniu būdu](er-fillable-excel.md#manual-entry) konfigūruojate ER formato komponentą, kad, naudodamas šabloną, jis generuotų siunčiamą dokumentą, turite neautomatiniu būdu įtraukti elementą **„Excel“\\Failas**, įtraukti reikiamą šabloną kaip redaguojamojo komponento priedą ir pasirinkti šį priedą įtrauktame elemente **„Excel\\Failas**. Tokiu būdu nurodote, kad įtrauktas elementas užpildys pasirinktą šabloną vykdymo metu. Konfigūruodami [būsenos](general-electronic-reporting.md#component-versioning) **Juodraštis** formato komponento versiją, į redaguojamąjį komponentą galite įtraukti kelis šablonus, o tada pasirinkti kiekvieną šabloną elemente **„Excel“\\Failas**, kad būtų vykdomas ER formatas. Tokiu būdu galite matyti, kaip vykdant užpildomi skirtingi šablonai. Jei turite šablonų, kurie nepasirinkti jokiuose elementuose **„Excel“\\Failas**, ER formato kūrimo įrankis jus įspėja, kad tie šablonai bus panaikinti redaguojamojo ER formato komponento versijoje, kai jo būsena iš **Juodraštis** bus pakeista į **Baigta**.

Toliau pateikti veiksmai rodo, kaip gali kilti ši problema.

1. Pradėkite konfigūruoti ER formato komponentą.
2. Formato struktūros medyje įtraukite elementą **„Excel“\\Failas**.
3. Į elementą **„Excel“\\Failas**, kurį ką tik įtraukėte, kaip priedą įtraukite „Excel“ darbaknygės failą **A.xlsx**. Naudokite dokumento tipą, kuris sukonfigūruotas naudojant [ER parametrus](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents), kad nurodytumėte ER formato šablonų saugyklą.
4. Į elementą **„Excel“\\Failas** kaip priedą įtraukite dar vieną „Excel“ darbaknygės failą **B.xlsx**. Naudoti tą patį dokumento tipą, kuris naudojamas su darbaknygės failu A.
5. Elemente **„Excel“\\Failas** pasirinkite darbaknygės failą A.
6. Pasirinkite **Tikrinti**, kad patikrintumėte redaguojamą formato komponentą puslapyje **Formato kūrimo įrankis**.

    ![Darbaknygės failo redaguojamojo formato komponento tikrinimas puslapyje Formato kūrimo įrankis](./media/er-components-inspections-12a.gif)

7. Atkreipkite dėmesį, kad pateikiamas tikrinimo įspėjimas. Pranešime teigiama, kad darbaknygės failas **B.xlsx** nėra susietas su jokiais komponentais ir kad jis bus pašalintas pakeitus konfigūracijos versijos būseną.

### <a name="automatic-resolution"></a>Automatinis sprendimas

Nėra parinkties šiai problemai išspręsti automatiškai.

### <a name="manual-resolution"></a>Neautomatinis sprendimas

Modifikuokite sukonfigūruotą formatą, pašalindami visus šablonus, kurie nėra susieti su jokiu elementu **„Excel“\\Failas**.

## <a name="not-synced-format"></a><a id="i13"></a>Nesinchronizuotas formatas

Kai [konfigūruojate](er-fillable-excel.md) ER formato komponentą, kad, naudodamas „Excel“ šabloną, jis generuotų siunčiamą dokumentą, galite neautomatiniu būdu įtraukti elementą **„Excel“\\Failas**, įtraukti reikiamą šabloną kaip redaguojamojo komponento priedą ir pasirinkti šį priedą įtrauktame elemente **„Excel\\Failas**. Tokiu būdu nurodote, kad įtrauktas elementas užpildys pasirinktą šabloną vykdymo metu. Kadangi įtrauktas „Excel“ šablonas sukurtas išorėje, redaguojamajame ER formate gali būti „Excel“ pavadinimų, kurių nėra įtrauktame šablone. ER formato kūrimo įrankis įspėja apie visus skirtumus tarp ER formato elementų ypatybių, susijusių su pavadinimais, kurie neįtraukti į įtrauktą „Excel“ šabloną.

Toliau pateikti veiksmai rodo, kaip gali kilti ši problema.

1. Pradėkite konfigūruoti ER formato komponentą.
2. Formato struktūros medyje įtraukite **„Excel“\\Failas** elementą **Ataskaita**.
3. Į elementą **„Excel“\\Failas**, kurį ką tik įtraukėte, kaip priedą įtraukite „Excel“ darbaknygės failą **A.xlsx**. Naudokite dokumento tipą, kuris sukonfigūruotas naudojant [ER parametrus](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents), kad nurodytumėte ER formato šablonų saugyklą.

    > [!IMPORTANT]
    > Įsitikinkite, kad įtrauktoje „Excel“ darbaknygėje nėra pavadinimo **ReportTitle**.

4. Įtraukite tolesnį **„Excel“\\Langelis** elementą **Pavadinimas** kaip įdėtąjį elemento **Ataskaita** elementą. Lauke **„Excel“ intervalas** įveskite **ReportTitle**.
5. Pasirinkite **Tikrinti**, kad patikrintumėte redaguojamą formato komponentą puslapyje **Formato kūrimo įrankis**.

    ![Įdėtųjų elementų ir laukų tikrinimas puslapyje Formato kūrimo įrankis](./media/er-components-inspections-13a.png)

6. Atkreipkite dėmesį, kad pateikiamas tikrinimo įspėjimas. Pranešime teigiama, kad „Excel“ šablono, kurį naudojate, lape **Lapas1** pavadinimo **ReportTitle** nėra.

    ![Tikrinimo įspėjimas, kad pavadinimo ReportTitle „Excel“ šablono lape Lapas1 nėra](./media/er-components-inspections-13b.png)

### <a name="automatic-resolution"></a>Automatinis sprendimas

Nėra parinkties šiai problemai išspręsti automatiškai.

### <a name="manual-resolution"></a>Neautomatinis sprendimas

#### <a name="option-1"></a>1 pasirinktis

Modifikuokite sukonfigūruotą formatą, pašalindami visus elementus, nurodančius „Excel“ pavadinimus, kurių trūksta šablone.

#### <a name="option-2"></a>2 pasirinktis

[Atnaujinkite](er-fillable-excel.md#template-import) redaguojamąjį ER formatą, importuodami „Excel“ šabloną. Redaguojamojo ER formato struktūra bus [sinchronizuojama](modify-electronic-reporting-format-reapply-excel-template.md) su importuoto „Excel“ šablono struktūra.

### <a name="additional-consideration"></a>Papildomos pastabos

Norėdami sužinoti, kaip formato struktūra gali būti sinchronizuojama su ER šablonu [verslo dokumentų valdymo](er-business-document-management.md) šablonų rengyklėje, žr. [Verslo dokumento šablono struktūros atnaujinimas](er-bdm-update-structure.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[ER ALLITEMS funkcija](er-functions-list-allitems.md)

[ER ALLITEMSQUERY funkcija](er-functions-list-allitemsquery.md)

[INT64VALUE ER funkcija](er-functions-conversion-int64value.md)

[ER INTVALUE funkcija](er-functions-conversion-intvalue.md)

[ER FILTER funkcija](er-functions-list-filter.md)

[WHERE ER funkcija](er-functions-list-where.md)

[Duomenų šaltinių JOIN naudojimas norint gauti duomenų iš kelių ER modelio susiejimų programos lentelių](er-join-data-sources.md)

[ER formatų vykdymo sekimas siekiant diagnozuoti našumo problemas](trace-execution-er-troubleshoot-perf.md)

[Verslo dokumentų valdymo apžvalga](er-business-document-management.md)
