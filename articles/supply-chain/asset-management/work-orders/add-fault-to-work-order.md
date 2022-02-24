---
title: Gedimo įtraukimas į darbo užsakymą
description: Šioje temoje aprašoma, kaip įtraukti gedimų registracijas į darbo užsakymus turto valdyme.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 083ceca9605ad044c172ba7aa23739d170f8c301
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019309"
---
# <a name="add-fault-to-work-order"></a>Gedimo įtraukimas į darbo užsakymą

[!include [banner](../../includes/banner.md)]



Į darbo užsakymą galite įtraukti gedimus, kurie buvo nustatyti gedimų dizaino įrankyje. Vienas ar daugiau gedimo įrašų turi būti susiję su turto tipais, naudojamais turtui, kuris yra pasirinktas darbo užsakyme. Daugiau informacijos apie sąranką žr. [Gedimų valdymas](../setup-for-work-orders/fault-management.md).

1. Pasirinkite **Turto valdymas** > **Bendra** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

2. Pasirinkite darbo užsakymą, kad įjungtumėte gedimų registravimą, tada veiksmų srityje, esančioje skirtuke **Darbo užsakymas**, grupėje **Turtas**, pasirinkite **Turto gedimas**.

3. „FastTab“ **Požymiai** pasirinkite **Įtraukti eilutę**. Iš eilės suteikiamas gedimo numeris automatiškai įvedamas į lauką **Gedimas**.

4. Lauke **Gedimo požymis** pasirinkite susijusį požymį.

5. Laukuose **Gedimo sritis** ir **Gedimo tipas** pasirinkite atitinkamas vertes.

6. Į lauką **Gedimo data** automatiškai įtraukiama esama data. Jei reikia, galite pasirinkti kitą datą.

7. „FastTab“ **Pažymėto požymio priežastys** įtraukite eilutę, aprašančią problemos priežastį.

8. „FastTab“ **Pažymėto požymio šalinimo priemonės** įtraukite eilutę, aprašančią galimą problemos sprendimą.

9. Pasirinkite **Įrašyti**.

Toliau esančiame paveikslėlyje pateiktas gedimo registravimo pavyzdys.

![1 pav.](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Turto gedimų rodinys

Sąraše **Turto gedimai** galite peržiūrėti visus užregistruotus turto gedimus.

Sąrašo puslapyje **Turto gedimai** galite peržiūrėti visus užregistruotus turto gedimus. Norėdami atidaryti puslapį, pasirinkite **Turto valdymas** > **Užklausos** > **Turto gedimas** > **Turto gedimai**.


## <a name="print-asset-fault-report"></a>Turto gedimo ataskaitos spausdinimas

Sąrašo puslapyje **Visas turtas** galite atspausdinti turto gedimo ataskaitą, kurioje nurodomi visos gedimų registracijos ir pateikiama grafinė gedimų statistikos apžvalga.

1. Pasirinkite **Turto valdymas** > **Bendra** > **Turtas** > **Visas turtas**.

2. Pasirinkite turtą, kuriam norite atspausdinti gedimų ataskaitą.

3. Veiksmų srityje, skirtuke **Bendra**, grupėje **Ataskaitos**, pasirinkite **Turto gedimas**.

4. Įveskite konkretų laikotarpį arba pažymėkite gedimo tipą.

5. Pasirinkite **Gerai**, kad atspausdintumėte ataskaitą.

>[!NOTE]
>Norėdami atspausdinti kelių turtų arba turto tipų gedimų ataskaitą, pasirinkite **Turto valdymas** > **Ataskaitos** > **Turtas** > **Turto gedimas**.

