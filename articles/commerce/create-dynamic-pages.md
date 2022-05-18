---
title: Dinaminių el. prekybos puslapių kūrimas pagal URL parametrus
description: Šioje temoje aprašoma, kaip nustatyti „Microsoft Dynamics 365 Commerce“ e-komercijos puslapį, kuris gali pateikti dinaminį turinį pagal URL parametrus.
author: StuHarg
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 348fdb30f4d0104e80bea5235c1e337b9f977311
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694345"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a>Dinaminių el. prekybos puslapių kūrimas pagal URL parametrus

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip nustatyti „Microsoft Dynamics 365 Commerce“ e-komercijos puslapį, kuris gali pateikti dinaminį turinį pagal URL parametrus.

El. komercijos puslapis gali būti konfigūruotas siekiant talpinti kitą turinį pagal segmentą URL kelyje. Dėl to, puslapis yra žinomas kaip dinaminis puslapis. Segmentas yra naudojamas kaip parametras siekiant gauti puslapio turinį. Pavyzdžiui, puslapis pavadinimu **tinklaraščio\_rodinys** yra sukuriamas ir susiejamas su URL `https://fabrikam.com/blog`. Šis puslapis tuomet gali būti naudojamas siekiant rodyti kitą turinį pagal paskutinį segmentą URL kelyje. Pavyzdžiui, paskutinis segmentas URL `https://fabrikam.com/blog/article-1` yra **straipsnis-1**.

Atskiri kliento puslapiai, viršijantys dinaminį puslapį, gali būti taip pat siejami su segmentais URL kelyje. Pavyzdžiui, puslapis pavadinimu **tinklaraščio\_santrauka** yra sukuriamas ir susiejamas su URL `https://fabrikam.com/blog/about-this-blog`. Kai URL yra reikalaujamas, **tinklaraštis\_santrauka** puslapis yra susiejamas su **/apie-šį-blogą** parametru ir grąžinamas vietoje **tinklaraštis\_rodinys** puslapio.

> [!NOTE]
> Talpinimo, gavimo ir rodymo dinaminio puslapio funkcijos turinys yra įgyvendinamas naudojant tinkintą modulį. Dėl daugiau informacijos, žr. [Interneto kanalo plėtinys](e-commerce-extensibility/overview.md).

## <a name="set-up-a-dynamic-e-commerce-page"></a>Nustatykite dinaminį el. komercijos puslapį

Norėdami nustatyti dinaminį el. komercijos puslapį, privalote sukurti dinaminį puslapį, pagrindinį URL ir konfigūruoti maršrutą į dinaminį puslapį.

### <a name="create-the-page-that-will-serve-dynamic-content"></a>Kurkite puslapį, kuris bus naudojamas dinaminiam turiniui

Norėdami sukurti puslapį, kuris bus naudojamas dinaminiam turiniui, atlikite veiksmus [Įtraukti naują saito puslapį](add-new-page.md). Jūsų sukurtam puslapiui reikės modulio įgyvendinimo, kuris naudoja paskutinį URL kelio segmentą siekiant gauti turinį iš išorės duomenų šaltinio. Dėl daugiau informacijos apie tinkinto modulio kūrimą, žr. [Interneto kanalo plėtinys](e-commerce-extensibility/overview.md).

### <a name="create-the-base-url-for-the-dynamic-page"></a>Kurkite pagrindinį URL dinaminiam puslapiui

Norėdami kurti pagrindinį URL dinaminiam puslapiui „Commerce“ saito kūrimo įrankyje, vadovaukitės šiais žingsniais.

1. Eikite į **URL** ir rinkitės **Naujas \> Naujas URL**.
1. Teksto laukelyje **Kurti naują URL** rinkitės **Vidinis puslapis**. Skyriuje **URL kelias**, įveskite kelią, kuris bus naudojamas kaip dinaminio puslapio šaknis (šiuo atveju, **/tinklaraštis**). Tada rinkitės **Kitas**.
1. Teksto laukelyje **Rinktis puslapį** rinkitės laukelį, puslapį, kurį sukūrėte, kad jis palaikytų dinaminį puslapį ir tada **Įrašyti**.
1. Pasirinkite **Publikuoti**.

### <a name="configure-the-route-to-the-dynamic-page"></a>Konfigūruokite maršrutą dinaminiam puslapiui

Norėdami konfigūruoti maršrutą į dinaminį puslapį „Commerce“ saito kūrimo įrankyje, vadovaukitės šiais žingsniais.

1. Eikite į **Saito nustatymai \> Plėtiniai**.
1. Skyriuje **Parametrų URL keliai**, rinkitės **Įtraukti** ir tuomet įveskite URL kelią, kurį įvedėte kai sukūrėte URL (šiuo atveju, **/tinklaraštis**).
1. Rinkitės **įrašyti ir publikuoti**.

Po to, kai maršrutas sukonfigūruotas, visos užklausos URL keliui su parametrais grąžins puslapį, kuris yra susietas su tuo URL. Jei bet kokios užklausos turi papildomą segmentą, susietas puslapis bus grąžinamas, o puslapio turinys bus gaunamas naudojant segmentą kaip parametrą. Pavyzdžiui, `https://fabrikam.com/blog/article-1` grąžins **tinklaraščio\_santraukos** puslapį, o puslapio turinys bus gautas naudojant **/straipsnio-1** parametrą.

## <a name="override-a-parameterized-url-with-a-custom-page"></a>Viršys URL su parametru su tinkintu puslapiu

Norėdami viršyti URL su parametrais su tinkintu puslapiu „Commerce“ saito kūrimo įrankiu, vadovaukitės šiais žingsniais.

1. Eikite į **URL** ir rinkitės **Naujas \> Naujas URL**.
1. Teksto laukelyje **Kurti naują URL** rinkitės **Vidinis puslapis**. Skyriuje **URL kelias**, įveskite kelią, kuris įtraukia keistiną segmentą (šiuo atveju, **/tinklaraštis/apie-šį-tinklaraštį**). Tada rinkitės **Kitas**.
1. Teksto laukelyje **Rinktis puslapį** rinkitės tinkintą puslapį ir tada **Įrašyti**.
1. Pasirinkite **Publikuoti**.
1. Jei tinkintas puslapis dar nebuvo publikuotas, eikite į **Puslapiai**, rinkitės tinkintą puslapį ir tada **Publikuoti**.

Po tinkinto puslapio publikavimo, jis gali būti naudojamas vietoje dinaminio puslapio, kuris turi turinį su parametrais.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modifikuoti esamą svetainės puslapį](modify-existing-page.md)

[Įtraukti naują svetainės puslapį](add-new-page.md)

[Pasirinkti puslapių maketus](select-page-layouts.md)

[Tvarkyti SEO metaduomenis](manage-seo-metadata.md)

[Įrašyti, peržiūrėti ir publikuoti puslapį](save-preview-publish-page.md)

[Papildyti produkto puslapį](enrich-product-page.md)

[Papildyti kategorijos nukreipimo puslapį](enrich-category-page.md)

[Patikrinti puslapio turinio pritaikymą neįgaliesiems](verify-accessibility.md)

[Interneto kanalo išplečiamumas](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
