---
title: Mokėjimo modulis
description: Ši tema paaiškina mokėjimo modulį ir tai, kaip jį sukonfigūruoti „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 11/18/2020
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: d9c0956e30d413f5ae695cf75b06fb58711b2944
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222502"
---
# <a name="payment-module"></a>Mokėjimo modulis

[!include [banner](includes/banner.md)]

Ši tema paaiškina mokėjimo modulį ir tai, kaip jį sukonfigūruoti „Microsoft Dynamics 365 Commerce“.

Mokėjimo modulis leidžia klientui sumokėti už užsakymus naudojant kredito ar debeto korteles. Mokėjimo papildymas šiam moduliui yra pateiktas „Dynamics 365 Payment Connector“ „Adyen“. Dėl išsamesnės informacijos, kaip nustatyti ir konfigūruoti mokėjimo jungtį, žr. [„Dynamics 365 Payment Connector“ „Adyen“](dev-itpro/adyen-connector.md).  

„Commerce“ versijoje 10.0.14, mokėjimo modulsi taip pat buvo integruotas su „Dynamics 365 Payment Connector“ skirtu „PayPal“ tam, kad leistų klientams sumokėti už užsakymus su „PayPal“. Dėl išsamesnės informacijos, kaip nustatyti ir konfigūruoti „Dynamics 365 Payment Connector“ skirtą „PayPal“, žr. [„Dynamics 365 Payment Connector“ skirtą „PayPal“](paypal.md). 

## <a name="dynamics-365-payment-connector-for-adyen"></a>„Dynamics 365“ mokėjimo jungtis, skirta sprendimui „Adyen“ 

Mokėjimo modulis talpina mokėjimo informaciją, kuri yra laikoma per „Ayden“ HTML vidaus rėmuose (iframe). Mokėjimo modulis sąveikauja su „Commerce Scale Unit“ tam, kad gautų „Adyen“ mokėjimo informaciją. Kaip „Commerce Scale Unit“ sąveikos dalis, mokėjimo modulis gali leisti mokėjimo adreso informaciją pateikti per „iframe“ per „Adyen“ ar kaip atskirą modulį. „Fabrikam“ temoje, mokėjimo adresas yra įjungtas kaip atskiras modulis. Ši prieiga leidžia lanksčiau formatuoti, nes adreso eilutės gali būti sukurtos taip, kad atspindetų siuntimo adreso eilutes.

Mokėjimo modulis taip pat leidžia prisijungusiems klientams įrašyti jų mokėjimo informaciją. Mokėjimo informacija ir sąskaitų adresai yra įrašomi ir valdomi per „Adyen“ mokėjimo jungtį.

Mokėjimo modulis apima visus mokesčius, kurie nėra apimti lojalumo taškų ar dovanų kortelės. Jei bendra užsakymo suuma yra visiškai padengiama lojalumo taškais ar dovanų kortelės kreditu, mokėjimo modulis bus paslėptas ir klientas galės be jo pateikti užsakymą.

„Adyen“ mokėjimo jungtis taip pat palaiko stiprią kliento autentifikaciją (SCA). Europos Sąjungos (ES) Peržiūrėtų mokėjimų paslaugų direktyvos (PSD2) dalis numato, kad internetiniai pirkėjai būtų atpažinti ne jų internetinėje apsiprekinimo patirtyje jiems naudojant elektroninį apmokėjimo būdą. Išsiregsitravimo eigos metu, klientai yra nukreipiami į jų banko puslapį ir ten autentifikuojami bei nukreipiami atgal į „Commerce“ išregistravimo eigą. Tokio nukreipimo metu, informacija, kurią klientas įvedė išsiregsitravimo eigos metu (pavyzdžiui, pristatymo adresas, pristatymo parinktys, dovanų kortelės informacija ir lojalumo informacija) išliks. Prieš jums įjungiant „Adyen“ mokėjimo jungties funkciją, mokėjimo jungtis turi būti konfigūruota SCA „Commerce“ štabe. Dėl išsamesnės informacijos, žr. [Stipri kliento autentifikacija naudojant „Adyen“](adyen_redirect.md). Ši funkcija buvo įjungta „Commerce“ versijoje 10.0.12.

> [!NOTE]
> Naudojant „Adyen” mokėjimo jungtį, „iframe” modulis, esantis mokėjimo modulyje, gali būti atvaizduotas tik tada, jei įtraukiate „Adyen” URL į jūsų svetainės leidžiamų URL sąrašą. Norėdami atlikti šį veiksmą, įtraukite **\*.adyen.com** į jūsų svetainės turinio saugos strategijos direktyvas **child-src**, **connect-src**, **img-src**, **script-src** ir **style-src**. Daugiau informacijos, žr. [Turinio saugos strategijos valdymas](manage-csp.md). 

Tolesnis paveikslėlis rodo dovanų kortelės pavyzdė ir „Adyen“ apmokėjimo modulius išsiregistravimo puslapyje.

![Dovanų kortelės pavyzdys ir „Adyen“ apmokėjimo modulius išsiregistravimo puslapyje](./media/ecommerce-payments.PNG)

## <a name="dynamics-365-payment-connector-for-paypal"></a>„Dynamics 365 Payment Connector“ skirtas „PayPal“

„Commerce“ versijoje 10.0.14, mokėjimo modulsi taip pat buvo integruotas su „Dynamics 365 Payment Connector“ skirtu „PayPal“. Dėl išsamesnės informacijos apie tai, kaip nustatyti ir konfigūruoti šią mokėjimo jungtį, žr. [„Dynamics 365 Payment Connector“ skirtą „PayPal“](paypal.md).
 
Išsiregistravimo puslapyje galite turėti tiek „Adyen“, tiek ir „PayPal“ sukonfigūruotas jungtis. Apmokėjimo modulis bus papildytas papildomomis ypatybėmis, kad jos padėtų nustatyti, kuri jungtis turi veikti su kuria. Dėl išsamios informacijos, žr. **Palaikomi nuomotojo tipai** ir **Yra pirminis mokėjimas** modulio ypatybes tolesnėje lentelėje.
  
Kai apmokėjimo modulis yra konfigūruotas siekiant naudoti „PayPal“ mokėjimo jungtį, „PayPal“ mygtukas pasirodo išsiregistravimo puslapyje. Kai klientas jį pasirenka, mokėjimo modulis apima „iframe“ su „Paypal“ informacija. Klientas gali prisijungti ir pateikti savo „Paypal“ informaciją esančią „iframe“, kad baigtų savo perlaidą. Kai klientas pasirenka sumokėti su „PayPal“, likęs likutis užsakyme bus nuskaičiuotas per „PayPal“.

„PayPal“ mokėjimo jungčiai nereikia mokėjimo adreso modulio, nes visa su mokėjimu susijusi informacija tvarkoma „Paypal“ per „iframe“. Nepaisant to, siuntimo adresas ir pristatymo parinkčių moduliai yra būtini.

Tolesnis paveikslėlis rodo dviejų mokėjimo modulių pavyzdį išsiregistravimo puslapyje, vienas kurių sukonfigūruotas su „Adyen“ mokėjimo jungtimi, o kitas su „Paypal“ mokėjimo jungtimi.
![„Adyen“ mokėjimo ir „Paypal“ modulių pavyzdys išsiregistravimo puslapyje](./media/ecommerce-paypal.png)

Tolesnis paveikslėlis rodo „PayPal“ „iframe“ pavyzdį, kuris naudojamas „PayPal“ mygtuku. 
![„Paypal“ „iframe“ išsiregistravimo puslapio pavyzdys](./media/ecommerce-paypal-iframe.png)

## <a name="payment-module-properties"></a>Mokėjimo modulio ypatybės

| Ypatybės pavadinimas | Reikšmės | aprašymas |
|---------------|--------|-------------|
| Antraštė | Antraštės tekstas | Pasirenkama antraštė mokėjimo moduliui. |
| „iframe“ aukštis | Pikseliai | „iframe“ aukštis pikseliais. Aukštis gali būti reguliuojamas, kaip būtina. |
| Rodyti sąskaitų siuntimo adresą | **Teisinga** arba **Klaidinga** | Jei ši ypatybė yra nustatyta į **Teisingą**, mokėjimo adresas bus pateiktas „Adyen“ mokėjimo modulio „iframe“ viduje. Jei nustatytas į **Netikras**, mokėjimo adresas nebus rodomas „Adyen“, o „Commerce“ vartotojas turės sukonfigūruoti modulį taip, kad jame būtų mokėjimo informacija išsiregistravimo puslapyje. „PayPal“ mokėjimo jungtyje, šis laukelis neturi jokio poveikio, nes mokėjimo adresą visiškai valdo „PayPal“. |
| Mokėjimo stiliaus nepaisymas | Kaskadinio stiliaus lapų (CSS) kodai | Kadangi mokėjimo modulis yra palaikomas „iframe“, esama apriboto stiliaus pajėgumo. Galite pasiekti tam tikrą stilių naudodami šią ypatybę. Vietos stiliaus viršijimui, turite įkelti CSS kodą kaip šios ypatybės vertę. Vietos kūrimo įrankis CSS viršija ir stiliai nėra taikomi šiam moduliui. |
|Palaikomi mokėjimo priemonių tipai| Eilutė| Jei konfigūruojami kelios mokėjimo jungtys, turite pateikti palaikomą nuomotojo tipo eilutę kaip nustatyta „Commerce“ štabo mokėjimo jungties konfigūravime (žr. tolesnį paveikslėlį). Jei jis tuščias, jis numatomas pagal „Adyen“ mokėjimo jungtį. Įtraukta į „Commerce” 10.0.14 leidimą.|
|Yra pirminis mokėjimas|  **Teisinga** arba **Klaidinga** | Jei **Teisingas**, bet koks klaidos pranešimas bus sukuriamas iš pirminės mokėjimo jungties išsiregistravimo puslapyje. Jei tiek „Adyen“, tiek „PayPal“ mokėjimo jungtys yra sukonfigūruotos, nustatykite „Adyen“ į **Teisinga**, kuris buvo įtrauktas į „Commerce“ leidimą 10.0.14.|

Tolesnis paveiksėlis rodo pavyzdį **Palaikomi nuomotojo tipai** su verte nustatyta į „PayPal" mokėjimo jungties konfigūravimą „Commerce“ štabe.
![Palaikomų nuomotojo tipų „Commerce“ štabe pavyzdys](./media/ecommerce-paymenttendertypes.png)

## <a name="billing-address"></a>Sąskaitų siuntimo adresas

Mokėjimo adreso modulis gali būti naudojamas išsiregistravimo puslapyje, jei „Adyen“ mokėjimo jungties mokėjimo adreso eilutės nepakankamai atitinka su likusio saito vaizdu. 

Norėdami naudoti mokėjimo adreso modulį išsiregistravimo puslapyje, kai mokėjimo modulis yra integruotas su „Adyen“ mokėjimo jungtimi, nustatykite **Rodyti mokėjimo adreso** ypatybę į **Netikra** tam, kad paskirtas mokėjimo adreso modulis būtų naudojamas, o ne nustatytasis „Adyen“ mokėjimo adresas. Tokiu atveju, saito autorius turėtų įtraukti mokėjimo adreso modulį į išsiregistravimo puslapį. „Adyen“ mokėjimo jungtis taip pat suteikia galimybę naudoti siuntimo adresą kaip mokėjimo siekiant sumažinti žingsnių skaičių saito vartotojui.

Panašiai į mokėjimo modulius. **Palaikomo nuomotojo tipų** ypatybė buvo įtraukta į mokėjimo adreso modulį „Commerce“ versijoje 10.0.14. Šios ypatybės vertė turi būti identiška vertei pateiktai mokėjimo modulyje siekiant užtikrinti, kad jos veiktų kartu. „Adyen“ mokėjimo jungčiai, tiek mokėjimo modulis, tiek mokėjimo adreso modulis turi palikti šią vertę tuščią (nustatytoji būsena). „PayPal“ jungčiai, paskirtas mokėjimo adreso modulis nebūtinas. Kitiems mokėjimo jungčių tipams, eilutė turi būti pateikta kaip konfigūruota „Commerce“ štabe.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Įtraukite mokėjimo modulį į galutinį puslapį ir nustatykite reikiamas ypatybes

Mokėjimo modulis gali būti įtrauktas tik į galutinį modulį. Dėl išsamesnės informacijos apie tai, kaip konfigūruoti mokėjimo modulį išsiregistravimo puslapis, žr. [Galutinis modulis](add-checkout-module.md).

Jei „Adyen“ ir „PayPal“ mokėjimo jungtys yra būtinos, įtraukite abu modulius į mokėjimo skyrių. Įsitikinkite, kad **Palaikomi nuomotojo tipai** ypatybės vertė yra sukonfigūruota „Paypal“ ir palikite tuščią „Adyen“. Taip pat, nustatykite **Yra priminis apmokėjimas** savybę į **Teisinga** „Adyen“.

## <a name="additional-resources"></a>Papildomi ištekliai

[Krepšelio modulis](add-cart-module.md)

[Krepšelio piktogramos modulis](cart-icon-module.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Siuntimo adreso modulis](ship-address-module.md)

[Pristatymo parinkčių modulis](delivery-options-module.md)

[Paėmimo informacijos modulis](pickup-info-module.md)

[Išsamios užsakymo informacijos modulis](order-confirmation-module.md)

[Dovanų kortelės modulis](add-giftcard.md)

[„Dynamics 365“ mokėjimo jungtis, skirta sprendimui „Adyen“](dev-itpro/adyen-connector.md)

[„Dynamics 365 Payment Connector“ skirtas „PayPal“](paypal.md)

[Stipri kliento autentifikacija naudojant „Adyen“](adyen_redirect.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]