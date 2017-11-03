---
title: "Kurti važtaraštį"
description: "Šioje temoje aprašoma, kaip kurti važtaraštį, kai naudojami sandėlio valdymo procesai."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b274ff572d2be9a71b91d533023b95be98591e4f
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="create-a-bill-of-lading"></a>Kurti važtaraštį

[!include[banner](../includes/banner.md)]


Šioje temoje aprašoma, kaip kurti važtaraštį, kai naudojami sandėlio valdymo procesai.  

Važtaraštis yra teisinis dokumentas, kurį pasirašo prekes siunčianti įmonė ir vežėjas. Dokumentas pridedamas prie išsiųstų prekių ir jis naudojamas kaip siuntos gavimo kvitas, kai prekės pristatomos į paskirties vietą. Jei naudojate sandėlio valdymą, važtaraštį sukurti galite dviem būdais.

  -   Kurkite ataskaitą neautomatiniu būdu, naudodami puslapį **Važtaraštis**.
  -   Generuokite ataskaitą iš **Krovinio planavimo darbo sritis**.

Jei važtaraštį generuojate iš **Krovinio planavimo darbo sritis**, krovinio būsena turi būti **Išsiųsta.** Jei krovinyje yra daugiau nei viena siunta, sukuriamas kiekvienos siuntos važtaraštis. Sukūrus važtaraštį, jį galima keisti puslapyje **Važtaraštis**.

## <a name="master-bill-of-lading"></a>Pagrindinis važtaraštis
Jei krovinyje yra daugiau nei viena siunta, galite generuoti bendrąjį važtaraštį. Jo maketas ir informacija yra tokie pat kaip važtaraščio, bet juose pateikiamas apibendrintas visų siuntų turinys. Kai puslapyje **Transportavimo valdymo parametrai** parinktis **Kurti bendrąjį važtaraštį, kai krovinyje yra daugiau nei viena siunta** nustatyta į **Taip**, bendrasis važtaraštis sugeneruojamas automatiškai, jei važtaraštį kuriate iš **Krovinio planavimo darbo sritis** ir jei yra daugiau nei viena siunta. Taip pat galite gauti važtaraščių sąrašą, spustelėdami **Susijusi informacija** &gt; **Važtaraštis**. Jei važtaraščius kuriate neautomatiniu būdu, bendrąjį važtaraštį galite kurti puslapyje **Važtaraštis**.




