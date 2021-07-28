---
title: Planavimas su neribotu pajėgumu
description: Šioje temoje pateikiama informacija apie Planavimo optimizavimo neriboto pajėgumo planavimą. Joje taip pat aprašomi dabartiniai funkcijų apribojimai.
author: crytt
ms.date: 6/9/2021
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c493522ea55dd7e69c0133aceef43a3e59021c3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361349"
---
# <a name="scheduling-with-infinite-capacity"></a>Planavimas su neribotu pajėgumu

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

*Planavimo optimizavimo neriboto pajėgumo planavimo* funkcija pristato planavimą pagal maršruto informaciją. Ji leidžia jums suplanuoti užduotis remiantis plačiu maršruto nustatymų diapazonu. Planavimo optimizavimo planavimas apima dažnai naudojamus maršruto parametrus, įskaitant maršruto operacijos seką arba maršruto operacijų išteklių reikalavimus.

## <a name="turn-on-the-infinite-capacity-scheduling-feature"></a>Neriboto pajėgumo planavimo funkcijos įjungimas

Jei jūsų sistemoje dar nėra šioje temoje aprašytos funkcijos, atidarykite [Funkcijų valdymo](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį ir įjunkite funkciją *Neriboto pajėgumo planavimas, skirtas planavimo optimizavimui*.

## <a name="added-functionality"></a>Įtrauktos funkcijos

*Planavimo optimizavimo neriboto pajėgumo planavimo* funkcija įgalina užduočių planavimą pagal maršruto informaciją. Todėl maršruto nustatymą galima naudoti gamybos procesams planuoti. Nors ši funkcija turi tam tikrų apribojimų, kurių neturi įdiegtas bendrasis planavimas, ji palaiko dažniausias funkcijas, kurių reikia gamybos scenarijams.

Funkcija atsižvelgia tiek į *paprastus maršrutus*, tiek į *maršrutų tinklus*. Naudodami lauką **Kitas** maršruto operacijoje, galite nustatyti sudėtingus maršrutus, kurie turi kelis pradžios taškus ir kelias operacijas, vykdomas lygiagrečiai. Planavimo metu sistema atsižvelgs į sudėtingas šio tipo maršruto struktūras.

Be to, priemonė palaiko *lygiagrečias operacijas* maršrutuose. Naudodami parinktis *Pirminis* ir *Antrinis* lauke **Prioritetas** maršruto operacijose, galite apibrėžti maršruto struktūrą, kurioje viena maršruto operacija yra pirminė operacija, o kita operacija – antrinė. Tokiu atveju planavimo metu sistema atsižvelgs į maršruto struktūrą.

Planavimo proceso metu sistema taip pat atsižvelgia į nurodytus operacijos *išteklių reikalavimus*. Sistema naudoja išteklių reikalavimus, kad nustatytų, kurių išteklių reikia operacijai atlikti. Šiuo metu *Planavimo optimizavimo neriboto pajėgumo planavimo* funkcija palaiko šiuos išteklių reikalavimų tipus:

- Išteklių tipas
- Ištekliai
- Išteklių grupė
- Sugebėjimas

> [!NOTE]
> Reikalavimai, susiję su žmogiškaisiais ištekliais, pavyzdžiui, įgūdžių arba sertifikatų reikalavimai, dar nepalaikomi.

Funkcija taip pat palaiko **Nustatymo laiko** ir **Vykdymo laiko** veikimo ypatybes. Kai nustatote šias ypatybes maršruto operacijoje, planavimo procesas sukurs atitinkamą nustatymą ir proceso užduotis.

Apibendrinant, Planavimo optimizavimo planavimas palaiko dažniausiai naudojamus scenarijus. Galite kurti maršrutą, įtraukti pirmines ir antrines operacijas, nurodyti kitas operacijas, įtraukti išteklių reikalavimus bei pridėti nustatymo ir vykdymo laikus. Tada planavimo metu sistema atsižvelgs į šią informaciją.

## <a name="limitations"></a>Apribojimai

Toliau nurodyti apribojimai taikomi, kai naudojate Planavimo optimizavimo planavimą:

- Funkcija palaiko tik užduočių planavimą. Planavimo metu nepaisoma parametrų, susijusių su operacijų planavimu, neatsižvelgiant į bendrųjų planų planavimo metodą.
- Funkcija palaiko tik neribotą pajėgumą.
- Funkcija nepalaiko išteklių įkėlimo funkcijos.
- Funkcija neatsižvelgia į maršruto nurašymą.
- Funkcija palaiko *Trukmę* tik kaip pirminių išteklių pasirinkimą.

Atkreipkite dėmesį, kad *Planavimo optimizavimo neriboto pajėgumo planavimo* funkcija yra nuolat tobulinama. „Microsoft” tikisi pristatyti papildomų planavimo parametrų palaikymą būsimuose leidimuose.
