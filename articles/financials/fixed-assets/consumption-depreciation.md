---
title: Produkcijos metodas
description: "Šiame straipsnyje apžvelgtas nusidėvėjimo Naudojimo metodas."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a8afea937087ac046f9933eb0ccedf4854515d9f
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="consumption-depreciation"></a>Produkcijos metodas

[!include[banner](../includes/banner.md)]


Šiame straipsnyje apžvelgtas nusidėvėjimo Naudojimo metodas.

Jei nustatote ilgalaikio turto nusidėvėjimo profilį ir **Nusidėvėjimo profilių** puslapio lauke **Metodas** pasirenkate **Naudojimas**, ilgalaikis turtas nusidėvėjimo profiliui priskiriamas pagal jo naudojimą. **Nusidėvėjimo profilių** puslapyje procentų ir intervalų nustatyti nereikia. Kai sukuriate nusidėvėjimo profilį, kuris naudoja Naudojimo metodą, metodą nustatyti galite įvairiais būdais.

## <a name="set-up-and-use-consumption-depreciation"></a>Nustatyti ir naudoti nusidėvėjimą pagal naudojimą
1.  **Nusidėvėjimo profilių** puslapyje sukurkite nusidėvėjimo profilį. Skaičiuojant suvartojimą, nusidėvėjimo profilis turi turėti ID ir pavadinimą, o **Metodo** lauke reikia pasirinkti **Naudojimas**.
2.  **Naudojimo koeficientų** puslapyje nustatykite naudojimo koeficientus. Kiekvienas naudojimo koeficientas turi turėti ID ir pavadinimą bei naudojimo koeficientą, nurodytą kaip kiekį arba procentą.
3.  **Naudojimo vienetų** puslapyje nustatykite naudojimo vienetus. Kiekvienas naudojimo vienetas turi turėti ID ir pavadinimą. Nusidėvėjimo vienetai naudojami skaičiuojant nusidėvėjimą pagal naudojimą **Nusidėvėjimo pagal naudojimą** puslapyje. Vienetų pavyzdžiai: kilometras (km), kilogramas (kg) ir valanda.
4.  **Ilgalaikio turto** puslapyje nustatykite atskirą ilgalaikį turtą. Kiekvienam ilgalaikiam turtui parinkite vertinimo modelius ir nusidėvėjimo knygas, turinčius nusidėvėjimo profilius. Jei bet kuris jūsų ilgalaikis turtas naudoja nusidėvėjimo profilius, paremtus Naudojimo metodu, turite nustatyti nusidėvėjimo pagal naudojimą vertinimo modelius ar nusidėvėjimo knygas. Ši sąranka atliekama arba **Vertinimo modelių** puslapio skirtuke **Nusidėvėjimas**, arba **Nusidėvėjimo profilio** puslapio „FastTab‟**Bendra**. Tą patį vertinimo modelį galite naudoti keliems ilgalaikio turto objektams. Nusidėvėjimo šablonai yra ilgalaikiam turtui parinkto vertinimo modelio arba nusidėvėjimo knygos dalis. Tiesiogiai **Ilgalaikio turto** puslapyje pridėti ar modifikuoti nusidėvėjimo profilių negalima. Modifikuoti nusidėvėjimo profilius galite tik **Nusidėvėjimo knygų** puslapyje.
5.  **Vertinimo modelių** puslapyje arba **Nusidėvėjimo knygų** puslapyje, **Nusidėvėjimo pagal naudojimą** laukų grupėje įveskite informaciją į toliau nurodytus laukus.
    -   Naudojimo koeficientas
    -   Vienetas
    -   Nusidėvėjimo vienetai
    -   Įvertintas suvartojimas

    Lauke **Užregistruotas naudojimas** rodomas nusidėvėjimas pagal naudojimą, išreikštas vienetais ir užregistruotas ilgalaikio turto ir vertinimo modelio derinyje arba nusidėvėjimo knygoje. Šio lauko reikšmės rankiniu būdu atnaujinti negalite.

## <a name="examples"></a>Pavyzdžiai
### <a name="example-1"></a>1 pavyzdys

Šis naudojimo koeficientas nustatytas sausio 31 d.:

-   Kiekis yra 1 000.
-   Nurodyta ilgalaikio turto vieneto nusidėvėjimo kaina yra 1,5.

Sausio 31 d. nusidėvėjimo pasiūlymas yra toks: Kiekis x Vieneto nusidėvėjimas 1 000 x 1,5 = 1 500 Jei nurodytas ilgalaikio turto koeficientas yra procento koeficientas, ilgalaikio turto vertinimo modelio kiekis, įvertintas **Įvertinto naudojimo** lauke, yra padauginamas iš nustatyto pasirinktos pabaigos datos procento. Gautas kiekis tada yra siūlomas kaip laikotarpio nusidėvėjimo kiekis.

### <a name="example-2"></a>2 pavyzdys

Šis nusidėvėjimo pagal suvartojimą koeficientas nustatytas sausio 31 d.:

-   Procentinė dalis yra 10 procentų.
-   Nurodyta ilgalaikio turto vieneto nusidėvėjimo kaina yra 1,5.
-   Įvertintas ilgalaikio turto kiekis yra 2 000.

Sausio 31 d. nusidėvėjimo pasiūlymas yra toks: Įvertintas kiekis x Procentas x Vieneto nusidėvėjimas 2 000 x 0,10 x 1,5 = 300




