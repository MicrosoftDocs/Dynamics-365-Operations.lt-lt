---
title: TDS skaičiavimas SF
description: Šiame straipsnyje pateikiama operacijų, kuriose mokestis, atskaitytas šaltinyje (TDS), apskaičiuojamas SF lygiu, nuoroda.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: efc12e0839fe87e9db435f481ce1fd733c286d6c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855369"
---
# <a name="tds-calculation-on-invoices"></a>TDS skaičiavimas SF

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama operacijų, kuriose mokestis, atskaitytas šaltinyje (TDS), apskaičiuojamas SF lygiu, nuoroda.

| Serijos Nr. | Operacijos tipas                                 | Operacijos suma | Puslapio pavadinimas ir pasirinkimo maršrutas                                 | Sąskaitos tipas ir kompensavimo sąskaitos tipas                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1.            | Pirkimas, atliktas iš tiekėjo/įrašymo išlaidų   | Debetas ar Kreditas  | Bendrųjų žurnalų puslapis (DIDŽIOJI knyga > Žurnalo įrašai > Žurnalai), SF patvirtinimo žurnalo puslapis (Mokėtinos sumos > SF > SF patvirtinimas), SF žurnalo puslapis (Mokėtinos sumos > SF > SF žurnalas) | DK (Dr.) tiekėjas (Cr.).  Išskaitomas mokestis skaičiuojamas tiekėjo ir DK kombinacijai tik tada, kai DK sąskaitos registravimo tipas yra **Pirkimas**  **grynaisiais pinigais**. |
| 2.            | Pirkimas, atliktas iš kliento/įrašymo išlaidų | Debetas ar Kreditas  | Bendrųjų žurnalų puslapis (DIDŽIOJI knyga > Žurnalo įrašai > Bendrieji žurnalai), SF žurnalo puslapis (Mokėtinos sumos > SF > SF žurnalas) | DK (Dr.) Klientas (Cr.)                                 |
| 3.            | Ilgalaikio turto pirkimas iš tiekėjo              | Debetas ar Kreditas  | Bendrųjų žurnalų puslapis (DIDŽIOJI knyga > Žurnalo įrašai > Žurnalai), SF registravimo žurnalo puslapis (Mokėtinos sumos > SF > SF registravimas), SF žurnalo puslapis (Mokėtinos sumos > SF > SF žurnalas) | Ilgalaikio turto (Dr.) tiekėjas (Cr.)                             |
| 4.            | Ilgalaikio turto pirkimas iš kliento            | Debetas ar Kreditas  | Bendrųjų žurnalų puslapis (DIDŽIOJI knyga > Žurnalo įrašai > Bendrieji žurnalai), SF žurnalo puslapis (Mokėtinos sumos > SF > SF žurnalas) | Ilgalaikio turto (Dr.) klientas (Cr.)                           |
| 5.            | Pirkimo SF (TDS mokėtina suma)                  |                    | Pirkimo užsakymo puslapis (Pirkimo užsakymai > Visi pirkimo užsakymai) |                                                              |
| 6.            | Pardavimo SF (gautinos TDS)                  |                    | Pardavimo užsakymo puslapis (Gautinos sumos > Užsakymai > Visi pardavimo užsakymai), laisvos formos SF puslapis (Gautinos sumos > SF > Visos laisvos formos SF) |                                                              |
