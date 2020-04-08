---
title: Tikrinti turimas atsargas
description: Ši procedūra parodo, kaip patikrinti konkretaus prekės numerio turimas ir faktinies turimas atsargas.
author: ShylaThompson
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a6ced839f93103a62bcfa8ea14ca463f0f1e174e
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145852"
---
# <a name="check-the-availability-of-stock"></a>Tikrinti turimas atsargas

[!include [banner](../../includes/banner.md)]

Ši procedūra parodo, kaip patikrinti konkretaus prekės numerio turimas ir faktinies turimas atsargas. Ji taip pat parodo, kaip gauti tiekimo informacijos, susijusios su preke. Faktinės turimos atsargos yra turimos atsargos, kurios yra prieinamos – t. y., nupirktos, gautos ir užregistruotos. Turimos atsargos apima ne tik prieinamas turimas atsargas, bet ir atsargas, kurios užsakytos ir laukiamos, bet dar nėra gautos ar registruotos. Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis. Jei naudojate USMF, galite naudoti rodomas pavyzdines reikšmes. Šias užduotis paprastai turėtų atlikti sandėlio darbuotojas.


## <a name="check-on-hand-inventory-for-an-item"></a>Patikrinti turimas prekės atsargas
1. Eikite į **Naršymo sritis > Moduliai > Atsargų valdymas > Užklausos ir ataskaitos > Turimos atsargos**.
2. Pasirinkti eilutę **Prekių skaičius**. Norėdami teikti užklausą dėl turimų atsargų pagal prekės numerį, pasirinkite eilutę, kurioje lentelė nustatyta į **Turimos atsargos**, o laukas nustatytas į **Prekės** numeris.
3. Lauke **Kriterijai** pasirinkite prekę, dėl kurios norite pateikti užklausą. Jei naudojate demonstracinių duomenų įmonę USMF, galite pasirinkti „M9201‟.  
4. Spustelėkite **Gerai**.
5. **Veiksmų srityje** spustelėkite **Dimensijos**. Skirtukas **Dimensijos** leidžia pasirinkti, kiek informacijos apie turimas atsargas norite matyti. Jei reikia duomenų, susijusių su rezervavimu, turite vaizduoti visas prekių, naudojančių patobulintus sandėlio (WHS) procesus, atsargų dimensijas.
6. Spustelėkite **Gerai**.
7. **Veiksmų srityje** spustelėkite **Susijusi informacija**. Jei tokios parinkties nematote, gali reikėti spustelėti ant elipsės mygtuko (...), kad matytumėte papildomų veiksmų srities parinkčių.
8. Spustelėkite **Tiekimo apžvalga**. Skirtuke **Tiekimo apžvalga** pateikiama konkrečios prekės tiekimo informacija, pvz., turimas kiekis, gamybos laikas ir tiekėjo informacija.  
9. Išplėskite sekciją **Turimas kiekis**.
10. Išplėskite skyrių **Tiekėjai**.
11. Uždarykite puslapį.
12. Uždarykite puslapį.

## <a name="check-physical-on-hand-inventory"></a>Tikrinti faktines turimas atsargas
1. Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Užklausos ir ataskaitos > Faktinės turimos atsargos**.
2. Lauke **Prekės numeris** įveskite vertę. Galite naudoti laukus Teritorija ir Sandėlis, kad filtruotumėte prekių sąrašą. 
3. Atnaujinkite puslapį.
4. **Veiksmų srityje** spustelėkite **Rodyti dimensijas**. Skirtukas Dimensijų rodymas leidžia pasirinkti, kiek informacijos apie turimas atsargas norite matyti.
5. Spustelėkite **Gerai**.
6. Uždarykite puslapį.

## <a name="check-on-hand-inventory-by-location"></a>Tikrinti turimas atsargas pagal vietą
1. Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Užklausos ir ataskaitos > Turimos atsargos pagal vietą**.
2. Lauke **Sandėlis** įveskite reikšmę. Jei naudojate demonstracinių duomenų įmonę USMF, galite naudoti „51‟.  
3. Atnaujinkite puslapį.
4. Spustelėkite **Rodyti dimensijas**.
5. Spustelėkite **Gerai**.
6. Uždarykite puslapį.

