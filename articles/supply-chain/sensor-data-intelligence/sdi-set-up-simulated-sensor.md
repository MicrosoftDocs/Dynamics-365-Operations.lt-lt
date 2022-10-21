---
title: Imituojamo jutiklio nustatymas bandymo tikslais
description: Šiame straipsnyje aprašoma, kaip nustatyti simuliatorių, kurį galima naudoti norint išbandyti "Jutiklio duomenų įžvalgą" neįdiegant jokių fizinių jutiklių.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: f12d6e1d417a260477b1eb4e027b850d1862f51f
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689810"
---
# <a name="set-up-a-simulated-sensor-for-testing"></a>Imituojamo jutiklio nustatymas bandymo tikslais

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Jei norite patikrinti Jutiklio duomenų tyrimų duomenis neįdiegdami jokių fizinių jutiklių, *galite naudotis Rasp azure IoT Online Simuliatoriaus* paslauga, norėdami imituoti jutiklio signalus ir siųsti juos į "Things" ("IoT") sprendimą Microsoft Azure. Daugiau informacijos apie simuliatorių ieškokite ["Connect Rasp tarpinis simuliatorius" su "Azure IoT Hub" (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started).

## <a name="video-instructions"></a>Vaizdo įrašų instrukcijos

Toliau pateiktame vaizdo įraše parodyta, kaip nustatyti bandymams sumodeliuotais jutikliais. Likusiuose šio straipsnio skyriuose tos pačios instrukcijos pateikiamos tekstiniu formatu.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE588g6]

## <a name="create-a-device-in-azure-iot-hub"></a>Įrenginio kūrimas "Azure IoT Hub"

Pirmiausia turite nustatyti įrenginį, kad būtų autentifikuoti "Azure IoT Hub" jutiklio signalai.

1. Azure, eikite į išteklių grupės, kurią sukūrėte naudoti su "Azure" duomenų paieška, išteklių sąrašą. (Daugiau informacijos žr. [Įdiekite "Azure" IOT sprendimą](sdi-deploy-iot-solution-on-azure.md).)
1. Išteklių sąraše raskite įrašą, kur laukas **Tipas nustatytas** kaip *IoT hub*. Stulpelyje **Pavadinimas** pasirinkite pavadinimą, kad atidarytumėte ištekliaus informacijos puslapį.
1. Kairiojoje naršymo srityje pasirinkite **Įrenginiai**.
1. Puslapyje Įrenginiai **pasirinkite** Įtraukti **įrenginį**.
1. Įrenginio **kūrimo puslapyje** nustatykite šiuos laukus:

    - **Įrenginio ID** – įveskite naujo įrenginio pavadinimą (pvz., *Mano–IoT–Įrenginys*).
    - **Autentifikavimo tipas** – pasirinkite simetrinį *raktus*.
    - **Automatiškai generuoti raktus** – pažymėkite šį žymės langelį.
    - **Prijungti šį įrenginį prie "IoT" centro** – pasirinkite *Įgalinti*.

1. Norėdami **grįžti** į puslapį Įrenginiai **, pasirinkite** Įrašyti.
1. Raskite naują įrenginį sąraše. Stulpelyje **Įrenginio ID** pasirinkite pavadinimą, kad atidarytumėte įrenginio informacijos puslapį. Jei sąraše nematote naujo įrenginio, atnaujinkite puslapį.
1. Kopijuoti pirminės **jungimosi eilutės** vertę (pavyzdžiui, pasirenkant mygtuką **Kopijuoti į mainų** sritį). Šios vertės jums reikės vėliau, kai rasite Rasplit Pi IoT simuliatorių, kad būtų imituoti jutiklio signalai. Todėl dabar nagrinėkime ją į tekstinį failą.

## <a name="add-the-azure-connection-string-to-the-raspberry-pi-iot-simulator"></a>Į Rasp azure Pi IoT simuliatorių įtraukti "Azure" ryšio eilutę

Atlikite šiuos veiksmus norėdami iš įrenginio, "Azure IoT Hub", įtraukti jungimosi eilutę į rasptorių tarnybos scenarijų.

1. Atidarykite [Rasplko Pi IoT simuliatorių](https://azure-samples.github.io/raspberry-pi-web-simulator/).
1. Kodų doroklio srityje raskite eilutę, kurioje yra ši komanda.

    `const connectionString = '[Your IoT hub device connection string]';`

1. Pakeisti žinyno tekstą, įskaitant skliaustelius, pirminės **ryšio eilutės** verte, kurią nukopijavote ankstesniame skyriuje. Rezultatas turi rodyti tolesnį pavyzdį.

    `const connectionString = 'HostName=XXX;DeviceId=YYY;SharedAccessKey=ZZZ';`

## <a name="add-sensor-ids-and-values-to-the-payload-in-the-raspberry-pi-iot-simulator"></a>Įtraukti jutiklio TD ir vertes į mokamo krūvio Rasprastos Pi IoT simuliatorių

Dabar turite nustatyti Rasp algalapio Pi IoT simuliatorių su modeliuotais jutikliais ir vertėmis, kurias jie siųs kaip mokami kroviniai.

- Rasplkės Pi IoT `getMessage` simuliatoriaus kodo doroklyje suraskite funkciją ir redaguokite ją, kad ji atitiktų šį kodą. (Jutikliai nustatomi eilutėse `cb()` .)

    ```cpp
    function getMessage(cb) {
        messageId++;
        sensor.readSensorData()
        .then(function (data) {
            cb(JSON.stringify({ value: 1, sensorId: 'MachineStatus' }), false);
            cb(JSON.stringify({ value: 70, sensorId: 'Quality' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'AssetMaintenance' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'ProductionDelay' }), false);
            cb(JSON.stringify({ value: 20, sensorId: 'AssetDowntime' }), false);
        })
        .catch(function (err) {
            console.error('Failed to read out sensor data: ' + err);
        });
    }
    ```

    > [!IMPORTANT]
    > Raspvz.Pi IoT simuliatoriaus kodų rengyklėje nustatyti jutiklių KODAI turi būti tokie patys, kaip jutiklių ID, kuriuos vėliau nurodysite tiekimo grandinės valdymo scenarijuose. Ankstesniame pavyzdyje kodas naudoja žmogiškuosius nuskaitomus jutiklio ID. Tačiau faktiniame scenarijuje jutiklių ID bus visuotinai unikalios identifikatoriaus (GUID) vertės, kurias pateikia jutiklių gamintojas. Šiame pavyzdyje kodai naudojami ir produkto kokybės scenarijaus, turto priežiūros scenarijaus, [...](sdi-scenario-product-quality.md)[gamybos delsos](sdi-scenario-asset-maintenance.md)[...](sdi-scenario-production-delays.md)[scenarijaus](sdi-scenario-equipment-downtime.md) ir įrenginio būsenos scenarijaus pavyzdžiuose. Todėl, naudokite šį kodą, jei dirbsite naudodami šiuos scenarijus.

## <a name="edit-the-interval-for-sending-sensor-signals"></a>Redaguoti jutiklio signalų siuntimo intervalą

Dabar turite nustatyti intervalą, kada Rasprastos Pi IoT simuliatorius turi siųsti imituojamo jutiklio signalus.

1. Rasprastos Pi IoT simuliatoriaus kodo doroklyje raskite toliau nurodytą funkciją.

    `setInterval(sendMessage, 2000);`

2. Pagal numatytuosius nustatymus Rasplit Pi IoT simuliatorius siunčia jutiklio signalą kas 2000 milisekundių (dviem sekundėmis). Jei reikia, vertę galite koreguoti.

## <a name="run-the-raspberry-pi-iot-simulator"></a>Paleisti Rasplko Pi IoT simuliatorių

- Jei norite **pradėti** simuliatorių ir pradėti siųsti modeliuojamas jutiklio duomenis, pasirinkite Vykdyti.
