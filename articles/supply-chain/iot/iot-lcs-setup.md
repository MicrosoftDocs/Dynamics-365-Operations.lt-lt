---
title: IoT analizės papildinio diegimas LCS
description: Šioje temoje aiškinama, kaip portale „Microsoft Dynamics Lifecycle Services“ (LCS) įdiegti IoT analizės papildinį.
author: robinarh
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2d1cc9a7535be05a3e466c27e53047d694cf0160
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826448"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>IoT analizės papildinio diegimas LCS

[!include [banner](../../includes/banner.md)]

Šioje temoje aiškinama, kaip portale „Microsoft Dynamics Lifecycle Services“ (LCS) įdiegti IoT analizės papildinį. Atkreipkite dėmesį, kad priedai negali būti įdiegti demo ar bandyminėje aplinkoje. Kad galėtumėte įdiegti papildinį, turite [sukurti „Azure“ išteklius ](iot-azure-setup.md).

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