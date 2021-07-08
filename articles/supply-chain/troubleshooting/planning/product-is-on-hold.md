---
title: Produktas yra sulaikytas operacijoms
description: Kai tvirtinate planavimo užsakymus, gaunate klaidos pranešimą, kuriame teigiama, kad prekė yra sulaikyta operacijoms.
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
ms.openlocfilehash: 6654e6437a088218db116b955631be4c7e62de5f
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301284"
---
# <a name="product-is-on-hold-for-transactions"></a>Produktas yra sulaikytas operacijoms

Klaidos kodas: SYS13295

## <a name="symptoms"></a>Požymiai

Kai tvirtinate suplanuotus užsakymus, gaunate tokį klaidos pranešimą:

> Prekė %1 sulaikoma dėl %2 esančių operacijų.

## <a name="cause"></a>Priežastis

Užblokuotų prekių apibūdinimui sistema naudoja terminus *užblokuota*, *sustabdyta* ir *sulaikyta* pakaitomis. Ši klaida reiškia, kad prekė nustatyta kaip **Sustabdyta** numatytuose užsakymo parametruose.

Jei prekė užblokuota ir ją pridedate prie pirkimo užsakymo arba pardavimo užsakymo eilutės, gaunate perspėjimo pranešimą. Kai prekė užblokuota, negalima modifikuoti su pirkimo užsakymo arba pardavimo užsakymo eilute susijusių atsargų operacijų (pavyzdžiui, registruojant važtaraštį arba sąskaitą faktūrą). Galite užblokuoti nusipirktą prekę ir tuo pačiu metu prekę parduoti. Tokiu atveju pirkimo užsakyme pasirenkamas **Sustabdyta** žymės langelis, bet prekė nėra blokuojama atsargose arba pardavimo užsakyme.

Štai keletas sąlygų, dėl kurių prekės numeris gali būti užblokuotas pardavimui:

- Prekė vis dar gaminama. Todėl nenorite jos parduoti ar rezervuoti.
- Gavote daug brokuotų prekių ir defektai turi būti ištaisyti prieš parduodant prekę.

Tokio tipo atvejais prekę galite blokuoti, kol problema bus išspręsta.

Jei prekė blokuojama, o jūs kuriate grąžinimo užsakymo eilutę, gaunate pranešimą. Jūs negalite užblokuoti prekės serijos arba partijos. Jeigu prekės dalys turi būti užblokuotos, jas galima užblokuoti perkeliant atsargas arba užblokuojant visas to laikotarpio prekės atsargas.

## <a name="resolution"></a>Sprendimas

- Atidarykite prekės **Numatytųjų užsakymo parametrų** puslapį ir išvalykite **Sustabdyta** žymės langelį.
