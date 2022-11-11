---
title: Grafiko sudarymas su neribotu pajėgumu
description: Šiame straipsnyje pateikta informacija apie neribotą pajėgumo planavimą. Joje taip pat aprašomi dabartiniai funkcijų apribojimai.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 7249734e5d2644145a36276dbc818a40b5962805
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740011"
---
# <a name="scheduling-with-infinite-capacity"></a>Grafiko sudarymas su neribotu pajėgumu

[!include [banner](../../includes/banner.md)]

*Planavimo optimizavimo neriboto pajėgumo planavimo* funkcija pristato planavimą pagal maršruto informaciją. Ji leidžia jums suplanuoti užduotis remiantis plačiu maršruto nustatymų diapazonu. Planavimas apima dažnai naudojamus maršruto parametrus, įskaitant maršruto operacijos seką arba maršruto operacijos išteklių reikalavimus.

## <a name="turn-the-infinite-capacity-scheduling-feature-on-or-off"></a>Įjungti arba išjungti neriboto pajėgumo planavimo funkciją

Jei norite naudoti šią funkciją, ją turite įjungti savo sistemoje. Kaip ir tiekimo grandinės valdymo versija 10.0.29, funkcija įjungiama pagal numatytąjį nustatymą. Administratoriai gali įjungti arba išjungti šią funkciją *ieškodami funkcijų valdymo darbo srityje funkcijos planavimo optimizavimo* funkcijos neriboto [pajėgumo](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) planavimo.

Daugiau informacijos apie šią funkciją rasite [Planavimas su išteklių pasirinkimu pagal pajėgumą](capability-based-scheduling.md).

## <a name="added-functionality"></a>Įtrauktos funkcijos

*Planavimo optimizavimo neriboto pajėgumo planavimo* funkcija įgalina užduočių planavimą pagal maršruto informaciją. Todėl maršruto nustatymą galima naudoti gamybos procesams planuoti. Nors ši funkcija turi keletą apribojimų, kurių neturi pasenusio bendrojo planavimo modulis, ji palaiko dažniausią gamybos scenarijų funkciją.

Funkcija atsižvelgia tiek į *paprastus maršrutus*, tiek į *maršrutų tinklus*. Naudodami lauką **Kitas** maršruto operacijoje, galite nustatyti sudėtingus maršrutus, kurie turi kelis pradžios taškus ir kelias operacijas, vykdomas lygiagrečiai. Planavimo metu sistema atsižvelgs į sudėtingas šio tipo maršruto struktūras.

Be to, priemonė palaiko *lygiagrečias operacijas* maršrutuose. Naudodami parinktis *Pirminis* ir *Antrinis* lauke **Prioritetas** maršruto operacijose, galite apibrėžti maršruto struktūrą, kurioje viena maršruto operacija yra pirminė operacija, o kita operacija – antrinė. Tokiu atveju planavimo metu sistema atsižvelgs į maršruto struktūrą.

Planavimo proceso metu sistema taip pat atsižvelgia į nurodytus operacijos *išteklių reikalavimus*. Sistema naudoja išteklių reikalavimus, kad nustatytų, kurių išteklių reikia operacijai atlikti. Šiuo metu *Planavimo optimizavimo neriboto pajėgumo planavimo* funkcija palaiko šiuos išteklių reikalavimų tipus:

- Išteklių tipas
- Ištekliai
- Išteklių grupė
- Pajėgumas (Daugiau informacijos rasite [Planavimas su išteklių pasirinkimu pagal pajėgumą](capability-based-scheduling.md).)

> [!NOTE]
>
> - Jei išteklius ir (arba) išteklių grupė nustatyta kaip neribotas pajėgumas, bendrojo planavimo metu jie bus naudojami kaip neriboti pajėgumai.
> - Reikalavimai, susiję su žmogiškaisiais ištekliais, pavyzdžiui, įgūdžių arba sertifikatų reikalavimai, dar nepalaikomi.

Funkcija taip pat palaiko **Nustatymo laiko** ir **Vykdymo laiko** veikimo ypatybes. Kai nustatote šias ypatybes maršruto operacijoje, planavimo procesas sukurs atitinkamą nustatymą ir proceso užduotis.

Apibendrinant, planavimas palaiko dažniausiai naudojamus scenarijus. Galite kurti maršrutą, įtraukti pirmines ir antrines operacijas, nurodyti kitas operacijas, įtraukti išteklių reikalavimus bei pridėti nustatymo ir vykdymo laikus. Tada planavimo metu sistema atsižvelgs į šią informaciją.

## <a name="limitations"></a>Apribojimai

Planavimo optimizavimo funkcijai naudojant neribotą *pajėgumų planavimą taikomi šie* apribojimai:

- Funkcija palaiko tik neribotą pajėgumą.
- Funkcija nepalaiko išteklių įkėlimo funkcijos.
- Funkcija neatsižvelgia į maršruto nurašymą.
- Funkcija palaiko *Trukmę* tik kaip pirminių išteklių pasirinkimą.
