---
title: Prieš patvirtinant suplanuotą gamybos užsakymą, reikia sudaryti jo grafiką
description: Kai bandote patvirtinti suplanuotą užsakymą, gaunate klaidos pranešimą, kuriame teigiama, kad prieš patvirtinant užsakymą, turi būti sudarytas jo grafikas.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294141"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a>Prieš patvirtinant suplanuotą gamybos užsakymą, reikia sudaryti jo grafiką

Klaidos kodas: SYS309802

## <a name="symptoms"></a>Požymiai

Kai bandote patvirtinti suplanuotą užsakymą, gaunate tokį klaidos pranešimą:

> Prieš patvirtinant suplanuotą gamybos užsakymą, reikia sudaryti jo grafiką.

## <a name="cause"></a>Priežastis

Suplanuotos pradžios ir pabaigos datos negali būti tuščios.

## <a name="resolution"></a>Sprendimas

Norėdami nurodyti suplanuoto užsakymo pradžios ir pabaigos datas, atlikite šiuos veiksmus.

1. Eikite į **Pagrindinis planavimas \> Pagrindinis planavimas \> Suplanuoti užsakymai**.
1. Atidarykite reikalingą suplanuotą užsakymą.
1. „FastTab” skirtuko **Bendra** skyriuje **Suplanuota** nurodykite datas **Pradžios data** ir **Pabaigos data** laukuose.
