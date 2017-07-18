---
title: "Sistemos grupavimas atidarytame darbų sąraše"
description: "Šioje temoje aprašoma, kaip mobiliajame įrenginyje filtruoti atidarytą darbų sąrašą."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: dbf0e49b1156c54cd37bbbe57ca564cdbc45fb2d
ms.contentlocale: lt-lt
ms.lasthandoff: 06/20/2017


---

# <a name="system-grouping-on-an-open-work-list"></a>Sistemos grupavimas atidarytame darbų sąraše

[!include[banner](../includes/banner.md)]

Naudodami sistemos grupavimo lauką, atidarytą darbų sąrašą galite filtruoti neredaguodami mobiliojo įrenginio meniu elemento.
Kai sistemos grupavimo funkcija taikytina, ją naudojant darbų sąrašą galima filtruoti viename darbo antraštės lauke. Sistemos grupavimo funkcijos negalite naudoti filtruodami eilutės lygio laukuose.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>Sistemos grupavimo funkcijos nustatymas atidarytame darbų sąraše
Norėdami sistemos grupavimo funkciją nustatyti atidarytame darbų sąraše, atlikite tolesnius veiksmus.

-   Mobiliojo įrenginio meniu elemente pasirinkite **Režimas: Netiesioginis** ir **Veiklos kodas: Rodyti atidarytą darbų sąrašą**. Tada galima rinktis iš tolesnių parinkčių. Norint sistemos grupavimo funkciją naudoti atidarytame darbų sąraše, šios parinktys yra būtinos. 

| Parinktis        | aprašymas   | 
| ------------- | ------------- |
| Leisti naudoti sistemos grupavimo funkciją   | Sistemos grupavimo funkciją galima naudoti su pasirinktu darbų sąrašo meniu elementu.| 
| Sistemos grupavimo laukas   | Galima naudoti tik jei **Leisti sistemos darbą** nustatyta kaip **Taip**. Pasirinkite lauką, nustatantį, kaip bus grupuojamas darbuotojų paėmimo darbas. Pavyzdžiui, jei pasirinksite lauką **ShipmentId**, norėdamas grupuoti išrinkimo darbus, darbuotojas nuskaitys siuntos ID. Tada visi siuntos darbai priskiriami darbuotojui. Šiam laukui reikia sukurti meniu elementą, kuris naudos esamus sistemos sugrupuotus darbus. Naudokite lauką **Sistemos grupavimo žyma**, kad darbuotoją informuotumėte, ką reikia nuskaityti. |
| Sistemos grupavimo žyma   | Galima naudoti tik jei **Leisti sistemos darbą** nustatyta kaip **Taip**. Įveskite informaciją darbuotojui apie tai, ką reikia nuskaityti, kai paėmimo darbas yra sugrupuotas. Pavyzdžiui, jei naudojate lauką **ShipmentId** norėdami grupuoti paėmimo darbą pagal siuntą, lauke galite įvesti Siuntos ID. Šiam laukui reikia sukurti meniu elementą, kuris naudos esamus sistemos sugrupuotus darbus. Be to, lauke **Sistemos grupavimas** reikia pasirinkti lauką, pagal kurį grupuosite.|
