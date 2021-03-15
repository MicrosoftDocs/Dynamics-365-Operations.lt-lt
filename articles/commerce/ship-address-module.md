---
title: Siuntimo adreso modulis
description: Ši tema paaiškina siuntimo adreso modulį ir tai, kaip jį sukonfigūruoti „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6a5eb69c7746be419779b1a844ee35ec375a324c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985641"
---
# <a name="shipping-address-module"></a>Siuntimo adreso modulis

[!include [banner](includes/banner.md)]

Ši tema aprašo siuntimo adreso modulį ir tai, kaip jį sukonfigūruoti „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūra

Siuntimo adreso modulis leidžia klientams įtraukti ar pasirinkti siuntimo adresą užsakymui išsiregistravimo srauto metu. Jei klientas yra prisijungęs, visi anksčiau tam klientui įrašyti adresai bus rodomi, o klientas galės iš jų pasirinkti. Klientas taip pat gali įtraukti naują adresą. Siuntimo adreso modulis yra naudojamas visoms užsakymo prekėms, kuriems reikalingas siuntimas.

Siuntimo adreso formatai gali būti nustatyti komercijos štabe kiekvienai šaliai ar regionui, o siuntimo adreso modulis tuomet įjungia valstybei/regionui priklausančias taisykles.

Kai klientai įveda siuntimo adresą išsiregistravimo sraute, jie turi pasirinkimą įrašyti adresą kaip pirminį. Ši parinktis rodoma tik klientui prisijungus.

Nepaisant to, kad siuntimo adreso modulis neleidžia patvirtinti adreso, ši funkcija gali būti įgyvendinta tinkinimo metu.

Tolesnis paveikslėlis rodo naujo siuntimo adreso modulio pavyzdį išsiregistravimo puslapyje.

![Siuntimo adreso pavyzdžio modulis išsiregistravimo puslapyje](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>Modulio ypatybės

| Ypatybės pavadinimas | Reikšmės | aprašymas |
|---------------|--------|-------------|
| Antraštė | Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** ar **H6**) | Pasirenkama antraštė siuntimo adreso moduliui. |
| Rodyti adreso tipą | **Teisinga** arba **Klaidinga** | Jei šios pasirenkamos ypatybės yra nustatytos į **Teisingos**, bus rodomas adreso tipas, toks kaip **Namų** ar **Įmonės**. Jei nėra nurodyta jokio adreso tipo, adresas automatiškai bus įrašomas kaip **Tipas**=**Kitas**. |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a>Įtraukite siuntimo adreso modulį į galutinį puslapį ir nustatykite reikiamas ypatybes

Siuntimo adreso modulis gali būti įtrauktas tik į galutinį modulį. Dėl išsamesnės informacijos apie tai, kaip konfigūruoti siuntimo adreso modulį ir įtraukti jį į galutinį puslapį, žr. [Galutinis modulis](add-checkout-module.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Krepšelio modulis](add-cart-module.md)

[Krepšelio piktogramos modulis](cart-icon-module.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Mokėjimo modulis](payment-module.md)

[Pristatymo parinkčių modulis](delivery-options-module.md)

[Paėmimo informacijos modulis](pickup-info-module.md)

[Išsamios užsakymo informacijos modulis](order-confirmation-module.md)

[Dovanų kortelės modulis](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]