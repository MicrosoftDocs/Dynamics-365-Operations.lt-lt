---
title: Automatinio rezervavimo raginimas rodomas su turimose atsargose
description: Kai naudojate tą pačią prekę sandėlyje, kuriame nėra įgalinti sandėlio procesai, automatinio rezervavimo raginimas yra rodomas. Nurodykite visas dimensijas virš vietos.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a15502ce8c5bc61d37cedd746985176408a2f362
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477129"
---
# <a name="auto-reservation-prompt-for-batch-number-is-shown-even-with-available-inventory"></a>Automatinio rezervavimo greitas paketos numeris yra rodomas net su turimose atsargose

## <a name="symptoms"></a>Požymiai

Kai naudojate prekę, turinčią *paketas aukščiau* rezervavimo hierarchiją sandėlyje, kuriame neįgalinti sandėlio procesai ir įgalintas automatinis rezervavimas, yra rodomas automatinio rezervavimo raginimas įvesti paketo numerį, net jeigu tik vienas paketas yra galimas paėmimui.

Tačiau, kai naudojate tą pačią prekę sandėlyje, kuriame įgalinti sandėlio procesai, automatinio rezervavimo raginimas nėra rodomas.

## <a name="resolution"></a>Sprendimas

Jei rezervavimo hierarchija apibrėžta kaip *paketas aukščiau* ar *serija aukščiau*, nurodyta dimensija (**Paketo numeris** arba **Serijos numeris**) visada turi būti nurodyta poreikio užsakymuose. Sandėlio procesai gali sugebėti užpildyti informaciją, jei yra vienas paketas ar serijos numeris. Tačiau, kadangi sandėlis nėra įgalintas sandėlio procesams, vartotojas visada turi nurodyti visas dimensijas, esančias virš **Vietos**.
