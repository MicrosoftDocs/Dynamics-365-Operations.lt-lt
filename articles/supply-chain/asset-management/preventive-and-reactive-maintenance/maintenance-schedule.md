---
title: Priežiūros grafikas
description: Šiame straipsnyje paaiškinamas turto valdymo priežiūros grafikas.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectCalendarCreateWO, EntAssetObjectCalendarListPagePoolsOpen, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePreviewPart, EntAssetObjectCalendarEdit, EntAssetObjectCalendarAdjust, EntAssetObjectCalendarDiscard, EntAssetObjectCalendarInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 782a8cc1f9e64b8c2d4364212c9c5755c103bbfb
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017064"
---
# <a name="maintenance-schedule"></a>Priežiūros grafikas

[!include [banner](../../includes/banner.md)]

 

Priežiūros grafike pateikiamas sąrašas visų numatomų prevencinių priežiūros planų, priežiūros užklausų ir atliktinų priežiūros ciklų. Kai kurios grafiko eilutės gali būti konvertuotos į darbo užsakymus.

Keturi priežiūros grafiko rodiniai truputį skiriasi, priklausomai nuo priežiūros grafiko eilučių, kurias norite matyti.

| Meniu elementas                  | Turinio aprašas                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Visas priežiūros grafikas       | Visos priežiūros grafiko eilutės yra rodomos.     |
| Mano turto grafikas        | Visos priežiūros grafiko eilutės, kuriose pateikiamas įdiegtas turtas funkcinei vietai, kurioje jūs dirbate kaip darbuotojas (sąranką žr. [Priežiūros darbuotojai ir darbo grupės](../setup-for-objects/workers-and-worker-groups.md)), rodomos sąraše. |
| Atidaryti priežiūros grafiko eilutes | Priežiūros grafiko eilutės, turinčios būseną „Sukurta“, rodomos šiame sąraše – jos dar nebuvo konvertuotos į darbo užsakymą arba panaikintos.                                            |
| Atidaryti priežiūros grafiko telkinius | Šiame sąraše rodomos priežiūros grafiko eilutės, susijusios su darbo užsakymo telkiniu.                                                                                                                  |

>[!NOTE]
>Jei priežiūros grafiko eilutė įtraukiama keliuose darbo užsakymų telkiniuose (žr. [Darbo užsakymų telkiniai](../work-orders/work-order-pools.md)), kiekvienam telkiniui skiltyje **Atidaryti priežiūros grafiko telkinius** rodomas vienas įrašas. Taip siekiama optimizuoti darbo užsakymų telkinių filtravimo parinktis.

Norėdami atidaryti priežiūros grafiką:

1. Spustelėkite Turto **valdymo priežiūros planas** > **Visos** > **priežiūros grafikas arba Atidaryti** priežiūros **grafiko eilutes arba** Atidaryti **priežiūros grafiko telkinius**.

2. Kad atnaujintumėte priežiūros grafiką, spustelėkite **Priežiūros planas** arba **Priežiūros ciklai**. 

3. Galite redaguoti priežiūros grafiko eilutę ją pasirinkę ir spustelėję **Redaguoti**. Pavyzdžiui, galite lengvai atnaujinti aptarnavimo lygį arba už darbą atsakingą darbuotoją. Galite redaguoti tik tas priežiūros grafiko eilutes, kurios dar nebuvo susietos su darbo užsakymu.

4. Galite panaikinti priežiūros grafiko eilutę ją pasirinkę sąrašo puslapyje ir spustelėję **Naikinti**.

5. Galite atsisakyti priežiūros grafiko eilutės ją pasirinkę sąrašo puslapyje ir spustelėję **Atsisakyti**. Ši funkcija naudinga, pavyzdžiui, kai turtui numatytas 2 000 km priežiūros planas ir 10 000 km priežiūros planas. Tokiu atveju, greičiausiai norėsite atsisakyti sukurtos eilutės iš 2 000 km priežiūros plano, kai ji sutaps su 10 000 km, 20 000 km, 30 000 km ir t. t. Jei atsisakysite priežiūros plano eilutės, susijusios su priežiūros planu, tos eilutės daugiau nebematysite, kai planuosite tą priežiūros planą.

6. Galite pasirinkti kelias priežiūros grafiko skiltyje **Visi priežiūros grafikai** ir spustelėti **Darbo užsakymų telkinys**, jei norite įtraukti į tą patį darbo užsakymų telkinį visas pažymėtas eilutes.

7. Galite pasirinkti kelias priežiūros grafiko eilutes skiltyje **Visi priežiūros grafikai** arba **Atidaryti priežiūros grafiko eilutes**, arba **Atidaryti priežiūros grafikų telkinius** ir spustelėti **Koreguoti grafiką**, jei norite taikyti tas pačias korekcijas kelioms eilutėms. Galite keisti numatomas pradžios ir pabaigos datas, aptarnavimo lygį ir atsakingą priežiūros darbo grupę arba atsakingą priežiūros darbuotoją, susijusius su pasirinktomis priežiūros grafiko eilutėmis.

- Kai priežiūros grafiko eilutė susieta su darbo užsakymu, darbo užsakymo ID bus rodomas lauke **Darbo užsakymas**.  
- Išsamios informacijos rodinyje **Visas turtas** > „FastTab“ **Turto priežiūros planai** galite turtui pasirinkti priežiūros planus. Vėliau, jei panaikinsite priežiūros plano eilutę, susijusią su turtu, skiltyje **Visas turtas**, taip pat galėsite automatiškai panaikinti visas priežiūros grafiko eilutes, turinčias būseną „Sukurta“ ir sukurtas pagal priežiūros planą. Taip pat žr. [Sukurti turtą](../objects/create-an-object.md).

Toliau pateiktame paveikslėlyje galite matyti sąrašo puslapį **Visas priežiūros grafikas**.

![1 iliustracija.](media/16-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]