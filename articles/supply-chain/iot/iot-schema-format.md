---
title: „IoT Hub“ schemos formatų pranešimai
description: Šioje temoje paaiškinama, kaip sukurti pranešimo schemą, kurią galite naudoti su „IoT“ įžvalgomis.
author: robinarh
ms.date: 04/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ecf4a70d69d24ea75f5448339057e7017cb93af
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/19/2021
ms.locfileid: "7652045"
---
# <a name="schema-formats-for-iot-hub-messages"></a>„IoT Hub“ schemos formatų pranešimai

[!include [banner](../../includes/banner.md)]

Šioje temoje paaiškinama, kaip sukurti pranešimo schemą, kurią galite naudoti su „IoT“ įžvalgomis.

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