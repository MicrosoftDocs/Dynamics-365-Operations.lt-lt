---
title: Verslo dokumentai, kuriuos palaiko Visuotinė atsargų apskaita
description: Šioje temoje išvardyti verslo dokumentai, kuriuos palaiko Visuotinė atsargų apskaita. Taip pat pateikiamas išsamus pirkimo užsakymo dokumentų pavyzdys.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 311c894d709985d0d053b0ec3a317142aa582c39
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273199"
---
# <a name="business-documents-supported-by-global-inventory-accounting"></a>Verslo dokumentai, kuriuos palaiko Visuotinė atsargų apskaita

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Visiškai nustačius Visuotinės atsargų apskaitos papildinį, jis parengtas apdoroti su atsargomis susijusius dokumentus, įvestus į „Microsoft Dynamics 365 Supply Chain Management”.

## <a name="supported-business-documents"></a>Palaikomi verslo dokumentai

Yra du verslo dokumentų tipai:

- **Dokumentai, turintys žurnalą** – Šie dokumentai apima produkto gavimo kvito, pirkimo sąskaitos faktūros, važtaraščio ir pardavimo sąskaitos faktūros dokumentus.
- **Dokumentai, neturintys žurnalo** – Šie dokumentai apima skaičiavimo, judėjimo ir atsargų koregavimo dokumentus.

Toliau šioje temoje pirkimo užsakymai bus naudojami kaip proceso iliustravimo pavyzdys.

Šioje lentelėje pateikiami dokumentai, kuriuos palaiko dabartinis paleidimas.

| Dokumento tipas      | Dokumentas        |
|--------------------|-----------------|
| Pirkimo Užsakymas     | Produkto kvitas |
| Pirkimo Užsakymas     | PVM sąskaita faktūra         |
| Pardavimo Užsakymas        | Važtaraštis    |
| Pardavimo Užsakymas        | PVM sąskaita faktūra         |
| Atsargų Žurnalai | Judėjimas        |
| Atsargų Žurnalai | Koregavimas      |
| Atsargų Žurnalai | Inventorizacija        |
| Atsargų Žurnalai | Perkelti        |
| Perkėlimo Užsakymas     | Siunta        |
| Perkėlimo Užsakymas     | Gauti         |

> [!IMPORTANT]
> Visuotinė atsargų apskaita asinchroniškai apdoroja dokumentus, įvestus į „Supply Chain Management”. Probleminiuose dokumentuose klaidų pranešimai nebus rodomi.

## <a name="example-purchase-order"></a>Pavyzdys: Pirkimo užsakymas

### <a name="product-receipt"></a>Gavimo dokumentas

Registruokite produktų gavimo kvitus įprastu būdu. Puslapyje **Visi pirkimo užsakymai** pasirinkite pirkimo užsakymą, o tada veiksmų srities skirtuke **Gauti** pasirinkite **Produkto gavimo kvitas**, kad atidarytumėte **Produkto gavimo kvitų žurnalų** puslapį. Kiekvienai eilutei generuojamas operacijos įvykis ir Visuotinės atsargų apskaitos įvykis. Todėl pasirinkite skirtuką **Eilutės** ir tada – **Atsargos \> Įvykiai ir matavimai**, kad atidarytumėte **Įvykiai ir matavimai** puslapį.

Visuotinė atsargų apskaita yra apskaitos sistema, pagrįsta įvykiais ir matavimais. Matavimo eilutės tinklelis **Įvykių ir matavimų** puslapyje rodo matavimų sąrašą. Kiekvienas matavimo vienetas turi dimensijų sąrašą.

Yra du kiekvieno operacijos įvykio matavimo vienetų tipai:

- **Operacijų matavimo vienetai** – Šie matavimai apibūdina verslo dokumentus bendrais terminais. Vienas matavimas yra produkto kiekis, naudojantis matavimo vienetą, kuris naudojamas dokumente. Taip pat yra matavimų, kurie paveikia atsargų vertę, pavyzdžiui, išplėstinę kainą, nuolaidą, nuolaidos procentą ir eilutės mokestį.
- **Išteklių apskaitos matavimai** – šie matavimai yra iš atsargų registro perspektyvos. Jie apibūdina dokumento poveikį atsargoms atsargų matavimo vienetu. Jei yra kelios atsargų registracijos, yra ir kelios išteklių apskaitos matavimų eilutės.

Dimensijos organizuojamos tokiu būdu:

- **Dvilypumas** – dvilypumas apibūdina agentus, kurie dalyvauja ekonominiuose įvykiuose. Išoriniams verslo dokumentams pirminės dimensijos apibūdina juridinį subjektą, kuriame įvestas dokumentas, o dvigubos dimensijos aprašo tiekėją, klientą ir panašiai. Vidiniams verslo dokumentams (pavyzdžiui, perkėlimo užsakymams) dvigubos dimensijos apibūdina atitinkamą sandėlį.
- **Dimensijos tipas** – Dimensijų tipai klasifikuoja dimensijas.
- **Dimensija** – dimensijos pavadinimas.
- **Dimensijos reikšmė** – dimensijos reikšmė.

### <a name="global-inventory-accounting-event"></a>Visuotinės Atsargų apskaitos įvykis

Visuotinė atsargų apskaita ima operacijos įvykius ir matavimus kaip įvestį. Tuomet ji atlieka atitinkamą kiekvienos susijusios didžiosios knygos apskaitą, paremtą pridėta valiuta ir konvencija. Galite pasirinkti **Visuotinės atsargų apskaitos įvykius ir matavimo vienetus**, kad peržiūrėtumėte Visuotinės atsargų apskaitos įvykį. Visuotinės atsargų apskaitos įvykis naudoja tą pačią metodologiją kaip ir operacijų įvykiai, tačiau naudojami skirtingi matavimai. Yra trys pagrindiniai matavimo tipai: produkto savikainos kiekis, produkto savikaina ir nuokrypis.

Papildomos knygos sąskaitos naudojamos toliau klasifikuoti matavimams. Gali būti keletas didžiųjų knygų. Šios didžiosios knygos yra susietos su juridiniu subjektu, kuriame įvestas dokumentas. Galite peržiūrėti kiekvienos didžiosios knygos įvykius ir matavimus pakeisdami lauko **Didžioji knyga** reikšmę.

### <a name="cost-element"></a>Savikainos elementas

Atsižvelgiant į prie didžiosios knygos pridėtą savikainos elemento strategiją, sistema priskiria savikainos elementą kiekvienam apskaičiuotos operacijos įvykio matavimui, kuris veikia atsargų savikainą. Šie matavimai apima išplėstinę kainą, nuolaidą, nuolaidos procentą ir eilutės mokestį.

### <a name="measurement-line-details"></a>Matavimo vieneto eilutės informacija

Skirtuke **Peržiūra** rodoma išsami informacija apie pridėtas strategijas. Savikainos objekto dimensijos rodo savikainos objektą, pagrįstą savikainos objekto strategija. Konkrečios identifikavimo dimensijos rodo paketo numerį, jei išlaidų srauto prielaida yra *Konkreti – Paketas*.

### <a name="purchase-invoice"></a>Pirkimo SF

Registruokite sąskaitą faktūrą įprastu būdu. Tada veiksmų srities skirtuke **Sąskaita faktūra**, grupėje **Žurnalai**, pasirinkite **Sąskaita faktūra**, kad atidarytumėte sąskaitos faktūros žurnalą. Kiekvienai eilutei sugeneruojamas operacijos įvykis ir Visuotinės atsargų apskaitos įvykis. Todėl pasirinkite skirtuką **Eilutės** ir tada – **Atsargos \> Įvykiai ir matavimai**, kad atidarytumėte **Įvykiai ir matavimai** puslapį. Puslapyje **Įvykiai ir matavimo vienetai** rodomas toks pats matavimo tipas. Tačiau, kadangi puslapyje rodomas kitoks matavimo vaidmuo ir matavimo modifikatorius, poveikis agentui (juridiniam subjektui) skiriasi.

Pasirinkite **Visuotinės atsargų apskaitos įvykius ir matavimo vienetus**, kad peržiūrėtumėte Visuotinės atsargų apskaitos įvykį. Atsargų kiekis ir savikaina dabar patenka iš *Gautos prekės, atsargoms nepadaryta sąskaita faktūra* papildomos knygos sąskaitos į *Nupirktų prekių savikaina* papildomos knygos sąskaitą.
