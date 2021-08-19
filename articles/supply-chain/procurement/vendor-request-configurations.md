---
title: Tiekėjo užklausos konfigūracijos
description: Šioje temoje aprašomi laukai, kuriuos reikia užpildyti naujoje tiekėjo užklausoje.
author: kamaybac
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 98b759e5c5c918f14ca36bec93908d2f5eeb35044de77e3f450d79ead0993c16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725703"
---
# <a name="vendor-request-configurations"></a>Tiekėjo užklausos konfigūracijos
[!include [banner](../includes/banner.md)]

Norėdamas baigti tiekėjo užklausą, tiekėjo kontaktinis asmuo turi baigti galimo tiekėjo registracijos vedlį.

Formoje **Tiekėjo užklausos konfigūracijos** galite kurti šablonus, kurie nurodo privalomus laukus ir matomus laukus galimo tiekėjo registracijos vedlyje.

Pirmiausia tiekėjo registracijos vedlys su galimu tiekėju susijusio vartotojo paklausia, kurioje šalyje / regione tiekėjas vykdo veiklą. Ši informacija padeda nustatyti taikomą konfigūraciją. Jei nenurodyta konkreti šalies / regiono konfigūracija, naudojama numatytoji konfigūracija.

### <a name="set-up-a-vendor-request-configuration"></a>Tiekėjo užklausos konfigūracijos nustatymas

Pagal numatytuosius parametrus tiekėjo konfigūracija teikiama formoje Tiekėjo užklausos konfigūracijos.

Negalima pasirinkti numatytosios konfigūracijos šalies / regiono, todėl srities **Šalys / regionai** keisti negalima.

1. Spustelėkite **Paraiškos** > **Sąranka** > **Tiekėjai**, tada spustelėkite **Tiekėjo užklausos konfigūracijos**.
2. Spustelėkite skirtuką **Laukai**, norėdami nustatyti išvardytų laukų būseną.
3. Paslėptas (nematomas)
4. Rodomas (matomas, bet neprivalomas)
5. Būtinas (matomas ir privalomas)
6. Spustelėkite skirtuką **Turinys**, norėdami nurodyti, ar tekstas bus rodomas vedlyje ir ar reikia nurodyti, kad su galimu tiekėju susijęs vartotojas turi su tuo sutikti prieš pereidamas prie kito vedlio veiksmo. Bus prašoma bet kurių sąlygų, su kuriomis vartotojas turi sutikti, patvirtinimo.

Taip pat galite įvesti patvirtinimo pranešimą, kuris bus rodomas, kai vedlys bus baigtas, ir galite įtraukti vieną arba kelis klausimynus.

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a>Konkrečios šalies / regiono tiekėjo konfigūracijos kūrimas
1.  Spustelėkite **Paraiškos** > **Sąranka** > **Tiekėjai**, tada spustelėkite **Tiekėjo užklausos konfigūracijos**.
2.  Spustelėkite parinktį **Nauja**, norėdami kurti naują konfigūraciją, ir nurodykite konfigūracijos pavadinimą.
3.  Spustelėkite **Įrašyti**.
4.  Atidarykite skirtuką **Šalis / regionas**, kad pasirinktumėte šalį / regioną, kuriam konfigūracija skirta.
5.  Nustatykite konfigūraciją, vadovaudamiesi numatytosios konfigūracijos nustatymo instrukcijomis.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]