---
title: Etapo priežasties kodų naudojimas
description: Naudokite priežasties kodą, kad nurodytumėte, kodėl teikiamų paslaugų sutartis (SLA) buvo atšaukta arba kodėl viršijamas paslaugų užsakymo laiko limitas, nurodytas SLA.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4acba8f723ceb3d629671833db59c97a900c9f01
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965710"
---
# <a name="use-stage-reason-codes"></a>Etapo priežasties kodų naudojimas 

[!include [banner](../includes/banner.md)]


Naudokite priežasties kodą, kad nurodytumėte, kodėl teikiamų paslaugų sutartis (SLA) buvo atšaukta arba kodėl viršijamas paslaugų užsakymo laiko limitas, nurodytas SLA.

Jūs taip pat galite nurodyti, kad priežasties kodas yra reikalingas atšaukus SLA arba viršijus laiko limitą, nurodytą paslaugų užsakymo SLA.

Jei nurodėte, kad priežasties kodas yra reikalingas, reikia įvesti priežasties kodą toliau nurodytais atvejais.

  - Kai paslaugų užsakymas yra perkeliamas į etapą, kuriame paslaugų trukmės įrašymas yra stabdomas pagal SLA.

  - Kai aptarnavimo užsakymas yra baigtas.

  - Kai laiko įrašymas yra sustabdomas rankiniu būdu.

## <a name="set-up-reason-codes"></a>Nustatyti priežasčių kodus

1.  Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo užsakymai** \> **Etapo priežasties kodai**.

2.  Formoje **Etapo priežasties kodai** spustelėkite **Naujas**, kad sukurtumėte naują priežasties kodą.

3.  Lauke **Etapo priežasties kodai** įveskite unikalųjį etapo priežasties kodą.

4.  Lauke **Aprašas** įveskite etapo priežasties kodo aprašą.

5.  Uždarę formą įrašysite savo pakeitimus.

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a>Priežasties kodų reikalavimas, kai atšaukiama aptarnavimo lygio sutartis

1.  Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo valdymo parametrai**.

2.  Formoje **Aptarnavimo valdymo parametrai** spustelėkite nuorodą **Bendra**, tada pasirinkite žymės langelį **Atšaukimo priežasties kodas**.

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a>Reikalavimas nurodyti priežasties kodus, kai viršijamas paslaugų užsakymo laiko limitas, nustatytas teikiamų paslaugų sutartyje

1.  Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo valdymo parametrai**.

2.  Formoje **Aptarnavimo valdymo parametrai** spustelėkite nuorodą **Bendra**, tada pasirinkite žymės langelį **Laiko viršijimo priežasties kodas**.

## <a name="see-also"></a>Taip pat žiūrėkite

[Aptarnavimo užsakymo laiko įrašymo pradžia ir sustabdymas](start-and-stop-time-recording-on-a-service-order.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]