---
title: Duomenų laukų įtraukimas į mokesčių konfigūracijas
description: Šiame straipsnyje paaiškinama, kaip pritaikyti mokesčių konfigūracijas, pridedant duomenų laukus.
author: Kai-Cloud
ms.date: 10/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 894c42f444d27b807288b84c7b9c620ad0121fa9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872332"
---
# <a name="add-data-fields-in-tax-configurations"></a>Duomenų laukų įtraukimas į mokesčių konfigūracijas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip pritaikyti mokesčių konfigūracijas naudojant [duomenų laukus, kurie įtraukiami į mokesčių integravimą](tax-service-add-data-fields-tax-integration-by-extension.md).

## <a name="customize-the-tax-data-model"></a>Mokesčių duomenų modelio tinkinimas

1. Microsoft Dynamics 365 finansuose eikite į elektroninių **ataskaitų mokesčių** > **konfigūracijas**.
2. Konfigūracijos medyje pasirinkite **Mokesčių skaičiavimo duomenų modelis**. Tada, veiksmų srityje pasirinkite **Kurti konfigūraciją**. 

  > [!NOTE] 
  > Jei konfigūracijos teikėjo nėra, sukurkite vieną ir padarykite jį aktyvų jūsų mokesčių konfigūracijai. Daugiau informacijos žr. [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
  
3. Iššokančiame dialogo lange pasirinkite **Apmokestinamo dokumento modelis, sudarytas iš Pavadinimo: Mokesčio skaičiavimo duomenų modelis**, įveskite naujo mokesčių duomenų modelio pavadinimą, o tada pasirinkite **Kurti konfigūraciją**.
4. Pasirinkite ką tik sukurtą mokesčių duomenų modelį, tada veiksmų srityje pasirinkite **Konstruktorius**.
5. Išplėskite duomenų modelio medį, **pasirinkite** Eilutės, tada pasirinkite **Naujas**.
6. Dialogo lange **Kurti mazgą** įveskite pavadinimą, nurodykite prekės tipą, tada pasirinkite **Įtraukti**.
7. Pridėkite būtinus stulpelius.
8. Veiksmų juostoje pasirinkite **Įrašyti** ir tada pasirinkite **Užbaigta**.
9. Uždaryti puslapį ir peržiūrėti jūsų mokesčių duomenų modelio užbaigtą versiją.

## <a name="customize-the-tax-configuration"></a>Tinkinti mokesčių konfigūravimą

1. „Finance“, eikite į **Elektroninės ataskaitos** > **Mokesčių konfigūravimas**.
2. Konfigūracijos medyje pasirinkite **Mokesčių skaičiavimo Konfigūracija**. Tada, veiksmų srityje pasirinkite **Kurti konfigūraciją**.
3. Iššokančiame dialogo lange pasirinkite **Mokesčių aptarnavimo konfigūracija, išvesta iš Pavadinimo: Mokesčio skaičiavimo Konfigūracija, „Microsoft”**, įveskite naujos mokesčių konfigūracijos pavadinimą, o tada pasirinkite **Kurti konfigūraciją**.
4. Pasirinkite ką tik sukurtą mokesčių konfigūravimą, tada veiksmų srityje pasirinkite **Konstruktorius**.
5. Skyriaus **Ypatybės** lauke **Duomenų modelis** pasirinkite pritaikytą mokesčių duomenų modelį, kurį sukūrėte anksčiau.
6. Lauke **Duomenų modelio** versija pasirinkite užbaigtą mokesčių duomenų modelio versiją.
7. Pasirinkite **Pridėti** ir pridėkite reikiamus mokesčių priemones.
8. Veiksmų juostoje pasirinkite **Įrašyti** ir tada pasirinkite **Užbaigta**.
9. Uždarykite puslapį ir peržiūrėkite jūsų mokesčių konfigūravimo užbaigtą versiją.

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a>Įdiegti mokesčių priemones pritaikytame mokesčių konfigūracijoje

1. „Regulatory Configuration Service“ (RCS), eikite į **Globalizavimo funkcijos** > **Mokesčiai**.
2. Pasirinkite **Įtraukti**, įveskite informaciją apie naują priemonę, tada pasirinkite **Sukurti** funkciją.
3. Skirtuke **Versijos** pasirinkite priemonę, o tada – **Redaguoti**.
4. Konfigūracijos **versijos** lauko skirtuke **Bendra pasirinkite** pritaikytą mokesčių konfigūraciją ir versiją.
5. Dialogo lange Stulpelių valdymas pasirinkite antraštę ir eilutės stulpelius, kuriuos norite įtraukti į pritaikytą mokesčių matą, tada pasirinkite rodyklės dešinėn mygtuką, norėdami juos įtraukti į **stulpelių** sąrašą **Pasirinkti**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
