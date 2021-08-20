---
title: Iškrovimo kainos modulis
description: Modulis „Iškrovimo kaina“ įmonėms padeda racionalizuoti gaunamas siuntų operacijas naudotojams suteikiant visišką finansinę ir logistinę importuoto transportavimo kontrolę iš gamintojo į sandėlį.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 87cce7a00d5ae8af2f9992a7dadda6a55880e4af51e26c31b54baf065c34059f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744135"
---
# <a name="landed-cost-module"></a>Iškrovimo kainos modulis

[!include [banner](../../includes/banner.md)]

Modulis **Iškrovimo kaina** įmonėms padeda racionalizuoti gaunamas siuntų operacijas naudotojams suteikiant visišką finansinę ir logistinę importuoto transportavimo kontrolę iš gamintojo į sandėlį. Importuotų prekių iškrovimo kainos gali padengti 40 procentų arba daugiau bendrųjų kiekvienos importuotos prekės nuo bendros savikainos. Todėl iškrovimo kainoms reikia pateikti tikslius vertinimus.

Įmonės gali naudoti į iškrovimo savikainą, kad galėtų atlikti šias užduotis:

- Iškrovimo kainą įvertinkite reiso sukūrimo metu.
- Paskirstykite iškrovimo kainą keliems prekių ir pirkimo užsakymams arba perkėlimo užsakymams viename reise.
- Palaikykite prekių pervežimą iš vienos fizinės vietos į kitą pripažindami iškrovimo kainą.
- Atpažinkite tranzito prekių kaupimus.

Iškrovimo kaina pateikia tikslias ir laiku atliktas pridėtinių iškrovos kainų prognozes. Tuo pat metu ji suteikia padidintą finansinį ir logistinį matomumą išplėstinei tiekimo grandinei. Ji taip pat padeda sumažinti įkainojimo ir įkainojimo klaidų administravimą.

## <a name="highlights"></a>Svarbiausi aspektai

### <a name="voyages"></a>Reisai

Iškrovimo kainoje reisas yra atskiras judėjimas iš siuntimo vietos per konkrečias paskirties vietas nurodytu laikotarpiu į nurodytą atvežimo sandėlio vietą. Pirkimo užsakymus ir užsakymo eilutes galima pridėti prie vieno arba kelių reiso konteinerių, o išlaidos teisingai priskiriamos prekės eilutėje. Užsakymus ir užsakymų eilutes taip pat galima pridėti juridiniams vieno reiso subjektams.

### <a name="item-ownership"></a>Prekės nuosavybės teisės

„Microsoft Dynamics 365 Supply Chain Management“ prekės paprastai gaunamos sandėlio paskirties vietoje, o tada joms išrašomos SF. Tačiau pagal daugumą tarptautinių prekybos sutarčių įmonė perima prekių nuosavybės teises nuo to laiko, kai jos išsiunčiamos iš išvykimo uosto, prieš jas gaunant fiziškai. Iškrovimo kaina įmonėms leidžia išrašyti SF prekėms prieš jas gaunant fiziškai. Ši sąvoka vadinama tranzito prekių užsakymu. Ji sukuria naują užsakymo tipą, kad būtų galima valdyti prekių gavimą išrašius pradinio pirkimo užsakymo SF.

### <a name="costs"></a>Išlaidos

Reisą sukūrus iškrovimo kainoje, savikaina prie jos pridedama automatiškai. Šios savikainos nustatomos iškrovimo kainoje, o joms galima pasirinkti įvairius savikainos variantus ir savikainos bazes. Kiekvieną savikainą galima nustatyti skirtingiems reiso lygiams ir juos priskirti prekės lygiui naudojant asignavimo taisykles, kurios palaiko kiekį, tūrį, svorį, sumą ir apibrėžtus tūrinius daliklius. Ši įvertinta savikaina suteikia tikslų visų reiso savikainų vertinimą.

Tada iškrovimo kaina paleidžia preliminarų įvertintos iškrovimo kainos registravimą / kaupimą, kad užtikrintų, jog kuriant reisą pateikiamas tikslus įvertintos savikainos skaičiavimas. Šioms automatinėms savikainoms išrašius SF, vertinamos savikainos atšaukiamos ir jas pakeičia faktinės savikainos pagal savikainų SF.

Faktinės išlaidos yra atšaukiamos įvertintos išlaidos, registruojamos išrašant išlaidų SF, naudojant kliringo sąskaitas, nustatytas kiekvienam išlaidų tipui (pvz., muito mokestis, transportavimas ir draudimas). Šie registravimas naudojamas atsižvelgiant į registravimo elgseną, susijusią su konkrečia preke. Jis automatiškai atnaujina atsargų registravimą neatsižvelgiant į tai, ar registravimo tipas yra pirmas įeinantis, pirmas išeinantis (FIFO), paskutinis įeinantis, pirmas išeinantis (LIFO), slankiojo svertinio vidurkio ar slankiojo vidurkio. Palaikomi visi atsargų modelių grupių registravimo tipai. Registruojant slankųjį vidurkį ir standartinę savikainą, pirkimo kainos nuokrypių sąskaitose galima registruoti skirtumus tarp įvertintų ir faktinių išlaidų.

### <a name="item-and-order-tracking"></a>Prekės ir užsakymo sekimas

Reisui judant iš pradinės siuntimo vietos į galutinį paskirties vietos sandėlį, naudotojai prireikus gali atnaujinti kiekvieną veiksmą arba kelionės *atkarpą*. Kiekvienai atkarpai identifikuojamas vykdymo laikas ir siuntimo būsena. Taip pat identifikuojamos patvirtintos perkėlimo į kitą veiklos ciklo atkarpą pristatymo datos. Kartu šios pristatymo datos nurodo numatomą prekių pristatymo į atvežimo sandėlį datą. Naudotojai gali keisti šias pristatymo datas. Tokiu atveju numatoma prekių pristatymo data atnaujinama automatiškai, remiantis gamybos laiku ir veiklos ciklo atkarpomis. Matomumą tranzito prekėms pagal reisus ir transporto priemones galima naudoti kiekvienam konteineriui atskirai prieš gaunant prekes. Kadangi datos atnaujinamos kiekvienoje pirkimo užsakymo eilutėje, įmonės turi daugiau logistikos ir sandėlio planavimo valdymo priemonių.

## <a name="landed-cost-concepts"></a>Iškrovimo kainos koncepcijos

Šioje lentelėje apibendrinamos kai kurios pagrindinės iškrovimo kainos koncepcijos.

| Koncepcija | aprašymas |
|---|---|
| Reisas | Paprastai reisas yra viena transporto priemonė. Tačiau, atsižvelgiant į jūsų praktiką ir procedūras, tai gali būti vienas tiekėjas arba vienas pirkimo užsakymas. Šios koncepcijos naudojimo apribojimų nėra. |
| Sąskaitos lapas | Registravimo lapai dažnai nustatomi pagal muitinės taisykles. Juos gali sudaryti vieno tiekėjo vienos siuntos prekės vienam objektui / įmonei. Viename registracijos lape esančios prekės gali būti viename konteineryje arba paskirstytos keliuose konteineriuose. |
| Gabenimo konteineris | Siuntimo konteinerių parduotuvės pirkimo užsakymo eilutės. Jos yra lygiu žemiau už siuntimo lygį. Paprastai jos naudojamos, jei išlaidos skirstomos pagal konteinerio prekes arba jei gaunama pagal konteinerį. |
| Gabenimo konteinerio tipas | Siuntimo konteinerių tipai gali nustatyti išlaidų tipo kainą (pvz., transportavimo). Juos taip pat pateikiama naudingos siuntimo informacijos. |
| Išlaidų tipas | Išlaidų tipai nurodo su importu susijusias išlaidas, pvz., muito mokestį, transportavimą ir draudimą. |
| Aut. išlaidos | Automatinė savikaina veikia kaip prekybos sutartys. Automatinė savikaina siejama su reiso lygiu. |
| Uostas | Uostai – tai sritys, kuriose prekės gaunamos ir iš kurių perkeliamos. |
| Transporto priemonė | Transporto priemonė – tai transporto priemonė, naudojama prekėms pervežti, pvz., laivas arba lėktuvas. |
| Tranzito prekės | Priklausomai nuo nustatymų, prekės įvežamos į tranzito sandėlį atnaujinus SF. |
| Veikla | Veiklas galima naudoti kiekvienam reikšmingam kelionės tarp dviejų uostų etapui saugoti. Jas galima naudoti datoms atnaujinti. |
| Kelionės šablonas | Veiklos ciklo šablonai – tai maršrutai, kuriais prekės pervežamos tarp dviejų uostų. |

Kad palygintumėte modulių **Iškrovimo kaina** ir  **Transportavimo valdymas** (TMS) terminologiją ir funkcijas, žr. skyrių [Iškrovimo kainos ir transportavimo valdymo palyginimas](landed-cost-vs-tms.md).
