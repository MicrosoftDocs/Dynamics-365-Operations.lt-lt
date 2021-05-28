---
title: Negalima atnaujinti prognozuojamų vieneto išlaidų importuojant poreikio prognozės įrašus
description: Kai duomenų objektus naudojate poreikio prognozės įrašams importuoti, esamų įrašų savikaina nėra atnaujinama taip, kad atitiktų importuotus duomenis.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026749"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>Negalima atnaujinti prognozuojamų vieneto išlaidų importuojant poreikio prognozės įrašus

KB numeris: 4614109

## <a name="symptoms"></a>Požymiai

Kai duomenų objektus naudojate poreikio prognozės įrašams importuoti, **Prognozuojamo vieneto kaštų** savikaina nėra atnaujinama taip, kad atitiktų importuotus duomenis.

## <a name="cause"></a>Priežastis

**Prognozuojamos vieneto išlaidos** yra tik skaitomas laukas. Vertė priklauso nuo produkto vieneto savikainos ir jos negalima tiesiogiai nustatyti importuojant.

## <a name="resolution"></a>Skiriamoji geba

Kadangi laukas yra tik skaitomas, jo verčių importuoti negalima. Vertė bus apskaičiuota pagal esamą verslo logiką.
