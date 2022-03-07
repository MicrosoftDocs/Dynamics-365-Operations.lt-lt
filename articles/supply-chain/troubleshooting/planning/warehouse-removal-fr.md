---
title: Negalima pašalinti sandėlio poreikio prognozės dimensijos iš prognozės eilučių
description: Negalima pašalinti sandėlio poreikio prognozės dimensijos iš prognozės eilučių.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 96af593d2e8a738258fe614f0f252620cb48c5f19eeb4425c9659ee6f9cd8c0c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741218"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a>Negalima pašalinti sandėlio poreikio prognozės dimensijos iš prognozės eilučių

KB numeris: 4614408

## <a name="symptoms"></a>Požymiai

Ši problema kyla, kai **sandėlio** dimensija nėra priskirta **poreikio prognozės** parametrų puslapio skirtuke **Prognozės dimensijos**. Nepaisant to, **Sandėlio** stulpelis yra rodomas **Poreikio prognozės** puslapyje (**Bendrojo planavimo \> prognozės \> Rankinio prognozės objekto \> Poreikio prognozės eilutėse**).

## <a name="resolution"></a>Skiriamoji geba

Nustatymai **Poreikio prognozės** skirtuke **Prognozės dimensijos parametrai** puslapyje neveikia **Poreikio prognozės** puslapio. Jie kontroliuoja bazinę prognozę, kuri yra generuojama ir rodoma pakoreguotoje poreikio prognozėje. Tačiau jie nekontroliuoja dimensijų, kurių reikia „tikrai" poreikio prognozei. Autorizdami įrašus, kurie rodomi puslapyje **Pakoreguota poreikio prognozė** galite juos konvertuoti į realius prognozės įrašus prognozės modeliui. Tada tą modelį galima naudoti bendrojo planavimo metu.

Poreikio prognozės puslapyje, **poreikio prognozės** dimensijos, rodomos poreikio prognozės eilutėse, yra atsargų dimensijų dalis. (Taip panaši į pardavimo užsakymo eilučių elgseną.) Jei jūsų sistema nėra nustatyta naudoti sandėlio kaip privalomos atsargų dimensijos, galite pritaikyti puslapį, kad **paslėptumėte** stulpelį.
