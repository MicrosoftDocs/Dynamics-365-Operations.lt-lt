---
title: "Atsargų vietos"
description: "Atsargų vietos naudojamos su pagrindinio sandėliavimo (WMS I) funkcijomis ir jomis nustatoma, kur prekės saugomos ir iš kur prekės paimamos WMS I sandėlyje."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSLocation
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 6acdcfc8bbd412eaab7ac458a023b4a7f1cab445
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="inventory-locations"></a>Atsargų vietos

[!include[banner](../includes/banner.md)]


Atsargų vietos naudojamos su pagrindinio sandėliavimo (WMS I) funkcijomis ir jomis nustatoma, kur prekės saugomos ir iš kur prekės paimamos WMS I sandėlyje.

Ši tema taikoma priemonėms modulyje Atsargų valdymas. Ji nėra taikoma priemonėms modulyje Sandėlio valdymas.

Terminas vieta reiškia vietą, kurioje laikomos ir iš kurios paimamos prekės.

Kiekvienai vietai taip pat galima nurodyti, kur prekę galima padėti. Pagal numatytuosius parametrus, tai – ta pati vieta. Prekės paprastai padedamos ir paimamos iš tos pačios vietos pusės, bet ne visada. Pavyzdžiui, stelažuose laikomos prekės padedamos viename perėjime, o paimamos iš kito. Pagrindiniai duomenys teikia vietos pavadinimą, kuris paprastai nustatomas pagal jos koordinates: sandėlis, perėjimas, stelažas, lentynos ir talpyklos. Šį pavadinimą arba ID galima įvesti rankiniu būdu arba generuoti naudojant vietos koordinates, pvz., 01-02-03-4 puslapyje Atsargų vietos reiškia 1 perėjimą, 2 stelažą, 3 lentyną, 4 talpyklą.
Vietos ypatybės
-------------------

Vieta apibūdinama nurodant:
-   Dydis (aukštis, plotis, gylis, taigi ir tūris)
-   Sandėlio, perėjimo, stelažo, lentynos ir talpyklos vieta
-   Vietos tipas (buferinė vieta, paėmimo vieta, atvežimo rampa, pakrovimo rampa, gamybos įvesties vieta, tikrinimo vieta arba „kanban“ prekybos centras)

Norint patikrinti, ar operatorius konkrečiai prekei pasirinko tinkamą vietą, tinklo sistemose gali būti naudojamas tikrinimo tekstas. Šį tikrinimo tekstą galima sukurti neautomatiniu būdu arba nustatyti kaip numatytąjį.

## <a name="sort-codes"></a>Rūšiavimo kodai
Naudojant rūšiavimo kodus galima optimizuoti paėmimo eilučių, kuriose smulkiai aprašoma informacija, būtina prekėms iš atsargų paimti, tvarkymą, įskaitant išrinkimo dokumentą. Rūšiavimo kodus galima nurodyti pagal perėjimus ir kitas koordinates arba priskirti vietai rankiniu būdu.

## <a name="blocked-locations"></a>Užblokuotos vietos
Kartais galite norėti nurodyti, kad tam tikram laikui vieta užblokuota, pvz., remontui. Be to, vietą kartais gali tekti nurodyti kaip užblokuotą tik įeigai arba tik išeigai.
Medžio struktūra
--------------

Puslapyje Atsargų vietos galite peržiūrėti medžio struktūros pagal atsargų vietų koordinates sandėlio maketą apibrėžto rodymo formatu.
Atsargų vietų tvarkymas naudojant sandėlio formą
---------------------------------------------------

Galima kopijuoti vietas iš vieno sandėlio į kitą ir kurti vietas naudojant vedlį. Prieš paleisdami vedlį, turite įsitikinti, kad puslapyje Sandėlis nustatėte numatytuosius vietų pavadinimus.



<a name="see-also"></a>Taip pat žiūrėkite
--------

[Kurti naują sandėlio maketą (užduočių vedlys)](https://ax.help.dynamics.com/en/wiki/create-a-new-warehouse-layout/)




