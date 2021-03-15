---
title: IoT analizės stebėjimas ir valdymas
description: Šioje temoje aiškinama, kaip stebėti ir valdyti IoT analizę.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7082f9e7640e8ef1b2873a954327b61a440e8ad0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000011"
---
# <a name="monitor-and-manage-iot-intelligence"></a>IoT analizės stebėjimas ir valdymas

[!include [banner](../../includes/banner.md)]

Šioje temoje aiškinama, kaip stebėti ir valdyti IoT analizę.

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a>Scenarijų stebėjimas programoje „Microsoft Dynamics 365 Supply Chain Management“

IoT analizės apdorojimą galite stebėti keliose vietose.

+ **Moduliai \> Gamybos kontrolė \> Užklausos ir ataskaitos \> IoT analizė \> Pranešimai** – peržiūrėkite neišspręstų pranešimų sąrašą.
+ **Moduliai \> Gamybos kontrolė \> Užklausos ir ataskaitos \> IoT analizė \> Uždaryti pranešimai** – peržiūrėkite išspręstų arba atmestų pranešimų sąrašą.
+ **Moduliai \> Gamybos kontrolė \> Užklausos ir ataskaitos \> IoT analizė \> Metrikos raktai** – peržiūrėkite laiko sekų diagramų **Išteklių būsena** metrikos raktus.
+ **Moduliai \> Gamybos kontrolė \> Gamybos vykdymas \> Išteklių būsena** – sekite specifinę metriką naudodami dialogo langą **Konfigūruoti**. Jei scenarijus aptinka išimtį, pranešime pateikiama išsami išimties informacija.
+ **Darbo sritys \> Gamybos vietos valdymas \> Pranešimai** – peržiūrėite neišspręstų pranešimų sąrašą.

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

+ [IoT kūrimo rinkinio AZ3166 prijungimas prie „Azure IoT Hub“](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [„Raspberry Pi“ internetinio simuliatoriaus prijungimas prie „Azure IoT Hub“ (Node.js)](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [Įrenginių modeliavimo sprendimų spartintuvo apžvalga](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]