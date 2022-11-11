---
title: Tvarkaraščio sudarymas su išteklių pasirinkimu pagal pajėgumą
description: Šiame straipsnyje aprašomas išteklių pasirinkimas neriboto pajėgumo planavimo metu, kai nurodote pajėgumus kaip operacijos išteklių reikalavimus.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: RouteInventProd, WrkCtrTable, WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 176f40ad8cd1aa1831bbe50c0ebd91ec0cc3bc89
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739904"
---
# <a name="scheduling-with-resource-selection-based-on-capability"></a>Planavimas su išteklių pasirinkimu, pagrįstu pajėgumais

[!include [banner](../../includes/banner.md)]

Nurodydami gamybos maršruto operacijos išteklių reikalavimus, jūs apibrėžiate, ko reikia tai operacijai atlikti. Pavyzdžiui, operacijai gali reikėti konkretaus ištekliaus, išteklių grupės arba įgūdžių ar galimybių derinio. Šiame straipsnyje aprašomas išteklių pasirinkimas neriboto pajėgumo planavimo metu, kai nurodote pajėgumus kaip operacijos išteklių reikalavimus.

## <a name="turn-the-capability-based-scheduling-feature-on-or-off"></a>Įjungti arba išjungti pajėgumų planavimo priemonę

Jei norite naudoti šią funkciją, ją turite įjungti savo sistemoje. Kaip ir tiekimo grandinės valdymo versija 10.0.29, funkcija įjungiama pagal numatytąjį nustatymą. Administratoriai gali įjungti arba išjungti šią funkciją *ieškodami funkcijų valdymo darbo srityje funkcijos planavimo optimizavimo* funkcijos neriboto [pajėgumo](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) planavimo.

Daugiau informacijos apie šią funkciją rasite [Planavimas naudojant neribotą pajėgumą](infinite-capacity-planning.md).

## <a name="capability-based-scheduling"></a>Pajėgumo pagrįstas planavimas

Pajėgumas yra operacijos ištekliaus gebėjimas atlikti konkrečią veiklą. Daugiau nei vienas pajėgumas gali būti priskirtas vienam operacijos ištekliui, o vieną pajėgumą galima priskirti daugiau nei vienam ištekliui. Pajėgumus galima priskirti visų tipų ištekliams, pavyzdžiui, įrankiams, tiekėjoms, mašinoms, vietoms, patalpoms ir žmogiškiesiems ištekliams.

Nurodę pajėgumus kaip išteklių reikalavimus galite atidėti išteklių paskirstymą, kol bus suplanuoti užsakymai. Užuot prie maršruto operacijos priskyrę tam tikrus išteklius arba išteklių grupes, galite nustatyti pajėgumus, reikalingus kiekvienai maršruto operacijai. Tada planavimo metu sistema suderina reikiamus pajėgumus su ištekliams apibrėžtais pajėgumais. Sistema pasirenka tik tuos išteklius, kurie atitinka reikalavimus.

Norėdami priskirti pajėgumus operacijos ištekliui, naudokite **Pajėgumų** „FastTab”, esančiame **Išteklių** puslapyje. Norėdami priskirti išteklius pajėgumui, naudokite **Išteklių** „FastTab”, esančiame **Išteklių pajėgumų** puslapyje. Abu puslapius galima pasiekti po **Gamybos kontrolė \> Nustatymas \> Ištekliai** naršymo puslapyje. Abiejuose „FastTab” yra tinklelis, kuriame išvardinti ištekliai, susieti su pasirinktu ištekliumi arba pajėgumu. Abiejuose „FastTabs” taip pat yra įrankių juosta, kurią galite naudoti eilutėms tinklelyje pridėti, pašalinti ir redaguoti. Tinklelyje yra šie stulpeliai:

- **Ištekliai** arba **Pajėgumas** – pasirinkite išteklius arba pajėgumą, kuriam priskirta eilutė.
- **Aprašas** – įveskite trumpą išteklių arba pajėgumų aprašą.
- **Įsigaliojimas** – nurodykite pirmą datą, kai taikomas išteklių arba pajėgumų priskyrimas. Planavimo metu sistema nenaudos išteklių ar pajėgumų, kurių pajėgumo priskyrimas nebegalioja, net jei kitais atžvilgiais šie ištekliai atitinka reikalavimus.
- **Galiojimas** – nurodykite paskutinę datą, kai taikomas išteklių arba pajėgumų priskyrimas. Planavimo metu sistema nenaudos išteklių ar pajėgumų, kurių pajėgumo priskyrimas nebegalioja, net jei kitais atžvilgiais šie ištekliai atitinka reikalavimus.
- **Lygis** – nurodykite pajėgumo kompetencijos lygį, kurį turi turėti ištekliai. Tada, jei nurodote **Reikalingo minimalaus lygio** reikšmę ištekliaus arba pajėgumo reikalavimui, planavimo variklis atsižvelgia į kompetencijos lygį ištekliaus pasirinkimo metu. Tada sistema parenka tik išteklius su reikiamais pajėgumais, kurių lygis atitinka arba viršija šaltinio reikalavime nurodytą minimalų lygį.
- **Prioritetas** – šio lauko dar nepalaiko planavimo optimizavimas. Tačiau jei naudojate pasenusią bendrojo planavimo sistemą, **ištekliaus** arba pajėgumo priskyrimo lauke Prioritetas galite nurodyti išteklių prioritetą. Tada, jeigu puslapio **Planavimo parametrai** lauke **Pirminių išteklių pasirinkimas** pasirinkta parinktis *Prioritetas*, planavimo metu sistema pirmiausia parenka aukščiausio prioriteto (tai yra, turintį mažiausią lauko **Prioritetas** skaitinę reikšmę) išteklių.

## <a name="example"></a>Pavyzdys

Šiame pavyzdyje parodyta, kaip planavimo variklis pasirenka išteklius pagal pajėgumą.

Gamybos maršrutas turi penkias operacijas: *„10”*, *„20”*, *„30”*, *„40”* ir *„50”*. Kiekvienai maršruto operacijai reikia ištekliaus, turinčio skirtingus pajėgumus. Pavyzdžiui, maršruto operacijai *„10”* reikia ištekliaus, kuris galėtų surinkti ausines (*0050 Ausinių rinkinys*) ir atlikti medžio darbus (*1010 Medžio darbų pajėgumai*). Maršruto operacijai *„50”* reikia išteklių, kurie gali supakuoti produktą (*0070 Pakavimo pajėgumas*).

![Planavimui panaudotas pajėgumas.](media/capability-based-scheduling.png "Planavimui panaudotas pajėgumas.")

Planavimo metu sistema ieško išteklių, atitinkančių operacijos reikalavimus. Pavyzdžiui, planavimo variklis pasirenka *„00101”* išteklių, kad jis atliktų operaciją *„10”*, nes šie ištekliai yra pirmasis rastas išteklius, turintis abu reikiamus pajėgumus. Planavimo variklis pasirenka *„00301”* išteklių, kad jis atliktų operaciją *„50”*, nes šie ištekliai yra vienintelis išteklius, turintis pakavimo pajėgumą.

Tada apsvarstykite, kaip šis pavyzdys yra paveikiamas, kai naudojami kompetencijos lygiai:

- Operacijai *„10”* reikalingas minimalus pajėgumo *0059 Rinkinys* kompetencijos lygis *„7”*.
- Ištekliaus *„00101”* pajėgumo *0059 rinkinys* kompetencijos lygis yra *„5”*.
- Ištekliaus *„00102”* pajėgumo *0059 rinkinys* kompetencijos lygis yra *„10”*.

Šiuo atveju, neriboto pajėgumo planavimo metu planavimo variklis pasirenka *„00102”* išteklių, kad atliktų operaciją *„10”*, nes šis išteklius, priešingai nei *„00101”* išteklius, turi reikiamą to pajėgumo kompetencijos lygį.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
