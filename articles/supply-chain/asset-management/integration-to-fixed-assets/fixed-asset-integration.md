---
title: Turto valdymo integravimas naudojant ilgalaikį turtą
description: Šioje temoje paaiškinama, kaip integruoti turto valdymo ir ilgalaikio turto modulius, kad galėtumėte susieti ilgalaikį turtą su prižiūrimu turtu.
author: kamaybac
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: a45bf1f62cdcc8abed2ec157a223e7f3fddec7ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809859"
---
# <a name="integrate-asset-management-with-fixed-assets"></a>Turto valdymo integravimas naudojant ilgalaikį turtą

[!include [banner](../../includes/banner.md)]

Integruodami **turto valdymo** ir **ilgalaikio turto** modulius, galite susieti ilgalaikį turtą su prižiūrimu turtu. Tada ilgalaikio turto vartotojai gali sukurti prižiūrimą turtą iš naujo arba esamo ilgalaikio turto, o turto valdymo vartotojai gali susieti prižiūrimą turtą su esamu ilgalaikiu turtu. Ši funkcija taip pat palengvina ilgalaikio turto vartotojų išlaidų, užregistruotų iš susijusio prižiūrimo turto darbo užsakymų, peržiūrą.

> [!NOTE]
> Šioje temoje *prižiūrimas turtas* nurodo **turto valdymo** modulio turtą, o *ilgalaikis turtas* nurodo **ilgalaikio turto** modulio turtą.

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a>Numatytosios naujo prižiūrimo turto, sukurto iš ilgalaikio turto, vietos nustatymas (nebūtina)

Ši papildoma konfigūracija leidžia nustatyti numatytąją naujo prižiūrimo turto, sukurto iš ilgalaikio turto, funkcinę vietą. Paprastai šią konfigūraciją atliekate tik vieną kartą, jei užbaigiate ją visą.

Norėdami užbaigti konfigūraciją, atlikite šiuos veiksmus.

1. Eikite į **Turto valdymas \> Sąranka \> Turto valdymo parametrai**.
1. Skirtuko **Ilgalaikis turtas** lauke **Funkcinės vieta** pasirinkite numatytąją vietą.
1. Veiksmų srityje pasirinkite **Įrašyti**.

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a>Darbas su integruotu prižiūrimu turtu ir ilgalaikiu turtu

Šiame skyriuje pateikiama procedūrų, rodančių įvairius būdus, kaip galima dirbti su integruotomis turto valdymo ir ilgalaikio turto funkcijomis, rinkinys.

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a>Esamo prižiūrimo turto susiejimas su ilgalaikiu turtu

Norėdami susieti esamą prižiūrimą turtą su ilgalaikiu turtu, atlikite tolesnius veiksmus.

1. Eikite į **Turto valdymas \> Turtas \> Visas turtas** (arba **Aktyvus turtas**).
1. Pasirinkite turtą.
1. „FastTab“ konteinerio **Ilgalaikis turtas** lauke **Ilgalaikio turto numeris** pasirinkite esamą ilgalaikį turtą.
1. Veiksmų srityje pasirinkite **Įrašyti**.

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a>Ilgalaikio turto, susieto su pasirinktu prižiūrimu turtu, peržiūra

Norėdami peržiūrėti ilgalaikį turtą, susietą su pasirinktu prižiūrimu turtu, atlikite tolesnius veiksmus.

1. Eikite į **Turto valdymas \> Turtas \> Visas turtas** (arba **Aktyvus turtas**).
1. Pasirinkite turtą.
1. „FastTab“ konteinerio **Ilgalaikis turtas** lauke **Ilgalaikio turto numeris** pasirinkite saitą.

    Atidaromas pasirinkto turto puslapis **Ilgalaikis turtas**. (Paprastai šis puslapis randamas **Ilgalaikis turtas \> Ilgalaikis turtas \> Ilgalaikis turtas**.)

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a>Prižiūrimo turto, susieto su pasirinktu ilgalaikiu turtu, peržiūra

Norėdami peržiūrėti prižiūrimą turtą, susietą su pasirinktu ilgalaikiu turtu, atlikite tolesnius veiksmus.

1. Eikite į **Ilgalaikis turtas \> Ilgalaikis turtas \> Ilgalaikis turtas**.
1. Pasirinkite turtą.
1. Veiksmų srityje, skirtuke **Turto valdymas**, grupėje **Peržiūrėti**, pasirinkite **Prižiūrimas turtas**.

    Atidaromas turto, susieto su pasirinktu ilgalaikiu turtu, puslapis **Prižiūrimas turtas**. (Paprastai šis puslapis randamas **Turto valdymas \> Turtas \> Visas turtas**.)

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a>Priežiūros išlaidų, susijusių su ilgalaikiu turtu, peržiūra

Prižiūrimo turto valdymo darbo užsakymai gali būti registruojami, o kiekvienam iš šių darbo užsakymų paprastai taikomos išlaidos. Kai ilgalaikis turtas susiejamas su prižiūrimu turtu, galite pereiti tiesiai iš ilgalaikio turto į susijusių išlaidų peržiūrą.

Norėdami peržiūrėti priežiūros išlaidas, susietas su ilgalaikiu turtu, atlikite tolesnius veiksmus.

1. Eikite į **Ilgalaikis turtas \> Ilgalaikis turtas \> Ilgalaikis turtas**.
1. Pasirinkite turtą.
1. Veiksmų srityje, skirtuke **Turto valdymas**, grupėje **Peržiūrėti**, pasirinkite **Priežiūros išlaidos**.

    Atidaromas puslapis **Priežiūros išlaidos** ir parodomos susijusios išlaidos.

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a>Esamo ilgalaikio turto prižiūrimo turto kūrimas

Norėdami sukurti naują esamo ilgalaikio turto prižiūrimą turtą, atlikite tolesnius veiksmus.

1. Eikite į **Ilgalaikis turtas \> Ilgalaikis turtas \> Ilgalaikis turtas**.
1. Pasirinkite turtą.
1. Veiksmų srityje, skirtuke **Turto valdymas**, grupėje **Naujas**, pasirinkite **Kurti prižiūrimą turtą**. (Jei ši pasirinktis neprieinama, gali būti, kad prižiūrimas turtas jau susietas su pasirinktu ilgalaikiu turtu.)
1. Baikite turto kūrimą, kaip nurodyta [Turto kūrimas](../objects/create-an-object.md).

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a>Naujo ilgalaikio turto kūrimas ir naujo prižiūrimo turto įtraukimas į jį

Norėdami sukurti naują ilgalaikį turtą ir į jį įtraukti naują prižiūrimą turtą, atlikite tolesnius veiksmus.

1. Eikite į **Ilgalaikis turtas \> Ilgalaikis turtas \> Ilgalaikis turtas**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Baikite ilgalaikio turto kūrimą, kaip nurodyta [Ilgalaikio turto kūrimas](../../../finance/fixed-assets/tasks/create-fixed-asset.md).
1. Veiksmų srityje, skirtuke **Turto valdymas**, grupėje **Naujas**, pasirinkite **Kurti prižiūrimą turtą**.
1. Baikite turto kūrimą, kaip nurodyta [Turto kūrimas](../objects/create-an-object.md).

### <a name="remove-the-association-between-two-assets"></a>Dviejų turto vienetų susiejimo šalinimas

Kai kuriais atvejais gali reikėti atsieti prižiūrimą turtą nuo jo ilgalaikio turto. Pavyzdžiui, jei norite [sukurti naują prižiūrimą turtą](#new-maintenance-from-fixed) iš ilgalaikio turto, pirmiausia turite pašalinti visus esamus susiejimus.

Norėdami pašalinti esamą prižiūrimo turto ir ilgalaikio turto susiejimą, atlikite tolesnius veiksmus.

1. Eikite į **Turto valdymas \> Turtas \> Visas turtas** (arba **Aktyvus turtas**).
1. Raskite ir atidarykite ilgalaikį turtą.
1. „FastTab“ konteineryje **Ilgalaikis turtas** išvalykite lauko **Funkcinė vieta** reikšmę.
1. Veiksmų srityje pasirinkite **Įrašyti**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]