---
title: Įtraukti parankinių piktogramą
description: Šiame straipsnyje paaiškinama, kaip į savo svetainę įtraukti aniconą.
author: bicyclingfool
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 41d6d8f823c7364f9206fd0f7588e35b6f0a018a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270443"
---
# <a name="add-a-favicon"></a>Įtraukti parankinių piktogramą

[!include [banner](includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip į savo svetainę įtraukti aniconą.

Parankinių piktograma yra mažas grafikos failas, rodomas žiniatinklio naršyklės skirtuke, adresų juostoje, naršymo retrospektyvoje, žymelėse, parankiniuose ir kitose vietose. Rekomenduojame parankinių piktogramą įtraukti į savo svetainę, nes ji vaizduoja ir sustiprina jūsų prekės ženklą bei jūsų svetainę padeda atskirti nuo kitų svetainių, kuriose lankosi jūsų klientai.

Nors į savo svetainę galite įtraukti kelis įvairių dydžių ir rinkmenų tipus, šiame straipsnyje parodyta, kaip pridėti vieną oficoną. Tačiau tas pats procesas ir vieta naudojami norint įtraukti daugiau parankinių piktogramų.

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

## <a name="create-a-fragment-that-contains-a-metatag-for-your-favicon"></a>Fragmento, kuriame yra jūsų parankinių piktogramos metažymių, kūrimas

Norėdami sukurti fragmentą, kuriame yra jūsų parankinių piktogramos metažymių, atlikite tolesnius veiksmus.

1. Eikite į **Fragmentai** ir tuomet pasirinkite **Naujas**.
1. Dialogo lange **Naujas fragmentas** pasirinkite **Meta skirtukai**, kaip modulį, kuriuo remiasi fragmentas.
1. Įveskite fragmento pavadinimą, tada pasirinkite **Gerai**.
1. Fragmento hierarchijos medyje pasirinkite antrinį elementą **Numatytosios metažymės**.
1. Dešiniosios srities dalyje **Metažymės** pasirinkite **Įtraukti** ir įveskite anksčiau sukurtą HTML eilutę, skirtą parankinių piktogramai. 
1. Pasirinkite **Baigti redagavimą**, o tada pasirinkite **Publikuoti**, kad publikuotumėte fragmentą.

## <a name="add-the-metatag-fragment-to-the-html-head-section-of-your-pages"></a>Metažymės fragmento įtraukimas į jūsų puslapių HTML antraštės sekciją

Norėdami įtraukti metažymės fragmentą į jūsų puslapių HTML **antraštės** sekciją, atlikite tolesnius veiksmus.

1. Eikite į **Šablonai**, atidarykite puslapių, į kuriuos norite įtraukti parankinių piktogramą, šabloną ir pasirinkite **Redaguoti**.
1. Šablonų hierarchijos medyje pasirinkite daugtaškio (**...**) mygtuką, esantį dešinėje konteinerio **HTML antraštė** pusėje, ir pasirinkite **Įtraukti fragmentą**.
1. Dialogo lange **Pasirinkti fragmentą** pasirinkite meta skirtuko fragmentą, kurį sukūrėte anksčiau ir tuomet pasirinkite **Gerai**.
1. Pasirinkite **Baigti redagavimą**, o tada pasirinkite **Publikuoti**, kad publikuotumėte šabloną.

> [!NOTE]
> Jei jūsų svetainė naudoja daugiau nei vieną šabloną, turite įtraukti metažymės fragmentą į visus juos.

Kai peržiūrite puslapius, pagrįstus šablonu, į kurį įtraukėte metažymės fragmentą, matysite parankinių piktogramą naršyklės skirtuke.

## <a name="additional-resources"></a>Papildomi ištekliai

[Įtraukti logotipą](add-logo.md)

[Pasirinkti svetainės temą](select-site-theme.md)

[Darbas su CSS perrašymo failais](css-override-files.md)

[Įtraukti informaciją apie autorių teises](add-copyright-notice.md)

[Kalbų įtraukimas į savo svetainę](add-languages-to-site.md)

[Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
