---
title: Kurti važtaraštį
description: Šiame straipsnyje aprašoma, kaip sukurti važtaraštį, naudojant sandėlio valdymo procesus (WMS).
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68a703475191255ff6ceaee25ef8e2bdf33ba0c2
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069703"
---
# <a name="create-a-bill-of-lading"></a>Kurti važtaraštį

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip sukurti važtaraštį, naudojant sandėlio valdymo procesus (WMS).  

Važtaraštis yra teisinis dokumentas, kurį pasirašo prekes siunčianti įmonė ir vežėjas. Dokumentas pridedamas prie išsiųstų prekių ir jis naudojamas kaip siuntos gavimo kvitas, kai prekės pristatomos į paskirties vietą. Jei naudojate sandėlio valdymą, važtaraštį sukurti galite dviem būdais.

  -   Kurkite ataskaitą neautomatiniu būdu, naudodami puslapį **Važtaraštis**.
  -   Generuokite ataskaitą iš **Krovinio planavimo darbo sritis**.

Jei važtaraštį generuojate iš **Krovinio planavimo darbo sritis**, krovinio būsena turi būti **Išsiųsta.** Jei krovinyje yra daugiau nei viena siunta, sukuriamas kiekvienos siuntos važtaraštis. Sukūrus važtaraštį, jį galima keisti puslapyje **Važtaraštis**.

## <a name="master-bill-of-lading"></a>Pagrindinis važtaraštis
Jei krovinyje yra daugiau nei viena siunta, galite generuoti bendrąjį važtaraštį. Jo maketas ir informacija yra tokie pat kaip važtaraščio, bet juose pateikiamas apibendrintas visų siuntų turinys. Kai puslapyje **Transportavimo valdymo parametrai** parinktis **Kurti bendrąjį važtaraštį, kai krovinyje yra daugiau nei viena siunta** nustatyta į **Taip**, bendrasis važtaraštis sugeneruojamas automatiškai, jei važtaraštį kuriate iš **Krovinio planavimo darbo sritis** ir jei yra daugiau nei viena siunta. Taip pat galite gauti važtaraščių sąrašą, spustelėdami **Susijusi informacija** &gt; **Važtaraštis**. Jei važtaraščius kuriate neautomatiniu būdu, bendrąjį važtaraštį galite kurti puslapyje **Važtaraštis**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]