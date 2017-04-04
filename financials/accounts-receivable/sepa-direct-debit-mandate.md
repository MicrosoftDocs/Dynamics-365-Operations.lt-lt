---
title: "SEPA tiesioginio debeto įgaliojimo nustatymas"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: bb835f8dad16938b56365c7b06d4a0228f9aba66
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-sepa-direct-debit-mandate"></a>SEPA tiesioginio debeto įgaliojimo nustatymas



Bendros mokėjimų eurais erdvės (SEPA) tiesioginis debetas leidžia kreditoriui surinkti lėšas iš kliento banko sąskaitos, jei klientas kreditoriui suteikė pasirašytą įgaliojimą. Įgaliojimas, kurį pasirašo klientas, įgalioja kreditorių surinkti mokėjimą ir nurodo kliento bankui jį išmokėti. Šioje temoje yra organizuojamas parodyti procesas dėl SEPA tiesioginio debeto būdu mandatų.

## <a name="prerequisites"></a>Būtinieji komponentai
Pateiktoje lentelėje parodytos būtinosios sąlygos, kurias reikia įvykdyti prieš pradedant.

| Kategorija       | Būtinoji sąlyga                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Šalis/regionas | Pagrindinis juridinio subjekto adresas turi būti šioje šalyje / regione: Austrija, Belgija, Nyderlandai, Ispanija, Italija, Prancūzija arba Vokietija. |

1. Nustatyti numeraciją tiesioginio debeto įgaliojimuose kiekvieno tiesioginio debeto įgaliojimą turi turėti unikalų numerį. Naudodami puslapį **Numeracijos** sukurkite tiesioginio debeto įgaliojimų numeraciją. Naudosite šį identifikatorių, kad priskirtumėte numeraciją tiesioginio debeto įgaliojimų sistemai puslapyje **Gautinų sumų parametrai**.

2. Gautinų sumų parametrai, tiesioginio debeto būdu įgaliojimų naudojimo nustatyti į **sudaro gautinų sumų parametrai** puslapį ir nustatyti parametrus tiesioginio debeto mandatų. Norėdami nustatyti parametrus, ant to **tiesioginio debeto** skirtuko lape pakeisti numatytuosius parametrus, jums reikia. Tada, kad **skaičių sekas** skirtuko lape atnaujinti, **tiesioginio debeto įgaliojimą ID** srityje, skaičių seką, galite nustatyti anksčiau.

3. Nustatytos mokėjimo kortelėmis tiesioginio debeto mandatą, jūs turite nustatyti tiesioginio debeto įgaliojimų vykdyti mokėjimo būdą. Naudojate šį mokėjimo būdą pateikdami SF užklausas, kad būtų generuojami tiesioginio debeto mokėjimai. Naudokite **Mokėjimo būdų** puslapį, kad nustatytumėte mokėjimo būdą. Norėdami nustatyti tiesioginio debeto įgaliojimų mokėjimo būdą, turite atlikti toliau nurodytus papildomus mokėjimo būdo veiksmus.

-   Lauke **Mokėjimo tipas** pasirinkite **Elektroninis mokėjimas**.
-   Pasirinktinai: Jei manote, kad kiekvienas iš jūsų klientams daug mandatą, be to **laikotarpį** lauke, pasirinkite **SF**. Turėsite sumokėti bus sukurti kiekvienos sąskaitos faktūros, o kiekvieno mokėjimo naudos įgaliojimus, nurodyta sąskaitoje faktūroje.
-   Pasirinkite parinktį **Reikalauti įgaliojimo**, kad sukurtumėte mokėjimus naudojant tiesioginio debeto įgaliojimus. Parinktis **Reikalauti įgaliojimo** prieinama tik tada, jei **Mokėjimo tipo** lauke pasirenkate **Elektroninis mokėjimas**.

Taip pat žr [tiesioginio debeto apžvalga](sepa-direct-debit-overview.md) 

