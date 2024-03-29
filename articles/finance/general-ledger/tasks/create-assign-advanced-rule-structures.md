---
title: Išplėstinių taisyklių struktūrų kūrimas ir priskyrimas
description: Šiame straipsnyje paaiškinama, kaip sukurti ir priskirti išplėstinės taisyklės struktūrą sąskaitos struktūrai.
author: aprilolson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72688642936f9428c96aebb34bf9f240dd48b46b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896325"
---
# <a name="create-and-assign-advanced-rule-structures"></a>Išplėstinių taisyklių struktūrų kūrimas ir priskyrimas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip sukurti ir priskirti išplėstinės taisyklės struktūrą sąskaitos struktūrai. Šiame vadove naudojama demonstracinė įmonė USMF.

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
