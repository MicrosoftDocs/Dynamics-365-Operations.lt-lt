---
title: Įtraukti naują svetainės puslapį
description: Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ įtraukti naują svetainės puslapį.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4a2ecc3ef3ff3f708cec50e42777b50ec4576e25
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797556"
---
# <a name="add-a-new-site-page"></a>Įtraukti naują svetainės puslapį

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ įtraukti naują svetainės puslapį.

Svetainei sukūrus šablonų ir fragmentų, kitas veiksmas yra pradėti kurti puslapius, kuriuose jie naudojami. Norėdami pradėti, turite pasirinkti šabloną arba maketą, puslapio pavadinimą ir puslapio URL.

## <a name="template-or-layout"></a>Šablonas arba maketas

Naujam puslapiui galite naudoti šabloną arba maketą. Norėdami gauti daugiau informacijos, žr. [Šablonų ir maketų apžvalga](templates-layouts-overview.md).

## <a name="page-name"></a>Puslapio pavadinimas

Jūsų puslapio pavadinimas turi būti unikalus. Jis turi būti aprašomasis, kad galėtumėte lengvai jį rasti ir kiti žmonės žinotų, kam puslapis skirtas. Puslapio pavadinimą pasirinkite atidžiai, nes jo negalima pakeisti vėliau.

## <a name="page-url"></a>Puslapio URL

Galite pasirinkti, kad būtų galima įvesti naujo puslapio URL. Sukūrę puslapį, galite įvesti eilutę, kuri bus naudojama visam URL sudaryti. Ši eilutė vadinama santykiniu URL arba kintamaisiais URL duomenimis. Tada pagal kintamuosius URL duomenis sugeneruojamas visas URL ir jam priskiriamas naujasis puslapis. Kintamuosius URL duomenis galite pakeisti vėliau, prieš publikuodami puslapį. Norėdami gauti daugiau informacijos, žr. [Puslapio URL sukūrimas](create-page-URL.md).

> [!NOTE]
> „Dynamics 365 Commerce“ atsieja URL adresus ir turinį. Kitaip tariant, galima sukurti puslapį, kuris nėra susietas su URL, ir URL, kuris nėra susietas su puslapiu. Todėl galima sukeisti URL turinį be prastovos ir lengviau valdyti peradresavimą.

## <a name="add-a-new-page"></a>Naujo puslapio įtraukimas

Norėdami į savo svetainę įtraukti naują puslapį, atlikite tolesnius veiksmus.

1. Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).
1. Pasirinkite **Naujas puslapis**.
1. Dialogo lange **Naujas puslapis** pasirinkite šabloną ir **Gerai**.
1. Lauke **Puslapio pavadinimas** įveskite puslapio pavadinimą, (pavyzdžiui, **Mano naujas puslapis**).
1. Lauke **URL** įveskite eilutę (kintamuosius URL duomenis), kad būtų įvestas visas URL (pavyzdžiui, **manonaujaspuslapis**).
1. Pasirinkite **Gerai**. Atidaroma puslapio rengyklė. Atkreipkite dėmesį, kad pagal jūsų pasirinktą šabloną antraštė ir poraštė yra automatiškai įtrauktos į puslapį.
1. Puslapio struktūroje pasirinkite vietą **Pagrindinis**, pasirinkite daugtaškio mygtuką (**...**) ir **Įtraukti modulį**.
1. Pasirinkite **Konteineris**, tada – **Gerai**.
1. Pasirinkite **Paslankusis konteineris**, tada – daugtaškio mygtuką ir **Įtraukti modulį**.
1. Pasirinkite **Raiškiojo turinio blokas** ir **Gerai**.
1. Pasirinkite **Raiškiojo turinio blokas**, tada – daugtaškio mygtuką ir **Įtraukti modulį**.
1. Pasirinkite **Raiškiojo turinio bloko elementas** ir **Gerai**.
1. Dešinėje esančioje ypatybių srityje pasirinkite **Pastraipa**, tada lauke įveskite **Mano bandomasis tekstas**.
1. Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.
1. Lauke **Komentarai** įveskite **Įtrauktas naujas puslapis** ir pasirinkite **Gerai**.
1. Norėdami peržiūrėti puslapį, pasirinkite **Peržiūra**. Baigę uždarykite peržiūros skirtuką – grįšite į kūrimo įrankį.
1. Pasirinkite **Publikuoti**.
1. Naršymo kelyje (kelio nuorodose) pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).
1. Kairėje esančioje naršymo srityje pasirinkite **URL adresai**.
1. Sąraše raskite ir pasirinkite savo URL (**manonaujaspuslapis**).
1. Pasirinkite **Publikuoti**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modifikuoti esamą svetainės puslapį](modify-existing-page.md)

[Pasirinkti puslapių maketus](select-page-layouts.md)

[Tvarkyti SEO metaduomenis](manage-seo-metadata.md)

[Įrašyti, peržiūrėti ir publikuoti puslapį](save-preview-publish-page.md)

[Papildyti produkto puslapį](enrich-product-page.md)

[Papildyti kategorijos nukreipimo puslapį](enrich-category-page.md)

[Patikrinti puslapio turinio pritaikymą neįgaliesiems](verify-accessibility.md)

[Sukurti dinaminius e-komercijos puslapius pagal URL parametrus](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
