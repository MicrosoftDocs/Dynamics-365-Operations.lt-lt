---
title: Siuntimo adreso modulis
description: Šiame straipsnyje aprašomas siuntimo adresų modulis ir paaiškinama, kaip jį konfigūruoti Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e30e639b7ba1c0caaf72fa66d13f80d04c2e861c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882201"
---
# <a name="shipping-address-module"></a>Siuntimo adreso modulis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomas siuntimo adresų modulis ir paaiškinama, kaip jį konfigūruoti Microsoft Dynamics 365 Commerce.

Siuntimo adreso modulis leidžia klientams įtraukti ar pasirinkti siuntimo adresą užsakymui išsiregistravimo srauto metu. Jei klientas yra prisijungęs, visi anksčiau tam klientui įrašyti adresai bus rodomi, o klientas galės iš jų pasirinkti. Klientas taip pat gali įtraukti naują adresą. Siuntimo adreso modulis yra naudojamas visoms užsakymo prekėms, kuriems reikalingas siuntimas.

Siuntimo adreso formatai gali būti nustatyti komercijos štabe kiekvienai šaliai ar regionui, o siuntimo adreso modulis tuomet įjungia valstybei/regionui priklausančias taisykles.

Kai klientai įveda siuntimo adresą išsiregistravimo sraute, jie turi pasirinkimą įrašyti adresą kaip pirminį. Ši parinktis rodoma tik klientui prisijungus.

Nepaisant to, kad siuntimo adreso modulis neleidžia patvirtinti adreso, ši funkcija gali būti įgyvendinta tinkinimo metu.

Tolesnis paveikslėlis rodo naujo siuntimo adreso modulio pavyzdį išsiregistravimo puslapyje.

![Siuntimo adreso pavyzdžio modulis išsiregistravimo puslapyje.](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>Modulio ypatybės

| Ypatybės pavadinimas | Reikšmės | Aprašas |
|---------------|--------|-------------|
| Antraštė | Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** ar **H6**) | Pasirenkama antraštė siuntimo adreso moduliui. |
| Rodyti adreso tipą | **Teisinga** arba **Klaidinga** | Jei šios pasirenkamos ypatybės yra nustatytos į **Teisingos**, bus rodomas adreso tipas, toks kaip **Namų** ar **Įmonės**. Jei nėra nurodyta jokio adreso tipo, adresas automatiškai bus įrašomas kaip **Tipas**=**Kitas**. |
| Įjungti automatinį pasiūlymą| **Teisinga** arba **Klaidinga** | Jei ši pasirinktinė ypatybė nustatyta į **Teisinga**, bus pateikiami automatiniai adreso pasiūlymai. Šiuos pasiūlymus teikia „Bing” žemėlapiai. Daugiau informacijos, kaip nustatyti „Bing” žemėlapių integravimą jūsų svetainėje, žr. [Parduotuvės išrinkiklio modulis](store-selector.md). Ši funkcija yra prieinama „Commerce“ versijos 10.0.15 leidime.|
|Automatinio pasiūlymo parinktys| Skaičius| Jei automatiniai adreso pasiūlymai įgalinti, galite nurodyti papildomas parinktis, pvz., didžiausią pasiūlymų, kuriuos reikia pateikti, skaičių.|

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

[Parduotuvės išrinkiklio modulis](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]