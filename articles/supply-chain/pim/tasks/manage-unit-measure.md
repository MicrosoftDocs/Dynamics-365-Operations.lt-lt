---
title: Tvarkyti matavimo vienetą
description: Ši procedūra nurodo, kaip apibrėžti matavimo vienetą, pateikti vieneto vertimus ir jo aprašą ir apibrėžti susijusių vienetų konvertavimo taisykles.
author: sorenva
manager: AnnBe
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 042a7495d55fb9d884771972cfc18e5ddb25330d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844326"
---
# <a name="manage-unit-of-measure"></a>Tvarkyti matavimo vienetą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra nurodo, kaip apibrėžti matavimo vienetą, pateikti vieneto vertimus ir jo aprašą ir apibrėžti susijusių vienetų konvertavimo taisykles. Šią procedūrą galite žingsnis po žingsnio atlikti naudodami demonstracinius duomenis arba savo pačių duomenis.

1. Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Patvirtinto produkto priežiūra**.
2. Spustelėkite **Vienetai**.

## <a name="create-a-unit-of-measure"></a>Kurti matavimo vienetą
1. Spustelėkite **Naujas**.
2. Lauke **Unit** įveskite reikšmę. Įveskite ID arba simbolį, naudojamą nurodant matavimo vienetą.  
3. Lauke **Description field**surinkite reikšmę. Įveskite matavimo vieneto aprašomąjį pavadinimą sistemos kalba.  
4. Lauke **Vieneto klasė** pasirinkite parinktį. Vieneto klasė apibrėžia, kokiai loginei grupei, pvz., plotui, masei ar kiekiui, priklauso matavimo vienetas.  
5. Lauke **Dešimtainis tikslumas** įveskite skaičių. Nurodykite dešimtainių dalių skaičių, iki kurio turi būti apvalinamas konvertuojamas matavimo vienetas atlikus skaičiavimą su šiuo matavimo vienetu.  
6. Spustelėkite **Įrašyti**.

## <a name="define-unit-translations"></a>Apibrėžti vieneto vertimus
1. **Action pane** spustelėkite **Unit texts**.
2. Spustelėkite **Naujas**. Naudodami vieneto tekstą sukurkite matavimo vienetą reprezentuojančio ID arba simbolio vertimą, kuris bus naudojamas išoriniuose dokumentuose konkretaus kliento arba tiekėjo kalbomis.  
3. Lauke **Kalba** įveskite arba pasirinkite reikšmę.
4. Lauke **Tekstas** įveskite reikšmę.
5. Spustelėkite **Įrašyti**.
6. Uždarykite puslapį.
7. **Action pane** spustelėkite **Translated unit descriptions**.
8. Spustelėkite **Naujas**. Nurodykite matavimo vieneto aprašus konkrečia kalba.  
9. Lauke **Kalba** įveskite arba pasirinkite reikšmę.
10. Lauke **Description field**surinkite reikšmę.
11. Spustelėkite **Įrašyti**.
12. Uždarykite puslapį.

## <a name="define-unit-conversion-rules"></a>Apibrėžti vieneto konvertavimo taisykles
1. **Action pane** spustelėkite **Unit conversions**. Apibrėžkite matavimo vieneto konvertavimo į ir iš kitų matavimo vienetų pasirinktoje vieneto klasėje taisykles.  
2. Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą.
3. Lauke **Koeficientas** įveskite skaičių. Konvertavimo iš vienetų į vienetus koeficientas. Pvz., konvertavimo iš centimetrus į metrus koeficientas yra 100, nes vienas metras turi 100 centimetrų.  
4. Lauke **Į vnt.** įveskite arba pasirinkite reikšmę.
5. Lauke **Apvalinimas** pasirinkite parinktį. Apibrėžkite, kaip turi būti apvalinama konvertuota reikšmė.  
6. Spustelėkite **Gerai**.
7. Uždarykite puslapį.

