---
title: PVM priskyrimas ir perrašymai
description: Ši procedūra parodo, kaip prekybos kanalams galima priskirti PVM grupes.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 74a7eed04648c63c0b19d5de26d2bdbef59aec7d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207604"
---
# <a name="sales-tax-assignment-and-overrides"></a> PVM priskyrimas ir perrašymai​

[!include [banner](../../includes/banner.md)]

Ši procedūra parodo, kaip prekybos kanalams galima priskirti PVM grupes. Joje taip pat paaiškinamas procesas, kurio metu sukuriamas naujas PVM perrašymas ir priskiriamas esamai PVM perrašymo grupei. Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.

1. Eikite į „Retail and Commerce“ > Kanalai > Parduotuvės > Visos parduotuvės.
2. Sąraše spustelėkite „Houston“ nuorodą „Kanalo ID“.
3. Spustelėkite Redaguoti.
    * Lauke PVM grupė pateikiamas dabartinės įmonės PVM grupių sąrašas. Šiuo metu priskirta grupė yra bendroji PVM grupė „Texas“. Taip pat galimos PVM grupės „Washington“ ir „Washington, King County“. PVM grupės gali apimti keliose savivaldybėse taikomus mokesčius.  
    * Lauke PVM perrašymas PVM perrašymo grupes galima susieti su kanalu. PVM perrašymo grupes galima naudoti norint grupuoti PVM perrašymus, taikomus kelioms parduotuvėms. Užuot neautomatiniu būdu priskyrus atskirus PVM perrašymus, galima sutaupyti laiko sukuriant grupę ir ją tiesiogiai priskiriant kanalams.  
4. Spustelėkite Įrašyti.
5. Uždarykite puslapį.
6. Eikite į „Retail and Commerce“ > Kanalo sąranka > PVM > PVM perrašymai.
7. Spustelėkite Naujas.
8. Lauke PVM perrašymas nurodykite naujo perrašymo pavadinimą.
9. Lauke Aprašas nurodykite perrašymo aprašą.
10. Nustatykite būseną į Įjungta.
11. Išplėskite arba sutraukite sekciją Perrašymas.
12. Lauke „Tipas“ pasirinkite parinktį.
    * Prekės PVM grupes galima naudoti norint perrašyti konkrečių grupei priklausančių prekių mokesčius. Pvz., maisto prekės paprastai apmokestinamos kitaip nei fizinės medžiagos ir tikėtina, kad jos priklauso atskirai PVM grupei. PVM grupės yra mokesčių, kurie taikomi konkrečiam kanalui, grupės. Pvz., jei kanale vykdoma tiek mažmeninė, „verslo verslui“ prekyba, gali būti naudojamos skirtingos prekių PVM grupės. Visi taikomi mokesčiai būtų susieti su PVM grupe.  
    * Dabar gali būti pasirinkti mokesčiai Iš ir Į arba Iš mokesčių grupės ir Į mokesčių grupę, kad būtų sukurtas PVM perrašymas. Lauke Iš nurodomi mokesčiai arba mokesčių grupė, kurią reikia perrašyti. Perrašant pagal prekės PVM grupę galima naudoti kitas parinktis nei perrašant pagal PVM grupę. Galima nustatyti, kad PVM perrašymai perrašytų visų operacijų mokesčius arba konkrečių operacijos eilučių mokesčius.  
13. Spustelėkite Įrašyti.
14. Uždarykite puslapį.
15. Eikite į „Retail and Commerce“ > Kanalo sąranka > PVM > PVM perrašymo grupės.
    * Atlikdami šį veiksmą jūs priskirsite naujai sukurtą PVM perrašymą PVM perrašymo grupei, priskirtai kanalui „Houston“.  
16. Spustelėkite Redaguoti.
17. Išplėskite arba sutraukite sekciją Sąranka.
18. Spustelėkite Pridėti.
19. Lauke PVM perrašymas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
20. Sąraše pasirinkite anksčiau sukurtą PVM perrašymą.
21. Sąraše spustelėkite saitą pasirinktoje eilutėje.
22. Spustelėkite Įrašyti.

