---
title: Gamybos vietos vykdymo sąsajos tinkinimas
description: Šiame straipsnyje paaiškinama, kaip išplėsti dabartines formas arba sukurti naujas formas ir mygtukus gamybos laiko vykdymo sąsajai.
author: johanhoffmann
ms.date: 05/04/2022
ms.topic: article
ms.search.form: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-11-08
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 13fa6c2f3c30a820585d1b5a758f57ec563664d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845988"
---
# <a name="customize-the-production-floor-execution-interface"></a>Gamybos vietos vykdymo sąsajos tinkinimas

[!include [banner](../includes/banner.md)]

Programuotojai gali išplėsti dabartines formas arba sukurti savo formas ir mygtukus gamybos laiko vykdymo sąsajai. Įtraukę šių naujų elementų kodą, administratoriai arba darbo laiko vadybininkai gali lengvai juos įtraukti į sąsają naudodami standartinius konfigūracijos valdiklius.

Pavyzdžiui, čia yra keletas galimų sprendimų, jei pagrindinėje formoje reikia naujų stulpelių:

- Išplėskite `JmgProductionFloorExecutionMainGrid` formą ir pridėkite norimus laukus.
- Sukurkite naują formą ir pridėkite ją kaip naują pagrindinį rodinį (skirtukas).

## <a name="add-a-new-button-action"></a>Įtraukti naują mygtuką (veiksmas)

Norėdami pridėti naują mygtuką (veiksmą), atlikite šiuos veiksmus, norėdami sukurti klasę, kuri vykdo jūsų pasirinktinį veiksmą.

1. Sukurkite naują klasę, pavadintą `<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action`, kur:

    - `<ExtensionPrefix>` unikaliai identifikuoja jūsų sprendimą, paprastai naudodamas jūsų įmonės pavadinimą.
    - `<ActionName>` yra unikalus klasės pavadinimas. Paprastai jis identifikuoja veiksmo rūšis.

1. Nauja klasė turi išplėsti klasę `JmgProductionFloorExecutionAction`.
1. Nepaisyti visų būtinų metodų.

Pavyzdžių ieškokite šių klasių kode:

- `JmgProductionFloorExecutionBreakAction`– paprasto veiksmo klasė, kuriai nereikia jokių įrašų.
- `JmgProductionFloorExecutionReportFeedbackAction`– klasė, kuri suteikia sudėtingesnę funkciją.

Kai baigiate, naujas mygtukas (veiksmas) bus automatiškai įrašytas į " **Microsoft" skirtukų dizaino** puslapį Dynamics 365 Supply Chain Management. Ten jūs (arba administratorius arba aukšto vadybininkas) galite lengvai pridėti ją prie pirminės arba antrinės įrankių juostos, kaip ir standartinių mygtukų pridėjimą. Instrukcijų ieškokite Gamybos [laiko vykdymo sąsajos kūrimas](production-floor-execution-tabs.md).

## <a name="add-a-new-main-view"></a>Įtraukti naują pagrindinį rodinį

1. Sukurkite naują formą, turi esančią norimus elementus ir funkcijas. Nepamirškite, kad ši forma yra nauja, o ne plėtinys. Pavadinkite formą `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`, kur:

    - `<ExtensionPrefix>` unikaliai identifikuoja jūsų sprendimą, paprastai naudodamas jūsų įmonės pavadinimą.
    - `<FormName>` yra unikalus formos pavadinimas.

1. Kurti meniu elementą, kuris pavadintas `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`.
1. Sukurkite plėtinį, pavadintą `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension` Kur `getMainMenuItemsList` šis metodas buvo išplėstas, įtraukdami naują meniu elementą į sąrašą. Šis kodas rodo pavyzdį.

    ```xpp
    [ExtensionOf(classStr(JmgProductionFloorExecutionMenuItemProvider))]
    public final class <ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>_Extension{
        static public List getMainMenuItemsList()
        {
            List menuItemList = next getMainMenuItemsList();
            menuItemList.addEnd(menuItemDisplayStr(<ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>));
            return menuItemList;
        }
    ```

Kai baigsite, naujas pagrindinis **rodinys** **bus** automatiškai pateiktas tiekimo grandinės valdymo puslapio Dizaino skirtukai lauke Pagrindinis rodinys. Ten jūs (arba administratorius arba aukšto vadybininkas) galite lengvai pridėti jį prie naujų ar esamų skirtukų, kaip ir standartines pagrindines peržiūras. Instrukcijų ieškokite Gamybos [laiko vykdymo sąsajos kūrimas](production-floor-execution-tabs.md).

## <a name="add-a-details-view"></a>Įtraukti informacijos rodinį

1. Sukurkite naują formą, turi esančią norimus elementus ir funkcijas. Atminkite, kad ši forma yra nauja, o ne plėtinys. Pavadinkite formą `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`, kur: 

    - `<ExtensionPrefix>` unikaliai identifikuoja jūsų sprendimą, paprastai naudodamas jūsų įmonės pavadinimą.
    - `<FormName>` yra unikalus formos pavadinimas.

1. Kurti meniu elementą, kuris pavadintas `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`.
1. Sukurkite plėtinį, pavadintą `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension` Kur `getDetailsMenuItemList` šis metodas buvo išplėstas, įtraukdami naują meniu elementą į sąrašą.

Kai baigiate, naujas išsamios informacijos rodinys **bus automatiškai pateiktas tiekimo grandinės valdymo puslapio** Dizainų skirtukų informacijos rodinio combo **lauke**. Ten jūs (arba administratorius arba laiko vadybininkas) galite lengvai pridėti jį prie naujų ar esamų skirtukų, kaip ir standartinių informacijos rodinių pridėjimą. Instrukcijų ieškokite Gamybos [laiko vykdymo sąsajos kūrimas](production-floor-execution-tabs.md).

## <a name="add-a-numeric-keypad-to-a-form-or-dialog"></a>Įtraukti skaitinę klavišo klaviatūrą į formą arba dialogą

Toliau pateikiamas pavyzdys rodo, kaip į formą pridėti skaičių klaviatūras.

1. Skaičių klaviatūros valdiklių skaičius, kurį turi sudaryti kiekviena forma, turi būti lygus šioje formoje skaitinių klavišų skaičių.

    ```xpp
    private JmgProductionFloorExecutionNumpadController   numpadController1;
    private JmgProductionFloorExecutionNumpadController   numpadController2;
    private JmgProductionFloorExecutionNumpadController   numpadController3;
    ```

1. Nustatykite kiekvieno skaičių klaviatūros valdiklio elgseną ir kiekvieną skaičių klaviatūros valdiklį prijunkite prie skaičių klaviatūros formos dalies.

    ```xpp
    /// <summary>
    /// Initializes all numpad controllers, defines their behavior and connects them with numpad form parts.
    /// </summary>
    public void initializeNumpadController()
    {
        numpadController1 = new JmgProductionFloorExecutionNumpadController();
        numpadController1.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_1);
        QuantityNumpad1.getPartFormRun().setNumpadController(numpadController1);
    
        numpadController2 = new JmgProductionFloorExecutionNumpadController();
        numpadController2.parmNumpadEnabled(false);
        numpadController2.parmNumpadValue(333.56);
        numpadController2.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_2);
        QuantityNumpad2.getPartFormRun().setNumpadController(numpadController2);
    }
    ```

## <a name="use-a-numeric-keypad-as-a-pop-up-dialog"></a>Skaitinės klaviatūros klaviatūrą naudoti kaip laikinąjį dialogo langą

Toliau pateiktas pavyzdys parodo vieną būdą skaitinio klaviatūros valdiklio nustatyti laikinam dialogo langui.

```xpp
private void setupNumpadController()
{
    numpadController = new JmgProductionFloorExecutionNumpadController();
    numpadController.parmShouldNumpadShowOkCancelButtons(true);
    numpadController.setNumpadValueToParentFormDelegate += eventhandler(this.setQtyValueFromNumpad);
}
```

Toliau pateikiamas pavyzdys rodo vieną būdą iškviesti skaitinį klaviatūros laikinąjį langą.

```xpp
Args args = new Args();
args.name(formstr(JmgProductionFloorExecutionNumpad));
args.menuItemName(menuItemDisplayStr(JmgProductionFloorExecutionNumpad));
args.caller(element);
Object formRun = classfactory.formRunClass(args);
formRun.init();
formRun.setNumpadController(numpadController);
numpadController.setValueToNumpad(333.56);
formRun.run();
```

## <a name="add-a-date-and-time-controls-to-a-form-or-dialog"></a>Datos ir laiko valdiklių pridėjimas prie formos arba dialogo

Šiame skyriuje rodoma, kaip pridėti datos ir laiko valdiklius prie formos ar dialogo lango. Jutikliniai datos ir laiko valdikliai įgalina darbuotojus nurodyti datas ir laiką. Toliau pateiktuose ekrano nuotraukaose parodyta, kaip valdikliai paprastai rodomi puslapyje. Laiko valdiklis pateikia ir 12 valandų, ir 24 valandų versijas; rodoma versija bus nustatyta pagal vartotojo abonemento, kuriame veikia sąsaja, nuostatų rinkinį.

![Datos valdiklio pavyzdys.](media/pfe-customize-date-control.png "Datos kontrolės pavyzdys")

![Laiko kontrolės pavyzdys su 12 valandų laikrodžiu.](media/pfe-customize-time-control-12h.png "Laiko kontrolės pavyzdys su 12 valandų laikrodžiu")

![Laiko kontrolės pavyzdys su 24 valandų laikrodžiu.](media/pfe-customize-time-control-24h.png "Laiko kontrolės pavyzdys su 24 valandų laikrodžiu")

Toliau pateiktoje procedūroje pateikiamas pavyzdys, kaip prie formos pridėti datą ir laiko valdiklius.

1. Prie formos pridėkite valdiklį kiekvienam datos ir laiko valdikliui, kuris turi būti formoje. (Valdiklių skaičius turi sulygiti formos datos ir laiko valdiklių skaičių.)

    ```xpp
    private JmgProductionFloorExecutionDateTimeController  dateFromController; 
    private JmgProductionFloorExecutionDateTimeController  dateToController; 
    private JmgProductionFloorExecutionDateTimeController  timeFromController; 
    private JmgProductionFloorExecutionDateTimeController  timeToController;
    ```

1. Deklaruoti būtinus kintamuosius (tipo `utcdatetime`).

    ```xpp
    private utcdatetime fromDateTime;
    private utcdatetime toDateTime;
    ```

1. Kurti metodus, kuriuose datos ir laiko atnaujinimas bus atnaujintas datos ir laiko valdiklių. Šiame pavyzdyje rodomas vienas toks metodas.

    ```xpp
    private void setFromDateTime(utcdatetime _value)
        {
            fromDateTime = _value;
        }
    ```

1. Nustatykite kiekvieno datos ir laiko valdiklio elgseną ir sujunkite kiekvieną valdiklį su formos dalimi. Toliau pateikiamas pavyzdys rodo, kaip nustatyti datos nuo ir laiko pradžios valdiklių duomenis. Galite pridėti panašų datos ir laiko pabaigos valdiklių kodą (nerodoma).

    ```xpp
    /// <summary>
    /// Initializes all date and time controllers, defines their behavior, and connects them with the form parts.
    /// </summary>
    private void initializeDateControlControllers()
    {
        dateFromController = new JmgProductionFloorExecutionDateTimeController();
        dateFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        dateFromController.parmDateTimeValue(fromDateTime);
    
        timeFromController = new JmgProductionFloorExecutionDateTimeController();
        timeFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        timeFromController.parmDateTimeValue(fromDateTime);
        
        DateFromFormPart.getPartFormRun().setDateControlController(dateFromController, timeFromController);
        TimeFromFormPart.getPartFormRun().setTimeControlController(timeFromController, dateFromController);
        
        ...

    }
    ```

    Jei jums reikia datos kontrolės, galite praleisti laiko kontrolės nustatymą ir vietoj jo tiesiog nustatyti datos valdiklį, kaip parodyta šiame pavyzdyje:

    ```xpp
    {
        dateFromController = new JmgProductionFloorExecutionDateTimeController();
        dateFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        dateFromController.parmDateTimeValue(fromDateTime);
    
        DateFromFormPart.getPartFormRun().setDateControlController(dateFromController, null);
    }
    ```

## <a name="additional-resources"></a>Papildomi ištekliai

- [Gamybos vietos vykdymo sąsajos stilius](production-floor-execution-styles.md)
- [Gamybos vietos vykdymo sąsajos kūrimas](production-floor-execution-tabs.md)
