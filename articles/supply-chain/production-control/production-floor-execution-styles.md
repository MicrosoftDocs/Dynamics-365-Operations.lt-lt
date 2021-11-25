---
title: Gamybos vietos vykdymo sąsajos projektavimas
description: Šioje temoje paaiškinama, kaip konfigūruoti formos valdiklius, kad jiems būtų pritaikyti numatytieji gamybos vietos vykdymo stiliai.
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: ef39dc6414f0afdadd4a4b5a41e1fb1fe60e4974
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790895"
---
# <a name="style-the-production-floor-execution-interface"></a>Gamybos vietos vykdymo sąsajos projektavimas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip konfigūruoti formos valdiklius, kad jiems būtų pritaikyti numatytieji gamybos vietos vykdymo stiliai.

## <a name="forms-and-dialogs"></a>Formos ir dialogai

Stilius galima taikyti formai arba dialogo langui tik tada, jei įvykdyti šie reikalavimai:

- Jei forma turėtų būti panaši į esamą ataskaitos eigos formą, formos pavadinimas arba dialogo langas turi prasidėti `JmgProductionFloorExecutionCustomInputDialog`.
- Formą arba dialogą gali sudaryti detali formos dalis. Jei norite taikyti stilius, informacijos formos dalies pavadinimas turi prasidėti `JmgProductionFloorExecutionCustomDetailsDialog`.
- Jei forma arba dialogas turi turėti paprastą rodinį, tai paprasto rodinio pavadinimas turi prasidėti `JmgProductionFloorExecutionCustomDialog`. Paprasto rodinio formų pavyzdžiai yra pradžios ir netiesioginės veiklos formos.
- Visi dialogo lango valdikliai turi būti sukonfigūruoti taip, kaip aprašyta šioje temoje.

> [!IMPORTANT]
> Funkcijos, paminėtos pirmuose dviejuose šio sąrašo taškuose, reikalauja 10.0.19 Supply Chain Management versijos arba vėlesnės.

Stilius galima taikyti **OK** mygtukui dialogo lange tik tada, jei įvykdyti šie reikalavimai:

- Mygtukas yra formų grupėje.
- Grupės pavadinimas prasideda `OkButtonGroup`.

Stilius galima taikyti **Cancel (Atšaukti)** mygtukui dialogo lange tik tada, jei įvykdyti šie reikalavimai:

- Mygtukas yra formų grupėje.
- Grupės pavadinimas prasideda `CancelButtonGroup`.

### <a name="header"></a>Antraštė

Šioje iliustracijoje pateikiama įprasta forma arba dialogo antraštė.

![Įprasta forma arba dialogo antraštė.](media/pfe-styles-header.png "Įprasta forma arba dialogo lango antraštė")

Antraštės Visual Studio kuriamos naudojant tokią struktūrą, kaip parodyta pateiktoje iliustracijoje.

![Įprasta kodų struktūra antraštei kurti.](media/pfe-styles-header-code-structure.png "Įprasta kodų struktūra antraštei sukurti")

Norėdami pridėti tekstą antraštėje, naudokite tokį kodą kaip šiame pavyzdyje.

```xpp
private void setCaption()
{
    HeaderFieldWithSeparatorText1.text("Report Progress");
    HeaderFieldWithSeparatorText2.text(ProdId);

    …

    HeaderFieldText.text(OprNum);
}
```

Kai įrašote antraštės kodą, pritaikykite šias taisykles:

- Pagrindinės grupės pavadinimas turi `TableRowHeaderGroup` būti.
- Kiekvienas teksto blokas (atskirtas ženkleliais) turi `HeaderFieldWithSeparatorText` prasidėti.
- Pavardė turi prasidėti `HeaderFieldText` tekstu.
- `CaptionImage` galima praleisti.

### <a name="progress-indicator"></a>Eigos indikatorius

Galite įtraukti eigos indikatorių, kuris rodomas dešinėje antraštės pusėje. Šioje iliustracijoje rodomas eigos indikatorius.

![Įprastas eigos indikatorius.](media/pfe-styles-header-progress.png "Įprastas eigos indikatorius")

Norint rodyti eigos indikatorių, teksto laukas turi būti `ShowProgress` pavadintas.

## <a name="grid"></a>Tinklelis

Stiliai pritaikomi automatiškai. Nereikia jokios specifinės konfigūracijos.

Tinklelis turi turėti stilių, o pasirinktinės formos metodas turi būti `TabularView``run()` perrašytas, nes naujas tinklelis dar nepalaikomas. Pridėti šį kodą.

```xpp
public void run()
{
    super();
    // To opt out a page from the new grid
    this.forceLegacyGrid();
}
```

Norėdami atnaujinti duomenis pagrindiniame rodinyje, galbūt norėsite naudoti ką nors `this.parmParentForm().updateLayout();` kaip `click` savo veiksmo metode. (Pvz., pažiūrėkite į `JmgProductionFloorExecutionReportFeedbackAction` klasę.) Tiesiog `parmDataSource` įsitikinkite, kad nustatytas jūsų naujos formos metodas `init``formCaller.parmDataSource(this.dataSource(1));` (). Pavyzdžiui, pažiūrėkite į `JmgProductionFloorExecutionMainGrid` formą.

## <a name="card-view"></a>Kortelių rodinys

Stilius galima taikyti kortelės vaizdo valdikliams tik tada, jei įvykdyti šie reikalavimai:

- Kiekvienas kortelės rodinys yra formos grupėje.
- Grupės pavadinimas prasideda `CardGroup` (pvz., `CardGroupJobsView`).

Šioje iliustracijoje rodomas kortelės rodinys, kuriame nėra valdiklių.

![Kortelės rodinys be elementų.](media/pfe-styles-empty-card.png)

Šiose iliustracijose rodomi kortelės rodinai, kuriuose yra valdiklių.

![Kortelė su elementais, kurie rodo Hz.](media/pfe-styles-elements.png)

![Kortelė su priežiūros užklausos elementais.](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a>Vizitinė kortelė

Stilius galima taikyti vizitinės kortelės valdikliams tik tada, jei įvykdyti šie reikalavimai:

- Kiekviena vizitinė kortelė yra formos grupėje.
- Grupės pavadinimas prasideda `BusinessCardGroup` (pvz., `BusinessCardGroupJobsList`).

Nustatykite šias vizitinės kortelės ypatybes:

- **Stilius:** *sąrašas*
- **Išplėstinis stilius:** *cardList*
- **Keli pasirinkti:** *ne*
- **Rodyti stulpelių žymas:** *ne*

![Vizitinė kortelė.](media/pfe-styles-business-card.png)

## <a name="radio-button"></a>Radijo mygtukas

Stilius galima taikyti radijo mygtukams tik tada, jei įvykdyti šie reikalavimai:

- Kiekvienas radijo mygtukas yra formų grupėje.
- Grupės pavadinimas prasideda arba `RadioTextBelow``RadioTextRight`, atsižvelgiant į tai, kur norite matyti tekstą.

Nustatykite šias radijo mygtuko ypatybes:

- **Perjungimo mygtukas:** *tikrinti*
- **Kaitalioti vertę:** *·* įjungti, jei reikia pasirinkti radijo mygtuką; jei ne, *išjungti*

Šioje iliustracijoje pateikiamas pavyzdys, kuriame tekstas pasirodo po radijo mygtukais.

![Radijo mygtukai su žemiau esančiu tekstu.](media/pfe-styles-radio-text-below.png)

Šioje iliustracijoje pateikiamas pavyzdys, kuriame tekstas pasirodo radijo mygtukų dešinėje.

![Radijo mygtukai su tekstu dešinėje.](media/pfe-styles-radio-text-right.png)

### <a name="radio-buttons-in-internet-explorer"></a>Radijo mygtukai Internet Explorer naršyklėje

Radijo mygtukų stiliai Internet Explorer naršyklės nepalaikomi. Tolesnėje iliustracijoje rodoma, kaip radijo mygtukai atrodo programoje Internet Explorer.

![Radijo mygtukai Internet Explorer naršyklėje.](media/pfe-styles-browser.png)

## <a name="buttons"></a>Sagos

Stilius galima taikyti mygtukams tik tada, jei įvykdyti šie reikalavimai:

- Kiekviena mygtukų grupė yra formų grupėje. Visi mygtukai grupėje turės vienodą stilių.
- Grupės pavadinimui nėra keliami jokie reikalavimai.

Nustatykite šias mygtukų ypatybes:

- **Mygtuko rodymas:** *TextWithImageLeft*
- **Įprastas** vaizdas: ši ypatybė negali būti tuščia. Pavyzdžiui, naudokite *CoffeeScript*.
- **Tekstas:** ši ypatybė negali būti tuščia. Pavyzdžiui, naudokite *Starto Pertrauką*.
- **Plotis:** *automatinis arba* *SizeToContent*
- **Aukštis:** *automatinis arba* *SizeToContent*

### <a name="primary-button"></a>Pagrindinis mygtukas

Stilius galima taikyti pirminiams mygtukams tik tada, jei įvykdyti šie reikalavimai:

- Mygtukas yra formų grupėje.
- Grupės pavadinimas prasideda arba `DefaultButtonGroup``PrimaryButtonGroup` (pvz.). `DefaultButtonGroup10`

![Pirminis mygtukas.](media/pfe-styles-first.png)

### <a name="secondary-button"></a>Antrinis mygtukas

Stilius galima taikyti antriniam mygtukui tik tada, jei įvykdyti šie reikalavimai:

- Mygtukas yra formų grupėje.
- Grupė pavadinta **Dešiniuoju** skydu arba grupės pavadinimas `SecondaryButtonGroup` prasideda.

![Antrinis mygtukas.](media/pfe-styles-second.png)

### <a name="third-group-button"></a>Trečiosios grupės mygtukas

Stilius galima taikyti trečiosios grupės mygtukui tik tada, jei įvykdyti šie reikalavimai:

- Mygtukas yra formų grupėje.
- Grupė pavadinta **Kairioji** sritis arba grupės pavadinimas prasideda `ThirdButtonGroup`.

![Trečiosios grupės mygtukas.](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a>Ketvirtos grupės mygtukas

Stilius galima taikyti ketvirtosios grupės mygtukui tik tada, jei įvykdyti šie reikalavimai:

- Mygtukas yra formų grupėje.
- Grupės pavadinimas `FourthButtonGroup` prasideda.

Nustatykite šias mygtuko ypatybes:

- **Mygtuko rodymas:** *TextOnly*
- **Įprastas vaizdas:** ši ypatybė turi būti tuščia.
- **Tekstas:** ši ypatybė negali būti tuščia. Pavyzdžiui, naudokite *Peržiūrėti* arba *Redaguoti*.
- **Plotis:** *automatinis*
- **Aukštis:** *automatinis*

![Ketvirtos grupės mygtukas.](media/pfe-styles-fourth.png)

### <a name="flat-button"></a>Plokščias mygtukas

Stilius galima pritaikyti plokščiam mygtukui tik tada, jei įvykdyti šie reikalavimai:

- Mygtukas yra formų grupėje.
- Grupės pavadinimas prasideda `FlatButtonGroup`.

Nustatykite šias mygtuko ypatybes:

- **Mygtuko rodymas:** *ImageOnly*
- **Įprastas** vaizdas: ši ypatybė negali būti tuščia. Pavyzdžiui, naudokite *CoffeeScript*.
- **Tekstas:** ši ypatybė turi būti tuščia.
- **Plotis:** *automatinis arba* *SizeToContent*
- **Aukštis:** *automatinis arba* *SizeToContent*

![Plokščias mygtukas.](media/pfe-styles-flat-button.png)

### <a name="continue-button"></a>Mygtukas Tęsti

Stilius galima taikyti mygtukui Tęsti tik tada, jei įvykdyti šie reikalavimai:

- Mygtukas yra formų grupėje.
- Grupės pavadinimas `ContinueButtonGroup` prasideda.

Nustatykite šias mygtuko ypatybes:

- **Mygtuko rodymas:** *ImageOnly*
- **Įprastas vaizdas:** *pirmyn*
- **Tekstas:** ši ypatybė turi būti tuščia.
- **Plotis:** *automatinis arba* *SizeToContent*
- **Aukštis:** *automatinis arba* *SizeToContent*

![Tęsti mygtuką.](media/pfe-styles-continue-button.png)

## <a name="combo-box"></a>Pasirinktinio įvedimo laukas

Pasirinktinio įvedimo laukas yra trijų valdiklių kombinacija: ją sudaro įvesties valdiklis, įvesties valdiklio išvalymo mygtukas ir ieškos mygtukas.

Stilius galima taikyti pasirinktinio įvedimo laukui tik tada, jei įvykdyti šie reikalavimai:

- Pasirinktinio įvedimo laukas yra formų grupėje.
- Grupės pavadinimas `Combobox` prasideda.
- Grupės viduje pirmasis valdiklis yra `AxFormStringControl` valdiklis. Šis valdiklis rodo esamą vertę ir tai yra vieta, kur vartotojas įveda reikiamą vertę.
- Antrasis valdiklis yra `CommonButton` valdiklis, o jo pavadinimas `ClearButton` prasideda. Šiame mygtuke turi būti kodas, kuris `enable` naudoja ypatybę mygtukui rodyti arba slėpti. Pavyzdžiui, jei norite rodyti arba slėpti mygtuką **Valyti**, kai vartotojas įvesties valdiklyje įveda informaciją, galite naudoti šį kodą.

    ```xpp
    public void textChange()
    {
        super();
        ClearButtonSerial.enabled(this.text()? true : false);
    }
    ```

    Turėtumėte turėti vieną metodą, kuriame duomenys nustatomi įvesties valdiklyje. Įgalinkite **Valyti** mygtuką šiuo metodu. Toliau pateikiamas pavyzdys.

    ```xpp
    public void setSerialId(str _serialId)
    {
        JmgTmpJobBundleProdFeedback.InventSerial = _serialId;
        ClearButtonSerial.enabled(_serialId? true : false);

        if (_serialId)
        {
            this.addSerialNumber();
        }
    }
    ```

    Naudokite šį mygtuko `clicked` Valyti **metodo** kodą.

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    Nustatykite įvesties valdiklio `AxFormStringControl` vertę, kai forma inicijuojama naudojant `init` metodą. Jei vertė nėra tuščia, įgalinkite mygtuką **Valyti**. Jei vertė yra tuščia, išjunkite **Valyti** mygtuką.

- Trečiasis valdiklis yra `CommonButton` valdiklis, o jo pavadinimas `SearchButton` prasideda.

Toliau pateikta iliustracija rodo du pasirinktinio įvedimo lauko valdiklius. Pasirinktinio įvedimo lauko kairėje yra tuščias teksto laukas, o **Valyti** mygtukas yra išjungtas. Pasirinktinio įvedimo lauko dešinėje teksto lauke yra tekstas, o **Valyti** mygtukas yra įgalintas.

![Pasirinktinio įvedimo laukai su mygtuku Valyti ir be jo.](media/pfe-styles-combo.png)

## <a name="quick-filter"></a>Spartusis filtras.

Sparčiojo filtro valdiklis į puslapį įtraukia ieškos lauką. Galite taikyti stilius sparčiajam filtrui, jei atitinka šiuos reikalavimus:

- Spartusis filtras yra formų grupėje.
- Grupės pavadinimas `SearchInputGroup` prasideda.
- Pirmasis valdiklis yra grupės `QuickFilter` viduje. (Šis valdiklis yra toks, kuriame vartotojas įveda paieškos eilutę.)
- Antrasis valdiklis yra `FormStaticTextControl` tas, kuris pavadintas. `NumberOfResults` (Šis valdiklis yra pasirinktinis. Jei įtraukta, rodomas rastos prekės skaičius.
- Trečiasis valdiklis yra `CommonButton` valdiklis, o jo pavadinimas `ClearButton` prasideda.

Toliau pateikta iliustracija rodo du sparčiojo filtro valdiklius. Spartusis filtras kairėje turi tuščią spartųjį filtrą ir rezultatų skaičius yra nematomas. Spartusis filtras dešinėje turi ieškos eilutė ir rodo rezultatų skaičių.

![Sparčiojo filtro valdiklio su ieškos eilute ir be jos pavyzdžiai.](media/pfe-styles-quick-filter.png "Sparčiojo filtro valdiklio su ieškos eilute ir be jos pavyzdžiai.")

## <a name="center-align-elements-on-a-tab"></a>Center lygiavimo elementai skirtuke

Norint lygiuoti elementus skirtuko centre, grupės pavadinimas turi prasidėti ir grupės ypatybės `TabContentGroup` turi būti tokios:

- **Pločio režimas:**`SizeToAvailable`
- **Aukščio režimas:**`SizeToAvailable`

## <a name="align-a-grid-detail-part-and-quick-filter"></a>Sulygiuoti tinklelį, informacijos dalį ir spartųjį filtrą

Norėdami išdėstyti pritaikytą tinklelį, informacijos dalį ir spartųjį filtrą, kad jie būtų panašūs į standartinį dizainą, kai juos visus sudėkite kartu, atkreipkite dėmesį į šiuos dalykus:

- Jei tinklelyje yra spartus filtras, ir tinklelis, ir spartusis filtras turi būti grupėje, kurios pavadinimas `GridGroup` prasideda.
- Jei norite taikyti stilius informacijos daliai, grupės pavadinimas turi `DetailInformationGroup` prasidėti,

Šioje iliustracijoje rodomas įprastas tinklelis, kuriame yra spartusis filtras ir išsamios informacijos dalis dešinėje.

![Įprastas tinklelis, kuriame yra spartusis filtras ir išsamios informacijos dalis.](media/pfe-styles-align-grid.png "Įprastas tinklelis, kuriame yra spartusis filtras ir informacijos dalis")

Tinklelyje, tinklelyje, informacijos dalyje ir spartusis filtras gali būti sukurtas naudojant tokią struktūrą, kaip pateikta Visual Studio toliau pateiktoje iliustracijoje.

![Įprasta kodų struktūra, kuri lygiuoti tinklelį, informacijos dalį ir spartųjį filtrą.](media/pfe-styles-header-code-structure2.png "Įprasta kodų struktūra, kuri lygiuoti tinklelį, informacijos dalį ir spartųjį filtrą")

## <a name="additional-resources"></a>Papildomi ištekliai

- [Gamybos vietos vykdymo sąsajos tinkinimas](production-floor-execution-customize.md)
- [Gamybos vietos vykdymo sąsajos kūrimas](production-floor-execution-tabs.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
