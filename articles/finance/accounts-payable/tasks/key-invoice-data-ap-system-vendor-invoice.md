---
title: Pagrindiniai SF duomenys veiksmų srityje, naudojant tiekėjo SF
description: Šis užduočių vadovas jums padės iš pirkimo užsakymo sukurti tiekėjo SF ir peržiūrėti pirkimo užsakymo, gavimo kvito ir SF gretinimo (trišalis gretinimas) rezultatus.
author: abruer
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ad75439bf3dfa1ed33e35fa9cfee153012e9f60
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716809"
---
# <a name="key-invoice-data-in-ap-using-a-vendor-invoice"></a>Pagrindiniai SF duomenys veiksmų srityje, naudojant tiekėjo SF

[!include [banner](../../includes/banner.md)]

Šis užduočių vadovas jums padės iš pirkimo užsakymo sukurti tiekėjo SF ir peržiūrėti pirkimo užsakymo, gavimo kvito ir SF gretinimo (trišalis gretinimas) rezultatus.


## <a name="create-a-purchase-order"></a>Pirkimo užsakymo kūrimas
1. Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Pirkimo užsakymai > Visi pirkimo užsakymai**.
2. Spustelėkite **Naujas**.
3. Lauke **Tiekėjo sąskaita** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Raskite tiekėją, kurį norite pasirinkti. Pavyzdžiui, slinkite žemyn iki US-104.
5. Pasirinkite tiekėją US-104.
6. Spustelėkite **Gerai**.
7. Lauke **Prekės numeris** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
8. Pasirinkite atsargų prekę. Pavyzdžiui, pasirinkite prekės numerį 1000.
9. Išplėskite FastTab **Eilutės informacija**.
10. Spustelėkite skirtuką **Sąranka**. Galite netaikyti atitikimo politikos, kad nenaudotumėte atitikimo, dvipusio ar trijų krypčių atitikimo.  
11. Veiksmų srityje spustelėkite **Pirkti**.
12. Spustelėkite **Patvirtinti**.

## <a name="receive-the-products"></a>Produktų gavimas
1. Veiksmų srityje spustelėkite **Gauti**.
2. Spustelėkite **Produkto gavimo kvitas**.
3. Lauke **Produkto gavimo kvitas** įveskite produkto gavimo kvito numerį. Pavyzdžiui, įveskite PR123.
4. Spustelėkite **Gerai**, kad registruotumėte produkto gavimo kvitą.
5. Uždarykite puslapį.

## <a name="create-a-vendor-invoice"></a>Kurti tiekėjo SF
1. Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Pirkimo užsakymai > Pirkimo užsakymai gauti, bet SF neišrašyta**.
2. Pasirinkite savo sukurtą pirkimo užsakymą.
3. Veiksmų srityje spustelėkite **Sąskaita faktūra**.
4. Spustelėkite **Sąskaita faktūra**.
5. Lauke **Numeris** įveskite SF numerį.
6. Lauke **Sąskaitos faktūros aprašas** įveskite reikšmę.
7. Lauke **SF data** įveskite datą.
8. Lauke **Vieneto kaina** įveskite 1200.
9. Spustelėkite **Pridėti eilutę**.
10. Lauke **Prekės numeris** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
11. Sąraše raskite diegimo išlaidų prekės numerį. Pavyzdžiui, S0001
12. Pasirinkite diegimo išlaidų prekės numerį. Atkreipkite dėmesį, kad nuo jūsų pakeitimų negretinta.  
13. Spustelėkite **Naujinti gretinimo būseną**.
14. Veiksmų srityje spustelėkite **Peržiūrėti**.
15. Spustelėkite **Gretinimo informacija**. Naujos eilutės su paslaugomis gretinti nereikia, todėl būsena yra „Neatlikta‟.  
16. Pasirinkite atsargų prekės, kurią gavote, produkto gavimo kvitą. Eilutė, kurioje yra produkto gavimo kvitas, buvo sugretinta, tačiau neatitinka kiekis arba kaina, todėl sugretinti nepavyko.  
17. Lauke **Vieneto kaina** įveskite skaičių. Dabar, kai vieneto kaina atitinka, būsena atnaujinama į Pavyko. Jei jūsų strategija leidžia nesutapimus arba jei gretinimas yra tik įspėjimas, SF vis tiek galite registruoti.  
18. Uždarykite puslapį.
19. Spustelėkite **Registruoti.**
20. Uždarykite formą. Atkreipkite dėmesį, kad pirkimo užsakymas pateikiamas nebe kaip gautas, o kaip užsakymas, kuriam neišrašyta SF.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
