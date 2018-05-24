---
title: "Produkto variantų numerių ir pavadinimų nomenklatūra"
description: "Šioje temoje aprašoma, kaip nustatyti produkto numerių nomenklatūrą, norint pakeisti fiksuotą [bendrojo produkto numeris – konfigūracija – dydis – spalva – stilius] formatą."
author: roxanadiaconu
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3baf1d7313d8ff03ae5ece035b6f3641c0f1d707
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a>Produkto variantų numerių ir pavadinimų nomenklatūra

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip nustatyti produkto numerių nomenklatūrą, norint pakeisti fiksuotą [bendrojo produkto numeris – konfigūracija – dydis – spalva – stilius] formatą. Naujojoje nomenklatūroje naudojamas tikslinis formatas, kuris apima bendrojo produkto numerį, aktyvias produkto dimensijas ir pasirinktus teksto skyriklius. Taip pat galite kurti produkto pavadinimų nomenklatūrą. Galiausiai galite kurti nomenklatūrą, norėdami nustatyti konfigūracijas, kurias sukūrė apribojimais pagrįstas produkto konfigūratorius. Į šias nomenklatūras galima įtraukti pasirinktus atributus.

Naujoji produkto variantų numerių ir produkto variantų pavadinimų nomenklatūra suteikia galimybę į produkto variantų identifikatorius įtraukti segmentus. Šie segmentai gali būti bendrojo produkto numeris ir pavadinimas, produkto dimensijų ID ir pavadinimai, numeracijos, teksto konstantos ir atributai. Naudodami šią funkciją galite greitai rasti konkretų produkto variantą, kai kuriate pardavimo užsakymą arba pirkimo užsakymą. Produkto variantų numerių ir produkto variantų pavadinimų nomenklatūras galite kurti naudodami puslapį **Produkto nomenklatūra**. Norėdami atidaryti šį puslapį, spustelėkite **Produkto informacijos valdymas** &gt; **Sąranka**.

## <a name="nomenclature-of-predefined-product-variants"></a>Iš anksto apibrėžtų produkto variantų nomenklatūra
Pagrindinių produktų variantai generuojami pagal vieną iš trijų konfigūravimo technologijų.

-   Iš anksto apibrėžti variantai
-   Pagrįsti apribojimais
-   Pagrįsti dimensijomis

Kiekvienas produkto variantas turi numerį ir pavadinimą, o produkto variantų identifikavimo nomenklatūros suteikia galimybę pasirinkti segmentus, kurie bus įtraukti į kiekvieno produkto varianto numerį arba pavadinimą. Puslapyje **Produkto nomenklatūra** galite pasirinkti toliau nurodytus segmentus.

-   Bendrojo produkto numeris
-   Bendrojo produkto pavadinimas
-   Numeracijos reikšmė
-   Teksto konstanta
-   Produktų dimensijos
    -   Konfigūracijos ID arba pavadinimas
    -   Spalvos ID arba pavadinimas
    -   Dydžio ID arba pavadinimas
    -   Stiliaus ID arba pavadinimas

Apibrėžus produkto variantų identifikavimo numerių nomenklatūrą, ją galima susieti su produkto dimensijų grupe. Tada visiems bendriesiems produktams, nurodantiems šią produkto dimensijų grupę, bus priskirti produkto variantų numeriai, atsižvelgiant į nomenklatūrą. Tačiau produkto variantų pavadinimų nomenklatūrų negalima susieti su produkto dimensijų grupėmis. Taip pat produkto variantų identifikavimo nomenklatūrą galite tiesiogiai priskirti bendrajam produktui. Šiuo atveju produkto variantams, kurie priklauso bendrajam produktui, bus priskirti produkto variantų numeriai ir pavadinimai, atsižvelgiant į nomenklatūras.

### <a name="example"></a>Pavyzdys

Gaminami trijų dydžių (S, M, L), keturių spalvų (raudona, žalia, mėlyna, geltona) ir dviejų tipų (Polo, V) marškinėliai (TS1234). Todėl galimi 24 produkto variantai (= 3 x 4 x 2). Galite kurti produkto variantų numerių nomenklatūrą, kurioje yra toliau nurodyti segmentai.

1.  Bendrojo produkto numeris
2.  Teksto konstanta: "-"
3.  Spalva
4.  Teksto konstanta: "-"
5.  Dydis
6.  Teksto konstanta: "-"
7.  Stilius

Šiuo atveju raudonų S dydžio Polo marškinėlių produkto varianto numeris bus: TS1234-Red-Small-Polo.

## <a name="nomenclature-of-constraint-based-configurations"></a>Konfigūravimo pagal apribojimus nomenklatūra
Atliekant konfigūravimą pagal apribojimus galima kurti specialią konfigūracijos produkto dimensijos nomenklatūrą. Puslapyje **Produkto nomenklatūra** galite pasirinkti toliau nurodytus segmentus.

-   Numeracijos reikšmė
-   Teksto konstanta
-   Atributo vertė

Kiekvienam produkto konfigūracijos modelio komponentui gali būti priskirta atskira konfigūracijos nomenklatūra. Galima naudoti tik komponentui priklausančius atributus. Subkomponentų arba vartotojo reikalavimų atributų naudoti negalima.

### <a name="example"></a>Pavyzdys

Produkto konfigūracijos modeliui priskiriamas šakninis komponentas su dviem atributais.

-   Medžiagos (plastmasė, medis, plienas)
-   Ilgis (10... 100)

Galite kurti konfigūracijos nomenklatūrą, kurioje yra toliau nurodyti segmentai.

1.  Atributo reikšmė: medžiagos
2.  Teksto konstanta: "AAA"
3.  Atributo reikšmė: ilgis

Šiuo atveju medžiagos iš medžio, kurios ilgis 78, konfigūracijos ID bus: WoodAAA78.

## <a name="nomenclature-of-dimension-based-configurations"></a>Konfigūravimo pagal dimensijas nomenklatūra
Atliekant konfigūravimą pagal dimensijas galima kurti specialią konfigūracijos produkto dimensijos nomenklatūrą. Puslapyje **Produkto nomenklatūra** galite pasirinkti toliau nurodytus segmentus.

-   Numeracijos reikšmė
-   Teksto konstanta
-   Konfigūracijos grupės prekė

Galima nurodyti konfigūracijos nomenklatūrą, skirtą komplektavimo specifikacijai (KS).

### <a name="example"></a>Pavyzdys

KS yra keturios KS eilutes, suskirstytos į dvi konfigūracijų grupes.

-   KS eilutė: M0007, standartinė spintelė
    -   Konfigūracijos grupė: spintelė
-   KS eilutė: M0008, aukštos kokybės spintelė
    -   Konfigūracijos grupė: spintelė
-   KS eilutė: M0021, priekinės grotelės iš audinio
    -   Konfigūracijos grupė: priekinės grotelės
-   KS eilutė: M0022, priekinės grotelės iš metalo
    -   Konfigūracijos grupė: priekinės grotelės

Galite kurti konfigūracijos nomenklatūrą, kurioje yra toliau nurodyti segmentai.

1.  Konfigūracijos grupė: spintelė
2.  Teksto konstanta: "&"
3.  Konfigūracijos grupė: priekinės grotelės

Šiuo atveju standartinės spintelės su priekinėmis grotelėmis iš audinio konfigūracijos ID bus: M0007&M0021.

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a>Produkto variantų ir konfigūracijų derinio nomenklatūra
Kai naudojate konfigūravimo pagal apribojimus arba konfigūravimo pagal dimensijas technologiją, norėdami konfigūruoti pagrindinio produkto variantus, į produkto variantų numerius gali būti įtraukta konfigūracijos dimensijos nomenklatūra. Norėdami konfigūruoti variantus, atlikite šiuos veiksmus.

1.  Puslapyje **Produkto nomenklatūra** nurodykite produkto variantų numerių nomenklatūrą, į kurią įtraukta konfigūracijos dimensija.
2.  Priskirkite nomenklatūrą produkto dimensijų grupei su konfigūracijos dimensija.
3.  Nurodykite komponentų arba KS konfigūracijos nomenklatūrą, kuri bus naudojama konfigūruojant produkto variantus.

Taip pat galite kurti produkto variantų pavadinimų nomenklatūras. Produkto variantų pavadinimus galima konfigūruoti ir įtraukti konfigūracijos ID arba pavadinimą.

### <a name="example-for-constraint-based-configurations"></a>Konfigūravimo pagal apribojimus pavyzdys

Šiame pavyzdyje galite naudoti produkto variantų numerių nomenklatūrą, kurią sudaro toliau nurodyti segmentai.

1.  Bendrojo produkto numeris
2.  Teksto konstanta: "\_"
3.  Konfigūravimas

Konfigūracijos nomenklatūrą sudaro toliau pateikti segmentai.

1.  Atributo reikšmė: medžiagos
2.  Teksto konstanta: "AAA"
3.  Atributo reikšmė: ilgis

Galite įvesti toliau nurodytas segmentų reikšmes.

-   Bendrojo produkto numeris = **M0099**
-   Medžiagos = **plastmasė**
-   Ilgis = **12**

Šiuo atveju produkto varianto numeris bus: M0099\_PlasticAAA12.

### <a name="example-for-dimension-based-configurations"></a>Konfigūravimo pagal dimensijas pavyzdys

Šiame pavyzdyje galite naudoti produkto variantų numerių nomenklatūrą, kurią sudaro toliau nurodyti segmentai.

1.  Bendrojo produkto numeris
2.  Teksto konstanta: "//"
3.  Konfigūravimas

Konfigūracijos nomenklatūrą sudaro toliau pateikti segmentai.

1.  Konfigūracijos grupė: spintelė
2.  Teksto konstanta: "&"
3.  Konfigūracijos grupė: priekinės grotelės

Galite įvesti toliau nurodytas segmentų reikšmes.

-   Bendrojo produkto numeris = **D0123**
-   Spintelė = **M0008**
-   Priekinės grotelės = **M0022**

Šiuo atveju produkto varianto numeris bus: D0123//M0008&M0022.

## <a name="numbering-conflicts"></a>Numeravimo nesuderinamumai
Kai kuriais atvejais naudojant nustatytą produkto variantų numerių nomenklatūrą nebus kuriami unikalūs produkto variantų numeriai. Pavyzdžiui, produkto variantų numeriai nebus unikalūs, jei viena aktyvi produkto dimensija nėra įtraukta į bendrojo produkto, kuriame naudojama apibrėžta variantų konfigūravimo technologija, nomenklatūrą. Konfliktų sprendimo būdas priklauso nuo konfigūracijos technologijos.

### <a name="predefined-variants"></a>Iš anksto apibrėžti variantai

Jei automatiškai arba neautomatiškai bandysite generuoti produkto variantus, kurių daugiau nei vienas turės tokį patį produkto varianto numerį, įvyks klaida. Norėdami to išvengti, turite naudoti visas aktyvias produkto dimensijų grupės produkto dimensijas. Taip pat galite įtraukti numeraciją ir taip užtikrinti, kad produkto varianto numeriai bus unikalūs.

### <a name="constraint-based-configurations"></a>Konfigūravimas pagal apribojimus

Priklausomai nuo nomenklatūros, sistema gali bandyti konfigūracijai priskirti ne unikalų produkto varianto numerį. Tokiu atveju sistema naudos konfigūracijos dimensijos numeraciją kaip produkto varianto numerį ir bus rodomas įspėjimas. Siekiant to išvengti, į nomenklatūrą turėtumėte įtraukti pakankamai atributų ir taip užtikrinti, kad produkto variantų numeriai bus unikalūs. Taip pat įsitikinkite, kad įjungta komponento parinktis **Naudoti pakartotinai**.

### <a name="dimension-based-configurations"></a>Konfigūravimas pagal dimensijas

Į konfigūravimo procesą įtrauktas etapas, kurio metu sistema pasiūlys konfigūracijos reikšmę pagal nomenklatūrą. Šio etapo metu galite neautomatiškai keisti konfigūracijos reikšmę. Kai įrašote konfigūraciją, sistema patikrins, ar konfigūracijos reikšmė yra unikali. Jei įvesta vertė nėra unikali, bus rodomas klaidos pranešimas. Turite įvesti unikalią konfigūracijos reikšmę, kad galėtumėte konfigūraciją įrašyti.

<a name="additional-resources"></a>Papildomi ištekliai
--------

[Iš anksto nustatytų produkto variantų produkto numerių nomenklatūros kūrimas](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[Sukonfigūruotų produkto variantų produkto numerių nomenklatūros kūrimas](tasks/create-product-number-nomenclature-product-variants_2016_11.md)


