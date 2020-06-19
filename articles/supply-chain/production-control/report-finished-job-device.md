---
title: Pranešti kaip baigtą iš užduoties kortelės įrenginio
description: Šioje temoje aprašoma, kaip konfigūruoti sistemą, kad užduočių kortelės įrenginio vartotojai galėtų pranešti apie gatavus produktus iš gamybos užsakymo į atsargas.
author: johanhoffmann
manager: tfehr
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f5d34893ddc8adc3785ec50dbd72438cf8f68c5d
ms.sourcegitcommit: 52ba8d3e6af72df5dab6c04b9684a61454d353ad
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/26/2020
ms.locfileid: "3403267"
---
# <a name="report-as-finished-from-the-job-card-device"></a>Pranešti kaip baigtą iš užduoties kortelės įrenginio

[!include [banner](../includes/banner.md)]

Darbuotojai naudoja **Progreso ataskaita** užduoties kortelės įrenginio ataskaitos puslapį, kad galėtų pranešti apie gamybos užduočiai baigtus kiekius.

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a>Kontroliuokite, ar kiekiai, kurie pranešami baigtais, įtraukiami į atsargas

Norėdami kontroliuoti, ar ir kaip kiekiai, pateikti baigtais paskutinėje operacijoje, turi būti pridėti į atsargas, atlikite šiuos veiksmus.

1. Eikite į **Produkto kontrolė \> Sąranka \> Gamybos vykdymas \> Gamybos užsakymo numatytieji nustatymai**.
1. Skirtuke **Pranešti kaip baigta** nustatykite **Atnaujinti baigtą ataskaitą prisijungus** lauką pagal vieną iš šių verčių:

    - **Ne** – joks kiekis nebus pridėtas į atsargas, kai pranešama apie paskutinės operacijos kiekius. Gamybos užsakymo būsena niekada nesikeičia.
    - **Būsena + Kiekis** – gamybos užsakymo būsena pasikeis į *Pranešti kaip baigta*, o kiekis bus praneštas baigtu į atsargas.
    - **Kiekis** – kiekis pranešamas kaip baigtas į atsargas, bet gamybos užsakymo būsena niekada nepasikeis.
    - **Būsena** – tik gamybos užsakymo būsena pasikeis. Joks kiekis nebus pridėtas į atsargas , kai apie kiekius pranešama paskutinės operacijos metu.

> [!NOTE]
> Kiekiai nėra stebimi atsargose, jei operacijos, kuriose pranešti baigti, nėra nustatyta kaip paskutinė operacija. Tačiau šie kiekiai gali būti naudojami peržiūrėti eigą. Jie taip pat gali būti įtraukti į taisykles, kontroliuojančias, ar darbuotojai gali pradėti kitą operaciją prieš pasiekus pranešamų kiekių nustatytą ribą ankstesnės operacijos metu. Galite nustatyti šias taisykles **Kiekio tikrinimas** skirtuke, esančiame **Gamybos užsakymo numatytieji nustatymai** puslapyje.

Daugiau informacijos apie tai, kaip naudoti **Gamybos užsakymo numatytieji nustatymai** puslapį, žr. [Gamybos parametrų gamyboje vykdymas](production-parameters-manufacturing-execution.md).

## <a name="report-batch-controlled-items-as-finished"></a>Paketo kontroliuojamų prekių kaip baigta pranešimas

Užduoties kortelės įrenginys palaiko tris paketo elementų ataskaitų scenarijus. Šie scenarijai taikomi tiek prekėms, apdorojamoms pažangių sandėliavimo procesų metu, tiek prekėms, neapdorojamoms pažangių sandėliavimo procesų metu.

- **Rankiniu būdu priskirti paketo numeriai:** darbuotojai įveda pasirinktinį paketo numerį. Šis paketo numeris gali atsirasti iš išorinio šaltinio, kuris nežinomas sistemai.
- **Iš anksto nustatyti paketo numeriai:** darbuotojai pasirenka paketo numerių sąraše esantį paketo numerį, kurį sistema automatiškai sugeneruoja prieš paleidžiant gamybos užsakymą į užduočių kortelės įrenginį.
- **Fiksuoti paketo numeriai:** darbuotojai neįveda ar nesitenka paketo numerio. Vietoj to, sistema automatiškai priskiria gamybos užsakymo paketo numerį prieš jį išleidžiant.

Norėdami įjungti scenarijų, atlikite toliau nurodytus veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Patvirtinti produktai**.
1. Pasirinkite konfigūruotiną produktą.
1. **Tvarkyti atsargas** „FastTab” **Paketo numerio grupė** lauke pasirinkite sekimo numerio grupę, kuri nustatyta palaikyti jūsų scenarijų.

> [!NOTE]
> Pagal numatytuosius nustatymus, jeigu paketo numerio grupė nepriskirta paketo valdomam produktui, užduoties kortelės įrenginys suteikia rankinį paketo numerio įvedimą, kai pranešama, kad baigta.

Toliau esančiuose poskyriuose aprašoma, kaip nustatyti sekimo numerių grupes, kad būtų palaikomas kiekvienas iš trijų paketo elementų ataskaitų scenarijų.

### <a name="enable-batch-number-reporting-on-the-job-card-device"></a>Įjunkite paketo numerio ataskaitą užduoties kortelės įrenginyje

Norėdami įjungti savo užduoties kortelės įrenginius, kad būtų galima priimti paketo numerį ataskaitos metu, kad baigta, turite naudoti [funkcijų valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), kad įjungtumėte šias funkcijas (šia tvarka):

1. Patobulinta Ataskaitos eigos dialogo lango vartotojo patirtis Užduoties kortelės įrenginyje
1. Įjunkite, kad galėtumėte įvesti paketo ir serijos numerius, kai pranešate apie baigimą Užduoties kortelės įrenginiu (peržiūra)

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a>Nustatykite sekimo numerių grupę, kuri leidžia darbuotojams neautomatiniu būdu priskirti paketo numerį

Norėdami leisti rankiniu būdu nustatyti paketo numerius, atlikite šiuos veiksmus, kad nustatytumėte sekimo numerių grupę.

1. Eikite į **Atsargų valdymas \>Nustatymas \>Dimensijos \>Sekimo numerių grupes**.
1. Sukurkite arba pasirinkite sekimo numerių grupę, kurią norite nustatyti.
1. **Bendra** skirtuke „FastTab” nustatykite **Rankinis** pasirinktį į **Taip**.

    ![Sekimo numerių grupių puslapis](media/tracking-number-group-manual.png "Sekimo numerių grupių puslapis")

1. Esant poreikiui, nustatykite kitas vertes, tada pasirinkite šią sekimo numerių grupę kaip paketų numerių grupę, skirtą išleistiems produktams, kuriems norite naudoti šį scenarijų.

Naudojant šį scenarijų, **Paketo numerio** laukas, kurį **Eigos ataskaita** puslapis pateikia Užduočių kortelės įrenginyje, yra teksto laukas, kuriame darbuotojai gali įvesti bet kokią vertę.

![Ataskaitos eigos puslapis, kuriame yra rankinio paketo numerių laukas](media/job-card-device-batch-manual.png "Ataskaitos eigos puslapis, kuriame yra rankinio paketo numerių laukas")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a>Nustatykite sekimo numerių grupę, kuri pateikia iš anksto nustatytų paketų numerių sąrašą

Norėdami pateikti iš anksto nustatytų paketo numerių sąrašą, atlikite šiuos veiksmus, kad nustatytumėte sekimo numerių grupę.

1. Eikite į **Atsargų valdymas \> Sąranka > Dimensijos \> Sekimo numerių grupės**.
1. Sukurkite arba pasirinkite sekimo numerių grupę, kurią norite nustatyti.
1. **Bendra** skirtuke „FastTab” nustatykite **Tik atsargų operacijos** pasirinktį į **Taip**.
1. Naudokite **Už vnt.** lauką, kad perskirtumėte paketo numerius už kiekį, atsižvelgdami į jūsų įvestą vertę. Pavyzdžiui, turite gamybos užsakymo dešimt vienetų, o **Už vnt.** laukas nustatytas į *2*. Šiuo atveju, sukurti penki paketo numerius bus priskirti gamybos užsakymui.

    ![Sekimo numerių grupių puslapis](media/tracking-number-group-predefined.png "Sekimo numerių grupių puslapis")

1. Esant poreikiui, nustatykite kitas vertes, tada pasirinkite šią sekimo numerių grupę kaip paketų numerių grupę, skirtą išleistiems produktams, kuriems norite naudoti šį scenarijų.

Naudojant šį scenarijų, **Paketo numerio** laukas, kurį **Eigos ataskaita** puslapis pateikia Užduočių kortelės įrenginyje, yra išsiskleidžiantis dialogo sąrašas, kuriame darbuotojai turi įvesti iš anksto nustatytą vertę.

![Ataskaitos eigos puslapi su iš anksto nustatytų paketo numerių laukas](media/job-card-device-batch-predefined.png "Ataskaitos eigos puslapi su iš anksto nustatytų paketo numerių laukas")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a>Nustatykite sekimo numerių grupę, kuri leidžia automatiškai priskirti paketo numerius

Jei paketo numeriai turi būti automatiškai priskirti, be darbuotojo įvesties, atlikite šiuos veiksmus, norėdami nustatyti sekimo numerių grupę.

1. Eikite į **Atsargų valdymas \>Nustatymas \>Dimensijos \>Sekimo numerių grupes**.
1. Sukurkite arba pasirinkite sekimo numerių grupę, kurią norite nustatyti.
1. **Bendra** skirtuke „FastTab” nustatykite **Tik atsargų operacijos** pasirinktį į **Ne**.
1. Nustatykite **Rankinis** pasirinktis **Nr.**.

    ![Sekimo numerių grupių puslapis](media/tracking-number-group-fixed.png "Sekimo numerių grupių puslapis")

1. Esant poreikiui, nustatykite kitas vertes, tada pasirinkite šią sekimo numerių grupę kaip paketų numerių grupę, skirtą išleistiems produktams, kuriems norite naudoti šį scenarijų.

Naudojant šį scenarijų, **Paketo numerio** laukas, kurį **Eigos ataskaita** puslapis pateikia Užduočių kortelės įrenginyje, rodo vertę, bet darbuotojai negali redaguoti.

![Ataskaitos eigos puslapis su fiksuotu paketo numeriu](media/job-card-device-batch-fixed.png "Ataskaitos eigos puslapis su fiksuotu paketo numeriu")

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

![Užduoties kortelės konfigūravimas įrenginių puslapiui](media/config-job-card-raf.png "Užduoties kortelės konfigūravimas įrenginių puslapiui")

> [!NOTE]
> Norėdami konfigūruoti etiketę, eikite į **Sandėlio valdymas \> Sąranka \> Dokumentų nukreipimas \> Dokumentų nukreipimas**. Norėdami gauti daugiau informacijos, žr. [Numerio lentelės etiketės spausdinimo įjungimas](../warehousing/tasks/license-plate-label-printing.md).
