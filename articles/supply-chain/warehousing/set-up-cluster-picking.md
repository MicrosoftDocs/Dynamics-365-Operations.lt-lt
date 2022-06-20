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
ms.openlocfilehash: 3094649da2ce9a700a4d1cde236609013f4b9744
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862314"
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

1. Mobiliojo įrenginio meniu elemente atidarykite darbo patvirtinimo sąrankos formą: **Sandėlio valdymas** \> **Sandėlio valdymas** \> **Sąranka** \> **Mobilusis įrenginys** \> **Mobiliojo įrenginio meniu elementai**.

1. Mobiliojo įrenginio meniu elemente atidarykite **Darbo patvirtinimo sąranka**. Naudodamiesi parinktimi **Produkto patvirtinimas** mobiliuoju įrenginiu nuskaitydami galite patikrinti kiekvieną atsargų dalį.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]