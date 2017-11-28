---
title: "Išlaidų kategorijos, naudojamos gamybos kelvadose"
description: "Šiame straipsnyje pateikiama informacija apie išlaidų kategorijas, taikoma gamybos aplinkoms, naudojančioms kelvadas."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjCategory, RouteCostCategoryPrice
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 78153
ms.assetid: a3fdc76c-0a27-4723-b1c7-4322f707d89e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 53e038183a10b8732a9a5e0f25aac440c224400e
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="cost-categories-used-in-production-routing"></a>Išlaidų kategorijos, naudojamos gamybos kelvadose

[!include[banner](../includes/banner.md)]


Šiame straipsnyje pateikiama informacija apie išlaidų kategorijas, taikoma gamybos aplinkoms, naudojančioms kelvadas.

Išlaidų kategorijos taikomos gamybos aplinkai, kuri naudoja kelvadas. Jos priskiriamos operacijų ištekliams ir kelvadų operacijoms, kad būtų galima nustatyti valandines išlaidas ir segmentuoti išlaidų įnašus pagamintos prekės apskaičiuotose išlaidose. Išlaidų grupės, kurios priskirtos prie išlaidų kategorijų, klasifikuoja pagaminimo išlaidų įnašus pagal operacijų išteklius ir veiklos tipą, pvz., nustatymo laiką ir apdorojimo laiką. Išlaidų grupės priskyrimų specifiškumas leidžia remiantis kelvados informacija apskaičiuoti pagaminimo papildomus duomenis. 

**Pastaba.** Gaminimo aplinkose išlaidų kategorijos vadinamos keliais kitais pavadinimais, pvz., darbo tarifo kodai arba įrenginio tarifo kodai. 

Kiekviena išlaidų kategorija turi su ja susijusius išlaidų įrašus ir priskirtą išlaidų grupę. Skirtingos išlaidų kategorijos reikalingos, kad būtų galima palaikyti skirtingus gamybos tikslus.

-   Atsižvelgiant į operacijų išteklių priskirti skirtingas valandines išlaidas. Pavyzdžiui, gali skirtis įvairių tipų darbo įgūdžių, įrenginių arba gamybos langelių tipų išlaidos.
-   Priskirti skirtingas valandines išlaidas, skirtas nustatymo arba apdorojimo laikui, kuris susietas su kelvados operacija.
-   Priskirti operacijų išteklių išlaidas remiantis išeigos kiekiu, o ne valandinėmis išlaidomis, pvz., dalių tarifais, skirtas mokėti už darbą.
-   Pateikti išlaidų įnašų grupių segmentavimą pagal pagamintos prekės apskaičiuotas išlaidas. Pavyzdžiui, galite segmentuoti darbo ir įrenginių išlaidas.
-   Pateikti išlaidų grupės pagrindą papildomų išlaidų apskaičiavimo formulėms, pvz., su darbu ir įrenginiais arba su nustatymu ir apdorojimo laiku susijusių papildomų išlaidų formulėms.

Išlaidų kategorija gali būti priskirta nustatymo, proceso laikui ir kelvados operacijos kiekiui. Kai, pavyzdžiui, išlaidų ar išlaidų grupės segmentacija skiriasi nuo nustatymo laiko ir proceso laiko, skirtingos išlaidų kategorijos turi būti nurodytos ir priskirtos nustatymo laikui bei proceso laikui. Pasirinktinis išlaidų kategorijų naudojimas, skirtas nustatymo laikui, proceso laikui ir kiekiui, nustatomas maršruto grupės, kuri priskiriama operacijai. Išlaidų kategorijų priskyrimas laikui ir kiekiui gali būti paremtas visos įmonės strategijomis, kurios apibrėžiamos puslapyje **Gamybos valdymo parametrai**. 

Kiekviena išlaidų kategorija turi su ja susietas išlaidas, kurios paremtos išlaidų įrašų aprašu įkainojimo versijoje. Norėdami apibrėžti nurodytos įkainojimo versijos ir vietos išlaidų įrašus, naudokite puslapį **Išlaidų kategorijos kaina**. Kai pirmiausia įvedamas išlaidų kategorijos išlaidų įrašas, jo būsena yra **Laukiama** bei nurodoma numatyta įsigaliojimo data. Kai išlaidų įrašą suaktyvinate, būsena atnaujinama į **Dabartinis aktyvus**, o įsigaliojimo data atnaujinama į aktyvavimo datą. Skirtingi išlaidų įrašai gali atspindėti skirtingas vietas, įsigaliojimo datas ar būsenas. Komplektavimo specifikacijų (KS) skaičiavimai ateičiai ar retrospektyvinei datai naudoja išlaidų įrašus su aktualia įsigaliojimo data. Šiuo metu aktyvių išlaidų įrašas bus naudojamas įvertinti gamybos užsakymų išlaidas ir vertinti paskirtą laiką pagal gamybos užsakymą. 

Išlaidų kategorijos išlaidų įrašas gali būti konkrečios vietos ar visos įmonės. Norėdami išlaidų įrašą nustatyti konkrečiai vietai, jam priskirkite vietą. Kitaip tuščia reikšmė nurodo, kad išlaidų įrašas taikomas visoms įmonės vietoms. Kadangi išlaidos gali skirtis (pvz., vietose), išlaidų įrašai turi būti nurodyti pagal vietą. 

Kelvados operacija paprastai paveldėja išlaidų kategorijas, kurios priskirtos operacijų ištekliui arba pagrindinei operacijai. Kai sukuriamas gamybos užsakymas, kelvados operacijos gamybos maršruto ribose rodo pasirinktą maršruto versiją. Galite nepaisyti išlaidų kategorijų, priskirtų operacijoms, esančioms gamybos maršruto ribose. 

Kai kurių tipų gamybos darbą galima taikyti projekto laiko įvertinimui ir ataskaitoms. Šiuo atveju gamybos ir projekto tikslais reikalinga išlaidų kategorija. Kai išlaidų kategorija pažymima naudoti projektuose, turite apibrėžti papildomą su projektais susijusią informaciją.




