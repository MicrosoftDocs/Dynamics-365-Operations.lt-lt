---
title: Klasterio paėmimo nustatymas
description: Šiame straipsnyje aprašoma, kaip nustatyti klasterio paėmimą ir kaip taikyti prekių patvirtinimą naudojant klasterio paėmimą.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm, WHSWorkCluster
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0ec3de073def2ff63af3c04b5696cbcec4f09948
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014769"
---
# <a name="set-up-cluster-picking"></a>Klasterio paėmimo nustatymas

[!include[banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip leisti darbuotojams naudoti savo mobiliųjų įrenginių paėmimo į klasterius grupes grupavimui, kad jie galėtų vienu metu paimti prekes iš vienos vietos keliems darbo užsakymams. Tai vadinama *klasterio paėmimu*.

## <a name="about-cluster-picking"></a>Apie klasterio paėmimą

Pateikus darbo užsakymus į sandėlį, darbuotojas gali naudoti mobilųjį įrenginį norėdamas priskirti užsakymus klasteriui. Klasteris darbuotojui suorganizuos paėmimo darbą. Kai darbo užsakymas priskiriamas klasteriui, darbuotojas turi naudoti klasterio paėmimą, kad atliktų užsakymo paėmimo darbą. Darbuotas negali naudoti kitų paėmimo būdų. Jei darbo užsakymas klasteriui priskiriamas per klaidą, darbuotojas turi išskaidyti klasterį ir perkurti.

Jei reikia, darbuotojas gali perduoti klasterį kitam darbuotojui. Tada klasterio būsena pakeičiama į Perduota. Kai darbuotojas naudoja mobilųjį įrenginį norėdamas nurodyti, kad paėmimo ir atidėjimo darbas baigtas, siuntą arba krovinį reikia patvirtinti kliente.

## <a name="enable-cluster-picking"></a>Klasterio paėmimo įgalinimas

Norėdami įgalinti klasterio paėmimą, turite nustatyti taip:

- **Klasterio šablonai** – nurodykite, ar norite automatiškai sugeneruoti klasterio ID, naudotinų padėčių skaičių, kada klasterius skaidyti ir kaip nuosekliai išdėstyti bei patikrinti paėmimo darbą.

- **Darbo šablonai** – apibrėžkite, kaip sukurti klasterio paėmimo darbą.

- **Vietos nurodymai** – nurodykite, iš kur prekes paimti ir kur jas padėti.

- **Mobiliojo įrenginio meniu elementai** – sukonfigūruokite mobiliojo įrenginio meniu elementą norėdami naudoti esamą darbą, kurį nurodo klasterio paėmimas. Tada turite įtraukti meniu elementą į mobiliojo įrenginio meniu, kad jis būtų rodomas mobiliuosiuose įrenginiuose.

- **Sandėlio valdymo parametrai** – nurodykite numeraciją, naudotiną norint sugeneruoti klasterių identifikatorius.

## <a name="set-up-a-cluster-profile"></a>Klasterio šablono nustatymas

Norėdami nustatyti klasterio šabloną atlikite šiuos veiksmus:

1. Spustelėkite **Sandėlio valdymas** \> **Sąranka** \> **Mobilusis įrenginys** \> **Klasterio šablonai**.

1. Norėdami sukurti naują šabloną spustelėkite **Naujas**.

1. Spustelėję **Sukurti klasterį**, o po to srityje **Klasterio rūšiavimas** spustelėję **Naujas** nustatykite klasterio rūšiavimo kriterijus. Rūšiavimo kriterijai valdo tvarką, kuria darbuotojas atliks paėmimo darbą. Galite įtraukti tiek kriterijų, kiek reikia.

1. Lauke **Eilės numeris** įveskite skaičių norėdami apibrėžti rūšiavimo kriterijų apdorojimo tvarką.

1. Lauke **Lauko pavadinimas** pasirinkite lauką, kuris nustatys rūšiavimą. Pavyzdžiui, jei pasirenkate lauką **WMSLocationId**, darbas bus rūšiuojamas pagal vietą.

1. Lauke **Rūšiavimas** pasirinkite vieną iš toliau nurodytų pasirinkčių.

| **Parinktis**     | **Aprašas**                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Didėjančiai**  | Paėmimo darbo seka nustatoma didėjimo tvarka remiantis rūšiavimo kriterijais. Pavyzdžiui, jei kaip rūšiavimo kriterijus naudojate lauką **WMSLocationId**, o jūsų vietos ID yra 1, 2, 3 ir 4, pirmiausia bus imama iš 4 vietos. |
| **Mažėjančiai** | Paėmimo darbo seka nustatoma mažėjimo tvarka remiantis rūšiavimo kriterijais. Pavyzdžiui, jei kaip rūšiavimo kriterijus naudojate lauką **WMSLocationId**, o jūsų vietos ID yra 1, 2, 3 ir 4, pirmiausia bus imama iš 1 vietos. |

## <a name="item-confirmation"></a>Prekės patvirtinimas

Kai taikomas klasterio pasirinkimas, būtina patvirtinti prekes, kad būtų galima patikrinti į klasterius įtraukiamas prekes. Galite patikrinti prekes atlikdami klasterių pasirinkimą, vykstant klasterio parinkimo procesui. Sąranka pagrįsta produkto brūkšninio kodo sąranka.

### <a name="set-up-item-verification-with-cluster-picking"></a>Prekės patikrinimo nustatymas atliekant klasterio parinkimą

1. Eiti į sandėlio **valdymo nustatymo** > **mobiliojo** > **įrenginio** > **mobiliojo įrenginio meniu elementus**.
1. Sąrašo srityje pasirinkite norimą nustatyti meniu elementą.
1. Veiksmų srityje pasirinkite darbo **patvirtinimo nustatymą**.
1. Atlikite vieną iš toliau nurodytų veiksmų.
    - Jei jau yra darbo tipo, kurį **norite** nustatyti, eilutė, pasirinkite ją, o tada **veiksmų** srityje pasirinkite Redaguoti.
    - Jei nėra tinkamos eilutės, veiksmų srityje **pasirinkite** Nauja ir tada nustatykite **atitinkamą** darbo tipą.
1. Pažymėkite naujos **arba pasirinktos** eilutės žymės langelį Produkto patvirtinimas. Taip darbuotojai galės tikrinti kiekvieną atsargų dalį naudodami mobilųjį įrenginį.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]