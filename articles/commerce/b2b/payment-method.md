---
title: Konfigūruoti kliento sąskaitos mokėjimo metodą B2B el. komercijos saitams
description: Ši tema aprašo, kaip konfigūruoti kliento sąskaitos mokėjimo metodą verslo su verslu (B2B) el. komercijos saitams.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 82dfd6ac7e97d838ef442fd6ded4a4f165fc795b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211206"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>Konfigūruoti kliento sąskaitos mokėjimo metodą B2B el. komercijos saitams

[!include [banner](../../includes/banner.md)]

Ši tema aprašo, kaip konfigūruoti kliento sąskaitos mokėjimo metodą verslo su verslu (B2B) el. komercijos saitams.

Mažmeniniai prekybininkai gali priimti įvairius mokėjimo tipus vietoje produktų ir paslaugų, kuriuos jie parduoda el. komercijos kanale. Nustačius sistemą, „Microsoft Dynamics 365 Commerce“ reikia sukonfigūruoti kiekvieną mokėjimo tipą, kurį pardavėjas priima. Kliento sąskaitos (ar „sąskaitoje“) mokėjimo metodas turi būti palaikomas B2B el. komercijos saituose. 

## <a name="prerequisites"></a>Būtinieji komponentai

1. Įtraukite kliento sąskaitos mokėjimo metodą į „Commerce“ būstinę.
2. Susiekite kliento sąskaitos mokėjimo metodą su el. komercijos kanalu.
3. Įsitikinkite, kad **Leisti sąskaitoje** yra įjungtas klientui **Mažmeninė prekybą ir komercija \> Klientai \> Visi klientai \> Numatyti mokėjimai** „Commerce“ būstinėje. Taip pat, įsitikinkite, kad **Kredito limito** parametrai yra nustatyti tinkamai klientams **Mažmeninė prekyba ir komercija \> Klientai \> Visi klientai \> Kreditas ir kolekcijos** „Commerce“ būstinėje. 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>Įjunkite kliento sąskaitos mokėjimo metodą „Commerce“ vietos kūrimo įrankyje 

Norėdami įjungti kliento sąskaitos mokėjimo metodą „Commerce“ saito kūrimo įrankyje, vadovaukitės šiais žingsniais.

1. Eikite į **Saito nustatymai \> Plėtiniai**.
1. Nustatykite **Įjungti kliento sąskaitos mokėjimus** ypatybę į **Įjungti B2B klientams**. 
1. Pasirinkite **Įrašyti ir publikuoti**.

> [!NOTE]
> Nauji saito nustatymai įsigalioja tik atnaujinus app.settings.json failą. Dėl daugiau informacijos, žr. [SDK ir modulio bibliotekos naujinimai](../e-commerce-extensibility/sdk-updates.md).

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>Įjunkite kliento sąskaitos mokėjimo metodą išsiregistravimo puslapyje B2B el. komercijos saite

Norėdami įjungti kliento sąskaitos mokėjimo metodą išsiregistravimo puslapyje B2B el. komercijos saite, atlikite šiuos žingsnius.

1. „Commerce“ saito kūrimo įrankyje, suraskite ir redaguokite išsiregistravimo puslapį ar fragmentą, kuriame yra išsiregistravimo modulis B2B el. komercijos saite.
1. Vietoje **Išsiregistravimo sektoriaus konteineris** rinkitės **Įtraukti modulį** ir tuomet įtraukite **Kliento sąskaitos mokėjimas** modulį.
1. Padėkite **Kliento sąskaitos mokėjimas** modulį pasirinkę daugtaškį (**...**) ir tuomet pasirinkę **Eiti aukštyn** ar **Eiti žemyn** kaip būtina.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>Patvirtinkite, kad kliento sąskaitos sumokėjimo metodas buvo įjungtas ir publikuotas

Norėdami patvirtinti, kad kliento sąskaitos sumokėjimo metodas buvo įjungtas ir publikuotas, atlikite šiuos veiksmus.

1. Prisijunkite prie el. komercijos saito.
1. Įtraukite prekę į vežimėlį.
1. Eikite į išsiregistravimo puslapį. Turėtumėte matyti naują **Kliento sąskaitos** mokėjimo metodą.

## <a name="additional-resources"></a>Papildomi ištekliai

[Nustatykite B2B el. komercijos saitą](set-up-b2b-site.md)

[Kurkite organizacijos modeliavimo hierarchijas B2B organizacijoms](org-model.md)

[Valdykite verslo partnerio vartotojus B2B el. komercijos saituose](manage-b2b-users.md)

[Nustatykite produkto kiekio apribojimus B2B el. komercijos saitams](quantity-limits.md)

[SDK ir Modulio biliotekos naujinimai](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]