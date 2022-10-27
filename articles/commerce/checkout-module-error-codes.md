---
title: Tikrinimo modulio klaidų nuorodų kodai
description: Šiame straipsnyje aprašomi tikrinimo modulio klaidų nuorodų kodai, rodomi vartotojo turimose klaidų pranešimuose Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 10/20/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: cd8269a71e56f23dbe3782ec3ffc69ec3ea6b151
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709377"
---
# <a name="checkout-module-error-reference-codes"></a>Tikrinimo modulio klaidų nuorodų kodai

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šiame straipsnyje aprašomi tikrinimo modulio klaidų kodai, rodomi vartotojo turimose klaidų pranešimuose Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce pateikė standartines klaidų nuorodas, kurias galima įtraukti į interneto kanalo tikrinimo klaidas, pateikiamas interneto klientams. "Commerce" 10.0.31 ir vėlesnėje versijoje tikrinimo modulyje rodomi klaidų pranešimai apima klaidų kodus ir nerodo nereikalingos informacijos tinklo klientui. Klaidų kodai nurodo klaidas, kurios išsamiai pateikiamos šiame straipsnyje.

Atsižvelgiant į klaidą, su kuriomis susidurta, šiame straipsnyje esančioje lentelėje pateikiama ši informacija:

- Sąlygos, dėl kurios įvyko klaida, aprašas arba papildoma informacija
- Informacija apie aplinkos arba mokėjimo jungties konfigūracijų apsaugą
- Informacija, kurią galima nurodyti palaikymo atveju, jei reikia papildomos pagalbos

## <a name="checkout-module-error-reference-codes"></a>Tikrinimo modulio klaidų nuorodų kodai

Norėdami gauti išsamesnės informacijos apie klaidų kodų nuorodas, kurias pateikė klientai arba kurios įvyko interneto parduotuvėje, naudokite šią lentelę.

| Klaidos kodas | Dynamics koreseliuojainės klaidos kodas | Klaidos aprašas |
| ---------- | ------------------------------ | ----------------- |
| CCR001     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ UnableToAuthorizePaymentCardTypeMissingOrNotSupported" | Nepavyko autorizuoti mokėjimo. Trūksta kortelės tipo **ID TokenizedPaymentCard** arba pateiktas kortelės tipo ID nepalaikomas. |
| CCR002     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ UnableToAuthorizePayment" | Sumažėjo. Nepavyko autorizuoti mokėjimo. |
| CCR003     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ UnableToAuthorizePaymentCardAdautionalContextRequired" | Nepavyko autorizuoti mokėjimo. Papildoma kliento reikalinga informacija. |
| CCR004     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ UnableToRetrieveCardPaymentAcceptResult" | Deja, kažkas negerai. Nepavyko gauti mokėjimo kortele priėmimo rezultato. Bandykite dar kartą arba kreipkitės į savo sistemos administratorių. |
| CCR005     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ PaymentRequiresMerchantProperties" | Nepavyko atlikti mokėjimo dėl trūkstamų prekybininko mokėjimo ypatybės. Kreipkitės į savo sistemos administratorių. |
| CCR006     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ InvalidPaymentRequest" | Nepavyko nuskaityti operacijos mokėjimo priemonės tarnybos. Patikrinkite pasirinkto mokėjimo priemonės tipo mokėjimo būdo nustatymą. |
| CCR007     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ MultipleCustomerAccountPaymentsNotAllowed" | Kliento sąskaitos mokėjimas jau pritaikytas. Leidžiamas tik vienas vienos operacijos mokėjimas. |
| CCR008     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ CustomerAccountLimitSignDifferentFromAmountDue" | Kliento sąskaitos limitas skiriasi nuo mokėtinos sumos. Pabandykite naudoti kitą mokėjimo būdą arba pagalbos kreipkitės į klientų aptarnavimo tarnybą. |
| CCR009     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ CustomerAccountPaymentExceedsTotalAmountForCarryOutAndReturnItems" | Kliento sąskaitos mokėjimas viršija bendrą už išvardytas prekes mokėtiną sumą. Bandykite dar kartą arba pagalbos kreipkitės į klientų aptarnavimo tarnybą. |
| CCR010     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ PaymentUsingUnauthorizedAccount" | Kliento sąskaitos mokėjimui reikia savo sąskaitos arba sutampančios SF sąskaitos mokėjimo priemonės eilutėje. |
| CCR011     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ CustomerAccountPaymentExceedsCustomerAccountFloorLimit" | Šiuo metu nepavyksta apdoroti kliento sąskaitos mokėjimo – viršyta apatinės ribos vertė. |
| CCR012     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ CustomerAccountPaymentForCustomerWithoutAllowOnAccount" | Šiam klientui neleidžiama apmokėti pagal sąskaitą. |
| CCR013     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ UnableToCancelPayment" | Deja, kažkas negerai. Nepavyko atšaukti mokėjimo. Pabandyk dar kartą. |
| CCR014     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ UnableToReadCardTokenInfo" | Apdorojant mokėjimą įvyko klaida. Bandykite dar kartą vėliau. |
| CCR015     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ NotEnoughRewardPoints" | Lojalumo mokėjimo suma viršija šioje operacijoje naudojamos lojalumo kortelės leistiną sumą. |
| CCR016     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ RefundAmountMoreThanAllowed" | Lojalumo grąžinimo suma viršija šioje operacijoje naudojamos lojalumo kortelės leistiną sumą. |
| CCR017     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ InvalidLoyaltyCardNumber" | Nerastas lojalumo kortelės numeris. Suaktyvinkite lojalumo kortelės numerį arba įveskite kitą kortelės numerį ir bandykite dar kartą. |
| CCR018     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ BlockedLoyaltyCard" | Šio lojalumo kortelės numerio naudoti negalima. Įveskite kitą kortelės numerį ir bandykite dar kartą. |
| CCR019     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ NoTenderLoyaltyCard" | Ši lojalumo kortelė neatitinka šios operacijos lojalumo taškų. |
| CCR020     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ GiftCardCurrencyMismatch" | Įvyko dovanų kortelės numerio klaida. Bandykite naudoti kitą dovanų kortelę arba pagalbos kreipkitės į klientų aptarnavimo tarnybą. |
| CCR021     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ PaymentAmountExceedsGiftBalance" | Suma viršija dovanų kortelės sumą. Įveskite kitą sumą ir bandykite dar kartą. |
| CCR022     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ NoMoreThanOneLoyaltyTender" | Operacijoje negali būti kelių lojalumo mokėjimo eilučių. |
| CCR023     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ PaymentAlreadyVoided" | Trūksta mokėjimo informacijos arba ji neteisinga. Patikrinkite mokėjimo informaciją ir bandykite dar kartą. |
| CCR024     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ FraudRisk" | Šiuo metu užsakymo apdoroti negalima. Bandykite dar kartą vėliau. |
| CCR025     | Fronto pabaigos skirtasis laikas, skirtas API išregistravimas | Pabaigtos operacijos skirtasis laikas. Patvirtinkite, ar užsakymas apdorotas būstinėje Dynamics 365 Commerce. |
| CCR026     | Originali įgaliota suma pakeista | Užsakymo suma pasikeitė iš pradinės autorizavimo sumos, apdorotos naudojant mokėjimo šliuzą. Tai gali būti dėl kupono, akcijos arba pardavimo termino pabaigos. |
| CCR027     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ InvalidCartVersion" | Apdorojant mokėjimą įvyko klaida. Į krepšelio API pateikta nuoroda turi kitokią nuorodą nei tikėtasi (atmesdama galimą nenuoseklumą tikrinimo proceso metu). |
| CCR028     | "Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ MissingRequiredCartTenderLines" | Bandant naudoti mokėjimo būdą įvyko klaida. Susisiekite su palaikymo tarnyba, norėdami peržiūrėti savo sąskaitos parametrus arba bandyti dar kartą, naudodami kitą mokėjimo būdą. |

## <a name="additional-resources"></a>Papildomi ištekliai

[DUK apie mokėjimus](dev-itpro/payments-retail.md)

[Pirkimo užbaigimo modulį](add-checkout-module.md)

[Mokėjimo modulis](payment-module.md)
