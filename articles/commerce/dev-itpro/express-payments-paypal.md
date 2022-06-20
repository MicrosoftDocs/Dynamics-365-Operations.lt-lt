---
title: Sukonfigūruokite greituosius mokėjimus „PayPal“
description: Šiame straipsnyje aprašoma, kaip konfigūruoti siųstų "PayPal" mokėjimus, kad būtų galima greičiau patikrinti galimybes Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 05/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: b69b7384992fb86370ff6881824a7d2c9a77d2c4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905287"
---
# <a name="configure-express-payments-for-paypal"></a>Sukonfigūruokite greituosius mokėjimus „PayPal“

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip konfigūruoti siųstų "PayPal" mokėjimus, kad būtų galima greičiau patikrinti galimybes Microsoft Dynamics 365 Commerce.

## <a name="key-terms"></a>Pagrindiniai terminai

| Semestras | Aprašymas |
|---|---|
| "PayPal" pavedimas | PayPal jungtis palaiko klientų patirtį ir integravimą. Tai taip pat vadinama PayPal mygtuku. |
| Piniginė | Mokėjimo tipas, į kurį nėra įtrauktos tradicinės mokėjimo charakteristikos, pvz., banko identifikavimo numerių (TALPYKLOS) diapazonas ir galiojimo data, kurie naudojami kredito ir debeto kortelių tipams atskirti. |
| Mokėjimas skubus | "Commerce" modulis, palaikantis spartesnį tikrinimo elgseną, kai naudojami palaikomi mokėjimo metodai. Šiame straipsnyje aprašomas mokėjimo siųstų modulių naudojimas su PayPal. |

Dynamics 365 Commerce siūlo papildomą PayPal integraciją į "PayPal". Kai "Dynamics 365" mokėjimo jungtis, skirta "PayPal", sukonfigūruota, "PayPal" mygtukas atsiranda kaip galimas mokėjimo būdas išsiregistravimo internete metu. Kai vartotojai pasirenka PayPal, jie yra nukreipiami į mokėjimo nurodymus tiesiogiai per PayPal, jie grįžta į interneto parduotuvės pirmą užsakymą. PayPal krepšelio patikrinimas leidžia klientams naudoti savo mokėjimo sąskaitos informaciją norint iš anksto užpildyti čekio formą, kad jie galėtų atlikti čekio procesą greičiau.

"Commerce" įtraukė mokėjimų siųstų modulį, kad būtų lengviau atlikti s express čekius. Mokėjimo siųstas modulis gali būti naudojamas fragmente, kuris gali būti įtrauktas į čekio ar krepšelio puslapį. Kai "PayPal" sukonfigūruota, ta pati "Dynamics 365" mokėjimo jungtis, skirta "PayPal" jungties nuorodai, naudojama ir mokėjimų s express pasirinktims, ir reguliariam išregistravimas.

## <a name="paypal-checkout-in-commerce"></a>"PayPal" tikrinimas "Commerce"

### <a name="prerequisites"></a>Būtinieji komponentai

Nustatykite "PayPal" "PayPal" aplinką, kaip [aprašyta "Dynamics 365" mokėjimo jungtyje, skirtoje PayPal](../paypal.md).

Jeigu payPal naudojate kaip įprasto tikrinimo srauto pasirinktį (kur vartotojai neautomatiniu būdu įveda savo sąskaitos informaciją, nenaudodami skritinio mokėjimo išankstinio pripildymo veiksmų), [vykdykite mokėjimo modulio nustatymo instrukcijas](../payment-module.md).

### <a name="payment-express-module-with-paypal"></a>Mokėjimo sąs. modulis su PayPal

Mokėjimų siųsimo modulis veikia su palaikymo mokėjimo metodais, kad pasiūlyti klientams galimybę pasitikrinti greičiau, iš anksto pripildant savo mokėjimo paslaugų sąskaitos informaciją per išsiregistravimo procesą. Mokėjimo siųsimo modulis naudoja sukonfigūruotą mokėjimo jungtį, kad iš anksto užpildytų čekio formą vartotojo sąskaitos informacija, pvz., adresas, kontaktinė informacija ir pasirinktas mokėjimo būdas.

Kai naudojamas "PayPal" skubus išregistravimas ir vartotojas pasirenka "PayPal" mygtuką mokėjimų mokėjimų skubiame čekių puslapio skyriuje, atidaromas PayPal iFrame mokėjimo langas. Tada vartotojas prisijungia prie savo PayPal sąskaitos, kad galėtų naudoti savo sąskaitos siuntimo adresą, sąskaitų siuntimo adresą, el. pašto adresą ir mokėjimo Būdą PayPal, kurį naudojant mokama už operaciją.

Vartotojui atlikus veiksmą "PayPal" lange, jie grįžta į komercijos svetainės tikrinimo puslapį, kur čekio forma iš anksto užpildoma jų pasirinkta informacija. Mokėjimo sraute, vartotojui iš anksto bus užpildyta pirmoji pristatymo pasirinktis, galima pristatymo adresu, kuris grąžinamas. Tada vartotojas turi pasirinktį peržiūrėti užsakymą ir **pakeisti užsakymo išregistravo informaciją prieš pasirinkant Užsakymo** vietą užsakymui baigti.

### <a name="add-the-payment-express-module-with-paypal-to-a-fragment"></a>Įtraukti mokėjimo siųstų modulių su PayPal į fragmentą

Norėdami įtraukti mokėjimo skubią modulį su PayPal į Komercijos svetainės generatoriaus fragmentą, atlikite šiuos veiksmus.

1. Eiti į savo svetainę.
1. Kairiojoje naršymo srityje pasirinkite **Fragmentai**, tada pasirinkite **Naujas**.
1. Naujo fragmento **dialogo** **lange** raskite ir pasirinkite mokėjimo siųstų modulį, **tada dalyje Fragmento** pavadinimas įveskite fragmento pavadinimą (pvz., **Skubus išregistravimas).**
1. Jei **norite** sukurti fragmentą, pasirinkite Gerai.
1. Struktūros rodinyje pasirinkite sukurto mokėjimo siųsto modulio atminties lauką.
1. Ypatybės srityje pasirinkite **Antraštė**.
1. Antraštės dialogo **lango** **teksto** lauke įveskite antraštės tekstą, kurį norite rodyti savo svetainės s express checkout sekcijai (pvz., **Skubus išregistravimas).**
1. Antraštės **lygyje** pasirinkite antraštės lygį (pvz., **H2**).
1. Pasirinkite **Gerai**.
1. Ypatybės srityje lauko aukštis **įveskite arba koreguokite iFrame** elemento iFrame aukštį (pvz., **60**).
1. Palaikomų **mokėjimo priemonių tipų** lauke įveskite **PayPal**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Įtraukti mokėjimo s express fragmentą į tikrinimo puslapį

Norėdami įtraukti mokėjimo s express fragmentą į svetainės generatoriaus tikrinimo puslapį, atlikite šiuos veiksmus.

1. Eiti į savo svetainę.
1. Kairiojoje naršymo srityje pasirinkite **Puslapiai** ir pasirinkite svetainės tikrinimo puslapį.
1. Jei **norite redaguoti** puslapį, pasirinkite Redaguoti.
1. Pagrindiniame laiko **atminties** atminties lape pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite konteinerio **modulį**, tada pasirinkite **Gerai**.

    > [!NOTE]
    > Jei konteinerio modulis, kuriame yra tikrinimo fragmentas, jau yra, perkelkite mokėjimo s express skyrių, kad jis būtų virš esamo išregistravimo konteinerio pagrindinėje atminties **atminties** dalyje. Tada mokėjimo siųstas skyrius bus atvaizduotas virš įprasto tikrinimo konteinerio. Norėdami perkelti konteinerio modulį aukštyn arba žemyn, pasirinkite daugtaškį (**...**), tada pasirinkite Perkelti **aukštyn** arba **Žemyn**.

1. **Konteinerio** ypatybių srityje rekomenduojame ypatybės parametrus konfigūruoti tokiu būdu:

    - **Konteinerio maketas** – pasirinkite **Suspausta**.
    - **Plotis** – pasirinkite užpildymo **konteinerį**.
    - **Rodomi tiks ir** pasirinkti **tris**.

1. Konteinerio **laiko** atminties atminties dalyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **fragmentą**.
1. Dialogo lange **Pasirinkti fragmentą** raskite ir pasirinkite siųstas mokėjimo fragmentą, kurį sukūrėte, tada pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Įtraukti mokėjimo s express fragmentą į krepšelio puslapį

Norėdami įtraukti mokėjimo siųstas fragmentą į krepšelio puslapį svetainės generatoriuje, atlikite šiuos veiksmus.

1. Eiti į savo svetainę.
1. Kairiojoje naršymo srityje pasirinkite **Puslapiai** ir svetainės krepšelio puslapį.
1. Jei **norite redaguoti** puslapį, pasirinkite Redaguoti.
1. Pagrindiniame laiko atminties **skyriuje** raskite konteinerį, kuriame yra krepšelio **modulis**. Krepšelio **modulyje** bus mokėjimo siųsimo **laiko atminties**.
1. Pasirinkite " **Payment Express"** laiko atminties lauką, pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite siųsdami **modulį** Mokėjimas ir pasirinkite **Gerai**.
1. Ypatybės srityje, lauke Palaikomų mokėjimo **priemonių tipai**, įveskite **Paypal**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

### <a name="modes-of-delivery"></a>Pristatymo būdai

Kai mokėjimo siųsimo modulis sukonfigūruotas naudoti PayPal, pirma pristatymo pasirinktis, grąžinta dėl siuntimo adreso, kuris buvo pasirinktas "PayPal" sąskaitai, bus iš anksto užpildyta. Jei reikia, vartotojai galės keisti siuntimo adresą.

Pristatymo būdo užsakymas konfigūruojamas "**Commerce** Headquarters" kanalo pristatymo būdų skyriuje. Dėl daugiau informacijos, žr. [Nustatyti pristatymo būdus](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Tikrinimo modulis taip pat naudos pristatymo parinkčių modulį, kai pristatymo būdai atvaizduojami išregistravimo metu. Daugiau informacijos rasite pristatymo [pasirinkčių modulyje](../delivery-options-module.md).

Pristatymo būdai įtraukiami į "Commerce Headquarters" interneto parduotuvės sąrašą. Eikite **į "Retail" ir "Commerce \>" \>** kanalų interneto parduotuves ir pasirinkite parduotuvės kanalo ID. Tada pasirinkite **Nustatymo \> pristatymo būdus**. Konfigūracijoje rodomi modulio pristatymo būdai bus panašiai rodomi teritorijoje. Norėdami įtraukti arba pašalinti mažmeninės prekybos kanalo ar produkto pristatymo būdus, **veiksmų srityje pasirinkite Tvarkyti** pristatymo būdus.

## <a name="additional-resources"></a>Papildomi ištekliai

[DUK apie mokėjimus](payments-retail.md)

[Pirkimo užbaigimo modulis](../add-checkout-module.md)

[Mokėjimo modulis](../payment-module.md)

[Nustatyti pristatymo būdus](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Pristatymo parinkčių modulis](../delivery-options-module.md)
