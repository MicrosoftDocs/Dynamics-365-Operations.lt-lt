---
title: Gamybos planavimas nepaiso laiko rezervų
description: Gamybos naujas suplanavimas neapima saugos maržų, kurios yra nustatytos prekės apimtyje fiksuotam tiekimui
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 738296b7570ded0a4ee806e4445204a68e6a08c8
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477071"
---
# <a name="production-scheduling-doesnt-consider-the-safety-margins"></a>Gamybos planavimas nepaiso laiko rezervų

## <a name="symptoms"></a>Požymiai

Pagrindinis planavimas apima saugos maržas. Nepaisant to, saugos maržos ignoruojamos planuojant prekybos užsakymus, kai jie yra suplanuojami iš anksto.

## <a name="resolution"></a>Sprendimas

Į maržas atsižvelgiama tik pagrindinio planavimo metu, o ne rankiniu būdu planuojant. Maržos skirtos veikti kaip buferis planavimo etapo metu tam, kad suteiktų šiokią tokią esamo proceso „maržą“.

Norėdami gauti norimą rezultatą, galite pašalinti maržą. Maršrutas turi būti tuomet atnaujintas taip, kad apimtų norimą laiką (pavyzdžiui, laukimo laiką). Tiek pagrindinis, tiek ir rankinis planavimas turi tuomet duoti tą patį rezultatą.
