---
title: "Mažmeninės prekybos EKA maketo dizaino įrankio diegimas"
description: "Galite naudoti vieno spustelėjimo dizaino įrankį, norėdami kurti skirtingus „Retail Modern POS“ (MPOS) ir „Cloud POS“ horizontalaus arba vertikalaus režimo maketus, skirtus parduotuvėms, registrams, kasininkams ir vadovams."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: b33cbf67c00b6baea4393e82d19300085781af29
ms.lasthandoff: 03/31/2017


---

# <a name="install-the-retail-pos-layout-designer"></a>Mažmeninės prekybos EKA maketo dizaino įrankio diegimas

Galite naudoti vieno spustelėjimo dizaino įrankį, norėdami kurti skirtingus „Retail Modern POS“ (MPOS) ir „Cloud POS“ horizontalaus arba vertikalaus režimo maketus, skirtus parduotuvėms, registrams, kasininkams ir vadovams.

MPOS ir „Cloud POS“ grafinio dizaino sąsają kontroliuoja kasos stalčiaus skyrelio maketas. Maketas valdo įvairių objektų išdėstymą. Pavyzdžiai: visas maketas, prekių tinklelio maketas, kliento maketas, mokėjimo maketas ir įvairių meniu mygtukų maketas. Maketai taip pat valdo bendrą darbuotojams pateikiamos pardavimo sąsajos išvaizdą.

## <a name="install-the-oneclick-designer"></a>Įdiegti oneclick dizaineris
1.  Microsoft Dynamics 365 operacijoms, naudokite meniu viršuje kairėje Norėdami pereiti į **mažmeninės prekybos****prekybos**&gt;**kanalo nustatymas**&gt;**POS sąrankos**&gt;**POS**&gt;**ekrano išdėstymas**.
2.  Pasirinkite maketą, kurio programos tipas yra **Modern POS for Windows** arba **Cloud POS**, o tada spustelėkite **Maketo dizaino įrankis**.
3.  „Internet Explorer“ apačioje rodomoje pranešimų juostoje spustelėkite **Atidaryti**, kad įdiegtumėte vieno spustelėjimo dizaino įrankį. (Kitose naršyklėse pranešimų juosta gali būti rodoma kitoje vietoje.)
4.  Pasirodančiame pranešimo lauke **Programos paleidimas – saugos įspėjimas** spustelėkite **Paleisti **, kad įdiegtumėte „Retail“ dizaino įrankį. Vykdymo indikatorius rodo diegimo proceso eigą.
5.  Baigus diegti, puslapyje **Prisijungimas** įveskite savo „Microsoft Dynamics 365 for Operations“ vartotojo vardą ir slaptažodį, o tada spustelėkite **Prisijungti**, kad paleistumėte dizaino įrankį.
6.  Kai kredencialai patvirtinti ir dizaino įrankis paleistas, galima kurti savo maketą arba modifikuoti esamą maketą. [![Maketo kūrimo priemonėje vienu paspaudimu](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Maketo dizaino įrankio diegimo trikčių šalinimas
-   Spustelėjus **Dizaino įrankis** nepasirodo raginimas atsisiųsti (arba paleisti) diegimo programą arba dabartiniai saugos parametrai neleidžia failo atsisiųsti. **Sprendimai.**
    -   Įsitikinkite, kad „Internet Explorer“ iššokančiųjų langų blokavimo programa šioje svetainėje yra išjungta. Spustelėkite **parametrai**&gt;**funkcijos**&gt;**privatumo**&gt;**rasti iššokančių langų blokavimo**, ir pakeiskite, jei reikia pakeisti.
    -   „Internet Explorer“ įtraukite „Dynamics 365 for Operations“ URL į savo patikimų svetainių sąrašą. Spustelėkite **parametrai**&gt;**funkcijos**&gt;**saugumo**&gt;**patikimų svetainių**&gt;**svetainių**&gt;**pridėti**.
-   Nepavyksta paleisti programos ir nurodoma susisiekti su tiekėju. **Sprendimas.** „Internet Explorer“ įtraukite „Dynamics 365 for Operations“ URL į savo patikimų svetainių sąrašą. Spustelėkite **parametras**&gt;**funkcijos**&gt;**saugumo**&gt;**patikimų svetainių**&gt;**svetainių**&gt;**pridėti**.

**Žinoma problema:** šiuo metu dizaino įrankis naršyklėse „Google Chrome“ ir „Mozilla Firefox“ tinkamai neveikia. Mes sprendžiame šią problemą.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[„Retail Modern POS“ konfigūravimas, atsisiuntimas, diegimas ir aktyvinimas](retail-modern-pos-device-activation.md)


