---
title: Ataskaitų generavimas įtraukiant turinį kaip neapdorotą XML
description: Galite sukurti elektroninių ataskaitų (ER) formatus, kurie generuoja siunčiamus dokumentus XLS formatu.
author: kfend
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 87b70d5893d71e5022205a2f39f8263edf6d5280
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277549"
---
# <a name="generate-reports-by-adding-content-as-raw-xml"></a>Generuoti ataskaitas įtraukiant turinį kaip neapdorotą XML

[!include[banner](../includes/banner.md)]

Galite naudoti naują formato elementą **NEAPDOROTAS XML**, skirtą kurti elektroninių ataskaitų (ER) formatus, generuojančius siunčiamus dokumentus XML formatu. Kai kuriais atvejais galite pageidauti įtraukti neapdorotus XML duomenis į šias ataskaitas dėl vienos ar daugiau iš šių priežasčių:

- Patogiau naudoti neapdorotą XML originaliam ataskaitos dizainui kurti ir vykdomai priežiūrai atlikti, nes XML struktūrą galima automatiškai sugeneruoti vykdant apdorojimo laiko išraišką. Todėl kuriant nereikia nustatyti kelių susiejimų keliems formato elementams. Tai įmanoma, kai naudojate duomenų šaltinius, apimančius informaciją, kurią galima naudoti XML elementams daryti, kol generuojama ataskaita.
- Jokių kitų metodų negalima naudoti pildant ataskaitą XML turiniu, kuris anksčiau buvo gautas ir saugotas sistemoje. Pvz., sugeneruotame XML atsakyme gali būti turinio iš XML užklausos, kuri buvo išsiųsta anksčiau.
- Jokio kito metodo negalima naudoti simboliams į sugeneruotą dokumentą įterpti pagal jų skaitinius kodus. Kai kuriose kalbose ir tarp simbolių šio tipo kodų nėra. Pavyzdžiai apima graikų kalbos raidę ro (ρ) ir HTML objekto kodus, pvz., \&eacute; yra *e*, kuriame yra aiškus kirtis (é).

> [!NOTE]
> Turėkite omenyje, kad sistema nekontroliuoja, ar XML turinys, kuris įvedamas į sugeneruotą dokumentą naudojant formato elementą **NEAPDOROTAS XML** yra teisingas.

Norėdami daugiau sužinoti apie šią funkciją, leiskite užduočių vedlius **Neapdorotų XML duomenų naudojimas ER generuojant XML ataskaitas (1 dalis: duomenų modelio kūrimas)** ir **Neapdorotų XML duomenų naudojimas generuojant XML ataskaitas (2 dalis: ataskaitos kūrimas ir paleidimas)**, kurie yra **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** verslo proceso dalis, juos galima atsisiųsti iš [„Microsoft“ atsisiuntimo centras](https://go.microsoft.com/fwlink/?linkid=874684). Šie užduočių vedliai parodys jums ER konfigūravimo procesą, norint įterpti neapdorotus XML duomenis į sugeneruotus failus.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
