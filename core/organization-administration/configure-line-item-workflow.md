---
title: "Eilutės elemento darbo eigos konfigūravimas"
description: "Šioje temoje paaiškinta, kaip konfigūruoti eilutės elemento darbo eigos elementą."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 6c2b2c863d0783bd436db57d9fd3c7c5aa8dba5c
ms.lasthandoff: 03/31/2017


---

# <a name="configure-a-line-item-workflow"></a>Eilutės elemento darbo eigos konfigūravimas

Šioje temoje paaiškinta, kaip konfigūruoti eilutės elemento darbo eigos elementą.

Norėdami darbo eigos rengyklėje konfigūruoti eilutės elemento darbo eigą, dešiniuoju pelės mygtuku spustelėkite elementą ir tada spustelėkite **Ypatybės**, kad atidarytumėte puslapį **Ypatybės**. Tada naudokite šias procedūras norėdami konfigūruoti eilutės elemento darbo eigos elementą.

## <a name="name-the-lineitem-workflow-element"></a>Pavadinimas lineitem darbo eigos elementui
Norėdami įvesti eilutės elemento darbo eigos elemento pavadinimą, atlikite šiuos veiksmus.

1.  Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.
2.  Lauke **Pavadinimas** įveskite unikalų eilutės elemento darbo eigos elemento pavadinimą.

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a>Nurodykite, ar tą pačią darbo eigą reikia naudoti visiems elementams apdoroti
Atlikite šiuos veiksmus, norėdami nurodyti, ar tą pačią darbo eigą reikia naudoti visiems dokumento elementams apdoroti.

1.  Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.
2.  Jei tą pačią darbo eigą reikia naudoti visiems dokumento elementams apdoroti, spustelėkite **Iškviesti vieną visų eilutės elementų darbo eigą**. Tada pasirinkite darbo eigą, kurią naudojant bus apdorojami eilutės elementai.
3.  Jei konkrečią darbo eigą reikia naudoti norint apdoroti elementus, kurie atitinka konkretaus rinkinio sąlygas, spustelėkite **Iškviesti atskirą kiekvienam eilutės elementui darbo eigą**. Tada, norėdami nurodyti sąlygų rinkinį, atlikite toliau nurodytus veiksmus.
    1.  Spustelėkite **Pridėti**.
    2.  Lentelėje pasirinkite sąlygą.
    3.  Skirtuke **Sąlygos pavadinimas** įveskite nustatomo sąlygų rinkinio pavadinimą.
    4.  Norėdami įvesti sąlygą, spustelėkite **Įtraukti sąlygą**.
    5.  Įveskite visas reikalingas papildomas sąlygas.
    6.  Norėdami patikrinti, ar įvestas sąlygų rinkinys yra sukonfigūruotas teisingai, spustelėkite **Tikrinti**. Puslapio **Tikrinti darbo eigos sąlygą** srityje **Tikrinti sąlygą** pasirinkite įrašą, o tada spustelėkite **Tikrinti**. Įvertinusi įrašą sistema nustatys, ar jis tenkina jūsų nurodytą sąlygą. Spustelėkite **Gerai** arba **Atšaukti**, kad grįžtumėte į puslapį **Ypatybės**.

    Skirtuke **Darbo eiga** pasirinkite darbo eigą, kurią naudojant bus apdorojami eilutės elementai, atitinkantys jūsų nurodytą sąlygų rinkinį.



