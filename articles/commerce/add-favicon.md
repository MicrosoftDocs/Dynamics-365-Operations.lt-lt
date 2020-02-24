---
title: Įtraukti parankinių piktogramą
description: Šioje temoje paaiškinama, kaip į savo svetainę įtraukti parankinių piktogramą.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 287663817232e7ce86e8fdb1fb5c2fcfeed33d20
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001547"
---
# <a name="add-a-favicon"></a>Įtraukti parankinių piktogramą


[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip į savo svetainę įtraukti parankinių piktogramą.

## <a name="overview"></a>Peržiūrėti

Parankinių piktogrma yra mažas grafikos failas, rodomas žiniatinklio naršyklės skirtuke, adresų juostoje, naršymo retrospektyvoje, žymelėse, parankiniuose ir kitose vietose. Rekomenduojame parankinių piktogramą įtraukti į savo svetainę, nes ji vaizduoja ir sustiprina jūsų prekės ženklą bei jūsų svetainę padeda atskirti nuo kitų svetainių, kuriose lankosi jūsų klientai.

Nors į svetainę galima įtraukti kelias įvairių dydžių ir failų tipų parankinių piktogramas, šioje temoje parodyta, kaip įtraukti vieną parankinių piktogramą. Tačiau tas pats procesas ir vieta naudojami norint įtraukti daugiau parankinių piktogramų.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Parankinių piktogramos nusiuntimas į svetainės turto rinkinį

Norėdami parankinių piktogramą nusiųsti į savo svetainės turto rinkinį, atlikite tolesnius veiksmus.

1. Nueikite į **Turtas \> Nusiųsti \> Nusiųsti turtą**.
1. Suraskite ir pasirinkite parankinių piktogramą vietinėje failų sistemoje.
1. Įveskite pavadinimą ir pasirinkite **Gerai**. 
1. Dešinėje esančioje ypatybių srityje nukopijuokite viešąjį parankinių piktogramos URL.

> [!NOTE]
> Jei nepasirenkate parinkties **Nusiųstą turtą publikuoti**, turite grįžti į puslapį **Turtas** ir parankinių piktogramą patys publikuoti vėliau.

## <a name="create-the-html-for-the-favicon"></a>Parankinių piktogramos HTML kūrimas

Norėdami sukurti parankinių piktogramos HTML, naudokite tolesnį HTML fragmentą. Atribute **href** **"Public\_URL\_for\_your\_favicon"** („viešasis parankinių piktogramos URL“) pakeiskite anksčiau nukopijuotu viešuoju URL.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a>Parankinių piktogramos HTML įtraukimas į puslapių elementą \<head\>

Norėdami į savo svetainę įtraukti parankinių piktogramą, naudokite tą pačią procedūrą, kurią naudojant į jūsų svetainės puslapių elementą **\<head\>** įtraukiamas bet kokio tipo HTML ar scenarijus.

## <a name="additional-resources"></a>Papildomi ištekliai

[Įtraukti logotipą](add-logo.md)

[Pasirinkti svetainės temą](select-site-theme.md)

[Darbas su CSS perrašymo failais](css-override-files.md)

[Įtraukti pasveikinimo pranešimą](add-welcome-message.md)

[Įtraukti informaciją apie autorių teises](add-copyright-notice.md)

[Kalbų įtraukimas į savo svetainę](add-languages-to-site.md)

[Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija](add-telemetry.md)

