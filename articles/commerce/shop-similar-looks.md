---
title: Įgalinti ""parduotuvės panašias atrodo" rekomendacijas
description: Šiame straipsnyje aprašoma, kaip įgalinti produktų rekomendacijas "panašus į parduotuvę"Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: 26eb436d889ac81cde730daca9b44d1deeda6c74
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282056"
---
# <a name="enable-shop-similar-looks-recommendations"></a>Įjungti „pirkti panašios išvaizdos“ rekomendacijas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip įgalinti "panašus į parduotuvę" produktų rekomendacijas Microsoft Dynamics 365 Commerce.

„Apsipirkti panašia mada“ rekomendacijų funkcija „Dynamics 365 Commerce“ naudoja dirbtinio intelekto galias ir mašinos mokymosi (AI-ML) tam, kad klientams pristatytų vizualiai panašių produktų rekomendacijas. Įjungus „apsipirkti panašia mada“ rekomendacijas prieinamas visiems mažmeniniams kanalams prekyboje, pardavėjai gali padidinti klientų pasitenkinimą padėdami jiems paprasčiau surasti jų norimas prekes.

„Apsipirkti panašia mada“ funkcijos rekomendacijos naudoja pagrindinių produkto variantų produkto paveikslėlius tam, kad surastų ir rekomenduotų vizualiai panašius produktus iš prekybininko produkto katalogo. 

„Apsipirkti panašia mada“ rekomendacijos yra prieinamas tiek prekybos vietoje (EKA), tiek ir el. prekybos patirtyse.

### <a name="example-scenarios"></a>Scenarijų pavyzdžiai

- Klientas peržiūri juodą dryžuotą megztinį ir gauna panašaus raudono megztinio rekomendaciją. Klientas pasirenka rekomenduojamą produktą, o ne originaliai peržiūrėtą produktą ir tuomet gauna panašių raudonų produktų rekomendacijas. 
- Klientas naudoja „apsipirkti panašia mada“ rekomendacijas tam, kad atrastų prie žiedo tinkančius auskarus, kuriuos jis nori įsigyti.

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a>Įjungti „apsipirkti panašia mada“ rekomendacijas prekybos štabe

Produkto rekomendacijas palaiko tik prekybos vartotojai, kurie perkėlė savo atsargas į „Azure Data Lake Gen2“.

### <a name="prerequisites"></a>Būtinieji komponentai

Prieš tai, kai pardavėjai gali pradėti rodyti „apsipirkti panašia mada“ rekomendacijas klientams, jie turi atlikti du išankstinių sąlygų žingsnius:

- [Įjungti produkto rekomendacijas](enable-product-recommendations.md) prekybos štabe.
- Patvirtinti, kad medijos serveris palaiko HTTPS skambučius.

Prekybininkai turi sukurti produkto URL rekomendacijoms variklio prieigai prie produkto paveikslėlių. Produkto URL sukūrimui prekybos štabe atlikite šiuos žingsnius.

1. Eikite į **Produkto paveikslėlius**.
1. Veiksmų juostoje pasirinkite **Nustatyti medijos šabloną**.
1. **Nustatyti medijos šabloną** ypatybių juostoje, **Medijos URL** pasirinkite **Kurti URL**.

> [!NOTE]
> Jums įjungiant „apsipirkti panašia mada“ rekomendacijos funkciją, pradedamas produkto rekomendacijų sąrašo kūrimas. Gali reikėti atnaujinti prieš tai, kai šie sąrašai bus prieinami ir matomi internete bei EKA terminaluose.

Tam, kad įjungtumėte „apsipirkti panašia mada“ rekomendacijas prekybos štabe, atlikite šiuos žingsnius.

1. Eikite į **Funkcijos valdymą**.
1. Prieinamų funkcijų sąraše ieškokite ir pasirinkite **Apsipirkti panašia mada**.
1. Dešinėje juostoje pasirinkite **Įjungti** tam, kad įjungtumėte paslaugą.

Tolesnis paveikslėlis rodo **Apsipirkti panašia mada** funkciją **Funkcijų valdymo** puslapyje prekybos štabe.

![Apsipirkti panašia mada funkcija funkcijų valdymo puslapyje prekybos štabe.](./media/enableshopsimilarlooks.png)

Užbaigus prieš tai aprašytus veiksmus, EKA terminalai automatiškai praplečiami su teksto **Apsipirkti panašia mada** juosta. Pasirinkę **Matyti daugiau**, EKA terminalo vartotojai gali būti nuvesti į paskirtą „apsipirkti panašia mada“ puslapį, kuris gali būti filtruojamas toliau.

> [!NOTE]
> Jei išjungiate „apsipirkti panašia mada“ rekomendacijų funkciją, jokie kiti produkto rekomendacijų tipai nebus paveikti. Dėl išsamesnės informacijos apie produkto rekomendacijas, žr. [Produkto rekomendacijų apžvalga](product-recommendations.md).

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a>Įtraukite apsipirkti panašia mada mygtuką į produkto išsamios informacijos puslapį naudodami komercijos vietos kūrimo įrankį.

Jums įjungus „apsipirkti panašia mada“ rekomendacijų funkciją prekybos štabe, prekybos vietos kūrimo įrankio parinktis leidžia prekybininkui įtraukti **Apsipirkti panašia mada** mygtuką į įsigijimo laukelį bet kurio produkto išsamios informacijos puslapyje (PDP). Klientas nustatęs šį mygtuką yra nuvedamas į paskirtą „apsipirkti panašia mada“ puslapį, kuris grįžta prie vizualiai panašių produktų. Ten klientas gali naudoti selektorius tolesniam produktų filtravimui.

Tam, kad įtrauktumėte **Apsipirkti panašia mada** mygtuką į PDP naudodami prekybos vietos kūrimo įrankį, atlikite šiuos veiksmus.

1. Atverkite esantį vietos kūrimo įrankio puslapį, turintį įsigijimo laukelio modulį.
1. Kairėje naršymo juostoje pasirinkite įsigijimo laukelio modulį.
1. Dešinėje naršymo juostoje, pasirinkite **Įjungti apsipirkimą panašia mada nurodą** žymimą laukelį.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį. Po to, kai puslapis yra išpublikuotas, PDP apims **Apsipirkti panašia mada** mygtuką.

Toliau pateiktas paveikslėlis rodo **Apsipirkti panašia mada nuorodos įjungimo** žymimą laukelį ir **Apsipirkti panašia mada** mygtuką PDP pavyzdyje vietos kūrimo įrankyje.

![Apsipirkti panašia mada nuorodos žymimas laukelis ir apsipirkti panašia mada mygtukas PDP vietos kūrimo įrankyje.](./media/SSLecomtooling.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Produktų rekomendacijų apžvalga](product-recommendations.md)

[„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje](enable-adls-environment.md)

[Įjungti produktų rekomendacijas](enable-product-recommendations.md)

[Personalizuotų rekomendacijų atsisakymas](personalization-gdpr.md)

[Produktų rekomendacijų įtraukimas į EKA](product.md)

[Rekomendacijų įtraukimas į operacijų ekraną](add-recommendations-control-pos-screen.md)

[AI-ML rekomendacijų rezultatų koregavimas](modify-product-recommendation-results.md)

[Kuruojamų rekomendacijų kūrimas rankiniu būdu](create-editorial-recommendation-lists.md)

[Rekomendacijų su demonstraciniais duomenimis kūrimas](product-recommendations-demo-data.md)

[DUK apie produktų rekomendacijas](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
