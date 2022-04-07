---
title: Negalima registruoti važtaraščio sustabdytai pardavimo užsakymo eilutei
description: Negalite registruoti sustabdytos pardavimo užsakymo eilutės važtaraščio
author: smithanataraj
ms.date: 03/07/2022
ms.topic: article
ms.search.form: WHSLoadTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2022-03-07
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 115cfe79e075eb36f73203818acdbb5e31fc0bad
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462922"
---
# <a name="cant-post-packing-slip-for-a-stopped-a-sales-order-line"></a>Negalima registruoti važtaraščio sustabdytai pardavimo užsakymo eilutei

Klaidos kodas: SYS13203

## <a name="symptoms"></a>Požymiai

Kai bandote užregistruoti krovinio važtaraštį, sistema rodo šį klaidos pranešimą:

> Negalima registruoti važtaraščio, kai sustabdoma pardavimo užsakymo eilutė patvirtinus siunčiamą siuntą; kiekis negali būti paimtas.

## <a name="cause"></a>Priežastis

Gali būti sustabdyta viena ar daugiau susijusių pardavimo užsakymo eilučių; tai reiškia, kad sistema neleis toliau apdoroti šio pardavimo užsakymo. Be to, tai reiškia, kad sistema neregistruos užsakymo važtaraščio.

Pavyzdžiui, vartotojas galėjo nuspręsti sustabdyti vieną ar daugiau užsakymo eilučių, nes klientas skambino ir atšaukė savo užsakymą. Tačiau, jei siuntimas jau buvo patvirtintas, siunta, kurioje yra pardavimo užsakymas, jau būtų faktiškai išvykusi į sandėlį, o tai reiškia, kad pardavimo užsakymo eilučių sustabdymas neturės jokios įtakos. Dėl to, kad nebėra faktiškai sustabdytos siuntos, galite ir atblokuoti eilutes, kad būtų galima registruoti važtaraštį. Tada atšaukimą reikės tvarkyti kaip grąžinimą.

## <a name="resolution"></a>Paaiškinimas

Norėdami registruoti važtaraštį įsitikinkite, kad nė viena iš atitinkamų pardavimo užsakymo eilučių nėra sustabdyta atliekant šiuos veiksmus.

1. Eiti į Visi **pardavimo užsakymai Pardavimas \> ir rinkodara \> Visi pardavimo užsakymai**.
1. Raskite ir atidarykite pardavimo užsakymą, su kuriuos turite problemų.
1. „FastTab“ **Pardavimo užsakymo eilutės** pasirinkite pardavimo užsakymo eilutę.
1. Išsamios eilutės **informacijos "** FastTab" atidarykite skirtuką **Bendra** ir įsitikinkite, kad **laukas** Sustabdyta nustatytas kaip *Ne*.
1. Tęskite darbą, kol visos atitinkamos pardavimo eilutės nebebus sustabdytos.
1. Bandykite dar kartą užregistruoti krovinio arba pardavimo užsakymo važtaraštį.
