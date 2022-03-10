---
title: Darbas su konfigūracijoje
description: Šioje temoje pateikiama pagrindinio darbo su elektroninės ataskaitos (ER) konfigūracijoje iš globalizavimo funkcijų darbo srities, apžvalga.
author: dkalyuzh
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4318399ee58ed54b29f8d360345b8930238ea9f2
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371966"
---
# <a name="work-with-configurations"></a>Darbas su konfigūracijoje

[!include [banner](../includes/banner.md)]

Elektroninių ataskaitų (ER) konfigūracijos yra vienas iš pagrindinių elektroninių SF išrašymo priemonių komponentų rinkinių. ER konfigūraciją sudaro failo struktūros nustatymas ir pakeitimo taisyklių rinkinys duomenims transformuoti dviem būdais:

- **Eksportuoti ER formato konfigūraciją** – ši konfigūracija keičia duomenis iš suvienodintos vidinės struktūros (ER modelio) į elektroninio failo formatą.
- **Importuoti ER formato konfigūraciją** – ši konfigūracija transformuoja duomenis iš elektroninio failo formato į suvienodintą vidinę struktūrą (ER modelį).

Be iš anksto nustatyto formato siunčiamų elektroninių failų generavimo, ER konfigūracijos labai nori išanalizuoti gaunamus pranešimus iš išorinių žiniatinklio tarnybų kaip atsakymus. Ši funkcija padeda sukurti konfigūruojamą logiką, kuri suteikia ryšio su išoriniais kanalais rezultatus, konvertuoti tuos rezultatus (kodus, pranešimus ir žurnalus) į vartotojo perskaitytą struktūrą, ir perduoti šią informaciją kliento programai.

Norėdami pradėti naudoti ER konfigūracijas savo elektroninio SF išrašymo priemonėje, **turite** susieti jas su priemone ir padaryti jas pasiekiamas dabartinės priemonės versijos skirtuke Konfigūracijos. Galite dirbti su susieta ER konfigūracija pasirinkdami **Pridėti**, **Naikinti**, **Redaguoti** arba **Peržiūrėti**.

Prieš pridėdami saitą į ER konfigūraciją, konfigūracija turi būti jūsų reguliavimo konfigūracijos tarnybos (RCS) saugykloje. Norėdami peržiūrėti ER konfigūracijas, kurios galimos jūsų RCS saugykloje, atlikite šiuos veiksmus.

1. Prisijunkite prie jūsų RCS abonemento.
2. Darbo srities **Elektroninės ataskaitos** dalyje **Konfigūracijos** pasirinkite plytelę **Ataskaitų konfigūracijos**.

Informacijos apie tai, kaip sukurti naują ER konfigūraciją arba importuoti esamą ER konfigūraciją iš visuotinės saugyklos, ieškokite elektroninės [ataskaitos](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Norėdami koreguoti susietą ER konfigūraciją, skirtuke **Konfigūracijos** pasirinkite Redaguoti, kad **būtų** galima naudoti dabartinę elektroninių SF išrašymo priemonę. Sistema automatiškai sukuria ER konfigūracijos versiją. Jei aktyviosios konfigūracijos teikėjas nesukūrė dabartinės versijos, sistema sukuria išvestinę versiją, kuri naudoja jūsų konfigūracijos teikėją. Jei aktyvių konfigūracijų teikėjas sukūrė dabartinę versiją, sistema sukuria naują versiją. Abiem atvejais galite modifikuoti sukurtą versiją ir automatiškai atlikti visus reikiamus naujinimus.
