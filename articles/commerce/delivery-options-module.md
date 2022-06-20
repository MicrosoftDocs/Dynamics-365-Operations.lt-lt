---
title: Pristatymo parinkčių modulis
description: Šiame straipsnyje aprašomi pristatymo pasirinkčių moduliai ir paaiškinama, kaip juos konfigūruoti Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 02/24/2022
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
ms.openlocfilehash: 554a17cf1c90f7fdaa20de74c3f6726910ab815d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894563"
---
# <a name="delivery-options-module"></a>Pristatymo parinkčių modulis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomi pristatymo pasirinkčių moduliai ir paaiškinama, kaip juos konfigūruoti Microsoft Dynamics 365 Commerce.

Pristatymo parinkčių moduliai leidžia klientams pasirinkti pristatymo būdą, tokį kaip siuntimas ar paėmimas pagal jų interneto užsakymą. Siuntimo adresas būtinas siekiant nustatyti pristatymo būdą. Jei siuntimo adresas pasikeitė, pristatymo parinktys turi būti dar kartą gautos. Jei užsakyme yra tik prekės pakuojamos parduotuvėje, šis modulis yra automatiškai paslepiamas.

Dėl informacijos apie tai, kaip sukonfigūruoti pristatymo būdus, žr. [Interneto kanalo nustatymai](channel-setup-online.md) ir [Pristatymo būdų nustatymas](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Visi pristatymo būdai gali turėti susietą mokestį. Dėl išsamesnės informacijos apie tai, kaip konfigūruoti mokesčius interneto parduotuvėje, žr. [Omni kanalo papildomi automatiniai mokesčiai](omni-auto-charges.md).

10.0.13 komercijos versijoje pristatymo parinkčių modulis buvo atnaujintas taip, kad palaikytų **Antraštės mokesčiai be paskirstymo** ir **Siuntimas kaip eilutės mokestis** funkcijas. Jei paskirstymas yra išjungtas, tikimasi, kad el. prekybos darbo srautas neleis maišyti pristatymo būdo prekėms vežimėlyje (tai yra, kai kurios prekės yra pasirinktos siuntimui, tačiau kitos yra pasirinktos paėmimui). **Antraštės mokesčio paskirstymo** funkcija reikalauja, kad **Nuolatinio pristatymo būdo tvarkymo kanale įjungimas** vėliava būtų įjungta prekybos štabe. Kai vėliavos funkcija yra įjungta, siuntimo mokesčiai bus taikomi antraštės lygmeniu ar eilutės lygmeniu priklausomai nuo „Commerce“ štabo konfigūravimo.

„Fabrikam“ tema palaiko maišytą pristatymo būdą, kai kai kurios prekės yra parinktos siuntimui, o kitos parinktos paėmimui. Šiame būde, siuntimo mokesčiai bus paskirstyti visoms prekėms, kurios yra parinktos siuntimo pristatymo būdui. Maišytam pristatymo į darbą būdui, pirmiausia turite sukonfigūruoti **Antraštės mokesčiai su paskirstymu** funkciją komercijos štabe. Dėl platesnės informacijos apie šį konfigūravimą, žr. [Atidėti antraštės mokesčius atitikimui su prekybos eilutėmis](pro-rate-charges-matching-lines.md).

Jei siuntimo mokesčiai taikomi eilutės prekėms, jos gali būti rodomos kiekvienos prekės vežimėlio eilutėje. Ši funkcija reikalauja, kad **Rodyti siuntimo mokesčius eilutės prekei** ypatybė būtų įjungti tiek vežimėlio moduliui tik ir galutiniam moduliui. Dėl platesnės informacijos, žr. [Vežimėlio modulis](add-cart-module.md) ir [Galutinis modulis](add-checkout-module.md).

Tolesnis paveikslėlis rodo pristatymo parinkčių modulį galutiniame puslapyje pavyzdį.

![Pristatymo parinkčių modulio galutiniame puslapyje pavyzdys.](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a>Pristatymo parinkčių modulio ypatybės

| Ypatybė | Reikšmės | Aprašas |
|----------|--------|-------------|
| Antraštė | Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** ar **H6**) | Pasirenkama antraštė pristatymo parinkčių moduliui. |
| Pasirinktinis CSS klasės pavadinimas | Tekstas | Tinkinto kaskadinio stiliaus lapų (CSS) klasės pavadinimas, kuris bus naudojamas šio modulio sukūrimui, jei taikomas. |
| Pristatymo būdo filtro parinktis | **Nefiltruoti** ar **Nesiųsti būdai** | Vertė, kuri nurodo, ar pristatymo parinkčių modulis turėtų filtruoti visus nesiunčiamus pristatymo būdus. |
| Automatiškai pasirinkti pristatymo pasirinktį | **Nefiltruoti** , **automatiškai pasirinkti pristatymo parinktį, rodyti suvestinę** arba automatiškai pasirinkti pristatymo parinktį ir **nerodyti suvestinės** | Ši ypatybė automatiškai pritaiko pirmą galima pristatymo pasirinktį patikrinti nereikalaujant, kad vartotojas ją pasirinktų. Jis turėtų būti naudojamas tik tada, jei yra viena galima pristatymo pasirinktis. Ši ypatybė yra palaikoma nuo „Commerce“ versijos 10.0.19 leidimo. |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a>Įtraukite pristatymo parinkčių modulį į galutinį puslapį ir nustatykite reikiamas ypatybes

Pristatymo parinkčių modulis gali būti įtrauktas tik į galutinį modulį. Dėl išsamesnės informacijos apie tai, kaip konfigūruoti pristatymo parinkčių modulį ir įtraukti jį į galutinį puslapį, žr. [Galutinis modulis](add-checkout-module.md).

> [!NOTE]
> Gali kilti nenuoseklaus pristatymo tvarkymo veiksmų arba el. komercijos kanale gali būti nematuotų antraštės lygio išlaidų. Informacijos, kaip išspręsti šias problemas, ieškokite Įgalinti nuoseklų [pristatymo režimo tvarkymą el. komercijos kanaluose](consistent-delivery-mode-handling.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Krepšelio modulis](add-cart-module.md)

[Pirkimo užbaigimo modulį](add-checkout-module.md)

[Mokėjimo modulis](payment-module.md)

[Siuntimo adreso modulis](ship-address-module.md)

[Paėmimo informacijos modulis](pickup-info-module.md)

[Išsamios užsakymo informacijos modulis](order-confirmation-module.md)

[Dovanų kortelės modulis](add-giftcard.md)

[Interneto kanalo nustatymas](channel-setup-online.md)

[Omni kanalo papildomi automatiniai mokesčiai](omni-auto-charges.md)

[Paskirstyti antraštės mokesčius tam, kad jie atitiktų prekybos eilutes](pro-rate-charges-matching-lines.md)

[Nustatyti pristatymo būdus](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
