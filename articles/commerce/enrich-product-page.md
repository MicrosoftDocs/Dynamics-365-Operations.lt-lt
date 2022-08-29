---
title: Papildyti produkto puslapį
description: Šiame straipsnyje aprašoma, kaip papildyti produkto puslapį Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: f01dcc2518fe861339b4984522582ed3de7aa6ad
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282140"
---
# <a name="enrich-a-product-page"></a>Papildyti produkto puslapį

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip papildyti produkto puslapį Microsoft Dynamics 365 Commerce.

Pagal numatytuosius parametrus, jūsų svetainė naudoja bendrąjį puslapį, kad būtų rodomi produkto duomenys. Šiame puslapyje yra pagrindinė informacija apie produktą ir valdiklius, kurie reikalingi tą produktą parduoti. Tačiau galite papildyti informaciją, kuri gaunama iš „Commerce Scale Unit“, papildomais konkretaus produkto paveikslėliais arba tekstu. Šis procesas žinomas kaip produkto puslapio papildymas.

Daugeliu atvejų, norėsite naudoti konkretų papildomą turinį savo produktams. Nuėję į **„Retail“ ir „Commerce“** kūrimo įrankyje, matysite produktų sąrašą iš kanalo, kuris priskirtas svetainei. Šiame sąraše, stulpelis **Papildyta** nurodo, ar buvo papildytas produkto puslapis. Jei stulpelyje atsiranda varnelė, to produkto puslapis buvo papildytas. Jei varnelė atsiranda, produktui naudojamas numatytasis produkto puslapis ir turinys. Galite peržiūrėti ir papildytų, ir nepapildytų produkto puslapių, pasirinkdami produkto pavadinimą sąraše.

## <a name="enrich-a-product-page"></a>Papildyti produkto puslapį

Norėdami papildyti produkto puslapį, atlikite šiuos veiksmus.

1. Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).
1. Kairėje naršymo srityje pasirinkite **Produktai**.
1. Pasirinkite bet kokį produktą, kuris neturi papildyto produkto puslapio.
1. Veiksmų srityje spustelėkite **Papildyti produkto puslapį**.
1. Pasirinkite **PDP šablonas**, tada – **Gerai**.
1. Puslapio struktūros medyje kairėje išplėskite atkarpą **Pagrindinis**.
1. Pasirinkite prie atkarpos **Pagrindinis** esantį daugtaškio mygtuką (**...**), tada – **Įtraukti modulį**.
1. Pasirinkite **Konteineris 2**, tada pasirinkite **Gerai**.
1. Pasirinkite daugtaškio mygtuką dalyje **Konteineris 2** ir pasirinkite **Įtraukti modulį**.
1. Pasirinkite **Funkcija**, tada pasirinkite **Gerai**.
1. Dešinėje, srityje Ypatybės, lauke **Raiškusis tekstas**, įveskite atnaujintą produkto aprašą.
1. Lauke **Antraštė** įveskite antraštės tekstą ir pasirinkite **Gerai**.
1. Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.
1. Lauke **Komentarai** įveskite **Papildyti produktą** ir pasirinkite **Gerai**.
1. Norėdami peržiūrėti papildytą produkto puslapį, pasirinkite **Peržiūra**. Baigę uždarykite peržiūros skirtuką – grįšite į kūrimo įrankį.
1. Pasirinkite **Publikuoti**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modifikuoti esamą svetainės puslapį](modify-existing-page.md)

[Įtraukti naują svetainės puslapį](add-new-page.md)

[Pasirinkti puslapių maketus](select-page-layouts.md)

[Tvarkyti SEO metaduomenis](manage-seo-metadata.md)

[Įrašyti, peržiūrėti ir publikuoti puslapį](save-preview-publish-page.md)

[Papildyti kategorijos nukreipimo puslapį](enrich-category-page.md)

[Patikrinti puslapio turinio pritaikymą neįgaliesiems](verify-accessibility.md)

[Sukurti dinaminius e-komercijos puslapius pagal URL parametrus](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
