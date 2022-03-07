---
title: Vidinės įmonės pirkimo užsakymo kūrimas ir SF išrašymas vidiniais įmonės tikslais
description: Šioje temoje paaiškinama, kaip sukurti vidinės įmonės pirkimo užsakymą vidiniam naudojimui ir išrašyti sąskaitą
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 88a14ff962c5cf0cd1cff24b16cc7a62e9e1c8ce
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548423"
---
# <a name="create-and-invoice-an-intercompany-purchase-order-for-internal-use"></a>Vidinės įmonės pirkimo užsakymo kūrimas ir SF išrašymas vidiniais įmonės tikslais

[!include [banner](../../includes/banner.md)]

Galite sukurti vidinės įmonės pirkimo užsakymą, skirtą vidinės įmonės tiekėjui. Bus automatiškai sukuriamas vidinės įmonės pardavimo užsakymas vidinės įmonės tiekėjo sistemoje.

![Vidinės įmonės vidinis pirkimo procesas](media/intercompanypurchaseprocess.png)

## <a name="create-an-intercompany-purchase-order-and-a-corresponding-intercompany-sales-order"></a>Kaip sukurti vidinės įmonės pirkimo užsakymą ir atitinkamą vidinės įmonės pardavimo užsakymą

Atlikite šiuos veiksmus naudodami AAA juridinį subjektą, kaip parodyta pavyzdyje.

1. Rinkitės **Mokėtinos sumos** \> **Pirkimo užsakymai** \> **Visi pirkimo užsakymai**.
1. Sąrašo **Visi pardavimo užsakymai** puslapyje sukurkite pirkimo užsakymą, skirtą vidinės įmonės tiekėjui. Lauko reikšmės nukopijuojamos iš tiekėjo sąskaitos į pirkimo užsakymą.

    Kadangi dirbate su vidinės įmonės tiekėju, juridiniame subjekte, kuris atitinka tiekėją, sukuriamas vidinės įmonės pardavimo užsakymas. Vidinės įmonės pardavimo užsakymo numeris gali būti toks pats kaip vidinės įmonės pirkimo užsakymo numeris, be to, jame gali būti nurodytas juridinio subjekto ID. Naudojama numeravimo struktūra priklauso nuo lauko **Pardavimo užsakymo numeravimas** lauke **Vidinė įmonė** puslapyje. Pavyzdžiui, jei sukuriate pirkimo užsakymą 00029\_064 juridiniame subjekte AAA, juridiniame subjekte BBB pardavimo užsakymo numeris yra AAA00029\_64.

    Informaciniu pranešimu informuojama, kad vidinės įmonės pirkimo užsakymas ir vidinės įmonės pardavimo užsakymas sukurti. Pranešime nurodomas vidinės įmonės pardavimo užsakymo numeris informaciniais tikslais.

1. Įtraukite eilučių prekes į pirkimo užsakymą. Atitinkamos eilutės prekės automatiškai pridedamos prie vidinės įmonės pardavimo užsakymo. Jei prekės nėra kitame juridiniame subjekte, rodomas pranešimas ir prekės negalima įtraukti į pirkimo užsakymą. Norėdami išspręsti šią problemą, pereikite prie kito juridinio subjekto ir išleisti produktą tam juridiniam subjektui. Prekę bus galima įtraukti į pardavimo užsakymus tame juridiniame subjekte. Tada grįžkite prie pirkimo užsakymo juridinio subjekto ir toliau pridėkite eilutės prekes.
1. Įvedę pirkimo užsakymo informaciją, patvirtinkite ją.

## <a name="process-the-intercompany-packing-slip-and-customer-invoice"></a>Kaip apdoroti vidinės įmonės važtaraštį ir kliento SF

Atlikite šiuos veiksmus naudodami BBB juridinį subjektą, kaip parodyta pavyzdyje.

1. Eikite į **Gautinos sumos \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Sąrašo **Visi pardavimo užsakymai** puslapyje rinkitės vidinės įmonės pardavimo užsakymą.
1. Veiksmų srityje pasirinkite skirtuką **Paėmimas ir pakavimas**, tada pasirinkite **Važtaraštis**.
1. Pažymėkite žymės langelį **Publikavimas**.
1. Pasirinkite **Gerai**. Važtaraštis užregistruojamas juridiniame subjekte BBB.
1. Sąrašo **Visi pardavimo užsakymai** puslapyje rinkitės vidinės įmonės pardavimo užsakymą.
1. Veiksmų srityje pasirinkite **Sąskaita faktūra** ir tada vėl pasirinkite **Sąskaita faktūra**.
1. Pažymėkite žymės langelį **Publikavimas**.
1. Pasirinkite **Gerai**.

    Vidinės įmonės pardavimo užsakymui skirta kliento SF užregistruojama juridiniame subjekte BBB.

## <a name="process-the-intercompany-product-receipt-and-vendor-invoice"></a>Kaip apdoroti vidinės įmonės produkto gavimo kvitą ir tiekėjo SF

Atlikite šiuos veiksmus naudodami AAA juridinį subjektą, kaip parodyta pavyzdyje.

1. Eikite į **Mokėtinos sumos \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.
1. Sąrašo **Visi pardavimo užsakymai** puslapyje rinkitės vidinės įmonės pirkimo užsakymą.
1. Veiksmų srityje rinkitės **Gauti** ir tada rinkitės **Produkto gavimas**. Sukuriamas produkto gavimo kvitas. Produkto gavimo kvito numeris yra toks pats kaip vidinės įmonės važtaraščio numeris.
1. Pažymėkite žymės langelį **Publikavimas**.
1. Pasirinkite **Gerai**.
1. Sąrašo **Visi pardavimo užsakymai** puslapyje rinkitės vidinės įmonės pirkimo užsakymą.
1. Veiksmų srityje pasirinkite **Sąskaita faktūra** ir tada vėl pasirinkite **Sąskaita faktūra**. Sukuriama tiekėjo SF. Tiekėjo SF numeris yra toks pats kaip vidinės įmonės kliento SF numeris.
1. Baikite įvesti tiekėjo SF, tada užregistruokite ją.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
