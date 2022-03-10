---
title: El. paštu siunčiamų pranešimų šablono nustatymas
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti el. paštu siunčiamų pranešimų šabloną.
author: bicyclingfool
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9f7adffd67e8198d16e4f7ed4fc4aadf59071b1d
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109636"
---
# <a name="set-up-an-email-notification-profile"></a>El. paštu siunčiamo pranešimo šablono nustatymas

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti el. paštu siunčiamų pranešimų šabloną.

Kurdami kanalus galite nustatyti el. paštu siunčiamo pranešimo profilį. El. paštu siunčiamo pranešimo šablonas nurodo pardavimo operacijos įvykius (pvz., sukurto užsakymo, supakuoto užsakymo ir užsakymų įvykių, kuriems išrašytos SF), kuriems jūs siųsite pranešimus savo klientams. 

Papildomos informacijos apie tai, kaip konfigūruoti el. paštą, žr. [El. laiškų konfigūravimas ir siuntimas](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="create-an-email-notification-profile"></a>El. paštu siunčiamų pranešimų šablono kūrimas

Norėdami sukurti el. paštu siunčiamų pranešimų šabloną, atlikite tolesnius veiksmus.

1. Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Būstinės sąranka \>„Commerce“ el. paštu siunčiamų pranešimų šablonas**.
1. Veiksmų srityje spustelėkite **Naujas**.
1. Lauke **El. paštu siunčiamų pranešimų šablonas** įveskite šablono pavadinimą.
1. Lauke **Aprašas** įveskite tinkamą aprašą.
1. Jungiklį **Aktyvusis** nustatykite į **Taip**.

### <a name="create-an-email-template"></a>El. laiško šablono kūrimas

Kad būtų galima įgalinti el. paštu siunčiamo pranešimo tipą, "Commerce Headquarters" turite sukurti kiekvieno pranešimo tipo, kurį norite palaikyti, organizacijos el. laiško šabloną. Šiame šablone nustatomas kiekvienos palaikomos kalbos el. laiško subjektas, siuntėjas, numatytoji kalba ir el. laiško tekstas.

Norėdami sukurti el. pašto šabloną, atlikite toliau nurodytus veiksmus.

1. Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Būstinės sąranka \> Parametrai \> Organizacijos el. laiškų šablonai**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Lauke **El. pašto ID** įveskite šio šablono ID.
1. Lauke **Siuntėjo vardas, pavardė** įveskite siuntėjo vardą, pavardę.
1. Lauke **El. pašto aprašas** įveskite reikšmingą aprašą.
1. Lauke **Siuntėjo el. paštas** įveskite siuntėjo el. pašto adresą.
1. Dalyje **Bendra** pasirinkite numatytąją el. laiško šablono kalbą. Numatytoji kalba bus naudojama, kai nėra jokio lokalizuoto šablono nurodyta kalba.
1. Išplėskite skyrių **El. laiško turinys** ir pasirinkite **Naujas**, kad sukurtumėte šablono turinį. Pasirinkite kiekvieno turinio elemento kalbą ir nurodykite el. pašto temą. Jei el. laiške bus teksto, užtikrinkite, kad pažymėtas žymės langelis **Yra teksto**.
1. Veiksmų srityje pasirinkite **El. laiško tekstas** ir sukurkite el. laiško teksto šabloną.

Toliau pateiktame vaizde parodyti keli el. pašto šablonų parametrų pavyzdžiai.

![El. pašto šablonų parametrai.](media/email-template.png)

Daugiau informacijos apie el. laiškų šablonų kūrimą rasite operacijų [įvykių el. laiškų šablonų kūrimas](email-templates-transactions.md). 

### <a name="create-an-email-event"></a>El. laiško įvykio kūrimas

Norėdami sukurti el. laiško įvykį, atlikite toliau nurodytus veiksmus.

1. Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Būstinės sąranka \>„Commerce“ el. paštu siunčiamų pranešimų šablonas**.
1. Sąraše raskite ir pasirinkite norimą įrašą. 
1. Išplečiamajame sąraše **El. pašto ID** pasirinkite el. laiško šabloną.
1. Išplečiamajame sąraše pasirinkite tinkamą parinktį **El. paštu siunčiamo pranešimo tipas**.
1. Pažymėkite žymės langelį **Aktyvusis**.
1. Veiksmų srityje pasirinkite **Įrašyti**.

Toliau pateiktame vaizde parodyti keli įvykių pranešimų parametrų pavyzdžiai.

![Įvykio pranešimo parametrai.](media/email-notification-profile.png)

> [!NOTE]
> Kliento sukurtas pranešimo tipas reikalauja tinkinimo, kad būtų galima siųsti el. paštu siunčiamą pranešimą.

### <a name="schedule-a-recurring-email-notification-process-job"></a>Suplanuoti pasikartojančio el. paštu siunčiamo pranešimo proceso užduotį

Norėdami išsiųsti el. paštu siunčiamus pranešimus, turite paleisti mažmeninės **prekybos užsakymo el. paštu siunčiamų pranešimų** užduotį.

Norėdami nustatyti mažmeninės prekybos užsakymo **el. paštu siunčiamo pranešimo** užduotį "Commerce Headquarters", jei to dar nepadarėte, atlikite šiuos veiksmus.

1. Eiti į "**Retail" ir "Commerce \> Retail" ir "Commerce IT" el \>. laišką ir pranešimus Siųsti el \>. paštu.**
1. Mažmeninės prekybos **užsakymo el. paštu siunčiamo pranešimo dialogo** lange pasirinkite **Pasikartojimas**.
1. Dialogo lange **Nustatyti pasikartojimą** pasirinkite Ne **pabaigos datą**.
1. Dalyje **Pasikartojimo** trafaretas **pasirinkite** Minutės, tada nustatykite **lauką** Skaičiavimas kaip **1**. Šie parametrai užtikrins, kad pranešimai el. paštu bus apdorojami kaip galima greičiau.
1. Pasirinkite Gerai **,** norėdami grįžti į mažmeninės prekybos užsakymo **el. paštu siunčiamo pranešimo** dialogo langą.
1. Norėdami **baigti** užduoties nustatymą, pasirinkite Gerai.

### <a name="next-steps"></a>Kiti veiksmai

Kad galėtumėte siųsti laiškus, turite sukonfigūruoti siunčiamo pašto paslaugą ir nustatyti paketinę užduotį. Norėdami gauti daugiau informacijos, žr. [El. laiškų konfigūravimas ir siuntimas](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="additional-resources"></a>Papildomi ištekliai

[El. pašto konfigūravimas ir siuntimas](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Kanalų apžvalga](channels-overview.md)

[Kanalo sąrankos būtinieji komponentai](channels-prerequisites.md)

[Organizacijų ir organizacijų hierarchijų apžvalga](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
