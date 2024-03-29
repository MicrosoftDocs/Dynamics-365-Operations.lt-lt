---
title: SF gretinimas ir įmonės vidaus pirkimo užsakymai
description: Gali būti nustatyta, kad perkantysis juridinis subjektas, kuris susijęs su vidinės įmonės prekybos operacija, naudoja mokėtinų sumų SF gretinimą. Tokiu atveju ir vidinės įmonės prekybos, ir mokėtinų sumų SF gretinimo registravimo reikalavimai turi būti įvykdyti prieš registruojant vidinės įmonės tiekėjo SF.
author: abruer
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchLineMatchingPolicy
audience: Application User
ms.reviewer: twheeloc
ms.custom: 3101
ms.assetid: 9c7c2e44-45f8-4325-b6de-a09fe790f9cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4be32a7158561bdf00a996831dca7395ce6f331
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879746"
---
# <a name="invoice-matching-and-intercompany-purchase-orders"></a>SF gretinimas ir įmonės vidaus pirkimo užsakymai

[!include [banner](../includes/banner.md)]

Gali būti nustatyta, kad perkantysis juridinis subjektas, kuris susijęs su vidinės įmonės prekybos operacija, naudoja mokėtinų sumų SF gretinimą. Kai mokėtinų **sumų parametrų puslapyje** nustatytas laukas **Registruoti SF su nesutapimų** yra nustatytas kaip **Būtinas patvirtinimas**, bus atliktas SF gretinimo tikrinimas. Tokiu atveju ir vidinės įmonės prekybos, ir mokėtinų sumų SF gretinimo registravimo reikalavimai turi būti įvykdyti prieš registruojant vidinės įmonės tiekėjo SF.

Šiame straipsnyje pateikti pavyzdžiai vidinės įmonės prekybai naudoja šį nustatymą:
-   Fabrikam Purchase yra perkantysis juridinis subjektas.
-   Fabrikam Sales yra parduodantysis juridinis subjektas.
-   Klientas 4020 yra įmonėje Fabrikam Sales.
-   Tiekėjas 3024 yra įmonėje Fabrikam Purchase.
-   Subjekte Fabrikam Purchase nurodoma 3024 tiekėjo įmonės vidaus informacija. Fabrikam Sales yra nurodytas kaip kliento įmonė, o 4020 klientas yra nurodytas kaip kliento sąskaita, atitinkanti Fabrikam Purchase juridinį subjektą.
-   Subjekte Fabrikam Sales nurodoma 4020 kliento įmonės vidaus informacija. Fabrikam Purchase yra nurodytas kaip tiekėjo įmonė, o 3024 tiekėjas yra nurodytas kaip tiekėjo sąskaita, atitinkanti Fabrikam Sales juridinį subjektą.

Pavyzdžiuose naudojama toliau pateikta mokėtinų sumų SF gretinimo sąranka įmonei Fabrikam Purchase.
-   Mokėtinų **sumų parametrų puslapyje** pasirinkta parinktis **Įgalinti SF gretinimo** tikrinimą.
-   Mokėtinų **sumų parametrų** puslapyje laukas **Registruoti SF su nesutapimų** nustatytas kaip **Reikalauti patvirtinimo**.
-   Leistino juridinio subjekto kainų nuokrypio procentas yra 2 procentai.

## <a name="example-price-matching-and-intercompany-trade"></a> Pavyzdys: kainos gretinimas ir įmonės vidaus prekyba
Vidinės įmonės tiekėjo SF ir vidinės įmonės kliento SF grynosios sumos turi būti lygios. Šiuo reikalavimu nepaisomi bet kokie taikomi SF gretinimo patvirtinimai ar leistino kainos nuokrypio procentai. Pavyzdžiui, atliekate toliau nurodytus veiksmus.
1.  Subjekte Fabrikam Purchase 4020 klientui sukurti pardavimo užsakymą SO888. Vidinės įmonės pirkimo užsakymas ICPO222 automatiškai kuriamas tiekėjui 3024 Fabrikam Purchase įmonėje ir pardavimo užsakymas ICSO888 automatiškai kuriamas Fabrikam Sales įmonėje.
2.  Subjekte Fabrikam Sales uržregistruoti, kad prekės gautos, ir registruoti važtaraštį. ICSO888 būsena pakito į – pristatyta. ICPO222 būsena pakito – gauta.
3.  Fabrikam Sales atnaujinkite ICSO888 SF. Vieneto kaina yra 0,45, ir atnaujinta 100 prekių.
4.  Subjekte Fabrikam Purchase sukurti SF ICPO222. Netyčia grynąją kainą pakeičiate iš 45,00 į 54,00. Rodoma piktograma, kuri nurodo, kad kaina leistiną kainos nuokrypį viršija 2 procentais.
5.  Informacijos apie SF **gretinimą** puslapyje pasirinkite pasirinktį, norėdami patvirtinti registravimą gretinimo nesutapimų. **Tiekėjo SF puslapyje** spustelėkite **Gerai**. Jei tiekėjo SF nebūtų vidinės įmonės tiekėjo SF, registravimas būtų sėkmingas. Tačiau, kadangi dirbate su vidinės įmonės tiekėjo SF, registravimas yra nesėkmingas. Vykdant vidinės įmonės prekybą, vidinės įmonės pardavimo užsakymo SF sumos turi būti lygios atitinkamo vidinės įmonės pirkimo užsakymo SF sumoms. Norėdami išspręsti šią problemą, turite pataisyti SF grynąją kainą, ją grąžindami į numatytąją kainą – 45,00.

## <a name="example-quantity-matching-with-intercompany-trade"></a> Pavyzdys: kiekio gretinimas su vidinės įmonės prekyba
Vidinės įmonės pirkimo ir pardavimo užsakymo kiekiai turi būti lygūs. Šiuo reikalavimu nepaisomi bet kokie taikomi SF gretinimo patvirtinimai. Šiame pavyzdyje naudojama toliau nurodyta papildoma vidinės įmonės prekybos sąranka.
-   Subjekte Fabrikam Purchase 3024 tiekėjo veiksmų strategija nustatoma automatiškai registruoti tiek pradinę kliento SF, tiek vidinės įmonės tiekėjo SF.

Šiame pavyzdyje naudojama toliau nurodyta papildoma mokėtinų sumų SF gretinimo įmonei Fabrikam Purchase sąranka.
-   Modelių grupės **, kurią naudoja** prekė B-R14, **puslapyje Prekių modelių grupės pasirinkta parinktis** Gavimo reikalavimai.
-   Turimas B-R14 prekės kiekis 0 (nulis).

Pavyzdžiui, atliekate toliau nurodytus veiksmus.
1.  Subjekte Fabrikam Purchase 4020 klientui sukurti pardavimo užsakymą SO999. Užsakyme yra viena eilutės prekė: 100 baterijų (prekė B-R14), kurių vieneto kaina yra 1,00. Vidinės įmonės pirkimo užsakymas ICPO333 automatiškai kuriamas tiekėjui 3024 Fabrikam Purchase įmonėje ir pardavimo užsakymas ICSO999 automatiškai kuriamas Fabrikam Sales įmonėje.
2.  Subjekte Fabrikam Sales atnaujinti SF ICSO999. Registravimas yra nesėkmingas, nes prekės nėra atsargose ir ji dar negauta. Todėl finansinės informacijos atnaujinti negalima.
3.  Subjekte Fabrikam Sales užregistruoti, kad prekės gautos, ir registruoti važtaraštį ICSO999. ICPO333 produkto gavimo kvitas automatiškai registruojamas subjekte Fabrikam Purchase. Subjekte Fabrikam Purchase gautas prekės B-R14 kiekis pasikeičia į 100.
4.  Subjekte Fabrikam Sales atnaujinti SF ICSO999. Registravimas sėkmingas abiejuose juridiniuose subjektuose. Subjekte Fabrikam Purchase nupirktas prekės B-R14 kiekis pasikeičia į 100. 







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
