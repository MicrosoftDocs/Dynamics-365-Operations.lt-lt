---
title: Puslapio URL kūrimas
description: Šiame straipsnyje aprašoma pagrindinės svetainės puslapio URL kūrimo koncepcijos ir procedūros.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1798c4812b535ef007cbd5ff310b534e64a2f11e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892309"
---
# <a name="create-a-page-url"></a>Puslapio URL kūrimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma pagrindinės svetainės puslapio URL kūrimo koncepcijos ir procedūros.

Visą arba absoliutųjį URL, kuris nurodo į jūsų svetainės puslapį, sudaro atskiros dalys. Pavyzdžiui, URL `https://www.contoso.com/en-us/contactus` sudaro tolesnės dalys.

- `https://www.contoso.com` – HTTP protokolas ir svetainės domenas.
- `/en-us` – svetainės kalbos kelias.
- `/contactus` – santykinis puslapio **Susisiekite su mumis** URL. Santykinis URL taip pat vadinamas *kintamaisiais URL duomenimis*.

Svetainės domeną ir pasirenkamą kalbos kelią nustatote nustatydami svetainę. Daugiau domenų ir kalbos kelių į svetainę galite įtraukti svetainės parametrų dalyje esančiame internetinių parduotuvių puslapyje.

Kintamieji puslapio URL duomenys egzistuoja kaip atskiras objektas svetainės kūrimo aplinkoje. Puslapio URL sudaro dvi dalys: pavadinimas, nurodantis kintamuosius URL duomenis, ir puslapio, esančio jūsų arba išorinėje svetainėje, žymeklis. Puslapio URL taip pat galima sukonfigūruoti taip, kad jis peradresauotų į kitą puslapį, esantį jūsų arba išorinėje svetainėje.

## <a name="create-a-page-url"></a>Kurti puslapio URL

Toliau nurodyti du puslapių URL adresų kūrimo būdai.

- Automatiškai, kai kuriate puslapį
- Neautomatiškai, puslapyje **URL adresai**

### <a name="create-a-page-url-when-you-create-a-page"></a>Puslapio URL kūrimas kuriant puslapį

Jei kurdami naują puslapį lauke **URL** nurodote pavadinimą, puslapyje **URL adresai** automatiškai sukuriamas puslapio URL, nurodantis į tą puslapį. Publikavus URL ir puslapį, į kurį jis nurodo, svetainės vartotojai (jūsų klientai) gali pasiekti puslapį, susietą su URL.

> [!NOTE]
> Jei publikuojate URL nepublikuodami puslapio, į kurį jis nurodo, bandydami pasiekti puslapį svetainės vartotojai mato klaidą 404. Jei publikuojate puslapį nepublikuodami URL, kuris į jį nurodo, naudojant URL puslapio pasiekti negalima.

### <a name="manually-create-a-page-url"></a>Neautomatinis puslapio URL kūrimas

Kuriant naujus puslapius, nurodyti puslapio URL nereikia. Jei URL lauką paliekate tuščią, puslapis sukuriamas nesusietos būsenos. Šiuo atveju klientai puslapio negalės pasiekti, net jei jis publikuojamas. Norėdami, kad puslapis būtų pasiekiamas, turite patys sukurti URL ir jį susieti su puslapiu.

Norėdami patys sukurti puslapio URL, atlikite tolesnius veiksmus.

1. Puslapyje **URL adresai** pasirinkite **Naujas**.
1. Pasirinkite svetainės puslapį, kurį norite susieti su URL.
1. Įveskite kintamuosius URL duomenis ir pasirinkite **Gerai**.

Šiuo metu URL yra juodraščio būsenos. Kad svetainės vartotojai galėtų pasiekti susietą puslapį, jį reikia publikuoti.

## <a name="update-a-page-url"></a>Puslapio URL atnaujinimas

Norėdami atnaujinti puslapio URL paskirties puslapį, atlikite tolesnius veiksmus.

1. Puslapyje **URL adresai** pasirinkite atnaujintiną URL.
1. Dešinėje esančioje ypatybių srityje pasirinkite prie paskirties puslapio esantį daugtaškio mygtuką (**...**).
1. Dialogo lange pasirinkite kitą puslapį, tada – **Gerai**.
1. URL įrašykite ir publikuokite.

## <a name="redirect-a-page-url"></a>Puslapio URL peradresavimas

Kartais galite norėti, kad, pageidavę konkretaus URL, jūsų klientai peržiūrėtų kitą puslapį. Tokiais atvejais dažnai geriausia ir paprasčiausia yra pakeisti puslapį, į kurį nurodo puslapio URL. Tačiau galbūt naudodami HTTP 301 arba 3023 peradresavimą URL užklausas į kitą URL peradresuojate dėl pagrįstų priežasčių.

Norėdami URL peradresuoti į kitą URL, atlikite tolesnius veiksmus.

1. Puslapyje **URL adresai** pasirinkite atnaujintiną URL.
1. Dešinėje esančioje ypatybių srityje pasirinkite **Peradresuoti**.
1. Pasirinkite peradresavimo paskirties vietą.

    - Norėdami nurodyti į kitą svetainės puslapį, pasirinkite **Vidinis URL**, daugtaškio mygtuką (**...**) ir URL, į kurį norite peradresuoti.
    - Norėdami nukreipti į puslapį išorinėje svetainėje, pasirinkite **Išorinis URL** ir įveskite visą to puslapio URL. Būtinai įtraukite protokolą. Pavyzdžiui, įveskite `https://domain.com/new/page`. Jei URL jau peradresuoja į vidinį URL, įvesti išorinį URL galėsite tik pasirinkę **Valyti pasirinkimą**.

1. Pasirinkite vieną iš tolesnių peradresavimo tipų.

    - **Peradresavimas visam laikui (301)** – pasirinkite šią parinktį, kai žinote, kad turinys perkeliamas visam laikui ir nebus grąžintas į ankstesnį URL. Ieškos moduliai peradresuojančio URL ieškos modulio optimizavimo (SEO) reikšmę priskirs peradresuojamam URL ir atnaujins savo įrašą, kad būtų rodomas naujasis URL. 
    - **Laikinas peradresavimas (302)** – pasirinkite šią parinktį, norėdami peradresuoti eismą neatnaujindami ieškos modulių. Šis metodas paprastai naudojamas, jei turinys greitai grįš į ankstesnį URL.

1. Kai būsite pasirengę vykdyti peradresavimą, įrašykite ir publikuokite URL.

## <a name="additional-resources"></a>Papildomi ištekliai

[Svetainės naršymo tinkinimas](customize-site-navigation.md)

[Įtraukti naują svetainės puslapį](add-new-page.md)

[Jūsų domeno vardo konfigūravimas](configure-your-domain-name.md)

[Kalbų įtraukimas į savo svetainę](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
