---
title: DUK apie asinchroninį kliento kūrimo režimą
description: Šiame straipsnyje pateikiami atsakymai į dažnai užduodamus klausimus apie asinchroninį kliento kūrimo režimą Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: bd5741aeb3278f1d40d63bb02ca57571a907dc21
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474075"
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

Ši problema kyla, kai Commerce Data Exchange (CDX) užduotys nebuvo paleistos siekiant užtikrinti, kad funkcijos būsena ir kiti kanalo metaduomenys yra sinchronizuojami su kanalu. Prieš kartodami scenarijų, įsitikinkite, kad "Commerce Headquarters" yra paleisto šios CDX užduotys:

- 1110 (visuotinis konfigūravimas)
- 1010 (klientai)
- 1070 (kanalo konfigūracija)

Paleidus CDX užduotis duomenys, įrašyti į talpyklą "Commerce Scale Unit" (CSU), gali būti ne iš karto rodomi "Commerce Headquarters".

### <a name="why-doesnt-commerce-headquarters-show-customer-creation-or-updates-from-the-point-of-sale-pos-or-e-commerce-channel"></a>Kodėl "Commerce Headquarters" nerodo klientų kūrimo ar atnaujinimų iš point sale (EKA) ar el. komercijos kanalo?

Užtikrinkite, kad šie veiksmai buvo atlikti tokia tvarka, kaip jie išvardyti čia.

1. Paleiskite CDX P užduotį "Commerce Headquarters", kad būtų galima užtikrinti, kad "Commerce **Headquarters" lentelėsE RETAILASYNCCUSTOMERV2**, **RETAILASYNCADDRESSV2**, **RETAILASYNCCUSTOMERCONTACT**, **RETAILASYNCCUSTOMERAFFILIATION** ir RETAILASYNCCUSTOMETRIBUTIVE2 **būtų galimi "Commerce Headquarters".**
1. Paleiskite paketinę **užduotį Sinchronizuoti klientus ir kanalų užklausas** "Commerce Headquarters". Sėkmingai atlikus paketinę užduotį visi įrašai, **sėkmingai apdoroti iš anksčiau paminėtų lentelių, lauke OnlineOperationCompleted** bus nustatytas kaip **1**.
