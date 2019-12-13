---
title: Pirkimo langelio modulis
description: Šioje temoje aprašomi pirkimo langelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e86b1881e6829ccc33f36ada453af20c1815a2fa
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811146"
---
# <a name="buy-box-module"></a>Pirkimo langelio modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašomi pirkimo langelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūrėti

Terminas *pirkimo langelis* paprastai reiškia produkto išsamios informacijos puslapio matomąją sritį, kurioje pateikiama visa svarbiausia informacija, kurios reikia norint įsigyti produktą. (Matomoji sritis yra matoma pirmą kartą įkėlus puslapį, kad ją vartotojai matytų neturėdami slinkti žemyn.)

Pirkimo langelio modulis yra specialus konteineris, kuriame laikomi visi moduliai, rodomi produkto išsamios informacijos puslapio pirkimo langelio srityje.

Produkto išsamios informacijos puslapio URL adrese yra produkto ID. Iš šio produkto ID išvedama visa informacija, kurios reikia norint atvaizduoti pirkimo langelio modulį. Jei produkto ID nėra nurodytas, pirkimo langelio modulis nebus tinkamai vaizduojamas puslapyje. Todėl pirkimo langelio modulio negalima naudoti jokiame puslapyje, kuriame nėra produkto konteksto (pavyzdžiui, pagrindiniame puslapyje ar rinkodaros puslapyje).

## <a name="buy-box-module-properties-and-slots"></a>Pirkimo langelio modulio ypatybės ir vietos 

Kaip konteineris pirkimo langelio modulis valdo keletą pagrindinių ypatybių, pvz., plotį. Pločio parametru nustatoma, ar konteineryje esantys moduliai turi tilpti tame konteineryje, ar jie gali užpildyti ekraną.

Produkto išsamios informacijos puslapyje pirkimo langelis yra padalytas į dvi sritis: medijos sritį kairėje ir turinio sritį dešinėje. Šias dvi sritis vaizduoja pirkimo langelio modulio vietos. Kiekviena vieta yra iš anksto sukonfigūruojama taip, kad joje galėtų būti tik jos palaikomi konkretūs moduliai. Pavyzdžiui, vieta **Medija** palaiko tik medijos galerijos modulį.

Numatyta, kad medijos srities ir turinio srities stulpelių pločių santykis yra 2:1. Tačiau stulpelių pločius gali perrašyti tema. Be to, mobiliuosiuose įrenginiuose šios dvi sritys yra sudėtos į šūsnį, kad viena sritis būtų rodoma po kita sritimi.

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moduliai, kuriuos galima naudoti pirkimo langelio modulyje

- **Medijos galerija** – naudojant šį modulį, produkto išsamios informacijos puslapyje demonstruojami produkto vaizdai. Jis gali palaikyti vieną ir daugiau vaizdų. Jis taip pat palaiko miniatiūrų vaizdus. Miniatiūrų vaizdus galima išdėstyti horizontaliai (kaip eilutę po vaizdu) arba vertikaliai (kaip stulpelį prie vaizdo). Medijos galerijos modulį galima įtraukti į pirkimo langelio modulio vietą **Medija**. Šiuo metu jis palaiko tik vaizdus ir vaizdo įrašus.
- **Produkto pavadinimas** – naudojant šį modulį, produkto išsamios informacijos puslapyje rodomas produkto pavadinimas. Numatyta, kad naudojama antraštės žymė **H1**, tačiau pagal poreikį antraštės žymę galima pakeisti.
- **Produkto įvertis** – naudojant šį modulį rodomi įverčiai žvaigždutėmis, atsižvelgiant į tai, kaip produktą įvertino klientai. Pirkimo langelio modulis kiekvieno produkto įvertį gauna iš įverčių tarnybos.
- **Produkto kaina** – naudojant šį modulį rodoma produkto kaina. Į kainą įtraukiamos perbrauktosios kainos ir nuolaidos.
- **Produkto aprašas** – naudojant šį modulį rodomas produkto aprašas.
- **Produkto konfigūracija** – naudojant šį modulį rodomas produkto dydis, stilius ir matmenys. Matmenų išrinkiklius galima sudėti į šūsnį vertikaliai arba jie gali būti rodomi vienas šalia kito. Pasirinkus kokį nors produkto variantą, atnaujinamos kitos pirkimo langelyje esančios ypatybės (pavyzdžiui, produkto aprašas ir vaizdai), kad atitiktų varianto informaciją.
- **Produkto kiekis** – naudojant šį modulį konfigūruojamas produkto kiekis. Produkto ar varianto kiekis, kurį galima įtraukti į krepšelį, yra ribojamas parametru.
- **Įtraukti į krepšelį** – naudojant šį modulį atliekamas veiksmas „įtraukti į krepšelį“. Į krepšelį galima įtraukti tik produktą arba variantą. Kitaip tariant, bendrojo produkto į krepšelį įtraukti negalima. Modulyje yra ypatybė **Pereiti į krepšelį**, kurią gali nustatyti svetainės autorius. Kai ši ypatybė nustatoma kaip **Teisinga**, kiekvieną kartą, kai suaktyvinamas veiksmas „įtraukti į krepšelį“, vartotojas yra nukreipiamas į krepšelio puslapį. Kai ji nustatoma kaip **Klaidinga**, klientas, įtraukęs prekių į krepšelį, gali toliau naršyti produkto išsamios informacijos puslapyje.
- **Įtraukti į pageidavimų sąrašą** – naudojant šį modulį prekė įtraukiama į kliento pageidavimų sąrašą. Į pageidavimų sąrašą galima įtraukti tik produktą arba variantą. Be to, klientas turi būti prisijungęs prie svetainės. Modulyje naudojama klaidų apdorojimo logika, užtikrinanti, kad būtų tenkinamos abi šios sąlygos.
- **Rasti parduotuvėje** – naudojant šį modulį suaktyvinamas srautas „pirkimas internetu, atsiėmimas parduotuvėje“.
- **Atsiimti parduotuvėje** – naudojant šį modulį rodomas netoliese esančių parduotuvių, kuriose galima atsiimti prekę, sąrašas. Numatyta, kad šis modulis rodo parduotuves, kurios yra 50 mylių spinduliu nuo kliento vietos. Tačiau ieškos spindulį modulyje galima tinkinti. Jei yra įjungta atsargų tikrinimo funkcija, patikrinamos kiekvienos parduotuvės atsargos ir parodomas atitinkamas pranešimas apie atsargų buvimą arba nebuvimą.
- **Parduotuvių ieška naudojant „Bing“ žemėlapius** – šį modulį galima naudoti atsiėmimo parduotuvėje modulyje. Jį naudodami klientai gali ieškoti parduotuvių įvesdami vietą. Naudojant „Bing“ žemėlapių geokodavimo programų programavimo sąsają (API), nurodyta vieta konvertuojama į platumą ir ilgumą. Jei naudojamas šis modulis, rodomos tik tos parduotuvės, kurios yra netoli dabartinės kliento vietos, ir klientas kitos vietos ieškoti negali.
- **Raiškiojo turinio blokas** – naudojant šį modulį gali būti rodomas pranešimas, kurį svetainės autorius ar pardavėjas nori reklamuoti pirkimo langelyje, pvz., „Jei kyla problemų dėl užsakymo, kreipkitės numeriu 1-800-FABRIKAM“ arba „Didesni, nei 100 USD, užsakymai pristatomi nemokamai“. Pranešimai grindžiami turinio valdymo sistema (TVS).

## <a name="buy-box-module-settings"></a>Pirkimo langelio modulių parametrai

Galima konfigūruoti tolesnius tris pirkimo langelio modulių parametrus.

- **Maksimalus kiekis** – maksimalus kiekvienos prekės skaičius, kurį galima įtraukti į krepšelį. Pavyzdžiui, pardavėjas gali nuspręsti, kad vienos operacijos metu galima parduoti tik 10 kiekvieno produkto vienetų.
- **Atsargų patikra** – kai reikšmė nustatoma kaip **Teisinga**, prekė į krepšelį įtraukiama tik tada, kai pirkimo langelio modulis užtikrina, kad yra jos atsargų. Ši atsargų patikra atliekama tiek tose situacijose, kai prekė bus siunčiama, tiek tose situacijose, kai ji bus atsiimama iš parduotuvės. Jei reikšmė nustatoma kaip **Klaidinga**, prieš prekę įtraukiant į krepšelį ir pateikiant užsakymą atsargos nepatikrinamos.
- **Atsargų buferis** – atsargos tvarkomos realiuoju laiku ir dideliam klientų skaičiui teikiant užsakymus gali būti sudėtinga turėti tikslų atsargų skaičių. Todėl galima nustatyti atsargų buferį. Jei, tikrinant atsargas, jų yra mažiau nei buferio suma, laikoma, kad produkto atsargų nėra. Todėl greitai pardudodant keliais kanalais, kai ne visiškai sinchronizuojamas atsargų kiekis, yra mažiau rizikos, kad bus parduota prekė, kurios atsargų nėra.

## <a name="retail-server-interaction"></a>Sąveika su „Retail Server“

Pirkimo langelio modulis produkto informaciją gauna naudodamas „Retail Server“ API sąsajas. Visa informacija gaunama naudojant produkto išsamios informacijos puslapyje esantį produkto ID.

## <a name="add-a-buy-box-module-to-a-page"></a>Pirkimo langelio modulio įtraukimas į puslapį

Norėdami į naują puslapį įtraukti pirkimo langelio modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Sukurkite fragmentą pavadinimu **pirkimo langelio fragmentas** ir į jį įtraukite pirkimo langelio modulį.
1. Pirkimo langelio modulio vietoje **Medija** įtraukite medijos galerijos modulį.
1. Į pirkimo langelio modulio vietą **Turinys** įtraukite šiuos modulius: Produkto pavadinimas, Produkto įvertis, Produkto kaina, Produkto aprašas, Produkto konfigūracija, Įtraukti į krepšelį, Įtraukti į pageidavimų sąrašą ir Rasti parduotuvėje. Vietos **Turinys** modulius galite išdėstyti taip, kaip norite.
1. Pasirinkite modulį Rasti parduotuvėje. Šio modulio vietoje įtraukite atsiėmimo parduotuvėje modulį.
1. Atsiėmimo parduotuvėje modulio vietoje įtraukite parduotuvių ieškos naudojant „Bing“ žemėlapius modulį.
1. Puslapį įrašykite ir atrakinkite bei publikuokite.
1. Sukurkite produkto išsamios informacijos puslapio šabloną ir jį pavadinkite **PIIP šablonas**.
1. Įtraukite numatytąjį puslapį.
1. Numatytojo puslapio vietoje **Pagrindinis** įtraukite pirkimo langelio fragmentą.
1. Šabloną įrašykite ir atrakinkite bei publikuokite.
1. Naudodami ką tik sukurtą šabloną, sukurkite puslapį, pavadintą **PIIP puslapis**.
1. Naujo puslapio vietoje **Pagrindinis** įtraukite pirkimo langelio fragmentą.
1. Puslapį įrašykite ir peržiūrėkite. Į peržiūros puslapio URL įtraukite užklausos eilutės parametrą **?productid=&lt;product id&gt;**. Taip peržiūros puslapis įkeliamas ir vaizduojamas naudojant produkto kontekstą.
1. Puslapį įrašykite ir atrakinkite bei publikuokite. Produkto išsamios informacijos puslapyje turėtų būti rodomas pirkimo langelis.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Konteinerio modulis](add-container-module.md)

[Krepšelio modulis](add-cart-module.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Užsakymo patvirtinimo modulis](order-confirmation-module.md)

[Antraštės modulis](author-header-module.md)

[Poraštės modulis](author-footer-module.md)
