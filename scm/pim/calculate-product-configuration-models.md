---
title: "Skaičiavimus už produkto konfigūracijos modelius DUK"
description: "Šiame straipsnyje aprašoma skaičiavimai produkto konfigūracijos modelius ir aiškinama, kaip naudoti skaičiavimus bei suvaržymus."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCConstraintEditor, PCProductConfigurationModelDetails, PCRuntimeConfigurator
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19191
ms.assetid: 8993f9a1-d1c0-49f5-afd3-5e1077ded0fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3d02a15387231160f5b8a237aa11008b91ef1223
ms.openlocfilehash: 3a82fdb8532c79e33c167c43554a3de7d3061fcb
ms.lasthandoff: 03/31/2017


---

# <a name="calculations-for-product-configuration-models-faq"></a>Skaičiavimus už produkto konfigūracijos modelius DUK

Šiame straipsnyje aprašoma skaičiavimai produkto konfigūracijos modelius ir aiškinama, kaip naudoti skaičiavimus bei suvaržymus.

Skaičiavimus galima naudoti aritmetinėse ir loginėse operacijose. Jie papildo produkto konfigūravimo modelių išraiškos apribojimus. Puslapyje **Produkto konfigūravimo pagal apribojimus modelio informacija** galima nustatyti skaičiavimus ir tada išraiškų rengyklėje kurti skaičiavimų išraiškas. Daugiau informacijos žr. dalyje Kurti skaičiavimus.

## <a name="what-is-a-calculation"></a>Kas yra skaičiavimas?
Skaičiavimas – tai elementas, kurį galite naudoti produkto konfigūravimo modelyje. Skaičiavimai papildo apribojimus suteikdami galimybę apskaičiuoti reikšmes dešimtainiais skaičiais, kai konfigūruojate produktą. Be to, skaičiavimai turi didesnį operatorių rinkinį nei apribojimai.  

Kaip ir apribojimas, skaičiavimas yra susietas su konkrečiu komponentu produkto konfigūracijos modelyje, jo negalima naudoti pakartotinai arba bendrai su kitu komponentu. Vienas svarbus skirtumas tarp skaičiavimų ir apribojimų – skaičiavimai yra būtini (vienos krypties), o apribojimai yra deklaratyvūs (dviejų krypčių). Daugiau informacijos apie apribojimus žr. dalyje [Išraiškos apribojimai ir lentelių apribojimai](expression-constraints-table-constraints-product-configuration-models.md).  

Skaičiavimą sudaro tikslinis atributas ir skaičiavimo išraiška.

## <a name="what-is-a-target-attribute"></a>Kas yra tikslinis atributas?
Tikslinis atributas – atributas, gaunantis skaičiavimo išraiškos rezultatą.  

Toliau nurodytoje išraiškoje tikslinis atributas yra staltiesės matavimas:  

**Išraiška:** jei\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]  

**DecimalAttribute1** – stalo ilgis, ir **decimalAttribute2** staltiesė ilgis. Išraiška pateikia tikslinio atributo reikšmę **True**, jei **decimalAttribute2** yra didesnis nei arba lygus **decimalAttribute1**. Kitu atveju išraiška pateikia reikšmę **False**. Taigi staltiesės matavimas yra priimtinas, jei staltiesės ilgis yra lygus stalo ilgiui arba didesnis.

## <a name="what-attribute-types-can-be-set-to-target-attributes"></a>Kokius tikslinių atributų tipus galima nustatyti?
Galima nustatyti visus tikslinių atributų tipus, palaikomus produkto konfigūratoriuje, išskyrus tekstą be fiksuoto sąrašo.

## <a name="can-the-value-of-a-target-attribute-restrict-the-values-of-the-input-attributes-in-a-calculation"></a>Ar gali tikslinio atributo reikšmė riboti įvesties atributų reikšmes skaičiavime?
Ne, tikslinio atributo reikšmė negali riboti įvesties atributų reikšmių, nes skaičiavimai yra vienakrypčiai. Todėl tikslinio atributo reikšmė yra nustatoma pagal įvesties atributų reikšmių keitimus, tačiau tikslinio atributo reikšmės keitimai neturi įtakos įvesties atributų reikšmėms. Ši elgsena skiriasi nuo apribojimų elgsenos. Apribojimai taikomi abiem kryptimis.

### <a name="example"></a>Pavyzdys

Šią išraišką, skaičiavimo tikslas maitinimo laido ilgis ir įvesties reikšmė yra spalvą:  

**Išraiška:**\[jei spalva == "Žalia", 1.5, 1,0\]  

Konfigūruojant prekę, yra lygi maitinimo laido ilgis **1.5** jei nurodysite **žalia** kaip spalvos atributo. Jei nurodote bet kokią kitą spalvą, nustatomas ilgis yra **1,0**. Bet kadangi skaičiavimai yra vienakrypčiai, skaičiavimas nenustato spalvos atributo reikšmės kaip **Žalia**, jei nurodote ilgį **1,5**.

## <a name="what-happens-if-a-calculation-has-a-target-attribute-of-the-integer-type-but-a-calculation-generates-a-decimal-number"></a>Kas nutinka, jei skaičiavime tikslinis atributas yra sveikojo skaičiaus tipo, bet skaičiavimas generuoja dešimtainį skaičių?
Jei tikslinis atributas yra sveikojo skaičiaus tipo, bet skaičiavimas sugeneruoja dešimtainį skaičių, grąžinama tik sveikoji apskaičiuoto rezultato skaičiaus dalis. Dešimtainė dalis pašalinama, o rezultatas neapvalinamas. Pavyzdžiui, rezultatas 12,70 rodomas kaip 12.

## <a name="when-do-calculations-occur"></a>Kada atliekami skaičiavimai?
Skaičiavimai atliekami, kai nurodoma visų įvesties atributų reikšmė.

## <a name="can-i-overwrite-the-value-that-is-calculated-for-the-target-attribute"></a>Ar galiu perrašyti apskaičiuotą tikslinio atributo reikšmę?
Galite perrašyti apskaičiuotą tikslinio atributo reikšmę, nebent tikslinis atributas nustatytas kaip paslėptas arba tik skaitomas.

## <a name="how-do-i-set-a-target-attribute-as-hidden-or-readonly"></a>Kaip nustatyti kaip paslėptas atributas target arba tik skaitomas?
Norėdami nustatyti atributą kaip paslėptą arba tik skaitomą, atlikite šiuos veiksmus.

1.  Spustelėkite **produkto informacijos valdymo**&gt;**bendras**&gt;**produkto konfigūracijos modelius**.
2.  Pasirinkite produkto konfigūravimo modelį ir tada veiksmų srityje spustelėkite **Redaguoti**.
3.  Puslapyje **Produkto konfigūravimo pagal apribojimus modelio informacija** pasirinkite, kurį atributą norite naudoti kaip tikslinį atributą.
4.  „FastTab“ **Atributai** pasirinkite **Paslėpta** arba **Tik skaitoma**.

## <a name="can-a-calculation-overwrite-the-values-that-i-set"></a>Ar skaičiavimas gali perrašyti mano nustatytas reikšmes?
Nr. Reikšmės, kurį nustatėte konfigūruodami produktas yra naudojamos reikšmės. Skaičiavimas, atliekamas pakeitus įvesties reikšmes skaičiavime, negali perrašyti jūsų nurodytų konkretaus atributo reikšmių.

## <a name="what-happens-if-i-remove-an-input-value-in-a-calculation"></a>Kas nutinka skaičiavime pašalinus įvesties reikšmę?
Jei pašalinate įvesties reikšmę skaičiavime, pašalinama ir tikslinio atributo reikšmė.

## <a name="why-do-i-receive-an-error-message-that-says-that-my-model-is-in-contradiction"></a>Kodėl gaunu pranešimą apie klaidą, kuriame teigiama, kad modelis neatitinka?
Šis pranešimas rodomas, kai skaičiavime yra klaida arba viename ar keliuose apribojimuose yra prieštaravimas. Daugiau informacijos apie prieštaravimus apribojimuose žr. dalyje [Išraiškos apribojimai ir lentelių apribojimai](expression-constraints-table-constraints-product-configuration-models.md). Toliau pateikiami atvejai, kurias skaičiuojant gali įvykti klaidų.

-   Reikšmė dalijama iš 0 (nulio).
-   Yra konfliktas tarp dviejų toliau pateiktų elementų.
    -   Reikšmės, kurios prieinamos atributui ir kurios yra ribojamos apribojimo.
    -   Reikšmė, sugeneruota skaičiuojant.
-   Skaičiavimo pateiktos reikšmės nepatenka į atributo sritį. Pavyzdys yra sveikasis skaičius nuo \[1..10\], yra apskaičiuota, kad 0.

## <a name="why-do-i-receive-an-error-message-even-though-i-successfully-validated-my-product-model"></a>Kodėl gaunu klaidos pranešimą, net jei sėkmingai patikrinau savo produkto modelį?
Skaičiavimai neįtraukiami į tikrinimą. Norėdami rasti skaičiavimų klaidas, turite išbandyti produkto konfigūracijos modelį. Tolesniuose veiksmuose paaiškinta, kaip išbandyti produkto konfigūracijos modelį.

1.  Spustelėkite **produkto informacijos valdymo**&gt;**bendras**&gt;**produkto konfigūracijos modelius**.
2.  Pasirinkite produkto konfigūravimo modelį ir tada veiksmų srities grupėje **Vykdyti** spustelėkite **Tikrinti**.



