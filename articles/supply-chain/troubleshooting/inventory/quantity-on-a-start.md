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
ms.openlocfilehash: 4625570cb706199dca78f23b1864ca1d81cc66e896cf10d6d5f16cf1a9d1dc16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713499"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>Pradėtas sulaikymo užsakymo kiekis nėra atnaujinamas skaidant užsakymą

KB numeris: 4613113

## <a name="symptoms"></a>Požymiai

Kai sukuriate sulaikymo užsakymą ir bandote jį skaidyti, užsakymo kiekis atnaujinamas į išskaidytą likusį kiekį po paskirstymo.

## <a name="resolution"></a>Skiriamoji geba

Sistema neatikeičia pradinio kiekio iš sulaikymo užsakymo, kad užtikrintų, jog galėsite sekti pradinį kiekį, sukurtą tam sulaikymo užsakymui. Tačiau sistema seka kiekį, kuris padalintas iš sulaikymo užsakymo. Norint atlikti šį sekimą, naudojamas duomenų bazės laukas, pavadintas `QuantityThatHasSplitIntoOtherQuarantineOrders`. Nepaisant to, šis laukelis vartotojo sąsajoje (UI) nematomas.
