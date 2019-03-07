---
title: Tikrinti turimas atsargas
description: Ši procedūra parodo, kaip patikrinti konkretaus prekės numerio turimas ir faktinies turimas atsargas.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26a8f51eda1f4249862a23fa0103b7a144d974a1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "337997"
---
# <a name="check-the-availability-of-stock"></a>Tikrinti turimas atsargas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra parodo, kaip patikrinti konkretaus prekės numerio turimas ir faktinies turimas atsargas. Ji taip pat parodo, kaip gauti tiekimo informacijos, susijusios su preke. Faktinės turimos atsargos yra turimos atsargos, kuros yra prieinamos – t. y., nupirktos, gautos ir užregistruotos. Turimos atsargos apima ne tik prieinamas turimas atsargas, bet ir atsargas, kurios užsakytos ir laukiamos, bet dar nėra gautos ar registruotos. Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis. Jei naudojate USMF, galite naudoti rodomas pavyzdines reikšmes. Šias užduotis paprastai turėtų atlikti sandėlio darbuotojas.


## <a name="check-on-hand-inventory-for-an-item"></a>Patikrinti turimas prekės atsargas
1. Pasirinktie Atsargų valdymas > Užklausos ir ataskaitos > Turimos atsargos.
2. Pasirinkite eilutę Prekės numeris.
    * Norėdami teikti užklausą dėl turimų atsargų pagal prekės numerį, pasirinkite eilutę, kurioje lentelė nustatyta į Turimos atsargos, o laukas nustatytas į Prekės numeris.  
3. Lauke Kriterijai pasirinkite prekę, dėl kurios norite pateikti užklausą.
    * Jei naudojate demonstracinių duomenų įmonę USMF, galite pasirinkti „M9201‟.  
4. Spustelėkite GERAI.
5. Spustelėkite Dimensijos.
    * Skirtukas Dimensijos leidžia pasirinkti, kiek informacijos apie turimas atsargas norite matyti. Jei reikia duomenų, susijusių su rezervavimu, turite vaizduoti visas prekių, naudojančių patobulintus sandėlio (WHS) procesus, atsargų dimensijas.  
6. Spustelėkite GERAI.
7. Veiksmų srityje spustelėkite Susijusi informacija.
    * Jei to nematote, gali reikėti spustelėti ant elipsės mygtuko (...), kad matytumėte papildomų veiksmų srities parinkčių.  
8. Spustelėkite Tiekimo apžvalga.
    * Skirtuke Tiekimo apžvalga pateikiama konkrečios prekės tiekimo informacija, pvz., turimas kiekis, gamybos laikas ir tiekėjo informacija.  
9. Išplėskite sekciją Turimas kiekis.
10. Išplėskite sekciją Tiekėjai.
11. Uždarykite puslapį.
12. Uždarykite puslapį.

## <a name="check-physical-on-hand-inventory"></a>Tikrinti faktines turimas atsargas
1. Pasirinkite Sandėlio valdymas > Užklausos ir ataskaitos > Faktinės turimos atsargos.
2. Lauke Prekės numeris surinkite reikšmę.
    * Galite naudoti laukus Teritorija ir Sandėlis, kad filtruotumėte prekių sąrašą.  
3. Atnaujinkite puslapį.
4. Spustelėkite Rodyti dimensijas.
    * Skirtukas Dimensijų rodymas leidžia pasirinkti, kiek informacijos apie turimas atsargas norite matyti.  
5. Spustelėkite GERAI.
6. Uždarykite puslapį.

## <a name="check-on-hand-inventory-by-location"></a>Tikrinti turimas atsargas pagal vietą
1. Pasirinkite Sandėlio valdymas > Užklausos ir ataskaitos > Turimos atsargos pagal vietą.
2. Lauke Sandėlis surinkite reikšmę.
    * Jei naudojate demonstracinių duomenų įmonę USMF, galite naudoti „51‟.  
3. Atnaujinkite puslapį.
4. Spustelėkite Rodyti dimensijas.
5. Spustelėkite GERAI.
6. Uždarykite puslapį.

