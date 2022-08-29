---
title: Mokėjimo modulis
description: Šiame straipsnyje aprašomas mokėjimo modulis ir paaiškinama, kaip jį konfigūruoti Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: fa1482cb73a40df5f9bc9d3037196def71accf18
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279481"
---
# <a name="payment-module"></a>Mokėjimo modulis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomas mokėjimo modulis ir paaiškinama, kaip jį konfigūruoti Microsoft Dynamics 365 Commerce.

Mokėjimo modulis leidžia klientui sumokėti už užsakymus naudojant kredito ar debeto korteles. Mokėjimo papildymas šiam moduliui yra pateiktas „Dynamics 365 Payment Connector“ „Adyen“. Dėl išsamesnės informacijos, kaip nustatyti ir konfigūruoti mokėjimo jungtį, žr. [„Dynamics 365 Payment Connector“ „Adyen“](dev-itpro/adyen-connector.md).  

„Commerce“ versijoje 10.0.14, mokėjimo modulis taip pat buvo integruotas su „Dynamics 365 Payment Connector“ skirtu „PayPal“ tam, kad leistų klientams sumokėti už užsakymus su „PayPal“. Dėl išsamesnės informacijos, kaip nustatyti ir konfigūruoti „Dynamics 365 Payment Connector“ skirtą „PayPal“, žr. [„Dynamics 365 Payment Connector“ skirtą „PayPal“](paypal.md). 

## <a name="dynamics-365-payment-connector-for-adyen"></a>„Dynamics 365“ mokėjimo jungtis, skirta sprendimui „Adyen“ 

Mokėjimo modulis talpina mokėjimo informaciją, kuri yra laikoma per „Ayden“ HTML vidaus rėmuose (iframe). Mokėjimo modulis sąveikauja su „Commerce Scale Unit“ tam, kad gautų „Adyen“ mokėjimo informaciją. Kaip „Commerce Scale Unit“ sąveikos dalis, mokėjimo modulis gali leisti mokėjimo adreso informaciją pateikti per „iframe“ per „Adyen“ ar kaip atskirą modulį. „Fabrikam“ temoje, mokėjimo adresas yra įjungtas kaip atskiras modulis. Ši prieiga leidžia lanksčiau formatuoti, nes adreso eilutės gali būti sukurtos taip, kad atspindėtų siuntimo adreso eilutes.

Mokėjimo modulis taip pat leidžia prisijungusiems klientams įrašyti jų mokėjimo informaciją. Mokėjimo informacija ir sąskaitų adresai yra įrašomi ir valdomi per „Adyen“ mokėjimo jungtį.

Mokėjimo modulis apima visus mokesčius, kurie nėra apimti lojalumo taškų ar dovanų kortelės. Jei bendra užsakymo suma yra visiškai padengiama lojalumo taškais ar dovanų kortelės kreditu, mokėjimo modulis bus paslėptas ir klientas galės be jo pateikti užsakymą.

„Adyen“ mokėjimo jungtis taip pat palaiko stiprią kliento autentifikaciją (SCA). Europos Sąjungos (ES) Peržiūrėtų mokėjimų paslaugų direktyvos (PSD2) dalis numato, kad internetiniai pirkėjai būtų atpažinti ne jų internetinėje apsipirkimo patirtyje jiems naudojant elektroninį apmokėjimo būdą. Išsiregistravimo eigos metu, klientai yra nukreipiami į jų banko puslapį ir ten autentifikuojami bei nukreipiami atgal į „Commerce“ išregistravimo eigą. Tokio nukreipimo metu, informacija, kurią klientas įvedė išsiregistravimo eigos metu (pavyzdžiui, pristatymo adresas, pristatymo parinktys, dovanų kortelės informacija ir lojalumo informacija) išliks. Prieš jums įjungiant „Adyen“ mokėjimo jungties funkciją, mokėjimo jungtis turi būti konfigūruota SCA „Commerce“ štabe. Dėl išsamesnės informacijos, žr. [Stipri kliento autentifikacija naudojant „Adyen“](adyen_redirect.md). Ši funkcija buvo įjungta „Commerce“ versijoje 10.0.12.

> [!NOTE]
> Naudojant „Adyen” mokėjimo jungtį, „iframe” modulis, esantis mokėjimo modulyje, gali būti atvaizduotas tik tada, jei įtraukiate „Adyen” URL į jūsų svetainės leidžiamų URL sąrašą. Norėdami atlikti šį veiksmą, įtraukite **\*.adyen.com** į jūsų svetainės turinio saugos strategijos direktyvas **child-src**, **connect-src**, **img-src**, **script-src** ir **style-src**. Daugiau informacijos, žr. [Turinio saugos strategijos valdymas](manage-csp.md). 

Tolesnis paveikslėlis rodo dovanų kortelės pavyzdys ir „Adyen“ apmokėjimo modulius išsiregistravimo puslapyje.

![Dovanų kortelės pavyzdys ir „Adyen“ apmokėjimo modulius išsiregistravimo puslapyje.](./media/ecommerce-payments.PNG)

## <a name="dynamics-365-payment-connector-for-paypal"></a>„Dynamics 365 Payment Connector“, skirta „PayPal“

„Commerce“ versijoje 10.0.14, mokėjimo modulis taip pat buvo integruotas su „Dynamics 365 Payment Connector“ skirtu „PayPal“. Dėl išsamesnės informacijos apie tai, kaip nustatyti ir konfigūruoti šią mokėjimo jungtį, žr. [„Dynamics 365 Payment Connector“ skirtą „PayPal“](paypal.md).
 
Išsiregistravimo puslapyje galite turėti tiek „Adyen“, tiek ir „PayPal“ sukonfigūruotas jungtis. Apmokėjimo modulis bus papildytas papildomomis ypatybėmis, kad jos padėtų nustatyti, kuri jungtis turi veikti su kuria. Norėdami gauti daugiau informacijos, žr **. palaikomų mokėjimo priemonių** **tipus ir yra** pirminio mokėjimo modulio ypatybės šioje lentelėje.
  
Kai apmokėjimo modulis yra konfigūruotas siekiant naudoti „PayPal“ mokėjimo jungtį, „PayPal“ mygtukas pasirodo išsiregistravimo puslapyje. Kai klientas jį pasirenka, mokėjimo modulis apima „iframe“ su „Paypal“ informacija. Klientas gali prisijungti ir pateikti savo „Paypal“ informaciją esančią „iframe“, kad baigtų savo perlaidą. Kai klientas pasirenka sumokėti su „PayPal“, likęs likutis užsakyme bus nuskaičiuotas per „PayPal“.

„PayPal“ mokėjimo jungčiai nereikia mokėjimo adreso modulio, nes visa su mokėjimu susijusi informacija tvarkoma „Paypal“ per „iframe“. Nepaisant to, siuntimo adresas ir pristatymo parinkčių moduliai yra būtini.

Tolesnis paveikslėlis rodo dviejų mokėjimo modulių pavyzdį išsiregistravimo puslapyje, vienas kurių sukonfigūruotas su „Adyen“ mokėjimo jungtimi, o kitas su „Paypal“ mokėjimo jungtimi.
![„Adyen“ mokėjimo ir „Paypal“ modulių pavyzdys išsiregistravimo puslapyje.](./media/ecommerce-paypal.png)

Tolesnis paveikslėlis rodo „PayPal“ „iframe“ pavyzdį, kuris naudojamas „PayPal“ mygtuku. 
![„Paypal“ „iframe“ išsiregistravimo puslapio pavyzdys.](./media/ecommerce-paypal-iframe.png)

## <a name="payment-module-properties"></a>Mokėjimo modulio ypatybės

| Ypatybės pavadinimas | Reikšmės | Aprašas |
|---------------|--------|-------------|
| Antraštė | Antraštės tekstas | Pasirenkama antraštė mokėjimo moduliui. |
| „iframe“ aukštis | Pikseliai | „iframe“ aukštis pikseliais. Aukštis gali būti reguliuojamas, kaip būtina. |
| Rodyti sąskaitų siuntimo adresą | **Teisinga** arba **Klaidinga** | Jei ši ypatybė yra nustatyta į **Teisingą**, mokėjimo adresas bus pateiktas „Adyen“ mokėjimo modulio „iframe“ viduje. Jei nustatytas į **Netikras**, mokėjimo adresas nebus rodomas „Adyen“, o „Commerce“ vartotojas turės sukonfigūruoti modulį taip, kad jame būtų mokėjimo informacija išsiregistravimo puslapyje. „PayPal“ mokėjimo jungtyje, šis laukelis neturi jokio poveikio, nes mokėjimo adresą visiškai valdo „PayPal“. |
| Mokėjimo stiliaus nepaisymas | Kaskadinio stiliaus lapų (CSS) kodai | Kadangi mokėjimo modulis yra palaikomas „iframe“, esama apriboto stiliaus pajėgumo. Galite pasiekti tam tikrą stilių naudodami šią ypatybę. Vietos stiliaus viršijimui, turite įkelti CSS kodą kaip šios ypatybės vertę. Vietos kūrimo įrankis CSS viršija ir stiliai nėra taikomi šiam moduliui. |
|Palaikomi mokėjimo priemonių tipai| Eilutė| Jei sukonfigūruotos kelios mokėjimo jungties, turėtumėte pateikti palaikomą mokėjimo priemonės tipo eilutę, kaip nurodyta "Commerce Headquarters" mokėjimo jungties konfigūracijoje (žr. toliau nurodytą vaizdą). Jei jis tuščias, jis numatomas pagal „Adyen“ mokėjimo jungtį. Įtraukta į „Commerce” 10.0.14 leidimą.|
|Yra pirminis mokėjimas|  **Teisinga** arba **Klaidinga** | Jei **Teisingas**, bet koks klaidos pranešimas bus sukuriamas iš pirminės mokėjimo jungties išsiregistravimo puslapyje. Jei tiek „Adyen“, tiek „PayPal“ mokėjimo jungtys yra sukonfigūruotos, nustatykite „Adyen“ į **Teisinga**, kuris buvo įtrauktas į „Commerce“ leidimą 10.0.14.|
|Naudoti jungties ID| **Teisinga** arba **Klaidinga** | Naudokite šią ypatybę, jei sukonfigūruotos kelios svetainės mokėjimo jungtis. Jei **teisinga**, ryšio jungtis reikės naudoti mokėjimo koreliacijai naudoti jungties ID.|
|Naudoti naršyklės rinkinio kalbos kodą, kuris skirtas iFrame|  **Teisinga** arba **Klaidinga** | (Tik Adyen) Jei **teisinga**, Adyen iFrame kalba bus atvaizduota remiantis svetainės vartotojo naršyklės kontekstu, o ne svetainės sukonfigūruoto "Commerce" kanalo kalbos kodu. Įtraukta į „Commerce” 10.0.27 leidimą.|

Tolesnis paveikslėlis rodo pavyzdį **Palaikomi nuomotojo tipai** su verte nustatyta į „PayPal" mokėjimo jungties konfigūravimą „Commerce“ štabe.
![Palaikomų nuomotojo tipų „Commerce“ štabe pavyzdys.](./media/ecommerce-paymenttendertypes.png)

## <a name="billing-address"></a>Sąskaitų siuntimo adresas

Mokėjimo adreso modulis gali būti naudojamas išsiregistravimo puslapyje, jei „Adyen“ mokėjimo jungties mokėjimo adreso eilutės nepakankamai atitinka su likusio saito vaizdu. 

Norėdami naudoti mokėjimo adreso modulį išsiregistravimo puslapyje, kai mokėjimo modulis yra integruotas su „Adyen“ mokėjimo jungtimi, nustatykite **Rodyti mokėjimo adreso** ypatybę į **Netikra** tam, kad paskirtas mokėjimo adreso modulis būtų naudojamas, o ne nustatytasis „Adyen“ mokėjimo adresas. Tokiu atveju, saito autorius turėtų įtraukti mokėjimo adreso modulį į išsiregistravimo puslapį. „Adyen“ mokėjimo jungtis taip pat suteikia galimybę naudoti siuntimo adresą kaip mokėjimo siekiant sumažinti žingsnių skaičių saito vartotojui.

Panašiai į mokėjimo modulius. **Palaikomo nuomotojo tipų** ypatybė buvo įtraukta į mokėjimo adreso modulį „Commerce“ versijoje 10.0.14. Šios ypatybės vertė turi būti identiška vertei pateiktai mokėjimo modulyje siekiant užtikrinti, kad jos veiktų kartu. „Adyen“ mokėjimo jungčiai, tiek mokėjimo modulis, tiek mokėjimo adreso modulis turi palikti šią vertę tuščią (nustatytoji būsena). „PayPal“ jungčiai, paskirtas mokėjimo adreso modulis nebūtinas. Kitiems mokėjimo jungčių tipams, eilutė turi būti pateikta kaip konfigūruota „Commerce“ štabe.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Įtraukite mokėjimo modulį į galutinį puslapį ir nustatykite reikiamas ypatybes

Mokėjimo modulis gali būti įtrauktas tik į galutinį modulį. Dėl išsamesnės informacijos apie tai, kaip konfigūruoti mokėjimo modulį išsiregistravimo puslapis, žr. [Galutinis modulis](add-checkout-module.md).

## <a name="configure-the-adyen-and-paypal-payment-connectors-when-both-are-used"></a>Konfigūruoti Adyen ir PayPal mokėjimo jungtis, kai naudojamos abi

Jei jūsų svetainei bus naudojamos ir Adyen, ir PayPal mokėjimo jungties, atlikite šiuos "Commerce" svetainių generatoriaus veiksmus, kad pridėtumėte kiekvienos jungties mokėjimo modulius prie tikrinimo modulio ir sukonfigūruokite kiekvieno modulio ypatybes.

1. PayPal mokėjimo modulio ypatybės srityje atlikite šiuos veiksmus:

    1. Palaikomų mokėjimo priemonių tipų **ypatybės lauke** įveskite **PayPal**.
    1. Išvalykite žymės langelį, jei ypatybė **Yra pirminis** mokėjimas.
    1. Pažymėkite žymės langelį, kad būtų naudojama **jungties ID** ypatybė.

1. Adyen mokėjimo modulio ypatybės srityje atlikite šiuos veiksmus:

    1. Palikite lauką, kad palaikoma **mokėjimo priemonių tipų** ypatybė būtų tuščia.
    1. Pažymėkite žymės langelį Ypatybė Yra **pirminis** mokėjimas.
    1. Pažymėkite žymės langelį, kad būtų naudojama **jungties ID** ypatybė.

> [!NOTE]
> Kai konfigūruojate, kad Adyen ir PayPal jungtis būtų naudojamos kartu, "Dynamics 365" mokėjimo jungtis, **skirta Adyen** **konfigūracijai**, turi būti pirma interneto kanalo mokėjimo sąskaitų jungties konfigūracijos vietoje "Commerce Headquarters". Norėdami patvirtinti arba pakeisti jungties užsakymą, eikite **į interneto parduotuves** ir pasirinkite savo svetainės kanalą. Tada skirtuke Nustatyti mokėjimo **sąskaitų** FastTab, skirtuke Jungtis, įsitikinkite, **·** **kad "Dynamics 365" mokėjimo jungtis, skirta Adyen** konfigūracijai, yra pirmoje vietoje (t. y. viršutinėje eilutėje) **ir ar "Dynamics 365" mokėjimo jungtis, skirta "PayPal**" konfigūracijai, yra antra eilutė.**·** Pridėkite arba pašalinkite jungtis, jei reikia jas pers tvarkai atlikti.

## <a name="additional-resources"></a>Papildomi ištekliai

[Krepšelio modulis](add-cart-module.md)

[Krepšelio piktogramos modulis](cart-icon-module.md)

[Pirkimo užbaigimo modulį](add-checkout-module.md)

[Siuntimo adreso modulis](ship-address-module.md)

[Pristatymo parinkčių modulis](delivery-options-module.md)

[Paėmimo informacijos modulis](pickup-info-module.md)

[Išsamios užsakymo informacijos modulis](order-confirmation-module.md)

[Dovanų kortelės modulis](add-giftcard.md)

[„Dynamics 365“ mokėjimo jungtis, skirta sprendimui „Adyen“](dev-itpro/adyen-connector.md)

[„Dynamics 365 Payment Connector“ skirtas „PayPal“](paypal.md)

[Stipri kliento autentifikacija naudojant „Adyen“](adyen_redirect.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
