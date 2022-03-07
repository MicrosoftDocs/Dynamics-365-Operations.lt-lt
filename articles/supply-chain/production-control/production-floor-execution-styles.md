---
title: Gamybos vietos vykdymo sąsajos projektavimas
description: Šioje temoje paaiškinama, kaip konfigūruoti formos valdiklius, kad jiems būtų pritaikyti numatytieji gamybos vietos vykdymo stiliai.
author: johanhoffmann
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 32e49458f6ea7c484bc4200e414d930381b31891
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/19/2021
ms.locfileid: "7652042"
---
# <a name="style-the-production-floor-execution-interface"></a>Gamybos vietos vykdymo sąsajos projektavimas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip konfigūruoti formos valdiklius, kad jiems būtų pritaikyti numatytieji gamybos vietos vykdymo stiliai.

## <a name="forms-and-dialogs"></a>Formos ir dialogai

Stilius galima taikyti formai arba dialogo langui tik tada, jei įvykdyti šie reikalavimai:

- Jei forma turi būti panaši į esamą ataskaitos eigos formą, tuomet formos arba dialogo lango pavadinimas turi prasidėti **JmgProductionFloorExecutionCustomInputDialog**.
- Formą arba dialogą gali sudaryti detali formos dalis. Norint jai pritaikyti stilius, detalios formos dalies pavadinimas turi prasidėti **JmgProductionFloorExecutionCustomDetailsDialog**.
- Jei formą arba dialogas turi turėti paprastą rodinį, tuomet paprasto rodinio pavadinimas turi prasidėti **JmgProductionFloorExecutionCustomDialog**. Paprasto rodinio formų pavyzdžiai yra pradžios ir netiesioginės veiklos formos.
- Visi dialogo valdikliai turi būti sukonfigūruoti taip, kaip aprašyta šioje temoje.

> [!IMPORTANT]
> Funkcijos, paminėtos pirmuose dviejuose šio sąrašo taškuose, reikalauja 10.0.19 Supply Chain Management versijos arba vėlesnės.

Stilius galima taikyti **OK** mygtukui dialogo lange tik tada, jei įvykdyti šie reikalavimai:

- Mygtukas yra formų grupėje.
- Grupės pavadinimas prasideda **OkButtonGroup**.

Stilius galima taikyti **Cancel (Atšaukti)** mygtukui dialogo lange tik tada, jei įvykdyti šie reikalavimai:

- Mygtukas yra formų grupėje.
- Grupės pavadinimas prasideda **CancelButtonGroup**.

## <a name="grid"></a>Tinklelis

Stiliai pritaikomi automatiškai. Nereikia jokios specifinės konfigūracijos.

## <a name="card-view"></a>Kortelių rodinys

Stilius galima taikyti kortelės vaizdo valdikliams tik tada, jei įvykdyti šie reikalavimai:

- Kiekvienas kortelės rodinys yra formos grupėje.
- Grupės pavadinimas prasideda **CardGroup** (pvz., **CardGroupJobsView**).

Šioje iliustracijoje rodomas kortelės rodinys, kuriame nėra valdiklių.

![Kortelės rodinys be elementų.](media/pfe-styles-empty-card.png)

Šiose iliustracijose rodomi kortelės rodinai, kuriuose yra valdiklių.

![Kortelė su elementais, kurie rodo Hz.](media/pfe-styles-elements.png)

![Kortelė su priežiūros užklausos elementais.](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a>Vizitinė kortelė

Stilius galima taikyti vizitinės kortelės valdikliams tik tada, jei įvykdyti šie reikalavimai:

- Kiekviena vizitinė kortelė yra formos grupėje.
- Grupės pavadinimas prasideda **BusinessCardGroup** (pvz., **BusinessCardGroupJobsList**).

Nustatykite šias vizitinės kortelės ypatybes:

- **Stilius**: **sąrašas**
- **Išplėstinis stilius**: **cardList**
- **Keli pasirinkimai**: **Ne**
- **Rodyti Col žymas**: **Ne**

![Vizitinė kortelė.](media/pfe-styles-business-card.png)

## <a name="radio-button"></a>Radijo mygtukas

Stilius galima taikyti radijo mygtukams tik tada, jei įvykdyti šie reikalavimai:

- Kiekvienas radijo mygtukas yra formų grupėje.
- Grupės pavadinimas prasideda **RadioTextBelow** arba **RadioTextRight**, priklausomai nuo to, kur norite, kad tekstas būtų rodomas.

Nustatykite šias radijo mygtuko ypatybes:

- **Perjungimo mygtukas**: **Tikrinti**
- **Perjungti vertę**: **Įjungta** jei reikia pasirinkti radijo mygtuką; kitu atveju, **Išjungta**

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

- **Mygtuko rodymas**: **TextWithImageLeft**.
- **Įprastas Vaizdas**: Ši ypatybė negali būti tuščia. Pavyzdžiui, naudokite **CoffeeScript**.
- **Tekstas**: Ši ypatybė negali būti tuščia. Pavyzdžiui, naudokite **Starto Pertrauką**.
- **Plotis**: **Automatinis**.
- **Aukštis**: **Automatinis**.

### <a name="primary-button"></a>Pagrindinis mygtukas

Stilius galima taikyti pirminiams mygtukams tik tada, jei įvykdyti šie reikalavimai:

- Mygtukas yra formų grupėje.
- Grupės pavadinimas prasideda **DefaultButtonGroup** arba **PrimaryButtonGroup** (pvz., **DefaultButtonGroup10**).

![Pirminis mygtukas.](media/pfe-styles-first.png)

### <a name="secondary-button"></a>Antrinis mygtukas

Stilius galima taikyti antriniam mygtukui tik tada, jei įvykdyti šie reikalavimai:

- Mygtukas yra formų grupėje.
- Grupė pavadinta **Dešiniuoju skydu** arba grupės pavadinimas prasideda **SecondaryButtonGroup**.

![Antrinis mygtukas.](media/pfe-styles-second.png)

### <a name="third-group-button"></a>Trečiosios grupės mygtukas

Stilius galima taikyti trečiosios grupės mygtukui tik tada, jei įvykdyti šie reikalavimai:

- Mygtukas yra formų grupėje.
- Grupė pavadinta **Kairiuoju skydu** arba grupės pavadinimas prasideda **ThirdButtonGroup**.

![Trečiosios grupės mygtukas.](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a>Ketvirtos grupės mygtukas

Stilius galima taikyti ketvirtosios grupės mygtukui tik tada, jei įvykdyti šie reikalavimai:

- Mygtukas yra formų grupėje.
- Grupės pavadinimas prasideda **FourthButtonGroup**.

Nustatykite šias mygtuko ypatybes:

- **Mygtuko rodinys:** **TextOnly**.
- **Įprastas Vaizdas**: Ši ypatybė privalo būti tuščia.
- **Tekstas**: Ši ypatybė negali būti tuščia. Pavyzdžiui, naudokite **Peržiūrėti** arba **Redaguoti**.
- **Plotis**: **Automatinis**.
- **Aukštis**: **Automatinis**.

![Ketvirtos grupės mygtukas.](media/pfe-styles-fourth.png)

### <a name="flat-button"></a>Plokščias mygtukas

Stilius galima pritaikyti plokščiam mygtukui tik tada, jei įvykdyti šie reikalavimai:

- Mygtukas yra formų grupėje.
- Grupės pavadinimas prasideda **FlatButtonGroup**.

Nustatykite šias mygtuko ypatybes:

- **Mygtuko rodinys:** **ImageOnly**.
- **Įprastas Vaizdas**: Ši ypatybė negali būti tuščia. Pavyzdžiui, naudokite **CoffeeScript**.
- **Tekstas**: Ši ypatybė privalo būti tuščia.
- **Plotis**: **Automatinis**.
- **Aukštis**: **Automatinis**.

![Plokščias mygtukas.](media/pfe-styles-flat-button.png)

## <a name="combo-box"></a>Pasirinktinio įvedimo laukas

Pasirinktinio įvedimo laukas yra trijų valdiklių kombinacija: ją sudaro įvesties valdiklis, įvesties valdiklio išvalymo mygtukas ir ieškos mygtukas.

Stilius galima taikyti pasirinktinio įvedimo laukui tik tada, jei įvykdyti šie reikalavimai:

- Pasirinktinio įvedimo laukas yra formų grupėje.
- Grupės pavadinimas prasideda **Combobox**.
- Grupėje pirmasis valdiklis yra **AxFormStringControl**. Šis valdiklis rodo esamą vertę ir tai yra vieta, kur vartotojas įveda reikiamą vertę.
- Antrasis valdiklis yra **CommonButton** valdiklis, o jo pavadinimas prasideda **ClearButton**. Šis mygtukas turi turėti kodą, kuris naudoja **įgalinti** ypatybę mygtukui rodyti arba slėpti. Pavyzdžiui, jei norite rodyti arba slėpti mygtuką **Valyti**, kai vartotojas įvesties valdiklyje įveda informaciją, galite naudoti šį kodą.

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

    Naudokite šį kodą, kai **spustelėjimo** mygtukui **Valyti** metodo.

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    Nustatykite įvesties valdiklio **AxFormStringControl** vertę, kai forma inicijuojama naudojant **init** metodą. Jei vertė nėra tuščia, įgalinkite mygtuką **Valyti**. Jei vertė yra tuščia, išjunkite **Valyti** mygtuką.

- Trečiasisi valdiklis yra **CommonButton** valdiklis, o jo pavadinimas prasideda **SearchButton**.

Toliau pateikta iliustracija rodo du pasirinktinio įvedimo lauko valdiklius. Pasirinktinio įvedimo lauko kairėje yra tuščias teksto laukas, o **Valyti** mygtukas yra išjungtas. Pasirinktinio įvedimo lauko dešinėje teksto lauke yra tekstas, o **Valyti** mygtukas yra įgalintas.

![Pasirinktinio įvedimo laukai su mygtuku Valyti ir be jo.](media/pfe-styles-combo.png)

## <a name="quick-filter"></a>Spartusis filtras.

Sparčiojo filtro valdiklis į puslapį įtraukia ieškos lauką. Galite taikyti stilius sparčiajam filtrui, jei atitinka šiuos reikalavimus:

- Spartusis filtras yra formų grupėje.
- Grupės pavadinimas prasideda **SearchInputGroup**.
- Grupėje pirmasis valdiklis yra **QuickFilter** valdiklis. (Šioje vietoje vartotojas įveda ieškos eilutę.)
- Antrasis valdiklis yra **FormStaticTextControl**, kurio pavadinimas **NumberOfResults**. (Tai yra pasirinktina ir rodo rastų prekių skaičių, jei įtraukta.)
- Trečiasisi valdiklis yra **CommonButton** valdiklis, o jo pavadinimas prasideda **ClearButton**.

Toliau pateikta iliustracija rodo du sparčiojo filtro valdiklius. Spartusis filtras kairėje turi tuščią spartųjį filtrą ir rezultatų skaičius yra nematomas. Spartusis filtras dešinėje turi ieškos eilutė ir rodo rezultatų skaičių.

![Sparčiojo filtro valdiklio su ieškos eilute ir be jos pavyzdžiai.](media/pfe-styles-quick-filter.png "Sparčiojo filtro valdiklio su ieškos eilute ir be jos pavyzdžiai.")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
