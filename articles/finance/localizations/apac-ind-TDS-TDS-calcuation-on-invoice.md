---
title: TDS skaičiavimas SF
description: Šioje temoje pateikiama operacijų, kuriose mokestis, atskaitytas šaltinyje (TDS), skaičiuojamas SF lygiu, nuoroda.
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
ms.openlocfilehash: faf381458fec27e3140579486485d89bb81dfd4c2eae2d60f906c69491009f4c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780367"
---
# <a name="tds-calculation-on-invoices"></a>TDS skaičiavimas SF

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama operacijų, kuriose mokestis, atskaitytas šaltinyje (TDS), skaičiuojamas SF lygiu, nuoroda.

| Serijos Nr. | Operacijos tipas                                 | Operacijos suma | Puslapio pavadinimas ir pasirinkimo maršrutas                                 | Sąskaitos tipas ir kompensavimo sąskaitos tipas                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1.            | Pirkimas, atliktas iš tiekėjo/įrašymo išlaidų   | Debetas ar Kreditas  | Bendrųjų žurnalų puslapis (DIDŽIOJI knyga > Žurnalo įrašai > Žurnalai), SF patvirtinimo žurnalo puslapis (Mokėtinos sumos > SF > SF patvirtinimas), SF žurnalo puslapis (Mokėtinos sumos > SF > SF žurnalas) | DK (Dr.) tiekėjas (Cr.).  Išskaitomas mokestis skaičiuojamas tiekėjo ir DK kombinacijai tik tada, kai DK sąskaitos registravimo tipas yra **Pirkimas**  **grynaisiais pinigais**. |
| 2.            | Pirkimas, atliktas iš kliento/įrašymo išlaidų | Debetas ar Kreditas  | Bendrųjų žurnalų puslapis (DIDŽIOJI knyga > Žurnalo įrašai > Bendrieji žurnalai), SF žurnalo puslapis (Mokėtinos sumos > SF > SF žurnalas) | DK (Dr.) Klientas (Cr.)                                 |
| 3.            | Ilgalaikio turto pirkimas iš tiekėjo              | Debetas ar Kreditas  | Bendrųjų žurnalų puslapis (DIDŽIOJI knyga > Žurnalo įrašai > Žurnalai), SF registravimo žurnalo puslapis (Mokėtinos sumos > SF > SF registravimas), SF žurnalo puslapis (Mokėtinos sumos > SF > SF žurnalas) | Ilgalaikio turto (Dr.) tiekėjas (Cr.)                             |
| 4.            | Ilgalaikio turto pirkimas iš kliento            | Debetas ar Kreditas  | Bendrųjų žurnalų puslapis (DIDŽIOJI knyga > Žurnalo įrašai > Bendrieji žurnalai), SF žurnalo puslapis (Mokėtinos sumos > SF > SF žurnalas) | Ilgalaikio turto (Dr.) klientas (Cr.)                           |
| 5.            | Pirkimo SF (TDS mokėtina suma)                  |                    | Pirkimo užsakymo puslapis (Pirkimo užsakymai > Visi pirkimo užsakymai) |                                                              |
| 6.            | Pardavimo SF (gautinos TDS)                  |                    | Pardavimo užsakymo puslapis (Gautinos sumos > Užsakymai > Visi pardavimo užsakymai), laisvos formos SF puslapis (Gautinos sumos > SF > Visos laisvos formos SF) |                                                              |
