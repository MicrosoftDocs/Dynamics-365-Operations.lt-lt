---
title: Prižiūrimo turto kontroliniai sąrašai
description: Šioje temoje aprašomi prižiūrimo turto kontroliniai sąrašai modulyje Turto valdymas.
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
ms.openlocfilehash: 325ff1fa0811d6aac5189cc69f21483fce6b3e8f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875804"
---
# <a name="maintenance-checklists"></a>Prižiūrimo turto kontroliniai sąrašai


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Prižiūrimo turto kontroliniai sąrašai nustatomi pagal priežiūros užduočių tipus ir naudojami, kai dirbate su darbo užsakymu. Prižiūrimo turto kontrolinių sąrašų pildymas – tai darbo užsakymo parengimo dalis. Žr. skyrių [Priežiūros užduočių tipų kategorijos ir priežiūros užduočių tipai, priežiūros užduočių tipų variantai, priežiūros užduočių pardavimas ir prižiūrimo turto kontroliniai sąrašai](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md), kad gautumėte daugiau informacijos apie tai, kaip nustatyti priežiūros užduočių tipų prižiūrimo turto kontrolinius sąrašus formoje **Priežiūros užduočių tipų numatytieji parametrai**.

Kai dirbate su darbo užsakymo prižiūrimo turto kontroliniais sąrašais, galite pildyti iš anksto nustatytus prižiūrimo turto kontrolinius sąrašus, susijusius su priežiūros užduočių tipais. Tai pat galima įtraukti papildomų prižiūrimo turto kontrolinių sąrašų.

## <a name="fill-out-a-maintenance-checklist"></a>Prižiūrimo turto kontrolinio sąrašo pildymas

1. Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

2. Pasirinkite darbo užsakymą ir spustelėkite **Prižiūrimo turto kontrolinis sąrašas**.

3. Pasirinkę **Darbo užsakymo prižiūrimo turto kontrolinis sąrašas**, pamatysite visų darbo užsakymo užduočių prižiūrimo turto kontrolinius sąrašus. Jei darbo užsakymo užduočių priežiūros užduočių tipai skiriasi, darbo užsakymo užduočių prižiūrimo turto kontroliniai sąrašai gali skirtis. Pasirinkite darbo užsakymo užduotį, norėdami dirbti su susijusiu prižiūrimo turto kontroliniu sąrašu. Išsami informacija apie pasirinktą prižiūrimo turto kontrolinio sąrašo eilutę rodoma FastTab **Eilutės informacija**.

4. Užpildykite visas prižiūrimo turto kontrolinio sąrašo eilutes po vieną, eilės tvarka, kuria jos pateikiamos. Prižiūrimo turto kontrolinio sąrašo eilutė, kurios tipas yra Antraštė, naudojama kaip toliau pateikiamų prižiūrimo turto kontrolinio sąrašo eilučių grupės antraštė. Antraštės pildyti nebūtina, tačiau į visų tipų prižiūrimo turto kontrolinio sąrašo eilučių antraštes galia įtraukti **Pastaba**.

5. Jei su prižiūrimo turto kontrolinio sąrašo eilute yra susijusių instrukcijų, pažymimas žymės langelis **Instrukcijos**. Skaitykite prižiūrimo turto kontrolinio sąrašo pasirinktos eilutės instrukcijas FastTab **Eilutės informacija** > sekcijoje **Instrukcijos**.

6. Informacija, kurią reikia įvesti į prižiūrimo turto kontrolinio sąrašo eilutę, gali skirtis atsižvelgiant į susijusio prižiūrimo turto kontrolinio sąrašo tipą. Prižiūrimo turto kontrolinio sąrašo eilutę pildote, užpildydami laukus FastTab **Eilutės informacija**. Pavyzdžiui, į eilutę, kurios tipas yra Tekstas, įtraukiama **Pastaba**, paaiškinant minėtos kontrolinio sąrašo eilutės rezultatą. Į eilutę, kurios tipas yra Matavimas, įtraukiama įrangos rodoma **Skaitiklio vertė**; tai pat, jei reikia, įtraukiama **Pastaba**.

- Užpildę prižiūrimo turto kontrolinio sąrašo eilutę, pažymėkite eilutės žymės langelį **Patikrinta**, kad pažymėtumėte, jog eilute užpildyta. Jei norite atmesti prižiūrimo turto kontrolinio sąrašo eilutę, nes ji neaktuali darbo užsakymo užduočiai, pažymėkite eilutės žymės langelį **Netaikoma**. Jei prižiūrimo turto kontrolinio sąrašo eilutėje pažymėta, kad ji **Privaloma**, turite pažymėti, kad ji arba Patikrinta, arba Netaikoma.  
- Prižiūrimo turto kontrolinio sąrašo registracijas galima atnaujinti tik tuo atveju, jei darbo užsakymo ciklo būsena yra [Aktyvus](../setup-for-work-orders/work-order-lifecycle-states.md).  


## <a name="add-a-maintenance-checklist-line"></a>Prižiūrimo turto kontrolinio sąrašo eilutės įtraukimas

Prižiūrimo turto kontroliniai sąrašai kuriami pagal priežiūros užduoties tipo numatytosios reikšmės apibrėžimą ir perkeliami į naują darbo užsakymo užduotį. Jei reikia, galima įtraukti prižiūrimo turto kontrolinio sąrašo eilučių į darbo užsakymo užduotį. Rankiniu būdu įtrauktoms prižiūrimo turto kontrolinio sąrašo eilutėms priskiriama nuoroda Neautomatinis.

1. Pasirinkę **Darbo užsakymo prižiūrimo turto kontrolinis sąrašas**, pasirinkite darbo užsakymo užduotį, į kurią norite įtraukti prižiūrimo turto kontrolinį sąrašą.

2. FastTab **Prižiūrimo turto kontrolinio sąrašo eilutės** pasirinkite prižiūrimo turto kontrolinio sąrašo eilutę ir paspauskite rodyklės žemyn klaviatūros mygtuką, jei norite įtraukti naują eilutę po pasirinktos prižiūrimo turto kontrolinio sąrašo eilutės. Kitas numeris eilės tvarka automatiškai įtraukiamas į lauką **Eilutės numeris**. Taip pat galite pasirinkti prižiūrimo turto kontrolinio sąrašo eilutę ir spustelėti mygtuką **Įtraukti eilutę**, jei norite įtraukti naują eilutę virš pasirinktos prižiūrimo turto kontrolinio sąrašo eilutės.

3. Lauke **Pavadinimas** įveskite prižiūrimo turto kontrolinio sąrašo eilutės pavadinimą.

4. Lauke **Tipas** pasirinkite prižiūrimo turto kontrolinio sąrašo eilutės tipą. Laukai, susiję su kiekvienu prižiūrimo turto kontrolinio sąrašo tipu, rodomi FastTab **Eilutės informacija**.  
  a. „Tekstas” naudojamas įtraukiant prižiūrimo turto kontrolinio sąrašo eilutę, kurioje yra veiksmų aprašas teksto formatu. Šį prižiūrimo turto kontrolinio sąrašo tipą galima naudoti, jei norite, kad darbuotojas ką nors patikrintų arba apžiūrėtų, bet nesitikite konkretaus (išmatuojamo) rezultato. Įterpkite veiksmų aprašą į sekciją **Instrukcijos**, kuri yra FastTab **Eilutės informacija**. b. Antraštė naudojama kaip po antrašte pateikiamų prižiūrimo turto kontrolinio sąrašo eilučių grupės antraštė. Tai naudinga, jei įtraukėte keletą prižiūrimo turto kontrolinio sąrašo eilučių, kurias galima suskirstyti į konkrečias sritis. Įterpkite aprašomąjį pavadinimą lauke **Pavadinimas**.  
  c. Šablonas netaikomas, kai į darbo užsakymo užduotį prižiūrimo turto kontrolinio sąrašo eilutę įtraukiate rankiniu būdu.  
  d. Kintamasis naudojamas apibrėžiant prižiūrimo turto kontrolinio sąrašo eilutės galimą rezultatą kaip intervalą. Prižiūrimo turto kontrolinio sąrašo eilučių kintamųjų sąranka aprašoma skyriuje [Priežiūros užduočių tipų kategorijos ir priežiūros užduočių tipai, priežiūros užduočių tipų variantai, priežiūros užduočių pardavimas ir prižiūrimo turto kontroliniai sąrašai](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md). Lauke **Pavadinimas** įveskite kintamojo pavadinimą. Pasirinkite kintamąjį lauke **Kintamasis**. Įterpkite veiksmų aprašą į sekciją **Instrukcijos**, kuri yra FastTab **Eilutės informacija**.  
  e. Matavimas naudojamas registruojant konkretų matavimo rezultatą. Lauke **Pavadinimas** įveskite matavimo pavadinimą. FastTab **Eilutės informacija** pasirinkite **Skaitiklis** ir **Vienetas**. Įterpkite veiksmų aprašą į sekciją **Instrukcijos**.  

5. Baigę įterpti prižiūrimo turto kontrolinio sąrašo eilutes rankiniu būdu, užpildykite eilutes, kaip aprašyta pirmiau esančiame skyriuje.

>[!NOTE]
>Pasirinkę **Darbo užsakymo prižiūrimo turto kontrolinis sąrašas**, negalite panaikinti prižiūrimo turto kontrolinio sąrašo eilučių, kurioms priskirta nuoroda Užduoties tipas. Galite panaikinti tik tas prižiūrimo turto kontrolinio sąrašo eilutes, kurių nuoroda yra Neautomatinis ir kurias jūs arba kiti priežiūros darbuotojai sukūrė rankiniu būdu.


![1 pav.](media/14-work-orders.png)

