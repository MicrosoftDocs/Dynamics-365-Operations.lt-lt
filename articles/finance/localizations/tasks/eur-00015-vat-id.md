---
title: 'EUR-00015: PVM ID nustatymas'
description: Šioje procedūroje aprašomos būtinosios PVM ID registracijos sąlygos, pvz., registracijos tipo nustatymas ir jo priskyrimas registracijos kategorijai.
author: AdamTrukawka
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: atrukawk
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: TaxRegistrationType, TaxRegistrationTypeCreate, TaxRegistrationLegislationTypes
ms.openlocfilehash: 26120765b61a27cab544c37163a34a0ef18da30a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283792"
---
# <a name="eur-00015-set-up-vat-id"></a>EUR-00015: PVM ID nustatymas

[!include [banner](../../includes/banner.md)]

Šioje procedūroje aprašomos būtinosios PVM ID registracijos sąlygos, pvz., registracijos tipo nustatymas ir jo priskyrimas registracijos kategorijai. Daugiau informacijos apie registracijos ID ir registracijos ID apdorojimą, įskaitant būtinas sąlygas, galite rasti registracijos ID žinyno straipsnyje. 

Čia pateikta informacija taikoma visoms Europos šalims / regionams. Užduotis buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, kurios pirminis adresas yra Vokietijoje. Ši užduotis yra skirta sistemos administratoriams. Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
