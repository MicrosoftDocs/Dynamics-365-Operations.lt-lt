---
title: Kelių užsakymų operacijų metu sistema neranda suplanuoto užsakymo
description: Atliekant operacijas keliuose suplanuotuose užsakymuose, "Suplanuoto užsakymo nėra", ir bent du užsakymai priklauso tam pačiam prekės ID.
author: t-benebo
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo_ReqTransPoMarkChangeType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 0ece4a331b63b86e896c5b337a58185ed3ea1049
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920858"
---
# <a name="the-system-cant-find-a-planned-order-during-operations-on-multiple-orders"></a>Kelių užsakymų operacijų metu sistema neranda suplanuoto užsakymo

Klaidos kodas: SYS24774

## <a name="symptoms"></a>Požymiai

Jei mėginsite vykdyti operaciją keliuose suplanuotuose užsakymuose vienu metu ir bent du užsakymai priklauso tam pačiam prekės ID, gausite toliau nurodytą klaidos pranešimą. Pavyzdžiui, klaida gali įvykti, kai užsakymai yra patvirtinti arba jų užsakymo tipas pakeičiamas.

> Suplanuoto užsakymo %1 nėra.

## <a name="cause"></a>Priežastis

Kai sistema rodo užsakymo tipą arba jį pakeičia, ji turi peržiūrėti esamus suplanuotus prekės užsakymus ir įsitikinti, kad suplanuotas tiekimas atitinka poreikį ir esamą tiekimą. Sistema kaip šio proceso dalį iš naujo sukuria suplanuotus prekės užsakymus. Todėl antrasis suplanuotas užsakymas, kurį sistema tikisi apdoroti, nebeegzistuoja.

## <a name="workaround"></a>Apėjimo būdas

Prieš apdorodami užsakymus patvirtinkite juos. Tokiu būdu užsakymai nebus panaikinti, kai sistema apdoros pirmą prekės užsakymą.
