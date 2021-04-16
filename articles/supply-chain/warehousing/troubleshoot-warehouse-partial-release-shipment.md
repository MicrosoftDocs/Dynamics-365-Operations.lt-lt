---
title: Trikčių šalinimo daliniai leidimai ir dalinis siuntimas
description: Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su daliniais leidimai ir daliniais siuntimais „Microsoft Dynamics 365 Supply Chain Management“.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 5534099f81a97a1dcf4908784fd71dd03cf94eaf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828159"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a>Trikčių šalinimo daliniai leidimai ir dalinis siuntimas

[!include [banner](../includes/banner.md)]

Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su daliniais leidimai ir daliniais siuntimais „Microsoft Dynamics 365 Supply Chain Management“.

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>Prekybos užsakymo paleidimo būsena išlieka dalinai paleista net ir po prekybos užsakymo įtraukimo į sąskaitą.

### <a name="issue-description"></a>Problemos aprašas

Pardavimo užsakymas yra pristatymo užsakymas, bet vienas ar keletas prekių jame turi skirtingą pristatymo būdą. Įtraukus į sąskaitą užsakymą, jis vis dar turi išleidimo būseną *Iš dalies išleistas*.

Pavyzdžiui, pardavimo užsakymas turi dvi prekes: vieną pristatymui ir kitą paėmimui. Tiek pristatymas, tiek paėmimas buvo atlikti. Dėl to, abi eilutės buvo įtrauktos į sąskaitą. Nepaisant to, išleidimo būsena vis dar rodoma kaip *Iš dalies išleistas*, o tai neteisinga.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Išleidimo būsena taikoma tik užsakymo eilutėms, kurioje prekės buvo įjungtos sandėlio valdymui. Dėl to, išleidimo būsena išlieka *Iš dalies išleista* šiame scenarijuje. „Microsoft“ įvertino šią klaidą ir nustatė jos funkcijos apribojimą. Išplėtimas gali būti įtrauktas kaip paėmimo praleidimo dalis ir sąskaitos procesas siekiant atnaujinti išleidimo būseną.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]