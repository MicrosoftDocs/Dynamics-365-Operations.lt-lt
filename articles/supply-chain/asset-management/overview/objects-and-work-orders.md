---
title: Turtas ir darbo užsakymai
description: Šioje temoje aprašomas turtas ir darbo užsakymai modulyje „Turto valdymas“.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b56234eac247185c5cd4d8ab45a65d258013acd
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571374"
---
# <a name="assets-and-work-orders"></a>Turtas ir darbo užsakymai

[!include [banner](../../includes/banner.md)]

 

Šioje temoje aprašomas turtas ir darbo užsakymai modulyje „Turto valdymas“. Turtas ir darbo užsakymai yra pagrindinės modulio „Turto valdymas“ dalys. *Turtas* yra mašina arba mašinos dalis, kurią reikia nuolat prižiūrėti ir teikti aptarnavimo paslaugas. Turtas gali būti kuriamas taikant hierarchinę struktūrą ir gali būti siejamas su funkcinėmis vietomis. Priežiūros užduotys gali būti planuojamos visais lygiais turto struktūroje.

Konfigūruojami įvairūs kiekvieno turto duomenys, pvz., produkto informacija ir turto specifikacija, taip pat reikiami priežiūros planai. Toliau pateiktame paveikslėlyje rodoma turto duomenų ir turto priskyrimo užduočių tipams apžvalga. Raudonas tekstas naudojamas pavyzdžiams, rodantiems paveldėjimą ir priklausomybes, pateikti.

![Diagrama, rodanti turto duomenis, susijusius su užduočių tipais](media/05-overview-image.png)

Kiekvienas darbo užsakymas turi darbo užsakymo tipą, pvz., prevencinė priežiūra, koreguojamoji priežiūra arba patikra. Darbo užsakymą sudaro viena ar daugiau darbo užsakymo užduočių. Kiekviena darbo užsakymo užduotis apibrėžia užduotį, kurią reikia atlikti su turtu ir susijusiu užduoties tipu. Susijusių užduočių tipų pavyzdžiai yra 10 000 km, 50 000 km, kapitalinis remontas po 1 metų ir saugos patikra. Vienas darbo užsakymas gali būti siejamas su keliais turtais.

Toliau pateiktame paveikslėlyje rodoma rakto duomenų darbo užsakyme apžvalga.

![Diagrama, rodanti pagrindinius darbo užsakymo duomenis](media/06-overview-image.png)

Darbo užsakymą galima susieti su kitu darbo užsakymu, o užduočių tipuose gali būti kitų užduočių, kurie sudaro darbo užsakymą. Apskritai, priklausomybės tarp darbo užsakymų nėra. Todėl gali keistis darbo užsakymų ciklo būsena ir juos galima planuoti nepriklausomai vieną nuo kito.

Darbo užsakymai gali būti kuriami įvairiais būdais, susijusiais su korekcine, prevencine arba einamąja priežiūra. Kategorijas taip pat galite kurti neautomatiniu būdu. Toliau pateiktame paveikslėlyje parodyta automatinio arba neautomatinio darbo užsakymų kūrimo proceso apžvalga.

![Diagrama, rodanti automatinį arba rankinį darbo užsakymų kūrimą](media/07-overview-image.png)

Kai norite planuoti ir vykdyti darbo užsakymo priežiūros užduotį, reikia atlikti keletą veiksmų. Toliau pateiktame paveikslėlyje parodyta darbo užsakymo vykdymo apžvalga.

![Diagrama, rodanti darbo užsakymo vykdymo apžvalgą](media/08-overview-image.png)

> [!NOTE]
> Kai dirbate programoje Dynamics 365 Supply Chain Management ir modulyje **Turto valdymas**, norėdami sukurti naują įrašą, pasirenkate **Naujas**, norėdami atnaujinti esamą įrašą, pasirenkate **Redaguoti** ir norėdami įrašyti naujus ar redaguotus duomenis, pasirenkate **Saugoti**.
