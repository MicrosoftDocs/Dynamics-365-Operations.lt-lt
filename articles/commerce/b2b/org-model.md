---
title: Kurkite organizacijos modeliavimo hierarchijas B2B organizacijoms
description: Šioje temoja aprašoma, kaip kurti organizacijos modelio hierarchijas verslo su verslu (B2B) organizacijoms.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 91cb01637faa69bd3c7fefefae69c60cb948510e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211230"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a>Kurkite organizacijos modeliavimo hierarchijas B2B organizacijoms

[!include [banner](../../includes/banner.md)]

Šioje temoja aprašoma, kaip kurti organizacijos modelio hierarchijas verslo su verslu (B2B) organizacijoms programoje „Microsoft Dynamics 365 Commerce”.

„Commerce“ štabe, verslo partnerio organizacijos yra atstovaujamos kliento ir kliento hierarchijos objektų. Verslo partnerio organizacija ir jos vartotojai yra atstovaujami kaip klientai ir kliento hierarchijos yra naudojamas siekiant susieti klientus tarpusavyje.

Kai verslo partneris užklausa prisijungti B2B el. komercijos saitas yra patvirtintas, atliekami tolesni veiksmai:

- Du nauji kleitno įrašai yra suukuriami sistemoje: **Organizacijos tipo** kliento įrašas verslo partnerio organizacijai ir **Asmens tipas** kliento įrašo besikreipiančiam asmeniui (tai reiškia, verslo partnerio vartotojas, kuris pateikė užklausą).
- Naujas kliento hierarchijos įrašas yra sukuriamas **Klientas \> Kliento hierarchija**. Šis įrašas turi tolesnes antraštės ypatybes:

    - **Kliento hierarchijos ID** – Unikalus ID kliento hierarchijai. Šis ID naudoja skaičių seką, kuris yra nustatyta „Commerce“ bendrintuose parametruose „Commerce“ būstinėje.
    - **Pavadinimas** – Verslo partnerio organizacijos pavadinimas, kaip nurodytas samdymo užklausoje.
    - **Tikslas** – Ši nuosavybė yra nustatytas iš anksto nustatytai vertei **B2B organizacija**.
    - **Organizacija** – Verslo partnerio kliento ID.

Toliau pateikiama kliento hierarchijos įrašo išsami informacija:

- Kliento užklausos teikėjo įrašas yra susietas su kliento hierarchija.
- Administratoriaus vaidmuo yra susietas su užklausos teikėju.

Kai administratorius įtraukia daugiau naudotojų į verslo partnerio organizaciją B2B vietoje, naujas kiekvieno naudotojo kliento įrašas yra sukuriamas „Commerce“ būstinėje. Kliento įrašas taip pat įtraukiamas į atitinkamą kliento hierarchijos įrašą verslo partneriui, o jo vaidmuo yra „vartotojas“.

> [!NOTE]
> Didžiojoje dalyje atvejų, atitinkamos nuosavybės visų kliento įrašų vertės hierarchijoje turėtų sutapti. Pavyzdžiui, kadangi visi verslo partnerio vartotojai turėtų gauti panašias kainas už produktus, jų kainos grupė ir susieti konfigūravimai turėtų sutapti. Nepaisant to, sistema neįgalina tokio nuoseklumo. Dėl to, atitinkami „Commerce“ štabo vartotojai yra atsakingi už nuosavybės verčių ir konfigūravimo atitikimą visiems klientams toje hierarchijoje.

„Commerce“ štabo vartotojai gali ieškoti nuosavybės verčių visuose kliento įrašuose hierarchijoje šalia esančiame rodinyje. Rinkitės atitinkamą kliento įrašo nuosavybę pasirinkdami skirtuko pavadinimus iškrentančiame meniu. Vartotojai gali tiesiogiai peržiūrėti ir redaguoti nuosavybės vertes šiame rodinyje. Kitu atveju, jei norite taikyti vertes administratoriaus kliento įrašui visies klientų įrašams, rinkitės **Viršyti** kliento išsamios informacijos hierarchijoje.

## <a name="additional-resources"></a>Papildomi ištekliai

[Nustatykite B2B el. komercijos saitą](set-up-b2b-site.md)

[Valdykite verslo partnerio vartotojus B2B el. komercijos saituose](manage-b2b-users.md)

[Konfigūruoti kliento sąskaitos mokėjimo metodą B2B el. komercijos saitams](payment-method.md)

[Nustatykite produkto kiekio apribojimus B2B el. komercijos saitams](quantity-limits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]