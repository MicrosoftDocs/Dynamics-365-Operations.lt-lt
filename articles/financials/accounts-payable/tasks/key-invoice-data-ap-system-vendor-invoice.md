--- 
title: "Pagrindiniai SF duomenys mokėtinose sumose naudojant tiekėjo SF"
description: "Šis užduočių vadovas jums padės iš pirkimo užsakymo sukurti tiekėjo SF ir peržiūrėti pirkimo užsakymo, gavimo kvito ir SF gretinimo (trišalis gretinimas) rezultatus."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 48535a283cbdfdc7343a20105b139c527cac85f4
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-a-vendor-invoice"></a>Pagrindiniai SF duomenys mokėtinose sumose naudojant tiekėjo SF

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šis užduočių vadovas jums padės iš pirkimo užsakymo sukurti tiekėjo SF ir peržiūrėti pirkimo užsakymo, gavimo kvito ir SF gretinimo (trišalis gretinimas) rezultatus.


## <a name="create-a-purchase-order"></a>Pirkimo užsakymo kūrimas
1. Eikite į Mokėtinos sumos > Pirkimo užsakymai > Visi pirkimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Raskite tiekėją, kurį norite pasirinkti. Pavyzdžiui, slinkite žemyn iki US-104.
5. Pasirinkite tiekėją US-104.
6. Spustelėkite Gerai.
7. Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
8. Pasirinkite atsargų prekę. Pavyzdžiui, pasirinkite prekės numerį 1000.
9. Išplėskite arba sutraukite dalį Išsami eilučių informacija.
10. Spustelėkite skirtuką Nustatymas.
    * Galite nepaisyti atitikimo strategijos ir jos nenaudoti, naudoti dvišalę arba trišalę atitikimo strategiją.  
11. Išplėskite arba sutraukite dalį Išsami eilučių informacija.
12. Veiksmų srityje spustelėkite Pirkti.
13. Spustelėkite Patvirtinti.

## <a name="receive-the-products"></a>Produktų gavimas
1. Veiksmų srityje spustelėkite Gauti.
2. Spustelėkite Produkto gavimo kvitas.
3. Lauke Produkto gavimo kvitas įveskite produkto gavimo kvito numerį. Pavyzdžiui, įveskite PR123.
4. Spustelėkite Gerai, kad registruotumėte produkto gavimo kvitą.
5. Uždarykite puslapį.

## <a name="create-a-vendor-invoice"></a>Kurti tiekėjo SF
1. Pasirinkite Mokėtinos sumos > Pirkimo užsakymai > Gauti pirkimo užsakymai, kuriems neišrašytos SF.
2. Pasirinkite savo sukurtą pirkimo užsakymą.
3. Veiksmų srityje spustelėkite Sąskaita faktūra.
4. Spustelėkite Sąskaita faktūra.
5. Lauke Numeris įveskite SF numerį.
6. Lauke Sąskaitos faktūros aprašas įveskite reikšmę.
7. Įveskite datą lauke Sąskaitos faktūros data.
8. Lauke Vieneto kaina įveskite 1200.
9. Spustelėkite Pridėti eilutę.
10. Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
11. Sąraše raskite diegimo išlaidų prekės numerį. Pavyzdžiui, S0001
12. Pasirinkite diegimo išlaidų prekės numerį.
    * Atkreipkite dėmesį, kad nuo jūsų pakeitimų negretinta.  
13. Spustelėkite Naujinti gretinimo būseną.
14. Veiksmų srityje spustelėkite Peržiūrėti.
15. Spustelėkite Gretinimo informacija.
    * Naujos eilutės su paslaugomis gretinti nereikia, todėl būsena yra „Neatlikta‟.  
16. Pasirinkite atsargų prekės, kurią gavote, produkto gavimo kvitą.
    * Eilutė, kurioje yra produkto gavimo kvitas, buvo sugretinta, tačiau neatitinka kiekis arba kaina, todėl sugretinti nepavyko.  
17. Lauke Vieneto kaina įveskite skaičių.
    * Dabar, kai vieneto kaina atitinka, būsena atnaujinama į Pavyko. Jei jūsų strategija leidžia nesutapimus arba jei gretinimas yra tik įspėjimas, SF vis tiek galite registruoti.  
18. Uždarykite puslapį.
19. Spustelėkite Registruoti.
20. Uždarykite formą.
    * Atkreipkite dėmesį, kad pirkimo užsakymas pateikiamas nebe kaip gautas, o kaip užsakymas, kuriam neišrašyta SF.  


