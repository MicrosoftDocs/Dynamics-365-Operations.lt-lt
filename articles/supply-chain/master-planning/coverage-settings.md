---
title: Padengimo parametrai
description: Šioje temoje pateikiama informacija apie padengimo parametrus, kurie bendrojo planavimo metu naudojami prekių poreikiui skaičiuoti.
author: roxanadiaconu
manager: tfehr
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0aaacf28701542d329afedd8206a12f7c11b7ac7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999986"
---
# <a name="coverage-settings"></a>Padengimo parametrai

[!include [banner](../includes/banner.md)]

Bendrasis planavimas naudoja padengimo parametrus prekės poreikiui apskaičiuoti.

Galite nurodyti padengimo parametrus keliais būdais:

- Nurodykite padengimo grupės padengimo parametrus.

    Galite sukurti padengimo grupę, kurioje būtų visų su padengimo grupe susijusių produktų parametrai. Norėdami sukurti padengimo grupę, eikite į **Bendrasis planavimas &gt; Sąranka &gt; Padengimas &gt; Padengimo grupės**. Padengimo grupę galite susieti su produktu. Jei saitas yra konkrečios teritorijos, sandėlio ar produkto dimensijos, naudokite puslapio **Prekės padengimas** lauką **Padengimo grupė**. Jei saitas yra bendrasis, neatsižvelgdami į produkto dimensijas, naudokite puslapio **Produkto informacija** sparčiajame skirtuke **Planas** esantį lauką **Padengimo grupė**. Pagal numatytuosius parametrus, jei padengimo grupės nesusiejate su produktu, bendrojo planavimo funkcija kaip numatytąją naudoja puslapyje **Bendrojo planavimo parametrai** nurodytą parinktį Bendroji padengimo grupė.

- Nurodykite produkto padengimo parametrus.

    Galite sukurti konkretaus produkto padengimo parametrus. Eikite į **Produkto informacijos valdymas &gt; Produktai &gt; Patvirtinti produktai**. Pasirinkite produktą ir Veiksmų srities skirtuko **Planas** lauke **Padengimo** grupėje pasirinkite **Prekės padengimas**, kad būtų atidarytas puslapis **Prekės padengimas**. Jei produktas jau susietas su padengimo grupe, galite nepaisyti padengimo grupės parametrų, naudodami lauką **Nepaisyti**. Padengimo parametrams puslapyje **Prekės padengimas** teikiama pirmenybė prieš parametrus puslapyje **Padengimo grupė**.

- Nurodykite produkto padengimo parametrus naudodami vedlį.

    Vediklis nuosekliai pademonstruos pagrindinių prekės padengimo parametrų sąrankos procesą. Veiksmų srities puslapyje **Prekės padengimas** pasirinkite **Vedlys**, kad būtų atidarytas **Prekės padengimo vedlys**.

- Nurodykite dimensijos grupės padengimo parametrus.

    Eikite į **Produkto informacijos valdymas &gt; Produktai &gt; Patvirtinti produktai**. Puslapio **Patvirtinto produkto informacija** sparčiajame skirtuke **Bendra** esančioje sekcijoje **Administravimas** pasirinkite saitą lauke **Saugojimo dimensijų grupė**. Puslapyje **Saugojimo dimensijų grupės** pasirinkite žymės laukelį **Padengimo planas dimensijomis**, kad sukurtumėte saugojimo dimensijų grupės dimensijos padengimo nustatymus. Visose produkto dimensijose, pvz., konfigūracijos, spalvos, dydžio, stiliaus, turi būti pasirinktas laukas **Padengimo planas pagal dimensiją**.


## <a name="coverage-codes"></a>Padengimo kodai

Bendrąjį planavimą galima konfigūruoti, kad būtų naudojami skirtingi papildymo metodai. Papildymo metodai ar partijų dydžio nustatymo metodai yra sistemos naudojami metodai, siekiant nustatyti įsigytų arba pagamintų prekių paketo dydį. 

Kiekvienam papildymo metodui priskiriamas vienas toliau pateiktų padengimo kodų.

- **Rankinis** – partijos dydžio nustatymo metodas, kai sistema nenurodo prekės pirkimo, perkėlimo ar gamybos užsakymų. Prekės planuotojas bus atsakingas už būtinų prekės papildymo užsakymų kūrimą.
- **Pagal poreikius** – partijos dydžio nustatymo metodas, pagal kurį sistema sukuria suplanuotą pirkimo, perkėlimo ar gamybos užsakymą kiekvienam prekės reikalavimui. Tai dažniausiai naudojama brangiems objektams su kintama paklausa.  
- **Per laikotarpį** – partijos dydžio nustatymo metodas, kuris sujungia visą laikotarpio paklausą į vieną prekės užsakymą. Užsakymas bus suplanuotas pirmai laikotarpio dienai, o jo kiekis patenkins grynuosius poreikius nustatyto laikotarpio metu. Laikotarpis pradedamas nuo pirmo prekės poreikio ir apima nustatytą laiko trukmę. Kitas laikotarpis prasidės nuo kitų prekės reikalavimų.
- **Min./maks.** – partijos dydžio nustatymo metodas, kuriame yra atsargų papildymas iki tam tikro lygio, kai prognozuojama, kad turimos atsargos yra žemiau ribinės reikšmės. Papildymo kiekis bus skirtumas tarp maksimalaus lygio ir prognozuojamo turimų atsargų lygio.


## <a name="additional-resources"></a>Papildomi ištekliai

[Bendrųjų planų apžvalga](master-plans.md)
