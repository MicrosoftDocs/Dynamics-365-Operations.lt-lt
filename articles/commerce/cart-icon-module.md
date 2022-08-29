---
title: Krepšelio piktogramos modulis
description: Šiame straipsnyje aprašomas krepšelio piktogramos modulis ir aprašoma, kaip įtraukti jį į svetainės puslapius Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: e35b0ee5341b8b5531ad2c80c868ca4c07ebd315
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280508"
---
# <a name="cart-icon-module"></a>Krepšelio piktogramos modulis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomas krepšelio piktogramos modulis ir aprašoma, kaip įtraukti jį į svetainės puslapius Microsoft Dynamics 365 Commerce.

Krepšelio piktogramos modulis nurodo krepšelį puslapio antraštės modulyje esantį krepšelį ir krepšelyje esančių prekių skaičių. Krepšelio piktogramos modulis taip pat nurodo ir krepšelio suvestinę (dar vadinamą mažuoju krepšeliu), kai pelės žymiklis užvestas virš krepšelio piktogramos. Mažasis krepšelis suteikia vartotojui krepšelyje esančių prekių suvestinę ir nereikia pereiti į krepšelio puslapį. Be to, jis taip pat leidžia vartotojui tiesiogiai pereiti prie pirkimo užbaigimo puslapio, jei jis patenkintas suvestine. Tai sumažina naršymo puslapių skaičių ir leidžia greičiau užbaigti pirkimą. 

Toliau pateiktame vaizde parodytas krepšelio piktogramos modulio, kuris rodo mažąjį krepšelį „Fabrikam“ antraštėje, pavyzdys.

![Krepšelio piktogramos modulio pavyzdys.](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Modulio ypatybės

- **Rodyti mažąjį krepšelį** – kai ši ypatybė yra nustatyta į **Teisingą**, krepšelio suvestinės (mažojo krepšelio) rodymas užvedus pelės žymiklį virš krepšelio piktogramos. Ši funkcija palaikoma tik darbalaukio rodinio prievaduose.
- **Leisti anoniminį tikrintoją** - ai ši ypatybė nustatyta kaip **Teisinga** mažame krepšelyje leidžiama vartotojams, kurie prisiregistravo, kad galėtų išregistruoti svečią. Ši ypatybė galima „Commerce" 10.0.21 versijoje, kaip „Commerce" modulio bibliotekos paketo dalis.
- **Prekių užsakymas** – ši ypatybė valdo tvarką, kuria prekės turėtų būti rodomos mažame krepšelyje. Kai pasirenkama pasirinktis **Nauja prekė, įtraukta į sąrašo viršų** į krepšelį įdėjus naujos prekės rodomos mažam krepšelio prekių sąrašui viršuje. Kai pasirenkama numatyta parinktis, **Nauja prekė, įtraukta į sąrašo viršų** ,į krepšelį įdėjus naujos prekės rodomos mažam krepšelio prekių sąrašui apačioje. Ši ypatybė galima „Commerce" 10.0.21 versijoje, kaip „Commerce" modulio bibliotekos paketo dalis.

> [!IMPORTANT]
> Ypatybės **Leisti anoniminį išsiregistravimą** ir **Prekių užsakymą** yra prieinamos „Commerce“ versijoje 10.0.21 leidime. Tam reikia, kad būtų įdiegta „Commerce“ modulio bibliotekos paketo versija 9.31.

## <a name="module-properties-and-slots-in-the-adventure-works-theme"></a>Modulio ypatybės ir vietos „Adventure Works” temoje

„Adventure Works” temoje krepšelio piktogramos modulyje yra dvi papildomos, mažam krepšeliui skirtos vietos. Šios vietos įtrauktos kaip modulio apibrėžimo plėtinys.

- **Tuščio krepšelio akcijos** – šiai vietai reikia turinio blokavimo modulio. Kai krepšelis tuščias, rodomas nurodytas turinio blokavimo modulis. Turinio blokavimo modulis gali būti naudojamas reklamoms, rinkodaros turiniui ir saitams į kategorijų puslapius, kad padėtų klientams tęsti jų apsipirkimą.
- **Reklaminis turinys** – šią vietą galima rodyti akcijoms, pavyzdžiui, „Nemokamas siuntimas užsakymams, kurių vertė didesnį nei $100.” Turinio blokavimo, teksto blokavimo ir vaizdų sąrašo modulius galima naudoti reklamuojamo turinio vietos segmente.

Šiame paveikslėlyje pateikiamas krepšelio piktogramos modulio pavyzdys „Adventure Works” temoje, kurioje reklaminis turinys rodomas mažame krepšelyje.

![Krepšelio piktogramos modulio pavyzdys „Adventure Works” temoje](./media/AW_minicart.PNG)

> [!IMPORTANT]
> „Adventure Works” temos vietos galimos kaip 10.0.20 „Dynamics 365 Commerce” versijos leidimas.

## <a name="add-a-cart-icon-module-to-a-page"></a>Krepšelio piktogramos modulio įtraukimas į puslapį

Norėdami įtraukti krepšelio piktogramos modulį, žr. [Antraštės modulis](author-header-module.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Krepšelio modulis](add-cart-module.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Mokėjimo modulis](payment-module.md)

[Siuntimo adreso modulis](ship-address-module.md)

[Pristatymo parinkčių modulis](delivery-options-module.md)

[Paėmimo informacijos modulis](pickup-info-module.md)

[Išsamios užsakymo informacijos modulis](order-confirmation-module.md)

[Dovanų kortelės modulis](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
