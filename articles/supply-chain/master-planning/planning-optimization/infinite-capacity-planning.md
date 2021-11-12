---
title: Planavimas su neribotu pajėgumu
description: Šioje temoje pateikiama informacija apie Planavimo optimizavimo neriboto pajėgumo planavimą. Joje taip pat aprašomi dabartiniai funkcijų apribojimai.
author: ChristianRytt
ms.date: 09/21/2021
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 5f3ecfa388eac42a817d751b882f365a51fc57cf
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678962"
---
# <a name="scheduling-with-infinite-capacity"></a>Planavimas su neribotu pajėgumu

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)] <!--KFM: Until 1/14/2022 -->

*Planavimo optimizavimo neriboto pajėgumo planavimo* funkcija pristato planavimą pagal maršruto informaciją. Ji leidžia jums suplanuoti užduotis remiantis plačiu maršruto nustatymų diapazonu. Planavimo optimizavimo planavimas apima dažnai naudojamus maršruto parametrus, įskaitant maršruto operacijos seką arba maršruto operacijų išteklių reikalavimus.

## <a name="turn-on-the-infinite-capacity-scheduling-feature"></a>Neriboto pajėgumo planavimo funkcijos įjungimas

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Bendrasis planavimas*
- **Funkcijos pavadinimas:** *Neribotas pajėgumo planavimas Planavimo optimizavimui*

Daugiau informacijos apie šią funkciją rasite [Planavimas su išteklių pasirinkimu pagal pajėgumą](capability-based-scheduling.md).

## <a name="added-functionality"></a>Įtrauktos funkcijos

*Planavimo optimizavimo neriboto pajėgumo planavimo* funkcija įgalina užduočių planavimą pagal maršruto informaciją. Todėl maršruto nustatymą galima naudoti gamybos procesams planuoti. Nors ši funkcija turi tam tikrų apribojimų, kurių neturi įdiegtas bendrasis planavimas, ji palaiko dažniausias funkcijas, kurių reikia gamybos scenarijams.

Funkcija atsižvelgia tiek į *paprastus maršrutus*, tiek į *maršrutų tinklus*. Naudodami lauką **Kitas** maršruto operacijoje, galite nustatyti sudėtingus maršrutus, kurie turi kelis pradžios taškus ir kelias operacijas, vykdomas lygiagrečiai. Planavimo metu sistema atsižvelgs į sudėtingas šio tipo maršruto struktūras.

Be to, priemonė palaiko *lygiagrečias operacijas* maršrutuose. Naudodami parinktis *Pirminis* ir *Antrinis* lauke **Prioritetas** maršruto operacijose, galite apibrėžti maršruto struktūrą, kurioje viena maršruto operacija yra pirminė operacija, o kita operacija – antrinė. Tokiu atveju planavimo metu sistema atsižvelgs į maršruto struktūrą.

Planavimo proceso metu sistema taip pat atsižvelgia į nurodytus operacijos *išteklių reikalavimus*. Sistema naudoja išteklių reikalavimus, kad nustatytų, kurių išteklių reikia operacijai atlikti. Šiuo metu *Planavimo optimizavimo neriboto pajėgumo planavimo* funkcija palaiko šiuos išteklių reikalavimų tipus:

- Išteklių tipas
- Ištekliai
- Išteklių grupė
- Pajėgumas (Daugiau informacijos rasite [Planavimas su išteklių pasirinkimu pagal pajėgumą](capability-based-scheduling.md).)

> [!NOTE]
> Reikalavimai, susiję su žmogiškaisiais ištekliais, pavyzdžiui, įgūdžių arba sertifikatų reikalavimai, dar nepalaikomi.

Funkcija taip pat palaiko **Nustatymo laiko** ir **Vykdymo laiko** veikimo ypatybes. Kai nustatote šias ypatybes maršruto operacijoje, planavimo procesas sukurs atitinkamą nustatymą ir proceso užduotis.

Apibendrinant, Planavimo optimizavimo planavimas palaiko dažniausiai naudojamus scenarijus. Galite kurti maršrutą, įtraukti pirmines ir antrines operacijas, nurodyti kitas operacijas, įtraukti išteklių reikalavimus bei pridėti nustatymo ir vykdymo laikus. Tada planavimo metu sistema atsižvelgs į šią informaciją.

## <a name="limitations"></a>Apribojimai

Toliau nurodyti apribojimai taikomi, kai naudojate Planavimo optimizavimo planavimą:

- Funkcija palaiko tik neribotą pajėgumą.
- Funkcija nepalaiko išteklių įkėlimo funkcijos.
- Funkcija neatsižvelgia į maršruto nurašymą.
- Funkcija palaiko *Trukmę* tik kaip pirminių išteklių pasirinkimą.

Atkreipkite dėmesį, kad *Planavimo optimizavimo neriboto pajėgumo planavimo* funkcija yra nuolat tobulinama. „Microsoft” tikisi pristatyti papildomų planavimo parametrų palaikymą būsimuose leidimuose.
