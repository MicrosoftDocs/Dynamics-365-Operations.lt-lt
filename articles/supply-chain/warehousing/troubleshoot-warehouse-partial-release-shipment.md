---
title: Trikčių šalinimo daliniai leidimai ir dalinis siuntimas
description: Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su daliniais leidimai ir daliniais siuntimais „Microsoft Dynamics 365 Supply Chain Management“.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e89a430f90374733b23fadaf53f5bab598d67d62
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645953"
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