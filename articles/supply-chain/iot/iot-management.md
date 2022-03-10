---
title: IoT analizės stebėjimas ir valdymas
description: Šioje temoje aiškinama, kaip stebėti ir valdyti IoT analizę.
author: tonyafehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8fbd750aa4a316f5e04f3c8622d0847ad9318360
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782662"
---
# <a name="monitor-and-manage-iot-intelligence"></a>IoT analizės stebėjimas ir valdymas

[!include [banner](../../includes/banner.md)]

Šioje temoje aiškinama, kaip stebėti ir valdyti IoT analizę.

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a> Scenarijų stebėjimas programoje „Microsoft Dynamics 365 Supply Chain Management“

IoT analizės apdorojimą galite stebėti keliose vietose.

+ **Moduliai \> Gamybos kontrolė \> Užklausos ir ataskaitos \> IoT analizė \> Pranešimai** – peržiūrėkite neišspręstų pranešimų sąrašą.
+ **Moduliai \> Gamybos kontrolė \> Užklausos ir ataskaitos \> IoT analizė \> Uždaryti pranešimai** – peržiūrėkite išspręstų arba atmestų pranešimų sąrašą.
+ **Moduliai \> Gamybos kontrolė \> Užklausos ir ataskaitos \> IoT analizė \> Metrikos raktai** – peržiūrėkite laiko sekų diagramų **Išteklių būsena** metrikos raktus.
+ **Moduliai \> Gamybos kontrolė \> Gamybos vykdymas \> Išteklių būsena** – sekite specifinę metriką naudodami dialogo langą **Konfigūruoti**. Jei scenarijus aptinka išimtį, pranešime pateikiama išsami išimties informacija.
+ **Darbo sritys \> Gamybos vietos valdymas \> Pranešimai** – Peržiūrėkite neišspręstų pranešimų sąrašą.

## <a name="modify-a-running-iot-intelligence-scenario"></a>Vykdomo IoT analizės scenarijaus modifikavimas

Kai scenarijus vykdomas, galite atlikti toliau nurodytus keitimus.

+ Įtraukti naujų jutiklio schemos apibrėžimų.
+ Pasirinkti naujas signalų duomenų reikšmes.
+ Atšaukti esamų signalo duomenų reikšmių pasirinkimą.
+ Įtraukti ir susieti naujas signalo duomenų reikšmes.
+ Atnaujinti ribines reikšmes.

Kai scenarijus vykdomas, toliau nurodyti keitimai yra draudžiami.

+ Schemos apibrėžimų, kuriuos einamuoju metu naudoja įgalintas scenarijus, naikinimas arba modifikavimas.
+ Įgalinto scenarijaus schemos kelių keitimas.

## <a name="simulation-options"></a>Modeliavimo parinktys

Galite modeliuoti gamyklos įrenginių signalus. Daugiau informacijos ieškokite šiose temose:

+ [IoT kūrimo rinkinio AZ3166 prijungimas prie „Azure IoT Hub“](/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [„Raspberry Pi“ internetinio simuliatoriaus prijungimas prie „Azure IoT Hub“ (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [Įrenginių modeliavimo sprendimų spartintuvo apžvalga](/azure/iot-accelerators/iot-accelerators-device-simulation-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]