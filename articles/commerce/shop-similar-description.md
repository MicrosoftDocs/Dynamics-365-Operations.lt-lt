---
title: Įgalinti "Parduotuvės panašių aprašymų" rekomendacijas
description: Šiame straipsnyje aprašoma, kaip įgalinti "pirkią panašią aprašą" produktų rekomendacijas Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: c15122d15660144f46528bd8c575029bf9d966c6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274984"
---
# <a name="enable-shop-similar-description-recommendations"></a>Rekomendacijų „pirkti su panašiu aprašymu“ įjungimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip įgalinti "parduotuvės panašios aprašymo" produkto rekomendacijas Microsoft Dynamics 365 Commerce.

„Panašios į parduotuvės aprašą“ rekomendacijų funkcija „Dynamics 365 Commerce“ naudoja dirbtinį intelektą ir mašininį mokymąsi (AI-ML) tam, kad pateiktų rekomendacijas produktams, kurių aprašai yra panašūs į kliento ieškomus. Padarydami „į parduotuvę panašų aprašą“ rekomendacijas prieinamas visiems mažmenos kanalams „Commerce“, mažmenos prekeiviai gali padėti klientams nesunkiai surasti jų norimus dalykus.

Funkcija „panašių į parduotuvės aprašą“ rekomendacijoms naudoja produkto pavadinimą ir matytų produktų aprašą siekiant surasti ir rekomenduojamus panašius produktus mažmeninių prekeivių produkto kataloge.

„Į parduotuvės aprašą panašios“ rekomendacijos yra prieinamos prekybos vietoje ir el. komercijos patirtyse.

## <a name="example-scenarios"></a>Scenarijų pavyzdžiai

Tolesnio pavyzdžio scenarijai rodo rekomendacijų tipus, kuriuos „į parduotuvės aprašą panašios“ funkcijos gali pateikti:

- Klientas mato retro stiliaus ragų formos porą ir gauna rekomendacijų rinkinį kitiems akiniams, kurie turi panašų dizainą mažmenos prekybininko pramonės kontekste.
- Klientas naudoja „į parduotuvę panašų aprašą“ rekomendacijas siekiant gauti kavos skonius, kurie yra panašūs į skonį, kurį anksčiau įsigijo iš mažmenininko.

## <a name="set-up-shop-similar-description-recommendations"></a>Nustatykite „į parduotuvės aprašą panašias“ rekomendacijas

Produkto rekomendacijos yra palaikomos tik „Commerce“ vartotojams, kurie perkėlė savo laikymus į „Azure Data Lake Storage“ Gen2.

### <a name="prerequisites"></a>Būtinieji komponentai

Prieš tai, kai „į parduotuvės aprašą panašios“ rekomendacijos gali būti rodomos klientams, turite užbaigti tolesnes išankstines sąlygas:

- [Įjungti produkto rekomendacijas](enable-product-recommendations.md) prekybos štabe.
- Patvirtinti, kad medijos serveris palaiko HTTPS skambučius.

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a>Įjunkite „į parduotuvės aprašą panašias“ rekomendacijų funkciją

Norėdami įjungti „į parduotuvės aprašą panašias“ rekomendacijas ir jų funkciją „Commerce“ būstinėje, atlikite šiuos žingsnius.

1. Darbo srityje **Funkcijų valdymas**, esamų funkcijų sąraše, ieškokite ir rinkitės **Į parduotuvę panašų aprašą**.
1. Dešiniojoje juostoje rinkitės **Įjungti**.

> [!NOTE]
> Jums įjungus funkciją, sistema pradeda kurti produkto rekomendacijų sąrašus. Gali užtrukti iki dienos, kol sąrašai bus prieinami ir matomi internete ir POS terminaluose.
>
> Jei išjungsite funkciją, kiti produkto rekomendacijų tipai paveikti nebus. Dėl išsamesnės informacijos apie produkto rekomendacijas, žr. [Produkto rekomendacijų apžvalga](product-recommendations.md).

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a>Įtraukti į parduotuvę panašaus aprašo mygtuką į parduotuvės išsamios informacijos puslapius

Jums įjungus į „parduotuvės aprašą panašias“ rekomendacijas ir jų funkciją „Commerce“ štabe, galite įtraukti **Į parduotuvę panašaus aprašo** mygtuką į įsigijimo laukelį bet kurio produkto išsamios informacijos puslapyje (PDP). Klientas pasirinkęs šį mygtuką yra nuvedamas į paskirtą **Į parduotuvę panašaus aprašą** puslapį, kuriame rodomi panašūs produktai. Klientas tada gali naudoti parinkiklius tolesniam produktų filtravimui.

Norėdami įtraukti **į parduotuvės aprašą panašų** mygtuką PDP naudodami „Commerce“ saito kūrimo įrankį, atlikite šiuos žingsnius.

1. Atverkite esantį vietos kūrimo įrankio puslapį, turintį įsigijimo laukelio modulį.
1. Kairėje naršymo juostoje pasirinkite įsigijimo laukelio modulį.
1. Dešiniojoje juostoje, rinkitės **Įjungti į parduotuvės aprašą panašią nuorodą** žymimą laukelį.
1. Pasirinkite **Įrašyti**.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį. Publikavus puslapį, PDP apims **Į parduotuvę panašaus aprašo** mygtuką.

Tolesnis paveikslėlis rodo **Įjungti į parduotuvę panašaus aprašo nuorodą** žymimą laukelį ir **Į parduotuvę panašaus aprašo** mygtuką PDP pavyzdyje saito kūrimo įrankyje.

![Įjunkite į parduotuvę panašaus aprašo nuorodą žymimame laukelyje ir į parduotuvę panašaus aprašo mygtuką PDP saito kūrimo įrankyje.](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Produktų rekomendacijų apžvalga](product-recommendations.md)

[„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje](enable-adls-environment.md)

[Įjungti produktų rekomendacijas](enable-product-recommendations.md)

[Įjungti „pirkti panašios išvaizdos“ rekomendacijas](shop-similar-looks.md)

[AI-ML rekomendacijų rezultatų koregavimas](modify-product-recommendation-results.md)

[Kuruojamų rekomendacijų kūrimas rankiniu būdu](create-editorial-recommendation-lists.md)

[DUK apie produktų rekomendacijas](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
