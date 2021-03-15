---
title: Finansinių dimensijų įtraukimas į CFO darbo sritį
description: Šioje temoje paaiškinama, kaip įtraukti finansines dimensijas į CFO darbo sritį, kad būtų galima jas naudoti DK ir biudžeto ataskaitose.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 457c547947ce6182d03e7a8276b380bc08535bca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985117"
---
# <a name="add-financial-dimensions-to-the-cfo-workspace"></a>Finansinių dimensijų įtraukimas į CFO darbo sritį

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip įtraukti finansines dimensijas į vyriausiojo finansininko (CFO) darbo sritį, kad būtų galima jas naudoti DK ir biudžeto ataskaitose. CFO darbo srityje yra skirtukai **Apžvalga** ir **Finansin.**. Ataskaitos šiuose dviejuose skirtukuose pagrįstos dviem priemonėmis: LedgerActivityMeasure ir BudgetActivityMeasure. Yra sąsaja tarp tų dviejų priemonių ir objekto DimensionCombinationEntity. Todėl galima pasirinkti dimensijas.

1. Naudojant „Finance“, puslapyje **Objekto parduotuvė** atnaujinkite priemonę **LedgerActivityMeasure** ir **BudgetActivityMeasure**.
2. Naudojant „Microsoft Visual Studio“, atidarykite programų naršymo priemonę ir ieškokite **LedgerCFO**.
3. Srityje **Ištekliai** atidarykite **LedgerCFOWorkspacePBIX**.
4. Kai bus atidarytas išteklius „Microsoft Power BI“ darbalaukyje, pasirinkite **Gauti duomenis**, pasirinkite **SQL serverio duomenų bazė** tada pasirinkite **Jungtis**.
5. Įveskite serverio vardą, tada įveskite **AxDW** kaip duomenų bazę. Pasirinkite **DirectQuery**, tada pasirinkite **OK**.
6. Raskite ir pasirinkite **LedgerActivityMeasure\_DimensionCombination**, tada pasirinkite **Load**.

    > [!TIP]
    > Sąraše **Laukai** pakeiskite lentelės **Finansinės dimensijos** pavadinimą, kad ją būtų paprasta identifikuoti.

7. Pasirinkite **Valdyti ryšius**, tada pasirinkite **Naujas**.
8. Pirmame lauke pasirinkite **Didžiosios knygos veiklos**, tada pasirinkite **LedgerDimension**.
9. Antrame lauke pasirinkite **LedgerActivityMeasure\_DimensionCombination** (arba **Finansinės dimensijos**, jei pervardijote lentelę). Pasirinkite antraštę **DimensionCombinationRECID**.
10. Lauke **Svarba** pasirinkite **Daugelis su vienu**.
11. Pakeiskite reikšmę **Kelių filtrų kryptys** į **Viena**.
12. Pasirinkite **Suaktyvinti šį ryšį** ir **Naudoti nurodomąjį integralumą**, pasirinkite **Gerai**, tada pasirinkite **Uždaryti**.

    [![Ryšio kūrimas](./media/Create-relationship.png)](./media/Create-relationship.png)

13. Sąraše **Laukai** turėtų būti rodoma lentelė ir pasiekiamos finansinės dimensijos. Vilkite norimas finansines dimensijas į ataskaitų lygio filtrus.
14. Įrašykite pakeitimus.
15. Programos objektų medyje (AOT) dešiniuoju pelės mygtuku spustelėkite projektą, tada pasirinkite **Sinchronizuoti**.
16. Sukurkite projektą, tada atidarykite programą, kad peržiūrėtumėte rezultatus.

    [![Baigta darbo sritis](./media/workspace.png)](./media/workspace.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]