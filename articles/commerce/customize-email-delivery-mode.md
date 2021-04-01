---
title: Tinkinti perlaidų el. paštus pagal pristatymo būdą
description: Šioje temoje aprašoma, kaip nustatyti tinkintus el. pašto šablonus konkretiems pranešimų tipams ir pristatymo būdams „Microsoft Dynamics 365 Commerce“.
author: stuharg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: d0d96ddb20b2b09751d8c0c0bf8af713de35279a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222638"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a>Operacijų el. laiškų tinkinimas pagal pristatymo būdą

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip nustatyti tinkintus el. pašto šablonus konkretiems pranešimų tipams ir pristatymo būdams „Microsoft Dynamics 365 Commerce“.

Perdavimo el. paštai gali būti dabar tinkinami pranešimo tipo deriniams (pavyzdžiui, **Sukurtas užsakymas**, **Paimtas užsakymas** ar **Išrašytas į sąskaitą užsakymas**) ir pristatymo būdas (pavyzdžiui, per naktį, atsiėmimas parduotuvėje ar atsiėmimas per langelį). Tinkinti perlaidos el. laiškai leidžia mažmeniniams prekiautojams pateikti jų klientams užsakymą su patirčių įgyvendinimu, kuris būtų pritaikytas prie užsakymo pristatymo būdo. Pavyzdžiui, „supakuoto užsakymo“ įvykis gali būti tinkintas taip, kad jis pateiktų atsiėmimo per langelį instrukcijas klientams, kurie tokį pasirenka. Kitu atveju, jis gali pateikti pristatymo vežėją ir informaciją klientams, kurie pasirenka siųsti savo užsakymą.

> [!NOTE]
> Norėdami naudoti tinkintos perlaidos el. laiškų funkciją, turite pirmiausia įjungti **Tinktintos perlaidos el. laiškų šablonai pagal pristatymo būdą** funkciją patekę į **Darbo aplinkos \> Funkcijų valdymas** „Commerce“ štabe.

El. laiškai gali būti tinkinti pagal pristatymo būdą tolesniems pranešimo tipams:

- **Užsakymo atšaukimas** – Šis el. laiško pranešimo tipas yra naujas.
- **Užsakymas sukurtas**
- **Užsakymas patvirtintas**
- **Užsakymo įrašymas į sąskaitą** – Šis el. laiško pranešimo tipas yra naujas. Jis gali būti naudojamas vietoje **Išsiųsto užsakymo** pranešimo tipas, kuris nusiųs pranešimą bet kurios sąskaitos įvykiui su pristatymo siuntimo būdu (ne atsiėmimo, vykdymo ar elektroninio pristatymo būdu).
- **Užsakymas paimtas**
- **Užsakymas supakuotas**
- **Užsakymas pasrengtas atsiėmimui** – Šis pranešimo tipas gali būti tinkintas pagal pristatymo būdą tik jei **Palaikyti keletą atsiėmimo pristatymo būdų** funkcija yra įjungta. Tokiu atveju, šis pranešimo tipas yra funkcija lygi **Supakuotas užsakymas** pranešimo tipui.
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
> - Jei prekybos užsakymas turi prisitatymo būdą, kuris nėra sukonfigūruotas tinkintam el. laiško šablonui, bus naudojamas numatytasis šablonas.

## <a name="additional-resources"></a>Papildomi ištekliai

[Skambučių centro užsakymų kūrimas](tasks/create-call-center-orders.md)

[Pristatymo režimo keitimas EKA](pos-change-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]