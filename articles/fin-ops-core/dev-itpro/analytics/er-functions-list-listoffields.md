---
title: ER LISTOFFIELDS funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama LISTOFFIELDS elektroninių ataskaitų (ER) funkcija.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: e795251004136469f64e8ebbb190a3bceaa382ed
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288175"
---
# <a name="listoffields-er-function"></a>ER LISTOFFIELDS funkcija

[!include [banner](../includes/banner.md)]

`LISTOFFIELDS` funkcija pateikia tipo *Įrašų sąrašas* reikšmę, sukurtą pagal nurodyto tipo *Išvardijimas* arba *Konteineris (įrašas)* argumento struktūrą.

## <a name="syntax-1"></a>1-oji sintaksė

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a>2-oji sintaksė

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a>Argumentai

`path`: Duomenų šaltinio nuroda

Tinkamas vieno iš tolesnių duomenų tipų duomenų šaltinio nuorodos kelias.

- Modelių išvardijimas
- Formatų išvardijimas
- Programų išvardijimas
- Konteineris (įrašas)

`language`: *Eilutė*

Tekstas, reiškiantis kalbos kodą.

## <a name="return-values"></a>Pateikiamos reikšmės

*Įrašų sąrašas*

Gautas įrašų sąrašas.

## <a name="usage-notes"></a>Naudojimo pastabos

Sukurtą sąrašą sudaro įrašai su tolesniais laukais.

- **Pavadinimas** (duomenų tipas *Eilutė*)
- **Žyma** (duomenų tipas *Eilutė*)
- **Aprašas** (duomenų tipas *Eilutė*)
- **IsTranslated** (duomenų tipas *Bulio logika*)

Jei `path` argumentas nurodo tipo *Konteineris (įrašas)* duomenų šaltinį, kiekviename nurodyto konteinerio įrašo lauke į sukurtą sąrašą įtraukiamas naujas įrašas. Kiekvieno sukurto įrašo laukas **Pavadinimas** pateikia nurodyto konteinerio įrašo, kuriam buvo sukurtas dabartinis įrašas, lauko pavadinimą.

Jei `path` argumentas nurodo vieno iš tipų *Išvardijimas* duomenų šaltinį, kiekvienos nurodyto išvardijimo reikšmės atveju į sukurtą sąrašą įtraukiamas naujas įrašas. Kiekvieno sukurto įrašo laukas **Pavadinimas** pateikia nurodyto išvardijimo, kuriam buvo sukurtas dabartinis įrašas, reikšmę, laukas **Aprašas** pateikia to išvardijimo aprašą, o laukas **Žyma** – to išvardijimo žymą.

Kai vykdant naudojama 1-oji sintaksė, laukuose **Žyma** ir **Aprašas** turi būti pateikiamos reikšmės, paremtos vykdomo modulio Elektroninės ataskaitų (ER) formato kalbos parametrais.

- Jei pageidaujamos kalbos žymos ir aprašai yra pasiekiami, laukuose **Žyma** ir **Aprašas** pateikiamos reikšmės, paremtos ta kalba, o lauke **IsTranslated** pateikiama **True**.
- Jei pageidaujamos kalbos žymos ir aprašai nėra pasiekiami, laukuose **Žyma** ir **Aprašas** pateikiamos reikšmės, paremtos numatytąja kalba **EN-US**, o lauke **IsTranslated** pateikiama **False**.

Kai vykdant naudojama 2-oji sintaksė, laukuose **Žyma** ir **Aprašas** turi būti pateikiamos reikšmės, paremtos kalba, kuri apibrėžta kaip antrasis iškviestos funkcijos argumentas.

- Jei pageidaujamos kalbos žymos ir aprašai yra pasiekiami, laukuose **Žyma** ir **Aprašas** pateikiamos reikšmės, paremtos ta kalba, o lauke **IsTranslated** pateikiama **True**.
- Jei pageidaujamos kalbos žymos ir aprašai nėra pasiekiami, laukuose **Žyma** ir **Aprašas** pateikiamos reikšmės, paremtos kalba **EN-US**, o lauke **IsTranslated** pateikiama **False**.

## <a name="example-1"></a>1 pavyzdys

Tolesnėje iliustracijoje ER duomenų modelyje įvestas išvardijimas.

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

Tolesnėje iliustracijoje parodyta tolesnė išsami informacija.

- Modelio išvardijimas įtrauktas į ataskaitą kaip duomenų šaltinis.
- ER reiškinyje modelio išvardijimas naudojamas kaip funkcijos `LISTOFFIELDS` parametras.
- Tipo *Įrašų sąrašas* duomenų šaltinis įterpiamas į ataskaitą naudojant sukurtą ER reiškinį.

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

Toliau pateiktame pavyzdyje parodyti ER formato elementai, susieti su tipo *Įrašų sąrašas* duomenų šaltiniu, kuris buvo sukurtas naudojant funkciją `LISTOFFIELDS`.

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

Tolesnėje iliustracijoje parodytas vaizdas, kai vykdomas sukurtas formatas.

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> Pagal pirminių formato elementų **FAILAS** ir **APLANKAS** kalbos parametrus išverstas žymų ir aprašų tekstas yra įvedamas į ER formato išeigą.

## <a name="example-2"></a>2 pavyzdys

Duomenų šaltinio tipas *Apskaičiuotasis laukas* naudojamas norint konfigūruoti **enumType** duomenų modelio išvardijimo duomenų šaltinius **enumType\_de** ir **enumType\_deCH**.

- **enumType\_de** = `LISTOFFIELDS (enumType, "de")`
- **enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`

Tokiu atveju naudodami tolesnį reiškinį galite gauti išvardijimo reikšmės žymą Šveicarijos vokiečių kalba (jei toks vertimas yra). Jei vertimas Šveicarijos vokiečių kalba nepateikiamas, žyma pateikiama vokiečių kalba.

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
