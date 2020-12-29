---
title: Planavimas, kai turimi kiekiai neigiami
description: Šioje temoje paaiškinama, kaip tvarkomas neigiamas turimas kiekis naudojant planavimo optimizavimo funkciją.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 72367927a11879adffe68d7242d88f5cfab73e22
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433564"
---
# <a name="planning-with-negative-on-hand-quantities"></a>Planavimas, kai turimi kiekiai neigiami

[!include [banner](../../includes/banner.md)]

Jei sistemoje rodomas neigiamas bendrasis turimas kiekis, planavimo mechanizmas kiekį laiko 0 (nuliu), kad padėtų išvengti tiekimo pertekliaus. Toliau nurodyta, kaip ši funkcija veikia.

1. Planavimo optimizavimo funkcija sujungia turimus kiekius taikydama mažiausią padengimo dimensijų lygį. (Pavyzdžiui, jei *vieta* nėra padengimo dimensija, planavimo optimizavimo funkcija turimus kiekius sujungia *sandėlio* lygiu.)
1. Jei bendrasis turimas kiekis taikant mažiausią padengimo dimensijų lygį yra neigiamas, sistema daro prielaidą, kad turimas kiekis tikrai yra 0 (nulis).

> [!IMPORTANT]
> Planavimo sistema gali būti tik tiek tiksli, kiek tikslūs įvesti duomenys. Jei įvesti duomenys yra netikslūs, neigiamo turimo kiekio įrašai nurodys, kad „Microsoft Dynamics 365 Supply Chain Management“ atsargų informacija nesusinchronizuota su realiu pasauliu. Todėl planavimo rezultatas bus klaidingas. Norėdami gauti tikslų planavimo rezultatą, turite sumažinti įrašų, kuriuose rodomas neigiamas turimas kiekis, skaičių.

## <a name="example-1"></a>1 pavyzdys

13 sandėlis sukonfigūruotas taip, kaip nurodyta toliau.

- **Padengimo kodas:** min. / maks.
- **Minimalus** 15 vienetų (vnt.)
- **Maksimalus:** 25 vnt.

Mažiausias padengimo dimensijų lygis yra *sandėlis*, o tolesni turimi kiekiai įrašomi *vietos* lygiu.

- **1 objektas, 13 sandėlis, 1 vieta:** 20 vnt.
- **1 objektas, 13 sandėlis, 2 vieta:** &minus;8 vnt.

Todėl bendrasis turimas 13 sandėlio kiekis yra 12 vnt. (= 20 vnt. &minus; 8 vnt.).

Šiuo atveju planavimo mechanizmas naudoja 12 vnt. bendrąjį turimą kiekį. 13 sandėlyje.

Rezultatas yra suplanuotas 13 vnt. užsakymas (= 25 vnt. &minus; 12 vnt.), kad 13 sandėlis būtų pripildytas nuo 12 vnt. iki 25 vnt.

## <a name="example-2"></a>2 pavyzdys

13 sandėlis sukonfigūruotas taip, kaip nurodyta toliau.

- **Padengimo kodas:** min. / maks.
- **Minimalus:** 15 vnt.
- **Maksimalus:** 25 vnt.

Mažiausias padengimo dimensijų lygis yra *sandėlis*, o tolesni turimi kiekiai įrašomi *vietos* lygiu.

- **1 objektas, 13 sandėlis, 1 vieta:** 4 vnt.
- **1 objektas, 13 sandėlis, 2 vieta:** &minus;8 vnt.

Todėl bendrasis turimas 13 sandėlio kiekis yra &minus;4 vnt. (= 4 vnt. &minus; 8 vnt.). Kitaip tariant, mažiau nei 0 (nulis).

Šiuo atveju planavimo mechanizmas daro prielaidą, kad turimas 13 sandėlio kiekis yra 0 vnt., o ne &minus;4 vnt.

Rezultatas yra suplanuotas 25 vnt. užsakymas (= 25 vnt. &minus; 0 vnt.), kad 13 sandėlis būtų pripildytas nuo 0 vnt. iki 25 vnt.

## <a name="related-resources"></a>Susiję ištekliai

[Planavimo optimizavimo apžvalga](planning-optimization-overview.md)

[Darbo su planavimo optimizavimu pradžia](get-started.md)

[Planavimo optimizavimo tinkamumo analizė](planning-optimization-fit-analysis.md)

[Plano retrospektyvos ir planavimo žurnalų peržiūra](plan-history-logs.md)

[Planavimo užduoties atšaukimas](cancel-planning-job.md)
