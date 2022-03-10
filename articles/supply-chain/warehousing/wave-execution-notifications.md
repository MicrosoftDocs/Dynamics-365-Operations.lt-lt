---
title: Bangos vykdymo pranešimai
description: Šioje temoje aprašyti bangos vykdymo pranešimai ir paaiškinta, kaip juos nustatyti.
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: af3983db1a96116a88914411a26f1ac5d4857ae9
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103244"
---
# <a name="wave-execution-notifications"></a>Bangos vykdymo pranešimai

[!include [banner](../includes/banner.md)]

Funkcija *Bangos vykdymo pranešimai* naudoja verslo įvykius ir veiksmų centrą pateikti pranešimams, susijusiems su bangos vykdymu. Tai leidžia jums nurodyti įvykius, kurie generuoja pranešimus, sandėliuos, kurie juos generuoja ir vartotojus, kurie juos gauna.

Mygtukas **Rodyti pranešimus** (skambučio simbolis), esantis dešinėje naršymo meniu pusėje, nurodo, kada veiksmų centro pranešimas bus pasiekiamas dabartiniam vartotojui. Vartotojas gali pasirinkti mygtuką **Rodyti pranešimus** veiksmų centrui atidaryti ir pranešimams peržiūrėti.

Verslo įvykiai įvyksta, kai paleidžiami verslo procesai. Verslo procesai susideda iš užduočių. Verslo proceso metu jame dalyvaujantys vartotojai atlieka verslo veiksmus toms užduotims atlikti. Verslo įvykiai suteikia mechanizmą, kuris leidžia išorinėms sistemoms gauti pranešimus iš finansų ir operacijų programų. Tokiu būdu sistemos gali atlikti verslo veiksmus, kaip atsaką į verslo įvykius. Daugiau informacijos rasite [Verslo įvykių apžvalga](../../fin-ops-core/dev-itpro/business-events/home-page.md).

## <a name="turn-the-wave-execution-notifications-feature-on-or-off"></a>Įjungti arba išjungti bangos vykdymo pranešimų funkciją

Kaip ir tiekimo grandinės valdymo versija 10.0.25 ši funkcija įjungiama pagal numatytąjį nustatymą. Administratoriai gali įjungti arba išjungti šią funkciją funkcijų *valdymo darbo srityje ieškodami bangos* vykdymo [pranešimų](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) funkcijos.

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a>Scenarijus: bangos paketinio vykdymo pranešimų siuntimas į veiksmų centrą

Šis scenarijus rodo tiesioginį srautą, skirtą pranešimų apie bangos paketinio vykdymo klaidas siuntimui į konkretų vaidmenį per veiksmų centrą.

### <a name="make-demo-data-available"></a>Demonstracinių duomenų įgalinimas

Šio scenarijaus įgyvendinimui, privalote turėti įdiegtus demo duomenis ir pasirinkti **USMF** juridinį asmenį.

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a>Užtikrinkite, kad bangos veikia paketiniu režimu

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**.
1. „FastTab” **Bangų apdorojimas** nustatykite parinktį **Apdoroti bangas paketais** į *Taip*.

> [!NOTE]
> Jei norite išjungti bangos paketinio vykdymo pranešimus, nustatykite parinktį **Išjungti bangos paketinio apdorojimo pranešimus** į *Taip*.

### <a name="configure-a-wave-notification-policy"></a>Bangos pranešimų strategijos konfigūravimas

Bangos pranešimų strategijos nurodo vartotojams siunčiamų pranešimų tipus.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Bangos \> Bangos pranešimų strategijos**.
1. Sukurkite įrašą, kuris turi šiuos nustatymus:

    - **Bangos pranešimų strategija:** *24 Paketo klaida*
    - **Aprašas:** *24 sandėlio bangų paketo klaida*
    - **Siųsti pranešimą:** *Tik klaidos*
    - **Į vaidmenį:** *Sistemos administratorius*

        > [!NOTE]
        > Kadangi šiame scenarijuje naudojami demonstraciniai duomenys, *Sistemos administratoriaus* vaidmuo buvo pasirinktas dėl paprastumo. Todėl, kadangi esate prisijungęs kaip sistemos administratoriaus vartotojas, gausite pranešimus. Tačiau praktiškai, įprastai turėtumėte pasirinkti konkretesnį vaidmenį, kuriam pranešti apie bangos paketinio vykdymo klaidas, pavyzdžiui, *Sandėlio vadovą*.

1. Veiksmų srityje pasirinkite **Įrašyti**.

### <a name="configure-a-wave-template"></a>Bangos šablono konfigūravimas

Bangos šablonai leidžia jums susieti konkrečius bangų metodų atvejus su atitinkamais bangos žymos šablonais.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.
1. Sąrašo srityje nustatykite lauką **Bangos šablono tipas** į *Siuntimas*, o tada pasirinkite *24 numatytojo siuntimo* bangos šabloną 24 sandėliui.
1. „FastTab“ **Bendra** nustatykite **Bangos pranešimų strategija** lauką į *24 Paketinė klaida*.

### <a name="configure-a-work-template"></a>Bangos šablono konfigūravimas

Darbo šablonai naudojami bangos vykdymo metu generuoti darbui. Šiame scenarijuje bangos vykdymas turi sukelti klaidą. Nustatydami darbo šablono užklausą neegzistuojančio sandėlio naudojimui, užtikrinsite, kad bangos vykdymas nepavyks, tad atsiųs pranešimą.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.
1. Sąrašo srityje nustatykite lauką **Darbo šablono tipas** į *Pardavimo užsakymai* ir tada pasirinkite *24 PU etapo* darbo šabloną 24 sandėliui.
1. Veiksmų srityje pasirinkite **Redaguoti užklausą**.
1. Užklausos redaktoriaus dialogo lango skirtuke **Diapazonas** redaguokite šią eilutę (arba pridėkite ją, jeigu jos nėra):

    - **Lentelė:** *Laikinos darbo operacijos*
    - **Išvestinė lentelė:** *Laikinos darbo operacijos*
    - **Laukas:** *Sandėlis*
    - **Kriterijai:** pakeiskite reikšmę *iš 24* į *Klaida*.

1. Pasirinkite **Gerai** ir patvirtinkite keitimą.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Sukurkite prekybos užsakymą ir išleiskite jį į sandėlį

1. Eikite į **Prekyba ir komercija \> Prekybos užsakymas \> Visi prekybos užsakymai**.
1. Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.

    - **Kliento sąskaita:** *US-001*
    - **Sandėlis:** *24*

1. „FastTab” **Pardavimo užsakymo eilutės** įtraukite pardavimo užsakymo eilutę, turinčią šiuos parametrus:

    - **Prekės numeris:** *A0001*
    - **Kiekis:** *10*

    > [!NOTE]
    > Šitos prekės ir kiekiai yra tik pavyzdžiai. Nurodytame sandėlyje turi būti pakankamai atsargų.

1. Kai „FastTab” **Pardavimo užsakymo eilutės** vis dar renkatės naują liniją, įrankių juostoje pasirinkite **Atsargos \> Rezervavimas**.
1. **Rezervacija** puslapyje, esančiame Veiksmų srityje, pasirinkite **Rezervuoti partiją**. Tada uždarykite puslapį.
1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.

### <a name="notifications-from-wave-batch-job-execution"></a>Pranešimai iš bangos paketo užduoties vykdymo

Atsižvelgiant į jūsų verslo įvykių nustatymą, galiausiai jūs gausite pranešimą apie bangos vykdymo nesėkmę. Veiksmų centro pranešimas bus panašus į toliau pateiktą pavyzdį ir įtrauks nuorodą į nepavykusią bangą.

> **Klaida vykdant bangą**  
> Vykdant bangą USMF-000000001 įvyko klaida.  
> Paskutiniai pranešimai: bangai USMF-000000001 nebuvo sukurta jokio darbo.
>
> **BŪSENA**  
> Aktyvi
>
> Atidaryti išsamią bangos informaciją

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
