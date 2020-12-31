---
title: PVM specifikacija pagal DK operacijų ataskaitą
description: Šioje temoje paaiškinama, kaip naudoti ataskaitą PVM specifikacija pagal DK operaciją, kad būtų galima peržiūrėti ir atsispausdinti informaciją apie DK operacijas, kurių PVM yra skaičiuojamas.
author: ericwang
manager: Ann Beebe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 438a640124e778b839c660f5e161efa22c319af0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445844"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a>PVM specifikacija pagal DK operacijų ataskaitą
[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip naudoti ataskaitą **PVM specifikacija pagal DK operaciją**, kad būtų galima peržiūrėti ir atsispausdinti informaciją apie DK operacijas, kurių PVM yra skaičiuojamas.

## <a name="tax-accounts-vs-non-tax-accounts"></a>Mokesčių sąskaitos, lyginant su ne mokesčių sąskaitomis

Ataskaitoje **PVM specifikacija pagal DK operaciją** rodomos mokesčių sąskaitų ir ne mokesčių sąskaitų mokesčių operacijos. Šios ataskaitos skirstomos į kategorijas toliau nurodytais būdais.

- **Mokesčių sąskaita** – sąskaita yra laikoma mokesčių sąskaita, kai užregistruojama mokesčių operacija, o pagrindinė sąskaita žurnalo eilutėje **PVM** yra mokesčių sąskaita, pvz., mokėtino PVM sąskaita arba gautino PVM sąskaita.
- **Ne mokesčių sąskaita** – sąskaita yra laikoma ne mokesčių sąskaita, kai užregistruojama mokesčių operacija, o pradinės operacijos pagrindinė sąskaita yra ne mokesčių sąskaita, pvz., įplaukų sąskaita arba išlaidų sąskaita.

Ataskaitose mokesčių sąskaitų stulpeliuose **Kilmė**, **Gautinas PVM** ir **Mokėtinas PVM** rodomas **0** (nulis). Ne mokesčių sąskaitose šiuose stulpeliuose rodomos sumos.

## <a name="filtering-the-data-on-the-report"></a>Ataskaitoje pateikiamų duomenų filtravimas

Kai generuojate ataskaitą, galimi šie numatytieji laukai. Šiuos laukus galite naudoti norėdami filtruoti duomenis, kurie rodomi ataskaitoje.

| Laukas                      | Aprašymas |
|----------------------------|-------------|
| Data                       | Norėdami nustatyti mokesčių operacijų datų intervalą, naudokite laukus dalyse **Nuo** ir **Iki**. |
| Korespondentinė sąskaita, subsąskaita               | Norėdami nustatyti pagrindinių sąskaitų intervalą, naudokite laukus dalyse **Nuo** ir **Iki**. |
| PVM kodas             | Norėdami nustatyti PVM kodų intervalą, naudokite laukus dalyse **Nuo** ir **Iki**. |
| Grupavimas                   | Pasirinkite, ar ataskaita turi būti grupuojama pagal DK sąskaitą, ar pagal PVM kodą. |
| Tarpinė suma pagal PVM kodą | Šioje parinktyje nustatykite **Taip**, kad būtų rodomos tarpinės sumos pagal PVM kodą. |
| Tik bendrosios sumos                | Šioje parinktyje nustatykite **Taip**, kad būtų rodomos tik bendrosios sumos. |
| Tik pagrindinės sąskaitos         | Šioje parinktyje nustatykite **Taip**, kad į ataskaitą būtų įtrauktos tik pagrindinės ataskaitos. |

## <a name="showing-only-non-tax-accounts-on-the-report"></a>Tik ne mokesčių sąskaitų rodymas ataskaitoje

Norėdami, kad ataskaitoje būtų rodomos tik ne mokesčių ataskaitos, nustatykite filtro sąlygą, pvz., žvaigždutę (\*), kaip parodyta toliau pateiktoje iliustracijoje.

![Ataskaita, kurioje rodomos ne mokesčių ataskaitos](media/taxspecperledgertrans.png)
