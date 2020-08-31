---
title: Sąrašo kategorijos ER funkcijų sąrašas
description: Šioje temoje pateikiama informacijos apie sąrašo funkcijas, palaikomas modulyje Elektroninės ataskaitos (ER).
author: NickSelin
manager: kfend
ms.date: 04/01/2020
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
ms.openlocfilehash: 6e51d9a1d68c48391a223fe48f396c63c206580e
ms.sourcegitcommit: 41e165482b9bff4175c0e3b224dbeead13461956
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/11/2020
ms.locfileid: "3687963"
---
# <a name="list-of-er-functions-in-the-list-category"></a>Sąrašo kategorijos ER funkcijų sąrašas

[!include [banner](../includes/banner.md)]

Naudojant modulio Elektroninės ataskaitos (ER) sąrašo funkcijas, galima išgauti informaciją iš duomenų tipų *Įrašų sąrašas* ir *Konteineris (įrašas)* duomenų šaltinių bei su jais atlikti operacijas. Šioje temoje pateikiama šių funkcijų suvestinė.

## <a name="list-of-supported-functions"></a>Palaikomų funkcijų sąrašas

| Funkcija | Aprašymas |
|----------|-------------|
| [AllItems](er-functions-list-allitems.md)                 | Ši funkcija veikia kaip atminties pasirinkimas. Ji pateikia naują plokščia padarytą tipo *Įrašų sąrašas* reikšmę, sudarytą iš įrašų sąrašo, kuriame nurodomi visi elementai, atitinkantys nurodytą kelią. |
| [AllItemsQuery](er-functions-list-allitemsquery.md)       | Ši funkcija veikia kaip sujungta SQL užklausa. Ji pateikia naują plokščia padarytą tipo *Įrašų sąrašas* reikšmę, sudarytą iš įrašų sąrašo, kuriame nurodomi visi elementai, atitinkantys nurodytą kelią. |
| [Eil. Nr.](er-functions-list-count.md)                       | Ši funkcija pateikia tipo *Sveikasis skaičius* reikšmę, nurodančią konkretaus sąrašo įrašų skaičių (jei sąrašas nėra tuščias). Jei sąrašas tuščias, ši funkcija pateikia **0** (nulį). |
| [EmptyList](er-functions-list-emptylist.md)               | Ši funkcija pateikia tuščią tipo *Įrašų sąrašas* reikšmę, kaip sąrašo struktūros šaltinį naudodama nurodytą sąrašą.|
| [Išvardyti](er-functions-list-enumerate.md)               | Ši funkcija pateikia naują tipo *Įrašų sąrašas* reikšmę, sudarytą iš išvardytų nurodyto sąrašo įrašų. |
| [Filtruoti](er-functions-list-filter.md)                     | Ši funkcija pateikia nurodytą sąrašą kaip tipo *Įrašų sąrašas* reikšmę, užklausą pakeitus taip, kad ji taikytų nurodytos sąlygos filtrą. |
| [Pirmas](er-functions-list-first.md)                       | Ši funkcija pirmąjį nurodyto sąrašo įrašą pateikia kaip tipo *Konteineris (įrašas)* reikšmę (jei tas sąrašas nėra tuščias). Jei sąrašas tuščias, ši funkcija pateikia išimtį. |
| [FirstOrNull](er-functions-list-firstornull.md)           | Ši funkcija pirmąjį nurodyto sąrašo įrašą pateikia kaip tipo *Konteineris (įrašas)* reikšmę (jei tas įrašas nėra tuščias). Jei įrašas tuščias, ši funkcija pateikia neapibrėžtą tipo *Konteineris (įrašas)* reikšmę. |
| [Index](er-functions-list-index.md)                       | Ši funkcija pateikia tipo *Konteineris (įrašas)* reikšmę, kuri pasirenkama naudojant konkretų nurodyto sąrašo skaitinį indeksą. Jei indekse nėra nurodyto sąrašo įrašų intervalo, ši funkcija pateikia išimtį. |
| [IsEmpty](er-functions-list-isempty.md)                   | Jei nurodytame sąraše nėra įrašų, ši funkcija pateikia *Bulio logikos* reikšmę **TRUE**. Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**. |
| [Sąrašas](er-functions-list-list.md)                         | Ši funkcija pateikia tipo *Įrašų sąrašas* reikšmę, sudarytą iš naujo sąrašo, sukurto iš nurodytų argumentų.|
| [Sąrašoatskiras](er-functions-list-listdistinct.md)         | Ši funkcija apskaičiuota nurodytą išraišką, kaip selektorių kiekvienam nurodyto sąrašo įrašui. Jis grįžta į naują *Įrašo sąrašo* vertę, kuri turi vieną įrašą kiekvienai atskirai selektoriaus vertei.|
| [ListJoin](er-functions-list-listjoin.md)                 | Ši funkcija pateikia tipo *Įrašų sąrašas* reikšmę, nurodančią naują jungtinį sąrašą, sukurtą iš nurodytų argumentų.|
| [ListOfFields](er-functions-list-listoffields.md)         | Ši funkcija pateikia tipo *Įrašų sąrašas* reikšmę, sukurtą pagal nurodyto tipo *Išvardijimas* arba *Konteineris (įrašas)* argumento struktūrą. |
| [ListOfFirstItem](er-functions-list-listoffirstitem.md)   | Ši funkcija pateikia tipo *Įrašų sąrašas* reikšmę, kurią sudaro tik pirmasis nurodyto sąrašo įrašas.|
| [OrderBy](er-functions-list-orderby.md)                   | Ši funkcija nurodytą sąrašą pateikia kaip tipo *Įrašų sąrašas* reikšmę, jį surikiavus pagal nurodytus argumentus. Šiuos argumentus galima apibrėžti kaip išraiškas. |
| [Atvirkštinis](er-functions-list-reverse.md)                   | Ši funkcija nurodytą sąrašą pateikia kaip tipo *Įrašų sąrašas* reikšmę, surikiuotą atvirkštine tvarka. |
| [Skaidyti](er-functions-list-split.md)                       | Ši funkcija nurodytą įvesties eilutę išskaido į antrines eilutes ir rezultatą pateikia kaip naują tipo *Įrašų sąrašas* reikšmę. |
| [SplitList](er-functions-list-splitlist.md)               | Ši funkcija nurodytą sąrašą išskaido į antrinius sąrašus (arba į paketus), iš kurių kiekviename būtų nurodytas įrašų skaičius. Tada grąžinamas rezultatas kaip nauja *Įrašų sąrašo* reikšmė, kurią sudaro paketai. |
| [SplitListByLimit](er-functions-list-splitlistbylimit.md) | Ši funkcija nurodytą sąrašą išskaido į naują antrinių sąrašų (paketų) sąrašą. Kiekvieno paketo įrašų skaičius yra dinamiškai apskaičiuojamas. Tada funkcija grąžina rezultatą kaip naują *Įrašų sąrašo* reikšmę, kurią sudaro paketai. |
| [StringJoin](er-functions-list-stringjoin.md)             | Ši funkcija pateikia tipo *Eilutė* reikšmę, kurią sudaro sujungtos nurodyto lauko, esančio nurodytame sąraše, reikšmės. Reikšmes galima skirti nurodytu skyrikliu. |
| [Kur](er-functions-list-where.md)                       | Ši funkcija nurodytą sąrašą pateikia kaip tipo *Įrašų sąrašas* reikšmę, jam pritaikius filtrą pagal nurodytą sąlygą. |

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)

[Elektroninių ataskaitų formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)

[Elektroninių ataskaitų formulių kalba](er-formula-language.md)
