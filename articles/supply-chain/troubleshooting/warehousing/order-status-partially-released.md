---
title: Iš dalies išleista užsakymo būsena lieka iš dalies po to, kai buvo išrašyta jo SF
description: Kai kuriais atvejais, prekybos užsakymo paleidimo būsena išlieka dalinai paleista net ir po prekybos užsakymo įtraukimo į sąskaitą. Šiame puslapyje paaiškinama, kodėl ir galimas problemos sprendimas.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8bfe7ecfd4beb6e77e8dd1e23ccd896d067bdb51
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477102"
---
# <a name="order-status-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>Prekybos užsakymo paleidimo būsena išlieka dalinai paleista net ir po prekybos užsakymo įtraukimo į sąskaitą

## <a name="symptoms"></a>Požymiai

Pardavimo užsakymas yra pristatymo užsakymas, bet vienas ar keletas prekių jame turi skirtingą pristatymo būdą. Įtraukus į sąskaitą užsakymą, jis vis dar turi išleidimo būseną *Iš dalies išleistas*.

Pavyzdžiui, pardavimo užsakymas turi dvi prekes: vieną pristatymui ir kitą paėmimui. Tiek pristatymas, tiek paėmimas buvo atlikti. Dėl to, abi eilutės buvo įtrauktos į sąskaitą. Nepaisant to, išleidimo būsena vis dar rodoma kaip *Iš dalies išleistas*, o tai neteisinga.

## <a name="workaround"></a>Apėjimo būdas

Išleidimo būsena taikoma tik užsakymo eilutėms, kurioje prekės buvo įjungtos sandėlio valdymui. Dėl to, išleidimo būsena išlieka *Iš dalies išleista* šiame scenarijuje. „Microsoft“ įvertino šią klaidą ir nustatė jos funkcijos apribojimą. Išplėtimas gali būti įtrauktas kaip paėmimo praleidimo dalis ir sąskaitos procesas siekiant atnaujinti išleidimo būseną.
