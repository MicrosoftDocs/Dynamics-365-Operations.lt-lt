---
title: Gamybos planavimas
description: Šioje temoje aprašomas gamybos planavimas ir paaiškinama, kaip modifikuoti suplanuotus gamybos užsakymus naudojant planavimo optimizavimą.
author: ChristianRytt
manager: tfehr
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: eda22aa6f1e8d665d8ef390f24b247a76d4c2956
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992400"
---
# <a name="production-planning"></a>Gamybos planavimas

Planavimo optimizavimas palaiko kelis gamybos scenarijus. Jei pereinate iš esamo, įtaisyto bendrojo planavimo mechanizmo, svarbu žinoti apie pasikeitusį veikimo būdą.

<!-- The following video gives a short introduction to some of the current capabilities. 
KFM: Link to video for production functionality, coming soon... -->

## <a name="planned-production-orders"></a>Suplanuoti gamybos užsakymai

Kai bendrasis planavimas sukuria suplanuotus užsakymus reikalavimų įgyvendinimui, užsakymo tipas nustatomas pagal lauko **Suplanuoto užsakymo tipas** reikšmę. Jei lauke **Suplanuoto užsakymo tipas** nustatyta *Gamyba*, kuriami suplanuoti gamybos užsakymai. Į šiuos suplanuotus gamybos užsakymus įtraukta informacija apie aktyvias komplektavimo specifikacijas (KS) ir maršruto ID iš susijusios gamybos sąrankos.

## <a name="requirements-from-boms"></a>KS reikalavimai

Bendrojo planavimo metu atsižvelgiama į KS informaciją. Plano išeiga apima medžiagų tiekimą, padengiantį susijusią medžiagų paklausą gamybai.

Bendrojo planavimo metu dabartinė ir aktyvi KS naudojama nustatyti gamybai reikalingas medžiagas. Šis veiksmas atliekamas visuose KS struktūros lygiuose, susijusiuose su reikalaujamu gamybos užsakymu. Medžiagų poreikis įvykdomas naudojant turimas atsargas, esamą tiekimą pagal užsakymą ir patvirtintus suplanuotus užsakymus. Jei bet kurioje vietoje reikia papildomos medžiagos, sukuriamas suplanuotas užsakymas poreikiui patenkinti.

## <a name="scheduling-during-firming"></a>Planavimas patvirtinimo metu

Suplanuoti gamybos užsakymai apima maršruto ID, kuris būtinas gamybai planavimui. Tačiau planavimo vykdymo metu laukiama planavimo palaikymo patvirtinimo. Maršruto ID yra naudojamas gamybos užsakymams planuoti patvirtinimo metu. Todėl suplanuotų gamybos užsakymų gamybos laikas gali skirtis nuo iš jų sugeneruojamų, susijusių suplanuotų ar patvirtintų gamybos užsakymų, gamybos laiko, kaip aprašyta čia:

- **Suplanuotas gamybos užsakymas** – gamybos laikas paremtas statiniu išleisto produkto gamybos laiku.
- **Patvirtintas gamybos užsakymas** – gamybos laikas paremtas planavimu, naudojančiu maršruto informaciją ir susijusius išteklių apribojimus.

Norėdami gauti daugiau informacijos apie numatomą funkcijos prieinamumą, žiūrėkite [Planavimo optimizavimo pritaikymo analizė](planning-optimization-fit-analysis.md).

Jei jums reikalingos gamybos funkcijos, kurios dar nėra prieinamos planavimo optimizavime, galite toliau naudoti įtaisytąjį bendrojo planavimo mechanizmą. Išimtis nebūtina.

## <a name="delays"></a>Atidėjimai

Jei reikiamos medžiagos gamybos laikas yra ilgesnis nei laikotarpis nuo šiandienos datos iki medžiagų poreikio datos, suplanuotas reikiamos medžiagos užsakymas ir susijęs gamybos užsakymas bus atidėti. Suplanuotų užsakymų atidėjimas (dienomis) skaičiuojamas pagal išleisto produkto gamybos laiką. Atidėjimo informacija tada bus perduodama per visus KS struktūros lygius. Todėl jūs galite sekti atidėtų žaliavų poveikį iki pat kliento pardavimo užsakymo.

## <a name="modifying-planned-orders"></a>Suplanuotų užsakymų modifikavimas

Keisdami suplanuoto užsakymo informaciją, gausite tokį pranešimą: „Atkreipkite dėmesį, kad neautomatinių pakeitimų poveikis suplanuotiems užsakymams nebus rodomas likusioje plano srityje iki kito bendrojo planavimo vykdymo.”

Jei norite pakeisti suplanuoto užsakymo informaciją ir pamatyti poveikį susijusiems medžiagų reikalavimams, atlikite šiuos veiksmus.

1. Atnaujinkite suplanuotą užsakymą.
2. Patvirtinkite suplanuotą užsakymą.
3. Vykdykite bendrąjį planavimą.

Kai vykdote bendrąjį planavimą, neturėtumėte naudoti filtrų, jeigu įtraukti suplanuoti gamybos užsakymai. Daugiau informacijos žiūrėkite tolesniame šios temos skyriuje [Filtrai](#filters).

> [!NOTE]
> Jei suplanuoto užsakymo pristatymo data pakeičiama į vėlesnę, poreikis gali būti iškviestas naujam suplanuotam užsakymui. Taip nutinka, kai dėl naujos tiekimo datos atidedamas iškviestas poreikis, tačiau atsižvelgiant į gamybos laiko parametrus, atidėjimo galima išvengti.

## <a name="explosion-page"></a>Išskleidimo puslapis

Galite naudoti **Išskleidimo** puslapį analizuoti poreikiui, kuris reikalingas konkrečiam arba suplanuotam gamybos užsakymui, susijusiai aprėpčiai ir iškvietimo informacijai. Informacija **Išskleidimo** puslapyje atnaujinama bendrojo planavimo metu. Negalite atnaujinti informacijos tiesiogiai iš **Išskleidimo** puslapio.

## <a name="filters"></a><a name="filters"></a>Filtrai

Planavimo scenarijuose, apimančiuose gamybą, rekomenduojame vengti vykdyti filtruotą bendrąjį planavimą. Norėdami užtikrinti, kad planavimo optimizavimas turi teisingam rezultatui apskaičiuoti reikalingą informaciją, turite įtraukti visus produktus, kurie turi bet kokį ryšį su produktais visoje suplanuoto užsakymo KS struktūroje.

Nors priklausomos antrinės prekės yra automatiškai aptinkamos ir įtraukiamos į bendrojo planavimo vykdymą, kai naudojamas įtaisytasis bendrojo planavimo mechanizmas, planavimo optimizavimas neatlieka šio veiksmo.

Pavyzdžiui, jei vienas varžtas iš produkto A KS struktūros taip pat naudojamas produktui B gaminti, visi A ir B produktų KS struktūros produktai turi būti įtraukti į filtrą. Kadangi gali būti labai sudėtinga užtikrinti, kad visi produktai būtų filtro dalis, rekomenduojame vengti filtruoto bendrojo planavimo vykdymo, kai įtraukiami gamybos užsakymai.
