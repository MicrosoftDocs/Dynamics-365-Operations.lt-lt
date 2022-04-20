---
title: Nepavyko pasiekti mokesčių paslaugos
description: Šioje temoje paaiškinama, kaip spręsti nepavyko pasiekti mokesčių skaičiavimo tarnybos.
author: hangwan
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 02/16/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: f4682b83405071b4ad7647958122ab2b4e082133
ms.sourcegitcommit: 2977e92a76211875421e608555311c363cfbdc25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/16/2022
ms.locfileid: "8612322"
---
# <a name="failed-to-access-tax-service"></a>Nepavyko pasiekti mokesčių paslaugos

[!include [banner](../includes/banner.md)]


Šioje temoje paaiškinama, kaip ištaisyti mokesčių skaičiavimo tarnybos klaidą "Nepavyko pasiekti mokesčių tarnybos".

## <a name="symptoms"></a>Požymiai

Microsoft Dynamics 365 finansuose pereikite į Mokesčių nustatymo **mokesčių** \> **·** \> **konfigūracijos mokesčių** \> **tarnybos parametrus.** Skirtuke **Bendra** įgalinate pasirinktį **Įgalinti mokesčio skaičiavimą**. Jei tada bandysite pasirinkti reikšmę lauke **Funkcijos** nustatymo pavadinimas, bus klaida. Klaidos pranešimo teigiama, kad "Nepavyko pasiekti mokesčių tarnybos".

## <a name="cause"></a>Priežastis

Ši klaida įvyko, nes finansai negali pasiekti mokesčių skaičiavimo tarnybos.

## <a name="resolution"></a>Paaiškinimas 

1. Prisijunkite prie „Microsoft Dynamics“ portale „Lifecycle Services“ (LCS).
2. Aplinkos puslapio **skirtuke** Aplinkos **papildiniai suraskite** mokesčių skaičiavimo **elementą ir** peržiūrėkite jo būseną. Būsena turi būti Diegimas **arba** **Įdiegta**. Jei mokesčių skaičiavimo tarnybos priedas neįdiegtas, gausite klaidą.

## <a name="mitigation"></a>Mažinimo priemonė

1. LCS finansų **puslapio**" "**Power platform" integravimo** skyriuje **pasirinkite Diegti naują priedą**.
2. Slinkti į puslapio apačią ir pasirinkti mokesčio skaičiavimo **priedą**, kad jį įdiegtumėte.
3. Grįžkite į savo finansų aplinką ir pabandykite prieiti prie mokesčių skaičiavimo tarnybos.

> [!NOTE]
> Prieš diegdami mokesčių skaičiavimo tarnybą, peržiūrėkite būtinuosius [mokesčių skaičiavimo tarnybos komponentus](global-get-started-with-tax-calculation-service.md#prerequisites).
> 
> Jei negalite įdiegti priedo, nes nėra " **Power platform** " integravimo skyriaus, žr [. priedo peržiūrą](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Jei įdiegę papildinį vis tiek įvyko klaida, kreipkitės į sistemos administratorių.
