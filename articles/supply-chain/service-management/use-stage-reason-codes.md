---
title: "Etapo priežasties kodų naudojimas"
description: "Naudokite priežasties kodą, kad nurodytumėte, kodėl teikiamų paslaugų sutartis (SLA) buvo atšaukta arba kodėl viršijamas paslaugų užsakymo laiko limitas, nurodytas SLA."
author: YuyuScheller
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e42172fe1b484b91e9a3e3d05d438e7e9b0b0eb4
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

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

  



