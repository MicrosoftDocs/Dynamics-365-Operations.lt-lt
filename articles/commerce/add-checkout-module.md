---
title: Pirkimo užbaigimo modulis
description: Šiame straipsnyje aprašoma, kaip į puslapį įtraukti tikrinimo modulį ir nustatyti būtinas ypatybes.
author: anupamar-ms
ms.date: 05/18/2022
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a30d56d7edf967a3afab7442338dd9f480ef7fd0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869033"
---
# <a name="checkout-module"></a>Pirkimo užbaigimo modulis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip į puslapį įtraukti tikrinimo modulį ir nustatyti būtinas ypatybes.

Pirkimo užbaigimo modulis yra specialus konteineris, kuriame yra visi moduliai, reikalingi užsakymui sukurti. Jame pateikiama nuosekli veiksmų eiga, pagal kurią klientas įveda visą pirkimui aktualią informaciją. Jis fiksuoja siuntimo adresą, siuntimo būdą ir atsiskaitymo informaciją. Jame taip pat pateikiama užsakymo suvestinė ir kita informacija, susijusi su kliento užsakymu.

Pirkimo užbaigimo modulis duomenis generuoja pagal krepšelio ID. Šis krepšelio ID įrašomas kaip naršyklės slapukas. Krepšelio ID reikia norint vaizduoti informaciją pirkimo užbaigimo modulyje, pvz., užsakymo prekes, visą sumą ir nuolaidas. 

Toliau pateiktame paveikslėlyje parodytas pirkimo užbaigimo puslapyje esančio „Fabrikam“ pirkimo užbaigimo modulio pavyzdys.

![Pirkimo užbaigimo modulio pavyzdys.](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a>Pirkimo užbaigimo modulio ypatybės

Pirkimo užbaigimo moduliuose rodoma užsakymo suvestinė ir pateikiama užsakymų pateikimo funkcija. Norint surinkti visą kliento informaciją, kurios reikia norint, kad būtų galima pateikti užsakymą, į pirkimo užbaigimo modulį reikia įtraukti papildomus modulius. Todėl mažmenininkai turi galimybę į pirkimo užbaigimo srautą įtraukti pasirinktinius modulius arba pašalinti modulius pagal savo reikalavimus.

| Ypatybės pavadinimas | Reikšmės | aprašymas |
|----------------|--------|-------------|
| Pirkimo užbaigimo antraštė | Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** ar **H6**) | Antraštė išsiregistravimo moduliui. |
| Užsakymo suvestinės antraštė | Antraštės tekstas | Antraštė užsakymo santraukos modulio skyriui. |
| Vežimėlio eilutės prekių antraštė | Antraštės tekstas | Antraštė vežimėlių eilutės prekėms, kurios yra rodomos išsiregistravimo modulyje. |
| Rodyti siuntimo kaštus eilutės prekei | **Teisinga** arba **Klaidinga** | Jei ši ypatybė yra nustatytą į **Teisinga**, eilutei taikomi siuntimo mokesčiai bus rodomo vežimėlio eilutėse. Jei **Antraštės mokestis be paskirstymo** funkcija yra įjungta komerciniame štabe, siuntimo mokestis bus taikomas antraštės lygiui, o ne eilutės lygiui. Funkcija buvo įtraukta 10.0.13 komercijos versijoje. |

## <a name="modules-that-can-be-used-in-the-checkout-module"></a>Moduliai, kuriuos galima naudoti pirkimo užbaigimo modulyje

- **Siuntimo adresas** – naudodamas šį modulį klientas gali įtraukti arba pasirinkti užsakymo siuntimo adresą. Dėl išsamesnės informacijos apie šį modulį, žr. [Siuntimo adreso modulis](ship-address-module.md).

    Toliau pateiktame paveikslėlyje parodytas pirkimo užbaigimo puslapyje esančio siuntimo adreso modulio pavyzdys.

    ![Siuntimo adreso modulio pavyzdys.](./media/ecommerce-shippingaddress.PNG)

- **Pristatymo parinktys** – Šis modulis leidžia klientui pasirinkti užsakymo pristatymo būdą. Dėl išsamesnės informacijos apie šį modulį, žr. [Pristatymo parinkčių modulis](delivery-options-module.md).

    Toliau pateiktame paveikslėlyje parodytas pirkimo užbaigimo puslapyje esančio pristatymo parinkčių modulio pavyzdys.
 
    ![Pristatymo parinkčių modulio pavyzdys.](./media/ecommerce-deliveryoptions.PNG)

- **Pirkimo užbaigimo skyriaus konteineris** – šis modulis yra konteineris, kuriame galite įdėti kelis modulius ir sukurti skyrių pirkimo užbaigimo eigoje. Pavyzdžiui, šiame konteineryje galite įdėti visus su mokėjimu susijusius modulius, kad jie būtų rodomi kaip vienas skyrius. Šis modulis turi įtakos tik eigos išdėstymui.

- **Dovanų kortelė** – naudodamas šį modulį klientas gali už užsakymą sumokėti dovanų kortele. Dėl išsamesnės informacijos apie šį modulį, žr. [Dovanos kortelės modulis](add-giftcard.md).

- **Lojalumo taškai** – naudodamas šį modulį klientas gali už užsakymą sumokėti lojalumo taškais. Jis pateikia turimų taškų ir baigiančių galioti taškų suvestinę, o klientas gali pasirinkti panaudotinų taškų skaičių. Jei klientas nėra prisijungęs, nėra lojalumo programos narys arba jei visa krepšelio suma yra 0 (nulis), šis modulis automatiškai paslepiamas.

- **Mokėjimas** – Šis modulis leidžia klientui sumokėti už užsakymą naudojant kredito ar debeto kortelę. Klientai taip pat gali pateikti mokėjimo adresą pasirinktai mokėjimo parinkčiai. Dėl išsamesnės informacijos apie šį modulį, žr. [Mokėjimo modulis](payment-module.md).

    Tolesnis paveikslėlis rodo dovanų kortelės lojalumo taškų pavyzdį ir mokėjimo modulius išsiregistravimo puslapyje.

    ![Dovanų kortelės, lojalumo taškų ir mokėjimo modulių pavyzdžiai pirkimo užbaigimo puslapyje.](./media/ecommerce-payments.PNG)

- **Kontaktinė informacija** – naudodamas šį modulį klientas gali įtraukti arba pakeisti užsakymo kontaktinę informaciją (el. pašto adresą).

- **Teksto blokas** – šiame modulyje yra pranešimai, grindžiami turinio valdymo sistema (TVS). Pavyzdžiui, jame gali būti pranešimas „Jei kyla problemų dėl užsakymo, kreipkitės numeriu 1-800-Fabrikam.“ 

- **Išsiregistravimo sąlygos ir terminai** – Šis modulis rodo platų tekstą, kuriame pateiktos sąlygos ir terminai ir užbaigimo laukelį kliento indėliui. Žymimas laukelis yra pasirenkamas ir konfigūruojamas. Indėlį apima modulis ir jis gali būti naudojamas kaip kvitas prieš užsakymo pateikimą, tačiau nėra įtrauktas į užsakymo santraukos informaciją. Šis modulis gali būti įtrauktas į užbaigimo talpyklą, užbaigimo skyriaus talpyklą ar sąlygų ir terminų vietą pagal verslo poreikius. Jei jis įtrauktas į užbaigimo talpyklą ar užbaigimo skyriaus talpyklos vietą, jis pasirodys kaip žingsnis užbaigimo procese. Jei jis įtrauktas į sąlygų ir terminų vietą, jis pasirodys šalia užsakymo pateikimo mygtuko.

    Tolesnis paveikslėlis rodo užbaigimo puslapyje esančių terminų ir sąlygų pavyzdį.

    ![Sąlygų ir nuostatų pavyzdys pirkimo užbaigimo puslapyje.](./media/ecommerce-checkout-terms.PNG)

## <a name="commerce-scale-unit-interaction"></a>„Commerce Scale Unit“ sąveika

Didžioji dalis pirkimo užbaigimo informacijos, pvz., siuntimo adresas ir siuntimo būdas, saugoma krepšelyje ir tvarkoma kartu su užsakymu. Vienintelė išimtis yra kredito kortelės informacija. Ši informacija tvarkoma tiesiogiai, naudojant „Adyen“ mokėjimo jungtį. Mokėjimas yra patvirtintas, tačiau jis nėra nuskaitytas iki tol, kol užsakymas yra įvykdomas.

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a>Pirkimo užbaigimo modulio įtraukimas į puslapį ir reikiamų ypatybių nustatymas

Norėdami į naują puslapį įtraukti pirkimo užbaigimo modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Eikite į **Fragmentai** ir tuomet pasirinkite **Naujas** tam, kad sukurtumėte naują fragmentą.
1. Dialogo lange **Pasirinkti fragmentą** pasirinkite tikrinimo **modulį**.
1. Dalyje **Fragmento pavadinimas** įveskite pavadinimą **Pirkimo užbaigimo fragmentas** ir pasirinkite **Gerai**.
1. Pasirinkite vietą **Pirkimo užbaigimas**.
1. Dešinėje pusėje esančioje ypatybių srityje pasirinkite pieštuko simbolį, į laukelį įveskite antraštės tekstą ir pasirinkite varnelės simbolį.
1. Tikrinimo informacijos **atminties laiko** atrinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite siuntimo **adresą**, pristatymo pasirinktis, **·** **tikrinimo skyriaus konteinerį** **ir** kontaktinės informacijos modulius, tada pasirinkite **Gerai.**
1. **Tikrinimo skyriaus konteinerio** modulyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti** modulius pasirinkite dovanų **kortelę**, lojalumo **ir** mokėjimo **modulius**, tada pasirinkite **Gerai**. Taip užtikrinate, kad viename skyriuje kartu rodomi visi mokėjimo būdai.
1. **Sąlygos ir terminai** vietoje įtraukite **Užbaigimo terminai ir sąlygos** modulį, jei jo reikia. Modulio ypatybių juostoje sukonfigūruokite teksto sąlygas ir terminus taip, kaip būtina.
1. Norėdami peržiūrėti fragmentą, pasirinkite **Įrašyti** ir **Peržiūrėti**. Kai kurie moduliai, kurie neturi krepšelio konteksto, peržiūroje gali būti neatvaizduoti.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Sukurkite šabloną, kuriame naudojamas naujasis pirkimo užbaigimo fragmentas.
1. Sukurkite pirkimo užbaigimo puslapį, kuriame naudojamas naujasis šablonas.

## <a name="additional-resources"></a>Papildomi ištekliai

[Krepšelio modulis](add-cart-module.md)

[Krepšelio piktogramos modulis](cart-icon-module.md)

[Mokėjimo modulis](payment-module.md)

[Siuntimo adreso modulis](ship-address-module.md)

[Pristatymo parinkčių modulis](delivery-options-module.md)

[Paėmimo informacijos modulis](pickup-info-module.md)

[Išsamios užsakymo informacijos modulis](order-confirmation-module.md)

[Dovanų kortelės modulis](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
