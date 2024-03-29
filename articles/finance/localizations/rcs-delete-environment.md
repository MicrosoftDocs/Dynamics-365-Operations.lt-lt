---
title: „Regulatory Configuration Service“ (RCS) – RCS aplinkos naikinimas
description: Šiame straipsnyje paaiškinama, kaip reguliavimo konfigūracijos tarnybos (RCS) sistemos administratorius gali panaikinti RCS aplinką ir susijusius duomenis.
author: kfend
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, System Admin
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.custom: 97423
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
ms.openlocfilehash: bdcb6820ead72fce0f89bf80cc5e474cb3942724
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277247"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>„Regulatory Configuration Service“ (RCS) – RCS aplinkos naikinimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip reguliavimo konfigūracijos tarnybos (RCS) sistemos administratorius gali panaikinti RCS aplinką ir susijusius duomenis.

Kad būtų galima užbaigti šiame straipsnyje nurodytą procedūrą, turi būti įvykdytos šios būtinosios sąlygos:

- Privalote turėti jums priskirtą **Sistemos administratoriaus** vaidmenį RCS aplinkai.
- **Sistemos administratoriaus** vaidmuo privalo turėti jam priskirtą **„RCSDeleteEnvironmentDuty”** vaidmenį.

## <a name="delete-an-rcs-environment"></a>RCS aplinkos naikinimas

1. Atidarykite RCS ir pasirinkite **Elektroninių ataskaitų** darbo srities plytelę.
2. Skyriuje **Susiję saitai** pasirinkite **Naikinti RCS aplinką**.

    ![RCS aplinkos saito naikinimas Susijusių nuorodų skyriuje.](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. Pasirodžiusiame dialogo lange peržiūrėkite pranešimus apie aplinkos naikinimo aprėptį.

    ![Pranešimai RCS aplinkos naikinimo dialogo lange.](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > RCS aplinkos panaikinimo negalima atšaukti.
    >
    > Operacija panaikina pasirinktą RCS aplinką ir visus susijusius duomenis, įskaitant funkcijas ir konfigūracijas, saugomas visuotinėje saugykloje. Funkcijos ir konfigūracijos, bendrai naudojamos su kitomis organizacijomis, nebebus bendrinamos, jei neturi priklausomybių. Funkcijos ir konfigūracijos, kurios turi priklausomybių, bus pažymėtos kaip nutrauktos.

4. Pateiktame lauke įveskite RCS aplinkos globaliai unikalų identifikatorių (GUID), kad patvirtintumėte, jog norite ją panaikinti. Aplinkos GUID yra įtrauktas į naikinimo pranešimą.
5. Pasirinkite **Naikinti aplinką**.
    
Dabar jūsų RCS aplinka ir visi susiję duomenys yra panaikinti.

> [!IMPORTANT]
> Panaikinus RCS aplinką, nėra jokio būdo atkurti duomenis. Naują RCS aplinką galima sukurti bet kuriame galimame RCS regione.
