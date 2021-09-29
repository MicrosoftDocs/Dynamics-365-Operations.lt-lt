---
title: Archyvuoti atspausdintas klientų sąskaitas faktūras su maišos numeriais
description: Šioje temoje paaiškinama, kaip įgalinti archyvavimą, kad būtų saugomos išspausdintos kliento sąskaitos-faktūros su „hash“ numeriais.
author: ilkond
ms.date: 09/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 093b1b8c516c0c659e7970d17d3f84b2ed0ccf8f
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500532"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a>Archyvuoti atspausdintas klientų sąskaitas faktūras su maišos numeriais

[!include [banner](../includes/banner.md)]

Kai kuriose šalyse nustatytas teisinis reikalavimas sistemoje laikyti apskaičiuotus „hash“ numerius kartu su kai kurių dokumentų spaudiniais. „Hash“ numerius galima naudoti teikiant ataskaitas valdžios institucijoms ir audito metu.

Šioje temoje paaiškinama, kaip konfigūruoti archyvavimą, kad būtų galima saugoti išspausdintas kliento sąskaitas-faktūras su „hash“ numeriais.

## <a name="prerequisites"></a>Būtinieji komponentai

- **Funkcijų valdymo** darbo srityje įjunkite funkciją **Archyvuoti išspausdintas kliento sąsaitas-faktūras su „hash“ numeriais.** Daugiau informacijos žr. [Funkcijų valdymo apžvalga](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Konfigūruokite spausdinamus reikiamų dokumentų formatus srityje **Spausdinimo valdymas**.

Ši funkcija taikoma toliau pateiktiems dokumentams.

**Gautinos sumos**
- Kliento SF
- Kliento kredito pažyma
- Laisvos formos SF
- Laisvos formos kredito pažyma

**Projektų valdymas ir apskaita**
- Projekto SF
- Projekto kredito pažyma

## <a name="configure-customer-master-data"></a>Klientų bendrųjų duomenų konfigūravimas
Norėdami konfigūruoti kliento duomenis ir įjungti galimybę automatiškai įrašyti išspausdintas sąskaitas-faktūras kaip priedus, atlikite nurodytus veiksmus.

1. Eikite į **Gautinos sumos** > **Visi klientai**. 
2. Pasirinkite klientą ir „FastTab“ skirtuke **Sąskaita-faktūra ir pristatymas**, esančiame skiltyje **EL. SĄSKAITA-FAKTŪRA**, laukelyje **el. sąskaitos-faktūros priedas** paspauskite **Taip**.

## <a name="print-invoices"></a>Spausdinti sąskaitą-faktūrą
Galite registruoti ir spausdinti bet kokį laisvos formos tekstą ir projekto sąskaitą-faktūrą arba kredito pažymą klientui, kurį sukonfigūravote ankstesnėje procedūroje.

Atidarykite puslapį **Priedai** išspausdintai sąskaitos-faktūrai. „FastTab“ skirtuke **Priedas**, esančiame laukelių grupėje **Papildomi duomenys**, laukelyje **Dokumento „hash“ numeris**, raskite įrašytą „hash“ numerį, apskaičiuotą išspausdintai sąskaitai-faktūrai.

![Priedo maišos numeris.](media/attach-hash-num.jpg)

