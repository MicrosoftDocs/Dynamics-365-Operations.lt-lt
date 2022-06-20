---
title: Bangos šablonai
description: Šiame straipsnyje aprašoma, kaip nustatyti kriterijus, lemiaius, ar bangos apdorojamos rankiniu būdu ar automatiškai, ir darbą, sugeneruotą sandėliui, kai apdorojama banga.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e4a74b61ea32df432da118ac8af550a4ca4b0089
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851204"
---
# <a name="wave-templates"></a>Bangos šablonai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip nustatyti kriterijus, lemiaius, ar bangos apdorojamos rankiniu būdu ar automatiškai, ir darbą, sugeneruotą sandėliui, kai apdorojama banga. Kriterijus galite nurodyti nustatydami bangos šablonus ir užklausas, kurios sugretina bangą su išleistomis pardavimo užsakymų, gamybos užsakymų ir „kanban“ eilutėmis.

## <a name="settings-for-wave-templates"></a>Bangos šablonų parametrai

Kai nustatote bangos šabloną, turite nurodyti šią informaciją:

- **Vietą** ir **Sandėlį** kuriems šablonas sukurs darbą.
- Tvarką, pagal kurią šablonai bus vertinami. Seką, kuria šablonai bus suderinami su pardavimo užsakymų, gamybos užsakymų ir „kanban“ išleistomis eilutėmis. Kai eilutė išleidžiama, sistema taiko pirmąjį bangos šabloną, kurio kriterijus atitinka eilutė. Kuo bendresni kriterijai, tuo labiau tikėtina, kad eilutė atitiks juos, todėl sąrašo viršuje turėtumėte patalpinti šablonus su pačiais konkrečiausiais kriterijais. Naudokite mygtukus **Judėti aukštyn** ir **Judėti žemyn** veiksmų srityje, kad sudėliotumėte šablonus sąraše.
- Kiekvieno šablono atliekamus veiksmus. Banga **Metodai** atlieka šablono sukurtus veiksmus, pavyzdžiui, sukuria arba paskirsto darbą kiekvienam bangos šablono tipui.
- Bangos atributus (filtrus), kurie turi būti taikomi naudojamam bangos šablonui.

> [!NOTE]
> Jei reikia, kūrėjas gali sukurti papildomus metodus. Pilną metodų sąrašą galite peržiūrėti **Bangos apdorojimo metodų** puslapyje.

Kai kurie parametrai nurodo strateginius sprendimus dėl bangos apdorojimo, kaip nurodyta toliau:

- Ar šablonas yra naudojamas pardavimo ir perkėlimo užsakymų prekių siuntimui, ar naudojamas norint perkelti prekes į gamybą gamybos užsakymuose arba „kanban“.
- Ar banga apdorojama rankiniu būdu, ar automatiškai, kaip nurodyta toliau:

  - **Rankinis apdorojimas** – eilutė įtraukiama į bangą ir atsargos yra rezervuojamos, bet turite pasirinkti **Procesas** iš **Visos bangos** sąrašo puslapio, kad sukurtumėte užsakymo paėmimo darbą.
  - **Automatinis apdorojimas** – galite visiškai arba iš dalies automatizuoti bangos apdorojimą. Jei jūs visiškai automatizuojate bangos apdorojimą, sukuriama banga, kurioje yra eilutė iš pardavimo užsakymo, gamybos užsakymo arba „kanban“, kai sukuriamas pardavimo užsakymas, gamybos užsakymas arba „kanban“. Prekės atimamos iš turimų atsargų ir sukuriamas paėmimo darbas. Jei jūs iš dalies automatizuojate bangos apdorojimą, galite nurodyti reikšmes, kurios suaktyvins bangos apdorojimą. Pavyzdžiui, galite nurodyti maksimalų siuntų svorį, kuris suaktyvins bangos apdorojimą, kai bendrasis bangos eilučių svoris pasieks reikšmę.

- Ar siuntos priskiriamos atidarytoms bangoms. Pavyzdžiui, jei pažadėjote klientams, kad iki 12:00 val. vakaro. pateiktas užsakymas bus išsiųstas per 24 valandas, galite nustatyti bangos šabloną, kad užsakymo eilutės būtų automatiškai priskiriamos prie atidarytos bangos iki 12:00 val. vakaro. Tuo metu banga bus apdorojama automatiškai.

Apdorojus bangą, sukuriamas paėmimo darbas pagal darbo šabloną ir nurodytą sandėlio vietos direktyvą. Darbo šablonas nurodo, kaip sukuriamas paėmimo darbas, o vietos direktyva nurodo paėmimo ir padėjimo vietas.

## <a name="create-a-wave-template"></a>Bangos šablono kūrimas

Norėdami nustatyti bangos šabloną atlikite šiuos veiksmus:

1. Eikite į **Sandėlio valdymas** \> **Sąranka** \> **Bangos** \> **Bangų šablonai**.
1. Pasirinkite **Naujas** sukurti naują bangos šabloną.
1. Lauke **Bangos šablono tipas** pasirinkite vieną iš toliau nurodytų parinkčių:

    - *Siuntimas* – naudokite bangos šabloną pardavimo ir perkėlimo užsakymo prekių siuntimui.
    - *Gamybos užsakymai* – naudokite bangos šabloną, kad perkeltumėte gamybos užsakymams skirtas prekes.
    - *„Kanban”* – naudokite bangos šabloną, kad perkeltumėte „kanban“ užsakymams skirtas prekes.

1. Laukuose **Bangos šablono pavadinimas** ir **Bangos šablono aprašas** įveskite bangos šablono pavadinimą ir aprašymą.

    > [!NOTE]
    > Jei sandėliui sukuriamas daugiau nei vienas šablonas, lauke **Bangos šablono seka** esantis skaičius rodo šablono vietą sekoje, kurioje taikomi šablonai, kai atitinkami šablono kriterijai. Galite pasirinkti **Perkelti aukštyn** arba **Perkelti žemyn** šablonų sekos pertvarkymui.

1. Laukuose **Vieta** ir **Sandėlis** pasirinkite vietą ir sandėlį, kuriems bangos šablonas sukurs bangas ir paėmimo darbus.
1. Jei norite automatizuoti bangos apdorojimą, nustatykite nurodytus parametrus kaip reikalaujama:

    - **Automatizuotas bangos kūrimas** – Nustatykite šią parinktį į *Taip*, jei norite automatiškai sukurti bangą į sandėlį išleidus pardavimo užsakymą, gamybos užsakymą arba „kanban“.
    - **Priskirti atidarytas bangas** – nustatykite į *Taip*, jei norite automatiškai priskirti eilutes atvirai bangai, kai išleidžiamos eilutės. Eilutės priskiriamos bangoms pagal bangos šablono užklausos filtrą.
    - **Apdoroti bangą išleidžiant į sandėlį** – nustatykite į *Taip*, jei norite automatiškai apdoroti bangą ir sukurti darbą, kai eilutė išleidžiama į sandėlį.
    - **Automatiškai apdoroti bangą** – nustatykite į *Taip*, jei norite automatiškai apdoroti bangą, kai pasiekiamos laukų grupėje **Bangos vertės** nustatytos svorio, siuntų ir eilučių ribinės vertės. Šis parametras aktyvus tik, jeigu lauke **Bangos šablono tipas** yra pasirinkta *Siuntimas*.
    - **Automatizuoti bangos išleidimą** – nustatykite į *Taip*, jei norite automatiškai išleisti bangą. Paėmimo darbas sukuriamas ir prieinamas mobiliuosiuose įrenginiuose.
    - **Automatizuoti papildymo darbo išleidimą** – nustatykite į *Taip*, jei norite sukurti užklausa pagrįstą papildymo darbą ir automatiškai jį išleisti. Turite įtraukti papildymo bangos metodą į bangos šabloną ir sukurti papildymo šabloną, naudodami *Bangos poreikio* tipą. Nustatykite papildymo šabloną **Papildymo šablonų** puslapyje. Norint tai padaryti reikia įtraukti metodą papildyti į bangos šabloną.
    - **Tęsti bangos apdorojimą nepavykus darbo kūrimui** – kai nustatyta į *Taip*, sistema naudos tuščią vietą, jei negalės rezervuoti atsargų vietos direktyvos siūlomoje vietoje (pavyzdžiui, dėl to, kad atsargos nebėra prieinamos). Nustatyta į *Ne*, banga neveiks, jei sistema negalės rezervuoti atsargų.

1. Pagal poreikį nustatykite **Bangos ribinės grupės** laukų grupę:
    - **Bangos svorio ribinė vertė** – įveskite didžiausią galimą bangos svorį.
    - **Siuntų ribinė reikšmė** – įveskite didžiausią siuntų, kurias galima įtraukti į bangą, skaičių.
    - **Eilučių ribinė reikšmė** – įveskite didžiausią eilučių, kurias galima įtraukti į bangą, skaičių.

1. Laukų grupėje **Numatytosios vertės** pasirinkite bangos atributus, kurie bus naudojami kaip papildomi bangos šablono kriterijai. Bangos atributai yra naudingi norint priskirti papildomus kriterijus, pavyzdžiui, konkretų kliento pavadinimą bangos šablonui. Šiuos atributus kurkite **Bangos atributai** puslapyje. 

1. Nustatykite **Bangos pranešimo strategiją** į tokią strategiją, kurią norite naudoti generuojant pranešimus, susijusius su šį šabloną naudojančiomis bangomis. Bangos pranešimų strategijos pavyzdį rasite [Bangos vykdymo pranešimai ](wave-execution-notifications.md).

1. „FastTab“ skirtuko **Metodai** sritis **Pasirinkti metodai** išvardija pasirinkto bangos šablono metodus. Bangos metodai atlieka šablono sukurtus veiksmus, pavyzdžiui, sukuria arba paskirsto darbą. Šie veiksmai taip pat vadinami bangos veiksmais. Bangos metodai yra iš anksto apibrėžti kiekvienam bangos šablono tipui. Negalite pašalinti iš anksto nustatytų bangos metodų, bet galite pakeisti metodų tvarką ir įtraukti papildomų metodų. Pavyzdžiui, jei kuriate siuntimo bangos šabloną, galite įtraukti papildymo ir krovimo į konteinerius metodus. Krovimo į konteinerius bangą galima pridėti prie bangos metodų sekos siekiant apibrėžti krovimą į konteinerius, taikomą bangos šablone apdorotoms eilutėms. Norėdami įtraukti papildomų metodų, atlikite toliau nurodytus veiksmus:

    - Pasirinkite metodą iš **Likę metodai** srities ir tada pasirinkite **Kairiąją** rodyklę jo įtraukimui į sritį **Pasirinkti projektai**.
    - Norėdami pakeisti seką, pasirinkite metodą ir pasirinkite rodyklę **Aukštyn** arba **Žemyn**.

    > [!NOTE]
    > Kai pridedate metodą, jis automatiškai pateikiamas atitinkamoje vietoje pagal sekos veiksmus.

1. Norėdami nustatyti užklausą, kuri sugretins išleistas eilutes su atitinkama bangą, veiksmų srityje pasirinkite **Redaguoti užklausą**.
1. Norėdami patikrinti, ar bangos šablono parametrai yra tinkami, pasirinkite **Tikrinti šabloną**.
