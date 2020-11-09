---
title: Kompensacija klientams
description: Šiame straipsnyje paaiškinta, kaip kurti klientų grupės kompensavimo operacijas. Jei klientas turi kredito balansą, galite kompensuoti klientui balanso sumą.
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
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
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bceeaf99437f6ef66bd3b4e1710b469c262e693e
ms.sourcegitcommit: 9e7ceb5604472f3088f611aa0360bd6a716db32b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022548"
---
# <a name="reimburse-customers"></a>Kompensacija klientams

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinta, kaip kurti klientų grupės kompensavimo operacijas. Jei klientas turi kredito balansą, galite kompensuoti klientui balanso sumą. 

Pateiktoje lentelėje parodytos būtinosios sąlygos, kurias reikia įvykdyti prieš pradedant.

| Būtinoji sąlyga                                                            | Prekės/Paslaugos pavadinimas                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nurodykite mažiausią kompensacijos sumą juridiniam subjektui.          | Puslapyje **Gautinų sumų parametrai** , srityje **Bendra** , lauke **Mažiausia kompensacija** įveskite mažiausią sumą, kurią galima kompensuoti dėl klientų permokėjimo. |
| Pasirinktinai: įtraukite tiekėjo sąskaitą kiekvienam klientui, kuriam galima kompensuoti. | Puslapyje **Klientai** , „FastTab“ skirtuke **Įvairi informacija** , lauke **Tiekėjo sąskaita** pasirinkite kliento tiekėjo sąskaitą.                                           |

Kuriant kompensavimo operacijas, kredito balanso sumai sukuriama tiekėjo SF. Kompensacijos procesas pašalina kliento sąskaitos kredito balansą ir sukuria mokėtiną balanso sumą tiekėjo sąskaitai, kuri atitinka klientą.

1.  Gautinų sumų srityje vykdykite procesą **Kompensacija**.
2.  Atlikite vieną iš toliau nurodytų veiksmų.
    -   Norėdami kompensuoti konkrečias kliento sąskaitas, spustelėkite **Pasirinkti** ir užklausoje nurodykite kliento sąskaitas.
    -   Norėdami kompensuoti visas kliento sąskaitas, spustelėkite **Gerai**.

    Kredito sumos perkeliamos į klientų tiekėjų sąskaitas ir apdorojamos kaip įprasti mokėjimai. Jei klientas neturi tiekėjo sąskaitos, klientui automatiškai sukuriama vienkartinė tiekėjo sąskaita.
3.  Norėdami peržiūrėti sukurtas kompensacijos operacijas, naudokite puslapį **Kompensacija**.
4.  Mokėtinų sumų srityje sukurkite mokėjimą tiekėjo SF, kurias sukūrė kompensacijos procesas.




