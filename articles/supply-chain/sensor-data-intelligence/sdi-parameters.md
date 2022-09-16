---
title: „Sensor Data Intelligence“ parametrai
description: Šiame straipsnyje pateikta informacija apie konfigūracijos parametrus, kurie galimi "Jutiklio duomenų tyrimų" parametrų puslapyje.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreServiceParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 4a6665cc078e54da4ebb7920ec8826352ab7a816
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/08/2022
ms.locfileid: "9429004"
---
# <a name="sensor-data-intelligence-parameters"></a>„Sensor Data Intelligence“ parametrai

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

" **Jutiklio duomenų įžvalgų** " puslapis pateikia keletą parametrų, kuriuos galite naudoti funkcijai konfigūruoti. Šie parametrai apima "Azure" ryšio parametrus ir parametrą įspėjimo pranešimų, siunčiamų vartotojams atsakant į matavimo matus, naudojimo laikotarpį.

## <a name="read-and-change-connection-details-for-your-azure-iot-solution"></a>Perskaitykite ir keiskite "Azure IoT" sprendimo ryšio informaciją

Paprastai nustatote savo "Azure IoT" sprendimą ir prijungi jį prie "Microsoft Dynamics 365 Supply Chain Management **" iš "Deploy" ir "Azure** " išteklių puslapio, kuris padės jums atlikti abi procedūras. (Daugiau informacijos žr. [Įdiekite "Azure" IOT sprendimą](sdi-deploy-iot-solution-on-azure.md).) Taip pat galite peržiūrėti ir redaguoti ryšio informaciją bet kuriuo metu tiekimo grandinės valdymo skyriuje, atlikite šiuos veiksmus.

1. Eiti į sistemos **administravimo nustatymo \> " \> Jutiklio duomenų" duomenų tyrimų \> parametrus**.
1. **Skirtuko Laiko** **serija lauke Redis metrinių** saugyklų ryšio eilutė įveskite "Azure IoT" sprendimo, prie kurio norite prisijungti, **pirminio jungimosi eilutę (StackExchange.Redis).** Norėdami gauti daugiau informacijos apie šios vertės surasti, žr. [IoT sprendimą įdiekite "Azure"](sdi-deploy-iot-solution-on-azure.md).
1. Skirtuke **Integravimas**, programos kliento **Azure AD ID** lauke įveskite **"Azure" "Azure" "IoT" sprendimo, prie kurio norite prisijungti, ID** vertę. Norėdami gauti daugiau informacijos apie šios vertės surasti, žr. [IoT sprendimą įdiekite "Azure"](sdi-deploy-iot-solution-on-azure.md).

## <a name="set-the-lifetime-of-alert-messages"></a>Nustatyti įspėjimo pranešimų naudojimo laikotarpį

Kiekvieną kartą, kai Jutiklio duomenų įžvalgos aptinka situaciją, į kurią reikia atkreipti vartotojo dėmesį, jis siunčia pranešimą susijusiems vartotojams. Norėdami neleisti, kad sistemoje šie pranešimai nebūtų kraunami, turite nustatyti, kad po kelių dienų jie baigtųsi galioti.

1. Eiti į sistemos **administravimo nustatymo \> " \> Jutiklio duomenų" duomenų tyrimų \> parametrus**.
1. Skirtuke **Pranešimai** lauke Pranešimų dienos **iki** tiesioginio įveskite dienų, per kiek reikia išsaugoti pranešimą, skaičių. Pasibaigus nurodytam laikui, pranešimas bus panaikintas.
