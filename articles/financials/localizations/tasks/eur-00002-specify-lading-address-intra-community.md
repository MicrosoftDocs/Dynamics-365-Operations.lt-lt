--- 
title: 'EUR-00002: ES vidaus operacijos pakrovimo adreso nurodymas'
description: "Šioje procedūroje parodoma, kaip nustatyti pakrovimo adresą, skirtą ES vidaus prekybos operacijai."
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, TransportationDocument, LogisticsPostalAddress, SysLookupMultiSelectGrid,  VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 4db22444bee1590770a47ca5946941b530ae85ce
ms.contentlocale: lt-lt
ms.lasthandoff: 10/16/2018

---
# <a name="eur-00002-specifying-a-lading-address-for-an-intra-community-transaction"></a>EUR-00002: ES vidaus operacijos pakrovimo adreso nurodymas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip nustatyti pakrovimo adresą, skirtą ES vidaus prekybos operacijai. Pavyzdžiui, Vokietijos įmonės užsisako prekių iš tiekėjo, kurio darbo adresas yra Vokietijoje. Šis tiekėjas turi sandėlį Italijoje ir siunčia prekes iš ten. Šis pristatymas turi būti pateiktas „Intrastat“ ataskaitoje. Tokia pati procedūra gali būti taikoma kliento grąžinimams.
Ši procedūra taikoma visoms Europos šalims / regionams. Užduotis buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, kurios pirminis adresas yra Vokietijoje. Prieš atlikdami šią procedūrą, turite sukonfigūruoti „Intrastat“ ataskaitas. Ši procedūra skirta buhalteriams. Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.

1. Eikite į Mokėtinos sumos > Pirkimo užsakymai > Visi pirkimo užsakymai.
2. Spustelėkite Naujas.
3. Įveskite arba pasirinkite reikšmę
    * Pavyzdžiui, pasirinkite DE-001. Šio tiekėjo darbo adresas yra Vokietijoje.  
4. Spustelėkite GERAI.
5. Sąraše pažymėkite pasirinktą eilutę.
6. Lauke Prekės numeris įveskite arba pasirinkite reikšmę D0001.
7. Spustelėkite Įrašyti.
8. Veiksmų srityje spustelėkite Gauti.
9. Spustelėkite Transportavimo informacija.
10. Lauke Pakrovimo data ir laikas įveskite datą ir laiką.
11. Spustelėkite Įtraukti adresą.
12. Spustelėkite Naujas ir sukurkite naują adresą, kurio paskirtis yra Pakrovimas.
13. Lauke Pavadinimas arba aprašas įveskite Italijos.
14. Pasirinkite reikšmę Pakrovimas.
    * Atminkite, kad adreso paskirtis turi būti Pakrovimas.  
15. Lauke Šalis / regionas įveskite arba pasirinkite reikšmę ITA.
16. Spustelėkite Įrašyti.
17. Uždarykite puslapį.
18. Spustelėkite Įrašyti.
    * Patikrinkite, ar pakrovimo adresas teisingas.  
19. Uždarykite puslapį.
20. Veiksmų srityje spustelėkite Pirkti.
21. Spustelėkite Patvirtinti.
22. Veiksmų srityje spustelėkite Sąskaita faktūra.
23. Spustelėkite Sąskaita faktūra.
24. Lauke Numeris surinkite reikšmę.
25. Įveskite datą lauke Sąskaitos faktūros data.
26. Spustelėkite Numatyt. iš: gavimo dokumento kiekio, kad atidarytumėte išplečiamąjį dialogo langą.
27. Lauke Numatytasis eilučių kiekis pasirinkite Užsakytas kiekis.
28. Spustelėkite GERAI.
29. Spustelėkite Transportavimo informacija.
    * Įsitikinkite, kad prekės buvo atgabentos iš Italijos. Jei reikia, galite redaguoti pakrovimo informaciją.  
30. Uždarykite puslapį.
31. Spustelėkite Registruoti.
32. Uždarykite puslapį.
33. Pasirinkite Mokesčiai > Deklaracijos > Užsienio prekyba > Intrastat.
34. Spustelėkite Perkelti.
35. Lauke Tiekėjo SF pasirinkite Taip.
36. Spustelėkite GERAI.
37. Spustelėkite skirtuką Bendra.
    * Raskite naujai sukurtą eilutę ir patikrinkite, ar siuntėjas prekes išsiuntė iš Italijos.  


