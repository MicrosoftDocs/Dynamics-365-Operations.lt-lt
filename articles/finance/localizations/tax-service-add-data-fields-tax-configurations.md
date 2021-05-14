---
title: Įtraukti duomenų laukus į mokesčių konfigūracijas
description: Šioje temoje paaiškinama, kaip pritaikyti mokesčių konfigūracijas, pridedant duomenų laukus.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 197a2d1605dd39188841aba02a71d228c7138c54
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921194"
---
# <a name="add-data-fields-in-tax-configurations"></a>Įtraukti duomenų laukus į mokesčių konfigūracijas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip pritaikyti mokesčių konfigūracijas [naudojant duomenų laukus, pridėtus prie mokesčių](tax-service-add-data-fields-tax-integration-by-extension.md) integravimo.

## <a name="customize-the-tax-data-model"></a>Mokesčių duomenų modelio tinkinimas

1. „Microsoft Dynamics 365 Finance“, eikite į **Elektroninės ataskaitos** \> **Mokesčių konfigūravimas**.
2. Konfigūracijos medyje pasirinkite **Mokesčių duomenų modelis** - Europa. Tada, veiksmų srityje pasirinkite **Kurti konfigūraciją**.
3. Išplečiamajame dialogo lange pasirinkite apmokestinamo dokumento modelį, išvestą iš pavadinimo: mokesčio duomenų modelis **– Europa, „Microsoft", įveskite naujo mokesčių duomenų modelio pavadinimą, tada pasirinkite** Kurti **konfigūraciją**.
4. Pasirinkite ką tik sukurtą mokesčių duomenų modelį, tada veiksmų srityje pasirinkite **Konstruktorius**.
5. Išplėskite duomenų modelio medį, **pasirinkite** Eilutės, tada pasirinkite **Naujas**.
6. Dialogo lange **Kurti mazgą** įveskite pavadinimą, nurodykite prekės tipą, tada pasirinkite **Įtraukti**.
7. Pridėkite būtinus stulpelius.
8. Veiksmų juostoje pasirinkite **Įrašyti** ir tada pasirinkite **Užbaigta**.
9. Uždaryti puslapį ir peržiūrėti jūsų mokesčių duomenų modelio užbaigtą versiją.

## <a name="customize-the-tax-configuration"></a>Tinkinti mokesčių konfigūravimą

1. „Finance“, eikite į **Elektroninės ataskaitos** \> **Mokesčių konfigūravimas**.
2. Konfigūracijos medyje pasirinkite **Mokesčių konfigūravimas** - Europa. Tada, veiksmų srityje pasirinkite **Kurti konfigūraciją**.
3. Išplečiamajame dialogo lange pasirinkite Mokesčių paslaugų konfigūravimą, išvestą iš pavadinimo: mokesčių konfigūravimas **– Europa, „Microsoft", įveskite naujo mokesčių konfigiūravimo pavadinimą, tada pasirinkite** Kurti **konfigūraciją**.
4. Pasirinkite ką tik sukurtą mokesčių konfigūravimą, tada veiksmų srityje pasirinkite **Konstruktorius**.
5. Skyriaus **Ypatybės** lauke **Duomenų modelis** pasirinkite pritaikytą mokesčių duomenų modelį, kurį sukūrėte anksčiau.
6. Lauke **Duomenų modelio** versija pasirinkite užbaigtą mokesčių duomenų modelio versiją.
7. Pasirinkite **Pridėti** ir pridėkite reikiamus mokesčių priemones.
8. Veiksmų juostoje pasirinkite **Įrašyti** ir tada pasirinkite **Užbaigta**.
9. Uždaryti puslapį ir peržiūrėti jūsų mokesčių konfigūravimo užbaigtą versiją.

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a>Įdiegti mokesčių priemones pritaikytame mokesčių konfigūracijoje

1. „Regulatory Configuration Service“ (RCS), eikite į **Globalizavimo funkcijos** \> **Mokesčiai**.
2. Pasirinkite **Įtraukti**, įveskite informaciją apie naują priemonę, tada pasirinkite **Sukurti** funkciją.
3. Skirtuke **Versijos** pasirinkite priemonę, o tada – **Redaguoti**.
4. Konfigūracijos **versijos** lauko skirtuke **Bendra pasirinkite** pritaikytą mokesčių konfigūraciją ir versiją.
5. Dialogo lange Stulpelių valdymas pasirinkite antraštę ir eilutės stulpelius, kuriuos norite įtraukti į pritaikytą mokesčių matą, tada pasirinkite rodyklės dešinėn mygtuką, norėdami juos įtraukti į **stulpelių** sąrašą **Pasirinkti**.
