---
title: DUK apie asinchroninį kliento kūrimo režimą
description: Šiame straipsnyje pateikiami atsakymai į dažnai užduodamus klausimus apie asinchroninį kliento kūrimo režimą Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 64c895fb9f3e55f7680759fa72626be6660aa67c
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690208"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>DUK apie asinchroninį kliento kūrimo režimą

[!include [banner](includes/banner.md)]

Šiame straipsnyje pateikiami atsakymai į dažnai užduodamus klausimus apie asinchroninį ("async") kliento kūrimo režimą Microsoft Dynamics 365 Commerce.

### <a name="why-cant-i-enable-the-enable-editing-customers-in-asynchronous-mode-feature"></a>Kodėl negalima įgalinti funkcijos Įgalinti klientų redagavimą asinchroninio režimu?

Prieš įjungdami **funkciją Įgalinti klientų redagavimą asinchroninio režimo** funkcija, turite įgalinti šias funkcijas:

- Patobulinti klientų užsakymų ir klientų operacijų našumo patobulinimai
- Įgalinti patobulintą "async" kliento kūrimą
- Įjungti asinchroninį klientų adresų kūrimą

### <a name="why-do-i-still-see-real-time-service-calls-made-to-commerce-headquarters-after-the-enable-editing-customers-in-asynchronous-mode-feature-is-enabled"></a>Kodėl vis dar matote "Commerce Headquarters" "Real-time Service" iškvertus funkciją Įgalinti klientų redagavimą asinchroniškai režimu?

Ši problema kyla, kai Commerce Data Exchange (CDX) užduotys nebuvo paleistos, siekiant užtikrinti funkcijos būseną, o kiti kanalo metaduomenys sinchronizuojami su kanalu. Prieš kartodami scenarijų, įsitikinkite, kad "Commerce Headquarters" bus paleisto šios CDX užduotys:

- 1110 (visuotinis konfigūravimas)
- 1010 (klientai)
- 1070 (kanalo konfigūracija)

Paleidus CDX užduotis duomenys, įrašyti į talpyklą "Commerce Scale Unit" (CSU), gali būti ne iš karto rodomi "Commerce Headquarters".

### <a name="why-doesnt-commerce-headquarters-show-customer-creation-or-updates-from-the-point-of-sale-pos-or-e-commerce-channel"></a>Kodėl "Commerce Headquarters" nerodo klientų kūrimo ar atnaujinimų iš point sale (EKA) ar el. komercijos kanalo?

Užtikrinkite, kad šie veiksmai atlikti tokia tvarka, kaip jie išvardyti čia.

1. Paleiskite CDX P užduotį "Commerce Headquarters", kad "Async **" kliento duomenys būtų saugomi lentelėsE RETAILASYNCCUSTOMERV2**, **RETAILASYNCADDRESSV2**, **RETAILASYNCCUSTOMERCONTACT**, **RETAILASYNCCUSTOMERAFFILIATION** **ir RETAILASYNCCUSTOMETRIBUTIVE2**.
1. Paleiskite paketinę **užduotį Sinchronizuoti klientus ir kanalų užklausas** "Commerce Headquarters". Sėkmingai atlikus paketinę užduotį visi įrašai, **sėkmingai apdoroti iš anksčiau paminėtų lentelių, lauke OnlineOperationCompleted** bus nustatytas kaip **1**.

### <a name="how-do-i-know-which-customer-management-in-asynchronous-mode-operation-has-failed-and-how-do-i-make-changes-if-they-are-required"></a>Kaip žinoti, kurio klientų valdymo asinchroninio režimo operacijos metu atlikti nepavyko ir kaip, jei reikia, man atlikti keitimus?

Norėdami peržiūrėti visas asinchronines režimo operacijas ir jų sinchronizavimo būseną, "Commerce Headquarters" pereikite į " **Commerce" ir "Retail \> " klientų klientų \> sinchronizavimo būseną**. Norėdami keisti, redaguokite konkrečią operaciją, atnaujinkite laukus, pasirinkite **Įrašyti**, **tada** pasirinkite Sinchronizuoti, kad keitimai būtų sinchronizuojami.

