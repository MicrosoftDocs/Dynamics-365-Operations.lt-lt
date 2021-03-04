---
title: Pirkimo langelio modulis
description: Šioje temoje aprašomi pirkimo langelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: fa9d42c20540f2ee2240cc4f2b180140c3f9a628
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517093"
---
# <a name="buy-box-module"></a>Pirkimo langelio modulis

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi pirkimo langelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūrėti

Terminas *pirkimo langelis* paprastai reiškia produkto išsamios informacijos puslapio matomąją sritį, kurioje pateikiama visa svarbiausia informacija, kurios reikia norint įsigyti produktą. (Matomoji sritis yra matoma pirmą kartą įkėlus puslapį, kad ją vartotojai matytų neturėdami slinkti žemyn.)

Pirkimo langelio modulis yra specialus konteineris, kuriame laikomi visi moduliai, rodomi produkto išsamios informacijos puslapio pirkimo langelio srityje.

Produkto išsamios informacijos puslapio URL adrese yra produkto ID. Iš šio produkto ID išvedama visa informacija, kurios reikia norint atvaizduoti pirkimo langelio modulį. Jei produkto ID nėra nurodytas, pirkimo langelio modulis nebus tinkamai vaizduojamas puslapyje. Todėl pirkimo langelio modulį galima naudoti tik tuose puslapiuose, kurie turi produkto kontekstą. Norėdami naudoti jį puslapyje, kuriame nėra produkto konteksto (pavyzdžiui, pagrindinis puslapis arba rinkodaros puslapis), turite atlikti papildomus tinkinimus.

Toliau pateiktame paveikslėlyje parodytas produkto informacijos puslapyje esančio pirkimo langelio modulio pavyzdys.

![Pirkimo langelio modulio pavyzdys](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a>Pirkimo langelio modulio ypatybės ir vietos 

Produkto išsamios informacijos puslapyje pirkimo langelis yra padalytas į dvi sritis: medijos sritį kairėje ir turinio sritį dešinėje. Numatyta, kad medijos srities stulpelio pločio ir turinio srities stulpelio pločio santykis yra 2:1. Mobiliuosiuose įrenginiuose šios dvi sritys yra sudėtos į šūsnį, kad viena sritis būtų rodoma po kita sritimi. Temas galima naudoti stulpelių pločiams ir rietuvės vertinimui tinkinti.

Pirkimo laukelio modulis suteikia produkto pavadinimą, aprašymą, kainą ir vertinimus. Jis taip pat leidžia klientams pasirinkti produkto variantus su skirtingais produkto atributais, pavyzdžiui, dydžio, stiliaus ir spalvos. Pasirinkus kokį nors produkto variantą, atnaujinamos kitos pirkimo langelyje esančios ypatybės (pavyzdžiui, produkto aprašas ir vaizdai), kad atitiktų varianto informaciją. 

Kiekio parinkiklis pateikiamas, kad klientai galėtų nurodyti perkamų prekių kiekį. Maksimalus kiekis, kurį galima nusipirkti, gali būti apibrėžtas svetainės parametruose.

Pirkimo laukelyje klientai gali atlikti tokius veiksmus, kaip produkto pridėjimas prie krepšelio, produkto pridėjimas prie pageidavimų sąrašo ir paėmimo vietos pasirinkimas. Šiuos veiksmus galima atlikti su produktu arba produkto variantu. Norėdamas įtraukti produktą į pageidavimų sąrašą, klientas turi būti prisijungęs.

Temos gali būti naudojamos norint pašalinti arba pakeisti pirkimo langelio produkto ypatybių ir veiksmų valdiklių tvarką. 

## <a name="module-properties"></a>Modulio ypatybės

- **Antraštės skirtukas** – ši ypatybė nurodo produkto pavadinimo antraštės skirtuką. Jei pirkimo langelis yra puslapio viršuje, ši ypatybė turi būti nustatyta kaip **h1**, kad atitiktų pritaikymo neįgaliesiems standartus. 

- **Įjungti „apsipirkti panašia mada“ rekomendacijas** – ši ypatybė leidžia pirkimo langelį, kad būtų rodomi saitai su produktus, kurie panašūs į šiuo metu peržiūrimą prekę. Ši funkcija pasiekiama 10.0.13 arba vėlesnio leidimo „Commerce“.

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moduliai, kuriuos galima naudoti pirkimo langelio modulyje

- **Medijos galerija** – naudojant šį modulį, produkto išsamios informacijos puslapyje demonstruojami produkto vaizdai. Dėl daugiau informacijos apie šį modulį, žr. [Medijos galerijos modulis](media-gallery-module.md).
- **Parduotuvės parinkiklis** – naudojant šį modulį rodomas netoliese esančių parduotuvių, kuriose galima atsiimti prekę, sąrašas. Jis leidžia vartotojams įvesti vietą, kad surastų netoliese esančias parduotuves. Norėdami gauti daugiau informacijos apie šį modulį, žr. [Parduotuvės parinkiklio modulis](store-selector.md).
- **„Social Share”** – šis modulis gali būti įtrauktas į pirkimo langelį, kad vartotojai galėtų bendrinti informaciją apie produktus socialiniuose tinkluose. Daugiau informacijos žr. [„Social Share” modulis](social-share-module.md).

## <a name="buy-box-module-settings"></a>Pirkimo langelio modulių parametrai

Dalyje **Svetainės parametrai \> Plėtiniai** galima konfigūruoti toliau pateiktus pirkimo langelio modulio parametrus:

- **Krepšelio eilutės kiekio riba** – ši ypatybė yra naudojama nurodyti maksimalų kiekvienos prekės skaičių, kurį galima įtraukti į krepšelį. Pavyzdžiui, pardavėjas gali nuspręsti, kad vienos operacijos metu galima parduoti tik 10 kiekvieno produkto vienetų.
- **Atsargos** – norėdami gauti informacijos apie atsargų parametrų taikymą, žr. [Atsargų parametrų taikymas](inventory-settings.md).
- **Įtraukite produktą į vežimėlį** - Ši ypatybė yra naudojama nurodyti elgesį po to, kai objektas yra įtrauktas į vežimėlį. Galimos vertė yra **Naršyti vežimėlio puslapyje**, **Nenaršyti vežimėlio puslapyje** ir **Rodyti pranešimą**. Kai vertė yra nustatyta į **Naršyti vežimėlio puslapyje**, vartotojai yra siunčiami į vežimėlio puslapį jiems įtraukus objektą. Kai vertė yra nustatyta į **Nenaršyti vežimėlio puslapyje**, vartotojai nėra siunčiami į vežimėlio puslapį jiems įtraukus objektą. Kai vertė yra nustatyta į **Rodyti pranešimą**, vartotojams yra rodomas pranešimo patvirtinimas ir jie gali tęsti naršyti produkto išsamios informacijos puslapyje. 

> [!IMPORTANT]
> **Įtraukti produktą į vežimėlį** saito nustatymai yra prieinami „Dynamics 365 Commerce“ 10.0.11 leidime. Jei atnaujinate iš senesnės „Dynamics 365 Commerce” versijos, turite rankiniu būdu atnaujinti failą appsettings.json. Instrukcijų, kaip atnaujinti failą appsettings.json, žr. [SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file). 

Toliau pateiktame paveikslėlyje parodytas „Fabrikam“ puslapyje esančio patvirtinimo pranešimo „Įtraukta į krepšelį“ pavyzdys.

![Pranešimo modulio pavyzdys](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a>„Commerce Scale Unit“ sąveika

Pirkimo langelio modulis produkto informaciją gauna naudodamas „Commerce Scale Unit“ programų kūrimo sąsajas (API). Visa informacija gaunama naudojant produkto išsamios informacijos puslapyje esantį produkto ID.

## <a name="add-a-buy-box-module-to-a-page"></a>Pirkimo langelio modulio įtraukimas į puslapį

Norėdami į naują puslapį įtraukti pirkimo langelio modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Eikite į **Fragmentai** ir tuomet pasirinkite **Naujas** tam, kad sukurtumėte naują fragmentą.
1. **Naujas fragmentas** teksto laukelyje pasirinkite **Pirkite dėžę** modulį.
1. Dalyje **Fragmento pavadinimas** įveskite pavadinimą **Pirkimo langelio fragmentas**, tada pasirinkite **Gerai**.
1. Pirkimo langelio modulio vietoje **Medijos galerija** pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Medijos galerija**, tada pasirinkite **Gerai**.
1. Pirkimo langelio modulio vietoje **Parduotuvės parinkiklis** pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Parduotuvės parinkiklis**, tada pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.
1. Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite **PDP šablonas** ir pasirinkite **Gerai**.
1. Vietoje **Pagrindinė dalis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Numatytasis puslapis**, tada pasirinkite **Gerai**.
1. Numatytojo puslapio vietoje **Pagrindinis** pasirinkite daugtaškio mygtuką (**...**) ir **Įtraukti fragmentą**.
1. Dialogo lange **Pasirinkti fragmentą** pasirinkite fragmentą **Pirkimo langelio fragmentas**, kurį sukūrėte anksčiau ir tuomet pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. Dialogo lange **Pasirinkti šabloną** pasirinkite šabloną **PDP šablonas**. Dalyje **Puslapio pavadinimas** įveskite **PDP puslapis**, tada pasirinkite **Gerai**.
1. Naujo puslapio vietoje **Pagrindinis** pasirinkite daugtaškio mygtuką (**...**) ir **Įtraukti fragmentą**.
1. Dialogo lange **Pasirinkti fragmentą** pasirinkite fragmentą **Pirkimo langelio fragmentas**, kurį sukūrėte anksčiau ir tuomet pasirinkite **Gerai**.
1. Puslapį įrašykite ir peržiūrėkite. Į peržiūros puslapio URL įtraukite užklausos eilutės parametrą **?productid=&lt;product id&gt;**. Taip peržiūros puslapis įkeliamas ir vaizduojamas naudojant produkto kontekstą.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį. Produkto išsamios informacijos puslapyje turėtų būti rodomas pirkimo langelis.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos apžvalga](starter-kit-overview.md)

[Parduotuvės išrinkiklio modulis](store-selector.md)

[Medijos galerijos modulis](media-gallery-module.md)

[Konteinerio modulis](add-container-module.md)

[Krepšelio modulis](add-cart-module.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Užsakymo patvirtinimo modulis](order-confirmation-module.md)

[Antraštės modulis](author-header-module.md)

[Poraštės modulis](author-footer-module.md)

[Bendrinimo socialiniuose tinkluose modulis](social-share-module.md)

[Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas](calculated-inventory-retail-channels.md)

[SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]