---
title: Pirkimo užbaigimo modulis
description: Šioje temoje aprašoma, kaip į puslapį įtraukti pirkimo užbaigimo modulį ir nustatyti reikiamas ypatybes.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bd1d66fc39872019fc38dbbfb56dc3015d57d0dd
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411215"
---
# <a name="checkout-module"></a>Pirkimo užbaigimo modulis


[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip į puslapį įtraukti pirkimo užbaigimo modulį ir nustatyti reikiamas ypatybes.

## <a name="overview"></a>Peržiūrėti

Pirkimo užbaigimo modulis yra specialus konteineris, kuriame yra visi moduliai, reikalingi užsakymui sukurti. Jame pateikiama nuosekli veiksmų eiga, kurią naudodamas klientas įvedas visą aktualią informaciją, kad galėtų pirkti. Jis fiksuoja siuntimo adresą, siuntimo būdą ir atsiskaitymo informaciją. Jame taip pat pateikiama užsakymo suvestinė ir kita informacija, susijusi su kliento užsakymu.

Pirkimo užbaigimo modulis duomenis generuoja pagal krepšelio ID. Šis krepšelio ID įrašomas kaip naršyklės slapukas. Krepšelio ID reikia norint vaizduoti informaciją pirkimo užbaigimo modulyje, pvz., užsakymo prekes, visą sumą ir nuolaidas. 

Toliau pateiktame paveikslėlyje parodytas pirkimo užbaigimo puslapyje esančio „Fabrikam“ pirkimo užbaigimo modulio pavyzdys.

![Pirkimo užbaigimo modulio pavyzdys](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a>Pirkimo užbaigimo modulio ypatybės

Pirkimo užbaigimo moduliuose rodoma užsakymo suvestinė ir pateikiama užsakymų pateikimo funkcija. Norint surinkti visą kliento informaciją, kurios reikia norint, kad būtų galima pateikti užsakymą, į pirkimo užbaigimo modulį reikia įtraukti papildomus modulius. Todėl mažmenininkai turi galimybę į pirkimo užbaigimo srautą įtraukti pasirinktinius modulius arba pašalinti modulius pagal savo reikalavimus.

### <a name="modules-that-can-be-used-in-the-checkout-module"></a>Moduliai, kuriuos galima naudoti pirkimo užbaigimo modulyje

- **Siuntimo adresas** – naudodamas šį modulį klientas gali įtraukti arba pasirinkti užsakymo siuntimo adresą. Jei klientas prisijungęs, rodomi visi anksčiau įrašyti to kliento adresai. Tada klientas gali pasirinkti iš šių adresų. Klientas taip pat gali įtraukti naują adresą. Siuntimo adresas naudojamas visoms užsakymo prekėms, kurias reikia siųsti. Jo negalima tinkinti atskiroms eilutės prekėms. Siuntimo adresų formatai nustatyti kiekvienai šaliai ar regionui ir šis modulis taiko konkrečių šalių / regionų taisykles. Nors šiame modulyje nėra adreso tikrinimo galimybės, ją galima įdiegti tinkinant. Jei užsakyme yra tik tokios prekės, kurios bus atsiimtos parduotuvėje, šis modulis automatiškai paslepiamas.

    Toliau pateiktame paveikslėlyje parodytas pirkimo užbaigimo puslapyje esančio siuntimo adreso modulio pavyzdys.

    ![Siuntimo adreso modulio pavyzdys](./media/ecommerce-shippingaddress.PNG)

- **Pristatymo parinktys** – naudodamas šį modulį klientas gali pasirinkti užsakymo pristatymo parinktį. Pristatymo parinktys priklauso nuo siuntimo adreso. Pakeitus siuntimo adresą, pristatymo parinktis reikia gauti iš naujo. Jei užsakyme yra tik tokios prekės, kurios bus atsiimtos parduotuvėje, šis modulis automatiškai paslepiamas.

    Toliau pateiktame paveikslėlyje parodytas pirkimo užbaigimo puslapyje esančio pristatymo parinkčių modulio pavyzdys.

    ![Pristatymo parinkčių modulio pavyzdys](./media/ecommerce-deliveryoptions.PNG)

- **Pirkimo užbaigimo skyriaus konteineris** – šis modulis yra konteineris, kuriame galite įdėti kelis modulius ir sukurti skyrių pirkimo užbaigimo eigoje. Pavyzdžiui, šiame konteineryje galite įdėti visus su mokėjimu susijusius modulius, kad jie būtų rodomi kaip vienas skyrius. Šis modulis turi įtakos tik eigos išdėstymui.
- **Dovanų kortelė** – naudodamas šį modulį klientas gali už užsakymą sumokėti dovanų kortele. Jis palaiko tik „Microsoft Dynamics 365 Commerce“ dovanų korteles. Užsakymui galima pritaikyti vieną arba kelias dovanų korteles. Jei dovanų kortelės balanso nepakanka krepšelio sumai padengti, dovanų kortelę galima naudoti su kitu mokėjimo būdu. Dovanų korteles galima panaudoti, tik jei klientas yra prisijungęs.
- **Lojalumo taškai** – naudodamas šį modulį klientas gali už užsakymą sumokėti lojalumo taškais. Jis pateikia turimų taškų ir baigiančių galioti taškų suvestinę, o klientas gali pasirinkti panaudotinų taškų skaičių. Jei klientas nėra prisijungęs, nėra lojalumo programos narys arba jei visa krepšelio suma yra 0 (nulis), šis modulis automatiškai paslepiamas.
- **Mokėjimas** – naudodamas šį modulį klientas gali už užsakymą sumokėti kredito kortele. Jei visą krepšelio sumą dengia lojalumo taškai ar dovanų kortelė arba jei ji yra 0 (nulis), šis modulis automatiškai paslepiamas. Šiam moduliui kredito kortelė integruojama naudojant „Adyen“ mokėjimo jungtį. Norėdami apie tai, kaip naudoti šią jungtį, gauti daugiau informacijos, žr. [„Dynamics 365“ mokėjimo jungtis, skirta „Adyen“](dev-itpro/adyen-connector.md).
- **Atsiskaitymo adresas** – naudodamas šį modulį klientas gali pateikti atsiskaitymo informaciją. Kartu su kredito kortelės informacija šią informaciją tvarko „Adyen“. Šiame modulyje yra parinktis, kurią naudodami klientai savo atsiskaitymo adresą gali naudoti kaip siuntimo adresą.

    Toliau pateiktame paveikslėlyje parodytas dovanų kortelės, lojalumo taškų, mokėjimo ir atsiskaitymo adreso modulių, esančių pirkimo užbaigimo puslapyje, pavyzdys.

    ![Dovanų kortelės, lojalumo taškų, mokėjimo ir atsiskaitymo adreso modulių pavyzdys](./media/ecommerce-payments.PNG)

- **Kontaktinė informacija** – naudodamas šį modulį klientas gali įtraukti arba pakeisti užsakymo kontaktinę informaciją (el. pašto adresą).

- **Teksto blokas** – šiame modulyje yra pranešimai, grindžiami turinio valdymo sistema (TVS). Pavyzdžiui, jame gali būti pranešimas „Jei kyla problemų dėl užsakymo, kreipkitės numeriu 1-800-Fabrikam“. 

## <a name="commerce-scale-unit-interaction"></a>„Commerce Scale Unit“ sąveika

Didžioji dalis pirkimo užbaigimo informacijos, pvz., siuntimo adresas ir siuntimo būdas, saugoma krepšelyje ir tvarkoma kartu su užsakymu. Vienintelė išimtis yra kredito kortelės informacija. Ši informacija tvarkoma tiesiogiai, naudojant „Adyen“ mokėjimo jungtį. Mokėjimas leidžiamas, tačiau nenuskaičiuojamas.

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a>Pirkimo užbaigimo modulio įtraukimas į puslapį ir reikiamų ypatybių nustatymas

Norėdami į naują puslapį įtraukti pirkimo užbaigimo modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Nueikite į **Puslapio fragmentai** ir pasirinkite **Naujas**, kad sukurtumėte naują fragmentą.
1. Dialogo lange **Naujas puslapio fragmentas** pasirinkite modulį **Pirkimo užbaigimas**.
1. Dalyje **Puslapio fragmento pavadinimas** įveskite pavadinimą **Pirkimo užbaigimo fragmentas** ir pasirinkite **Gerai**.
1. Pasirinkite vietą **Pirkimo užbaigimas**.
1. Dešinėje pusėje esančioje ypatybių srityje pasirinkite pieštuko simbolį, į laukelį įveskite antraštės tekstą ir pasirinkite varnelės simbolį.
1. Vietoje **Pirkimo užbaigimo informacija** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulius **Siuntimo adresas**, **Pristatymo parinktys**, **Pirkimo užbaigimo skyriaus konteineris** ir **Kontaktinė informacija**, tada pasirinkite – **Gerai**.
1. Modulyje **Pirkimo užbaigimo skyriaus konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** dalyje pasirinkite modulius **Dovanų kortelė**, **Lojalumas** ir **Mokėjimas** ir pasirinkite **Gerai**. Taip užtikrinate, kad viename skyriuje kartu rodomi visi mokėjimo būdai.
1. Norėdami peržiūrėti fragmentą, pasirinkite **Įrašyti** ir **Peržiūrėti**. Kai kurie moduliai, kurie neturi krepšelio konteksto, peržiūroje gali būti neatvaizduoti.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Sukurkite šabloną, kuriame naudojamas naujasis pirkimo užbaigimo fragmentas.
1. Sukurkite pirkimo užbaigimo puslapį, kuriame naudojamas naujasis šablonas.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Konteinerio modulis](add-container-module.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Krepšelio modulis](add-cart-module.md)

[Užsakymo patvirtinimo modulis](order-confirmation-module.md)

[Antraštės modulis](author-header-module.md)

[Poraštės modulis](author-footer-module.md)
