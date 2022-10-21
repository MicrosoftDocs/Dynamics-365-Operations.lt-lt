---
title: Kliento operacijų būstinėje audito sinchronizavimas
description: Šiame straipsnyje paaiškinama, kaip atlikti kliento operacijų būstinėje sinchronizavimą Microsoft Dynamics 365 Commerce, siekiant padėti išspręsti visas svetainės vartotojo problemas.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-28
ms.openlocfilehash: c615b0b436e01a1423b5611a72f0056b5b14f8e8
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690964"
---
# <a name="audit-synchronization-of-customer-operations-in-headquarters"></a>Kliento operacijų būstinėje audito sinchronizavimas

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šiame straipsnyje paaiškinama, kaip atlikti kliento operacijų būstinėje sinchronizavimą Microsoft Dynamics 365 Commerce, siekiant padėti išspręsti visas svetainės vartotojo problemas.

Kadangi organizacijos pradeda taikyti galimybę kurti ir redaguoti klientus asinchroniškai, svetainės administratoriams reikia būdo peržiūrėti ir šalinti operacijas, remiantis svetainės vartotojo užklausomis arba proceso triktimis. Tokiu atveju svetainės administratoriai turėtų turėti galimybę audituoti klientų kūrimą ir redaguoti operacijas bei ištaisyti visas triktis, naudodami savitarnos modelį.

## <a name="customer-synchronization-status"></a>Kliento sinchronizavimo būsena

Kai pasirenkate asinchroninį klientų valdymo režimą ir atitinkamas jo funkcijas, "Commerce Headquarters" administratoriai turi sukurti ir suplanuoti pasikartojančią P **užduoties paketinę užduotį,** sinchronizuoti klientus **ir verslo partnerius iš "Async** **" režimo užduoties ir 1010** užduoties, kad visi "Async" klientai būtų konvertuoti į sinchronizavimo klientus "Commerce Headquarters". Kliento valdymo operacijų sinchronizavimas įvyksta šių užduočių vykdymo metu. Daugiau informacijos ieškokite asinchroninis [kliento kūrimo režimas](async-customer-mode.md).

Kaip verslo savininkas galite atlikti šias operacijas:

- Peržiūrėkite visas svetainės vartotojų kūrimo / redagavimo operacijas. Išsami informacija apie būseną ir laiko antspaudą.
- Filtruoti operacijas, naudojant bet kurį kliento lentelės lauką ir vertes audito žurnalui sumažinti.
- Peržiūrėkite trumpą pakeitimų aprašą ir būsenos informaciją, kad suprastumėte aukšto lygio operacijas.
- Dėl trikčių redaguokite ir ištaisykite probleminius laukus, tada įrašykite ir sinchronizuokite konkrečias kliento operacijas.

### <a name="elements-on-the-customer-synchronization-status-page"></a>Elementai kliento sinchronizavimo būsenos puslapyje

Norėdami peržiūrėti visų sinchronizavimo operacijų sąrašą, "Commerce Headquarters" pereikite į " **Commerce" ir "Retail \> Customers" klientų \> sinchronizavimo būseną**. Šioje iliustracijoje pateikiamas kliento sinchronizavimo **būsenos puslapio** pavyzdys.

![Klientų sinchronizavimo būsenos puslapis "Commerce Headquarters".](media/D365-Commerce-Customer-Mgmt-Audi-Async-Operations.png)

Pagal numatytuosius nustatymus kliento sinchronizavimo operacijų, kurios yra kairėje Kliento **sinchronizavimo būsenos puslapio pusėje,** sąrašas apima šiuos stulpelius:

- Kanalo pavadinimas
- Kliento kodas
- Nesinchroninio kliento kodas
- Operacijų laiko žyma
- Kliento sinchronizavimo būsena

Viršutiniame dešiniajame puslapio kampe rodoma kliento sąskaitos informacija, pvz., **kliento kodas, "** Retail async"**operacija,** **kliento** sinchronizavimo būsena ir paskutinės žinomos klaidos **vertės.**

Pakeitimo **aprašymo** skyriuje yra kliento valdymo operacijos, kuri buvo atliekama (pvz., kliento kūrimas, sąskaitos atnaujinimas arba sinchronizavimo triktis su išsamiai, tipo aprašas).

Kliento **atributų** skyriuje yra tinklelis, kuriame rodomi visi kliento atributai bei senos ir naujos vertės. Galite redaguoti šį skyrių, jei norite pakeisti savo kliento atributo vertes, kad būtų ištaisytos klaidos, ir sinchronizuoti dar kartą.
