---
title: Vidinės įmonės operacijų TDS skaičiavimas
description: Šioje temoje aprašomas procesas, naudojamas apskaičiuoti atskaičius mokesčius šaltinio (TDS) vidinės įmonės operacijose etapais.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 0e304747cc93bfe0a39beababc3182ca14664b11
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023451"
---
# <a name="tds-calculation-on-intercompany-transactions"></a>Vidinės įmonės operacijų TDS skaičiavimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomas procesas, naudojamas apskaičiuoti atskaičius mokesčius šaltinio (TDS) vidinės įmonės operacijose etapais.

Kai sukuriamas vidinės įmonės pirkimo užsakymas arba pardavimo užsakymas, TDS grupė, nurodyta klientui ar tiekėjui, naudojama TDS sumai apskaičiuoti. TDS suma užregistruojama susigrąžinamose arba mokėtinose sąskaitose po to, kai UŽREGISTRUOJAma SF.

Vidinės įmonės pardavimo arba pirkimo užsakymas automatiškai sukuriamas pradiniam pirkimo užsakymui arba pardavimo užsakymui. Vidinės įmonės užsakyme rodoma numatytoji TDS grupė, kad būtų galima apskaičiuoti TDS. TDS grupę galite keisti. SF galima registruoti tik tada, jei vidinės įmonės užsakymo, kuris automatiškai sukuriamas, grynoji SF suma sutampa su pradinio užsakymo SF suma. (Grynoji suma yra SF suma, atskaičius TDS.)

Pavyzdžiui, sukuriama 50 000 pardavimo SF, prie jos pridedama **10%** TDS grupė. Užregistruota SF suma yra 45 000, o užregistruota pardavimo SF TDS suma yra 5000. Automatiškai sukuriamas vidinės įmonės pardavimo užsakymo pirkimo užsakymas, prie jo pridedama **10%** TDS grupė. Jeigu TDS grupę pakeisite į **15%**  SF užregistruoti nepavyks, nes automatiškai sukurto vidinės įmonės pardavimo užsakymo grynoji SF suma neatitinka pradinio pardavimo užsakymo grynosios SF sumos.

Automatiškai užregistruojamas vidinės įmonės SF sukurtas mokėjimo žurnalas. Šį mokėjimų žurnalą galima registruoti tik tada, jei jo grynoji mokėjimo suma atitinka pradinio mokėjimų žurnalo grynąją mokėjimo sumą.
