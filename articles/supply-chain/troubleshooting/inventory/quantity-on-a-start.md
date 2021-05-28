---
title: Pradėtas sulaikymo užsakymo kiekis nėra atnaujinamas skaidant užsakymą
description: Kai sukuriate sulaikymo užsakymą ir bandote jį skaidyti, užsakymo kiekis atnaujinamas į išskaidytą likusį kiekį.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026758"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>Pradėtas sulaikymo užsakymo kiekis nėra atnaujinamas skaidant užsakymą

KB numeris: 4613113

## <a name="symptoms"></a>Požymiai

Kai sukuriate sulaikymo užsakymą ir bandote jį skaidyti, užsakymo kiekis atnaujinamas į išskaidytą likusį kiekį po paskirstymo.

## <a name="resolution"></a>Skiriamoji geba

Sistema neatikeičia pradinio kiekio iš sulaikymo užsakymo, kad užtikrintų, jog galėsite sekti pradinį kiekį, sukurtą tam sulaikymo užsakymui. Tačiau sistema seka kiekį, kuris padalintas iš sulaikymo užsakymo. Norint atlikti šį sekimą, naudojamas duomenų bazės laukas, pavadintas `QuantityThatHasSplitIntoOtherQuarantineOrders`. Nepaisant to, šis laukelis vartotojo sąsajoje (UI) nematomas.
