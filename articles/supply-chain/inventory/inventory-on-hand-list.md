---
title: Turimų atsargų sąrašas
description: Ši tema aprašo, kaip naudoti turimo sąrašo puslapį siekiant peržiūrėti turimų atsargų informaciją. Jis rodo įvairius būdus, kuriais skirtingos filtravimo ir rūšiavimo parinktys veikia kartu ir kaip šios parinktys gali kartais sukurti netikėtus rezultatus, kartu susiderinant.
author: sherry-zheng
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 537595e23cd48dd7ba7d0f28bd4dfe39768fe9ac
ms.sourcegitcommit: 7be450990ba04a6c118dda01b40d7306b180fcb8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/30/2020
ms.locfileid: "3639008"
---
# <a name="inventory-on-hand-list"></a>Turimų atsargų sąrašas

[!include [banner](../includes/banner.md)]

Ši tema aprašo, kaip naudoti **Turimo sąrašo** puslapį siekiant peržiūrėti turimų atsargų informaciją. Jis rodo įvairius būdus, kuriais skirtingos filtravimo ir rūšiavimo parinktys veikia kartu ir kaip šios parinktys gali kartais sukurti netikėtus rezultatus, kartu susiderinant.

## <a name="query-your-on-hand-inventory"></a>Pateikite užklausą savo turimoms atsargoms

Tam, kad patikrintumėte atsargų prieinamumą, eikite į **Atsargų valdymas \> Užklausos ir ataskaitos \> Turimas sąrašas**.

**Turimas sąrašas** puslapis automatiškai atnaujinamas, kai perlaidos yra atliekamos atsargose. Šios perlaidos gali būti suplanuotos, fizinės ar finansinės.

Naudokite toliau pateiktus įrankius siekiant surasti produktus, kurių ieškote:

- Veiksmų juostoje, pasirinkite [**Dimensijos**](#dimensions) tam, kad atidarytumėte teksto laukelį, kuriame galite įtraukti ar pašalinti stulpelius rodomus **Turimame** tinklelyje.
- [**Filtrai** juostoje](#filters-pane), įveskite vertes konkretiems laukeliams siekiant parodyti tik įrašus, kurie atitinka tas vertes. Atkreipkite dėmesį, kad filtrai, kuriuos nustatėte čia taikomi šaltinio lentelėms, kurios gali būti įtraukiamos vėliau pagal pasirinktas rodyti dimensijas. Dėl informacijos apie tai, kaip šis elgesys gali paveikti jūsų rezultatus, žr. [pavyzdžiai](#examples) toliau šiame skyriuje.
- **Filtrai** juostoje, pasirinkite **Taikyti** tam, kad sukurtumėte atitinkamo turimų atasargų sąrašą **Turimų** tinklelyje.
- **Turimame** tinklelyje, pasirinkite bet kurio stulpelio antraštę rūšiavimui ar filtravimui pagal to stulpelio vertes. Greitas filtravimas tinklelio viršuje suteikia papildomą filtravimo parinktį. Šie filtrai taikomi rezultatams, tačiau ne šaltinio lentelėms. Dėl informacijos apie tai, kaip šis elgesys gali paveikti jūsų rezultatus, žr. [pavyzdžiai](#examples) toliau šiame skyriuje.

Kiekvienam sutinkančiam elementui, **Turimas** tinklelis pateikia tolesnius atsargų informacijos stulpelius.

| Stulpelis | aprašymas |
|---|---|
| Faktinės atsargos | Fizinis kiekis esantis atsargose. |
| Faktiškai rezervuota | Bendras kiekis, kuris buvo faktiškai rezervuotas. |
| Faktiškai turima | Esamas (nerezervuotas) kiekis, kuris yra prieinamas faktiniam inventoriui.<p>**Faktiškai prieinamas** yra apskaičiuojamas laukelis. Vertė yra lygi **Faktiško inventoriaus** vertei, iš kurios atimama **Faktiškai peržiūrėta** vertė.</p> |
| Faktiškai esančios pagal papildomas dimensijas | Esamas faktinis kiekis visoms dimensijoms, kurios yra rodomos tinklelyje. |
| Iš viso užsakyta | Bendras kiekis, kuris yra įtrauktas į vidaus užsakymus arba kuris yra teigiamas kiekis įvairiuose atsargų žurnaluose. |
| Užsakyta | Bendras kiekis, kuris yra įtrauktas į išorės užsakymus arba kuris yra neigiamas kiekis įvairiuose atsargų žurnaluose. |
| Užsakyta rezervuotų | Bendras kiekis, kuris buvo rezervuotas pagal užsakytus kvitus. Vertė šiame laukelyje atspindi bendrą elementų skaičių išorės perlaidose, kurios turi _Užsakytos peržiūrėtos_ būseną. Elementai, kurie yra rezervuoti kaip užsakyti nėra faktiškai prieinami atsargose. Dėl to, jie gali būti tiesiogiai paimti ir pristatyti. |
| Galima rezervuoti | Bendras turimų atsargų kiekis, kuris gali būti rezervuotas.<p>**Pastaba:** Jei **Rezervuoti užsakyti elementai** pažymimas laukelis yra pasirinktas **Inventoriaus ir sandėlio valdymo parametrai** puslapyje, vertė šiame laukelyje apima tikėtinus kvitus. Jei žymimas laukelis yra tuščias, vertė neapima tikėtinų kvitų.</p> |
| Iš viso turima | Bendras prieinamas kiekis.<p>**Bendras prieinamas** yra apskaičiuojamas laukelis. Vertė yra lygi **Faktiškai prieinamai** vertei pridedant **Bendrai užsakytai** vertei ir iš jos atėmus **Užsakyme** vertę.</p> |

## <a name="apply-filters-to-find-the-records-that-youre-looking-for"></a><a name="filters-pane"></a>Taikyti filtrus siekiant surasti įrašus, kurių ieškote

Naudokite **Filtrų** juostą tam, kad filtruotumėte turimų atsargų sąrašą taip, kad jis apimtų tik įrašus, kuriuose laukelio vertės atitinka filtravimo kriterijus. Filtro nustatymui, atlikite šiuos žingsnius.

1.  **Filtrai** juostoje, suraskite laukelį, kurį norite filtruoti.
2. Tolesniame laukelyje galutinio laukelio pavadinime, pasirinkite loginį operatorių (pavyzdžiui, *prasideda su*, *lygus* arba *didesnis nei*).
3. Įveskite ar pasirinkite vertę, kurios ieškote.

> [!IMPORTANT]
> **Turimo sąrašo** puslapis yra sureguliuotas iš išsamaus turimo inventoriaus lentelės, kuri apima visas apimas dimensijas. Nepaisant to, sąrašas šiame puslapyje santrauka. Dėl to, tai gali apimti eilutes iš šaltinio lentelės apimant vertes pagal rodomas dimensijas.
>
> Filtrai, kuriuos nustatote **Filtrų** juostoje taikomi šaltinio lentelei, tačiau apibendrintam sąrašui. Toks elgesys gali kartais sukelti netikėtų rezultatų. Dėl informacijos apie tai, kaip šis elgesys gali paveikti jūsų rezultatus, žr. [pavyzdžiai](#examples) toliau šiame skyriuje.
> 
> Nepaisant to, [tinklelyje pateikti filtrai](#grid-filters) *yra* taikomi apibendrintam sąrašui. Šie filtrai apima tiek „QuickFilter“ tinklelio viršuje, tiek filtrą kiekvieno stulpelio antraštėje.

Galite modifikuoti filtrų nustatymą, kuris yra prieinamas **Filtrų** juostoje tolesniais žingsniais.

- Siekiant pašalinti filtrą iš juostos, pasirinkite jos **Uždarymo** mygtuką (**X**).
- Filtro įtraukimui, pasirinkite **Įtraukti** **Filtrų** juostos viršuje. **Įtraukti filtro laukelius** teksto laukelyje, kuris pasirodo, yra rodomas esamų laukelių sąrašas. Jis taip pat rodo informaciją apie duomenų tipą ir lentelę kiekvienam laukeliui. Naudokite stulpelio antraštę tam, kad filtruotumėte ir rūšiuotumėte sąrašą kaip reikia ir tuomet pasirinkite žymimą laukelį kiekvienam laukeliui, kurį norite įtraukti į **Filtro** juostą. Kai baigėte, pasirinkite **Įvesti** jūsų keitimų taikymui.

## <a name="select-which-dimensions-to-show"></a><a name="dimensions"></a>Pasirinkite rodomas dimensijas

Dimensijos sako jums daugiau apie kiekvieno elemento turimą atsargumo sąrašą ir suteikti jums daugiau būdų rūšiuoti ir filtruoti sąrašą. Dimensijos, kurias pasirenkate rodymui taip pat paveikia tai, kaip eilutės apibendrintos **Turimų sąrašo** puslapyje. Toks apibendrinimas kitu atveju gali paveikti tai, kaip eilutės iš šaltinio lentelės yra derinamos su rezultatais, kuriuos matote. Dėl informacijos apie tai, kaip šis elgesys gali paveikti jūsų rezultatus, žr. [pavyzdžiai](#examples) toliau šiame skyriuje.

Tam, kad tinkintumėte rodomų inventoriaus dimensijų pasirinkimą, atlikite šiuos žingsnius.

1. Veiksmų juostoje, pasirinkite **Dimensijos**.

    **Dimensijos rodymas** teksto laukelyje, kuris pasirodo, rodomos visos dimensijos.

2. Pasirinkite žymimą laukelį kiekvienai dimensijai, kurią norite įtraukti į tinklelį.
3. Jei norite, kad jūsų pasirinkimas būtų naudojamas kaip iš anksto nustatytas, kitą kartą kai atidarote **Turimų sąrašas** puslapį, nustatykite **Nustatymų įrašymo** parinktį į **Taip**. Jei nustatote šią parinktį į **Ne**, jūsų pasirinkimas bus naudojamas esamos sesijos metu. Kitą kartą, kai atidarote puslapį, bus naudojamas esamas nustatytasis pasirinkimas.
4. Pasirinkite **Gerai** tam, kad uždarytumėte teksto laukelį ir pritaikytumėte savo pakeitimus.

## <a name="filter-on-the-output-of-the-inventory-on-hand-list"></a><a name="grid-filters"></a>Filtruokite turimų atsargų sąrašo išorėje

Galite pasirinkti bet kurio stulpelio antraštę**Turimo** tinklelio rūšiavime arba filtruoti pagal to stulpelio vertes. Greitas filtravimas tinklelio viršuje suteikia papildomą filtravimo parinktį. Šie filtrai taikomi rezultatams, tačiau ne šaltinio lentelėms. Dėl informacijos apie tai, kaip šis elgesys gali paveikti jūsų rezultatus, žr. [pavyzdžiai](#examples) toliau šiame skyriuje.

> [!NOTE]
> Negalite filtruoti ir rūšiuoti pagal visus stulpelius. Didžioji dalis stulpelių neįtraukia rūšiavimo ir filtravimo valdiklių, nes jie yra apskaičiuoti laukeliai. **Užsakyme** stulpelis yra išimtis.

## <a name="examples"></a><a name="examples"></a>Pavyzdžiai

Jūsų sistema apima išsamią (neapibendrintą) atsargų lentelę, kuri rodo toliau pateiktas turimas atsargas.

| Prekės numeris | Vieta | Sandėlis | Faktinės atsargos | Faktiškai turima |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 2 | 2 | 2 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-1"></a>1 scenarijus

**Turimas sąrašas**puslapis yra nustatytas rodyti tolesnes galutines dimensijas:

- Prekės Nr.
- Vieta
- Sandėlis

**Filtrai** juostoje, yra nustatyti tolesni filtravimo kriterijai:

- **Elemento numeris** \| **yra tiksliai** \| _IA0001_
- **Faktiškai turima** \| **yra mažiau arba lygu** \| _1_

Čia yra išorės rezultatai.

| Prekės numeris | Vieta | Sandėlis | Faktinės atsargos | Faktiškai turima |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-2"></a>2 scenarijus

**Turimas sąrašas**puslapis yra nustatytas rodyti tolesnes galutines dimensijas:

- Prekės Nr.
- Vieta

**Filtrai** juostoje, yra nustatyti tolesni filtravimo kriterijai:

- **Elemento numeris** \| **yra tiksliai** \| _IA0001_
- **Faktiškai turima** \| **yra mažiau arba lygu** \| _1_

Čia yra išorės rezultatai.

| Prekės numeris | Vieta | Faktinės atsargos | Faktiškai turima |
|---|---|---|---|
| IA0001 | 1 | 2 | 2 |

Atkreipkite dėmesį, kad nustatymai **Filtrų** juostoje taikomi išsamiai (neapibendrintai) atsargų lentelei, kuri yra rodoma šio skyriaus pradžioje. Dėl to, kriterijus **Faktiškai turima** \| **mažiau arba lygu** \| _1_ randa dvi eilutes iš tos lentelės (pirmąją ir trečiąją eilutę, kurių kiekviena rodo **Faktiškai turima** _1_ vertę). Nepaisant to, šiame scenarijuje **Turimo sąrašo** puslapis nėra nustatytas taip, kad rodytų **Sandėlio** dimensiją. Dėl to, jis apibendrina dvi originalias reilutes į vietą rezultatų eilutę, nes abi eilutės turi identiškas vetes visose rodomose dimensijose. Ši eilutė pasirodo pažeisdama filtravimo kriterijus, nes**Faktiškai turima** vertė rodoma kaip _2_. Nepaisant to, rezultatas yra teisingas, nes nustatymai**Filtrų** juostoje taikomi šaltinio lentelei, o ne apibendrintai lentelei, kuri yra rodoma **Turimo sąrašo** puslapyje.
