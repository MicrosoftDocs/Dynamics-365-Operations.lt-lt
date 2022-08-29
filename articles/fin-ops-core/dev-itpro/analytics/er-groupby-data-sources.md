---
title: Grupuoti įrašus ir sujungti skaičiavimus naudojant GROUPBY duomenų šaltinius
description: Šiame straipsnyje paaiškinama, kaip naudoti GROUPBY tipo duomenų šaltinius elektroninėse ataskaitose (ER).
author: kfend
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: ''
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
ms.openlocfilehash: 0e520705d2441ead5a68ec3284db74999b3d90b5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277608"
---
# <a name="group-records-and-aggregate-calculations-by-using-groupby-data-sources"></a>Grupuoti įrašus ir sujungti skaičiavimus naudojant GROUPBY duomenų šaltinius

[!include[banner](../includes/banner.md)]

Konfigūruodami elektroninių [ataskaitų (ER) modelių](general-electronic-reporting.md) susiejimus ar formatus, [galite](#AddMmDataSource2) pridėti reikalingus GroupBy tipo **duomenų šaltinius**.

Dizaino metu GroupBy **duomenų** šaltinis konfigūruojamas, kad būtų galima identifikuoti šiuos elementus:

- Pagrindinis [duomenų šaltinis,](#BaseDataSource) kuriame yra įrašai, kurie bus sugrupuoti vykdyklėje
- [Pagrindinio duomenų](#GroupingFields) šaltinio grupavimo laukai, kurie bus naudojami grupuojant įrašus apdorojimo laiku
- [Sujungti funkcijas](#AggregateFunctions), kurios nurodo sudėtiius skaičiavimus, kurie bus atliekami kiekvienai rastai grupei vykdyklėje

Apdorojimo metu sukonfigūruoti **GroupBy duomenų** šaltinio grupių įrašai, kurių vertės grupavimo laukuose yra vienodos, tada pateikiamas įrašų sąrašas. Kiekvienas įrašas vaizduoja vieną grupę. Kiekvienos grupės duomenų šaltinis rodo lauko vertes, pagal kurias buvo sugrupuoti pradiniai įrašai, apskaičiuotos sudėties funkcijos vertes ir pagrindinių duomenų šaltinio įrašų, kurie priklauso grupei, sąrašą.

## <a name="aggregate-functions"></a><a name="AggregateFunctions"></a> Sujungti funkcijas

Vykdomas kiekvienas kiekvienos įrašų grupės sudėties skaičiavimas vykdymo metu. Šis skaičiavimas **atliekamas naudojant vieno lauko arba išraiškos vertę duomenų šaltinio, kuris buvo pasirinktas grupuoti redaguojamame GroupBy tipo duomenų šaltinyje, įrašuose**. Šios suminės funkcijos šiuo metu palaikomos:

- **AVG** – ši funkcija grąžina grupės verčių vidurkį. Gali būti naudojamas tik su skaitiniais laukais.
- **SKAIČIUS** – ši funkcija grąžina prekių, kurios buvo grupę surasta, skaičių.
- **Min** . – ši funkcija grąžina minimalią vertę tarp grupės verčių.
- **Maks** . – ši funkcija grąžina maksimalią vertę tarp grupės verčių.
- **SUMA** – ši funkcija grąžina visų grupės verčių sumą. Gali būti naudojamas tik su skaitiniais laukais.

## <a name="execution-location"></a><a name="ExecutionLocation"></a>Vykdymo vieta

Kai redaguojate **GroupBy** duomenų šaltinį ir nurodote duomenų šaltinį, kuriame yra įrašai, kuriuos reikia sugrupuoti, [...](#ExecutionLocation)**sistema automatiškai aptinka efektyviiausią vietą, kad būtų galima vykdyti GroupBy** duomenų šaltinį. Jei pagrindinis [duomenų](er-functions-list-filter.md#usage-notes) šaltinis yra užklausuojamas (t. y., jei jį galima paleisti duomenų bazės lygiu), **programos duomenų bazė taip pat nurodoma kaip redaguojamo GroupBy** duomenų šaltinio vykdymo vieta. Kitu atveju programos serverio atmintis nurodoma kaip vykdymo vieta.

Galite rankiniu būdu pakeisti automatiškai aptiktą vykdymo vietą pasirinkdami vietą, kuri taikoma sukonfigūruotiems duomenų šaltinyje. Jei pasirinkta vykdymo vieta netaikoma, dizaino [metu](er-components-inspections.md#i5) rodoma tikrinimo klaida.

> [!TIP]
> Duomenų bazės vietą rekomenduojame naudoti duomenų šaltiniams, kurie rodo didelį įrašų skaičių, grupuoti.

## <a name="memory-consumption"></a><a name="MemoryConsumption"></a> Atminties suvartojimas

Pagal numatytuosius nustatymus, **jei GroupBy** duomenų šaltinis yra paleistas atmintyje, programos serverio atmintis naudojama pagrindinio duomenų šaltinio, kuris priklauso kiekvienai aptiktai grupei kaip vienos grupės įrašai, įrašams saugoti. Norėdami sumažinti atminties suvartojimą, galite sulaikyti GroupBy **duomenų šaltinių įrašų saugojimą,** jei jie sukonfigūruoti skaičiuoti tik susudėtas funkcijas, o jų grupės įrašai apdorojimo laiku nenaudojami. Norėdami tokiu būdu sumažinti atminties suvartojimą, įgalinkite **ER** **naudoti mažiau atminties,** kai įrašų grupavimas naudojamas tik telkimo funkcijai, esančiai funkcijų valdymo darbo srityje, apskaičiuoti.

## <a name="alternatives"></a><a name="Alternatives"></a> Alternatyvų

Panašius telkimus galima apskaičiuoti naudojant [skirtingų](er-data-collection-data-sources.md#if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions) tipų duomenų šaltinius arba ER įdiegtas funkcijas.

Norėdami daugiau sužinoti apie šią funkciją, atlikite toliau pateiktą pavyzdį.

## <a name="example-use-a-groupby-data-source-for-aggregate-calculations-and-record-grouping"></a><a name="Example"></a> Pavyzdys: grupuojant skaičiavimus ir įrašų grupavimą naudoti GROUPBY duomenų šaltinį

Šis pavyzdys rodo, kaip sistemos administratoriaus arba elektroninio ataskaitų funkcinės konsultanto vaidmens vartotojas gali konfigūruoti ER **modelio susiejimą, kuriame yra GROUPBY** duomenų šaltinis, naudojamas sujungti funkcijas ir grupių įrašus. Šis modelio susiejimas naudojamas valdiklio ataskaitai spausdinti, kai sugeneruota Intrastat deklaracija. Ši ataskaita leidžia peržiūrėti paskelbtas Intrastat operacijas.

Šiame pavyzdyje pateiktas procedūras galima atlikti DEMF įmonėje **"** Microsoft Dynamics 365 Finance". 

### <a name="prepare-sample-data"></a>Duomenų pavyzdžio paruošimas

Įsitikinkite, kad Yra Intrastat operacijų ataskaitoms **Intrastat** puslapyje. Turite turėti skirtingų transportavimo kodų operacijas, nes šiame pavyzdyje operacijas **grupuosite pagal** lauką Transportavimas.

![Intrastat puslapio paruošimas Intrastat operacijoms.](./media/er-groupby-data-sources-prepare-transactions.png)

### <a name="configure-the-er-framework"></a>ER sistemos konfigūracija

Atlikite veiksmus, aprašytus skyriuje [Konfigūruoti ER sistemą](er-quick-start2-customize-report.md#ConfigureFramework), kad nustatytumėte minimalų ER parametrų rinkinį. Prieš pradėdami naudoti ER sistemą ER modelio susiejimui kurti, turite užbaigti šį nustatymą.

### <a name="import-the-standard-er-format-configuration"></a>Standartinio ER formato konfigūracijos importavimas

Norėdami įtraukti standartines [ER konfigūracijas į dabartinį "Dynamics 365 Finance" egzempliorių, atlikite standartinės ER](er-quick-start2-customize-report.md#ImportERSolution1) formato konfigūracijos importavimo veiksmus. Importuoti 1 Intrastat modelio **konfigūracijos** versiją iš saugyklos.

### <a name="create-a-custom-data-model-configuration"></a>Pasirinktinio duomenų modelio konfigūracijos kūrimas

Norėdami rankiniu būdu pridėti [naują](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration)**"Intrastat" modelio ("Litware")** ER duomenų modelio konfigūraciją, kurią išvedote iš importuoto "Intrastat **" modelio konfigūracijos, atlikite** nurodytus veiksmus.

### <a name="configure-a-custom-data-model-component"></a>Pasirinktinio duomenų modelio komponento konfigūravimas

Norėdami atlikti reikalingus išvestinio **"Intrastat" modelio ("Litware")** duomenų modelio pakeitimus, kad jį būtų galima naudoti norint rodyti transportavimo kodus, kurie turi reikiamą informaciją, atlikite šiuos veiksmus.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. **Konfigūracijos puslapyje**, konfigūracijos medyje, pasirinkite Intrastat modelį **(litware)**.
3. Pasirinkite **Dizaino įrankis**.
4. Modelio medžio **duomenų modelio dizainerio** puslapyje pasirinkite **Intrastat**.
5. Pasirinkite **Naujas,** jei norite pridėti naują įdėtą pasirinkto Intrastat mazgo **mazgą**. Iškrentančiame teksto laukelyje duomenų modelio mazgo įtraukimui, atlikite šiuos žingsnius:

    1. Lauke Pavadinimas **įveskite Transportavimas** **.**
    2. Lauke **Elemento tipas** pasirinkite **Įrašų sąrašas**.
    3. Pasirinkite **Įtraukti** tam, kad įtrauktumėte naują mazgą.

6. Pasirinkite **Naujas,** jei norite įtraukti naują įdėtojo mazgo transportuoti **mazgą**, kurį ką tik pridėjote. Iškrentančiame teksto laukelyje duomenų modelio mazgo įtraukimui, atlikite šiuos žingsnius:

    1. **Lauke Pavadinimas** įveskite **Kodą**.
    2. Lauke **Elemento tipas** pasirinkite **Eilutė**.
    3. Pasirinkite **Įtraukti** tam, kad įtrauktumėte naują mazgą.

7. Pasirinkite **Naujas,** kad pridėtumėte kitą naują įdėtą transportavimo mazgo **mazgą**. Iškrentančiame teksto laukelyje duomenų modelio mazgo įtraukimui, atlikite šiuos žingsnius:

    1. Lauke Pavadinimas **įveskite** **TotalInvoicedAmount**.
    2. Lauke **Elemento tipas** pasirinkite **Realusis skaičius**.
    3. Pasirinkite **Įtraukti** tam, kad įtrauktumėte naują mazgą.

8. Pasirinkite **Naujas,** kad pridėtumėte kitą naują įdėtą transportavimo mazgo **mazgą**. Iškrentančiame teksto laukelyje duomenų modelio mazgo įtraukimui, atlikite šiuos žingsnius:

    1. **Lauke Pavadinimas** įveskite **NumberOfTransactions**.
    2. Lauke **Elemento tipas** pasirinkite **Sveikasis skaičius**.
    3. Pasirinkite **Įtraukti** tam, kad įtrauktumėte naują mazgą.

9. Pasirinkite **Naujas,** kad pridėtumėte kitą naują įdėtą transportavimo mazgo **mazgą**. Iškrentančiame teksto laukelyje duomenų modelio mazgo įtraukimui, atlikite šiuos žingsnius:

    1. Lauke Pavadinimas **įveskite Operacija** **.**
    2. Lauke **Elemento tipas** pasirinkite **Įrašų sąrašas**.
    3. Pasirinkite **Įtraukti** tam, kad įtrauktumėte naują mazgą.

10. Ką tik **įtrauktame** Operacijos mazge, mazgo **·**"FastTab" pasirinkite Perjungti **prekės nuorodą**.
11. Duomenų modelio **medžio dialogo** lange Perjungti prekės nuorodą pasirinkite **CommodityRecord**. Tada pasirinkite **Gerai**.

![Konfigūruotas duomenų modelis ER duomenų modelio kūrimo įrankyje.](./media/er-groupby-data-sources-configure-data-model.png)

### <a name="complete-the-design-of-a-custom-data-model"></a>Pasirinktinio duomenų modelio dizaino kūrimas

Norėdami baigti išvestinio ["Intrastat" modelio (litware](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration))**duomenų modelio dizainą,** atlikite nurodytus veiksmus.

### <a name="create-a-new-model-mapping-configuration"></a>Sukurkite naują modelio žemėlapio konfigūravimą

Norėdami rankiniu būdu įtraukti [naują](er-quick-start1-new-solution.md#CreateModelMapping)**"Intrastat" modelių susiejimo ER** modelio susiejimo konfigūraciją į išvestinio "Intrastat **" modelio (litware) konfigūraciją, atlikite naujo modelio susiejimo konfigūracijos kūrimo** veiksmus.

### <a name="add-a-new-model-mapping-component"></a>Įtraukti naują modelio susiejimo komponentą

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. **Konfigūracijos puslapyje**, konfigūracijos medyje, išplėskite **Intrastat modelio konfigūraciją**.
3. **Pasirinkite Intrastat pavyzdžio susiejimo** konfigūraciją.
4. Norėdami atidaryti susiejimų sąrašą, pasirinkite **Dizaino įrankis**.
5. Norėdami pašalinti **esamą** susiejimo komponentą, pasirinkite Naikinti.
6. Norėdami įtraukti **naują** susiejimo komponentą, pasirinkite Naujas.
7. Apibrėžimo **lauke** pasirinkite **Intrastat**.
8. Lauke Pavadinimas **įveskite** Intrastat **susiejimą**.
9. Norėdami konfigūruoti **naują** susiejimą, pasirinkite konstruktorių.

### <a name="design-the-added-model-mapping-component"></a>Įtraukti modelio susiejimo komponento kūrimas

#### <a name="add-a-data-source-to-access-an-application-table"></a><a name="AddMmDataSource1"></a> Duomenų šaltinio įtraukimas, kad būtų galima pasiekti programos lentelę

Konfigūruoti duomenų šaltinį, kad būtų galima pasiekti programos lenteles, kuriose yra Intrastat operacijų informacija.

1. **Modelio žemėlapio kūrimo įrankis** puslapyje, **Duomenų šaltinio tipai** juostoje, pasirinkite **Dynamics 365 for Operations\\Lentelės įrašai**.
2. Duomenų šaltinių **srityje** pasirinkite Įtraukti šakninį **elementą**, kad įtraukumėte naują duomenų šaltinį, kuris bus naudojamas intrastat lentelei **pasiekti**. Kiekvienas Intrastat lentelės įrašas **vaizduoja** vieną Intrastat operaciją.
3. **Duomenų šaltinio ypatybės dialogo** lange, lauke **Pavadinimas**, įveskite **Operacija**.
4. **Lentelės lauke** įveskite **Intrastat**.
5. Pasirinkite **Gerai** tam, kad įtrauktumėte naują duomenų šaltinį.

#### <a name="add-a-data-source-to-group-intrastat-transactions"></a><a name="AddMmDataSource2"></a> Duomenų šaltinio įtraukimas į grupės Intrastat operacijas

Sukonfigūruokite **GroupBy** duomenų šaltinį, kad būtų galima grupuoti Intrastat operacijas ir apskaičiuoti sudėties funkcijas.

1. Modelio susiejimo dizainerio **puslapio duomenų šaltinio** tipų srityje **pasirinkite Funkcijos** **grupuoti pagal\\.**
2. Duomenų šaltinių **srityje** pasirinkite Įtraukti šakninį, kad įtraukumėte naują duomenų šaltinį, **kuris** bus naudojamas Intrastat operacijoms grupuoti ir sudėtinėms funkcijoms atlikti.
3. **Duomenų šaltinio ypatybės dialogo** lango lauke **Pavadinimas įveskite** **TransportRecord**.
4. Norėdami konfigūruoti **grupavimo sąlygas,** pasirinkite Redaguoti grupę.
5. Skirtuko Redaguoti **pagal parametrus puslapyje**, duomenų šaltinių sąraše, kuris yra dešinioje srityje, **pasirinkite** Operacijos duomenų šaltinį ir išplėskite jį.
6. Pasirinkite **Įtraukti lauką į \> grupę norėdami** **nurodyti**, kad operacijos duomenų šaltinis pasirinktas kaip pagrindinis sukonfigūruoto **GroupBy duomenų** <a name="BaseDataSource">šaltinio duomenų šaltinis</a>. Operacijos duomenų šaltinio **įrašai** bus sugrupuoti, ir šio duomenų šaltinio lauko vertės bus naudojamos skaičiavimams grupinėse funkcijose.
7. Pasirinkite **Sandoris\Transportas** lauką, tada pasirinkite **Pridėti lauką prie \> Sugrupuotas laukas** nurodyti, kad **Transportas** bazinio duomenų šaltinio laukas pasirenkamas kaip <a name="GroupingFields">grupavimo kriterijus</a> sukonfigūruotiems **Grupuoti pagal** duomenų šaltinis. Kitaip tariant, operacijos duomenų šaltinio **įrašai** bus sugrupuoti pagal lauko Transportavimas **vertę**. Kiekvienas sukonfigūruoto **GroupBy duomenų šaltinio** įrašas nurodo vieną transportavimo kodą, kuris rastas pagrindinio duomenų šaltinio įrašuose.
8. Pasirinkite lauką **Operacija\AmountMST**, tada atlikite šiuos veiksmus:

    1. Norėdami **nurodyti, kad \> bus skaičiuojama** šio lauko <a name="AggregateFunctions">su sujungti funkcija</a>, pasirinkite lauką Įtraukti.
    2. Telkimo **srityje**, įraše **, kuris įtrauktas į pasirinktą lauką Transaction\AmountMST**, **lauke** Metodas pasirinkite **sumos** funkciją.
    3. Lauke Pavadinimas **įveskite** **TotalInvoicedAmount**.

    Šie parametrai nurodo, kad kiekvienai transportavimo grupei bus skaičiuojama bendroji **lauko Operacija\AmountMST** suma.

9. Pasirinkite lauką **Transaction\RecId**, tada atlikite šiuos veiksmus:

    1. Norėdami **nurodyti, kad \> bus skaičiuojama** šio lauko su sujungti funkcija, pasirinkite lauką Įtraukti.
    2. Telkimo **srityje**, įraše **, kuris įtrauktas į pasirinktą lauką Transaction\RecId**,**lauke** Metodas pasirinkite skaičiavimo **funkciją**.
    3. Lauke Pavadinimas **įveskite** **NumberOfTransactions**.

    Šie parametrai nurodo, kad kiekvienai transportavimo grupei bus skaičiuojamas operacijų skaičius grupėje.

10. Pasirinkite **Įrašyti**.
11. Peržiūrėkite <a name="ExecutionLocation">redaguojamo</a> duomenų šaltinio vykdymo parametrus. Atkreipkite **dėmesį, kad** lauke Vykdymo vieta **buvo** automatiškai pasirinktas automatinis išjungimas, **o vykdymo lauke** yra SQL **vertė**. Šie parametrai nurodo, kad pasirinktas **operacijos pagrindinis** duomenų šaltinis šiuo metu yra užklausuojamas, **ir galite vykdyti redaguojamą GroupBy** duomenų šaltinį duomenų bazės lygiu.
12. Atidarykite vykdymo vietos lauko **peržvalgą**, kad peržiūrėtumėte galimų verčių sąrašą. Atkreipkite dėmesį, kad **galite pasirinkti užklausą** **·** **arba atmintyje, kad šis GroupBy** duomenų šaltinis būtų vykdomas duomenų bazės lygiu arba programos serverio atmintyje.
13. Pasirinkite **Įrašyti** ir uždarykite parametrų **puslapį Redaguoti 'Grupuoti pagal** '.
14. Pasirinkite **Gerai**, kad užbaigtumėte duomenų šaltinio **GroupBy** parametrus.

#### <a name="bind-the-groupby-data-source-to-data-model-fields"></a><a name="AddMmBindings"></a> Susieti GroupBy duomenų šaltinį su duomenų modelio laukais

Susiekite sukonfigūruotą duomenų šaltinį su duomenų modelio laukais, norėdami nurodyti, kaip duomenų modelis apdorojimo metu bus užpildytas programos duomenimis.

1. Modelio susiejimo **dizainerio** puslapio duomenų modelio **srityje** išplėskite transportavimo **mazgą**.
2. Duomenų šaltinių **srityje** išplėskite **TransportRecord duomenų** šaltinį.
3. Pridėti susiejimą, kad būtų rodomas aptiktų transportavimo grupių sąrašas:

    1. **Duomenų modelio srityje** pasirinkite transportavimo **prekę**.
    2. Duomenų šaltinių **srityje** pasirinkite **TransportRecord duomenų** šaltinį.
    3. Pasirinkite **Susieti**.

4. Pridėti susiejimą, kad būtų galima rodyti kiekvienos aptiktos transportavimo grupės transportavimo kodą:

    1. Pasirinkite transportavimo **kodo duomenų** modelio elementą.
    2. Pasirinkite sugrupuotą **TransportRecord.grouped.TransportMode** lauką.
    3. Pasirinkite **Susieti**.

5. Pridėti susiejimą, kad būtų galima rodyti kiekvienos aptiktos transportavimo grupės apskaičiuotų suvestinių funkcijų vertes:

    1. Pasirinkite Transport.NumberOfTransactions **duomenų** modelio elementą.
    2. Pasirinkite sudėtintį **lauką TransportRecord.aggregated.NumberOfTransactions**.
    3. Pasirinkite **Susieti**.
    4. **Pasirinkite Transport.TotalInvoicedAmount duomenų** modelio prekę.
    5. Pasirinkite lauką **TransportRecord.aggregated.TotalInvoicedAmount**, sujungtą.
    6. Pasirinkite **Susieti**.

6. Įtraukite susiejimą, kad operacijos įrašai, priklausantys kiekvienai aptiktai transportavimo grupei, būtų pateikti:

    1. Pasirinkite elementą **Transport.Transaction** duomenų modelis.
    2. Pasirinkite lauką **TransportRecord.lines**.
    3. Pasirinkite **Susieti**.

    **Galite toliau konfigūruoti Įdėtųjų Transport.Transaction** **duomenų modelio prekės ir TransportRecord.eilučių** duomenų šaltinio laukų susiejimus, kad apdorojimo metu būtų pateikta Intrastat operacijų, kurios priklauso kiekvienai aptiktai transportavimo grupei, informacija.

![Konfigūruotas žemėlapio modelis ER duomenų žemėlapio modelio kūrimo įrankyje.](./media/er-groupby-data-sources-configure-model-mapping.png)

### <a name="debug-the-added-model-mapping-component"></a>Derinti pridėto modelio susiejimo komponentą

Norėdami patikrinti [sukonfigūruotą modelio susiejimą naudokite](er-debug-data-sources.md) ER duomenų šaltinio derintuvą.

1. Modelio susiejimo **dizainerio** puslapyje pasirinkite Pradėti **derinti**.
2. Duomenų šaltinių **derinimo puslapyje**, kairiojoje srityje, **pasirinkite TransportRecord** duomenų šaltinį, tada pasirinkite Skaityti **visus įrašus**.
3. Išplėskite **TransportRecord duomenų** šaltinį, tada atlikite šiuos veiksmus:

    1. **Pasirinkite TransportRecord.grouped.TransportMode** duomenų šaltinį.
    2. Pasirinkti **Gauti reikšmę**.
    3. **Pasirinkite TransportRecord.grouped.NumberOfTransactions duomenų** šaltinį.
    4. Pasirinkti **Gauti reikšmę**.
    5. **Pasirinkite TransportRecord.grouped.TotalInvoicedAmount** duomenų šaltinį.
    6. Pasirinkti **Gauti reikšmę**.

4. Dešiniajame lange pasirinkite Išplėsti **viską**.

TransportRecord **duomenų** šaltinis parodo du įrašus ir pateikia du transportavimo kodus. Kiekvienam transportavimo kodui skaičiuojamas operacijų skaičius ir bendroji suma, už kurią išrašyta SF.

> [!NOTE]
> "panaudos skaitymo" būdas naudojamas, kai Duomenų šaltinis **GroupBy** iškvie čia optimizuoja duomenų bazės skambučius. Todėl kai kurios **GroupBy** duomenų šaltinio lauko vertės ER duomenų šaltinio derintuve skaičiuojamos tik tada, kai jos susiejamos su duomenų modelio laukais.

![Duomenų šaltinio derinimo rezultatai puslapyje Derinti duomenų šaltinius.](./media/er-groupby-data-sources-debug-datasource.png)

## <a name="frequently-asked-questions"></a>Dažniausiai užduodami klausimai

### <a name="is-there-any-way-to-calculate-grand-totals-when-the-group-totals-are-calculated"></a>Ar yra būdas skaičiuoti bendras sumas, kai skaičiuojamos grupės bendrosios sumos?

Taip. Norėdami apskaičiuoti bendras sumas, sukonfigūruokite **kitą GroupBy** **duomenų šaltinį, kuriame anksčiau sukonfigūruotas GroupBy** duomenų šaltinis naudojamas kaip pagrindinis duomenų šaltinis. Toliau esanti **iliustracija** **rodo GroupBy** **tipo bendrųjų sumų duomenų šaltinį, naudojamą skaičiuojant funkciją sujungti** **SUM**, **remiantis TransportRecord duomenų šaltinio TransportRecord** **duomenų šaltiniu, kuris yra GroupBy tipo**, sumavimu.

![Bendrųjų duomenų šaltinis ER modelio susiejimo konstruktoriuje.](./media/er-groupby-data-sources-configure-model-mapping2.png)

Toliau esanti iliustracija pateikia bendrųjų sumų **duomenų** šaltinio derinimo rezultatus.

![Bendrųjų sumų duomenų šaltinio derinimo rezultatai puslapyje Derinti duomenų šaltinius.](./media/er-groupby-data-sources-debug-datasource2.png)

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)
- [Įvykdyto ER formato duomenų šaltinių derinimas duomenų srautams ir transformacijai analizuoti](er-debug-data-sources.md)
- [DUOMENŲ RINKIMO duomenų šaltinių naudojimas elektroninių ataskaitų formatuose](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
