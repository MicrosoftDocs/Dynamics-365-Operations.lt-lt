---
title: Išplėstinių taisyklių struktūrų kūrimas ir priskyrimas
description: Šioje temoje aiškinama, kaip sukurti ir priskirti išplėstinės taisyklės struktūrą prie sąskaitos struktūros.
author: aprilolson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b81e3cc169bf0164af0b9c4de4faeb936df6784
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837062"
---
# <a name="create-and-assign-advanced-rule-structures"></a>Išplėstinių taisyklių struktūrų kūrimas ir priskyrimas

[!include [banner](../../includes/banner.md)]

Šioje temoje aiškinama, kaip sukurti ir priskirti išplėstinės taisyklės struktūrą prie sąskaitos struktūros. Šiame vadove naudojama demonstracinė įmonė USMF.

## <a name="create-an-advanced-rule-structure"></a>Kurti išplėstinės taisyklės struktūrą
1. Eikite į **Naršymo sritis > Moduliai > Didžioji knyga > Sąskaitų planas > Struktūros > Išplėstinės taisyklės struktūros**.
2. Pasirinkite **Naujas**, kad atidarytumėte išplečiamąjį dialogo langą.
3. Lauke **Išplėstinės taisyklės struktūra** įveskite pavadinimą, aprašantį taisyklės struktūrą.
4. Pasirinkite **Gerai**.
5. Pasirinkite **Pridėti segmentą**.
6. Segmentų sąraše pasirinkite finansinę dimensiją. Pavyzdžiui, **Parduotuvė**.  
7. Pasirinkite **Pridėti segmentą**.
8. Pasirinkite **Aktyvinti**.

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a>Išplėstinės taisyklės struktūros taikymas sąskaitos struktūrai
1. Eikite į **Naršymo sritis > Moduliai > Didžioji knyga > Sąskaitų planas > Struktūros > Sukonfigūruoti sąskaitų struktūras**.
2. Sąraše raskite ir pasirinkite sąskaitos struktūrą, kuriai norite taikyti išplėstinę taisyklę.
3. Pasirinkite **Redaguoti**. Taip pat galite spustelėti **Išplėstinės taisyklės** ir jūs būsite paraginti pateikti sąskaitos struktūrą **juodraščio režimu**.  
4. Pasirinkite **Išankstinis**.
5. Pasirinkite **Naujas**, kad atidarytumėte išplečiamąjį dialogo langą.
6. Lauke **Išplėstinė taisyklė** įveskite reikšmę.
7. Lauke **Pavadinimas** įveskite reikšmę.
8. Pasirinkite **Kurti**.
9. Spustelėkite **Įtraukti naujų kriterijų**.
10. Lauke **Kur** pasirinkite pagrindinę sąskaitą arba finansinę dimensiją.
11. Lauke **Operatorius**, pasirinkite parinktį, pvz., **yra tarp** ir **apima**.
12. Lauke **Reikšmė** įveskite reikšmę.
13. Lauke **per** įveskite reikšmę.
14. Pasirinkite **Įtraukti** ir atidarykite išplečiamąjį dialogo langą.
15. Sąraše raskite išplėstinės taisyklės struktūrą, kurią norėsite naudoti, kai bus išpildyti įvesti kriterijai.
16. Pasirinkite **Įtraukti**.
17. Uždarykite puslapį.
18. Pasirinkite **Aktyvinti**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]