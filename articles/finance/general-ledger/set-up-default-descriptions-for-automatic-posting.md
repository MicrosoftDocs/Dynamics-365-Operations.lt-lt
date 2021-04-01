---
title: Numatytųjų aprašų registruojant automatiškai nustatymas
description: Šioje temoje paaiškinta, kaip nustatyti numatytąjį tekstą, naudojamą aprašyti apskaitos įrašams, automatiškai registruojamiems didžiojoje knygoje. Galite nustatyti numatytąjį aprašo tekstą naudodami laisvos formos tekstą arba pasirinkdami fiksuotus kintamuosius.
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5955b796cbc7917eb5500b96c879d1b0819d2edc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204863"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a>Numatytųjų aprašų registruojant automatiškai nustatymas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinta, kaip nustatyti numatytąjį tekstą, naudojamą aprašyti apskaitos įrašams, automatiškai registruojamiems didžiojoje knygoje. Galite nustatyti numatytąjį aprašo tekstą naudodami laisvos formos tekstą arba pasirinkdami fiksuotus kintamuosius.

> [!NOTE]
> Atlikdami kai kurių tipų operacijas arba tam tikrose šalyse ar regionuose taip pat galite įtraukti tekstą iš laukų „Microsoft Dynamics AX“ duomenų bazėje, susietų su šių tipų operacijomis. Operacijos tipų bei šalių ir regionų sąrašą žr. skyriuje [Pasirinktinai: kito teksto įtraukimas į numatytuosius aprašus](#optional-add-other-text-to-default-descriptions), esančiame toliau šioje temoje.

## <a name="set-up-default-descriptions"></a>Numatytųjų aprašų nustatymas

1. Eikite į **Organizacijos administravimas** \> **Sąranka** \> **Numatytieji aprašai**.
2. Veiksmų srityje pasirinkite **Naujas**.
3. Lauke **Aprašas** pasirinkite operacijos tipą, kuriam bus kuriamas numatytasis aprašas.
4. Lauke **Kalba** pasirinkite kalbą, kuriai taikomas šis aprašas.
5. Lauke **Tekstas** įveskite numatytąjį aprašą. Tekstą galite įvesti lauke arba galite naudoti vieną arba kelis iš toliau nurodytų laisvos formos teksto kintamųjų:

    - **%1** – Pridėti operacijos datą.
    - **%2** – Pridėti identifikatorių, kuris atitinka dokumento tipą, kuris yra registruojamas didžiojoje knygoje. Pvz., naudojant su SF susijusius operacijų tipus, kintamasis **%2** įtraukia SF numerį.
    - **%3** – Pridėti identifikatorių, susijusį su dokumento tipu, kuris yra registruojamas didžiojoje knygoje. Pvz., naudojant su SF susijusius operacijų tipus, kintamasis **%3** įtraukia kliento sąskaitos numerį.

## <a name="optional-add-other-text-to-default-descriptions"></a>Pasirinktinai: kito teksto įtraukimas į numatytuosius aprašus

Atlikdami tam tikrų tipų operacijas tam tikrose šalyse ar regionuose, į numatytuosius aprašus galite įtraukti tekstą, gautą iš su šiais operacijų tipais susijusių laukų duomenų bazėje. Toliau pateiktame sąraše nurodyti operacijų tipai bei šalys ir regionai, kuriems taikoma ši galimybė.

**Operacijų tipai**

Atlikdami operacijas, kurių tipai susiję su šiais dokumentų tipais, į numatytuosius aprašus galite įtraukti kitą tekstą:

- Kliento SF
- Kliento kredito pažymos
- Kliento mokėjimai grynaisiais
- Tiekėjo mokėjimai
- Pardavimo užsakymai
- Pirkimo užsakymai
- Atsargų žurnalai
- Bendrasis planavimas (MRP)
- Ilgalaikis turtas

**Šalys ir regionai**

Ši parinktis galima šiose šalyse ir regionuose:

- Brazilija
- Kinija
- Čekijos Respublika
- Rytų Europa
- Vengrija
- Indija
- Japonija
- Lietuva
- Latvija
- Lenkija
- Rusija

### <a name="add-text-to-default-descriptions"></a>Teksto įtraukimas į numatytuosius aprašus

Atlikę veiksmus, nurodytus [Numatytųjų aprašų nustatymas](#set-up-default-descriptions) prieš tai šioje temoje, įtraukite į numatytuosius aprašus kitą tekstą atlikdami šiuos veiksmus:

1. „FastTab“ **Parametrai** pasirinkite **Pridėti**.
2. Lauke **Nuorodų lentelė** pasirinkite duomenų bazės lentelę, iš kurios norite įtraukti parametro duomenis į aprašą.
3. Lauke **Nuorodos laukas** pasirinkite lauką, iš kurio norite įtraukti parametro duomenis į aprašą.
4. Norėdami pridėti daugiau parametrų, kartokite 1–3 veiksmus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]