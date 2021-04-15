---
title: GETENUMVALUEBYNAME ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama GETENUMVALUEBYNAME elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72b5831e3d2bc2e839b0a569fb314a8ec074a5a1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746416"
---
# <a name="getenumvaluebyname-er-function"></a>GETENUMVALUEBYNAME ER funkcija

[!include [banner](../includes/banner.md)]

`GETENUMVALUEBYNAME`funkcija ieško nurodytame išvardijimo duomenų šaltinyje konkrečios *Enum* reikšmės, naudodama išvardijimo pavadinimą, kuris nurodytas kaip *Eilutės* reikšmė. Jei *Enum* reikšmė randama, funkcija ją pateikia. Priešingu atveju funkcija grąžina **null** išvardijimo reikšmę.

## <a name="syntax"></a>Sintaksė

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>Argumentai

`enumeration data source path`: *Išvardijimas*

Tinkamas vieno iš tolesnių išvardijimo tipų duomenų šaltinio maršrutas:

- Elektroninių ataskaitų (ER) modelių išvardijimas
- ER formatų išvardijimas
- „Microsoft Dynamics 365 Finance“ išvardijimas

`enumeration value text`: *Eilutė*

Eilutės reikšmė, nurodanti vienos išvardijimo reikšmės pavadinimą.

## <a name="return-values"></a>Grįžimo vertės

*Išvard.* leidžiama reikšmė NULL

Gaunama išvardijimo reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Nėra pateikiama jokia išimtis, jei reikšmė *Enum* nerasta naudojant išvardijimo reikšmę, nurodytą kaip *Eilutės* reikšmė.

## <a name="example-1"></a>1 pavyzdys

Tolesnėje iliustracijoje duomenų modelyje įvestas išvardijimas **ReportDirection**. Atkreipkite dėmesį, kad išvardijimo reikšmėms nurodytos žymos.

![Galimos duomenų modelio išvardijimo vertės](./media/ER-data-model-enumeration-values.PNG)

Tolesnėje iliustracijoje parodyta tolesnė išsami informacija.

- Duomenų šaltinis **$Direction** sukonfigūruotas ER ataskaitoje. Šis duomenų šaltinis yra sukonfigūruotas pagal modelių išvardijimą **ReportDirection**.
- Išraiška `$IsArrivals` sukurta naudoti modelių išvardijime veikiantį duomenų šaltinį **$Direction** kaip šios funkcijos parametrą.
- Šios lyginamosios išraiškos reikšmė yra **TEISINGA**.

![Duomenų modelio išvardijimo pavyzdys](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a>2 pavyzdys

`GETENUMVALUEBYNAME` ir [`LISTOFFIELDS`](er-functions-list-listoffields.md) funkcijos leidžia kaip teksto vertes iškviesti vertes ir palaikomų išvardijimų žymes. (Palaikomi išvardijimai yra prašymų išvardijimai, duomenų modelio išvardijimai ir formato išvardijimai.)

Tolesnėje iliustracijoje **TransType** duomenų šaltinis pristatytas duomenų modelio susiejime. Šis duomenų šaltinis nurodo **LedgerTransType** prašymo išvardijimą.

![Duomenų modelio susiejimo, kuris nurodo prašymo išvardijimą, duomenų šaltinis](./media/er-functions-text-getenumvaluebyname-example2-1.png)

Tolesnė iliustracija rodo **TransTypeList** duomenų šaltinį, konfigūruotą duomenų modelio susiejime. Šis duomenų šaltinis yra sukonfigūruotas pagal **TransType** prašymo išvardijimą. `LISTOFFIELDS` funkcija naudojama norint grąžinti visas išvardijimo vertes kaip įrašų, kuriuose yra laukų, sąrašą. Tokiu būdu informacija apie kiekvieną išvardijimo vertę yra rodoma.

> [!NOTE]
> Laukas **EnumValue** yra sukonfigūruotas **TransTypeList** duomenų šaltiniui, naudojant `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` išraišką. Šis laukas grąžina kiekvieno šio sąrašo įrašo išvardijimo vertę.

![Duomenų modelio išdėstymo duomenų šaltinis, kuris grąžina visas pasirinkto išvardijimo vertes kaip įrašų sąrašą](./media/er-functions-text-getenumvaluebyname-example2-2.png)

Tolesnė iliustracija rodo **VendTrans** duomenų šaltinį, konfigūruotą duomenų modelio susiejime. Šis duomenų šaltinis grąžina tiekėjo operacijų įrašus iš **VendTrans** programos lentelės. Kiekvienos operacijos didžiosios knygos tipas apibrėžiamas **TransType** lauko verte.

> [!NOTE]
> Laukas **TransTypeTitle** yra sukonfigūruotas **VendTrans** duomenų šaltiniui, naudojant `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` išraišką. Šis laukas grąžina esamos operacijos, kaip teksto, išvardijimo vertės žymę, jei ši išvardijimo vertė yra galima. Kitu atveju, jis pateikia tuščią eilutės vertę.
>
> Laukas **TransTypeTitle** yra susietas su duomenų modelio, kuris įgalina šią informaciją naudoti kiekvienu ER formatu, kuris naudoja duomenų modelį kaip duomenų šaltinį, **LedgerType** lauku.

![Duomenų modelio susiejimo, kuris grąžina tiekėjo operacijas, duomenų šaltinis](./media/er-functions-text-getenumvaluebyname-example2-3.png)

Toliau pateiktoje iliustracijoje parodyta, kaip galite naudoti [duomenų šaltinio derintuvę](er-debug-data-sources.md), kad galėtumėte patikrinti sukonfigūruotą duomenų modelio susiejimą.

![Duomenų šaltinio derintuvės naudojimas, norint patikrinti sukonfigūruotą duomenų modelio susiejimą](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

**LedgerType** duomenų modelio laukas rodo operacijų tipų žymas numatytu būdu.

Jei planuojate naudoti šį metodą dideliam operacijų duomenų kiekiui, turite apsvarstyti vykdymo efektyvumą. Daugiau informacijos, žr. [ER formatų vykdymo sekimas, siekiant pašalinti našumo problemas](trace-execution-er-troubleshoot-perf.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)

[ER formatų vykdymo sekimas siekiant diagnozuoti našumo problemas](trace-execution-er-troubleshoot-perf.md)

[ER LISTOFFIELDS funkcija](er-functions-list-listoffields.md)

[ER FIRSTORNULL funkcija](er-functions-list-firstornull.md)

[WHERE ER funkcija](er-functions-list-where.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]