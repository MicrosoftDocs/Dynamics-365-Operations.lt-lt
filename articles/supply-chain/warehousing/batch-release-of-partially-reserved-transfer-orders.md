---
title: Iš dalies rezervuotų perkėlimo užsakymų paketinis išleidimas
description: Šioje temoje aprašoma, kaip mobiliuoju įrenginiu nustatyti ir taikyti paketinį iš dalies rezervuotų perkėlimo užsakymų išleidimą.
author: pjacobse
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSFulfillmentPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7807ae109a4a708f3530112feed1a4fb210a30ef
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433956"
---
# <a name="batch-release-of-partially-reserved-transfer-orders"></a>Iš dalies rezervuotų perkėlimo užsakymų paketinis išleidimas

[!include [banner](../includes/banner.md)]

Paketinio iš dalies rezervuotų perkėlimo užsakymų išleidimo funkcija leidžia naudojant paketinę užduotį į sandėlį iš dalies išleisti perkėlimo užsakymus.
Kadangi galite pasirinkti išleisti dalinį kiekį, prieš išleisdami užsakymą neprivalote laukti, kol sandėlyje bus visas užsakymo kiekis.

Užsakymų išleidimas į sandėlį yra patobulinto sandėlio valdymo procesas. Šis procesas apima tokias veiklas kaip paėmimas, pakavimas ir siuntimas, kurias sandėlio darbininkas gali atlikti naudodamas mobilųjį įrenginį.

## <a name="where-it-applies"></a>Kai taikoma

Naudojant šią funkciją užsakymai į sandėlį išleidžiami naudojant paketinę užduotį. Ši funkcija yra naudinga, kai sandėlyje neturite pakankamai atsargų, tačiau vis tiek norite iš vieno sandėlio į kitą perkelti prekių.

## <a name="how-it-is-set-up"></a>Kaip tai nustatoma

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a>Perkėlimo užsakymų ir pardavimo užsakymų įvykdymo kriterijų nurodymas

Kad, naudojant paketinę užduotį, užsakymą būtų galima iš dalies išleisti į sandėlį, turi būti patenkinti įvykdymo kriterijai. Šiuos įvykdymo kriterijus nustato įvykdymo strategija.

Perkėlimo užsakymų ir pardavimo užsakymų įvykdymo strategijos nurodomos įmonės lygiu. Atsižvelgiant į įvykdymo strategijos sąranką, paketinio užsakymų išleidimo procesas bus patvirtintas arba atmestas. Tada užsakymai bus atitinkamai apdorojami.

-   Norėdami sukurti perkėlimo užsakymų ir pardavimo užsakymų įvykdymo strategijų, spustelėkite **Sandėlio valdymas** \> **Sąranka** \> **Išleidimas į sandėlį** \> **Įvykdymo strategija** ir sukurkite įvykdymo strategiją įvesdami pavadinimą bei aprašą.

-   Norėdami nurodyti įvykdymo koeficientą, reikšmės tipą ir pranešimą, kuris rodomas pažeidus įvykdymo strategiją, spustelėkite **Sandėlio valdymas** \> **Sąranka** \> **Išleidimas į sandėlį** \> **Įvykdymo strategija** ir nustatykite laukus **Įvykdymo koeficientas**, **Reikšmės tipas** bei **Pranešimas apie įvykdymo pažeidimą**.

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a>Perkėlimo užsakymų ir pardavimo užsakymų įvykdymo strategijų nustatymas

-   Norėdami nustatyti perkėlimo užsakymų įvykdymo strategijas, spustelėkite **Atsargų valdymas** \> **Sąranka** \> **Atsargų ir sandėlio valdymo parametrai** \> **Perkėlimo užsakymai** \> **Sandėlio valdymas** ir pasirinkite perkėlimo užsakymo įvykdymo strategiją.

-   Norėdami nustatyti pardavimo užsakymų įvykdymo strategijas, spustelėkite **Gautinos sumos** \> **Sąranka** \> **Gautinų sumų parametrai** \> **Sandėlio valdymas** ir pasirinkite pardavimo užsakymo įvykdymo strategiją.

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a>Paketinio išleidimo proceso leidimas ir kiekio, kurį reikia išleisti kaip paketą, nurodymas

Užsakymai į sandėlį kaip paketas išleidžiami naudojant paketinę užduotį. Parametrai, atskiriantys užsakymus, kurie turi būti vykdomi naudojant paketinę užduotį, yra nustatomi pačioje paketinėje užduotyje.

Parametras **Kiekis** nurodo, ar kaip paketas turi būti išleistas visas kiekis, ar fiziškai rezervuotas kiekis. Parametras **Leisti išleisti iš dalies išleistus užsakymus** nurodo, ar kaip paketas išleidžiami užsakymai turi būti patvirtinti, ar atmesti, jei jie buvo iš dalies išleisti anksčiau.

-   Norėdami nustatyti perkėlimo užsakymų parametrus **Kiekis** ir **Leisti išleisti iš dalies išleistus užsakymus**, spustelėkite **Sandėlio valdymas** \> **Išleidimas į sandėlį** \> **Automatinis perkėlimo užsakymų išleidimas**.

-   Norėdami nustatyti pardavimo užsakymų parametrus **Kiekis** ir **Leisti išleisti iš dalies išleistus užsakymus**, spustelėkite **Sandėlio valdymas** \> **Išleidimas į sandėlį** \> **Automatinis pardavimo užsakymų išleidimas**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]