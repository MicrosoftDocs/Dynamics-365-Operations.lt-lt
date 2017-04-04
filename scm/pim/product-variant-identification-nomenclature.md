---
title: "Nomenklatūrą numerių"
description: "Šioje temoje aprašoma, kaip galite nustatyti nomenklatūrą numerių pakeisti nustatyta forma, [produkto meistras - konfigūracija - dydis - spalva - numerio], su tikslinės formatą, kuris apima pagrindinio produkto numerį, aktyvus produkto matmenys ir teksto skyrikliai savo pasirinkimą. Taip pat galite kurti nomenklatūrą, norėdami nustatyti konfigūracijas, kurias sukūrė apribojimais pagrįstas produkto konfigūratorius. Į šias nomenklatūras galima įtraukti pasirinktus atributus."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220104
ms.assetid: 31c9efb4-b5f6-4af3-b884-8f1e128469bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 58afcd62e7ef317e624fd26d198c2606bf53e6a5
ms.lasthandoff: 03/31/2017


---

# <a name="product-number-nomenclature"></a>Nomenklatūrą numerių

Šioje temoje aprašoma, kaip galite nustatyti nomenklatūrą numerių pakeisti nustatyta forma, [produkto meistras - konfigūracija - dydis - spalva - numerio], su tikslinės formatą, kuris apima pagrindinio produkto numerį, aktyvus produkto matmenys ir teksto skyrikliai savo pasirinkimą. Taip pat galite kurti nomenklatūrą, norėdami nustatyti konfigūracijas, kurias sukūrė apribojimais pagrįstas produkto konfigūratorius. Į šias nomenklatūras galima įtraukti pasirinktus atributus.

Naujoji produkto variantų numerių nomenklatūra suteikia galimybę į produkto variantų identifikatorius įtraukti segmentų. Šie segmentai gali būti bendrojo produkto numeris, produkto dimensijos, numeracijos, teksto konstantos ir atributai. Naudodami šią funkciją galite greitai rasti konkretų produkto variantą, kai kuriate pardavimo užsakymą arba pirkimo užsakymą.

## <a name="nomenclature-of-predefined-product-variants"></a>Iš anksto apibrėžtų produkto variantų nomenklatūra
Pagrindinių produktų variantai generuojami pagal vieną iš trijų konfigūravimo technologijų.

-   Iš anksto apibrėžti variantai
-   Pagrįsti apribojimais
-   Pagrįsti dimensijomis

Kiekvienas produkto variantas turi numerį, produkto variantų identifikavimo nomenklatūra suteikia galimybę pasirinkti segmentus, kurie bus įtraukti į kiekvieno produkto varianto numerį. Puslapyje **Produktų nomenklatūra** galite pasirinkti toliau nurodytus segmentus.

-   Bendrojo produkto numeris
-   Numeracijos reikšmė
-   Teksto konstanta
-   Produktų dimensijos
    -   Konfigūravimas
    -   Spalva
    -   Dydis
    -   Stilius

Apibrėžus produkto variantų identifikavimo nomenklatūrą, ją galima susieti su produkto dimensijų grupe. Taigi, visiems bendriesiems produktams, nurodantiems šią produkto dimensijų grupę, bus priskirti produkto variantų numeriai, atsižvelgiant į nomenklatūrą. Taip pat produkto variantų identifikavimo nomenklatūrą galima tiesiogiai priskirti bendrajam produktui. Tokiu atveju šiam bendrajam produktui priklausantiems produkto variantams bus priskirti produkto variantų numeriui, atsižvelgiant į nomenklatūrą.

### <a name="example"></a>Pavyzdys

Marškinėliai (TS1234) gaminami 3 skirtingų dydžių (S, M, L), 4 skirtingų spalvų (raudoni, žali, mėlyni, geltoni) ir 2 stilių (Polo, V), todėl iš viso galimi 24 produkto variantai. Sukuriama produkto variantų identifikavimo nomenklatūra, naudojant toliau pateiktus segmentus.

1.  Bendrojo produkto numeris
2.  Teksto konstanta: '-'
3.  Spalva
4.  Teksto konstanta: '-'
5.  Dydis
6.  Teksto konstanta: '-'
7.  Stilius

Raudonų S dydžio Polo marškinėlių produkto varianto numeris bus: TS1234-Red-Small-Polo.

## <a name="nomenclature-of-constraintbased-configurations"></a>Nomenklatūros constraintbased konfigūracijų
Apribojimas, pagrįstas konfigūracijoms, skirta nomenklatūrą gali būti pastatyta konfigūracijos prekės dimensija. Puslapyje **Produktų nomenklatūra** galite pasirinkti toliau nurodytus segmentus.

-   Numeracijos reikšmė
-   Teksto konstanta
-   Atributo vertė 

Kiekvienam produkto konfigūracijos modelio komponentui gali būti priskirta atskira konfigūracijos nomenklatūra. Galima naudoti tik komponentui priklausančius atributus. Subkomponentų arba vartotojo reikalavimų atributų naudoti negalima.

### <a name="example"></a>Pavyzdys

Produkto konfigūracijos modeliui priskiriamas šakninis komponentas su dviem atributais.

-   Medžiagos (plastmasė, medis, plienas)
-   Ilgis (10... 100)

Konfigūracijos nomenklatūra nurodoma naudojant toliau pateiktus segmentus.

1.  Atributo reikšmė: medžiagos
2.  Teksto konstanta: 'AAA'
3.  Atributo reikšmė: ilgis

Medžiagos iš medžio, kurios ilgis 78, konfigūracijos ID bus: WoodAAA78.

## <a name="nomenclature-of-dimensionbased-configurations"></a>Nomenklatūros dimensionbased konfigūracijų
Dimensijos pagal konfigūracijoms, skirta nomenklatūrą gali būti pastatyta konfigūracijos prekės dimensija. Puslapyje **Produktų nomenklatūra** galite pasirinkti toliau nurodytus segmentus.

-   Numeracijos reikšmė
-   Teksto konstanta
-   Konfigūracijos grupės prekė

Galima nurodyti konfigūracijos nomenklatūrą, skirtą komplektavimo specifikacijai (KS).

### <a name="example"></a>Pavyzdys

Komplektavimo specifikacijoje 4 KS eilutės padalintos į 2 konfigūracijų grupes.

-   KS eilutė: M0007, standartinė spintelė
    -   Konfigūracijos grupė: spintelė
-   KS eilutė: M0008, aukštos kokybės spintelė
    -   Konfigūracijos grupė: spintelė
-   KS eilutė: M0021, priekinės grotelės iš audinio
    -   Konfigūracijos grupė: priekinės grotelės
-   KS eilutė: M0022, priekinės grotelės iš metalo
    -   Konfigūracijos grupė: priekinės grotelės

Konfigūracijos nomenklatūra nurodoma naudojant toliau pateiktus segmentus.

1.  Konfigūracijos grupė: spintelė
2.  Teksto konstanta: '&'
3.  Konfigūracijos grupė: priekinės grotelės

Standartinės spintelės su priekinėmis grotelėmis iš audinio konfigūracijos ID bus: M0007&M0021.

## <a name="nomenclature-of-a-combination-of-product-variants-and-configurations"></a>Produkto variantų ir konfigūracijų derinio nomenklatūra
Kai naudojate konfigūravimo pagal apribojimus arba konfigūravimo pagal dimensijas technologiją, norėdami konfigūruoti pagrindinio produkto variantus, produkto variantams galima priskirti produkto variantų numerius, į kuriuos įtraukta konfigūracijos dimensijos nomenklatūra. Norėdami konfigūruoti variantus, atlikite šiuos veiksmus.

1.  Puslapyje **Produktų nomenklatūra** nurodykite produkto variantų numerių nomenklatūrą, į kurią įtraukta konfigūracijos dimensija.
2.  Priskirkite šią nomenklatūrą produkto dimensijų grupei su konfigūracijos dimensija.
3.  Nurodykite komponentų arba KS konfigūracijos nomenklatūrą, kuri bus naudojama konfigūruojant produkto variantus.

### <a name="example-for-constraint-based-configurations"></a>Konfigūravimo pagal apribojimus pavyzdys

Šiame pavyzdyje galite naudoti produkto variantų numerių nomenklatūrą, kurią sudaro toliau nurodyti segmentai.

1.  Bendrojo produkto numeris
2.  Tekstine konstanta "\_"
3.  Konfigūravimas

Konfigūracijos nomenklatūrą gali sudaryti toliau pateikti segmentai.

1.  Atributo reikšmė: medžiagos
2.  Teksto konstanta: 'AAA'
3.  Atributo reikšmė: ilgis

Galite įvesti toliau nurodytas segmentų reikšmes.

-   Bendrojo produkto numeris = M0099
-   Medžiagos = plastmasė
-   Ilgis = 12

Taps produkto rūšies numerį: M0099\_PlasticAAA12.

### <a name="example-for-dimension-based-configurations"></a>Konfigūravimo pagal dimensijas pavyzdys

Šiame pavyzdyje galite naudoti produkto variantų numerių nomenklatūrą, kurią sudaro toliau nurodyti segmentai.

1.  Bendrojo produkto numeris
2.  Teksto konstanta: '//'
3.  Konfigūravimas

Konfigūracijos nomenklatūrą gali sudaryti toliau pateikti segmentai.

1.  Konfigūracijos grupė: spintelė
2.  Teksto konstanta: '&'
3.  Konfigūracijos grupė: priekinės grotelės

Galite įvesti toliau nurodytas segmentų reikšmes.

-   Bendrojo produkto numeris = D0123
-   Spintelė = M0008
-   Priekinės grotelės = M0022

Produkto varianto numeris bus: D0123//M0008&M0022.

## <a name="numbering-conflicts"></a>Numeravimo nesuderinamumai
Galima nustatyti produkto variantų numerių nomenklatūrą, kurią naudojant nebūtų kuriami unikalūs produkto variantų numeriai. Pavyzdžiui, taip gali nutikti, jei viena aktyvi produkto dimensija nėra įtraukta į bendrojo produkto, kuriame naudojama apibrėžta variantų konfigūravimo technologija, nomenklatūrą. Skirtingos konfigūravimo technologijose nesuderinamumai tvarkomi skirtingai.

### <a name="predefined-variants"></a>Iš anksto apibrėžti variantai

Jei automatiškai arba neautomatiškai bandysite generuoti produkto variantus, kurių vienas ar daugiau turės tokį patį produkto varianto numerį, įvyks klaida. Norėdami to išvengti, turite naudoti visas aktyvias produkto dimensijų grupės produkto dimensijas arba įtraukti numeraciją ir taip užtikrinti, kad produkto varianto numeriai bus unikalūs.

### <a name="constraint-based-configurations"></a>Konfigūravimas pagal apribojimus

Priklausomai nuo nomenklatūros, sistema gali bandyti konfigūracijai priskirti ne unikalų produkto varianto numerį. Tokiu atveju sistema naudos numeracija konfigūracijos dimensiją kaip produkto rūšies numerį vietoj. Jei taip nutinka, gausite įspėjimą. Norėdami to išvengti, turėtumėte į nomenklatūrą įtraukti pakankamai atributų, kad užtikrintumėte unikalumą, ir įsitikinti, kad įjungta komponento parinktis **Pakartotinai naudoti**.

### <a name="dimension-based-configurations"></a>Konfigūravimas pagal dimensijas

Į konfigūravimo procesą įtrauktas etapas, kurio metu sistema pasiūlys konfigūracijos reikšmę pagal nomenklatūrą. Šio etapo metu galite neautomatiškai keisti konfigūracijos reikšmę. Kai įrašote konfigūraciją, sistema patikrins, ar konfigūracijos reikšmė yra unikali. Jei ji nėra unikali, rodoma klaida. Turite įvesti unikalią konfigūracijos reikšmę, kad galėtumėte konfigūraciją įrašyti.



<a name="see-also"></a>Taip pat žiūrėkite
--------

[Sukurti produkto numeris nomenklatūros iš anksto nustatytų prekių dimensijų kombinacijoje (darbo vadovas)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-predefined-product-variants/)

[Sukurti produkto numeris nomenklatūros konfigūruotų gaminių variantams (darbo vadovas)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-configured-product-variants/)


