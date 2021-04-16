---
title: Lygiagrečių darbo eigos veiklų konfigūravimas
description: Norėdami konfigūruoti lygiagrečią veiklą, darbo eigos rengyklėje atlikite toliau nurodytas procedūras.
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1a47857cbe65c00ad678b2b0372c642abf01b41
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747836"
---
# <a name="configure-parallel-activities-in-a-workflow"></a>Lygiagrečių darbo eigos veiklų konfigūravimas

[!include [banner](../includes/banner.md)]

Norėdami konfigūruoti lygiagrečią veiklą, darbo eigos rengyklėje atlikite toliau nurodytas procedūras.

Lygiagrečią veiklą sudaro vienu metu veikiančios darbo eigos šakos.

## <a name="name-a-parallel-activity"></a>Lygiagrečios veiklos pavadinimas

Norėdami įvesti lygiagrečios veiklos pavadinimą, atlikite šiuos veiksmus.

1. Dešiniuoju pelės mygtuku spustelėkite lygiagrečią veiklą, o tada spustelėkite **Ypatybės**, kad atidarytumėte formą **Ypatybės**.
2. Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.
3. Lauke **Pavadinimas** įveskite unikalų lygiagrečios veiklos pavadinimą.
4. Spustelėkite **Uždaryti**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Lygiagrečios veiklos šakų konfigūravimas

Atlikite šiuos veiksmus, norėdami įtraukti ir konfigūruoti šios lygiagrečios veiklos šakas.

1. Dukart spustelėkite lygiagrečią veiklą, kad būtų rodomos lygiagrečios veiklos šakos.
2. Norėdami įtraukti šaką, nuvilkite elementą **Šaka** iš srities **Darbo eigos elementai** į įterpimo vietą drobėje. Toliau pateiktame paveikslėlyje parodyta įterpimo vieta.

    ![Įterpimo vieta](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > Šakų tvarka nėra svarbi, nes visos lygiagrečios veiklos šakos vykdomos tuo pačiu metu.

3. Norėdami sukonfigūruoti kiekvieną šaką, žr. puslapį [Lygiagrečių šakų konfigūravimas darbo eigoje](configure-parallel-branch-workflow.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]