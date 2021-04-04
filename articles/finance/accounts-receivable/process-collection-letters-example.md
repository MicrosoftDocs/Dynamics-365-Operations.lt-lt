---
title: Priminimo laiškų apdorojimo pavyzdys
description: Šioje temoje pateikiamas pavyzdys, kuriame parodomas priminimo laiškų kūrimo, spausdinimo ir registravimo procesas.
author: JodiChristiansen
manager: AnnBe
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: df4252513f9e3a02632561b4e465c98edc888ea7
ms.sourcegitcommit: 4ecc1bf82fbb04882d7ef5e1994ef3c07ef953dc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/08/2021
ms.locfileid: "5558316"
---
# <a name="process-collection-letters-example"></a>Priminimo laiškų apdorojimo pavyzdys

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamas pavyzdys, kuriame parodomas priminimo laiškų kūrimo, spausdinimo ir registravimo procesas. Pavyzdys yra pagrįstas **Nepaisyti mokėjimų ir kredito pažymų skaičiuojant priminimo laiško kodą** parinktis Kredite ir priminimuose. Ji naudoja duomenis USMF demonstracinėje įmonėje ir naują klientą, JAV-045.

Norėdami pradėti, eikite į **Gautinos sąskaitos \> Klientai \> Visi klientai**, pasirinkite **Nauja** ir tada įveskite būtiną informaciją, kad sukurtumėte klientą JAV-045.

Pabaigus atlikite šiuos veiksmus.

1. Eikite į **Kreditas ir priminimai \> Priminimo laiškas \> Nustatyti priminimo laiško eiliškumą** ir nustatykite priminimo laiško eiliškumą, kaip parodyta žemiau pateiktoje lentelėje, kuri paskirta kliento registravimo profilyje.

|     Priminimo laiško kodas      |     aprašymas                           |     Valiuta      |     Pagrindinė sąskaita        |     Mokestis valiuta     |     Mažiausiai virš        |     Dienos blokuoti      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     1 priminimo laiškas         |     Antras pranešimas su mokesčiu        |     USD           |                           |     0,00                  |     0,00                  |     2                 |
|     2 priminimo laiškas         |     Antras pranešimas su mokesčiu        |     USC           |     403150                |     20.00                 |     10,00                 |     3                 |
|     Rinkimas                    |     Paskutinis pranešimas su mokesčiu         |     USD           |     403150                |     50.00                 |     100.00                |     15                |

Toliau pateikiamoje iliustracijoje rodoma informacija, kuri yra lentelėje tokia, kaip ji bus pateikta **Priminimo laiškai** puslapyje. 

[![Priminimo laiško sekos nustatymas](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)

 Dabar turite nustatyti du šiam pavyzdžiui būtinus parametrus.

2. Eikite į **Kreditai ir priminimai \> Sąranka \> Gautinų sąskaitų parametrai** ir atlikite šiuos veiksmus:

    1. **Priminimai** skirtuke nustatykite **Nepaisyti mokėjimų ir kreditų pažymų skaičiuojant priminimo laiško kodą** parinktį į **Taip**.
    2. Įsitikinkite, kad lauke **Kurti priminimo laišką** nustatytas į **Klientas**.

    [![Gautinų sąskaitų parametrų Kredito priminimams nustatymas](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)

3. Eikite į **Gautinos sąskaitos  \> Sąskaitos faktūros \> Visi laisvos formos teksto sąskaitos faktūros** ir tada pasirinkite **Nauja**, ir tada atlikite šiuos veiksmus:

    1. Lauke **Kliento sąskaita** pasirinkite **JAV-045**.
    2. Lauke **Sąskaitos faktūros data** įveskite **2021-01-15**.
    3. Lauke **Termino pabaigos data** įveskite **2021-01-16**.
    4. „FastTab”  **Sąskaitos faktūros eilutės** skirtuke **Pagrindinė sąskaita** įveskite **401100**.
    5. Lauke **Vieneto kaina** įveskite **500.00**.
    6. Pasirinkite **Registruoti**.

    Dabar turite įvesti dvi kliento kredito pažymas.

4. Pasirinkite **Nauja** ir atlikite tolesnius veiksmus:

    1. Lauke **Kliento kodas** pasirinkite **„US-045”**.
    2. Lauke **Sąskaitos faktūros data** įveskite **2021-01-15**.
    3. Lauke **Termino pabaigos data** įveskite **2021-01-16**.
    4. „FastTab”  **Sąskaitos faktūros eilutės** skirtuke **Pagrindinė sąskaita** įveskite **401100**.
    5. Lauke **Vieneto kaina** įveskite **-100,00**.
    6. Pasirinkite **Registruoti**.

5. Pakartokite 4-ą veiksmą, bet įveskite **-200,00** **Vieneto kaina** lauke.
6. Eikite į **Gautinos sąskaitos  \> Klientai \> Visi klientai** ir pasirinkite klientą **JAV-045**. Tada Veiksmų srityje pasirinkite **Operacijos \> Operacijos**, kad peržiūrėtumėte anksčiau paskelbtas kliento operacijas.

    [![Paskelbtų kliento operacijų peržiūra](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)

    Dabar privalote sukurti priminimo laiškus klientui JAV-045.

7. Eikite į **Kreditai ir priminimai  \> Priminimo laiškas \> Sukurti priminimo laiškus** ir atlikite žemiau pateiktus veiksmus:

    1. Nustatykite **Sąskaita faktūra** ir **Kredito pažyma** parinktis į **Taip**.

        Pagal numatytuosius nustatymus, lauke **Priminimo laiškas** turėtų būti nustatytas į **Kliento priminimas**.

    2. Lauke **Priminimo laiško data** įveskite **2021-01-19**.
    3. „FastTab” skirtuke **Įrašai, kuriuose reikia įtraukti** pasirinkite **Filtruoti** ir tada lauke **Kliento paskyra** pridėkite kliento **JAV-045**.
    4. Pasirinkite **Gerai**.
    5. Pasirinkite **Gerai**, kad sukurtumėte priminimo laiškus.

8. Eikite į **Kreditai ir priminimai  \> Priminimo laiškas \>Peržiūrėti ir apdoroti priminimo laiškus** ir atlikite žemiau pateiktus veiksmus:

    1. Atkreipkite dėmesį, kad priminimo laiško kodas antraštėje ir operacijų eilutėse yra **Priminimo laiškas Nr. 1**, nes šis priminimo laiškas yra pirmas priminimo laiškas pagal eiliškumą. (Norėdami peržiūrėti operacijos eilutes, jums gali tekti pasirinkti **Operacijos** „FastTab” skirtuke.)

   [![Patikrinimas, ar antraštėje ir eilutėse rodomas toks pats priminimo laiško kodas](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)

    2. Veiksmų srityje pasirinkite **Registruoti**.
    3. Lauke **Registravimo data** įveskite **2021-01-19**.

    Dabar privalote vėl sukurti priminimo laiškus klientui JAV-045.

9. Eikite į **Kreditai ir priminimai  \> Priminimo laiškas \> Sukurti priminimo laiškus** ir atlikite žemiau pateiktus veiksmus:

    1. Nustatykite **Sąskaita faktūra** ir **Kredito pažyma** parinktis į **Taip**.

        Pagal numatytuosius nustatymus, lauke **Priminimo laiškas** turėtų būti nustatytas į **Kliento priminimas**.

    2. Lauke **Priminimo laiško data** įveskite **2021-01-23**.
    3. „FastTab” skirtuke **Įrašai, kuriuose reikia įtraukti** pasirinkite **Filtruoti** ir tada lauke **Kliento paskyra** pridėkite kliento **JAV-045**.
    4. Pasirinkite **Gerai**.
    5. Pasirinkite **Gerai**, kad sukurtumėte priminimo laiškus.

10. Eikite į **Kreditai ir priminimai  \> Priminimo laiškas \>Peržiūrėti ir apdoroti priminimo laiškus** ir atlikite žemiau pateiktus veiksmus:

    1. Atkreipkite dėmesį, kad priminimo laiško kodas antraštėje yra **Priminimo laiškas Nr. 1**. Tačiau operacijos eilučių kodas yra **Priminimo laiškas Nr. 2**.

   [![Patikrina, ar antraštėje ir eilutėse rodomi skirtingi priminimo laiško kodai](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)

  Kodai skiriasi, nes **Ignoruoti mokėjimus ir kredito pažymas skaičiuojant priminimo laiškų kodą** parinktis nustatyta į **Taip**.

  2. Neregistruokite šio priminimo laiško.

11. Eikite į **Kreditas ir priminimai \> Sąranka \> Gautinų sąskaitų parametrai** ir tada **Priminimai** skirtuke nustatykite **Nepaisyti mokėjimų ir kredito pažymų skaičiuojant laiško kodą** parinktį į **Ne**.

    [![Nustatykite parinktį „Nepaisyti mokėjimų ir kredito pažymų apskaičiuojant priminimo laiško kodą” į Ne](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)

    Dabar privalote vėl sukurti priminimo laiškus klientui JAV-045.

12. Eikite į **Kreditai ir priminimai  \> Priminimo laiškas \> Sukurti priminimo laiškus** ir atlikite žemiau pateiktus veiksmus:

    1. Nustatykite **Sąskaita faktūra** ir **Kredito pažyma** parinktis į **Taip**.

        Pagal numatytuosius nustatymus, lauke **Priminimo laiškas** turėtų būti nustatytas į **Kliento priminimas**.

    2. Lauke **Priminimo laiško data** įveskite **2021-01-23**.
    3. „FastTab” skirtuke **Įrašai, kuriuose reikia įtraukti** pasirinkite **Filtruoti** ir tada lauke **Kliento paskyra** pridėkite kliento **JAV-045**.
    4. Pasirinkite **Gerai**.
    5. Pasirinkite **Gerai**, kad sukurtumėte priminimo laiškus.

13. Eikite į **Kreditas ir priminimai \> Priminimo laiškas \> Peržiūrėti ir apdoroti priminimų laiškus** ir atkreipkite dėmesį, ar priminimo laiško kodas antraštėje ir operacijų eilutėse yra **Priminimo laiško Nr. 2**.

    [![Tokio paties priminimo laiško kodo antraštėje ir eilutėse pakartotinis rodymas](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)

    Toks pat kodas atsiras abiejose vietose, nes **Nepaisyti mokėjimų ir kredito pažymų skaičiuojant priminimo laiško kodą** parinktis dabar nustatyta į **Ne**.
