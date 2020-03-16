---
title: ER ENUMERATE funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) ENUMERATE funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d34904571ee6de8b36a0840a9470f16858489163
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042149"
---
# <a name="ENUMERATE">ER ENUMERATE funkcija</a>

[!include [banner](../includes/banner.md)]

`ENUMERATE` funkcija pateikia naują tipo *Įrašų sąrašas* reikšmę, sudarytą iš išvardytų nurodyto sąrašo įrašų.

## <a name="syntax"></a>Sintaksė

```vb
ENUMERATE (list)
```

## <a name="arguments"></a>Argumentai

`list`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

## <a name="return-values"></a>Pateikiamos reikšmės

*Įrašų sąrašas*

Gautas įrašų sąrašas.

## <a name="usage-notes"></a>Naudojimo pastabos

Pateiktame išvardytų įrašų sąraše rodomi tolesni papildomi elementai.

- Laukų įrašas (komponentas **Reikšmė**)
- dabartinio įrašo indeksą (**Numerio**komponentas).

## <a name="example"></a>Pavyzdys

Tolesnėje iliustracijoje duomenų šaltinis **Išvardytas** sukurtas kaip išvardytas tiekėjo įrašų sąrašas iš duomenų šaltinio **Tiekėjai**, kuris nurodo lentelę VendTable.

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

Tolesnėje iliustracijoje parodytas modulio Elektroninės ataskaitos (ER) formatas. Šiame formate sukuriami duomenų susiejimai, siekiant generuoti išeigą XML formatu. Ši išeiga atskirus tiekėjus pateikia kaip išvardytus mazgus.

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

Tolesnėje iliustracijoje parodytas vaizdas, kai vykdomas sukurtas formatas.

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)
