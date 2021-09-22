---
title: Negaliu atšaukti paėmimo kvito po to, kai jis publikuotas prekybos užsakyme
description: Paimant ir siunčiant procesus įjungtus WMS, negalite atšaukti pakavimo kvitą po to, kai jis publikuotas iš pardavimo užsakyme. Šiame puslapyje siūlomas problemos sprendimas.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d20e66e2721560b8409eb63c3546a79adc188c7c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477145"
---
# <a name="cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Negaliu atšaukti paėmimo kvito po to, kai jis publikuotas prekybos užsakyme

## <a name="symptoms"></a>Požymiai

Paimant ir siunčiant procesus įjungtus WMS, negalite atšaukti pagerinto sandėlio valdymo (WMS) po to, kai jis publikuotas iš pardavimo užsakyme.

## <a name="resolution"></a>Sprendimas

Siekiant tinkamai publikuoti pakavimo kvitus prekėms, kurios bus įjungtos WMS, publikavimas turi vykti iš krovinio, o ne iš užsakymo. „Microsoft“ įvertino šią klaidą ir nustatė jos funkcijos apribojimą.  

Bendrrai, prekybos užsakymas, kuris buvo paimtas ir siųstas per sandėlio valdymo procesus gali būti supakuotas naujinant kvitą iš krovinio ar siuntimo ir prekybos užsakymo dokumente. Nepaisant to, jei pakuojate kvito naujinimą prekybos užsakyme iš pardavimo užsakymo dokumento, pakavimo dokumento grąžinimas negali būti atliekamas iš krovinio ar prekybos užsakymo. Dėl to, rekomenduojame jums naudoti pakavimo kvito publikavimą iš krovinio. Tokiu atveju, grąžinimas turi būti atliekamas, kai įjungtas krovinys.
