---
title: Eksperimento būsenos peržiūra
description: Šioje temoje paaiškinama, kokia yra eksperimento būsena eksperimento ciklo metu „Dynamics 365 Commerce”.
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
ms.openlocfilehash: f7bdd292893ee42d49bdf977a55d8b10896ca1cd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792444"
---
# <a name="review-the-status-of-an-experiment"></a>Eksperimento būsenos peržiūra
Yra daug veiksmų, susijusių su eksperimento nustatymu ir vykdymu „Dynamics 365 Commerce”. Informacijos apie eksperimento ciklą žr. [Eksperimentavimas „Dynamics 365 Commerce”](experimentation-overview.md).

Norėdami sužinoti, kurioje ciklo vietoje yra eksperimentas, „Commerce” svetainių daryklės kairiojoje naršymo srityje pasirinkite **Eksperimentai**. „Commerce“ ir trečiosios šalies paslaugoje, kuri naudojama eksperimentams kurti, variacijoms priskirti ir duomenims analizuoti, rodomas eksperimentų sąrašas su kiekvieno eksperimento būsena.

Stulpelyje **„Commerce” būsena** gali būti rodomos toliau pateiktos reikšmės. 
- **Juodraštis** – eksperimentas prijungtas prie „Commerce” puslapio arba fragmento ir yra redaguojamas.
- **Publikuota** – eksperimento variacijos paruoštos rodymui jūsų svetainėje. Jei eksperimentas vykdomas trečiosios šalies paslaugoje, svetainės vartotojai matys puslapio ar fragmento variaciją kaip pasirinktą trečiosios šalies paslaugos.
- **Nepublikuota** – eksperimentas nebėra pasiekiamas jūsų svetainėje. Svetainės vartotojai matys tik numatytąją puslapio ar fragmento versiją, net jei eksperimentas vykdomas trečiosios šalies paslaugoje.
- **Baigta** – eksperimentas buvo įvykdytas ir visiems svetainės vartotojams buvo skatinama variacija.

Taip pat **trečiosios šalies būsenos** stulpelyje gali būti rodomos toliau nurodytos reikšmės, nurodančios, kokia yra eksperimentų būsena trečiosios šalies paslaugoje.
- **Juodraštis** – eksperimentas nustatytas trečiosios šalies paslaugoje, bet nepradėtas.
- **Vykdoma** – eksperimentas buvo pradėtas trečiosios šalies paslaugoje ir jo metu renkami duomenys.
- **Pristabdyta** – eksperimentas pristabdytas ir duomenys nerenkami. Norėdami, kad duomenys vėl būtų renkami, turite tęsti eksperimento vykdymą.
- **Suarchyvuota** – eksperimentas buvo įvykdytas ir įrašytas į trečiosios šalies paslaugos katalogą, kad jį būtų galima naudoti ateityje.

Toliau pateiktoje diagramoje parodyti abu būsenų rinkiniai ir kaip jie susiję tarpusavyje.

[ ![Eksperimentų būsenos](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)


[!INCLUDE[footer-include](../includes/footer-banner.md)]