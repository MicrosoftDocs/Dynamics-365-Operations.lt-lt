---
title: Įtraukti parankinių piktogramą
description: Šioje temoje paaiškinama, kaip į savo svetainę įtraukti parankinių piktogramą.
author: bicyclingfool
manager: annbe
ms.date: 04/27/2020
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
ms.openlocfilehash: 2d95e8b799c3b89418657342868e0ec7e94a86f9
ms.sourcegitcommit: ce79fb570e299a26a644e29da7ceb5a57a1374e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/28/2020
ms.locfileid: "3295085"
---
# <a name="add-a-favicon"></a>Įtraukti parankinių piktogramą

[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip į savo svetainę įtraukti parankinių piktogramą.

## <a name="overview"></a>Peržiūrėti

Parankinių piktogrma yra mažas grafikos failas, rodomas žiniatinklio naršyklės skirtuke, adresų juostoje, naršymo retrospektyvoje, žymelėse, parankiniuose ir kitose vietose. Rekomenduojame parankinių piktogramą įtraukti į savo svetainę, nes ji vaizduoja ir sustiprina jūsų prekės ženklą bei jūsų svetainę padeda atskirti nuo kitų svetainių, kuriose lankosi jūsų klientai.

Nors į svetainę galima įtraukti kelias įvairių dydžių ir failų tipų parankinių piktogramas, šioje temoje parodyta, kaip įtraukti vieną parankinių piktogramą. Tačiau tas pats procesas ir vieta naudojami norint įtraukti daugiau parankinių piktogramų.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Parankinių piktogramos nusiuntimas į svetainės turto rinkinį

Norėdami parankinių piktogramą nusiųsti į savo svetainės turto rinkinį, atlikite tolesnius veiksmus.

1. Kairiojoje naršymo srityje pasirinkite **Medijos biblioteka**.
1. Komandų juostoje pasirinkite **įkelti \> Įkelti medijos elementus**.
1. Failų naršyklės lange eikite į parankinių piktogramos vaizdo failą, kurį norite įkelti, pasirinkite jį ir tada pasirinkite **Atidaryti**.
1. Dialogo lange **Įkelti medijos elementą** įveskite reikiamą pavadinimą ir alternatyvųjį tekstą.
1. Norėdami iš karto po nusiuntimo publikuoti vaizdą, pažymėkite žymės langelį **Publikuoti medijos elementus po įkėlimo**.

    > [!NOTE]
    > Jei nepasirenkate žymės langelio **Publikuoti medijos elementus po įkėlimo**, turite grįžti į puslapį **Medijos elementai** ir parankinių piktogramą patys publikuoti vėliau.

1. Pasirinkite **Gerai**.
1. Dešinėje esančioje ypatybių srityje nukopijuokite viešąjį parankinių piktogramos URL. Šį URL naudosite vėliau.

## <a name="create-the-html-for-your-favicon"></a>Jūsų parankinių piktogramos HTML kūrimas

Norėdami sukurti parankinių piktogramos HTML, naudokite tolesnę HTML eilutę. Atribute **href** **Public\_URL\_for\_your\_favicon** („viešasis parankinių piktogramos URL“) pakeiskite anksčiau nukopijuotu viešuoju URL.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-page-fragment-that-contains-a-metatag-for-your-favicon"></a>Puslapio fragmento, kuriame yra jūsų parankinių piktogramos metažymių, kūrimas

Norėdami sukurti puslapio fragmentą, kuriame yra jūsų parankinių piktogramos metažymių, atlikite tolesnius veiksmus.

1. Eikite į **Puslapio fragmentai** ir pasirinkite **Naujas**.
1. Dialogo lange **Naujas puslapio fragmentas** kaip modulį, kuriuo paremtas puslapio fragmentas, pasirinkite **Metažymės**.
1. Įveskite puslapio fragmento pavadinimą, tada pasirinkite **Gerai**.
1. Fragmento hierarchijos medyje pasirinkite antrinį elementą **Numatytosios metažymės**.
1. Dešiniosios srities dalyje **Metažymės** pasirinkite **Įtraukti** ir įveskite anksčiau sukurtą HTML eilutę, skirtą parankinių piktogramai. 
1. Pasirinkite **Baigti redagavimą**, o tada pasirinkite **Publikuoti**, kad publikuotumėte puslapio fragmentą.

## <a name="add-the-metatag-page-fragment-to-the-html-head-section-of-your-pages"></a>Metažymės puslapio fragmento įtraukimas į jūsų puslapių HTML antraštės sekciją

Norėdami įtraukti metažymės puslapio fragmentą į jūsų puslapių HTML **antraštės** sekciją, atlikite tolesnius veiksmus.

1. Eikite į **Šablonai**, atidarykite puslapių, į kuriuos norite įtraukti parankinių piktogramą, šabloną ir pasirinkite **Redaguoti**.
1. Šablonų hierarchijos medyje pasirinkite daugtaškio (**...**) mygtuką, esantį dešinėje konteinerio **HTML antraštė** pusėje, ir pasirinkite **Įtraukti puslapio fragmentą**.
1. Dialogo lange **Pasirinkti puslapio fragmentą** pasirinkite anksčiau sukurtą metažymės puslapio fragmentą ir pasirinkite **Gerai**.
1. Pasirinkite **Baigti redagavimą**, o tada pasirinkite **Publikuoti**, kad publikuotumėte šabloną.

> [!NOTE]
> Jei jūsų svetainė naudoja daugiau nei vieną šabloną, turite įtraukti metažymės puslapio fragmentą į visus juos.

Kai peržiūrite puslapius, pagrįstus šablonu, į kurį įtraukėte metažymės puslapio fragmentą, matysite parankinių piktogramą naršyklės skirtuke.

## <a name="additional-resources"></a>Papildomi ištekliai

[Įtraukti logotipą](add-logo.md)

[Pasirinkti svetainės temą](select-site-theme.md)

[Darbas su CSS perrašymo failais](css-override-files.md)

[Įtraukti pasveikinimo pranešimą](add-welcome-message.md)

[Įtraukti informaciją apie autorių teises](add-copyright-notice.md)

[Kalbų įtraukimas į savo svetainę](add-languages-to-site.md)

[Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija](add-telemetry.md)

