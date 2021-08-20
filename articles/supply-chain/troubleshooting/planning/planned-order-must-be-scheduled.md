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
ms.openlocfilehash: a89f5f98895be5b934dbdc1194fa58b9af34f9cbc7f5e2092f6f47791dd52400
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777748"
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
