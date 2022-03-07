---
title: Vidinės įmonės nėra nepalaikomas paketo elementas
description: Sugrupuotos prekės negalima pirkti. Pardavimo užsakymas perka tik grupės prekės komponentus, o ne pačią grupavimo prekę.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 21adc7d071837b762157364f6f8ed370c69c7fd3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477094"
---
# <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>Vidinės įmonės procese nepalaikomas paketo elementas

## <a name="symptoms"></a>Požymiai

Paketo elementas negalimas pirkimo užsakyme, nes, jei patikrinsite paketo elemento pardavimo užsakymo eilutes, pastebėsite, kad kiekis yra *0* (nulis), o būsena *Atšaukta*.

## <a name="resolution"></a>Sprendimas

Toks veikimo būdas yra numatytas. Pardavimo užsakymas perka tik paketo elemento komponentus. Jis neperka pačio paketo elemento. Jei privalote įsigyti paketą, apsvarstykite, ar reikės jį pažymėti kaip paketo elementą, nes šis funkcionalumas yra skirtas pelno atpažinimo scenarijams. Daugiau informacijos apie paketo elementus žr. [Paketai](/dynamics365/finance/accounts-receivable/revenue-recognition-setup).
