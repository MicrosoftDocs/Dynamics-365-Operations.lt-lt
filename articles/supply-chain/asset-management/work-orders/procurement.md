---
title: Įsigijimas
description: Šioje temoje aiškinama apie įsigijimą skiltyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1678dbe2432e4be46aebb40a12e73dfd695c3e77
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875796"
---
# <a name="procurement"></a>Įsigijimas


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Turto valdyme galite peržvelgti pirkimo paraiškas ir pirkimo užsakymus, susijusius su darbo užsakymais. Taip pat galima sukurti pirkimo užsakymą arba pirkimo paraišką iš darbo užsakymo.

Sąraše **Darbo užsakymo pirkimo paraiška** (**Turto valdymas** > **Bendrieji dalykai** > **Įsigijimas** > **Darbo užsakymo pirkimo paraiška**) galite matyti pirkimo paraiškų, susijusių su darbo užsakymais, sąrašą.

- Pasirinkite darbo užsakymo užduotį iš sąrašo **Darbo užsakymo pirkimo paraiška** ir spustelėkite mygtuką **Pirkimo paraiška**, kad atidarytumėte susijusią pirkimo paraišką.  
- Pasirinkite darbo užsakymą iš sąrašo **Darbo užsakymo pirkimo paraiška** ir spustelėkite mygtuką **Darbo užsakymas**, kad atidarytumėte susijusį darbo užsakymą.  
- Pasirinkite darbo užsakymo užduotį iš sąrašo **Darbo užsakymo pirkimo paraiška** ir spustelėkite mygtuką **Elementas naudojamas kur**, jei pageidaujate matyti, kur pasirinktoje eilutėje esantis elementas yra naudojamas Turto valdyme, atsižvelgiant į turtą, priežiūros užduoties tipo numatytąsias reikšmes, atsargines dalis ir darbo užsakymus. 

![1 pav.](media/08-work-orders.png)


Sąraše **Darbo užsakymo pirkimas** (**Įmonės turto valdymas** > **Bendrieji dalykai** > **Įsigijimas** > **Darbo užsakymo pirkimas**) galite matyti su darbo užsakymais susijusių pirkimo užsakymų sąrašą.

- Pasirinkite darbo užsakymo užduotį iš sąrašo **Darbo užsakymo pirkimas** ir spustelėkite mygtuką **Pirkimo užsakymas**, kad atidarytumėte susijusį pirkimo užsakymą.  
- Pasirinkite darbo užsakymo užduotį iš sąrašo **Darbo užsakymo pirkimas** ir spustelėkite mygtuką **Darbo užsakymas**, kad atidarytumėte susijusį darbo užsakymą.  
- Pasirinkite darbo užsakymo užduotį iš pirkimo sąrašo **Darbo užsakymas** ir spustelėkite mygtuką **Elementas naudojamas kur**, jei pageidaujate matyti, kur pasirinktoje eilutėje esantis elementas yra naudojamas Turto valdyme, atsižvelgiant į turtą, priežiūros užduoties tipo numatytąsias reikšmes, atsargines dalis ir darbo užsakymus. 

![2 paveikslėlis](media/09-work-orders.png)


Ankstesniuose sąrašuose dešinėje kiekvienos eilutės pusėje yra piktograma nurodanti pristatymo datos valdiklį. Jei piktogramoje yra šauktukas raudoname apskritime, tai reiškia, kad susijęs su pirkimo paraiška arba pirkimo užsakymu siuntinys gali vėluoti.

Pirkimo paraiškoje galite rasti datą, pagal kurią apskaičiuojama galima delsa, formos **Pirkimo paraiškos** > lauke **Pirkimo paraiškos antraštė** „FastTab“ > **Pageidaujama data**. Data lyginama su galima data darbo užsakyme arba darbo užsakymo užduotyje tokiu pačiu būdu kaip ir pirkimo užsakymo data.

Pirkimo užsakyme data, naudojama skaičiuoti galimai delsai, yra su pirkimo užsakymo eilute susijusi data, kurią galima rasti formoje **Pirkimo užsakymas** > pasirinkus pirkimo užsakymo eilutę > „FastTab“ **Eilutės išsami informacija** > skirtuką **Sąranka** > lauke **Patvirtinta pristatymo data**. Jei šis laukas yra tuščias data lauke **Pristatymo data** naudojama iš „FastTab“ **Pirkimo užsakymo antraštė**. Viena iš šių datų lyginama su galima data darbo užsakyme arba darbo užsakymo užduotyje šia tvarka:

- Darbo užsakymo faktinis pradžios laikas arba  

- Suplanuota pradžios data susijusioje darbo užsakymo užduotyje, arba  

- Suplanuota pradžios data darbo užsakyme, arba  

- Numatoma pradžios data darbo užsakyme  


## <a name="create-purchase-order-from-a-work-order"></a>Kurkite pirkimo užsakymą iš darbo užsakymo

Skiltyje **Visi darbo užsakymai** pasirinkite darbo užsakymo užduotį ir sukurkite susijusį pirkimo užsakymą arba pirkimo paraišką. Tai atliekama, kad būtų užtikrinti projekto ryšiai tarp pirkimo užsakymo arba pirkimo paraiškos ir darbo užsakymo.

1. Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

2. Sąrašuose **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai** pasirinkite darbo užsakymą, kuriam ketinate sukurti pirkimo užsakymą, ir spustelėkite **Redaguoti**.

3. Formoje **Darbo užsakymas** > „FastTab“ **Darbo užsakymo priežiūros užduotys** pasirinkite darbo užsakymo užduotį, kuriai ketinate sukurti pirkimo užsakymą.

4. Spustelėkite **Elemento užduotys** > **Pirkimo užsakymas iš darbo užsakymo užduoties**.

5. Sąrašų puslapyje **Projekto pirkimo užsakymai** spustelėkite **Naujas**.

6. Sukurkite pirkimo užsakymą.

>[!NOTE]
>Pirkimo paraiška kuriama beveik taip pat kaip ir kuriant pirkimo užsakymą. Vien skiriasi tai, kad anksčiau minėtoje procedūros 2 žingsnyje turite spustelėti **Elemento užduotys** > **Pirkimo paraiška iš darbo užsakymo užduoties**.

## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a>Projekto ryšys tarp darbo užsakymo ir pirkimo užsakymo arba pirkimo paraiškos

Pirkimo užsakymo eilutė arba pirkimo paraiškos eilutė yra susijusi su darbo užsakymo užduoties projektu ir susijusio projekto veiklos numeriu. Kai kuriate pirkimo užsakymą arba pirkimo paraišką iš darbo užsakymo užduoties, susijusio projekto veiklos numeris yra privalomas. Projekto veiklos numeris automatiškai įterpiamas į pirkimo užsakymą arba pirkimo paraišką, jei susijusiame darbo užsakyme yra darbo užsakymo užduočių, kurios visos naudoja tą patį priežiūros užduoties tipą. Jei darbo užsakymo užduočių priežiūros užduočių tipai skiriasi, projekto veiklos numeris turi būti įterptas rankiniu būdu.

Kad pamatytumėte ar įterptumėte veiklos numerį, susijusį su pirkimo užsakymo eilute, atidarykite **Darbo užsakymo pirkimas** > pasirinkite pirkimo užsakymo įrašą > spustelėkite pirkimo užsakymą stulpelyje **Pirkimo užsakymas** > „FastTab“ **Eilutės išsami informacija** > skirtuke **Projektas** > lauke **Veiklos numeris**.


![3 paveikslėlis](media/10-work-orders.png)


Panašiai, norėdami matyti arba įterpti veiklos numerį, susijusį su darbo užsakymo pirkimo paraiškos eilute, atidarykite **Darbo užsakymo pirkimo paraiška** > pasirinkite pirkimo paraiškos įrašą > spustelėkite pirkimo paraišką stulpelyje **Pirkimo paraiška** > „FastTab“ **Eilutės išsami informacija** > skirtuke **Projektas** > lauką **Veiklos numeris**.

