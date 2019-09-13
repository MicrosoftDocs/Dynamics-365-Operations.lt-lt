---
title: Prižiūrimo turto prastova
description: Šioje temoje aprašoma prižiūrimo turto prastova modulyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918249"
---
# <a name="maintenance-downtime"></a>Prižiūrimo turto prastova


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Galite kurti darbo užsakyme pasirinkto turto prižiūrimo turto prastovos registracijas. Tai naudinga, jei norite registruoti vienos arba keleto gamybos srityje esančių mašinų prižiūrimo turto prastovą. Pirma kuriate norimus naudoti prižiūrimo turto prastovos priežasčių kodus, pavyzdžiui, gedimą ir planinį sustabdymą. Tai daroma pasirinkus **Prižiūrimo turto prastovos priežasčių kodai**. Paskui galite kurti prižiūrimo turto prastovos registracijas, pasirinkę **Prižiūrimo turto prastova**, ir įtraukti atitinkamus priežasčių kodus.

## <a name="create-maintenance-downtime-reason-codes"></a>Prižiūrimo turto prastovos priežasčių kodų kūrimas

1. Spustelėkite **Turto valdymas** > **Sąranka** > **Darbo užsakymai** > **Prižiūrimo turto prastovos priežasčių kodai**.

2. Spustelėkite **Naujas**.

3. Į lauką **Prižiūrimo turto prastovos priežasties kodas** įterpkite ID.

4. Lauke **Pavadinimas** įveskite priežasties kodo pavadinimą.

5. Pažymėkite žymės langelį **Įtraukti į KPI**, jei priežasties kodas turėtų būti įtrauktas į turto KPI skaičiavimus. Paprastai planiniai gamybos sustabdymai neturėtų būti įtraukiami į KPI skaičiavimus, nes jie nedaro įtakos numatomiems rezultatams.

6. Spustelėkite **Įrašyti**.

![1 pav.](media/15-work-orders.png)


Sukūrę norimus naudoti prižiūrimo turto prastovos priežasčių kodus, galite kurti darbo užsakymų ir turto prižiūrimo turto prastovos registracijas.


## <a name="create-maintenance-downtime-registrations"></a>Prižiūrimo turto prastovos registracijų kūrimas

1. Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

2. Pasirinkite darbo užsakymą ir spustelėkite **Prižiūrimo turto prastova**.

3. Spustelėkite **Naujas**.

4. Įterpkite prižiūrimo turto prastovos registracijos datą ir laiko intervalą laukuose **Nuo** ir **Iki**.

5. Kai paliekate lauką **Iki**, trukmė valandomis automatiškai įterpiamą į lauką **Trukmė**.

6. Lauke **Prižiūrimo turto prastovos priežasties kodas** pasirinkite priežasties kodą.

7. Jei norite įtraukti daugiau registracijų, pakartokite 3–6 veiksmus.

8. Spustelėkite **Įrašyti**.


![2 paveikslėlis](media/16-work-orders.png)


Kalendorius, naudojamas apskaičiuojant prižiūrimo turto prastovos registraciją, priklauso nuo jūsų pasirinkimo turto ir parametrų sąrankoje. Jei turto išteklius pasirenkamas perėjus į **Visas turtas** > FastTab **Ilgalaikis turtas** > lauką **Išteklius**, naudojama susijusios išteklių grupės kalendoriaus sąranka, kaip parodyta toliau pateikiamame paveikslėlyje.

![3 paveikslėlis](media/17-work-orders.png)


Jei turto išteklius nepasirenkamas, naudojamas standartinis kalendorius, pasirinktas **Turto valdymo parametrai**, kaip parodyta toliau pateikiamame paveikslėlyje.

![4 paveikslėlis](media/18-work-orders.png)


Spustelėkite **Įmonių turto valdymas** > **Užklausos** > **Prižiūrimo turto prastova**, kad pamatytumėte visų prižiūrimo turto prastovos registracijų apžvalgą.

>[!NOTE]
>Visi modulyje **Turto valdymas** naudojami kalendoriai nustatomi pasirinkus **Organizacijos administravimas** > **Sąranka** > **Kalendoriai** > **Kalendoriai**.

