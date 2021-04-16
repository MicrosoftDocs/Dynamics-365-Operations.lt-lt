---
title: Produkto konfigūravimo pagal dimensijas apžvalga
description: Produktų konfigūravimas pagal dimensijas nurodo paprastą sprendimą norint kurti daug produkto variantų iš vieno bendrojo produkto ir jo KS.
author: cvocph
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16027cc7fd22a34e3f689678aa9f5e85800cbf02
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829527"
---
# <a name="dimension-based-product-configuration-overview"></a>Produkto konfigūravimo pagal dimensijas apžvalga

[!include [banner](../includes/banner.md)]

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
Natūrali dimensijomis paremto produkto modelio kūrimo seka pradedama apibrėžiant aktualias konfigūracijos grupes. Svarbu užtikrinti, kad visi produktai, kurie bus naudojami KS, išleisti į įmonę, kuriai sukurtas produkto modelis. Pasirūpinęs šiais kūrimo blokais, naudotojas gali kurti KS ir visoms aktualioms KS eilutėms priskirti konfigūracijos grupes. Kai KS baigta, galima apibrėžti konfigūracijos maršrutą, kad konfigūracijos grupės būtų surikiuotos tinkama tvarka. [![Dimensijomis paremtų produktų modeliavimo procesas](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Jei skirtingose konfigūracijos grupėse yra tam tikrų produktų, kuriuos arba reikia naudoti kartu, arba nereikia, galite sukurti konfigūracijos taisykles, kurios užtikrins šiuos produktų ryšius. Kai, naudojant KS versiją, KS susieta su dimensijomis paremtu bendruoju produktu, ir jie abu patvirtinti bei suaktyvinti, galite kurti produktų konfigūracijų ir įvesti kiekvienos konfigūracijos pavadinimą. Konfigūracijas galima apibrėžti prieš sugeneruojant bet kokias operacijas, arba tai galima atlikti atsiradus tam tikros konfigūracijos poreikiui.

### <a name="suggested-use"></a>Rekomenduojama paskirtis

Konfigūravimo pagal dimensijas technologiją geriausia naudoti su ribotos įvairovės produktais su standartinių produkto dimensijų dydžio, spalvos, stiliaus deriniu ir kai konfigūracija netinka identifikuoti konkrečiam produkto variantui. Pavyzdys galėtų būti dviratis, kurio nurodytas rėmo aukštis, ratų dydis, stabdžių tipai ir skirtingos pavaros.

### <a name="next-step"></a>Kitas veiksmas 

Toliau nurodyti aštuoni užduočių vedliai išvardyti tokia tvarka, kokia juos turite atlikti. 

1.  [Bendrojo produkto pagal dimensijas kūrimas](tasks/create-dimension-based-product-master.md)
2.  [Bendrojo produkto pagal dimensijas išleidimas](tasks/release-dimension-based-product-master.md)
3.  [Pagrindinės išleisto bendrojo produkto sąrankos baigimas](tasks/complete-basic-setup-released-product-master.md)
4.  [Konfigūracijų grupių apibrėžimas](tasks/define-configuration-groups.md)
5.  [Bendrojo produkto pagal dimensijas KS kūrimas](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [Konfigūracijos maršrutų apibrėžimas](tasks/define-configuration-route.md)
7.  [Konfigūracijos taisyklių kūrimas](tasks/create-configuration-rules.md)
8.  [Konfigūracijų pagal dimensijas kūrimas](tasks/create-dimension-based-configurations.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]