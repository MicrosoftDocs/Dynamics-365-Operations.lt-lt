---
title: "Žurnalo eilučių ir dokumentų publikavimas iš „Excel“"
description: "Šioje temoje aiškinama, kaip įvesti ir publikuoti bendrųjų žurnalų eilutes iš „Microsoft Excel“. Pateikiama informacija apie įvairius šablonus, kuriuos galite naudoti, priklausomai nuo įvedamų operacijų tipo."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 087339cb3002b42bcb985c2ccfc2d97c752a817c
ms.lasthandoff: 03/31/2017


---

# <a name="publish-journal-lines-and-documents-from-excel"></a>Žurnalo eilučių ir dokumentų publikavimas iš „Excel“

Šioje temoje aiškinama, kaip įvesti ir publikuoti bendrųjų žurnalų eilutes iš „Microsoft Excel“. Pateikiama informacija apie įvairius šablonus, kuriuos galite naudoti, priklausomai nuo įvedamų operacijų tipo.

Vartotojai gali įvesti ir publikuoti finansinių žurnalų eilutes iš „Microsoft Excel“. Vartotojui sukūrus žurnalą naudojant mygtuką **Atidaryti eilutes programoje „Excel“** rodomi galimi naudoti šablonai. Šablonai sukurti taip, kad palaikytų tam tikrus scenarijus, tačiau žurnale palaikomi ne visi sąskaitos tipo deriniai. Šioje lentelėje rodomi galimi naudoti šablonai ir jų palaikomi sąskaitų tipai.
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Šablonas**             | **Palaikomi sąskaitų tipai**                                                                                             | **Kaip prieiti prie šablono**                                                          |
| Didžiosios knygos žurnalo eilutės     | Sąskaita: didžioji knyga, klientas, tiekėjas, banko korespondentinė sąskaita: didžioji knyga, klientas, tiekėjas, banko vidinė įmonė palaikoma.       | Pagrindinis žurnalas                                                                         |
| SF registras         | Sąskaita: tiekėjo korespondentinė sąskaita: didžiosios knygos vidinė įmonė nepalaikoma.                                                    | Mokėtinų sumų sąskaitos faktūros registras                                                                     |
| SF žurnalas          | Sąskaitos: tiekėjo korespondentinė sąskaita: didžiosios knygos vidinė įmonė palaikomos.                                                      | AP SF žurnalas                                                                      |
| Tiekėjo SF           |                                                                                                                         | Tiekėjo SF                                                                          |
| Kliento SF žurnalas | Sąskaita: kliento korespondentinė sąskaita: didžiosios knygos vidinė įmonė palaikoma.                                                     | Pagrindinis žurnalas                                                                         |
| Laisvos formos SF        |                                                                                                                         | Puslapyje **Laisvos formos SF** spustelėkite **Atidaryti naudojant „Excel“** („Microsoft Office“ piktograma). |
| Ilgalaikio turto žurnalas     | Priskirti turtą didžiajai knygai, bankui, klientui arba tiekėjui. Vidinė įmonė nepalaikoma.                                               | Ilgalaikio turto žurnalas                                                                     |
| Tiekėjo mokėjimų žurnalas   | Sąskaita: tiekėjo korespondentinė sąskaita: didžioji knyga, banko vidinė įmonė palaikoma.                                                 | Tiekėjo mokėjimų žurnalas                                                                  |
| Kliento mokėjimų žurnalas | Sąskaita: kliento korespondentinė sąskaita: didžioji knyga, banko vidinė įmonė palaikoma.                                               | Kliento mokėjimų žurnalas                                                                |
| Projekto išlaidų žurnalas  | Sąskaita: projektas, didžioji knyga, klientas, tiekėjo korespondentinė sąskaita: projektas, didžioji knyga, klientas, tiekėjo vidinė įmonė palaikoma. | Bendrojo žurnalo išlaidos (dalyje Projekto valdymas ir apskaita)                       |

Kai eilutės publikuojamos, jos įvertinamos, kad būtų įsitikinama, ar jos atitinka finansiniuose žurnaluose nustatytas taisykles. Kai eilutės paskelbtos, vartotojai gali redaguoti arba registruoti kvitus iš „Microsoft Dynamics 365 for Operations“. 

Norint į šabloną įtraukti finansinių dimensijų, reikalingi papildomi pokyčiai. Daugiau informacijos ieškokite [Dimensijų įtraukimas į „Microsoft Excel“ šabloną](\dev-itpro\financial-dimensions\add-dimensions-excel-templates). Kai dimensijos įtraukiamos į objektą, jas galima matyti naudojant „Excel“ kūrimo įrankį ir jas galima įtraukti į šabloną.




