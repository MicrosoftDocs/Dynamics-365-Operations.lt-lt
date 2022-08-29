---
title: IoT analizės papildinio diegimas LCS
description: Šiame straipsnyje paaiškinama, kaip įdiegti "IoT Intelligence" papildinį ciklo Microsoft Dynamics tarnybose (LCS).
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
ms.openlocfilehash: e18b05be1f2ba78c71515e4e76f180355d044b98
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227841"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>IoT analizės papildinio diegimas LCS

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

Šiame straipsnyje paaiškinama, kaip įdiegti "IoT Intelligence" papildinį ciklo Microsoft Dynamics tarnybose (LCS). Atkreipkite dėmesį, kad priedai negali būti įdiegti demo ar bandyminėje aplinkoje. Kad galėtumėte įdiegti papildinį, turite [sukurti „Azure“ išteklius ](iot-azure-setup.md).

Galite nustatyti ir konfigūruoti „IoT“ įžvalgos nerašydami jokio kodo. Čia yra pagrindiniai veiksmai.

1. [Nustatyti „Azure" išteklius](iot-azure-setup.md) – kurti „IoT" centrą, „Redis" talpyklą ir rakto saugyklą, kurią galima pasiekti iš „Supply Chain Management“.
2. [Pranešimo schemų formatai IoT hub](iot-schema-format.md) – sukonfigūruokite savo įrenginius, kad jie siųsų pranešimus į „IoT hub“, ir nustatykite „JavaScript Object Notation" (JSON) pranešimo formatą.
3. Funkcijų valdymo srityje įgalinkite „IoT“ įžvalgos funkcijos vėliavėlę.
4. Įdiekite "IoT Intelligence Microsoft Dynamics " papildinį į ciklo tarnybas (LCS) – įdiekite papildinį LCS ir sukonfigūruokite "Azure" slaptumus (kaip aprašyta šiame straipsnyje).
5. [Nustatyti metriką](iot-metrics-setup.md) – „Supply Chain Management“ sistemos metrika.
6. [Scenarijaus nustatymas](iot-scenario-setup.md) – „Supply Chain Management“ nustatykite scenarijus.

## <a name="set-up-the-lcs-environment"></a>LCS aplinkos konfigūravimas

1. Atidarykite LCS ir eikite į savo „Microsoft Dynamics 365 Supply Chain Management“ aplinką.
2. Slinkite iki dalies **Aplinkos papildiniai**.
3. Pasirinkite **Diegti naują papildinį**, kad būtų rodomas aplinkoje įgalintų papildinių sąrašas.
4. Dialogo lange **Diegiamo papildinio pasirinkimas** pasirinkite **IoT analizė**.
5. Dialogo lange **Papildinio sąranka** pateikite savo „IoT Hub“ ir „Redis“ talpyklos informaciją. Reikiamas reikšmes galite rasti raktų saugykloje, kurią sukūrėte dalyje [„Azure“ išteklių kūrimas](iot-azure-setup.md).

    + **Nuomotojo ID** – „Azure“ portale eikite į raktų saugyklą, tada kairiojoje naršymo srityje pasirinkite **Apžvalga** ir nukopijuokite **Katalogo ID** reikšmę. Įklijuokite šią reikšmę dialogo lange **Papildinio sąranka**.
    + **Su „IoT Event Hub“ suderinamo galinio punkto raktų saugyklos URI** – eikite į raktų saugyklą, tada kairiojoje naršymo srityje pasirinkite **Apžvalga** ir nukopijuokite **DNS pavadinimas** reikšmę. Įklijuokite šią reikšmę dialogo lange **Papildinio sąranka**.
    + **Su „IoT Event Hub“ suderinamo galinio punkto slaptasis pavadinimas** – eikite į raktų saugyklą, tada kairiojoje naršymo srityje pasirinkite **Slaptieji raktai** ir nukopijuokite slaptojo rakto, kur saugoma „IoT Event Hub“ ryšio eilutė, pavadinimą. Įklijuokite šią reikšmę dialogo lange **Papildinio sąranka**.
    + **„Redis“ talpyklos raktų saugyklos URI** – eikite į raktų saugyklą, tada kairiojoje naršymo srityje pasirinkite **Apžvalga** ir nukopijuokite **DNS pavadinimas** reikšmę. Įklijuokite šią reikšmę dialogo lange **Papildinio sąranka**.
    + **„Redis“ talpyklos galinio punkto slaptasis pavadinimas** – eikite į raktų saugyklą, tada kairiojoje naršymo srityje pasirinkite **Slaptieji raktai** ir nukopijuokite slaptojo rakto, kur saugoma „Redis“ talpyklos ryšio eilutė, pavadinimą. Įklijuokite šią reikšmę dialogo lange **Papildinio sąranka**.

6. Pažymėkite žymės langelį, kad sutiktumėte su sąlygomis.
7. Pasirinkti **Diegti**.
8. Atidaromas pranešimo langas, kuriame nurodoma, kad „Papildinys sėkmingai pradėtas diegti“. Pasirinkite **Gerai**.

LCS sąranka dabar baigta. Kitas veiksmas – [nustatyti scenarijus](iot-scenario-setup.md).

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a>Papildinio šalinimas

1. Programoje „Supply Chain Management“ [išjunkite scenarijus](iot-scenario-setup.md#disable-a-scenario).
2. LCS eikite į „Supply Chain Management” aplinkos informaciją.
3. Slinkite iki dalies **Aplinkos papildiniai**.
4. Prie IoT analizės papildinio pasirinkite **Šalinti**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]