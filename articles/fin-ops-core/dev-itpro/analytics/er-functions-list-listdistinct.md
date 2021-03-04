---
title: LISTDISTINCT ER funkcija
description: Šioje temoje pateikta informacija apie tai, kaip yra naudojama LISTDISTINCT elektroninės ataskaitos funkcija.
author: NickSelin
manager: kfend
ms.date: 7/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 2333cfc21a16a5905acadd590982020fdf878330
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682272"
---
# <a name="listdistinct-er-function"></a>LISTDISTINCT ER funkcija

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

`LISTDISTINCT` funkcija apskaičiuota nurodytą išraišką, kaip selektorių kiekvienam nurodyto sąrašo įrašui. Jis grįžta į naują *Įrašo sąrašo* vertę, kuri turi vieną įrašą kiekvienai atskirai selektoriaus vertei.

## <a name="syntax"></a>Sintaksė

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a>Argumentai

`list`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

`selector`: *Pirminių duomenų tipas*

Galiojanti išraiška yra naudojama selektoriaus vertės apskaičiavimui kiekvienam sąraše nurodytam įrašui.

Toliau pateikti duomenys yra palaikomi šiam parametrui:

- Bulio logika
- Data
- DateTime
- Guid
- Sveikasis skaičius
- Int64
- Tikrasis
- Eilutė

## <a name="return-values"></a>Grįžties vertės

*Įrašų sąrašas*

Gautas įrašų sąrašas.

## <a name="usage-notes"></a>Naudojimo pastabos

Sąrašo struktūra yra sukuriama tiap, kad atitiktų sąraše nurodytą struktūrą.

Ta pati selektoriaus vertė gali būti apskaičiuojama keliems įrašams nurodytame sąraše. Tokiu atveju, įrašą atitinkančios sąraše sukurtos laukelio vertės atitinka pirmojo įrašo vertes nurodytas sąraše, kuriame yra apskaičiuota selektoriaus vertė.

Šios funkcijos vykdymas yra atliekamas bet kuriame [Elektroninių ataskaitų (ER)](general-electronic-reporting.md) duomenų *Įrašo sąrašo* tipo šaltinyje, kuris yra atmintyje.

**GROUPBY** duomenų šaltinis gali būti taip pat naudojamas siekiant sukurti įrašų sąrašą, kuriam selektorius apskaičiuota atskiras vertes. Nepaisant to, iš vykdymo ir atminties vartojimo perspektyvos, geriau naudoti `LISTDISTINCT` funkciją nei **GROUPBY** duomenų šaltinį, nes ši funkcija yra vykdoma atmintyje.

## <a name="example"></a>Pavyzdys

Toliau pateiktas pavyzdys rodo, kaip galite gauti unikalios kliento paskyros skaičių sąrašą, turintį mažiausiai vieną pardavimo sąskaitą ar projekto sąskaitą, išduotą per tam tikrą laikotarpį.

1. Įveskite **Prekybossąskaita** `Record list` tipo duomenų šaltinį, kuris atitinka **Klientosąskaitosdiena** programos lentelę ir filtruoja prekybos sąskaitas per tam tikrą laikotarpį.

    Šių duomenų šaltinio `InvoiceAccount` laukelis grąžina klientui išrašytus paskyros skaičius.

2. Įveskite **Projektosąskaitos** `Record list` tipo duomenų šaltinį, kuris atitinka **Projektosąskaitosdienos** programos lentelę ir filtruoja projekto sąskaitas per tam tikrą laikotarpį.

    Šių duomenų šaltinio `InvoiceAccount` laukelis grąžina klientui išrašytus paskyros skaičius.

3. Konfigūruokite **Visossąskaitos**`Calculated field` duomenų šaltinio tipą, kuriame yra išsireiškimas `LISTJOIN(SalesInvoice, ProjectInvoice)`.

    Šis duomenų šaltinis grąžina bendrą prekybos sąskaitų ir projekto sąskaitų sąrašą.

4. Konfigūruokite **Išrašytaklientui** `Record list` duomenų šaltinio tipą, kuriame yra išraiška `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.

    Šis duomenų šaltinis grąžina naują sąrašą, kuriame yra vienas įrašas kiekvienam atskiram klientui, gavusiam sąskaitą per nustatytą laikotarpį. Šio sąrašo `InvoiceAccount` laukelyje yra kliento paskyros numeris.

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]