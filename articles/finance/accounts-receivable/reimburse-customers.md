---
title: Kompensacija klientams
description: Šiame straipsnyje paaiškinta, kaip kurti klientų grupės kompensavimo operacijas. Jei klientas turi kredito balansą, galite kompensuoti klientui balanso sumą.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97982dec140ed440682ae507f40557670ebccd3e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179080"
---
# <a name="reimburse-customers"></a>Kompensacija klientams

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinta, kaip kurti klientų grupės kompensavimo operacijas. Jei klientas turi kredito balansą, galite kompensuoti klientui balanso sumą. 

Pateiktoje lentelėje parodytos būtinosios sąlygos, kurias reikia įvykdyti prieš pradedant.

| Būtinoji sąlyga                                                            | Prekės/Paslaugos pavadinimas                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nurodykite mažiausią kompensacijos sumą juridiniam subjektui.          | Puslapyje **Gautinų sumų parametrai**, srityje **Bendra**, lauke **Mažiausia kompensacija** įveskite mažiausią sumą, kurią galima kompensuoti dėl klientų permokėjimo. |
| Pasirinktinai: įtraukite tiekėjo sąskaitą kiekvienam klientui, kuriam galima kompensuoti. | Puslapyje **Klientai**, „FastTab“ skirtuke **Įvairi informacija**, lauke **Tiekėjo sąskaita** pasirinkite kliento tiekėjo sąskaitą.                                           |

Kuriant kompensavimo operacijas, kredito balanso sumai sukuriama tiekėjo SF. Kompensacijos procesas pašalina kliento sąskaitos kredito balansą ir sukuria mokėtiną balanso sumą tiekėjo sąskaitai, kuri atitinka klientą.

1.  Gautinų sumų srityje vykdykite procesą **Kompensacija**.
2.  Atlikite vieną iš toliau nurodytų veiksmų.
    -   Norėdami kompensuoti konkrečias kliento sąskaitas, spustelėkite **Pasirinkti** ir užklausoje nurodykite kliento sąskaitas.
    -   Norėdami kompensuoti visas kliento sąskaitas, spustelėkite **Gerai**.

    Kredito sumos perkeliamos į klientų tiekėjų sąskaitas ir apdorojamos kaip įprasti mokėjimai. Jei klientas neturi tiekėjo sąskaitos, klientui automatiškai sukuriama vienkartinė tiekėjo sąskaita.
3.  Norėdami peržiūrėti sukurtas kompensacijos operacijas, naudokite puslapį **Kompensacija**.
4.  Mokėtinų sumų srityje sukurkite mokėjimą tiekėjo SF, kurias sukūrė kompensacijos procesas.



