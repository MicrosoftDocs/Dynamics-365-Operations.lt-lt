---
title: Kompensacija klientams
description: Šiame straipsnyje paaiškinta, kaip kurti klientų grupės kompensavimo operacijas.
author: JodiChristiansen
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 892b089edb16ba560f588c086d37faafdf16958d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891788"
---
# <a name="reimburse-customers"></a>Kompensacija klientams

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinta, kaip kurti klientų grupės kompensavimo operacijas. Jei klientas turi kredito balansą, galite kompensuoti klientui balanso sumą. 

Pateiktoje lentelėje parodytos būtinosios sąlygos, kurias reikia įvykdyti prieš pradedant.

| Būtinoji sąlyga                                                            | Prekės/Paslaugos pavadinimas |
|-------------------------------------------------------------------------|-------------|
| Nurodykite mažiausią kompensacijos sumą juridiniam subjektui.          | Puslapyje **Gautinų sumų parametrai**, srityje **Bendra**, lauke **Mažiausia kompensacija** įveskite mažiausią sumą, kurią galima kompensuoti dėl klientų permokėjimo. |
| Pasirinktinai: įtraukite tiekėjo sąskaitą kiekvienam klientui, kuriam galima kompensuoti. | Puslapyje **Klientai**, „FastTab“ skirtuke **Įvairi informacija**, lauke **Tiekėjo sąskaita** pasirinkite kliento tiekėjo sąskaitą. |

Kuriant kompensavimo operacijas, kredito balanso sumai sukuriama tiekėjo SF. Kompensacijos procesas pašalina kliento sąskaitos kredito balansą ir sukuria mokėtiną balanso sumą tiekėjo sąskaitai, kuri atitinka klientą.

1. Gautinose sumose vykdykite procesą **Kompensavimas** (**Gautinos sumos \> Periodinės užduotys \> Kompensavimas**).
2. Norėdami sugrupuoti visas operacijas, nepriklausomai nuo DK dimensijų, nustatykite parinktį **Klientų sumavimas** į parametrą **Taip**. Norėdami grupuoti tik tas operacijas, kurių DK dimensijos yra panašios, nustatykite pasirinktį **Ne**.
3. Pasirinkite **Įtraukti klientus su neapmokėtomis debeto operacijomis** ir pasirinkite klientus, kurie turi nesudengtų debeto sumų.
4. Norėdami kompensuoti tam tikras klientų sąskaitas, „FastTab“ **Įtrauktini įrašai** pasirinkite **Filtruoti** ir nurodykite klientų sąskaitas užklausoje.

    Kredito sumos perkeliamos į klientų tiekėjų sąskaitas ir apdorojamos kaip įprasti mokėjimai. Jei klientas neturi tiekėjo sąskaitos, klientui automatiškai sukuriama vienkartinė tiekėjo sąskaita.

5. Norėdami peržiūrėti sukurtas kompensavimo operacijas, naudokite ataskaitą **Kompensavimas** (**Gautinos sumos \> Užklausos ir ataskaitos \> Kompensavimo ataskaita**).
6. Mokėtinų sumų srityje sukurkite mokėjimą tiekėjo SF, kurias sukūrė kompensacijos procesas. Norėdami gauti daugiau informacijos apie tai, kaip mokėti tiekėjams, žr. [Tiekėjų mokėjimo apžvalga](../accounts-payable/Vendor-payments-workspace.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
