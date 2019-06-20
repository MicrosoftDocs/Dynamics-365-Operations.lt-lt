---
title: Pasirinktinių laukų naudojimas „Microsoft Dynamics 365 Project Timesheet“ mobiliojoje programoje (sistemose „iOS“ ir „Android“)
description: Šioje temoje pateikiami įprasti plėtinių naudojimo diegiant pasirinktinius laukus būdai.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 4343c875da05641c57b7784bf52f1c814dd26d20
ms.sourcegitcommit: 19859d8566a8c7840066b2c10c6b08b67f1b83f4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2019
ms.locfileid: "1618001"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Pasirinktinių laukų naudojimas „Microsoft Dynamics 365 Project Timesheet“ mobiliojoje programoje (sistemose „iOS“ ir „Android“)

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiami įprasti plėtinių naudojimo diegiant pasirinktinius laukus būdai. Įtrauktos toliau nurodytos temos.

- Įvairių tipų duomenys, kuriuos palaiko pasirinktinių laukų sistema
- Kaip rodyti tik skaitomus arba redaguojamus laukus tabelio įrašuose ir įrašyti vartotojo pateiktas vertes duomenų bazėje
- Kaip rodyti tik skaitomus laukus tabelio antraštėje
- Kaip integruoti kitą pasirinktinę verslo logiką, kad būtų galima įvesti numatytąsias vertes laukuose ir atlikti papildomą tikrinimą

## <a name="audience"></a>Auditorija

Ši tema skirta kūrėjams, kurie integruoja savo pasirinktinius laukus į „Microsoft Dynamics 365 Project Timesheet“ mobiliąją programą, kuri pasiekiama „Apple iOS“ ir „Google. Android“. Daroma prielaida, kad skaitytojai yra susipažinę su X++ programavimo ir projektų tabelio funkcijomis.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Duomenų sutartis – klasė TSTimesheetCustomField X++

Klasė **TSTimesheetCustomField** yra X++ duomenų sutarties klasė, kuri nurodo informaciją apie pasirinktinį tabelio funkcijos lauką. Pasirinktinio lauko objektų sąrašai perduodami į TSTimesheetDetails duomenų sutartį ir TSTimesheetEntry duomenų sutartį, kad pasirinktiniai laukai būtų rodomi mobilioje programoje.

- **TSTimesheetDetails** – tabelio antraštės sutartis.
- **TSTimesheetEntry** – tabelio operacijos sutartis. Šių objektų, kurių projekto informacija ir **timesheetLineRecId** reikšmės sutampa, grupės sudaro eilutę.

### <a name="fieldbasetype-types"></a>fieldBaseType (tipai)

Ypatybė **FieldBaseType**, pateikta objekte **TsTimesheetCustom** nustato lauko, kuris rodomas programoje, tipą. Palaikomos toliau nurodytos **tipų** vertės.

| Tipų vertė | Tipas              | Pastabos |
|-------------|-------------------|-------|
| 0           | Eilutė (ir išvardijimas) | Laukas rodomas kaip teksto laukas. |
| 1           | Sveikasis skaičius           | Reikšmė rodoma kaip skaičius be dešimtainių vietų. |
| 2           | Tikrasis              | Reikšmė rodoma kaip skaičius su skaitmenimis po kablelio.<p>Norėdami programoje rodyti realiąją vertę kaip valiutą, naudokite ypatybę **fieldExtenededType**. Galite naudoti ypatybę **numberOfDecimals** norėdami nustatyti rodomų skaitmenų po kablelio skaičių.</p> |
| 3           | Data              | Datos formatai nustatomi pagal vartotojo parametrą **Datos, laiko ir skaičių formatas**, kuris nurodytas lango **Kalbos ir šalies / regiono nuostata** skiltyje **Vartotojo parinktys**. |
| 4           | Būlio logika           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Jei ypatybė **stringOptions** nėra pateikta objekte **TSTimesheetCustomField**, laisvos formos teksto laukas pateikiamas vartotojui.

    Ypatybė **stringLength** gali būti naudojama norint nustatyti maksimalų eilutės ilgį, kurį vartotojai gali įvesti.

- Jei ypatybė **stringOptions** pateikiama objekte **TSTimesheetCustomField**, šie sąrašo elementai yra vienintelės vertės, kurias vartotojai gali pasirinkti naudodami parinkčių mygtukus (išrinkimo mygtukus).

    Šiuo atveju eilutės laukas gali būti naudojamas kaip išvardijimo vertė vartotojui įvedant informaciją. Norėdami į duomenų bazę įrašyti vertę kaip išvardijimą, neautomatiniu būdu susiekite eilutės vertę su išvardijimo verte prieš įrašymą į duomenų bazę naudodami eiliškumo modelį (pavyzdžių žr. tolesniame šios temos skyriuje „Eiliškumo modelio naudojimas klasėje TSTimesheetEntryService norint įrašyti tabelio įrašą iš programos į duomenų bazę).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Šią ypatybę galite naudoti norėdami formatuoti realiąsias vertes kaip valiutą. Šis metodas taikomas tik kai lauko **fieldBaseType** vertė yra **Realusis**.

- **TSCustomFieldExtendedType:None** – formatavimas netaikomas.
- **TSCustomFieldExtendedType::Currency** – formatuokite vertę kaip valiutą

    Kai valiutos formatavimas aktyvus, laukas **stringValue** gali būti naudojamas norint perduoti valiutos kodą, kuris turėtų būti rodomas programoje. Vertė yra tik skaitoma vertė.

    Lauke **realValue** pateikiama pinigų suma, kuri turi būti įrašyta duomenų bazėje.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Šią ypatybę galite naudoti norėdami nurodyti, kuriose programos vietose pasirinktiniai laukai turėtų būti rodomi.

- **TSCustomFieldSection::Header** – laukas bus rodomas programos skiltyje **Peržiūrėti daugiau informacijos**. Šie laukai visada yra tik skaitomi.
- **TSCustomFieldSection::Line** – laukas bus rodomas po visais parengtais naudoti eilutės laukais tabelio įrašuose. Šie laukai gali būti redaguojami arba tik skaitomi.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Ši ypatybė identifikuoja lauką, kai vertės, kurias pateikia programa, yra įrašomos į duomenų bazę.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Ši ypatybė identifikuoja lauką, kai vertės, kurias pateikia programa, yra įrašomos į duomenų bazę.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Nustatykite šios ypatybės vertę **Taip**, kad nurodytumėte, jog lauką, esantį tabelio įrašo skiltyje, vartotojai galės redaguoti. Nustatykite ypatybės vertę **Ne**, jei laukas turi būti tik skaitomas.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Nustatykite šios ypatybės vertę **Taip**, kad nurodytumėte, jog laukas, esantis tabelio įrašo skiltyje, turi būti privalomas.

### <a name="label-str"></a>label (str)

Ši ypatybė nurodo žymę, kuri rodoma šalia lauko programoje.

### <a name="stringoptions-list-of-strings"></a>stringOptions (List of Strings)

Ši ypatybė taikoma tik kai nustatyta parametro **fieldBaseType** vertė **Eilutė**. Jei **stringOptions** nustatyta, eilutės vertes, kurias galima pasirinkti naudojant parinkčių mygtukus (išrinkimo mygtukus), nurodo eilutės sąraše. Jei eilutės nepateikiamos, laisvos formos įrašas eilutės lauke yra leistinas (pavyzdžių žr. tolesniame šios temos skyriuje „Eiliškumo modelio naudojimas klasėje TSTimesheetEntryService norint įrašyti tabelio įrašą iš programos į duomenų bazę).

### <a name="stringlength-int"></a>stringLength (int)

Ši ypatybė nurodo maksimalų eilutės lauko ilgį. Ji taikoma tik kai nustatyta parametro **fieldBaseType** vertė **Eilutė**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Ši ypatybė nurodo realiosios vertės lauke rodomų skaitmenų po kablelio skaičių. Ji taikoma tik kai nustatyta parametro **fieldBaseType** vertė **Realusis**.

### <a name="ordersequence-int"></a>orderSequence (int)

Ši ypatybė valdo tvarką, kuria pasirinktiniai laukai rodomi programoje, kai nurodytas daugiau kaip vienas pasirinktinis laukas. Pirmiau rodomi laukai, kurių skaičiai mažesni.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Tipo **Bulio logika** laukuose ši ypatybė perduoda lauko Bulio logikos vertę tarp serverio ir programos.

### <a name="guidvalue-guid"></a>guidValue (guid)

Tipo **GUID** laukuose ši ypatybė perduoda lauko visuotinai unikalų identifikatoriaus (GUID) vertę tarp serverio ir programos.

### <a name="int64value-int64"></a>int64Value (int64)

Tipo **Int64** laukuose ši ypatybė perduoda lauko „int64“ vertę tarp serverio ir programos.

### <a name="intvalue-int"></a>intValue (int)

Tipo **Int** laukuose ši ypatybė perduoda lauko „int“ vertę tarp serverio ir programos.

### <a name="realvalue-real"></a>realValue (real)

Tipo **Realusis** laukuose ši ypatybė perduoda lauko realiąją vertę tarp serverio ir programos.

### <a name="stringvalue-str"></a>stringValue (str)

Tipo **Eilutė** laukuose ši ypatybė perduoda lauko eilutės vertę tarp serverio ir programos. Ji taip pat naudojama tipo **Realusis** laukuose, kurie formatuojami kaip valiuta. Šiuose laukuose ypatybė naudojama perduodant valiutos kodą programai.

### <a name="datevalue-date"></a>dateValue (date)

Tipo **Data** laukuose ši ypatybė perduoda lauko datos vertę tarp serverio ir programos.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Pasirinktinio lauko rodymas ir įrašymas tabelio įrašo skiltyje

Toliau pateikiama mobiliosios programos tabelio įrašo kūrimo ekrano kopija. Joje galima matyti parengtus naudoti laukus ir skiltyje Laiko įrašas pateiktą pasirinktinį pavadinimu Tikrinimo eilutė, kai tipo Antroji parinktis išvardijimo vertė jau nustatyta.

![Tikrinimo eilutės pasirinktinis laukas programoje](media/timesheet-entry.jpg)



Toliau pateikiama mobiliosios programos ekrano kopija, kurioje vartotojas pasirinko vieną iš išvardijimo parinkčių, kurios pateikiamos pasirinktiniame lauke Tikrinimo eilutė.  Šios pasirinktys yra Pirmoji parinktis ir Antroji parinktis, rodomos kaip išrinkimo mygtukai. Šiuo metu pasirinkta antroji parinktis.

![Tikrinimo eilutės pasirinktinio lauko parinkčių mygtukai (išrinkimo mygtukai)](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Lentelės TSTimesheetLine išplėtimas, kad joje būtų pasirinktinis laukas

Esant įprastam scenarijui, tikėtina, kad lentelėje TSTimesheetLine bus įrašytas pasirinktinis laukas, esantis tabelio įrašo skiltyje. Tačiau galima naudoti kitas lenteles, jei duomenis galima nuskaityti pagal pateiktą TSTimesheetTrans įrašą arba jei nėra konkretaus įrašo konteksto (pvz., projekto parametruose laukas nustatytas kaip tik skaitomas).

Atkreipkite dėmesį, kad pasirinktiniuose laukuose neprivalo būti jokių atsarginių duomenų bazės įrašų. Jie gali būti dinamiškai generuojami pagal X++ logiką. Šis metodas gali būti naudingas tik skaitomų laukų scenarijuose (dinamiškai generuojamų pasirinktinių laukų verčių pavyzdžių žr. tolesniame šios temos skyriuje „Eiliškumo modelio naudojimas klasėje TSTimesheetDetails, metode buildCustomFieldListForHeader norint užpildyti tabelio informaciją“).

Toliau pateikta „Visual Studio“ programos objektų medžio ekrano kopija. Joje rodomas lentelės TSTimesheetLine plėtinys ir laukas TestLineString, įtrauktas kaip pasirinktinis laukas.

![Eilutės eilutė](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Norėdami rodyti lauką tabelio įrašo skiltyje naudokite eiliškumo modelį klasės buildCustomFieldList metode TSTimesheetSettings.

Šis kodas valdo programos lauko rodymo parametrus. Pavyzdžiui, jis valdo lauko tipą, žymą, nustatymus, nurodančius, ar šis laukas yra privalomas ir kokioje skiltyje laukas rodomas.

Toliau pateiktame pavyzdyje rodomas eilutės laukas laiko įrašuose. Šiame lauke yra dvi parinktys, **Pirmoji parinktis** ir **Antroji pasirinktis**, kurios pateikiamos naudojant parinkčių mygtukus (išrinkimo mygtukus). Programos laukas yra susietas lauku **TestLineString**, kuris yra įtrauktas į lentelę TSTimesheetLine.

Atkreipkite dėmesį, kad galite naudoti metodą **TSTimesheetCustomField::newFromMetatdata()** norėdami supaprastinti pasirinktinių laukų ypatybių inicijavimą: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** ir **numberOfDecimals**. Šiuos parametrus taip pat galite nustatyti neautomatiniu būdu, kaip pageidaujate.

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Eiliškumo modelio naudojimas klasės TSTimesheetEntry metode buildCustomFieldListForEntry norint įvesti vertes į tabelio įrašą.

Metodas **buildCustomFieldListForEntry** naudojamas norint įvesti vertes įrašytose tabelio eilutėse mobilioje programoje. Įrašas TSTimesheetTrans naudojamas kaip parametras. Šio įrašo laukai gali būti naudojami norint užpildyti pasirinktinę lauko vertę programoje.

```
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Eiliškumo modelio naudojimas klasėje TSTimesheetEntryService norint įrašyti tabelio įrašą iš programos į duomenų bazę

Norėdami įrašyti pasirinktinį lauką į duomenų bazę įprasto naudojimo sąlygomis, turite išplėsti kelis toliau nurodytus metodus.

- Metodas **timesheetLineNeedsUpdating** naudojamas siekiant nustatyti, ar vartotojas pakeitė eilutės įrašą programoje, ir turi būti įrašytas į duomenų bazę. Jei našumas nėra svarbu, šį metodą galima supaprastinti, kad jis visuomet pateiktų **true**.
- Metodus **populateTimesheetLineFromEntryDuringCreate** ir **populateTimesheetLineFromEntryDuringUpdate** galima išplėsti, kad jie įvestų vertes duomenų bazės įraše TSTimesheetLine iš pateikto duomenų sutarties įrašo TSTimesheetEntry. Toliau pateiktame pavyzdyje atkreipkite dėmesį, kaip duomenų bazės lauko ir įrašo lauko susiejimas atliekamas neautomatiniu būdu naudojant X++ kodą.
- Metodą **populateTimesheetWeekFromEntry** taip pat galima išplėsti, jei pasirinktinis laukas, kuris yra susietas su objektu **TSTimesheetEntry**, tiro būti įrašytas į duomenų bazės lentelę TSTimesheetLineweek.

> [!NOTE]
> Toliau pateiktame pavyzdyje įrašoma vertė **firstOption** arba **firstOption**, kurią vartotojas pasirenka duomenų bazėje kaip neapdorotą eilutės vertę. Jei duomenų bazės laukas yra tipo **Išvardijimas** laukas, šias vertes galima neautomatiniu būdu susieti su išvardijimo verte ir įrašyti į duomenų bazės lentelės išvardijimo lauką.

```
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Pasirinktinio lauko rodymas tabelio antraštės skiltyje

Toliau pateikiama mobiliosios programos tabelio vartotojo peržiūra. Mygtukas Daugiau informacijos pasirinktas viršutiniame dešiniajame kampe, kad būtų rodoma parinktis Rodyti daugiau informacijos.  

![Papildomos informacijos komandos peržiūra](media/show-more.png)



Toliau pateikiama mobiliosios programos tabelio skilties Daugiau peržiūra. Pasirinktinis laukas pavadinimu Šio tabelio naudojimo koeficientas (apskaičiuotas pasirinktinis laukas) buvo įtrauktas į tabelio antraštės skiltį. Tik skaitoma vertė 0,667 nustatoma pasirinktiniame lauke.

![Skiltis Daugiau](media/more-section.jpg)



### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Lentelės TSTimesheetTable išplėtimas, kad joje būtų pasirinktinis laukas

Esant įprastam scenarijui, tikėtina, kad pasirinktinis laukas, esantis antraštės skiltyje, bus nuskaitytas iš lentelės TSTimesheetHeader. Tačiau galima naudoti kitas lenteles, jei duomenis galima nuskaityti pagal pateiktą TSTimesheetTable įrašą arba jei nėra konkretaus įrašo konteksto (pvz., projekto parametruose laukas nustatytas kaip tik skaitomas).

Atkreipkite dėmesį, kad pasirinktiniuose laukuose neprivalo būti jokių atsarginių duomenų bazės įrašų. Jie gali būti dinamiškai generuojami pagal X++ logiką. Šis metodas nurodytas tolesniame pavyzdyje.

Antraštės skilties laukai programoje visada tik skaitomi.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Norėdami rodyti lauką antraštės skiltyje naudokite eiliškumo modelį klasės buildCustomFieldList metode TSTimesheetSettings.

Šis kodas valdo programos lauko rodymo parametrus. Pavyzdžiui, jis valdo lauko tipą, žymą, nustatymus, nurodančius, ar šis laukas yra privalomas ir kokioje skiltyje laukas rodomas.

Toliau pateiktame pavyzdyje rodoma apskaičiuota vertė programos antraštės skiltyje.

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Eiliškumo modelio naudojimas klasės TSTimesheetDetails metode buildCustomFieldListForHeader norint užpildyti tabelio informaciją

Metodas **buildCustomFieldListForHeader** naudojamas norint užpildyti tabelio antraštės informaciją mobilioje programoje. Įrašas TSTimesheetTable naudojamas kaip parametras. Šio įrašo laukai gali būti naudojami norint užpildyti pasirinktinę lauko vertę programoje. Toliau pateiktame pavyzdyje nenuskaitomos jokios vertės iš duomenų bazės. Tačiau naudojama X++ logika siekiant generuoti apskaičiuotą vertę, kuri rodoma programoje.


```
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Kitos konfigūravimo / išplėtimo galimybės

### <a name="adding-additional-validation-for-the-app"></a>Papildomo programos tikrinimo įtraukimas

Esama tabelio funkcijos logika duomenų bazės lygiu vis tiek veiks, kaip tikėtasi. Norėdami nutraukti įrašymo arba pateikimo operacijų užbaigimą ir rodyti konkretų klaidos pranešimą, galite įtraukti kodą **throw error("message to user")** naudodami eiliškumo modelio plėtinį. Toliau pateikti naudingų išplečiamų metodų pavyzdžiai.

- Jei lentelės TSTimesheetLine parametras **validateWrite** pateikia **false** tabelio eilutės įrašymo operacijos metu, mobiliojoje programoje rodomas klaidos pranešimas.
- Jei lentelės TSTimesheetTable parametras **validateSubmit** pateikia **false** tabelio pateikimo programoje metu, vartotojui rodomas klaidos pranešimas.
- Logika, pagal kurią užpildomi laukai (pvz., **Eilutės ypatybė**) naudojant **įterpimo** metodą lentelėje TSTimesheetLine, vis tiek veiks.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Parengtų naudoti laukų slėpimas ir žymėjimas tik skaitomais naudojant konfigūraciją

Projekto parametruose galite nustatyti, kad parengti naudoti laukai būtų tik skaitomi arba paslėpti mobiliojoje programoje. Parinktis nustatykite puslapio **Projekto valdymo ir apskaitos parametrai** skirtuko **Tabelis** skiltyje **Mobilieji tabeliai**.

![Projekto parametrai](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Veiklų, kurias galima pasirinkti naudojant plėtinius, keitimas

Projekto veiklos, kurias galima pasirinkti, užpildomos naudojant metodus **getActivitiesForProject()** bei **getActivityQuery()** ir klasę **TsTimesheetProjectService**. Norėdami keisti šį veikimą, kad veiklos, kurias galima pasirinkti konkrečiame projekte, atitiktų jūsų verslo scenarijų, galite naudoti eiliškumo modelį.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Numatytosios projekto kategorijos įvedimas tabelio įrašuose

Numatytosios projekto kategorijos įrašymas tabelio įrašuose vykdomas trimis lygiais. Galite naudoti eiliškumo metodą, kad koreguotumėte veikimą bet kuriame arba visuose šiuose lygiuose ir užtikrintumėte pageidaujamą veikimą. Naudojama toliau nurodyta hierarchija.

1. Programa bando pateikti numatytąją kategoriją iš projekto ištekliaus. Ši numatytoji kategorija nustatyta klasės **TSTimesheetSettingsService** metoduose **getCurrentUserResource** ir **getDelegatedResourcesForCurrentUser**.
2. Jei numatytoji kategorija nepateikta projekto išteklių lygiu, programa bandys nuskaityti ją iš projekto veiklos. Ši numatytoji kategorija nustatoma klasės **TSTimesheetProjectService** metode **getActivitiesForProject**.
3. Jei numatytoji kategorija nepateikta projekto veiklos lygiu, numatytoji kategorija nuskaitoma projekto parametrų. Ši numatytoji kategorija nustatoma klasės **TSTimesheetProjectService** metode **getProjectDetailsbyRule**.
