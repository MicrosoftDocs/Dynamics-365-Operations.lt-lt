---
title: Operacijų el. laiškų tinkinimas pagal pristatymo būdą
description: Šiame straipsnyje aprašoma, kaip nustatyti pasirinktinius el. laiškų šablonus, pagal konkrečius pranešimų tipus ir pristatymo būdus Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 0c0bd218c10a373d142ddcc7780c5339569f7a07
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275710"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a>Operacijų el. laiškų tinkinimas pagal pristatymo būdą

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip nustatyti pasirinktinius el. laiškų šablonus, pagal konkrečius pranešimų tipus ir pristatymo būdus Microsoft Dynamics 365 Commerce.

Perdavimo el. paštai gali būti dabar tinkinami pranešimo tipo deriniams (pavyzdžiui, **Sukurtas užsakymas**, **Paimtas užsakymas** ar **Išrašytas į sąskaitą užsakymas**) ir pristatymo būdas (pavyzdžiui, per naktį, atsiėmimas parduotuvėje ar atsiėmimas per langelį). Tinkinti perlaidos el. laiškai leidžia mažmeniniams prekiautojams pateikti jų klientams užsakymą su patirčių įgyvendinimu, kuris būtų pritaikytas prie užsakymo pristatymo būdo. Pavyzdžiui, „supakuoto užsakymo“ įvykis gali būti tinkintas taip, kad jis pateiktų atsiėmimo per langelį instrukcijas klientams, kurie tokį pasirenka. Kitu atveju, jis gali pateikti pristatymo vežėją ir informaciją klientams, kurie pasirenka siųsti savo užsakymą.

> [!NOTE]
> Norėdami naudoti tinkintos perlaidos el. laiškų funkciją, turite pirmiausia įjungti **Tinkintos perlaidos el. laiškų šablonai pagal pristatymo būdą** funkciją patekę į **Darbo aplinkos \> Funkcijų valdymas** „Commerce“ štabe.

El. laiškai gali būti tinkinti pagal pristatymo būdą tolesniems pranešimo tipams:

- **Užsakymo atšaukimas** – Šis el. laiško pranešimo tipas yra naujas.
- **Užsakymas sukurtas**
- **Užsakymas patvirtintas**
- **Užsakymo įrašymas į sąskaitą** – Šis el. laiško pranešimo tipas yra naujas. Jis gali būti naudojamas vietoje **Išsiųsto užsakymo** pranešimo tipas, kuris nusiųs pranešimą bet kurios sąskaitos įvykiui su pristatymo siuntimo būdu (ne atsiėmimo, vykdymo ar elektroninio pristatymo būdu).
- **Užsakymas paimtas**
- **Užsakymas supakuotas**
- **Užsakymas parengtas atsiėmimui** – Šis pranešimo tipas gali būti tinkintas pagal pristatymo būdą tik jei **Palaikyti keletą atsiėmimo pristatymo būdų** funkcija yra įjungta. Tokiu atveju, šis pranešimo tipas yra funkcija lygi **Supakuotas užsakymas** pranešimo tipui.
- **Mokėjimo atlikti nepavyko**
- **Pakeitimo užsakymas sukurtas**

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a>Konfigūruoti el. laiško šablonus konkrečiam pristatymo būdui

Šiai procedūrai, yra prielaida, kad jau sukūrėte naują, tinkintą el. laiško šabloną ir įtraukėte jį į **Organizacijos el. laiško šablonus** puslapį. Dėl informacijos apie tai, kaip sukurti ir naujinti el. laiškų šablonus, žr. [Sukurti el. laiško šablonus perlaidų įvykiams](email-templates-transactions.md).

Siekiant konfigūruoti el. laiško šablonus konkretiems pristatymo būdams „Commerce“ štabe, atlikite šiuos žingsnius.

1. Eikite į **Komercijos el. laiško pranešimo profilis**.
1. Skyriuje **Mažmeninės prekybos įvykio pranešimo nustatymai**, pasirinkite esantį pranešimo tipą.
1. Pasirinkus pranešimo tipą, pasirinkite **Konfigūruoti pristatymo būdus**.
1. Teksto laukelyje **Pristatymo būdai** rinkitės **Naujas**.
1. Naujoje eilutėje **Pristatymo būdas** laukelyje, rinkitės pristatymo būdą.
1. Laukelyje **El. pašto ID**, rinkitės el. laiško šabloną, kad talpintumėte į žemėlapį pristatymo būdą.
1. Pažymėkite žymės langelį **Aktyvusis**.
1. Pakartokite žingsnius nuo 4 iki 7, kad įtrauktumėte daugiau pristatymo būdų.
1. Pabaigus, rinkitės **Gerai**.

> [!NOTE]
> - Kai daugiau nei vienas pristatymo būdas yra tarp eilučių prekybos užsakyme, bus naudojamas nustatytasis šablonas. Nustatytasis šablonas yra šablonas, kuris patalpintas prie pranešimo tipo, puslapyje **„Commerce“ el. laiško pranešimo profilyje**.
> - Jei prekybos užsakymas turi pristatymo būdą, kuris nėra sukonfigūruotas tinkintam el. laiško šablonui, bus naudojamas numatytasis šablonas.

## <a name="additional-resources"></a>Papildomi ištekliai

[Skambučių centro užsakymų kūrimas](tasks/create-call-center-orders.md)

[Pristatymo režimo keitimas EKA](pos-change-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
