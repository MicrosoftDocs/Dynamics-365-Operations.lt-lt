--- 
title: PVM ID nustatymas
description: "Šioje procedūroje aprašomos būtinosios PVM ID registracijos sąlygos, pvz., registracijos tipo nustatymas ir jo priskyrimas registracijos kategorijai."
author: v-oloski
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: b9db3b66b86f79540145e9da8e2a3dab728b12b8
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-vat-id"></a>PVM ID nustatymas

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje aprašomos būtinosios PVM ID registracijos sąlygos, pvz., registracijos tipo nustatymas ir jo priskyrimas registracijos kategorijai. Žinyno temoje Registracijos ID galite rasti papildomos informacijos apie registracijos ID ir registracijos ID apdorojimą, įskaitant būtinąsias sąlygas. 

Čia pateikta informacija taikoma visoms Europos šalims / regionams. Užduotis buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, kurios pirminis adresas yra Vokietijoje. Ši užduotis yra skirta sistemos administratoriams. Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.

1. Pasirinkite Organizacijos administravimas > Visuotinė adresų knygelė > Registracijos tipai > Registracijos tipai.
2. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
3. Lauke Pavadinimas įveskite VAT ID.
4. Lauke Aprašas įveskite PVM numeris.
5. Lauke Šalis / regionas įveskite arba pasirinkite reikšmę DEU
6. Lauke Unikalus pasirinkite Taip.
    * Pažymėkite šį žymės langelį, jei norite patikrinti, ar PVM ID yra unikalus.  
7. Lauke Pagrindinis šalies pasirinkite Taip.
    * Pažymėkite šį žymės langelį, jei PVM ID turi būti taikomas visiems nurodytos šalies / regiono adresams.  
8. Spustelėkite Kurti.
9. Spustelėkite Pridėti.
10. Lauke Šalis / regionas įveskite arba pasirinkite reikšmę ITA
11. Lauke Formatas įveskite ###########.
    * Kai įvedate šio tipo pasirinktos šalies / regiono registracijos ID, registracijos ID bus patikrintas pagal šį formatą.  
12. Pažymėkite žymės langelį Unikalus.
    * Pažymėkite šį žymės langelį, jei norite patikrinti, ar PVM ID yra unikalus.  
13. Pasirinkite žymės langelį Pirminės šalies.
    * Pažymėkite šį žymės langelį, jei PVM ID turi būti taikomas visiems nurodytos šalies / regiono adresams.  
14. Spustelėkite Įrašyti.
15. Pasirinkite Organizacijos administravimas > Visuotinė adresų knygelė > Registracijos tipai > Registracijos kategorijos.
16. Spustelėkite Naujas.
17. Lauke Šalis / regionas įveskite arba pasirinkite reikšmę VAT ID, DEU
18. Lauke Registracijos kategorija pasirinkite VAT ID.
    * Priskirkite registracijos tipą, kurį sukūrėte anksčiau, iš anksto nustatytai registracijos kategorijai.  
19. Spustelėkite Naujas.
20. Lauke Šalis / regionas įveskite arba pasirinkite reikšmę VAT ID, ITA
21. Lauke Registracijos kategorija pasirinkite VAT ID.
    * Priskirkite registracijos tipą, kurį sukūrėte, iš anksto nustatytai registracijos kategorijai.  
22. Spustelėkite Įrašyti.


