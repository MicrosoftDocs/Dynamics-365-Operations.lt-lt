---
title: Eilutės elemento darbo eigų konfigūravimas
description: Šioje temoje paaiškinta, kaip konfigūruoti eilutės elemento darbo eigos elementą.
author: ChrisGarty
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d6d9dcb99e00d4ce3f99e525a72421cb12af178
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070126"
---
# <a name="configure-line-item-workflows"></a>Eilutės elemento darbo eigų konfigūravimas

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Šioje temoje paaiškinta, kaip konfigūruoti eilutės elemento darbo eigos elementą.

Norėdami darbo eigos rengyklėje konfigūruoti eilutės elemento darbo eigą, dešiniuoju pelės mygtuku spustelėkite elementą ir tada spustelėkite **Ypatybės**, kad atidarytumėte puslapį **Ypatybės**. Tada naudokite šias procedūras norėdami konfigūruoti eilutės elemento darbo eigos elementą.

## <a name="name-the-line-item-workflow-element"></a>Eilutės elemento darbo eigos elemento pavadinimas

Norėdami įvesti eilutės elemento darbo eigos elemento pavadinimą, atlikite šiuos veiksmus.

1. Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.
2. Lauke **Pavadinimas** įveskite unikalų eilutės elemento darbo eigos elemento pavadinimą.

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a>Nurodykite, ar tą pačią darbo eigą reikia naudoti visiems elementams apdoroti

Atlikite šiuos veiksmus, norėdami nurodyti, ar tą pačią darbo eigą reikia naudoti visiems dokumento elementams apdoroti.

1. Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.
2. Jei tą pačią darbo eigą reikia naudoti visiems dokumento elementams apdoroti, spustelėkite **Iškviesti vieną visų eilutės elementų darbo eigą**. Tada pasirinkite darbo eigą, kurią naudojant bus apdorojami eilutės elementai.
3. Jei konkrečią darbo eigą reikia naudoti norint apdoroti elementus, kurie atitinka konkretaus rinkinio sąlygas, spustelėkite **Iškviesti atskirą kiekvienam eilutės elementui darbo eigą**. Tada, norėdami nurodyti sąlygų rinkinį, atlikite toliau nurodytus veiksmus.

    1. Spustelėkite **Pridėti**.
    2. Lentelėje pasirinkite sąlygą.
    3. Skirtuke **Sąlygos pavadinimas** įveskite nustatomo sąlygų rinkinio pavadinimą.
    4. Norėdami įvesti sąlygą, spustelėkite **Įtraukti sąlygą**.
    5. Įveskite visas reikalingas papildomas sąlygas.
    6. Norėdami patikrinti, ar įvestas sąlygų rinkinys yra sukonfigūruotas teisingai, spustelėkite **Tikrinti**. Puslapio **Tikrinti darbo eigos sąlygą** srityje **Tikrinti sąlygą** pasirinkite įrašą, o tada spustelėkite **Tikrinti**. Įvertinusi įrašą sistema nustatys, ar jis tenkina jūsų nurodytą sąlygą. Spustelėkite **Gerai** arba **Atšaukti**, kad grįžtumėte į puslapį **Ypatybės**.

    Skirtuke **Darbo eiga** pasirinkite darbo eigą, kurią naudojant bus apdorojami eilutės elementai, atitinkantys jūsų nurodytą sąlygų rinkinį.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]