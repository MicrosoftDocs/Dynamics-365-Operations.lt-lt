---
title: „IoT Hub“ schemos formatų pranešimai
description: Šiame straipsnyje paaiškinama, kaip sukurti pranešimo schemą, kurią galima naudoti naudojant IOT įžvalgas.
author: johanhoffmann
ms.date: 04/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 705a2150042f9b65f1f4528d6f2699f7306996f5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887463"
---
# <a name="schema-formats-for-iot-hub-messages"></a>„IoT Hub“ schemos formatų pranešimai

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip sukurti pranešimo schemą, kurią galima naudoti naudojant IOT įžvalgas.

## <a name="message-requirements"></a>Pranešimo reikalavimai

Taikomos „IoT“ įžvalgos rinkimo pranešimų stebėjimo taisyklės:

+ Pranešimo schemos turi būti formatu „JavaScript Object Notation" (JSON).
+ UNIX **laiko žymos** ypatybė, kurioje vertė išreiškiama milisekundėmis (ms), turi būti „Microsoft Azure“ IoT Hub pranšime.
+ Pranešimas sekamas tik tada, jei jame yra visos scenarijaus nustatyme apibrėžtos ypatybės. Pavyzdžiui, jei nustatote **id**, **laiko žymę** ir **vertės** ypatybes, stebimas šis pranešimas.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    }
    ```

    Šis pranešimas nėra stebimas, nes **trūksta** vertės ypatybės.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
    }
    ```

+ „IoT“ įžvalgos nepaiso pranešimo ypatybės, kurios nėra apibrėžtos scenarijaus konfigūracijoje. Pavyzdžiui, jei nustatote **id**, **laiko žymę** ir **vertės** ypatybes, „IoT“ įžvalgos stebės šiuos pranešimus.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
        "machine" : "Machine1225",
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
         "activity": "PartOut"
    },
    ```

+ „IoT“ įžvalgos tyliuoju būdu nepaiso pranešimų, kurie neatitinka scenarijaus konfigūracijos kriterijų.
+ Galite nurodyti ir naudoti kelių tipų pranešimų schemas.
+ Būtina apibrėžti ne kiekvieną pranešimo schemos tipą. Turi būti nustatytos tik tos schemos, kurios bus naudojamos IoT įžvalgos tyrimų scenarijams.

## <a name="id-value-pair-schema"></a>ID - verčių poros schema

ID verčių pora yra bendras IoT įžvalgos pranešimo schemų šablonas. Naudodami ID verčių porą užtikrinate, kad visų scenarijų pranešimų schema yra ta pati. Pavyzdžiui, čia pateikiamas pranešimas dėl **įrangos prasto laiko** arba **gamybos delsos** scenarijaus.

```json
{
    "id": "IoTInt.Machine1225.PartOut",
    "timestamp": 1576016821614,
    "value": True
}
```

Čia pateikiamas produkto **kokybės scenarijaus** pranešimas.

```json
{
    "id": "IoTInt.Machine1225.Temperature",
    "timestamp": 1576016821614,
    "value": 105
}
```

Abiejuose pranešimuose yra **ID** ir **verčių** ypatybės. **ID** vertes galima susieti lentelėje **Signalo duomenų vertės** scenarijaus nustatymo metu. **Įrangos downtime** scenarijui jūs susiesite **IoTInt.Machine1225.PartOut** vertę. **Produkto kokybės** scenarijui jūs susiesite **IoTInt.Machine1225.Temperature** vertę.

Daugiau informacijos ieškokite [„Azure IoT Hub“ dokumentus](/azure/iot-hub/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]