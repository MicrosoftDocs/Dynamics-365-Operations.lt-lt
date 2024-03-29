---
title: Sparčiosios peržiūros modulis
description: Šiame straipsnyje aprašomi spartieji rodinio moduliai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 16f4b0aad803434f10a1c0ab8375552772ee534a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286870"
---
# <a name="quick-view-module"></a>Sparčiosios peržiūros modulis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomi spartieji rodinio moduliai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.

Greito rodinio modulis leidžia vartotojams greitai peržiūrėti produkto informaciją, kai jie naršo produktus sąrašo puslapyje ir įtraukia vieną ar daugiau produktų į vežimėlį iš sąrašo puslapio be poreikio eiti į produkto išsamios informacijos puslapį (PDP). Greito rodinio modulis pateikia produkto informacijos apžvalgą, dėl kurios vartotojai turi padaryti „pridėti prie vežimėlio“ sprendimą. Jis taip pat pateikia nuorodą į PDP tam, kad vartotojai galėtų peržiūrėti papildomą produkto informaciją ir pirkimo parinktis.

Greito rodinio modulis yra palaikomas [produkto kolekcijos](product-collection-module-overview.md) ir [paieškos rezultatų](search-result-module.md) modulių.

> [!IMPORTANT]
> Greito rodinio modulis yra prieinamas nuo „Commerce“ versijos 10.0.17 leidime.

Tolesnis paveikslėlis rodo greito rodinio modulio pavyzdžio produkto sąrašą puslapyje.

![Greito rodinio modulio produkto sąrašo puslapyje pavyzdys.](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a>Modulio ypatybės

Greito rodinio modulis palaiko kelias tas pačias funkcijas, tokias kaip pirkimo dėžutės modulis. Dėl to, greito rodinio modulio ypatybės rodo pirkimo dėžutės modulio ypatybes.

| Ypatybė | Reikšmės | aprašymas |
|----------------|--------|-------------|
| Antraštės žymė | **H1**, **H2**, **H3**, **H4**, **H5** ar **H6** | Šios ypatybės nustato antraštės skirtuką produkto pavadinimui. Jei greito rodinio modulis yra puslapio viršuje, ši ypatybė turi būti nustatyta į **H1** tam, kad atitiktų prieinamumo standartus. |
| Leisti pasirinktinę kainą | **Teisinga** arba **Klaidinga** | Jei ši ypatybė yra nustatyta į **Teisingą**, vartotojas gali įvesti tinkintą kainą. |
| Minimali kaina | Sveikasis skaičius | Ši ypatybė yra taikoma tik, jei **Leisti tinkintą kainą** ypatybė yra nustatyta į **Teisingą**. Ji nustato minimalią kainą, kurią vartotojas gali įvesti (pavyzdžiui, $1). |
| Maksimali kaina | Sveikasis skaičius | Ši ypatybė yra taikoma tik, jei **Leisti tinkintą kainą** ypatybė yra nustatyta į **Teisingą**. Ji nustato maksimalią kainą, kurią vartotojas gali įvesti (pavyzdžiui, $1,000). |

## <a name="commerce-site-builder-settings"></a>„Commerce“ saito kūrimo įrankio nustatymai

Kaip ir pirkimo laukelio modulis, greito rodinio modulis laikosi nustatymų **Saito nustatymai \> Plėtiniai \> Įtraukti produktą į vežimėlį**. Nepaisant to, **Naršyti į vežimėlio puslapį** nustatymai yra ignoruojami, nes jie nėra nenuoseklūs su greito rodinio modulio tikslu, kuris skirtas įjungti vartotojams galimybę naršyti keliuose produktuose puslapio sąraše ir įtraukti juos į vežimėlį neatsitraukiant nuo sąrašo puslapio.

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a>Įtraukite greito rodinio modulį į produkto kolekcijos modulį

Greito rodinio modulis gali būti įtrauktas į produkto kolekciją ir paieškos rezultatų modulius.

Norėdami įtraukti greito rodinio modulį į produkto kolekcijos modulį „Commerce“ saito kūrimo įrankyje, atlikite šiuos veiksmus.

1. Eikite į **Puslapiai** ir tada rinkitės pagrindinį puslapį „Fabrikam“ saite.
1. Eikite į **bet kurį produktų** rinkinio modulį pagrindiniame puslapyje, pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite modulį Spartusis **rodinys**, tada pasirinkite **Gerai**.
1. Ypatybių juostoje **Greito rodinio** modulyje rinkitės **Antraštė**. Teksto laukelyje **Antraštė** nustatykite **Antraštės lygio** laukelį į **H2** ir tada rinkitės **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Produktų atsiėmimo modulis](product-collection-module-overview.md)

[Ieškokite rezultatų modulio](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
