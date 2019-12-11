---
title: Pirkimo užbaigimo modulis
description: Šioje temoje aprašoma, kaip į puslapį įtraukti pirkimo užbaigimo modulį ir nustatyti reikiamas ypatybes.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 4b810441fd25d41ee0893b119b4f7d91e7435d21
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697088"
---
# <a name="checkout-module"></a>Pirkimo užbaigimo modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip į puslapį įtraukti pirkimo užbaigimo modulį ir nustatyti reikiamas ypatybes.

## <a name="overview"></a>Peržiūrėti

Pirkimo užbaigimo modulis yra specialus konteineris, kuriame yra visi moduliai, reikalingi užsakymui sukurti. Pirkimo užbaigimo modulyje gali būti modulių, tvarkančių siuntimo adresą, siuntimo būdus, atsiskaitymo informaciją, užsakymo suvestinę ir kitą su kliento užsakymu susijusią informaciją. Jame pateikiama nuosekli veiksmų eiga, kurią naudodamas klientas įvedas visą aktualią informaciją, kad galėtų pirkti.

Pirkimo užbaigimo modulis duomenis generuoja pagal krepšelio ID. Šis krepšelio ID įrašomas kaip naršyklės slapukas. Krepšelio ID reikia norint vaizduoti informaciją pirkimo užbaigimo modulyje, pvz., užsakymo prekes, visą sumą ir nuolaidas.

## <a name="checkout-module-properties"></a>Pirkimo užbaigimo modulio ypatybės

Pirkimo užbaigimo modulyje yra keletas modulių. Naudodami pločio ypatybę, galite nurodyti, ar pirkimo užbaigimo modulio prekės turi būti priderintos prie jo pločio, ar užpildyti ekraną.

Pirkimo užbaigimo modulyje yra kelios vietos, pvz., vieta **Pirkimo užbaigimo informacija**, vieta **Užsakymo suvestinė** ir vieta **Pateikti užsakymą**. Kiekviena vieta palaiko tam tikrus modulius, kurie bus rodomi konkrečiame puslapio makete. Pavyzdžiui, vietoje **Pirkimo užbaigimo informacija** yra visi moduliai, kurių reikia norint suaktyvinti pirkimo užbaigimą, pvz., siuntimo adreso ir mokėjimo būdo moduliai. Vietoje **Užsakymo suvestinė** rodoma užsakymo suvestinė ir ji palaiko užsakymo pateikimo veiksmą. Vieta **Pateikti užsakymą** taip pat palaiko užsakymo pateikimo veiksmą. Užsakymo pateikimo modulius galima apibrėžti dviejose vietose, taip optimizuojant užsakymų pateikimo iš įvairių platformų procesą.

### <a name="modules-that-can-be-used-in-the-checkout-module"></a>Moduliai, kuriuos galima naudoti pirkimo užbaigimo modulyje

- **Siuntimo adresas** – naudodamas šį modulį klientas gali įtraukti arba pasirinkti užsakymo siuntimo adresą. Jei klientas prisijungęs, rodomi visi anksčiau įrašyti to kliento adresai. Tada klientas gali pasirinkti iš šių adresų. Klientas taip pat gali įtraukti naują adresą. Siuntimo adresas naudojamas visoms užsakymo prekėms, kurias reikia siųsti. Jo negalima tinkinti atskiroms eilutės prekėms. Siuntimo adresų formatai nustatyti kiekvienai šaliai ar regionui ir šis modulis taiko konkrečių šalių / regionų taisykles. Nors šiame modulyje nėra adreso tikrinimo galimybės, ją galima įdiegti tinkinant. Jei užsakyme yra tik tokios prekės, kurios bus atsiimtos parduotuvėje, šis modulis automatiškai paslepiamas.
- **Pristatymo parinktys** – naudodamas šį modulį klientas gali pasirinkti užsakymo pristatymo parinktį. Pristatymo parinktys priklauso nuo siuntimo adreso. Pakeitus siuntimo adresą, pristatymo parinktis reikia gauti iš naujo. Jei užsakyme yra tik tokios prekės, kurios bus atsiimtos parduotuvėje, šis modulis automatiškai paslepiamas.
- **Pirkimo užbaigimo skyriaus konteineris** – šis modulis yra konteineris, kuriame galite įdėti kelis modulius ir sukurti skyrių pirkimo užbaigimo eigoje. Pavyzdžiui, šiame konteineryje galite įdėti visus su mokėjimu susijusius modulius, kad jie būtų rodomi kaip vienas skyrius. Šis modulis turi įtakos tik eigos išdėstymui.
- **Dovanų kortelė** – naudodamas šį modulį klientas gali už užsakymą sumokėti dovanų kortele. Jis palaiko tik „Microsoft Dynamics 365 Commerce“ dovanų korteles. Užsakymui galima pritaikyti vieną arba kelias dovanų korteles. Jei dovanų kortelės balanso nepakanka krepšelio sumai padengti, dovanų kortelę galima naudoti su kitu mokėjimo būdu. Dovanų korteles galima panaudoti, tik jei klientas yra prisijungęs.
- **Lojalumo taškai** – naudodamas šį modulį klientas gali už užsakymą sumokėti lojalumo taškais. Jis pateikia turimų taškų ir baigiančių galioti taškų suvestinę, o klientas gali pasirinkti panaudotinų taškų skaičių. Jei klientas nėra prisijungęs, nėra lojalumo programos narys arba jei visa krepšelio suma yra 0 (nulis), šis modulis automatiškai paslepiamas.
- **Kredito kortelė** – naudodamas šį modulį klientas gali už užsakymą sumokėti kredito kortele. Jei visą krepšelio sumą dengia lojalumo taškai ar dovanų kortelė arba jei ji yra 0 (nulis), šis modulis automatiškai paslepiamas. Kredito kortelė integruojama naudojant „Adyen“ mokėjimo jungtį. Norėdami apie tai, kaip naudoti šią jungtį, gauti daugiau informacijos, žr. [„Adyen“ mokėjimo jungtis](https://).
- **Atsiskaitymo adresas** – naudodamas šį modulį klientas gali pateikti atsiskaitymo informaciją. Kartu su kredito kortelės informacija šią informaciją tvarko „Adyen“. Šiame modulyje yra parinktis, kurią naudodami klientai savo atsiskaitymo adresą gali naudoti kaip siuntimo adresą.
- **Kontaktinė informacija** – naudodamas šį modulį klientas gali įtraukti arba pakeisti užsakymo kontaktinę informaciją (el. pašto adresą).
- **Pateikti užsakymą** – naudodamas šį modulį klientas gali pateikti užsakymą.
- **Raiškinio turinio blokas** – šiame modulyje yra pranešimai, grindžiami turinio valdymo sistema (TVS). Pavyzdžiui, jame gali būti pranešimas „Jei kyla problemų dėl užsakymo, kreipkitės numeriu 1-800-FABRIKAM“. 
- **Užsakymo suvestinė** – šiame modulyje rodomas užsakymo išlaidų paskirstymas.
- **Užsakymo eilutės prekės** – šiame modulyje rodoma prekių, kurios bus įtrauktos į užsakymą, suvestinė.

## <a name="retail-server-interaction"></a>Sąveika su „Retail Server“

Didžioji dalis pirkimo užbaigimo informacijos, pvz., siuntimo adresas ir siuntimo būdas, saugoma krepšelyje ir tvarkoma kartu su užsakymu. Vienintelė išimtis yra kredito kortelės informacija. Ši informacija tvarkoma tiesiogiai, naudojant „Adyen“ mokėjimo jungtį. Mokėjimas leidžiamas, tačiau nenuskaičiuojamas.

## <a name="add-a-checkout-module-to-a-new-page-and-set-the-required-properties"></a>Pirkimo užbaigimo modulio įtraukimas į naują puslapį ir reikiamų ypatybių nustatymas

Norėdami į naują puslapį įtraukti pirkimo užbaigimo modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Nueikite į **Fragmentas \> Naujas fragmentas** ir naują fragmentą pavadinkite **Pirkimo užbaigimo fragmentas**.
1. Į fragmentą įtraukite pirkimo užbaigimo modulį.
1. Į pirkimo užbaigimo modulį įtraukite antrašę.
1. Vietoje **Pirkimo užbaigimo informacija** įtraukite siuntimo adreso, pristatymo parinkčių, pirkimo užbaigimo skyriaus konteinerio ir kontaktinės informacijos modulius. Vietoje **Pirkimo užbaigimo informacija** dabar turėtų būti keturi skyriai.
1. Pirkimo užbaigimo skyriaus konteinerio modulyje įtraukite dovanų kortelės, lojalumo taškų ir kredito kortelės modulius. Taip užtikrinate, kad viename skyriuje kartu rodomi visi mokėjimo būdai.
1. Vietoje **Užsakymo suvestinė** įtraukite užsakymo suvestinės, užsakymo pateikimo ir raiškiojo turinio bloko modulius.
1. Raiškiojo turinio bloko modulyje įtraukite tokį tekstą: **Jei turite klausimų dėl užsakymo, kreipkitės numeriu 1-800-FABRIKAM.**
1. Vietoje **Pateikti užsakymą** įtraukite užsakymo pateikimo modulį.
1. Pasirinkite **Įrašyti**. Kai kurie moduliai peržiūroje gali būti neatvaizduoti, nes jie neturi krepšelio konteksto.
1. Fragmentą įrašykite ir atrakinkite bei publikuokite.
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
