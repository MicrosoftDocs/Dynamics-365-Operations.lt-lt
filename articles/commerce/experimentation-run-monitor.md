---
title: Eksperimento vykdymas ir stebėjimas
description: Šioje temoje aprašoma, kaip vykdyti ir stebėti eksperimentą trečiosios šalies paslaugoje. Taip pat aprašoma, kaip atlikti variacijų keitimus po to, kai eksperimentas pradėtas.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4afc19ed103f204fec61ab20b88f767ad5f05b38
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792540"
---
# <a name="run-and-monitor-an-experiment"></a>Eksperimento vykdymas ir stebėjimas

Šioje temoje aprašoma, kaip vykdyti ir stebėti jūsų eksperimentą trečiosios šalies programoje ir kaip atlikti variacijų keitimus, jei reikia. Prieš atlikdami šioje temoje aprašytus veiksmus, pirmiausia turite [publikuoti](experimentation-preview-publish.md) jūsų eksperimentą „Commerce”. 

Toliau pateiktoje diagramoje rodomi visi veiksmai, susiję su eksperimento nustatymu ir vykdymu „e-Commerce“ svetainėje „Dynamics 365 Commerce”. Papildomi veiksmai aprašomi kitose temose.

[ ![Vartotojo eksperimentavimo kelionė – vykdymas ir stebėjimas](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)

Publikavus jūsų variacijas, visi veiksmai, kuriuos reikia atlikti „Commerce”, kad jūsų eksperimentas būtų vykdomas, yra baigti. Kitas veiksmas – nustatyti, kurią variaciją parodyti kiekvienam vartotojui, reikalaujančiam puslapio. Šį nustatymą atlieka trečiosios šalies paslauga, bet pirmiausia jūs turite suaktyvinti eksperimentą paslaugoje. Kadangi eksperimento aktyvavimo veiksmai priklauso nuo paslaugos, turite sekti instrukcijas, įtrauktas kartu su jūsų paslauga ar tiekėju. Jei eksperimentas nesuaktyvintas, vartotojai matys tik numatytąją puslapio versiją (variacijos nebus rodomos).

Jums reikės vykdyti eksperimentą tiek laiko, kad būtų surinkti statistiškai tinkamų rezultatų duomenys. Naudokite trečiosios šalies paslaugą, norėdami stebėti su eksperimentu susijusius duomenis ir analizę eksperimento vykdymo metu.

## <a name="adjust-your-variations"></a>Jūsų variacijų koregavimas
Jei dėl kokių nors priežasčių reikia koreguoti jūsų variacijas, atlikite toliau nurodytus veiksmus.

> [!IMPORTANT]
> Jei atliekate aktyvaus eksperimento keitimus „Commerce” arba trečiosios šalies paslaugoje, rezultatai gali būti reikšmingai paveikti. Apsvarstykite galimybę leisti eksperimentui įvykti ir tada sukurti naują didelių pakeitimų eksperimentą.

1. „Commerce” svetainių daryklės kairiojoje naršymo srityje pasirinkite **Eksperimentai** ir tada pasirinkite eksperimentą. 
1. Pasirinkite norimą atnaujinti variaciją iš išplečiamojo meniu.
1. Atlikite reikiamus keitimus, tada peržiūrėkite ir publikuokite variacijas. Daugiau informacijos žr. [Eksperimento peržiūra ir publikavimas](experimentation-preview-publish.md).
1. Norėdami atlikti bet kokius su eksperimento nustatymu susijusius keitimus, eikite į trečiosios šalies paslaugą.
    
## <a name="previous-step"></a>Ankstesnis veiksmas
[Eksperimento peržiūra ir publikavimas](experimentation-preview-publish.md)

## <a name="next-step"></a>Kitas veiksmas
[Variacijos skatinimas ir eksperimento užbaigimas](experimentation-review-complete.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]