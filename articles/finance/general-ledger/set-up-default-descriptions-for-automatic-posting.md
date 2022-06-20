---
title: Numatytųjų aprašų registruojant automatiškai nustatymas
description: Šiame straipsnyje paaiškinama, kaip nustatyti numatytąjį tekstą, kuris naudojamas apskaitos įrašams, automatiškai registruojamims į DK, aprašyti. Galite nustatyti numatytąjį aprašo tekstą naudodami laisvos formos tekstą arba pasirinkdami fiksuotus kintamuosius.
author: aprilolson
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 71982a7d5b1bb08d3e238646ea0b15f17260bdcc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904505"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a>Numatytųjų aprašų registruojant automatiškai nustatymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti numatytąjį tekstą, kuris naudojamas apskaitos įrašams, automatiškai registruojamims į DK, aprašyti. Galite nustatyti numatytąjį aprašo tekstą naudodami laisvos formos tekstą arba pasirinkdami fiksuotus kintamuosius.

> [!NOTE]
> Kai kuriuose operacijų tipuose kai kuriose šalyse ar regionuose taip pat galite įtraukti tekstą iš laukų, susijusių su tais operacijų tipais. Operacijų tipų ir šalių bei [regionų sąrašą žr. nebūtina: įtraukite kitą tekstą į numatytuosius](#optional-add-other-text-to-default-descriptions) aprašų skyrių vėliau šiame straipsnyje.

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

Kai atlikite veiksmus anksčiau šiame [straipsnyje skyriuje Nustatyti numatytuosius aprašus, atlikite šiuos veiksmus, norėdami į numatytuosius](#set-up-default-descriptions) aprašus įtraukti kitą tekstą.

1. „FastTab“ **Parametrai** pasirinkite **Pridėti**.
2. Lauke **Nuorodų lentelė** pasirinkite duomenų bazės lentelę, iš kurios norite įtraukti parametro duomenis į aprašą.
3. Lauke **Nuorodos laukas** pasirinkite lauką, iš kurio norite įtraukti parametro duomenis į aprašą.
4. Norėdami pridėti daugiau parametrų, kartokite 1–3 veiksmus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
