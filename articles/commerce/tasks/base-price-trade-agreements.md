---
title: " Bazinė kaina ir prekybos sutartys"
description: Ši procedūra padeda kurti konkretaus kanalo pardavimo kainos prekybos sutartis.
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44dc059f7bfc3ba83a375c197ce67f1378a9bc9b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414407"
---
# <a name="base-price-and-trade-agreements"></a> Bazinė kaina ir prekybos sutartys

[!include [banner](../includes/banner.md)]

Ši procedūra padeda kurti konkretaus kanalo pardavimo kainos prekybos sutartis. Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.

1. **Naršymo sritis** eikite į **Moduliai > Mažmeninė prekyba ir prekyba > Kainodaros ir nuolaidų valdymas > Kainų grupės > Visos kainų grupės**. Naudojant kainų grupes, prekybos sutartys priskiriamos konkretiems kanalams. Naudojant kainų grupes prekybos sutartims kanalui priskirti, galima nustatyti konkretaus kanalo kainas.  
2. Spustelėkite **Naujas**.
3. Lauke **Kainų grupės** įveskite reikšmę.
4. Lauke **Pavadinimas** įveskite reikšmę.
5. Spustelėkite **Įrašyti**.
6. Uždarykite puslapį.
7. **Naršymo sritis** eikite į **Moduliai > Mažmeninė prekyba ir prekyba > Kanalai > Parduotuvės > Visos parduotuvės**.
8. Sąraše pasirinkite „Niujorkas“.
9. Veiksmų srityje spustelėkite **Parduotuvė**.
10. Spustelėkite **Kainų grupės**.
11. Spustelėkite **Naujas**.
12. Lauke **Kainų grupės** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
13. Sąraše raskite ir pasirinkite norimą įrašą.
14. Spustelėkite **Įrašyti**.
15. Uždarykite puslapį.
16. Uždarykite puslapį.
17. **Naršymo sritis** eikite į **Moduliai > Mažmeninė prekyba ir prekyba > Kanalai > Produktai ir kategorijos > Išleisti produktai pagal kategoriją**.
18. Sąraše spustelėkite saitą pasirinktoje eilutėje.
19. Spustelėkite **Redaguoti**.
20. Išplėskite „fastTab“ **Pardavimas**.
21. Lauke **Kaina** įveskite skaičių. Ši kaina naudojama, jei nerasta jokių taikomų prekybos sutarčių.  
22. Spustelėkite **Įrašyti**.
23. **Veiksmų srityje** spustelėkite **Pardavimas**.
24. Spustelėkite **Kurti prekybos sutartis**.
25. Spustelėkite **Naujas**.
26. Lauke **Pavadinimas** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
27. Sąraše pasirinkite **Prekyba**. Demonstraciniuose duomenyse žurnalo pavadinimo **Prekyba** numatytasis ryšys yra **Prekė (pardavimas)**. Tai reiškia, kad visos naujos sukurtos eilutės bus taikomos pardavimo kainos prekybos sutartims kaip numatytosios.  
28. **Veiksmų srityje** spustelėkite **Eilutės**.
29. Lauke **Šalies kodo tipas** pasirinkite Grupė.
30. Lauke **Sąskaitos pasirinkimas** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
31. Sąraše raskite ir pasirinkite norimą įrašą. Tokiu būdu bus baigtas kanalo susiejimas su kainų grupe arba prekybos sutartimi.  
32. Lauke **Elemento ryšiai** įveskite reikšmę.
33. Lauke **Sumos valiuta** įveskite skaičių.
34. „fastTab“ **Išsami informacija** pažymėkite arba atžymėkite žymės langelį **Surasti kitą**. Kai **Surasti kitą** nustatytas kaip Taip, kainodaros modulis toliau ieškos taikytinų prekybos sutarčių su mažesne pardavimo kaina. Kai **Surasti kitą** nustatytas kaip Ne, kainodaros modulis nebeieško ir naudoja prekybos sutartį.  
35. Spustelėkite **Registruoti.**
36. Spustelėkite **Gerai**.
37. Uždarykite puslapį.
38. **Veiksmų sritis** spustelėkite Parduoti.
39. Spustelėkite **Pardavimo kaina**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]