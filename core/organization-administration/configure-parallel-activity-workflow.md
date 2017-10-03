---
title: "Lygiagrečios darbo eigos veiklos konfigūravimas"
description: "Norėdami konfigūruoti lygiagrečią veiklą, darbo eigos rengyklėje atlikite toliau nurodytas procedūras."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4c2f98803164d5c761d2089152c077cfb9e83c43
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017

---

# <a name="configure-a-parallel-activity-in-a-workflow"></a>Lygiagrečios darbo eigos veiklos konfigūravimas

[!include[banner](../includes/banner.md)]


Norėdami konfigūruoti lygiagrečią veiklą, darbo eigos rengyklėje atlikite toliau nurodytas procedūras.

Lygiagrečią veiklą sudaro vienu metu veikiančios darbo eigos šakos.

## <a name="name-a-parallel-activity"></a>Lygiagrečios veiklos pavadinimas
Norėdami įvesti lygiagrečios veiklos pavadinimą, atlikite šiuos veiksmus.
1.  Dešiniuoju pelės mygtuku spustelėkite lygiagrečią veiklą, o tada spustelėkite **Ypatybės**, kad atidarytumėte formą **Ypatybės**.
2.  Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.
3.  Lauke **Pavadinimas** įveskite unikalų lygiagrečios veiklos pavadinimą.
4.  Spustelėkite **Uždaryti**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Lygiagrečios veiklos šakų konfigūravimas
Atlikite šiuos veiksmus, norėdami įtraukti ir konfigūruoti šios lygiagrečios veiklos šakas.
1.  Dukart spustelėkite lygiagrečią veiklą, kad būtų rodomos lygiagrečios veiklos šakos.
2.  Norėdami įtraukti šaką, nuvilkite elementą **Šaka** iš srities **Darbo eigos elementai** į įterpimo vietą drobėje. Toliau pateiktame paveikslėlyje parodyta įterpimo vieta.![Įterpimo vieta](./media/workflow_insertionpoint.gif)
    | **Pastaba.**                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | Šakų tvarka nėra svarbi, nes visos lygiagrečios veiklos šakos vykdomos tuo pačiu metu. |

3.  Norėdami konfigūruoti kiekvieną šaką, žr. puslapį [Lygiagrečios šakos konfigūravimas](configure-parallel-branch-workflow.md).






