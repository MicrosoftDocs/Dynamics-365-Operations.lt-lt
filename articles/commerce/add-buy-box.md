---
title: Pirkimo langelio modulis
description: Šioje temoje aprašomi pirkimo langelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: 35b7027e0f0b680dd82ebfcea754fef1617c0163
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261403"
---
# <a name="buy-box-module"></a>Pirkimo langelio modulis


[!include [banner](includes/banner.md)]

Šioje temoje aprašomi pirkimo langelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūrėti

Terminas *pirkimo langelis* paprastai reiškia produkto išsamios informacijos puslapio matomąją sritį, kurioje pateikiama visa svarbiausia informacija, kurios reikia norint įsigyti produktą. (Matomoji sritis yra matoma pirmą kartą įkėlus puslapį, kad ją vartotojai matytų neturėdami slinkti žemyn.)

Pirkimo langelio modulis yra specialus konteineris, kuriame laikomi visi moduliai, rodomi produkto išsamios informacijos puslapio pirkimo langelio srityje.

Produkto išsamios informacijos puslapio URL adrese yra produkto ID. Iš šio produkto ID išvedama visa informacija, kurios reikia norint atvaizduoti pirkimo langelio modulį. Jei produkto ID nėra nurodytas, pirkimo langelio modulis nebus tinkamai vaizduojamas puslapyje. Todėl pirkimo langelio modulį galima naudoti tik tuose puslapiuose, kurie turi produkto kontekstą. Norėdami naudoti jį puslapyje, kuriame nėra produkto konteksto (pavyzdžiui, pagrindinis puslapis arba rinkodaros puslapis), turite atlikti papildomus tinkinimus.

## <a name="buy-box-module-properties-and-slots"></a>Pirkimo langelio modulio ypatybės ir vietos 

Produkto išsamios informacijos puslapyje pirkimo langelis yra padalytas į dvi sritis: medijos sritį kairėje ir turinio sritį dešinėje. Numatyta, kad medijos srities stulpelio pločio ir turinio srities stulpelio pločio santykis yra 2:1. Mobiliuosiuose įrenginiuose šios dvi sritys yra sudėtos į šūsnį, kad viena sritis būtų rodoma po kita sritimi. Temas galima naudoti stulpelių pločiams ir rietuvės vertinimui tinkinti.

Pirkimo laukelio modulis suteikia produkto pavadinimą, aprašymą, kainą ir vertinimus. Jis taip pat leidžia klientams pasirinkti produkto variantus su skirtingais produkto atributais, pavyzdžiui, dydžio, stiliaus ir spalvos. Pasirinkus kokį nors produkto variantą, atnaujinamos kitos pirkimo langelyje esančios ypatybės (pavyzdžiui, produkto aprašas ir vaizdai), kad atitiktų varianto informaciją. 

Kiekio parinkiklis pateikiamas, kad klientai galėtų nurodyti perkamų prekių kiekį. Maksimalus kiekis, kurį galima nusipirkti, gali būti apibrėžtas svetainės parametruose.

Pirkimo laukelyje klientai gali atlikti tokius veiksmus, kaip produkto pridėjimas prie krepšelio, produkto pridėjimas prie pageidavimų sąrašo ir paėmimo vietos pasirinkimas. Šiuos veiksmus galima atlikti su produktu arba produkto variantu. Norėdamas įtraukti produktą į pageidavimų sąrašą, klientas turi būti prisijungęs.

Temos gali būti naudojamos norint pašalinti arba pakeisti pirkimo langelio produkto ypatybių ir veiksmų valdiklių tvarką. 

## <a name="module-properties"></a>Modulio ypatybės

- **Antraštės skirtukas** – ši ypatybė nurodo produkto pavadinimo antraštės skirtuką. Jei pirkimo langelis yra puslapio viršuje, ši ypatybė turi būti nustatyta kaip **h1**, kad atitiktų pritaikymo neįgaliesiems standartus. 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moduliai, kuriuos galima naudoti pirkimo langelio modulyje

- **Medijos galerija** – naudojant šį modulį, produkto išsamios informacijos puslapyje demonstruojami produkto vaizdai. Jis gali palaikyti vieną ir daugiau vaizdų. Jis taip pat palaiko miniatiūrų vaizdus. Miniatiūrų vaizdus galima išdėstyti horizontaliai (kaip eilutę po vaizdu) arba vertikaliai (kaip stulpelį prie vaizdo). Medijos galerijos modulį galima įtraukti į pirkimo langelio modulio vietą **Medija**. Šiuo metu jis palaiko tik vaizdus. 
- **Parduotuvės parinkiklis** – naudojant šį modulį rodomas netoliese esančių parduotuvių, kuriose galima atsiimti prekę, sąrašas. Jis leidžia vartotojams įvesti vietą, kad surastų netoliese esančias parduotuves. Daugiau informacijos apie šį modulį žr. [Parduotuvės parinkiklio modulis](store-selector.md).

## <a name="buy-box-module-settings"></a>Pirkimo langelio modulių parametrai

Galima konfigūruoti tolesnius tris pirkimo langelio modulių parametrus einant į **Svetainės parametrai \> Plėtiniai**:

- **Maksimalus kiekis** – ši ypatybė yra naudojama nurodyti maksimalų kiekvienos prekės skaičių, kurį galima įtraukti į krepšelį. Pavyzdžiui, pardavėjas gali nuspręsti, kad vienos operacijos metu galima parduoti tik 10 kiekvieno produkto vienetų.
- **Atsargų patikra** – kai reikšmė nustatoma kaip **Teisinga**, prekė į krepšelį įtraukiama tik tada, kai pirkimo langelio modulis užtikrina, kad yra jos atsargų. Ši atsargų patikra atliekama tose situacijose, kai prekė bus siunčiama, ir situacijose, kai ji bus atsiimama iš parduotuvės. Jei reikšmė nustatoma kaip **Klaidinga**, prieš prekę įtraukiant į krepšelį ir pateikiant užsakymą atsargos nepatikrinamos. Informacijos apie tai, kaip sukonfigūruoti atsargų parametrus įmonės padalinyje, žr. [Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas](calculated-inventory-retail-channels.md).

- **Atsargų buferis** – ši ypatybė naudojama norint nurodyti atsargų buferio skaičių. Atsargos tvarkomos realiuoju laiku ir dideliam klientų skaičiui teikiant užsakymus gali būti sudėtinga turėti tikslų atsargų skaičių. Jei, tikrinant atsargas, jų yra mažiau nei buferio suma, laikoma, kad produkto atsargų nėra. Todėl greitai pardudodant keliais kanalais, kai ne visiškai sinchronizuojamas atsargų kiekis, yra mažiau rizikos, kad bus parduota prekė, kurios atsargų nėra.

## <a name="commerce-scale-unit-interaction"></a>„Commerce Scale Unit“ sąveika

Pirkimo langelio modulis produkto informaciją gauna naudodamas „Commerce Scale Unit“ API sąsajas. Visa informacija gaunama naudojant produkto išsamios informacijos puslapyje esantį produkto ID.

## <a name="add-a-buy-box-module-to-a-page"></a>Pirkimo langelio modulio įtraukimas į puslapį

Norėdami į naują puslapį įtraukti pirkimo langelio modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Sukurkite fragmentą pavadinimu **pirkimo langelio fragmentas** ir į jį įtraukite pirkimo langelio modulį.
1. Pirkimo langelio modulio vietoje **Medija** įtraukite medijos galerijos modulį.
1. Į pirkimo langelio modulio atkarpą **Parduotuvės parinkiklis** įtraukite parduotuvės parinkiklio modulį.
1. Puslapį įrašykite ir atrakinkite bei publikuokite.
1. Sukurkite produkto išsamios informacijos puslapio šabloną ir jį pavadinkite **PIIP šablonas**.
1. Įtraukite numatytąjį puslapį.
1. Numatytojo puslapio vietoje **Pagrindinis** įtraukite pirkimo langelio fragmentą.
1. Įrašykite šabloną, baikite redagavimą ir publikuokite.
1. Naudodami ką tik sukurtą šabloną, sukurkite puslapį, pavadintą **PIIP puslapis**.
1. Naujo puslapio vietoje **Pagrindinis** įtraukite pirkimo langelio fragmentą.
1. Puslapį įrašykite ir peržiūrėkite. Į peržiūros puslapio URL įtraukite užklausos eilutės parametrą **?productid=&lt;product id&gt;**. Taip peržiūros puslapis įkeliamas ir vaizduojamas naudojant produkto kontekstą.
1. Įrašykite puslapį, baikite redagavimą ir publikuokite. Produkto išsamios informacijos puslapyje turėtų būti rodomas pirkimo langelis.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Parduotuvės išrinkiklio modulis](store-selector.md)

[Konteinerio modulis](add-container-module.md)

[Krepšelio modulis](add-cart-module.md)

[Krepšelio piktogramos modulis](cart-icon-module.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Užsakymo patvirtinimo modulis](order-confirmation-module.md)

[Antraštės modulis](author-header-module.md)

[Poraštės modulis](author-footer-module.md)

[Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas](calculated-inventory-retail-channels.md)
