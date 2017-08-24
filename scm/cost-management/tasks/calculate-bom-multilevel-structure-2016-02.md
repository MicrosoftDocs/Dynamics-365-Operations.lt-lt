--- 
title: "Apskaičiuoti KS naudojant kelių lygių struktūrą (tik 2016 m. vasario mėn.)"
description: "Šioje procedūroje nurodoma, kaip apskaičiuoti galutinio produkto savikainą naudojant kelių lygių išskleidimą, paremtą įkainojimo lapu."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 1ad38f67bba299bbd581aba6010b4028c91fbf3a
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016-only"></a>Apskaičiuoti KS naudojant kelių lygių struktūrą (tik 2016 m. vasario mėn.)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje nurodoma, kaip apskaičiuoti galutinio produkto savikainą naudojant kelių lygių išskleidimą, paremtą įkainojimo lapu. Tai septintoji KS skaičiavimo sekų užduotis. Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.

1. Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.
2. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkite produktą BOM_1.  
3. Veiksmų srityje spustelėkite Valdyti išlaidas.
4. Spustelėkite Prekės kaina.
5. Spustelėkite Skaičiuoti prekės savikainą.
    * Gali reikėti spustelėti elipsės mygtuką (...), kad šią parinktį matytumėte viršutiniame meniu.  
6. Lauke Įkainojimo versija įveskite arba pasirinkite reikšmę.
    * Pasirinkite įkainojimo versijos reikšmę 20, nes jos suplanuotų išlaidų tipas ir išskleidimo režimas yra kelių lygių.   Kelių lygių išskleidimo režimas skirtas suplanuotoms išlaidoms ir modeliavimui. Jis nenaudojamas standartinei savikainai.  
7. Spustelėkite GERAI.
8. Spustelėkite Peržiūrėti skaičiavimo informaciją.
    * Gali reikėti spustelėti elipsės mygtuką (...), kad šią parinktį matytumėte viršutiniame meniu.  Šiuo atveju atkreipkite dėmesį, kaip apskaičiuota BOM_2 atsižvelgiant į žaliavas, procesą ir pridėtines išlaidas (iš viso – 29,40) vietoj standartinės savikainos – 10, suaktyvintos pradiniame šios serijos užduočių vadove.  
9. Spustelėkite skirtuką Įkainojimo lapas.
    * Perėjus į skirtuką Įkainojimo lapas, išlaidų grupės bendrosios sumos skiriasi lyginant su ankstesniame užduočių vadove atliktu skaičiavimu.  
10. Lauke „Lygis” pasirinkite „Keli”.
    * Pasirinkus Keli, išlaidos klasifikuojamos pagal BOM_2 sudėtį, kur 10 išvedamas iš M1 išlaidų grupės (ITEM_C), o 15,60 išvedama iš jos gamybos, kur išlaidų grupė yra L2. Netiesioginės išlaidos taip pat skiriasi.  
11. Uždarykite puslapį.
12. Uždarykite puslapį.


