---
title: Prižiūrimo turto kontroliniai sąrašai
description: Šioje temoje aprašomi prižiūrimo turto kontroliniai sąrašai modulyje Turto valdymas.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderChecklist, EntAssetMobileWorkOrderLineChecklistDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9ece9abcbaed0a1881f6b6a0d1b2357bc87ef181636a37564709f62c6aa38475
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760567"
---
# <a name="maintenance-checklists"></a>Prižiūrimo turto kontroliniai sąrašai

[!include [banner](../../includes/banner.md)]



Prižiūrimo turto kontroliniai sąrašai nustatomi pagal priežiūros užduočių tipus. Prižiūrimo turto kontrolinių sąrašų pildymas – tai darbo užsakymo parengimo proceso dalis. Daugiau informacijos apie tai, kaip nustatyti priežiūros užduočių tipų prižiūrimo turto kontrolinius sąrašus puslapyje **Priežiūros užduočių tipų numatytosios reikšmės**, žr. [Priežiūros užduočių tipų kategorijos ir priežiūros užduočių tipai, priežiūros užduočių tipų variantai, priežiūros užduočių pardavimas ir prižiūrimo turto kontroliniai sąrašai](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

Kai dirbate su darbo užsakymo prižiūrimo turto kontroliniais sąrašais, galite pildyti iš anksto nustatytus prižiūrimo turto kontrolinius sąrašus, susijusius su priežiūros užduočių tipais. Taip pat galite įtraukti daugiau prižiūrimo turto kontrolinių sąrašų.


## <a name="fill-in-a-maintenance-checklist"></a>Prižiūrimo turto kontrolinio sąrašo pildymas

1. Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

2. Pasirinkite darbo užsakymą, tada veiksmų srityje, skirtuke **Darbo užsakymas**, grupėje **Eilutės**, pasirinkite **Prižiūrimo turto kontrolinis sąrašas**.

3. **Darbo užsakymo prižiūrimo turto kontroliniame sąraše** rodomi visų darbo užsakymo užduočių kontroliniai sąrašai. Jei darbo užsakymo užduočių priežiūros užduočių tipai skiriasi, darbo užsakymo užduočių prižiūrimo turto kontroliniai sąrašai gali skirtis. Pasirinkite darbo užsakymo užduotį, norėdami dirbti su susijusiu prižiūrimo turto kontroliniu sąrašu. Išsami informacija apie pasirinktą prižiūrimo turto kontrolinio sąrašo eilutę rodoma „FastTab” **Eilutės informacija**.

4. Užpildykite visas prižiūrimo turto kontrolinio sąrašo eilutes po vieną, eilės tvarka, kuria jos pateikiamos. Prižiūrimo turto kontrolinio sąrašo eilutę pildote, užpildydami laukus „FastTab” **Eilutės informacija**. Informacija, kurios reikia norint užbaigti eilutę, gali skirtis atsižvelgiant į eilutės tipą. Pavyzdžiui, į eilutę, kurios tipas yra **Tekstas**, įtraukiama pastaba, paaiškinanti jūsų patikros rezultatą. Į eilutę, kurios tipas yra **Matavimas**, įvedama įrangos rodoma skaitiklio vertė; tai pat, jei reikia, įtraukiama pastaba. Prižiūrimo turto kontrolinio sąrašo eilutė, kurios tipas yra **Antraštė**, naudojama kaip toliau pateikiamų prižiūrimo turto kontrolinio sąrašo eilučių grupės antraštė. Antraštės pildyti nebūtina. Kaip ir visų kitų tipų prižiūrimo turto kontrolinio sąrašo eilutėse, galite įtraukti pastabą į eilutę, kurios tipas – **Antraštė**.

5. Jei su prižiūrimo turto kontrolinio sąrašo eilute yra susijusių instrukcijų, pažymimas žymės langelis **Instrukcijos**. Skaitykite prižiūrimo turto kontrolinio sąrašo pasirinktos eilutės instrukcijas „FastTab” **Eilutės informacija** lauke **Instrukcijos**.

6. Užpildę prižiūrimo turto kontrolinio sąrašo eilutę, pažymėkite tos eilutės žymės langelį **Patikrinta**, kad pažymėtumėte, jog eilutė užpildyta. Jei norite atmesti prižiūrimo turto kontrolinio sąrašo eilutę, nes ji neaktuali darbo užsakymo užduočiai, pažymėkite eilutės žymės langelį **Netaikoma**. Jei prižiūrimo turto kontrolinio sąrašo eilutėje yra pažymėtas žymės langelis **Privaloma**, turite pažymėti žymės langelį **Patikrinta** arba **Netaikoma**.

>[!NOTE]
>Prižiūrimo turto kontrolinio sąrašo registracijas galima atnaujinti tik tuo atveju, jei darbo užsakymo ciklo būsena yra [Aktyvus](../setup-for-work-orders/work-order-lifecycle-states.md).  


## <a name="add-a-maintenance-checklist-line"></a>Prižiūrimo turto kontrolinio sąrašo eilutės įtraukimas

Prižiūrimo turto kontroliniai sąrašai kuriami pagal priežiūros užduoties tipo numatytosios reikšmės apibrėžimą ir perkeliami į naują darbo užsakymo užduotį. Jei reikia, galima įtraukti prižiūrimo turto kontrolinio sąrašo eilučių į darbo užsakymo užduotį. Rankiniu būdu įtrauktoms prižiūrimo turto kontrolinio sąrašo eilutėms priskiriama nuoroda **Neautomatinis**.

1. Puslapyje **Darbo užsakymo prižiūrimo turto kontrolinis sąrašas** pasirinkite darbo užsakymo užduotį, į kurią norite įtraukti prižiūrimo turto kontrolinį sąrašą.

2. „FastTab” **Prižiūrimo turto kontrolinio sąrašo eilutės** pasirinkite prižiūrimo turto kontrolinio sąrašo eilutę. Tada, norėdami įterpti naują eilutę po pasirinktos eilutės, paspauskite klavišą **Rodyklė žemyn**. Kitas numeris eilės tvarka automatiškai įvedamas į lauką **Eilutės numeris**. Norėdami įterpti naują eilutę prieš pasirinktą eilutę, pasirinkite **Įtraukti eilutę**. 

3. Lauke **Pavadinimas** įveskite prižiūrimo turto kontrolinio sąrašo eilutės pavadinimą.

4. Lauke **Tipas** pasirinkite prižiūrimo turto kontrolinio sąrašo eilutės tipą. Laukai, susiję su kiekvienu prižiūrimo turto kontrolinio sąrašo tipu, rodomi „FastTab” **Eilutės informacija**.
    - **Tekstas**: naudokite šį tipą norėdami įtraukti prižiūrimo turto kontrolinio sąrašo eilutę, kurioje yra tekstas, aprašantis, ką reikia atlikti. Pavyzdžiui, naudokite šį tipą, jei norite, kad darbuotojas ką nors patikrintų arba apžiūrėtų, bet nesitikite konkretaus (išmatuojamo) rezultato. Pasirinkę šį tipą, „FastTab” **Eilučių informacija**, lauke **Instrukcijos**, įveskite tekstą, aprašantį, ką reikia atlikti.
    - **Antraštė**: šio tipo prižiūrimo turto kontrolinio sąrašo eilutė naudojama kaip toliau pateikiamų prižiūrimo turto kontrolinio sąrašo eilučių grupės antraštė. Šis tipas yra naudingas, jei įtraukėte keletą prižiūrimo turto kontrolinio sąrašo eilučių, kurias galima suskirstyti į konkrečias sritis. Pasirinkę šį tipą, lauke **Pavadinimas** įveskite aprašomąjį pavadinimą.
    - **Šablonas**: šis tipas netaikomas, kai į darbo užsakymo užduotį prižiūrimo turto kontrolinio sąrašo eilutę įtraukiate rankiniu būdu.  
    - **Kintamasis**: šis tipas naudojamas apibrėžiant prižiūrimo turto kontrolinio sąrašo eilutės galimą rezultatą kaip intervalą. Daugiau informacijos apie tai, kaip nustatyti prižiūrimo turto kontrolinio sąrašo eilučių kintamuosius, žr. [Priežiūros užduočių tipų kategorijos ir priežiūros užduočių tipai, priežiūros užduočių tipų variantai, priežiūros užduočių pardavimas ir prižiūrimo turto kontroliniai sąrašai](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md). Pasirinkę šį tipą, lauke **Pavadinimas** įveskite aprašomąjį kintamojo pavadinimą. „FastTab” **Eilutės informacija**, lauke **Kintamasis**, pasirinkite kintamąjį. Lauke **Instrukcijos** įveskite tekstą, aprašantį, ką reikia atlikti.
    - **Matavimas**: naudokite šį tipą, norėdami įrašyti konkretų matavimą prižiūrimo turto kontrolinio sąrašo eilutėje. Pasirinkę šį tipą, lauke **Pavadinimas** įveskite matavimo pavadinimą. „FastTab” **Eilutės informacija**, laukuose **Skaitiklis** ir **Vienetas**, pasirinkite tinkamas vertes. Lauke **Instrukcijos** įveskite tekstą, aprašantį, ką reikia atlikti.

5. Baigę rankiniu būdu įtraukti prižiūrimo turto kontrolinio sąrašo eilutes, užpildykite eilutes taip, kaip aprašyta pirmesniame skyriuje **Prižiūrimo turto kontrolinio sąrašo pildymas**.

>[!NOTE]
>Puslapyje **Darbo užsakymo prižiūrimo turto kontrolinis sąrašas** negalite panaikinti prižiūrimo turto kontrolinio sąrašo eilučių, kurioms priskirta nuoroda **Užduoties tipas**. Galite panaikinti tik tas prižiūrimo turto kontrolinio sąrašo eilutes, kurių nuoroda yra **Neautomatinis** ir kurias jūs arba kiti priežiūros darbuotojai sukūrė rankiniu būdu.

Toliau pateikiamoje iliustracijoje rodomas prižiūrimo turto kontrolinio sąrašo pavyzdys.

![1 iliustracija.](media/14-work-orders.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]