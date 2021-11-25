---
title: Gamybos vietos vykdymo sąsajos tinkinimas
description: Šioje temoje paaiškinama, kaip išplėsti dabartines formas arba sukurti naujas gamybos laiko vykdymo sąsajos formas ir mygtukus.
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-11-08
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 414fe5d6e16ad125bc2b9bb7ed427e5db5180ec9
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790984"
---
# <a name="customize-the-production-floor-execution-interface"></a>Gamybos vietos vykdymo sąsajos tinkinimas

[!include [banner](../includes/banner.md)]

Programuotojai gali išplėsti dabartines formas arba sukurti savo formas ir mygtukus gamybos laiko vykdymo sąsajai. Įtraukę šių naujų elementų kodą, administratoriai arba darbo laiko vadybininkai gali lengvai juos įtraukti į sąsają naudodami standartinius konfigūracijos valdiklius.

Pavyzdžiui, čia yra keletas galimų sprendimų, jei pagrindinėje formoje reikia naujų stulpelių:

- Išplėskite `JmgProductionFloorExecutionMainGrid` formą ir pridėkite norimus laukus.
- Sukurkite naują formą ir pridėkite ją kaip naują pagrindinį rodinį (skirtukas).

## <a name="add-a-new-button-action"></a>Įtraukti naują mygtuką (veiksmas)

Norėdami pridėti naują mygtuką (veiksmą), atlikite šiuos veiksmus, norėdami sukurti klasę, kuri vykdo jūsų pasirinktinį veiksmą.

1. Sukurkite naują klasę, `<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action` pavadintą, kur:

    - `<ExtensionPrefix>` unikaliai identifikuoja jūsų sprendimą, paprastai naudodamas jūsų įmonės pavadinimą.
    - `<ActionName>` yra unikalus klasės pavadinimas. Paprastai jis identifikuoja veiksmo rūšis.

1. Nauja klasė turi išplėsti `JmgProductionFloorExecutionAction` klasę.
1. Nepaisyti visų būtinų metodų.

Pavyzdžių ieškokite šių klasių kode:

- `JmgProductionFloorExecutionBreakAction`– paprasto veiksmo klasė, kuriai nereikia jokių įrašų.
- `JmgProductionFloorExecutionReportFeedbackAction`– klasė, kuri suteikia sudėtingesnę funkciją.

Kai baigiate, naujas mygtukas (veiksmas) bus automatiškai įrašytas į **"Microsoft" skirtukų** dizaino Dynamics 365 Supply Chain Management puslapį. Ten jūs (arba administratorius arba aukšto vadybininkas) galite lengvai pridėti ją prie pirminės arba antrinės įrankių juostos, kaip ir standartinių mygtukų pridėjimą. Instrukcijų ieškokite [Gamybos laiko vykdymo sąsajos](production-floor-execution-tabs.md) kūrimas.

## <a name="add-a-new-main-view"></a>Įtraukti naują pagrindinį rodinį

1. Sukurkite naują formą, turi esančią norimus elementus ir funkcijas. Nepamirškite, kad ši forma yra nauja, o ne plėtinys. Pavadinkite `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>` formą, kur:

    - `<ExtensionPrefix>` unikaliai identifikuoja jūsų sprendimą, paprastai naudodamas jūsų įmonės pavadinimą.
    - `<FormName>` yra unikalus formos pavadinimas.

1. Kurti meniu elementą, kuris `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>` pavadintas.
1. Sukurkite plėtinį, `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension` pavadintą Kur `getMainMenuItemsList` šis metodas buvo išplėstas, įtraukdami naują meniu elementą į sąrašą. Šis kodas rodo pavyzdį.

    ```xpp
    [ExtensionOf(classStr(JmgProductionFloorExecutionForm))]
    public final class <ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>_Extension{
        static public List getMainMenuItemsList()
        {
            List menuItemList = next getMainMenuItemsList();
            menuItemList.addEnd(menuItemDisplayStr(<ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>));
            return menuItemList;
        }
    ```

Kai baigsite, naujas pagrindinis rodinys bus automatiškai pateiktas tiekimo grandinės valdymo puslapio Dizaino skirtukai lauke Pagrindinis rodinys. **·** **·** Ten jūs (arba administratorius arba aukšto vadybininkas) galite lengvai pridėti jį prie naujų ar esamų skirtukų, kaip ir standartines pagrindines peržiūras. Instrukcijų ieškokite [Gamybos laiko vykdymo sąsajos](production-floor-execution-tabs.md) kūrimas.

## <a name="add-a-details-view"></a>Įtraukti informacijos rodinį

1. Sukurkite naują formą, turi esančią norimus elementus ir funkcijas. Atminkite, kad ši forma yra nauja, o ne plėtinys. Pavadinkite `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail` formą, kur: 

    - `<ExtensionPrefix>` unikaliai identifikuoja jūsų sprendimą, paprastai naudodamas jūsų įmonės pavadinimą.
    - `<FormName>` yra unikalus formos pavadinimas.

1. Kurti meniu elementą, kuris `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail` pavadintas.
1. Sukurkite plėtinį, `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension` pavadintą Kur `getDetailsMenuItemList` šis metodas buvo išplėstas, įtraukdami naują meniu elementą į sąrašą.

Kai baigiate, naujas išsamios informacijos rodinys bus automatiškai pateiktas tiekimo grandinės valdymo puslapio Dizainų skirtukų informacijos rodinio **·** combo **·** lauke. Ten jūs (arba administratorius arba laiko vadybininkas) galite lengvai pridėti jį prie naujų ar esamų skirtukų, kaip ir standartinių informacijos rodinių pridėjimą. Instrukcijų ieškokite [Gamybos laiko vykdymo sąsajos](production-floor-execution-tabs.md) kūrimas.

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

## <a name="additional-resources"></a>Papildomi ištekliai

- [Gamybos vietos vykdymo sąsajos stilius](production-floor-execution-styles.md)
- [Gamybos vietos vykdymo sąsajos kūrimas](production-floor-execution-tabs.md)
