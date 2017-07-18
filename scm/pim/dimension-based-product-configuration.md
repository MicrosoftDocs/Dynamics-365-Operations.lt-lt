---
title: "Produktų konfigūravimas pagal dimensijas"
description: "Produktų konfigūravimas pagal dimensijas nurodo paprastą sprendimą norint kurti daug produkto variantų iš vieno bendrojo produkto ir jo KS."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d13fc55342030d96d38f264f6bff9586832b4ab5
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017

---

# <a name="dimension-based-product-configuration"></a>Produktų konfigūravimas pagal dimensijas

[!include[banner](../includes/banner.md)]


Produktų konfigūravimas pagal dimensijas nurodo paprastą sprendimą norint kurti daug produkto variantų iš vieno bendrojo produkto ir jo KS.

Produktų konfigūravimas pagal dimensijas yra viena iš trijų integruotų produktų konfigūravimo technologijų. Kitos dvi technologijos yra iš anksto apibrėžti variantai ir konfigūravimas pagal apribojimus. Visos trys technologijos kaip pradžios tašką naudoja bendrąjį produktą ir naudotojui leidžia kurti daug vieno bendrojo produkto variantų.

## <a name="key-concepts"></a>Pagrindinės koncepcijos
Produktų konfigūravimas pagal dimensijas paremtas tolesnėmis pagrindinėmis koncepcijomis.

-   Bendrieji produktai
-   Konfigūracijų produkto dimensija
-   Konfigūracijų grupės
-   Komplektavimo specifikacijos (KS)
-   Konfigūracijos maršrutas
-   Konfigūracijos taisyklės

### <a name="product-masters"></a>Bendrieji produktai

Bendrasis produktas yra pradinis bet kokio produktų konfigūravimo proceso taškas. Norint produktus konfigūruoti pagal dimensijas, reikia bendrojo produkto su šia konkrečia konfigūravimo technologija ir produkto dimensijų grupės, kurioje būtų konfigūracijų produkto dimensija.

### <a name="configuration-product-dimension"></a>Konfigūracijų produkto dimensija

Konfigūracijų produkto dimensija naudojama indentifikuoti bendrojo produkto su konfigūravimo pagal dimensijas technologija variantams. Konfigūracijos dimensijos reikšmę įveda naudotojas, ir ji turėtų padėti identifikuoti atskirus produktų variantus.

### <a name="configuration-groups"></a>Konfigūracijų grupės

Konfigūracijos grupės apibrėžiamos centrinėje saugykloje ir gali būti naudojamos su visais produktų konfigūravimo pagal dimensijas modeliais. Konfigūracijos grupės susietos su atskiromis KS eilutėmis ir kartu sudaro tarpusavyje nesuderinamų eilučių grupę. Tai reiškia, kad vienam produkto variantui galima parinkti tik vieną grupės eilutę.

### <a name="bill-of-materials-bom"></a>Komplektavimo specifikacijos (KS)

KS – tai produktų konfigūravimo pagal dimensijas kūrimo blokai. Ji turi apimti visus skirtingus produktus, kuriuos galima naudoti su bet kuriuo produkto variantu. Kiekviena KS eilutė gali nurodyti į konfigūracijos grupę. Jei eilutė nenurodo į konfigūracijos grupę, ji bus įtraukta į visus produkto variantus.

### <a name="configuration-route"></a>Konfigūracijos maršrutas

Konfigūracijos maršrutas nustato konfigūracijos grupių seką: kaip jos bus rodomos naudotojui vykdant produktų konfigūravimą.

### <a name="configuration-rules"></a>Konfigūracijos taisyklės

Konfigūracijos taisyklės – tai mechanizmas, skirtas užtikrinti, kad produktas, įtrauktas į vieną KS konfigūracijos grupę, lemtų produkto kitoje tos pačios KS konfigūracijos grupėje išėmimą arba įtraukimą.

## <a name="product-modeling-process"></a>Produkto modeliavimo procesas
Natūrali dimensijomis paremto produkto modelio kūrimo seka pradedama apibrėžiant aktualias konfigūracijos grupes. Svarbu užtikrinti, kad visi produktai, kurie bus naudojami KS, išleisti į įmonę, kuriai sukurtas produkto modelis. Pasirūpinęs šiais kūrimo blokais, naudotojas gali kurti KS ir visoms aktualioms KS eilutėms priskirti konfigūracijos grupes. Kai KS baigta, galima apibrėžti konfigūracijos maršrutą, kad konfigūracijos grupės būtų surikiuotos tinkama tvarka. \[caption id="attachment\_282671" align="alignnone" width="1187"\][![Dimensijomis paremtų produktų modeliavimo procesas](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Dimensijomis paremtų produktų modeliavimo procesas\[/caption\] Jei skirtingose konfigūracijos grupėse yra tam tikrų produktų, kuriuos arba reikia naudoti kartu, arba nereikia, galite sukurti konfigūracijos taisykles, kurios užtikrins šiuos produktų ryšius. Kai, naudojant KS versiją, KS susieta su dimensijomis paremtu bendruoju produktu, ir jie abu patvirtinti bei suaktyvinti, galite kurti produktų konfigūracijų ir įvesti kiekvienos konfigūracijos pavadinimą. Konfigūracijas galima apibrėžti prieš sugeneruojant bet kokias operacijas, arba tai galima atlikti atsiradus tam tikros konfigūracijos poreikiui.

### <a name="suggested-use"></a>Rekomenduojama paskirtis

Konfigūravimo pagal dimensijas technologiją geriausia naudoti su ribotos įvairovės produktais su standartinių produkto dimensijų dydžio, spalvos, stiliaus deriniu ir kai konfigūracija netinka identifikuoti konkrečiam produkto variantui. Pavyzdys galėtų būti dviratis, kurio nurodytas rėmo aukštis, ratų dydis, stabdžių tipai ir skirtingos pavaros.




