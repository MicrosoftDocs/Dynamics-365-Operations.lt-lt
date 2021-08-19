---
title: Fiksuoto kiekio „kanban“ gamybos taisyklės kūrimas
description: Šia procedūra sutelkiamas dėmesys į nustatymą, reikalingą norint „lean“ aplinkos darbo elemente sukurti fiksuotą gamybos „kanban“ taisyklę, skirtą transformavimo veiklos aktyvinimui.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a2edce5ac4506dead8d150e9f332e00817f35ce7a16910d30b9c77203518b07
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775560"
---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a>Fiksuoto kiekio „kanban“ gamybos taisyklės kūrimas

[!include [banner](../../includes/banner.md)]

Šia procedūra sutelkiamas dėmesys į nustatymą, reikalingą norint „lean“ aplinkos darbo elemente sukurti fiksuotą gamybos „kanban“ taisyklę, skirtą transformavimo veiklos aktyvinimui. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Ši procedūra skirta proceso inžinieriui arba vertės srauto vadybininkui, nes jie parengia naujos arba pakeistos prekės gamybą.


## <a name="create-new-kanban-rule"></a>Naujos „kanban“ taisyklės kūrimas
1. Eikite į „Kanban“ taisyklės.
2. Spustelėkite Naujas.
    * Atkreipkite dėmesį, kad numatytasis tipas Gamybos ir papildymo strategija yra Fiksuotas. Jums nereikia keisti šių parametrų.  
3. Lauke Pirmoji plano veikla įveskite arba pasirinkite reikšmę.
    * Tai veikla, kuri bus atliekama naudojant „kanbans“, sukurtus remiantis šia „kanban“ taisykle.  Pasirinkite „SpeakerTestAndPackaging“.  
4. Išplėskite skyrių Išsami informacija.
5. Lauke Produktas įveskite arba pasirinkite reikšmę.
    * Pažymėkite L0050.  
6. Lauke Matavimo vienetas įveskite arba pasirinkite reikšmę.
    * Pasirinkite minutes.  
7. Lauke Gamybos laikas įveskite skaičių.
    * Įveskite 5.  

## <a name="set-quantities"></a>Kiekių nustatymas
1. Išplėskite skyrių Kiekiai.
2. Nustatykite pasirinkties Numatytasis kiekis reikšmę „10“.
    * Tai kiekis, kuris bus perduotas kiekvienam „kanban“.  
3. Pažymėkite žymės langelį Produkto kiekio nuokrypis.
    * Tokiu būdu pasirinktus „kanbans“ galima užbaigti su nuokrypiu nuo numatytojo kiekio.  Norėdami užbaigti „kanbans“, kai jų kiekio reikšmė nuo 8 iki 12, nustatykite abiejų nuokrypių reikšmes 2.  
4. Nustatykite pasirinkties Nuokrypis mažesnis negu reikšmę „2“.
    * Tai leis užbaigti mažėjant iki 10 - 2 = 8  
5. Nustatykite pasirinkties Nuokrypis didesnis negu reikšmę „2“.
    * Tai leis užbaigti didėjant iki 10 + 2 = 12  
6. Lauke Fiksuotas „kanban“ kiekis įveskite skaičių.
    * Tai yra „kanbans“, kurie turi būti aktyvūs, suma. Šiuo atveju 5 „kanbans“, iš kurių kiekvienas apdoroja 10.  
7. Lauke Žemiausia įspėjimo riba įveskite „2“.
    * Naudojama norint sekti minimalią visų paskirties vietoje turinčių būti „kanbans“ sumą. Pavyzdžiui, tai naudojama „kanban“ kiekio apžvalgoje.  
8. Lauke Aukščiausia įspėjimo riba įveskite „4“.
    * Naudojama norint sekti maksimalią visų paskirties vietoje turinčių būti „kanbans“ sumą. Pavyzdžiui, tai naudojama „kanban“ kiekio apžvalgoje.  
9. Lauke Automatinio planavimo kiekis įveskite „1“.
    * Nustačius 1 reiškia, kad kiekvienas „kanban“ bus suplanuotas automatiškai.   Jei įvedėme 3, „kanbans“ nebus planuojami, kol planavimui nebus paruošti 3 tušti „kanbans“. Tai naudinga grupuojant darbą ir norint išvengti per daug nustatymų.  

## <a name="create-kanbans"></a>„Kanbans“ kūrimas
1. Išplėskite skyrių „Kanbans“.
2. Spustelėkite Įrašyti.
    * Tam, kad būtų galima kurti „kanbans“, turi būti įrašyta „kanban“ taisyklė.  
3. Spustelėkite Pridėti.
    * Atkreipkite dėmesį, kad nėra jokių aktyvių „kanbans“, todėl siūlomas „Naujų „kanbans“ skaičius“ yra 5. Jis lygus „fiksuotam „kanban“ kiekiui“.  
4. Spustelėkite Kurti.
    * Taip sukursite 5 „kanbans“.  
    * Atkreipkite dėmesį, kad 5 „kanbans“, kiekvienas po 10, buvo sukurti šiai gamybos „kanban“ taisyklei. Tai yra paskutinis šios procedūros veiksmas.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]