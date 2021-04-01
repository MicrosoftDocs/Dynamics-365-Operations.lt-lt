---
title: Darbas su CSS perrašymo failais
description: Šioje temoje aprašoma, kodėl, kada ir kaip programoje „Microsoft Dynamics 365 Commerce“ naudoti pakopinių stilių sąrašo (CSS) perrašymo failus.
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 41fb0be51f7af25faba1b860319aea84ae7a8b56
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207804"
---
# <a name="work-with-css-override-files"></a>Darbas su CSS perrašymo failais


[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kodėl, kada ir kaip programoje „Microsoft Dynamics 365 Commerce“ naudoti pakopinių stilių sąrašo (CSS) perrašymo failus.

## <a name="overview"></a>Peržiūra

Nuolatiniai svetainės stiliai paprastai turėtų būti tvarkomi naudojant svetainės temą. Naudojant temas pasiekiami pagrindiniai bet kurio svetainės puslapio CSS ir stilių parametrai. Temos kuriamos naudojant „Dynamics 365 Commerce“ internetinį programinės įrangos kūrimo rinkinį (SDK), o į svetaines įdiegiamos naudojant „Microsoft Dynamics Lifecycle Services“ (LCS). Naudodami temų derinimo galimybes ir modulių sąsajos konfigūracijas SDK žinyno svetainėje, svetainių programuotojai gali lengviau kurti tinkinamus ir darnius svetainių dizaino paketus. Kai šie dizaino paketai įdiegiami į svetainę, jos autoriai gali sutelkti dėmesį į turinio kūrimą, redagavimą ir publikavimą, o ne į svetainės programavimą.

Atsižvelgiant į įprastą temos ciklą, priklausomybė nuo programuotojų, keičiančių stilius per SDK ir LCS diegimo srautą, kai kuriose situacijose gali būti pernelyg didelė. Jei SDK nesukonfigūruotas arba jei neturite laiko laukti įdiegties per LCS, svetainės prototipai ar karštosios pataisos gali atrodyti sudėtingi.

Tokiose situacijose gali padėti CSS perrašymo failai. Naudodami „Commerce“ kūrimo įrankius, autentifikuoti vartotojai gali nusiųsti CSS failą, jį peržiūrėti ir aktyvinti, kad perrašytų svetainės temą. Nereikalinga papildoma SDK ar LCS įdiegtis. CSS perrašymo faile gali būti nurodytas toks mažas perrašymas, kaip vieno teksto stiliaus pakeitimas, arba toks platus, kaip visiškas prekės ženklo perkūrimas.

Prieš naudodami CSS perrašymo failus, turėkite omenyje tolesnius apribojimus.

- Vienu metu svetainėje gali būti aktyvus tik vienas CSS perrašymo failas. Todėl visi aktyvūs perrašymo veiksmai turi būti viename perrašymo faile.
- Nors perrašymo veiksmus galite peržiūrėti „Commerce“ kūrimo įrankiuose, juose nėra specialių derinimo funkcijų, padedančių nustatyti perrašymo veiksmų sukeliamas klaidas. Kitaip tariant, kai naudojate CSS perrašymo failus, neturite tokio paties įrankių rinkinio, kurį SDK suteikia moduliams ir kūrimui tikrinti.

Nepaisant to, CSS perrašymo failai yra greitas būdas dizaino prototipui sukurti ar karšajai pataisai įdiegti prieš sukuriant ir įdiegiant visapusį temos naujinimą.

## <a name="create-a-css-override-file"></a>CSS perrašymo failo sukūrimas

Norėdami sukurti CSS perrašymo failą, galite naudoti integruotąją programavimo aplinką (IDE), teksto rengyklę arba šaltinio kodo rengyklę. Įprasta naršyklėje naudojant standartines žiniatinklio derintuves nustatyti esamos svetainės stilių išrinkiklius, ypatybes ir reikšmes. Daugelyje naršyklių galima keisti reikšmes ir jas peržiūrėti derintuvėje. Identifikavę norimus atlikti keitimus, galite juos įrašyti į savo CSS failą.

## <a name="upload-a-css-override-file"></a>CSS perrašymo failo nusiuntimas

Norėdami programoje „Commerce“ į svetainę nusiųsti CSS failą, atlikite tolesnius veiksmus.

1. Naudodami kūrimo įrankius, nueikite į savo svetainę.
1. Kairėje esančioje naršymo srityje pasirinkite **Dizainas**.

    > [!NOTE]
    > Kad galėtumėte pasirinkti **Dizainas**, naršymo srityje gali reikėti išplėsti elementą **Parametrai** – tai priklauso nuo naudojamos „Commerce“ kūrimo įrankių versijos.

1. Jei jis dar nepasirinktas, pagrindinės dizaino srities viršuje pasirinkite skirtuką **CSS perrašymas**.
1. Dalyje **Galimi CSS perrašymo veiksmai** pasirinkite **Nusiųsti CSS failą**. Atisranda failų naršyklės langas.
1. Naršydami failų naršyklėje pasirinkite CSS failą, tada – **Atidaryti**. Nusiųstas CSS failas dabar rodomas dalyje **Galimi CSS perrašymo veiksmai**.

## <a name="preview-a-css-override-file"></a>CSS perrašymo failo peržiūra

Jei CSS perrašymo failą norite peržiūrėti prieš jį suaktyvindami savo paleistoje svetainėje, atlikite toliau nurodytus veiksmus.

1. Kairėje esančioje naršymo srityje pasirinkite **Dizainas**, tada skirtuko **CSS perrašymas** dalyje **Galimi CSS perrašymo veiksmai** suraskite CSS failą, kurį norite peržiūrėti.
1. Prie CSS failo pavadinimo pasirinkite **Peržiūrėti svetainę**.
1. Dialogo lange **Pasirinkite URL** pasirinkite svetainės, kuriai norite taikyti perrašymo veiksmą, URL, tada – **Gerai**.
1. Jei yra keli pasirinkto URL variantai, pasirodžiusiame dialogo lange **Peržiūros variantai** pasirinkite norimą variantą.

Atidaromas naujas naršyklės skirtukas arba langas, kuriame galite patikrinti svetainės stilių perrašymo veiksmus. URL tada galite bendrinti su kitais autentifikuotais „Commerce“ vartotojais, kad jie galėtų svetainę įvertinti ir pateikti atsiliepimų.

## <a name="activate-a-css-override-file-on-your-live-site"></a>CSS perrašymo failo suaktyvinimas paleistoje svetainėje

Peržiūrėję ir patvirtinę CSS perrašymo failą, jį galite suaktyvinti paleistoje svetainėje.

> [!NOTE]
> Vienu metu svetainėje gali būti aktyvus tik vienas CSS perrašymo failas. Jei suaktyvinate naują perrašymo failą, ankstesnis perrašymo failas supasyvinamas. Todėl įsitikinkite, kad visi reikiami perrašymo veiksmai yra viename CSS perrašymo faile.

Norėdami suaktyvinti CSS perrašymo failą, atlikite tolesnius veiksmus.

1. Kairėje esančioje naršymo srityje pasirinkite **Dizainas**, tada skirtuko **CSS perrašymas** dalyje **Galimi CSS perrašymo veiksmai** suraskite CSS failą, kurį norite suaktyvinti.
1. Po CSS failo pavadinimu pasirinkite **Aktyvinti**. Perrašymo failas iš karto tampa aktyvus jūsų paleistoje svetainėje.

## <a name="deactivate-a-css-override-file-on-your-live-site"></a>CSS perrašymo failo išjungimas paleistoje svetainėje

Norėdami savo svetainėje CSS perrašymo failą išjungti, atlikite tolesnius veiksmus.

1. Kairėje esančioje naršymo srityje pasirinkite **Dizainas**, tada skirtuko **CSS perrašymas** dalyje **Galimi CSS perrašymo veiksmai** suraskite CSS failą, kurį norite išjungti.
1. Po CSS failo pavadinimu pasirinkite **Išjungti**. Perrašymo failas iš karto tampa neaktyvus jūsų paleistoje svetainėje.

> [!TIP]
> Norėdami pasiekti papildomas CSS perrašymo failų parinktis, pasirinkite prie CSS failo pavadinimo esantį daugtašį (**...**). Parinktys **Atsisiųsti**, **Pervardyti** ir **Pakeisti** yra naudingos norint greitai pakeisti esamą CSS perrašymo failą.

## <a name="additional-resources"></a>Papildomi ištekliai

[Įtraukti logotipą](add-logo.md)

[Pasirinkti svetainės temą](select-site-theme.md)

[Darbas su stilių išankstinėmis parinktimis](style-presets.md)

[Įtraukti parankinių piktogramą](add-favicon.md)

[Įtraukti pasveikinimo pranešimą](add-welcome-message.md)

[Įtraukti informaciją apie autorių teises](add-copyright-notice.md)

[Kalbų įtraukimas į savo svetainę](add-languages-to-site.md)

[Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]