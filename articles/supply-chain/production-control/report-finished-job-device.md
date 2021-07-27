---
title: Pranešti kaip baigtą iš užduoties kortelės įrenginio
description: Šioje temoje aprašoma, kaip konfigūruoti sistemą, kad užduočių kortelės įrenginio vartotojai galėtų pranešti apie gatavus produktus iš gamybos užsakymo į atsargas.
author: johanhoffmann
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 5da18ff1013f0e767ca64b090eb1559bf05cb056
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350527"
---
# <a name="report-as-finished-from-the-job-card-device"></a>Pranešti kaip baigtą iš užduoties kortelės įrenginio

[!include [banner](../includes/banner.md)]

Darbuotojai naudoja **Progreso ataskaita** užduoties kortelės įrenginio ataskaitos puslapį, kad galėtų pranešti apie gamybos užduočiai baigtus kiekius. Ši tema aprašo, kaip nustatyti įvairias parinktis, kurios įjungia būdą, kuriuo darbuotojai gali pateikti pabaigtas ataskaitas naudodami šį puslapį ir tai, kas nutinka vėliau. Parinktys apima:

- Valdyti, ar ir kiek kiekių yra pateikta ataskaitose yra baigti ir įtraukiami į inventorių.
- Valdyti, ar ir kiek paketų skaičių yra sukuriama ir taikoma, kai ataskaitų kūrimas yra pabaigtas.
- Valdyti, ar ir kiek serijinių skaičių yra sukuriama ir taikoma, kai ataskaitų kūrimas yra pabaigtas.
- Valdyti, ar ir kaip ataskaita yra pabaigiama į licencijos numerį.

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a>Kontroliuokite, ar kiekiai, kurie pranešami baigtais, įtraukiami į atsargas

Norėdami kontroliuoti, ar ir kaip kiekiai, pateikti baigtais paskutinėje operacijoje, turi būti pridėti į atsargas, atlikite šiuos veiksmus.

1. Eikite į **Produkto kontrolė \> Sąranka \> Gamybos vykdymas \> Gamybos užsakymo numatytieji nustatymai**.
1. Skirtuke **Pranešti kaip baigta** nustatykite **Atnaujinti baigtą ataskaitą prisijungus** lauką pagal vieną iš šių verčių:

    - **Ne** – joks kiekis nebus pridėtas į atsargas, kai pranešama apie paskutinės operacijos kiekius. Gamybos užsakymo būsena niekada nesikeičia.
    - **Būsena + Kiekis** – gamybos užsakymo būsena pasikeis į *Pranešti kaip baigta*, o kiekis bus praneštas baigtu į atsargas.
    - **Kiekis** – kiekis pranešamas kaip baigtas į atsargas, bet gamybos užsakymo būsena niekada nepasikeis.
    - **Būsena** – tik gamybos užsakymo būsena pasikeis. Joks kiekis nebus pridėtas į atsargas , kai apie kiekius pranešama paskutinės operacijos metu.

> [!NOTE]
> Kiekiai nėra stebimi atsargose, jei operacijos, kuriose pranešti baigti, nėra nustatyta kaip paskutinė operacija. Tačiau šie kiekiai gali būti naudojami peržiūrėti eigą. Jie taip pat gali būti įtraukti į taisykles, kontroliuojančias, ar darbuotojai gali pradėti kitą operaciją prieš pasiekus pranešamų kiekių nustatytą ribą ankstesnės operacijos metu. Galite nustatyti šias taisyklės **Kiekio patvirtinimo** skirtuke **Gamybos užsakymo nustatytosios vertės** puslapyje.

Daugiau informacijos apie tai, kaip naudoti **Gamybos užsakymo numatytieji nustatymai** puslapį, žr. [Gamybos parametrų gamyboje vykdymas](production-parameters-manufacturing-execution.md).

## <a name="report-batch-controlled-items-as-finished"></a>Paketo kontroliuojamų prekių kaip baigta pranešimas

Užduoties kortelės įrenginys palaiko tris paketo elementų ataskaitų scenarijus. Šie scenarijai taikomi tiek prekėms, apdorojamoms pažangių sandėliavimo procesų metu, tiek prekėms, neapdorojamoms pažangių sandėliavimo procesų metu.

- **Rankiniu būdu priskirti pakuotės skaičius** - Darbuotojai įveda pasirinktą paketo skaičių. Šis paketo numeris gali atsirasti iš išorinio šaltinio, kuris nežinomas sistemai.
- **Iš anksto nustatyti paketų skaičiai** - Darbuotojai pasirenka paketo skaičių paketų skaičių sąraše, kuriuos sistema automatiškai sukuria prieš tai, kai gamybos užsakymas yra išleidžiamas į užduoties kortelės prietaisą.
- **Rankiniu būdu priskirti pakuotės skaičius** - Darbuotojai įveda pasirinktą paketo skaičių. Vietoj to, sistema automatiškai priskiria gamybos užsakymo paketo numerį prieš jį išleidžiant.


### <a name="enable-the-feature-on-your-system"></a>Įjungti funkciją jūsų sistemoje

Norėdami įjungti savo užduoties kortelės įrenginius, kad būtų galima priimti paketo numerį ataskaitos metu, kad baigta, turite naudoti [funkcijų valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), kad įjungtumėte šias funkcijas (šia tvarka):

1. Patobulinta Ataskaitos eigos dialogo lango vartotojo patirtis Užduoties kortelės įrenginyje
1. Įgalinkite paketo ir serijos numerių įvedimą, kai pranešate apie baigimą darbo kortelės įrenginiu

### <a name="configure-products-that-require-batch-number-reporting"></a>Konfigūruoti produktus, kuriems reikia paketo numerio ataskaitos

Produkto pagalbos bet kuriam paketo kontroliuojamam scenarijui įjungimui, atlikite šiuos žingsnius:

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Patvirtinti produktai**.
1. Pasirinkite konfigūruotiną produktą.
1. **Tvarkyti atsargas** „FastTab” **Paketo numerio grupė** lauke pasirinkite sekimo numerio grupę, kuri nustatyta palaikyti jūsų scenarijų.

> [!NOTE]
> Pagal numatytuosius nustatymus, jeigu paketo numerio grupė nepriskirta paketo valdomam produktui, užduoties kortelės įrenginys suteikia rankinį paketo numerio įvedimą, kai pranešama, kad baigta.

Toliau pateikti skyriai aprašo, kaip nustatyti sekimo numerio grupes tam, kad būtų palaikomas bet kuris iš trijų scenarijų ataskaitoms paketo prekėse.

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a>Nustatykite sekimo numerių grupę, kuri leidžia darbuotojams neautomatiniu būdu priskirti paketo numerį

Norėdami leisti rankiniu būdu nustatyti paketo numerius, atlikite šiuos veiksmus, kad nustatytumėte sekimo numerių grupę.

1. Eikite į **Atsargų valdymas \>Nustatymas \>Dimensijos \>Sekimo numerių grupes**.
1. Sukurkite arba pasirinkite sekimo numerių grupę, kurią norite nustatyti.
1. **Bendra** skirtuke „FastTab” nustatykite **Rankinis** pasirinktį į **Taip**.

    ![Sekimo numeris rankinio paketo numerio grupei.](media/tracking-number-group-manual.png "Sekimo numeris rankinio paketo numerio grupei")

1. Esant poreikiui, nustatykite kitas vertes, tada pasirinkite šią sekimo numerių grupę kaip paketų numerių grupę, skirtą išleistiems produktams, kuriems norite naudoti šį scenarijų.

Naudojant šį scenarijų, **Paketo numerio** laukas, kurį **Eigos ataskaita** puslapis pateikia Užduočių kortelės įrenginyje, yra teksto laukas, kuriame darbuotojai gali įvesti bet kokią vertę.

![Ataskaitos eigos puslapis, kuriame yra rankinio paketo numerių laukas.](media/job-card-device-batch-manual.png "Ataskaitos eigos puslapis, kuriame yra rankinio paketo numerių laukas")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a>Nustatykite sekimo numerių grupę, kuri pateikia iš anksto nustatytų paketų numerių sąrašą

Norėdami pateikti iš anksto nustatytų paketo numerių sąrašą, atlikite šiuos veiksmus, kad nustatytumėte sekimo numerių grupę.

1. Eikite į **Atsargų valdymas \> Sąranka > Dimensijos \> Sekimo numerių grupės**.
1. Sukurkite arba pasirinkite sekimo numerių grupę, kurią norite nustatyti.
1. **Bendra** skirtuke „FastTab” nustatykite **Tik atsargų operacijos** pasirinktį į **Taip**.
1. Naudokite **Kiekiui** laukelį, kad išskirstytumėte paketo numerius pagal kiekį pagal jūsų įvedamą vertę. Pavyzdžiui, turite produkto užsakymą dešimčiai veinetų, o **Kiekio** laukelis yra nustatytas į *2*. Šiuo atveju, sukurti penki paketo numerius bus priskirti gamybos užsakymui.

    ![Sekimo numeris iš anksto nustatyto paketo numerių grupei.](media/tracking-number-group-predefined.png "Sekimo numeris iš anksto nustatyto paketo numerių grupei")

1. Esant poreikiui, nustatykite kitas vertes, tada pasirinkite šią sekimo numerių grupę kaip paketų numerių grupę, skirtą išleistiems produktams, kuriems norite naudoti šį scenarijų.

Naudojant šį scenarijų, **Paketo numerio** laukas, kurį **Eigos ataskaita** puslapis pateikia Užduočių kortelės įrenginyje, yra išsiskleidžiantis dialogo sąrašas, kuriame darbuotojai turi įvesti iš anksto nustatytą vertę.

![Ataskaitos eigos puslapi su iš anksto nustatytų paketo numerių laukas.](media/job-card-device-batch-predefined.png "Ataskaitos eigos puslapi su iš anksto nustatytų paketo numerių laukas")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a>Nustatykite sekimo numerių grupę, kuri leidžia automatiškai priskirti paketo numerius

Jei paketo numeriai turi būti automatiškai priskirti, be darbuotojo įvesties, atlikite šiuos veiksmus, norėdami nustatyti sekimo numerių grupę.

1. Eikite į **Atsargų valdymas \>Nustatymas \>Dimensijos \>Sekimo numerių grupes**.
1. Sukurkite arba pasirinkite sekimo numerių grupę, kurią norite nustatyti.
1. **Bendra** skirtuke „FastTab” nustatykite **Tik atsargų operacijos** pasirinktį į **Ne**.
1. Nustatykite **Rankinis** pasirinktis **Nr.**.

    ![Sekimo numeris fiksuoto paketo numerio grupei.](media/tracking-number-group-fixed.png "Sekimo numeris fiksuoto paketo numerio grupei")

1. Esant poreikiui, nustatykite kitas vertes, tada pasirinkite šią sekimo numerių grupę kaip paketų numerių grupę, skirtą išleistiems produktams, kuriems norite naudoti šį scenarijų.

Naudojant šį scenarijų, **Paketo numerio** laukas, kurį **Eigos ataskaita** puslapis pateikia Užduočių kortelės įrenginyje, rodo vertę, bet darbuotojai negali redaguoti.

![Ataskaitos eigos puslapis su fiksuotu paketo numeriu.](media/job-card-device-batch-fixed.png "Ataskaitos eigos puslapis su fiksuotu paketo numeriu")

## <a name="report-serial-controlled-items-as-finished"></a>Raportuoti serijines kontroliuojamas prekes kaip baigtas

Darbo kortelės prietaisas palaiko tris raportavimo scenarijus serijinėms kontroliuojamoms prekėms. Šie scenarijai taikomi tiek prekėms, apdorojamoms pažangių sandėliavimo procesų metu, tiek prekėms, neapdorojamoms pažangių sandėliavimo procesų metu.

- **Rankiniu būdu priskirti serijinis skaičius** - Darbuotojai įveda pasirinktą serijinį skaičių. Šis serijinis numeris gali ateiti iš išorės šaltinių, kurų sistema nežino.
- **Iš anksto nustatyti serijiniai skaičiai** - Darbuotojai pasirenka serijinį skaičių serijinių skaičių sąraše, kuriuos sistema automatiškai sukuria prieš tai, kai gamybos užsakymas yra išleidžiamas į užduoties kortelės prietaisą.
- **Rankiniu būdu priskirti serijinis skaičius** - Darbuotojai įveda pasirinktą serijinį skaičių. Vietoje to, sistema automatiškai priskiria serijinį skaičių gamybos užsakymui prieš išleidimą.

### <a name="enable-the-feature-on-your-system"></a>Įjungti funkciją jūsų sistemoje

Tam, kad įjungtumėte savo užduoties kortelės prietaisą, kad jis priimtų serijinį numerį po ataskaitų rengimo pabaigos, turite naudoti [funkcijos valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tam, kad įjungtumėte vieną iš tolesnių funkcijų (tokia tvarka):

1. Patobulinta Ataskaitos eigos dialogo lango vartotojo patirtis Užduoties kortelės įrenginyje
1. Įgalinkite paketo ir serijos numerių įvedimą, kai pranešate apie baigimą darbo kortelės įrenginiu

### <a name="configure-products-that-require-serial-number-reporting"></a>Konfigūruoti produktus, kuriems reikia serijinio numerio ataskaitos

Produkto pagalbos bet kuriam serijinio numerio kontroliuojamam scenarijaus įjungimui, atlikite šiuos žingsnius:

Norėdami įjungti scenarijų, atlikite toliau nurodytus veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Patvirtinti produktai**.
1. Pasirinkite konfigūruotiną produktą.
1. **Atsargų valdymas** „FastTab“, **Serijinio numerio grupės** laukelyje pasirinkite sekimo numerio grupę, kuri yra nustatyta palaikyti jūsų scenarijų.

> [!NOTE]
> Pagal nutylėjimą, jei nėra serijinio numerio grupės priskirtos prie serijinio kontroliuojamo produkto, užduoties kortelės prietaisas suteikia rankinį įrašą serijiniam numeriui po to, kai ataskaitos rengimas yra pabaigtas.

Toliau pateikti skyriai aprašo, kaip nustatyti sekimo numerio grupes tam, kad būtų palaikomas bet kuris iš trijų scenarijų ataskaitų rengimui serijinio numerio kontroliuojamoms prekėms.

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-serial-number"></a>Nustatyti sekimo numerio grupę, kuri leidžia darbuotojams rankiniu būdu priskirti serijinį numerį

Tam, kad leistumėte rankiniu būdu priskirti serijinius numerius, atlikite šiuos žingsnius tam, kad nustatytumėte sekimo numerio grupes.

1. Eikite į **Atsargų valdymas \>Nustatymas \>Dimensijos \>Sekimo numerių grupes**.
1. Sukurkite arba pasirinkite sekimo numerių grupę, kurią norite nustatyti.
1. **Bendra** skirtuke „FastTab” nustatykite **Rankinis** pasirinktį į **Taip**.

    ![Sekimo numeris grupių puslapiui, serijiniams numeriams.](media/tracking-number-group-manual-serial.png "Sekimo numeris grupių puslapiui, serijiniams numeriams")

1. Nustatykite kitas jūsų norimas vertes ir tuomet pasirinkite šią sekimo numerio grupę kaip serijinio numerio grupę išleistiems produktams, kuriuos norite naudoti šiam scenarijui.

Kai naudojate šį scenarijų, **Serijinio numerio** laukelis tam **Ataskaitos progreso** puslapiui darbo kortelės prietaise pateikia teksto laukelį, kuriame darbuotojai gali įvesti bet kokią vertę serijiniam numeriui. Įvedus vertę, ji įtraukiama į serijinio numerio sąrašą. Šiame sąraše darbuotojai gali atlikti šiuos veiksmus:

- Tam, kad pažymėtų serijinį numerį kaip pašalintą, pasirinkite **Šalinti** mygtuką tinkamai eilutei. Darbuotojas bus paskatintas pateikti **Klaidos priežastį**.
- Tam, kad panaikintų serijinį numerį kaip pašalintą, pasirinkite **Naikinti** mygtuką tinkamai eilutei.

![Ataskaitos progreso puslapis su laukeliu rankiniams serijiniams numeriams.](media/job-card-device-serial-manual.png "Ataskaitos progreso puslapis su laukeliu rankiniams serijiniams numeriams")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-serial-numbers"></a>Nustatyti sekimo numerio grupę, kuri suteikia iš anksto nustatytų serijinių numerių sąrašą

Tam, kad pateiktumėte iš anksto nustatytą serijinių numerių sąrašą, atlikite šiuos žingsnius tam, kad nustatytumėte sekimo numerio grupes.

1. Eikite į **Atsargų valdymas \>Nustatymas \>Dimensijos \>Sekimo numerių grupes**.
1. Sukurkite arba pasirinkite sekimo numerių grupę, kurią norite nustatyti.
1. **Bendra** skirtuke „FastTab” nustatykite **Tik atsargų operacijos** pasirinktį į **Taip**.
1. Naudokite **Kiekiui** laukelį, kad išskirstytumėte serijinius numerius kiekiams po vieną.

    ![Sekimo numeris iš anksto nustatyto serijinių numerių grupei.](media/tracking-number-group-predefined-sn.png "Sekimo numeris iš anksto nustatyto serijinių numerių grupei")

1. Nustatykite kitas jūsų norimas vertes ir tuomet pasirinkite šią sekimo numerio grupę kaip serijinio numerio grupę išleistiems produktams, kuriuos norite naudoti šiam scenarijui.

Kai naudojate šį scenarijų, **Serijinio numerio** laukelis tam **Ataskaitos progreso** puslapiui darbo kortelės prietaise pateikia iškrentantį sąrašą, kuriame darbuotojai privalo pasirinkti iš anksto nustatytą vertę.

![Ataskaitos progreso puslapis su iš anksto nustatytų serijinių numerių sąrašu.](media/job-card-device-serial-predefined.png "Ataskaitos progreso puslapis su iš anksto nustatytų serijinių numerių sąrašu")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-serial-numbers"></a>Nustatyti sekimo numerio grupę, kuri automatiškai priskiria serijinius numerius

Jei serijinis numeris turi būti priskirtas automatiškai be darbuotojo indėlio, atlikite šiuos veiksmus tam, kad nustatytumėte sekimo numerio grupę.

1. Eikite į **Atsargų valdymas \>Nustatymas \>Dimensijos \>Sekimo numerių grupes**.
1. Sukurkite arba pasirinkite sekimo numerių grupę, kurią norite nustatyti.
1. **Bendra** skirtuke „FastTab” nustatykite **Tik atsargų operacijos** pasirinktį į **Ne**.
1. Nustatykite **Rankinis** pasirinktis **Nr.**.

    ![Sekimo numeris fiksuoto serijinio numerio grupei.](media/tracking-number-group-fixed-sn.png "Sekimo numeris fiksuoto serijinio numerio grupei")

1. Nustatykite kitas jūsų norimas vertes ir tuomet pasirinkite šią sekimo numerio grupę kaip serijinio numerio grupę išleistiems produktams, kuriuos norite naudoti šiam scenarijui.

Kai naudojate šį scenarijų, **Serijinio numerio** laukelis tam **Ataskaitos progreso** puslapiui darbo kortelės prietaise pateikia vertę, tačiau darbuotojai jos redaguoti negali. Šis scenarijus tinkamas, jei gamybos užsakymas yra sukurta serijinio numerio kontroliuojamos prekės vieno vieneto kiekiui.

![Ataskaitos progreso puslapis su fiksuotu serijiniu numeriu.](media/job-card-device-serial-fixed.png "Ataskaitos progreso puslapis su fiksuotu serijiniu numeriu")

## <a name="report-as-finished-to-a-license-plate"></a>Praneškite kaip baigta į numerio lentelę

Papildomiems sandėlių procesams gali būti naudojama numerio lentelės dimensija, kad sektumėte atsargas sandėlių vietose, nustatytose šiam tikslui. Šiuo atveju, numerio lentelės numeris reikalingas, kai darbuotojas praneša apie baigtus kiekius.

### <a name="enable-license-plate-reporting-and-label-printing"></a>Numerio lentelės ataskaita ir etiketės spausdinimas

Norėdami naudoti šiame skyriuje aprašytas funkcijas, turite naudoti [funkcijų valdymą, ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), kad galėtumėte įjungti šias funkcijas (šia tvarka):

1. Užbaigtos ataskaitos numerio lentelė įtraukta į užduoties kortelės įrenginį
1. Įgalinkite automatinį numerio lentelės numerio generavimą, kai Užduoties kortelės įrenginyje pranešama apie pabaigimą
1. Spausdinti etiketę iš užduoties kortelės įrenginio

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a>Nustatykite baigimo pranešimą į numerio lentelę

Norėdami kontroliuoti, ar darbuotojai turėtų dar kartą panaudoti numerio lentelę, ar generuoti naują numerio lentelę, kai jie praneša apie baigtus kiekius, atlikite šiuos veiksmus.

1. Eikite į **Gamybos kontrolė \> Sąranka \> Gamybos vykdymas \>Konfigūruoti įrenginių užduoties kortelę**.
2. Nustatykite šias parinktis kiekvienam įrenginiui:

    - **Generuoti numerio lentelę** – nustatykite šią pasirinktį į **Taip**, kad sugeneruotumėte naują numerio lentelę kiekvienai baigimo ataskaitai. Nustatykite į **Ne**, jei esama numerio lentelė turėtų būti naudojama kiekvienai baigimo ataskaitai.
    - **Spausdinti etiketę** – nustatykite šią pasirinktį į **Taip**, jei darbuotojas privalo atspausdinti numerio lentelės etiketę kiekvienai baigimo ataskaitai. Nustatykite į **Ne**, jei nereikia nei vienos etiketės. 

![Užduoties kortelės konfigūravimas įrenginių puslapiui.](media/config-job-card-raf.png "Užduoties kortelės konfigūravimas įrenginių puslapiui")

> [!NOTE]
> Norėdami konfigūruoti etiketę, eikite į **Sandėlio valdymas \> Sąranka \> Dokumentų nukreipimas \> Dokumentų nukreipimas**. Norėdami gauti daugiau informacijos, žr. [Numerio lentelės etiketės spausdinimo įjungimas](../warehousing/tasks/license-plate-label-printing.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]