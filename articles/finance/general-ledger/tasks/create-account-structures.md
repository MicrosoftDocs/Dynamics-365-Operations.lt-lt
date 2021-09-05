---
title: Sąskaitų struktūrų kūrimas
description: Ši procedūra padeda sukurti sąskaitos struktūrą.
author: aprilolson
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9ba43e243df4ba4b7c0eb6188629686206ff09b
ms.sourcegitcommit: 03f53980a4bc67b73ac2be76a3b3e7331d0db705
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/18/2021
ms.locfileid: "7394544"
---
# <a name="create-account-structures"></a>Sąskaitų struktūrų kūrimas

[!include [banner](../../includes/banner.md)]

Ši procedūra padeda sukurti sąskaitos struktūrą. Veiksmuose naudojama demonstracinių duomenų įmonė USMF.

1. Eikite į **Naršymo sritis > Moduliai > Didžioji knyga > Sąskaitų planas > Struktūros > Konfigūruoti sąskaitų struktūras**.
2. **Veiksmų sritis** spustelėkite **Naujas**, kad atidarytumėte tiesioginio dialogo langą.
3. Lauke **Sąskaitos struktūra** įveskite pavadinimą, aprašantį sąskaitos struktūros tikslą.
4. Lauke **Aprašas** įveskite aprašą, apibūdinantį sąskaitos struktūros tikslą.
5. Spustelėkite **Kurti**.
6. **Segmentai ir leidžiamos reikšmės** spustelėkite **Įtraukti segmentą**.
7. Matmenų sąraše pažymėkite į sąskaitos struktūrą įtrauktiną matmenį.
8. Sąrašo pabaigoje spustelėkite **Įtraukti segmentą**.
9. Jei reikia, pakartokite 6–9 veiksmus.
10. Skyriuje **Leidžiamos reikšmės išsami informacija** pažymėkite segmentą, kad galėtumėte redaguoti leidžiamas reikšmes.
    Pavyzdžiui, spustelėkite lauką **Pagrindinė sąskaita**.  
11. Lauke **Operatorius** pasirinkite parinktį, pvz., „yra tarp“ ir „apima“.
12. Lauke **Reikšmė** įveskite reikšmę. Pavyzdžiui, 600000.  
13. Lauke **per** įveskite reikšmę. Pavyzdžiui, 699999.  
14. Skyriuje **Leidžiamos reikšmės išsami informacija** spustelėkite **Taikyti**.
15. Jei reikia, pakartokite 10–15 veiksmus.  
16. Skyriuje **Leidžiamos reikšmės išsami informacija** spustelėkite **Įtraukti naujus kriterijus**.
17. Lauke Operatorius, pasirinkite parinktį, pvz., „yra tarp“ ir „apima“.
18. Lauke **Reikšmė** įveskite reikšmę. Pavyzdžiui, 033.  
19. Lauke **per** įveskite reikšmę. Pavyzdžiui, 034.  
20. Spustelėkite **Taikyti**.
21. Tinklelyje pasirinkite segmentą, kad galėtumėte redaguoti leidžiamas reikšmes. Pavyzdžiui, Išlaidų centras.  
22. Lauke **CostCenter laukas** įveskite reikšmę. Pavyzdžiui, 007..021.  
23. **Segmentai ir leidžiamos reikšmės** spustelėkite **Įtraukti**.
24. Lauke **MainAccount** įveskite reikšmę. Pavyzdžiui, 600000..699999  
25. Tinklelyje pasirinkite segmentą, kad galėtumėte redaguoti leidžiamas reikšmes. Pavyzdžiui, Padalinys.  
26. Lauke Padalinys įveskite reikšmę. Pavyzdžiui, 032.  
27. Lauke Išlaidų centras įveskite reikšmę. Pavyzdžiui, 086.  
28. **Veiksmų sritis** spustelėkite **Tikrinti**.
29. **Veiksmų sritis** spustelėkite **Aktyvinti**.
30. Spustelėkite **Aktyvinti**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
