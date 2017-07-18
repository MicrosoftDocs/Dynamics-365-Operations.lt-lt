---
title: "Produktų konfigūracijos modelių skaičiavimų DUK"
description: "Šiame straipsnyje aprašyti produktų konfigūracijos modelių skaičiavimai ir paaiškinta, kaip naudoti skaičiavimus kartu su apribojimais."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCConstraintEditor, PCProductConfigurationModelDetails, PCRuntimeConfigurator
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19191
ms.assetid: 8993f9a1-d1c0-49f5-afd3-5e1077ded0fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f13d03e5d1a26a5c87d71732b692537be94bdfb8
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017

---

# <a name="calculations-for-product-configuration-models-faq"></a>Produktų konfigūracijos modelių skaičiavimų DUK

[!include[banner](../includes/banner.md)]


Šiame straipsnyje aprašyti produktų konfigūracijos modelių skaičiavimai ir paaiškinta, kaip naudoti skaičiavimus kartu su apribojimais.

Skaičiavimus galima naudoti aritmetinėse ir loginėse operacijose. Jie papildo produkto konfigūravimo modelių išraiškos apribojimus. Puslapyje **Produkto konfigūravimo pagal apribojimus modelio informacija** galima nustatyti skaičiavimus ir tada išraiškų rengyklėje kurti skaičiavimų išraiškas. Daugiau informacijos žr. dalyje Kurti skaičiavimus.

## <a name="what-is-a-calculation"></a>Kas yra skaičiavimas?
Skaičiavimas – tai elementas, kurį galite naudoti produkto konfigūravimo modelyje. Skaičiavimai papildo apribojimus suteikdami galimybę apskaičiuoti reikšmes dešimtainiais skaičiais, kai konfigūruojate produktą. Be to, skaičiavimai turi didesnį operatorių rinkinį nei apribojimai.  

Kaip ir apribojimas, skaičiavimas yra susietas su konkrečiu komponentu produkto konfigūracijos modelyje, jo negalima naudoti pakartotinai arba bendrai su kitu komponentu. Vienas svarbus skirtumas tarp skaičiavimų ir apribojimų – skaičiavimai yra būtini (vienos krypties), o apribojimai yra deklaratyvūs (dviejų krypčių). Daugiau informacijos apie apribojimus žr. dalyje [Išraiškos apribojimai ir lentelių apribojimai](expression-constraints-table-constraints-product-configuration-models.md).  

Skaičiavimą sudaro tikslinis atributas ir skaičiavimo išraiška.

## <a name="what-is-a-target-attribute"></a>Kas yra tikslinis atributas?
Tikslinis atributas – atributas, gaunantis skaičiavimo išraiškos rezultatą.  

Toliau nurodytoje išraiškoje tikslinis atributas yra staltiesės matavimas:  

**Išraiška:** If\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]  

**DecimalAttribute1** yra stalo ilgis, o **decimalAttribute2** – staltiesės ilgis. Išraiška pateikia tikslinio atributo reikšmę **True**, jei **decimalAttribute2** yra didesnis nei arba lygus **decimalAttribute1**. Kitu atveju išraiška pateikia reikšmę **False**. Taigi staltiesės matavimas yra priimtinas, jei staltiesės ilgis yra lygus stalo ilgiui arba didesnis.

## <a name="what-attribute-types-can-be-set-to-target-attributes"></a>Kokius tikslinių atributų tipus galima nustatyti?
Galima nustatyti visus tikslinių atributų tipus, palaikomus produkto konfigūratoriuje, išskyrus tekstą be fiksuoto sąrašo.

## <a name="can-the-value-of-a-target-attribute-restrict-the-values-of-the-input-attributes-in-a-calculation"></a>Ar gali tikslinio atributo reikšmė riboti įvesties atributų reikšmes skaičiavime?
Ne, tikslinio atributo reikšmė negali riboti įvesties atributų reikšmių, nes skaičiavimai yra vienakrypčiai. Todėl tikslinio atributo reikšmė yra nustatoma pagal įvesties atributų reikšmių keitimus, tačiau tikslinio atributo reikšmės keitimai neturi įtakos įvesties atributų reikšmėms. Ši elgsena skiriasi nuo apribojimų elgsenos. Apribojimai taikomi abiem kryptimis.

### <a name="example"></a>Pavyzdys

Toliau nurodytoje išraiškoje skaičiavimo tikslas yra maitinimo laido ilgis, o įvesties reikšmė yra spalva.  

**Išraiška**: \[Jei Spalva == Žalia, 1,5, 1,0\]  

Konfigūruojant prekę, nustatomas **1,5** laido ilgis, jei nurodote **Žalia** kaip spalvos atributą. Jei nurodote bet kokią kitą spalvą, nustatomas ilgis yra **1,0**. Bet kadangi skaičiavimai yra vienakrypčiai, skaičiavimas nenustato spalvos atributo reikšmės kaip **Žalia**, jei nurodote ilgį **1,5**.

## <a name="what-happens-if-a-calculation-has-a-target-attribute-of-the-integer-type-but-a-calculation-generates-a-decimal-number"></a>Kas nutinka, jei skaičiavime tikslinis atributas yra sveikojo skaičiaus tipo, bet skaičiavimas generuoja dešimtainį skaičių?
Jei tikslinis atributas yra sveikojo skaičiaus tipo, bet skaičiavimas sugeneruoja dešimtainį skaičių, grąžinama tik sveikoji apskaičiuoto rezultato skaičiaus dalis. Dešimtainė dalis pašalinama, o rezultatas neapvalinamas. Pavyzdžiui, rezultatas 12,70 rodomas kaip 12.

## <a name="when-do-calculations-occur"></a>Kada atliekami skaičiavimai?
Skaičiavimai atliekami, kai nurodoma visų įvesties atributų reikšmė.

## <a name="can-i-overwrite-the-value-that-is-calculated-for-the-target-attribute"></a>Ar galiu perrašyti apskaičiuotą tikslinio atributo reikšmę?
Galite perrašyti apskaičiuotą tikslinio atributo reikšmę, nebent tikslinis atributas nustatytas kaip paslėptas arba tik skaitomas.

## <a name="how-do-i-set-a-target-attribute-as-hidden-or-readonly"></a>Kaip nustatyti tikslinį atributą kaip paslėptą arba tik skaitomą?
Norėdami nustatyti atributą kaip paslėptą arba tik skaitomą, atlikite šiuos veiksmus.

1.  Spustelėkite **Produkto informacijos valdymas** &gt; **Bendrasis** &gt; **Produkto konfigūracijos modeliai**.
2.  Pasirinkite produkto konfigūravimo modelį ir tada veiksmų srityje spustelėkite **Redaguoti**.
3.  Puslapyje **Produkto konfigūravimo pagal apribojimus modelio informacija** pasirinkite, kurį atributą norite naudoti kaip tikslinį atributą.
4.  „FastTab“ **Atributai** pasirinkite **Paslėpta** arba **Tik skaitoma**.

## <a name="can-a-calculation-overwrite-the-values-that-i-set"></a>Ar skaičiavimas gali perrašyti mano nustatytas reikšmes?
Nr. Naudojamos reikšmės, kurias nustatote konfigūruodami produktą. Skaičiavimas, atliekamas pakeitus įvesties reikšmes skaičiavime, negali perrašyti jūsų nurodytų konkretaus atributo reikšmių.

## <a name="what-happens-if-i-remove-an-input-value-in-a-calculation"></a>Kas nutinka skaičiavime pašalinus įvesties reikšmę?
Jei pašalinate įvesties reikšmę skaičiavime, pašalinama ir tikslinio atributo reikšmė.

## <a name="why-do-i-receive-an-error-message-that-says-that-my-model-is-in-contradiction"></a>Kodėl gaunu pranešimą apie klaidą, kuriame teigiama, kad modelis neatitinka?
Šis pranešimas rodomas, kai skaičiavime yra klaida arba viename ar keliuose apribojimuose yra prieštaravimas. Daugiau informacijos apie prieštaravimus apribojimuose žr. dalyje [Išraiškos apribojimai ir lentelių apribojimai](expression-constraints-table-constraints-product-configuration-models.md). Toliau pateikiami atvejai, kurias skaičiuojant gali įvykti klaidų.

-   Reikšmė dalijama iš 0 (nulio).
-   Yra konfliktas tarp dviejų toliau pateiktų elementų.
    -   Reikšmės, kurios prieinamos atributui ir kurios yra ribojamos apribojimo.
    -   Reikšmė, sugeneruota skaičiuojant.
-   Skaičiavimo pateiktos reikšmės nepatenka į atributo sritį. Pavyzdys yra sveikasis skaičius \[1..10\], kuris apskaičiuojamas kaip 0.

## <a name="why-do-i-receive-an-error-message-even-though-i-successfully-validated-my-product-model"></a>Kodėl gaunu klaidos pranešimą, net jei sėkmingai patikrinau savo produkto modelį?
Skaičiavimai neįtraukiami į tikrinimą. Norėdami rasti skaičiavimų klaidas, turite išbandyti produkto konfigūracijos modelį. Tolesniuose veiksmuose paaiškinta, kaip išbandyti produkto konfigūracijos modelį.

1.  Spustelėkite **Produkto informacijos valdymas** &gt; **Bendrasis** &gt; **Produkto konfigūracijos modeliai**.
2.  Pasirinkite produkto konfigūravimo modelį ir tada veiksmų srities grupėje **Vykdyti** spustelėkite **Tikrinti**.





