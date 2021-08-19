---
title: Darbo su kaštų apskaitos paslauga pradžia (privati peržiūra)
description: Šioje temoje pateikiama licencijavimo informacija ir kaštų apskaitos paslaugos diegimo instrukcijos.
author: AndersGirke
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 87d705aaff0dca73812a444c003088fd9b8293f077d6f42f94812631f0887a54
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719001"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a>Darbo su kaštų apskaitos paslauga pradžia (privati peržiūra)

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

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a>Kaip gauti kaštų apskaitos paslaugą (privati peržiūra)

> [!IMPORTANT]
> Norėdami naudoti kaštų apskaitos paslaugą, turite turėti plačiai pasiekiamą aplinką su įgalintais LCS (ne „OneBox” aplinką) ir „Dynamics 365 Supply Chain Management” 10.0.11 arba naujesnę versiją.

Norėdami užsiregistruoti privačiai kaštų apskaitos paslaugos peržiūrai, atsiųskite savo LCS aplinkos ID el. paštu [Kaštų apskaitos paslauga (privati peržiūra)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29). Patvirtinę jūsų dalyvavimą programoje, atsiųsime jums tolesnį el. laišką, kuriame bus kaštų apskaitos paslaugos beta raktas. Gavę beta raktą, galite pradėti [papildinio diegimą](#install).

## <a name="licensing"></a>Licencijavimas

Kaštų apskaitos paslauga licencijuojama kartu su standartinėmis atsargų apskaitos funkcijomis, kurios pasiekiamos „Supply Chain Management”. Nereikia pirkti papildomos licencijos, norint naudoti kaštų apskaitos paslaugą.

## <a name="install-the-add-in"></a><a name="install"></a>Papildinio įdiegimas

Norėdami naudoti kaštų apskaitos paslaugą, įdiekite „Supply Chain Management” kaštų apskaitos paslaugos papildinį, kaip aprašyta tolesnėje procedūroje.

1. [Užsiregistruokite](#sign-up) kaštų apskaitos paslaugai gauti (privati peržiūra).

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]