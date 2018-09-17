--- 
title: "PVM priskyrimas ir perrašymai"
description: "Šioje procedūroje parodoma, kaip PVM grupes priskirti mažmeninės prekybos kanalams."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 816e00e4238cb0d90a2aea9b2bc070d31504c2ce
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="sales-tax-assignment-and-overrides"></a>PVM priskyrimas ir perrašymai

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip PVM grupes priskirti mažmeninės prekybos kanalams. Joje taip pat paaiškinamas procesas, kurio metu sukuriamas naujas PVM perrašymas ir priskiriamas esamai PVM perrašymo grupei. Šiai procedūrai

naudojama įmonė USRT demonstraciniams duomenims.

1. Eikite į Mažmeninė prekyba ir prekyba > Kanalai > Mažmeninės prekybos parduotuvės > Visos mažmeninės prekybos parduotuvės.
2. Sąraše spustelėkite „Houston“ saitą Mažmeninės prekybos kanalo ID.
3. Spustelėkite Redaguoti.
    * Lauke PVM grupė pateikiamas dabartinės įmonės PVM grupių sąrašas. Šiuo metu priskirta grupė yra bendroji PVM grupė „Texas“. Taip pat galimos PVM grupės „Washington“ ir „Washington, King County“. PVM grupės gali apimti keliose savivaldybėse taikomus mokesčius.  
    * Lauke PVM perrašymas PVM perrašymo grupes galima susieti su kanalu. PVM perrašymo grupes galima naudoti norint grupuoti PVM perrašymus, taikomus kelioms parduotuvėms. Užuot neautomatiniu būdu priskyrus atskirus PVM perrašymus, galima sutaupyti laiko sukuriant grupę ir ją tiesiogiai priskiriant kanalams.  
4. Spustelėkite Įrašyti.
5. Uždarykite puslapį.
6. Pasirinkite Mažmeninė prekyba ir prekyba > Kanalo sąranka > PVM > PVM perrašymai.
7. Spustelėkite Naujas.
8. Lauke PVM perrašymas nurodykite naujo perrašymo pavadinimą.
9. Lauke Aprašas nurodykite perrašymo aprašą.
10. Nustatykite būseną į Įjungta.
11. Išplėskite arba sutraukite sekciją Perrašymas.
12. Lauke „Tipas“ pasirinkite parinktį.
    * Prekės PVM grupes galima naudoti norint perrašyti konkrečių grupei priklausančių prekių mokesčius. Pvz., maisto prekės paprastai apmokestinamos kitaip nei fizinės medžiagos ir tikėtina, kad jos priklauso atskirai PVM grupei.     PVM grupės yra mokesčių, kurie taikomi konkrečiam kanalui, grupės. Pvz., jei kanale vykdoma tiek mažmeninė, „verslo verslui“ prekyba, gali būti naudojamos skirtingos prekių PVM grupės. Visi taikomi mokesčiai būtų susieti su PVM grupe.  
    * Dabar gali būti pasirinkti mokesčiai Iš ir Į arba Iš mokesčių grupės ir Į mokesčių grupę, kad būtų sukurtas PVM perrašymas.    Lauke Iš nurodomi mokesčiai arba mokesčių grupė, kurią reikia perrašyti. Perrašant pagal prekės PVM grupę galima naudoti kitas parinktis nei perrašant pagal PVM grupę.    Galima nustatyti, kad PVM perrašymai perrašytų visų operacijų mokesčius arba konkrečių operacijos eilučių mokesčius.  
13. Spustelėkite Įrašyti.
14. Uždarykite puslapį.
15. Pasirinkite Mažmeninė prekyba ir prekyba > Kanalo sąranka > PVM > PVM perrašymų grupės.
    * Atlikdami šį veiksmą jūs priskirsite naujai sukurtą PVM perrašymą PVM perrašymo grupei, priskirtai kanalui „Houston“.  
16. Spustelėkite Redaguoti.
17. Išplėskite arba sutraukite sekciją Sąranka.
18. Spustelėkite Pridėti.
19. Lauke PVM perrašymas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
20. Sąraše pasirinkite anksčiau sukurtą PVM perrašymą.
21. Sąraše spustelėkite saitą pasirinktoje eilutėje.
22. Spustelėkite Įrašyti.


