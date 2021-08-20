---
title: Negalima išrašyti sf su klientu susieti pardavimo užsakymui
description: Kai įgalinsite pasirinktį Registruoti SF automatiškai, nebegalėsite išrašyti pradinio pardavimo užsakymo ir pradinio tiesioginio pristatymo pirkimo užsakymo SF.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 30c485be79be5ebbec8b51272b8bbe6e0c7df9d81bbaaaef316dbfede03abf68
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756756"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>Negalima išrašyti sf su klientu susieti pardavimo užsakymui

KB numeris: 4611793

## <a name="symptoms"></a>Požymiai

Nebegalėsite išrašyti originalaus pardavimo užsakymo ir originalaus tiesioginio pristatymo įsigijimo užsakymo po jo įjungimo **Publikuoti sąskaitą automatiškai** parinktį **Tarpinės įmonės** puslapyje tiekėjui.

## <a name="resolution"></a>Skiriamoji geba

Vidinės įmonės ir tiesioginio pristatymo užsakymo SF sinchronizavimo elgseną kontroliuoja ir juos verčia parametrai, aprašyti parametruose, kuriuos reikia nurodyti [vidinės įmonės užsakymui registruoti](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).

Nustatę šiuos parametrus, pirmiausia turite išrašyti vidinės įmonės pardavimo užsakymo SF. Tada sinchronizuojami pradiniai pardavimo ir pirkimo užsakymai.
