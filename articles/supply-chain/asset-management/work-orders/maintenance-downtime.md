---
title: Darbo užsakymų prižiūrimo turto prastova
description: Šioje temoje aprašoma, kaip galite kurti darbo užsakyme pasirinkto turto prižiūrimo turto prastovos registracijas.
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
ms.openlocfilehash: 53487a0173453ef7a8f5ea818672d999fe71cb65
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020916"
---
# <a name="maintenance-downtime-for-work-orders"></a>Darbo užsakymų prižiūrimo turto prastova

[!include [banner](../../includes/banner.md)]


Galite kurti darbo užsakyme pasirinkto turto prižiūrimo turto prastovos registracijas. Ši galimybė naudinga, jei norite registruoti vienos arba keleto gamybos srityje esančių mašinų prižiūrimo turto prastovą. Pirma kuriate norimus naudoti prižiūrimo turto prastovos priežasčių kodus, pavyzdžiui, **gedimą** ir **planinį sustabdymą**. Tai daroma puslapyje **Prižiūrimo turto prastovos priežasčių kodai**. Paskui puslapyje **Prižiūrimo turto prastova** galite kurti prižiūrimo turto prastovos registracijas ir įtraukti atitinkamus prižiūrimo turto prastovos priežasčių kodus.

## <a name="create-maintenance-downtime-reason-codes"></a>Prižiūrimo turto prastovos priežasčių kodų kūrimas

1. Pasirinkite **Turto valdymas** > **Sąranka** > **Darbo užsakymai** > **Prižiūrimo turto prastovos priežasčių kodai**.

2. Pasirinkite **Naujas**.

3. Lauke **Prižiūrimo turto prastovos priežasties kodas** įveskite prižiūrimo turto prastovos priežasties kodo ID.

4. Tada lauke **Pavadinimas** įveskite pavadinimą.

5. Pažymėkite žymės langelį **Įtraukti į KPI**, jei priežasties kodas turi būti įtrauktas į turto pagrindinių efektyvumo indikatorių (KPI) skaičiavimus. Paprastai planiniai gamybos sustabdymai neturėtų būti įtraukiami į KPI skaičiavimus, nes jie nedaro įtakos numatomiems rezultatams.

6. Pasirinkite **Įrašyti**.

Paveikslėlyje pavaizduotas puslapio **Prižiūrimo turto prastovos priežasčių kodai** pavyzdys.

![1 pav.](media/15-work-orders.png)

Sukūrę norimus naudoti prižiūrimo turto prastovos priežasčių kodus, galite kurti darbo užsakymų ir turto prižiūrimo turto prastovos registracijas.


## <a name="create-maintenance-downtime-registrations"></a>Prižiūrimo turto prastovos registracijų kūrimas

1. Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

2. Pasirinkite darbo užsakymą, tada skirtuke **Darbo užsakymas**, grupėje **Turtas**, pasirinkite **Prižiūrimo turto prastova**.

3. Pasirinkite **Naujas**.

4. Laukuose **Nuo** ir **Iki** įterpkite prižiūrimo turto prastovos registracijos datą ir laiko intervalą.

>[!NOTE]
>Kai paliekate lauką **Iki**, trukmė valandomis automatiškai įterpiamą į lauką **Trukmė**.

5. Lauke **Prižiūrimo turto prastovos priežasties kodas** pasirinkite priežasties kodą.

6. Norėdami pridėti daugiau registravimų, kartokite 3–5 veiksmus.

7. Pasirinkite **Įrašyti**.

Toliau pateikiamoje iliustracijoje rodomas prižiūrimo turto prastovos registravimo pavyzdys.

![2 pav.](media/16-work-orders.png)

Kalendorius, naudojamas apskaičiuojant prižiūrimo turto prastovos registraciją, priklauso nuo jūsų pasirinkimo turto ir parametrų sąrankoje. Jei turto išteklius pasirenkamas perėjus į puslapio **Visas turtas** „FastTab” **Ilgalaikis turtas** lauką **Ištekliai**, naudojama susijusios išteklių grupės kalendoriaus sąranka, kaip parodyta toliau pateikiamame paveikslėlyje.

![3 pav.](media/17-work-orders.png)

Jei turto išteklius nepasirenkamas, naudojamas standartinis kalendorius, pasirinktas puslapyje **Turto valdymo parametrai**, kaip parodyta toliau pateikiamame paveikslėlyje.

![4 pav.](media/18-work-orders.png)

Spustelėkite **Turto valdymas** > **Užklausos** > **Prižiūrimo turto prastova**, kad pamatytumėte visų prižiūrimo turto prastovos registracijų apžvalgą.

>[!NOTE]
>Visi modulyje **Turto valdymas** naudojami kalendoriai nustatomi pasirinkus **Organizacijos administravimas** > **Sąranka** > **Kalendoriai** > **Kalendoriai**.

