---
title: Darbo su kaštų apskaitos paslauga pradžia
description: Šioje temoje pateikiama licencijavimo informacija ir kaštų apskaitos paslaugos diegimo instrukcijos.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: cbbce7eaac264973bf0b95ad5175bf70ed2b4ae9
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276944"
---
# <a name="get-started-with-the-cost-accounting-service"></a>Darbo su kaštų apskaitos paslauga pradžia

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> Šioje temoje nurodytos funkcijos yra privačiosios peržiūros versijos leidimo dalis. Šios temos turinys ir aprašomos funkcijos gali būti keičiami. Norėdami apie peržiūros leidimus gauti daugiau informacijos, žr. [DUK apie vienos versijos paslaugų naujinimus](../../fin-ops-core/fin-ops/get-started/one-version.md).

Kaštų apskaitos paslauga leidžia atlikti kelias atsargų apskaitas kaštų apskaitos didžiosiose knygose, kurias nustatėte. Galite susieti kiekvieną kaštų apskaitos didžiąją knygą su *konvencija*. Konvencija yra toliau pateiktų apskaitos strategijų tipų rinkinys.

- Savikainos objektas
- Įeigos matavimo vieneto pagrindas
- Savikainos srauto numanymas
- Savikainos elementas

> [!NOTE]
> Netgi po to, kai įjungėte kaštų apskaitos paslaugą, galite atlikti atsargų apskaitą „Microsoft Dynamics 365 Supply Chain Management”, kaip įprasta.

Kaštų apskaitos paslauga yra papildinys. Turite paslaugą įdiegti iš „Microsoft Dynamics Lifecycle Services” (LCS), kad jos funkcijos būtų prieinamos. Todėl prieš įjungdami paslaugą gamybos aplinkose galite pasirinkti, kad ji būtų vertinama tikrinimo aplinkoje.

Kaštų apskaitos paslauga šiuo metu nepalaiko visų išlaidų valdymo funkcijų, kurios yra „Dynamics 365 Supply Chain Management”. Todėl svarbu, kad įvertintumėte, ar funkcijų rinkinys, kurį šiuo metu galima naudoti, atitiks jūsų reikalavimus.

## <a name="licensing"></a>Licencijavimas

Kaštų apskaitos paslauga licencijuojama kartu su standartinėmis atsargų apskaitos funkcijomis, kurios pasiekiamos „Supply Chain Management”. Nereikia pirkti papildomos licencijos, norint naudoti kaštų apskaitos paslaugą.

## <a name="install-the-add-in"></a>Papildinio įdiegimas

> [!IMPORTANT]
> Norėdami naudoti kaštų apskaitos paslaugą, turite turėti plačiai pasiekiamą aplinką su įgalintais LCS (ne „OneBox” aplinką) ir „Dynamics 365 Supply Chain Management” 10.0.11 arba naujesnę versiją.

Norėdami naudoti kaštų apskaitos paslaugą, įdiekite „Supply Chain Management” kaštų apskaitos paslaugos papildinį, kaip aprašyta tolesnėje procedūroje.

1. Prisijunkite prie LCS.

1. Eikite į **Peržiūros funkcijų valdymas**.

1. Pasirinkite pliuso ženklą (**+**).

1. Lauke **Kodas** įveskite jūsų kaštų apskaitos paslaugos papildinio beta raktą. (Raktą turite gauti el. paštu.)

1. Pasirinkite **Atblokuoti**.

1. Atidarykite LCS aplinką, į kurią norite įtraukti paslaugą.

1. Eikite į **Išsami informacija**.

1. Slinkite žemyn iki „FastTab“ **Aplinkos papildiniai**.

1. Pasirinkite **Diegti naują papildinį**.

1. Pasirinkite **Kaštų apskaitos paslauga**.

1. Vadovaukitės diegimo vadovu ir sutikite su sąlygomis ir nuostatomis.

1. Pasirinkti **Diegti**.

1. „FastTab” **Aplinkos papildiniai** turėtumėte matyti, kad kaštų apskaitos paslauga įdiegta. Po kelių minučių būsena turėtų pasikeisti iš **Diegiama** į **Įdiegta**. (Gali reikėti atnaujinti puslapį, kad pamatytumėte šį pakeitimą.) Tada kaštų apskaitos paslauga parengta naudoti.

## <a name="set-up-the-integration"></a>Integravimo nustatymas

Norėdami nustatyti kaštų apskaitos paslaugos ir „Dynamics 365 Supply Chain Management” integravimą, atlikite tolesnius veiksmus.

1. Eikite į **Sistemos administravimas > Funkcijų valdymas**.

1. Pasirinkite **Tikrinti, ar yra naujinimų**.

1. Atidarykite skirtuką **Visi** ir ieškokite funkcijos pavadinimu *Kaštų apskaitos paslauga*.

1. Pasirinkite **Įjungti dabar**.

1. Eiti į **Kaštų valdymas > Kaštų apskaitos paslauga > Nustatymas > Kaštų apskaitos paslaugos parametrai > Integravimo parametrai**.

1. Lauke **Programos ID** įveskite toliau nurodytą kodą.<br> „08231eb2-a501-4edb-b3c5-aede5e5e0c3f“

1. Lauke **Duomenų paslaugos galinis punktas** įveskite toliau nurodytą URL.<br>https://operationsdataservice.operations365.dynamics.com/

1. Lauke **Kaštų apskaitos paslaugos galinis punktas** įveskite toliau nurodytą URL.<br>https://costaccountingservice.operations365.dynamics.com/

1. Kaštų apskaitos paslauga dabar parengta naudoti.

## <a name="related-resources"></a>Susiję ištekliai

[Kaštų apskaitos paslaugos pagrindinis puslapis](cost-accounting-service-home.md)
