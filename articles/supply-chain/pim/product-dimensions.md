---
title: "Produktų dimensijos"
description: "Produktų dimensijos yra keturios – Spalva, Konfigūracija, Dydis ir Stilius. Produktų dimensijos jungiamos į dimensijų grupes, o dimensijų grupės priskiriamos bendriesiems produktams. Produktų dimensijų kombinacijomis nustatoma, kaip apibrėžiami produktų variantai."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 105324f146f28bc61e87dff1089b367958ff9062
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="product-dimensions"></a>Produktų dimensijos

[!include[banner](../includes/banner.md)]

[!include[Retail name](../includes/retail-name.md)]


Produktų dimensijos yra keturios – Spalva, Konfigūracija, Dydis ir Stilius. Produktų dimensijos jungiamos į dimensijų grupes, o dimensijų grupės priskiriamos bendriesiems produktams. Produktų dimensijų kombinacijomis nustatoma, kaip apibrėžiami produktų variantai.

Produkto dimensijos – tai charakteristikos, naudojamos produkto variantui nustatyti. Galite naudoti produkto dimensijų derinius produkto variantams nustatyti. Norėdami sukurti produkto variantą, turite nustatyti bent vieną bendrojo produkto dimensiją.
Produkto variantai
----------------

Produkto variantai taip pat vadinami prekėmis. Prekė – tai materialus produktas, kuris nėra apibūdinamas visiškai taip pat, kaip paslauga. Taip pat galima nustatyti bendrąjį produktą naudojant tipą Paslauga. Naudodami tipą Paslauga, galite nurodyti produkto variantus, kuriuose yra paslaugų. Pavyzdžiui, galite nurodyti konsultacinio darbo bendrąjį produktą bei vyresniųjų ir jaunesniųjų konsultantų atliekamo darbo produkto variantus.

## <a name="product-dimensions"></a>Produktų dimensijos
Galimos šios produktų dimensijos: Konfigūracija, Spalva, Dydis ir Stilius. Produkto variantas gali būti kuriamas pagal produkto dimensijų reikšmes.

Produkto dimensijų vertes, pvz., Dydis, Spalva ir Stilius, galima sukurti puslapiuose **Dydis**, **Spalva** ir **Stilius**, kuriuos galima pasiekti iš šių vietų: **Produkto informacijos valdymas** &gt; **Sąranka** &gt; **Dimensijų ir variantų grupės** &gt; **Dydžiai / Spalvos / Stiliai**. Konfigūracijos dimensijos produkto dimensijų vertės paprastai kuriamos naudojant produkto konfigūratorių arba dimensijomis pagrįstą konfigūratorių. Produkto dimensijos taip pat gali būti kuriamos ir tvarkomos puslapyje **Produktų dimensijos**, kurį galima pasiekti šiose vietose:
-   Spustelėkite **Produkto informacijos valdymas** &gt; **Produktai** &gt; **Bendrieji produktai**. Dalyje **Veiksmų sritis** spustelėkite **Produktų dimensijos**.
-   Spustelėkite **Produkto informacijos valdymas** &gt; **Produktai** &gt; **Visi produktai ir bendrieji produktai**. Pasirinkite bendrąjį produktą. Dalyje **Veiksmų sritis** spustelėkite **Produktų dimensijos**.
-   Spustelėkite **Produkto informacijos valdymas** &gt; **Patvirtinti produktai**. Pasirinkite bendrąjį produktą. Dalyje **Veiksmų sritis** spustelėkite **Produktas**. Grupėje **Bendrasis produktas** spustelėkite **Produktų dimensijos**.

Variantų, kuriuos galite sukurti prekei, kiekis ribojamas pagal galimų produkto dimensijų derinių kiekį.
| **Patarimas**                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pavyzdžiui, užsakymo eilutėje naudodami produktą, pasirinkę produkto dimensijas identifikuosite norimą naudoti produkto variantą. |

## <a name="example"></a>Pavyzdys
Įmonė parduoda džinsus. Prekei (džinsams) apibūdinti naudojamos produktų dimensijos Spalva ir Dydis. Parduodami trijų skirtingų spalvų ir šešių skirtingų dydžių džinsai. Spalvos: mėlyna, juoda, ruda Dydžiai: XS, S, M, L, XL, XXL Ne visi dydžiai galimi visų trijų spalvų. Jei būtų galimi visi deriniai, būtų sukurta 18 skirtingų tipų džinsų. Šiame pavyzdyje sukurti tik šie devyni produkto variantų deriniai.

| Spalva | Dydis |
|-------|------|
| Mėlyna  | XS   |
| Mėlyna  | Š.    |
| Mėlyna  | P    |
| Juoda | P    |
| Juoda | L    |
| Juoda | XL   |
| Ruda | L    |
| Ruda | XL   |
| Ruda | XXL  |






