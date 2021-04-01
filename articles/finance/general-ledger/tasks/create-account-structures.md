---
title: Sukurti sąskaitos struktūras
description: Šis užduoties vadovas padeda sukurti sąskaitos struktūrą.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed8ce37ab642277ff843e6320a880fac40d41acb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235794"
---
# <a name="create-account-structures"></a>Sukurti sąskaitos struktūras

[!include [banner](../../includes/banner.md)]

Šis užduoties vadovas padeda sukurti sąskaitos struktūrą. Veiksmuose naudojama demonstracinių duomenų įmonė USMF.

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