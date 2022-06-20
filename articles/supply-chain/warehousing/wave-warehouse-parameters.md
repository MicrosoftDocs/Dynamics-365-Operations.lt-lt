---
title: Sandėlio parametrai bangos apdorojimui
description: Šiame straipsnyje aprašoma, kaip nustatyti sandėlio parametrus bangai apdoroti. Galite naudoti bangos apdorojimą norėdami grupuoti kelių darbo užsakymų išrinkimo darbą į vieną bangą.
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
ms.openlocfilehash: 2a64cba837faf84f3e8470a9831d1641213a5cc4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909618"
---
# <a name="warehouse-parameters-for-wave-processing"></a>Sandėlio parametrai bangos apdorojimui

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip nustatyti sandėlio parametrus bangai apdoroti. Galite naudoti bangos apdorojimą norėdami grupuoti kelių darbo užsakymų išrinkimo darbą į vieną bangą.

Norėdami naudoti bangos apdorojimą, puslapyje **Sandėlio valdymo parametrai** nurodykite:

- Ar galite apdoroti bangas naudodami paketinę užduotį.
- Ar renkate informaciją žurnalo faile, kai apdorojamos bangos.

## <a name="set-up-warehouse-management-parameters-for-wave-processing"></a>Sandėlio valdymo parametrų nustatymas bangos apdorojimui

Norėdami nustatyti sandėlio parametrus bangos apdorojimui, atlikite toliau nurodytus veiksmus:

1. Eikite į **Sandėlio valdymas** \> **Sąranka** \> **Sandėlio valdymo parametrai**.

1. „FastTab” **Bangos apdorojimas** nustatykite šiuos parametrus:

    - **Bangos apdorojimo paketo grupė** – pasirinkite paketo grupę, kurią norite naudoti apdorodami bangas naudodami paketines užduotis. Paketų grupė nurodo serverį, kuriame bus vykdomos paketinės užduotys.
    - **Apdoroti bangas pakete** – pasirinkite, ar įgalinti automatinį bangų apdorojimą paketine užduotimi. Norėdami naudoti lygiagretųjį apdorojimą, tai turite nustatyti į *Taip*. Paketinę užduotį nustatote puslapyje **Apdoroti bangas**. (Taip pat žiūrėkite pastabą šio sąrašo pabaigoje.)
    - **Kurti bangos eigos žurnalą** – pasirinkite, ar sistema turėtų sugeneruoti žurnalo įrašą kiekvieną kartą prasidėjus ir pasibaigus prekės ir jos dimensijų paskirstymui. Šį žurnalą turėtumėte įgalinti tik tada, kai jis reikalingas, pavyzdžiui, atliekant pradinį bandymą arba trikčių diagnostiką. Daugiau informacijos rasite [Bangos paskirstymas](wave-allocation-method.md).
    - **Kurti bangos apdorojimo retrospektyvos žurnalą** – pasirinkite, ar automatiškai įrašyti informaciją apie bangą žurnalo faile po to, kai banga apdorojama, įskaitant lygiagretų laukiančių paskirstymų apdorojimą. Įprastai, tai turėtumėte įgalinti tik trikčių diagnostikos metu, kadangi tai prideda papildomų pridėtinių išlaidų. Norėdami peržiūrėti žurnalą, eikite į **Sandėlio valdymas \> Siunčiamos bangos \> Bangų apdorojimo retrospektyvos žurnalas**. Daugiau informacijos rasite [Bangos kūrimas ir apdorojimas](wave-processing.md).
    - **Kurti krovimo į konteinerius retrospektyvos žurnalą** – pasirinkite, ar automatiškai įrašyti informaciją apie krovimo į konteinerius bangą žurnalo faile po to, kai banga apdorojama. Norėdami peržiūrėti žurnalą, eikite į **Sandėlio valdymas \> Pakavimas ir krovimas į konteinerius \> Krovimo į konteinerius retrospektyvos žurnalas**.
    - **Laukti užrakto (ms)** – Įveskite laiką (milisekundėmis), kiek paskirstymo veiksmas lauks sistemos ištekliaus, kurį užrakino kitas paskirstymo veiksmas. Viršijus laiką, banga neapdorojama ir rodomas klaidos pranešimas.

1. „FastTab” **Išleisti į sandėlį** nustatykite šiuos parametrus:

    - **Paketinių užduočių klaida** – pasirinkite, ar generuoti klaidą, kai nepavyksta išleidimo į sandėlio paketinė užduotis. Jei ši funkcija įgalinta, nepavykusi užduotis turės būseną *Klaida*. Jei ši funkcija neįgalinta, nepavykusi užduotis turės būseną *Pasibaigė*.

> [!NOTE]
> Bangos šablone, kuris naudojamas apdorojant bangą, galite nurodyti parametrus, kurie automatizuoja bangos apdorojimą. Jei nustatote paketinės užduoties grafiką, galite derinti laiką su automatizavimo parametrais bangos šablone. Daugiau informacijos rasite [Bangos šablono kūrimas](wave-templates.md).
>
> Jei naudojate *Transportavimo valdymą* ir *Išplėstinį sandėlio valdymą*, galite nurodyti, ar sujungti krovinius, kai apdorojate bangą. Pavyzdžiui, tai naudinga, kai keli maži kroviniai gali būti siunčiami tuo pačiu metu. Norėdami konsoliduoti krovinius, kai apdorojate bangą, skirtuke **Kroviniai** pasirinkite žymės langelį **Konsoliduoti krovinius bangos apdorojimo metu**.</P>

## <a name="set-up-full-or-partial-reservation-for-production-waves"></a>Gamybos bangų visų arba dalinių rezervavimų nustatymas

Pardavimo užsakymų ir „kanban“ užsakymų atsargos turi būti rezervuotos prie išleidžiant užsakymą į sandėlį. Kitu atveju prekės arba paskirstymo eilutės negalės būti apdorojamos bangoje. Tačiau gamybos užsakymai yra šiek tiek lankstesni. Gamybos užsakymams galite nurodyti tai, kas išvardyta toliau:

- Galite leisti, kad gamybos užsakymai būtų išleidžiami į sandėlį, nors visos medžiagos negali būti rezervuotos. Jei pasirinksite šią parinktį, turėsite rankiniu būdu kartoti išleidimo į sandėlį procesą, kai taps pasiekiama papildomų medžiagų. Pavyzdžiui, tai naudinga, jei turite medžiagų, kurių reikia, kad galėtumėte pradėti gamybą, ir galite palaukti, kai taps pasiekiamos papildomos medžiagos.
- Galite reikalauti, kad visos medžiagos būtų rezervuotos prieš užsakymą išleidžiant į sandėlį.

Norėdami reikalauti viso arba dalinio rezervavimo, atlikite toliau nurodytus veiksmus:

1. Eikite į **Gamybos kontrolė** \> **Nustatymas** \> **Gamybos kontrolės parametrai**.
1. Skirtuko **Bendra** lauke **Išleisti į sandėlį** pasirinkite numatytąjį parametrą.
