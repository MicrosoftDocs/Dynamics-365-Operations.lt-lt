---
title: Aptarnavimo užduočių apžvalga
description: Norėdami aprašyti aptarnavimo užsakymo metu turimą atlikti užduotį naudokite aptarnavimo užduotis. Šią informaciją gali matyti ir technikai, ir klientai.
author: sorenva
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc0dee0747c26b073d750d19328a6a59c234fd3f
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016406"
---
# <a name="service-tasks-overview"></a>Aptarnavimo užduočių apžvalga

[!include [banner](../includes/banner.md)]

Norėdami aprašyti aptarnavimo užsakymo metu turimą atlikti užduotį naudokite aptarnavimo užduotis.
Šią informaciją gali matyti ir technikai, ir klientai.

Aptarnavimo užduotis galite kurti puslapyje **Aptarnavimo užduotys** ir aptarnavimo užduotis galite susieti su tam tikra aptarnavimo sutartimi arba aptarnavimo užsakymu sukurdami aptarnavimo užduočių ryšius. Kiekvieną kartą sukūrę aptarnavimo užduoties ryšį, galite sukurti:

-  Vidines užduoties pastabas, tokias kaip smulkios techninės užklausos, kurios yra svarbios technikui.

-  Išorinės pastabos, kurias gali matyti klientas. Jose gali būti ne taip techniškai paaiškinta pagal sutartį tarp kliento ir aptarnavimo įmonės atliekama užduotis.

Sukūrę aptarnavimo užduoties ryšį tarp aptarnavimo užduoties ir aptarnavimo užsakymo arba aptarnavimo sutarties, galite nurodyti šią aptarnavimo užduotį kurdami aptarnavimo užsakymo eilutes arba aptarnavimo sutarties eilutes esamam aptarnavimo užsakymui ar aptarnavimo sutarčiai.

Kurdami aptarnavimo užsakymus iš aptarnavimo sutarties, galite naudoti kiekvienai aptarnavimo sutarties eilutei priskirtas aptarnavimo užduotis, kad sugrupuotumėte aptarnavimo užsakymo eilutes į aptarnavimo užsakymus.

## <a name="create-a-service-task"></a>Aptarnavimo užduoties kūrimas

1. Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo užduotys**.
2. Sukurkite naują eilutę.
3. Įveskite aptarnavimo ID ir aprašymą.

## <a name="example"></a>Pavyzdys

Technikas privalo atlikti dvi pavarų dėžės užduotis (aptarnavimo objektas GB-1234) kliento patalpose. Klientui sukuriama aptarnavimo sutartis ir su užduotimis susiejamos kelios operacijos. Aptarnavimo sutartis ir aptarnavimo sutarties eilutės šioms dviem užduotims parodytos čia:

### <a name="service-agreement"></a>Aptarnavimo sutartis

| Projektas | Aptarnavimo sutartis | aprašymas                                  | Grupuoti   |
|---------|-------------------|----------------------------------------------|---------|
| 9012    | 000008 \_ 001       | Patikrinimas ir programos pakeitimas – GB-1234 | Priedas |

### <a name="service-agreement-lines"></a>Aptarnavimo sutarties eilutės

| aprašymas             | Operacijos tipas | Aptarnavimo objektas | Aptarnavimo užduotis |
|-------------------------|------------------|----------------|--------------|
| Patikrinimas ir valymas | Valanda             | GB-1234        | I/C - GB1234 |
| Kelionė                  | Išlaidos          | GB-1234        | I/C - GB1234 |
| Medžiagos               | Produktas             | GB-1234        | I/C - GB1234 |
| Programos pakeitimas     | Valanda             | GB-1234        | RR - GB1234  |
| GR-1                    | Produktas             | GB-1234        | RR - GB1234  |
| GR-5                    | Produktas             | GB-1234        | RR - GB1234  |

Dviejų užduočių aptarnavimo sutarčių eilutės turi dvi prie jų pridėtas aptarnavimo užduotis. Aptarnavimo užduotys apibrėžia kiekvienai užduočiai priklausančias operacijas. Pirmuoju atveju aptarnavimo užduotis I/C - GB1234 identifikuoja visas aptarnavimo sutarties eilutes, kurios yra susijusios su objekto GB-1234 patikrinimu ir valymu. Antruoju atveju aptarnavimo užduotis RR - GB1234 identifikuoja visas aptarnavimo sutarties eilutes, kurios yra susijusios su planinio pakeitimo užduoties įvykdymu.

Aptarnavimo užduoties ryšiai, jungiantys aptarnavimo užduotis su tam tikra sutartimi yra tokie:

### <a name="service-tasks"></a>Aptarnavimo užduotys

| Aptarnavimo užduotis | Aprašymas                             | Vidinė pastaba                                                                                                                 | Išorinė pastaba                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| I/C - GB1234 | Pavarų dėžės GB-1234 patikrinimas           | GB-1234 pavarų dėžės apžiūra ir mechaninis patikrinimas bei valymas.                                                              | Planinis pavarų dėžės patikrinimas |
| RR - GB1234  | Planinis GB-1234 dalių pakeitimas | Planinis aptarnavimo GR-1 ir GR-5 komponentų pakeitimas (iki 2002 m. pagamintoms pavarų dėžėms taip pat pakeiskite GR-2 komponentą) | Planinis dalių pakeitimas  |

## <a name="group-service-orders"></a>Grupuoti aptarnavimo užsakymus

Automatiškai kurdami aptarnavimo užsakymus, aptarnavimo užduotis galite naudoti kaip grupavimo kriterijų. Norėdami sugrupuoti aptarnavimo užsakymus, aptarnavimo sutartyje nurodykite, kad pagal aptarnavimo sutartį atliekami aptarnavimo užsakymai turi būti grupuojami pagal aptarnavimo užduoties ID, laikant pastarąjį jų pradiniu grupavimo kriterijumi.

**Grupavimas pagal aptarnavimo užduotį**

1. Spustelėkite Aptarnavimo **valdymo sutartys** \> **Aptarnavimo** \> **sutartys**.
2. Skirtuke **Sąranka** pasirinkite laukelyje **Jungti aptarnavimo užsakymus** esantį kriterijų **Pagal aptarnavimo užduotį**.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]