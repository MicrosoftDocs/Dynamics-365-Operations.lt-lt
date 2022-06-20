---
title: El. komercijos skaitmeninės dovanų kortelės
description: Šiame straipsnyje aprašoma, kaip skaitmeniniai dovanų kortelės veikia "el. komercijos" diegimo metu Microsoft Dynamics 365 Commerce. Taip pat, tema apžvelgia svarbius konfigūravimo veiksmus.
author: anupamar-ms
ms.date: 05/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 60de6988f14a0dcbbb881e84a9e4d8a45ca1289a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884909"
---
# <a name="e-commerce-digital-gift-cards"></a>El. komercijos skaitmeninės dovanų kortelės

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip skaitmeniniai dovanų kortelės veikia "el. komercijos" diegimo metu Microsoft Dynamics 365 Commerce. Taip pat, tema apžvelgia svarbius konfigūravimo veiksmus.

„Dynamics 365 Commerce“, skaitmeninių kortelių dovanų kortelės vadovaujasi ta pačia eiga kaip ir kitų produktų sistemoje pirkimas. Nereikia konfigūruoti jokių kitų papildomų modulių. Jei kelios dovanų kortelės yra įtraukiamos į vežimėlį, dovanų kortelės prekės nėra apibendrinamos vienoje pardavimų eilutėje. Toks elgesys yra būtinas, nes kiekviena pardavimų eilutė yra įtraukiama į sąskaitą naudojant atskirą dovanų kortelės numerį.

Skaitmeninių dovanų kortelių įsigijimas yra palaikomas „Dynamics 365 Commerce“ 10.0.16 versijoje ir vėlesnėse.

Tolesnis paveikslėlis rodo produkto išsamios informacijos puslapio (PDF) pavyzdį skaitmeninei dovanų kortelei „Fabrikam“ el. komercijos saite.

![PDP dovanų kortelės pavyzdys „Fabrikam“ elektroninės prekybos saite.](./media/GiftcardPDP.PNG)

## <a name="turn-on-the-digital-gift-card-feature-in-commerce-headquarters"></a>Įjunkite skaitmeninės dovanų kortelės funkciją „Commerce“ būstinėje

Tam, kad pirkimo eiga skaitmeninėms dovanų kortelėms veiktų „Dynamics 365 Commerce“, **Pirkimo dovanų kortelė el. komercijos funkcijoje** funkcija turi būti įjungta „Commerce“ būstinėje. Galite rasti funkciją **Funkcijos valdymo** darbo srityje, esančioje „Commerce“ būstinėje, kaip parodyta tolesniame paveikslėlyje.

![Funkcijos valdymo darbo eiga „Commerce“ būstinėje.](./media/Featureflag.PNG)

## <a name="configure-a-digital-gift-card-in-commerce-headquarters"></a>Konfigūruoti skaitmeninės dovanų kortelės funkciją „Commerce“ būstinėje

Skaitmeninės kortelės prekės turi būti konfigūruotos „Commerce“ būstinėje. Procesas iliustruoja procesą kitiems produktams. Nepaisant to, tolesni svarbūs žingsniai yra konkretūs dovanų kortelių įsigijimo konfigūravimui. Dėl daugiau informacijos, kaip kurti ir konfigūruoti produktus, žr. [Kurti naują produktą „Commerce“](create-new-product-commerce.md).

- Jums konfigūruojant skaitmeninės dovanų kortelės produktus **Naujo produkto** teksto laukelyje, nustatykite **Produkto tipo** laukelį į **Paslaugos**. (Norėdami atverti teksto laukelį, eikite į **Mažmeninė prekyba ir komercija \> Produktai ir kategorijos \> Produktai pagal kategoriją** ir rinkitės **Naujas**.) Produktai pagal **Paslaugos** tipą nėra žymimi prieinamam inventoriui prieš padarant užsakymą. Dėl daugiau informacijos, žr. [Kurti naują produktą](create-new-product-commerce.md#create-a-new-product).
- Puslapyje **„Commerce“ parametrai** skirtuke **Publikavimas** laukelis **Dovanų kortelės produktas** turi būti nustatytas **Skaitmeninė dovanų kortelė**, kaip rodo tolesnis paveikslėlis. Jei produktas yra išorės dovanų kortelė, žr. [Parama išorės dovanų kortelėms](./dev-itpro/gift-card.md) dėl išsamesnės informacijos.

    ![Dovanų kortelės produkto laukelis „Commerce“ būstinėje.](./media/PostGiftcard.png)

- Jei dovanų kortelė turi būti palaikoma kelių iš anksto nustatytų sumų (pavyzdžiui, 25 $, 50 $ ir 100 $), **Dydžio** dimensija turi būti naudojama siekiant nustatytas iš anksto nustatytas sumas. Kiekviena iš anksto nustatyta suma bus produkto variantas. Dėl daugiau informacijos, žr. [Produkto dimensijos](../supply-chain/pim/product-dimensions.md?toc=%2fdynamics365%2fretail%2ftoc.json).
- Jei klientams be iš anksto nustatytų sumų turi būti suteikta galimybė nurodyti pasirinktinę dovanų kortelės sumą, pirmiausia nustatykite variantą, pagal kurį bus leidžiama pasirinktinė suma. Dydžio atributas **palaiko** pasirinktinius sumos variantus. Tada kategorijos **puslapyje** Išleistus produktus atidarykite produktą ir **tada "Commerce** FastTab **·** **·**" nustatykite kainos rakto lauką kaip Turi įvesti naują kainą, kaip parodyta toliau pateiktame pavyzdyje. Šis nustatymas užtikrina, kad klientai galės įvesti kainą naršydami produktą PDP.

    ![Raktas kainos laukelyje „Commerce“ būstinėje.](./media/KeyInPrice.png)
    
    Šiame pavyzdyje pateikiamas skaitmeninių dovanų kortelių produktų variantų sąrašas "Commerce Headquarters", įskaitant du pasirinktinius kainų variantus.
    ![Skaitmeninių dovanų kortelių produktų variantai su pasirinktinio kainos varianto pavyzdžiu](./media/DigitalGiftCards_ProductVariantsWithCustom.png)

- Pristatymo būdas skaitmeninei dovanų kortelei turi būti nustatytas į **Elektroninį**. Puslapyje **Pristatymo būdai** (**Mažmeninė prekyba ir komercija \> Kanalo nustatymai \> Pristatymo būdai**), rinkitės **Elektroninį** pristatymo būdą sąrašo juostoje ir tuomet įtraukite skaitmeninį dovanų kortelės produktą į tinklelį **Produktai** „FastTab“, kaip parodyta tolesniame paveikslėlyje. Dėl daugiau informacijos, žr. [Nustatyti pristatymo būdus](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

    ![Skaitmeninės kortelės prekės Pristatymo būdo puslapyje „Commerce“ būstinėje.](./media/ElectronicMode.PNG)
    
- Įsitikinkite, kad interneto funkcijos profilis buvo sukurtas ir susietas su jūsų interneto parduotuve „Commerce“ būstinėje. Funkcijų profilyje, nustatykite **Bendrinti produktus** parinktį į **Taip**. Šie nustatymai užtikrina, kad visos prekės, išskyrus dovanų korteles, bus subendrintos. Dėl daugiau informacijos, žr. [Kurti interneto funkcijos profilį](online-functionality-profile.md).
- Siekiant užtikrinti, kad klientai gaus el. laiškus įtraukus dovanų kortelę į sąskaitą, sukurkite naują el. laiško pranešimo tipą **El. laiško pranešimo profiliai** puslapyje ir nustatykite **El. laiško pranešimo tipo** laukelį į **Išduoti dovanų kortelę**. Dėl daugiau informacijos, žr. [Nustatyti el. laiško pranešimo profilį](email-notification-profiles.md).

## <a name="add-product-images-to-the-commerce-site-builder-media-library"></a>Įtraukit produkto paveikslėlius į „Commerce“ saito kūrimo įrankio medijos biblioteką

Privalote įtraukti produkto paveikslėlius skaitmeninės dovanų kortelės prekėms į „Commerce“ saito kūrimo įrankio medijos biblioteką. Įsitikinkite, kad dovanų kortelių paveikslėlio failų pavadinimai atitiktų jūsų saito pavadinimo konvencijas prekės paveikslėliams. Dėl daugiau informacijos, žr. [Įkelti paveikslėlius](dam-upload-images.md).

## <a name="configure-a-custom-amount-for-a-digital-gift-card-in-commerce-site-builder"></a>Konfigūruoti tinkintą sumą skaitmeninei dovanų kortelei „Commerce“ saito kūrimo įrankiui

Jei skaitmeninė dovanų kortelė yra konfigūruojama siekiant leisti kliento sumai, toks elgesys turi būti taip pat įgalintas [įsigyti laukelio modulį](add-buy-box.md), kuris yra naudojamas jūsų saito PDP. Įsigijimo laukelio modulis palaiko modulio konfigūravimą siekiant leisti kliento sumas. Galite taip pat nustatyti minimalias ir maksimalias sumas, kurios yra leidžiamos tinkintoms sumoms.

Norėdami konfigūruoti tinkintą sumą skaitmeninei kortelei „Commerce“ saito kūrimo įrankyje, atlikite šiuos veiksmus.

1. Eikite į įsigijimo laukelio modulį, kuris yra naudojamas jūsų saito PDP. Šis įsigijimo laukelio modulis gali būti įdiegtas fragmente, šablone ar puslapyje.
1. Pasirinkite **Redaguoti**.
1. Ypatybių juostoje dešinėje, rinkitės **Leisti tinkintą kainą** žymimą laukelį.
1. Pasirenkamas: Norėdami nustatyti minimalias ir maksimalias sumas tinkintoms sumoms, įveskite sumas **Minimalios kainos** ir **Maksimalios kainos** laukeliuose.
1. Pasirinkite **Baigti redagavimą** ir tada rinkitės **Publikuoti**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Pirkimo langelio modulis](add-buy-box.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Krepšelio modulis](add-cart-module.md)

[Naujo produkto kūrimas „Commerce“](create-new-product-commerce.md)

[Nustatyti pristatymo būdus](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Produktų dimensijos](../supply-chain/pim/product-dimensions.md?toc=%2fdynamics365%2fretail%2ftoc.json)

[El. paštu siunčiamo pranešimo šablono nustatymas](email-notification-profiles.md)

[Internetinių funkcijų šablono kūrimas](online-functionality-profile.md)

[Išorinių dovanų kortelių palaikymas](./dev-itpro/gift-card.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
