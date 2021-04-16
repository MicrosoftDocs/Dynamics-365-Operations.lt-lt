---
title: Sistemos grupavimas atidarytame darbų sąraše
description: Šioje temoje aprašoma, kaip mobiliajame įrenginyje filtruoti atidarytą darbų sąrašą.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a4faa358fc598859bf3b226b48b57594317f37d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831103"
---
# <a name="system-grouping-on-an-open-work-list"></a>Sistemos grupavimas atidarytame darbų sąraše

[!include [banner](../includes/banner.md)]

Naudodami sistemos grupavimo lauką, atidarytą darbų sąrašą galite filtruoti neredaguodami mobiliojo įrenginio meniu elemento.
Kai sistemos grupavimo funkcija taikytina, ją naudojant darbų sąrašą galima filtruoti viename darbo antraštės lauke. Sistemos grupavimo funkcijos negalite naudoti filtruodami eilutės lygio laukuose.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>Sistemos grupavimo funkcijos nustatymas atidarytame darbų sąraše
Norėdami sistemos grupavimo funkciją nustatyti atidarytame darbų sąraše, atlikite tolesnius veiksmus.

-   Mobiliojo įrenginio meniu elemente pasirinkite **Režimas: Netiesioginis** ir **Veiklos kodas: Rodyti atidarytą darbų sąrašą**. Tada galima rinktis iš tolesnių parinkčių. Norint sistemos grupavimo funkciją naudoti atidarytame darbų sąraše, šios parinktys yra būtinos. 

|        Parinktis         |                                                                                                                                                                                                                                                                         aprašymas                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Leisti naudoti sistemos grupavimo funkciją |                                                                                                                                                                                                                                                 Sistemos grupavimo funkciją galima naudoti su pasirinktu darbų sąrašo meniu elementu.                                                                                                                                                                                                                                                  |
| Sistemos grupavimo laukas | Galima naudoti tik jei <strong>Leisti sistemos darbą</strong> nustatyta kaip <strong>Taip</strong>. Pasirinkite lauką, nustatantį, kaip bus grupuojamas darbuotojų paėmimo darbas. Pavyzdžiui, jei pasirinksite lauką <strong>ShipmentId</strong>, norėdamas grupuoti išrinkimo darbus, darbuotojas nuskaitys siuntos ID. Tada visi siuntos darbai priskiriami darbuotojui. Šiam laukui reikia sukurti meniu elementą, kuris naudos esamus sistemos sugrupuotus darbus. Naudokite lauką <strong>Sistemos grupavimo žyma</strong>, kad darbuotoją informuotumėte, ką reikia nuskaityti. |
| Sistemos grupavimo žyma |                       Galima naudoti tik jei <strong>Leisti sistemos darbą</strong> nustatyta kaip <strong>Taip</strong>. Įveskite informaciją darbuotojui apie tai, ką reikia nuskaityti, kai paėmimo darbas yra sugrupuotas. Pavyzdžiui, jei naudojate lauką <strong>ShipmentId</strong> norėdami grupuoti paėmimo darbą pagal siuntą, lauke galite įvesti Siuntos ID. Šiam laukui reikia sukurti meniu elementą, kuris naudos esamus sistemos sugrupuotus darbus. Be to, lauke <strong>Sistemos grupavimas</strong> reikia pasirinkti lauką, pagal kurį grupuosite.                       |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]