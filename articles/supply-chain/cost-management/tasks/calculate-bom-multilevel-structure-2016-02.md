---
title: Apskaičiuoti KS naudojant kelių lygių struktūrą (2016 m. vasario mėn.)
description: Šioje procedūroje nurodoma, kaip apskaičiuoti galutinio produkto savikainą naudojant kelių lygių išskleidimą, paremtą įkainojimo lapu.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 859f7b7c828dcdad1aa836044d2cc26847630f1e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821422"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a>Apskaičiuoti KS naudojant kelių lygių struktūrą (2016 m. vasario mėn.)

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]