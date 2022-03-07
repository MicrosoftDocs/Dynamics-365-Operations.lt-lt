---
title: Įjunkite „parduotuvės panašaus aprašo“ rekomendacijas
description: Šioje temoje aprašoma, kaip įjungti „panašių į parduotuvės aprašą“ produkto rekomendacijas „Microsoft Dynamics 365 Commerce“.
author: bsokolov
manager: AnnBe
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b6b397b1f21e3dfcdb4a2b7fe67ddb541d090a97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234394"
---
# <a name="enable-shop-similar-description-recommendations"></a>Rekomendacijų „pirkti su panašiu aprašymu“ įjungimas

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip įjungti „panašių į parduotuvės aprašą“ produkto rekomendacijas „Microsoft Dynamics 365 Commerce“.

„Panašios į paruodutuvės aprašą“ rekomendacijų funkcija „Dynamics 365 Commerce“ naudoja dirbtinį intelektą ir mašininį mokymąsi (AI-ML) tam, kad pateiktų rekomendacijas produktams, kurių aprašai yra panašūs į kliento ieškomus. Padarydami „į parduotuvę panašų aprašą“ rekomendacijas prieinamas visiems mažmenos kanalams „Commerce“, mažmenos prekeiviai gali padėti klientams nesunkiai surasti jų norimus dalykus.

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

1. Darbo srtiyje **Funkcijų valdymas**, esamų funkcijų sąraše, ieškokite ir rinkitės **Į parduotuvę apanšų aprašą**.
1. Dešiniojoje juostoje rinkitės **Įjungti**.

> [!NOTE]
> Jums įjungus funkciją, sistema pradeda kurti produkto rekomendacijų sąrašus. Gali užtrukti iki dienos, kol sąrašai bus prieinami ir matomi internete ir POS terminaluose.
>
> Jei išjungsite funkciją, kiti produkto rekomendacijų tipai paveikti nebus. Dėl išsamesnės informacijos apie produkto rekomendacijas, žr. [Produkto rekomendacijų apžvalga](product-recommendations.md).

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a>Įtraukti į parduotuvę panašaus aprašo mygtuką į parduotuvės išsamios informacijos puslapius

Jums įjungus į „parduotuvės aprašą panašias“ rekomendacijas ir jų funkciją „Commerce“ štabe, galite įtraukti **Į parduotuvę panašaus aprašo** mygtuką į įsigijimo laukelį bet kurio produkto išsamios informacijos puslapyje (PDP). Klientas pasirinkęs šį mygtuką yra nuvedamas į paskirtą **Į parduotuvę panašaus aprašą** puslapį, kuriame rodomi panašūs produktai. Klientas tada gali naudoti parinkiklius tolesniam produktų filtravimui.

Norėdami įtrarukti **į parduotuvės aprašą panašų** mygtuką PDP naudodami „Commerce“ saito kūrimo įrankį, atlikite šiuos žingsnius.

1. Atverkite esantį vietos kūrimo įrankio puslapį, turintį įsigijimo laukelio modulį.
1. Kairėje naršymo juostoje pasirinkite įsigijimo laukelio modulį.
1. Dešiniojoje juostoje, rinkitės **Įjungti į parduotuvės aprašą panašią nuorodą** žymimą laukelį.
1. Pasirinkite **Įrašyti**.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį. Publikavus puslapį, PDP apims **Į parduotuvę panašaus aprašo** mygtuką.

Tolesnis paveikslėlis rodo **Įjungti į parduotuvę panašaus aprašo nuorodą** žymimą laukelį ir **Į parduotuvę panašaus aprašo** mygtuką PDP pavyzdyje saito kūrimo įrankyje.

![Įjunkite į parduotuvę panašaus aprašo nuorodą žymimame laukelyje ir į parduotuvę panašaus aprašo mygtuką PDP saito kūrimo įrankyje](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Produktų rekomendacijų apžvalga](product-recommendations.md)

[„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje](enable-adls-environment.md)

[Įjungti produktų rekomendacijas](enable-product-recommendations.md)

[Įjungti „pirkti panašios išvaizdos“ rekomendacijas](shop-similar-looks.md)

[AI-ML rekomendacijų rezultatų koregavimas](modify-product-recommendation-results.md)

[Kuruojamų rekomendacijų kūrimas rankiniu būdu](create-editorial-recommendation-lists.md)

[DUK apie produktų rekomendacijas](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]