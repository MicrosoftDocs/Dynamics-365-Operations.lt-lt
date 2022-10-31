---
title: Dokumentai, laukiantys apskaitos
description: Šiame straipsnyje aprašoma, kaip naudoti puslapyje „Dokumentai, laukiantys apskaitos“ funkcijas.
author: ryanCCarlson2
ms.date: 09/02/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: f37d46659b2fc5bf9933719811a7b90cc4e80f52
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709256"
---
# <a name="documents-pending-accounting"></a>Dokumentai, laukiantys apskaitos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip naudoti puslapyje **Dokumentai, laukiantys apskaitos** funkcijas.

Programoje „Microsoft Dynamics 365 Finance 10.0.30“ yra funkcija **Pagerintas šaltinio dokumento apskaitos sistemos našumas**. Ši funkcija pagerina šaltinio dokumento pagrindu parengtų dokumentų registravimo procesus, pradedant nuo laisvos formos sąskaitų faktūrų registravimo proceso.

Kai ši funkcija įgalinta, papildomos knygos dokumentas registruojamas atskirai, ne apskaitos generavimo ar *registravimo žurnale* proceso, kuris sukuria visą į didžiąją knygą perkeliamą apskaitos informaciją, metu. Pavyzdžiui, registruojant laisvos formos sąskaitą faktūrą, kliento SF modulyje **Gautinos sumos** įrašoma prieš sugeneruojant visą apskaitą. Naudojant šią patobulintą efektyvumo funkciją galima daug greičiau įrašyti kliento SF, kol apskaitos generavimas atidėtas.

Puslapyje **Dokumentai, laukiantys apskaitos** yra toliau nurodyti mygtukai.

- **Generuoti apskaitą** – pateikti dokumentą, kuris šiuo metu laukia apskaitos generavimo, kad būtų galima registruoti žurnale.
- **Peržiūrėti paskirstymus** – peržiūrėti sąraše pasirinkto dokumento apskaitos paskirstymus.
- **Peržiūrėti klaidų žurnalą** – peržiūrėti bet kokią dokumento klaidų informaciją, kai apskaitos būsena rodo klaidas. Tą pačią klaidos pranešimo informaciją galite peržiūrėti dokumento eilutėje pasirinkdami saitą **Klaidų žurnalas**.

Apskaitos generavimą atlieka proceso automatizavimo foninis procesas, kuris vadinamas **Apskaitos sistemos procesoriumi**. Daugiau informacijos apie visų procesų automatizavimų sąranką ir konfigūravimą žr. [Procesų automatizavimas](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
