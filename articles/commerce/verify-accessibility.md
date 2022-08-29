---
title: Patikrinti puslapio turinio pritaikymą neįgaliesiems
description: Šiame straipsnyje aprašoma, kaip patikrinti puslapio turinio pasiekiamumą Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: retail
ms.search.form: ''
ms.openlocfilehash: 686ec37f24cf68902c4dd918c0ca8aea7612e1a9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291979"
---
# <a name="verify-page-content-accessibility"></a>Patikrinti puslapio turinio pritaikymą neįgaliesiems

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip patikrinti puslapio turinio pasiekiamumą Microsoft Dynamics 365 Commerce.

Baigę keisti puslapį, turėtumėte įsitikinti, kad turinys pasiekiamas visiems žiniatinklio vartotojams. Naudodami „Commerce“ kūrimo įrankius, galite lengvai patikrinti puslapio turinio pritaikymą neįgaliesiems integruotoje paslaugoje [„Microsoft Accessibility Insights“](https://accessibilityinsights.io/). Ši paslauga patikrina jūsų puslapio turinį pagal naujausias [Žiniatinklio konsorciumo W3C pritaikymo neįgaliesiems](https://www.w3.org/standards/webdesign/accessibility) gaires.

Prieš naudojant paslaugą [„Microsoft Accessibility Insights“](https://accessibilityinsights.io/), nuomotojo arba svetainės lygiu reikia įjungti jos integravimą.

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a>Paslaugos „Microsoft Accessibility Insights“ įjungimas visose nuomotojo svetainėse

Norėdami įjungti paslaugos [„Microsoft Accessibility Insights“](https://accessibilityinsights.io/) integravimą visose nuomotojo „Commerce“ svetainėse, atlikite toliau pateikiamus veiksmus.

> [!NOTE]
> Norėdami pasiekti nuomotojo parametrus, turite būti prisijungę prie „Commerce“ kaip sistemos administratorius.

1. Prisijunkite prie „Commerce“ kaip sistemos administratorius.
1. Kairiojoje naršymo srityje pasirinkite **Nuomotojo parametrai** (šalia krumpliaračio simbolio), kad juos išplėstumėte.
1. Dalyje **Nuomotojo parametrai** pasirinkite **Funkcijos**.
1. Nustatykite parinkties **Pritaikymo neįgaliesiems tikrinimas** vertę **Įjungta**.

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a>Paslaugos „Microsoft Accessibility Insights“ įjungimas vienoje svetainėje

Norėdami įjungti paslaugos [„Microsoft Accessibility Insights“](https://accessibilityinsights.io/) integravimą vienoje „Commerce“ svetainėje, atlikite toliau pateikiamus veiksmus.

1. Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).
1. Kairiojoje naršymo srityje pasirinkite ir išskleiskite **Svetainės parametrai**.
1. Dalyje **Svetainės parametrai** pasirinkite **Funkcijos**.
1. Nustatykite parinkties **Pritaikymo neįgaliesiems tikrinimas** vertę **Įjungta**.

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a>Pagrindinio puslapio turinio pritaikymo neįgaliesiems patikrinimas

Norėdami naudoti integruotą paslaugą [„Microsoft Accessibility Insights“](https://accessibilityinsights.io/), kad nuskaitytumėte ir patikrintumėte pagrindinio „Commerce“ puslapio turinį, atlikite toliau nurodytus veiksmus.

1. Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).
1. Kairiojoje naršymo srityje pasirinkite **Puslapiai**.
1. Raskite ir pasirinkite pagrindinį puslapį, kad jis būtų atidaromas puslapio rengyklėje.
1. Komandų juostoje pasirinkite **Tikrinti pritaikymą neįgaliesiems**. Atidaromas puslapis **Tikrinti pritaikymą neįgaliesiems**.
1. Nuskaitymui pasibaigus, peržiūrėkite ataskaitos turinį.
1. Jei kurių nors patikrinimų rezultatas neigiamas, pasirinkite elementus, kurių tikrinimo rezultatai neigiami, kad išplėstumėte elementus ir pamatytumėte daugiau informacijos.
1. Norėdami uždaryti ataskaitą ją peržiūrėję, slinkite į puslapio **Tikrinti pritaikymą neįgaliesiems** apačią ir pasirinkite **Gerai**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modifikuoti esamą svetainės puslapį](modify-existing-page.md)

[Įtraukti naują svetainės puslapį](add-new-page.md)

[Pasirinkti puslapių maketus](select-page-layouts.md)

[Tvarkyti SEO metaduomenis](manage-seo-metadata.md)

[Įrašyti, peržiūrėti ir publikuoti puslapį](save-preview-publish-page.md)

[Papildyti produkto puslapį](enrich-product-page.md)

[Papildyti kategorijos nukreipimo puslapį](enrich-category-page.md)

[Sukurti dinaminius e-komercijos puslapius pagal URL parametrus](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
