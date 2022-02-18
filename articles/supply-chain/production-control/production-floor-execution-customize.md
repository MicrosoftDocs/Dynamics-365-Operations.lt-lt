---
title: Gamybos vietos vykdymo sąsajos tinkinimas
description: Šioje temoje paaiškinama, kaip išplėsti esamas formas arba sukurti naujas formas ir mygtukus gamybos aukšto vykdymo sąsajai.
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
ms.openlocfilehash: 67fb381cbef6f1673afcaa834666b4a859bdf4e6
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066551"
---
# <a name="customize-the-production-floor-execution-interface"></a>Gamybos vietos vykdymo sąsajos tinkinimas

[!include [banner](../includes/banner.md)]

Kūrėjai gali išplėsti esamas formas arba sukurti savo formas ir mygtukus gamybos grindų vykdymo sąsajai. Pridėjus šių naujų elementų kodą, administratoriai arba parduotuvės vadovai gali lengvai įtraukti juos į sąsają naudodami standartinius konfigūracijos valdiklius.

Pavyzdžiui, čia yra keletas galimų sprendimų, jei reikia naujų stulpelių pagrindinėje formoje:

- Išplėskite`JmgProductionFloorExecutionMainGrid` formą ir pridėkite norimus laukus.
- Sukurkite naują formą ir pridėkite ją kaip naują pagrindinį rodinį (skirtuką).

## <a name="add-a-new-button-action"></a>Pridėti naują mygtuką (veiksmas)

Norėdami pridėti naują mygtuką (veiksmą), atlikite šiuos veiksmus, kad sukurtumėte klasę, kuri įgyvendina jūsų pasirinktinį veiksmą.

1. Sukurkite naują klasę, pavadintą`<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action`, kur:

    - `<ExtensionPrefix>` unikaliai identifikuoja jūsų sprendimą, paprastai naudojant jūsų įmonės pavadinimą.
    - `<ActionName>` yra unikalus klasės pavadinimas. Paprastai tai nurodo veiksmo rūšį.

1. Naujoji klasė turi išplėsti`JmgProductionFloorExecutionAction` klasė.
1. Nepaisykite visų būtinų metodų.

Norėdami gauti pavyzdžių, pažiūrėkite į šių klasių kodą:

- `JmgProductionFloorExecutionBreakAction`– Klasė paprastam veiksmui, kuriam nereikia jokių įrašų.
- `JmgProductionFloorExecutionReportFeedbackAction`– Klasė, teikianti sudėtingesnes funkcijas.

Kai baigsite, naujas mygtukas (veiksmas) bus automatiškai pateiktas sąraše **Dizaino skirtukai** puslapis Microsoft Dynamics 365 Supply Chain Management. Čia jūs (arba administratorius ar aukšto valdytojas) galite lengvai įtraukti jį į pirminę ar antrinę įrankių juostą, kaip galite pridėti standartinius mygtukus. Instrukcijas žr [Sukurkite gamybos grindų vykdymo sąsają](production-floor-execution-tabs.md).

## <a name="add-a-new-main-view"></a>Pridėti naują pagrindinį vaizdą

1. Sukurkite naują formą su norimais elementais ir funkcionalumu. Atminkite, kad ši forma yra nauja forma, o ne plėtinys. Pavadinkite formą`<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`, kur:

    - `<ExtensionPrefix>` unikaliai identifikuoja jūsų sprendimą, paprastai naudojant jūsų įmonės pavadinimą.
    - `<FormName>` yra unikalus formos pavadinimas.

1. Sukurkite meniu elementą, pavadintą `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`.
1. Sukurkite plėtinį, pavadintą`<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, kur`getMainMenuItemsList` metodas pratęsiamas įtraukiant į sąrašą naują meniu elementą. Šis kodas rodo pavyzdį.

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

Kai baigsite, naujas pagrindinis vaizdas bus automatiškai pateiktas sąraše **Pagrindinis vaizdas** kombinuotasis langelis **Dizaino skirtukai** Tiekimo grandinės valdymo puslapyje. Čia jūs (arba administratorius ar aukšto valdytojas) galite lengvai pridėti jį prie naujų ar esamų skirtukų, kaip galite pridėti standartinius pagrindinius rodinius. Instrukcijas žr [Sukurkite gamybos grindų vykdymo sąsają](production-floor-execution-tabs.md).

## <a name="add-a-details-view"></a>Pridėkite išsamios informacijos rodinį

1. Sukurkite naują formą su norimais elementais ir funkcionalumu. Atminkite, kad ši forma yra nauja, o ne plėtinys. Pavadinkite formą`<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`, kur: 

    - `<ExtensionPrefix>` unikaliai identifikuoja jūsų sprendimą, paprastai naudojant jūsų įmonės pavadinimą.
    - `<FormName>` yra unikalus formos pavadinimas.

1. Sukurkite meniu elementą, pavadintą `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`.
1. Sukurkite plėtinį, pavadintą`<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, kur`getDetailsMenuItemList` metodas pratęsiamas įtraukiant į sąrašą naują meniu elementą.

Kai baigsite, naujas išsamios informacijos rodinys bus automatiškai pateiktas sąraše **Išsamios informacijos vaizdas** kombinuotasis langelis **Dizaino skirtukai** Tiekimo grandinės valdymo puslapyje. Čia jūs (arba administratorius ar aukšto valdytojas) galite lengvai pridėti jį prie naujų ar esamų skirtukų, kaip galite pridėti standartinius išsamios informacijos rodinius. Instrukcijas žr [Sukurkite gamybos grindų vykdymo sąsają](production-floor-execution-tabs.md).

## <a name="add-a-numeric-keypad-to-a-form-or-dialog"></a>Pridėkite skaičių klaviatūrą prie formos arba dialogo lango

Šiame pavyzdyje parodyta, kaip prie formos pridėti skaičių klaviatūras.

1. Kiekvienoje formoje esančių skaičių klaviatūros valdiklių skaičius turi būti lygus toje formoje esančių skaičių klaviatūrų skaičiui.

    ```xpp
    private JmgProductionFloorExecutionNumpadController   numpadController1;
    private JmgProductionFloorExecutionNumpadController   numpadController2;
    private JmgProductionFloorExecutionNumpadController   numpadController3;
    ```

1. Nustatykite kiekvieno skaičių klaviatūros valdiklio veikimą ir kiekvieną skaičių klaviatūros valdiklį prijunkite prie skaitmeninės klaviatūros formos dalies.

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

## <a name="use-a-numeric-keypad-as-a-pop-up-dialog"></a>Naudokite skaičių klaviatūrą kaip iššokantįjį dialogo langą

Šiame pavyzdyje parodytas vienas iš būdų, kaip nustatyti skaitmeninės klaviatūros valdiklį iškylančiame dialogo lange.

```xpp
private void setupNumpadController()
{
    numpadController = new JmgProductionFloorExecutionNumpadController();
    numpadController.parmShouldNumpadShowOkCancelButtons(true);
    numpadController.setNumpadValueToParentFormDelegate += eventhandler(this.setQtyValueFromNumpad);
}
```

Šiame pavyzdyje parodytas vienas iš būdų, kaip iškviesti skaičių klaviatūros iššokantįjį dialogo langą.

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
