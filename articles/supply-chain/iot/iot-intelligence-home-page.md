---
title: Pagrindinis IoT įžvalgų puslapis
description: Šioje temoje pateikiami saitai į informaciją apie IoT įžvalgas.
author: robinarh
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: intro-internal
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f32cb5578f3c15a10f863980491a687f64312cd
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/19/2021
ms.locfileid: "7652044"
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

+ **Gamybos atidėjimas** – šiuo scenarijumi palyginamas faktinis ciklo laikas ir suplanuotas ciklo laikas. „Supply Chain Management“ jus informuoja, kai gamyba nesuplanuojama, kad galėtumėte pasistenti maksimaliai padidinti veiklos efektyvumą ir išvengti užsakymo vėlavimo.
+ **Įrangos prastovo laikas** – šiuo scenarijumi matuojami upeiniai parametrai palyginami su vartotojo nurodytais parametrais. „Supply Chain Management“ jus praneša, kai viršijama ribinė vertė, kad galėtumėte atlikti veiksmus, pvz., perplanuoti gamybos darbo užsakymą arba kurti priežiūros darbo užsakymą.
+ **Produkto kokybė** – šiuo scenarijumi lyginami jutiklio rodmenys, pvz., temperatūra ir pagal vartotojo nustatytą kokybės metriką. „Supply Chain Management“ jus praneša, kai atsiranda nuokrypis, taigi galite pasižiūrėti kokybės standartus ir sumažinti atliekas.

Toliau esanti iliustracija parodo „Azure IoT Hub", „IoT“ įžvalgos ir „Supply Chain Management“ sąveiką.

![IoT centras, IoT įžvalgos ir „Supply Chain Management“.](media/iot_intelligence.png)

## <a name="setup"></a>Sąranka

Galite nustatyti ir konfigūruoti „IoT“ įžvalgos nerašydami jokio kodo. Čia yra pagrindiniai veiksmai.

1. [Nustatyti „Azure" išteklius](iot-azure-setup.md) – kurti „IoT" centrą, „Redis" talpyklą ir rakto saugyklą, kurią galima pasiekti iš „Supply Chain Management“.
2. [Pranešimo schemų formatai IoT hub](iot-schema-format.md) – sukonfigūruokite savo įrenginius, kad jie siųsų pranešimus į „IoT hub“, ir nustatykite „JavaScript Object Notation" (JSON) pranešimo formatą.
3. Funkcijų valdymo srityje įgalinkite „IoT“ įžvalgos funkcijos vėliavėlę. 
4. [Įdiekite „IoT" įžvalgos papildinį į ciklo „Microsoft Dynamics Lifecycle Services“ (LCS)](iot-lcs-setup.md) – įdiekite papildinį LCS ir sukonfigūruokite „Azure" slaptumus.
5. [Nustatyti metriką](iot-metrics-setup.md) – „Supply Chain Management“ sistemos metrika.
6. [Scenarijaus nustatymas](iot-scenario-setup.md) – „Supply Chain Management“ nustatykite scenarijus.

## <a name="tracking-and-maintenance"></a>Sekimas ir priežiūra

+ [Stebėjimo scenarijai „Dynamics 365 Supply Chain Management“](iot-management.md#monitor-scenarios)
+ [Scenarijaus išjungimas](iot-scenario-setup.md#disable-a-scenario)
+ [Papildinio šalinimas](iot-lcs-setup.md#uninstall-addin)
+ [Vykdomo IoT analizės scenarijaus modifikavimas](iot-management.md#modify-a-running-iot-intelligence-scenario)
+ [Modeliavimo parinktys](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]