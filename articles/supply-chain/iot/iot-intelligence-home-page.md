---
title: Pagrindinis IoT įžvalgų puslapis
description: Šioje temoje pateikiami saitai į informaciją apie IoT įžvalgas.
author: johanhoffmann
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2386d71fde8196304fde846cbff4cd45d1edc834
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674427"
---
# <a name="iot-intelligence-home-page"></a>Pagrindinis IoT įžvalgų puslapis

[!include [banner](../../includes/banner.md)]

> [!IMPORTANT]
> Ši priemonė šiuo metu galima tik šiose šalyse / regionuose:
>
> - JAV (Jungtinės Amerikos Valstijos)
> - Europos Sąjunga (ES)
> - AU (Australija)
> - CA (Kanada)
> - JK (Jungtinė Karalystė)

IoT įžvalgos yra „Microsoft Dynamics 365 Supply Chain Management“ priedas. Jis integruoja daiktų interneto (IoT) signalus su „Supply Chain Management“ duomenimis, kad būtų rastos programinės žinių.

IoT įžvalgos palaiko šiuos scenarijus:

- **Gamybos atidėjimas** – šiuo scenarijumi palyginamas faktinis ciklo laikas ir suplanuotas ciklo laikas. „Supply Chain Management“ jus informuoja, kai gamyba nesuplanuojama, kad galėtumėte pasistenti maksimaliai padidinti veiklos efektyvumą ir išvengti užsakymo vėlavimo.
- **Įrangos prastovo laikas** – šiuo scenarijumi matuojami upeiniai parametrai palyginami su vartotojo nurodytais parametrais. „Supply Chain Management“ jus praneša, kai viršijama ribinė vertė, kad galėtumėte atlikti veiksmus, pvz., perplanuoti gamybos darbo užsakymą arba kurti priežiūros darbo užsakymą.
- **Produkto kokybė** – šiuo scenarijumi lyginami jutiklio rodmenys, pvz., temperatūra ir pagal vartotojo nustatytą kokybės metriką. „Supply Chain Management“ jus praneša, kai atsiranda nuokrypis, taigi galite pasižiūrėti kokybės standartus ir sumažinti atliekas.

Toliau esanti iliustracija parodo „Azure IoT Hub", „IoT“ įžvalgos ir „Supply Chain Management“ sąveiką.

![IoT centras, IoT įžvalgos ir „Supply Chain Management“.](media/iot_intelligence.png)

<!-- KFM: hide setup info for now

## Setup

You can set up and configure IoT Intelligence without writing any code. Here are the basic steps.

1. [Set up Azure resources](iot-azure-setup.md) – Create an IoT hub, a Redis cache, and a key vault that can be accessed from Supply Chain Management.
2. [Message schema formats for IoT Hub](iot-schema-format.md) – Configure your devices to send messages to IoT Hub, and define the JavaScript Object Notation (JSON) message format.
3. In Feature Management, enable the IoT Intelligence feature flag. 
4. [Install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Install the add-in in LCS, and configure the Azure secrets.
5. [Set up metrics](iot-metrics-setup.md) – Set up metrics in Supply Chain Management.
6. [Scenario setup](iot-scenario-setup.md) – Set up the scenarios in Supply Chain Management.

-->

## <a name="tracking-and-maintenance"></a>Sekimas ir priežiūra

- [Stebėjimo scenarijai „Dynamics 365 Supply Chain Management“](iot-management.md#monitor-scenarios)
- [Scenarijaus išjungimas](iot-scenario-setup.md#disable-a-scenario)
- [Vykdomo IoT analizės scenarijaus modifikavimas](iot-management.md#modify-a-running-iot-intelligence-scenario)
- [Modeliavimo parinktys](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]