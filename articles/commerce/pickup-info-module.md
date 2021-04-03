---
title: Paėmimo informacijos modulis
description: Ši tema apima paėmimo informacijos modulį ir aprašo, kaip įtraukti jį į išregistravimo puslapius „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 222e8ad79b30e5197f7140958309d442b284f286
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263185"
---
# <a name="pickup-information-module"></a>Paėmimo informacijos modulis

[!include [banner](includes/banner.md)]

Ši tema apima paėmimo informacijos modulį ir aprašo, kaip įtraukti jį į išregistravimo puslapius „Microsoft Dynamics 365 Commerce“.

Paėmimo informacijos modelis gali būti naudojamas išsiregistravimo modeliui, kad jis rodytų užsakymo paėmimo informaciją. Klientai gali peržiūrėti esamas paėmimo datas ir laiko vietas ir tada rinktis tinkamą laiką jų užsakymo paėmimui. Pavyzdžiui, klientas gali rinktis paėmimą 15 valandą kovo 21 dieną iš San Francisko parduotuvės.

Paėmimo laikai atitinkamoms parduotuvėms turi būti sukonfigūruoti komercijos štabe. Dėl išsamesnės informacijos, žr. [Sukurti ir naujinti laiko vietas kliento paėmimui](dev-itpro/pickup-timeslots.md).

Jei paėmimo informacijos modulis sukuriamas išsiregistravimo puslapyje, bet nėra jokių laiko vietų nustatytų parduotuvei, kuri pasirinkta, modulis rodys informaciją, bet vartotojas negalės pasirinkti laiko vietos. Laiko vietos yra pasirenkamos ir nebūtinos užsakymo padarymui.

Jei kelios prekės pasirenkamos paėmimui keletoje parduotuvių, paėmimo informacijos modulis leidžia vartotojui pasirinkti laiko vietą kiekvienai parduotuvei su sąlyga, kad laiko vietos yra joms prieinamos.

> [!NOTE]
> Palaikymas laiko vietoms ir išsiregistravimo paėmimo informacijos modulis prieinamas „Dynamics 365 Commerce“ versijoje 10.0.15 ir vėlesnėse.

Tolesnis paveikslėlis rodo pavyzdį laiko vietos pasirinkimo per paėmimo informacijos modulį išsiregistravimo puslapyje.

![Paėmimo informacijos modulio pavyzdys išsiregsitravimo puslapyje](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a>Modulio ypatybės

- **Antraštė** – Įveskite antraštę moduliui.

## <a name="show-time-slot-information-after-an-order-is-placed"></a>Rodyti vietos informaciją po užsakymo padarymo

Kai užsakymas yra padarytas, informacija apie pasirinktą laiko vietą gali būti peržiūrėta [užsakymo patvirtinimo modulis](order-confirmation-module.md) ir [užsakymo informacijos modulis](account-management.md#order-details-page). Abu šie moduliai turi **Rodyti laiko vietos informacijos** ypatybę. Prieš tai, kai galima rodyti pasirinktą laiko vietą užsakymo proceso metu, ši ypatybė turi būti nustatyta į **Teisinga**.

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a>Įtraukite išsiregistravimo paėmimo informacijos modulį į puslapį

Dėl instrukcijų, kaip įtraukti paėmimo informacijos modulį į išsiregistravimo puslapį ir nustatyti būtinas ypatybes, žr. [Išsiregistravimo modulis](add-checkout-module.md).

Tolesnis paveikslėlis rodo e-komercijos išsiregistravimo puslapio pavyzdį, kuris apima laiko vietas paėmimo eilučių prekėms.

![E-komercijos išsiregistravimo puslapio pavyzdys, kuris apima laiko vietas paėmimo eilučių prekėms.](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a>Papildomi ištekliai

[Sukurti ir naujinti laiko vietas kliento paėmimu](dev-itpro/pickup-timeslots.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Užsakymo patvirtinimo modulis](order-confirmation-module.md)

[Išsamios užsakymo informacijos modulis](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]