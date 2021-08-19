---
title: Atšaukus ataskaitą kaip baigtą sukuriama netikėta atvira operacija
description: Skelbimo baigtu su žymėjimu atšaukimas sukuria atvirą operaciją, kurioje atšauktas kiekis turi tas pačias atsargų dimensijas kaip ir atšaukta operacija.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 73ebc45ee83516f573c3f73ef8106da9ae44c590c05d8dbd08520bc5ef19e49a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714215"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>Atšaukus ataskaitą kaip baigtą sukuriama netikėta atvira operacija

KB numeris: 4612469

## <a name="symptoms"></a>Požymiai

Jei pakeičiate ataskaitą kaip baigtą su žymėjimu, sistema sukuria atvirą operaciją, kai pakeistas kiekis turi tas pačias atsargų dimensijas, kaip operacija, kuri buvo pakeista.

## <a name="resolution"></a>Skiriamoji geba

Kai atšaukiate skelbimo baigtu operaciją, atsargų dimensija inicijuojama iš gamybos žurnalo. Todėl jis gauna paketo numerį. Dėl žymėjimo pardavimo užsakymo operacijos paveldės paketo numerį.

Dimensiją galima nustatyti iš naujo registruojant ataskaitą kaip baigtą.
