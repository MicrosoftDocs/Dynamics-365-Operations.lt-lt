---
title: Įtraukti tiekėjo parametrai, skirti įkeltoms išlaidoms
description: Šioje temoje aprašomi nauji laukai, kurie įtraukiami į esamų tiekėjų puslapį, kai įgalinate įkeltų išlaidų modulį. Šiuos laukus naudojate nustatyti tiekėjams, kuriuos naudosite kartu su įkeltų išlaidų funkcijomis.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: dc68cfd1afab808b1aa79fe4d0387cb6bb6c198f
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568740"
---
# <a name="vendor-settings-added-for-landed-cost"></a>Įtraukti tiekėjo parametrai, skirti įkeltoms išlaidoms

[!include [banner](../../includes/banner.md)]

Kai įgalinate **Įkeltų išlaidų** modelį, į esamų **Tiekėjų** puslapį įtraukiami keli nauji laukai. Šiuos laukus naudojate nustatyti tiekėjams, kuriuos naudosite kartu su įkeltų išlaidų funkcijomis.

Atitinkamų laukų nustatymui eikite į **Įsigijimas ir tiekimas \> Tiekėjai \> Visi tiekėjai**. Atidarykite esamą tiekėją arba sukurkite naują tiekėją, o tada pasirinkite **Įvairi informacija** „FastTab”. Visi nauji laukai, kuriuos prideda **Įkeltų išlaidų** modulis, rodomi **Reisų** antraštėje. Toliau pateiktoje lentelėje aprašomi šie laukai.

| Laukas | Aprašymas |
|---|---|
| Gabenimo tipas | <p>Pasirinkite tiekėjo vaidmenį, ryšium su Įkeltomis išlaidomis:</p><ul><li>**Jokia** – Tiekėjas neturi konkretaus vaidmens, susijusio su Įkeltomis išlaidomis. Ši reikšmė yra numatytasis parametras, nes daugelis tiekėjų tikriausiai neturės konkretaus vaidmens.</li><li>**Siuntimo įmonė** – Tiekėjas yra siuntimo įmonė. Šio siuntimo tipo tiekėjus galima pasirinkti puslapio **Reisai** lauke **Siuntimo įmonė**.</li><li>**Muitinės tarpininkas** – Tiekėjas yra muitinės tarpininkas. Šio siuntimo tipo tiekėjus galima pasirinkti puslapio **Registravimo lapai** lauke **Muitinės tarpininkas**.</li><li>**Agentas** – Tiekėjas yra agentas. Šio siuntimo tipo tiekėjus galima pasirinkti puslapių **Tiekėjai** ir **Pirkimo užsakymai** lauke **Agentas**.</li></ul> |
| Išlaidų tipo grupė | Priskirkite tiekėją išlaidų tipo grupei, kad būtų galima pasirinkti [automatines išlaidas](auto-cost-setup.md). |
| Kilmės uostas | Pasirinkite reiso kilmės uostą. |
| Agentas | Numatytasis agentas, kai perkama iš tiekėjo. |
| Importuoti įkainojimo tiekėją | <p>Nurodykite, ar tiekėjas yra Įkeltų išlaidų tiekėjas.</p><p>**Patarimas:** Šį lauką galite naudoti kartu su įrašo lygio sauga, norėdami apriboti pirkimo užsakymus, kurie rodomi kuriant reisą.</p> |
| Gabenimo įmonė | Pasirinkite numatytąją siuntimo įmonę, naudojamą kuriant pirkimo užsakymus tiekėjui. |
| Paslaugų teikėjas | Nurodykite, ar tiekėjas yra paslaugų teikėjas. |
| Leistino perviršio/trūkumo grupė | Pasirinkite numatytąją leistino perviršio/trūkumo grupę tiekėjui. |
