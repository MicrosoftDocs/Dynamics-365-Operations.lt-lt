---
title: "Kurti važtaraštį"
description: "Šioje temoje aprašoma, kaip kurti važtaraštį, kai naudojami sandėlio valdymo procesai."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: b88679f1be00d6a7168c8976f0d7db894c7e77fc
ms.lasthandoff: 03/31/2017


---

# <a name="create-a-bill-of-lading"></a>Kurti važtaraštį

Šioje temoje aprašoma, kaip kurti važtaraštį, kai naudojami sandėlio valdymo procesai.  

Važtaraštis yra teisinis dokumentas, kurį pasirašo prekes siunčianti įmonė ir vežėjas. Dokumentas pridedamas prie išsiųstų prekių ir jis naudojamas kaip siuntos gavimo kvitas, kai prekės pristatomos į paskirties vietą. Jei naudojate sandėlio valdymą, važtaraštį sukurti galite dviem būdais.

  -   Kurkite ataskaitą neautomatiniu būdu, naudodami puslapį **Važtaraštis**.
  -   Generuokite ataskaitą iš **Krovinio planavimo darbo sritis**.

Jei važtaraštį generuojate iš **Krovinio planavimo darbo sritis**, krovinio būsena turi būti **Išsiųsta.** Jei yra daugiau nei vienai siuntai apkrovos, važtaraštį sukuriamas kiekvienos siuntos. Po to, kai važtaraštis buvo sukurtas jums gali keiskite jį ant to **važtaraščio** puslapis.

## <a name="master-bill-of-lading"></a>Pagrindinis važtaraštis
Jei krovinyje yra daugiau nei viena siunta, galite generuoti bendrąjį važtaraštį. Jo maketas ir informacija yra tokie pat kaip važtaraščio, bet juose pateikiamas apibendrintas visų siuntų turinys. Kai puslapyje **Transportavimo valdymo parametrai** parinktis **Kurti bendrąjį važtaraštį, kai krovinyje yra daugiau nei viena siunta** nustatyta į **Taip**, bendrasis važtaraštis sugeneruojamas automatiškai, jei važtaraštį kuriate iš **Krovinio planavimo darbo sritis** ir jei yra daugiau nei viena siunta. Taip pat galite gauti konosamentai sąrašą spustelėdami **susijusi informacija**&gt;**važtaraščio**. Jei važtaraščius kuriate neautomatiniu būdu, bendrąjį važtaraštį galite kurti puslapyje **Važtaraštis**.


