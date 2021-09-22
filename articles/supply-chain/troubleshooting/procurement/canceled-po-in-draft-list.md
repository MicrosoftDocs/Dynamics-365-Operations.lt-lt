---
title: Atšaukti pirkimo užsakymai rodomi juodraštyje, esančiame pirkimo užsakymo paruošimo darbo srityje
description: Atšaukti pirkimo užsakymai rodomi juodraštyje, esančiame pirkimo užsakymo paruošimo darbo srityje
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: f1dc23cd7e5b4b99cb7a9440d7d4666d8396511f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477114"
---
# <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-workspace"></a>Atšaukti pirkimo užsakymai rodomi juodraštyje, esančiame pirkimo užsakymo paruošimo darbo srityje

## <a name="symptoms"></a>Požymiai

Atšaukus pirkimo užsakymus, kurių būsena buvo *Patvirtinta*, atšaukti pirkimo užsakymai vis dar rodomi **Pirkimo užsakymo paruošimo** darbo srities pirkimo užsakymų juodraščių sąraše.

## <a name="resolution"></a>Sprendimas

Ši problema kyla tik pirkimo užsakymams, kuriems taikomas keitimų valdymas. Tai įvyksta, nes atšaukimas laikomas pakeitimu, kuris turi būti patvirtintas. Šį patvirtinimą sistema gali atlikti automatiškai. Todėl reikalingas procesas pateikti atšauktą pirkimo užsakymą į patvirtinimo darbo eigą, kad jis galėtų patekti į *Patvirtintą* būseną. Tuo metu pirkimo užsakymas nebebus rodomas **Pirkimo užsakymo paruošimo** darbo srities pirkimo užsakymų juodraščių sąraše.
