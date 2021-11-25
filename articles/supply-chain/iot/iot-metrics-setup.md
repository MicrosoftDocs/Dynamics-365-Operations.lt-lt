---
title: IoT analizės papildiniui skirtų „IoT“ įžvalgoms
description: Šioje temoje aiškinama, kaip stebėti ir valdyti IoT įžvalgas.
author: tonyafehr
ms.date: 04/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85db0211c32ad4e27c3a9a65d2c74c5a39687f9c
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783103"
---
# <a name="set-up-metrics-for-iot-intelligence"></a>IoT analizės papildiniui skirtų „IoT“ įžvalgoms

[!include [banner](../../includes/banner.md)]

## <a name="configure-metrics"></a>Sukonfigūruokite metriką

Jei norite peržiūrėti savo pranešimų laiko serijų diagramas turite nustatyti "Microsoft Dynamics 365 Supply Chain Management“ metriką, atlikite nurodytus veiksmus.

1. Kopijuoti jungties eilutę į „Redis“ slaptą:

    1. „Azure“ portale eikite į „Redis“ slaptą.
    2. Eiti į **Parametrų** \> **Prieigos raktus**.
    3. Nukopijuokite lauke **Pagrindinė ryšio eilutė** esančią reikšmę.

2. Programoje „Supply Chain Management“ eikite į **Gamybos kontrolė \> Sąranka \> IoT įžvalgos \> Scenarijaus parametrai**.
3. Puslapyje **Scenarijaus parametrai** lauke **Laiko serijos** skirtuke, **Redis metrikos parduotuvės ryšio eilutė** laukelyje, įklijuokite jungties eilutę, kurią anksčiau nukopijavote. Šis veiksmas įgalina „Azure IoT Hub" metriką vizualizuoti „Supply Chain Management“. Įklijuoti vertę į lauką, ji rodoma kaip **\*\*\*\*\*\***.

    > [!NOTE]
    > Atnaujindami vieną iš „Redis“ slapto jungties eilučių, taip pat turite atnaujinti šį laukelį.

4. Eikite į **Gamybos kontrolės \> Užklausas ir ataskaitas \> IoT įžvalgos \> Metrinius raktus**.
5. Puslapyje **Metrinių raktų** pasirinkite **Naujinti**.
6. Dialogo lange **Atnaujinimo metrikos raktų** atkreipkite dėmesį, kad lauke pasirinkta **Vykdyti fone**. Pasirinkite **Gerai**.

Visi metriniai raktai Redis talpykloje yra nuskaitomi ir pridedami prie **Metrinių raktų** sąrašo. Metrinės vertės nebus rodomos, kol [nebus įgalinti scenarijai](iot-scenario-setup.md).

## <a name="configure-the-resource-status-time-series"></a>Išteklių būsenos laiko serijų konfigūravimas

Norėdami konfigūruoti **išteklių būsenos** laiko serijas, atlikite šiuos veiksmus.

1. „Supply Chain Management“ eikite į **gamybos kontrolės \> gamybos vykdymo \> išteklių būseną**.
2. Puslapyje **išteklių būsna** pasirinkite **Konfigūruoti**.
2. Išteklių sąraše, **Konfigūruoti** dialogo lange pasirinkite norimą stebėti **elementą**.
3. Pasirinkite **Redaguoti** mygtuką **Laiko serijos 1**.
4. Dialogo lange **Pasirinkti laiko serijas** pasirinkite metriką tinklelyje. (Taip pat galite naudoti **Atnaujinkite metrinių raktų** saitą, kad atnaujintų metrikos raktus iš šio dialogo lango.)
5. Pasirinkite **Gerai** norėdami sugrįžti į **Konfigūruoti** dialogo langą.
6. Įvesti rodomą vardą.
7. Lauke **Rodyti duomenis iš** pasirinkite laiko tarpą.
8. Pasirinkite **Gerai**.

Rodoma diagrama.

## <a name="delete-a-metric-key"></a>Metrikos rakto naikinimas

1. „Supply Chain Management“ eikite į **Gamybos kontrolės \> Užklausas ir ataskaitas \> IoT įžvalgos \> Metrinius raktus**.
2. **Metrinių raktų** puslapyje pasirinkite metrikos raktą, kad jį panaikinsite.
3. Pasirinkite **Naikinti**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]