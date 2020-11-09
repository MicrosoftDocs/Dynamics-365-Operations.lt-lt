---
title: Mokėjimo modulis
description: Ši tema paaiškina mokėjimo modulį ir tai, kaip jį sukonfigūruoti „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 894ac35973927c193d6e9c54e326daefb8a3f4a5
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055386"
---
# <a name="payment-module"></a>Mokėjimo modulis

[!include [banner](includes/banner.md)]

Ši tema paaiškina mokėjimo modulį ir tai, kaip jį sukonfigūruoti „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūra

Mokėjimo modulis leidžia klientui sumokėti už užsakymus naudojant kredito ar debeto korteles. Mokėjimo papildymas šiam moduliui yra pateiktas „Dynamics 365 Payment Connector“ „Adyen“. Dėl išsamesnės informacijos, kaip nustatyti ir konfigūruoti mokėjimo jungtį, žr. [„Dynamics 365 Payment Connector“ „Adyen“](dev-itpro/adyen-connector.md).

Mokėjimo modulis talpina mokėjimo informaciją, kuri yra laikoma per „Ayden“ HTML vidaus rėmuose (iframe). Mokėjimo modulis sąveikauja su „Commerce Scale Unit“ tam, kad gautų „Adyen“ mokėjimo informaciją. Kaip dalis sąveikos su „Commerce Scale Unit”, mokėjimo modulis gali leisti, kad sąskaitos adreso informacija būtų naudojama kaip „iframe“ arba atskiras modulis. „Fabrikam“ temoje mokėjimo adresas yra rodomas atskirame modulyje. Ši prieiga leidžia lanksčiau formatuoti, nes adreso eilutės gali būti sukurtos taip, kad atspindetų siuntimo adreso eilutes.

Mokėjimo modulis taip pat leidžia prisijungusiems klientams įrašyti jų mokėjimo informaciją. Mokėjimo informacija ir sąskaitų adresai yra įrašomi ir valdomi per „Adyen“ mokėjimo jungtį.

Mokėjimo modulis apima visus mokesčius, kurie nėra apimti lojalumo taškų ar dovanų kortelės. Jei bendra užsakymo suuma yra visiškai padengiama lojalumo taškais ar dovanų kortelės kreditu, mokėjimo modulis bus paslėptas ir klientas galės be jo pateikti užsakymą.

„Adyen“ mokėjimo jungtis taip pat palaiko stiprią kliento autentifikaciją (SCA). Europos Sąjungos (ES) mokėjimų paslaugų direktyvos 2.0 (PSD2.0) dalis reikalauja, kad interneto pirkėjai būtų autentifikuojami ne jų interneto apsipirkimo patirtyje jiems naudojant elektroninio apmokėjimo metodą. Išsiregistravimo srauto metu, klientai yra nukreipiama į jų banko svetainę. Tuomet, po autentifikavimo, jie yra nukreipiami atgal į prekybos išsiregistravimo srautą. Šio nukreipimo metu, informacija, kad klientas įvedė išsiregistravimo srautą (pavyzdžiui, siuntimo adresą, pristatymo parinktis, dovanų kortelės informaciją ir lojalumo informaciją) išliks. Prie jums įjungiant šią funkciją, mokėjimo jungtis turi būti sukonfigūruota SCA prekybos štabe. Dėl išsamesnės informacijos, žr. [Stipri kliento autentifikacija naudojant „Adyen“](adyen_redirect.md).

> [!NOTE]
> Naudojant „Adyen” mokėjimo jungtį, „iframe” modulis, esantis mokėjimo modulyje, gali būti atvaizduotas tik tada, jei įtraukiate „Adyen” URL į jūsų svetainės leidžiamų URL sąrašą. Norėdami atlikti šį veiksmą, įtraukite **\*.adyen.com** į jūsų svetainės turinio saugos strategijos direktyvas **child-src** , **connect-src** , **img-src** , **script-src** ir **style-src**. Daugiau informacijos, žr. [Turinio saugos strategijos valdymas](manage-csp.md). 

Tolesnis paveikslėlis rodo dovanų kortelės lojalumo taškų pavyzdį ir mokėjimo modulius išsiregistravimo puslapyje.

![Dovanų kortelės taškų pavyzdys ir mokėjimo moduliai užbaigimo puslapyje.](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a>Mokėjimo modulio ypatybės

| Ypatybės pavadinimas | Reikšmės | aprašymas |
|---------------|--------|-------------|
| Antraštė | Antraštės tekstas | Pasirenkama antraštė mokėjimo moduliui. |
| „iframe“ aukštis | Pikseliai | „iframe“ aukštis pikseliais. Aukštis gali būti reguliuojamas, kaip būtina. |
| Rodyti sąskaitų siuntimo adresą | **Teisinga** arba **Klaidinga** | Jei ši ypatybė yra nustatyta į **Teisingą** , mokėjimo adresas bus pateiktas „Adyen“ mokėjimo modulio „iframe“ viduje. Jei jis nustatytas į **Neteisingas** , mokėjimo adreso „Adyen“ neteiks ir prekybos vartotojas turės sukonfigūruoti modulį tam, kad rodytų mokėjimo adresą išsiregistravimo puslapyje. |
| Mokėjimo stiliaus nepaisymas | Kaskadinio stiliaus lapų (CSS) kodai | Kadangi mokėjimo modulis yra palaikomas „iframe“, esama apriboto stiliaus pajėgumo. Galite pasiekti tam tikrą stilių naudodami šią ypatybę. Vietos stiliaus viršijimui, turite įkelti CSS kodą kaip šios ypatybės vertę. Vietos kūrimo įrankis CSS viršija ir stiliai nėra taikomi šiam moduliui. |

## <a name="billing-address"></a>Sąskaitų siuntimo adresas

Mokėjimo modulis taip pat leidžia klientams pateikti sąskaitos adresą jų mokėjimo informacijai. Jis taip pat leidžia jiems naudoti jų siuntimo adresą kaip mokėjimo adresą siekiant supaprastinti ir pagreitinti išsiregistravimo srautą. Jei **Rodyti mokėjimo adresą** ypatybė yra nustatyta į **Netikrą** , mokėjimo modulis turi būti konfigūruotas išsiregistravimo puslapyje.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Įtraukite mokėjimo modulį į galutinį puslapį ir nustatykite reikiamas ypatybes

Mokėjimo modulis gali būti įtrauktas tik į galutinį modulį. Dėl išsamesnės informacijos apie tai, kaip konfigūruoti mokėjimo modulį išsiregistravimo puslapis, žr. [Galutinis modulis](add-checkout-module.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Krepšelio modulis](add-cart-module.md)

[Krepšelio piktogramos modulis](cart-icon-module.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Siuntimo adreso modulis](ship-address-module.md)

[Pristatymo parinkčių modulis](delivery-options-module.md)

[Išsamios užsakymo informacijos modulis](order-confirmation-module.md)

[Dovanų kortelės modulis](add-giftcard.md)

[„Dynamics 365“ mokėjimo jungtis, skirta sprendimui „Adyen“](dev-itpro/adyen-connector.md)

[Stipri kliento autentifikacija naudojant „Adyen“](adyen_redirect.md)
