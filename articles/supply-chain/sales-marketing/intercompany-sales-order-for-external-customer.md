---
title: Vidinės įmonės pardavimo užsakymo kūrimas ir sąskaitos faktūros išrašymas išoriniam klientui
description: Šioje temoje paaiškinama, kaip sukurti vidinės įmonės pirkimo užsakymą išoriniam klientui ir išrašyti sąskaitą
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: b5f7342a997407c8701b836c2a6a6222d8512121
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8074999"
---
# <a name="create-and-invoice-an-intercompany-sales-order-for-an-external-customer"></a>Vidinės įmonės pardavimo užsakymo kūrimas ir sąskaitos faktūros išrašymas išoriniam klientui

[!include [banner](../../includes/banner.md)]

Galite naudoti vidinės įmonės prekybą, norėdami įrašyti produkto pardavimą iš vieno juridinio subjekto į kitą, esantį toje pačioje organizacijoje.

Kai kuriate pradinį pardavimo užsakymą, galite automatiškai sukurti vidinės įmonės pirkimo užsakymą vidinės įmonės tiekėjui. Bus automatiškai sukuriamas vidinės įmonės pardavimo užsakymas vidinės įmonės tiekėjo juridiniame subjekte.

Šioje iliustracijoje parodytas operacijų srautas pardavimo užsakymo kūrimo išoriniam klientui metu, tačiau prieš pristatant produktą klientui, jis turi būti užsakytas iš kito jūsų organizacijos juridinio subjekto. Šiuo atveju vidinės įmonės pirkimo užsakymas kuriamas tiekėjo sąskaitai, kuri nurodo kitą juridinį subjektą. Savo ruožtu vidinės įmonės pardavimo užsakymas sukuriamas kitame juridiniame subjekte jūsų juridinį subjektą nurodančiai kliento sąskaitai. Išrašius vidinės įmonės pirkimo užsakymo sąskaitą faktūrą, pradinio pardavimo užsakymo sąskaita faktūra užregistruojama automatiškai, jei tai yra tiesioginis pristatymas.

![Vidinės įmonės išoriniam pardavimo procesas](media/intercompanyexternalsalesprocess.png)

Jei naudojate tiesioginį pristatymą ir pasirenkate parinktį **Važtaraštis** lauke **Kiekis** puslapyje **Publikavimo SF** formoje, vidinės įmonės tiekėjo sąskaita faktūra išrašoma pagal anksčiau užregistruotą vidinės įmonės produkto gavimo kvitą.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradėdami įsitikinkite, kad laikomasi šių būtinųjų sąlygų, leidžiančių automatiškai registruoti ir spausdinti vidinės įmonės sąskaitas faktūras.

1. Eikite į **Pardavimas ir rinkodara \> Klientai \> Visi klientai**.
1. Veiksmų srities skirtuke **Bendra** pasirinkite **Vidinė įmonė**.
1. Eikite į **Įsigijimas ir šaltinio pasirinkimas \> Tiekėjai \> Visi tiekėjai**.
1. Veiksmų srities skirtuke **Bendra** pasirinkite **Vidinė įmonė**.
1. Tiekėjo arba kliento **Vidinė įmonė** puslapyje, pirkimo užsakymo strategijos srities laukų grupėje **Vidinės įmonės pirkimo užsakymas** srityje **Vidinės įmonės pirkimo užsakymas (tiesioginis pristatymas)** lauko grupėje rinkitės **Publikuoti SF automatiškai** žymimą laukelį.
1. Lauko grupėje **Originalus pardavimo užsakymas (tiesioginio pristatymo)** rinkitės **Publikuoti užsakymų politikas** laukelyje ir pašalinkite tikrinimo ženklinimą iš **Spausdinti sąskaitą automatiniu būdu** laukelyje. Pažymėkite šį žymės langelį, jei norite, kad pradinio pardavimo užsakymo sąskaita faktūra būtų spausdinama automatiškai, kai užregistruojate vidinės įmonės tiekėjo sąskaitą faktūrą.

> [!NOTE]
> Sąskaitos faktūros spausdinimo parametrai nustatomi atliekant modulio, dokumento ar operacijos sąranką **Spausdinti valdymo nustatymus** puslapį.

## <a name="create-an-original-sales-order-for-an-external-customer"></a>Pradinio pardavimo užsakymo kūrimas išoriniam klientui

Atlikite šiuos veiksmus juridiniame subjekte A. Ši procedūra atitinka iliustracijoje pateiktą 1 laukelį.

1. Eikite į **Gautinos sumos \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Kurkite originalų pardavimo užsakymą ir grįžkite į **Visi pardavimų užsakymai** sąrašo puslapį. Lauko vertės nukopijuojamos iš kliento sąskaitos į pardavimo užsakymą.
1. Veiksmų srities skirtuke **Antraštės rodinys** rinkitės **Pardavimo užsakymų kilmės**.
1. Vidinės **įmonės parametrų** „FastTab" pažymėkite žymės langelį **Automatiškai kurti vidinės įmonės užsakymus**.
1. Jei norite, kad vidinės įmonės tiekėjas prekę pristatytų tiesiogiai išoriniam klientui, pažymėkite žymės langelį **Tiesioginis pristatymas**.
1. Baigę pildyti pardavimo užsakymą, **Pardavimo užsakymas** puslapį.

Automatiškai sukuriamas vidinės įmonės pirkimo užsakymas visos prekėms, kurioms priskirtas vidinės įmonės tiekėjas, tada sukuriamas vidinės įmonės pardavimo užsakymas. Informaciniu pranešimu informuojama, kad vidinės įmonės pirkimo užsakymas ir vidinės įmonės pardavimo užsakymas sukurti. Pranešime taip pat pateikiami jų saitai. Jei prekė nerasta, rodomas raudonas perspėjimas, tai reiškia, kad užsakymo kūrimo procesas nebuvo baigtas.

> [!NOTE]
> Jei kuriate kelis užsakymus skirtinguose juridiniuose subjektuose ir viename iš jų prekių nerandama, užsakymo kūrimo procesas sustabdomas net ir tuose juridiniuose subjektuose, kurie galėtų įvykdyti savo užsakymus.

## <a name="invoice-an-intercompany-sales-order"></a>Vidinės įmonės pardavimo užsakymo sąskaitos faktūros išrašymas

Išrašius vidinės įmonės pardavimo užsakymo sąskaitą faktūrą, automatiškai išrašoma atitinkamo vidinės įmonės pirkimo užsakymo sąskaita faktūra. Tada, jei pradinis pardavimo užsakymas yra tiesioginio pristatymo užsakymas, automatiškai išrašoma pradinio pardavimo užsakymo sąskaita faktūra.

Atlikite šiuos veiksmus juridiniame subjekte B. Ši procedūra atitinka iliustracijoje pateiktą 2 laukelį.

1. Eikite į **Gautinos sumos \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Sąrašo **Visi pardavimo užsakymai** puslapyje rinkitės vidinės įmonės pardavimo užsakymą.
1. Veiksmų srityje pasirinkite **Sąskaita faktūra** ir tada vėl pasirinkite **Sąskaita faktūra**.
1. Pažymėkite žymės langelį **Publikavimas**.
1. Pasirinkite pardavimo užsakymą ir rinkitės **Gerai**.

Vidinės įmonės pardavimo užsakymo kliento SF automatiškai užregistruojama juridiniame subjekte B. Tada automatiškai sukuriama ir juridiniame subjekte A užregistruojama vidinės įmonės tiekėjo SF. Jei pradinis pardavimo užsakymas yra nustatytas kaip tiesioginis pristatymas, juridiniame subjekte A sukuriama pradinio pardavimo užsakymo kliento SF.

> [!NOTE]
> Anksčiau tarp įmonių pardavimo scenarijuose, jei tiekėjo sąskaitos faktūros darbo eiga buvo sukonfigūruota tarpįmonių pirkimo įmonėje, tarp įmonių pardavimo užsakymo nebuvo galima sėkmingai išrašyti sąskaitos faktūros. Todėl tiekėjo sąskaitų faktūrų darbo eiga turėjo būti išjungta tarpįmonių perkančiajai įmonei. 
> 
> Šis apribojimas buvo ištaisytas naudojant naujausią 10.0.25 versijos funkciją. Dabar tarp įmonių pardavimo užsakymus galima išrašyti sąskaitas faktūras, kai tiekėjo sąskaitų faktūrų darbo eiga sukonfigūruojama tarpįmonių pirkimo įmonėje.
> 
> Norėdami įjungti šią funkciją, atlikite šiuos veiksmus.
>
> 1. Pasirinkite tarpįmonių pardavimo juridinį asmenį.  
> 2. Eikite į **Gautinos sumos \> Klientai \> Visi klientai**.
> 3. Pasirinkite tarpįmonių pirkimo įmonės klientą.
> 4. Eiti į **Generolas \> Nustatyti \> Tarpkompanija**.
> 5. Ant **Pirkimo užsakymo taisyklės** skirtuką, pasirinkite **Apeiti tiekėjo sąskaitų faktūrų darbo eigą tarp įmonių tiekėjo sąskaitoms faktūroms** parametras.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
