---
title: Paėmimo informacijos modulis
description: Šiame straipsnyje aprašomas paėmimo informacijos modulis ir aprašoma, kaip jį pridėti prie checkout puslapių Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 57633b7a23e581278ec0bc09ea146f5453570c4e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288412"
---
# <a name="pickup-information-module"></a>Paėmimo informacijos modulis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomas paėmimo informacijos modulis ir aprašoma, kaip jį pridėti prie checkout puslapių Microsoft Dynamics 365 Commerce.

Paėmimo informacijos modelis gali būti naudojamas išsiregistravimo modeliui, kad jis rodytų užsakymo paėmimo informaciją. Klientai gali peržiūrėti esamas paėmimo datas ir laiko vietas ir tada rinktis tinkamą laiką jų užsakymo paėmimui. Pavyzdžiui, klientas gali rinktis paėmimą 15 valandą kovo 21 dieną iš San Francisko parduotuvės.

Paėmimo laikai atitinkamoms parduotuvėms turi būti sukonfigūruoti komercijos štabe. Dėl išsamesnės informacijos, žr. [Sukurti ir naujinti laiko vietas kliento paėmimui](dev-itpro/pickup-timeslots.md).

Jei paėmimo informacijos modulis sukuriamas išsiregistravimo puslapyje, bet nėra jokių laiko vietų nustatytų parduotuvei, kuri pasirinkta, modulis rodys informaciją, bet vartotojas negalės pasirinkti laiko vietos. Laiko vietos yra pasirenkamos ir nebūtinos užsakymo padarymui.

Jei kelios prekės pasirenkamos paėmimui keliose parduotuvių, paėmimo informacijos modulis leidžia vartotojui pasirinkti laiko vietą kiekvienai parduotuvei su sąlyga, kad laiko vietos yra joms prieinamos.

> [!NOTE]
> Palaikymas laiko vietoms ir išsiregistravimo paėmimo informacijos modulis prieinamas „Dynamics 365 Commerce“ versijoje 10.0.15 ir vėlesnėse.

Tolesnis paveikslėlis rodo pavyzdį laiko vietos pasirinkimo per paėmimo informacijos modulį išsiregistravimo puslapyje.

![Paėmimo informacijos modulio pavyzdys išsiregistravimo puslapyje.](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a>Modulio ypatybės

- **Antraštė** – Įveskite antraštę moduliui.

## <a name="show-time-slot-information-after-an-order-is-placed"></a>Rodyti vietos informaciją po užsakymo padarymo

Kai užsakymas yra padarytas, informacija apie pasirinktą laiko vietą gali būti peržiūrėta [užsakymo patvirtinimo modulis](order-confirmation-module.md) ir [užsakymo informacijos modulis](account-management.md#order-details-page). Abu šie moduliai turi **Rodyti laiko vietos informacijos** ypatybę. Prieš tai, kai galima rodyti pasirinktą laiko vietą užsakymo proceso metu, ši ypatybė turi būti nustatyta į **Teisinga**.

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a>Įtraukite išsiregistravimo paėmimo informacijos modulį į puslapį

Dėl instrukcijų, kaip įtraukti paėmimo informacijos modulį į išsiregistravimo puslapį ir nustatyti būtinas ypatybes, žr. [Išsiregistravimo modulis](add-checkout-module.md).

Tolesnis paveikslėlis rodo e-komercijos išsiregistravimo puslapio pavyzdį, kuris apima laiko vietas paėmimo eilučių prekėms.

![E-komercijos išsiregistravimo puslapio pavyzdys, apimantis laiko vietas paėmimo eilučių prekėms.](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a>Papildomi ištekliai

[Kliento paėmimo laiko atkarpų kūrimas ir naujinimas](dev-itpro/pickup-timeslots.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Užsakymo patvirtinimo modulis](order-confirmation-module.md)

[Išsamios užsakymo informacijos modulis](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
