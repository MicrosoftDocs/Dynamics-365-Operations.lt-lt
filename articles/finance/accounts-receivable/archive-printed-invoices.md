---
title: Archyvuoti atspausdintas klientų sąskaitas faktūras su maišos numeriais
description: Šiame straipsnyje paaiškinama, kaip įgalinti archyvavimą saugoti išspausdintas kliento SF su hash numeriais.
author: ilkond
ms.date: 09/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3f19968b4f4cf76a48ac5485e915785e9be5c7db
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909191"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a>Archyvuoti atspausdintas klientų sąskaitas faktūras su maišos numeriais

[!include [banner](../includes/banner.md)]

Kai kuriose šalyse nustatytas teisinis reikalavimas sistemoje laikyti apskaičiuotus „hash“ numerius kartu su kai kurių dokumentų spaudiniais. „Hash“ numerius galima naudoti teikiant ataskaitas valdžios institucijoms ir audito metu.

Šiame straipsnyje paaiškinama, kaip konfigūruoti archyvavimą, kad būtų galima saugoti išspausdintas kliento SF su hash numeriais.

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

