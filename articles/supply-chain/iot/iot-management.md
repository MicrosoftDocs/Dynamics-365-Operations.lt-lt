---
title: IoT analizės stebėjimas ir valdymas
description: Šiame straipsnyje paaiškinama, kaip stebėti ir valdyti ĮT įžvalgas.
author: johanhoffmann
ms.date: 08/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f1804e8b9cfa407f6549dc146df17338c4d51572
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228866"
---
# <a name="monitor-and-manage-iot-intelligence"></a>IoT analizės stebėjimas ir valdymas

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

Šiame straipsnyje paaiškinama, kaip stebėti ir valdyti ĮT įžvalgas.

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a>Scenarijų stebėjimas programoje „Microsoft Dynamics 365 Supply Chain Management“

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

Galite modeliuoti gamyklos įrenginių signalus. Norėdami gauti daugiau informacijos, žr. šiuos straipsnius:

+ [IoT kūrimo rinkinio AZ3166 prijungimas prie „Azure IoT Hub“](/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [„Raspberry Pi“ internetinio simuliatoriaus prijungimas prie „Azure IoT Hub“ (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
