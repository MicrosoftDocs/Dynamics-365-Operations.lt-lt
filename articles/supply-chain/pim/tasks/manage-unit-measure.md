---
title: Tvarkyti matavimo vienetą
description: Ši procedūra nurodo, kaip apibrėžti matavimo vienetą, pateikti vieneto vertimus ir jo aprašą ir apibrėžti susijusių vienetų konvertavimo taisykles.
author: sorenva
manager: tfehr
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8d9b6f18fdc1c47d6a695ca6a2330f6f02fc1bd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433449"
---
# <a name="manage-unit-of-measure"></a>Tvarkyti matavimo vienetą

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip apibrėžti matavimo vienetą, pateikti vieneto vertimus ir jo aprašą ir apibrėžti susijusių vienetų konvertavimo taisykles. Šią procedūrą galite žingsnis po žingsnio atlikti naudodami demonstracinius duomenis arba savo pačių duomenis.

1. Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Patvirtinto produkto priežiūra**.
2. Spustelėkite **Vienetai**.

## <a name="create-a-unit-of-measure"></a>Kurti matavimo vienetą
1. Spustelėkite **Naujas**.
2. Lauke **Vienetas** įveskite reikšmę. Įveskite ID arba simbolį, naudojamą nurodant matavimo vienetą.  
3. Lauke **Aprašymas įveskite** surinkite reikšmę. Įveskite matavimo vieneto aprašomąjį pavadinimą sistemos kalba.  
4. Lauke **Vieneto klasė** pasirinkite parinktį. Vieneto klasė apibrėžia, kokiai loginei grupei, pvz., plotui, masei ar kiekiui, priklauso matavimo vienetas.  
5. Lauke **Dešimtainis tikslumas** įveskite skaičių. Nurodykite dešimtainių dalių skaičių, iki kurio turi būti apvalinamas konvertuojamas matavimo vienetas atlikus skaičiavimą su šiuo matavimo vienetu.  
6. Spustelėkite **Įrašyti**.

## <a name="define-unit-translations"></a>Apibrėžti vieneto vertimus
1. **Veiksmų srityje** spustelėkite **Vieneto tekstai**.
2. Spustelėkite **Naujas**. Naudodami vieneto tekstą sukurkite matavimo vienetą reprezentuojančio ID arba simbolio vertimą, kuris bus naudojamas išoriniuose dokumentuose konkretaus kliento arba tiekėjo kalbomis.  
3. Lauke **Kalba** įveskite arba pasirinkite reikšmę.
4. Lauke **Tekstas** įveskite reikšmę.
5. Spustelėkite **Įrašyti**.
6. Uždarykite puslapį.
7. **Veiksmų srityje** spustelėkite **Išversti vienetų aprašai**.
8. Spustelėkite **Naujas**. Nurodykite matavimo vieneto aprašus konkrečia kalba.  
9. Lauke **Kalba** įveskite arba pasirinkite reikšmę.
10. Lauke **Aprašymas įveskite** surinkite reikšmę.
11. Spustelėkite **Įrašyti**.
12. Uždarykite puslapį.

## <a name="define-unit-conversion-rules"></a>Apibrėžti vieneto konvertavimo taisykles
1. **Veiksmų srityje** spustelėkite **Vienetų konvertavimas**. Apibrėžkite matavimo vieneto konvertavimo į ir iš kitų matavimo vienetų pasirinktoje vieneto klasėje taisykles.  
2. Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą.
3. Lauke **Koeficientas** įveskite skaičių. Konvertavimo iš vienetų į vienetus koeficientas. Pvz., konvertavimo iš centimetrus į metrus koeficientas yra 100, nes vienas metras turi 100 centimetrų.  
4. Lauke **Į vnt.** įveskite arba pasirinkite reikšmę.
5. Lauke **Apvalinimas** pasirinkite parinktį. Apibrėžkite, kaip turi būti apvalinama konvertuota reikšmė.  
6. Spustelėkite **Gerai**.
7. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]