---
title: Eksperimento būsenos peržiūra
description: Šioje temoje paaiškinama, kokia yra eksperimento būsena eksperimento ciklo metu „Dynamics 365 Commerce”.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 5ae29fe5ac49d92c261c59d115664b50e87880a0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965119"
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