---
title: Neatitikties operacijos
description: Šioje temoje aprašoma, kaip sukurti ir naudoti neatitikčių operacijas.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35619454af8b1cb1b7d383d393362f58d9dd0ea6
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573878"
---
# <a name="operations-for-nonconformances"></a>Neatitikties operacijos

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip sukurti ir naudoti neatitikčių operacijas.

Norėdami nurodyti darbų, kurie gali būti atlikti atsiradus patvirtintai neatitikčiai, klasifikaciją, naudokite puslapį **Operacijos**. Priskyrę susijusią operaciją neatitikčiai taip pat galite pateikti išsamią informaciją , pvz., apie susijusią medžiagą, darbo valandas ir papildomas išlaidas, būtinas atliekant operaciją. Sistema informacija naudojama skaičiuojant operacijos įvertintą savikainą. Išsami informacija ir įvertinta savikaina naudojamos kaip nuorodos. Susijusios kokybės operacijos skiriasi nuo galimų nurodyti gamybos maršruto operacijų.

> [!NOTE]
> Nors galite sekti išlaidas, laiką ir prekes, naudojamas operacijoje, susijusioje su neatitiktimi, jūsų įvesti duomenys yra tik informaciniai. Jis nėra automatiškai integruotas su DK, atsargų antrašu arba laiko ir **lankomumo** moduliu.

## <a name="examples-of-operations"></a>Operacijų pavyzdžiai

Jūs dirbate gamybos įmonei. Neatitiktis buvo sukurta ir patvirtinta prekėms, kurių kokybės tikrinimo atlikti nepavyko. Buvo sukurtas pataisymas, nurodantis, kad problema buvo susijusi su bloga įrenginio pereime. Norint pakeisti operaciją reikia atlikti keletą veiksmų, ir sekama kiekvienos operacijos atsakomybė. Pavyzdžiui, gali reikėti atlikti šiuos veiksmus:

1. Gamybos eilutė sustabdyta ir vykdomas išvalomas režimas.
1. Priežiūros personalas pakeičia esamą.
1. Kokybės užtikrinimo personalas tikrina mašiną prieš įjungdami jį atgal.

Pavyzdžiui, šios operacijos gali būti sukurtos, kad atspindėtų darbą, kuris turi būti atliktas:

- Sustabdyti gamybos eilutę.
- Išvalykite gamybos eilutę.
- Vykdyti mašinos priežiūrą.
- Patikrinti įrenginį.

## <a name="create-an-operation"></a>Kurti veiksmą

1. Eikite į **Atsargų valdymas \> Nustatymas \> Kokybės valdymas \> Operacijos**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį. Tada nustatykite šiuos laukus naujai eilutei:

    - **Operacija** – įveskite unikalų tikrinimo prietaiso ID pavadinimą ar operaciją.
    - **Aprašas** – įveskite išsamų bandymo operacijos aprašą.
    - **Tipas – jei operacija gali būti naudojama tik su neatitiktimis, susijusiomis su konkrečiu užsakymo tipu, pasirinkite užsakymo tipą (Pirkimo užsakymas** arba *arba Pardavimo* *užsakymas*).

1. Uždarykite puslapį.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Kokybės valdymo apžvalga](quality-management-processes.md)
- [Įjungti kiekio ir neatitikties valdymą](enable-quality-management.md)
- [Neatitikimo kūrimas ir apdorojimas](tasks/create-process-non-conformance.md)
- [Darbuotojai, atsakingi už neatitikties tvirtinimą](quality-responsible-workers.md)
- [Neatitikimų sulaikymo zonos](quality-quarantine-zones.md)
- [Neatitikimų diagnostikos tipai](quality-diagnostic-types.md)
- [Neatitikimų kokybės mokesčiai](quality-charges.md)
- [Neatitikimų diagnostikos problemos](quality-operations.md)
- [Sandėlio procesų kokybės valdymas](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
